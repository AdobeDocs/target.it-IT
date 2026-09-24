---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti;aggiornamenti;aggiornamenti correnti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di [!DNL Adobe Target].
short-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di [!DNL Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
TQID: https://experienceleague.adobe.com/-Unx6cVsw3wch2LJgPtvBYPe-10rdpiJ4v9F7tMSP08
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
subfeature_v2:
  - id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
    internal-label: at.js
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 4d083419d76b0287c3c254a0fc382abc7444cc75
workflow-type: tm+mt
source-wordcount: '874'
ht-degree: 32%
---
# Note sulla versione (corrente) di [!DNL Target]

Esplora le funzioni, i miglioramenti e le correzioni più recenti in [!DNL Adobe Target]. Queste note sulla versione descrivono anche gli aggiornamenti alle API [!DNL Target], agli SDK, a [!DNL Adobe Experience Platform Web SDK], at.js e ad altri componenti della piattaforma, se applicabili.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target Standard/Premium] 26.9.6 (24 settembre 2026)

**[!UICONTROL Compositore esperienza visivo] (VEC)**

+++Vedi i dettagli

* **Ciclo di reindirizzamento senza fine durante l&#39;accesso a una pagina autenticata da SSO tramite il Compositore esperienza visivo**. Quando un URL di pagina caricato nel Compositore esperienza visivo passa attraverso un flusso di reindirizzamento SSO/login, il Compositore esperienza visivo entra in un ciclo di reindirizzamento senza fine e non raggiunge mai la pagina desiderata. (TGT-56233)

+++

## [!DNL Target Standard/Premium] 26.9.5 (21 settembre 2026)

### Funzione

<table>
<thead>
<tr>
<th><strong>Pre-hiding dei contenuti</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il pre-hiding dei contenuti aiuta a ridurre lo sfarfallio della pagina nascondendo solo le sezioni che la personalizzazione Adobe Target sta per modificare, fornendo un’esperienza più fluida durante il caricamento dei contenuti. Questo approccio evita di nascondere l’intera pagina e aiuta a ridurre al minimo lo sforzo di implementazione quando vengono avviate nuove attività.</p>
<p>Precedentemente rilasciata in Disponibilità limitata, questa funzionalità è ora disponibile per tutti gli ambienti (Disponibilità generale).</p>
<p>Per ulteriori informazioni, consulta la <a href="../administrating-target/content-pre-hiding.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

### Migliori

**[!UICONTROL Analytics per Target]**

+++Vedi i dettagli

* **Collegamento al report A4T non generato nell&#39;interfaccia utente [!DNL Target]**. Per le attività [!DNL A4T], il collegamento al report non è stato generato nella sezione **[!UICONTROL Reports]**, anche se i dati del report sottostante erano visibili sia nell&#39;interfaccia utente [!DNL Target] che in quella [!DNL Adobe Analytics]. (TGT-56247)

+++

## [!DNL Target Standard/Premium] 26.9.4 (17 settembre 2026)

**[!UICONTROL Compositore esperienza visivo] (VEC)**

+++Vedi i dettagli

* **[!UICONTROL Inserisci controllo Before] inaccessibile per [!DNL Experience Fragments] nell&#39;elemento della pagina superiore**. Nel Compositore esperienza visivo, quando si seleziona l&#39;elemento più in alto in una pagina, la pagina viene scorsa verso l&#39;alto, causando il rendering del controllo **[!UICONTROL Inserisci prima]** sopra il riquadro di visualizzazione visibile in cui non è stato possibile selezionarlo. (TGT-55829)

+++

## [!DNL Target Standard/Premium] 26.9.3 (16 settembre 2026)

**[!UICONTROL Generazione di rapporti]**

+++Vedi i dettagli

* **Valori [!UICONTROL Lift] e [!UICONTROL Confidence] mancanti in alcuni [!DNL A4T Auto-Target] report**. Per le attività [!DNL A4T Auto-Target] che utilizzano l&#39;obiettivo di ottimizzazione del **[!UICONTROL Tasso di conversione visita massimo]**, la metrica di report predefinita **[!UICONTROL Metrica principale]** non è stata risolta correttamente, lasciando vuoti **[!UICONTROL Incremento]** e **[!UICONTROL Affidabilità]**. (TGT-56137)

+++

**[!UICONTROL Analytics per Target]**

+++Vedi i dettagli

* Il campo **[!UICONTROL Reporting di Source] è ora di sola lettura per le attività live senza accesso [!DNL Analytics]**. In precedenza, quando il proprietario di un&#39;attività live non aveva accesso a [!DNL Adobe Analytics], il campo **[!UICONTROL Source]** per la generazione di rapporti e il relativo campo rimanevano modificabili. (TGT-56089)

