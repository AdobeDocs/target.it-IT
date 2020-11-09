---
keywords: customer relationship management;customer record service;crs;crm;mbox3rdpartyid;customer attributes;targeting;csv;crm;adobe experience cloud people
description: Informazioni sull'utilizzo dei dati del cliente aziendale da database CRM (Customer Relationship Management) per il targeting dei contenuti in  Adobe Target, utilizzando Attributi cliente nel servizio di base Persone di Adobe Experience Cloud.
title: Attributi del cliente in  Adobe Target
feature: visitor profiles
subtopic: Getting Started
topic: Standard
uuid: fc3c9a02-30d7-43df-838d-10ce1aa17f16
translation-type: tm+mt
source-git-commit: a05d2a28b7bea3aa559cd0174930af10c6d94134
workflow-type: tm+mt
source-wordcount: '1494'
ht-degree: 40%

---


# Attributi del cliente {#customer-attributes}

Information about using enterprise customer data from Customer Relationship Management (CRM) databases for content targeting in [!DNL Adobe Target] by using customer attributes in the [!DNL Adobe Enterprise Cloud People] core service.

Enterprise customer data collected through multiple sources and stored inside CRM databases can be used in [!DNL Target] to strategically deliver the most relevant content to customers, specifically focusing on returning customers. Audiences and customer attributes in the [!DNL People] core service (formerly Profiles and Audiences) brings together data collection and analysis with testing and optimization, making data and insights actionable.

## Customer attributes overview {#section_B4099971FA4B48598294C56EAE86B45A}

[Gli attributi](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/attributes.html) del cliente nel [!DNL People] servizio di base fanno parte del [!DNL Adobe Experience Cloud] servizio e forniscono alle aziende uno strumento per inviare i dati dei clienti alla [!DNL Experience Cloud] piattaforma.

I dati inseriti nell&#39;[!DNL Experience Cloud] sono disponibili per tutti i flussi di lavoro di [!DNL Experience Cloud]. [!DNL Target] utilizza questi dati per il targeting del cliente di ritorno in base agli attributi. [!DNL Adobe Analytics] utilizza questi attributi che possono essere utili per l&#39;analisi e la segmentazione.

![esempio CRS](/help/c-target/c-visitor-profile/assets/crs.png)

Considera le seguenti informazioni mentre lavori con gli attributi del cliente e [!DNL Target]:

