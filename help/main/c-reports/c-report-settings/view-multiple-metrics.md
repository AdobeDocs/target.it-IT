---
keywords: Target;report;impostazioni report;metriche multiple;metriche;metriche visualizzate;metriche nascoste;Target;reports;report settings;multiple metrics;metrics;viewed metrics;hidden metrics
description: Scopri come selezionare più metriche da visualizzare in un rapporto utilizzando Adobe Target.
title: Come si visualizzano più metriche in un rapporto?
feature: Reports
exl-id: 8d8aedd8-4583-4131-8ae0-df14e071940a
source-git-commit: c1a71d1fb6fa9b5c14e22fa3199358a4594bb4a1
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 12%

---

# Visualizzare più metriche in un rapporto

È possibile selezionare più metriche da visualizzare in un report [!DNL Adobe Target].

Tieni presente le informazioni seguenti quando lavori con più metriche nei rapporti:

* La possibilità di visualizzare più metriche è disponibile solo per le attività [Test A/B](/help/main/c-activities/t-test-ab/test-ab.md), [Allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md), [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) e [Targeting esperienza](/help/main/c-activities/t-experience-target/experience-target.md) (XT).
* Impossibile aggiungere più di 20 metriche a un report per un&#39;attività che utilizza [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T). Puoi aggiungere ai rapporti tutte le metriche disponibili nell&#39;attività per le attività che *non* utilizzano A4T.
* Se hai selezionato più metriche, non puoi utilizzare l&#39;[opzione di download](/help/main/c-reports/c-report-settings/downloading-data-in-csv-file.md) per scaricare i rapporti in formato CSV. Selezionare una sola metrica per abilitare l&#39;opzione [!UICONTROL Download].
* Non è possibile visualizzare più metriche per le attività create prima della versione di [!DNL Target] di luglio 2015 (30 luglio 2015).

**Per selezionare più metriche da visualizzare nel rapporto:**

1. Per visualizzare un report, fare clic su **[!UICONTROL Activities]**, selezionare l&#39;attività desiderata dall&#39;elenco, quindi fare clic sulla scheda **[!UICONTROL Reports]**.
1. Fare clic sull&#39;elenco a discesa **[!UICONTROL Report Metric]** per visualizzare gli elenchi [!UICONTROL Shown Metrics] e [!UICONTROL Hidden Metrics].

   La casella [!UICONTROL Search] consente di trovare rapidamente le metriche disponibili da aggiungere all&#39;elenco [!UICONTROL Shown Metrics].

   Si noti che è possibile selezionare più metriche dalle modalità [!UICONTROL Table View] e [!UICONTROL Graph View] del report.

1. Passa il puntatore del mouse sulle metriche desiderate nell&#39;elenco [!UICONTROL Hidden Metrics], quindi fai clic su **[!UICONTROL Select]** per spostarle nell&#39;elenco [!UICONTROL Shown Metrics].

   Oppure

   Trascinare le metriche desiderate dall&#39;elenco [!UICONTROL Hidden Metrics] all&#39;elenco [!UICONTROL Shown Metrics].

   Deve essere presente almeno una metrica nell&#39;elenco [!UICONTROL Shown Metrics].

   È possibile ridisporre le metriche trascinandole nell&#39;ordine desiderato nell&#39;elenco [!UICONTROL Shown Metrics]. L&#39;ordine selezionato verrà riflesso in [!UICONTROL Table View] e [!UICONTROL Graph View]. Per rimuovere una metrica dall&#39;elenco [!UICONTROL Shown Metrics], posiziona il puntatore del mouse sulla metrica, quindi fai clic sull&#39;icona **X**.

1. Al termine, fare clic su **[!UICONTROL Save]**.
1. (Condizionale) Quando visualizzi il report in [!UICONTROL Table View], passa il puntatore del mouse sull&#39;intestazione di colonna di una metrica per visualizzare una freccia blu. Fare clic sulla freccia per espandere la tabella e visualizzare [!UICONTROL Lift] e [!UICONTROL Confidence] per la metrica.

   È possibile espandere solo una metrica/colonna alla volta. Fai nuovamente clic sulla freccia per comprimere le colonne.

1. (Condizionale) Quando visualizzi il rapporto in [!UICONTROL Graph View], puoi selezionare singole metriche da visualizzare dall&#39;elenco a discesa.
