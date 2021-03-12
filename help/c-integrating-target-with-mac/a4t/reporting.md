---
keywords: analytics for target;a4t;analytics come origine per la generazione di rapporti;analytics
description: Scopri come utilizzare Analytics for Target (A4T). A4T fornisce l’accesso ai rapporti di Analytics per le attività di Target che utilizzano le metriche di Analytics e i segmenti di pubblico.
title: Come si utilizza il reporting in A4T?
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: 7b2d5251275f42da66d09370501d0882671d5cca
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 30%

---


# Generazione di rapporti per A4T{#a-t-reporting}

Utilizzando [!DNL Adobe Analytics] come origine per la generazione di rapporti per [!DNL Adobe Target] (A4T) puoi accedere ai rapporti [!DNL Analytics] per le attività [!DNL Target].

Puoi visualizzare i rapporti relativi alle attività sia in [!DNL Analytics] che in [!DNL Target].

Per informazioni sulle best practice di reporting utilizzando [!DNL Analytics] per [!DNL Target], [visita questo Adobe Spark Page](https://spark.adobe.com/page/Lo3Spm4oBOvwF/).

## Panoramica {#section_035A62D65608423285D8A5A54731E2C5}

Sia i rapporti [!DNL Analytics] che [!DNL Target] misurano i partecipanti (le persone incluse nei test), anziché i visitatori del sito.

Ogni volta che un visitatore visualizza il contenuto dell&#39;attività sulla pagina, [!DNL Target] effettua una chiamata diretta da server a server a [!DNL Analytics], inclusa l&#39;attività e l&#39;esperienza visualizzate dal visitatore. [!DNL Target] richiama anche  [!DNL Analytics] ogni volta che viene effettuata la conversione. [!DNL Analytics] aggiunge la conversione come un nuovo  [!DNL Analytics] evento specifico denominato &quot;Conversione attività&quot;, che viene tracciato insieme ad altri dati raccolti da  [!DNL Analytics].

Quando si utilizza l&#39;operazione [!UICONTROL Seleziona] e si esegue l&#39;ordinamento su *Partecipanti*, nei rapporti vengono visualizzate solo le esperienze che hanno ricevuto partecipanti durante il periodo di tempo selezionato.

>[!NOTE]
>
>I rapporti forniti da [!DNL Target] hanno una latenza di quattro minuti. Per le attività fornite da A4T, nei rapporti [!DNL Target] e [!DNL Analytics] , possono essere necessarie fino a 24 ore prima che i dati del rapporto possano essere suddivisi per esperienze. I dati raccolti nelle prime 24 ore sono comunque precisi e vengono attribuiti all’esperienza corretta.

## Rapporti in Analytics {#analytics}

In [!DNL Analytics] sono disponibili diverse dimensioni e metriche dopo l’abilitazione dell’integrazione A4T.

### Dimensioni

* [!UICONTROL Analytics for Target] : l&#39;ID principale trasmesso tramite l&#39;integrazione. Il formato di questa dimensione è `Activity ID:Experience ID:3rd ID`. Le dimensioni seguenti sono classificazioni di questa dimensione.
* [!UICONTROL Attività di Target]
* [!UICONTROL Esperienze Target]
* [!UICONTROL Attività]  Target >  [!UICONTROL Esperienza]
* [!UICONTROL 3o ID] : può essere ignorato

### Metrics (Metriche)

* [!UICONTROL Impression attività]  - Corrisponde al numero di   partecipanti nel  [!DNL Target] rapporto.
* [!UICONTROL Conversioni attività]  - Corrisponde al numero  [!UICONTROL di ] conversazioni personalizzate nel  [!DNL Target] rapporto.

In [!DNL Analysis Workspace], utilizza il pannello [!UICONTROL Analytics for Target] per analizzare le attività e le esperienze [!DNL Target] con incremento e affidabilità. Per ulteriori informazioni, consulta il pannello [Analytics for Target (A4T)](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html) nella *Guida agli strumenti di Analytics*.

>[!IMPORTANT]
>
>Se il rapporto [!UICONTROL Attività di Target] in [!DNL Analytics] elenca &quot;non specificato&quot; invece di elencare le attività, è necessario un aggiornamento dell&#39;account predisposto. Contatta il servizio clienti per risolvere il problema.

Per informazioni ed esempi dettagliati, apri [Analytics &amp; Target: Esercitazione sulle best practice per l&#39;analisi](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) fornita da Adobe Experience League.

## Rapporti in Target  {#section_C0D1F17F88374B6690BF904D7B83B42E}

Quando [!DNL Analytics] viene utilizzato come origine per la generazione di rapporti, i rapporti in [!DNL Target] mostrano i dati raccolti da [!DNL Analytics]. Il rapporto è in qualche modo diverso da altri rapporti [!DNL Target]:

* L&#39;elenco [!UICONTROL Tipi di pubblico] mostra i tipi di pubblico disponibili nella suite di rapporti [!DNL Analytics].
* L&#39;elenco [!UICONTROL Metrica] mostra tutte le metriche disponibili tramite [!DNL Analytics].

   Ogni metrica è disponibile, comprese quelle personalizzate o calcolate che sono integrate in [!DNL Analytics].

   Eventuali numeri che aumentano vengono visualizzati come positivi nel rapporto, anche quando un aumento è indesiderato. Ad esempio, anche se si desidera una percentuale di mancato recapito più bassa, la percentuale più elevata viene visualizzata come vincitore con l’incremento più alto. Considera queste metriche e ad altre simili, e se preferisci aumentare o diminuire i numeri, quando prendi decisioni in base ai rapporti.

Puoi applicare la metrica o il pubblico al rapporto in [!DNL Target] dopo l’avvio dell’attività, o anche dopo il completamento del test. Non devi sapere preventivamente con precisione che cosa vuoi misurare.

Fai clic su per visualizzare il rapporto completo [!DNL Analytics] direttamente dalla pagina del rapporto attività.

## Creazione di attività {#section_311586E3FF5541E7A91D1A3CE5F9ACE3}

Durante la creazione di attività, devi specificare un obiettivo per l’attività nella pagina [!UICONTROL Impostazioni]. Questo obiettivo diventa la metrica predefinita per il rapporto e viene sempre indicato come prima opzione nel selettore delle metriche. Non puoi selezionare i segmenti per il rapporto come faresti per una normale attività di Target. Un test con [!DNL Analytics] utilizza segmenti [!DNL Adobe Analytics] anziché [!DNL Target] tipi di pubblico.

## Esecuzione di calcoli offline per Analytics for Target (A4T) {#section_33A97A691F3A45D497DAF57A844388F0}

Puoi eseguire calcoli offline per A4T, ma è necessario un ulteriore passaggio di esportazione dei dati di [!DNL Analytics].

Per ulteriori informazioni, vedi [Esecuzione di calcoli offline per Analytics for Target (A4T)](/help/c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B).