* There are some prerequisite requirements that you must meet before you can use the [!UICONTROL Customer attributes] feature in the [!DNL People] core service. For more information, see &quot;Prerequisites for uploading Customer Attributes&quot; in [Customer attributes](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/attributes.html#section_BD38693AFBF34926BA28E964963B4EA0) in the *Experience Cloud and Core Services Product documentation*.

   >[!NOTE]
   >
   >[!DNL at.js] (qualsiasi versione) o [!DNL mbox.js] versione 58 o successiva.

* [!DNL Adobe] non garantisce che il 100% dei dati attributo del cliente (profilo visitatore) provenienti dai database CRM sia imbarcato sul [!DNL Experience Cloud] e, quindi, sia disponibile per l&#39;uso per il targeting in [!DNL Target]. Nella nostra progettazione attuale, esiste la possibilità che una piccola percentuale di dati (fino allo 0,1% dei batch di produzione di grandi dimensioni) potrebbe non essere caricata.
* The lifetime of customer attributes data imported from the [!DNL Experience Cloud] to [!DNL Target] depends on the lifetime of the visitor profile, which is 14 days by default. Per ulteriori informazioni, consulta Durata del profilo [visitatore](/help/c-target/c-visitor-profile/visitor-profile-lifetime.md#concept_D9F21B416F1F49159F03036BA2DD54FD).
* If the `vst.*` parameters are the only thing identifying the visitor, the existing &quot;authenticated&quot; profile will not be fetched as long as `authState` is UNAUTHENTICATED (0). The profile will come into play only if `authState` is changed to AUTHENTICATED (1).

   For example, if the `vst.myDataSource.id` parameter is used to identify the visitor (where `myDataSource` is the data source alias) and there is no MCID or third-party ID, using the parameter `vst.myDataSource.authState=0` won&#39;t fetch the profile that might have been created through a Customer Attributes import. If the desired behavior is to fetch the authenticated profile, the `vst.myDataSource.authState` must have the value of 1 (AUTHENTICATED).

* Non puoi inviare i seguenti caratteri in `mbox3rdPartyID`: segno più (+) e barra (/).

## Accesso agli attributi del cliente nel servizio di base Persone

1. Fate [!DNL Adobe Experience Cloud]clic sull&#39;icona del menu (icona ![del](/help/c-target/c-visitor-profile/assets/menu-icon.png) menu), quindi fate clic su **[!UICONTROL Persone]**.

   ![Persone](/help/c-target/c-visitor-profile/assets/people.png)

1. Fare clic sulla scheda Attributi **[!UICONTROL del]** cliente.

   ![Attributi del cliente, scheda](/help/c-target/c-visitor-profile/assets/customer-attributes-tab.png)

## Customer attribute workflow for Target {#section_00DAE94DA9BA41398B6FD170BC7D38A3}

Completa i passaggi seguenti per utilizzare i dati CRM in [!DNL Target], come illustrato di seguito:

![flusso di lavoro crm](/help/c-target/c-visitor-profile/assets/crm_workflow.png)

Detailed instructions for completing each of the following tasks can be found in [Create a customer attribute source and upload the data file](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html) in the *Experience Cloud and Core Services Product Documentation*.

1. Creazione di un file di dati.

   Esporta i dati dei clienti dal tuo CRM in formato CSV per creare un file .csv. In alternativa, puoi creare un file zip o gzip per il caricamento. Assicurati che la prima riga del file CSV sia l’intestazione e che tutte le righe (dati cliente) abbiano lo stesso numero di voci.

   L&#39;illustrazione seguente mostra un esempio di file di dati del cliente aziendale:

   ![campione CRS](/help/c-target/c-visitor-profile/assets/CRS_sample.png)

   L&#39;illustrazione seguente mostra un esempio di file .csv del cliente Enterprise:

   ![esempio CSV](/help/c-target/c-visitor-profile/assets/CRS_CSV_sample.png)

1. Creazione di una sorgente attributo e caricamento del file di dati.

   Specifica un nome e una descrizione dell&#39;origine dati e l&#39;ID dell&#39;alias. L&#39;ID alias è un ID univoco da utilizzare nel codice dell&#39;attributo del cliente in `VisitorAPI.js`.

   >[!IMPORTANT]
   >
   >Il nome dell’origine dati e il nome dell’attributo non possono contenere un punto.

   Il file di dati deve essere conforme ai requisiti di caricamento del file e non deve superare i 100 MB. Se il file è troppo grande o hai dei dati che dovranno essere caricati su base periodica, puoi invece inviare i tuoi file tramite FTP.

   * **HTTPS:** Puoi trascinare il file di dati .csv o fare clic su **[!UICONTROL Sfoglia]** per caricarlo dal file system.
   * **FTP:** Fate clic sul collegamento FTP per [caricare il file tramite FTP](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-upload-attributes-ftp.html). Il primo passo è quello di fornire una password per il server FTP fornito da Adobe. Specify the password, then click **[!UICONTROL Done]**.

   Ora puoi trasferire il file CSV/ZIP/GZIP al server FTP. Dopo il trasferimento del file, create un nuovo file con lo stesso nome ed estensione .fin. Trasferisci questo file vuoto al server. This indicates a End Of Transfer and the [!DNL Experience Cloud] starts to process the data file.

1. Convalida dello schema.

   Il procedimento di convalida consente di mappare i nomi e le descrizioni visualizzati agli attributi caricati (stringhe, interi, numeri e così via). Mappa ogni attributo al tipo di dati corretto, al nome visualizzato e alla descrizione.

   Click **[!UICONTROL Save]** after the schema validation is complete. Il tempo di upload dei file varia a seconda delle dimensioni.

   ![Convalida schema](/help/c-target/c-visitor-profile/assets/SchemaValidate.png)

   ![Carica schema](/help/c-target/c-visitor-profile/assets/upload1.png)

1. Configurazione delle sottoscrizioni e attivazione dell&#39;origine attributo.

   Fai clic su **[!UICONTROL Aggiungi sottoscrizione]**, quindi seleziona la soluzione per sottoscrivere questi attributi. [Configura sottoscrizioni](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/subscription.html) imposta il flusso di dati tra le soluzioni [!DNL Experience Cloud] e. Attivando l&#39;origine attributo consenti la trasmissione dei dati alle soluzioni sottoscritte. I record cliente che hai caricato vengono fatti corrispondere ai segnali ID in ingresso provenienti dal sito Web o dall&#39;applicazione.

   ![Configurare la soluzione](/help/c-target/c-visitor-profile/assets/solution.png)

   ![Attiva](/help/c-target/c-visitor-profile/assets/activate.png)

   Durante l&#39;esecuzione di questo passaggio, tieni presente le limitazioni seguenti:

   * La dimensione massima del file per ogni caricamento tramite il metodo HTTP è 100 MB.
   * La dimensione massima del file per ogni caricamento tramite il metodo FTP è 4 GB.
   * Il numero di attributi ammessi per la sottoscrizione: 5 per [!DNL Target Standard] e 200 per [!DNL Target Premium].

## Uso degli attributi del cliente in Target {#section_107E3A0F0EC7478E82E6DBD17B30B756}

È possibile utilizzare gli attributi del cliente in [!DNL Target] nei modi seguenti:

### Creazione di targeting di pubblico

In [!DNL Target] puoi selezionare un attributo del cliente dalla sezione Profilo visitatore al momento della creazione di un tipo di pubblico.  Tutti gli attributi del cliente hanno il prefisso &lt; data_source_name > nell’elenco. Per creare di tipi di pubblico combina questi attributi con altri attributi di dati.

![Pubblico di Target](/help/c-target/c-visitor-profile/assets/TargetAudience.png)

### Creazione di script di profilo tramite token

Gli attributi dei clienti possono essere referenziati negli script di profilo utilizzando il formato `crs.get('<Datasource Name>.<Attribute name>')`.

Questo script di profilo può essere utilizzato direttamente nelle offerte per la consegna degli attributi che appartengono al visitatore corrente.

### Utilizzo di mbox3rdPartyID nel sito Web per una corretta implementazione e utilizzo

Pass `mbox3rdPartyId` as a parameter to the global mbox inside the `targetPageParams()` method. The value of `mbox3rdPartyId` should be set to the customer ID that was present in the CSV data file.

```
<script type="text/javascript">
            function targetPageParams() {
               return 'mbox3rdPartyId=2000578';
            }
</script>
```

### Utilizzo del servizio Experience Cloud ID

Se utilizzi il servizio Experience Cloud ID, devi impostare un ID cliente e uno stato di autenticazione per utilizzare gli attributi del cliente nel targeting. For more information, see [Customer IDs and Authentication State](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html) in the *Experience Cloud Identity Service Help*.

Per ulteriori informazioni sull&#39;utilizzo degli attributi del cliente in [!DNL Target], consulta le risorse seguenti:

* [Creare un&#39;origine attributo del cliente e caricare il file](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html) di dati nella Documentazione prodotto del *Experience Cloud*
* [Customer Attributes: The More You Know, The Better You Connect](https://blogs.adobe.com/digitalmarketing/analytics/customer-attributes-know-better-connect/) (Attributi del cliente: più si conoscono, meglio ci si connette) nel *Digital Marketing Blog*

## Issues frequently encountered by customers {#section_BE0F70E563F64294B17087DE2BC1E74C}

È possibile che si verifichino i seguenti problemi quando si utilizzano gli attributi del cliente e [!DNL Target].

>[!NOTE]
>
>Le questioni 1 e 2 causano circa il 60 per cento dei problemi in questo settore. Il numero 3 causa circa il 30% dei problemi. Il numero 4 causa circa il 5% dei problemi. Il restante 5% è dovuto a questioni varie.

### Problema 1: Gli attributi del cliente vengono rimossi perché il profilo è troppo grande

Non è presente alcun limite di carattere in un determinato campo nel profilo dell&#39;utente, ma se il profilo diventa più grande di 64 K, viene troncato rimuovendo gli attributi meno recenti finché il profilo non è di nuovo inferiore a 64 K.

### Issue 2: Attributes not listing in the Audience Library in [!DNL Target], even after several days

Questo è di solito un problema di connessione della pipeline. Come risoluzione, chiedi al team degli Attributi dei clienti di ripubblicare il feed.

### Problema 3: Consegna non funzionante in base all&#39;attributo

Il profilo non è stato ancora aggiornato alla versione più recente. Come risoluzione, chiedi al team degli Attributi dei clienti di ripubblicare il feed.

### Problema 4: Problemi di implementazione

Tieni conto dei seguenti problemi di implementazione:

* L&#39;ID del visitatore non è stato passato correttamente. The ID was passed in `mboxMCGVID` instead of `setCustomerId`.
* L&#39;ID del visitatore è stato passato correttamente, ma lo stato di autenticazione non è stato impostato su AUTENTICATO.
* `mbox3rdPartyId` non è stato passato correttamente.

### Numero 5: `mboxUpdate` non eseguito correttamente

`mboxUpdate` non è stato eseguito correttamente con `mbox3rdPartyId`.

### Issue 6: Customer attributes are not being imported into [!DNL Target]

If you cannot find Customer Attributes data in Target, ensure that the import occurred within the last *x* days where *x* is the Target [Visitor Profile Lifetime](/help/c-target/c-visitor-profile/visitor-profile-lifetime.md) value (14 days by default).

## Training video: Upload Offline Data using Customer Attributes ![Tutorial badge](/help/assets/tutorial.png) {#section_9A4E0FA0D0934D06BD8D5BFA673E9BD8}

This video shows you how to import offline CRM, help desk, point-of-sale, and other marketing data into the [!DNL Experience Cloud People] service and associate it with visitors using their known IDs.

>[!VIDEO](https://video.tv.adobe.com/v/17802t1/)
