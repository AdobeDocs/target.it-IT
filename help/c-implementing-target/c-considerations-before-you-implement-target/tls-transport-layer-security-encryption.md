---
description: Informazioni sulle modifiche relative al modo in cui Adobe e Target utilizzano TLS (Transport Layer Security) per mantenere standard di sicurezza elevati e promuovere la sicurezza dei dati dei clienti.
keywords: tls;tls 1.0;transport layer security;crittografia
seo-description: Informazioni sulle modifiche relative al modo in cui Adobe e Target utilizzano TLS (Transport Layer Security) per mantenere standard di sicurezza elevati e promuovere la sicurezza dei dati dei clienti.
seo-title: Modifiche alla crittografia di TLS (Transport Layer Security)
solution: Target
title: Modifiche alla crittografia di TLS (Transport Layer Security)
topic: Standard
uuid: d222b966-ee73-4254-87b7-68099583e0dd
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Modifiche alla crittografia di TLS (Transport Layer Security){#tls-transport-layer-security-encryption-changes}

Informazioni sulle modifiche relative al modo in cui Adobe e Target utilizzano TLS (Transport Layer Security) per mantenere standard di sicurezza elevati e promuovere la sicurezza dei dati dei clienti.

Transport Layer Security (TLS) è tra i protocolli di sicurezza distribuiti più ampiamente ed è oggi utilizzato per i browser web e per altre applicazioni dove i dati devono essere scambiati in modo sicuro all’interno di una rete. Gli standard di sicurezza e conformità adottati da [!DNL Adobe] richiedono la dismissione dei protocolli più vecchi e l’utilizzo di TLS 1.2 per poter utilizzare sempre la versione più aggiornata e più sicura.

>[!NOTE]
>
>Il 20 febbraio 2019, l’infrastruttura Adobe Target è stata aggiornata nelle aree EMEA, Giappone e APAC per non raccogliere più dati dagli utenti finali con dispositivi meno recenti o browser web che non supportano TLS 1.1 o versione successiva. Lo stesso aggiornamento è pianificato per l’area Nord America al **1 aprile 2019**. La migrazione a TLS 1.2 offre una maggiore protezione. Per evitare problemi durante la transizione, è importante esaminare a fondo le specifiche e pianificare le modifiche con il tuo team IT.

Non è previsto un impatto significativo di tale cambiamento sui dati dei clienti o sulla creazione di rapporti.

## Compositore esperienza visivo con Compositore esperienza avanzato abilitato {#section_B374B62DEC3344C194AC7BECC2EE0AA0}

Finora, il [Compositore esperienza avanzato](../../c-experiences/experiences.md#section_34265986611B4AB8A0E4D6ACC25EF91D) di Adobe Target ha utilizzato TLS 1.0 per impostazione predefinita. A partire dalla versione 18.4.1 di Target (25 aprile 2018), Target passerà a TLS 1.2 per impostazione predefinita.

Adobe sposterà i clienti a TLS 1.2 in modo graduale. Per quanto riguarda coloro che sono in possesso di domini già conformi alla versione 1.2, verranno spostati a TLS 1.2 senza la necessità di apportare delle modifiche. La maggior parte dei domini dei clienti supportano già TLS 1.2; tuttavia, se il tuo non lo supporta, manterremo il tuo dominio su TLS 1.0 (fino a febbraio 2019).

Non dovresti riscontrare alcun problema durante questa fase di migrazione. Se il Compositore esperienza visivo ha smesso di caricare un sito che prima funzionava, [apri una segnalazione per l’Assistenza clienti](../../cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) riportando questa migrazione come possibile causa.

Se, tuttavia, sei uno dei clienti che utilizzano TLS 1.0 e i tuoi domini/infrastrutture non supportano TLS 1.2, allora dovresti pianificare lo spostamento di questi a TLS 1.2. Continueremo a supportare il protocollo TLS 1.0 fino a febbraio 2019. A partire da febbraio 2019, Target non supporterà più il protocollo TLS 1.0 per l’utilizzo per il Compositore esperienza visivo tramite la funzionalità Compositore esperienza avanzato.

Anche se consigliamo vivamente a tutti di utilizzare fin da ora TLS 1.2, se sei un nuovo cliente ma *NON* supporti questo protocollo, contatta l’Assistenza clienti informandola che hai bisogno di TLS 1.0 per il Compositore esperienza avanzato. Tuttavia, ti invitiamo a pianificare lo spostamento a TLS 1.2, dato che la versione 1.0 non verrà più supportata dopo febbraio 2019.

## Consegna attività {#section_46CA5943E4354B259014C2BF340AECD6}

A partire da febbraio 2019 i server di Target non supporteranno più TLS 1.0. In seguito a questa modifica, questi server non accetteranno più richieste da utenti finali che utilizzano i dispositivi o i browser web più vecchi che non supportano TLS 1.1 o le versioni successive. Di conseguenza, i dispositivi e i browser più vecchi che supportano solo TLS 1.0 (o supportano TLS 1.0 per impostazione predefinita) non riceveranno più il contenuto dell&#39;attività da Adobe Target. Il contenuto predefinito del sito viene eseguito.

Tra i dispositivi e i browser più vecchi che saranno interessati sono compresi:

* Android 4.3 e versioni precedenti
* Internet Explorer 8-10 su Windows 7 e versioni precedenti
* Internet Explorer 10 su Windows Phone 8.0
* Safari 6.0.4/OS X10.8.4 e versioni precedenti

Mentre pianifichi questa modifica, considera quanto segue (ricorda che la scadenza di febbraio 2019 riguarda tutti questi elementi):

* Devi assicurarti che il tuo sito predefinito sia pronto per essere riprodotto sui dispositivi e sui browser conformi.
* Tieni presente che il numero di visitatori nei rapporti di Target potrebbe avere un calo non significativo.
* Potresti dover modificare i tipi di pubblico creati specificamente per i dispositivi o i browser più vecchi che non supportano TLS 1.0: la consegna a questi dispositivi e browser non funzionerà più.

Per ulteriori dettagli sui browser supportati e le loro versioni, consulta [Browser supportati](../../c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md#reference_01B4BF99E7D545A7998773202A2F6100).

## API di Adobe Target {#section_88797FA5434049EC89F908853CC76903}

A partire da febbraio 2019, le API di Target non supporteranno più la crittografia TLS 1.0. I clienti che accedono all’API devono assicurarsi che questo cambiamento non produca effetti negativi.

* I clienti API che utilizzano Java 7 con impostazioni predefinite avranno bisogno di apportare modifiche per supportare TLS 1.2. Per ulteriori informazioni, consulta “ [Modifica della versione del protocollo TLS predefinito per gli endpoint del cliente: da TLS 1.0 a TLS 1.2](https://www.java.com/en/configure_crypto.html)” sul sito web Java.
* I clienti API che utilizzano Java 8 non dovrebbero essere interessati, perché l’impostazione predefinita è TLS 1.2.
* Per i clienti che utilizzano l’API con altri framework, occorre contattare il fornitore per ottenere informazioni sul supporto per TLS 1.2.

## Accesso alle interfacce delle soluzioni Experience Cloud {#section_748870ADE77B4CBEB18518DC784E64E5}

Poiché l’interfaccia di Target Standard/ Premium richiede già un [browser Web moderno](../../c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md#reference_01B4BF99E7D545A7998773202A2F6100), non prevediamo alcun problema. Se non riesci più a connetterti a Target, devi aggiornare il browser all’ultima versione.

## Controllare quale versione di TLS è utilizzata dal browser {#section_44716DA2CEFF492BABD95AE32B1A3FC6}

Per controllare la versione TLS sul tuo sito web con Firefox (altri browser hanno passaggi simili):

1. Apri il sito interessato in Firefox.
1. Fai clic sull&#39;icona **[!UICONTROL Mostra informazioni del sito]** nella barra degli indirizzi del browser.

   ![](assets/firefox_more_info.png)

1. Fai clic su **[!UICONTROL Mostra dettagli di connessione]** &gt; **[!UICONTROL Ulteriori informazioni]**.

   ![](assets/firefox_more_info_2.png)

1. Verifica la versione di TLS alla voce Dettagli tecnici:

   ![](assets/firefox_more_info_3.png)

## Comportamento previsto con browser che supportano solo TLS 1.0 {#section_B5DA97A34EF248EB927610A5DA71EF2F}

Questa sezione descrive cosa aspettarsi con i browser che supportano TLS 1.0 solo quando si utilizza un&#39;implementazione at.js o mbox.js. A scopo di confronto, questa sezione descrive inoltre cosa aspettarsi con i browser che supportano TLS 1.1 e 1.2.

### Endpoint centrali

| Implementazione JavaScript di Target | Dettagli |
|--- |--- |
| at.js | Con TLS 1.0 abilitato:<ul><li>Utilizzando gli strumenti di sviluppo del browser, nella scheda Rete, vedrai “200 OK”. Ciò significa che la richiesta è riuscita.</li><li>L&#39;utente visualizza un messaggio “Impossibile connettersi in modo sicuro a questa pagina”. Il messaggio spiega che ciò potrebbe essere causato perché il sito utilizza impostazioni di protezione TLS obsolete o non sicure.</li><li>Non vengono visualizzati errori di console.</li></ul>Con TLS 1.1 o 1.2 abilitato:<ul><li>Il file at.js viene scaricato.</li></ul> |
| mbox.js | Con TLS 1.0 abilitato:<ul><li>Utilizzando gli strumenti di sviluppo del browser, nella scheda Rete, vedrai “200 OK”. Ciò significa che la richiesta è riuscita.</li><li>L&#39;utente visualizza un messaggio “Impossibile connettersi in modo sicuro a questa pagina”. Il messaggio spiega che ciò potrebbe essere causato perché il sito utilizza impostazioni di protezione TLS obsolete o non sicure.</li><li>Non vengono visualizzati errori di console.</li></ul>Con TLS 1.1 o 1.2 abilitato:<ul><li>Il file mbox.js viene scaricato.</li></ul> |

### Endpoint Edge

| Implementazione JavaScript di Target | Dettagli |
|--- |--- |
| at.js | Con TLS 1.0 abilitato:<ul><li>Utilizzando gli strumenti di sviluppo del browser, nella scheda Rete, vedrai “200 OK”. Ciò significa che la richiesta è riuscita.</li><li>L&#39;utente visualizza un messaggio “Impossibile connettersi in modo sicuro a questa pagina”. Il messaggio spiega che ciò potrebbe essere causato perché il sito utilizza impostazioni di protezione TLS obsolete o non sicure.</li><li>Non vengono visualizzati errori di console.</li><li>Viene servito il contenuto predefinito.</li></ul>Con TLS 1.1 o 1.2 abilitato:<ul><li>Viene servito il contenuto dell’offerta.</li></ul> |
| mbox.js | Con TLS 1.0 abilitato:<ul><li>Utilizzando gli strumenti di sviluppo del browser, nella scheda Rete, vedrai “200 OK”. Ciò significa che la richiesta è riuscita.</li><li>L&#39;utente visualizza un messaggio “Impossibile connettersi in modo sicuro a questa pagina”. Il messaggio spiega che ciò potrebbe essere causato perché il sito utilizza impostazioni di protezione TLS obsolete o non sicure.</li><li>Non vengono visualizzati errori di console.</li><li>Viene servito il contenuto predefinito.</li></ul>Con TLS 1.1 o 1.2 abilitato:<ul><li>Viene servito il contenuto dell’offerta</li></ul> |

### Attività con targeting per il pubblico della versione del browser (Internet Explorer, versioni 6, 7 o 8)

>[!NOTE]
>
>I tipi di pubblico cessano di funzionare.

| Implementazione JavaScript di Target | Dettagli |
|--- |--- |
| at.js | at.js non è supportato nelle versioni di Internet Explorer precedenti alla versione 10. |
| mbox.js | Con TLS 1.0 abilitato:<ul><li>Viene servito il contenuto predefinito.</li><li>Non viene attivata alcuna richiesta di Target.</li><li>Non viene visualizzato alcun errore di console.</li><li>Utilizzando gli strumenti di sviluppo del browser, nella scheda Rete, vedrai “200 OK”. Ciò significa che la richiesta è riuscita.</li></ul>Con TLS 1.1 o 1.2 abilitato:<ul><li>Viene servito il contenuto dell’offerta.</li></ul> |