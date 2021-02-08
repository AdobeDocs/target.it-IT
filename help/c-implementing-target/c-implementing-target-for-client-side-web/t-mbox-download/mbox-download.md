---
keywords: implementazione;mbox;download mbox.js;download api;mbox.js api
description: Scoprite l'implementazione legacy di mbox.js  Adobe Target. Esegui la migrazione all’SDK Web Adobe Experience Platform (AEP Web SDK) o all’ultima versione di at.js.
title: Come posso implementare Target con mbox.js?
feature: at.js
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 47%

---


# Implementazione di mbox.js

Per utilizzare [!DNL Adobe Target Standard] o [!DNL Target Premium], aggiungi una riga di codice per chiamare mbox.js.

Potete utilizzare uno dei due riferimenti libreria: [!DNL Adobe Experience Platform Web SDK] o [!DNL at.js]. [I vantaggi di at.](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#benefits) jsspiega le differenze tra le librerie mbox.js e at.js.

>[!IMPORTANT]
>
>**fine ciclo di vita** di mbox.js: Il 31 marzo 2021 non  [!DNL Adobe Target] supporterà più la libreria mbox.js. Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto positivo sulle pagine che hanno attività [!DNL Target] in esecuzione distribuendo contenuti predefiniti.
>
>È consigliabile che tutti i clienti effettuino la migrazione alla versione più recente della nuova [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js prima di tale data, per evitare potenziali problemi con i siti. Per ulteriori informazioni, vedere [Panoramica: implementate Target per Web lato client](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

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