---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di Adobe Target.
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: c351044163a6fb32ca72fa015724d3b0388c059a
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 90%

---

# Note sulla versione di Target (prerelease)

Questo articolo contiene informazioni di pre-release. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 25 maggio 2022**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle versioni. I codici tra parentesi sono per uso interno di [!DNL Adobe].

## Versione della piattaforma Target (25 maggio 2022)

Questa versione include i miglioramenti e le correzioni seguenti:

* Aggiunto [Suggerimenti client agente utente](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/user-agent-and-client-hints.md) supporto.
* È stato risolto un problema che causava in modo intermittente timeout durante il rendering [!UICONTROL Decisioni di offerta] in [!UICONTROL Targeting esperienza] Attività (XT). (TNT-44611)

## at.js versione 2.9.0 (27 maggio 2022)

* Aggiunto [Suggerimenti client agente utente](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/user-agent-and-client-hints.md) supporto.
* È stato corretto un bug a causa del quale più richieste mbox sulla stessa pagina avevano ID impression diversi.

## [!DNL Target Standard/Premium] 22.5.1 (rilascio scaglionato; 11-13 maggio 2022)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **11 maggio**: area geografica Asia-Pacifico (APAC)
* **12 maggio**: Regione delle Americhe
* **13 maggio**: area geografica Europa, Medio Oriente e Africa (EMEA)

Questa versione include i miglioramenti e le correzioni seguenti:

* È stato risolto un problema che causava un errore JavaScript e impediva ad alcuni clienti di accedere ai dettagli di alcune attività [!UICONTROL Automated Personalization] (AP). (TGT-43526)
* È stato risolto un problema che impediva ad alcuni clienti di aggiungere (o modificare) un’offerta specifica a un’attività AP. (TGT-43503)
* È stato risolto un problema nell’interfaccia utente di [!DNL Target] a causa del quale veniva visualizzato il seguente messaggio di errore: “La mbox globale potrebbe non essere sincronizzata. Prova a salvarla di nuovo.” Questo problema era relativo alla sola interfaccia utente e non aveva alcun impatto sulle implementazioni dei clienti. (TGT-43475)
* È stato risolto un problema che impediva a un cliente di modificare perfezionamenti e tipi di pubblico a livello di esperienza per un’attività, se questi erano stati creati prima dell’implementazione della nuova interfaccia utente [!UICONTROL Tipi di pubblico]. (TGT-43433)
* È stato risolto un problema a causa del quale i clienti potevano selezionare tipi di pubblico [!DNL Adobe Audience Manager] (AAM) duplicati durante la modifica dei tipi di pubblico di reporting per un’attività. (TGT-43430)
* È stato risolto un problema che impediva ai clienti di creare tipi di pubblico duplicati, ma in aree di lavoro diverse. (TGT-43423)
* È stato risolto un problema che impediva ai clienti di eliminare le posizioni con offerte ad hoc nelle attività create nel [!UICONTROL Compositore esperienza basato su moduli]. (TGT-43315)
* È stato risolto un problema che impediva ai clienti di accedere alle offerte con codice dopo aver fatto clic su offerte con immagini e aver quindi aggiornato l’interfaccia utente. (TGT-43566)
* È stato risolto un problema che causava il ripristino dello script originale non modificato dopo che uno script di profilo veniva modificato, attivato e quindi disattivato. Ora vengono mantenute le modifiche applicate allo script di profilo. (TGT-43249)
* È stato risolto un problema che generava il seguente errore se si tentava di spostare un pubblico in un’altra area di lavoro: “Impossibile completare la richiesta. Se il problema persiste, contatta l’Assistenza clienti di Adobe.” (TGT-43212)
* È stato corretto un errore che si verificava se si clonavano modifiche al codice personalizzato per le pagine di app a pagina singola (SPA). (TGT-43137)
* È stato risolto un problema che interessava la modifica della promozione originale dopo la duplicazione di un’esperienza e la successiva modifica della promozione. (TGT-41775)

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
