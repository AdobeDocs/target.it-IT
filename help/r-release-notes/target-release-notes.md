---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: Note sulla versione che forniscono informazioni su funzioni, miglioramenti e correzioni per le versioni DNL  Adobe Target più recenti o imminenti.
title: ' note sulla versione prerelease di Adobe Target'
feature: null
translation-type: tm+mt
source-git-commit: 531e147d99bbc73414f790d66a3633bd1de8f50f
workflow-type: tm+mt
source-wordcount: '762'
ht-degree: 11%

---


# Note sulla versione di Target (prerelease){#target-release-notes-prerelease}

Questo articolo contiene informazioni prerelease. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 6 gennaio 2021**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni presenti in queste pagine potrebbero essere le stesse, a seconda della data di rilascio. I codici tra parentesi sono per uso interno di [!DNL Adobe].

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

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
