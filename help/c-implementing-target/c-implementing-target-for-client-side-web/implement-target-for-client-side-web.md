---
keywords: implementazione;implementazione;at.js;adobe experience platform web sdk;aep web sdk
description: Informazioni sull'implementazione di  Adobe Target per il Web lato client tramite at.js.
title: Implementazione  Adobe Target per il Web lato client
feature: at.js
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 18%

---


# Panoramica: Implementare Target per web lato client

In un’implementazione lato client di [!DNL Adobe Target], [!DNL Target] distribuisce le esperienze associate a un’attività direttamente al browser client. Il browser determina quale esperienza visualizzare e la visualizza. Con un’implementazione lato client, puoi utilizzare un editor WYSIWYG, il [Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) o un’interfaccia non visiva, il [Compositore esperienza basato su moduli](/help/c-experiences/form-experience-composer.md), per creare esperienze di attività e personalizzazione.

Per implementare [!DNL Adobe Target] lato client, è necessario utilizzare una delle seguenti librerie JavaScript:

* [Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md)
* [Targeting della libreria JavaScript at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md)

>[!IMPORTANT]
>
>**fine ciclo di vita** di mbox.js: Il 31 marzo 2021 non  [!DNL Adobe Target] supporterà più la libreria mbox.js. Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto positivo sulle pagine che hanno attività [!DNL Target] in esecuzione distribuendo contenuti predefiniti. È consigliabile che tutti i clienti effettuino la migrazione alla versione più recente della nuova [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js prima di tale data, per evitare potenziali problemi con i siti.
>
>* **Adobe Experience Platform Web SDK**: L’ [!UICONTROL Adobe Experience Platform Web ] SDK consente di interagire con i vari servizi presenti nel  [!DNL Experience Cloud] (incluso  [!DNL Target]) tramite Adobe Experience Edge Network. Se scegli di eseguire la migrazione a [!DNL Adobe Experience Platform Web SDK], consulta [Cos&#39;è Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) nella *Guida per l&#39;SDK Web*.
   >
   >
* **at.js**: La libreria JavaScript at.js offre molti vantaggi rispetto a mbox.js. Tra gli altri vantaggi, at.js migliora i tempi di caricamento delle pagine per le implementazioni Web, migliora la sicurezza e offre migliori opzioni di implementazione per le applicazioni a pagina singola. Se scegli di effettuare la migrazione a at.js, consulta [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) and [ Adobe Target Experience Builder: Chat sviluppatore, migrate  Adobe Target mbox.js in at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
>
>
Sebbene mbox.js sia attualmente supportato (fino al 31 marzo 2021), a partire da luglio 2017 non è disponibile alcun aggiornamento della funzione per questa libreria. Spostando tutti i clienti su [!UICONTROL Adobe Experience Platform Web SDK] o at.js, i nostri tecnici e personale di supporto saranno in grado di fornire nuove funzionalità e offrire il supporto che ci si aspetta da  Adobe.
