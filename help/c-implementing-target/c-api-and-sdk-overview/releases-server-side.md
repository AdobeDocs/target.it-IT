---
keywords: at.js;api;release;updates;apis;sdks;server side;serverside;server-side;api;delivery api
description: Note sulla versione relative  API lato server Adobe Target.
title: Note sulla versione relative  API lato server Adobe Target.
feature: release notes
topic: Standard
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 2%

---


# Note sulla versione - API lato server di Target

Note sulla versione relative alle API lato server [Adobe Target](https://developers.adobetarget.com/api/delivery-api/).

## V1/consegna (9 ottobre 2019)

È stato rilasciato un endpoint API di consegna completamente nuovo.

* New [documentation](https://developers.adobetarget.com/api/delivery-api/) is available.
* Un endpoint per recuperare le esperienze per una o più mbox.
* Recuperate le attività create VEC tramite l&#39;API.

   La risposta che contiene attività create con VEC dispone di selettori che possono essere utilizzati per prenascondere solo parti della pagina che devono essere personalizzate. Questo consente di ottimizzare la metrica [](https://developers.google.com/web/fundamentals/performance/user-centric-performance-metrics.html)First Contentful Paint della pagina, che è un indicatore KPI importante per la tua attività per ottenere un punteggio elevato nel sistema [Google PageRank](https://en.wikipedia.org/wiki/PageRank) .

* Supporto per un oggetto completamente nuovo, denominato Views (Visualizzazioni), utilizzato per le applicazioni [SPA (](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md) Single Page Applications) e le applicazioni [](/help/c-target-mobile-app/target-mobile-app.md)mobili.
* Supporto per la preacquisizione di viste e mbox da ottimizzare per le prestazioni tramite caching.
* Supporto per l&#39;invio di notifiche per viste e mbox precaricate.

>[!IMPORTANT]
>
>È ancora possibile accedere alla documentazione [precedente relativa alle API](https://developers.adobetarget.com/api/legacy-api/index.html) /v1/mbox e /v2/batchmbox. Tuttavia, le nuove funzionalità saranno sviluppate nella nuova API di consegna e non saranno inviate nuovamente alle API legacy.
