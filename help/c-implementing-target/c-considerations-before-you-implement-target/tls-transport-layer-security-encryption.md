---
keywords: tls;tls 1.0;transport layer security;encryption;tls 1.1;tls 1.2
description: Informazioni sulle modifiche relative al modo in cui Adobe e Target utilizzano TLS (Transport Layer Security) per mantenere standard di sicurezza elevati e promuovere la sicurezza dei dati dei clienti.
title: Modifiche alla crittografia di TLS (Transport Layer Security)
feature: null
topic: Standard
uuid: d222b966-ee73-4254-87b7-68099583e0dd
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '1233'
ht-degree: 62%

---


# Modifiche alla crittografia di TLS (Transport Layer Security){#tls-transport-layer-security-encryption-changes}

Informazioni sulle modifiche alle modalità  Adobe e  Adobe Target utilizzano TLS (Transport Layer Security) per mantenere gli standard di sicurezza più elevati e promuovere la sicurezza dei dati dei clienti.

Transport Layer Security (TLS) è tra i protocolli di sicurezza distribuiti più ampiamente ed è oggi utilizzato per i browser web e per altre applicazioni dove i dati devono essere scambiati in modo sicuro all’interno di una rete. Adobe possiede degli standard di sicurezza e conformità che richiedono la chiusura dei protocolli più vecchi e l’utilizzo di TLS 1.2 per poter avere la versione in uso più aggiornata e più sicura.

>[!IMPORTANT]
>
>Dopo il 1 marzo 2020,  Adobe Target non supporterà più la cifratura TLS 1.1 per Visual Experience Composer (VEC), Enhanced Experience Composer (EEC), distribuzione di attività, API e così via. Per evitare problemi, effettua l&#39;aggiornamento a TLS 1.2 prima del 1 marzo 2020.

Non è previsto un impatto significativo di tale cambiamento sui dati dei clienti o sulla creazione di rapporti.

## Compositore esperienza visivo con Compositore esperienza avanzato abilitato {#section_B374B62DEC3344C194AC7BECC2EE0AA0}

TLS 1.2 è il valore predefinito a partire dal 1 marzo 2020 e TLS 1.1 non sarà più supportato.

Adobe sposterà i clienti a TLS 1.2 in modo graduale. Per quanto riguarda coloro che sono in possesso di domini già conformi alla versione 1.2, verranno spostati a TLS 1.2 senza la necessità di apportare delle modifiche. La maggior parte dei domini cliente supporta già TLS 1.2; tuttavia, se il tuo dominio non supporta TLS 1.2, manterremo tali domini su TLS 1.1 come oggi (fino a marzo 2020).

Non dovresti riscontrare alcun problema durante questa fase di migrazione. Se il Compositore esperienza visivo ha smesso di caricare un sito che prima funzionava, [apri una segnalazione per l’Assistenza clienti](../../cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) riportando questa migrazione come possibile causa.

Se, tuttavia, sei uno di quei clienti che si trovano su TSL 1.1 senza supportare TLS 1.2, allora dovresti pianificare lo spostamento dei tuoi domini/infrastruttura a TLS 1.2. Continueremo a supportare il protocollo TLS 1.1 fino al 1 marzo 2020. A partire dal 1 marzo 2020, Target non supporterà il protocollo TLS 1.1 da utilizzare per il VEC tramite la funzionalità Enhanced Experience Composer (Compositore esperienza avanzato).

Anche se consigliamo vivamente a tutti di utilizzare fin da ora TLS 1.2, se sei un nuovo cliente ma *NON* supporti questo protocollo, contatta l’Assistenza clienti informandola che hai bisogno di TLS 1.1 per il Compositore esperienza avanzato. Tuttavia, pianificate di passare a TLS 1.2 perché non sarete supportati oltre il 1 marzo 2020.

## Activity delivery {#section_46CA5943E4354B259014C2BF340AECD6}

