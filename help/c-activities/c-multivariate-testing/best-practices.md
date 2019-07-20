---
description: Suggerimenti per migliorare le prestazioni, evitare problemi e correggere problemi noti che potrebbero verificarsi durante la creazione ed esecuzione di attività Test multivariato in Adobe Target.
keywords: MVT;test multivariato;best practice per test multivariato;procedure consigliate MVT;combinazioni MVT;rapporti MVT
seo-description: Suggerimenti per migliorare le prestazioni, evitare problemi e correggere problemi noti che potrebbero verificarsi durante la creazione ed esecuzione di attività Test multivariato in Adobe Target.
seo-title: Best practice multivariate con Adobe Target
solution: Target
title: Best practice relative ai test multivariati
topic: Standard
uuid: 4468a2eb-3fc1-4bc5-85ac-90cc02db4fbb
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Best practice relative ai test multivariati{#multivariate-test-best-practices}

Tips to help you improve performance, avoid issues, and correct known issues that might occur when creating and running Multivariate Test (MVT) activities in [!DNL Adobe Target].

## Pianificare {#section_4D4A1F6226F042379BF48DB753608579}

* Presta particolare attenzione alle posizioni sulla pagina che produrranno probabilmente risultati significativi.

   Ad esempio, un banner o un'immagine hero porterà probabilmente più conversioni rispetto a una modifica nel piè di pagina. L'inclusione di posizioni meno significative nel test aumenta la quantità di traffico e il tempo necessario per eseguire il test sulle posizioni più importanti della pagina.
* Prepara anticipatamente le varianti di pagina.

   Assicurati di comprendere le differenze di contenuto per ogni offerta e di creare tutte le offerte immagine, testo e HTML che prevedi di utilizzare nel test MVT.

## Creare {#section_C59C722CA82E48ABA58A4A7FA758F193}

* Non includere più combinazioni del necessario per il test.

   Ogni combinazione inclusa nel test aumenta in modo significativo la quantità di traffico e il tempo necessario per ottenere risultati accettabili. Ad esempio, in presenza di tre posizioni con tre offerte ciascuna, le possibili combinazioni sono 27 (3 x 3 x 3). Tre posizioni, dove due posizioni contengono tre offerte possibili e una posizione due offerte, forniscono 18 opzioni (3 x 3 x 2). Queste cifre aumentano in modo significativo per ogni posizione e offerta aggiuntive.

* Denomina posizioni e offerte.

   Puoi rinominare ogni posizione e offerta nel test in modo più significativo. Il numero di offerte in ogni posizione è riportato nell’intestazione della posizione. I nomi descrittivi ti aiuteranno a riconoscere le offerte quando esamini i rapporti.

* Sfrutta le funzioni di anteprima per evitare combinazioni di contenuto indesiderate.

   Rivedi tutte le esperienze generate dal test prima di pubblicarle. Assicurati che non vi siano combinazioni con affermazioni contraddittorie (ad esempio, 20% e €20 di sconto nella stessa esperienza) o progettazioni incompatibili, come sfondo e carattere dello stesso colore.

* Use the [Traffic Estimator](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md) to make sure that your test is designed for the amount of traffic your page receives.

   Assicurati che con il Calcolatore del traffico sia possibile convalidare la configurazione del test in modo da poter ottenere i risultati desiderati.
* È consigliabile che le alternative per ciascun elemento siano notevolmente diverse tra loro.

## Analizzare {#section_9A2118CF1039451681C13D9AE79A58AB}

* Make frequent use of the [Location Contribution report](/help/c-reports/location-contribution-report.md) to monitor the performance of each location and each offer.
* In the [Experience Performance report](/help/c-reports/experience-performance-report.md), base your decisions on the data shown using the Best 5 and Worst 5 filters.

   The [!UICONTROL All] filter makes it difficult to extract the desired information, and not all experiences can display in the graph. Use the [!UICONTROL All] filter if you want to look at a specific experience that is not in the best or worst five.

## Eseguire il followup {#section_1C44A767F6AB4441A3EAA8AC995F46B0}

* Although [!DNL Target] allows you to edit a live activity, be aware that editing an activity that is in progress could reset the test. Pertanto, i rapporti potrebbero non riconoscere alcune delle modifiche. È importante apportare modifiche alle offerte HTML solo nella libreria di offerte.

   Le azioni specifiche che ripristinano i nomi e i rapporti relativi alle esperienze sono:

   * Aggiunta di una nuova posizione
   * Eliminazione di una posizione
   * Aggiunta di nuove offerte o eliminazione di offerte da una posizione esistente
   * Modifica di offerte di testo avanzate
   * Modifica del colore di sfondo

* Facendo seguire un test MVT da uno o più test A/B, puoi determinare il contenuto migliore possibile per i risultati desiderati.

   Una volta determinate le posizioni e il contenuto più utili per raggiungere gli obiettivi, puoi eseguire un test A/B per perfezionare ulteriormente i risultati. Ad esempio, quando sono note le posizioni più rilevanti, puoi sottoporre a test reciproco due immagini specifiche oppure confrontare il testo o i colori di un invito all'azione.

