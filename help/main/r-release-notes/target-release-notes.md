---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di [!DNL Adobe Target].
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione [!DNL Target] ?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: dbf9a51044f317d02a705f2331d6dc58b6549606
workflow-type: tm+mt
source-wordcount: '784'
ht-degree: 100%

---

# Note sulla versione (prerelease) di [!DNL Target]

Questo articolo contiene informazioni prerelease per le prossime versioni di [!DNL Adobe Target], incluse SDK, API e librerie JavaScript.

**Ultimo aggiornamento: 3 ottobre 2023**

>[!NOTE]
>
>Date di rilascio, funzioni e altre informazioni sono soggette a modifica senza preavviso.
>
>Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle release. I codici tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target] Standard/Premium 23.9.4 (4-6 ottobre 2023)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **4 ottobre**: area geografica Asia-Pacifico (APAC)
* **5 ottobre**: area geografica Europa, Medio Oriente e Africa (EMEA)
* **6 ottobre**: area geografica delle Americhe

Questa versione include i miglioramenti e le correzioni seguenti:

| Funzione | Dettagli |
| --- | --- |
| Aggiornamento interfaccia utente [!UICONTROL Attività]<P>e<P>aggiornamento interfaccia utente [!UICONTROL Feed] | Come parte del continuo impegno del team di [!DNL Adobe Target] per migliorare l’esperienza utente di [!DNL Target], questa versione aggiorna le pagine [!UICONTROL Attività] e [!UICONTROL Feed] di [!DNL Recommendations] nell’interfaccia utente di [!DNL Target]. Questo aggiornamento unisce e standardizza i modelli di progettazione precedentemente incoerenti, aggiungendo allo stesso tempo nuovi miglioramenti.<P>Per ulteriori informazioni, consulta [Attività](/help/main/c-activities/activities.md) e [Feed](/help/main/c-recommendations/c-products/feeds.md). |
| Pattern di implementazione di [!DNL Recommendations] | Gli articoli *Pattern di implementazione di Recommendations tramite at.js* contribuiscono a comprendere e creare l’implementazione di [!DNL Adobe Target Recommendations] quando si utilizza la libreria JavaScript at.js.<P>Per ulteriori informazioni, consulta [Panoramica sul pattern di implementazione di Recommendations tramite at.js](https://experienceleague.adobe.com/docs/target-dev/developer/implementation-patterns/atjs/recs-implementation-pattern-atjs.html?lang=it){target=_blank} nella *Guida per gli sviluppatori di Adobe Target*. |

* Sono stati aggiunti miglioramenti al [!UICONTROL Compositore esperienza visivo] (VEC) per i framework dinamici. (TGT-44064)
* È stato risolto un problema che causava un aggiornamento non corretto alla data selezionata nella richiesta `getViewInAnalyticsId`. Questa correzione consente di ricalcolare il collegamento di [!DNL Analytics] nel reporting quando vengono modificate le impostazioni dei rapporti relativi alle metriche e agli intervalli di date. (TGT-46246)

## [!DNL Target] Standard/Premium 23.9.3 (18 settembre 2023)

Questa versione include i miglioramenti e le correzioni seguenti:

* È stato migliorato il [!UICONTROL Compositore esperienza visivo] (VEC) per supportare componenti Web Lightning (Light DOM). (TGT-45422)
* È stato risolto un problema che causava l’applicazione delle azioni VEC in un ordine errato. In alcuni casi, il VEC ha applicato alcune modifiche in modo asincrono e l’aggiunta di ulteriori modifiche a un elemento ha causato errori se tale elemento viene visualizzato dopo un’azione [!UICONTROL Inserisci]. Corregge anche l’URL del VEC, che ora si aggiorna quando si clicca sui collegamenti di ancoraggio. (TGT-45983)
* È stato risolto un problema relativo alla funzione [!UICONTROL Sovrapposizione] del VEC, che ora supporta gli elementi in shadow DOM. (TGT-45202 e TGT-45262)
* È stato risolto un problema che si verificava all’apertura della pagina di un’applicazione a pagina singola (SPA) nel VEC e di conseguenza il passaggio alla modalità [!UICONTROL Sfoglia] causava il malfunzionamento delle frecce Indietro e Avanti. (TGT-45956)
* È stato risolto un problema che impediva il caricamento di alcune pagine web nel VEC. (TGT-45983)

## [!DNL Target] Standard/Premium 23.9.2 (12-14 settembre 2023)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **12 settembre**: area geografica delle Americhe
* **13 settembre**: area geografica Asia-Pacifico (APAC)
* **14 settembre**: area geografica Europa, Medio Oriente e Africa (EMEA)

Questa versione include i miglioramenti e le correzioni seguenti:

* È stata modificata l’API di [!DNL Analytics] per la nuova versione 2.0 API di [!DNL Analytics]. (TGT-45345)
* Sono stati risolti i problemi che hanno interessato le attività [!UICONTROL Automated Personalization] (AP) per alcuni clienti, inclusa la sincronizzazione tempestiva dell’attività sul back-end di [!DNL Target] e la possibilità di fornire l’esperienza prevista nei collegamenti di anteprima. (TGT-46202)

## [!DNL Target] Standard/Premium 23.9.1 (6-11 settembre 2023)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **6 settembre**: area geografica delle Americhe
* **7 settembre**: area geografica Europa, Medio Oriente e Africa (EMEA)
* **11 settembre**: area geografica Asia-Pacifico (APAC)

Questa versione include i miglioramenti e le correzioni seguenti:

* È stato corretto un problema che causava incoerenza nei dati di reporting nell’interfaccia utente di [!DNL Target] e nell’interfaccia utente di [!DNL Adobe Analytics] per attività di [!UICONTROL allocazione automatica] che utilizzano [!UICONTROL Analytics for Target] (A4T) come origine di reporting. (TGT-46112)
* Il timeout per le chiamate PUT all’API di consegna di Target è stato aumentato a 15 secondi, per evitare errori di timeout. (TGT-46091)
* È stato corretto un problema che impediva l’aggiornamento costante dell’URL durante la navigazione nel sito web di un’applicazione a pagina singola (SPA). (TGT-45417)

## [!DNL Target] Standard/Premium 23.5.2 (data da definire)

Questa versione include i miglioramenti e le correzioni seguenti:

* Abilitazione della selezione dei criteri di ottimizzazione per le metriche di [!DNL Adobe Analytics].
* Abilitazione della sincronizzazione di tipi di pubblico esterni tramite processi sling.
* È stato risolto un problema per cui le suite di rapporti SC contenenti un carattere punto nel nome non erano supportate.
* È stata abilitata la funzionalità per consentire alla clientela di eliminare e modificare i tipi di pubblico incorporati.

## [!DNL Target] Standard/Premium 23.5.3 (data da definire)

Questo rilascio contiene i seguenti miglioramenti:

| Funzione | Dettagli |
|--- |--- |
| [!UICONTROL Modalità Controllo qualità] per attività di [!UICONTROL Automated Personalization] | [!DNL Adobe Target] La [!UICONTROL Modalità Controllo qualità] è ora disponibile per le attività di [!UICONTROL Automated Personalization], in sostituzione della funzionalità [!UICONTROL Collegamenti di anteprima].<P>Per ulteriori informazioni, consulta [Controllo qualità delle attività](/help/main/c-activities/c-activity-qa/activity-qa.md). |

## Note aggiuntive e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js di [!DNL Adobe Target]. |

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
