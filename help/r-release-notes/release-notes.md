---
description: Queste note sulla versione forniscono informazioni su funzionalità, miglioramenti, correzioni e problemi noti per ogni versione di Target Standard e Target Premium.
keywords: Note sulla versione;prerelease
seo-description: Queste note sulla versione forniscono informazioni su funzioni, miglioramenti, correzioni e problemi noti per ciascuna versione di Adobe Target Standard e Target Premium.
seo-title: Note sulla versione di Target (corrente)
solution: Target
title: Note sulla versione di Target (corrente)
topic: 'Consigli '
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: 2462ad2d49449217827fa474aa5f3f0a3e8c777d

---


# Note sulla versione di Target (corrente){#target-release-notes-current}

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di Target Standard e Target Premium.

## Annunci

Tieni presenti i seguenti importanti annunci:

* Il 20 febbraio 2019 l&#39;infrastruttura Adobe Target è stata aggiornata nelle aree EMEA, Japan e APAC per non raccogliere più dati dagli utenti finali con dispositivi meno recenti o browser Web che non supportano TLS 1.1 o versione successiva. Lo stesso aggiornamento è pianificato per l&#39;area Nord America del **1 aprile 2019**. La migrazione a TLS 1.2 offre una maggiore protezione. È importante seguire le specifiche e pianificare le modifiche con il team IT per una transizione uniforme. Per ulteriori informazioni, vedi [Modifiche alla crittografia TLS (Transport Layer Security)](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md).
* [!DNL Target] e [!DNL Adobe Marketing Cloud] abbandoneranno il supporto per Microsoft Internet Explorer 11 a partire da marzo 2019. Questa modifica influisce solo sull’authoring di [!DNL Target] senza influire sulla distribuzione delle esperienze. Passa a Microsoft Edge o a un altro browser. Per ulteriori informazioni, consulta [Browser supportati](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md).

## at. js versione 2.1.0 (3 giugno 2019)

