---
keywords: implementare;implementazione;at.js;adobe experience platform web sdk;aep web sdk
description: Scopri come implementare Adobe [!DNL Target] for client-side web using the Adobe Experience Platform Web SDK  (AEP Web SDK) or the [!DNL Target] Libreria JavaScript at.js.
title: Come si implementa [!DNL Target] per web lato client
feature: at.js
role: Developer
exl-id: 34c1e39b-acae-4547-b67f-584bcd59913f
source-git-commit: bef2b493e8964f468d4f766c932a96d32e994a03
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 47%

---

# Panoramica: implementare [!DNL Target] per web lato client

In un’implementazione lato client di [!DNL Adobe Target], [!DNL Target] distribuisce le esperienze associate a un’attività direttamente al browser client. Il browser determina quale esperienza visualizzare e la visualizza. Con un’implementazione lato client, puoi utilizzare un editor WYSIWYG, il [Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) o un’interfaccia non visiva, il [Compositore esperienza basato su moduli](/help/c-experiences/form-experience-composer.md), per creare esperienze di attività e personalizzazione.

Implementazione [!DNL Adobe Target] lato client, è necessario utilizzare una delle seguenti librerie JavaScript:

* [Tutorial per Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md)
* [Libreria JavaScript at.js di Target](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md)

>[!IMPORTANT]
>
>**Termine del ciclo di vita di**: a partire dal 31 marzo 2021, [!DNL Adobe Target] non supporta più la libreria mbox.js. Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto sulle pagine che hanno attività [!DNL Target] in esecuzione, che presenteranno il contenuto predefinito. Adobe consiglia a tutti i clienti di eseguire la migrazione alla versione più recente della nuova [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js prima di tale data, per evitare potenziali problemi con i siti.
>
>* **Adobe Experience Platform Web SDK**: La [!UICONTROL Adobe Experience Platform Web SDK] consente di interagire con i vari servizi nel [!DNL Experience Cloud] (tra cui [!DNL Target]) tramite Adobe Experience Edge Network. Se scegli di eseguire la migrazione al [!DNL Adobe Experience Platform Web SDK], vedi [Cos’è Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) in *Guida all’SDK per web*.
>
>* **at.js**: La libreria JavaScript at.js migliora i tempi di caricamento delle pagine per le implementazioni web, migliora la sicurezza e fornisce migliori opzioni di implementazione per le applicazioni a pagina singola. Se scegli di eseguire la migrazione a at.js, consulta [Funzionamento di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) e [Generatore di competenze Adobe Target: Sviluppatore chat, migrazione di Adobe Target mbox.js in at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).


