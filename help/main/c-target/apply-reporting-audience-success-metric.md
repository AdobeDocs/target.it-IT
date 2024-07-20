---
keywords: Targeting;pubblico;creazione di rapporti;metrica di successo
description: Scopri come scegliere una metrica di successo in [!DNL Adobe Target] che qualifichi l'utente per il pubblico di reportistica.
title: Posso applicare un pubblico di reportistica a una metrica di successo?
feature: Success Metrics
exl-id: 6b2f6669-6178-4da4-850d-8b1ce796a50d
source-git-commit: bcbb6dec9d6add07c109b07bf125c1356ad2a8b9
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 33%

---

# Applicare un pubblico di reportistica a una metrica di successo

Scegliere una metrica di successo che qualifichi l&#39;utente per il pubblico di reportistica in [!DNL Adobe Target].

Per tutte le attività, l&#39;elenco a discesa [!UICONTROL Applied At] consente di applicare un pubblico a una metrica di successo in modo da poter visualizzare i numeri di reporting dopo che la metrica è stata raggiunta e per le azioni successive.

![immagine di successo](assets/success_metric.png)

Ad esempio, supponi di aver creato un’attività per tutti i visitatori che accedono all’attività dalla pagina principale e arrivano alla pagina di conversione; inoltre, desideri approfondire l’analisi per i visitatori che hanno aggiunto al carrello articoli per un valore superiore ai 50 $ prima della conversione.

L&#39;elenco a discesa [!UICONTROL Applied At] fornisce potenzialmente tre categorie:

* Qualsiasi visitatore dell’attività
* Solo i visitatori che raggiungono un determinato passaggio nell’attività
* Solo i visitatori che raggiungono la conversione

Oppure, per formularlo in altro modo, è possibile specificare che un visitatore deve aver raggiunto una mbox sulla pagina di accesso all’attività, una mbox che definisce un certo punto nel mezzo dell’attività o la mbox di conversione alla fine dell’attività.

>[!NOTE]
>
>[Le metriche di successo](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) sono disponibili solo se sono state configurate per l’attività. Se non sono state definite metriche di successo, verranno visualizzate solo due opzioni dall&#39;elenco a discesa: [!UICONTROL Campaign Entry] e [!UICONTROL Conversion].


## Considerazioni

Considera le seguenti informazioni quando applichi un pubblico per la reportistica a una metrica di successo:

* Solo le metriche di successo che iniziano da quella a cui viene applicato il pubblico mostreranno i dati di reporting segmentati dal pubblico
* Le metriche di successo che precedono quelle a cui è applicato il pubblico non verranno segmentate dal pubblico e mostreranno tutti i dati dei visitatori
* Le metriche vengono considerate in base al loro ordine nella definizione dell&#39;attività, con [!UICONTROL Primary Goal] come ultimo.

## Visualizzare la segmentazione nel reporting

Per visualizzare la segmentazione nel reporting, seleziona il pubblico desiderato dall&#39;elenco a discesa [!UICONTROL Audience] nel rapporto dell&#39;attività.

![immagine a discesa reporting_audience](assets/reporting_audience_dropdown.png)

## Esempio

Prendi in considerazione un’attività con Metrica di successo1, Metrica di successo2, Metrica di successo3 e Obiettivo principale.

Supponiamo di avere il Pubblico di reportistica1 impostato su &quot;Entrata&quot; e il Pubblico di reportistica2 impostato su Metrica di successo2. I tipi di pubblico filtrano i dati di reporting come segue:

|  | Visitatori | Metrica di successo1 | Metrica di successo 2 | Metrica di successo3 | Obiettivo principale |
| --- | --- | --- | --- | --- | --- |
| Pubblico1 | Applicato | Applicato | Applicato | Applicato | Applicato |
| Pubblico2 | Non applicato | Non applicato | Applicato | Applicato | Applicato |
