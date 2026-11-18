---
keywords: mvt;test multivariato;offerte;combinazioni
description: Scopri come utilizzare il [!UICONTROL Compositore esperienza visivo] (VEC) in Adobe [!DNL Target] per creare le offerte da includere nel [!UICONTROL test multivariato] (MVT).
title: Come si creano combinazioni in un [!UICONTROL test multivariato] (MVT)?
feature: Multivariate Tests
exl-id: 8b5883de-de76-403d-ae20-c933a8665555
TQID: 'https://experienceleague.adobe.com/3vxuP07ZViE1etmmvBdYVHIOrtZqRZfL3nE5RMHo9rU'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: b934e7cf-c07f-5a64-924b-3c9da8413e3d
    internal-label: Multivariate Tests
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 0ae6991a6a86854bd64a632070a1fcbe544cc606
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 29%
---
# Creare combinazioni {#create-combinations}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come creare l&#39;immagine e le offerte HTML che costituiscono le combinazioni di un **[!UICONTROL test multivariato]**.

>[!ENDSHADEBOX]

In un **[!UICONTROL test multivariato]** (MVT), ogni posizione contiene diverse offerte e ogni combinazione di offerte nelle posizioni è un&#39;esperienza. Utilizza il **[!UICONTROL Compositore esperienza visivo]** (VEC) in [!DNL Adobe Target] per creare le offerte da includere nel test.

Per ulteriori informazioni sull’utilizzo del Compositore esperienza visivo per creare e modificare le offerte, consulta [Opzioni del Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

>[!NOTE]
>
>È possibile fare clic su **[!UICONTROL Espandi selezione]** quando si selezionano oggetti nella pagina per selezionare l&#39;elemento padre in aggiunta all&#39;elemento selezionato originariamente. Quando selezioni un elemento principale, tutti i relativi elementi secondari vengono selezionati automaticamente. Puoi espandere la selezione più volte.
>
>Per navigare tra gli elementi puoi anche usare il [percorso DOM](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path).

## Offerte immagine {#image-offers}

Sottoponi a test offerte immagine multiple all&#39;interno di una posizione per determinare quale immagine sia più efficace.

1. Fai clic su un&#39;immagine nella pagina e seleziona **[!UICONTROL Modifica offerta immagine]**.

   ![Modifica menu offerta immagine](../assets/multivariate-1.png)

1. Dalla finestra di dialogo **[!UICONTROL Offerta immagine]**, seleziona tutte le immagini che desideri includere nel test, quindi fai clic su **[!UICONTROL Aggiungi]**.

   ![Modifica menu offerta immagine](../assets/multivariate-3.png)

Ogni immagine diventa un&#39;esperienza separata nella posizione in questione.

## Offerte HTML {#html-offers}

Sottoponi a test offerte HTML multiple all&#39;interno di una posizione per determinare quale sia più efficace.

1. Fai clic su un&#39;offerta HTML nella tua pagina, quindi fai clic su **[!UICONTROL Modifica offerta HTML]**.

   ![Modifica il menu Offerta HTML](../assets/multivariate-2.png)

1. Scegli la tua offerta HTML e fai clic su **[!UICONTROL Crea offerta]** e quindi su **[!UICONTROL Offerta HTML]**.

   ![Modifica il menu Offerta HTML](../assets/multivariate-4.png)

1. Assegna un nome all&#39;offerta, digita o incolla il codice per l&#39;offerta HTML, quindi fai clic su **[!UICONTROL Crea]**.

   Ripeti l’operazione per eventuali altre offerte HTML da includere.

1. Fai clic su **[!UICONTROL Salva]**.

Ogni offerta HTML diventa un&#39;esperienza separata nella posizione in questione.

Per raccomandazioni su quante combinazioni includere e su come rivederle prima di avviare il test, consulta [Best practice per i test multivariati](/help/main/c-activities/c-multivariate-testing/best-practices.md#create).
