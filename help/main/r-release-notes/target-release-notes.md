---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease;early access
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di [!DNL Target].
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione [!DNL Target] ?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: fda279c909e2bb35e919d1bb4f4b611401a367cf
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 17%

---

# Note sulla versione (prerelease) di [!DNL Target]

Questo articolo contiene informazioni prerelease per le prossime versioni di [!DNL Adobe Target], incluse SDK, API e librerie JavaScript.

**Ultimo aggiornamento: 29 agosto 2025**

>[!NOTE]
>
>* Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso. Le informazioni contenute in questo articolo vengono aggiornate frequentemente, soprattutto prima delle versioni di.
>
>* Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md).
>
>* I codici tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target Standard/Premium] 25.8.4 (1° settembre 2025)

Questa versione include i seguenti aggiornamenti e correzioni:

**[!UICONTROL Activities]**

+++Vedi i dettagli
* **I clienti non potevano copiare i nomi di attività o documenti da[!UICONTROL Activity Overview]**: in precedenza, i clienti non potevano copiare il nome di un&#39;attività o l&#39;offerta/documento associato direttamente da [!UICONTROL Activity Overview] nel processo di creazione attività aggiornato. Questa limitazione ha influito sull’usabilità, in particolare sugli schermi più piccoli. I clienti possono ora copiare facilmente sia i nomi delle attività che i nomi dei documenti senza soluzioni alternative. (TGT-51850)
* **Acquisizione proattiva dei dati dei clienti [!DNL Target] curati durante la creazione dell&#39;attività**: il processo di creazione dell&#39;attività è stato migliorato abilitando la raccolta proattiva di report, contenuti e schermate da [!DNL Target] clienti. Questo miglioramento risolve le lacune nei dati identificate nei casi di utilizzo esistenti e aiuta a garantire informazioni più precise durante la configurazione di attività e esperimenti. (TGT-52415)
* **Le attività di Personalizzazione automatizzata non hanno recuperato i dati pronti per il modello nella sezione [!UICONTROL Reports]**: i clienti che visualizzavano le attività di Automated Personalization (AP) nella sezione [!UICONTROL Reports] non sono stati in grado di visualizzare gli indicatori pronti per il modello a livello di gruppo di rapporti e di offerta. Questo problema si verificava perché i dati pronti per il modello non venivano recuperati correttamente dal backend. La funzionalità è stata ripristinata e ora vengono visualizzati i dati pronti per il modello come previsto. (TGT-53600 e TGT-53601)

+++

**[!UICONTROL Recommendations]**

+++Vedi i dettagli
* **Elenco prodotti non visibile nella finestra di dialogo [!UICONTROL View Collection]:** In precedenza, i clienti non potevano visualizzare l&#39;elenco prodotti quando visualizzavano una raccolta nella scheda [!UICONTROL Recommendations]. La finestra di dialogo [!UICONTROL View Collection] visualizza ora correttamente i prodotti associati, migliorando la trasparenza e l&#39;usabilità nell&#39;interfaccia utente Consigli aggiornata. (TGT-50531)
* **È stato risolto un problema che causava un filtro sensibile a maiuscole e minuscole nella ricerca avanzata di [!UICONTROL Product Catalog Search]**: il filtro della ricerca avanzata nella pagina [!UICONTROL Product Catalog Search] ignora ora correttamente la distinzione tra maiuscole e minuscole, in linea con il comportamento dei servizi di back-end e GraphQL. Questo aggiornamento garantisce risultati coerenti e precisi per i suggerimenti per i clienti indipendentemente dall’involucro di testo. (TGT-53585)
* **La ricerca avanzata nell&#39;interfaccia utente aggiornata di [!UICONTROL Product Catalog Search] non ha fornito suggerimenti**: i clienti che utilizzano la funzione di ricerca avanzata nell&#39;interfaccia utente aggiornata di [!UICONTROL Product Catalog Search] dovevano immettere valori esatti con l&#39;ortografia corretta, poiché non venivano visualizzati suggerimenti. Ciò rendeva difficile individuare i prodotti in modo efficiente. I suggerimenti vengono ora visualizzati come previsto durante l’input della ricerca avanzata. (TGT-52008)

