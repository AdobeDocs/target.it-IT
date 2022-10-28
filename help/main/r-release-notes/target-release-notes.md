---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di Adobe Target.
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 1b737f963fe63770cb04d05f3414ed946548d882
workflow-type: ht
source-wordcount: '455'
ht-degree: 100%

---

# Note sulla versione di Target (prerelease)

Questo articolo contiene informazioni di pre-release. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 19 ottobre 2022**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle versioni. I codici tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target] Standard/Premium 22.10.3 (rilascio scaglionato dal 25 al 27 ottobre 2022)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **25 ottobre**: area geografica Europa, Medio Oriente e Africa (EMEA)
* **26 ottobre**: area geografica Asia-Pacifico (APAC)
* **27 ottobre**: area geografica delle Americhe

Questa versione include le nuove funzioni, i miglioramenti e le correzioni seguenti:

| Funzione | Dettagli |
| --- | --- |
| [!DNL Recommendations] | Aggiunti nomi descrittivi nel reporting di [!UICONTROL Analytics for Target] (A4T). Precedentemente, [!DNL Target] elencava solo ID esperienza. Questo miglioramento allinea il reporting tra [!DNL Adobe Analytics] e [!DNL Target] e aiuta i clienti a semplificare la creazione di rapporti in A4T. (TGT-41853) |
| Metriche A4T ottimizzate per [!UICONTROL Allocazione automatica] e [!UICONTROL targeting automatico]<br> (disponibile per il testing per alcuni clienti selezionati. Sarà disponibile per tutti i clienti in una versione futura). | In particolare, tieni conto dei seguenti cambiamenti:<ul><li>È stato aggiunto il supporto per metriche binarie e di ottimizzazione nel reporting di [!UICONTROL Analytics for Target] (A4T) per le attività di [!UICONTROL Allocazione automatica] e [!UICONTROL targeting automatico]</li><li>Il comportamento delle attività esistenti verrà mantenuto fino al febbraio 2023. Dopo tale data, le attività verranno interrotte e sarà necessario effettuarne la migrazione ai nuovi comportamenti.</li><li>A partire dal 20 febbraio 2023, il supporto per le metriche `averagetimespentonsite`, `bouncerate` e `entries` nelle attività [!DNL Target] sarà ritirato.</li></ul> |

* Sono state aggiunte descrizioni comando nell’interfaccia utente di [!DNL Target] per consentire ai clienti di navigare nel generatore di pubblico in modo più efficiente e per scoprire come utilizzare funzioni che potrebbero non essere familiari. (TGT-44139)
* È stata aggiunta una funzionalità per impedire ai clienti di modificare un’attività disabilitata da [!DNL Target] perché utilizza metriche non supportate. Un messaggio nell’interfaccia utente indica ai clienti di duplicare l’attività e quindi aggiornare la metrica di conversione.

   Con questa versione le metriche `averagetimespentonsite`, `bouncerate` e `entries` nelle attività di [!DNL Target] diventeranno obsolete per le nuove attività. Le attività esistenti possono continuare a utilizzare tali metriche fino a febbraio 2023. (TGT-43860, TGT-43861, TGT-43650)

* È stata aggiunta una descrizione comando nell’interfaccia utente di [!DNL Target] per consentire ai clienti di selezionare un criterio di ottimizzazione durante la creazione o la modifica di un’attività di [!UICONTROL targeting automatico] che utilizza A4T. (TGT-43713)

## Note aggiuntive sulla versione e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js di [!DNL Adobe Target]. |


## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
