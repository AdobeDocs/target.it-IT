---
keywords: mvt;test multivariato;best practice per test multivariato;procedure consigliate mvt;combinazioni mvt;rapporti mvt
description: Scopri come migliorare le prestazioni, evitare problemi e correggere problemi noti che potrebbero verificarsi durante la creazione ed esecuzione di [!UICONTROL Test multivariato] attività in [!DNL Adobe Target].
title: Quali best practice per un [!UICONTROL Test multivariato] attività?
feature: Multivariate Tests
exl-id: bcd15517-1b5f-4425-9404-1d7dd0689e28
source-git-commit: 0d73a062f70080057c3323f5150af067e3a2e27e
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 70%

---

# [!UICONTROL Best practice relative ai test multivariati]

Suggerimenti per migliorare le prestazioni, evitare problemi e correggere problemi noti che potrebbero verificarsi durante la creazione ed esecuzione di attività di [!UICONTROL Test multivariato] (MVT) in [!DNL Adobe Target].

## Pianificare {#section_4D4A1F6226F042379BF48DB753608579}

* Presta particolare attenzione alle posizioni sulla pagina che produrranno probabilmente risultati significativi.

  Ad esempio, un banner o un’immagine protagonista porterà probabilmente più conversioni di una modifica del piè di pagina. L&#39;inclusione di posizioni meno significative nel test aumenta la quantità di traffico e il tempo necessario per eseguire il test sulle posizioni più importanti della pagina.
* Prepara anticipatamente le varianti di pagina.

  Assicurati di comprendere le differenze di contenuto per ogni offerta e di creare tutte le offerte immagine, testo e HTML che prevedi di utilizzare nel test MVT.

## Creare {#section_C59C722CA82E48ABA58A4A7FA758F193}

* Non includere più combinazioni del necessario per il test.

  Ogni combinazione inclusa nel test aumenta in modo significativo la quantità di traffico e il tempo necessario per ottenere risultati accettabili. Ad esempio, in presenza di tre posizioni con tre offerte ciascuna, le possibili combinazioni sono 27 (3x3x3). Tre posizioni, due delle quali includono tre offerte possibili e una due offerte, forniscono 18 opzioni (3x3x2). Queste cifre aumentano in modo significativo per ogni posizione e offerta aggiuntive.

* Denomina posizioni e offerte.

  Puoi rinominare ogni posizione e offerta nel test in modo più significativo. Il numero di offerte in ogni posizione è riportato nell’intestazione della posizione. I nomi utili consentono di identificare le offerte quando si esaminano i rapporti.

* Sfrutta le funzioni di anteprima per evitare combinazioni di contenuto indesiderate.

  Rivedi tutte le esperienze generate dal test prima di pubblicarle. Assicurati che non vi siano combinazioni con affermazioni contraddittorie (ad esempio, 20% di sconto e $ 19 di sconto nella stessa esperienza) o con design incompatibili, come avere sfondo e font dello stesso colore.

* Utilizza il [Calcolatore del traffico](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md) per assicurarti che il test sia progettato per la quantità di traffico ricevuto dalla pagina.

  Assicurati che il Calcolatore del traffico fornisca alla configurazione di test la luce verde in modo da ottenere i risultati desiderati.

* Le alternative di ciascun elemento dovrebbero essere significativamente diverse tra loro.

## Analizzare {#section_9A2118CF1039451681C13D9AE79A58AB}

* Utilizza spesso il [Rapporto Contributo posizione](/help/main/c-reports/multivariate-test-reports/location-contribution-report.md) per monitorare le prestazioni di ogni posizione e offerta.
* Nel [rapporto Prestazioni esperienza](/help/main/c-reports/multivariate-test-reports/experience-performance-report.md) basa le tue decisioni sui dati riportati utilizzando i filtri Migliori 5 e Peggiori 5.

  L’utilizzo del filtro [!UICONTROL Tutto] rende difficile estrarre le informazioni desiderate ed è possibile che nel grafico non vengano visualizzate tutte le esperienze. Usa il filtro [!UICONTROL Tutto] per trovare un’esperienza specifica che non rientri tra le cinque migliori o peggiori.

## Eseguire il followup {#section_1C44A767F6AB4441A3EAA8AC995F46B0}

* Anche se [!DNL Target] consente di modificare un’attività live; la modifica di un’attività in corso potrebbe reimpostare il test. I report potrebbero non riconoscere alcune delle modifiche. È importante apportare modifiche alle offerte HTML solo nella libreria di offerte.

  Le azioni specifiche che reimpostano i nomi delle esperienze e i rapporti includono:

   * Aggiunta di una nuova posizione
   * Eliminazione di una posizione
   * Aggiunta di nuove offerte o eliminazione di offerte da una posizione esistente
   * Modifica di offerte di testo avanzate
   * Modifica del colore di sfondo

* Facendo seguire un test MVT da uno o più test A/B, puoi determinare il contenuto migliore possibile per i risultati desiderati.

  Una volta determinate le posizioni e il contenuto più utili per raggiungere gli obiettivi, puoi eseguire un test A/B per perfezionare ulteriormente i risultati. Ad esempio, quando sai quali posizioni sono più importanti, testa due immagini specifiche tra loro o confronta il testo o i colori di un invito all’azione.
