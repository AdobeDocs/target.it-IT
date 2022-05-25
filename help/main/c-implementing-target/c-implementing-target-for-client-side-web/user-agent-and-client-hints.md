---
keywords: at.js;agente utente del browser;agente utente;suggerimenti client;agente utente
description: Scopri come [!DNL Adobe Target] utilizza l’agente utente e i suggerimenti client per qualificare i visitatori per la segmentazione e la personalizzazione.
title: User Agent e suggerimenti client
feature: at.js
role: Developer
exl-id: 22d29bfe-e022-44b2-913f-c8c32c65bc48
source-git-commit: c351044163a6fb32ca72fa015724d3b0388c059a
workflow-type: tm+mt
source-wordcount: '1332'
ht-degree: 3%

---

# User-agent e Client Hint

[!DNL Adobe Target] utilizza l’agente utente per qualificare i visitatori per la segmentazione e la personalizzazione.

>[!NOTE]
>
>Le informazioni contenute in questo articolo si applicano a [at.js versione 2.9.0](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) (o successiva).


Ogni volta che un browser Web effettua una richiesta a un server, incluso nell’intestazione della richiesta, sono presenti informazioni sul browser e sull’ambiente in cui viene eseguito il browser. Fin dai primi giorni di Internet, questi dati sono stati aggregati in una singola stringa denominata user-agent.

Il testo seguente è un esempio di agente utente di un computer basato su Mac OS X che utilizza un browser Safari:

```
Mozilla/5.0 (Linux; Android 12; SM-S908E) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/101.0.4951.41 Mobile Safari/537.36 
```

Da questo agente utente, il server che riceve la richiesta può discernere le seguenti informazioni sul browser e sul sistema operativo:

| Informazioni | Dettagli |
| --- | --- |
| Nome software | Chrome |
| Versione software | 101 |
| Versione software completa | 101.0.4951.41 |
| Nome del motore di layout | AppleWebKit |
| Versione del motore di layout | 537,36 |
| Sistema operativo | Android |
| Versione del sistema operativo | Android 12 (Cono neve) |
| Dispositivo | SM-S908E (Ultra Samsung Galaxy S22) |

Nel corso degli anni, la quantità di informazioni sul browser e sul dispositivo incluse nella stringa agente utente è aumentata.

## Casi d’uso dell’agente utente

Gli agenti utente sono stati a lungo utilizzati per fornire ai team di marketing e sviluppatori informazioni importanti su come browser e sistemi operativi. e i dispositivi visualizzano il contenuto del sito e il modo in cui gli utenti interagiscono con i siti web. Gli agenti utente vengono inoltre utilizzati per bloccare spam e filtrare bot che esaminano i siti per diversi scopi aggiuntivi.

Tuttavia, negli ultimi anni alcuni proprietari di siti e fornitori di marketing hanno utilizzato l&#39;agente utente insieme ad altre informazioni incluse nelle intestazioni della richiesta per creare impronte digitali che possono essere utilizzate come mezzo per identificare gli utenti senza esserne a conoscenza. Nonostante lo scopo importante che l’agente utente svolge per i proprietari del sito, gli sviluppatori del browser hanno deciso di apportare modifiche al modo in cui gli agenti utente operano per limitare potenziali problemi di privacy per i visitatori del sito.

User-Agent Client Hint è la soluzione sviluppata dagli sviluppatori del browser. I suggerimenti client consentono ancora ai siti di raccogliere le informazioni necessarie sul browser, il sistema operativo e il dispositivo, fornendo al tempo stesso una maggiore protezione contro i metodi di tracciamento nascosti, come la impronte digitali.

## Suggerimenti client

User-Agent Client Hint forniscono ai proprietari del sito web la possibilità di accedere a gran parte delle stesse informazioni disponibili nell&#39;agente utente, ma in un modo più sicuro della privacy. Quando i browser moderni inviano un agente utente a un server web, l’intero agente utente viene inviato su ogni richiesta, indipendentemente dal fatto che sia necessaria. I suggerimenti client, invece, impongono un modello in cui il server deve chiedere al browser le informazioni aggiuntive che desidera conoscere sul client. Dopo aver ricevuto questa richiesta, il browser può applicare i propri criteri o la propria configurazione utente per determinare quali dati vengono restituiti. Invece di esporre l&#39;intero agente utente per impostazione predefinita su tutte le richieste, l&#39;accesso viene ora gestito in modo esplicito e verificabile.

