---
keywords: Note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di Adobe Target, inclusi SDK, API e librerie JavaScript.
title: Quali nuove funzioni sono incluse nella versione corrente?
feature: Note sulla versione
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 42%

---


# Note sulla versione di Target (corrente)

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di Target Standard e Target Premium. Sono inoltre incluse, se applicabile, le note sulla versione per API di Target, SDK, libreria JavaScript (at.js) e altre modifiche alla piattaforma.

>[!IMPORTANT]
>
>**Terminazione di mbox.js**: Il 31 marzo 2021 non  [!DNL Adobe Target] supporterà più la libreria mbox.js . Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto positivo sulle pagine che hanno [!DNL Target] attività in esecuzione servendo il contenuto predefinito.
>
>È consigliabile che tutti i clienti effettuino la migrazione alla versione più recente della nuova [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js prima di tale data, per evitare potenziali problemi con i siti. Per ulteriori informazioni, consulta [Panoramica: implementare Target per web lato client](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

(I codici tra parentesi sono per uso interno di [!DNL Adobe].)

## Target Standard/Premium 21.1.1 (19 gennaio 2021)

Questa versione di manutenzione contiene i miglioramenti, le correzioni e le modifiche seguenti.

I codici tra parentesi sono per uso interno di [!DNL Adobe].

* È stato aggiunto un avviso durante la selezione di una metrica [!DNL Adobe Analytics] quando si utilizza [!UICONTROL Analytics come origine per la generazione di rapporti] (A4T) in un’attività [!UICONTROL Targeting automatico]. [!UICONTROL I modelli di ] Targeting automatico sono ottimizzati per lavorare con metriche binarie (basate sulla conversione). La selezione di una metrica continua, come i ricavi, potrebbe avere risultati non ottimali e i rapporti [!UICONTROL Registri di personalizzazione] potrebbero non essere accurati. (TGT-38926)
* È stata aggiunta un&#39;icona di stato nel rapporto [!UICONTROL Riepilogo del Targeting automatico] per le attività [!UICONTROL Targeting automatico] che utilizzano A4T. L&#39;icona di controllo verde accanto a ogni esperienza nel rapporto indica che per quell&#39;esperienza è stato generato un modello di apprendimento automatico personalizzato. L&#39;icona dell&#39;orologio indica che non è stato fornito abbastanza traffico per generare il modello. (TGT-38925)
* I rapporti [!UICONTROL Segmenti automatizzati] e [!UICONTROL Attributi importanti] per le attività [!UICONTROL Targeting automatico] che utilizzano le metriche di conversione A4T e [!DNL Analytics] vengono generati e hanno lo stesso aspetto di quando si utilizza [!DNL Target] come origine per la generazione di rapporti. (TGT-38931)
* È stata aggiunta un’opzione di filtro dell’ambiente all’elenco [!UICONTROL Consigli] [!UICONTROL Raccolte] . (TGT-38353)
* È stato risolto un problema che causava la visualizzazione di un numero errato di prodotti nelle raccolte [!UICONTROL Consigli] . (TGT-39162)
* È stato aggiunto un filtro [!UICONTROL Ultimo aggiornamento] a [!UICONTROL Consigli] [!UICONTROL Ricerca nel catalogo]. (TGT-38340)
* È stato risolto un problema in [!UICONTROL Consigli] che causava il blocco della pagina [!UICONTROL Crea sequenza] dopo la modifica del settore verticale. (TGT-38160)
* È stato risolto un problema che impediva il salvataggio dell’attività se Device Co-op era abilitato e l’utente passava da [!DNL Target] come origine per la generazione di rapporti a [!DNL Analytics] (A4T). (TGT-38163)
* È stato risolto un problema che impediva agli utenti di rimuovere un pubblico da un&#39;offerta in un&#39;attività [!UICONTROL Personalizzazione automatizzata] (AP). (TGT-39058)
* È stato risolto un problema che causava la visualizzazione errata dell&#39;intervallo di tempo (date di inizio e di fine) nelle schede [!UICONTROL Informazioni sul pubblico] per alcuni clienti. (TGT-39150)
* È stato risolto un problema che impediva ad alcuni clienti di visualizzare l&#39;elenco delle attività in [!UICONTROL Area di lavoro predefinita]. (TGT-38526)

## at.js 2.4.0 (14 gennaio 2021)

Questa versione di at.js è una versione di manutenzione e include le seguenti correzioni:

* Aggiunge il supporto per l’id di piattaforma/profilo unificato agli ID cliente API di consegna.
* Corregge l&#39;iniezione di tag di stile non valida.

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
| Note sulla versione di Adobe Experience Cloud | Ultime note sulla versione per le soluzioni Adobe Experience Cloud.<br>Per ulteriori informazioni, consulta Note sulla versione di  [Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html). |

## Informazioni in anteprima {#section_5D588F0415A2435B851A4D0113ACA3A0}

Le risorse seguenti contengono informazioni sulle funzionalità in arrivo con la prossima versione di Target.

| Risorsa | Dettagli |
|--- |--- |
| Adobe Priority Product Update | Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:<br>[](https://www.adobe.com/subscription/priority-product-update.html)https://www.adobe.com/subscription/priority-product-update.html |
| Note sulle prossime versioni | Per informazioni sulle versioni di Target del mese corrente, incluse le informazioni prerelease, consulta la pagina [Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md). |
