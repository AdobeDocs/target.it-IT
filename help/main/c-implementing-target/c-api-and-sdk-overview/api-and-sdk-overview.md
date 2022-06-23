---
keywords: lato server;api;sdk;node.js;nodejs;node js;api consigli;api:apis
description: Scopri l’Adobe [!DNL Target] API di distribuzione lato server, SDK e [!DNL Target] API di Recommendations.
title: Dove posso saperne di più [!DNL Target] API e SDK di distribuzione lato server?
feature: Implement Server-side
role: Developer
exl-id: cdee007f-f54d-4cf3-9575-6319da3434a5
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 21%

---

# Lato server: implementare Target

Informazioni su [!DNL Adobe Target] API di distribuzione lato server, SDK e [!DNL Target Recommendations] API.

Il processo seguente si verifica in un’implementazione lato server di [!DNL Target]:

1. Un dispositivo client richiede un’esperienza attraverso il server.
1. Il server invia la richiesta a [!DNL Target].
1. [!DNL Target] restituisce la risposta al server.
1. Il server decide quale esperienza distribuire al dispositivo client per il rendering.

L’esperienza non deve essere visualizzata in un browser. L’esperienza può essere visualizzata in un’e-mail o un chiosco, tramite un assistente vocale o tramite un’altra esperienza non visiva o un dispositivo non basato su browser. Poiché il server risiede tra il client e [!DNL Target], questo tipo di implementazione è ideale anche se hai bisogno di maggiore controllo e sicurezza oppure in presenza di processi di backend complessi che devono essere eseguiti sul server.

>[!NOTE]
>
>È possibile inizializzare un visitatore per la prima volta solo sul lato client. Un nuovo visitatore *impossibile* inizializzato sul lato server.

Le sezioni seguenti forniscono ulteriori informazioni sulle varie API e sull’SDK di NodeJS:

## API di distribuzione lato server

Collegamento: [API di distribuzione lato server](https://developers.adobetarget.com/api/delivery-api/)

`/rest/v1/delivery`

Utilizzo della [!DNL Target] API di consegna, puoi:

* Offri esperienze su diversi canali web, compresi SPA e dispositivi mobili, nonché dispositivi IoT non basati su browser, come televisori collegati, chioschi o schermi digitali in-store.
* Distribuisci esperienze da qualsiasi piattaforma o applicazione lato server in grado di effettuare chiamate HTTP/s.
* Fornisci esperienze coerenti e personalizzate a un visitatore indipendentemente dal canale o dai dispositivi utilizzati dal visitatore per interagire con la tua attività.
* Memorizza in cache le esperienze di un visitatore all’interno di una sessione sul server, in modo da evitare chiamate API multiple, che consentono di ottenere prestazioni migliori.
* Integrazione perfetta con [!DNL Adobe Experience Cloud] prodotti, quali [!DNL Adobe Analytics], [!DNL Adobe Audience Manager] (AAM) e [!DNL Experience Cloud ID Service] dal lato server.

## SDK lato server

Collegamento: [SDK per Adobe Target](https://developer.adobe.com/target/)

La [!DNL Adobe Target] il portale della documentazione SDK lato server consente di implementare [!DNL Target] sui server nella lingua scelta.

## API per la funzione Consigli di Target

Collegamento: [API Recommendations di Target](https://developer.adobe.com/target/).

Le API di Recommendations consentono di interagire in modo programmatico con [!DNL Target] server delle raccomandazioni. Queste API possono essere integrate con una serie di stack di applicazioni per eseguire funzioni normalmente eseguite tramite il [!DNL Target] interfaccia utente.
