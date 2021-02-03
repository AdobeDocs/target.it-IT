---
keywords: gestione delle relazioni con i clienti;servizio record cliente;crs;crm;mbox3rdpartyid;attributi cliente;targeting;csv;crm;adobe experience cloud people
description: Informazioni sull'utilizzo dei dati del cliente Enterprise provenienti da database CRM (Customer Relationship Management) per il targeting dei contenuti in  Adobe Target mediante l'uso di Attributi del cliente nel servizio Adobe Experience Cloud People.
title: Attributi del cliente
feature: Audiences
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '1504'
ht-degree: 40%

---


# Attributi del cliente

Informazioni sull&#39;utilizzo dei dati del cliente aziendale dai database CRM (Customer Relationship Management) per il targeting dei contenuti in [!DNL Adobe Target] utilizzando gli attributi del cliente nel servizio [!DNL Adobe Enterprise Cloud People].

I dati dei clienti Enterprise raccolti attraverso più origini e memorizzati all&#39;interno di database CRM possono essere utilizzati in [!DNL Target] per fornire strategicamente i contenuti più rilevanti ai clienti, concentrandosi in particolare sui clienti di ritorno. Audience e attributi del cliente nel servizio [!DNL People] (ex Profili e pubblico) riunisce la raccolta e l&#39;analisi dei dati con test e ottimizzazione, rendendo fruibili i dati e le informazioni.

## Panoramica sugli attributi del cliente {#section_B4099971FA4B48598294C56EAE86B45A}

[Gli ](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/attributes.html) attributi del cliente nel  [!DNL People] servizio fanno parte del servizio  [!DNL Adobe Experience Cloud] e forniscono alle aziende uno strumento per inviare i dati dei clienti alla  [!DNL Experience Cloud] piattaforma.

I dati inseriti nell&#39;[!DNL Experience Cloud] sono disponibili per tutti i flussi di lavoro di [!DNL Experience Cloud]. [!DNL Target] utilizza questi dati per il targeting del cliente di ritorno in base agli attributi. [!DNL Adobe Analytics] utilizza questi attributi che possono essere utili per l&#39;analisi e la segmentazione.

![esempio CRS](/help/c-target/c-visitor-profile/assets/crs.png)

Considera le seguenti informazioni mentre lavori con gli attributi del cliente e [!DNL Target]:

