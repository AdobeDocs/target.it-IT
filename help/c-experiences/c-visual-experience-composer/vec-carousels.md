---
keywords: Compositore esperienza visivo;VEC;carosello
description: Scopri come creare un carosello che può essere modificato in Adobe [!DNL Target] Compositore esperienza visivo (VEC).
title: Come si creano i caroselli di immagini nel Compositore esperienza visivo?
feature: Compositore esperienza visivo
exl-id: 50bc11d2-c9fc-4b53-8218-49842b59269a
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 71%

---

# Creazione di caroselli di immagini adatti al Compositore esperienza visivo

Questo argomento illustra come creare un carosello che possa essere modificato nel [!DNL Adobe Target] [!UICONTROL Compositore esperienza visivo] (VEC).

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
