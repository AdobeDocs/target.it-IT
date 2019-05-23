---
description: Per utilizzare Target Standard o Target Premium, aggiungi una riga di codice per chiamare mbox.js.
keywords: Implementazione;mbox;scaricare mbox.js;scaricare api;api mbox.js
seo-description: Per utilizzare Target Standard o Target Premium, aggiungi una riga di codice per chiamare mbox.js.
seo-title: Implementazione di mbox.js
solution: Target
subtopic: Introduzione
title: Implementazione di mbox.js
topic: Standard
uuid: aa53dfd4-db42-4a33-b561-7e84ca7e4497
translation-type: tm+mt
source-git-commit: b45a1a141e9e1d229ed3f92b8124d3edf3bc3042

---


# Implementazione di mbox.js{#mbox-js-implementation}

Per utilizzare Target Standard o Target Premium, aggiungi una riga di codice per chiamare mbox.js.

Puoi utilizzare uno dei due riferimenti di libreria: [!DNL mbox.js] o [!DNL at.js]. [Informazioni sulle librerie JavaScript](../../../c-implementing-target/c-considerations-before-you-implement-target/target-implement.md#concept_60B748DE4293488F917E8F1FA4C7E9EB) di Target per comprendere le differenze tra le due librerie.

>[!NOTE]
>
>La libreria mbox.js è ancora supportata, ma non ci saranno aggiornamenti di funzionalità. Tutti i clienti devono migrare a at.js. Per ulteriori informazioni, consulta [Migrazione a at.js da mbox.js](../../../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA).

Il singolo riferimento a [!DNL mbox.js] in ogni pagina fornisce le librerie necessarie per tutte le attività. [!DNL mbox.js] chiama [!DNL Target] da ogni pagina che fa riferimento al file [!DNL mbox.js]. Questo consente a [!DNL Target] di effettuare le seguenti operazioni:

* Fornire attività Target
* Tracciamento dei clic
* Tracciare le metriche di maggior successo

>[!TIP]
>
>Per semplificare l’implementazione, puoi fare riferimento a [!DNL mbox.js] nell’intestazione globale.

Non è necessario mantenere diverse versioni del file specifiche per le singole attività.

1. Inserisci un riferimento a [!DNL mbox.js] nella sezione `<head>` di ogni pagina del tuo sito.

   `<script src="/ *`directory`*/ *`scripts`*/mbox.js"></script>`

   Dove ` *`directory`*/ *`scripts`*` è la directory in cui è stato salvato il file [!DNL mbox.js] dopo averlo scaricato.
Se disponi già di elementi mbox sulla tua pagina derivanti da un&#39;implementazione precedente, questi possono ancora essere utilizzati nella nuova interfaccia. Il file [!DNL mbox.js] aggiornato rimane necessario, ma queste mbox possono essere selezionate per le attività e modificate utilizzando il [!UICONTROL Compositore esperienza visivo].