---
keywords: offerta;preacquisizione;iOS;android;sdk;mobile;sdk mobile
description: Utilizzate la  funzione di preacquisizione Adobe Target negli SDK iOS e Android Mobile per recuperare il contenuto delle offerte il minor numero possibile di volte, memorizzando nella cache le risposte del server.
title: È possibile recuperare in anteprima il contenuto dell'offerta per le app mobili?
feature: Implement Mobile
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 47%

---


# Preacquisire il contenuto dell’offerta{#prefetch-offer-content}

La funzione di preacquisizione di [!DNL Target] utilizza gli SDK per dispositivi mobili iOS e Android per recuperare il contenuto delle offerte il minor numero di volte possibile, memorizzando nella cache le risposte dal server.

Questo processo consente di ridurre il tempo di caricamento, evita l’esecuzione di più chiamate di rete e permette di notificare ad [!DNL Target] quale elemento mbox è stato visitato dall’utente dell’app mobile. Tutto il contenuto viene recuperato e memorizzato in cache durante la chiamata di preacquisizione, e da qual momento viene richiamato dalla cache per tutte le chiamate future che includono quel contenuto per il nome di mbox specificato.

Considerate le seguenti limitazioni quando utilizzate il metodo di preacquisizione con gli SDK iOS e Android Mobile:

* Il contenuto di preacquisizione non rimane tra un avvio dell’app e quello successivo. Viene memorizzato nella cache per tutto il tempo in cui l’app rimane attiva oppure fino alla chiamata del metodo `clearPrefetchCache()`.
* La funzionalità di preacquisizione non è supportata per i metodi di allocazione del traffico [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target], per i tipi di attività [!UICONTROL  Automated Personalization] o [!UICONTROL Recommendations] o per le offerte di [raccomandazioni all&#39;interno di un&#39;attività A/B o XT](/help/c-recommendations/recommendations-as-an-offer.md).

Per ulteriori informazioni, inclusi i metodi di preacquisizione, le classi pubbliche e gli esempi di codice, vedi:

* **iOS:**  [Preacquisizione del contenuto dell&#39;offerta in ](https://experienceleague.adobe.com/docs/mobile-services/ios/target-ios/c-mob-target-prefetch-ios.html) iOS *nella guida* dell&#39;SDK per iOS Mobile Services.
* **Android:**  [Preacquisizione del contenuto delle offerte in ](https://experienceleague.adobe.com/docs/mobile-services/android/target-android/c-mob-target-prefetch-android.html) Android nella guida *dell&#39;SDK per* Mobile Services Android.
