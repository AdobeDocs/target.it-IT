---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease;early access
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di [!DNL Adobe Target].
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione [!DNL Target] ?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 065220af5c8e3b6cc25ef7289d006a901d2e932a
workflow-type: tm+mt
source-wordcount: '1210'
ht-degree: 15%

---

# Note sulla versione (prerelease) di [!DNL Target]

Questo articolo contiene informazioni prerelease per le prossime versioni di [!DNL Adobe Target], incluse SDK, API e librerie JavaScript.

**Ultimo aggiornamento: 22 luglio 2025**

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
* È stato introdotto un nuovo endpoint API che consente agli utenti di ripristinare da un database secondario le opzioni delle attività precedentemente eliminate. Questa funzionalità sfrutta l&#39;infrastruttura esistente fornita dalle classi `RemovedCampaignElements` e `RemovedOptionInfo`, garantendo la perfetta reintegrazione delle opzioni eliminate nelle attività attive. (TGT-52903)
* È stato risolto un problema nell&#39;interfaccia utente [!DNL Target] aggiornata a causa del quale le offerte eliminate nelle attività [!UICONTROL Automated Personalization] (AP) venivano visualizzate come `Deleted option with ID: X` invece dei nomi originali (ad esempio, `Offer Name [Deleted]` come mostrato nell&#39;interfaccia utente legacy). Questa correzione ripristina un’etichettatura significativa per le offerte eliminate, migliorando la chiarezza e rendendo il reporting più preciso e intuitivo. (TGT-52921)
* È stato risolto un problema nel livello di persistenza back-end a causa del quale le opzioni eliminate venivano memorizzate correttamente ma non erano accessibili tramite gli endpoint API esistenti. Di conseguenza, le applicazioni front-end non sono state in grado di recuperare nomi significativi per le opzioni eliminate, influendo sulle visualizzazioni di reporting storiche. Questa correzione assicura che i dati delle opzioni eliminati conservati possano ora essere visualizzati correttamente nell’interfaccia utente. (TGT-52973)
* È stato risolto un problema a causa del quale alcune attività migrate dal front-end di Target a Target Central presentavano configurazioni di metriche incoerenti a causa di un bug di sincronizzazione precedentemente corretto. In particolare, le attività che originariamente utilizzavano una metrica di conversione e successivamente venivano aggiornate a una metrica basata su Analytics mantenevano valori obsoleti nei campi `primaryMetricType` e `successCriteria`. (TGT-52643)

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
* È stato risolto un problema che impediva l&#39;apertura o la modifica di [!DNL Recommendations] attività contenenti nomi di metriche con più di 25 caratteri a causa di limitazioni API. Questa correzione assicura la compatibilità con i nomi delle metriche che superano il limite di caratteri, ripristinando l’accesso completo alle attività interessate. (TGT-52839)
* È stato risolto un problema che impediva agli utenti di modificare l&#39;attività site_cart_z1 [!DNL Recommendation] nell&#39;interfaccia utente [!DNL Target]. Il tentativo di aprire l&#39;attività ha generato un errore nella pagina [!UICONTROL Overview], bloccando l&#39;accesso all&#39;editor. (TGT-53221)

+++

**Generazione di rapporti**

+++Consulta i dettagli
* È stato risolto un problema che impediva la cancellazione del campo sandbox nel database delle attività quando si cambiava l&#39;origine per la generazione di rapporti da [!DNL Customer Journey Analytics] o [!DNL Analytics] a [!DNL Target]. In precedenza, l’interfaccia utente inviava correttamente sandbox: null, ma il backend ignorava questo valore, lasciando sul posto i dati sandbox obsoleti. Il backend ora cancella correttamente il campo sandbox quando viene ricevuto null. (TGT-52798)
* È stato reimplementato il livello di persistenza delle opzioni eliminate nel backend di Target per supportare rapporti cronologici accurati nelle attività [!UICONTROL Automated Personalization] (AP). In precedenza, quando un’opzione veniva eliminata, il suo nome andava perso, rendendo difficile l’interpretazione dei dati sulle prestazioni passati.

  **Miglioramenti chiave**:

   * Le opzioni eliminate vengono ora tracciate utilizzando l&#39;infrastruttura esistente `RemovedCampaignElements` e `RemovedOptionInfo`.
   * Quando un’opzione viene rimossa da un’attività di Personalizzazione automatizzata, i relativi metadati (ad esempio, ID e nome) vengono mantenuti.
   * L&#39;interfaccia utente di reporting può ora visualizzare il nome dell&#39;opzione originale (ad esempio, `Option Name [Deleted]`) insieme alle metriche cronologiche, migliorando la chiarezza e l&#39;usabilità.

  Questo aggiornamento assicura rapporti coerenti e significativi, anche dopo la rimozione di opzioni da un’attività. (TGT-52986)

