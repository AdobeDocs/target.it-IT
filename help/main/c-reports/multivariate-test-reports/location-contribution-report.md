---
keywords: MVT;test multivariato;rapporto contributo posizione
description: Scopri come utilizzare il rapporto Contributo posizione per le attività Adobe [!DNL Target] [!UICONTROL Experience Targeting] che mostrano le prestazioni di ogni elemento e di ogni offerta.
title: Come si utilizza il report [!UICONTROL Location Contribution] per le attività [!UICONTROL Multivariate Test]?
feature: Reports
exl-id: 2fb7d2b3-d981-44fd-9bb2-021903605a09
source-git-commit: 6f70ff18cfbee5c02e6bb2bd345acbd2e1b2006f
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 39%

---

# Rapporto [!UICONTROL Location Contribution] (MVT)

Il report [!UICONTROL Location Contribution] mostra le prestazioni di ogni elemento e di ogni offerta.

La parte superiore del rapporto mostra la metrica, le date di inizio e fine e il pubblico utilizzato nel rapporto. Puoi modificare ciascuno di questi fattori.

>[!NOTE]
>
>Tenere presenti le seguenti informazioni mentre si utilizza il report [!UICONTROL Location Contribution]:
>
>* I selettori di pubblico e metriche sono disponibili solo se [!DNL Analytics] è utilizzato come origine per la generazione di rapporti (A4T).
>
>* I dati per il report [!UICONTROL Location Contribution] vengono recuperati dal backend [!DNL Target] anche se l&#39;attività è configurata per l&#39;utilizzo di [!UICONTROL Analytics as the reporting source] (A4T).
>
>* I dati per il report [!UICONTROL Location Contribution] vengono recuperati per l&#39;ambiente &quot;Produzione&quot; anche se a livello di account [!DNL Target] è definito un ambiente predefinito diverso.

Il report [!UICONTROL Location Contribution] include due tabelle.

La prima tabella mostra l’influenza relativa di ogni elemento. Questa tabella mostra quali degli elementi in cui sono state aggiunte le offerte generano il maggior numero di conversioni.

![Rapporto sul contributo posizione in Adobe Target](/help/main/c-reports/assets/locationcontributiontop.png)

La seconda tabella fornisce un rapporto a livello di offerta. Mostra tasso di conversione, incremento e affidabilità per ogni offerta in ogni elemento. Questa tabella consente di determinare quali offerte sono più efficaci. La seconda colonna mostra i valori per la metrica selezionata (tasso di conversione, ricavo per visita, valore medio dell’ordine, ordini o metriche di coinvolgimento) dell’offerta e di una standardizzazione.

![Rapporto sul contributo posizione in Adobe Target](/help/main/c-reports/assets/locationcontributionbottom.png)

## Video di formazione: crea un test MVT ![Icona esercitazione](/help/main/assets/tutorial.png)

In questo video viene illustrato come creare un test multivariato utilizzando il flusso di lavoro guidato in tre passaggi di Target. Il rapporto Contributo posizione è descritto a partire dal minuto 8:45.

>[!VIDEO](https://video.tv.adobe.com/v/17395)
