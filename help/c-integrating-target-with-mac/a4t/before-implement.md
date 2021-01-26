---
keywords: Recommendations
description: Diverse modifiche si verificano nel processo di raccolta dei dati quando si abilita Analytics come origine della generazione di rapporti per Target (A4T).
title: Prima di implementare  Adobe Analytics come origine di reporting per  Adobe Target (A4T)
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: cf47b7f3625bb1c3430b9fba00c573f489efc448
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 54%

---


# Prima dell’implementazione{#before-you-implement}

Nel processo di raccolta dei dati si verificano diverse modifiche quando si abilita [!DNL Analytics] come origine di reporting per [!DNL Target] (A4T).

Prima di decidere di utilizzare questa integrazione, consulta le sezioni seguenti e considera l&#39;impatto sui processi di reporting:

## Requisiti di implementazione {#section_A0D2EF18033D4C3997B08A6EBB34C17A}

>[!IMPORTANT]
>
>Prima di iniziare a utilizzare A4T, è necessario richiedere che il tuo account sia predisposto per l’integrazione. Utilizzate il modulo di provisioning [Integrazioni Marketing Cloud](https://www.adobe.com/go/audiences) per richiedere il provisioning.

Questa integrazione A4T richiede l’implementazione delle seguenti versioni della libreria (o più recenti), a seconda che si desideri utilizzare o meno le offerte di reindirizzamento con A4T:

### Requisiti necessari se *non* si utilizzano offerte di reindirizzamento con A4T

Questa integrazione richiede l&#39;implementazione delle seguenti versioni della libreria (o successive) se non si prevede di utilizzare le offerte di reindirizzamento con A4T. L’ordine nell’elenco corrisponde all’ordine delle operazioni.

* [!DNL Experience Cloud Visitor ID Service]: visitorAPI.js versione 1.8.0
* [!DNL Adobe Target] (a seconda dell&#39;implementazione): at.js versione 0.9.1 o mbox.js versione 61
* Adobe Analytics: appMeasurement.js versione 1.7.0

### Requisiti necessari se si utilizzano offerte di reindirizzamento con A4T

Per utilizzare le offerte di reindirizzamento con A4T, devi implementare le seguenti versioni della libreria (o successive). L’ordine nell’elenco corrisponde all’ordine delle operazioni.

* [!DNL Experience Cloud Visitor ID Service]: visitorAPI.js versione 2.3.0
* [!DNL Adobe Target]: at.js versione 1.6.2

   **Nota:** la libreria mbox.js non supporta le offerte di reindirizzamento con A4T. L’implementazione deve utilizzare at.js.

* Adobe Analytics: appMeasurement.js versione 2.1

Le istruzioni di download e distribuzione sono elencate in [Analytics for Target Implementation](/help/c-integrating-target-with-mac/a4t/a4timplementation.md).

## Aspetti da considerare prima dell’implementazione {#section_50D49CC52E11414089C89FB67F9B88F5}

* Questa integrazione è abilitata sulle nuove attività quando si seleziona l&#39;utilizzo di [!DNL Analytics] come origine di reporting. Dopo avere apportato le modifiche all&#39;implementazione descritte in questo documento, le attività esistenti non vengono influenzate.
* Il processo di configurazione di [!DNL Analytics] come origine di reporting per [!DNL Target] include diverse fasi di implementazione, seguite da una fase di provisioning. È opportuno rivedere l&#39;intero processo come descritto di seguito prima di procedere all&#39;implementazione. Una volta completati questi passaggi, sarà possibile utilizzare [!DNL Analytics] come origine di reporting non appena questa sarà abilitata. Il processo di previsionamento può richiedere fino a cinque giorni lavorativi.
* Il [!DNL Visitor ID service] crea un [!DNL Visitor ID] condiviso all&#39;interno di [!DNL Adobe Experience Cloud]. Sebbene non sostituisca l&#39;ID [!DNL Target] mboxPC o [!DNL Audience Manager] UUID, esso sostituisce il modo in cui [!DNL Analytics] identifica i nuovi visitatori. Se la configurazione è corretta, i visitatori di ritorno [!DNL Analytics] devono essere identificati anche tramite il loro [!DNL Analytics] ID per evitare che i visitatori cali. Allo stesso modo, poiché la [!DNL Target] mboxPCid rimane intatta, nessun dato del profilo visitatore [!DNL Target] viene perso quando si esegue l&#39;aggiornamento alla [!DNL Visitor ID service].
* L&#39;esecuzione di [!DNL Visitor ID service] deve essere eseguita prima del codice di pagina [!DNL Analytics] e [!DNL Target]. Accertatevi che `VisitorAPI.js` sia visualizzato sopra i tag per tutte le altre soluzioni [!DNL Experience Cloud].

## Latenza {#section_9489BE6FD21641A4844E591711E3F813}

Dopo l&#39;abilitazione di questa integrazione, è possibile che si verifichi una latenza aggiuntiva di 5-10 minuti in [!DNL Analytics]. Questo aumento di latenza consente di memorizzare i dati di [!DNL Analytics] e [!DNL Target] sullo stesso hit, consentendo di suddividere le attività per pagina e sezione del sito.

Questo aumento si riflette in tutti i servizi e gli strumenti [!DNL Analytics], inclusi i rapporti in tempo reale e in tempo reale, e si applica nei seguenti scenari:

* Per lo streaming live, i rapporti in tempo reale e le richieste API e per i dati correnti per le variabili di traffico, vengono ritardati solo gli insiemi con ID di dati supplementari.
* Per i dati correnti sulle metriche di conversione, i dati finalizzati e i feed di dati, tutti gli hit sono ritardati di altri 5-7 minuti.

L&#39;aumento della latenza inizia dopo che hai implementato il servizio ID visitatore [!DNL Experience Cloud], anche se non hai implementato completamente questa integrazione.

## ID supplementare {#section_2C1F745A2B7D41FE9E30915539226E3A}

Tutte le [!DNL Target] chiamate utilizzate da un&#39;attività A4T per distribuire contenuto o registrare la metrica dell&#39;obiettivo devono avere un hit [!DNL Analytics] corrispondente che condivide lo stesso ID supplementare affinché A4T possa funzionare correttamente.

Gli hit che contengono dati di [!DNL Analytics] e [!DNL Target] contengono un ID dati supplementare. Potete visualizzare questo ID in [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html) come parametro `sdid`. Ad esempio: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`. Questo ID viene generato in qualsiasi momento siano presenti i seguenti criteri:

* È implementato il servizio ID visitatore
* È implementata una versione di [!DNL mbox.js] che supporta questa integrazione.

Quando [risoluzione dei problemi](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md), verificare che l&#39;ID supplementare sia presente negli hit [!DNL Analytics].

## Registrazione Analytics lato client {#client-side}

Per impostazione predefinita, quando at.js, [!DNL Experience Cloud Visitor ID Service] e appMeasurement.js si trovano nella pagina, [!DNL Analytics] e [!DNL Target] uniscono correttamente gli eventi a scopo di reporting e analisi, nel backend, purché l’ID supplementare corretto sia incluso dalla pagina, come indicato in precedenza. Per il corretto funzionamento di A4T non sarà necessario gestire ed eseguire altre operazioni.

Tuttavia, in alcuni casi potrebbe essere opportuno avere maggiore controllo su quando e come inviare dati analitici di [!DNL Target] a [!DNL Analytics] a scopo di reporting. Ad esempio, potreste voler usare uno strumento di analisi aziendale per scopi interni, ma anche inviare i dati di analisi a [!DNL Analytics] tramite il prodotto di analisi aziendale in modo che altri membri dell’organizzazione possano continuare a utilizzare [!DNL Analytics] come origine di reporting visiva. Per ulteriori informazioni, consulta [Passaggio 7: Includere un riferimento a at.js o mbox.js in tutte le pagine del sito](/help/c-integrating-target-with-mac/a4t/a4timplementation.md#step7) nella sezione *Implementazione di Analytics for Target*.

## Pubblico condiviso

Durante la compilazione del [modulo di provisioning integrazioni di Marketing Cloud](https://www.adobe.com/go/audiences), prendere nota delle seguenti informazioni importanti relative all&#39;opzione [!UICONTROL Audience condivise] elencata in &quot;[!UICONTROL Per quali funzionalità si richiede il provisioning]?&quot;

![Modulo di richiesta](/help/c-integrating-target-with-mac/a4t/assets/request-form.png)

Quando richiedete [!UICONTROL Audience condivise], abilitate [!UICONTROL Target] e [!UICONTROL Adobe Audience Manager] (AAM) per condividere le informazioni, in questo caso i tipi di pubblico.

>[!IMPORTANT]
>
>Questa integrazione tra [!UICONTROL Target] e AAM comporta costi aggiuntivi. Sarai fatturato per ogni chiamata [!UICONTROL Target] in AAM.
