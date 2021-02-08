---
keywords: limite di caratteri;parametri mbox;batch delivery api;parametri di profilo;limits;incorporati in profili;massimo;limite;vincolo;carattere;best practice;orderTotal;mbox3rdPartyID;category;categoryID;risoluzione dei problemi
description: Visualizzare un elenco di limiti di caratteri e altri limiti (dimensioni dell’offerta, audience, profili, valori, parametri, ecc.) che influenzano le attività e altri elementi in Adobe Target.
title: Rivedete un elenco di limiti di caratteri e altri limiti (dimensioni dell’offerta, audience, profili, valori, parametri, ecc.) che influenzano le attività e altri elementi in Adobe Target.
feature: Troubleshooting
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 67%

---


# Limiti

Informazioni sui limiti dei caratteri e altri limiti (dimensioni dell&#39;offerta, pubblico, profili, valori, parametri, ecc.) che influenzano le attività e altri elementi in [!DNL Adobe Target].

>[!NOTE]
>
>I limiti elencati di seguito devono essere considerati come limiti “rigorosi”, a meno che non sia indicato “consigliato”.
>
>Quando si raggiungono i superano i limiti indicati come “consigliati”, si può verificare un deterioramento delle prestazioni. Un rallentamento nei tempi di caricamento dell’interfaccia può essere anche dovuto ad attività molto complesse, ad esempio se un’attività contiene molti tipi di pubblico, obiettivi ed esperienze.
>
>Le attività altamente complesse dovrebbero essere riviste con la [!DNL Adobe] Consulenza e collaudate in un ambiente limitato prima di essere immesse in produzione.

## Attività

**Limite consigliato**: 10.000 attività live attive.

**Limite** consigliato: 10.000 attività salvate (e non finite) attive.

## Nomi di attività

**Limite**: 250 caratteri.

## Nomi di pubblico

**Limite**: 255 caratteri.

## Tipi di pubblico

**Limite**: 50 tipi di pubblico per mbox, metrica o esperienza.

## Pubblico, riutilizzabile per account

**Limite consigliato**: 20,000 tipi di pubblico.

## Parametro categoryId

**Limite**: 128 caratteri.

## Nomi di attributi cliente

**Limite**: 250 caratteri tramite feed o API.

## ID alias di attributo cliente

**Limite**: 50 caratteri.

## Attributi del cliente, caricamento

* **Dimensione massima per ciascun caricamento mediante il metodo** HTTP: 100 MB.
* **dimensione massima del file per ogni caricamento mediante il metodo** FTP: 4 GB
* **Numero di attributi consentiti per la sottoscrizione**: 5 for  [!DNL Target Standard] e 200 for  [!DNL Target Premium].

## Entità

Il numero massimo di entità a cui puoi fare riferimento in una progettazione, tramite codifica fissa o cicli, è 99.

## Attributi personalizzati entità

Potete includere fino a 100 attributi di entità personalizzati

**Limite**: La lunghezza massima dei caratteri dipende dalla lingua.

* 15.000 caratteri (valore singolo, lingue a uno o due byte)
* 500 valori, 100 caratteri per valore (multivalore)

La lunghezza massima degli attributi personalizzati delle entità con valore singolo è di 15.000 caratteri (per lingue con codifica UTF-8 a uno e due byte, come inglese e altre lingue basate su alfabeto latino) oppure 10.000 caratteri (per lingue con codifica UTF-8 a tre byte come cinese, giapponese e coreano).

Gli attributi personalizzati delle entità con più valori possono contenere un massimo di 500 valori. Ogni singolo valore è limitato a 100 caratteri. Il numero totale di caratteri su tutti i valori deve rispettare le limitazioni di lunghezza massima degli attributi personalizzati delle entità a valore singolo (vedi sopra).

## Parametri entityID

**Limite**: 1.000 caratteri.

## excludedIds {#excludedid}

**Limite**: 5 KB per richieste POST. 2.083 caratteri meno la lunghezza dell’URL per le richieste GET.

Per le richieste GET, anche se il limite è di 5 KB, a causa del fatto che Microsoft Internet Explorer limita l’URL a 2.083 caratteri, il limite realistico è di 2.083 caratteri meno la lunghezza corrente dell’URL.

## Nomi di esperienza

**Limite**: 50 caratteri.

## Esperienze per attività

**Limite**: 2.000 esperienze per attività Targeting esperienza, Test A/B, Test multivariato (MVT) e Targeting automatico.

30.000 esperienze per attività Personalizzazione automatizzata.

## Valore dell’attributo del profilo In-mbox

**Limite**: 256 caratteri.

I valori più lunghi vengono troncati.

## Nomi di profilo In-mbox

**Limite**: 128 caratteri.

## nomi mbox

**Limite**: 250 caratteri.

## Parametri mbox

**Limite**: i seguenti limiti si applicano ai parametri mbox:

Per le chiamate mbox standard:
* Parametri mbox: 500 parametri per mbox.
* Parametri profilo: 500 parametri di profilo per mbox.
* Altri parametri (URL, URL di riferimento e così via): 50 per mbox, per un altro tipo di parametro.

Questi limiti possono essere applicati a meno che la richiesta non venga ridotta a causa di limiti del browser web.

Se utilizzate l&#39;API di consegna batch, il limite è di 50 mbox per ogni richiesta batch.

Se utilizzi [l’API di distribuzione in batch](https://developers.adobetarget.com/api/#server-side-batch-delivery)nell’SDK dei Mobile Services, il limite di 50 parametri mbox, 50 parametri del profilo e 50 per altri tipi di parametri sono limitazioni dell’API stessa. Non è possibile inviare una richiesta contenente numeri superiori a questi utilizzando l&#39;API di distribuzione in batch. Se una richiesta contiene più di questi limiti, l&#39;API restituirà il seguente messaggio di errore:

&quot;Il numero di mboxParameters non può superare 50.&quot;

Limiti impostati per gli endpoint:

Mbox batch v2:
* parametri mbox 100
* nome parametro mbox max 128
* il valore del parametro mbox non può essere null
* valore del parametro mbox 5000
* parametri di profilo 50
* nome del parametro del profilo lunghezza max 128
* il valore del parametro del profilo non può essere null
* valore del parametro del profilo lunghezza massima 256

Endpoint API di consegna
* parametri mbox 50
* nome parametro mbox max 128
* il valore del parametro mbox non può essere null
* valore del parametro mbox 5000
* parametri di profilo 50
* nome del parametro del profilo lunghezza max 128
* il valore del parametro del profilo non può essere null
* valore del parametro del profilo lunghezza massima 256

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

**Limite consigliato**: 50.000 offerte totali.

## Parametro orderId

**Limite consigliato**: 120 caratteri.

## Parametro orderTotal

**Limite consigliato**: 120 caratteri.

## Parametro productPurchasedId

**Limite**: 47 caratteri per il valore separato da virgole e 250 caratteri in totale. I singoli valori superiori a 47 caratteri possono essere troncati dal sistema. Le lunghezze totali superiori a 250 caratteri possono causare un errore 400.

## Script di profilo

**Limite consigliato di script** di profilo attivi: 300

**Limite consigliato di script di profilo totali per account**: 2.000

**Recommendations per limitare la complessità** degli script di profilo: Gli script di profilo possono eseguire un numero limitato di istruzioni. Per ulteriori informazioni, vedere [Best practice](/help/c-target/c-visitor-profile/profile-parameters.md#best) in *Attributi del profilo*.

## Proprietà

**Limite consigliato**: 5.000 proprietà.

## Tipi di pubblico/Segmenti di reporting

**Limite**: 50 tipi di pubblico/segmenti di reporting per attività.

## Casella di immissione profilo di script nell’interfaccia utente di Target

**Limite consigliato**: 2.000 caratteri.

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

## Condizioni di destinazione

**Limite consigliato**: 1.000 valori.

Si riferisce al numero di valori separati da riga nell’area di testo di destinazione. Ad esempio, se si inseriscono 1.000 codici postali in un campo di destinazione CAP.

## Regole di targeting

**Limite** consigliato: 2.500 caratteri per valore della regola di targeting.

**Limite consigliato**: 30.000 valori univoci per pubblico in tutte le regole di targeting.

**Limite consigliato**: 100.000 valori di regole di targeting univoci per attività.

