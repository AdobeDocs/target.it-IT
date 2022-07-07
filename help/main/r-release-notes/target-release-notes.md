---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di Adobe Target.
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: fa6324606b32f265084615fd1c13ce6c49921b48
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 55%

---

# Note sulla versione di Target (prerelease)

Questo articolo contiene informazioni di pre-release. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 30 giugno 2022**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle versioni. I codici tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target Standard/Premium] 22.6.2 (30 giugno 2022)

Questa versione contiene le seguenti funzioni, miglioramenti e correzioni:

| Funzione | Descrizione |
| --- | ---  |
| Notifiche interne al prodotto | Ottieni le seguenti notifiche interne al prodotto:<ul><li>**Attività**: Notifiche per tutti i tipi di attività quando un&#39;attività viene approvata o disattivata, manualmente o quando raggiunge la data di inizio o di fine. La notifica include il nome dell’attività con un collegamento alla pagina di panoramica dell’attività.</li><li>**Script di profilo** Notifiche quando uno script di profilo viene attivato o disattivato, manualmente o da Target.</li><li>**Feed Recommendations**: Notifiche quando un feed Recommendations viene attivato o disattivato, manualmente o da Target. Le notifiche vengono inviate anche quando un feed Recommendations non riesce.</li></ul> Per impostazione predefinita, le notifiche vengono ricevute da amministratori di prodotto, editori e approvatori. Le notifiche sono configurabili nelle preferenze di Experience Cloud.<br>Per ulteriori informazioni consulta [Notifiche e annunci](/help/main/c-intro/understand-the-target-ui.md#notifications-announcements). |
| *Guida per gli sviluppatori di Adobe Target* | La *Guida per gli sviluppatori di Adobe Target* consolida tutti [!DNL Target] contenuti per sviluppatori in un’unica guida utile. La guida include informazioni sull’implementazione di [!DNL Target] e [!DNL Recommendations], [!DNL Target] SDK e [!DNL Target] API.<br>Per ulteriori informazioni, consulta [Guida per gli sviluppatori di Adobe Target](https://developer.adobe.com/target/){target=_blank}. |

* Gli utenti con il ruolo di [!UICONTROL editor] non possono più modificare i tipi di pubblico nelle attività live. (TGT-43582)
* Viene visualizzato un messaggio di avvertenza se un cliente tenta di salvare un pubblico il cui nome contiene un punto esclamativo ( ! ) come primo carattere (esempio: !Londra). (TGT-43643)
* È stato risolto un problema a causa del quale alcune schede dei dettagli di definizione del pubblico per alcuni clienti indicavano che un’attività terminata è ancora in esecuzione. (TGT-43527)

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
