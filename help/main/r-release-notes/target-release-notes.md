---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di Adobe Target.
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: bc4b04ae0be1fade2456eb42ade7ee87c0f14b16
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 55%

---

# Note sulla versione di Target (prerelease)

Questo articolo contiene informazioni di pre-release. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 20 luglio 2022**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle versioni. I codici tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target] versione di platform (20 luglio 2022)

Questa versione include i miglioramenti e le correzioni seguenti:

| Funzione | Descrizione |
| --- | --- |
| Miglioramento della precisione di valutazione del pubblico e riduzione della latenza degli utenti finali tramite il supporto IPv6 (TNT-43364, TNT-44692) | Le geolocalizzazioni dei visitatori ora sono determinate dagli indirizzi IPv6, se disponibili, anziché solo dagli indirizzi IPv4. Le API di consegna supportano anche i parametri di input IPv6. I filtri e l’elenco Consentiti supportano sia gli indirizzi IPv4 che IPv6. Il supporto di IPv6 in questa versione significa che i visitatori verranno inclusi in modo più preciso nei tipi di pubblico (più accuratamente qualificati per le attività o da includere nei criteri di filtro). Inoltre, migliora la latenza dei dati, in quanto i client IPv6 vengono instradati direttamente, evitando il sovraccarico del gateway IPv6-IPv4. |
| È stato risolto un problema di gestione del payload lato client di A4T (TNT-44926) | Con l’integrazione lato server di A4T, se Adobe Target identifica una richiesta come proveniente da un bot, non inoltra il payload ad Analytics e non esiste un evento mod_stats in registrato nel [!DNL Target] registri. Con questa versione, la registrazione lato client di A4T è stata migliorata in modo che il comportamento relativo al payload A4T sia lo stesso di quello relativo al lato server di A4T: I visitatori identificati come bot sono esclusi [!DNL Target] conteggio/reporting. (Nota che il problema in questione era limitato alle implementazioni che utilizzavano la gestione del carico utile sul lato client; lato server non interessato. Con questa versione, il comportamento è ora coerente sia per la gestione del payload lato server che per quello lato client.) |


## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
