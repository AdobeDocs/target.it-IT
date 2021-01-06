---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: Queste note sulla versione forniscono informazioni su funzioni, miglioramenti, correzioni e problemi noti per ciascuna versione di Adobe Target Standard e Target Premium.
title: 'Note sulla versione di Adobe Target (corrente) '
feature: Release Notes
translation-type: tm+mt
source-git-commit: 531e147d99bbc73414f790d66a3633bd1de8f50f
workflow-type: tm+mt
source-wordcount: '958'
ht-degree: 26%

---


# Note sulla versione di Target (corrente)

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di Target Standard e Target Premium. Inoltre, se applicabile, sono incluse anche le note sulla versione per le API Target, gli SDK, la libreria JavaScript (at.js) e altre modifiche alla piattaforma.

>[!IMPORTANT]
>
>**fine ciclo di vita** di mbox.js: Il 31 marzo 2021 non  [!DNL Adobe Target] supporterà più la libreria mbox.js. Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto positivo sulle pagine che hanno attività [!DNL Target] in esecuzione distribuendo contenuti predefiniti. È consigliabile che tutti i clienti effettuino la migrazione alla versione più recente della nuova [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js prima di tale data, per evitare potenziali problemi con i siti.
>
>* **Adobe Experience Platform Web SDK**: L’ [!UICONTROL Adobe Experience Platform Web ] SDK consente di interagire con i vari servizi presenti nel  [!DNL Experience Cloud] (incluso  [!DNL Target]) tramite Adobe Experience Edge Network. Se scegli di eseguire la migrazione a [!DNL Adobe Experience Platform Web SDK], consulta [What is Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html), nella *Web SDK Guide*. Per informazioni specifiche su [Target overview](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/adobe-target/target-overview.html), vedere [!DNL Target].
   >
   >
* **at.js**: La libreria JavaScript at.js offre molti vantaggi rispetto a mbox.js. Tra gli altri vantaggi, at.js migliora i tempi di caricamento delle pagine per le implementazioni Web, migliora la sicurezza e offre migliori opzioni di implementazione per le applicazioni a pagina singola. Se scegli di effettuare la migrazione a at.js, consulta [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) and [ Adobe Target Experience Builder: Chat sviluppatore, migrate  Adobe Target mbox.js in at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
>
>
Sebbene mbox.js sia attualmente supportato (fino al 31 marzo 2021), a partire da luglio 2017 non è disponibile alcun aggiornamento della funzione per questa libreria. Spostando tutti i clienti su [!UICONTROL Adobe Experience Platform Web SDK] o at.js, i nostri tecnici e personale di supporto saranno in grado di fornire nuove funzionalità e offrire il supporto che ci si aspetta da  Adobe.

I codici tra parentesi sono per uso interno di [!DNL Adobe].

## at.js 2.3.3 (13 novembre 2020)

Questa versione di at.js è una versione di manutenzione e include le seguenti correzioni:

* È stato risolto un problema relativo al tracciamento dei clic mbox e A4T.

## Target Standard/Premium 20.10.1 (27 ottobre 2020)

Questa versione contiene le nuove funzioni seguenti:

| Funzione | Dettagli |
| --- | --- |
| [Decisioni su dispositivo](https://adobetarget-sdks.gitbook.io/docs/on-device-decisioning/introduction-to-on-device-decisioning) | La decisione sul dispositivo consente sia agli esperti di marketing che agli sviluppatori di prodotti di distribuire la sperimentazione e la personalizzazione basata sull&#39;apprendimento automatico dall&#39;interno del dispositivo dell&#39;utente, attraverso i canali, a una latenza quasi zero.<br>La velocità e le prestazioni sono importanti, in termini di approfondimenti e soddisfazione degli utenti.<br>La decisione sul dispositivo consente di compilare le istruzioni chiave di personalizzazione e sperimentazione nei tipi di attività Test e Targeting delle esperienze (XT) A/B in oggetti JSON &quot;ottimization artifact:&quot; caricati sui dispositivi dei clienti tramite CDN. Inoltre, poiché le decisioni sui dispositivi si connettono in modo nativo con i prodotti [!DNL Adobe Experience Cloud], gli utenti [!DNL Target] ricevono analisi rapide e iterazioni di esperienza più veloci.<br>Per ulteriori informazioni, vedere *[Regolazione](/help/c-implementing-target/c-api-and-sdk-overview/on-device-decisioning.md) del dispositivo. |

Questa versione contiene i seguenti miglioramenti, correzioni e modifiche:

* È stato risolto un problema che impediva la visualizzazione di [!UICONTROL Intervallo di confidenza media dell&#39;incremento] e [!UICONTROL Confidence] nel report [!DNL Auto-Target] per la riga [!UICONTROL Totale]. Misurazioni visualizzate correttamente per tutte le singole esperienze. (TGT-37301)
* È stato risolto un problema che interessava il reporting degli [!DNL Adobe Target Premium] utenti [!UICONTROL Auto-Target] dal 15 settembre alle 2:30 p.m. (PDT) al 6 ottobre, 9:25 (PDT). Quando si visualizzano i rapporti per le metriche di conversione interessate (configurate mediante l&#39;opzione &quot;[!UICONTROL Visualizzato una pagina]&quot; o &quot;[!UICONTROL Selezionato su mbox]&quot;), i tassi di conversione vengono riportati in modo non corretto. Nessun problema di consegna noto al momento. Per informazioni su come risincronizzare e correggere il reporting, vedere [Generazione di rapporti con targeting automatico](/help/r-release-notes/known-issues-resolved-issues.md#at-metrics) in *Problemi risolti* in *Problemi noti e problemi risolti*.
* È stata aggiunta una colonna [!UICONTROL Ultimo aggiornamento a ] selezionabile nella tabella [!UICONTROL Ricerca nel catalogo] e un filtro [!UICONTROL Ultimo aggiornamento a]. Questo miglioramento consente di risparmiare tempo e fatica perché non è necessario aprire ogni singolo elemento per vedere quando è stato aggiornato per l&#39;ultima volta e si può filtrare per data l&#39;ultimo aggiornamento degli elementi.

   ![Ultimo aggiornamento a colonna e illustrazione filtro](/help/r-release-notes/assets/column-and-filter.png)

* Sono stati effettuati aggiornamenti per rendere l&#39;interfaccia utente di Target conforme alle [Linee guida per l&#39;accessibilità dei contenuti Web](https://www.w3.org/WAI/standards-guidelines/wcag/) 2.0 Livello A e ai criteri di successo AA (WCAG 2.0 AA). (TGT-34384 e TGT-24679)
* Miglioramenti apportati all&#39;informativa sulla sicurezza dei contenuti (CSP). (TGT-37035)
* È stato introdotto un modo per specificare il codice client come parametro per i clienti che utilizzano CNAME. (TNT-38571)
* [!DNL Adobe Experience Cloud] la documentazione si sta spostando in  [!DNL Experience League]. Durante ottobre, tutte le note sulla versione, gli articoli, i video e le esercitazioni verranno spostati dalla posizione corrente in `docs.adobe.com` a [!DNL Experience League]. Questa operazione garantisce che tutti i contenuti di apprendimento, supporto autonomo, abilitazione e community vengano serviti da un&#39;unica posizione. Quando si verifica questa modifica, non è necessario eseguire alcuna operazione, in quanto tutti i collegamenti verranno reindirizzati a [!DNL Experience League]. Le note sulla versione verranno aggiornate all’inizio del ritaglio.

## Note aggiuntive sulla versione e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Dettagli sulle versioni di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js [!DNL Adobe Target]. |

## Modifiche alla documentazione, precedenti note sulla versione e note sulla versione di Experience Cloud

Per informazioni aggiuntive, oltre alle note di ciascuna versione, consulta le seguenti risorse:

| Risorsa | Dettagli |
|--- |--- |
| Modifiche alla documentazione | Informazioni dettagliate sugli aggiornamenti apportati a questa guida che potrebbero non essere incluse nelle note sulla versione.<br>Per ulteriori informazioni, consulta [Modifiche alla documentazione](/help/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Note sulla versione per le versioni precedenti | Informazioni su nuove funzionalità e miglioramenti introdotti nelle versioni precedenti di Target Standard e Target Premium.<br>Per ulteriori informazioni, consulta [Note sulla versione per le versioni precedenti](/help/r-release-notes/release-notes-for-previous-releases.md). |
| Note sulla versione di Adobe Experience Cloud | Ultime note sulla versione per le soluzioni Adobe Experience Cloud.<br>Per ulteriori informazioni, consulta  [ Experience Cloud - Note](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html) sulla versione. |

## Informazioni in anteprima {#section_5D588F0415A2435B851A4D0113ACA3A0}

Le risorse seguenti contengono informazioni sulle funzionalità in arrivo con la prossima versione di Target.

| Risorsa | Dettagli |
|--- |--- |
| Adobe Priority Product Update | Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:<br>[](https://www.adobe.com/subscription/priority-product-update.html)https://www.adobe.com/subscription/priority-product-update.html |
| Note sulle prossime versioni | Per informazioni sulle versioni di Target del mese corrente, incluse le informazioni prerelease, consulta la pagina [Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md). |
