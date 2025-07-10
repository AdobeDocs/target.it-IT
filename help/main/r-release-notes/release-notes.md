---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti,aggiornamenti correnti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
short-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 576ec970f572176b28d1b9f050706574e6813b0c
workflow-type: tm+mt
source-wordcount: '2514'
ht-degree: 13%

---

# Note sulla versione (corrente) di [!DNL Target]

Esplora le funzioni, i miglioramenti e le correzioni più recenti in [!DNL Adobe Target]. Queste note sulla versione descrivono anche gli aggiornamenti alle API [!DNL Target], agli SDK, a [!DNL Adobe Experience Platform Web SDK], at.js e ad altri componenti della piattaforma, se applicabili.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## Aggiornamenti urgenti da conoscere {#time-sensitive}

[!BADGE Importante]{type=Informative}

Per aggiornamenti sensibili al tempo relativi a [!DNL Adobe Target] e alla tua implementazione, [!DNL Adobe]fornisce note dettagliate sulla versione e documentazione tramite [!UICONTROL Experience League]. Di seguito sono riportati alcuni punti salienti relativi alla tua implementazione:

### La versione dell&#39;interfaccia utente [!DNL Target] è deprecata

+++Vedi i dettagli
Il team [!DNL Target] offre una funzionalità temporanea che consente di passare dall&#39;interfaccia utente [!DNL Target] aggiornata alla versione precedente utilizzando un pulsante di attivazione/disattivazione. Questa opzione è disponibile solo durante la fase finale del rollout dell’interfaccia utente.

![Attivazione/disattivazione versione interfaccia utente di Target](/help/main/r-release-notes/assets/toggle.png)

Una volta completato il rollout, l’interruttore viene rimosso e tutti gli utenti passano definitivamente all’interfaccia utente aggiornata. [!DNL Adobe] consiglia di pianificare in anticipo, in quanto questa funzione verrà gradualmente eliminata a breve.

#### Timeline obsoleto

A causa dei problemi recenti identificati, principalmente correlati a complesse personalizzazioni dei clienti, il team [!DNL Target] ha regolato la timeline di obsolescenza:

* **17 giugno 2025**: tutte le organizzazioni IMS sono state abilitate per l&#39;interfaccia utente [!DNL Target] aggiornata, per utenti specifici o a livello di organizzazione, per iniziare a testare la nuova esperienza.

* **30 giugno 2025**: l&#39;esperienza [aggiornata [!DNL Target] interfaccia utente](/help/main/c-intro/understand-the-target-ui.md) è diventata predefinita per tutte le organizzazioni IMS che hanno attivato l&#39;interruttore della versione dell&#39;interfaccia utente.

   * Per impostazione predefinita, i clienti che attualmente vedono l’interfaccia utente legacy visualizzano ora l’interfaccia utente aggiornata al momento dell’accesso.
   * L’interruttore della versione dell’interfaccia utente rimane disponibile fino alla fine di luglio e consente agli utenti di tornare indietro se necessario.

  >[!IMPORTANT]
  >
  > [!DNL Adobe] consiglia vivamente di utilizzare l&#39;interfaccia utente [!DNL Target] aggiornata. Torna all&#39;interfaccia utente legacy solo se si verifica un problema di blocco, a causa di [limitazioni del comportamento di attivazione/disattivazione](#limitations).

* **dal 15 luglio al 30 luglio 2025**: l&#39;attivazione/disattivazione della versione dell&#39;interfaccia utente verrà disabilitata in modo permanente in più fasi. Le organizzazioni IMS interessate non sono più in grado di ripristinare l’interfaccia utente legacy.

   * Le eccezioni vengono esaminate caso per caso.
   * I ritardi nell’attivazione/disattivazione dell’impostazione obsoleta vengono concessi solo brevemente (alcuni giorni), mentre i problemi di blocco vengono risolti.

Contatta l&#39;[Assistenza clienti Adobe](/help/main/cmp-resources-and-contact-information.md#/help/main/cmp-resources-and-contact-information.md) per qualsiasi problema o se prevedi problemi durante questa transizione.

