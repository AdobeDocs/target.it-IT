---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di Adobe Target.
title: Quali nuove funzioni saranno incluse nella prossima versione?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 3fb58864e265653b48e851c8dff404589bb867a6
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 51%

---

# Note sulla versione di Target (prerelease)

Questo articolo contiene informazioni di pre-release. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 25 ottobre 2021**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle versioni. I codici tra parentesi sono per uso interno di [!DNL Adobe].

>[!IMPORTANT]
>
>**Termine del ciclo di vita di mbox.js**: a partire dal 31 marzo 2021, [!DNL Adobe Target] non supporta più la libreria mbox.js. Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto sulle pagine che hanno attività [!DNL Target] in esecuzione, che presenteranno il contenuto predefinito.
>
>Per evitare potenziali problemi con i siti, effettua la migrazione alla versione più recente del nuovo [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js. Per ulteriori informazioni, consulta [Panoramica: implementare Target per web lato client](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## [!DNL Target Standard/Premium] 21.10.5 (28 ottobre 2021)

Questa versione di manutenzione contiene i seguenti miglioramenti:

| Funzione | Dettagli |
| --- | --- |
| [!UICONTROL Compositore esperienza visivo] | È stato aggiunto il supporto per [Componenti web](https://developer.mozilla.org/en-US/docs/Web/Web_Components). È possibile creare e testare esperienze e offerte personalizzate su elementi personalizzati e su elementi all’interno di elementi personalizzati.<br>Questa versione coinciderà con la versione 2.7.0 di at.js. |

## [!DNL Target Standard/Premium] 21.10.4 (21 ottobre 2021)

Questa versione di manutenzione contiene i seguenti miglioramenti:

| Funzione | Dettagli |
| --- | --- |
| Recommendations basato su carrello | È stata aggiunta una nuova famiglia di algoritmi per distribuire consigli basati sul contenuto del carrello del visitatore.<br>Per ulteriori informazioni, consulta &quot;Basato su carrello&quot; in [Creare criteri](/help/c-recommendations/c-algorithms/create-new-algorithm.md) e &quot;Il carrello aggiunge/visualizza carrello/pagine di pagamento&quot; e &quot;Escludi elementi già presenti nel carrello del visitatore&quot; in [Pianificare e implementare Recommendations](/help/c-recommendations/plan-implement.md). |

## [!DNL Target Standard/Premium] 21.10.3 (19 ottobre 2021)

Questa versione di manutenzione include i seguenti miglioramenti, correzioni e modifiche:

* Sono stati risolti i problemi che impedivano ai clienti di aprire [!UICONTROL A4T] pannello in [!DNL Analysis Workspace] facendo clic sul pulsante [!UICONTROL Visualizzazione in Analytics] ingresso pulsante [!DNL Target] reporting delle attività. (TGT-42099, TGT-42100)
* È stato risolto un problema che causava il [!UICONTROL Modifica progettazione] pulsante per non visualizzare durante la modifica [!UICONTROL Test A/B] e [!UICONTROL Targeting esperienza] (XT) attività che utilizzano [!UICONTROL Compositore esperienza basato su moduli]. (TGT-41980)
* È stato risolto un problema che impediva la [!UICONTROL Compatibile] visualizzazione di una casella di controllo nella selezione dei criteri durante la creazione di una nuova [!UICONTROL Recommendations] attività. (TGT-42053)
* È stato corretto un messaggio di errore errato visualizzato quando non era possibile selezionare [!DNL Analytics] come origine per la generazione di rapporti (A4T) per mancanza di [!DNL Analytics] autorizzazioni. (TGT-41954)
* Sono state implementate più correzioni di accessibilità per migliorare la navigazione da tastiera in tutti gli [!DNL Target] Interfaccia utente.

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
