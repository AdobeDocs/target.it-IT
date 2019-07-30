---
description: Note sulla versione che forniscono informazioni su funzioni, miglioramenti e correzioni per i prossimi o imminenti [! DNL Adobe Target].
keywords: note sulla versione
seo-description: Note sulla versione che forniscono informazioni su funzioni, miglioramenti e correzioni per i prossimi o imminenti [! DNL Adobe Target].
seo-title: Note di rilascio di Adobe Target (prerelease)
solution: Target
title: Note sulla versione di Target (prerelease)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: f49c0c94afe6bf8aadbfb76930b57bf7cd5602dc

---


# Note sulla versione di Target (prerelease){#target-release-notes-prerelease}

Queste note sulla versione contengono informazioni su funzioni, miglioramenti e correzioni per le versioni più recenti o in arrivo di [!DNL Adobe Target].

**Ultimo aggiornamento: 24 luglio 2019**

>[!NOTE]
>
>Queste note sulla versione contengono delle informazioni in anteprima. Le date di rilascio, le funzioni e altre informazioni sono soggette a modifiche senza preavviso. Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali o possono essere diverse, a seconda della tempistica delle release.
>
>The issue numbers in parentheses are for internal [!DNL Adobe] use.

## Target Standard/Premium 19.7.1 (24 luglio 2019) {#tgt-19-7-1}

Questa versione include le seguenti nuove funzionalità e miglioramenti:

| Funzione / Miglioramento | Descrizione |
| --- | --- |
| Compositore esperienza visivo per app mobile | Nella VEC App mobile viene visualizzato un nuovo pannello Modifiche che mostra gli elementi configurati per il tracciamento dei clic. (TGT-31741)<br> See [Set up click tracking in the Mobile App](/help/c-target-mobile-app/c-mobile-visual-experience-composer/set-up-click-tracking-in-the-mobile-vec.md). |
| ![Premium badgerecommendations](/help/assets/premium.png)<br>in A/B Testing and Experience Targeting (XT) attività | Lo stato Offer Offer (algoritmo) di Recommendations viene visualizzato nella pagina Overview (Panoramica) per le attività A/B Test and XT che contengono Recommendations offerte. Gli stati includono: Risultati pronti, Risultati non pronti e Feed di feed. (TGT-33649)<br>See [Recommendations as an offer](/help/c-recommendations/recommendations-as-an-offer.md#status). |
| Supporto di monitoraggio tra più domini per at. js 2.0 + tramite la libreria Experience Cloud ID (ECID) | In precedenza, il monitoraggio tra domini non era supportato in at. js 2.*x*. Con questa release, i clienti che usano at. js 2.0 o versioni successive possono ora utilizzare il tracciamento tra domini attraverso la libreria ECID. Affinché il tracciamento interdominio funzioni, la libreria ECID deve essere installata sulla pagina insieme a. js 2.0 o versione successiva. [È](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-release-notes.html) necessario utilizzare la libreria Experience Cloud ID 4.3.0 +.<br>Consultate [Supporto di monitoraggio tra domini in at. js 2. x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md#cross-domain). |
| Supporto di Target per ITP 2.1 e ITP 2.2 di Apple tramite la libreria Experience Cloud ID (ECID) 4.3 | Oggi, i clienti di Target possono attenuare ITP 2.1 e ITP 2.2 Apple sfruttando il programma di certificazione CNAME di Adobe.<br>Con questa release, Target introduce un'integrazione senza soluzione di continuità con la libreria ECID 4.3, che sfrutta un cookie lato server per attenuare ITP 2.1 e ITP 2.2. Si consiglia fortemente ai clienti di Target di distribuire [la libreria ECID 4.3 + in](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-release-notes.html) combinazione con la libreria javascript di Target per attenuare eventuali rilasci ITP futuri. La libreria ECID continuerà a presentare miglioramenti che offrono una soluzione solida ai criteri di cookie in continua evoluzione introdotti dai browser.<br>Consultate [Apple Intelligent Tracking Prevention (ITP) 2. x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md). |

## at. js versione 2.1.1 (24 luglio 2019)

Questo rilascio di at. js è una versione di manutenzione e include i seguenti miglioramenti e correzioni:

(I codici tra parentesi sono per uso interno di Adobe.)

* È stato risolto un problema che causava l'attivazione di più beacon quando si utilizzava la metrica Click Tracking (Tracciamento) nella pagina Goals &amp; Settings (Obiettivi e impostazioni) in Visual Experience Composer (Compositore esperienza visivo) (VEC). (TNT-32812)
* Fixed an issue that caused `triggerView()` to not render offers more than once. (TNT-32780)
* Fixed an issue with `triggerView()` to ensure that the request contains Marketing Cloud ID (MCID) information. (TNT-32776)
* Fixed an issue that prevented the `triggerView()` notification to fire even if there are no saved views. (TNT-32614)
* È stato risolto un problema che causava un errore a causa dell'utilizzo di decodeuricomponent che causava problemi quando l'URL conteneva un parametro stringa di query non valido. (TNT-32710)
* The beacon flag is now set to "true" in the context of delivery requests sent via the `Navigator.sendBeacon()` API. (TNT-32683)
* È stato risolto un problema che impediva la visualizzazione delle offerte Recommendations sui siti Web per alcuni clienti. I clienti possono vedere il contenuto delle offerte nella chiamata API per la consegna, ma l'offerta non è stata applicata al sito Web. (TNT-32680)
* È stato risolto un problema che causava il mancato funzionamento del tracciamento di clic tra più esperienze. (TNT-32644)
* È stato risolto un problema che impediva all '. js di applicare la seconda metrica dopo il rendering della prima metrica. (TNT-32628)
* Fixed an issue when passing `mboxThirdPartyId` using the `targetPageParams` function that caused the request payload to not be present in either the query parameters or in the request payload. (TNT-32613)
* È stato risolto un problema che causava la visualizzazione e la selezione di risposte di notifica da bloccare nei browser basati su Chromium (incluso Google Chrome). (TNT-32290)

For information about this and previous versions of at.js, see [at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

**Miglioramenti, correzioni e modifiche**

* È stato risolto un problema che impediva la cancellazione dei valori di esclusione in Recommendations durante l'aggiunta di valori duplicati. (TGT-34996)
* Ora potete rimuovere una progettazione in un'attività di Recommendations dalla pagina Targeting (Passaggio 2 del flusso di lavoro guidato in tre parti). Per rimuovere una progettazione, è necessario selezionare più di una progettazione. (TGT-35118)
* È stato risolto un problema che impediva di caricare correttamente le schede dei criteri personalizzate nell'interfaccia utente di Target o di modificarle. (TGT-35170)

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
