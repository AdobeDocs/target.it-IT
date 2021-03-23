---
keywords: Note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di Adobe Target, inclusi SDK, API e librerie JavaScript.
title: Quali nuove funzioni sono incluse nella versione corrente?
feature: Note sulla versione
translation-type: tm+mt
source-git-commit: 9155c487ed078f8af493755a2b4f067eafc8ae68
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 36%

---


# Note sulla versione di Target (corrente)

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, se applicabile, le note sulla versione per API di Target, SDK, libreria JavaScript (at.js) e altre modifiche alla piattaforma.

>[!IMPORTANT]
>
>**Terminazione di mbox.js**: Il 31 marzo 2021 non  [!DNL Adobe Target] supporterà più la libreria mbox.js . Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto positivo sulle pagine che hanno [!DNL Target] attività in esecuzione servendo il contenuto predefinito.
>
>Esegui la migrazione alla versione più recente della nuova [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js prima di questa data per evitare potenziali problemi con i tuoi siti. Per ulteriori informazioni, consulta [Panoramica: implementare Target per web lato client](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

(I codici tra parentesi sono per uso interno di [!DNL Adobe].)

## Modifiche all&#39;indirizzo IP per i server di elaborazione dei feed Recommendations (16 marzo 2021)

Gli indirizzi IP del server di elaborazione dei feed [!DNL Target Recommendations] sono stati aggiornati il 16 marzo 2021. Per ulteriori informazioni, consulta [Indirizzi IP utilizzati dai server di elaborazione dei feed Recommendations](/help/c-recommendations/c-recommendations-faq/ip-addresses-marketing-cloud.md).

## Target Standard/Premium 21.2.1 (9 marzo 2021)

Questa versione di manutenzione contiene i miglioramenti, le correzioni e le modifiche seguenti.

I codici tra parentesi sono per uso interno di [!DNL Adobe].

* È stata aumentata la dimensione dell’offerta consentita (TGT-38304):

   | Tipo | Limite precedente | Nuovo limite |
   | --- | --- | --- |
   | HTML | 256 KB | 1024 KB |
   | Offerte visive dall’interfaccia utente di Target | 64 KB | 1024 KB per ogni esperienza |
   | Tramite API | 512 KB | 1024 KB |

* [!UICONTROL I rapporti ] Approfondimenti personalizzazione per le attività di  [!UICONTROL Targeting automatico]  (AT) e  [!UICONTROL Automated Personalization]  (AP) ora vengono prodotti ogni giorno. Puoi scegliere un rapporto che fornisce [!UICONTROL Segmenti automatizzati] o [!UICONTROL Attributi importanti] per gli ultimi 15, 30 e 60 giorni. Le opzioni di 45 giorni e 90 giorni sono state rimosse per consentire l’esecuzione giornaliera delle altre impostazioni dell’intervallo di lookback. (TGT-39472)
* È stato risolto un problema che impediva la visualizzazione della dipendenza corrente quando i clienti fanno clic su [!UICONTROL Modifica dipendenza] nella pagina [!UICONTROL Obiettivi e impostazioni] di un&#39;attività. (TGT-39340)
* È stato risolto un problema che si verificava durante l&#39;aggiornamento della [!UICONTROL Libreria pubblico] di un&#39;area di lavoro. Prima dell’aggiornamento, vengono visualizzati i tipi di pubblico per l’area di lavoro attualmente selezionata. Dopo l&#39;aggiornamento, vengono visualizzati il [!UICONTROL Area di lavoro predefinita] e i relativi tipi di pubblico. L’area di lavoro corrente e i relativi tipi di pubblico ora persistono dopo l’aggiornamento. (TGT-38871)
* È stato risolto un problema che si verificava durante la copia di un&#39;attività [!UICONTROL Recommendations] e in seguito durante la modifica dell&#39;attività originale modificando la sequenza di criteri. La modifica nella sequenza di criteri nell’attività originale è stata applicata in modo errato anche all’attività copiata. (TGT-39155)
* È stato risolto un problema che causava la visualizzazione di un numero errato di prodotti per le esclusioni [!UICONTROL Recommendations]. (TGT-39599)

## Note aggiuntive sulla versione e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Dettagli sulle versioni di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js [!DNL Adobe Target]. |

## Modifiche alla documentazione, precedenti note sulla versione e note sulla versione di Experience Cloud

Per informazioni aggiuntive, oltre alle note di ciascuna versione, consulta le seguenti risorse:

| Risorsa | Dettagli |
|--- |--- |
| Modifiche alla documentazione | Visualizza informazioni dettagliate sugli aggiornamenti apportati a questa guida che non sono inclusi in queste note sulla versione.<br>Per ulteriori informazioni, consulta [Modifiche alla documentazione](/help/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Note sulla versione per le versioni precedenti | Informazioni su nuove funzionalità e miglioramenti introdotti nelle versioni precedenti di Target Standard e Target Premium.<br>Per ulteriori informazioni, consulta [Note sulla versione per le versioni precedenti](/help/r-release-notes/release-notes-for-previous-releases.md). |
| Note sulla versione di Adobe Experience Cloud | Ultime note sulla versione per le soluzioni Adobe Experience Cloud.<br>Per ulteriori informazioni, consulta  [Experience Cloud Note sulla versione](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html). |

## Informazioni in anteprima {#section_5D588F0415A2435B851A4D0113ACA3A0}

Le risorse seguenti contengono informazioni sulle funzionalità in arrivo con la prossima versione di Target.

| Risorsa | Dettagli |
|--- |--- |
| Adobe di aggiornamento prioritario del prodotto | Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:<br>[](https://www.adobe.com/subscription/priority-product-update.html)https://www.adobe.com/subscription/priority-product-update.html |
| Note sulle prossime versioni | Per informazioni sulle versioni di Target del mese corrente, incluse le informazioni prerelease, consulta la pagina [Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md). |
