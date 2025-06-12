---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti,aggiornamenti correnti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
short-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 1d72a708ce68d34a603f750010caa4eb68290f7a
workflow-type: tm+mt
source-wordcount: '1701'
ht-degree: 21%

---

# Note sulla versione (corrente) di [!DNL Target]

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione di API di [!DNL Target], SDK, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target Standard/Premium] 25.6.2 (venerdì 12 giugno 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato aggiunto un [nuovo articolo di domande frequenti](/help/main/c-intro/updated-ui-faq.md) per risolvere le domande comuni sull&#39;interfaccia utente [!DNL Target] e sul Compositore esperienza visivo aggiornati di [!UICONTROL Visual Experience Composer].
* È stato risolto un problema che impediva il funzionamento della regola &quot;[!UICONTROL URL - does not contain]&quot; in [!UICONTROL Page Delivery], consentendo la visualizzazione del contenuto anche quando avrebbe dovuto essere bloccato. (TGT-52754)
* È stato risolto un problema che impediva a [!UICONTROL Page Delivery] di visualizzare correttamente il messaggio di errore: &quot;Non sono consentiti URL di pagina duplicati. (TGT-52765)
* È stato risolto un problema a causa del quale i tipi di pubblico per [!UICONTROL Page Delivery] URL contenenti frammenti di esperienza venivano creati con # erroneamente aggiunto. (TGT-52786)
* È stato risolto un problema che causava la mancata risposta dell&#39;interfaccia utente di [!DNL Target] a causa della copia di un&#39;attività e della modifica delle impostazioni nella pagina [!UICONTROL Goals and Settings]. (TGT-52797)
* È stato risolto un problema nel Compositore esperienza visivo [!UICONTROL Visual Experience Composer] aggiornato che consentiva erroneamente il reindirizzamento di una pagina aggiuntiva in un&#39;attività [!UICONTROL A/B Test] allo stesso URL. (TGT-51838)
* È stato risolto un problema che impediva il salvataggio delle modifiche alle metriche nella pagina [!UICONTROL Goals and Settings] durante la modifica di un&#39;attività. (TGT-52799)
* È stato risolto un problema a causa del quale l’aggiunta di una nuova esperienza durante il caricamento dell’editor web causava la duplicazione del contenuto dell’esperienza precedente. (TGT-51397)
* È stata ripristinata la possibilità di utilizzare codice personalizzato all&#39;esterno del tag `<head>`, una funzione precedentemente disponibile nell&#39;interfaccia utente di Target precedente. (TGT-52304 e TGT-52300)
* È stata rimossa la convalida non necessaria durante la selezione dell’area di lavoro predefinita durante la creazione dell’attività. La convalida obbligatoria delle proprietà non si applica più all’area di lavoro predefinita, ma rimane attiva per le aree di lavoro non predefinite. (TGT-52449)
* È stato risolto un problema nel Compositore esperienza visivo [!UICONTROL Visual Experience Composer] aggiornato a causa del quale non venivano rilevate `triggerView()` chiamate. (TGT-52575)
* È stato risolto un problema nel Compositore esperienza visivo [!UICONTROL Visual Experience Composer] aggiornato che impediva agli utenti di aggiungere modifiche alle visualizzazioni di [!UICONTROL Single Page Application] (SPA). (TGT-52556)
* È stato risolto un problema nell&#39;interfaccia utente [!DNL Target] aggiornata che impediva ai clienti di visualizzare i dettagli delle offerte. (TGT-52607)
* È stato risolto un problema che impediva agli aggiornamenti apportati alle offerte in [!UICONTROL Offers Library] di trovarsi nel [!UICONTROL Visual Experience Composer] (Compositore esperienza visivo) aggiornato. (TGT-52637)
* È stato risolto un problema che impediva la corretta visualizzazione della sezione Offerte durante la creazione di un’attività. (TGT-52773)
* È stata aggiunta la convalida per garantire che tutti i `optionLocalIds` a cui si fa riferimento in `optionGroups` siano presenti nell&#39;array delle opzioni. I riferimenti non validi vengono rimossi automaticamente durante la creazione dell’attività. (TGT-52687)
* È stato risolto un problema a causa del quale i gruppi di reporting e le esclusioni non venivano mantenuti dopo l’aggiunta di una nuova offerta. (TGT-52728)
* È stato risolto un problema che causava la visualizzazione di un selettore di opzioni vuoto nelle attività senza un pulsante [!UICONTROL Activity QA]. (TGT-52733)
* È stato risolto un problema che impediva il corretto rendering del contenuto dei collegamenti di controllo qualità. (TGT-52718)
* È stato risolto un problema a causa del quale la sostituzione di un elemento con un frammento di esperienza non rifletteva correttamente le modifiche nell’ambiente di controllo qualità. (TGT-52762)
* È stato risolto un problema nel Compositore esperienza visivo [!UICONTROL Visual Experience Composer] aggiornato che causava un errore di tipo &quot;Input non valido&quot; quando gli utenti tentavano di aggiungere frammenti di esperienza. (TGT-52701)
* È stato risolto un problema che causava la visualizzazione del modale &quot;Modifica pubblico&quot; vuoto durante la modifica del targeting del pubblico nel [!UICONTROL Visual Experience Composer] (VEC) aggiornato. (TGT-52749)
* È stato aggiunto un messaggio per informare gli utenti quando un’entità non è accessibile nell’area di lavoro selezionata. (TGT-52767)
* È stato risolto un problema che impediva all’interfaccia utente di consentire l’assegnazione manuale di un ID ambiente a un criterio. Viene invece utilizzato l&#39;ID predefinito per il gruppo host [!UICONTROL Product Catalog Search]. Questa correzione assicura che le modifiche ai criteri vengano ora applicate in tutti gli ambienti, non solo a quello predefinito. (TGT-52817)
* È stato risolto un problema che causava l&#39;assenza dell&#39;opzione &quot;[!UICONTROL Download Recommendations data]&quot; per le attività [!UICONTROL Experience Targeting] (XT) con consigli. (TGT-52730 e TGT-52756)



## [!DNL Target Standard/Premium] 25.6.1 (sabato 6 giugno 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema a causa del quale i collegamenti di controllo qualità non fornivano l’esperienza corretta per l’attività associata. (TGT-52163 e TGT-52790)
* È stato risolto un problema che causava la mancanza dell’ID del pubblico associato nei collegamenti di controllo qualità. (TGT-52722)
* È stato risolto un problema per garantire che le esperienze vengano consegnate solo quando le condizioni URL di consegna pagina configurate vengono soddisfatte con precisione. (TGT-52696)
* È stato risolto un problema che impediva ai clienti di creare un modello struttura [!DNL Recommendations]. Il tentativo di creare un modello ha attivato l’errore: &quot;Deve essere utilizzata almeno 1 variabile di entità nello script&quot;. (TGT-52395)
* È stato risolto un problema che impediva il salvataggio delle progettazioni di [!DNL Recommendations] tramite gli array Velocity. Il messaggio di errore &quot;Deve essere utilizzata almeno 1 variabile di entità nello script&quot; è stato attivato in modo errato. (TGT-52734)
* È stato risolto un problema che impediva l&#39;accesso alle modifiche nel [!UICONTROL Visual Experience Composer] (VEC) quando non era possibile caricare la pagina per le pagine Web interne. (TGT-52488 &amp;TGT-52470)
* È stato risolto un problema che impediva la visualizzazione del pannello [!UICONTROL Modifications] nel Compositore esperienza visivo con schermi di dimensioni inferiori. (TGT-52470)
* È stato risolto un problema nel Compositore esperienza visivo aggiornato a causa del quale il passaggio dalla modalità [!UICONTROL Browse] alla modalità [!UICONTROL Design] causava un errore della console e impediva ulteriori interazioni. (TGT-52532)
* È stato risolto un problema nel Compositore esperienza visivo a causa del quale, facendo clic su alcuni elementi, le dimensioni venivano involontariamente estese. (TGT-52497)
* È stato risolto un problema che impediva il caricamento o il riconoscimento di alcuni elementi di pagina nel Compositore esperienza visivo, impedendo interazioni quali la selezione di pulsanti o banner e l’interruzione del tracciamento accurato degli eventi nelle attività. (TGT-52663)
* È stato risolto un problema che impediva ai clienti di eliminare o rimuovere le offerte nelle attività [!UICONTROL Automated Personalization] (AP). (TGT-52690)
* È stato risolto un problema che causava un comportamento incoerente di qualificazione delle attività nelle attività multipagina. (TGT-52694)
* È stato risolto un problema che causava la visualizzazione di un URL non valido per la pagina [!UICONTROL Overview] dell&#39;attività. [!UICONTROL Activity Location] (TGT-52695)
* È stato risolto un problema nell&#39;interfaccia utente [!DNL Target] aggiornata che causava la visualizzazione di voci duplicate per i percorsi attività. (TGT-52693)
* È stato risolto un problema che attivava un errore `getAudiencesV3`, impedendo ai clienti di modificare o copiare le attività. (TGT-52709)
* È stato risolto un problema che causava un errore di payload non valido durante l&#39;aggiunta di [!UICONTROL Experience Fragments] o offerte HTML a un&#39;attività. (TGT-52779 e TGT-52773)
* È stato risolto un problema nell&#39;interfaccia utente [!DNL Target] aggiornata a causa del quale E[!UICONTROL xperience Fragments] non veniva visualizzato correttamente a causa di un errore di input non valido. (TGT-52701)
* È stato risolto un problema che impediva ai clienti di modificare le attività in [!UICONTROL Form-based Experience Composer] a causa di un errore utente non valido. (TGT-52470)
* È stato risolto un problema di localizzazione nella lingua coreana a causa del quale le traduzioni precedenti utilizzavano caratteri al di fuori del piano multilingue di base. La traduzione aggiornata utilizza caratteri appropriati che trasmettono con precisione il significato previsto. (TGT-52508 e TGT-52509)
* È stato risolto un problema di localizzazione nella lingua coreana a causa del quale la traduzione di &quot;date&quot; risultava incoerente quando si selezionavano le date di inizio e di fine per un’attività. (TGT-52510)

## Deprecazione attivazione versione interfaccia utente di Target (23 maggio 2025) {#toggle}

Il rollout della nuova interfaccia utente [!DNL Target] verrà completato entro il **27 maggio 2025**. A questo punto, tutti i clienti avranno accesso all’ultima versione dell’interfaccia utente.

A partire dal **22 giugno 2025**, l&#39;interruttore della versione dell&#39;interfaccia utente verrà rimosso. Tutti gli utenti passeranno in modo permanente alla nuova interfaccia, senza alcuna opzione per tornare alla versione precedente.

>[!NOTE]
>
>I clienti con casi speciali che devono mantenere l’interruttore dopo il 22 giugno possono contattare l’Assistenza clienti di Adobe.

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

* [[!DNL Target] Domande frequenti sull&#39;aggiornamento dell&#39;interfaccia utente](/help/main/c-intro/updated-ui-faq.md): queste domande frequenti riguardano le domande comuni sulla nuova interfaccia utente [!DNL Target] e sul nuovo Compositore esperienza visivo [!UICONTROL Visual Experience Composer], incluse le modifiche alla navigazione, le posizioni delle funzioni e la rimozione dell&#39;opzione di versione temporanea dell&#39;interfaccia utente. Che tu sia un addetto marketing, uno sviluppatore o un amministratore, queste domande frequenti consentono una transizione fluida e di sfruttare al massimo l’interfaccia utente aggiornata.

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
