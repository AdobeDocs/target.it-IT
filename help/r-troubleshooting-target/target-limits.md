---
description: Informazioni sui limiti dei caratteri e altri limiti (dimensioni dell'offerta, pubblico, profili, valori, parametri, ecc.) che influenzano le attività e altri elementi in Adobe Target.
keywords: limite di caratteri;parametri mbox;api di distribuzione in batch;parametri di profilo;limiti;profili incorporati;numero massimo;limite;vincolo;carattere;buona prassi; orderid;orderTotal;mbox3rdPartyID;categoria;categoryID
seo-description: Informazioni sui limiti dei caratteri e altri limiti (dimensioni dell'offerta, pubblico, profili, valori, parametri, ecc.) che influenzano le attività e altri elementi in Adobe Target.
seo-title: Limiti
solution: Target
title: Limiti
topic: Standard
uuid: 603fb800-a26c-43ec-b2d9-ef7a8ed8721e
translation-type: tm+mt
source-git-commit: 5e8edb25f0b0255247c535bcac1d960b6e8acf94

---


# Limiti{#limits}

Informazioni sui limiti dei caratteri e altri limiti (dimensioni dell&#39;offerta, pubblico, profili, valori, parametri, ecc.) che influenzano le attività e altri elementi in Adobe Target.

I limiti indicati di seguito sono i limiti consigliati. Quando si raggiungono o superano tali limiti, le prestazioni possono degradarsi. Un rallentamento nei tempi di caricamento dell’interfaccia può essere anche dovuto ad attività molto complesse, ad esempio se un’attività contiene molti tipi di pubblico, obiettivi ed esperienze.

Le attività molto complesse dovrebbero essere esaminate con il coinvolgimento di Adobe Consulting e testate in un ambiente limitato prima di essere rilasciate in un ambiente di produzione.

## Nomi delle attività

**Limite**: 250 caratteri.

## Nomi dei destinatari

**Limite**: 256 caratteri.

I valori più lunghi di 256 caratteri vengono troncati.

## Parametro categoryId

**Limite**: 250 caratteri.

## Nomi degli attributi cliente

**Limite**: 128 caratteri.

## ID alias cliente ID

**Limite** 50 caratteri.

## Attributi personalizzati entità

**Limite**: La lunghezza massima dipende dalla lingua.

* 15,000 caratteri (a un valore singolo, a una e a due byte)
* 500 valori, 100 caratteri per valore (più valori)

La lunghezza massima degli attributi personalizzati delle entità con valore singolo è di 15,000 caratteri (per linguaggi UTF -8 con codifica singola, ad esempio inglese e altri alfabeti latini di script) oppure 10,000 caratteri (per linguaggi UTF -8 con codifica UTF quali cinese, giapponese e coreano).

Gli attributi personalizzati delle entità con più valori possono contenere un massimo di 500 valori. Ogni singolo valore è limitato a 100 caratteri. Il numero totale di caratteri su tutti i valori deve rispettare le limitazioni per la lunghezza massima degli attributi personalizzati delle entità a valore singolo (vedi sopra).

## Parametri entityid

**Limite**: 1,000 caratteri.

## Excludedids {#excludedid}

**Limite**: 5 KB per richieste POST. 2,083 caratteri meno la lunghezza dell&#39;URL per le richieste GET.

Per le richieste GET, anche se il limite è di 5 KB, a causa del fatto che Microsoft Internet Explorer limita l&#39;URL a 2,083 caratteri, il limite realistico è di 2,083 caratteri meno la lunghezza corrente dell&#39;URL.

## Nomi delle esperienze

**Limite**: 20 caratteri.

## Valore attributo di profilo in-mbox

**Limite**: 256 caratteri.

I valori più lunghi vengono troncati.

## Profili in-mbox in una richiesta mbox

**Limite**: 50 profili.

Tutti i profili oltre i primi 50 vengono ignorati.

## Nomi dei profili in-mbox

**Limite**: 128 caratteri.

## nomi mbox

**Limite**: 250 caratteri.

## Parametri mbox

**Limite**: I limiti seguenti si applicano ai parametri mbox:

* parametri mbox: 500 parametri per mbox.
* Parametri profilo: 500 parametri.
* Parametri del profilo per mbox:
* Altri parametri (URL, URL di riferimento e così via): 50 per mbox, per un altro tipo di parametro.

Per i parametri che hanno eseguito l&#39;accesso al database di Target, i limiti indicati sopra sono per richieste mbox standard. Questi limiti possono essere applicati a meno che la richiesta non venga ridotta a causa di limiti del browser web.

Se utilizzi [l’API di distribuzione in batch](https://developers.adobetarget.com/api/#server-side-batch-delivery)nell’SDK dei Mobile Services, il limite di 50 parametri mbox, 50 parametri del profilo e 50 per altri tipi di parametri sono limitazioni dell’API stessa. Non è possibile inviare una richiesta contenente numeri superiori a questi utilizzando l&#39;API di distribuzione in batch. Se una richiesta supera tali limiti, l’API restituisce il seguente messaggio di errore:“Il numero di mboxParameters non può essere superiore a 100”.

## URL di richiesta mbox

**Limite**: 2,083 caratteri.

Questo limite è dovuto alle limitazioni sulla lunghezza URL di Microsoft Internet Explorer.

## Parametro mbox3rdPartyId

**Limite**: 60 caratteri.

## Nomi delle offerte

**Limite**: 250 caratteri.

## Dimensione offerta

**Limite**: I limiti di dimensione seguenti si applicano alle offerte:

* 256 KB per le offerte HTML.
* 64 KB per le offerte visive dall’interfaccia utente.
* 512 KB dall’API.

Se utilizzate una mbox globale, il limite è relativo all&#39;intero set di contenuto restituito per la pagina. È utile limitare le dimensioni dell’offerta per migliorare i tempi di caricamento della pagina. Se il limite viene superato, viene visualizzato un messaggio di tipo:

“Il contenuto per l’esperienza è troppo grande per essere consegnato. Modifica l’esperienza in modo da interessare meno codice sulla pagina.”

## Parametro orderId

**Limite**: 120 caratteri.

Limite consigliato.

## Parametro orderTotal

**Limite**: 120 caratteri.

Limite consigliato.

## Parametro productPurchasedId

**Limite**: 47 caratteri per valore separato da virgole.

Tutto il sistema viene troncato.

## Pubblico riutilizzabile per account

**Limite**: 75 audience.

Limite consigliato. Nell’interfaccia possono verificarsi timeout di JavaScript in presenza di troppi tipi di pubblico.

## Casella di immissione profilo di script nell&#39;interfaccia di Target

**Limite**: 2,000 caratteri.

Limite consigliato. Dipende dalla dimensione della stringa codificata, che potrebbe essere molto più lunga della stringa non elaborata. Se la stringa è troppo grande, si verifica un errore prima di raggiungere Adobe Target.

## Nomi dei profili di script

**Limite**: 50 caratteri.

## Valori del profilo di script

**Limite**: 2,048 caratteri.

Per motivi di prestazioni, si consiglia di restituire un valore restituito non superiore ai 256 caratteri.

Per un valore restituito stringa, se la dimensione del valore restituito supera i 2,048 caratteri, lo script viene disabilitato dal sistema.

Per un valore restituito array, se la dimensione dei valori concatenati dell&#39;array supera 2,048 caratteri, lo script viene disabilitato dal sistema.

## Condizioni di Target

**Limite**: 1,000 valori.

Limite consigliato. Si riferisce al numero di valori separati da riga nell’area di testo di destinazione. Ad esempio, se si inseriscono 1.000 codici postali in un campo di destinazione CAP.