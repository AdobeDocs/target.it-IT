---
keywords: Visual Experience Composer;VEC;carousel
description: In questo argomento viene illustrato come creare un carosello che può essere modificato in  Adobe Target Visual Experience Composer (VEC).
title: Creazione di caroselli di immagini adatti al Compositore esperienza visivo
feature: Visual Experience Composer (VEC)
translation-type: tm+mt
source-git-commit: 8110807a73e4d6d9848a52224db04faba033c98c
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 74%

---


# Creazione di caroselli di immagini adatti al Compositore esperienza visivo

In questo argomento viene illustrato come creare un carosello che può essere modificato in [!DNL Adobe Target] [!UICONTROL Visual Experience Composer (Compositore esperienza visivo)] (VEC).

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