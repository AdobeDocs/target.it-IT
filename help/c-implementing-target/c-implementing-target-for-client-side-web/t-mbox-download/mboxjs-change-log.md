---
keywords: modifiche a mbox. js;versioni di mbox.js
description: Scopri l’implementazione legacy di mbox.js di Adobe Target. Esegui la migrazione a Adobe Experience Platform Web SDK (AEP Web SDK) o all’ultima versione di at.js.
title: Che cosa è incluso in ogni versione di mbox.js?
feature: at.js
role: Developer
exl-id: 4e95de13-2848-497a-9d06-41e9cbd98b42
source-git-commit: dd20791535e47c83d0f0ac60addfe0888748f86a
workflow-type: tm+mt
source-wordcount: '2377'
ht-degree: 84%

---

# Dettagli sulle versioni di mbox.js

In questa pagina sono elencate le modifiche per ogni versione di mbox.js.

>[!IMPORTANT]
>
>**Terminazione di mbox.js**: a partire dal 31 marzo 2021, [!DNL Adobe Target] non supporta più la libreria mbox.js. Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e le pagine che hanno attività [!DNL Target] in esecuzione, si troveranno a utilizzare il contenuto predefinito.
>
>Esegui la migrazione alla versione più recente del nuovo [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js prima di questa data per evitare potenziali problemi con i siti. Per ulteriori informazioni, consulta [Panoramica: implementare Target per web lato client](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

>[!NOTE]
>
>Adobe consiglia a tutti gli utenti di mbox.js di eseguire l’aggiornamento alla versione 57 o successiva. Alcuni utenti hanno avuto problemi di timeout per il mancato caricamento di `target.js`. La versione 57 ha risolto questo problema. Tuttavia, se utilizzi il servizio [!DNL Experience Cloud Visitor ID], è richiesta la versione 58 o successiva.

Il modo in cui Target effettua e risponde alle chiamate dalla pagina dipende dalla versione della libreria di Target che stai utilizzando, dall’eventuale implementazione del servizio ID visitatore e dall’esistenza dell’ID del visitatore. Per informazioni, consulta [Risposte alle chiamate di Target a seconda della versione della libreria](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/call-responses-library-version.md#concept_A95A4758A1E7405D947E9B4BCB5D62F0).

>[!NOTE]
>
>La libreria mbox.js non verrà più sviluppata. Tutti i clienti devono migrare da mbox.js a at.js.

## mbox.js versione 63 {#section_ED8EFCF653A845ED8927F759578C4A33}

**Versione di Target:** 17.7.1

È ora disponibile la versione 63 di [!DNL mbox.js]. 

I seguenti miglioramenti e correzioni sono inclusi nella versione 63 di [!DNL mbox.js]:

* È stato risolto un problema nella generazione di SDID quando si utilizzano `mboxDefine()` e `mboxUpdate()`. Questo problema riguarda solo i clienti che hanno API Visitor sulla pagina.

## mbox.js versione 62 {#section_723A9119FE204183847D3B0929A99B41}

* Sono stati risolti i problemi di visualizzazione momentanea nelle attività di reindirizzamento visualizzate nei browser Google Chrome.
* È stata aggiunta l’impostazione `secureOnly` che indica se mbox.js deve utilizzare solo HTTPS o può passare da HTTP a HTTPS in base al protocollo della pagina. Si tratta di un&#39;impostazione avanzata con impostazione predefinita False.

## mbox.js versione 61 {#section_F3B59C5578B64883AE013B9342151193}

**Versione di Target:** 16.7.2

**Data di rilascio:** 28 luglio 2016

La versione 61 di mbox.js contiene i seguenti miglioramenti:

* L’algoritmo per la generazione ID di mboxSession nell’API Data JavaScript genera ora una stringa casuale anziché utilizzare un timestamp più una stringa casuale.
* I seguenti dettagli sono applicabili solo in presenza di API visitatore nella pagina:

   * [!DNL mbox.js] versione 61 non sostituisce la proprietà `loadTimeout` dell’API visitatore. I clienti possono utilizzare `visitorApiTimeout` + `visitorApiPageDisplayTimeout` per controllare l’integrazione dell’API visitatore.
   * È stata aggiunta l’impostazione `optoutEnabled` per supportare la futura funzionalità di rifiuto del consenso di Adobe Experience Cloud. Il valore predefinito è False. Se questa proprietà è abilitata, tutte le richieste vengono eseguite in modo asincrono rispetto all’endpoint [!DNL /ajax], proprio come nella versione 60.
   * La funzione che nasconde il corpo è disattivata per impostazione predefinita. Target utilizza la funzione che nasconde il corpo solo quando le opzioni Creazione automatica mbox globale e Nascondi il corpo sono abilitate.
   * Se non ci sono cookie di ID visitatore di Experience Cloud, tutte le richieste vengono eseguite in modo asincrono rispetto a [!DNL /ajax] durante il primo caricamento della pagina. Durante il secondo caricamento della pagina, Target utilizza il flusso normale perché i valori di ID visitatore sono già presenti.
   * Se utilizzi Adobe Analytics come origine per la generazione di rapporti dell’attività e la versione 61 (o successiva) di mbox.js o la versione 0.9.1 (o successiva) di at.js, non è necessario specificare un server di tracciamento durante la creazione di attività. La libreria mbox.js o at.js invia automaticamente i valori del server di tracciamento a [!DNL Target]. Durante la creazione di attività, puoi lasciare vuoto il campo [!UICONTROL Server di tracciamento] nella pagina [!UICONTROL Obiettivi e impostazioni].

## mbox.js versione 60 {#section_3BDAB885FA13444A8D35940A4BFF5825}

**Versione di Target:** 16.4.1

**Data di rilascio:** 21 aprile 2016

Per impostazione predefinita, il contenuto della pagina non è nascosto. La versione 60 nasconde il contenuto della pagina solo quando è abilitata l’opzione “Creazione automatica mbox globale”. Per nascondere la pagina utilizza la proprietà `opacity:0` di CSS anziché `display:none`. Questa proprietà assicura la corretta consegna per i siti reattivi e si allinea a [!DNL at.js].

È possibile abilitare la funzione Nascondi il corpo utilizzando due impostazioni:

* `bodyHidingEnabled` Il valore predefinito è False, il che significa che la sezione BODY dell’HTML non è nascosta.

* bodyHiddenStyle

   Il valore predefinito è `body{opacity:0}`. Questo valore può essere modificato in uno diverso, ad esempio `body{display:none}`.

Queste impostazioni possono essere ignorate tramite l’inclusione di quanto segue:

```
<script> 
window.targetGlobalSettings = { 
 bodyHidingEnabled: true, 
 bodyHiddenStyle: "body{opacity:0}", 
 visitorApiPageDisplayTimeout: 2000 
}; 
</script>
```

La tecnica che nasconde la pagina utilizza i tag di stile per aggiungere e rimuovere stili. Questa tecnica assicura che gli stili del sito rimangano invariati dopo l’esecuzione del codice che nasconde la pagina.

**Utenti DTM:** questa tecnica ti impedisce di utilizzare l’opzione Importa automaticamente, in quanto non è possibile salvare la configurazione di cui sopra nell’interfaccia utente di Target. È necessario utilizzare le istruzioni di cui sopra e quindi incollare il contenuto nella casella del codice dell&#39;opzione di hosting Personalizzato.

Anche nella versione 60, se il file [!DNL visitorAPI.js] è presente per il servizio di ID visitatore di Experience Cloud, tutte le mbox sono richieste tramite un endpoint AJAX. Questo processo è necessario perché i metodi API dei visitatori sono asincroni. Un vantaggio di questo approccio è che il tempo di rendering in avvio viene ridotto drasticamente, poiché le richieste mbox non lo bloccano. Tuttavia, questo approccio significa anche che il contenuto delle offerte [!DNL Target] viene eseguito in modo asincrono, pertanto il codice delle offerte deve essere scritto di conseguenza. Le offerte contenenti `document.write` e altro codice che presuppone che venga eseguito al caricamento della pagina iniziale non vengono eseguite come previsto.

* Chiamate asincrone nella versione 60 (V60)

   Quando utilizzi v60 con il servizio ID visitatore, tutte le chiamate mbox vengono eseguite in modo asincrono. Si tratta di un nuovo metodo di lavoro per mbox, quindi fai attenzione se vuoi eseguire l’aggiornamento a questa versione.
* Possibile visualizzazione momentanea per i nuovi visitatori

   Quando utilizzi le versioni da v58 a v60 con il servizio ID visitatore, le chiamate mbox attendono che l’ID visitatore sia impostato prima dell’attivazione (o fino a quando non si è verificato un timeout). Questo accade durante il primo caricamento della pagina per un nuovo visitatore.

## mbox.js versione 59 {#section_FF0E70C4C17E402D8374DE428C5D996E}

**Versione di Target:** 16.2.1

**Data di rilascio:** 17 febbraio 2016

La versione 59 di mbox.js contiene i seguenti miglioramenti:

* L’impostazione Disabilita Mbox è stata abbassata a 30 minuti
* È stato risolto un problema relativo alla funzione Nascondi/mostra pagina

   Invece di utilizzare `display:none` per nascondere la pagina come nella versione 58, viene usato `opacity:0`. Questo risolve i problemi del metodo precedente nel nascondere la pagina per i siti reattivi.

## mbox.js versione 58 {#section_5070B0D1C87F4937BB97727923DD36C7}

**Versione di Target:** 15.7.1

**Data di rilascio:** 30 luglio 2015

Questa versione di mbox.js è necessaria se utilizzi Analytics come origine per la generazione di rapporti per Target ed è altamente consigliata per Profili e Tipi di pubblico.

La versione 58 di mbox.js assicura che il servizio ID visitatore di Experience Cloud restituisca un ID visitatore prima che vengano effettuate le chiamate Target. In tal modo, i dati del pubblico condivisi attraverso il servizio principale Profili e Tipi di pubblico sono disponibili per la prima chiamata Target nella sessione del visitatore. Per evitare che appaia momentaneamente il contenuto predefinito prima che venga restituito il contenuto del test, Target nasconde l’elemento `<BODY>` finché non viene restituita la risposta del servizio ID visitatore. Per nascondere la pagina viene utilizzato `display:none`.

Questo aggiornamento risolve anche un problema che si verificava quando si utilizzava Analytics come origine per la generazione di rapporti per Target e che causava un numero gonfiato di visitatori in Analytics per le visite che comprendevano solo una pagina.

Mbox.js imposta i valori di timeout nel caso in cui il servizio ID visitatore non sia disponibile. Il timeout predefinito per il servizio ID visitatore è di 500 ms (0,5 secondi). Un timeout aggiuntivo imposta il limite massimo di tempo in cui il tag `<BODY>` è nascosto. Tale impostazione predefinita è di 500 ms (0,5 secondi). Questi timeout possono essere modificati inserendo il codice seguente prima del riferimento a mbox.js in ogni pagina:

```
<script> 
window.targetGlobalSettings = { 
 visitorApiTimeout: 500, 
 visitorApiPageDisplayTimeout: 500 
}; 
</script> 
```

La versione 58 o successiva di mbox.js esegue il contenuto non-JavaScript per la mbox globale subito dopo il tag HTML `BODY`. Il contenuto JavaScript all’interno dei tag `<script>` per la mbox globale viene eseguito dopo che l’attivazione dell’evento `DOMContentLoaded`. Questo ordine di consegna dei contenuti assicura che il contenuto JavaScript per la mbox globale sia consegnato e renderizzato correttamente.

## mbox.js versione 57 {#section_6BA1CDBF75B14A94B59E8624ACF583D4}

**Versione di Target:** 15.4.1

**Data di rilascio:** 21 aprile 2015

Le seguenti modifiche sono state apportate in questa versione:

* La risposta con Creazione automatica mbox globale per Target Standard non utilizza più document.write() né crea un `<div>` elemento.

   Questa modifica elimina la condizione per la quale il file mbox.js doveva essere l’ultimo elemento della sezione `<head>` della pagina. Ti consigliamo di effettuare un controllo qualità approfondito dopo l’aggiornamento a questa nuova versione.

   Questa modifica potrebbe causare modifiche nel comportamento durante la distribuzione di alcuni tipi di offerta. Ecco le condizioni specifiche da considerare:

   * Il contenuto HTML restituito come parte di una “offerta plug-in” non esegue il rendering correttamente, ma il codice JavaScript all’interno delle offerte viene eseguito come previsto.
   * Per le offerte JavaScript che vengono restituite alla mbox globale, il codice JavaScript può essere incorporato nel tag `<script>` oppure come riferimento da un attributo `src`.

      A tale scopo, aggiungi l’attributo `async` alla chiamata dello script, come segue:

      `<script src='external-url' async='true'></script>`

      L&#39;attributo `async` ha un supporto limitato in Internet Explorer (per informazioni: [https://developer.mozilla.org/en/docs/Web/HTML/Element/script#Browser_compatibility](https://developer.mozilla.org/en/docs/Web/HTML/Element/script#Browser_compatibility)) per escludere i visitatori che utilizzano versioni di IE precedenti da test che includono questi script di terze parti.

* Sono stati corretti dei problemi segnalati nella versione 56 a causa di cambiamenti nella sezione JavaScript extra di mbox.js. Tutto il codice nella sezione JavaScript extra è nuovamente disponibile nell’ambito globale.

La seguente funzionalità non è supportata nella versione 57 di mbox.js:

* Una mbox globale creata automaticamente generata in Target Standard non funziona con i tipi di offerta gestiti da Target Classic. Questi includono “offerta sul tuo sito” e “offerta esterna a Test&amp;Target”.

   Ciò significa che in Target Classic non devi selezionare la mbox globale creata automaticamente da Target Standard quando una di queste offerte è necessaria.
* Sono supportati solo i plug-in di JavaScript.

   Se l’offerta di un plug-in combina codice JavaScript e HTML, allora il codice JavaScript viene eseguito ma il contenuto HTML non viene mostrato.

La versione 57 di mbox.js include anche importanti risoluzioni di problemi:

* È stato risolto un problema che causava il mancato funzionamento del plug-in SiteCatalyst in mbox.js v56.
* È stato risolto un problema che provocava errori JavaScript aggiuntivi a causa della modifica dell’ambito.
* Ripristina le impostazioni di fabbrica di mboxFactory.

## mbox.js versione 56 {#section_C4F4A53584B741FF9FD907D81CB7E164}

**Versione di Target:** 15.1.2

**Data di rilascio:** 17 febbraio 2015

>[!NOTE]
>
>Alcuni utenti hanno avuto problemi di timeout per il mancato caricamento di `target.js`. La versione 57 ha risolto questo problema. Tuttavia, se utilizzi il servizio [!DNL Experience Cloud Visitor ID], è richiesta la versione 58 o successiva.

Le seguenti modifiche sono state apportate in questa versione:

* Modifiche apportate a Premium Recommendations per supportare la trasmissione dei parametri alla mbox globale
* Aggiunge un timeout di 5 secondi alla chiamata di caricamento di target.js. Nel raro caso in cui il file non venga caricato, la pagina viene sottoposta a rendering e non viene visualizzata alcuna attività di Target Standard.
* Spostamento di “extra JavaScript” affinché venga eseguito prima della mbox globale

   Tutte le impostazioni in v56+ sono con spazio dei nomi. Eventuali funzioni dichiarate in “extra JavaScript” devono essere precedute da `window`.

   Ad esempio:

   `function foo {`

   `}`

   Diventa:

   `window.foo = function() {`

   `}`

   Anche qualsiasi variabile che debba essere accessibile a livello globale deve essere preceduta da `window`.

* Aggiunta di un cookie chiamato “em-disabled” fornito da mbox.js se target.js non riesce a caricare durante la distribuzione. Questo cookie impedisce alle offerte create tramite il Compositore esperienza visivo di essere visualizzate sul sito. Gli utenti con questo cookie non vedono il contenuto del test né vengono conteggiati in tali rapporti di attività. Tutti gli altri contenuti dell’offerta (da campagne in Target Classic per esempio) continuano ad essere caricati. Il cookie ha una durata di 30 minuti dal momento del caricamento non riuscito.

## mbox versione 55

**Versione di Target:** 15.1

**Data di rilascio:** 19 gennaio 2015

Modifica la versione 53 con correzioni IE.

## mbox versione 54

**Versione di Target:** 14.9.2

**Data di rilascio:** 30 settembre 2014

Modifica l’implementazione della mbox globale in AJAX da document.write. Questa modifica rimuove il requisito che il file mbox.js sia l’ultimo elemento della sezione `<head>` della pagina. Questa versione è disponibile solo tramite API. I client possono scaricare e utilizzare questo file mbox.js. In alcuni siti il contenuto viene visualizzato momentaneamente con questa implementazione; si consiglia quindi di convalidare l’integrazione sul sito.

## mbox versione 53

**Versione di Target:** 14.9.1

**Data di rilascio:** 14 settembre 2014

È stato corretto un problema a causa del quale i parametri di pagina di Target non vengono attivati correttamente in Internet Explorer.

## mbox versione 52

**Versione di Target:** 14.8

**Data di rilascio:** 14 agosto 2014

La funzione mboxParameter ora funziona in Target Standard e Premium.

È stato risolto un problema che impediva il funzionamento del monitoraggio di Analytics in IE 9 e 11. Questa modifica riguarda solo gli utenti di Analytics.

È ora possibile [trasmettere parametri](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/pass-parameters-to-global-mbox.md) come array, come un oggetto JSON o come elenco separato da virgole (già supportato) a target-global-mbox utilizzando la funzione targetPageParams().

Sono stati rinominati M2PcId e tutti gli elementi collegati a VisitorId.

È consentita l’eliminazione di defaultDiv per una mbox registrata.

## mbox versione 51

**Versione di Target:** 14.6

**Data di rilascio:** 25 giugno 2014

È stato corretto un bug che impostava un cookie non corretto nei siti con due caratteri nel dominio di primo livello.

È stato corretto un bug minore in mbox.js che causava la restituzione di valori hashtag.

## mbox versione 50

È stata migliorata la sincronizzazione tra Target Standard e Target Classic.

## mbox versione 49

È stato migliorato il supporto in Internet Explorer 10 per mbox nidificate.

## mbox versione 48

È stato aggiunto il supporto per Adobe Analytics come origine per la generazione di rapporti per Target.

## mbox versione 47

mbox.js ora supporta l’utilizzo di un nome di mbox globale personalizzato per Target Standard.

## mbox versione 46

È stato aggiunto il supporto completo per il servizio ID visitatore di Experience Cloud per l’implementazione a singola riga di codice di Target Standard. Ciò consente l’integrazione lato server di Adobe Analytics e la condivisione del profilo di Experience Cloud.

È stato corretto un problema relativo alla distribuzione dei contenuti in IE10 in modalità documento.

## mbox versione 45

È stato aggiunto il supporto completo per il servizio ID visitatore di Experience Cloud. Ciò consente l’integrazione lato server di Adobe Analytics e la condivisione del profilo di Experience Cloud.

## mbox versione 44

È stato aggiunto un nuovo parametro URL per mboxVizTarget:

mboxDOMLoaded

## mbox versione 43

È stato aggiunto supporto per Target Standard.

## mbox versione 42

È stato aggiunto il supporto iniziale per il servizio ID visitatore condiviso di Experience Cloud.

## mbox versione 41

* Anche con l’impostazione x-only, disattiva il cookie di prima parte per migliorare il tempo di caricamento ed evitare continui aggiornamenti di pagina

   Viene impostato un cookie di timeout se la chiamata a Target non viene restituita in tempo. Questo è un metodo più veloce rispetto all’utilizzo del solo cookie di terze parti. Con il solo cookie di terze parti, la pagina viene costantemente aggiornata in attesa di una risposta valida dai server di Target.

* È stata corretta la limitazione del traffico, in modo che venga applicata solo quando mbox.js è abilitato

   Questo problema si verificava se per un cliente era presente una limitazione di traffico sulla propria mbox.js, con conseguente mancato funzionamento dell’impostazione di timeout. Ciò comportava l’aggiornamento della pagina in attesa di una buona risposta dai server di Target.

* È stato corretto il plug-in SiteCatalyst in modo che utilizzi sempre il fetcher Ajax

   Prima di questa modifica, in alcuni casi per gli utenti del plug-in Test&amp;Target to SiteCatalyst, a seconda di quando il plug-in veniva caricato, poteva verificarsi l’attivazione di un document.write che eliminava la pagina.

## mbox versione 38

È stato aggiunto supporto per l’integrazione tra SiteCatalyst e Test&amp;Target basata su pagina (deve essere abilitata)

## mbox versione 37

Sono state codificate le chiavi URL

## mbox versione 36

È stata modificata la mbox per utilizzare tt.omtrdc.net

## mbox versione 35

* Il debug della mbox ora avviene sempre da remoto
* È stato aggiunto il parametro mboxTime. Questo parametro rappresenta l’ora come viene visualizzata dall’utente, in millisecondi a partire da Epoch, GMT. Viene calcolato una sola volta.

## mbox versione 34

* Tenta sempre di ottenere l’ultimo div predefinito anziché fare riferimento a una versione in cache.

   Questo risolve un problema con un div di contenuto predefinito nella cache non presente nel DOM a causa di una voce mboxUpdate, che forniva il contenuto per il div predefinito.

* Nuovo parametro booleano facoltativo per mbox.getDefaultDiv. Se true, restituisce il div predefinito corrente. Se false, restituisce l’ultimo div predefinito nella cache.
* È stato aggiornato mbox.loaded per supportare il carico di Ajax
* Il parametro mboxURL è ora codificato con encodeURIComponent invece che escape
* Test del supporto di encodeURIComponent nel browser e visualizzazione del contenuto predefinito, in caso contrario. Sono state rimosse anche le seguenti opzioni di configurazione mbox.js:
   * encode\_mbox\_parameters
   * mbox\_signal\_support
