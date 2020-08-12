---
keywords: implement;implementing;setting up;setup;page parameter;tomcat;url encoded;in-page profile attribute;mbox parameter;in-page profile attributes;script profile attribute;bulk profile update API;single file update API;customer attributes;data providers;dataprovider;data provider
description: Informazioni sui vari metodi possibili per ottenere i dati in Target, inclusi parametri di pagina, attributi di profilo nella pagina, attributi di profilo script, fornitori dei dati, API di aggiornamento collettivo dei profili, API di aggiornamento di singoli profili e attributi dei clienti.
title: Metodi per immettere i dati in Target
feature: null
subtopic: Getting Started
topic: Standard
uuid: a6d64e39-6cdc-49fe-afe5-ecf7dcacf97d
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '1940'
ht-degree: 96%

---


# Metodi per immettere i dati in Target{#methods-to-get-data-into-target}

Informazioni sui diversi metodi possibili per ottenere i dati in Target, inclusi parametri di pagina, attributi di profilo nella pagina, attributi di profilo script, fornitori dei dati, API di aggiornamento collettivo dei profili, API di aggiornamento di singoli profili e attributi dei clienti.

## Parametri di pagina (detti anche “parametri mbox”){#section_5A297816173C4FE48DC4FE03860CB42B}

I parametri di pagina sono coppie di nome e valore passate direttamente tramite codice di pagina che non sono memorizzati nel profilo del visitatore per un utilizzo futuro.

I parametri di pagina sono utili per inviare ulteriori dati di pagina alla destinazione che non devono essere memorizzati con il profilo del visitatore per un futuro targeting. Questi valori vengono invece utilizzati per descrivere la pagina o l&#39;azione che l&#39;utente ha assunto nella pagina specifica.

### Formato

I parametri di pagina vengono passati alla destinazione tramite una chiamata al server come stringa di coppia nome e valore. I nomi dei parametri e i valori sono personalizzabili (anche se ci sono alcuni “nomi riservati” per usi specifici).

Esempi:

* `page=productPage`

* `categoryId=homeLoans`

### Esempi di casi d&#39;uso

**Pagine dei prodotti**: invia informazioni sul prodotto specifico visualizzato (questo è il modo in cui funzionano i consigli)

**Dettagli ordine**: invia ID ordine, orderTotal e così via per la raccolta dell’ordine

**Affinità tra categorie**: invia informazioni visualizzate per categoria a Target per conoscere l’affinità dell’utente a particolari categorie di siti

**Dati di terze parti**: invia informazioni da fonti di dati di terze parti, ad esempio i provider di targeting del meteo, i dati dell’account (DemandBase), i dati demografici (ad esempio Experian) e altro ancora.

### Vantaggi del metodo

I dati vengono inviati a Target in tempo reale e possono essere utilizzati sulla stessa chiamata server su cui entrano i dati.

### Avvertenze

