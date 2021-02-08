---
keywords: api;adobe i/o
description: Scoprite come passare dalle  API legacy di Adobe Target Classic alle nuove API  Adobe I/O.
title: Come si passa dalle API legacy a  Adobe I/O?
feature: Implement Server-side
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 89%

---


# Transizione dalle API legacy di Target ad Adobe I/O

Informazioni sulla transizione dalle API legacy di Target alle nuove API su Adobe I/O.

Con il ritiro di Adobe Target Classic, le API che sono connesse al tuo account Target Classic sono state rese non disponibili. Questo documento è utile per effettuare la transizione dalle API legacy di Target alle nuove API su Adobe I/O.

Per ulteriori informazioni sulla documentazione API di Target, vedi [API di Target e SDK di NodeJS](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md#concept_5718EC1FF2ED4436935D0BCCD7AA29A6).

## Terminologia {#section_D8286EDAE3B24D208DA432AEF2E88FD9}

| Termine | Descrizione |
|--- |--- |
| API legacy | API collegate all’account di Target Classic. Queste chiamate API richiedono l’autenticazione con nome utente e password e utilizzano il nome host `testandtarget.omniture.com`. Se le tue chiamate API contengono un nome utente e una password nell’URL della richiesta, devi eseguire la transizione alle API dell’interfaccia di Adobe I/O. |
| Adobe I/O | Adobe I/O è il nuovo gateway per le API di Target. Queste API sono connesse al tuo account Target Standard/Premium. Le API di Target su Adobe I/O utilizzano un’autenticazione basata su JWT, che è lo standard di settore per le API aziendali sicure. |

## Linea temporale {#section_A478EBF637554A2DB5A31661955121ED}

Le API legacy verranno ritirate insieme a Target Classic:

| Data | Dettagli |
|--- |--- |
| 17 ottobre 2017 | Tutti i metodi delle API che eseguono un’operazione di scrittura (`saveCampaign`, `copyCampaign`, `saveHTMLOfferContent` e `setCampaignState`) sono stati ritirati.<br>È la stessa data in cui tutti gli account utente di Target Classic sono stati impostati sullo stato di sola lettura. |
| 14 novembre 2017 | Le API rimanenti sono state disattivate. È la data in cui l&#39;interfaccia utente di Target Classic è stata ritirata. |

Le API di Recommendations Classic non saranno influenzate da questa linea temporale.

## Metodi equivalenti  {#section_DDB42CCC172545B09CB728D794CC466B}

Nella tabella seguente sono elencati i nuovi metodi delle API di Target equivalenti ai metodi API legacy. Le nuove API restituiscono JSON quando confrontate con la risposta XML fornita dalle API legacy.

I nuovi metodi delle API sono collegati alla sezione corrispondente nel sito della documentazione API. Ogni metodo di API è corredato da esempio. È inoltre possibile utilizzare la raccolta di Postman per amministratori che contiene le chiamate API di esempio per tutti i nuovi metodi delle API Adobe su Adobe I/O.

| Raggruppamento | Metodo API legacy | Nuovo metodo API | Note |
|--- |--- |--- |--- |
| Campagna/attività | Crea campagna | [Crea attività AB](http://developers.adobetarget.com/api/#create-ab-activity)<br>[Crea attività XT](http://developers.adobetarget.com/api/#create-xt-activity) | Le nuove API forniscono metodi di creazione separati per AB e XT |
|  | Aggiorna campagna | [Aggiorna l&#39;attività AB](http://developers.adobetarget.com/api/#update-ab-activity)<br>[Aggiorna l&#39;attività XT](http://developers.adobetarget.com/api/#update-xt-activity) |  |
|  | Copia campagna | N/D | Utilizza le API Crea attività |
|  | Elenco campagne | [Elenco attività](http://developers.adobetarget.com/api/#list-activities) |  |
|  | Stato campagna | [Aggiorna stato attività](http://developers.adobetarget.com/api/#update-activity-state) |  |
|  | Visualizza campagna | [Ottieni l&#39;attività AB da ID](http://developers.adobetarget.com/api/#get-ab-activity-by-id)<br>[Ottieni l&#39;attività XT per ID](http://developers.adobetarget.com/api/#get-xt-activity-by-id) |  |
|  | ID campagna di terze parti | N/D | Se si utilizza un thirdpartyID, puoi utilizzare i metodi di attività rilevanti |
| Offerte | Crea offerta | [Crea offerta](http://developers.adobetarget.com/api/#create-offer) |  |
|  | Ottieni offerta | [Ottieni offerta per ID](http://developers.adobetarget.com/api/#get-offer-by-id) |  |
|  | Elenco offerte | [Elenco offerte](http://developers.adobetarget.com/api/#list-offers) |  |
|  | Elenco cartelle | N/D | Le cartelle non sono supportate in Target Standard/Premium |
| Generazione di rapporti | Rapporto prestazioni campagna | [Ottieni rapporto prestazioni AB](http://developers.adobetarget.com/api/#get-ab-performance-report)<br>[Ottieni rapporto prestazioni XT](http://developers.adobetarget.com/api/#get-xt-performance-report) |  |
|  | Rapporto audit | [Ottieni rapporto audit](http://developers.adobetarget.com/api/#get-audit-report) |  |
|  | Rapporto contenuto 1-1 | [Ottieni rapporto prestazioni AP](http://developers.adobetarget.com/api/#get-ap-activity-performance-report) |  |
| Impostazioni account | Ottieni gruppi host | [Elenco ambienti](http://developers.adobetarget.com/api/#list-environments) |  |

## Eccezioni {#section_09CF9A0E289149279783B4801D1B6D4C}

Se hai bisogno di un&#39;eccezione, contatta il tuo Customer Success Manager.

## Aiuto  {#section_591F850E2B7A4342B1C233693425415C}

Ti invtiamo a contattare l’Assistenza clienti di Adobe Target (tt-support@adobe.com) per eventuali o se hai bisogno di aiuto nella transizione alle nuove API di Target su Adobe I/O.
