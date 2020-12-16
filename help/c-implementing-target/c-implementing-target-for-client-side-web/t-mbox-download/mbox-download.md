---
keywords: Implementation;Mbox;download mbox.js;download api;mbox.js api
description: Per utilizzare Target Standard o Target Premium, aggiungi una riga di codice per chiamare mbox.js.
title: Implementazione di mbox.js
feature: null
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 55%

---


# Implementazione di mbox.js{#mbox-js-implementation}

Per utilizzare Target Standard o Target Premium, aggiungi una riga di codice per chiamare mbox.js.

Puoi utilizzare uno dei due riferimenti di libreria: [!DNL mbox.js] o [!DNL at.js]. La sezione [Vantaggi di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#benefits) spiega le differenze tra le due librerie.

>[!NOTE]
>
>**fine ciclo di vita** di mbox.js: Il 18 gennaio 2021  Adobe Target non supporterà più la libreria mbox.js. Dopo il 18 gennaio 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto positivo sulle pagine che hanno attività Target in esecuzione distribuendo contenuto predefinito. È consigliabile che tutti i clienti effettuino la migrazione alla versione più recente della libreria at.js prima di tale data, in modo da evitare potenziali problemi con i siti. Per ulteriori informazioni, vedere [Come funziona At.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md).
>
>Sebbene mbox.js sia attualmente supportato, a partire da luglio 2017 non sono stati forniti aggiornamenti di funzionalità per questa libreria. Il più recente at.js offre molti vantaggi rispetto a mbox.js. Tra gli altri vantaggi, at.js migliora i tempi di caricamento delle pagine per le implementazioni Web, migliora la sicurezza e offre migliori opzioni di implementazione per le applicazioni a pagina singola.
>
>Trasferendo tutti i clienti a at.js, i nostri tecnici e il nostro staff di supporto saranno in grado di fornirvi nuove funzionalità e di offrire il supporto che vi aspettate da  Adobe.

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