+++

**[!UICONTROL Reports]**

+++Vedi i dettagli
* **Impossibile caricare i report per il pubblico desktop a causa di un errore di nome del pubblico non valido**: si è verificato un errore di GraphQL durante il tentativo di visualizzare i report per il solo pubblico nel processo di creazione attività. Il sistema ha restituito un messaggio di tipo &quot;Nome pubblico non valido: XXXXX&quot; che impediva l’accesso ai dati di reporting. I rapporti ora vengono caricati correttamente per il pubblico del desktop. (TGT-53371)
* **Il cambio di pubblico nella pagina Rapporti ha causato errori nell&#39;interfaccia utente di Target**: i clienti hanno riscontrato errori durante la selezione di alcuni tipi di pubblico nella sezione Reports dell&#39;interfaccia utente di Target aggiornata. Questo problema era causato da una gestione non valida del pubblico nelle chiamate GraphQL back-end, che causava errori imprevisti e dati mancanti. Il problema è stato risolto e i tipi di pubblico desktop ora vengono caricati senza errori, anche quando non sono disponibili dati. (TGT-53370)
+++

**[!UICONTROL Visual Experience Composer](VEC)**

+++Vedi i dettagli
* **Impossibile fare clic su &quot;Accetta cookie&quot; con il Compositore esperienza avanzato [!UICONTROL Enhanced Experience Composer] a causa di una funzione mancante**: i clienti hanno segnalato che il tentativo di accettare i cookie tramite il Compositore esperienza avanzato ha restituito un errore della console: `handleclickAcceptAllButton is not defined`. La funzionalità di accettazione dei cookie ora funziona come previsto, garantendo un’esperienza più fluida durante la creazione dell’attività nell’interfaccia utente aggiornata. (TGT-52794)
* **La nuova interfaccia utente Compositore esperienza avanzato non è riuscita a caricare alcune pagine precedentemente supportate nell&#39;interfaccia utente legacy**: i clienti hanno segnalato che il nuovo Compositore esperienza avanzato non poteva caricare alcune pagine accessibili nell&#39;interfaccia utente legacy nonostante il codice non compatibile con iframe presente sul sito. Il processo aggiornato di creazione delle attività ora supporta il caricamento di queste pagine, ripristinando la compatibilità per i flussi di lavoro di creazione delle attività. (TGT-53061)
* **Il Compositore esperienza visivo mostrava una schermata bianca vuota durante la modifica delle esperienze**: i clienti di un determinato tenant segnalavano che la schermata del Compositore esperienza visivo era vuota quando si tentava di modificare le esperienze nel Compositore esperienza visivo aggiornato. Questo problema interessava sia le attività nuove che quelle precedenti, impedendo la continuità del flusso di lavoro. Il Compositore esperienza visivo ora si carica correttamente, consentendo ai clienti di modificare le esperienze senza interruzioni. (TGT-53547)
* **Il Compositore esperienza visivo si è verificato un arresto anomalo ed è stata visualizzata una schermata vuota durante il caricamento di alcune attività**: i clienti di un determinato tenant hanno segnalato che il Compositore esperienza visivo non è riuscito a caricare attività specifiche. L’editor esperienze rimaneva bloccato su &quot;Applicazione delle modifiche iniziali&quot; prima dell’arresto anomalo e della visualizzazione di una schermata vuota. Gli errori della console indicano un errore durante la lettura delle proprietà non definite. L’editor ora carica le attività interessate senza errori nel Compositore esperienza visivo aggiornato. (TGT-53548)

+++

## Note aggiuntive e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK]&#x200B;(https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js di [!DNL Adobe Target]. |

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
