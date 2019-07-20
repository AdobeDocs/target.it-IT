---
description: Il Compositore esperienza visivo mobile supporta l’impostazione degli obiettivi di tracciamento dei clic per le attività Target.
keywords: VEC app mobile;compositore esperienza visivo mobile;opzioni compositore esperienza mobile;opzioni esperienza mobile;visualizzazione di target;clic, tracciamento dei clic;tracciare
seo-description: Il Compositore esperienza visivo mobile supporta l’impostazione degli obiettivi di tracciamento dei clic per le attività di Adobe Target.
seo-title: Configurare il tracciamento dei clic nel Compositore esperienza visivo per app mobile
solution: Target
title: Configurare il tracciamento dei clic nel Compositore esperienza visivo per app mobile
topic: Standard
uuid: 7e4ce7c0-0027-417c-8dae-45b6f5045e65
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Configurare il tracciamento dei clic nel Compositore esperienza visivo per app mobile{#set-up-click-tracking-in-the-mobile-vec}

Il Compositore esperienza visivo mobile supporta l’impostazione degli obiettivi di tracciamento dei clic per le attività [!DNL Target].

1. Quando imposterai gli obiettivi dell'attività nella pagina Obiettivi e impostazioni, seleziona la metrica di successo [!UICONTROL Conversione].

   ![](assets/mobile-vec-clicktrack1.png)

1. Per eseguire tale azione, seleziona **[!UICONTROL Scegli un elemento]**, quindi fai clic su **[!UICONTROL Seleziona elementi]**.

   L’applicazione per dispositivi mobili viene visualizzata nel Compositore esperienza visivo (VEC) mobile.

   ![](assets/mobile-vec-clicktrack2.png)

1. Seleziona gli elementi di cui desideri tenere traccia.

   Per suggerimenti sulla selezione degli elementi, consulta la sezione [!UICONTROL Considerazioni] di seguito.

   ![](assets/mobile-vec-clicktrack3.png)

1. Fai clic sul segno di spunta nella parte superiore dello schermo per salvare le selezioni.

È inoltre possibile modificare e cambiare le selezioni dei clic o eliminarle se è necessario iniziare da zero.

![](assets/mobile-vec-clicktrack4.png)

Quando un partecipante all'attività fa clic su un elemento selezionato, tale clic viene conteggiato come conversione.

## Considerazioni {#considerations}

Ci sono diversi fattori da considerare quando si selezionano gli elementi:

* Quando sono selezionati più elementi e un visitatore fa clic su uno di essi, viene conteggiato il clic. Per contare ogni clic separatamente, imposta le metriche di successo individuali per ogni elemento.
* Gli eventi di clic vengono inviati a Target non appena l'utente fa clic sull'elemento.
* Nel Compositore esperienza visivo per app mobile, sono consentiti solo gli elementi con un gestore di clic allegato.
* Puoi passare a qualsiasi sezione dell'applicazione, ma assicurati che le [visualizzazioni](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md#target-views) siano definite per la sezione in cui stai selezionando gli elementi per il tracciamento dei clic.
* Durante la modifica di un'attività, se il dispositivo è già selezionato nel Passaggio 1, non è necessario selezionare nuovamente il dispositivo. Tuttavia, se arrivi direttamente alla pagina di tracciamento dei clic, verrà visualizzata la schermata di selezione del dispositivo per selezionare un dispositivo autorizzato.
