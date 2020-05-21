---
keywords: analytics for target;a4t;analytics as the reporting source
description: Utilizzando Analytics come origine per la generazione di rapporti per Target (A4T), puoi accedere ai rapporti di Analytics per le attività di Target.
title: Generazione di rapporti per A4T
subtopic: Multivariate Test
topic: Standard
uuid: bd3a7fa4-ba45-4ea3-81b6-fc2584831ce4
translation-type: tm+mt
source-git-commit: 68f356b0711abf9acf7ef631edf3656bd3dd49e3
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 45%

---


# Generazione di rapporti per A4T{#a-t-reporting}

Using [!DNL Analytics] as your reporting source for [!DNL Target] (A4T) gives you access to [!DNL Analytics] reports for your [!DNL Target] activities.

You can view reports for your activities in both [!DNL Analytics] and [!DNL Target].

For reporting best practices using [!DNL Analytics] for [!DNL Target], [visit this Adobe Spark page](https://spark.adobe.com/page/Lo3Spm4oBOvwF/).

## Panoramica {#section_035A62D65608423285D8A5A54731E2C5}

Both [!DNL Analytics] and [!DNL Target] reports measure entrants (the people who enter the tests), rather than visitors to the site.

Every time a visitor sees activity content on the page, [!DNL Target] makes a direct server-to-server call to [!DNL Analytics], including which activity and experience the visitor saw. [!DNL Target] inoltre, richiama [!DNL Analytics] ogni volta che viene effettuata la conversione. [!DNL Analytics] aggiunge la conversione come un nuovo [!DNL Analytics] evento specifico denominato &quot;Activity Conversion&quot; (Conversione attività), che viene tracciato insieme ad altri dati raccolti da [!DNL Analytics].

When the [!UICONTROL Select] operation is used and you sort on *Entrants*, then only experiences that received entrants during the selected time period are displayed in the reports.

>[!NOTE]
>
>Reports powered by [!DNL Target] have a latency of four minutes. For activities powered by A4T, in both the [!DNL Target] and [!DNL Analytics] reports, it can take up to 24 hours after the activity is initially saved before the report data can be broken down by experiences. I dati raccolti nelle prime 24 ore sono comunque precisi e vengono attribuiti all’esperienza corretta.

## Rapporti in Analytics {#section_F6884872DC864AE7913587FAED4CD11C}

In [!DNL Analytics], click **[!UICONTROL Target]** > **[!UICONTROL Target Activities]** in the left menu. In [!DNL Target], the activity&#39;s reports automatically show [!DNL Analytics] data, metrics, and segments. I dati sono visualizzati in questi rapporti circa un’ora dopo essere stati raccolti dal sito. Tutte le metriche, i destinatari e i valori nei rapporti provengono dalla suite di rapporti selezionata quando si configura l’attività.

In [!DNL Analytics], use the [!UICONTROL Target Activities] report to view the results of your [!DNL Target] activity. Test&amp;Target (Legacy) Reports provides information about your old Test&amp;Target plug-in style page integrations and does not include [!DNL Analytics] for [!DNL Target] data. In the [!UICONTROL Activities] report, view information about your [!DNL Target] experiences. Fai clic su **[!UICONTROL Metriche]**, quindi seleziona il tipo di metrica di **[!UICONTROL Target]**. Per il rapporto sono disponibili due metriche:

* **Accessi attività:**[!DNL Target] corrisponde al numero di partecipanti nel rapporto di 
* **Conversioni attività:**[!DNL Target] corrisponde al numero di conversioni personalizzate nel rapporto di 

>[!NOTE]
>
>[!DNL Target] dettagli relativi all&#39;incremento e alla confidenza sono disponibili anche in [!DNL Analytics]. Per ulteriori informazioni, vedi [Target Lift and Confidence](https://docs.adobe.com/content/help/en/analytics/components/variables/dimensions-reports/report-target-lift-confidence.html) (Incremento e confidenza *di Target) nella Guida* ai componenti diAnalytics.

>[!IMPORTANT]
>
>If your [!UICONTROL Target Activities] report in [!DNL Analytics] lists &quot;unspecified&quot; instead of listing your activities, an update is required to your provisioned account. Contatta il servizio clienti per risolvere il problema.

## Rapporti in Target {#section_C0D1F17F88374B6690BF904D7B83B42E}

When [!DNL Analytics] is used as the reporting source, reports in [!DNL Target] show the data gathered from [!DNL Analytics]. The report differs somewhat from other [!DNL Target] reports:

* The [!UICONTROL Audiences] list shows the audiences available to your [!DNL Analytics] report suite.
* The [!UICONTROL Metric] list shows every metric available through [!DNL Analytics].

   Ogni metrica è disponibile, comprese quelle personalizzate o calcolate che sono integrate in [!DNL Analytics].

   Presta attenzione al fatto che tutti i numeri in aumento appaiono nel rapporto come positivi, anche quando l’aumento è indesiderato. Ad esempio, anche se si desidera una percentuale di mancato recapito più bassa, la percentuale più elevata viene visualizzata come vincitore con l’incremento più alto. Considera queste metriche e ad altre simili, e se preferisci aumentare o diminuire i numeri, quando prendi decisioni in base ai rapporti.

You can apply the metric or audience to the report in [!DNL Target] after the activity has started, or even after the test has completed. Non devi sapere preventivamente con precisione che cosa vuoi misurare.

Click to view the full [!DNL Analytics] report directly from the activity report page.

## Rapporti in Analysis Workspace {#reports-in-analysis-workspace}

Puoi utilizzare [!DNL Adobe Analysis Workspace] per approfondire e visualizzare i dati o individuare informazioni nascoste sotto la superficie.

For detailed information and examples, open the [Analytics &amp; Target: Best Practices for Analysis tutorial](https://spark.adobe.com/page/Lo3Spm4oBOvwF/), provided by [!DNL Adobe Experience League].

## Creazione di attività {#section_311586E3FF5541E7A91D1A3CE5F9ACE3}

Durante la creazione di attività, devi specificare un obiettivo per l’attività nella pagina [!UICONTROL Impostazioni]. Questo obiettivo diventa la metrica predefinita per il rapporto e viene sempre indicato come prima opzione nel selettore delle metriche. Non puoi selezionare i segmenti per il rapporto come faresti per una normale attività di Target. A test with [!DNL Analytics] uses [!DNL Adobe Analytics] segments rather than [!DNL Target] audiences.

## Performing offline calculations for Analytics for Target (A4T) {#section_33A97A691F3A45D497DAF57A844388F0}

Puoi eseguire calcoli offline per A4T, ma è necessario un ulteriore passaggio di esportazione dei dati di [!DNL Analytics].

Per ulteriori informazioni, vedi [Esecuzione di calcoli offline per Analytics for Target (A4T)](../../c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B).
