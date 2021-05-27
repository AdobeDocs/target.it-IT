---
keywords: limite di caratteri;parametri mbox;api di distribuzione in batch;parametri di profilo;limiti;profili incorporati;numero massimo;limite;vincolo;carattere;best practice; orderid;orderTotal;mbox3rdPartyID;categoria;categoryID;risoluzione dei problemi
description: Visualizza una lista sui limiti dei caratteri e altri limiti (dimensioni dell’offerta, pubblico, profili, valori, parametri, ecc.) che influenzano le attività e altri elementi in Adobe Target.
title: Quali sono i vari caratteri, dimensioni e altri limiti in Adobe Target?
feature: Risoluzione dei problemi relativi al
mini-toc-levels: 3
exl-id: b318ab16-1382-4f3a-8764-064adf384d6b
source-git-commit: ef524775dc64e00e75f05c48534a0f8dd57fa705
workflow-type: tm+mt
source-wordcount: '1184'
ht-degree: 90%

---

# Limiti

Limiti dei caratteri e altri limiti (dimensioni dell’offerta, pubblico, profili, valori, parametri, ecc.) che influenzano le attività e altri elementi in [!DNL Adobe Target].

>[!NOTE]
>
>I limiti elencati di seguito devono essere considerati come limiti “rigorosi”, a meno che non sia indicato “consigliato”.
>
>Quando si raggiungono i superano i limiti indicati come “consigliati”, si può verificare un deterioramento delle prestazioni. Un rallentamento nei tempi di caricamento dell’interfaccia può essere anche dovuto ad attività molto complesse, ad esempio se un’attività contiene molti tipi di pubblico, obiettivi ed esperienze.
>
>Le attività molto complesse dovrebbero essere esaminate con consulenza [!DNL Adobe] e testate in un ambiente limitato prima di essere rilasciate in un ambiente di produzione.

## Attività

### Nomi di attività

* **Limite**: 250 caratteri.

### Numero di attività per account

* **Limite consigliato**: 10.000 attività live attive.

* **Limite consigliato**: 10.000 attività salvate (e non terminate) primarie.

## Chiamate API di Target

* **Limite**: 50 chiamate al minuto.

   Se effettui più di 50 chiamate API al minuto, [!DNL Target] restituisce un messaggio di errore &quot;503 HTTP status&quot;.

## Tipi di pubblico

### Nomi di pubblico

* **Limite**: 255 caratteri.

### Tipi di pubblico riutilizzabili per account

* **Limite consigliato**: 20,000 tipi di pubblico.

### Numero di tipi di pubblico per mbox, metrica ed esperienza

* **Limite**: 50 spettatori

## Parametro categoryId

* **Limite**: 250 caratteri.

## Attributi del cliente

### Nomi di attributi cliente

* **Limite**: 250 caratteri tramite feed o API.

### ID alias di attributo cliente

* **Limite**: 50 caratteri.

### Attributi del cliente, caricamento

* **Dimensione massima del file per ogni caricamento tramite il metodo HTTP**: 100 MB.
* **Dimensione massima del file per ogni caricamento tramite il metodo FTP**: 4 GB.
* **Numero di attributi ammessi per la sottoscrizione**: 5 per [!DNL Target Standard] e 200 per [!DNL Target Premium].

## Entità

### Numero di entità

* Il numero massimo di entità a cui puoi fare riferimento in una progettazione, tramite codifica fissa o cicli, è 99.
* Il limite consigliato per le migliori prestazioni è quello di mantenere il catalogo con meno di un milione di elementi per ambiente e meno di dieci milioni di elementi per tutti gli ambienti.
* Il limite massimo è di dieci milioni di elementi per ambiente e 100 milioni di elementi per tutti gli ambienti. Se hai tra un milione e dieci milioni di elementi per ambiente, le prestazioni dell&#39;interfaccia utente [!UICONTROL Ricerca nel catalogo] sono influenzate. [!DNL Target Recommendations]Tuttavia, continua a produrre e a fornire raccomandazioni.

