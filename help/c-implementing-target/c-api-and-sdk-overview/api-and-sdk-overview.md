---
keywords: server side;server-side;api;sdk;node.js;nodejs;node js;recommendations api;api:apis
description: Informazioni  API di consegna lato server Adobe Target, SDK Node.js e API Recommendations Target.
title: Informazioni  API di consegna lato server Adobe Target, SDK Node.js e API Recommendations Target.
feature: server-side
topic: Recommendations
uuid: 21d321c7-3da4-44a2-a04f-1807cc2a893b
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 11%

---


# Lato server: implementare Target{#server-side-implement-target}

Informazioni sulle API di consegna lato [!DNL Adobe Target] server, l’SDK Node.js e [!DNL Target Recommendations] le API.

Il processo seguente si verifica in un’implementazione lato server di [!DNL Target]:

1. Un dispositivo client richiede un’esperienza attraverso il server.
1. Il server invia la richiesta a [!DNL Target].
1. [!DNL Target] restituisce la risposta al server.
1. Il server determina l’esperienza da distribuire al dispositivo client per il rendering.

L&#39;esperienza non deve essere visualizzata in un browser. L&#39;esperienza può essere visualizzata in un&#39;e-mail o in un chiosco, tramite un assistente vocale o tramite un&#39;altra esperienza non visiva o un dispositivo non basato su browser. Poiché il server risiede tra il client e [!DNL Target], questo tipo di implementazione è ideale anche se hai bisogno di maggiore controllo e sicurezza oppure in presenza di processi di backend complessi che devono essere eseguiti sul server.

Le sezioni seguenti forniscono ulteriori informazioni sulle varie API e l’SDK NodeJS:

## API di distribuzione lato server

Link: [Server Side Delivery APIs](https://developers.adobetarget.com/api/delivery-api/)

`/rest/v1/delivery`

Tramite l&#39;API [!DNL Target] di consegna, potete:

* Distribuite esperienze in tutto il Web, inclusi gli SPA e i canali mobili, nonché dispositivi IoT non basati su browser, come televisori connessi, chioschi o schermi digitali all&#39;interno del negozio.
* Distribuite esperienze da qualsiasi piattaforma o applicazione lato server in grado di effettuare chiamate HTTP/s.
* Distribuisci esperienze coerenti e personalizzate a un visitatore, indipendentemente dal canale o dai dispositivi utilizzati dal visitatore per interagire con il tuo business.
* Memorizza nella cache le esperienze di un visitatore all’interno di una sessione sul server, in modo da evitare chiamate API multiple, che consentono di ottenere prestazioni migliori.
* Integrazione perfetta con [!DNL Adobe Experience Cloud] prodotti quali [!DNL Adobe Analytics], [!DNL Adobe Audience Manager] (AAM) e il lato [!DNL Experience Cloud ID Service] del server.

## Node.js SDK

Collegamento: [Node.js SDK](https://github.com/adobe/target-nodejs-sdk)

Node.js SDK è un sofisticato kit di sviluppo software che elimina la complessità della gestione di cookie, sessioni e integrazioni con [!DNL Experience Cloud] prodotti come [!DNL Analytics], [!DNL Experience Cloud Visitor ID Service]e [!DNL Audience Manager]. Dietro le quinte, l’SDK Node.js utilizza l’ `/rest/v1/delivery` API. Di seguito sono riportate alcune funzionalità importanti supportate nell’SDK Node.js:

* **Supporto per preacquisizione e notifiche che consentono di ottimizzare le prestazioni mediante la memorizzazione nella cache:** Puoi usare l’SDK Node.js per recuperare esperienze e memorizzarle nella cache locale sul server Node.js allo scopo di ridurre al minimo le chiamate al server [!DNL Target] e ottimizzare le prestazioni dell’applicazione.
* **Possibilità di recuperare le attività create VEC:** Recuperate le attività create VEC sul lato server. La risposta che contiene attività create con VEC dispone di selettori che possono essere utilizzati per prenascondere solo parti della pagina che devono essere personalizzate. Questo consente di ottimizzare la metrica [](https://developers.google.com/web/fundamentals/performance/user-centric-performance-metrics.html)First Contentful Paint della pagina, che è un indicatore KPI importante per la tua attività per ottenere un punteggio elevato nel sistema [Google PageRank](https://en.wikipedia.org/wiki/PageRank) .

## Target Java SDK

Collegamento: [Target Java SDK](https://github.com/adobe/target-java-sdk)

Java SDK è un sofisticato kit di sviluppo software che elimina la complessità della gestione di cookie, sessioni e integrazioni con [!DNL Adobe Experience Cloud] soluzioni, come [!DNL Adobe Analytics], il [!DNL Experience Cloud Visitor ID Service]e [!DNL Adobe Audience Manager]. Dietro le quinte, l&#39;SDK Java utilizza l&#39; `/rest/v1/delivery` API. Di seguito sono riportate alcune funzionalità importanti supportate nell’SDK Java:

* **Supporto per preacquisizione e notifiche che consentono di ottimizzare le prestazioni mediante la memorizzazione nella cache**: Potete utilizzare JavaSDK per recuperare esperienze e memorizzarle nella cache locale sul server Java allo scopo di ridurre al minimo le chiamate server [!DNL Target] e ottimizzare le prestazioni dell’applicazione.
* **Possibilità di recuperare le attività** create VEC: Recuperate le attività create VEC sul lato server. La risposta che contiene attività create con VEC dispone di selettori che possono essere utilizzati per prenascondere solo parti della pagina che devono essere personalizzate. Questo consente di ottimizzare la metrica [First Contentful Paint](https://developers.google.com/web/fundamentals/performance/user-centric-performance-metrics.html) della pagina, che è un indicatore KPI importante per la tua attività per ottenere un punteggio elevato nel sistema [Google PageRank](https://en.wikipedia.org/wiki/PageRank) .

## API per la funzione Consigli di Target

Collegamento: [API](https://developers.adobetarget.com/api/recommendations) Recommendations Target e [Panoramica](https://docs.adobe.com/content/help/en/target-learn/recommendations-api-tutorial/recs-api-overview.html)API Adobe Recommendations.

The Recommendations APIs let you programmatically interact with [!DNL Target] recommendations servers. These APIs can be integrated with a range of application stacks to perform functions that you would typically do via the [!DNL Target] user interface.
