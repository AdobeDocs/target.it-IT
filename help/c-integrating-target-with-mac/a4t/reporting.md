---
keywords: analytics for target;a4t;analytics as the reporting source
description: Utilizzando Analytics come origine per la generazione di rapporti per Target (A4T), puoi accedere ai rapporti di Analytics per le attività di Target.
title: Generazione di rapporti per A4T
feature: a4t reports
subtopic: Multivariate Test
topic: Standard
uuid: bd3a7fa4-ba45-4ea3-81b6-fc2584831ce4
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 36%

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

## Rapporti in Analytics {#analytics}

In [!DNL Analytics], dopo l&#39;abilitazione dell&#39;integrazione A4T sono disponibili diverse dimensioni e metriche.

### Dimensioni

* [!UICONTROL Analytics per Target] - L&#39;ID principale trasmesso tramite l&#39;integrazione. Il formato di questa dimensione è `Activity ID:Experience ID:3rd ID`. Le seguenti dimensioni sono classificazioni di questa dimensione.
* [!UICONTROL Attività Target]
* [!UICONTROL Esperienze Target]
* [!UICONTROL Attività] Target > [!UICONTROL Esperienza]
* [!UICONTROL 3° ID] : può essere ignorato

### Metrics (Metriche)

* [!UICONTROL Impression] attività - Corrisponde al numero di [!UICONTROL partecipanti] nel [!DNL Target] rapporto.
* [!UICONTROL Conversioni] attività - Corrisponde al numero di conversioni  personalizzate presente nel [!DNL Target] rapporto.

In [!DNL Analysis Workspace]questa sezione, utilizzate il pannello [!UICONTROL Analytics for Target] per analizzare le [!DNL Target] attività e le esperienze in modo più sicuro. Per ulteriori informazioni, vedi Pannello [di](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/a4t-panel.html) Analytics per Target (A4T) nella Guida *agli strumenti di* Analytics.

>[!IMPORTANT]
>
>If your [!UICONTROL Target Activities] report in [!DNL Analytics] lists &quot;unspecified&quot; instead of listing your activities, an update is required to your provisioned account. Contatta il servizio clienti per risolvere il problema.

For detailed information and examples, open the [Analytics &amp; Target: Best Practices for Analysis](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) tutorial, provided by Adobe Experience League.

## Rapporti in Target {#section_C0D1F17F88374B6690BF904D7B83B42E}

When [!DNL Analytics] is used as the reporting source, reports in [!DNL Target] show the data gathered from [!DNL Analytics]. The report differs somewhat from other [!DNL Target] reports:

* The [!UICONTROL Audiences] list shows the audiences available to your [!DNL Analytics] report suite.
* The [!UICONTROL Metric] list shows every metric available through [!DNL Analytics].

   Ogni metrica è disponibile, comprese quelle personalizzate o calcolate che sono integrate in [!DNL Analytics].

   Presta attenzione al fatto che tutti i numeri in aumento appaiono nel rapporto come positivi, anche quando l’aumento è indesiderato. Ad esempio, anche se si desidera una percentuale di mancato recapito più bassa, la percentuale più elevata viene visualizzata come vincitore con l’incremento più alto. Considera queste metriche e ad altre simili, e se preferisci aumentare o diminuire i numeri, quando prendi decisioni in base ai rapporti.

You can apply the metric or audience to the report in [!DNL Target] after the activity has started, or even after the test has completed. Non devi sapere preventivamente con precisione che cosa vuoi misurare.

Click to view the full [!DNL Analytics] report directly from the activity report page.

## Creazione di attività {#section_311586E3FF5541E7A91D1A3CE5F9ACE3}

Durante la creazione di attività, devi specificare un obiettivo per l’attività nella pagina [!UICONTROL Impostazioni]. Questo obiettivo diventa la metrica predefinita per il rapporto e viene sempre indicato come prima opzione nel selettore delle metriche. Non puoi selezionare i segmenti per il rapporto come faresti per una normale attività di Target. A test with [!DNL Analytics] uses [!DNL Adobe Analytics] segments rather than [!DNL Target] audiences.

## Performing offline calculations for Analytics for Target (A4T) {#section_33A97A691F3A45D497DAF57A844388F0}

Puoi eseguire calcoli offline per A4T, ma è necessario un ulteriore passaggio di esportazione dei dati di [!DNL Analytics].

Per ulteriori informazioni, vedi [Esecuzione di calcoli offline per Analytics for Target (A4T)](/help/c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B).
