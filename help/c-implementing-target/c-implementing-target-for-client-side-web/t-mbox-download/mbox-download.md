---
keywords: implementazione;mbox;scaricare mbox.js;scaricare api;api mbox.js
description: Scopri l’implementazione legacy di mbox.js di Adobe Target. Esegui la migrazione a Adobe Experience Platform Web SDK (AEP Web SDK) o all’ultima versione di at.js.
title: Come posso implementare [!DNL Target] con mbox.js?
feature: at.js
role: Developer
exl-id: 105095d7-8e29-413b-a7f4-e46e2e30e91f
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 47%

---

# Implementazione di mbox.js

Per utilizzare [!DNL Adobe Target Standard] o [!DNL Target Premium], aggiungi una riga di codice per chiamare mbox.js.

Puoi utilizzare uno dei due riferimenti di libreria: i valori [!DNL Adobe Experience Platform Web SDK] o [!DNL at.js]. [I vantaggi di at.](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#benefits) js spiegano le differenze tra le librerie mbox.js e at.js.

>[!IMPORTANT]
>
>**Terminazione di mbox.js**: A partire dal 31 marzo 2021,  [!DNL Adobe Target] non supporta più la libreria mbox.js . Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto positivo sulle pagine che hanno [!DNL Target] attività in esecuzione servendo il contenuto predefinito.
>
>È consigliabile che tutti i clienti effettuino la migrazione alla versione più recente della nuova [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js prima di tale data, per evitare potenziali problemi con i siti. Per ulteriori informazioni, consulta [Panoramica: implementare Target per web lato client](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

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
