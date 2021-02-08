---
keywords: lato server;lato server;api;sdk;node.js;nodejs;nodo js;Recommendations api;api:apis
description: Scopri le  API di distribuzione lato server Adobe Target, gli SDK e le API Recommendations di Target.
title: Dove è possibile reperire informazioni sulle API e gli SDK di Target Server-Side Delivery?
feature: Implement Server-side
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 20%

---


# Lato server: implementare Target

Informazioni su [!DNL Adobe Target] API di distribuzione lato server, SDK e [!DNL Target Recommendations] API.

Il processo seguente si verifica in un’implementazione lato server di [!DNL Target]:

1. Un dispositivo client richiede un’esperienza attraverso il server.
1. Il server invia la richiesta a [!DNL Target].
1. [!DNL Target] restituisce la risposta al server.
1. Il server determina l’esperienza da distribuire al dispositivo client per il rendering.

L&#39;esperienza non deve essere visualizzata in un browser. L&#39;esperienza può essere visualizzata in un&#39;e-mail o in un chiosco, tramite un assistente vocale o tramite un&#39;altra esperienza non visiva o un dispositivo non basato su browser. Poiché il server risiede tra il client e [!DNL Target], questo tipo di implementazione è ideale anche se hai bisogno di maggiore controllo e sicurezza oppure in presenza di processi di backend complessi che devono essere eseguiti sul server.

>[!NOTE]
>
>Un visitatore della prima volta può essere inizializzato solo sul lato client. Un visitatore di prima visita *non può* essere inizializzato sul lato server.

Le sezioni seguenti forniscono ulteriori informazioni sulle varie API e l’SDK NodeJS:

## API di distribuzione lato server

Collegamento: [Server Side Delivery APIs](https://developers.adobetarget.com/api/delivery-api/)

`/rest/v1/delivery`

Tramite l&#39;API di consegna [!DNL Target] potete:

* Distribuite esperienze in tutto il Web, inclusi canali SPA e mobili, nonché dispositivi IoT non basati su browser, come televisori connessi, chioschi o schermi digitali all&#39;interno del negozio.
* Distribuite esperienze da qualsiasi piattaforma o applicazione lato server in grado di effettuare chiamate HTTP/s.
* Distribuisci esperienze coerenti e personalizzate a un visitatore, indipendentemente dal canale o dai dispositivi utilizzati dal visitatore per interagire con il tuo business.
* Memorizza nella cache le esperienze di un visitatore all’interno di una sessione sul server, in modo da evitare chiamate API multiple, che consentono di ottenere prestazioni migliori.
* Integrazione perfetta con i prodotti [!DNL Adobe Experience Cloud], come [!DNL Adobe Analytics], [!DNL Adobe Audience Manager] (AAM) e [!DNL Experience Cloud ID Service] dal lato server.

## SDK lato server

Collegamento: [ SDK Adobe Target](https://adobetarget-sdks.gitbook.io/docs/)

Il portale della documentazione dell&#39;SDK lato server [!DNL Adobe Target] consente di implementare [!DNL Target] sui server nella lingua desiderata.

## API per la funzione Consigli di Target

Collegamento: [Target Recommendations APIs](https://developers.adobetarget.com/api/recommendations) e [ Adobe Recommendations API Overview](https://experienceleague.adobe.com/docs/target-learn/recommendations-api-tutorial/recs-api-overview.html).

Le API Recommendations consentono di interagire in modo programmatico con i server [!DNL Target] delle raccomandazioni. Queste API possono essere integrate con una serie di stack di applicazioni per eseguire funzioni che normalmente si eseguono tramite l&#39;interfaccia utente [!DNL Target].
