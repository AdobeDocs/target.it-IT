---
keywords: server side;server-side;api;sdk;node.js;nodejs;node js;recommendations api;api:apis
description: Informazioni  API di distribuzione lato server Adobe Target, SDK e API Recommendations Target.
title: Informazioni  API di consegna lato server Adobe Target, SDK Node.js e API Recommendations Target.
feature: server-side
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 20%

---


# Lato server: implementare Target{#server-side-implement-target}

Informazioni su API di consegna lato [!DNL Adobe Target] server, SDK e [!DNL Target Recommendations] API.

Il processo seguente si verifica in un’implementazione lato server di [!DNL Target]:

1. Un dispositivo client richiede un’esperienza attraverso il server.
1. Il server invia la richiesta a [!DNL Target].
1. [!DNL Target] restituisce la risposta al server.
1. Il server determina l’esperienza da distribuire al dispositivo client per il rendering.

L&#39;esperienza non deve essere visualizzata in un browser. L&#39;esperienza può essere visualizzata in un&#39;e-mail o in un chiosco, tramite un assistente vocale o tramite un&#39;altra esperienza non visiva o un dispositivo non basato su browser. Poiché il server risiede tra il client e [!DNL Target], questo tipo di implementazione è ideale anche se hai bisogno di maggiore controllo e sicurezza oppure in presenza di processi di backend complessi che devono essere eseguiti sul server.

>[!NOTE]
>
>Un visitatore della prima volta può essere inizializzato solo sul lato client. Un visitatore della prima volta *non può* essere inizializzato sul lato server.

Le sezioni seguenti forniscono ulteriori informazioni sulle varie API e l’SDK NodeJS:

## API di distribuzione lato server

Link: [Server Side Delivery APIs](https://developers.adobetarget.com/api/delivery-api/)

`/rest/v1/delivery`

Tramite l&#39;API [!DNL Target] di consegna, potete:

* Distribuite esperienze in tutto il Web, inclusi canali SPA e mobili, nonché dispositivi IoT non basati su browser, come televisori connessi, chioschi o schermi digitali all&#39;interno del negozio.
* Distribuite esperienze da qualsiasi piattaforma o applicazione lato server in grado di effettuare chiamate HTTP/s.
* Distribuisci esperienze coerenti e personalizzate a un visitatore, indipendentemente dal canale o dai dispositivi utilizzati dal visitatore per interagire con il tuo business.
* Memorizza nella cache le esperienze di un visitatore all’interno di una sessione sul server, in modo da evitare chiamate API multiple, che consentono di ottenere prestazioni migliori.
* Integrazione perfetta con [!DNL Adobe Experience Cloud] prodotti quali [!DNL Adobe Analytics], [!DNL Adobe Audience Manager] (AAM) e il lato [!DNL Experience Cloud ID Service] del server.

## SDK lato server

Collegamento: [Adobe Target SDK](https://adobetarget-sdks.gitbook.io/docs/)

Il portale della documentazione dell&#39;SDK lato [!DNL Adobe Target] server consente di implementare [!DNL Target] sui server nella lingua desiderata.

## API per la funzione Consigli di Target

Collegamento: [API](https://developers.adobetarget.com/api/recommendations) Recommendations Target e [Panoramica](https://experienceleague.adobe.com/docs/target-learn/recommendations-api-tutorial/recs-api-overview.html)API Adobe Recommendations.

The Recommendations APIs let you programmatically interact with [!DNL Target] recommendations servers. These APIs can be integrated with a range of application stacks to perform functions that you would typically do via the [!DNL Target] user interface.
