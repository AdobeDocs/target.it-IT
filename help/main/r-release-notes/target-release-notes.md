---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di Adobe Target.
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: d0b6f81507cc5d5bc17d029c3d8f5b36c2c71a29
workflow-type: tm+mt
source-wordcount: '657'
ht-degree: 56%

---

# Note sulla versione di Target (prerelease)

Questo articolo contiene informazioni di pre-release. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 18 luglio 2022**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle versioni. I codici tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target Standard/Premium] 22.7.1 (20 luglio 2022)

Questa versione include i miglioramenti e le correzioni seguenti:

| Funzione | Descrizione |
| --- | --- |
| Miglioramento della precisione di valutazione del pubblico e della latenza dell&#39;utente finale tramite il supporto IPv6 | Le geolocalizzazioni dei visitatori ora sono determinate dagli indirizzi IPv6, se disponibili, anziché solo dagli indirizzi IPv4. Le API di distribuzione supportano anche i parametri di input IPv6. I filtri e l’inserimento nell’elenco Consentiti supportano sia gli indirizzi IPv4 che IPv6. Questo supporto IPv6 in questa versione significa che i visitatori verranno inclusi in modo più preciso nei tipi di pubblico (più accuratamente qualificati per le attività o da includere nei criteri di filtro). Inoltre, migliora la latenza dei dati, in quanto i client IPv6 si instradano direttamente, evitando il sovraccarico del gateway IPv6-to-IPv4. |
| Miglioramento della gestione del payload lato client di A4T | Con l’integrazione lato server di A4T, se Adobe Target identifica una richiesta come proveniente da un bot, non inoltra il payload ad Analytics e non esiste un evento mod_stats nei registri di Target. Prima di questa versione, le integrazioni lato client di A4T inoltravano il payload ad Analytics, anche quando era stato identificato come traffico da bot. Questa incoerenza tra lato server e lato client creerebbe discrepanze, in quanto i rapporti A4T per quest’ultimo includevano il traffico da bot. Inoltre, il traffico da bot non è stato necessariamente identificato né segnalato, il che significa che non è stato possibile distinguere o rimuovere il traffico da bot dal resto del traffico. E anche se un cliente tenesse conto del traffico da solo, non corrisponderebbe necessariamente all&#39;insieme di traffico che Target identificava ed escludeva come traffico da bot, il che porterebbe a discrepanze separate o altri problemi. Con questa versione, la registrazione lato client di A4T è stata migliorata in modo che il comportamento relativo al payload A4T sia lo stesso di quello relativo al lato server di A4T: I visitatori identificati come bot sono esclusi dal conteggio/reporting di Target, sia per le implementazioni lato server che per quelle lato client. |

## [!DNL Target Standard/Premium] 22.6.2 (30 giugno 2022)

Questa versione include i miglioramenti e le correzioni seguenti:

| Funzione | Descrizione |
| --- | ---  |
| Notifiche interne al prodotto | Ottieni le seguenti notifiche interne al prodotto:<ul><li>**Attività**: notifiche per tutti i tipi di attività quando un&#39;attività viene approvata o disattivata, manualmente o alla sua data di inizio o di fine. La notifica include il nome dell’attività e un collegamento per accedere alla pagina di panoramica dell’attività.</li><li>**Script di profilo**: notifiche quando uno script di profilo viene attivato o disattivato, manualmente o da Target.</li><li>**Feed di Recommendations**: notifiche quando un feed di Recommendations viene attivato o disattivato, manualmente o da Target. Le notifiche vengono inviate anche quando un feed di Recommendations non riesce.</li></ul> Per impostazione predefinita, le notifiche vengono ricevute dagli amministratori di prodotto, e dagli utenti che pubblicano e che approvano. Le notifiche possono essere configurate nelle preferenze di Experience Cloud.<br>Per ulteriori informazioni consulta [Notifiche e annunci](/help/main/c-intro/understand-the-target-ui.md#notifications-announcements). |
| *Guida per gli sviluppatori di Adobe Target* | La *Guida per gli sviluppatori di Adobe Target* consolida tutti i contenuti per sviluppatori di [!DNL Target] in un’unica pratica guida. La guida include informazioni sull’implementazione di [!DNL Target] e [!DNL Recommendations], sugli SDK di [!DNL Target] e sulle API di [!DNL Target].<br>Per ulteriori informazioni, consulta la [Guida per gli sviluppatori di Adobe Target](https://developer.adobe.com/target/){target=_blank}. |

* Gli utenti con il ruolo di [!UICONTROL editor] non possono più modificare i tipi di pubblico nelle attività live. (TGT-43582)
* Viene visualizzato un messaggio di avvertenza se un cliente tenta di salvare un pubblico il cui nome contiene un punto esclamativo ( ! ) come primo carattere (esempio: !Londra). (TGT-43643)
* È stato risolto un problema a causa del quale alcune schede dei dettagli di definizione del pubblico per alcuni clienti indicavano che un’attività terminata è ancora in esecuzione. (TGT-43527)

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
