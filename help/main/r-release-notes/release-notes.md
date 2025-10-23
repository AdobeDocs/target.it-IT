---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti;aggiornamenti;aggiornamenti correnti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
short-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 7d73870275c266055825c2fce90489ef82825fca
workflow-type: tm+mt
source-wordcount: '1700'
ht-degree: 17%

---

# Note sulla versione (corrente) di [!DNL Target]

Esplora le funzioni, i miglioramenti e le correzioni più recenti in [!DNL Adobe Target]. Queste note sulla versione descrivono anche gli aggiornamenti alle API [!DNL Target], agli SDK, a [!DNL Adobe Experience Platform Web SDK], at.js e ad altri componenti della piattaforma, se applicabili.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## Aggiornamenti urgenti da conoscere {#time-sensitive}

[!BADGE Importante]{type=Informative}

Per gli aggiornamenti sensibili al tempo relativi a [!DNL Adobe Target] e alla tua implementazione, [!DNL Adobe] fornisce note dettagliate sulla versione e documentazione tramite [!UICONTROL Experience League]. Di seguito sono riportate alcune caratteristiche principali relative all’implementazione:

### La versione dell&#39;interfaccia utente [!DNL Target] è deprecata

Per ulteriori informazioni, vedere [[!DNL Target] Domande frequenti sull&#39;aggiornamento dell&#39;interfaccia utente](/help/main/c-intro/updated-ui-faq.md).

## [!DNL Target Standard/Premium] 25.10.1 (22 ottobre 2025)

Questa versione include i seguenti aggiornamenti e correzioni:

**Attività**

+++ Vedi i dettagli
* **È stato risolto un problema di usabilità nell&#39;interfaccia utente aggiornata**. [!UICONTROL Observers] può ora visualizzare in anteprima le attività utilizzando l&#39;opzione [!UICONTROL View Activity], proprio come nell&#39;interfaccia utente legacy. (TGT-51741)
* **[!UICONTROL Observer]utenti possono ora visualizzare il contenuto delle attività nell&#39;interfaccia utente aggiornata.** È stata ripristinata la visibilità per gli utenti del ruolo Osservatore nell&#39;interfaccia utente aggiornata dell&#39;attività. In precedenza, gli osservatori non erano in grado di visualizzare modifiche, offerte e modifiche al contenuto, funzionalità disponibile nell’interfaccia utente legacy. (TGT-53785)
* **[!UICONTROL Approver]utenti possono ora modificare gli obiettivi dell&#39;attività senza l&#39;errore del privilegio dell&#39;editor.** È stato risolto un problema di autorizzazioni nell&#39;interfaccia utente di creazione attività che impediva agli utenti a livello di approvatore di salvare le modifiche alle impostazioni avanzate dell&#39;obiettivo. Gli utenti interessati hanno ricevuto un errore `403 Forbidden.Resource` che richiede i privilegi dell&#39;editor, pur disponendo di un accesso sufficiente. (TGT-53819)

+++

**Tipi di pubblico**

+++Vedi i dettagli
* **Selezione di più tipi di pubblico ripristinata nel reporting &quot;Solo questa attività&quot;.** È stato risolto un problema nell&#39;interfaccia utente di creazione attività che impediva agli utenti di selezionare più tipi di pubblico nella sezione [!UICONTROL This activity only] in [!UICONTROL Goals & Settings]. (TGT-53283)
* **I grafici di reporting basati sul pubblico ora visualizzano correttamente i dati di conversione.** È stato risolto un problema nella scheda [!UICONTROL Reports] che causava errori nei grafici durante la selezione di tipi di pubblico non predefiniti. Anche se i dati e le metriche di affidabilità erano disponibili, il grafico visivo mostrava solo una linea continua, rendendo l’analisi difficile. (TGT-53769)
* **L&#39;interfaccia utente di [!UICONTROL Targeting] ora indica chiaramente le regole per il pubblico escluso.** È stato risolto un problema nella sezione [!UICONTROL Targeting] dell&#39;interfaccia utente di creazione attività in cui le regole del pubblico impostate su [!UICONTROL Exclude] non venivano visualizzate chiaramente. Ciò ha portato a confusione durante la revisione della logica di targeting, in particolare per i tipi di pubblico che escludevano URL specifici. (TGT-53809)
* **I valori di definizione del pubblico ora sono selezionabili e copiabili nella scheda [!UICONTROL Targeting].** È stato risolto un problema nell&#39;interfaccia di Creazione attività che impediva agli utenti di selezionare e copiare i valori delle regole del pubblico nella scheda [!UICONTROL Targeting]. Questa funzionalità era disponibile nell’interfaccia utente legacy ma non nell’interfaccia utente aggiornata. (TGT-53856)

+++

**Localizzazione**

+++Vedi i dettagli
* **Correzione della traduzione errata delle &quot;virgolette&quot; nel contesto dell&#39;editor pagina zh_CN.** È stato corretto un errore di traduzione contestuale nella lingua zh_CN in cui il termine &quot;virgolette&quot; veniva tradotto in modo inesatto come &quot;报价&quot;, implicando un prezzo commerciale. Nella sezione Composizione tipografica > Stile intestazione > Virgolette, il significato desiderato si riferisce a un elemento di formattazione, ovvero un blocco di quotazione, e non alla determinazione dei prezzi. (TGT-53841)
* **Correzione della traduzione errata di &quot;virgolette rimosse&quot; nel contesto dell&#39;editor pagina zh_CN.** È stato corretto un errore di traduzione nella lingua zh_CN in cui &quot;preventivo rimosso&quot; veniva erroneamente visualizzato come &quot;移除了报价&quot;, implicando un prezzo commerciale. Nella sezione Composizione tipografica > Stile intestazione > Citazioni bloccate, il termine si riferisce a un elemento di formattazione, ovvero un blocco di quotazione, e non alla determinazione del prezzo. (TGT-53843)
* **Correzione della traduzione errata di &quot;virgolette ridisposte&quot; nel contesto dell&#39;editor pagina zh_CN.** È stato corretto un errore di traduzione contestuale nelle impostazioni locali zh_CN in cui le &quot;quotazioni riorganizzate&quot; venivano tradotte in modo errato come &quot;重新排列了报价&quot;, implicando un prezzo commerciale. Nella sezione Composizione tipografica > Stile intestazione > Citazioni bloccate, il termine si riferisce a un elemento di formattazione, ovvero un blocco di quotazione, e non alla determinazione del prezzo. (TGT-53844)
* **Corretta traduzione errata delle &quot;virgolette modificate&quot; nel contesto dell&#39;editor pagina zh_CN.** È stato corretto un errore di traduzione nelle impostazioni locali zh_CN in cui &quot;quote changed&quot; veniva visualizzato in modo errato come &quot;更改了报价&quot;, suggerendo un prezzo commerciale. Nella sezione Composizione tipografica > Stile intestazione > Citazioni bloccate, il termine si riferisce a un elemento di formattazione, ovvero un blocco di quotazione, e non alla determinazione del prezzo. (TGT-53845)

+++

**Raccomandazioni**

+++Vedi i dettagli
* **Le modifiche al selettore CSS per i consigli ora vengono salvate correttamente.** È stato risolto un problema nell&#39;interfaccia utente di creazione attività che impediva agli utenti di aggiornare il selettore CSS per i posizionamenti dei consigli. Le modifiche sono state ripristinate dopo il salvataggio, bloccando gli aggiornamenti ai contenitori di targeting. (TGT-53835)
* **La selezione dell&#39;evento di caricamento pagina ora persiste nelle modifiche dei consigli.** È stato risolto un problema nell&#39;interfaccia utente di creazione attività che impediva agli utenti di salvare le modifiche quando si cambiava il tipo di evento di un consiglio da [!UICONTROL View] a [!UICONTROL Page Load]. Anche se la selezione sembrava riuscita, è tornata dopo essere uscita, bloccando la pubblicazione dell’attività. (TGT-53957)

+++

**Rapporti**

+++Vedi i dettagli
* **&quot;[!UICONTROL Export order details to CSV]&quot; ora scarica i dati completi.** È stato risolto un problema nell&#39;interfaccia utente [!UICONTROL Overview] aggiornata che causava il download di file vuoti da parte dell&#39;opzione &quot;[!UICONTROL Export Order details to CSV]&quot;, anche quando erano presenti dati di report validi. (TGT-53787)

+++

**Sicurezza**

+++Vedi i dettagli
* È stato aggiunto **il prefiltro IMS per proteggere gli endpoint GQL dall’esposizione di dati tra organizzazioni diverse.** È stata risolta una vulnerabilità di sicurezza nella scheda Amministrazione che interessava gli endpoint di GraphQL licenseGroups e targetProperties. Il problema è stato causato dall’utilizzo dell’API JIL con un token client amministratore che poteva essere sfruttato per accedere ai dati di prodotto tra organizzazioni diverse. (TGT-53837)

+++

**Compositore esperienza visivo**

+++Vedi i dettagli
* **Stabilità di authoring ripristinata nell&#39;interfaccia utente di creazione attività.** È stato risolto un problema intermittente nell&#39;interfaccia utente del Compositore esperienza visivo che causava errori di authoring e la possibilità di fare clic sui collegamenti in modo imprevisto, reindirizzando gli utenti fuori dalla pagina. (TGT-53153)
* **Modifica ripristinata per le attività salvate nell&#39;interfaccia utente di creazione attività.** È stato risolto un problema che impediva agli utenti di modificare le attività dopo il salvataggio delle modifiche. Le attività interessate sono rimaste bloccate in &quot;[!UICONTROL Applying initial modifications]&quot;, bloccando ulteriori aggiornamenti e nascondendo il pulsante [!UICONTROL Cancel]. (TGT-53631)
* **Il Compositore esperienza visivo non si blocca più su &quot;[!UICONTROL Applying initial modifications]&quot;.** È stato risolto un problema di prestazioni nel Compositore esperienza visivo che causava lunghi ritardi durante il caricamento di esperienze con un numero elevato di modifiche. Gli utenti interessati hanno visto l&#39;interfaccia utente bloccata su &quot;[!UICONTROL Applying initial modifications]&quot; per alcuni minuti, in particolare negli scenari dell&#39;esperienza B. (TGT-53727)
* **Il Compositore esperienza visivo carica le modifiche senza elementi radice.**
È stato risolto un problema nel Compositore esperienza visivo che causava l&#39;arresto delle esperienze durante il caricamento di modifiche prive di un elemento principale chiaro. Queste modifiche in precedenza causavano il blocco indefinito dell&#39;interfaccia utente su &quot;A[!UICONTROL pplying initial modifications]&quot;. (TGT-53799)
* **Il salvataggio delle modifiche nelle attività ora funziona come previsto.** È stato risolto un problema relativo alle autorizzazioni nella nuova interfaccia utente di creazione che impediva agli utenti di salvare le modifiche durante la modifica degli obiettivi e delle impostazioni avanzate nelle attività. Gli utenti interessati hanno visualizzato una barra multifunzione di errore rossa e un messaggio &quot;Forbidden.Resource&quot;, pur disponendo dell’accesso appropriato. (TGT-53816)
* **L&#39;interfaccia utente del Compositore esperienza visivo mantiene le modifiche dell&#39;esperienza in tutte le visualizzazioni.** Sono stati risolti diversi problemi nel Compositore esperienza visivo aggiornato che hanno interessato lo sviluppo dell&#39;esperienza. Le modifiche non persistevano correttamente, soprattutto quando si utilizzavano le offerte HTML o si passava da una visualizzazione all’altra. (TGT-53825)
* **Tutte le visualizzazioni ora vengono visualizzate correttamente quando una modifica si estende su più esperienze.** È stato risolto un problema nell&#39;interfaccia utente di creazione attività in cui veniva visualizzata una sola visualizzazione quando una modifica veniva applicata a più visualizzazioni. La descrizione del passaggio del mouse non elencava tutte le viste associate, anche se la modifica era stata applicata correttamente. (TGT-53827)
* **Il Compositore esperienza visivo non si arresta più in modo intermittente su &quot;[!UICONTROL Applying initial modifications]&quot;.** È stato risolto un problema intermittente nel Compositore esperienza visivo a causa del quale le esperienze non venivano caricate e rimanevano bloccate in &quot;[!UICONTROL Applying initial modifications]&quot;. Questo comportamento era incoerente e talvolta attivava loop di reindirizzamento o richiedeva la cancellazione manuale della cache. (TGT-53916)
* **Impossibile riprodurre il problema di caricamento del Compositore esperienza visivo.** È stato esaminato un problema segnalato in cui il Compositore esperienza visivo rimaneva bloccato su &quot;[!UICONTROL Applying initial modifications]&quot; durante la modifica di attività esistenti. Si sospettava che il comportamento fosse correlato al contenuto HTML privo di un elemento principale. Continueremo a monitorare la ricorrenza e consiglieremo di utilizzare contenitori strutturati per le offerte HTML per garantire la stabilità. (TGT-53972)
* La modalità **[!UICONTROL Design]nel Compositore esperienza visivo non si comporta più come la modalità [!UICONTROL Browse] in modo intermittente.** È stato risolto un problema nell&#39;interfaccia utente in cui la modalità [!UICONTROL Design] si comportava in modo intermittente come la modalità [!UICONTROL Browse], consentendo collegamenti `<a>` cliccabili e impedendo la selezione di elementi. Questo causava la scomparsa della casella di passaggio del mouse e bloccava i flussi di lavoro di modifica. (TGT-53136)
* **I clic del pulsante in modalità [!UICONTROL Composer] non attivano più il reindirizzamento della pagina.** È stato risolto un problema nell&#39;interfaccia utente del Compositore esperienza visivo aggiornata a causa del quale facendo clic su un pulsante in modalità [!UICONTROL Composer] si verificava un reindirizzamento imprevisto all&#39;URL di destinazione del pulsante. Questo impediva agli utenti di modificare elementi di call-to-action (CTA) e interrompeva il flusso di lavoro di authoring. (TGT-53137)
* **Gli aggiornamenti del codice offerta nelle attività di personalizzazione automatizzata ora vengono salvati senza errori.** È stato risolto un problema nella nuova interfaccia utente di creazione che causava un errore &quot;[!UICONTROL Invalid user input]&quot; durante l&#39;aggiornamento del codice offerta nelle attività [!UICONTROL Automated Personalization]. L’errore ha impedito agli utenti di salvare le modifiche, anche quando l’input era valido. (TGT-53586)
* La modalità **[!UICONTROL Design]nel Compositore esperienza visivo ora blocca la navigazione dei collegamenti per i componenti modificabili.** È stato risolto un problema nel Compositore esperienza visivo aggiornato in cui gli elementi cliccabili, come pulsanti e collegamenti, attivavano il reindirizzamento delle pagine anche in modalità [!UICONTROL Design]. Questo comportamento imita la modalità [!UICONTROL Browse] e impedisce agli utenti di modificare i componenti chiave. (TGT-53696)
* La metrica **&quot;[!UICONTROL Clicked an element]&quot; ora funziona senza reindirizzamento o errore.** È stato risolto un problema nella nuova interfaccia utente di creazione che causava reindirizzamenti imprevisti e schermate vuote durante la selezione della metrica di conversione &quot;[!UICONTROL Clicked an element]&quot;. Facendo clic su un pulsante durante l&#39;installazione è stata attivata la navigazione invece di registrare l&#39;elemento, causando un errore &quot;[!UICONTROL element not found]&quot;. (TGT-53817)
* **Le attività esistenti non si bloccano più in un ciclo di caricamento infinito durante la modifica.** È stato risolto un problema nella nuova interfaccia utente di creazione in cui la modifica di un&#39;attività esistente nel Compositore esperienza visivo causava il blocco della pagina in un ciclo di caricamento infinito. Questo problema non ha interessato le attività appena create ed è stato attivato da modifiche preesistenti sulla pagina. (TGT-53913)
* **Le pagine di attività esistenti con modifiche ora vengono caricate correttamente nel Compositore esperienza visivo.** È stato risolto un problema nel Compositore esperienza visivo aggiornato che causava il blocco delle pagine nella fase di caricamento durante la modifica di un&#39;attività esistente con modifiche salvate. Nuove attività caricate senza problema, ma il rendering delle attività configurate in precedenza non è riuscito. (TGT-53967)

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
