---
description: Utilizzando Analytics come origine per la generazione di rapporti per Target (A4T), puoi accedere ai rapporti di Analytics per le attività di Target.
keywords: analytics for target;a4t;analytics come fonte dei rapporti
seo-description: Utilizzando Analytics come origine per la generazione di rapporti per Target (A4T), puoi accedere ai rapporti di Analytics per le attività di Target.
seo-title: Generazione di rapporti per A4T
solution: Target
subtopic: Test multivariato
title: Generazione di rapporti per A4T
topic: Standard
uuid: bd3a7fa4-ba45-4ea3-81b6-fc2584831ce4
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Generazione di rapporti per A4T{#a-t-reporting}

Utilizzando Analytics come origine per la generazione di rapporti per Target (A4T), puoi accedere ai rapporti di Analytics per le attività di Target.

Puoi visualizzare i rapporti per le attività in Analytics e in Target Standard/Premium.

Per le best practice per la generazione di rapporti con Analytics for Target, [visita questa pagina di Adobe Spark](https://spark.adobe.com/page/Lo3Spm4oBOvwF/).

## Panoramica {#section_035A62D65608423285D8A5A54731E2C5}

Sia i rapporti di Analytics che di Target misurano i partecipanti (le persone incluse nei test), non i visitatori del sito.

Ogni volta che un visitatore vede un contenuto di attività nella pagina, Target effettua una chiamata diretta, da server a server, ad Analytics in cui sono comprese l’attività e l’esperienza viste dal visitatore. Target inoltre richiama Analytics ogni volta che viene effettuata la conversione. In Analytics la conversione viene aggiunta come un nuovo evento specifico denominato “Conversione attività”, che viene tracciato insieme ad altri dati raccolti da Analytics.

Quando si utilizza l’operazione Seleziona e si esegue l’ordinamento per *Partecipanti*, il rapporto mostra solo esperienze che hanno ricevuto partecipanti durante il periodo di tempo selezionato.

>[!NOTE]
>
>I rapporti forniti da Target hanno una latenza di quattro minuti. Per le attività fornite da A4T, sia nei rapporti di Target che di Analytics, possono trascorrere fino a 24 ore dal salvataggio iniziale dell’attività prima che i dati del rapporto possano essere suddivisi per esperienza. I dati raccolti nelle prime 24 ore sono comunque precisi e vengono attribuiti all’esperienza corretta.

## Rapporti in Analytics  {#section_F6884872DC864AE7913587FAED4CD11C}

In Analytics, fai clic su **[!UICONTROL Target]** &gt; **[!UICONTROL Attività di Target]** nel menu a sinistra. In Target, i rapporti dell’attività mostrano automaticamente dati, metriche e segmenti di Analytics. I dati sono visualizzati in questi rapporti circa un’ora dopo essere stati raccolti dal sito. Tutte le metriche, i destinatari e i valori nei rapporti provengono dalla suite di rapporti selezionata quando si configura l’attività.

In Analytics, utilizza il rapporto delle attività di Target per visualizzarne i risultati. I rapporti (legacy) di Test&amp;Target forniscono informazioni sulle integrazioni di pagina nello stile del precedente plug-in Test&amp;Target e non includono i dati di Analytics for Target. Nel rapporto delle attività puoi visualizzare le informazioni sulle esperienze di Target. Fai clic su **[!UICONTROL Metriche]**, quindi seleziona il tipo di metrica di **[!UICONTROL Target]**. Per il rapporto sono disponibili due metriche:

* **Accessi attività:** corrisponde al numero di partecipanti nel rapporto di Target.
* **Conversioni attività:** corrisponde al numero di conversioni personalizzate nel rapporto di Target.

>[!NOTE]
>
>I dettagli dell’incremento e dell’affidabilità di Target sono disponibili anche in Analytics. Per ulteriori informazioni, vedi [Tipi di rapporto di incremento e affidabilità di Target](https://marketing.adobe.com/resources/help/en_US/reference/report_target_lift_confidence.html) nella documentazione del prodotto Adobe Analytics.

>[!IMPORTANT]
>
>Se il rapporto delle attività di Target in Analytics presenta “non specificato” invece di elencare le attività, è necessario un aggiornamento dell’account predisposto. Contatta il servizio clienti per risolvere il problema.

## Rapporti in Target  {#section_C0D1F17F88374B6690BF904D7B83B42E}

Quando Analytics viene utilizzato come origine per la generazione di rapporti, i rapporti in Target Standard mostrano i dati raccolti da Analytics. Tra questo rapporto e gli altri presenti in Target Standard esistono alcune differenze:

* Nell’elenco Pubblico sono inclusi i gruppi di destinazione disponibili nella suite di rapporti di Analytics.
* L’elenco Metrica mostra tutte le metriche disponibili in Analytics.

   Ogni metrica è disponibile, comprese quelle personalizzate o calcolate che sono integrate in Analytics.

   Presta attenzione al fatto che tutti i numeri in aumento appaiono nel rapporto come positivi, anche quando l’aumento è indesiderato. Ad esempio, anche se si desidera una percentuale di mancato recapito più bassa, la percentuale più elevata viene visualizzata come vincitore con l’incremento più alto. Considera queste metriche e ad altre simili, e se preferisci aumentare o diminuire i numeri, quando prendi decisioni in base ai rapporti.

Puoi applicare la metrica o il pubblico al rapporto in Target dopo che il test è iniziato, o anche dopo che è stato completato. Non devi sapere preventivamente con precisione che cosa vuoi misurare.

Fai clic per visualizzare il rapporto completo di Analytics direttamente dalla pagina del rapporto delle attività.

## Rapporti in Analysis Workspace {#reports-in-analysis-workspace}

Puoi utilizzare [!DNL Adobe Analysis Workspace] per approfondire e visualizzare i dati o individuare le informazioni nascoste sotto la superficie.

Per informazioni ed esempi dettagliati, aprite [Analytics &amp; Target: Esercitazione](https://spark.adobe.com/page/Lo3Spm4oBOvwF/)Best practice per analisi, fornita da Adobe Experience Ltd.

## Creazione di attività  {#section_311586E3FF5541E7A91D1A3CE5F9ACE3}

Durante la creazione di attività, devi specificare un obiettivo per l’attività nella pagina [!UICONTROL Impostazioni]. Questo obiettivo diventa la metrica predefinita per il rapporto e viene sempre indicato come prima opzione nel selettore delle metriche. Non puoi selezionare i segmenti per il rapporto come faresti per una normale attività di Target. Un test con Analytics utilizza i segmenti di Adobe Analytics anziché il pubblico di Target Standard.

## Esecuzione di calcoli offline per Analytics for Target (A4T) {#section_33A97A691F3A45D497DAF57A844388F0}

Puoi eseguire calcoli offline per A4T, ma è necessario un ulteriore passaggio di esportazione dei dati di [!DNL Analytics].

Per ulteriori informazioni, vedi [Esecuzione di calcoli offline per Analytics for Target (A4T)](../../c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B).
