---
keywords: offer;prefetch;iOS;android;sdk;mobile;mobile sdk
description: La funzione di preacquisizione di Adobe Target utilizza gli SDK per dispositivi mobili iOS e Android per recuperare il contenuto delle offerte il minor numero di volte possibile, memorizzando nella cache le risposte dal server.
title: Preacquisire il contenuto dell’offerta
topic: Advanced,Standard,Classic
uuid: 715e0e77-bfd9-437b-b42c-899d66f2890c
translation-type: tm+mt
source-git-commit: 4f877bf6a0bd73e2d29c2d41ab64dc2a39c61a31

---


# Preacquisire il contenuto dell’offerta{#prefetch-offer-content}

La funzione di preacquisizione di [!DNL Target] utilizza gli SDK per dispositivi mobili iOS e Android per recuperare il contenuto delle offerte il minor numero di volte possibile, memorizzando nella cache le risposte dal server.

Questo processo consente di ridurre il tempo di caricamento, evita l’esecuzione di più chiamate di rete e permette di notificare ad [!DNL Target] quale elemento mbox è stato visitato dall’utente dell’app mobile. Tutto il contenuto viene recuperato e memorizzato in cache durante la chiamata di preacquisizione, e da qual momento viene richiamato dalla cache per tutte le chiamate future che includono quel contenuto per il nome di mbox specificato.

Considerate le seguenti limitazioni quando utilizzate il metodo di preacquisizione con gli SDK iOS e Android Mobile:

* Il contenuto di preacquisizione non rimane tra un avvio dell’app e quello successivo. Viene memorizzato nella cache per tutto il tempo in cui l’app rimane attiva oppure fino alla chiamata del metodo `clearPrefetchCache()`.
* La funzionalità di recupero preventivo non è supportata per i metodi di allocazione del traffico [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target] , per i tipi di attività [!UICONTROL Automated Personalization (Personalizzazione] automatizzata) o [!UICONTROL Recommendations] o per le offerte di [raccomandazioni all'interno di un'attività](/help/c-recommendations/recommendations-as-an-offer.md)A/B o XT.

Per ulteriori informazioni, inclusi i metodi di preacquisizione, le classi pubbliche e gli esempi di codice, vedi:

* **** iOS:  Preacquisizione [del contenuto delle offerte in iOS](https://docs.adobe.com/content/help/en/mobile-services/ios/target-ios/c-mob-target-prefetch-ios.html) nella guida ** dell'SDK per iOS Mobile Services.
* **** Android:  Preacquisizione [del contenuto delle offerte in Android](https://docs.adobe.com/content/help/en/mobile-services/android/target-android/c-mob-target-prefetch-android.html) nella guida *dell'SDK per Android di* Mobile Services.
