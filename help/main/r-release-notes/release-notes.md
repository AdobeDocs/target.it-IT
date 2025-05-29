---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti,aggiornamenti correnti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
short-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: bc9a0fe1977629a00eebb2f7aafd30263c8b55af
workflow-type: tm+mt
source-wordcount: '2119'
ht-degree: 18%

---

# Note sulla versione (corrente) di [!DNL Target]

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione di API di [!DNL Target], SDK, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target Standard/Premium] 25.5.4 (29 maggio 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che impediva l’aggiunta o la modifica di URL in modalità di controllo qualità. (TGT-51941)
* È stata aggiunta un&#39;impostazione di traffico in modalità Controllo di qualità in [!UICONTROL Reports] > [!UICONTROL Report Settings] ( ![icona Impostazioni report](/help/main/assets/icons/Setting.svg) ) per allinearla alle funzionalità dell&#39;interfaccia utente legacy di [!DNL Target]. (TGT-52228 e TGT-52329)
* È stato risolto un problema che causava la generazione di collegamenti di controllo qualità errati da parte dell’attività basata su moduli. L’URL/posizione dell’attività includeva un &quot;1&quot; non voluto alla fine, che ora è stato rimosso per garantire un collegamento accurato. (TGT-52355 e TGT-52358)
* È stato risolto un problema che causava la generazione di collegamenti di controllo qualità errati da parte dell’attività basata su moduli. L&#39;URL attività includeva un `http://pid-ppc` non previsto all&#39;inizio dell&#39;URL, che ora è stato rimosso per garantire un collegamento accurato. (TGT-52557)
* È stato risolto un problema a causa del quale [!DNL Target] generava collegamenti di controllo qualità non validi per le attività basate su moduli. (TGT-52528 e TGT-52603)
* È stato risolto un problema che causava l&#39;elaborazione del salvataggio di un&#39;attività modificata, ma mai completata, e nessun messaggio di errore veniva visualizzato in [!DNL Target]. (TGT-52461)
* È stato risolto un problema che impediva al [!UICONTROL Visual Experience Composer] (VEC) aggiornato di rilevare automaticamente il valore `at_property`. (TGT-52347)
* È stato risolto un problema che causava la registrazione di due modifiche quando ne era prevista solo una dopo il passaggio tra le modalità [!UICONTROL Browse] e [!UICONTROL Design] nel Compositore esperienza visivo durante l&#39;interazione con un elemento modulo. (TGT-52455)
* È stato risolto un problema che impediva la selezione dell’impostazione [!UICONTROL Clicked an Element] nel Compositore esperienza visivo aggiornato a causa di un errore che indicava che il selettore non era valido, era già utilizzato o non era visibile. (TGT-52467)
* È stato risolto un problema che causava la visualizzazione di caselle duplicate (ghost) a causa dell’aggiunta di una casella [!UICONTROL Recommendation Offer] nel Compositore esperienza visivo aggiornato. Il passaggio tra l’Esperienza A e B ha aggiunto ripetutamente più caselle fantasma. (TGT-52505 e TGT-52519)
* È stato risolto un problema nell&#39;interfaccia utente [!DNL Target] aggiornata a causa del quale le modifiche apportate a un&#39;offerta HTML tramite il menu [!UICONTROL Offer] non venivano riportate nell&#39;attività associata e viceversa. Questo comportamento ora corrisponde all&#39;interfaccia utente legacy, in cui gli aggiornamenti vengono sincronizzati correttamente tra il menu [!UICONTROL Offer] e l&#39;attività. (TGT-52540 e TGT-52541)
* È stato risolto un problema a causa del quale gli aggiornamenti recenti di [!UICONTROL Experience Fragments] in [!UICONTROL Offers Library] non venivano rispecchiati durante il tentativo di utilizzarli all&#39;interno di un&#39;attività. (TGT-52659)
* È stato risolto un problema di localizzazione nella traduzione in cinese semplificato di un messaggio di conferma. Nella versione precedente mancavano le virgolette intorno al nome della posizione e utilizzava un linguaggio informale, contrariamente a quanto previsto dalla guida di stile del cliente. La traduzione aggiornata ora utilizza la punteggiatura corretta e un tono formale. (TGT-52364)

## Deprecazione attivazione versione interfaccia utente di Target (23 maggio 2025) {#toggle}

Il rollout della nuova interfaccia utente [!DNL Target] verrà completato entro il **27 maggio 2025**. A questo punto, tutti i clienti avranno accesso all’ultima versione dell’interfaccia utente.

A partire dal **22 giugno 2025**, l&#39;interruttore della versione dell&#39;interfaccia utente verrà rimosso. Tutti gli utenti passeranno in modo permanente alla nuova interfaccia, senza alcuna opzione per tornare alla versione precedente.

### Informazioni importanti sull’interruttore della versione dell’interfaccia utente

È disponibile una funzione temporanea che consente di passare dall&#39;interfaccia utente [!DNL Target] aggiornata alla versione precedente utilizzando un pulsante di attivazione/disattivazione. Questa opzione è disponibile solo durante la fase finale del rollout dell’interfaccia utente.

![Attivazione/disattivazione versione interfaccia utente di Target](/help/main/r-release-notes/assets/toggle.png)

Una volta completato il rollout, l&#39;interruttore verrà rimosso e tutti gli utenti passeranno definitivamente all&#39;interfaccia utente aggiornata il **22 giugno 2025**. Adobe consiglia di pianificare in anticipo, in quanto questa funzione verrà gradualmente eliminata a breve.

### Limitazioni del comportamento di attivazione/disattivazione dell’interfaccia utente

* **Visibilità delle nuove attività**: le attività create nell&#39;interfaccia utente aggiornata non saranno visibili se si torna all&#39;interfaccia precedente.
* **Modifica di attività esistenti**: le modifiche apportate alle attività esistenti (originariamente create nell&#39;interfaccia utente legacy) durante l&#39;utilizzo dell&#39;interfaccia utente aggiornata verranno pubblicate nel sito Web. Tuttavia, se passi all’interfaccia precedente, questi aggiornamenti non saranno visibili; verranno visualizzati solo gli ultimi aggiornamenti effettuati dall’interfaccia precedente.
* **Coerenza dei dettagli dell&#39;attività**: le modifiche più recenti, indipendentemente dall&#39;interfaccia utente utilizzata, verranno applicate al sito Web attivo. Tuttavia, nell’interfaccia utente legacy verranno visualizzate solo le modifiche più recenti apportate all’interno di tale versione. Questo potrebbe causare confusione se le attività modificate nell’interfaccia utente aggiornata hanno un aspetto diverso da quello visualizzato nell’interfaccia utente precedente.

### Ulteriori informazioni sull’interfaccia utente aggiornata

* [[!DNL Target Standard/Premium] 25.2.1 (17 febbraio 2025) - Note sulla versione](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2): fornisce un riepilogo delle modifiche principali apportate all&#39;interfaccia utente in [!DNL Target] per [!UICONTROL Activities], [!UICONTROL Recommendations] e [!UICONTROL Visual Experience Composer] (Compositore esperienza visivo).

* [[!DNL Target Standard/Premium] 25.1.1 (9 gennaio 2025) - Note sulla versione](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-1): fornisce un riepilogo delle modifiche principali apportate all&#39;interfaccia utente in [!DNL Target] per [!UICONTROL Offers Library].

* [Comprendere l&#39;interfaccia utente [!DNL Target] UI](/help/main/c-intro/understand-the-target-ui.md): fornisce una breve panoramica per acquisire familiarità con [!DNL Target] e fornisce collegamenti per informazioni più approfondite e istruzioni dettagliate.

* [[!UICONTROL Visual Experience Composer] modifiche](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md): la versione di [!DNL Adobe Target Standard/Premium] 25.2.1 (17 febbraio 2015) introduce una versione aggiornata di [!UICONTROL Visual Experience Composer] (VEC). Questo articolo spiega le differenze tra le versioni legacy e aggiornata del Compositore esperienza visivo.

* [[!UICONTROL Visual Experience Composer] opzioni](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md): questo articolo illustra l&#39;interfaccia utente del Compositore esperienza visivo aggiornata e le relative opzioni.

## [!DNL Target Standard/Premium] 25.5.3 (22 maggio 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che impediva il corretto funzionamento della funzione di ricerca per nome nell&#39;elenco [!UICONTROL Activities] con query con più parole. (TGT-52529)
* È stato risolto un problema che impediva l&#39;esclusione delle esperienze dalle attività [!UICONTROL Automated Personalization] (AP). (TGT-52383)
* È stato risolto un problema che causava l&#39;assenza dell&#39;opzione &quot;[!UICONTROL Contains]&quot; da [!UICONTROL Filter Rules] durante la gestione del contenuto nelle attività di Personalizzazione automatizzata. (TGT-52384)
* È stata risolta un&#39;incoerenza di reporting nelle attività di [!UICONTROL Automated Personalization] (AP), in particolare per quanto riguarda il modo in cui le offerte predefinite vengono tracciate e segnalate utilizzando i valori `optionLocalId` del sistema interno di [!DNL Target].
* È stato risolto un problema che impediva ai collegamenti di controllo qualità di fornire l’esperienza di attività desiderata. (TGT-52163)
* È stato risolto un problema che impediva agli utenti con autorizzazioni [!UICONTROL Approver] di modificare le attività live in modo errato, ricevendo un messaggio di errore &quot;Accesso negato&quot;. (TGT-52416)
* È stato risolto un problema che impediva la visualizzazione dei perfezionamenti del pubblico per alcune attività nell&#39;interfaccia utente [!DNL Target] aggiornata. (TGT-52057)
* È stato risolto un problema che causava l’inversione dei perfezionamenti del pubblico e dei tipi di pubblico dell’attività nell’interfaccia utente aggiornata. (TGT-52158)
* È stato risolto un problema a causa del quale la generazione di offerte ad hoc generava offerte duplicate. (TGT-51938)
* È stato risolto un problema che bloccava gli aggiornamenti delle offerte e causava la visualizzazione errata di un errore &quot;Utente non valido&quot;. (TGT-52361)
* È stato risolto un problema che impediva il salvataggio delle attività esistenti, causando un errore di tipo &quot;Input utente non valido&quot;. (TGT-52422)
* È stato risolto un problema che impediva la modifica delle offerte HTML esistenti, causando un errore di tipo &quot;Input utente non valido&quot; al momento del salvataggio, anche quando non venivano apportate modifiche al codice. (TGT-52351)
* È stato risolto un problema che impediva a [!DNL Target] di riconoscere il carattere &quot;#&quot; nell&#39;URL di un sito Web. (TGT-52093)
* È stato risolto un problema che impediva la modifica delle attività [!DNL Recommendations] per aggiungere o aggiornare promozioni, causando errori di salvataggio e promozioni duplicate. (TGT-52343)
* È stato risolto un problema che impediva la modifica di criteri o progettazioni nelle attività [!DNL Recommendations], causando un errore &quot;JSON non valido: nome proprietà non riconosciuto&quot;. (TGT-52375)
* È stato risolto un problema che impediva la corretta visualizzazione dei criteri di sequenza nel Compositore esperienza visivo [!UICONTROL Visual Experience Composer] per le attività [!DNL Recommendations]. (TGT-52435)
* È stato risolto un problema che impediva la corretta identificazione delle visualizzazioni nelle pagine di applicazioni a pagina singola quando si utilizzava [!DNL Adobe Experience Platform Web SDK]. (TGT-52106)
* È stato risolto un problema a causa del quale i dettagli di On-Device Decisioning (ODS) non venivano salvati correttamente, nonostante fossero inclusi nel payload dell’operazione batch. (TGT-52406)
* Alle attività è stato aggiunto un campo `audienceMetadata` che consente di leggerlo e aggiornarlo durante la modifica. (TGT-51004)
* È stato aggiunto un messaggio di errore per avvisare gli utenti quando un arco temporale del pubblico non è valido. (TGT52522)
* È stata aggiornata la struttura delle attività per supportare tipi di pubblico duplicati di diversi tipi. (TGT-51200)

## Versione di [!DNL Adobe Target] [!DNL AI Assistant] (16 maggio 2025)

Siamo entusiasti di annunciare il lancio di [!DNL AI Assistant] in [!DNL Adobe Target]. Questa potente funzionalità dell&#39;interfaccia utente è stata progettata per facilitare la navigazione e la comprensione dei concetti di [!DNL Target]. Disponibile in più prodotti in [!DNL Adobe Experience Cloud], tra cui [!DNL Target], [!DNL AI Assistant] è qui per rivoluzionare la tua esperienza.

[!DNL AI Assistant] in [!UICONTROL Target] è uno strumento di conversazione che puoi utilizzare per accelerare i flussi di lavoro con le applicazioni e i servizi [!DNL Experience Platform]. Utilizza [!DNL AI Assistant] per migliorare la tua produttività complessiva e approfondire la tua conoscenza dei prodotti

In [!DNL Target], la prima fase di [!DNL AI Assistant] fornisce informazioni preziose sui prodotti basate sulla documentazione di [!DNL Experience League]. Sono state trattate sia la configurazione di uno script di profilo, la risoluzione di problemi o l&#39;aggiornamento a AEP Web SDK, [!DNL AI Assistant].

Per ulteriori informazioni, vedere [Panoramica dell&#39;Assistente di Adobe Experience Platform AI](/help/main/c-intro/ai-assistant.md).

## [!DNL Target Standard/Premium] 25.5.2 (8 maggio 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* [!DNL Target] utenti con diritti [!UICONTROL Product Administrator] e [!UICONTROL System Administrator] possono ora modificare tutte le impostazioni nelle pagine [!UICONTROL Administration], indipendentemente dal loro ruolo in [!DNL Target]. Gli utenti senza queste autorizzazioni dispongono di accesso in sola lettura a queste impostazioni. Questo aggiornamento garantisce un controllo dell&#39;accesso più rigoroso sulle [impostazioni di amministrazione](/help/main/administrating-target/administrating-target.md). (TGT-48179)
* È stato risolto un problema di caching che impediva il salvataggio dell&#39;attività [Preferenze sito](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#settings). (TGT-52213)
* È stato risolto un problema che impediva ai clienti di abilitare la selezione per ID e classe nella sezione [!UICONTROL Site Preferences] dopo il caricamento del sito nel Compositore esperienza visivo. L&#39;impostazione [!UICONTROL Site Preferences] è stata automaticamente disabilitata anche dopo l&#39;abilitazione. (TGT-52207)
* È stato risolto un problema che impediva a [!UICONTROL Visual Experience Composer] (VEC) di visualizzare la pagina corretta quando [gli URL di consegna della pagina](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#settings) terminavano con una barra (/). (TGT-52237)
* È stato risolto un problema che impediva la rimozione delle modifiche al codice personalizzato durante la modifica delle esperienze. (TGT-52240)
* È stato risolto un problema a causa del quale le modifiche HTML nel Compositore esperienza visivo sovrapponevano gli elementi di pagina esistenti. (TGT-52265)
* È stato risolto un problema che impediva la modifica del codice personalizzato nel Compositore esperienza visivo aggiornato a causa del fatto che il codice personalizzato esistente non era visibile nell’editor. (TGT-52272)
* È stato risolto un problema che causava il messaggio di errore &quot;I nomi duplicati non sono consentiti&quot; durante il salvataggio di un’attività Consigli. (TGT-52318)
* È stato risolto un problema nel Compositore esperienza visivo aggiornato che impediva ai clienti di modificare elementi di testo o rimuovere oggetti contenitore. (TGT-52348)
* È stato risolto un problema che impediva la corretta visualizzazione di [!DNL Customer Journey Analytics] in una pagina attività [!UICONTROL Overview]. (TGT-52359)
* È stato risolto un problema che impediva ai gruppi di reporting di persistere nelle attività [!UICONTROL Automated Personalization] (AP). (TGT-52368)
* È stato risolto un problema che impediva il salvataggio di attività che includevano offer decisioning. (TGT-52390)
* È stato risolto un problema che causava la selezione dell&#39;offerta predefinita ma la visualizzazione di altri contenuti dell&#39;offerta nelle attività [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Multivariate Test] (MVT). (TGT-52372)
* È stata corretta la logica delle autorizzazioni di GET per verificare con OR tra accesso completo all’organizzazione e accesso specifico per organizzazione + utente. (TGT-52374)
* È stato risolto un problema che impediva la visualizzazione dei nomi del pubblico dopo la selezione di un pubblico per [!UICONTROL Managed Content] e [!UICONTROL Reporting Audiences], anche se [!UICONTROL Show Only Selected] era abilitato. (TGT-52393)

## [!DNL Target Standard/Premium] 25.5.1 (5 maggio 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che impediva la visualizzazione di perfezionamenti del pubblico per alcune attività nell’interfaccia utente aggiornata. (TGT-52057)
* È stato risolto un problema che impediva l’utilizzo di tipi di pubblico combinati nelle attività di. (TGT-52346)
* È stato risolto un problema che impediva la creazione di una nuova attività in un’area di lavoro non predefinita utilizzando un pubblico per sola attività dalla stessa area di lavoro. (TGE-52349)
* È stato risolto un problema che causava la scomparsa dei tipi di pubblico per sola attività dall’interfaccia utente aggiornata dopo la creazione e la selezione di un nuovo pubblico. (TGT=52091)
* È stato risolto un problema che impediva l’utilizzo di tipi di pubblico duplicati nelle attività di. (TGT-51200 e TGT-52057)
* È stato risolto un problema che causava l’inversione dei perfezionamenti del pubblico e dei tipi di pubblico dell’attività nell’interfaccia utente aggiornata. (TGT-52158)
* È stato risolto un problema che impediva la creazione di una nuova attività a causa dell’errore di inserimento dell’utente: &quot;area di lavoro non predefinita non consentita per questo utente&quot;. (TGT-52267)
* È stato risolto un problema che impediva la visualizzazione delle offerte nell’interfaccia utente aggiornata per le aree di lavoro predefinite e non predefinite. [!DNL Target] ora visualizza le offerte da entrambe le aree di lavoro. (TGT-52339)
* È stato risolto un problema a causa del quale [!DNL Target] non avvisava i clienti quando modificava un&#39;attività e modificava un elemento del sito Web modificato. (TGT-52100)
* È stato risolto un problema a causa del quale la modifica di un’offerta con offerte ad hoc creava una nuova offerta invece di aggiornare quella esistente. (TGT-52135)
* È stato risolto un problema che causava un errore di payload non valido durante lo spostamento delle offerte nelle cartelle. (TGT-52325)
* È stato risolto un problema che causava un errore di inserimento dell’utente durante lo spostamento delle offerte nelle cartelle. (TGT-52296)
* È stato aggiunto un campo `audienceMetadata` per ogni attività, per assicurarti che venga letto e aggiornato durante la modifica dell&#39;attività. (TGT-51004)

## Note aggiuntive e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js [!DNL Adobe Target]. |

## Modifiche alla documentazione, precedenti note sulla versione e note sulla versione di Experience Cloud

Per informazioni aggiuntive, oltre alle note di ciascuna versione, consulta le seguenti risorse:

| Risorsa | Dettagli |
|--- |--- |
| [Modifiche alla documentazione](/help/main/r-release-notes/doc-change.md) | Consulta le informazioni dettagliate sugli aggiornamenti di questa guida che non sono inclusi nelle presenti note sulla versione. |
| [Note sulla versione per le versioni precedenti](/help/main/r-release-notes/release-notes-for-previous-releases.md). | Informazioni su nuove funzionalità e miglioramenti introdotti nelle versioni precedenti di Target Standard e Target Premium. |
| [Note sulla versione di Adobe Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=it){target=_blank} | Ultime note sulla versione per le soluzioni Adobe Experience Cloud. |

## Informazioni in anteprima {#section_5D588F0415A2435B851A4D0113ACA3A0}

Le risorse seguenti contengono informazioni sulle funzionalità in arrivo con la prossima versione di Target.

| Risorsa | Dettagli |
|--- |--- |
| [Adobe Priority Product Update](https://www.adobe.com/subscription/priority-product-update.html){target=_blank} | Notifiche anticipate sui miglioramenti dei prodotti in arrivo per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud]. |
| [Note sulla versione di Target: prerelease](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informazioni sulle versioni di Target del mese corrente, incluse le informazioni prerelease. |