* È stato implementato un nuovo endpoint di migrazione per supportare il trasferimento delle opzioni di attività eliminate dalle attività basate su JCR a [!DNL Target] Central. Questa funzionalità consente di eseguire il tracciamento e il reporting in modo coerente tra i sistemi. Questa funzione garantisce che le opzioni eliminate vengano mantenute e sincronizzate nel front-end e nel back-end di [!DNL Target], migliorando l&#39;integrità dei dati e dei report cronologici. (TGT-53217)

+++

**Compositore esperienza visivo**

+++Consulta i dettagli

* È stato risolto un problema nel Compositore esperienza visivo a causa del quale l’applicazione di una modifica a una visualizzazione causava la duplicazione e attivava un errore di tipo &quot;Input utente non valido&quot;. (TGT-52886)
* È stato risolto un problema con la funzionalità [!UICONTROL Undo] per le opzioni [!UICONTROL Insert Before] e [!UICONTROL Insert After] durante la configurazione delle offerte di immagini nel Compositore esperienza visivo.

  In precedenza, l&#39;annullamento di un&#39;azione [!UICONTROL Insert Before] o [!UICONTROL Insert After] sulle offerte di immagini causava un comportamento incoerente o il mancato ripristino corretto della modifica, in particolare nelle attività create nell&#39;interfaccia utente legacy di [!DNL Target]. Questo problema è stato risolto per garantire che le azioni di annullamento ora funzionino in modo affidabile per queste modifiche. (TGT-52809)

* È stato risolto un problema che causava l&#39;impostazione involontaria dell&#39;attributo `contentEditable` su true e persisteva nel contenuto HTML salvato. Questo aggiornamento garantisce un output HTML più pulito e atteso senza un comportamento di modifica non intenzionale. (TGT-52319)
* Per evitare la perdita permanente delle opzioni eliminate e garantire un comportamento coerente tra i servizi, è stata implementata la funzionalità di eliminazione temporanea per le opzioni nell’interfaccia utente e nei microservizi correlati.

  **Modifiche chiave**:

   * Le opzioni non vengono più eliminate definitivamente. Vengono invece contrassegnati con un nuovo flag eliminato: true nell&#39;oggetto XML dei parametri.
   * Questo flag viene utilizzato solo dall&#39;interfaccia utente [!DNL Target] aggiornata per escludere dal rendering le opzioni eliminate e per impedire che vengano inviate ai servizi Edge.
   * Le opzioni eliminate rimangono parte del payload dell’attività durante le modifiche, garantendo la tracciabilità ed evitando la consegna ai clienti di opzioni inesistenti.

  Questo aggiornamento migliora l’integrità dei dati e si allinea alle best practice per la gestione delle eliminazioni nei sistemi distribuiti. (TGT-52726)

+++

**Aree di lavoro**

+++Consulta i dettagli
* È stato risolto un problema che si verificava durante la copia di un’attività da un’area di lavoro non predefinita a quella predefinita o tra aree di lavoro non predefinite. Le offerte ora sono duplicate con funzioni avanzate di tracciamento e denominazione per evitare conflitti.

  **Miglioramenti chiave**:
   * Le offerte vengono ricreate nell’area di lavoro di destinazione con ID e metadati aggiornati.
   * Le offerte copiate vengono rinominate utilizzando il formato: &quot;Copia nome offerta&quot; più un numero casuale o una marca temporale per garantire l’univocità.
   * Il sistema aggiorna gli stati dell’offerta e dell’attività in modo da riflettere i nuovi ID.
   * Questa funzionalità evita gli errori causati da più nomi identici di &quot;Copia offerta&quot; durante le azioni di copia ripetute.
   * Le offerte potrebbero non essere visualizzate immediatamente nell’elenco delle offerte dell’area di lavoro di destinazione, ma vengono elaborate e visualizzate in modo appropriato.

  Questo aggiornamento migliora l’affidabilità e la tracciabilità durante la gestione delle offerte in più aree di lavoro. (TGT-53080)

+++

## Note aggiuntive e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK]&#x200B;(https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js di [!DNL Adobe Target]. |

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
