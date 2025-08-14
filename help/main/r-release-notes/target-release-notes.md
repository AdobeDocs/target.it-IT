---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease;early access
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di [!DNL Target].
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione [!DNL Target] ?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: c5016d212edafa908b8755044e73d28167e20e8a
workflow-type: tm+mt
source-wordcount: '1167'
ht-degree: 13%

---

# Note sulla versione (prerelease) di [!DNL Target]

Questo articolo contiene informazioni prerelease per le prossime versioni di [!DNL Adobe Target], incluse SDK, API e librerie JavaScript.

**Ultimo aggiornamento: 24 luglio 2025**

>[!NOTE]
>
>* Date di rilascio, funzioni e altre informazioni sono soggette a modifica senza preavviso.
>
>* Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md).
>
>* I codici tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target Standard/Premium] 25.8.2 (13 agosto 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

**[!UICONTROL Activities]**

+++Vedi i dettagli
* È stato risolto un problema nell&#39;interfaccia utente [!DNL Target] aggiornata a causa del quale alcune attività non venivano caricate durante il tentativo di modifica. Questo problema causava la partenza degli utenti da una schermata di caricamento indefinita. Questo problema ha interessato più attività ed è stato segnalato come incoerente tra i clienti. Con questa correzione, le attività interessate ora vengono caricate correttamente, consentendo una modifica diretta e riducendo le interruzioni dei flussi di lavoro delle attività. (TGT-53209)
* È stato risolto un problema nel processo di creazione attività che impediva ai clienti di salvare le modifiche a causa di un errore di convalida del back-end: `OptionLocalIdReferentialIntegrity.ABActivity - Invalid optionLocalIds:` Questo problema si verificava durante la modifica di elementi specifici all&#39;interno di un&#39;attività, causando un&#39;operazione di salvataggio non riuscita. La correzione assicura che `optionLocalId` riferimenti siano ora convalidati correttamente, consentendo ai clienti di salvare le attività senza incontrare questo errore. (TGT-53293)
* È stato risolto un problema nel processo di creazione delle attività che causava l’arresto anomalo dell’interfaccia utente dopo il cambio di pagina per tre volte durante la modifica. L&#39;arresto anomalo è stato attivato da riferimenti di opzione non validi, causando errori della console quali &quot;Impossibile trovare l&#39;opzione con localId &#39;7&#39;.&quot; Con questo aggiornamento, i clienti possono passare da una pagina all’altra e applicare le modifiche senza incontrare errori o interruzioni del sistema. (TGT-53295)
* È stato risolto un problema nel processo di creazione attività a causa del quale i clienti non potevano salvare le modifiche apportate a un’attività a causa di un errore di inserimento utente non valido. L’errore si è verificato durante la modifica delle esperienze nell’interfaccia utente aggiornata, impedendo il commit degli aggiornamenti. L’attività ora può essere salvata correttamente, consentendo ai clienti di modificarla e pubblicarla senza interruzioni. (TGT-53267)
* È stato risolto un problema nel processo di creazione attività a causa del quale i clienti non potevano modificare le attività nell’interfaccia utente aggiornata a causa di una schermata di caricamento continuo. Ora i clienti possono aprire e modificare le attività senza riscontrare errori di caricamento. (TGT-53415)

+++

**Frammenti esperienza (XF)**

+++Vedi i dettagli
* È stato risolto un problema nel processo di creazione attività che consentiva ai clienti di modificare il HTML di [!DNL Experience Fragments] (XF) esportati da [!DNL Adobe Experience Manager] (AEM) entro [!DNL Target]. Questo comportamento non era intenzionale, poiché gli XF dovrebbero rimanere bloccati per la modifica dopo la pubblicazione da AEM. La correzione assicura che l’opzione &quot;Modifica HTML&quot; non sia più disponibile per i frammenti esportati da AEM, mantenendo l’integrità dei contenuti e la governance prevista. (TGT-53286)

+++

**Modalità Controllo di qualità**

+++Vedi i dettagli
* È stato risolto un problema nel processo di creazione attività a causa del quale gli spazi iniziali nell’URL attività non venivano tagliati correttamente durante il salvataggio. Questo causava collegamenti QA non validi e formattazione errata nel back-end. Dopo l’aggiornamento, gli URL vengono ora salvati correttamente, evitando collegamenti interrotti e migliorando l’affidabilità dei flussi di lavoro di controllo qualità per i clienti. (TGT-53427)

+++

**[!UICONTROL Recommendations]**

+++Vedi i dettagli
* È stato risolto un problema nella nuova interfaccia utente [!UICONTROL Catalog Search] a causa del quale la funzionalità [!UICONTROL Advanced Search] non forniva suggerimenti. Gli utenti dovevano immettere valori esatti con un’ortografia precisa, rendendo l’esperienza di ricerca complicata e soggetta a errori. Con questa correzione, [!UICONTROL Advanced Search] offre ora suggerimenti rilevanti per la digitazione degli utenti, migliorando l&#39;usabilità e riducendo l&#39;attrito nella ricerca dei prodotti. (TGT-52008)
* Sono stati risolti diversi problemi, tra cui la scarsa reattività dei dettagli dei criteri sui dispositivi con schermo piccolo, la mancanza di risultati durante la selezione di &quot;Tutti i gruppi di host&quot; nel filtro [!UICONTROL Environment] e l&#39;impossibilità di interagire con entità prive di nome. Queste correzioni migliorano l’usabilità tra le dimensioni dello schermo, garantiscono un filtraggio accurato e consentono la piena interazione con tutte le entità prodotto, migliorando l’esperienza complessiva per gli utenti. (TGT-52992)
* È stato risolto un problema nel processo di creazione attività [!DNL Recommendations] a causa del quale gli ID prodotto mancavano dalla schermata dei dettagli del prodotto, rendendo difficile per i clienti copiare o fare riferimento agli ID prodotto durante i flussi di lavoro. Gli ID prodotto vengono ora visualizzati chiaramente nella visualizzazione dettagliata, migliorando la visibilità e supportando una gestione più efficiente dei prodotti per i clienti. (TGT-51964)
* È stato risolto un problema nel processo di creazione attività a causa del quale la colonna [!UICONTROL Message] nella visualizzazione [!DNL Recommendations] non visualizzava i dati del prodotto, anche se erano presenti messaggi. I clienti hanno dovuto rimuovere manualmente e aggiungere nuovamente la colonna per visualizzare temporaneamente il contenuto, che spesso scompariva nuovamente durante lo scorrimento o la ricerca. Questo aggiornamento ripristina una visibilità coerente dei messaggi dei prodotti, migliorando la navigazione del catalogo e i flussi di lavoro di revisione. (TGT-52777)
* È stato risolto un problema nel processo di creazione attività a causa del quale la selezione dell&#39;ambiente &quot;Tutti i gruppi di host&quot; nella visualizzazione [!DNL Recommendations] non restituiva alcun risultato. Ora i clienti possono visualizzare i dati dei prodotti in tutti i gruppi di host come previsto, migliorando la visibilità e la precisione dei filtri durante la configurazione dell’attività. (TGT-53006)
* È stato risolto un problema nel processo di creazione attività a causa del quale la disattivazione dell’opzione di promozione frontale nelle impostazioni dell’attività non persisteva dopo il salvataggio. I clienti che tentavano di rimuovere la promozione iniziale hanno riscontrato che l’interruttore era stato riattivato al momento della revisione dell’attività, impedendo la corretta personalizzazione. Questo aggiornamento consente di salvare le modifiche in modo affidabile, offrendo ai clienti pieno controllo sulle impostazioni di promozione. (TGT-53215)

+++

**Compositore esperienza visivo**

+++Vedi i dettagli
* È stato risolto un problema nel processo di creazione attività a causa del quale alcune attività non venivano caricate, impedendo ai clienti di accedere alle modifiche. Inoltre, il pulsante [!UICONTROL Cancel] non rispondeva, impedendo ai clienti di arrestare il processo di caricamento o uscire dalla visualizzazione di modifica. Questa correzione assicura che le attività ora vengano caricate in modo affidabile e che il pulsante [!UICONTROL Cancel] funzioni come previsto, migliorando la stabilità complessiva e l&#39;esperienza utente nel Compositore esperienza visivo (TGT-53218)
* È stato risolto un problema nell’interfaccia utente del Compositore esperienza visivo aggiornata a causa del quale non era possibile caricare le modifiche quando si passava da un’esperienza all’altra in un’attività Targeting esperienza. I clienti non sono stati in grado di modificare le esperienze oltre a quella inizialmente immessa e il pulsante [!UICONTROL Cancel] risulta mancante o non risponde. Questa correzione assicura che le modifiche ora vengano caricate correttamente in tutte le esperienze e che il pulsante [!UICONTROL Cancel] funzioni in modo affidabile, anche senza l&#39;estensione Helper, migliorando i flussi di lavoro di modifica e riducendo la frustrazione. (TGT-53256)
* È stato risolto un problema che causava la visualizzazione di una schermata bianca quando si passava da un’esperienza all’altra. È stato inoltre risolto un problema nel processo di creazione delle attività a causa del quale i clienti riscontravano una schermata bianca durante il tentativo di modificare più esperienze all’interno di un’attività. Questo problema si verificava dopo aver applicato le modifiche a due esperienze e aver selezionato una terza esperienza, impedendo ulteriori modifiche. L’aggiornamento garantisce una transizione fluida tra le esperienze, consentendo ai clienti di apportare modifiche senza interruzioni. (TGT-53266)
* È stato risolto un problema a causa del quale le modifiche al codice personalizzato apportate nel Compositore esperienza visivo non venivano salvate in modo affidabile in un singolo tentativo. I clienti hanno segnalato che le modifiche, come gli aggiornamenti degli stili o le modifiche di HTML, mancavano in modo intermittente dagli URL del sito Web e del controllo qualità, anche dopo aver utilizzato sia il pulsante [!UICONTROL Edit Content] che il pulsante [!UICONTROL Save] finale. Questa regressione è stata risolta, garantendo che tutte le modifiche al codice personalizzato persistano come previsto tra le sessioni di modifica. (TGT-53418)

+++

## Note aggiuntive e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK]&#x200B;(https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js di [!DNL Adobe Target]. |

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