#### Limitazioni del comportamento di attivazione/disattivazione dell’interfaccia utente {#limitations}

Le informazioni seguenti descrivono i limiti di cui tenere conto quando si sceglie di utilizzare l’interruttore di versione:

* **Visibilità delle nuove attività**: le attività create nell&#39;interfaccia utente aggiornata non saranno visibili se si torna all&#39;interfaccia precedente.
* **Modifica di attività esistenti**: le modifiche apportate alle attività esistenti (originariamente create nell&#39;interfaccia utente legacy) durante l&#39;utilizzo dell&#39;interfaccia utente aggiornata verranno pubblicate nel sito Web. Tuttavia, se passi all’interfaccia precedente, questi aggiornamenti non saranno visibili; verranno visualizzati solo gli ultimi aggiornamenti effettuati dall’interfaccia precedente.
* **Coerenza dei dettagli dell&#39;attività**: le modifiche più recenti, indipendentemente dall&#39;interfaccia utente utilizzata, verranno applicate al sito Web attivo. Tuttavia, nell’interfaccia utente legacy verranno visualizzate solo le modifiche più recenti apportate all’interno di tale versione. Questo potrebbe causare confusione se le attività modificate nell’interfaccia utente aggiornata hanno un aspetto diverso da quello visualizzato nell’interfaccia utente precedente.

#### Altre risorse sull’interfaccia utente aggiornata

* [[!DNL Target] Domande frequenti sull&#39;aggiornamento dell&#39;interfaccia utente](/help/main/c-intro/updated-ui-faq.md): queste domande frequenti riguardano le domande comuni sulla nuova interfaccia utente [!DNL Target] e sul nuovo Compositore esperienza visivo [!UICONTROL Visual Experience Composer], incluse le modifiche alla navigazione, le posizioni delle funzioni e la rimozione dell&#39;opzione di versione temporanea dell&#39;interfaccia utente. Che tu sia un addetto marketing, uno sviluppatore o un amministratore, queste domande frequenti consentono una transizione fluida e di sfruttare al massimo l’interfaccia utente aggiornata.
* [[!DNL Target Standard/Premium] 25.2.1 (17 febbraio 2025) - Note sulla versione](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2): fornisce un riepilogo delle modifiche principali apportate all&#39;interfaccia utente in [!DNL Target] per [!UICONTROL Activities], [!UICONTROL Recommendations] e [!UICONTROL Visual Experience Composer] (Compositore esperienza visivo).
* [[!DNL Target Standard/Premium] 25.1.1 (9 gennaio 2025) - Note sulla versione](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-1): fornisce un riepilogo delle modifiche principali apportate all&#39;interfaccia utente in [!DNL Target] per [!UICONTROL Offers Library].
* [Comprendere l&#39;interfaccia utente [!DNL Target] UI](/help/main/c-intro/understand-the-target-ui.md): fornisce una breve panoramica per acquisire familiarità con [!DNL Target] e fornisce collegamenti per informazioni più approfondite e istruzioni dettagliate.
* [[!UICONTROL Visual Experience Composer] modifiche](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md): la versione di [!DNL Adobe Target Standard/Premium] 25.2.1 (17 febbraio 2015) introduce una versione aggiornata di [!UICONTROL Visual Experience Composer] (VEC). Questo articolo spiega le differenze tra le versioni legacy e aggiornata del Compositore esperienza visivo.
* [[!UICONTROL Visual Experience Composer] opzioni](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md): questo articolo illustra l&#39;interfaccia utente del Compositore esperienza visivo aggiornata e le relative opzioni.

+++

## [!DNL Target Standard/Premium] 25.7.1 (sabato 11 luglio 2025)

A causa dei problemi recenti identificati, principalmente correlati a complesse personalizzazioni dei clienti, questa versione include le correzioni e gli aggiornamenti seguenti:

**Attività**

+++Consulta i dettagli
* È stato risolto un problema a causa del quale l&#39;URL [!UICONTROL Activity QA] includeva un parametro di query non necessario: `at_preview_evaluate_as_true_audience_ids`. (TGT-52907)
* È stato risolto un problema a causa del quale gli URL di anteprima includevano erroneamente tipi di pubblico aggiuntivi oltre a quello esplicitamente digitato dall’utente. Questo comportamento è stato corretto per garantire che solo il pubblico specificato venga applicato durante la generazione di un collegamento di controllo qualità o di anteprima. (TGT-52912)
* È stato risolto un problema che impediva agli utenti di creare attività [!UICONTROL Auto-Target] (AT) se [!UICONTROL Auto-Allocate] (AA) era selezionato per primo durante la configurazione dell&#39;allocazione del traffico. Questo problema causava un errore di convalida del back-end e impediva il salvataggio dell’attività. (TGT-53096)

+++

**Tipi di pubblico**

+++Consulta i dettagli
* È stato risolto un problema che impediva agli utenti con il ruolo [!UICONTROL Approver] di aggiungere o salvare perfezionamenti del pubblico per sola attività. Il tentativo di eseguire questa operazione ha generato un errore 403 Forbidden, che indica che il privilegio &quot;[editor]&quot; è obbligatorio, anche se l&#39;utente dispone di autorizzazioni sufficienti per approvare e gestire le attività. (TGT-52984)
* È stato risolto un problema che si verificava quando un pubblico specifico per l&#39;attività veniva rimosso utilizzando l&#39;opzione [!UICONTROL Remove Audience Refinement] e il pubblico non veniva più visualizzato nell&#39;elenco dei tipi di pubblico per essere riselezionato all&#39;interno della stessa attività. Questo comportamento impediva agli utenti di aggiungere nuovamente lo stesso pubblico, a meno che non venga ricreato da zero. (TGT-52979)
* È stato risolto un problema a causa del quale i perfezionamenti del pubblico per sola attività scomparivano dall’interfaccia utente subito dopo essere stati rimossi da una posizione, anche prima del salvataggio dell’attività. Questo comportamento contraddiceva le funzionalità previste e le linee guida con la descrizione comando, che recita: &quot;Tutti i tipi di pubblico non utilizzati da questa libreria verranno eliminati una volta salvata l’attività&quot;. (TGT-52982)
* È stato risolto un problema che si verificava durante il tentativo di assegnare un pubblico diverso da [!UICONTROL All Visitors] a un&#39;attività. Al momento del salvataggio, veniva visualizzato il seguente messaggio di errore: &quot;Impossibile completare la richiesta. Se il problema persiste, contatta [!UICONTROL Adobe Client Care].&quot; (TGT-53008)
* È stato risolto un problema che impediva il salvataggio di un’attività dopo la creazione e l’assegnazione di un nuovo pubblico all’interno dell’editor attività. Il messaggio di errore visualizzato era: &quot;Impossibile completare la richiesta. Se il problema persiste, contattare [!UICONTROL Adobe Client Care].&quot; (TGT-52977)

+++

**[!UICONTROL Analytics for Target] (A4T)**

+++Consulta i dettagli
* È stato risolto un problema che causava un errore &quot;Input utente non valido&quot; durante la copia di un&#39;attività esistente e la modifica dell&#39;origine per la generazione di rapporti in [!DNL Adobe Analytics] (A4T). L&#39;errore è stato attivato quando alcune azioni di metrica incompatibili con il reporting di [!DNL Analytics], come `restart_same_experience`, `restart_random_experience` e `restart_new_experience`, sono state mantenute dall&#39;attività originale. (TGT-52900)
* È stato risolto un problema che impediva ai clienti di creare o salvare un&#39;attività selezionando [!DNL Adobe Analytics] (A4T) come origine per la generazione di rapporti nel passaggio [!UICONTROL Goals & Settings]. Il problema si è verificato in modo specifico quando si selezionava una metrica [!UICONTROL Custom Event] (ad esempio, &quot;Evento personalizzato 16&quot;), causando il seguente errore: &quot;Input utente non valido&quot;. (TGT-52910)
* È stato risolto un problema a causa del quale facendo clic sul collegamento &quot;[!UICONTROL View in Analytics]&quot; gli utenti venivano reindirizzati alla home page invece del dashboard [!DNL Analytics] desiderato. (TGT-53092 e TGT-53093)
<!-- * Fixed an issue when cloning an existing activity and changing the reporting source from [!DNL Target] to [!DNL Adobe Analytics], users encounter a "400 - Invalid User Input" error, preventing the activity from being saved. (TGT-52875)
* Fixed an issue when viewing a [!DNL Recommendations] activity in the updated [!UICONTROL Overview] UI, the [!UICONTROL Goals & Settings] section fails to load when [!DNL Adobe Analytics] (A4T) is selected as the reporting source. The following error message was displayed: "Something went wrong. We cannot complete your request. Please contact Adobe Client Care if the problem persists." (TGT-52999)-->

+++

**[!UICONTROL Experiences]e[!UICONTROL Offers]**

+++Vedi i dettagli
<!-- * Fixed an issue where using the [!UICONTROL Manage Content] feature in [!UICONTROL Automated Personalization] (AP) activities caused the page to crash and remain blank. This issue occurred after clicking [!UICONTROL Done] in the content manager, particularly in activities created or edited in the updated UI. (TGT-53047)-->
* È stato risolto un problema che impediva alla funzionalità [!UICONTROL Manage Content] di convalidare correttamente lo stato di una posizione dopo la rimozione di tutte le opzioni di contenuto. Questo poteva causare un comportamento incoerente o errori durante il tentativo di salvare o procedere con la configurazione dell’attività. (TGT-52801)
* È stato risolto un problema che causava la visualizzazione di un errore di tipo &quot;Input non valido&quot; durante l’aggiunta di una nuova pagina e l’eliminazione di elementi specifici in diverse esperienze. L&#39;errore è stato attivato dalla generazione del duplicato `LocalIds` durante la manipolazione dell&#39;elemento, in particolare quando si passa da un&#39;esperienza all&#39;altra e si modificano le strutture di pagina condivise. (TGT-52720)
* È stato risolto un problema che causava la visualizzazione di posizioni non definite nel pannello [!UICONTROL Generate Adhoc Offer] da parte dell&#39;utilizzo della funzione [!UICONTROL Manage Content]. (TGT-53076 e TGT-53070)
* È stato chiarito il comportamento del cliente in cui le modifiche apportate utilizzando un&#39;offerta HTML potrebbero sembrare mancanti quando si torna dal passaggio [!UICONTROL Targeting] a [!UICONTROL Experiences]. Per questo cliente, il sito web interessato ha generato in modo dinamico più selettori DOM modificati a ogni caricamento di pagina. Di conseguenza, il selettore originariamente utilizzato per la modifica non viene trovato quando l’editor viene riaperto, causando la visualizzazione della modifica come mancante o non valida. Questo funziona come previsto. Per garantire che le modifiche persistano visivamente nell’editor, si consiglia ai client di utilizzare selettori stabili e coerenti che non cambiano tra i ricaricamenti delle pagine. (TGT-52874)
* È stato risolto un problema a causa del quale il tentativo di eliminare o disattivare un’offerta che faceva parte di un’esperienza esclusa generava un errore di tipo &quot;Input utente non valido&quot;. Questo problema si verificava anche se l’offerta non veniva utilizzata attivamente nelle esperienze incluse. (TGT-52917)

+++

**Compositore esperienza basato su moduli**

+++Consulta i dettagli
* È stato risolto un problema nelle attività basate su moduli a causa del quale la duplicazione di un’esperienza e la modifica del codice personalizzato in una delle esperienze duplicate applicavano involontariamente tali modifiche a tutte le esperienze duplicate. Dopo la duplicazione, ora ogni esperienza conserva il proprio codice personalizzato in modo indipendente. (TGT-51600)

+++

**Localizzazione**

+++Consulta i dettagli
* È stato risolto un problema di traduzione contestuale nelle impostazioni internazionali coreane (ko-KR) per la stringa &quot;Preview Experience&quot;. (TGT-52928)
* Sono state corrette le incoerenze terminologiche identificate nella traduzione in cinese semplificato (zh_CN) di diverse stringhe di testo. (TGT-52954 e TGT-52955)

+++

**[!DNL Recommendations]**

+++Consulta i dettagli
* È stato aggiunto un nuovo feed [!DNL Recommendations] [status](/help/main/c-recommendations/c-products/feeds.md#status): [!UICONTROL Partial Import Failed]. (KB-2215)
* È stato risolto un problema che interessava il flusso di lavoro di creazione attività durante l&#39;aggiunta di [!DNL Recommendations] con [!UICONTROL promotions]. Quando gli utenti hanno selezionato &quot;[!UICONTROL Promote by Attribute]&quot; e aggiunto una regola di filtro (ad esempio, [!UICONTROL Parameter Matching]), il tipo di regola e i valori dell&#39;operando selezionati non sono stati mantenuti dopo il salvataggio e la modifica dell&#39;attività. Alla riapertura, il tipo di regola di filtro cambiava in modo imprevisto e mancavano i valori dell’operando. (TGT-53059)
* È stato risolto un problema nell&#39;interfaccia utente [!DNL Recommendations] a causa del quale qualsiasi promozione creata con una singola regola veniva erroneamente interpretata e visualizzata come un tipo di promozione &quot;Elenco di elementi&quot;, indipendentemente dalla logica della regola. (TGT-53063)
* È stato risolto un problema che si verificava durante l&#39;utilizzo dell&#39;interfaccia utente [!UICONTROL Overview] aggiornata. Il pulsante &quot;[!UICONTROL Download Recommendations Data]&quot; era mancante per le attività [!UICONTROL Experience Targeting] (XT) che includono [!DNL Recommendations]. (TGT-52730 e TGT-52756)
* In precedenza, nell’interfaccia utente Consigli veniva visualizzato solo il numero di entità importate correttamente da un feed. Tuttavia, il formato del messaggio di back-end include sia il numero di entità importate che il numero totale di entità nel formato: `# of entities imported / # of total entities`. A causa di questa discrepanza, gli utenti visualizzavano solo il primo valore (conteggio importato) nell’interfaccia utente, creando confusione. Ora l’interfaccia utente visualizza entrambi i numeri. (TGT-53073)

+++

**Rapporti**

+++Consulta i dettagli
* È stato risolto un problema che causava il download di un file vuoto durante la selezione di &quot;[!UICONTROL Export order details to CSV]&quot; dalla pagina [!UICONTROL Reports]. Questo problema si verificava anche quando nell’attività erano presenti dati di ordine validi. (TGT-52225)
* È stato risolto un problema che si verificava durante il tentativo di salvare un’attività dopo la creazione e l’assegnazione di un nuovo pubblico di reportistica. Il messaggio di errore restituito era: &quot;Accesso negato. Per eseguire questa operazione, sono necessari tutti i privilegi seguenti: [editor].&quot; Questo problema si verificava nonostante l’utente avesse accesso a livello di approvatore. (TGT-53103)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++Consulta i dettagli
* È stato risolto un problema a causa del quale l’applicazione di una modifica a una vista determinava la duplicazione della vista e l’attività restituiva un errore di tipo &quot;Input utente non valido&quot;. Questa correzione assicura che le modifiche della visualizzazione vengano applicate correttamente senza causare errori di duplicazione o convalida. (TGT-52886)
* È stato risolto un problema che impediva la corretta visualizzazione delle modifiche al codice personalizzato in caso di esperienza errata. In particolare, le modifiche progettate per un’esperienza sono state mostrate in un’esperienza diversa, generando confusione e potenziale configurazione errata delle attività live. (TGT-52776)
* È stato risolto un problema che impediva la modifica o il salvataggio delle modifiche del codice personalizzato nella nuova interfaccia utente del Compositore esperienza visivo. In particolare:

   * Dopo aver modificato un blocco di codice personalizzato e aver salvato, le modifiche non venivano riportate nell’interfaccia utente o nell’anteprima Controllo qualità.
   * In alcuni casi, non è stato possibile eliminare le modifiche a meno che l’attività non sia stata chiusa e riaperta.
   * Come soluzione alternativa, gli utenti dovevano copiare il codice, eliminare la modifica e ricrearla manualmente con il contenuto aggiornato. (TGT-53072)

* È stato risolto un problema che causava la mancata risposta del pannello [!UICONTROL Modifications] a causa della modifica e del salvataggio del codice personalizzato. (TGT-53075)
* È stato risolto un problema a causa del quale le modifiche apportate al codice personalizzato nelle esperienze di varianti venivano applicate involontariamente all&#39;esperienza [!UICONTROL Control]. Questo causava modifiche non intenzionali nel comportamento di consegna. L&#39;esperienza [!UICONTROL Control] ora rimane isolata dalle modifiche al codice personalizzato apportate ad altre esperienze. (TGT-52413)
* È stato risolto un problema a causa del quale le modifiche apportate a un’esperienza (ad esempio, Esperienza B) venivano duplicate involontariamente a un’altra esperienza (Esperienza A) se l’utente faceva clic sulla seconda esperienza prima del caricamento completo dell’editor. Questo comportamento potrebbe anche causare la perdita di modifiche se l’esperienza selezionata inizialmente non avesse subito modifiche. (TGT-52597)
* È stato risolto un problema per cui le modifiche apportate nel passaggio [!UICONTROL Modifications] della creazione dell&#39;attività non venivano salvate in modo coerente. In alcuni casi, dopo aver completato tutti i passaggi e aver fatto clic su [!UICONTROL Save], lo script personalizzato aggiunto nella sezione [!UICONTROL Modifications] non si rifletterebbe sul sito live, nonostante nessun errore visibile durante il processo di salvataggio. (TGT-52661)
* È stato risolto un problema a causa del quale le modifiche al codice personalizzato non venivano salvate correttamente e venivano involontariamente applicate a più esperienze all’interno della stessa attività. Inoltre, si sono verificati problemi di accesso all’apertura o all’aggiornamento di alcune attività, con la conseguente visualizzazione di schermate vuote. Questi problemi sono stati risolti per garantire una modifica stabile delle attività e un isolamento accurato delle esperienze. (TGT-52594)
* È stato risolto un problema che impediva agli utenti di passare a un URL diverso in [!UICONTROL Browse Mode]. Ciò impediva ai tester e agli editor di convalidare o visualizzare in anteprima pagine alternative all’interno della stessa sessione di attività. (TGT-53052)
* È stato risolto un problema che causava l&#39;apertura simultanea di più istanze di [!UICONTROL Visual Experience Composer] (VEC) durante la creazione dell&#39;attività. Questo problema si verificava quando gli utenti disabilitavano [!UICONTROL Enhanced Experience Composer] (EEC) e rimuovevano la barra finale dall&#39;URL del sito Web nel passaggio [!UICONTROL Page Delivery]. (TGT-52782)
* È stato risolto un problema a causa del quale il menu a discesa della metrica [!UICONTROL Revenue] nel passaggio [!UICONTROL Goals & Settings] impostava erroneamente il valore predefinito [!UICONTROL Revenue per Visit] (RPVISIT), anche dopo che l&#39;utente aveva selezionato una metrica diversa.  si è verificato un problema durante la compressione e la nuova espansione del pannello di configurazione della metrica, causando il ripristino del valore selezionato in precedenza. (TGT-52811 e TGT-52878)
* Sono stati risolti diversi problemi nel flusso di lavoro di creazione attività relativi alla denominazione delle offerte e alla traduzione dei contenuti in [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Multivariate Testing] (MVT) attività:

  Problemi chiave risolti:

   * La creazione di più offerte HTML con lo stesso nome (ad esempio, &quot;Esperienza&quot;) ha attivato l’errore &quot;I nomi di offerta duplicati non sono consentiti&quot;, ma l’interfaccia utente non indicava chiaramente quali offerte causavano il conflitto.
   * La ridenominazione delle offerte tramite il pannello di destra ha aggiornato il nome nell&#39;interfaccia utente, ma la modifica non è stata riportata nella scheda [!UICONTROL Manage Content] o nella scheda [!UICONTROL Offers], causando errori di convalida persistenti.
   * Nelle attività MVT, anche se l’errore di nome duplicato non persisteva dopo la ridenominazione, l’interfaccia utente non riusciva ancora a riflettere i nomi delle offerte aggiornati in modo coerente tra le schede. (TGT-52933)

+++

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