* Per poter utilizzare la funzionalità [!UICONTROL Attributi del cliente] nel servizio [!DNL People], è necessario soddisfare alcuni requisiti preliminari. Per ulteriori informazioni, vedere &quot;Prerequisiti per il caricamento di attributi del cliente&quot; in [Attributi del cliente](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/attributes.html#section_BD38693AFBF34926BA28E964963B4EA0) nella *documentazione  servizi e amministrazione di Experience Cloud*.

   >[!NOTE]
   >
   >[!DNL at.js] (qualsiasi versione) o  [!DNL mbox.js] versione 58 o successiva è necessaria.

* [!DNL Adobe] non garantisce che il 100% dei dati attributo del cliente (profilo visitatore) provenienti dai database CRM sia imbarcato sul  [!DNL Experience Cloud] e, quindi, sia disponibile per l&#39;uso per il targeting in  [!DNL Target]. Nella nostra progettazione attuale, esiste la possibilità che una piccola percentuale di dati (fino allo 0,1% dei batch di produzione di grandi dimensioni) potrebbe non essere caricata.
* La durata dei dati degli attributi del cliente importati da [!DNL Experience Cloud] a [!DNL Target] dipende dalla durata del profilo del visitatore, che per impostazione predefinita è di 14 giorni. Per ulteriori informazioni, vedere [Durata del profilo del visitatore](/help/c-target/c-visitor-profile/visitor-profile-lifetime.md#concept_D9F21B416F1F49159F03036BA2DD54FD).
* Se i parametri `vst.*` sono l&#39;unica cosa che identifica il visitatore, il profilo esistente &quot;autenticato&quot; non verrà recuperato finché `authState` non sarà ANNULLATO (0). Il profilo verrà riprodotto solo se `authState` viene cambiato in AUTENTICATED (1).

   Ad esempio, se il parametro `vst.myDataSource.id` viene utilizzato per identificare il visitatore (dove `myDataSource` è l&#39;alias dell&#39;origine dati) e non esiste un MCID o un ID di terza parte, l&#39;utilizzo del parametro `vst.myDataSource.authState=0` non recupererà il profilo che potrebbe essere stato creato tramite un&#39;importazione di Attributi cliente. Se il comportamento desiderato è quello di recuperare il profilo autenticato, il `vst.myDataSource.authState` deve avere il valore 1 (AUTENTICATED).

* Non puoi inviare i seguenti caratteri in `mbox3rdPartyID`: segno più (+) e barra (/).

## Accesso agli attributi del cliente nel servizio Persone

1. In [!DNL Adobe Experience Cloud], fare clic sull&#39;icona del menu ( ![icona del menu](/help/c-target/c-visitor-profile/assets/menu-icon.png) ), quindi fare clic su **[!UICONTROL Persone]**.

   ![Persone](/help/c-target/c-visitor-profile/assets/people.png)

1. Fare clic sulla scheda **[!UICONTROL Attributi del cliente]**.

   ![Attributi del cliente, scheda](/help/c-target/c-visitor-profile/assets/customer-attributes-tab.png)

## Flusso di lavoro attributo cliente per Target {#section_00DAE94DA9BA41398B6FD170BC7D38A3}

Completa i passaggi seguenti per utilizzare i dati CRM in [!DNL Target], come illustrato di seguito:

![flusso di lavoro crm](/help/c-target/c-visitor-profile/assets/crm_workflow.png)

Istruzioni dettagliate per l&#39;esecuzione di ciascuna delle seguenti attività sono reperibili in [Creare un&#39;origine attributo del cliente e caricare il file di dati](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html) nella *documentazione Servizi di Experience Cloud e Amministrazione*.

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

   * **HTTPS:** Puoi trascinare il file di dati .csv o fare clic su  **** Sfoglia per caricarlo dal file system.
   * **FTP:** Fai clic sul collegamento FTP per  [caricare il file tramite FTP](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-upload-attributes-ftp.html). Il primo passo è quello di fornire una password per il server FTP fornito da Adobe. Specificate la password, quindi fate clic su **[!UICONTROL Fine]**.

   Ora puoi trasferire il file CSV/ZIP/GZIP al server FTP. Dopo il trasferimento del file, create un nuovo file con lo stesso nome ed estensione .fin. Trasferisci questo file vuoto al server. Indica la fine del trasferimento e l&#39; [!DNL Experience Cloud] inizia a elaborare il file di dati.

1. Convalida dello schema.

   Il procedimento di convalida consente di mappare i nomi e le descrizioni visualizzati agli attributi caricati (stringhe, interi, numeri e così via). Mappa ogni attributo al tipo di dati corretto, al nome visualizzato e alla descrizione.

   Fare clic su **[!UICONTROL Salva]** al termine della convalida dello schema. Il tempo di upload dei file varia a seconda delle dimensioni.

   ![Convalida schema](/help/c-target/c-visitor-profile/assets/SchemaValidate.png)

   ![Carica schema](/help/c-target/c-visitor-profile/assets/upload1.png)

1. Configurazione delle sottoscrizioni e attivazione dell&#39;origine attributo.

   Fai clic su **[!UICONTROL Aggiungi sottoscrizione]**, quindi seleziona la soluzione per sottoscrivere questi attributi. [Configura ](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/subscription.html) sottoscrizioni consente di impostare il flusso di dati tra le soluzioni  [!DNL Experience Cloud] e. Attivando l&#39;origine attributo consenti la trasmissione dei dati alle soluzioni sottoscritte. I record cliente che hai caricato vengono fatti corrispondere ai segnali ID in ingresso provenienti dal sito Web o dall&#39;applicazione.

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

Passa `mbox3rdPartyId` come parametro alla mbox globale all&#39;interno del metodo `targetPageParams()`. Il valore di `mbox3rdPartyId` deve essere impostato sull&#39;ID cliente presente nel file di dati CSV.

```javascript
<script type="text/javascript">
            function targetPageParams() {
               return 'mbox3rdPartyId=2000578';
            }
</script>
```

### Utilizzo del servizio Experience Cloud ID

Se utilizzi il servizio Experience Cloud ID, devi impostare un ID cliente e uno stato di autenticazione per utilizzare gli attributi del cliente nel targeting. Per ulteriori informazioni, vedere [ID cliente e stato di autenticazione](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html) nella *Guida del servizio ID Experience Cloud*.

Per ulteriori informazioni sull&#39;utilizzo degli attributi del cliente in [!DNL Target], consulta le risorse seguenti:

* [Creare un&#39;origine attributo del cliente e caricare il ](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html) file di dati nella documentazione Servizi e Amministrazione  *Experience Cloud*
* [Customer Attributes: The More You Know, The Better You Connect](https://blogs.adobe.com/digitalmarketing/analytics/customer-attributes-know-better-connect/) (Attributi del cliente: più si conoscono, meglio ci si connette) nel *Digital Marketing Blog*

## Problemi riscontrati frequentemente dai clienti {#section_BE0F70E563F64294B17087DE2BC1E74C}

È possibile che si verifichino i seguenti problemi quando si utilizzano gli attributi del cliente e [!DNL Target].

>[!NOTE]
>
>Le questioni 1 e 2 causano circa il 60 per cento dei problemi in questo settore. Il numero 3 causa circa il 30% dei problemi. Il numero 4 causa circa il 5% dei problemi. Il restante 5% è dovuto a questioni varie.

### Problema 1: Gli attributi del cliente vengono rimossi perché il profilo è troppo grande

Non è presente alcun limite di carattere in un determinato campo nel profilo dell&#39;utente, ma se il profilo diventa più grande di 64 K, viene troncato rimuovendo gli attributi meno recenti finché il profilo non è di nuovo inferiore a 64 K.

### Problema 2: Attributi non elencati nella Libreria Pubblico in [!DNL Target], anche dopo diversi giorni

Questo è di solito un problema di connessione della pipeline. Come risoluzione, chiedi al team degli Attributi dei clienti di ripubblicare il feed.

### Problema 3: Consegna non funzionante in base all&#39;attributo

Il profilo non è stato ancora aggiornato alla versione più recente. Come risoluzione, chiedi al team degli Attributi dei clienti di ripubblicare il feed.

### Problema 4: Problemi di implementazione

Tieni conto dei seguenti problemi di implementazione:

* L&#39;ID del visitatore non è stato passato correttamente. L&#39;ID è stato passato in `mboxMCGVID` invece di `setCustomerId`.
* L&#39;ID del visitatore è stato passato correttamente, ma lo stato di autenticazione non è stato impostato su AUTENTICATO.
* `mbox3rdPartyId` non è stato passato correttamente.

### Numero 5: `mboxUpdate` non eseguito correttamente

`mboxUpdate` non è stato eseguito correttamente con `mbox3rdPartyId`.

### Problema 6: Gli attributi del cliente non vengono importati in [!DNL Target]

Se non riesci a trovare i dati degli attributi del cliente in Target, accertati che l&#39;importazione sia avvenuta entro gli ultimi *x* giorni in cui *x* è il valore [Durata profilo visitatore ](/help/c-target/c-visitor-profile/visitor-profile-lifetime.md) (per impostazione predefinita, 14 giorni).

## Video di formazione: Caricare i dati offline utilizzando gli attributi del cliente ![badge di esercitazione](/help/assets/tutorial.png) {#section_9A4E0FA0D0934D06BD8D5BFA673E9BD8}

Questo video illustra come importare CRM offline, help desk, punti vendita e altri dati di marketing nel servizio [!DNL Experience Cloud People] e associarli ai visitatori che utilizzano i loro ID noti.

>[!VIDEO](https://video.tv.adobe.com/v/17802t1/)
