---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti;aggiornamenti;aggiornamenti correnti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
short-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: ada5803424b4930d91dda735901390fe5073932f
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 39%

---

# Note sulla versione (corrente) di [!DNL Target]

Esplora le funzioni, i miglioramenti e le correzioni più recenti in [!DNL Adobe Target]. Queste note sulla versione descrivono anche gli aggiornamenti alle API [!DNL Target], agli SDK, a [!DNL Adobe Experience Platform Web SDK], at.js e ad altri componenti della piattaforma, se applicabili.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## Aggiornamenti urgenti da conoscere {#time-sensitive}

[!BADGE Importante]{type=Informative}

Per gli aggiornamenti sensibili al tempo relativi a [!DNL Adobe Target] e alla tua implementazione, [!DNL Adobe] fornisce note dettagliate sulla versione e documentazione tramite [!UICONTROL Experience League]. Di seguito sono riportate alcune caratteristiche principali relative all’implementazione:

### La versione dell&#39;interfaccia utente [!DNL Target] è deprecata

Per ulteriori informazioni, vedere [[!DNL Target] Domande frequenti sull&#39;aggiornamento dell&#39;interfaccia utente](/help/main/c-intro/updated-ui-faq.md).

<!--
## [!DNL Target Standard/Premium] 26.4.2 (April 7, 2026)

**Activities**

+++See details

* **Custom code preserved when applied to additional views.** Fixed an issue where custom code applied to one **[!UICONTROL View]** could be removed when adding or saving custom code for another **[!UICONTROL View]** in the same **[!UICONTROL Activity]**. (TGT-53933)

* **Reporting metrics column order.** The updated [!DNL Target] interface allows reporting metrics to be reordered without clearing the full selection and re-adding metrics in sequence. Previously, users were required to unselect all metrics and select them again in the desired order, which was time-consuming when many metrics were enabled and when adjusting column placement to limit horizontal scrolling. (TGT-53044)

+++

-->

## [!DNL Target Standard/Premium] 26.4.1 (venerdì 2 aprile 2026)

**Attività**

+++Vedi i dettagli

* **Attributi del pubblico visibili nella vista Attività.** È stato risolto un problema a causa del quale i dettagli della regola del pubblico visualizzati da un **[!UICONTROL Activity]** non mostravano alcuni attributi visualizzati quando si apriva lo stesso pubblico dalla sezione **[!UICONTROL Audiences]**. (TGT-54742)

* **Esporta file CSV nelle pagine di elenco Attività e Tipi di pubblico.** Aggiunta azione **[!UICONTROL Export CSV]** per esportare gli elenchi di attività dall&#39;interfaccia utente, anche quando vengono applicati i filtri, senza affidarsi esclusivamente alle API per le esportazioni di routine. (TGT-51466)

* **Modifiche dell&#39;esperienza contrassegnate quando i selettori non vengono trovati.** Le modifiche all&#39;esperienza ora eseguono un controllo di esistenza del selettore; quando un selettore non viene trovato nella pagina, la modifica viene contrassegnata come non valida. (TGT-54815)

* **[!UICONTROL Automated personalization]attività.** Sono stati risolti i problemi relativi all&#39;interfaccia e al caricamento delle attività che impedivano agli utenti di creare, modificare o gestire in modo affidabile le attività di Personalizzazione automatizzata, bloccando la configurazione della campagna e ritardando i casi di utilizzo della personalizzazione. (TGT-54421)

+++

**Tipi di pubblico**

+++Vedi i dettagli

* **Nome e descrizione del pubblico visibili durante la creazione di tipi di pubblico da un&#39;attività.** È stato risolto un problema che impediva ai campi del pubblico **[!UICONTROL Name]** e **[!UICONTROL Description]** di emergere chiaramente durante la creazione o la modifica di un pubblico dal flusso di attività, rispetto alla creazione del pubblico direttamente in **[!UICONTROL Audiences]**. (TGT-54837)

+++

**Informazioni**

+++Vedi i dettagli

* **[!UICONTROL Live Activities]contano su Insights.** È stato risolto un problema a causa del quale la metrica **[!UICONTROL Live Activities]** nel dashboard Approfondimenti poteva riportare un totale maggiore del numero di attività visualizzate come attive in **[!UICONTROL All Activities]**. (TGT-54788)

+++

**Funzione Consigli**

+++Vedi i dettagli

* **Elenchi ID lunghi in [!UICONTROL Global Exclusions].** È stato risolto un problema che causava il troncamento dell&#39;operazione Incolla o Inserimento di un lungo elenco di ID in **[!UICONTROL Global Exclusions]** nell&#39;interfaccia aggiornata rispetto alla versione precedente, causando un elenco di esclusione incompleto. (TGT-54422)

+++

**[!UICONTROL Visual Experience Composer](VEC)**

+++Vedi i dettagli

* **Indicatore di stato Compositore esperienza avanzato in [!UICONTROL Visual Experience Composer].** L&#39;indicatore EEC indica se il Compositore esperienza avanzato è abilitato. La sua presentazione è stata rivista in modo che non assomigli più a un interruttore interattivo, in quanto funge solo da visualizzazione di stato non interattivo. (TGT-54828)

* **Barra a sinistra comprimibile in [!UICONTROL Visual Experience Composer].** È ora possibile comprimere la barra a sinistra mentre un&#39;attività è aperta per la modifica. Ciò migliora l&#39;accesso a **[!UICONTROL Components]** e **[!UICONTROL Properties]** per le attività che includono più tipi di pubblico e pagine, anche su schermi più piccoli. (TGT-54269)

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

## Informazioni pre-release {#section_5D588F0415A2435B851A4D0113ACA3A0}

Le risorse seguenti contengono informazioni sulle funzionalità in arrivo con la prossima versione di Target.

| Risorsa | Dettagli |
|--- |--- |
| [Adobe Priority Product Update](https://www.adobe.com/subscription/priority-product-update.html){target=_blank} | Notifiche anticipate sui miglioramenti dei prodotti in arrivo per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud]. |
| [Note sulla versione di Target: pre-release](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informazioni sulle versioni di Target del mese corrente, incluse le informazioni pre-release. |
