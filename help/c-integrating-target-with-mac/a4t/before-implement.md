---
keywords: Recommendations
description: Diverse modifiche si verificano nel processo di raccolta dei dati quando si abilita Analytics come origine della generazione di rapporti per Target (A4T).
title: Prima di implementare  Adobe Analytics come origine di reporting per  Adobe Target (A4T)
feature: a4t implementation
uuid: fe603a4b-bd61-49f4-b1b7-a0329aa905f5
translation-type: tm+mt
source-git-commit: 2619e4fb3b8548d8186e23127968ea395b07c525
workflow-type: tm+mt
source-wordcount: '903'
ht-degree: 54%

---


# Prima dell’implementazione{#before-you-implement}

Several changes occur in your data collection process when enabling [!DNL Analytics] as the reporting source for [!DNL Target] (A4T).

Prima di decidere di utilizzare questa integrazione, consulta le sezioni seguenti e considera l&#39;impatto sui processi di reporting:

## Requisiti di implementazione {#section_A0D2EF18033D4C3997B08A6EBB34C17A}

>[!IMPORTANT]
>
>Prima di iniziare a utilizzare A4T, è necessario richiedere che il tuo account sia predisposto per l’integrazione. Utilizzate il modulo [di provisioning Integrazioni](https://www.adobe.com/go/audiences) Marketing Cloud per richiedere il provisioning.

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

Download and deployment instructions are listed in [Analytics for Target Implementation](/help/c-integrating-target-with-mac/a4t/a4timplementation.md).

## Aspetti da considerare prima dell’implementazione {#section_50D49CC52E11414089C89FB67F9B88F5}

* This integration is enabled on new activities when you select to use [!DNL Analytics] as the reporting source. Dopo avere apportato le modifiche all&#39;implementazione descritte in questo documento, le attività esistenti non vengono influenzate.
* The process of setting up [!DNL Analytics] as the reporting source for [!DNL Target] includes several implementation steps, followed by a provisioning step. È opportuno rivedere l&#39;intero processo come descritto di seguito prima di procedere all&#39;implementazione. After you complete these steps, you will be ready to use [!DNL Analytics] as your reporting source as soon as it is enabled for you. Il processo di previsionamento può richiedere fino a cinque giorni lavorativi.
* L&#39; [!DNL Visitor ID service] oggetto crea una condivisione [!DNL Visitor ID] all&#39;interno dell&#39; [!DNL Adobe Experience Cloud]. Although it does not replace the [!DNL Target] mboxPC id or [!DNL Audience Manager] UUID, it does replace the way [!DNL Analytics] identifies new visitors. If set up properly, returning [!DNL Analytics] visitors should also be identified via their old [!DNL Analytics] ID to prevent visitor cliffing. Similarly, because the [!DNL Target] mboxPCid remains intact, no [!DNL Target] visitor profile data is lost when you upgrade to the [!DNL Visitor ID service].
* L&#39;operazione [!DNL Visitor ID service] deve essere eseguita prima del codice [!DNL Analytics] e della [!DNL Target] pagina. Make sure that `VisitorAPI.js` appears above the tags for all other [!DNL Experience Cloud] solutions.

## Latenza {#section_9489BE6FD21641A4844E591711E3F813}

Dopo l&#39;abilitazione di questa integrazione, è possibile che si verifichi una latenza aggiuntiva di 5-10 minuti in [!DNL Analytics]. This latency increase allows data from [!DNL Analytics] and [!DNL Target] to be stored on the same hit, allowing you to break down activities by page and site section.

This increase is reflected in all [!DNL Analytics] services and tools, including the live-stream and real-time reporting, and applies in the following scenarios:

* Per lo streaming live, i rapporti in tempo reale e le richieste API e per i dati correnti per le variabili di traffico, vengono ritardati solo gli insiemi con ID di dati supplementari.
* Per i dati correnti sulle metriche di conversione, i dati finalizzati e i feed di dati, tutti gli hit sono ritardati di altri 5-7 minuti.

Be aware that the latency increase starts after you implement the [!DNL Experience Cloud] visitor ID service, even if you have not fully implemented this integration.

## ID supplementare {#section_2C1F745A2B7D41FE9E30915539226E3A}

All [!DNL Target] calls used by an A4T activity to deliver content or record the goal metric must have a corresponding [!DNL Analytics] hit that shares the same supplemental ID for A4T to work properly.

Hits that contain data from [!DNL Analytics] and [!DNL Target] contain a supplemental data ID. You can see this ID in the [Adobe Experience Cloud Debugger](https://docs.adobe.com/content/help/en/debugger/using/experience-cloud-debugger.html) as the `sdid` parameter. Ad esempio: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`. Questo ID viene generato in qualsiasi momento siano presenti i seguenti criteri:

* È implementato il servizio ID visitatore
* È implementata una versione di [!DNL mbox.js] che supporta questa integrazione.

When [troubleshooting](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md), be sure to confirm that the supplemental ID is present on [!DNL Analytics] hits.

## Registrazione Analytics lato client {#client-side}

Per impostazione predefinita, quando at.js, [!DNL Experience Cloud Visitor ID Service] e appMeasurement.js si trovano nella pagina, [!DNL Analytics] e [!DNL Target] uniscono correttamente gli eventi a scopo di reporting e analisi, nel backend, purché l’ID supplementare corretto sia incluso dalla pagina, come indicato in precedenza. Per il corretto funzionamento di A4T non sarà necessario gestire ed eseguire altre operazioni.

Tuttavia, in alcuni casi potrebbe essere opportuno avere maggiore controllo su quando e come inviare dati analitici di [!DNL Target] a [!DNL Analytics] a scopo di reporting. Ad esempio, potreste voler usare uno strumento di analisi aziendale per scopi interni, ma anche inviare i dati di analisi a [!DNL Analytics] tramite il prodotto di analisi aziendale in modo che altri membri dell’organizzazione possano continuare a utilizzare [!DNL Analytics] come origine di reporting visiva. Per ulteriori informazioni, consulta [Passaggio 7: Includere un riferimento a at.js o mbox.js in tutte le pagine del sito](/help/c-integrating-target-with-mac/a4t/a4timplementation.md#step7) nella sezione *Implementazione di Analytics for Target*.

## Pubblico condiviso

Durante la compilazione del modulo [di provisioning Integrazioni](https://www.adobe.com/go/audiences)Marketing Cloud, tenete presente le seguenti informazioni importanti relative all&#39;opzione Pubblico  condiviso elencata in[!UICONTROL Per quali funzionalità si richiede il provisioning]?

![Modulo di richiesta](/help/c-integrating-target-with-mac/a4t/assets/request-form.png)

Quando richiedete Audience condivise, abilitate [!UICONTROL Target] e [!UICONTROL Adobe Audience Manager] (AAM) a condividere informazioni, in questo caso audience.

>[!IMPORTANT]
>
>Questa integrazione tra [!UICONTROL Target] e AAM comporta costi aggiuntivi. Sarai fatturato per ogni chiamata [!UICONTROL Target] in AAM.
