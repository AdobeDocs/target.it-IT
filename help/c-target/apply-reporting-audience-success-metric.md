---
keywords: Targeting;pubblico;creazione di rapporti;metrica di successo
description: Scopri come scegliere una metrica di successo in [!DNL Adobe Target] che qualifichi l’utente per il pubblico di reporting.
title: Posso applicare un pubblico di reportistica a una metrica di successo?
feature: Metriche di successo
exl-id: 6b2f6669-6178-4da4-850d-8b1ce796a50d
source-git-commit: 20a5201b5c05b1f083252ac73b3b4bbc91e97aaa
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 54%

---

# Applicare un pubblico di reportistica a una metrica di successo

Scegli una metrica di successo che qualifichi l’utente per il pubblico di reporting in [!DNL Adobe Target].

Per tutte le attività, l’elenco a discesa [!UICONTROL Applicato a] consente di applicare un pubblico a una metrica di successo in modo da poter visualizzare i numeri per i rapporti una volta conseguita tale metrica e per le azioni successive.

![](assets/success_metric.png)

Ad esempio, supponi di aver creato un’attività per tutti i visitatori che accedono all’attività dalla pagina principale e arrivano alla pagina di conversione; inoltre, desideri approfondire l’analisi per i visitatori che hanno aggiunto al carrello articoli per un valore superiore ai 50 $ prima della conversione.

L&#39;elenco a discesa [!UICONTROL Applicato a] può fornire tre categorie: qualsiasi visitatore dell’attività, solo i visitatori che raggiungono un determinato passaggio nell’attività o solo i visitatori che raggiungono la conversione. Oppure, per formularlo in altro modo, è possibile specificare che un visitatore deve aver raggiunto una mbox sulla pagina di accesso all’attività, una mbox che definisce un certo punto nel mezzo dell’attività o la mbox di conversione alla fine dell’attività.

[Le metriche di successo](/help/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) sono disponibili solo se sono state configurate per l’attività. Se non hai definito le metriche di successo, vedrai solo due opzioni dall&#39;elenco a discesa: [!UICONTROL Ingresso campagna] e [!UICONTROL Conversione].

Considera le seguenti informazioni quando applichi un pubblico per la reportistica a una metrica di successo:

* Per le azioni prima dell’azione con la metrica di successo applicata, [!DNL Target] non applica un pubblico segmentato.
* Per le azioni successive alla metrica di successo applicata, [!DNL Target] applica un pubblico segmentato.

Per visualizzare la segmentazione nel reporting, seleziona il pubblico desiderato dall’elenco a discesa [!UICONTROL Pubblico] nel rapporto dell’attività.

![](assets/reporting_audience_dropdown.png)
