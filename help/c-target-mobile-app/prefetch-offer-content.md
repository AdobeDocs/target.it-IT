---
keywords: offerta;preacquisizione;iOS;android;sdk;mobile;sdk mobile
description: Utilizza la funzione di preacquisizione di Adobe [!DNL Target] negli SDK per dispositivi mobili iOS e Android per recuperare il contenuto delle offerte il minor numero di volte possibile, memorizzando nella cache le risposte dal server.
title: Posso preacquisire il contenuto dell’offerta per le app mobili?
feature: Implementare Mobile
role: Developer
exl-id: 83a96a41-cf27-4ed8-8169-277f3ef3f249
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 47%

---

# Preacquisire il contenuto dell’offerta

La funzione di preacquisizione di [!DNL Target] utilizza gli SDK per dispositivi mobili iOS e Android per recuperare il contenuto delle offerte il minor numero di volte possibile, memorizzando nella cache le risposte dal server.

Questo processo consente di ridurre il tempo di caricamento, evita l’esecuzione di più chiamate di rete e permette di notificare ad [!DNL Target] quale elemento mbox è stato visitato dall’utente dell’app mobile. Tutto il contenuto viene recuperato e memorizzato in cache durante la chiamata di preacquisizione, e da qual momento viene richiamato dalla cache per tutte le chiamate future che includono quel contenuto per il nome di mbox specificato.

Quando utilizzi il metodo di preacquisizione con gli SDK per dispositivi mobili iOS e Android, considera le seguenti limitazioni:

* Il contenuto di preacquisizione non rimane tra un avvio dell’app e quello successivo. Viene memorizzato nella cache per tutto il tempo in cui l’app rimane attiva oppure fino alla chiamata del metodo `clearPrefetchCache()`.
* La funzionalità di preacquisizione non è supportata per i tipi di attività [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico], per i tipi di attività [!UICONTROL Automated Personalization] o [!UICONTROL Recommendations] o per le offerte di consigli all&#39;interno di un&#39;attività A/B o XT](/help/c-recommendations/recommendations-as-an-offer.md).[

Per ulteriori informazioni, inclusi i metodi di preacquisizione, le classi pubbliche e gli esempi di codice, vedi:

* **iOS:**  [Preacquisire il contenuto delle offerte in ](https://experienceleague.adobe.com/docs/mobile-services/ios/target-ios/c-mob-target-prefetch-ios.html) iOSnella Guida dell&#39;SDK iOS di  *Mobile Services*.
* **Android:**  [Preacquisire il contenuto delle offerte in ](https://experienceleague.adobe.com/docs/mobile-services/android/target-android/c-mob-target-prefetch-android.html) Android nella Guida dell&#39;SDK per  *Mobile Services per Android*.
