---
keywords: Visual Experience Composer;VEC;carousel
description: Questo argomento illustra come creare un carosello che possa essere modificato nel Compositore esperienza visivo.
title: Creazione di caroselli di immagini adatti al Compositore esperienza visivo
feature: vec
translation-type: tm+mt
source-git-commit: 6704ac2ec73361ad95e110e9182485537d0de642
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 100%

---


# Creazione di caroselli di immagini adatti al Compositore esperienza visivo{#creating-carousels-that-work-in-the-visual-experience-composer}

Questo argomento illustra come creare un carosello che possa essere modificato nel Compositore esperienza visivo.

Quando esegui i passaggi seguenti, [!DNL Target] saprà sempre che la diapositiva selezionata avrà il “selettore” per la diapositiva corretta, anche se viene modificato nel Compositore esperienza visivo dopo pochi secondi.

1. Crea segnaposti HTML statici.

   ```html
   <ul>
   <li class="show"> slide 1 </li>
   <li class="hidden"> slide 2 </li>
   <li class="hidden"> slide 3 </li>
   </ul>
   ```

1. Aggiungi CSS per definire l’aspetto grafico.

   Non utilizzare JavaScript per questo.

   >[!NOTE]
   >
   >L’opzione [!UICONTROL Rendering con JavaScript] non è attualmente supportata se viene utilizzata con codice personalizzato nel Compositore esperienza visivo.

1. Aggiorna i valori classNames solo per nascondere le altre slide e mostrare quella successiva con timer/animazione.

   Non aggiornare mai la struttura DOM tramite JavaScript.