+++

## [!DNL Target Standard/Premium] 26.9.2 (8 settembre 2026)


**[!UICONTROL Funzione Consigli]**

+++Vedi i dettagli

* L&#39;interfaccia utente **[!DNL New]codifica gli URL del feed in modo errato**. Durante la creazione di un feed di consigli da un URL nella nuova interfaccia [!DNL Target], l&#39;URL del feed non è stato codificato correttamente. La creazione del feed non è riuscita a causa di un errore sconosciuto. (TGT-56084)

+++

**[!UICONTROL Generazione di rapporti]**

+++Vedi i dettagli

* Il report **Segmenti automatizzati non visualizza in modo coerente i valori degli attributi**. Nel rapporto Segmenti automatizzati sono stati visualizzati valori e intervalli di attributi non coerenti per le attività [!DNL Automated Personalization] e [!DNL Auto-Target]. Alcuni segmenti automatizzati mostravano solo il nome dell’attributo invece del valore o dell’intervallo associato. (TGT-55855)

+++

## [!DNL Target Standard/Premium] 26.9.1 (1° settembre 2026)

**[!UICONTROL Pubblico]**

+++Vedi i dettagli

* **Impossibile salvare la copia di un&#39;attività con un pubblico per sola attività**. Quando un’attività A/B utilizza una regola di pubblico per sola attività (con ambito locale) e una modifica del Codice personalizzato, la copia e il salvataggio della copia non riescono e viene visualizzato un errore di tipo &quot;ID pubblico non validi&quot;. (TGT-55785)

+++

Server MCP **[!DNL Adobe Target]- Strumenti di Recommendations (Beta pubblico)**

+++Vedi i dettagli

Il server MCP [!DNL Adobe Target] ora espone gli strumenti Consigli, consentendo di elencare, esaminare, creare e aggiornare criteri, raccolte, progettazioni, promozioni ed esclusioni e di eseguire ricerche nel catalogo prodotti direttamente dall&#39;assistente AI.

Questa funzionalità richiede un tenant abilitato per Recommendations con **Target Premium**; non è disponibile per account non Premium.

Per ulteriori informazioni, vedere [Riferimento strumenti server MCP](../c-integrating-target-with-mac/mcp/target-mcp-tools-reference.md).

+++

## Aggiornamenti urgenti da conoscere {#time-sensitive}

[!BADGE Importante]{type=Informative}

Per gli aggiornamenti sensibili al tempo relativi a [!DNL Adobe Target] e alla tua implementazione, [!DNL Adobe] fornisce note dettagliate sulla versione e documentazione tramite [!UICONTROL Experience League]. Di seguito sono riportate alcune caratteristiche principali relative all’implementazione:

### La versione dell&#39;interfaccia utente [!DNL Target] è deprecata

Per ulteriori informazioni, vedere [[!DNL Target] Domande frequenti sull&#39;aggiornamento dell&#39;interfaccia utente](/help/main/c-intro/updated-ui-faq.md).

## Note aggiuntive e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js di [!DNL Adobe Target]. |

## Modifiche alla documentazione, precedenti note sulla versione e note sulla versione di Experience Cloud

Per informazioni aggiuntive, oltre alle note di ciascuna versione, consulta le seguenti risorse:

| Risorsa | Dettagli |
|--- |--- |
| [Modifiche alla documentazione](/help/main/r-release-notes/doc-change.md) | Consulta le informazioni dettagliate sugli aggiornamenti di questa guida che non sono inclusi nelle presenti note sulla versione. |
| [Note sulla versione per le versioni precedenti](/help/main/r-release-notes/release-notes-for-previous-releases.md). | Informazioni su nuove funzionalità e miglioramenti introdotti nelle versioni precedenti di Target Standard e Target Premium. |
| [Note sulla versione di Adobe Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=it){target=_blank} | Ultime note sulla versione per le soluzioni Adobe Experience Cloud. |

## Informazioni pre-release {#section_5D588F0415A2435B851A4D0113ACA3A0}

Le risorse seguenti contengono informazioni sulle funzionalità in arrivo con la prossima versione di Target.

| Risorsa | Dettagli |
|--- |--- |
| [Adobe Priority Product Update](https://www.adobe.com/subscription/priority-product-update.html){target=_blank} | Notifiche anticipate sui miglioramenti dei prodotti in arrivo per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud]. |
| [Note sulla versione di Target: pre-release](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informazioni sulle versioni di Target del mese corrente, incluse le informazioni pre-release. |
