---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di Adobe Target.
title: Quali nuove funzioni saranno incluse nella prossima versione?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 89b995f20491fe0a51c91f8a1fe7e6b1ccc7f974
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 100%

---

# Note sulla versione di Target (prerelease)

Questo articolo contiene informazioni di pre-release. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 28 ottobre 2021**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle versioni. I codici tra parentesi sono per uso interno di [!DNL Adobe].

>[!IMPORTANT]
>
>**Termine del ciclo di vita di mbox.js**: a partire dal 31 marzo 2021, [!DNL Adobe Target] non supporta più la libreria mbox.js. Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto sulle pagine che hanno attività [!DNL Target] in esecuzione, che presenteranno il contenuto predefinito.
>
>Per evitare potenziali problemi con i siti, effettua la migrazione alla versione più recente del nuovo [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js. Per ulteriori informazioni, consulta [Panoramica: implementare Target per web lato client](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## at.js versione 2.7.0 (28 ottobre 2021)

Questa versione contiene i seguenti miglioramenti:

* È stato aggiunto il supporto per [Componenti web](https://developer.mozilla.org/en-US/docs/Web/Web_Components). Questa versione di at.js è necessaria per creare e testare esperienze e offerte personalizzate su elementi personalizzati e su elementi al loro interno. Questa funzionalità è inclusa in [!DNL Target Standard/Premium] versione 21.10.5.

## [!DNL Target Standard/Premium] 21.10.5 (28 ottobre 2021)

Questa versione di manutenzione include i seguenti miglioramenti:

| Funzione | Dettagli |
| --- | --- |
| [!UICONTROL Compositore esperienza visivo] | È stato aggiunto il supporto per [Componenti web](https://developer.mozilla.org/en-US/docs/Web/Web_Components). È possibile creare e testare esperienze e offerte personalizzate su elementi personalizzati e su elementi al loro interno.<br>Per ulteriori informazioni, consulta la sezione sulle [opzioni del Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#custom). |

## [!DNL Target Standard/Premium] 21.10.4 (21 ottobre 2021)

Questa versione di manutenzione include i seguenti miglioramenti:

| Funzione | Dettagli |
| --- | --- |
| Consigli in base al carrello | È stata aggiunta una nuova famiglia di algoritmi per distribuire consigli in base al contenuto del carrello del visitatore.<br>Per ulteriori informazioni, consulta “In base al carrello” in [Creare i criteri](/help/c-recommendations/c-algorithms/create-new-algorithm.md) e “Aggiunte al carrello, Visualizzazioni carrello, Pagine pagamento” ed “Escludi articoli già nel carrello del visitatore” in [Pianificare e implementare i consigli](/help/c-recommendations/plan-implement.md). |

## [!DNL Target Standard/Premium] 21.10.3 (19 ottobre 2021)

Questa versione di manutenzione include i seguenti miglioramenti, correzioni e modifiche:

* Sono stati risolti i problemi che impedivano ai clienti di aprire il pannello [!UICONTROL A4T] in [!DNL Analysis Workspace] facendo clic sul pulsante [!UICONTROL Visualizza in Analytics] nel reporting delle attività di [!DNL Target]. (TGT-42099, TGT-42100)
* È stato risolto un problema che impediva la visualizzazione del pulsante [!UICONTROL Modifica progettazione] durante la modifica delle attività [!UICONTROL Test A/B] e [!UICONTROL targeting dell’esperienza] (XT) utilizzando il [!UICONTROL Compositore esperienza basato su moduli]. (TGT-41980)
* È stato risolto un problema che impediva la visualizzazione di una casella di controllo [!UICONTROL Compatibile] nella selezione dei criteri durante la creazione di una nuova attività [!UICONTROL Recommendations]. (TGT-42053)
* È stato corretto un messaggio di errore errato visualizzato quando non era possibile selezionare [!DNL Analytics] come origine per la generazione di rapporti (A4T) per mancanza di autorizzazioni [!DNL Analytics]. (TGT-41954)
* Sono state implementate più correzioni di accessibilità per migliorare la navigazione da tastiera in tutte le aree dell’interfaccia utente di [!DNL Target].

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
