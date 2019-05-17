---
description: Queste note sulla versione forniscono informazioni su funzionalità, miglioramenti, correzioni e problemi noti per ogni versione di Target Standard e Target Premium.
keywords: Note sulla versione;prerelease
seo-description: Queste note sulla versione forniscono informazioni su funzioni, miglioramenti, correzioni e problemi noti per ciascuna versione di Adobe Target Standard e Target Premium.
seo-title: Note sulla versione di Target (corrente)
solution: Target
title: Note sulla versione di Target (corrente)
topic: 'Consigli '
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Note sulla versione di Target (corrente){#target-release-notes-current}

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di Target Standard e Target Premium.

## Annunci

Tieni presenti i seguenti importanti annunci:

* Il 20 febbraio 2019 l&#39;infrastruttura Adobe Target è stata aggiornata nelle aree EMEA, Japan e APAC per non raccogliere più dati dagli utenti finali con dispositivi meno recenti o browser Web che non supportano TLS 1.1 o versione successiva. Lo stesso aggiornamento è pianificato per l&#39;area Nord America del **1 aprile 2019**. La migrazione a TLS 1.2 offre una maggiore protezione. È importante seguire le specifiche e pianificare le modifiche con il team IT per una transizione uniforme. Per ulteriori informazioni, vedi [Modifiche alla crittografia TLS (Transport Layer Security)](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md).
* [!DNL Target] e [!DNL Adobe Marketing Cloud] abbandoneranno il supporto per Microsoft Internet Explorer 11 a partire da marzo 2019. Questa modifica influisce solo sull’authoring di [!DNL Target] senza influire sulla distribuzione delle esperienze. Passa a Microsoft Edge o a un altro browser. Per ulteriori informazioni, consulta [Browser supportati](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md).

## Mobile App Visual Experience Composer (14 maggio 2019) {mobile-vec}

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| Mobile App Visual Experience Composer (VEC) | La VEC App mobile consente di creare attività e personalizzare il contenuto su app native per dispositivi mobili in modo autonomo senza continuità di sviluppo e cicli di rilascio delle app.<br>Per ulteriori informazioni, vedi:<ul><li>[Compositore esperienza visivo per app mobile](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md)</li><li>[Android: configurare l&#39;app mobile](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-android.md)</li><li>[iOS: configurare l&#39;app mobile](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-ios.md)</li><li>[Configurare il tracciamento dei clic nel Compositore esperienza visivo mobile](/help/c-target-mobile-app/c-mobile-visual-experience-composer/set-up-click-tracking-in-the-mobile-vec.md)</li></ul> |

## [!DNL Target] Standard/Premium 19.4.2 (30 aprile 2019) {#release-19-4-2}

Questa versione include i miglioramenti, le modifiche e le funzioni seguenti:

(I codici tra parentesi sono per uso interno di [!DNL Adobe].)

### Aggiornamenti delle funzioni

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| [!UICONTROL Compositore esperienza visivo] | [!UICONTROL Visual Experience Composer (Compositore] esperienza visivo) include i seguenti miglioramenti per rendere il lavoro più rapido ed efficiente:<ul><li>La funzione path path (Percorso DOM) ora è disponibile quando si imposta il tracciamento dei clic.<br>Per ulteriori informazioni, vedi [monitoraggio dei clic](/help/c-activities/r-success-metrics/click-tracking.md#considerations).</li><li>Il pannello Stili consente di visualizzare o modificare il valore degli stili esistenti per l&#39;elemento selezionato. Potete inoltre aggiungere ulteriore stile.<br>Per accedere al pannello Stili, fare clic su un elemento di pagina dall&#39;interno della VEC, quindi fare clic su [!UICONTROL Modifica] &gt; [!UICONTROL Stili].<br>Il pannello Stili viene visualizzato sul lato destro della VEC. Il pannello contiene un elenco di stili che consente di modificare o aggiungere all&#39;elemento selezionato. Un editor CSS in tempo reale consente di visualizzare le modifiche e aggiungere stili se avete familiarità con Cascading Style Sheets (CSS) o se ricevete codice dallo sviluppatore.<br>Per ulteriori informazioni, consultate [Stili](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#styles) in *Visual Experience Composer (Opzioni di composita esperienza visivo*).</li><li>L&#39;editor Rich Text supporta ora elementi HTML 5 nidificati.<br>Le specifiche HTML 5 consentono nuove combinazioni di tag per la nidificazione. La versione precedente dell&#39;editor Rich Text non supportava la nuova nidificazione di tag come consentito dalle specifiche HTML 5. Di conseguenza, tutti gli elementi nidificati selezionati nell&#39;aula virtuale non venivano gestiti correttamente, generando modifiche HTML indesiderate. (TGT -33618)<br>Per ulteriori informazioni, consultate [Modifica testo/HTML](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#edit-text-html) nelle opzioni *di Visual Experience Composer (Compositore esperienza visivo*).</li> |

### Miglioramenti, correzioni e modifiche

* È stato migliorato il flusso di lavoro quando si eliminano le risorse nel Compositore esperienza visivo. Le risorse eliminate vengono rimosse dalla libreria [!UICONTROL Offerte] e da [!DNL Scene7] (se applicabile). Le risorse eliminate non vengono più visualizzate nei risultati di ricerca. (TGT-31981)
* Potete ora eliminare le cartelle delle risorse anche se contengono immagini (cartelle non vuote). (TGT-33265)

   In precedenza, non era possibile eliminare una cartella non vuota dall&#39;immagine delle offerte di Target ([!UICONTROL Offerte] &gt; [!UICONTROL Offerte immagini]). Si ottiene una cartella «Folder is not empty!» quando si tenta di eliminare la cartella dall&#39;interfaccia utente. Con questa funzione, stiamo aggiungendo la funzionalità di eliminazione della cartella per rimuovere un&#39;intera cartella contenente un numero qualsiasi di risorse e sottocartelle all&#39;interno. Questa funzione è disponibile anche nell&#39;interfaccia utente di Target, nell&#39;interfaccia utente di Adobe Experience Cloud Assets.

   * Le cartelle non vuote nella libreria Offerta immagini possono essere eliminate. Se non viene fatto riferimento a tutte le immagini all&#39;interno della cartella, l&#39;intera cartella e il relativo contenuto vengono eliminati. Se in un&#39;attività vi sono riferimenti a alcune immagini, tutte le immagini non di riferimento vengono eliminate, ma vengono mantenute le immagini di riferimento e le cartelle contenenti tali immagini.
   * Il rendering delle offerte delle immagini nel selettore delle risorse immagine risulta più rapido ed efficiente.
   Per ulteriori informazioni, consultate [Operazioni con il contenuto della libreria](/help/c-experiences/c-manage-content/assets-working.md). (TGT-32897)

* Abbiamo migliorato il rendering delle offerte immagini nel selettore di Assets. La visualizzazione e la selezione delle offerte immagini sono ora più veloci ed efficienti. (TGT-32897)
* Abbiamo migliorato la gestione dei reindirizzamenti agli URL quando si annulla il caricamento di una pagina nel Compositore esperienza visivo. (TGT-33815)
* Dopo aver selezionato una [!UICONTROL raccolta di Recommendations] dal selettore raccolte, ora dovete fare clic sul [!UICONTROL pulsante Salva] . Questo flusso di lavoro è in linea con gli altri flussi di lavoro all’interno di [!DNL Target]. (TGT-33205)
* È stato risolto un problema a causa del quale un piccolo set di report Approfondimenti restituiva tassi di conversione del 0% al posto dei tassi di conversione effettivi. (TNT-32125)

## [!DNL Target] Standard/Premium 19.4.1 (15 aprile 2019) {#release-19-4-1}

Questa è una versione di manutenzione e include la seguente modifica:

(I codici tra parentesi sono per uso interno di [!DNL Adobe].)

* Aggiornamento [!DNL Adobe Experience Cloud] dell&#39;interfaccia utente per riflettere le modifiche al marchio e al prodotto. (TGT-33546, TGT-33272 e TGT-33331)

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
| Adobe Priority Product Update | Per ricevere notifiche anticipate sui miglioramenti dei prodotti in arrivo a Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Prossime note sulla versione | Per informazioni sulle versioni di Target del mese corrente, incluse le informazioni pre-rilascio, consulta la pagina [Note sulla versione di Target - Pre-rilascio](/help/r-release-notes/target-release-notes.md). |