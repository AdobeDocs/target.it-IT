---
description: La funzione di preacquisizione di Adobe Target utilizza gli SDK per dispositivi mobili iOS e Android per recuperare il contenuto delle offerte il minor numero di volte possibile, memorizzando nella cache le risposte dal server.
keywords: offerta;preacquisizione;iOS;Android; sdk; mobile; SDK per dispositivi mobili
seo-description: La funzione di preacquisizione di Adobe Target utilizza gli SDK per dispositivi mobili iOS e Android per recuperare il contenuto delle offerte il minor numero di volte possibile, memorizzando nella cache le risposte dal server.
seo-title: Preacquisire il contenuto dell’offerta
solution: Target
title: Preacquisire il contenuto dell’offerta
topic: Advanced,Standard,Classic
uuid: 715e0e77-bfd9-437b-b42c-899d66f2890c
translation-type: tm+mt
source-git-commit: 95bf4b2070cc2de235ac09ac164f0f9ec48dd6cd

---


# Preacquisire il contenuto dell’offerta{#prefetch-offer-content}

La funzione di preacquisizione di [!DNL Target] utilizza gli SDK per dispositivi mobili iOS e Android per recuperare il contenuto delle offerte il minor numero di volte possibile, memorizzando nella cache le risposte dal server.

Questo processo consente di ridurre il tempo di caricamento, evita l’esecuzione di più chiamate di rete e permette di notificare ad [!DNL Target] quale elemento mbox è stato visitato dall’utente dell’app mobile. Tutto il contenuto viene recuperato e memorizzato nella cache durante la chiamata di preacquisizione e questo contenuto viene recuperato dalla cache per tutte le chiamate future che contengono contenuto memorizzato nella cache per il nome mbox specificato.

Quando usi nel metodo preacquisizione con gli SDK di iOS e Android Mobile, prendi in considerazione quanto segue:

* Il contenuto di preacquisizione non rimane tra un avvio dell'app e quello successivo. Viene memorizzato nella cache per tutto il tempo in cui l’app rimane attiva oppure fino alla chiamata del metodo `clearPrefetchCache()`.
* La funzionalità di preacquisizione negli SDK iOs e Android Mobile non è supportata per i tipi di attività Auto Target, Allocazione automatica e Automated Personalization (Personalizzazione automatizzata).

Per ulteriori informazioni, inclusi i metodi di preacquisizione, le classi pubbliche e gli esempi di codice, vedi:

* **iOS:** [Preacquisizione del contenuto dell'offerta in iOS](https://marketing.adobe.com/resources/help/en_US/mobile/ios/c_mob_target-prefetch_ios.html) nella guida *iOS SDK 4.x per Experience Cloud Solutions*.
* **Android:** [Preacquisizione del contenuto dell'offerta in Android](https://marketing.adobe.com/resources/help/en_US/mobile/android/c_mob_target-prefetch_android.html) nella guida *Android SDK 4.x per Experience Cloud Solutions*.