A partire dal 1 marzo 2020, i server Target non supporteranno più TLS 1.1. Con questa modifica, i server di Target non accetteranno più richieste da visitatori con dispositivi o browser Web meno recenti che non supportano TLS 1.2 (o versioni successive). Di conseguenza, i dispositivi e i browser più vecchi che supportano solo TLS 1.1 (o supportano TLS 1.1 per impostazione predefinita) non riceveranno più il contenuto dell&#39;attività da Adobe Target. Il contenuto predefinito del sito viene eseguito.

Tra i dispositivi e i browser più vecchi che saranno interessati sono compresi:

* Google Chrome (Chrome per Android) versioni 29 e precedenti
* Browser Opera (Opera Mobile) versioni 12.17 e precedenti
* Mozilla Firefox (Firefox per dispositivi mobili) versioni 26 e precedenti
* Android 4.3 e versioni precedenti
* Internet Explorer 8-10 su Windows 7 e versioni precedenti
* Internet Explorer 10 su Windows Phone 8.0
* Safari 6.0.4/OS X10.8.4 e versioni precedenti

Mentre pianificate questa modifica, tenete presente quanto segue (la scadenza del 1 marzo 2020 interessa tutti questi elementi):

* Devi assicurarti che il tuo sito predefinito sia pronto per essere riprodotto sui dispositivi e sui browser conformi.
* Tieni presente che il numero di visitatori nei rapporti di Target potrebbe avere un calo non significativo.
* Potrebbe essere necessario modificare i tipi di pubblico creati specificamente per dispositivi o browser meno recenti che non supportano TLS 1.2. La distribuzione a tali dispositivi e browser non funzionerà più.

