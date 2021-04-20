---
keywords: implementare;implementazione;at.js;adobe experience platform web sdk;aep web sdk
description: Scopri come implementare Adobe Target per il web lato client utilizzando Adobe Experience Platform Web SDK (AEP Web SDK) o la libreria JavaScript at.js di Target.
title: Come si implementa Target per il web lato client
feature: at.js
role: Developer
exl-id: 34c1e39b-acae-4547-b67f-584bcd59913f
translation-type: tm+mt
source-git-commit: 0a685427a047bfc0a2f5e81525b32df70af6d69f
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 18%

---

# Panoramica: Implementare Target per web lato client

In un’implementazione lato client di [!DNL Adobe Target], [!DNL Target] distribuisce le esperienze associate a un’attività direttamente al browser client. Il browser determina quale esperienza visualizzare e la visualizza. Con un’implementazione lato client, puoi utilizzare un editor WYSIWYG, il [Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) o un’interfaccia non visiva, il [Compositore esperienza basato su moduli](/help/c-experiences/form-experience-composer.md), per creare esperienze di attività e personalizzazione.

Per implementare [!DNL Adobe Target] lato client, devi utilizzare una delle seguenti librerie JavaScript:

* [Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md)
* [Libreria JavaScript at.js di Target](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md)

>[!IMPORTANT]
>
>**Terminazione di mbox.js**: A partire dal 31 marzo 2021,  [!DNL Adobe Target] non supporta più la libreria mbox.js . Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto positivo sulle pagine che hanno [!DNL Target] attività in esecuzione servendo il contenuto predefinito. È consigliabile che tutti i clienti effettuino la migrazione alla versione più recente della nuova [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js prima di tale data, per evitare potenziali problemi con i siti.
>
>* **SDK** web Adobe Experience Platform: L’ [!UICONTROL Adobe Experience Platform Web ] SDK consente di interagire con i vari servizi in  [!DNL Experience Cloud] (incluso  [!DNL Target]) tramite Adobe Experience Edge Network. Se scegli di eseguire la migrazione a [!DNL Adobe Experience Platform Web SDK], consulta [Cos’è Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) nella *Guida all’SDK per web*.
   >
   >
* **at.js**: La libreria JavaScript at.js offre molti vantaggi rispetto a mbox.js. Ad esempio, at.js migliora i tempi di caricamento delle pagine per le implementazioni web, migliora la sicurezza e fornisce migliori opzioni di implementazione per le applicazioni a pagina singola. Se scegli di eseguire la migrazione a at.js, consulta [Funzionamento di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) e [Generatore di competenze Adobe Target: Sviluppatore chat, esegui la migrazione di Adobe Target mbox.js in at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
>
>
Anche se mbox.js è attualmente supportato (fino al 31 marzo 2021), a partire da luglio 2017 non sono disponibili aggiornamenti di funzionalità per questa libreria. Spostando tutti i clienti su [!UICONTROL Adobe Experience Platform Web SDK] o at.js, i nostri tecnici e il nostro personale di supporto saranno in grado di fornirti nuove funzionalità e offrire il supporto che ti aspetti dall&#39;Adobe.
