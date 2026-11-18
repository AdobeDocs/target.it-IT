---
keywords: mvt;test multivariato;best practice per test multivariato;procedure consigliate mvt;combinazioni mvt;rapporti mvt
description: Scopri come migliorare le prestazioni, evitare problemi e correggere problemi noti che potrebbero verificarsi durante la creazione ed esecuzione di [!UICONTROL attività Test multivariato] in [!DNL Adobe Target].
title: Quali sono le best practice per un'attività [!UICONTROL Test multivariato]?
feature: Multivariate Tests
exl-id: bcd15517-1b5f-4425-9404-1d7dd0689e28
TQID: 'https://experienceleague.adobe.com/nQEf5GZ8-zVZakygPtMAYWk-xoJPdcycFbzCNKTqJ-k'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: b934e7cf-c07f-5a64-924b-3c9da8413e3d
    internal-label: Multivariate Tests
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 0ae6991a6a86854bd64a632070a1fcbe544cc606
workflow-type: tm+mt
source-wordcount: '868'
ht-degree: 30%
---
# [!UICONTROL Best practice per il test multivariato] {#mvt-best-practices}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come pianificare, creare, analizzare e seguire un&#39;attività di **[!UICONTROL Test multivariato]** per ottenere risultati affidabili.

>[!ENDSHADEBOX]

I suggerimenti seguenti consentono di migliorare le prestazioni, evitare problemi e correggere problemi noti che potrebbero verificarsi durante la creazione ed esecuzione di **[!UICONTROL attività Test multivariato]** (MVT) in [!DNL Adobe Target].

## Pianificare {#plan}

* **Utilizzare almeno tre elementi nel test.**

  Se il numero è inferiore, esegui una serie di test A/B. Per ulteriori informazioni, vedere [Quando utilizzare il test multivariato rispetto a A/B](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md#when-to-use-mvt).

* **Tieni presente la quantità di traffico che in genere ottieni, incluso il numero di impression e di conversioni.**

  MVT richiede traffico sufficiente per generare risultati utili e queste informazioni aiutano a ridurre la probabilità di progettare un test con requisiti che superano il traffico del sito.

* **Tieni presente le posizioni sulla pagina che produrranno probabilmente risultati significativi.**

  Un banner o un’immagine protagonista porterà probabilmente più conversioni di una modifica del piè di pagina. L&#39;inclusione di posizioni meno significative nel test aumenta la quantità di traffico e il tempo necessario per eseguire il test sulle posizioni più importanti della pagina.

* **Mantenere gli elementi indipendenti tra loro.**

  Ad esempio, non testare il layout e il contenuto nello stesso test.

* **Esaminare il codice HTML per le pagine che si desidera verificare.**

  Assicurati che gli elementi HTML sul tuo sito non presentino ID DOM duplicati. Gli ID duplicati possono fare sì che lo stesso contenuto sia distribuito a più posizioni.

* **Prepara le varianti di pagina in anticipo.**

  Assicurati di comprendere le differenze di contenuto per ogni offerta e di creare tutte le offerte immagine, testo e HTML che prevedi di utilizzare nel test MVT.

* **Pianifica tempo aggiuntivo per il controllo qualità.**

  Il numero di esperienze aumenta, pertanto il QA richiede più tempo.

## Crea {#create}

* **Non includere più combinazioni del necessario per il test.**

  Ogni combinazione inclusa nel test aumenta in modo significativo la quantità di traffico e il tempo necessario per ottenere risultati accettabili. Ad esempio, in presenza di tre posizioni con tre offerte ciascuna, le possibili combinazioni sono 27 (3x3x3). Tre posizioni, due delle quali includono tre offerte possibili e una due offerte, forniscono 18 opzioni (3x3x2). Queste cifre aumentano in modo significativo per ogni posizione e offerta aggiuntive.

* **Denomina posizioni e offerte.**

  Puoi rinominare ogni posizione e offerta nel test in modo più significativo. Il numero di offerte in ogni posizione è riportato nell’intestazione della posizione. I nomi utili consentono di identificare le offerte quando si esaminano i rapporti.

* **Sfrutta le funzionalità di anteprima per evitare combinazioni di contenuto indesiderate.**

  Rivedi tutte le esperienze generate dal test prima di pubblicarle. Assicurati che non vi siano combinazioni con affermazioni contraddittorie (ad esempio, 20% di sconto e $ 19 di sconto nella stessa esperienza) o con design incompatibili, come uno sfondo e un font dello stesso colore.

* **Utilizza [Calcolatore traffico](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md#traffic-estimator) per assicurarti che il test sia progettato per la quantità di traffico ricevuto dalla pagina.**

  Assicurati che il **[!UICONTROL Calcolatore del traffico]** fornisca alla configurazione del test la luce verde in modo da ottenere i risultati desiderati.

* **Differenza significativa tra le alternative di ogni elemento.**

  Sebbene non sia obbligatorio, è buona prassi che ogni elemento abbia lo stesso numero di alternative.

## Analizzare {#analyze}

* **Utilizza spesso il [rapporto Contributo posizione](/help/main/c-reports/multivariate-test-reports/location-contribution-report.md)** per monitorare le prestazioni di ogni posizione e offerta.

* **Nel [rapporto Prestazioni esperienza](/help/main/c-reports/multivariate-test-reports/experience-performance-report.md), basa le tue decisioni sui dati visualizzati utilizzando i filtri [!UICONTROL Migliori 5] e [!UICONTROL Peggiori 5].**

  Il filtro **[!UICONTROL All]** rende difficile estrarre le informazioni desiderate ed è possibile che nel grafico non vengano visualizzate tutte le esperienze. Utilizza il filtro **[!UICONTROL Tutti]** per trovare un&#39;esperienza specifica che non rientri tra le cinque migliori o peggiori.

## Completa {#follow-up}

* Sebbene [!DNL Target] consenta di modificare un&#39;attività live, **la modifica di un&#39;attività in corso potrebbe reimpostare il test.** I report potrebbero non riconoscere alcune delle modifiche. È possibile apportare modifiche alle offerte di HTML solo nella libreria delle offerte.

  Le azioni specifiche che reimpostano i nomi delle esperienze e i rapporti includono:

  * Aggiunta di una nuova posizione
  * Eliminazione di una posizione
  * Aggiunta di nuove offerte o eliminazione di offerte da una posizione esistente
  * Modifica di offerte di testo avanzate
  * Modifica del colore di sfondo

* **Se la suite di rapporti non viene caricata quando si modifica un&#39;attività che utilizza metriche basate su [!DNL Analytics] (viene visualizzato un elemento spinner),** passa alle metriche [!DNL Target], quindi torna alle metriche basate su [!DNL Analytics]. In questo modo sarà possibile caricare la suite di rapporti.

* **Segui un test MVT con uno o più test A/B** per determinare il contenuto migliore possibile per i risultati desiderati. Una volta determinate le posizioni e il contenuto più utili per raggiungere gli obiettivi, puoi eseguire un test A/B per perfezionare ulteriormente i risultati. Ad esempio, quando sai quali posizioni sono più importanti, testa due immagini specifiche tra loro o confronta il testo o i colori di un call to action.
