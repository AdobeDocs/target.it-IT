---
keywords: implementazione;libreria javascript;js;atjs;decisionale su dispositivo;decisionale su dispositivo;at.js;on-device;on device
description: Scopri come eseguire le decisioni sul dispositivo con la libreria at.js
title: Come funziona il Decisioning su dispositivo con la libreria JavaScript at.js?
feature: at.js
role: Developer
exl-id: 5ad6032b-9865-4c80-8800-705673657286
source-git-commit: a0a20b99a76ba0346f00e3841a345e916ffde8ea
workflow-type: tm+mt
source-wordcount: '3552'
ht-degree: 18%

---

# Decisioni sul dispositivo per at.js

A partire dalla versione 2.5.0, at.js offre funzioni decisionali sul dispositivo. Le decisioni sul dispositivo consentono di memorizzare nella cache [Test A/B](/help/main/c-activities/t-test-ab/test-ab.md) e [Targeting esperienza](/help/main/c-activities/t-experience-target/experience-target.md) (XT) attività sul browser per eseguire decisioni in memoria senza una richiesta di rete di blocco al [!DNL Adobe Target] Rete Edge.

[!DNL Target] offre anche la flessibilità di fornire l&#39;esperienza più pertinente e aggiornata dalle attività di personalizzazione basate sulla sperimentazione e sull&#39;apprendimento automatico (basate su ML) tramite una chiamata al server live. In altre parole, quando le prestazioni sono più importanti, puoi scegliere di utilizzare le decisioni sul dispositivo. Tuttavia, quando è necessaria l’esperienza più pertinente, aggiornata e basata su ML, è possibile effettuare una chiamata al server.

## Quali sono i vantaggi delle decisioni su dispositivi?

I vantaggi delle decisioni sul dispositivo includono:

* **Consegnare decisioni ed esperienze veloci.** Il bucket e le decisioni vengono eseguiti in memoria e sul browser per evitare di bloccare le richieste di rete.
* **Migliorare le prestazioni dell&#39;applicazione.** Esegui esperimenti e distribuisci personalizzazioni ai tuoi clienti e utenti senza compromettere le esperienze degli utenti finali.
* **Migliorare il punteggio di qualità del sito Google.** Con le decisioni che avvengono in memoria, migliora il punteggio Google Site Quality della tua attività online per renderla più individuabile dai consumatori.
* **Scopri le funzioni di analisi in tempo reale.** Acquisisci informazioni sulle prestazioni dell’attività in tempo reale tramite [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) Generazione di rapporti (A4T). A4T consente di eseguire il pivot della strategia in momenti critici.

## Funzioni supportate

L’SDK di Adobe Target JS offre ai clienti la flessibilità di scegliere tra prestazioni e aggiornamento dei dati per le decisioni. In altre parole, se la distribuzione di contenuti personalizzati più rilevanti e coinvolgenti tramite l’apprendimento automatico è per te più importante, è necessario effettuare una chiamata al server live. Ma quando le prestazioni sono più importanti, è necessario prendere una decisione su dispositivo e in memoria. Per il corretto funzionamento delle decisioni sul dispositivo, consulta l’elenco delle funzioni supportate:

* Tipi di attività
* Targeting del pubblico
* Metodo di allocazione

