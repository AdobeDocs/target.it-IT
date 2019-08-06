---
description: Queste note sulla versione forniscono informazioni su funzionalità, miglioramenti, correzioni e problemi noti per ogni versione di Target Standard e Target Premium.
keywords: Note sulla versione;prerelease
seo-description: Queste note sulla versione forniscono informazioni su funzioni, miglioramenti, correzioni e problemi noti per ciascuna versione di Adobe Target Standard e Target Premium.
seo-title: Note sulla versione di Adobe Target (corrente)
solution: Target
title: Note sulla versione di Target (corrente)
topic: Consigli
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: 51f52bb40a0af4dac63236d46e6d6f0286cbb877

---


# Note sulla versione di Target (corrente){#target-release-notes-current}

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di Target Standard e Target Premium.

## Annunci

**31 luglio 2019**

[!UICONTROL Le autorizzazioni Enterprise] consentono [!DNL Target] ai clienti di utilizzare un'unica organizzazione, ma dividerla in aree di lavoro per diversi team o flussi di lavoro. La [!UICONTROL funzione Autorizzazioni] Enterprise semplifica il ridimensionamento efficace dei programmi di ottimizzazione tra i team. Anche se questa funzione era disponibile nell' [!DNL Target] interfaccia utente, le API amministratore non hanno superato il supporto corrispondente fino alla release [!DNL Target] di febbraio 2019. Adobe ha aggiornato le API Amministratore per poter utilizzare l'account di integrazione per accedere a tutte le aree di lavoro create nell'organizzazione. Così, mentre nelle versioni precedenti, le API amministratore erano limitate all'area di lavoro predefinita, l'aggiornamento di febbraio 2019 consentiva l'accesso a tutte le aree di lavoro con accesso [!UICONTROL Approver] .

Con la prossima release [!DNL Target] di settembre 2019, [!UICONTROL le autorizzazioni Enterprise] concederanno ai clienti i seguenti controlli di accesso:

* Potete scegliere le aree di lavoro a cui applicare l'integrazione.
* Potete applicare un ruolo all'integrazione I/O di Adobe: [!UICONTROL Approver], [!UICONTROL Editor]o [!UICONTROL Observer].

**Azione richiesta**: I clienti che stanno sfruttando API per operazioni CRUD su risorse (attività, tipi di pubblico, offerte e rapporti) in tutte le aree di lavoro devono concedere l'accesso esistente di integrazione I/O di Adobe a tutte le aree di lavoro con il ruolo desiderato. Prior to the September release, all integrations operated using [!UICONTROL Approver] access, regardless of the role selected from the [!UICONTROL Product Role] drop-down list. Con la prossima release, è possibile selezionare il ruolo desiderato.

Questa azione deve essere eseguita nel corso del mese **di agosto 2019**. Dopo la [!DNL Target] versione di settembre 2019, i controlli di accesso verranno attivati e potrete osservare l'accesso solo all'area di lavoro predefinita, se questa è la modalità di configurazione. Non vi sono conseguenze negative per configurare i ruoli di integrazione in anticipo.

