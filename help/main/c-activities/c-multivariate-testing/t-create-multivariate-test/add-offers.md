---
keywords: mvt;test multivariato;offerte;combinazioni
description: Scopri come utilizzare il [!UICONTROL Compositore esperienza visivo] (VEC) in Adobe [!DNL Target] per creare le offerte da includere nel [!UICONTROL Test multivariato] (MVT)
title: Come si creano le combinazioni in una [!UICONTROL Test multivariato] (MVT)
feature: Multivariate Tests
exl-id: 8b5883de-de76-403d-ae20-c933a8665555
source-git-commit: 7853d8c5934e40d1026e067dfa413f520ecba931
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 71%

---

# Creare combinazioni

Utilizza il [!UICONTROL Compositore esperienza visivo] (VEC) in [!DNL Adobe Target] per creare le offerte da includere nel [!UICONTROL Test multivariato] (MVT)

Per ulteriori informazioni sull’utilizzo del Compositore esperienza visivo per creare e modificare le offerte, consulta [Opzioni del Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

>[!NOTE]
>
>Fai clic su **[!UICONTROL Espandi selezione]** durante la scelta degli oggetti nella pagina per selezionare l’elemento principale in aggiunta all’elemento selezionato originariamente. Quando selezioni un elemento padre, tutti i relativi figli vengono selezionati automaticamente. Puoi espandere la selezione più volte.
>
>Per navigare tra gli elementi puoi anche usare il [percorso DOM](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path).

## Offerte immagine {#section_A48333211DB149ED926AE467D0032914}

Sottoponi a test offerte di immagini multiple all’interno di una posizione per determinare quale immagine ha più successo.

1. Fa clic su un&#39;immagine nella pagina e quindi seleziona **[!UICONTROL Cambia immagine]**.

   ![Opzione Cambia immagine](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/changeimage.png)

1. Seleziona tutte le immagini da includere nel test, quindi fai clic su **[!UICONTROL Salva]**.

   ![Finestra di dialogo Seleziona contenuto per aggiungere immagini](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/addimage.png)

Ogni immagine diventa un&#39;esperienza separata nella posizione in questione.

## Offerte HTML {#section_DF016101AFA9412C9B99862C23DE77B1}

Sottoponi a test offerte in formato testo/HTML multiple all’interno di una posizione per determinare quale sia la più efficace.

1. Fai clic su un’offerta in formato test/HTML nella pagina e quindi fai clic su **[!UICONTROL Cambia testo/HTML]**.

   ![Cambia testo/HTML](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/changehtml.png)

1. Fai clic su **[!UICONTROL Aggiungi offerta testo/HTML]**, assegna un nome all’offerta, quindi digita o incolla il codice per l’offerta in formato testo/HTML.

   ![Modificare le offerte](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/editoffers.png)

   Ripeti l’operazione per eventuali altre offerte in formato testo/HTML da includere.

1. Fai clic su **[!UICONTROL Salva]**.

Ogni offerta in formato testo/HTML diventa un’esperienza separata nella posizione in questione.

## Best practice {#section_2E98C23D2F1A460FA732A31799CE6291}

* Non includere più posizioni del necessario per il test. Ogni esperienza inclusa nel test aumenta in modo significativo la quantità di traffico e di tempo necessari per ottenere risultati accettabili. Ad esempio, in presenza di elementi della pagina con tre offerte ciascuno, le possibili combinazioni sono nove (3x3). Tre elementi, di cui due includono tre offerte possibili e uno due offerte, forniscono 18 alternative (3x3x2). Le cifre aumentano in modo significativo per ogni elemento e offerta supplementare.
* Quando si creano test multivariati, è possibile escludere più del 10% di esperienze dal test, purché si riconosca l’avviso che è necessario utilizzare il reporting offline per l’analisi.
* Sfrutta le funzioni di anteprima per evitare combinazioni di contenuto indesiderate. Ad esempio, due immagini potrebbero offrire sconti diversi sullo stesso elemento o servizio. Visualizzare entrambe le immagini sulla stessa pagina è illogico e rischia di creare confusione.
* Utilizza il [Calcolatore del traffico](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md) per assicurarti che il test sia progettato per la quantità di traffico ricevuto dalla pagina. Assicurati che il Calcolatore del traffico fornisca alla configurazione di test la luce verde in modo da ottenere i risultati desiderati.
* È necessario disporre di almeno tre elementi per eseguire il test. Se il numero è inferiore, esegui una serie di test A/B.
* Le alternative di ciascun elemento dovrebbero essere significativamente diverse tra loro.
* Anche se non obbligatorio, è buona norma che per ogni elemento sia presente lo stesso numero di alternative.
