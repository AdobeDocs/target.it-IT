---
keywords: offerta;preacquisizione;iOS;android;sdk;mobile;sdk mobile
description: Utilizza l’Adobe [!DNL Target] funzione di preacquisizione negli SDK per dispositivi mobili iOS e Android per recuperare il contenuto delle offerte il minor numero di volte possibile, memorizzando nella cache le risposte dal server.
title: Posso preacquisire il contenuto dell’offerta per le app mobili?
feature: Implement Mobile
role: Developer
exl-id: 83a96a41-cf27-4ed8-8169-277f3ef3f249
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 54%

---

# Preacquisire il contenuto dell’offerta

La funzione di preacquisizione di [!DNL Target] utilizza gli SDK per dispositivi mobili iOS e Android per recuperare il contenuto delle offerte il minor numero di volte possibile, memorizzando nella cache le risposte dal server.

Questo processo consente di ridurre il tempo di caricamento, evita l’esecuzione di più chiamate di rete e permette di notificare ad [!DNL Target] quale elemento mbox è stato visitato dall’utente dell’app mobile. Tutto il contenuto viene recuperato e memorizzato in cache durante la chiamata di preacquisizione, e da qual momento viene richiamato dalla cache per tutte le chiamate future che includono quel contenuto per il nome di mbox specificato.

Quando utilizzi il metodo di preacquisizione con gli SDK per dispositivi mobili iOS e Android, considera le seguenti limitazioni:

* Il contenuto di preacquisizione non rimane tra un avvio dell’app e quello successivo. Viene memorizzato nella cache per tutto il tempo in cui l’app rimane attiva oppure fino alla chiamata del metodo `clearPrefetchCache()`.

Per ulteriori informazioni, inclusi i metodi di preacquisizione, le classi pubbliche e gli esempi di codice, vedi:

* **iOS:**  [Preacquisizione del contenuto delle offerte in iOS](https://experienceleague.adobe.com/docs/mobile-services/ios/target-ios/c-mob-target-prefetch-ios.html) in *Guida all&#39;SDK per iOS di Mobile Services*.
* **Android:**  [Preacquisizione del contenuto delle offerte in Android](https://experienceleague.adobe.com/docs/mobile-services/android/target-android/c-mob-target-prefetch-android.html) in *Guida all’SDK per Android Mobile Services*.
