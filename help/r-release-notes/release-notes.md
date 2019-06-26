---
description: Queste note sulla versione forniscono informazioni su funzionalità, miglioramenti, correzioni e problemi noti per ogni versione di Target Standard e Target Premium.
keywords: Note sulla versione;prerelease
seo-description: Queste note sulla versione forniscono informazioni su funzioni, miglioramenti, correzioni e problemi noti per ciascuna versione di Adobe Target Standard e Target Premium.
seo-title: Note sulla versione di Target (corrente)
solution: Target
title: Note sulla versione di Target (corrente)
topic: Consigli
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: 3d0849af03dcaf1fb400b21e4f975fb35d7be87d

---


# Note sulla versione di Target (corrente){#target-release-notes-current}

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di Target Standard e Target Premium.

## Annunci

Tieni presenti i seguenti importanti annunci:

* Il 20 febbraio 2019, l’infrastruttura Adobe Target è stata aggiornata nelle aree EMEA, Giappone e APAC per non raccogliere più dati dagli utenti finali con dispositivi meno recenti o browser web che non supportano TLS 1.1 o versione successiva. Lo stesso aggiornamento è pianificato per l’area Nord America al **1 aprile 2019**. La migrazione a TLS 1.2 offre una maggiore protezione. Per evitare problemi durante la transizione, è importante esaminare a fondo le specifiche e pianificare le modifiche con il tuo team IT. Per ulteriori informazioni, vedi [Modifiche alla crittografia TLS (Transport Layer Security)](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md).
* [!DNL Target] e [!DNL Adobe Marketing Cloud] abbandoneranno il supporto per Microsoft Internet Explorer 11 a partire da marzo 2019. Questa modifica influisce solo sull’authoring di [!DNL Target] senza influire sulla distribuzione delle esperienze. Passa a Microsoft Edge o a un altro browser. Per ulteriori informazioni, consulta [Browser supportati](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md).

## Target Standard/Premium 19.6.1 (26 giugno 2019)

Questa versione include le seguenti nuove funzionalità e miglioramenti:

