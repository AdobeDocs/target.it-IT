---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti,aggiornamenti correnti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
short-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 65ac352a1de7ad532f8c39781054fb09fa62c0fa
workflow-type: tm+mt
source-wordcount: '1125'
ht-degree: 27%

---

# Note sulla versione (corrente) di [!DNL Target]

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione di API di [!DNL Target], SDK, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

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