Per istruzioni dettagliate e ulteriori informazioni, consultate [Concedere l'accesso alle integrazioni I/O Adobe alle aree di lavoro e assegnare ruoli](/help/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md).

## Ios Mobile VEC SDK iOS 2.1.0 e Android 1.1.0 (7 agosto 2019)

Questa versione di Mobile VEC SDK include i seguenti miglioramenti e correzioni:

(I codici tra parentesi sono per uso interno di Adobe.)

* Aggiunto supporto per Anteprima per attività visive su dispositivi mobili. (TGT-27875)
* È stato risolto un problema che causava la violazione di Apple Standard a causa `UIImagePickerController` dell'utilizzo.
* Dipendenza GSON rimossa da Android SDK. (TGT-31710)
* È stato risolto un problema che impediva la reimpostazione dell'offerta di consegna al momento dell'authoring. (TGT-35270)

## Target Standard/Premium 19.7.1 (24 luglio 2019) {#tgt-19-7-1}

Questa versione include le seguenti nuove funzionalità e miglioramenti:

(I codici tra parentesi sono per uso interno di Adobe.)

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| Compositore esperienza visivo per app mobile | Nella VEC App mobile viene visualizzato un nuovo pannello Modifiche che mostra gli elementi configurati per il tracciamento dei clic. (TGT -31741)<br> Vedete [Configurare il monitoraggio dei clic nell'app mobile](/help/c-target-mobile-app/c-mobile-visual-experience-composer/set-up-click-tracking-in-the-mobile-vec.md). |
| ![Premium badgerecommendations](/help/assets/premium.png)<br>in A/B Testing and Experience Targeting (XT) attività | Lo stato Offer Offer (algoritmo) di Recommendations viene visualizzato nella pagina Overview (Panoramica) per le attività A/B Test and XT che contengono Recommendations offerte. Gli stati includono: Risultati pronti, Risultati non pronti e Feed di feed. (TGT-33649)<br>See [Recommendations as an offer](/help/c-recommendations/recommendations-as-an-offer.md#status). |
| Supporto di monitoraggio tra più domini per at. js 2.0 + tramite la libreria Experience Cloud ID (ECID) | In precedenza, il monitoraggio tra domini non era supportato in at. js 2.*x*. Con questa release, i clienti che usano at. js 2.0 o versioni successive possono ora utilizzare il tracciamento tra domini attraverso la libreria ECID. Affinché il tracciamento interdominio funzioni, la libreria ECID deve essere installata sulla pagina insieme a. js 2.0 o versione successiva. [È](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-release-notes.html) necessario utilizzare la libreria Experience Cloud ID 4.3.0 +.<br>Consultate [Supporto di monitoraggio tra domini in at. js 2. x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md#cross-domain). |
| Supporto di Target per ITP 2.1 e ITP 2.2 di Apple tramite la libreria Experience Cloud ID (ECID) 4.3 | Oggi, i clienti di Target possono attenuare ITP 2.1 e ITP 2.2 Apple sfruttando il programma di certificazione CNAME di Adobe.<br>Con questa release, Target introduce un'integrazione senza soluzione di continuità con la libreria ECID 4.3, che sfrutta un cookie lato server per attenuare ITP 2.1 e ITP 2.2. Si consiglia fortemente ai clienti di Target di distribuire [la libreria ECID 4.3 + in](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-release-notes.html) combinazione con la libreria javascript di Target per attenuare eventuali rilasci ITP futuri. La libreria ECID continuerà a presentare miglioramenti che offrono una soluzione solida ai criteri di cookie in continua evoluzione introdotti dai browser.<br>Consultate [Apple Intelligent Tracking Prevention (ITP) 2. x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md). |

**Miglioramenti, correzioni e modifiche**

* È stato risolto un problema che impediva la cancellazione dei valori di esclusione in Recommendations durante l'aggiunta di valori duplicati. (TGT-34996)
* Ora potete rimuovere una progettazione in un'attività di Recommendations dalla pagina Targeting (Passaggio 2 del flusso di lavoro guidato in tre parti). Per rimuovere una progettazione, è necessario selezionare più di una progettazione. (TGT-35118)
* È stato risolto un problema che impediva di caricare correttamente le schede dei criteri personalizzate nell'interfaccia utente di Target o di modificarle. (TGT-35170)

## at. js versione 2.1.1 (24 luglio 2019)

Questo rilascio di at. js è una versione di manutenzione e include i seguenti miglioramenti e correzioni:

(I codici tra parentesi sono per uso interno di Adobe.)

* È stato risolto un problema che causava l'attivazione di più beacon quando si utilizzava la metrica Click Tracking (Tracciamento) nella pagina Goals &amp; Settings (Obiettivi e impostazioni) in Visual Experience Composer (Compositore esperienza visivo) (VEC). (TNT-32812)
* È stato corretto un problema a causa `triggerView()` del quale le offerte non venivano rese più di una volta. (TNT-32780)
* Risolto un problema relativo `triggerView()` al fatto che la richiesta contenga informazioni Marketing Cloud ID (MCID). (TNT-32776)
* È stato risolto un problema che impediva l'attivazione della `triggerView()` notifica anche in assenza di visualizzazioni salvate. (TNT-32614)
* È stato risolto un problema che causava un errore a causa dell'utilizzo di decodeuricomponent che causava problemi quando l'URL conteneva un parametro stringa di query non valido. (TNT-32710)
* Il flag beacon ora è impostato su "true" nel contesto di richieste di consegna inviate tramite l' `Navigator.sendBeacon()` API. (TNT-32683)
* È stato risolto un problema che impediva la visualizzazione delle offerte Recommendations sui siti Web per alcuni clienti. I clienti possono vedere il contenuto delle offerte nella chiamata API per la consegna, ma l'offerta non è stata applicata al sito Web. (TNT-32680)
* È stato risolto un problema che causava il mancato funzionamento del tracciamento di clic tra più esperienze. (TNT-32644)
* È stato risolto un problema che impediva all '. js di applicare la seconda metrica dopo il rendering della prima metrica. (TNT-32628)
* Risolto un problema durante il passaggio `mboxThirdPartyId` utilizzando la `targetPageParams` funzione che impediva la presenza del payload richiesta nei parametri query o nel payload della richiesta. (TNT-32613)
* È stato risolto un problema che causava la visualizzazione e la selezione di risposte di notifica da bloccare nei browser basati su Chromium (incluso Google Chrome). (TNT-32290)

For information about this and previous versions of at.js, see [at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

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
| Adobe Priority Product Update | Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:<br>[](https://www.adobe.com/subscription/priority-product-update.html)https://www.adobe.com/subscription/priority-product-update.html |
| Note sulle prossime versioni | Per informazioni sulle versioni di Target del mese corrente, incluse le informazioni prerelease, consulta la pagina [Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md). |