Siamo entusiasti di annunciare le seguenti funzionalità entusiasmanti in at. js 2.1.0:

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| Assistenza Adobe Consenso | Adobe Opt-in è un metodo per semplificare le integrazioni delle soluzioni Adobe con le piattaforme di gestione del consenso.<br>Per ulteriori informazioni su Adobe Opt-in, consulta [Privacy e Regolamento generale sulla protezione dei dati (RGPD)](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md). |
| Conformità standard di settore CSP | at. js no uses eval () to execute javascript. |
| Registrazione analisi lato client | Offre ai clienti il controllo completo su come desiderano inviare dati analitici ad Adobe Analytics, sia sul lato client che sul lato server.<br>Per ulteriori informazioni, vedi [Accesso a Analytics lato client](/help/c-integrating-target-with-mac/a4t/before-implement.md#client-side) in *prima di implementare*. |
| Inviare notifiche | Consente agli sviluppatori di inviare notifiche quando un&#39;esperienza viene sottoposta a rendering dal codice anziché utilizzare `applyOffer()` o `applyOffers()`.<br>Per ulteriori informazioni, vedete [adobe. target. sendnotifications (opzioni)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe.target.sendnotifications-atjs-21.md). |
| Dimensioni file ridotte | La dimensione di at. js viene ridotta di ~ 24%. Le dimensioni del file più piccole migliorano le prestazioni di caricamento delle pagine e riducono il tempo di download su. js sulla pagina. |
| aggiornamenti della documentazione at. js | Per un elenco completo di tutti gli articoli aggiornati a causa del rilascio. js 2.1.0, consultate il 3 giugno 2019 delle modifiche [alla documentazione](/help/r-release-notes/doc-change.md). |

## Mobile App Visual Experience Composer (Compositore esperienza visivo) (14 maggio 2019) {#mobile-app-vec-may14-1}

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| Mobile App Visual Experience Composer (VEC) | La VEC App mobile consente di creare attività e personalizzare il contenuto su app native per dispositivi mobili in modo autonomo senza continuità di sviluppo e cicli di rilascio delle app.<br>Per ulteriori informazioni, consulta:<ul><li>[Compositore esperienza visivo per app mobile](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md)</li><li>[Android: configurare l&#39;app mobile](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-android.md)</li><li>[iOS: configurare l&#39;app mobile](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-ios.md)</li><li>[Configurare il tracciamento dei clic nel Compositore esperienza visivo mobile](/help/c-target-mobile-app/c-mobile-visual-experience-composer/set-up-click-tracking-in-the-mobile-vec.md)</li></ul> |

## [!DNL Target] Standard/Premium 19.5.1 (21 maggio 2019) {#tgt-19-5-1}

(I codici tra parentesi sono per uso interno di [!DNL Adobe].)

### Aggiornamenti delle funzioni

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| Compositore esperienza visivo per app a pagina singola (SPA di SPA) | Il Compositore di esperienze visive SPA include i seguenti miglioramenti per permetterti di lavorare in modo più rapido ed efficiente:<ul><li>Facendo clic su un&#39;azione in SPA viene evidenziata l&#39;elemento sul sito in cui verrà applicata l&#39;azione. Ogni azione VEC creata in una vista presenta quattro icone corrispondenti: Informazioni, Modifica, Sposta ed Elimina. La nuova funzionalità Sposta di questa versione consente di spostare l&#39;azione in un evento di caricamento pagina o in qualsiasi altra visualizzazione già esistente nel pannello delle modifiche. (TGT-33746)</li><li>Potrai eseguire molte azioni prima che la pagina si carichi nel VEC, anche nel caso in cui la pagina non riesca a caricarsi completamente (per esempio, il codice personalizzato non è più operativo). Nell’interfaccia utente di Target, le azioni che possono essere modificate solo dopo il caricamento del sito risultano disabilitate. (TGT-33851 e TGT-34149)</li></ul>Per ulteriori informazioni, consulta [Compositore esperienza visivo per app a pagina singola](/help/c-experiences/spa-visual-experience-composer.md). |

### Miglioramenti, correzioni e modifiche

* Le icone della barra degli strumenti vengono visualizzate correttamente dopo aver annullato il caricamento di una pagina nel Compositore esperienza visivo. Se non è possibile eseguire azioni specifiche finché non è stato completato il caricamento della pagina, le icone della barra degli strumenti associate sono disattivate. (TGT-33811)

## Mobile App Visual Experience Composer (Compositore esperienza visivo) (14 maggio 2019) {#mobile-vec-may14-2}

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| Mobile App Visual Experience Composer (VEC) | La VEC App mobile consente di creare attività e personalizzare il contenuto su app native per dispositivi mobili in modo autonomo senza continuità di sviluppo e cicli di rilascio delle app.<br>Per ulteriori informazioni, consulta:<ul><li>[Compositore esperienza visivo per app mobile](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md)</li><li>[Android: configurare l&#39;app mobile](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-android.md)</li><li>[iOS: configurare l&#39;app mobile](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-ios.md)</li><li>[Configurare il tracciamento dei clic nel Compositore esperienza visivo mobile](/help/c-target-mobile-app/c-mobile-visual-experience-composer/set-up-click-tracking-in-the-mobile-vec.md)</li><li>[Video: Mobile App Visual Experience Composer (Compositore esperienza visivo)](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md#video)</li></ul> |

## Modifiche alla documentazione, precedenti note sulla versione e note sulla versione di Experience Cloud {#section_1BC5F5208DA548E9B4344A0836E4B943}

Per informazioni aggiuntive, oltre alle note di ciascuna versione, consulta le seguenti risorse:

| Risorsa | Dettagli |
|--- |--- |
| Modifiche alla documentazione | Informazioni dettagliate sugli aggiornamenti apportati a questa guida che potrebbero non essere incluse nelle note sulla versione.<br>Per ulteriori informazioni, consulta [Modifiche alla documentazione](../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Note sulla versione per le versioni precedenti | Informazioni su nuove funzionalità e miglioramenti introdotti nelle versioni precedenti di Target Standard e Target Premium.<br>Per ulteriori informazioni, consulta [Note sulla versione per le versioni precedenti](../r-release-notes/release-notes-for-previous-releases.md). |
| Note sulla versione di Adobe Experience Cloud | Ultime note sulla versione per le soluzioni Adobe Experience Cloud.<br>Per ulteriori informazioni, vedi [Note sulla versione di Experience Cloud](https://marketing.adobe.com/resources/help/en_US/whatsnew/). |

## Informazioni in anteprima {#section_5D588F0415A2435B851A4D0113ACA3A0}

Le risorse seguenti contengono informazioni sulle funzionalità in arrivo con la prossima versione di Target.

| Risorsa | Dettagli |
|--- |--- |
| Adobe Priority Product Update | Per ricevere notifiche anticipate sui miglioramenti dei prodotti in arrivo a Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Prossime note sulla versione | Per informazioni sulle versioni di Target del mese corrente, incluse le informazioni pre-rilascio, consulta la pagina [Note sulla versione di Target - Pre-rilascio](/help/r-release-notes/target-release-notes.md). |