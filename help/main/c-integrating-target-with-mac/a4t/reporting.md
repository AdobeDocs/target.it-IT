---
keywords: analytics for target;a4t;analytics come origine per la generazione di rapporti;analytics
description: Scopri come utilizzare Analytics per [!DNL Target] (A4T). A4T consente di accedere ai rapporti di Analytics per [!DNL Target] attività che utilizzano metriche di Analytics e segmenti di pubblico.
title: Come si utilizza il reporting in A4T?
feature: Analytics for Target (A4T)
exl-id: cab5dc5f-166a-468e-8382-ae734684afdd
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 30%

---

# Generazione di rapporti per A4T

Utilizzo [!DNL Adobe Analytics] come origine per la generazione di rapporti per [!DNL Adobe Target] (A4T) consente di accedere a [!DNL Analytics] rapporti per [!DNL Target] attività.

Puoi visualizzare i rapporti per le attività in entrambi [!DNL Analytics] e [!DNL Target].

Per le best practice di reporting che utilizzano [!DNL Analytics] per [!DNL Target], [visita Adobe Spark Page](https://spark.adobe.com/page/Lo3Spm4oBOvwF/).

## Panoramica {#section_035A62D65608423285D8A5A54731E2C5}

Entrambi [!DNL Analytics] e [!DNL Target] i rapporti misurano i partecipanti (le persone incluse nei test), anziché i visitatori del sito.

Ogni volta che un visitatore visualizza il contenuto dell’attività sulla pagina, [!DNL Target] effettua una chiamata diretta da server a server a [!DNL Analytics], tra cui quale attività ed esperienza ha visto il visitatore. [!DNL Target] anche le chiamate [!DNL Analytics] ogni volta che viene effettuata la conversione. [!DNL Analytics] aggiunge la conversione come nuova specifica [!DNL Analytics] evento denominato &quot;Conversione attività&quot;, tracciato insieme ad altri dati raccolti da [!DNL Analytics].

Quando il [!UICONTROL Seleziona] viene utilizzata e viene eseguito l&#39;ordinamento *Partecipanti*, nei rapporti vengono quindi visualizzate solo le esperienze che hanno ricevuto partecipanti durante il periodo di tempo selezionato.

>[!NOTE]
>
>Rapporti forniti da [!DNL Target] hanno una latenza di quattro minuti. Per le attività basate su A4T, sia nella [!DNL Target] e [!DNL Analytics] nei rapporti, potrebbero essere necessarie fino a 24 ore dopo il salvataggio iniziale dell’attività prima che i dati del rapporto possano essere suddivisi per esperienze. I dati raccolti nelle prime 24 ore sono comunque precisi e vengono attribuiti all’esperienza corretta.

## Rapporti in Analytics {#analytics}

In [!DNL Analytics], dopo l’abilitazione dell’integrazione A4T sono disponibili diverse dimensioni e metriche.

### Dimensioni

* [!UICONTROL Analytics for Target] - L&#39;ID principale trasmesso tramite l&#39;integrazione. Il formato di questa dimensione è `Activity ID:Experience ID:3rd ID`. Le dimensioni seguenti sono classificazioni di questa dimensione.
* [!UICONTROL Attività di Target]
* [!UICONTROL Esperienze Target]
* [!UICONTROL Attività Target] > [!UICONTROL Esperienza]
* [!UICONTROL 3o ID] - può essere ignorato

### Metrics (Metriche)

* [!UICONTROL Impression attività] - Corrisponde al [!UICONTROL Partecipanti] nel [!DNL Target] rapporto.
* [!UICONTROL Conversioni attività] - Corrisponde al [!UICONTROL Conversioni personalizzate] nel [!DNL Target] rapporto.

In [!DNL Analysis Workspace], utilizza [!UICONTROL Analytics for Target] pannello per analizzare [!DNL Target] attività ed esperienze con incremento e affidabilità. Per ulteriori informazioni, consulta [Pannello Analytics for Target (A4T)](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html?lang=it) in *Guida agli strumenti di Analytics*.

>[!IMPORTANT]
>
>Se [!UICONTROL Attività di Target] in [!DNL Analytics] elenca &quot;non specificato&quot; invece di elencare le attività, è necessario un aggiornamento al tuo account predisposto. Contatta il servizio clienti per risolvere il problema.

Per informazioni ed esempi dettagliati, apri la [Analytics e Target: Best practice per l’analisi](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) esercitazione, fornita da Adobe Experience League.

## Rapporti in [!DNL Target] {#section_C0D1F17F88374B6690BF904D7B83B42E}

Quando [!DNL Analytics] viene utilizzato come origine per la generazione di rapporti, nei [!DNL Target] mostra i dati raccolti da [!DNL Analytics]. La relazione è in qualche modo diversa dalle altre [!DNL Target] rapporti:

* La [!UICONTROL Tipi di pubblico] mostra i tipi di pubblico disponibili per le [!DNL Analytics] suite di rapporti.
* La [!UICONTROL Metrica] elenco mostra ogni metrica disponibile attraverso [!DNL Analytics].

   Ogni metrica è disponibile, comprese quelle personalizzate o calcolate che sono integrate in [!DNL Analytics].

   Eventuali numeri che aumentano vengono visualizzati come positivi nel rapporto, anche quando un aumento è indesiderato. Ad esempio, anche se si desidera una percentuale di mancato recapito più bassa, la percentuale più elevata viene visualizzata come vincitore con l’incremento più alto. Considera queste metriche e ad altre simili, e se preferisci aumentare o diminuire i numeri, quando prendi decisioni in base ai rapporti.

Puoi applicare la metrica o il pubblico al rapporto in [!DNL Target] dopo l’avvio dell’attività, o anche dopo il completamento del test. Non devi sapere preventivamente con precisione che cosa vuoi misurare.

Fai clic per visualizzare il testo completo [!DNL Analytics] rapporti direttamente dalla pagina del rapporto di attività.

## Creazione di attività {#section_311586E3FF5541E7A91D1A3CE5F9ACE3}

Durante la creazione di attività, devi specificare un obiettivo per l’attività nella pagina [!UICONTROL Impostazioni]. Questo obiettivo diventa la metrica predefinita per il rapporto e viene sempre indicato come prima opzione nel selettore delle metriche. Non puoi selezionare i segmenti per il rapporto come faresti per una normale attività di Target. Un test con [!DNL Analytics] utilizza [!DNL Adobe Analytics] segmenti anziché [!DNL Target] pubblico.

## Esecuzione di calcoli offline per Analytics for Adobe Target (A4T) {#section_33A97A691F3A45D497DAF57A844388F0}

Puoi eseguire calcoli offline per A4T, ma è necessario un ulteriore passaggio di esportazione dei dati di [!DNL Analytics].

Per ulteriori informazioni, vedi [Esecuzione di calcoli offline per Analytics for Target (A4T)](/help/main/c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B).