Per ulteriori dettagli sui browser supportati e le loro versioni, consulta [Browser supportati](../../c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md#reference_01B4BF99E7D545A7998773202A2F6100).

## API di Adobe Target {#section_88797FA5434049EC89F908853CC76903}

A partire dal 1 marzo 2020, le API Target non supporteranno più la crittografia TLS 1.1. I clienti che accedono all’API devono assicurarsi che questo cambiamento non produca effetti negativi.

* I clienti API che utilizzano Java 7 con impostazioni predefinite avranno bisogno di apportare modifiche per supportare TLS 1.2. Per ulteriori informazioni, consulta “ [Modifica della versione del protocollo TLS predefinito per gli endpoint del cliente: da TLS 1.0 a TLS 1.2](https://www.java.com/en/configure_crypto.html)” sul sito web Java.
* I clienti API che utilizzano Java 8 non dovrebbero essere interessati, perché l’impostazione predefinita è TLS 1.2.
* Per i clienti che utilizzano l’API con altri framework, occorre contattare il fornitore per ottenere informazioni sul supporto per TLS 1.2.

## Access to Experience Cloud Solutions interfaces {#section_748870ADE77B4CBEB18518DC784E64E5}

Poiché l’interfaccia di Target Standard/ Premium richiede già un [browser Web moderno](../../c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md#reference_01B4BF99E7D545A7998773202A2F6100), non prevediamo alcun problema. Se non riesci più a connetterti a Target, devi aggiornare il browser all’ultima versione.

## How to check which TLS version your browser uses {#section_44716DA2CEFF492BABD95AE32B1A3FC6}

Per controllare la versione TLS sul tuo sito web utilizzando Google Chrome:

1. Apri il sito Web interessato in Chrome.
1. Dal menu Chrome (le tre ellissi verticali), fate clic su Altri strumenti > Strumenti per sviluppatori.

   ![Strumenti per sviluppatori Chrome](/help/c-implementing-target/c-considerations-before-you-implement-target/assets/chrome-developer-tools.png)

1. Aprite la scheda Protezione, quindi esaminate le informazioni sulla versione TLS in Connessione:

   ![Dettagli versione TLS](/help/c-implementing-target/c-considerations-before-you-implement-target/assets/chrome-tls-version.png)

>[!NOTE]
>
>Queste istruzioni sono aggiornate al momento della pubblicazione e sono soggette a modifiche. Una ricerca rapida su Internet dovrebbe essere di aiuto in caso di modifica di queste istruzioni.  Altri browser hanno passaggi simili.

## Funzionamento previsto con i browser che supportano le versioni TLS inferiori alla 1.2 {#section_B5DA97A34EF248EB927610A5DA71EF2F}

Questa sezione descrive cosa aspettarsi dai browser che supportano le versioni TLS inferiori alla 1.2 solo quando si utilizza un&#39;implementazione at.js o mbox.js. A scopo di confronto, questa sezione descrive anche cosa aspettarsi dai browser che supportano TLS 1.2.

### Endpoint centrali

| Implementazione JavaScript di Target | Dettagli |
|--- |--- |
| at.js | Con TLS 1.0 o TLS 1.1 abilitato:<ul><li>Utilizzando gli strumenti di sviluppo del browser, nella scheda Rete, vedrai “200 OK”. Ciò significa che la richiesta è riuscita.</li><li>L&#39;utente visualizza un messaggio “Impossibile connettersi in modo sicuro a questa pagina”. Il messaggio spiega che ciò potrebbe essere causato perché il sito utilizza impostazioni di protezione TLS obsolete o non sicure.</li><li>Non vengono visualizzati errori di console.</li></ul>Con TLS 1.2 abilitato:<ul><li>Il file at.js viene scaricato.</li></ul> |
| mbox.js | Con TLS 1.0 o TLS 1.1 abilitato:<ul><li>Utilizzando gli strumenti di sviluppo del browser, nella scheda Rete, vedrai “200 OK”. Ciò significa che la richiesta è riuscita.</li><li>L&#39;utente visualizza un messaggio “Impossibile connettersi in modo sicuro a questa pagina”. Il messaggio spiega che ciò potrebbe essere causato perché il sito utilizza impostazioni di protezione TLS obsolete o non sicure.</li><li>Non vengono visualizzati errori di console.</li></ul>Con TLS 1.2 abilitato:<ul><li>Il file mbox.js viene scaricato.</li></ul> |

### Endpoint dei bordi

| Implementazione JavaScript di Target | Dettagli |
|--- |--- |
| at.js | Con TLS 1.0 o TLS 1.1 abilitato:<ul><li>Utilizzando gli strumenti di sviluppo del browser, nella scheda Rete, vedrai “200 OK”. Ciò significa che la richiesta è riuscita.</li><li>L&#39;utente visualizza un messaggio “Impossibile connettersi in modo sicuro a questa pagina”. Il messaggio spiega che ciò potrebbe essere causato perché il sito utilizza impostazioni di protezione TLS obsolete o non sicure.</li><li>Non vengono visualizzati errori di console.</li><li>Viene servito il contenuto predefinito.</li></ul>Con TLS 1.2 abilitato:<ul><li>Viene servito il contenuto dell’offerta.</li></ul> |
| mbox.js | Con TLS 1.0 o TLS 1.1 abilitato:<ul><li>Utilizzando gli strumenti di sviluppo del browser, nella scheda Rete, vedrai “200 OK”. Ciò significa che la richiesta è riuscita.</li><li>L&#39;utente visualizza un messaggio “Impossibile connettersi in modo sicuro a questa pagina”. Il messaggio spiega che ciò potrebbe essere causato perché il sito utilizza impostazioni di protezione TLS obsolete o non sicure.</li><li>Non vengono visualizzati errori di console.</li><li>Viene servito il contenuto predefinito.</li></ul>Con TLS 1.2 abilitato:<ul><li>Viene servito il contenuto dell’offerta</li></ul> |

### Attività con targeting per audience con versione del browser (Internet Explorer, versioni 6, 7 o 8)

>[!NOTE]
>
>I tipi di pubblico cessano di funzionare.

| Implementazione JavaScript di Target | Dettagli |
|--- |--- |
| at.js | at.js non è supportato nelle versioni di Internet Explorer precedenti alla versione 10. |
| mbox.js | Con TLS 1.0 o TLS 1.1 abilitato:<ul><li>Viene servito il contenuto predefinito.</li><li>Non viene attivata alcuna richiesta di Target.</li><li>Non viene visualizzato alcun errore di console.</li><li>Utilizzando gli strumenti di sviluppo del browser, nella scheda Rete, vedrai “200 OK”. Ciò significa che la richiesta è riuscita.</li></ul>Con TLS 1.2 abilitato:<ul><li>Viene servito il contenuto dell’offerta.</li></ul> |