Gli hint client User-Agent sono disponibili in Chrome dalla versione 89. Le versioni recenti dei browser basati su Chromium, come Microsoft Edge, Opera, Brave, Chrome Android, Opera Android e Samsung Internet, supportano anche l’API dei suggerimenti client.

I suggerimenti client contenuti nelle intestazioni della prima richiesta effettuata dal browser a un server web contengono il marchio del browser, la versione principale del browser e un indicatore che indica se il client è un dispositivo mobile. Ciascun elemento dati ha un proprio valore di intestazione, anziché essere raggruppato in una singola stringa agente utente, come illustrato nell’esempio seguente:

```
Sec-CH-UA: "Chromium";v="101", "Google Chrome";v="101", " Not;A Brand";v="99" 
Sec-CH-UA-Mobile: ?0 
Sec-CH-UA-Platform: "macOS"
```

L’esempio seguente è l’agente utente dello stesso browser:

```
Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/101.0.4951.54 Safari/537.36 
```

Sebbene le informazioni siano simili, la prima richiesta al server contiene suggerimenti client che contengono solo un sottoinsieme di ciò che è disponibile nella stringa agente utente. Mancano nella richiesta l&#39;architettura del sistema operativo, la versione completa del sistema operativo, il nome del motore di layout, la versione del modulo di gestione del layout e la versione completa del browser. Tuttavia, nelle richieste successive, l’API dei suggerimenti client consente ai server web di richiedere ulteriori dettagli di entropia elevata sul dispositivo. Quando si richiedono questi valori entropici elevati, a seconda dei criteri del browser o delle impostazioni utente, la risposta del browser può includere tali informazioni.

L’esempio seguente è un oggetto JSON restituito dall’API Client Hint quando vengono richiesti valori di entropia elevati:

```
{ 

    "architecture":"x86", 
    "bitness":"64", 
    "brands":[ 
        { 
            "brand":" Not A;Brand", 
            "version":"99" 
        }, 
        { 
            "brand":"Chromium", 
            "version":"100" 
        }, 
        { 
            "brand":"Google Chrome", 
            "version":"100" 
        } 
    ], 
    "fullVersionList":[ 
        { 
            "brand":" Not A;Brand", 
            "version":"99.0.0.0" 
        }, 
        { 
            "brand":"Chromium", 
            "version":"100.0.4896.127" 
        }, 
        { 
            "brand":"Google Chrome", 
            "version":"100.0.4896.127" 
        } 
    ], 
    "mobile":false, 
    "model":"", 
    "platformVersion":"12.2.1" 
} 
```

Gli elevati valori di entropia includono diverse informazioni aggiuntive che non sono disponibili nelle informazioni predefinite dei suggerimenti client. La tabella seguente contiene i dettagli dei dati disponibili nella richiesta predefinita rispetto alle informazioni sui suggerimenti client entropici elevati.

| Intestazione HTTP | JavaScript | Agente utente | Suggerimento client | Suggerimento client entropico elevato |
| --- | --- | --- | --- | --- |
| Sec-CH-UA | marchi | Sì | Sì | No |
| Piattaforma Sec-CH-UA | piattaforma | Sì | Sì | No |
| Sec-CH-UA-Mobile | dispositivi mobili | Sì | Sì | No |
| Sec-CH-UA-Platform-Version | platformVersion | Sì | No | Sì |
| Sec-CH-UA-Arch | architettura | Sì | No | Sì |
| Modello Sec-CH-UA | model | Sì | No | Sì |
| Sec-CH-UA-Bitness | Amarezza | Sì | No | Sì |
| Sec-CH-UA-Elenco completo delle versioni | fullVersionList | Sì | No | Sì |

## Migrazione agli hint client

Attualmente, i browser basati su Chromium continuano a inviare l&#39;agente utente insieme agli Hint client nelle intestazioni delle richieste effettuate ai server web. Tuttavia, a partire da aprile 2022 e fino a febbraio 2023, la quantità di dati contenuti nella stringa agente utente sarà ridotta. Altri browser, come Safari e Firefox, continueranno a sfruttare la stringa agente utente; tuttavia, anche loro ridurranno la quantità di informazioni ivi contenute.

## [!DNL Target] casi d’uso che richiedono suggerimenti clinici

I seguenti casi d’uso in Target richiedono suggerimenti client:

### Attributi del pubblico

Se utilizzi [!DNL Target] tipi di pubblico e utilizzare uno dei seguenti attributi di pubblico, [!DNL Target] richiede suggerimenti client per eseguire la segmentazione corretta:

