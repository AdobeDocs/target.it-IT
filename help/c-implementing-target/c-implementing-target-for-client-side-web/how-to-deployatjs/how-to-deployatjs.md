---
keywords: implement;at.js;javascript library
description: Informazioni su come distribuire la libreria JavaScript di Adobe Target, at.js, utilizzando Adobe Launch, senza utilizzare un sistema per la gestione dei o Adobe Dynamic Tag Management (DTM).
title: Come distribuire at.js
feature: client-side
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 57%

---


# Come distribuire at.js{#how-to-deploy-at-js}

Informazioni su come distribuire la libreria JavaScript di Adobe Target, at.js, utilizzando Adobe Launch, senza utilizzare un sistema per la gestione dei o Adobe Dynamic Tag Management (DTM).

Puoi implementare at.js utilizzando i seguenti metodi:

* **[Implementare Target con Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md)**: Launch è la piattaforma di gestione dei tag di nuova generazione di Adobe ed è il metodo preferito per implementare Adobe Target. Launch offre ai clienti un modo semplice di implementare e gestire tutti i tag di analisi, marketing e annunci pubblicitari necessari per fornire ai clienti esperienze personalizzate.
* **[Implementare Target senza un sistema per la gestione tag](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md)**: puoi implementare Target senza un sistema per la gestione dei tag (Adobe Launch o Dynamic Tag Management).
* **[Implementa Target tramite Gestione](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-using-dynamic-tag-management.md)** tag dinamica: Puoi implementare Target utilizzando  Gestione dinamica dei tag (DTM, Dynamic Tag Management)  Adobe  gestore di tag legacy. Adobe Launch è il metodo preferito e aggiornato per l’implementazione di Target e della libreria at.js. Per le nuove implementazioni di Target, utilizza Launch.
* **Implementate Target utilizzando un gestore** di tag di terze parti:  [ Adobe ](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md) Launchis è il metodo preferito per implementare Target; tuttavia, potete anche implementare Target utilizzando un gestore di tag di terze parti, come Tealium, Ensight, Google Tag, ecc. Per un elenco dei vantaggi dell&#39;utilizzo di Launch, vedere [Vantaggi dell&#39;implementazione di at.js tramite l&#39;estensione di Target Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#section_48B3F938B6F8491DAF798E0DB54EF304).

   Tuttavia, se sai come implementare Target senza un gestore di tag, puoi facilmente implementarlo con un gestore di tag di terze parti invece di codificare il file at.js nel codice del sito.

   Di seguito sono riportati due argomenti rilevanti per l&#39;implementazione di Target con un gestore di tag di terze parti:

   * [Prima dell’implementazione](/help/c-implementing-target/c-considerations-before-you-implement-target/considerations-before-you-implement-target.md)
   * [Implementare Target senza un sistema per la gestione dei tag](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md)

   Per ulteriori informazioni, consulta la documentazione relativa al gestore di tag di terze parti.

Per implementare Target quando si utilizzano le app a pagina singola, vedi [Implementazione delle applicazioni a pagina singola](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md).