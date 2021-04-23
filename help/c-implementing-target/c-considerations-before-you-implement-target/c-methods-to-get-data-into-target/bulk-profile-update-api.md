---
keywords: implementare;implementazione;configurazione;configurazione;aggiornamento bulk profilo
description: Ottieni i dati in  [!DNL Target] utilizzando l'API di aggiornamento collettivo dei profili.
title: Come posso inserire i dati in [!DNL Target] utilizzando l'API di aggiornamento del profilo bulk?
feature: Implementazione
role: Developer
exl-id: 068658fc-7082-425a-87c1-dd0de03cdc71
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 79%

---

# API di aggiornamento del profilo bulk

Tramite API, invia un file .csv a [!DNL Adobe Target] con aggiornamenti del profilo visitatore per molti visitatori. Ogni profilo visitatore può essere aggiornato con più attributi di profilo nella pagina in una chiamata.

Questa opzione è simile agli attributi del cliente con alcune differenze:

* Gli attributi del cliente utilizzano un caricamento FTP mentre l&#39;API di aggiornamento del profilo bulk di Target utilizza un&#39;API HTTP post.
* I dati degli attributi dei clienti possono essere condivisi con Analytics. L&#39;aggiornamento del profilo bulk è utilizzabile solo in Target.
* Gli attributi del cliente supportano la creazione di un profilo per una destinazione utente non ancora visibile. L&#39;API di aggiornamento del profilo bulk aggiorna solo i profili di Target esistenti.
* Gli Attributi cliente richiedono l&#39;utilizzo di Experience Cloud ID (ECID). L&#39;API di aggiornamento del profilo bulk richiede l&#39;ID TNT o `mbox3rdPartyId`.
* Non puoi inviare i seguenti caratteri in `mbox3rdPartyID`: segno più (+) e barra (/).

## Formato

Il file .csv deve fare riferimento a ciascun visitatore tramite il proprio target PCID o mboxThirdPartyId . Experience Cloud ID (ECID) non è supportato. Tutti gli attributi e valori del profilo vengono creati e aggiornati tramite l&#39;API. I dettagli del formato sono disponibili nella documentazione API.

## Esempi di casi d’uso

Il CRM o altro sistema interno archivia dati importanti relativi ai visitatori che si desidera aggiornare costantemente in Target, senza esporre i dati del profilo nell&#39;implementazione della pagina.

## Vantaggi del metodo

Nessun limite al numero di attributi del profilo.

Gli attributi del profilo inviati tramite il sito possono essere aggiornati tramite l&#39;API e viceversa.

## Avvertenze

La dimensione del file batch deve essere inferiore a 50 MB. Inoltre, il numero totale di righe non deve superare 500000 righe per upload.

Non esiste alcun limite al numero o alle righe che è possibile caricare per un periodo di 24 ore nei batch successivi. Tuttavia, il processo di ingestione potrebbe essere limitato durante l&#39;orario di ufficio per garantire che altri processi vengano eseguiti in modo efficiente.

Le [chiamate all’aggiornamento collettivo V2](https://developers.adobetarget.com/api/#updating-profiles) senza chiamate mbox tra gli stessi thirdPartyIds sovrascrivono le proprietà aggiornate nella prima chiamata di aggiornamento collettivo.

## Esempi di codice

Consulta [Aggiornamento di profili](https://developers.adobetarget.com/api/#updating-profiles).

### Link a informazioni rilevanti

[Aggiornamento di profili](https://developers.adobetarget.com/api/#updating-profiles)