* Browser
* Sistema operativo
* Dispositivi mobili

### Script di profilo

Se utilizzi gli script di profilo e fai riferimento al `user.browser` attributo (che fa riferimento all’agente utente), potrebbe essere necessario aggiornare lo script del profilo per controllare anche uno o più suggerimenti client. Puoi accedere a qualsiasi suggerimento client utilizzando la funzione . `user.clientHint('sec-ch-ua-xxxxx')`. Il nome dell&#39;intestazione Client Hint deve essere tutto minuscolo.

L&#39;esempio seguente mostra come rilevare correttamente un sistema operativo Windows in uno script di profilo:

```
"return (((user.browser != null) && (user.browser.indexOf(\"Windows\") > -1)) || " + 
      "((user.clientHint('sec-ch-ua-platform') != null) && 
(user.clientHint('sec-ch-ua-platform') === 'Windows')));" 
```

Le sezioni seguenti mostrano le intestazioni dei suggerimenti client e la relativa semantica di utilizzo degli script di profilo.

#### Sec-CH-UA

Entropia: Documentazione bassa: [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA)Attributo pubblico {target=_blank}: Utilizzo dello script del profilo del browser: `user.clientHint('sec-ch-ua')`

#### Sec-CH-UA-Arch

Entropia: Documentazione elevata: [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Arch](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Arch)Attributo pubblico {target=_blank}: Esposto agli utenti tramite script di profilo.
Utilizzo degli script di profilo: `user.clientHint('sec-ch-ua-arch')`

#### Sec-CH-UA-Bitness

Entropia: Documentazione elevata: [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Bitness](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Bitness)Attributo pubblico {target=_blank}: Esposto agli utenti tramite script di profilo.
Utilizzo degli script di profilo: `user.clientHint('sec-ch-ua-bitness')`

#### Sec-CH-UA-Elenco completo delle versioni

Entropia: Documentazione elevata: [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Full-Version-List](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Full-Version-List)Attributo pubblico {target=_blank}: Utilizzo dello script del profilo del browser: `user.clientHint('sec-ch-ua-full-version-list')`

#### Sec-CH-UA-Mobile

Entropia: Documentazione bassa: [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Mobile](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Mobile)Attributo pubblico {target=_blank}: Utilizzo script profilo mobile: `user.clientHint('sec-ch-ua-mobile')`

#### Modello Sec-CH-UA

Entropia: Documentazione elevata: [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Model](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Model)Attributo pubblico {target=_blank}: Utilizzo script profilo mobile: `user.clientHint('sec-ch-ua-model')`

#### Piattaforma Sec-CH-UA

Entropia: Documentazione bassa: [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Platform](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Platform)Attributo pubblico {target=_blank}: Utilizzo dello script del profilo del sistema operativo: `user.clientHint('sec-ch-ua-platform')`

#### Sec-CH-UA-Platform-Version

Entropia: Documentazione elevata: [https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Platform-Version](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Sec-CH-UA-Platform-Version)Attributo pubblico {target=_blank}: Esposto agli utenti tramite script di profilo.
Utilizzo degli script di profilo: `user.clientHint('sec-ch-ua-platform-version')`

## Come passare gli hint client a [!DNL Adobe Target]

Le sezioni seguenti contengono ulteriori informazioni su come passare gli Hint client, a seconda del [!DNL Target] implementazione.

### at.js versione 2.9.0 (o successiva)

A partire da at.js 2.9.0, gli hit client dell’agente utente verranno raccolti automaticamente dal browser e inviati a [!DNL Target] quando `getOffer/getOffers()` viene chiamato. Per impostazione predefinita, at.js raccoglie solo i suggerimenti client &quot;Bassa Entropia&quot;. Se esegui la segmentazione del pubblico o utilizzi script di profilo basati su dati classificati come &quot;Alta Entropia&quot; dalle sezioni precedenti, devi configurare at.js per raccogliere &quot;Alta Entropia&quot; Suggerimenti client dal browser tramite `targetGlobalSettings`.

`window.targetGlobalSettings = { allowHighEntropyClientHints: true };`

### SDK lato server

Per ulteriori informazioni su come trasmettere gli hint client tramite SDK lato server, vedi [Suggerimenti client](https://adobetarget-sdks.gitbook.io/docs/core-principles/audience-targeting#client-hints){target=_blank} nel *SDK per Adobe Target* documentazione.
