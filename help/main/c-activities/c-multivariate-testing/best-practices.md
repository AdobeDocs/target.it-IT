---
keywords: mvt;test multivariato;best practice per test multivariato;procedure consigliate mvt;combinazioni mvt;rapporti mvt
description: Suggerimenti per migliorare le prestazioni, evitare problemi e correggere problemi noti che potrebbero verificarsi durante la creazione ed esecuzione di attività di test multivariato in Adobe Target.
title: Quali sono le best practice per i test multivariati?
feature: Multivariate Tests
exl-id: bcd15517-1b5f-4425-9404-1d7dd0689e28
source-git-commit: d90e541588f51e16dd9b11ead1ece77e9ca1408b
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 100%

---

# Best practice relative ai test multivariati

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

   Puoi rinominare ogni posizione e offerta nel test in modo più significativo. Il numero di offerte in ogni posizione è riportato nell’intestazione della posizione. I nomi descrittivi ti aiuteranno a riconoscere le offerte quando esamini i rapporti.

* Sfrutta le funzioni di anteprima per evitare combinazioni di contenuto indesiderate.

   Rivedi tutte le esperienze generate dal test prima di pubblicarle. Assicurati che non vi siano combinazioni con affermazioni contraddittorie (ad esempio, 20% e €20 di sconto nella stessa esperienza) o progettazioni incompatibili, come sfondo e carattere dello stesso colore.

* Utilizza il [Calcolatore del traffico](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md) per assicurarti che il test sia progettato per la quantità di traffico ricevuto dalla pagina.

   Assicurati che con il Calcolatore del traffico sia possibile convalidare la configurazione del test in modo da poter ottenere i risultati desiderati.
* È consigliabile che le alternative per ciascun elemento siano notevolmente diverse tra loro.

## Analizzare {#section_9A2118CF1039451681C13D9AE79A58AB}

* Utilizza spesso il [rapporto Contributo posizione](/help/main/c-reports/multivariate-test-reports/location-contribution-report.md) per monitorare le prestazioni di ogni elemento e di ogni offerta.
* Nel [rapporto Prestazioni esperienza](/help/main/c-reports/multivariate-test-reports/experience-performance-report.md) basa le tue decisioni sui dati riportati utilizzando i filtri Migliori 5 e Peggiori 5.

   L’utilizzo del filtro [!UICONTROL Tutto] rende difficile estrarre le informazioni desiderate ed è possibile che nel grafico non vengano visualizzate tutte le esperienze. Usa il filtro [!UICONTROL Tutto] per trovare un’esperienza specifica che non rientri tra le cinque migliori o peggiori.

## Eseguire il followup {#section_1C44A767F6AB4441A3EAA8AC995F46B0}

* Sebbene in [!DNL Target] sia possibile modificare un’attività live, è importante considerare che la modifica di un’attività in corso potrebbe reimpostare il test. Pertanto, i rapporti potrebbero non riconoscere alcune delle modifiche. È importante apportare modifiche alle offerte HTML solo nella libreria di offerte.

   Le azioni specifiche che ripristinano i nomi e i rapporti relativi alle esperienze sono:

   * Aggiunta di una nuova posizione
   * Eliminazione di una posizione
   * Aggiunta di nuove offerte o eliminazione di offerte da una posizione esistente
   * Modifica di offerte di testo avanzate
   * Modifica del colore di sfondo

* Facendo seguire un test MVT da uno o più test A/B, puoi determinare il contenuto migliore possibile per i risultati desiderati.

   Una volta determinate le posizioni e il contenuto più utili per raggiungere gli obiettivi, puoi eseguire un test A/B per perfezionare ulteriormente i risultati. Ad esempio, quando sono note le posizioni più rilevanti, puoi sottoporre a test reciproco due immagini specifiche oppure confrontare il testo o i colori di un invito all&#39;azione.
