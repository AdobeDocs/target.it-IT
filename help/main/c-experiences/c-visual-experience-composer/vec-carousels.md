---
keywords: Compositore esperienza visivo;VEC;carosello
description: Scopri come creare un carosello che può essere modificato nel Compositore esperienza visivo di Adobe [!DNL Target].
title: Come posso creare caroselli di immagini nel Compositore esperienza visivo?
feature: Visual Experience Composer (VEC)
exl-id: 50bc11d2-c9fc-4b53-8218-49842b59269a
TQID: 'https://experienceleague.adobe.com/RN04MJgC49BI2-h2e-i-kgSRTejpLHzKACm-hOv2VCE'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 2%
---
# Creazione di caroselli di immagini adatti al [!UICONTROL Compositore esperienza visivo] {#vec-carousels}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come creare un carosello che può essere modificato nel **[!UICONTROL Compositore esperienza visivo]**.

>[!ENDSHADEBOX]

Un carosello creato con la seguente struttura può essere modificato nel [!DNL Adobe Target] **[!UICONTROL Compositore esperienza visivo]** (VEC). La struttura mantiene valido il selettore di ogni diapositiva, pertanto [!DNL Target] identifica sempre la diapositiva corretta, anche quando la diapositiva visualizzata cambia pochi secondi dopo il caricamento della pagina nel Compositore esperienza visivo.

1. Creare le diapositive come segnaposto statici di HTML, con una diapositiva visibile e le altre diapositive nascoste per classe.

   ```html
   <ul>
   <li class="show"> slide 1 </li>
   <li class="hidden"> slide 2 </li>
   <li class="hidden"> slide 3 </li>
   </ul>
   ```

1. Progetta il look and feel solo con CSS. Non utilizzare JavaScript per questo.

   >[!NOTE]
   >
   >L&#39;opzione **[!UICONTROL Rendering con JavaScript]** non è attualmente supportata se utilizzata insieme al codice personalizzato nel **[!UICONTROL Compositore esperienza visivo]**.

1. Visualizzare la diapositiva successiva aggiornando solo i nomi delle classi: nascondere le altre diapositive e mostrare quella successiva con un timer o un&#39;animazione. Non aggiornare mai la struttura DOM con JavaScript.
