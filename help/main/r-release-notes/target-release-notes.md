---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease;early access
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di [!DNL Adobe Target].
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione [!DNL Target] ?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: b91abbd3b7418fd4d1444d96f160c3d9017f3bf8
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 34%

---

# Note sulla versione (prerelease) di [!DNL Target]

Questo articolo contiene informazioni prerelease per le prossime versioni di [!DNL Adobe Target], incluse SDK, API e librerie JavaScript.

**Ultimo aggiornamento: 21 luglio 2025**

>[!NOTE]
>
>* Date di rilascio, funzioni e altre informazioni sono soggette a modifica senza preavviso.
>
>* Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md).
>
>* I codici tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target Standard/Premium] 25.7.3 (venerdì 24 luglio 2025)

A causa dei problemi recenti identificati, principalmente correlati a complesse personalizzazioni dei clienti, questa versione include le correzioni e gli aggiornamenti seguenti:

**Attività**

+++Consulta i dettagli
* È stato risolto un problema a causa del quale il metodo `buildViews` nella classe del generatore impostava erroneamente `viewMaxLocalId` sul numero totale di visualizzazioni, anziché sul numero massimo di `viewLocalId` assegnate. (TGT-53207)

+++

**Compositore esperienza basato su moduli**

+++Consulta i dettagli
* È stato risolto un problema in [!UICONTROL Form-Based Experience Composer] che causava l&#39;arresto anomalo dell&#39;editor dopo aver fatto clic sull&#39;icona **[!UICONTROL Manage Content]** ( ![icona Gestisci contenuto](/help/main/assets/icons/Experience.svg) ) durante la creazione o la modifica di un&#39;attività [!UICONTROL Automated Personalization] (AP). (TGT-53047)

+++

**Raccomandazioni**

+++Consulta i dettagli
* È stato risolto un problema che impediva a [!UICONTROL Catalog Search] di caricare risultati aggiuntivi durante lo scorrimento alla fine dell&#39;elenco, ripristinando un comportamento coerente con l&#39;interfaccia utente legacy. (TGT-53088)
* È stato risolto un problema che causava l&#39;assenza della colonna [!UICONTROL Number of Products] dalla pagina [!UICONTROL Collections] nell&#39;interfaccia utente [!DNL Target] aggiornata. La colonna ora viene visualizzata correttamente, ripristinando la funzionalità prevista. (TGT-53168)
* È stato risolto un problema a causa del quale [!UICONTROL Collection] regole non venivano filtrate correttamente in base alle regole. (TGT-53254)
* È stato risolto un problema che impediva l&#39;eliminazione di elementi dalla finestra di dialogo [!UICONTROL Criteria Details]. (TGT-53245)
* È stato risolto un problema che impediva l’apertura o l’interazione con prodotti senza nome. Questo problema si verificava durante la selezione di ambienti che restituivano risultati senza nome, impedendo l’accesso ai dettagli del prodotto. (TGT-53007)
* È stato risolto un problema che causava l&#39;arresto anomalo della pagina [!UICONTROL Catalog Search] e la visualizzazione di una schermata vuota durante la selezione di alcuni prodotti. (TGT-53087)

+++

**Compositore esperienza visivo**

+++Consulta i dettagli

* È stato risolto un problema nel Compositore esperienza visivo a causa del quale l’applicazione di una modifica a una visualizzazione causava la duplicazione e attivava un errore di tipo &quot;Input utente non valido&quot;. (TGT-52886)
* È stato risolto un problema con la funzionalità [!UICONTROL Undo] per le opzioni [!UICONTROL Insert Before] e [!UICONTROL Insert After] durante la configurazione delle offerte di immagini nel Compositore esperienza visivo.

  In precedenza, l&#39;annullamento di un&#39;azione [!UICONTROL Insert Before] o [!UICONTROL Insert After] sulle offerte di immagini causava un comportamento incoerente o il mancato ripristino corretto della modifica, in particolare nelle attività create nell&#39;interfaccia utente legacy di [!DNL Target]. Questo problema è stato risolto per garantire che le azioni di annullamento ora funzionino in modo affidabile per queste modifiche. (TGT-52809)

+++

## Note aggiuntive e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK]&#x200B;(https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js di [!DNL Adobe Target]. |

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