### Attributi personalizzati entità

* **Attributi di entità personalizzati**: 100.

* **Limite carattere**: la lunghezza massima dipende dalla lingua.

   * 15.000 caratteri (valore singolo, lingue a uno o due byte)
   * 500 valori, 100 caratteri per valore (multivalore)

   La lunghezza massima degli attributi personalizzati delle entità con valore singolo è di 15.000 caratteri (per lingue con codifica UTF-8 a uno e due byte, come inglese e altre lingue basate su alfabeto latino) oppure 10.000 caratteri (per lingue con codifica UTF-8 a tre byte come cinese, giapponese e coreano).

   Gli attributi personalizzati delle entità con più valori possono contenere un massimo di 500 valori. Ogni singolo valore è limitato a 100 caratteri. Il numero totale di caratteri su tutti i valori deve rispettare le limitazioni di lunghezza massima degli attributi personalizzati delle entità a valore singolo (vedi sopra).

### Parametri entityID

* **Limite**: 1.000 caratteri.

## excludedIds {#excludedid}

* **Limite**: 5 KB per richieste POST. 2.083 caratteri meno la lunghezza dell’URL per le richieste GET.

   Per le richieste GET, anche se il limite è di 5 KB, a causa del fatto che Microsoft Internet Explorer limita l’URL a 2.083 caratteri, il limite realistico è di 2.083 caratteri meno la lunghezza corrente dell’URL.

## Esperienze

### Nomi di esperienza

* **Limite**: 50 caratteri.

### Esperienze per attività

* **Limite**: 2.000 esperienze per attività Targeting esperienza, Test A/B, Test multivariato (MVT) e Targeting automatico.

   30.000 esperienze per attività Automated Personalization.

## mbox

### Valore dell’attributo del profilo In-mbox

* **Limite**: 256 caratteri.

   I valori più lunghi vengono troncati.

### Nomi di profilo In-mbox

* **Limite**: 128 caratteri.

### nomi mbox

* **Limite**: 250 caratteri.

### Parametri mbox