| Funzione / Miglioramento | Descrizione |
| --- | --- |
| Compositore esperienza visivo | **Nuove opzioni del menu VEC**: Quando fate clic su un elemento di pagina nella VEC, un menu mostra le opzioni disponibili per tale tipo di elemento.<ul><li>You can now use the [!UICONTROL Styles &gt; Background] option to change the background image and color for the selected element. (TGT-15001)</li></ul>See *Styles* in [Visual Experience Options](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#styles).<br>**Miglioramenti del monitoraggio dei clic**: È stata migliorata la procedura per configurare il monitoraggio dei clic all&#39;interno della VEC e della VEC (Single Page Application).<ul><li>Quando selezionate gli elementi da usare nel tracciamento dei clic, i nomi di tutti gli elementi disponibili vengono visualizzati nel pannello Modifiche a destra, rendendo più facile e veloce selezionare gli elementi desiderati.</li><li>The [!UICONTROL Goals &amp; Settings] page of the three-part guided activity workflow displays a number representing the number of elements selected for click tracking. Potete passare il cursore sopra questo numero per visualizzare i nomi di tutti gli elementi selezionati. (TGT-33878)</li></ul>See [Click tracking](/help/c-activities/r-success-metrics/click-tracking.md). |
| Compositore esperienza visivo per app a pagina singola (SPA VEC) | **Flusso di lavoro guidato**: Un nuovo flusso di lavoro guidato consente di comprendere in che modo le impostazioni della regola di consegna pagina devono essere configurate per eseguire ed eseguire un&#39;attività per l&#39;app singola pagina. (TGT-33718)<br> See [Single Page App (SPA) Visual Experience Composer](/help/c-experiences/spa-visual-experience-composer.md#page-delivery-settings).<br>**Modifiche clone**: Ora potete definire una modifica utilizzando la VEC di SPA e quindi clonarla per utilizzarla in altre viste nell&#39;app pagina singola. (TGT-33882)<br>See [Single Page App (SPA) Visual Experience Composer](/help/c-experiences/spa-visual-experience-composer.md). |
| Compositore esperienza visivo mobile | **Più versioni app**: Ora puoi creare attività per più versioni della tua app mobile. In questo modo potrete risparmiare tempo e fatica quando le versioni sono simili e non dovete modificare in modo significativo l&#39;interfaccia utente dell&#39;app. (TGT-34231)<br>See &quot;Manage multiple app versions&quot; in [Mobile App Visual Experience Composer](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md#using-the-mobile-vec). |
| ![Badge Premium](/help/assets/premium.png) Automated Personalization (Personalizzazione automatizzata) (AP) e Auto-Target | **Esperienza specifica come controllo**: Potete selezionare un&#39;esperienza da utilizzare come controllo durante la creazione di un&#39;attività AP o Auto-Target. Questa funzione consente di indirizzare l&#39;intero traffico di controllo a un&#39;esperienza specifica, in base alla percentuale di allocazione del traffico configurata nell&#39;attività. Potete quindi valutare i rapporti sulle prestazioni del traffico personalizzato contro il controllo del traffico verso quella singola esperienza. L&#39;opzione di controllo corrente (in modo casuale) continuerà a essere disponibile. (TGT-32801, TGT-26572, &amp; TGT-26571)<br>See [Select the control for your Automated Personalization or Auto-Target Activity](/help/c-activities/t-automated-personalization/experience-as-control.md).<br>**Rapporti sulle personalizzazioni**: La denominazione intuitiva degli attributi per gli attributi quando un visitatore visualizza contenuti specifici in una posizione specifica fornisce informazioni più significative. (TGT-33421 &amp; TGT-34957)<br>See [Data collection for the Target personalization algorithms](/help/c-activities/t-automated-personalization/ap-data.md). |
| ![Recommendations badge](/help/assets/premium.png) Recommendations | È possibile utilizzare l’opzione Consigliare gli articoli precedentemente acquistati durante la creazione della logica Articoli visualizzati di recente. (TGT-34030)<br>Per ulteriori informazioni, consultate [Recently Viewed Items](/help/c-recommendations/c-algorithms/create-new-algorithm.md#previously-purchased) in &quot;Create criteria.&quot; |
| Criteri cookie Google Chrome samesite | Google ha recentemente annunciato che a partire da Chrome 76, che viene ridotto a una versione del 30 luglio 2019, gli sviluppatori devono specificare esplicitamente quali cookie funzionano tra i siti Web e quali cookie possono tracciare gli utenti.<br>Poiché il settore si occupa della creazione di un Web più sicuro per i consumatori, Target si impegna costantemente a distribuire esperienze personalizzate durante la riunione e superare le aspettative sulla privacy dei visitatori.<br>Consultate [Criteri cookie Google Chrome samesite](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/google-chrome-samesite-cookie-policies.md). |

## at. js versione 2.1.0 (3 giugno 2019)

Siamo entusiasti di annunciare le seguenti funzionalità entusiasmanti in at. js 2.1.0:

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| Assistenza Adobe Consenso | Adobe Opt-in è un metodo per semplificare le integrazioni delle soluzioni Adobe con le piattaforme di gestione del consenso.<br>Per ulteriori informazioni su Adobe Opt-in, consulta [Privacy e Regolamento generale sulla protezione dei dati (RGPD)](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md). |
| Conformità standard di settore CSP | at. js no uses eval () to execute javascript. |
| Registrazione analisi lato client | Offre ai clienti il controllo completo su come desiderano inviare dati analitici ad Adobe Analytics, sia sul lato client che sul lato server.<br>Per ulteriori informazioni, vedi [Accesso a Analytics lato client](/help/c-integrating-target-with-mac/a4t/before-implement.md#client-side) in *prima di implementare*. |
| Inviare notifiche | Allows developers to send notifications when an experience is rendered by their code instead of using `applyOffer()` or `applyOffers()`.<br>Per ulteriori informazioni, vedete [adobe. target. sendnotifications (opzioni)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe.target.sendnotifications-atjs-21.md). |
| Dimensioni file ridotte | La dimensione di at. js viene ridotta di ~ 24%. Le dimensioni del file più piccole migliorano le prestazioni di caricamento delle pagine e riducono il tempo di download su. js sulla pagina. |
| aggiornamenti della documentazione at. js | For a full list of all articles updated due to the at.js 2.1.0 release, see the June 3, 2019 entries in [Documentation changes](/help/r-release-notes/doc-change.md). |

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