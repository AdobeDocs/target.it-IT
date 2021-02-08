---
keywords: analytics for target;a4t;analytics come fonte dei rapporti
description: Scoprite come utilizzare Analytics per Target (A4T). A4T fornisce l'accesso ai report di Analytics per le attività Target che utilizzano le metriche di Analytics e i segmenti di audience.
title: Come si utilizza il reporting in A4T?
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 34%

---


# Generazione di rapporti per A4T{#a-t-reporting}

L&#39;utilizzo di [!DNL Analytics] come origine di reporting per [!DNL Target] (A4T) consente di accedere ai report [!DNL Analytics] per le attività [!DNL Target].

Puoi visualizzare i rapporti per le tue attività sia in [!DNL Analytics] che in [!DNL Target].

Per informazioni sulle procedure ottimali di reporting utilizzando [!DNL Analytics] per [!DNL Target], [visitare questa  pagina Adobe Spark](https://spark.adobe.com/page/Lo3Spm4oBOvwF/).

## Panoramica {#section_035A62D65608423285D8A5A54731E2C5}

Sia i rapporti [!DNL Analytics] che [!DNL Target] misurano i partecipanti (le persone che partecipano ai test), piuttosto che i visitatori del sito.

Ogni volta che un visitatore visualizza il contenuto dell&#39;attività sulla pagina, [!DNL Target] esegue una chiamata server-to-server diretta a [!DNL Analytics], che include l&#39;attività e l&#39;esperienza che il visitatore ha visto. [!DNL Target] inoltre, richiama  [!DNL Analytics] ogni volta che viene effettuata la conversione. [!DNL Analytics] aggiunge la conversione come un nuovo  [!DNL Analytics] evento specifico denominato &quot;Activity Conversion&quot; (Conversione attività), che viene tracciato insieme ad altri dati raccolti da  [!DNL Analytics].

Quando si utilizza l&#39;operazione [!UICONTROL Select] e si esegue l&#39;ordinamento su *Entrants*, nei rapporti vengono visualizzate solo le esperienze che hanno ricevuto partecipanti durante il periodo di tempo selezionato.

>[!NOTE]
>
>I report basati su [!DNL Target] hanno una latenza di quattro minuti. Per le attività basate su A4T, nei report [!DNL Target] e [!DNL Analytics] possono essere necessarie fino a 24 ore dopo che l&#39;attività è stata inizialmente salvata prima che i dati del report possano essere suddivisi per esperienze. I dati raccolti nelle prime 24 ore sono comunque precisi e vengono attribuiti all’esperienza corretta.

## Rapporti in Analytics {#analytics}

In [!DNL Analytics], dopo l&#39;abilitazione dell&#39;integrazione A4T sono disponibili diverse dimensioni e metriche.

### Dimensioni

* [!UICONTROL Analytics per Target]  - L&#39;ID principale trasmesso tramite l&#39;integrazione. Il formato di questa dimensione è `Activity ID:Experience ID:3rd ID`. Le seguenti dimensioni sono classificazioni di questa dimensione.
* [!UICONTROL Attività Target]
* [!UICONTROL Esperienze Target]
* [!UICONTROL Attività]  Target >  [!UICONTROL Esperienza]
* [!UICONTROL 3rd ID] - può essere ignorato

### Metrics (Metriche)

* [!UICONTROL Impressioni]  attività - Corrisponde al numero   di partecipanti nel  [!DNL Target] rapporto.
* [!UICONTROL Conversioni]  attività - Corrisponde al numero  [!UICONTROL di ] conversazioni personalizzate nel  [!DNL Target] rapporto.

In [!DNL Analysis Workspace], utilizzate il pannello [!UICONTROL Analytics for Target] per analizzare le attività e le esperienze [!DNL Target] con maggiore sicurezza. Per ulteriori informazioni, vedete [Pannello Analytics for Target (A4T)](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html) nella *Guida agli strumenti di Analytics*.

>[!IMPORTANT]
>
>Se il report [!UICONTROL Target Activities] in [!DNL Analytics] elenca &quot;unspecified&quot; invece di elencare le attività, è necessario aggiornare l&#39;account con provisioning. Contatta il servizio clienti per risolvere il problema.

Per informazioni dettagliate ed esempi, aprite [Analytics &amp; Target: Tecniche consigliate per l&#39;analisi](https://spark.adobe.com/page/Lo3Spm4oBOvwF/), fornite da  Adobe Experience League.

## Rapporti in Target  {#section_C0D1F17F88374B6690BF904D7B83B42E}

Quando [!DNL Analytics] viene utilizzato come origine di reporting, i report in [!DNL Target] mostrano i dati raccolti da [!DNL Analytics]. Il rapporto è in qualche modo diverso da altri report [!DNL Target]:

* L&#39;elenco [!UICONTROL Audiences] mostra le audience disponibili per la suite di rapporti [!DNL Analytics].
* L&#39;elenco [!UICONTROL Metric] mostra tutte le metriche disponibili tramite [!DNL Analytics].

   Ogni metrica è disponibile, comprese quelle personalizzate o calcolate che sono integrate in [!DNL Analytics].

   Presta attenzione al fatto che tutti i numeri in aumento appaiono nel rapporto come positivi, anche quando l’aumento è indesiderato. Ad esempio, anche se si desidera una percentuale di mancato recapito più bassa, la percentuale più elevata viene visualizzata come vincitore con l’incremento più alto. Considera queste metriche e ad altre simili, e se preferisci aumentare o diminuire i numeri, quando prendi decisioni in base ai rapporti.

Puoi applicare la metrica o l&#39;audience al report in [!DNL Target] dopo l&#39;avvio dell&#39;attività, o anche dopo il completamento del test. Non devi sapere preventivamente con precisione che cosa vuoi misurare.

Fate clic per visualizzare il rapporto completo [!DNL Analytics] direttamente dalla pagina del rapporto attività.

## Creazione di attività {#section_311586E3FF5541E7A91D1A3CE5F9ACE3}

Durante la creazione di attività, devi specificare un obiettivo per l’attività nella pagina [!UICONTROL Impostazioni]. Questo obiettivo diventa la metrica predefinita per il rapporto e viene sempre indicato come prima opzione nel selettore delle metriche. Non puoi selezionare i segmenti per il rapporto come faresti per una normale attività di Target. Un test con [!DNL Analytics] utilizza [!DNL Adobe Analytics] segmenti anziché [!DNL Target] tipi di pubblico.

## Esecuzione di calcoli offline per Analytics per Target (A4T) {#section_33A97A691F3A45D497DAF57A844388F0}

Puoi eseguire calcoli offline per A4T, ma è necessario un ulteriore passaggio di esportazione dei dati di [!DNL Analytics].

Per ulteriori informazioni, vedi [Esecuzione di calcoli offline per Analytics for Target (A4T)](/help/c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B).