Per ulteriori informazioni, consulta [Funzioni supportate per le decisioni su dispositivi](https://developer.adobe.com/target/implement/client-side/atjs/on-device-decisioning/supported-features/).

## Come funziona il processo decisionale su dispositivo?

Quando distribuisci e inizializzi at.js con le decisioni sui dispositivi abilitate, un [artefatto delle regole](https://developer.adobe.com/target/implement/client-side/atjs/on-device-decisioning/rule-artifact/){target=_blank} che include le decisioni sul dispositivo per attività, tipi di pubblico e risorse A/B e XT, viene scaricato dal CDN Akamai più vicino al visitatore e memorizzato nella cache locale sul browser del visitatore. Quando viene effettuata una richiesta da at.js per recuperare un’esperienza, la decisione relativa all’esperienza da restituire viene presa in memoria, in base ai metadati codificati nell’artefatto della regola nella cache.

## Metodo di decisione

Con le decisioni sul dispositivo, [!DNL Target] introduce una nuova impostazione denominata [!UICONTROL Decisioning, metodo]. La [!UICONTROL Decisioning, metodo] imposta il modo in cui at.js distribuisce le esperienze. [!UICONTROL Decisioning, metodo] ha tre valori:

* [!UICONTROL Solo lato server]
* [!UICONTROL Solo su dispositivo]
* [!UICONTROL Ibrido]

### Solo lato server

[!UICONTROL Solo lato server] è il metodo decisionale predefinito impostato automaticamente quando at.js 2.5.0+ viene implementato e distribuito sulle proprietà web.

Se si utilizza [!UICONTROL Solo lato server] come configurazione predefinita, tutte le decisioni vengono prese sulla rete Edge di [!DNL Target], il che comporta una chiamata di blocco al server. Questo approccio può introdurre una latenza incrementale, ma offre anche vantaggi significativi, come la possibilità di applicare le funzionalità di machine learning di Target, come le attività [Consigli](/help/main/c-recommendations/recommendations.md), [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) e [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md).

Inoltre, l’ottimizzazione delle esperienze personalizzate mediante l’utilizzo del profilo utente di Target (che viene mantenuto tra sessioni e canali diversi) può fornire risultati molto efficaci per la tua azienda.

Infine, [!UICONTROL Solo lato server] consente di utilizzare Adobe Experience Cloud e di perfezionare i tipi di pubblico a cui rivolgersi grazie ai segmenti di Audience Manager e Adobe Analytics.

Il diagramma seguente illustra l’interazione tra il visitatore, il browser, at.js 2.5.0+ e la rete Adobe Target Edge. Questo diagramma di flusso acquisisce nuovi visitatori e visitatori di ritorno.

![Diagramma di flusso solo lato server](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/server-side-only.png)

L’elenco seguente corrisponde ai numeri nel diagramma:

| Passaggio | Descrizione |
| --- | --- |
| 1 | La [!DNL Experience Cloud Visitor ID] viene recuperato da [Servizio Adobe Experience Cloud Identity](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en). |
| 2 | La libreria at.js viene caricata in modo sincrono e nasconde il corpo del documento.<br>   La libreria at.js può anche essere caricata in modo asincrono con un frammento pre-hiding facoltativo implementato nella pagina. |
| 3 | La libreria at.js nasconde il corpo per evitare sfarfallii. |
| 4 | Viene effettuata una richiesta di caricamento pagina che include tutti i parametri configurati, ad esempio (ECID, ID cliente, parametri personalizzati, profilo utente e così via). |
| 5 | Gli script di profilo vengono eseguiti e quindi inseriti nell’archivio profili.<br>L’archivio profili richiede tipi di pubblico idonei dalla libreria Pubblico (ad esempio, tipi di pubblico condivisi da [!DNL Adobe Analytics], [!DNL Adobe Audience Manager]e così via).<br>Gli attributi del cliente vengono inviati all’archivio profili in un processo batch. |
| 6 | L’archivio profili viene utilizzato per la qualifica del pubblico e il bucket per filtrare le attività. |
| 7 | Il contenuto risultante viene selezionato dopo che l’esperienza è stata determinata dal live [!DNL Target] attività. |
| 8 | La libreria at.js nasconde gli elementi corrispondenti nella pagina associati all’esperienza di cui è necessario eseguire il rendering. |
| 9 | La libreria at.js visualizza il corpo in modo che il resto della pagina possa essere caricato perché il visitatore possa visualizzarlo. |
| 10 | La libreria at.js gestisce il DOM per eseguire il rendering dell’esperienza dalla rete Edge di Target. |
| 11 | Viene eseguito il rendering dell’esperienza per il visitatore. |
| 12 | Viene caricata l’intera pagina web. |
| 13 | I dati [!DNL Analytics] vengono inviati ai server di raccolta dati. |
| 14 | Ai dati di destinazione corrisponde [!DNL Analytics] i dati tramite SDID e vengono elaborati nel [!DNL Analytics] archiviazione dei rapporti. I dati di [!DNL Analytics] possono quindi essere visualizzati sia in [!DNL Analytics] che in [!DNL Target] tramite i rapporti [!UICONTROL Analytics for Target] (A4T). |

### Solo su dispositivo

[!UICONTROL Solo su dispositivo] è il metodo decisionale che deve essere impostato in at.js 2.5.0+ quando le decisioni su dispositivo devono essere utilizzate solo in tutte le pagine web.

Le decisioni sul dispositivo possono fornire esperienze e attività di personalizzazione a una velocità sorprendente, perché derivano da un artefatto di regole memorizzate nella cache che contiene tutte le attività che si qualificano per le decisioni sul dispositivo.

Per ulteriori informazioni sulle attività idonee per le decisioni su dispositivi, consulta [Funzioni supportate nelle decisioni su dispositivi](https://developer.adobe.com/target/implement/client-side/atjs/on-device-decisioning/supported-features/).

Questo metodo decisionale deve essere utilizzato solo se le prestazioni sono altamente critiche in tutte le pagine che richiedono decisioni da [!DNL Target]. Inoltre, ricorda che quando viene selezionato questo metodo decisionale, le attività [!DNL Target] che non possono avvalersi delle decisioni su dispositivo non verranno consegnate o eseguite. La libreria at.js 2.5.0+ è configurata per cercare solo l’artefatto delle regole memorizzate nella cache per prendere decisioni.

Il diagramma seguente illustra l’interazione tra il visitatore, il browser, at.js 2.5.0+ e la rete CDN di Akamai. La rete CDN di Akamai memorizza in cache l’artefatto delle regole per la prima visita del visitatore. Per la prima visita di pagina per un nuovo visitatore, l’artefatto delle regole JSON deve essere scaricato dalla rete CDN Akamai per essere memorizzato nella cache locale sul browser del visitatore. Una volta scaricato l’artifact delle regole JSON, la decisione viene presa immediatamente senza una chiamata di rete di blocco. Il diagramma di flusso seguente acquisisce nuovi visitatori.

![Diagramma di flusso solo su dispositivo](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-only.png)

L’elenco seguente corrisponde ai numeri nel diagramma:

>[!NOTE]
>
>[!DNL Adobe Target] I server di amministrazione qualificano tutte le attività idonee per le decisioni sui dispositivi, generano l’artefatto delle regole JSON e lo propagano alla rete CDN Akamai. Le tue attività sono costantemente monitorate per verificare la disponibilità di aggiornamenti per restituire un nuovo artefatto di regole JSON da propagare alla rete CDN Akamai.

| Passaggio | Descrizione |
| --- | --- |
| 1 | La [!DNL Experience Cloud Visitor ID] viene recuperato da [Servizio Adobe Experience Cloud Identity](https://experienceleague.adobe.com/docs/id-service/using/home.html). |
| 2 | La libreria at.js viene caricata in modo sincrono e nasconde il corpo del documento.<br>La libreria at.js può anche essere caricata in modo asincrono con un frammento pre-hiding facoltativo implementato nella pagina. |
| 3 | La libreria at.js nasconde il corpo per evitare sfarfallii. |
| 4 | La libreria at.js effettua una richiesta per recuperare l’artefatto della regola JSON dal CDN Akamai più vicino al visitatore. |
| 5 | La rete CDN di Akamai risponde con l’artefatto della regola JSON. |
| 6 | L’artefatto della regola JSON viene memorizzato nella cache locale sul browser del visitatore. |
| 7 | La libreria at.js interpreta l’artefatto della regola JSON ed esegue la decisione di recuperare l’esperienza e nasconde gli elementi testati. |
| 8 | La libreria at.js visualizza il corpo in modo che il resto della pagina possa essere caricato perché il visitatore possa visualizzarlo. |
| 9 | La libreria at.js manipola il DOM per eseguire il rendering dell’esperienza dall’artefatto della regola JSON memorizzato nella cache. |
| 10 | Viene eseguito il rendering dell’esperienza per il visitatore. |
| 11 | Viene caricata l’intera pagina web. |
| 12 | I dati [!DNL Analytics] vengono inviati ai server di raccolta dati. Ai dati di destinazione corrisponde [!DNL Analytics] i dati tramite SDID e vengono elaborati nel [!DNL Analytics] archiviazione dei rapporti. [!DNL Analytics][!DNL Analytics]I dati di possono quindi essere visualizzati sia in che in tramite i rapporti Analytics for Target (A4T).[!DNL Target] |

Il diagramma seguente illustra l’interazione tra il visitatore, il browser, at.js 2.5.0+ e l’artefatto della regola JSON memorizzata nella cache per l’hit di pagina o la visita di ritorno del visitatore successivo. Poiché l’artifact delle regole JSON è già memorizzato nella cache e disponibile nel browser, la decisione viene presa immediatamente senza una chiamata di rete di blocco. Questo diagramma di flusso acquisisce la navigazione delle pagine successive o i visitatori di ritorno.

![Diagramma di flusso solo su dispositivo per la navigazione delle pagine successive e le visite ripetute](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-only-subsequent.png)

L’elenco seguente corrisponde ai numeri nel diagramma:

>[!NOTE]
>
>[!DNL Adobe Target] I server di amministrazione qualificano tutte le attività idonee per le decisioni sui dispositivi, generano l’artefatto delle regole JSON e lo propagano alla rete CDN Akamai. Le tue attività sono costantemente monitorate per verificare la disponibilità di aggiornamenti per restituire un nuovo artefatto di regole JSON da propagare alla rete CDN Akamai.

| Passaggio | Descrizione |
| --- | --- |
| 1 | La [!DNL Experience Cloud Visitor ID] viene recuperato da [Servizio Adobe Experience Cloud Identity](https://experienceleague.adobe.com/docs/id-service/using/home.html). |
| 2 | La libreria at.js viene caricata in modo sincrono e nasconde il corpo del documento.<br>La libreria at.js può anche essere caricata in modo asincrono con un frammento pre-hiding facoltativo implementato nella pagina. |
| 3 | La libreria at.js nasconde il corpo per evitare sfarfallii. |
| 4 | La libreria at.js interpreta l’artefatto della regola JSON ed esegue la decisione in memoria per recuperare l’esperienza. |
| 5 | Gli elementi testati sono nascosti. |
| 6 | La libreria at.js visualizza il corpo in modo che il resto della pagina possa essere caricato perché il visitatore possa visualizzarlo. |
| 7 | La libreria at.js manipola il DOM per eseguire il rendering dell’esperienza dall’artefatto della regola JSON memorizzato nella cache. |
| 8 | Viene eseguito il rendering dell’esperienza per il visitatore. |
| 9 | Viene caricata l’intera pagina web. |
| 10 | I dati [!DNL Analytics] vengono inviati ai server di raccolta dati. Ai dati di destinazione corrisponde [!DNL Analytics] i dati tramite SDID e vengono elaborati nel [!DNL Analytics] archiviazione dei rapporti. I dati di [!DNL Analytics] possono quindi essere visualizzati sia in [!DNL Analytics] che in [!DNL Target] tramite i rapporti [!UICONTROL Analytics for Target] (A4T). |

### Ibrido

[!UICONTROL Ibrido] è il metodo decisionale che deve essere impostato in at.js 2.5.0+ quando è necessario eseguire sia le decisioni su dispositivo che le attività che richiedono una chiamata alla rete Edge di Adobe Target.

Quando gestisci sia le attività di decisione su dispositivo che quelle lato server, può essere un po’ complicato e noioso pensare a come distribuire ed eseguire il provisioning di [!DNL Target] sulle pagine. Con il metodo decisionale ibrido, [!DNL Target] sa quando deve effettuare una chiamata al server alla rete Edge di Adobe Target per le attività che richiedono l’esecuzione lato server e anche quando eseguire solo le decisioni su dispositivo.

L’artefatto delle regole JSON include i metadati che informano at.js se una mbox ha un’attività lato server in esecuzione o un’attività decisionale su dispositivo. Questo metodo decisionale assicura che le attività che intendi consegnare rapidamente vengano eseguite tramite le decisioni su dispositivo, e che quelle che richiedono una personalizzazione basata su ML più potente vengano eseguite tramite la rete Edge di Adobe Target.

Il diagramma seguente illustra l’interazione tra il visitatore, il browser, at.js 2.5.0+, la rete CDN di Akamai e la rete Adobe Target Edge per un nuovo visitatore che visita la pagina per la prima volta. Il vantaggio di questo diagramma è che l’artefatto delle regole JSON viene scaricato in modo asincrono mentre le decisioni vengono prese tramite la rete Adobe Target Edge.

Questo approccio assicura che le dimensioni dell’artefatto, che possono includere molte attività, non influenzino negativamente la latenza della decisione. Il download dell’artefatto delle regole JSON in modo sincrono e la decisione successiva possono avere effetti negativi sulla latenza e possono essere incoerenti. Pertanto, il metodo di decisione ibrido è una raccomandazione di best practice per effettuare sempre una chiamata lato server per la decisione di un nuovo visitatore e quando l’artefatto delle regole JSON viene memorizzato nella cache in parallelo. Per qualsiasi visita di pagina successiva e visita di ritorno, le decisioni vengono prese dalla cache e in memoria tramite l’artefatto delle regole JSON.

![Diagramma di flusso ibrido per un nuovo visitatore](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/hybrid-first-time-visitor.png)

L’elenco seguente corrisponde ai numeri nel diagramma:

>[!NOTE]
>
>[!DNL Adobe Target] I server di amministrazione qualificano tutte le attività idonee per le decisioni sui dispositivi, generano l’artefatto delle regole JSON e lo propagano alla rete CDN Akamai. Le tue attività sono costantemente monitorate per verificare la disponibilità di aggiornamenti per restituire un nuovo artefatto di regole JSON da propagare alla rete CDN Akamai.

| Passaggio | Descrizione |
| --- | --- |
| 1 | La [!DNL Experience Cloud Visitor ID] viene recuperato da [Servizio Adobe Experience Cloud Identity](https://experienceleague.adobe.com/docs/id-service/using/home.html). |
| 2 | La libreria at.js viene caricata in modo sincrono e nasconde il corpo del documento.<br>La libreria at.js può anche essere caricata in modo asincrono con un frammento pre-hiding facoltativo implementato nella pagina. |
| 3 | La libreria at.js nasconde il corpo per evitare sfarfallii. |
| 4 | Viene effettuata una richiesta di caricamento pagina ad Adobe Target Edge Network, con tutti i parametri configurati come (ECID, ID cliente, parametri personalizzati, profilo utente e così via). |
| 5 | In parallelo, at.js invia una richiesta per recuperare l’artefatto della regola JSON dal CDN Akamai più vicino al visitatore. |
| 6 | (Adobe Target Edge Network) Gli script di profilo vengono eseguiti e quindi inseriti nell’archivio profili. L’archivio profili richiede tipi di pubblico idonei dalla libreria Pubblico (ad esempio, tipi di pubblico condivisi da [!DNL Adobe Analytics], [!DNL Adobe Audience Manager]e così via). |
| 7 | La rete CDN di Akamai risponde con l’artefatto della regola JSON. |
| 8 | L’archivio profili viene utilizzato per la qualifica del pubblico e il bucket per filtrare le attività. |
| 9 | Il contenuto risultante viene selezionato dopo che l’esperienza è stata determinata dal live [!DNL Target] attività. |
| 10 | La libreria at.js nasconde gli elementi corrispondenti nella pagina associati all’esperienza di cui è necessario eseguire il rendering. |
| 11 | La libreria at.js visualizza il corpo in modo che il resto della pagina possa essere caricato perché il visitatore possa visualizzarlo. |
| 12 | La libreria at.js gestisce il DOM per eseguire il rendering dell’esperienza dalla rete Edge di Target. |
| 13 | Viene eseguito il rendering dell’esperienza per il visitatore. |
| 14 | Viene caricata l’intera pagina web. |
| 15 | I dati [!DNL Analytics] vengono inviati ai server di raccolta dati. Ai dati di destinazione corrisponde [!DNL Analytics] i dati tramite SDID e vengono elaborati nel [!DNL Analytics] archiviazione dei rapporti. I dati di [!DNL Analytics] possono quindi essere visualizzati sia in [!DNL Analytics] che in [!DNL Target] tramite i rapporti [!UICONTROL Analytics for Target] (A4T). |

Il diagramma seguente illustra l’interazione tra il visitatore, il browser, at.js 2.5.0+ e l’artefatto delle regole JSON memorizzate nella cache per una navigazione di pagina successiva o una visita di ritorno. In questo diagramma, fai particolare attenzione solo al caso d’uso in cui viene presa una decisione sul dispositivo per la navigazione o la visita di ritorno della pagina successiva. Tieni presente che a seconda delle attività live per determinate pagine, puoi effettuare una chiamata lato server per eseguire decisioni lato server.

![Diagramma di flusso ibrido per la navigazione delle pagine successive e le visite ripetute](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/hybrid-subsequent.png)

L’elenco seguente corrisponde ai numeri nel diagramma:

>[!NOTE]
>
>[!DNL Adobe Target] I server di amministrazione qualificano tutte le attività idonee per le decisioni sui dispositivi, generano l’artefatto delle regole JSON e lo propagano alla rete CDN Akamai. Le tue attività sono costantemente monitorate per verificare la disponibilità di aggiornamenti per restituire un nuovo artefatto di regole JSON da propagare alla rete CDN Akamai.

| Passaggio | Descrizione |
| --- | --- |
| 1 | La [!DNL Experience Cloud Visitor ID] viene recuperato da [Servizio Adobe Experience Cloud Identity](https://experienceleague.adobe.com/docs/id-service/using/home.html). |
| 2 | La libreria at.js viene caricata in modo sincrono e nasconde il corpo del documento.<br>La libreria at.js può anche essere caricata in modo asincrono con un frammento pre-hiding facoltativo implementato nella pagina. |
| 3 | La libreria at.js nasconde il corpo per evitare sfarfallii. |
| 4 | Viene effettuata una richiesta per recuperare un’esperienza. |
| 5 | La libreria at.js conferma che l’artefatto della regola JSON è già stato memorizzato nella cache ed esegue la decisione in memoria di recuperare l’esperienza. |
| 6 | Gli elementi testati sono nascosti. |
| 7 | La libreria at.js visualizza il corpo in modo che il resto della pagina possa essere caricato perché il visitatore possa visualizzarlo. |
| 8 | La libreria at.js manipola il DOM per eseguire il rendering dell’esperienza dall’artefatto della regola JSON memorizzato nella cache. |
| 9 | Viene eseguito il rendering dell’esperienza per il visitatore. |
| 10 | Viene caricata l’intera pagina web. |
| 11 | I dati [!DNL Analytics] vengono inviati ai server di raccolta dati. Ai dati di destinazione corrisponde [!DNL Analytics] i dati tramite SDID e vengono elaborati nel [!DNL Analytics] archiviazione dei rapporti. I dati di [!DNL Analytics] possono quindi essere visualizzati sia in [!DNL Analytics] che in [!DNL Target] tramite i rapporti [!UICONTROL Analytics for Target] (A4T). |

## Come si abilitano le decisioni sul dispositivo?

Le decisioni sul dispositivo sono disponibili per tutti [!DNL Target] clienti che utilizzano at.js 2.5.0+.

Per abilitare le decisioni sul dispositivo:

>[!NOTE]
>
>Devi avere la [!UICONTROL Amministratore] o [!UICONTROL Approvatore] [ruolo utente](/help/main/administrating-target/c-user-management/user-management.md) per attivare o disattivare l&#39;interruttore On-Device Decisioning.

1. Fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]** > **[!UICONTROL Dettagli account]**.
1. Sotto **[!UICONTROL Dettagli account]**, scivolare il **[!UICONTROL Decisioning su dispositivo]** passa alla posizione &quot;on&quot;.

   ![Attiva/disattiva le decisioni sul dispositivo](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-decisioning-toggle.png)

   &quot;[!UICONTROL Includi tutte le attività qualificate esistenti per le decisioni sul dispositivo nell&#39;artefatto]&quot; viene visualizzata se abiliti le decisioni sul dispositivo.
1. (Condizionale) Fai scorrere l’interruttore nella posizione &quot;on&quot; se desideri che tutte le attività di Target live idonee per le decisioni sul dispositivo siano incluse automaticamente nell’artefatto.

   Se questa opzione è disattivata, è necessario ricreare e attivare tutte le attività di decisione sul dispositivo affinché siano incluse nell’artefatto delle regole generate. In altre parole, qualsiasi attività in stato live prima di attivare [!UICONTROL Decisioning su dispositivo] l’opzione non è inclusa nell’artefatto delle regole.

Dopo aver abilitato la [!UICONTROL Decisioning su dispositivo] interruttore, [!DNL Target] inizia a generare e a propagarsi [artefatti delle regole](https://developer.adobe.com/target/implement/client-side/atjs/on-device-decisioning/rule-artifact/){target=_blank} per il client.

>[!IMPORTANT]
>
>Assicurati di attivare l&#39;interruttore prima di inizializzare l&#39;SDK di Adobe Target per l&#39;utilizzo delle decisioni sui dispositivi. Gli artefatti della regola devono prima generare e propagarsi ai CDN di Akamai per il funzionamento delle decisioni sui dispositivi. La propagazione può richiedere da cinque a dieci minuti perché il primo artefatto della regola generi e si propaghi alla rete CDN Akamai.

## Come si configura at.js 2.5.0+ per l’utilizzo delle decisioni sul dispositivo?

1. Fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]** > **[!UICONTROL Dettagli account]**.
1. Sotto **[!UICONTROL Metodi di Implementazione]** > **[!UICONTROL Metodo di implementazione principale]**, fai clic su **[!UICONTROL Modifica]** accanto alla versione at.js (deve essere at.js 2.5.0 o successiva).

   ![Modificare le impostazioni del metodo di implementazione principale](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/main-implementation-method.png)

   >[!IMPORTANT]
   >
   >Prima di modificare queste impostazioni predefinite, consulta l’Assistenza clienti in modo da non influenzare l’implementazione corrente.

1. Selezionare il metodo decisionale desiderato:

   * [!UICONTROL Solo lato server]
   * [!UICONTROL Solo su dispositivo]
   * [!UICONTROL Ibrido]

   ![Modificare il pannello delle impostazioni di at.js](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/global-settings.png)

### Impostazioni globali

È possibile configurare un valore predefinito [!UICONTROL Decisioning, metodo] per tutti [!DNL Target] decisioni. I vari metodi decisionali sono [!UICONTROL Solo lato server], [!UICONTROL Solo su dispositivo]e [!UICONTROL Ibrido]. Il metodo decisionale selezionato nell&#39;interfaccia utente di Target è configurato in `window.targetGlobalSettings` in `decisioningMethod` campo . Ulteriori informazioni sulle `decisioningMethod` in [targetGlobalSettings()](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/).

```javascript
<head> 
    <script type="text/javascript">

        window.targetGlobalSettings = { 
            clientCode: "yourClientCodeHere", 
            imsOrgId: "imsOrgId@AdobeOrg", 
            decisioningMethod: "on-device"

        }; 
    </script>

    <script type="text/javascript" src="at.js"></script> 
</head>
```

### Impostazione personalizzata

Se imposti la `decisioningMethod` in `window.targetGlobalSettings`, ma desidera ignorare il `decisioningMethod` per ogni decisione di Adobe Target in base al tuo caso d’uso, puoi eseguire questa procedura specificando `decisioningMethod` in at.js 2.5.0+’s [getOffers()](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-getoffers-atjs-2/)Chiamata {target=_blank}.

```javascript
adobe.target.getOffers({ 

  decisioningMethod:"on-device", 
  request: { 
    execute: { 
      mboxes: [ 
        { 
          index: 0, 
          name: "homepage" 
        } 
      ] 
    } 
 } 
});
```

>[!NOTE]
>
>Per utilizzare &quot;on-device&quot; o &quot;ibrido&quot; come metodo decisionale nella chiamata getOffers() , assicurati che l’impostazione globale abbia `decisioningMethod` come &quot;on-device&quot; o &quot;ibrido&quot;. La libreria at.js 2.5.0+ deve sapere se scaricare e memorizzare nella cache l’artefatto delle regole JSON immediatamente dopo il caricamento sulla pagina. Se il metodo decisionale per l’impostazione globale è impostato su &quot;lato server&quot; e il metodo decisionale &quot;sul dispositivo&quot; o &quot;ibrido&quot; viene passato nella chiamata getOffers() , at.js 2.5.0+ non avrà l’artefatto della regola JSON memorizzato nella cache per eseguire le decisioni sul dispositivo.

### TTL della cache degli artefatti

[!DNL Target] rappresenta le attività idonee per le decisioni sul dispositivo come un artefatto costituito da metadati, regole e condizioni. Questo artefatto è memorizzato nella cache della rete CDN Akamai. Durante la prima visita dell’utente, il browser dell’utente scarica e memorizza in cache l’artefatto che rappresenta le attività di decisione sul dispositivo.

Nelle visite successive al sito, il browser controlla automaticamente se deve scaricare una versione più recente dell’artefatto. Questo controllo aggiunge latenza. Il TTL della cache degli artefatti definisce il numero di minuti che non si desidera che il browser verifichi la presenza di un artefatto aggiornato dall&#39;ultimo download riuscito. Più è lungo l&#39;intervallo di tempo, migliori sono le prestazioni. Più breve è l&#39;intervallo di tempo, migliore è la freschezza dei dati, ma al costo di una maggiore latenza.

## Come faccio a sapere che un&#39;attività è idonea per le decisioni sui dispositivi?

Dopo aver creato un’attività che può essere considerata idonea per le decisioni sui dispositivi, un’etichetta che legge [!UICONTROL Decisioning on-Device Idoneo], è visibile nel [!UICONTROL Panoramica] pagina.

![Etichetta Idonea di On-Device Decisioning nella pagina Panoramica dell’attività.](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-decisioning-eligible-label.png)

Questa etichetta non significa che l’attività verrà sempre consegnata tramite decisioni sul dispositivo. Solo quando at.js 2.5.0+ è configurato per utilizzare le decisioni sul dispositivo, questa attività verrà eseguita sul dispositivo. Se at.js 2.5.0+ non è configurato per l’utilizzo sul dispositivo, questa attività verrà comunque recapitata tramite una chiamata al server effettuata da at.js.

Puoi filtrare tutte le attività che richiedono decisioni su dispositivi idonee per la [!UICONTROL Attività] tramite [!UICONTROL Decisioning on-Device Idoneo] filtro.

![Filtro idoneo di On-Device Decisioning nella pagina Attività.](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-decisioning-filter.png)

>[!NOTE]
>
>Dopo aver creato e attivato un’attività che può essere considerata idonea per le decisioni dei dispositivi, l’inclusione di un’attività nelle regole generata e propagata al punto di presenza CDN di Akamai può richiedere da cinque a dieci minuti.

## Riepilogo dei passaggi per garantire che le mie attività decisionali su dispositivi vengano distribuite tramite At.js 2.5.0+?

1. Accedi all’interfaccia utente di Adobe Target e passa a **[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]** > **[!DNL Account Details]** per abilitare **[!UICONTROL Decisioning su dispositivo]** alternare.
1. Abilita la **&quot;[!UICONTROL Includi tutte le attività qualificate esistenti per le decisioni sul dispositivo nell&#39;artefatto]&quot;** alternare.

   La prima generazione di artifact delle regole JSON può richiedere fino a 10 minuti.

1. Crea e attiva un [tipo di attività supportato dalle decisioni sul dispositivo](https://developer.adobe.com/target/implement/client-side/atjs/on-device-decisioning/supported-features/)e verifica che le decisioni sul dispositivo siano idonee.
1. Imposta la **[!UICONTROL Decisioning, metodo]** a **[!UICONTROL &quot;Ibrido&quot;]** o **[!UICONTROL &quot;Solo su dispositivo&quot;]** tramite l’interfaccia utente delle impostazioni di at.js.
1. Scarica e distribuisci at.js 2.5.0+ nelle tue pagine.
