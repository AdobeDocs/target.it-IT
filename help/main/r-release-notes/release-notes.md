---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti,aggiornamenti correnti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
short-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 579ebd9bebd3faa724f0d1d542f4d23766adefe3
workflow-type: tm+mt
source-wordcount: '1677'
ht-degree: 24%

---

# Note sulla versione (corrente) di [!DNL Target]

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione di API di [!DNL Target], SDK, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target Standard/Premium] 25.4.5 (25 aprile 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che causava discrepanze nelle inserzioni del pubblico tra la pagina delle impostazioni [!UICONTROL Activity] e la pagina della panoramica [!UICONTROL Reporting]. (TGT-52203)
* È stato risolto un problema che impediva l’aggiunta di una nuova pagina a un’attività a causa di un errore di input dell’utente non valido. (TGT-52263)
* È stato risolto un problema che causava l&#39;incremento errato di `OptionLocalIDs` quando l&#39;opzione rimaneva invariata. (TGT-52187)
* È stato risolto un problema che causava l&#39;incremento errato di `location` e `OptionLocalIDs` quando l&#39;opzione rimaneva invariata. (TGT-52188)
* È stato risolto un problema che causava un errore nella posizione della pagina [!UICONTROL Overview] dell&#39;attività. (TGT-52182)
* È stato risolto un problema che impediva la visualizzazione di un avviso di selezione non valido per una posizione non valida. (TGT-52110)
* È stato risolto un problema a causa del quale i file di reporting scaricati mostravano correttamente i dati presenti nell’interfaccia utente di reporting. (TGT-52068)
* È stato risolto un problema che impediva il corretto funzionamento delle operazioni batch dopo l’aggiunta delle regole di consegna della pagina. (TGT-52097)
* È stato risolto un problema a causa del quale [!DNL Target] eliminava tutti i parametri di query dall&#39;URL del sito Web. (TGT-52100)
* È stato risolto un errore della console che impediva ai clienti di creare attività nell&#39;interfaccia utente [!DNL Target] legacy e aggiornata. (TGT-52181)
* È stato risolto un problema che impediva ai clienti di aggiungere nuove pagine, causando un errore di input dell’utente non valido. (TGT-52258)
* È stato risolto un problema che causava la scomparsa delle modifiche dopo l&#39;aggiunta di ulteriori pagine e il ritorno alla scheda [!UICONTROL Experiences]. (TGT-52264)
* È stato risolto un problema che impediva ai clienti di modificare il pubblico in un&#39;attività [!UICONTROL Experience Targeting] (XT). (TGT-52191)
* È stato corretto un errore che impediva la modifica di un’attività XT a causa di una regola dell’interfaccia utente non supportata. (TGT-52273)
* È stato risolto un problema nel [!UICONTROL Visual Experience Composer] (VEC) aggiornato a causa del quale le breadcrumb non venivano sempre visualizzate nella parte inferiore dell’editor, causando difficoltà nella selezione precisa degli elementi. (TGT-52169)
* È stato risolto un problema che impediva all&#39;elenco a discesa [!UICONTROL Audience] di visualizzare tutti i tipi di pubblico a causa dell&#39;impaginazione. (TGT-52204)
* È stato risolto un problema che causava un messaggio di input utente non valido durante l&#39;aggiunta di nuove offerte nelle attività [!UICONTROL Automated Personalization] (AP). (TGT-52210)
* È stato risolto un problema a causa del quale [!UICONTROL Analytics for Target] (A4T) veniva erroneamente selezionato come origine per la generazione di rapporti, anche se il cliente non aveva accesso ad A4T. (TGT-52226)
* È stato risolto un problema che impediva il salvataggio di un&#39;attività con la metrica URL [!UICONTROL View a Page]. (TGT-52260)
* È stato risolto un problema che impediva ai clienti di selezionare aree di lavoro durante la creazione di offerte all’interno di un’attività. (TGT-52289)
* È stato risolto un problema che impediva ai clienti di creare attività in tutte le aree di lavoro. (Tgt-52218)
* È stato risolto un problema che causava la visualizzazione errata delle modifiche da un’esperienza quando si passava a un’altra. (TGT-52184)
* È stato risolto un problema che impediva la corretta visualizzazione dell&#39;offerta predefinita nell&#39;interfaccia utente [!DNL Target] all&#39;apertura dell&#39;attività. (TGT-52198)

## Aggiornamento delle autorizzazioni di Target (22 aprile 2025)

Questo aggiornamento futuro migliora il controllo dell&#39;organizzazione sulle configurazioni delle istanze [!DNL Target], impedendo aggiornamenti accidentali che potrebbero influire sulla distribuzione delle attività tra i vari team di test e personalizzazione.

A decorrere dal 22 aprile 2025, solo gli amministratori [!UICONTROL Product] e [!UICONTROL Solutions] potranno aggiornare le impostazioni nelle sezioni [!UICONTROL Administration], indipendentemente dai loro ruoli nelle aree di lavoro [!DNL Target]. Gli utenti senza questa autorizzazione avranno accesso in sola lettura alle sezioni [!UICONTROL Administration].

Per ulteriori informazioni, vedere [Amministrare Target](/help/main/administrating-target/start-target.md).

## [!DNL Target Standard/Premium] 25.4.4 (17 aprile 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato aggiunto un messaggio di errore per guidare gli utenti nella risoluzione delle opzioni duplicate in un’attività. (TGT-51927)
* È stato risolto un problema che impediva la rimozione di `ClickTrack` selettori durante l&#39;eliminazione di pagine o esperienze con offerte di reindirizzamento. (TGT-51952)
* È stato risolto un problema che causava l&#39;autorizzazione di selettori `ClickTrack` vuoti. [!DNL Target] ora richiede che il campo del selettore non sia vuoto. (TGT-52107)
* È stato risolto un problema che consentiva erroneamente le metriche con nomi duplicati. Le metriche ora richiedono nomi univoci. (TGT-52201)
* È stato risolto un problema a causa del quale le definizioni dei tipi di pubblico non erano visibili durante la modifica del targeting a livello di offerta nelle attività [!UICONTROL Automated Personalization] (AP). (TGT-52148)
* È stato risolto un problema che impediva ai clienti con diritti [!UICONTROL Editor] di salvare le attività. (TGT-52227)
* `OptionLocalIDs` non incrementa più in modo errato quando l&#39;opzione rimane invariata. (TGT-52139)
* È stato risolto un problema che causava un messaggio &quot;Non valido `optionLocalIds`&quot; durante il tentativo di creare un&#39;attività. (TGT-52154)
* Sono state corrette le discrepanze tra `OptionLocalIDs` definiti per un&#39;attività e quelli utilizzati per definire le esperienze. (TGT-52215)
* È stato risolto un problema che causava un errore di convalida durante il tentativo di creazione di un’attività A/B. (TGT-51923)

## [!DNL Target Standard/Premium] 25.4.3 (11 aprile 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato corretto un errore che impediva ai clienti di aprire il pop-up di informazioni sul pubblico per alcune attività [!UICONTROL Experience Targeting] (XT). (TGT-52049)
* È stato risolto un problema che causava il ripristino dell&#39;impostazione del pubblico su &quot;[!UICONTROL All Visitors]&quot; a seguito delle modifiche apportate in [!UICONTROL Visual Experience Composer] (VEC). (TGT-52132)
* È stato risolto un problema che impediva la visualizzazione di perfezionamenti del pubblico per attività specifiche (TGT-52057)
* È stato risolto un problema che impediva ai clienti di inserire un [!UICONTROL Experience Fragment] nell&#39;area di lavoro predefinita. (TGT-52073)
* È stato risolto un problema che causava la visualizzazione di un&#39;offerta come &quot;Contenuto non trovato&quot; e non sulla pagina [!UICONTROL Offers] per un&#39;attività [!UICONTROL Automated Personalization] (AP). (TGT-52150)
* È stata aggiunta la possibilità di consentire la duplicazione dei tipi di pubblico all’interno di un’attività. (TGT-51200)
* È stato risolto un problema che causava la visualizzazione del nome mbox errato nella pagina [!UICONTROL Goals & Settings] per un&#39;attività XT dopo la modifica. (TGT-52026)
* È stato risolto un problema che causava la visualizzazione di `defaultContent` nelle opzioni nonostante non fosse in `experiences/optionLocations`. (TGT-52036)
* È stato risolto un problema per garantire che le stringhe vuote non vengano convertite in valori Null. (TGT-52037)
* È stato risolto un problema che richiedeva ai clienti di riconfigurare [!UICONTROL Optimization Goal] in [!UICONTROL Reporting Settings] nella pagina [!UICONTROL Goals & Settings] dopo le modifiche. (TGT-52071)
* È stato risolto un problema a causa del quale un&#39;attività senza regole di consegna pagina visualizzava più regole sulla pagina [!UICONTROL Overview]. (TGT-52084)
* È stato aggiunto un messaggio di errore per gli utenti che tentano di salvare un’offerta con caratteri al di fuori del piano multilingue di base, ad esempio emoji. (TGT-52105)
* È stato risolto un problema a causa del quale l’apertura di un’attività attivava il messaggio di errore: &quot;Questa attività utilizza uno o più tipi di pubblico eliminati alla sorgente&quot;. (TGT-52120)
* È stato risolto un problema che impediva la visualizzazione delle metriche ClickTrack nel Compositore esperienza visivo [!UICONTROL Visual Experience Composer] aggiornato durante la modifica. (TGT-52152)
* È stato risolto un problema a causa del quale un URL con un parametro di query come posizione dell&#39;attività non visualizzava il parametro di query nella pagina [!UICONTROL Overview] dell&#39;attività. (TGT-51635)
* È stato risolto un problema che impediva la visualizzazione dell&#39;intero URL dell&#39;esperienza in [!UICONTROL Browse mode] all&#39;interno del [!UICONTROL Visual Experience Composer] (VEC). (TGT-52101)
* È stato risolto un problema a causa del quale la modifica di un’attività causava l’aggiunta di &quot;/&quot; alla fine dell’URL da parte della consegna della pagina, che ne causava l’invalidità. (TGT-52114)
* È stato risolto un problema che causava il reindirizzamento errato del collegamento [!UICONTROL Activity QA] nella home page di [!UICONTROL Form-Based Experience Composer] alla home page di [!DNL Adobe Experience Cloud]. (TGT-52055)
* È stato risolto un problema che impediva il mantenimento delle pagine aggiuntive aggiunte all&#39;attività [!UICONTROL A/B Test] dopo il salvataggio e la riapertura. (TGT-51994)
* È stato risolto un problema che impediva ai clienti di eliminare gli stili nella sezione stile in linea. (TGT-52070)
* È stato ripristinato l&#39;accesso alle [schede di definizione del pubblico](/help/main/c-target/c-audiences/audiences.md#section_11B9C4A777E14D36BA1E925021945780) nella finestra di dialogo [!UICONTROL Activity QA], in modo simile all&#39;interfaccia utente legacy. (TGT-52056)
* L’interfaccia utente aggiornata non salvava pagine o tipi di pubblico senza modifiche. Se i clienti hanno aggiunto nuove pagine o tipi di pubblico a un&#39;attività ma non vi apportano modifiche, [!DNL Target] ha eliminato i tipi di pubblico non modificati al momento del salvataggio. Le notifiche sono state aggiunte in posizioni rilevanti per informare gli utenti di questo comportamento. (TGT-52104)

## [!DNL Target Standard/Premium] 25.4.1 (2 aprile 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che causava la scomparsa dei tipi di pubblico dell’esperienza dalle attività di. (TGT-52003)
* È stato risolto un problema che causava elementi imprevisti durante la consegna. (TGT-52011)
* È stato risolto un problema che impediva ai clienti di visualizzare il pubblico nel grafico di targeting nella pagina Ove[!UICONTROL r]view e durante la modifica dell&#39;attività. (TGT-52050)
* È stato risolto un problema che impediva ai clienti di riordinare le esperienze in ordine di priorità nelle attività [!UICONTROL Experience Targeting] (XT). (TGT-52054)
* È stato risolto un problema che causava un rendering errato quando si annullavano le modifiche allo stile del testo. (TGT-51876)
* È stato risolto un problema a causa del quale durante la modifica di un&#39;offerta di reindirizzamento, [!DNL Target] rimuove anche i selettori [!UICONTROL ClickTrack] associati a tale offerta. (TGT-51936)
* È stato risolto un problema che causava il salvataggio errato del selettore da parte di [!DNL Target] durante l&#39;annullamento di [!UICONTROL ClickTrack]. (TGT-51937)
* È stato risolto un problema che causava un errore di nome non valido dopo l&#39;apertura e la chiusura del selettore mbox sulla pagina [!UICONTROL Goals & Settings] senza apportare modifiche. (TGT-51983)
* È stato risolto un problema che impediva la modifica delle offerte ad hoc create nell&#39;interfaccia utente legacy di [!DNL Target]. (TGT-51984)
* È stato risolto un problema che bloccava le attività di modifica con offerte ad hoc contenenti codice personalizzato. (TGT-51995)
* È stato risolto un problema che causava la visualizzazione delle regole di esclusione come regole di inclusione durante la modifica delle definizioni di pubblico combinato. (TGT-51999)
* È stato risolto un problema che impediva la corretta visualizzazione del codice personalizzato durante la modifica dell’esperienza. (TGT-52005)
* È stato risolto un problema che rendeva l&#39;opzione [!UICONTROL Insert Before] non disponibile per l&#39;inserimento di contenuto prima della barra di navigazione. (TGT-52031)
* È stato risolto un problema che impediva la corretta evidenziazione dell’esperienza predefinita nel reporting. (TGT-51716)
* È stato risolto un problema che attivava un messaggio `default message [Invalid optionLocalIds: xx]]` durante la creazione di un&#39;attività. (TGT-52038)

## at.js versione 2.11.8 (31 marzo 2025)

* È stata risolta una vulnerabilità identificata da CodeQL nella convalida del suffisso di stringa per evitare casi edge durante le operazioni di ridimensionamento e spostamento. (TNT-51516)

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