* Richiede l&#39;aggiornamento del codice della pagina (direttamente o tramite un sistema di gestione dei tag).
* Se i dati devono essere utilizzati per la destinazione di una successiva chiamata di pagina/server, è necessario tradurli in uno script di profilo.
* Le stringhe di query possono contenere solo caratteri che rispettano lo [standard Internet Engineering Task Force (IETF)](https://www.ietf.org/rfc/rfc3986.txt).

   Oltre a quelli menzionati sul sito di IETF, Target consente l’utilizzo dei seguenti caratteri nelle stringhe di query:

   `&lt; > # % ” { } | \\ ^ \[\] \``

   Tutto il resto deve avere la codifica URL. The standard specifies the following format ( [https://www.ietf.org/rfc/rfc1738.txt](https://www.ietf.org/rfc/rfc1738.txt) ), as illustrated below:

   ![](assets/ietf1.png)

   Oppure, l&#39;elenco completo per semplicità:

   ![](assets/ietf2.png)

### Esempi di codice

targetPageParamsAll (aggiunge i parametri a tutte le chiamate mbox nella pagina):

`function targetPageParamsAll() { return "param1=value1&param2=value2&p3=hello%20world";`

targetPageParams (aggiunge i parametri alla MBOX globale nella pagina):

`function targetPageParams() { return "param1=value1&param2=value2&p3=hello%20world";`

Parametri nel codice mboxCreate:

`<div class="mboxDefault"> default content to replace by offer </div> <script> mboxCreate('mboxName','param1=value1','param2=value2'); </script>`

### Link a informazioni rilevanti

Consigli: [Implementazione in base al tipo di pagina](/help/c-recommendations/plan-implement.md#reference_DE38BB07BD3C4511B176CDAB45E126FC)

Conferma ordine: [Tracciare le conversioni](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#task_E85D2F64FEB84201A594F2288FABF053)

Affinità tra categorie: [Affinità tra categorie](/help/c-target/c-visitor-profile/category-affinity.md#concept_75EC1E1123014448B8B92AD16B2D72CC)

## Attributi di profilo nella pagina (detti anche “attributi di profilo nella mbox”){#section_57E1C161AA7B444689B40B6F459302B6}

Gli attributi di profilo nella pagina sono coppie di nome e valore passate direttamente tramite il codice della pagina archiviato nel profilo del visitatore per un utilizzo futuro.

Gli attributi di profilo nella pagina consentono l&#39;archiviazione dei dati specifici dell&#39;utente nel profilo di Target per targeting e segmentazione in un secondo momento.

### Formato

Gli attributi di profilo nella pagina vengono passati a Target tramite una chiamata al server come stringa di coppia di nome e valore con il prefisso “profile.” prima del nome dell&#39;attributo.

I nomi e i valori degli attributi sono personalizzabili (sebbene esistano alcuni “nomi riservati” per usi specifici).

Esempi:

* `profile.membershipLevel=silver`
* `profile.visitCount=3`

### Esempi di casi d&#39;uso

**Informazioni di login**: condividi dati non-PII (personalmente identificabili) con Target in base al login dell’utente. Questo potrebbe essere status di appartenenza, cronologia degli ordini, ecc.

**Informazioni sul negozio**: tracciare quale negozio è la posizione preferita dell’utente.

**Interazioni precedenti**: tenere traccia di ciò che l’utente ha fatto precedentemente sul sito per informare le future personalizzazioni.

### Vantaggi del metodo

I dati vengono inviati a Target in tempo reale e possono essere utilizzati sulla stessa chiamata server su cui entrano i dati.

### Avvertenze

Richiede aggiornamenti del codice della pagina (direttamente o tramite un sistema di gestione dei tag).

Gli attributi e i valori sono visibili nelle chiamate al server, pertanto un visitatore può visualizzare i valori. Se si condividono informazioni quali le gamme di credito o altre informazioni potenzialmente private, questo potrebbe non essere l&#39;approccio migliore.

### Esempi di codice

targetPageParamsAll (aggiunge gli attributi a tutte le chiamate mbox nella pagina):

`function targetPageParamsAll() { return "profile.param1=value1&profile.param2=value2&profile.p3=hello%20world"; }`

targetPageParams (aggiunge gli attributi alla mbox globale nella pagina):

`function targetPageParams() { return profile.param1=value1&profile.param2=value2&profile.p3=hello%20world"; }`

Attributi nel codice mboxCreate:

`<div class="mboxDefault"> default content to replace by offer </div> <script> mboxCreate('mboxName','profile.param1=value1','profile.param2=value2'); </script>`

### Link a informazioni rilevanti

[Attributi del profilo](/help/c-target/c-visitor-profile/profile-parameters.md#concept_01A30B4762D64CD5946B3AA38DC8A201)

[Profilo visitatore](/help/c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E)

## Attributi di profilo script {#section_3E27B58C841448C38BDDCFE943984F8D}

Gli attributi di profilo script sono coppie di nome e valore definite nella soluzione di Target. Il valore è determinato dall&#39;esecuzione di un frammento JavaScript sul server di destinazione per ogni chiamata del server.

Gli utenti scrivono frammenti di codice di piccole dimensioni che vengono eseguiti per chiamata mbox e prima che un visitatore venga valutato per l&#39;appartenenza al pubblico e all&#39;attività.

### Formato

Gli attributi di profilo script vengono creati nella sezione Tipi di pubblico di Target. Qualsiasi nome di attributo è valido e il valore è il risultato di una funzione JavaScript scritta dall&#39;utente di Target. Il nome dell&#39;attributo viene automaticamente preceduto da “user. ” in Target per distinguerlo dagli attributi di profilo nella pagina.

Il frammento di codice è scritto nel linguaggio Rhino JS e può fare riferimento a token e altri valori.

### Esempi di casi d&#39;uso

**Abbandono del carrello**: quando il visitatore raggiunge il carrello, imposta lo script del profilo su 1. Quando il visitatore si converte, reimpostarlo a 0. Se il valore è uguale a 1, allora il visitatore ha un elemento nel carrello.

**Conteggio delle visite**: a ogni nuova visita, incrementa il conteggio di 1 per tenere traccia di quanto spesso un visitatore ritorna al sito.

### Vantaggi del metodo

Non richiede aggiornamenti del codice della pagina.

Viene eseguito prima delle decisioni relative all&#39;appartenenza al pubblico e all&#39;attività, pertanto questi attributi di script profilo possono influenzare l&#39;appartenenza a una singola chiamata al server.

Può essere molto robusto. Ben 2000 istruzioni possono essere eseguite per ogni script.

### Avvertenze

Richiede conoscenza di JavaScript.

L&#39;ordine di esecuzione degli script di profilo non può essere garantito, quindi non possono contare l&#39;uno sull&#39;altro.

Il debug può essere difficile da eseguire.

### Esempi di codice

Gli script di profilo sono abbastanza flessibili:

`user.purchase_recency: var dayInMillis = 3600 * 24 * 1000; if (mbox.name == 'orderThankyouPage') {  user.setLocal('lastPurchaseTime', new Date().getTime()); } var lastPurchaseTime = user.getLocal('lastPurchaseTime'); if (lastPurchaseTime) {  return ((new Date()).getTime()-lastPurchaseTime)/dayInMillis; }`

### Link a informazioni rilevanti

[Attributi degli script di profilo](/help/c-target/c-visitor-profile/profile-parameters.md#concept_8C07AEAB0A144FECA8B4FEB091AED4D2)

## Fornitori di dati {#section_14FF3BE20DAA42369E4812D8D50FBDAE}

Fornitori di dati è una funzionalità che ti permette di trasmettere facilmente dati da terze parti a Target.

Nota: Fornitori di dati richiede at.js 1.3 o successive.

### Formato

L&#39;impostazione `window.targetGlobalSettings.dataProviders` è un array dei fornitori di dati.

Per ulteriori informazioni sulla struttura di ciascun fornitore di dati, vedi [Fornitori di dati](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers).

### Esempi di casi d&#39;uso

Un esempio di terza parte potrebbe essere un servizio meteo, un DMP o persino il tuo servizio web. Puoi utilizzare questi dati per generare tipi di pubblico e contenuti mirati e per arricchire il profilo del visitatore.

### Vantaggi del metodo

Questa impostazione consente ai clienti di raccogliere dati da fornitori di dati terzi, come Demandbase, BlueKai e servizi personalizzati, e di passare i dati a Target come parametri mbox nella richiesta globale di mbox.

Supporta la raccolta di dati da più provider tramite richieste sincrone e asincrone.

L&#39;utilizzo di questo approccio semplifica la gestione della visualizzazione momentanea del contenuto della pagina predefinito, inclusi i timeout indipendenti per ogni provider per limitare l&#39;impatto sulle prestazioni della pagina.

### Avvertenze

Se i fornitori di dati aggiunti a `window.targetGlobalSettings.dataProviders` sono asincroni, verranno eseguiti in parallelo. La richiesta API dei visitatori verrà eseguita in parallelo con le funzioni aggiunte a `window.targetGlobalSettings.dataProviders` per consentire un tempo minimo di attesa.

at.js non tenterà di memorizzare i dati nella cache. Se il fornitore di dati recupera i dati una sola volta, deve assicurarsi che i dati siano memorizzati nella cache e, quando viene invocata la funzione di fornitore di dati, deve servire i dati della cache per la seconda invocazione.

### Esempi di codice

Diversi esempi sono disponibili in [Fornitori di dati](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers).

### Link a informazioni rilevanti

Documentazione: [Fornitori di dati](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers)

### Video di formazione:

* [Utilizzo di Fornitori di dati in Adobe Target](https://helpx.adobe.com/it/target/kt/using/dataProviders-atjs-feature-video-use.html)
* [Implementazione di Fornitori di dati in Adobe Target](https://helpx.adobe.com/it/target/kt/using/dataProviders-atjs-technical-video-implement.html)

## API di aggiornamento del profilo bulk {#section_92AB4820A5624C669D9A1F1B6220D4FA}

Tramite l&#39;API, inviare un file .csv a Target con gli aggiornamenti del profilo visitatori per molti visitatori. Ogni profilo visitatore può essere aggiornato con più attributi di profilo nella pagina in una chiamata.

Questa opzione è molto simile agli attributi del cliente con alcune differenze:

* Gli attributi del cliente utilizzano un caricamento FTP mentre l&#39;API di aggiornamento del profilo bulk di Target utilizza un&#39;API HTTP post.
* I dati degli attributi dei clienti possono essere condivisi con Analytics. L&#39;aggiornamento del profilo bulk è utilizzabile solo in Target.
* Gli attributi del cliente supportano la creazione di un profilo per una destinazione utente non ancora visibile. L&#39;API di aggiornamento del profilo bulk aggiorna solo i profili di Target esistenti.
* Gli Attributi cliente richiedono l&#39;utilizzo di Experience Cloud ID (ECID). L&#39;API di aggiornamento del profilo bulk richiede l&#39;ID TNT o `mbox3rdPartyId`.
* Non puoi inviare i seguenti caratteri in `mbox3rdPartyID`: segno più (+) e barra (/).

### Formato

Il file .csv deve fare riferimento a ciascun visitatore tramite il proprio target PCID o mboxThirdPartyId . Experience Cloud ID (ECID) non è supportato. Tutti gli attributi e valori del profilo vengono creati e aggiornati tramite l&#39;API. I dettagli del formato sono disponibili nella documentazione API.

### Esempi di casi d&#39;uso

Il CRM o altro sistema interno archivia dati importanti relativi ai visitatori che si desidera aggiornare costantemente in Target, senza esporre i dati del profilo nell&#39;implementazione della pagina.

### Vantaggi del metodo

Nessun limite al numero di attributi del profilo.

Gli attributi del profilo inviati tramite il sito possono essere aggiornati tramite l&#39;API e viceversa.

### Avvertenze

La dimensione del file batch deve essere inferiore a 50 MB. Inoltre, il numero totale di righe non deve superare 500000 righe per upload.

Non esiste alcun limite al numero o alle righe che è possibile caricare per un periodo di 24 ore nei batch successivi. Tuttavia, il processo di ingestione potrebbe essere limitato durante l&#39;orario di ufficio per garantire che altri processi vengano eseguiti in modo efficiente.

Le [chiamate all’aggiornamento collettivo V2](https://developers.adobetarget.com/api/#updating-profiles) senza chiamate mbox tra gli stessi thirdPartyIds sovrascrivono le proprietà aggiornate nella prima chiamata di aggiornamento collettivo.

### Esempi di codice

Consulta [Aggiornamento di profili](https://developers.adobetarget.com/api/#updating-profiles).

### Link a informazioni rilevanti

[Aggiornamento di profili](https://developers.adobetarget.com/api/#updating-profiles)

## Aggiornamento di singolo profilo API {#section_5D7A9DD7019F40E9AEF2F66F7F345A8D}

Quasi identico all&#39;API di aggiornamento del profilo bulk, ma un solo profilo visitatore alla volta viene aggiornato, in linea con la chiamata API anziché con un file .csv

### Formato

Il visitatore deve essere identificato tramite il valore mboxPC di Target o il valore mboxThirdPartyId. Experience Cloud ID (ECID) non è supportato.

### Esempi di casi d&#39;uso

Si vuole aggiornare Target in tempo reale quando un visitatore esegue alcune azioni offline, ad esempio se chiama un Call Center, richiede un prestito, utilizza una carta fedeltà in negozio, accede a un chiosco, e così via.

### Vantaggi del metodo

Nessun limite al numero di attributi del profilo.

Gli attributi del profilo inviati tramite il sito possono essere aggiornati tramite l&#39;API e viceversa.

### Avvertenze

Limite delle chiamate API di 1 milione per 24 ore

Aggiorna solo i profili. Impossibile creare un profilo per un potenziale utente che Target non ha ancora visto.

### Esempi di codice

GET e POST supportati. `https://CLIENT.tt.omtrdc.net/m2/client/profile/update?mboxPC=1368007744041-575948.01_00&profile.attr1=0&profile.attr2=1...`

### Link a informazioni rilevanti

[Aggiornamento di profili](https://developers.adobetarget.com/api/#updating-profiles)

## Attributi del cliente {#section_C47FC7980A9A4608BD1A5F0BD900FA70}

Gli attributi dei clienti consentono di caricare i dati del profilo visitatori tramite FTP nell&#39;Experience Cloud. Una volta effettuato l&#39;aggiornamento, sfrutta i dati in Adobe Analytics e Adobe Target.

I clienti di Target Standard possono sfruttare 5 attributi, i clienti Target Premium possono sfruttare 200 attributi.

### Formato

Un file con estensione .csv con gli ID di Experience Cloud ID (ECID) e coppie di nome attributo e valore viene caricato tramite FTP o manualmente nell’interfaccia utente di Experience Cloud.

### Esempi di casi d&#39;uso

Il tuo CRM o altro sistema interno memorizza informazioni preziose che desideri condividere con Adobe Experience Cloud, inclusi Target e Analytics.

### Vantaggi del metodo

Il caricamento dei dati del cliente crea una voce di profilo per il visitatore in Target, anche se Target non ha ancora visto il visitatore.

Gli stessi dati sono automaticamente disponibili in Target e Analytics.

FTP può essere un metodo di implementazione più semplice rispetto all&#39;API.

### Avvertenze

I clienti di Target Standard possono sfruttare 5 attributi, i clienti Target Premium possono sfruttare 200 attributi

Può solo aggiornare i valori tramite gli attributi del cliente, non sulla pagina.

Richiede l&#39;implementazione di Experience Cloud ID (ECID).

### Esempi di codice

Details can be found in [Create a customer attribute source and upload the data file](https://docs.adobe.com/content/help/en/core-services/interface/customer-attributes/t-crs-usecase.html).

### Link a informazioni rilevanti

[Crea un&#39;origine attributo del cliente e carica il file di dati](https://docs.adobe.com/content/help/en/core-services/interface/customer-attributes/t-crs-usecase.html).