* **Limite**: i seguenti limiti si applicano ai parametri mbox:

   Per le chiamate mbox standard:

   * Parametri mbox: 500 parametri per mbox.
   * Parametri profilo: 500 parametri profilo per mbox.
   * Altri parametri (URL, URL di riferimento e così via): 50 per mbox, per un altro tipo di parametro.

   Questi limiti possono essere applicati a meno che la richiesta non venga ridotta a causa di limiti del browser web.

   Se utilizzi l’API di distribuzione in batch, il limite è 50 mbox per richiesta batch.

   Se utilizzi [l’API di distribuzione in batch](https://developers.adobetarget.com/api/#server-side-batch-delivery) nell’SDK dei Mobile Services, il limite di 50 parametri mbox, 50 parametri del profilo e 50 per altri tipi di parametri sono limitazioni dell’API stessa. Non è possibile inviare una richiesta contenente numeri superiori a questi utilizzando l&#39;API di distribuzione in batch. Se una richiesta supera tali limiti, l’API restituisce il seguente messaggio di errore:

   “Il numero di mboxParameters non può essere superiore a 50”.

   Limiti impostati per gli endpoint:

   **Batch mbox v2**:

   * Parametri mbox: 100
   * Lunghezza massima del nome del parametro mbox: 128
   * Il valore del parametro mbox non può essere null
   * Valore del parametro mbox: 5000
   * Parametri del profilo: 50
   * Lunghezza massima del nome del parametro: 128
   * Il valore del parametro di profilo non può essere null
   * Lunghezza massima valore del parametro del profilo: 256

   **Endpoint API di consegna**:

   * Parametri mbox: 50
   * Lunghezza massima del nome del parametro mbox: 128
   * Il valore del parametro mbox non può essere null
   * Valore del parametro mbox: 5000
   * Parametri del profilo: 50
   * Lunghezza massima del nome del parametro: 128
   * Il valore del parametro di profilo non può essere null
   * Lunghezza massima valore del parametro del profilo: 256



### URL richieste mbox

* **Limite**: 2.083 caratteri.

   Questo limite è dovuto alle limitazioni sulla lunghezza URL di Microsoft Internet Explorer.

### Parametro mbox3rdPartyId

* **Limite**: 60 caratteri.

## Offerte

### Nomi di offerta

* **Limite**: 250 caratteri.

### Numero di offerte

* **Limite consigliato**: 50.000 offerte totali.

### Dimensione offerta {#offer-size}

I seguenti limiti di dimensione si applicano alle offerte:

* 1024 KB per le offerte HTML.
* 1024 KB (per ogni esperienza) per le offerte visive dall’interfaccia utente.
* 1024 KB dall’API.

   Se utilizzi una mbox globale, il limite è per l’intero insieme di contenuti restituiti per la pagina. È utile limitare le dimensioni dell’offerta per migliorare i tempi di caricamento della pagina. Se il limite viene superato, viene visualizzato un messaggio di tipo:

   “Il contenuto per l’esperienza è troppo grande per essere consegnato. Modifica l’esperienza in modo da interessare meno codice sulla pagina.”

## Parametro orderId

* **Limite consigliato**: 120 caratteri.

## Parametro orderTotal

* **Limite consigliato**: 120 caratteri.

## Parametro productPurchasedId

* **Limite**: 47 caratteri per valore separato da virgole e 250 caratteri in totale. I singoli valori più lunghi di 47 caratteri possono essere troncati dal sistema. Le lunghezze totali superiori a 250 caratteri possono causare un errore 400.

## Script di profilo

* **Limite consigliato per gli script di profilo attivi (quelli abilitati)**: 300

* **Limite consigliato di script di profilo totali per account**: 2.000

* **Raccomandazioni per limitare la complessità degli script di profilo**: gli script di profilo possono eseguire un numero limitato di istruzioni. Per ulteriori informazioni, consulta [Best practice](/help/c-target/c-visitor-profile/profile-parameters.md#best) in *Attributi del profilo*.

## Proprietà

* **Limite consigliato**: 5.000 proprietà.

## Tipi di pubblico/Segmenti di reporting

* **Limite**: 50 tipi di pubblico/segmenti di reporting per attività.

## Casella di immissione profilo script nell’ interfaccia utente [!DNL Target]

* **Limite consigliato**: 2.000 caratteri.

   Dipende dalla dimensione della stringa codificata, che potrebbe essere molto più lunga della stringa non elaborata. Se la stringa è troppo grande, si verifica un errore prima di raggiungere Adobe Target.

## Profili script

### Nomi di profilo script

* **Limite**: 50 caratteri.

### Valori profilo script

* **Limite**: 2.048 caratteri.

   Per motivi di prestazioni, si consiglia di restituire un valore restituito non superiore ai 256 caratteri.

   Per un valore di ritorno Stringa, se la dimensione del valore restituito supera i 2.048 caratteri, il sistema disabilita lo script.

   Per un valore di ritorno Array, se la dimensione dei valori concatenati dell’array supera i 2.048 caratteri, il sistema disabilita lo script.

## Metriche di successo

* **Limite**: 200 per attività.

## Targeting

### Condizioni di destinazione

* **Limite consigliato**: 1.000 valori.

   Si riferisce al numero di valori separati da riga nell’area di testo di destinazione. Ad esempio, se si inseriscono 1.000 codici postali in un campo di destinazione CAP.

### Regole di targeting

* **Limite consigliato**: 2.500 caratteri per valore della regola di targeting.
* **Limite consigliato**: 30.000 valori univoci per pubblico in tutte le regole di targeting.
* **Limite consigliato**: 100.000 valori di regole di targeting univoci per attività.
