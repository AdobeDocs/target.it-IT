---
keywords: implementa;implementazione;impostazione;installazione;parametro di pagina;tomcat;codifica url;attributo profilo di pagina;parametro mbox;attributi profilo di pagina;attributo profilo script;aggiornamento API bulk profilo;aggiornamento API file singolo;attributi cliente;fornitori di dati;fornitori dati;fornitori di dati
description: Trasferisci i dati in Target (parametri di pagina, attributi di profilo, attributi di profilo di script, fornitori di dati, API di aggiornamento di profili singolo e in blocco, attributi del cliente).
title: Come posso inserire dati in Target?
feature: Implementazione
role: Developer
exl-id: b42eb846-d423-4545-a8fe-0b8048ab689e
translation-type: tm+mt
source-git-commit: 70d4c5b4166081751246e867d90d43b67efa5469
workflow-type: tm+mt
source-wordcount: '1082'
ht-degree: 89%

---

# Panoramica dei metodi

Informazioni sui diversi metodi possibili per ottenere i dati in [!DNL Adobe Target].

I metodi disponibili includono:

| Metodo | Dettagli |
| --- | --- |
| [](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/page-parameters.md)<br>Parametri di pagina (detti anche “parametri mbox”) | I parametri di pagina sono coppie di nome e valore passate direttamente tramite codice di pagina che non sono memorizzati nel profilo del visitatore per un utilizzo futuro.<br>I parametri di pagina sono utili per inviare ulteriori dati di pagina alla destinazione che non devono essere memorizzati con il profilo del visitatore per un futuro targeting. Questi valori vengono invece utilizzati per descrivere la pagina o l&#39;azione che l&#39;utente ha assunto nella pagina specifica. |
| [](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/in-page-profile-attributes.md)<br>Attributi di profilo nella pagina (detti anche “attributi di profilo nella mbox”) | Gli attributi di profilo nella pagina sono coppie di nome e valore passate direttamente tramite il codice della pagina archiviato nel profilo del visitatore per un utilizzo futuro.<br>Gli attributi di profilo nella pagina consentono l&#39;archiviazione dei dati specifici dell&#39;utente nel profilo di Target per targeting e segmentazione in un secondo momento. |
| [Attributi di profilo script](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/script-profile-attributes.md) | Gli attributi di profilo script sono coppie di nome e valore definite nella soluzione di Target. Il valore è determinato dall&#39;esecuzione di un frammento JavaScript sul server di destinazione per ogni chiamata del server.<br>Gli utenti scrivono frammenti di codice di piccole dimensioni che vengono eseguiti per chiamata mbox e prima che un visitatore venga valutato per l&#39;appartenenza al pubblico e all&#39;attività. |
| [Fornitori di dati](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/data-providers.md) | Fornitori di dati è una funzionalità che ti consente di trasmettere facilmente dati da terze parti a Target. |
| API di aggiornamento del profilo bulk | Tramite l&#39;API, inviare un file .csv a Target con gli aggiornamenti del profilo visitatori per molti visitatori. Ogni profilo visitatore può essere aggiornato con più attributi di profilo nella pagina in una chiamata. |
| Aggiornamento di singolo profilo API | Quasi identico all&#39;API di aggiornamento del profilo bulk, ma un solo profilo visitatore alla volta viene aggiornato, in linea con la chiamata API anziché con un file .csv. |
| Attributi del cliente | Gli attributi dei clienti consentono di caricare i dati del profilo visitatori tramite FTP nell&#39;Experience Cloud. Una volta effettuato l&#39;aggiornamento, sfrutta i dati in Adobe Analytics e Adobe Target. |







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

Quasi identico all&#39;API di aggiornamento del profilo bulk, ma un solo profilo visitatore alla volta viene aggiornato, in linea con la chiamata API anziché con un file .csv.

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

I dettagli sono disponibili in [Crea un&#39;origine attributo del cliente e carica il file di dati](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html).

### Link a informazioni rilevanti

[Crea un&#39;origine attributo del cliente e carica il file di dati](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html).
