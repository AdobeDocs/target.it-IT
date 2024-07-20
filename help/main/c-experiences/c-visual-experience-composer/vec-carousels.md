---
keywords: Compositore esperienza visivo;VEC;carosello
description: Scopri come creare un carosello che può essere modificato nell'Adobe  [!DNL Target] Compositore esperienza visivo.
title: Come posso creare caroselli di immagini nel Compositore esperienza visivo?
feature: Visual Experience Composer (VEC)
exl-id: 50bc11d2-c9fc-4b53-8218-49842b59269a
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 58%

---

# Creazione di caroselli di immagini adatti al Compositore esperienza visivo

In questo argomento viene illustrato come creare un carosello modificabile nel [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC).

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
   >L&#39;opzione [!UICONTROL Render Using JavaScript] non è attualmente supportata se viene utilizzata insieme al codice personalizzato nel Compositore esperienza visivo.

1. Aggiorna i valori classNames solo per nascondere le altre slide e mostrare quella successiva con timer/animazione.

   Non aggiornare mai la struttura DOM tramite JavaScript.
