---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: Queste note sulla versione forniscono informazioni su funzioni, miglioramenti, correzioni e problemi noti per ciascuna versione di Adobe Target Standard e Target Premium.
title: 'Note sulla versione di Adobe Target (corrente) '
feature: release notes
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: b6d4cc35e32f118ff46fcd3b235c8b5deae35d05
workflow-type: tm+mt
source-wordcount: '950'
ht-degree: 26%

---


# Note sulla versione di Target (corrente){#target-release-notes-current}

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di Target Standard e Target Premium. Inoltre, se applicabile, sono incluse anche le note sulla versione per le API Target, gli SDK, la libreria JavaScript (at.js) e altre modifiche alla piattaforma.

>[!IMPORTANT]
>
>* **fine ciclo di vita** di mbox.js: Il 18 gennaio 2021  Adobe Target non supporterà più la libreria mbox.js. Dopo il 18 gennaio 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto positivo sulle pagine che hanno attività Target in esecuzione distribuendo contenuto predefinito. È consigliabile che tutti i clienti effettuino la migrazione alla versione più recente della libreria at.js prima di tale data, in modo da evitare potenziali problemi con i siti. Per ulteriori informazioni, consulta [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) and [Adobe Target Skill Builder (Funzionamento di At.js e generazione di competenze): Chat sviluppatore, migrate  Adobe Target mbox.js in at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
   >
   >   
   Sebbene mbox.js sia attualmente supportato, a partire da luglio 2017 non sono stati forniti aggiornamenti di funzionalità per questa libreria. Il più recente at.js offre molti vantaggi rispetto a mbox.js. Tra gli altri vantaggi, at.js migliora i tempi di caricamento delle pagine per le implementazioni Web, migliora la sicurezza e offre migliori opzioni di implementazione per le applicazioni a pagina singola.
   >
   >   
   Trasferendo tutti i clienti a at.js, i nostri tecnici e il nostro staff di supporto saranno in grado di fornirvi nuove funzionalità e di offrire il supporto che vi aspettate da  Adobe.
   >
   >
* **Annunci** Target: Consultate la pagina degli annunci di Target per informazioni sugli eventi in programma, comprese le sessioni di Target Experience Builder, le chat per sviluppatori, i webinar e le sessioni Target Coffee Break. Per ulteriori informazioni, vedi Annunci [Target](/help/r-release-notes/target-announcements.md).


I codici tra parentesi sono per uso interno di [!DNL Adobe].

## Target Standard/Premium 20.10.1 (28 ottobre 2020)

Questa versione contiene le nuove funzioni seguenti:

| Funzione | Dettagli |
| --- | --- |
| [Decisioni su dispositivo](https://adobetarget-sdks.gitbook.io/docs/on-device-decisioning/introduction-to-on-device-decisioning) | La decisione sul dispositivo consente sia agli esperti di marketing che agli sviluppatori di prodotti di distribuire la sperimentazione e la personalizzazione basata sull&#39;apprendimento automatico dall&#39;interno del dispositivo dell&#39;utente, attraverso i canali, a una latenza quasi zero.<br>La velocità e le prestazioni sono importanti, in termini di approfondimenti e soddisfazione degli utenti.<br>La decisione sul dispositivo consente di compilare le istruzioni chiave di personalizzazione e sperimentazione nei tipi di attività Test e Targeting delle esperienze (XT) A/B in oggetti JSON &quot;ottimization artifact:&quot; caricati sui dispositivi dei clienti tramite CDN. Inoltre, grazie al collegamento nativo delle decisioni sui dispositivi con [!DNL Adobe Experience Cloud] i prodotti, [!DNL Target] gli utenti possono eseguire analisi rapide e iterazioni più veloci dell&#39;esperienza.<br>Per ulteriori informazioni, consulta *[Introduzione alle decisioni](https://adobetarget-sdks.gitbook.io/docs/on-device-decisioning/introduction-to-on-device-decisioning)* sul dispositivo nella Guida agli SDK per *Adobe Target*.<br>**Registratevi ora per un webinar live.** Partecipate  esperti di prodotti Adobe Target per discutere di come le decisioni di ottimizzazione dell&#39;esperienza sul dispositivo, da eseguire localmente con latenza zero, possano aprire le porte a nuovi casi d&#39;uso entusiasmanti e migliorare le prestazioni del sito per i vostri clienti.<ul><li>10 novembre 2020</li><li>10 PT / 12 CT / 1 p.m. ET</li><li>[Registrati qui](https://www.adobeeventsonline.com/Target/2020/OnDeviceDecisions/invite.html)</li></ul> |

Questa versione contiene i seguenti miglioramenti, correzioni e modifiche:

* È stato risolto un problema che impediva la visualizzazione dell&#39;intervallo [!UICONTROL medio di confidenza e della] confidenza [!UICONTROL dell&#39;incremento nel] reporting per la riga [!DNL Auto-Target] Totale  . Misurazioni visualizzate correttamente per tutte le singole esperienze. (TGT-37301)
* È stato risolto un problema che interessava il reporting di [!DNL Adobe Target Premium] Auto-Target  degli utenti a partire dal 15 settembre alle 2:30. (PDT) al 6 ottobre, 9:25 (PDT). Quando visualizzate i rapporti per le metriche di conversione interessate (configurate utilizzando l&#39;opzione &quot;[!UICONTROL Visualizzato una pagina]&quot; o &quot;[!UICONTROL Premuto su mbox]&quot;), i tassi di conversione vengono segnalati in modo non corretto. Nessun problema di consegna noto al momento. Per informazioni su come risincronizzare e correggere i rapporti, vedi Report [di](/help/r-release-notes/known-issues-resolved-issues.md#at-metrics) Auto-Target in Problemi ** risolti in Problemi *noti e problemi* risolti.
* È stata aggiunta una colonna [!UICONTROL Ultimo aggiornamento] selezionabile nella tabella Ricerca  catalogo e un filtro [!UICONTROL Ultimo aggiornamento a] . Questo miglioramento consente di risparmiare tempo e fatica perché non è necessario aprire ogni singolo elemento per vedere quando è stato aggiornato per l&#39;ultima volta e si può filtrare per data l&#39;ultimo aggiornamento degli elementi.

   ![Ultimo aggiornamento a colonna e illustrazione filtro](/help/r-release-notes/assets/column-and-filter.png)

* Sono stati effettuati aggiornamenti per rendere l&#39;interfaccia utente di Target conforme alle linee guida [per l&#39;accessibilità dei contenuti](https://www.w3.org/WAI/standards-guidelines/wcag/) Web 2.0 di livello A e AA (WCAG 2.0 AA). (TGT-34384 e TGT-24679)
* Miglioramenti apportati all&#39;informativa sulla sicurezza dei contenuti (CSP). (TGT-37035)
* È stato introdotto un modo per specificare il codice client come parametro per i clienti che utilizzano CNAME. (TNT-38571)
* [!DNL Adobe Experience Cloud] la documentazione si sta spostando in [!DNL Experience League]. Nel mese di ottobre, tutte le note sulla versione, gli articoli, i video e le esercitazioni verranno spostati dalla posizione corrente `docs.adobe.com` alla [!DNL Experience League]. Questa operazione garantisce che tutti i contenuti di apprendimento, supporto autonomo, abilitazione e community vengano serviti da un&#39;unica posizione. Quando si verifica questa modifica, non è necessario eseguire alcuna operazione, in quanto tutti i collegamenti verranno reindirizzati a [!DNL Experience League]. Le note sulla versione verranno aggiornate all’inizio del ritaglio.

## Note aggiuntive sulla versione e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Dettagli sulle versioni di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js [!DNL Adobe Target]. |

## Modifiche alla documentazione, precedenti note sulla versione e note sulla versione di Experience Cloud

Per informazioni aggiuntive, oltre alle note di ciascuna versione, consulta le seguenti risorse:

| Risorsa | Dettagli |
|--- |--- |
| Modifiche alla documentazione | Informazioni dettagliate sugli aggiornamenti apportati a questa guida che potrebbero non essere incluse nelle note sulla versione.<br>Per ulteriori informazioni, consulta [Modifiche alla documentazione](../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Note sulla versione per le versioni precedenti | Informazioni su nuove funzionalità e miglioramenti introdotti nelle versioni precedenti di Target Standard e Target Premium.<br>Per ulteriori informazioni, consulta [Note sulla versione per le versioni precedenti](../r-release-notes/release-notes-for-previous-releases.md). |
| Note sulla versione di Adobe Experience Cloud | Ultime note sulla versione per le soluzioni Adobe Experience Cloud.<br>Per ulteriori informazioni, consulta [Experience Cloud - Note](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html)sulla versione. |

## Informazioni in anteprima {#section_5D588F0415A2435B851A4D0113ACA3A0}

Le risorse seguenti contengono informazioni sulle funzionalità in arrivo con la prossima versione di Target.

| Risorsa | Dettagli |
|--- |--- |
| Adobe Priority Product Update | Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:<br>[](https://www.adobe.com/subscription/priority-product-update.html)https://www.adobe.com/subscription/priority-product-update.html |
| Note sulle prossime versioni | Per informazioni sulle versioni di Target del mese corrente, incluse le informazioni prerelease, consulta la pagina [Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md). |
