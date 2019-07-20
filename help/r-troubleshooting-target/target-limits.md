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
source-git-commit: 8038b4758e9ce72ff8e43e7427c273aeed734288

---


# Limiti{#limits}

Informazioni sui limiti dei caratteri e altri limiti (dimensioni dell'offerta, pubblico, profili, valori, parametri, ecc.) che influenzano le attività e altri elementi in Adobe Target.

>[!NOTE]
>
>I limiti elencati di seguito devono essere considerati limiti "rigidi", se specificati.
>
>Se si avvicinano o si superano i limiti indicati come «consigliato», le prestazioni possono risultare rallentate. Un rallentamento nei tempi di caricamento dell’interfaccia può essere anche dovuto ad attività molto complesse, ad esempio se un’attività contiene molti tipi di pubblico, obiettivi ed esperienze.
>
>Le attività molto complesse dovrebbero essere esaminate con il coinvolgimento di Adobe Consulting e testate in un ambiente limitato prima di essere rilasciate in un ambiente di produzione.

## Attività

**Limite consigliato**: 10,000 attività attive attive.

**Limite consigliato**: 10,000 attivazioni attive salvate (e non terminate).

## Nomi di attività

**Limite**: 250 caratteri.

## Nomi di pubblico

**Limite**: 256 caratteri.

I valori più lunghi di 256 caratteri vengono troncati.

## Tipi di pubblico

**Limite**: 50 audience per mbox, metrica o esperienza.

## Parametro categoryId

**Limite**: 250 caratteri.

## Nomi di attributi cliente

**Limite**: 128 caratteri.

## ID alias cliente ID

**Limite** 50 caratteri.

## Attributi personalizzati entità

**Limite**: la lunghezza massima dipende dalla lingua.

* 15.000 caratteri (valore singolo, lingue a uno o due byte)
* 500 valori, 100 caratteri per valore (multivalore)

La lunghezza massima degli attributi personalizzati delle entità con valore singolo è di 15,000 caratteri (per i linguaggi con codifica UTF -8 e con codifica UTF -8, ad esempio inglese e altri alfabeti di script latini, oppure 10,000 caratteri (per linguaggi UTF con codifica a tre byte quali cinese, giapponese e coreano).

Gli attributi personalizzati delle entità con più valori possono contenere un massimo di 500 valori. Ogni singolo valore è limitato a 100 caratteri. Il numero totale di caratteri su tutti i valori deve rispettare le limitazioni di lunghezza massima degli attributi personalizzati delle entità a valore singolo (vedi sopra).

## Parametri entityID

**Limite**: 1.000 caratteri.

## excludedIds {#excludedid}

**Limite**: 5 KB per richieste POST. 2.083 caratteri meno la lunghezza dell’URL per le richieste GET.

Per le richieste GET, anche se il limite è di 5 KB, a causa del fatto che Microsoft Internet Explorer limita l’URL a 2.083 caratteri, il limite realistico è di 2.083 caratteri meno la lunghezza corrente dell’URL.

## Nomi di esperienza

**Limite**: 20 caratteri.

## Esperienze per attività

**Limite**: 2,000 esperienze per targeting delle esperienze (XT), test A/B, Test multivariato (MVT) e attività Automatica di Target.

30,000 esperienze per attività Automated Personalization (Personalizzazione automatizzata).

## Valore dell’attributo del profilo In-mbox

**Limite**: 256 caratteri.

I valori più lunghi vengono troncati.

## Profili In-mbox in una richiesta mbox

**Limite**: 50 profili.

Tutti i profili oltre i primi 50 vengono ignorati.

## Nomi di profilo In-mbox

**Limite**: 128 caratteri.

## nomi mbox

**Limite**: 250 caratteri.

## Parametri mbox

**Limite**: i seguenti limiti si applicano ai parametri mbox:

* Parametri mbox: 500 parametri per mbox.
* Parametri profilo: 500 parametri.
* Parametri del profilo per mbox:
* Altri parametri (URL, URL di riferimento e così via): 50 per mbox, per un altro tipo di parametro.

Per i parametri che hanno eseguito l’accesso al database di Target, i limiti indicati sopra si riferiscono per richieste mbox standard. Questi limiti possono essere applicati a meno che la richiesta non venga ridotta a causa di limiti del browser web.

Se utilizzi [l’API di distribuzione in batch](https://developers.adobetarget.com/api/#server-side-batch-delivery)nell’SDK dei Mobile Services, il limite di 50 parametri mbox, 50 parametri del profilo e 50 per altri tipi di parametri sono limitazioni dell’API stessa. Non è possibile inviare una richiesta contenente numeri superiori a questi utilizzando l'API di distribuzione in batch. Se una richiesta supera tali limiti, l’API restituisce il seguente messaggio di errore:“Il numero di mboxParameters non può essere superiore a 100”.

## URL richieste mbox

**Limite**: 2.083 caratteri.

Questo limite è dovuto alle limitazioni sulla lunghezza URL di Microsoft Internet Explorer.

## Parametro mbox3rdPartyId

**Limite**: 60 caratteri.

## Nomi di offerta

**Limite**: 250 caratteri.

## Dimensione offerta

**Limite**: i seguenti limiti di dimensione si applicano alle offerte:

* 256 KB per le offerte HTML.
* 64 KB per le offerte visive dall’interfaccia utente.
* 512 KB dall’API.

Se utilizzi una mbox globale, il limite è per l’intero insieme di contenuti restituiti per la pagina. È utile limitare le dimensioni dell’offerta per migliorare i tempi di caricamento della pagina. Se il limite viene superato, viene visualizzato un messaggio di tipo:

“Il contenuto per l’esperienza è troppo grande per essere consegnato. Modifica l’esperienza in modo da interessare meno codice sulla pagina.”

## Offerte

**Limite consigliato**: 50,000 offerte totali.

## Parametro orderId

**Limite consigliato**: 120 caratteri.

## Parametro orderTotal

**Limite consigliato**: 120 caratteri.

## Parametro productPurchasedId

**Limite**: 47 caratteri per valore separato da virgole.

Qualsiasi valore superiore viene troncato dal sistema.

## Script di profilo

**Limite consigliato**: 300 script di profilo attivi.

**Limite consigliato**: Numero massimo di loop 500,000 per script di profilo.

## Proprietà

**Limite consigliato**: 5,000 proprietà.

## Segnalazione di audience/segmenti

**Limite**: 50 audience/segmenti di reporting per attività.

## Pubblico riutilizzabile per account

**Limite consigliato**: 75 audience.

Nell’interfaccia possono verificarsi timeout di JavaScript in presenza di troppi tipi di pubblico.

## Casella di immissione profilo di script nell’interfaccia utente di Target

**Limite consigliato**: 2,000 caratteri.

Dipende dalla dimensione della stringa codificata, che potrebbe essere molto più lunga della stringa non elaborata. Se la stringa è troppo grande, si verifica un errore prima di raggiungere Adobe Target.

## Nomi di profilo script

**Limite**: 50 caratteri.

## Valori profilo script

**Limite**: 2.048 caratteri.

Per motivi di prestazioni, si consiglia di restituire un valore restituito non superiore ai 256 caratteri.

Per un valore di ritorno Stringa, se la dimensione del valore restituito supera i 2.048 caratteri, il sistema disabilita lo script.

Per un valore di ritorno Array, se la dimensione dei valori concatenati dell’array supera i 2.048 caratteri, il sistema disabilita lo script.

## Metriche di successo

**Limite**: 200 per attività.

## Condizioni Target

**Limite consigliato**: 1,000 valori.

Si riferisce al numero di valori separati da riga nell’area di testo di destinazione. Ad esempio, se si inseriscono 1.000 codici postali in un campo di destinazione CAP.

## Regole di targeting

**Limite consigliato**: 2,500 valori univoci per regola di targeting.

**Limite consigliato**: 30,000 valori univoci per audience nelle regole di targeting.

**Limite consigliato**: 100,000 valori di regole di targeting univoci per attività.
