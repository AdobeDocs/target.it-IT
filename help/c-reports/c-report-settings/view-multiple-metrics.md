---
keywords: Target;reports;report settings;multiple metrics;metrics;shown metrics;hidden metrics
description: Seleziona più metriche da visualizzare in un report utilizzando  Adobe Target.
title: Visualizzare più metriche in un report utilizzando  Adobe Target
feature: Reports
translation-type: tm+mt
source-git-commit: 7b86db4b45f93a3c6169caf81c2cd52236bb5a45
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 61%

---


# Visualizzare più metriche in un rapporto{#view-multiple-metrics-in-a-report}

Puoi selezionare più metriche da visualizzare in un report [!DNL Adobe Target].

Tieni presente le informazioni seguenti quando lavori con più metriche nei rapporti:

* La possibilità di visualizzare più metriche è disponibile solo per le attività [A/B Test](/help/c-activities/t-test-ab/test-ab.md), [Auto-Allocate](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md), [Auto-Target](/help/c-activities/auto-target/auto-target-to-optimize.md) e [Experience Targeting](/help/c-activities/t-experience-target/experience-target.md) (XT).
* Non puoi aggiungere più di 20 metriche a un report per un&#39;attività che utilizza [Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T). Puoi aggiungere tutte le metriche di cui disponi nell&#39;attività ai report per le attività che *non* utilizzano A4T.
* Non puoi utilizzare l&#39;opzione [](/help/c-reports/downloading-data-in-csv-file.md)Scarica per scaricare i rapporti in formato CSV se sono state selezionate più metriche. Devi selezionare una sola metrica per attivare l’opzione [!UICONTROL Scarica].
* Non è possibile visualizzare più metriche per le attività create prima della release [!DNL Target] di luglio 2015 (30 luglio 2015).

**Per selezionare più metriche da visualizzare nel rapporto:**

1. Per visualizzare un rapporto, fai clic su **[!UICONTROL Attività]**, scegli l’attività desiderata dall’elenco, quindi fai clic sulla scheda **[!UICONTROL Rapporti]**.
1. Fai clic sull&#39;elenco a discesa **[!UICONTROL Metrica rapporto]** per visualizzare gli elenchi [!UICONTROL Metriche visualizzate] e [!UICONTROL Metriche nascoste].

   ![](assets/multiple_metrics.png)

   Puoi utilizzare la [!UICONTROL casella di ricerca] per trovare rapidamente le metriche disponibili da aggiungere all&#39;elenco [!UICONTROL Metriche visualizzate].

   È possibile selezionare più metriche sia dalla modalità [!UICONTROL Vista tabella] sia dalla modalità [!UICONTROL Vista grafico] del rapporto.

1. Posiziona il puntatore del mouse sulla metrica desiderata nell&#39;elenco [!UICONTROL Metriche nascoste], quindi fai clic su **[!UICONTROL Seleziona]** per spostarle nell&#39;elenco [!UICONTROL Metriche visualizzate].

   Oppure

   Trascina le metriche desiderate dall&#39;elenco [!UICONTROL Metriche nascoste] all&#39;elenco [!UICONTROL Metriche visualizzate].

   Nell&#39;elenco [!UICONTROL Metriche visualizzate] deve essere presente almeno una metrica.

   È possibile ridisporre le metriche trascinandole nell&#39;ordine desiderato nell&#39;elenco [!UICONTROL Metriche visualizzate]. L&#39;ordine selezionato verrà riportato nella [!UICONTROL Visualizzazione tabella] e nella [!UICONTROL Visualizzazione grafico]. Per rimuovere una metrica dall&#39;elenco [!UICONTROL Metriche visualizzate], posiziona il puntatore del mouse sulla metrica, quindi fai clic sull&#39;icona **X**.

1. Al termine, fai clic su **[!UICONTROL Salva]**.
1. (Condizionale) Durante la visualizzazione del rapporto in [!UICONTROL Visualizzazione tabella], posizionate il puntatore del mouse sull&#39;intestazione della colonna di una metrica per visualizzare una freccia blu. Fai clic sulla freccia per espandere la tabella e visualizzare i parametri di [!UICONTROL Incremento] e [!UICONTROL Affidabilità] per tale metrica.

   ![](assets/multiple_metrics_table.png)

   È possibile espandere solo una metrica/colonna alla volta. Fai nuovamente clic sulla freccia per comprimere le colonne.

1. (Condizionale) Quando visualizzi il rapporto nella visualizzazione grafico, puoi selezionare dall’elenco a discesa singole metriche da visualizzare:

   ![](assets/multiple_metrics_graph.png)

