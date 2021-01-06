---
keywords: implementation;mbox;download mbox.js;download api;mbox.js api
description: Per utilizzare  Adobe Target Standard o Target Premium, aggiungete una riga di codice per chiamare mbox.js.
title: Implementazione di mbox.js
feature: null
translation-type: tm+mt
source-git-commit: 863c5137383d35b2eaa33082c2136b81793281ca
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 30%

---


# Implementazione di mbox.js

Per utilizzare [!DNL Adobe Target Standard] o [!DNL Target Premium], aggiungi una riga di codice per chiamare mbox.js.

Potete utilizzare uno dei due riferimenti libreria: [!DNL Adobe Experience Platform Web SDK] o [!DNL at.js]. [I vantaggi di at.](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#benefits) jsspiega le differenze tra le librerie mbox.js e at.js.

>[!IMPORTANT]
>
>**fine ciclo di vita** di mbox.js: Il 31 marzo 2021 non  [!DNL Adobe Target] supporterà più la libreria mbox.js. Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto positivo sulle pagine che hanno attività [!DNL Target] in esecuzione distribuendo contenuti predefiniti. È consigliabile che tutti i clienti effettuino la migrazione alla versione più recente della nuova [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js prima di tale data, per evitare potenziali problemi con i siti.
>
>* **Adobe Experience Platform Web SDK**: L’ [!UICONTROL Adobe Experience Platform Web ] SDK consente di interagire con i vari servizi presenti nel  [!DNL Experience Cloud] (incluso  [!DNL Target]) tramite Adobe Experience Edge Network. Se scegli di eseguire la migrazione a [!DNL Adobe Experience Platform Web SDK], consulta [What is Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html), nella *Web SDK Guide*. Per informazioni specifiche su [Target overview](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/adobe-target/target-overview.html), vedere [!DNL Target].
   >
   >
* **at.js**: La libreria JavaScript at.js offre molti vantaggi rispetto a mbox.js. Tra gli altri vantaggi, at.js migliora i tempi di caricamento delle pagine per le implementazioni Web, migliora la sicurezza e offre migliori opzioni di implementazione per le applicazioni a pagina singola. Se scegli di effettuare la migrazione a at.js, consulta [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) and [ Adobe Target Experience Builder: Chat sviluppatore, migrate  Adobe Target mbox.js in at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
>
>
Sebbene mbox.js sia attualmente supportato (fino al 31 marzo 2021), a partire da luglio 2017 non è disponibile alcun aggiornamento della funzione per questa libreria. Spostando tutti i clienti su [!UICONTROL Adobe Experience Platform Web SDK] o at.js, i nostri tecnici e personale di supporto saranno in grado di fornire nuove funzionalità e offrire il supporto che ci si aspetta da  Adobe.

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