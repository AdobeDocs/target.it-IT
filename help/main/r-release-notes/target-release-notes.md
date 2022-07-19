---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di Adobe Target.
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: a5d2c07105b1d0fac6115fe507537be6a36799e9
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 33%

---

# Note sulla versione di Target (prerelease)

Questo articolo contiene informazioni di pre-release. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 19 luglio 2022**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle versioni. I codici tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target Standard/Premium] 22.7.1 (20 luglio 2022)

Questa versione include i miglioramenti e le correzioni seguenti:

| Funzione | Descrizione |
| --- | --- |
| Miglioramento della precisione di valutazione del pubblico e della latenza dell&#39;utente finale tramite il supporto IPv6 | Le geolocalizzazioni dei visitatori ora sono determinate dagli indirizzi IPv6, se disponibili, anziché solo dagli indirizzi IPv4. Le API di distribuzione supportano anche i parametri di input IPv6. I filtri e l’inserimento nell’elenco Consentiti supportano sia gli indirizzi IPv4 che IPv6. Questo supporto IPv6 in questa versione significa che i visitatori verranno inclusi in modo più preciso nei tipi di pubblico (più accuratamente qualificati per le attività o da includere nei criteri di filtro). Inoltre, migliora la latenza dei dati, in quanto i client IPv6 si instradano direttamente, evitando il sovraccarico del gateway IPv6-to-IPv4. |
| Miglioramento della gestione del payload lato client di A4T | Con l’integrazione lato server di A4T, se Adobe Target identifica una richiesta come proveniente da un bot, non inoltra il payload ad Analytics e non esiste un evento mod_stats in registrato nel [!DNL Target] registri. Prima di questa versione, le integrazioni lato client di A4T inoltravano il payload a [!DNL Analytics], anche quando era stato identificato come traffico da bot. Questa incoerenza tra lato server e lato client creerebbe discrepanze, in quanto i rapporti A4T per quest’ultimo includevano il traffico da bot. Inoltre, il traffico da bot non è stato necessariamente identificato né segnalato, il che significa che non è stato possibile distinguere o rimuovere il traffico da bot dal resto del traffico. E anche se un cliente tenesse conto del traffico da solo, non corrisponderebbe necessariamente all&#39;insieme di traffico che [!DNL Target] identificato ed escluso come traffico da bot, che si traduce in discrepanze diverse o altre questioni. Con questa versione, la registrazione lato client di A4T è stata migliorata in modo che il comportamento relativo al payload A4T sia lo stesso di quello relativo al lato server di A4T: I visitatori identificati come bot sono esclusi [!DNL Target] conteggio/reporting, per implementazioni lato server e lato client. |


## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
