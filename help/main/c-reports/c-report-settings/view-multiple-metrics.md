---
keywords: Target;rapporti;impostazioni rapporti;più metriche;metriche;metriche visualizzate;metriche nascoste
description: Scopri come selezionare più metriche da visualizzare in un rapporto utilizzando Adobe Target.
title: Come si visualizzano più metriche in un rapporto?
feature: Reports
exl-id: 8d8aedd8-4583-4131-8ae0-df14e071940a
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 59%

---

# Visualizzare più metriche in un rapporto

Puoi selezionare più metriche da visualizzare in un [!DNL Adobe Target] rapporto.

Tieni presente le informazioni seguenti quando lavori con più metriche nei rapporti:

* È disponibile la possibilità di visualizzare più metriche per [Test A/B](/help/main/c-activities/t-test-ab/test-ab.md), [Allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md), [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md)e [Targeting esperienza](/help/main/c-activities/t-experience-target/experience-target.md) Solo attività (XT).
* Non puoi aggiungere più di 20 metriche a un rapporto per un&#39;attività che utilizza [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T). Puoi aggiungere quante metriche hai nell’attività ai rapporti per attività che *not* utilizza A4T.
* Non puoi utilizzare l&#39;opzione [](/help/main/c-reports/downloading-data-in-csv-file.md)Scarica per scaricare i rapporti in formato CSV se sono state selezionate più metriche. Devi selezionare una sola metrica per attivare l’opzione [!UICONTROL Scarica].
* Non puoi visualizzare più metriche per le attività create prima di luglio 2015 [!DNL Target] rilascio (30 luglio 2015).

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

   È possibile ridisporre le metriche trascinandole nell&#39;ordine desiderato nell&#39;elenco [!UICONTROL Metriche visualizzate]. L&#39;ordine selezionato verrà riportato nella [!UICONTROL Vista a tabella] e [!UICONTROL Vista grafico]. Per rimuovere una metrica dall&#39;elenco [!UICONTROL Metriche visualizzate], posiziona il puntatore del mouse sulla metrica, quindi fai clic sull&#39;icona **X**.

1. Al termine, fai clic su **[!UICONTROL Salva]**.
1. (Condizionale) Durante la visualizzazione del rapporto nel [!UICONTROL Vista a tabella], passa il puntatore del mouse sull’intestazione di colonna di qualsiasi metrica per visualizzare una freccia blu. Fai clic sulla freccia per espandere la tabella e visualizzare i parametri di [!UICONTROL Incremento] e [!UICONTROL Affidabilità] per tale metrica.

   ![](assets/multiple_metrics_table.png)

   È possibile espandere solo una metrica/colonna alla volta. Fai nuovamente clic sulla freccia per comprimere le colonne.

1. (Condizionale) Quando visualizzi il rapporto nella Vista grafico, puoi selezionare singole metriche da visualizzare dall’elenco a discesa:

   ![](assets/multiple_metrics_graph.png)
