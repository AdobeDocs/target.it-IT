---
keywords: customer relationship management;customer record service;crs;crm;mbox3rdpartyid;attributi cliente;targeting;csv;crm;adobe experience cloud persone
description: Scopri come utilizzare i dati dei clienti aziendali da un database di gestione delle relazioni con i clienti (CRM) per il targeting dei contenuti in [!DNL Adobe Target].
title: Cosa sono gli attributi del cliente e come li utilizzo?
feature: Audiences
exl-id: 4a36230a-ae86-42a2-b6fe-60e7ab45e1a8
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '1513'
ht-degree: 31%

---

# Attributi del cliente

Informazioni sull&#39;utilizzo dei dati dei clienti aziendali dai database CRM (Customer Relationship Management) per il targeting del contenuto in [!DNL Adobe Target] mediante gli attributi del cliente nel servizio [!DNL Adobe Enterprise Cloud People].

I dati dei clienti aziendali raccolti tramite più origini e memorizzati all&#39;interno dei database CRM possono essere utilizzati in [!DNL Target] per fornire in modo strategico il contenuto più pertinente ai clienti, specificatamente concentrandosi sui clienti fidelizzati. I tipi di pubblico e gli attributi del cliente nel servizio [!DNL People] (già Profili e tipi di pubblico) uniscono la raccolta e l&#39;analisi dei dati con test e ottimizzazione, rendendo immediatamente fruibili i dati e le informazioni.

## Panoramica degli attributi del cliente {#section_B4099971FA4B48598294C56EAE86B45A}

[Attributi del cliente](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/attributes.html?lang=it) nel servizio [!DNL People] fa parte di [!DNL Adobe Experience Cloud] e fornisce alle aziende uno strumento per inviare i dati dei clienti alla piattaforma [!DNL Experience Cloud].

I dati inseriti nell&#39;[!DNL Experience Cloud] sono disponibili per tutti i flussi di lavoro di [!DNL Experience Cloud]. [!DNL Target] utilizza questi dati per il targeting dei clienti fidelizzati in base agli attributi. [!DNL Adobe Analytics] utilizza questi attributi che possono essere utili per l&#39;analisi e la segmentazione.

![esempio crs](/help/main/c-target/c-visitor-profile/assets/crs.png)

Considera le seguenti informazioni mentre lavori con gli attributi del cliente e [!DNL Target]:

* Per poter utilizzare la funzionalità [!UICONTROL Customer attributes] nel servizio [!DNL People], è necessario soddisfare alcuni prerequisiti. Per ulteriori informazioni, consulta &quot;Prerequisiti per il caricamento di attributi del cliente&quot; in [Attributi del cliente](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/attributes.html?lang=it#section_BD38693AFBF34926BA28E964963B4EA0) nella *documentazione dei servizi e dell&#39;amministrazione di Experience Cloud*.
* Presta attenzione alle limitazioni relative al caricamento di file, come documentato in [Informazioni su file di dati e origini dati per Attributi del cliente](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/crs-data-file.html?lang=it) nella *Guida ai componenti dell&#39;interfaccia centrale di Experience Cloud*. Best practice:

   * Carica singoli file di grandi dimensioni (entro i [limiti specificati](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/crs-data-file.html?lang=it)). I singoli file di grandi dimensioni sono preferiti rispetto a più file di piccole dimensioni.
   * Se devi suddividere il caricamento in più file, assicurati che i file siano completamente elaborati prima di inviare nuovi file. Verificare che ogni file di un batch sia stato elaborato completamente prima di inviare il file successivo del batch.

* [!DNL Adobe] non garantisce che il 100% dei dati dell&#39;attributo del cliente (profilo visitatore) provenienti dai database di gestione delle relazioni con i clienti sia integrato in [!DNL Experience Cloud] e sia quindi disponibile per l&#39;utilizzo per il targeting in [!DNL Target]. Nella progettazione corrente, esiste la possibilità che una piccola percentuale di dati (fino allo 0,1% dei batch di produzione di grandi dimensioni) potrebbe non essere integrata.
* La durata dei dati degli attributi del cliente importati da [!DNL Experience Cloud] a [!DNL Target] dipende dalla durata del profilo del visitatore, che è di 14 giorni per impostazione predefinita. Per ulteriori informazioni, consulta [Durata del profilo del visitatore](/help/main/c-target/c-visitor-profile/visitor-profile-lifetime.md#concept_D9F21B416F1F49159F03036BA2DD54FD).
* Se i parametri `vst.*` sono l&#39;unica cosa che identifica il visitatore, il profilo &quot;autenticato&quot; esistente non verrà recuperato fintanto che `authState` non è AUTENTICATO (0). Il profilo entra in gioco solo se `authState` viene modificato in AUTENTICATO (1).

  Ad esempio, se il parametro `vst.myDataSource.id` viene utilizzato per identificare il visitatore (dove `myDataSource` è l&#39;alias dell&#39;origine dati) e non esiste alcun ID MCID o di terze parti, l&#39;utilizzo del parametro `vst.myDataSource.authState=0` non recupera il profilo che potrebbe essere stato creato tramite un&#39;importazione di attributi del cliente. Se il comportamento desiderato è quello di recuperare il profilo autenticato, il valore di `vst.myDataSource.authState` deve essere 1 (AUTENTICATO).

* Non puoi inviare i seguenti caratteri in `mbox3rdPartyID`: segno più (+) e barra (/).

## Accedere agli attributi del cliente nel servizio People

1. In [!DNL Adobe Experience Cloud], fai clic sull&#39;icona del menu ( ![icona del menu](/help/main/c-target/c-visitor-profile/assets/menu-icon.png) ), quindi fai clic su **[!UICONTROL People]**.

   ![Persone](/help/main/c-target/c-visitor-profile/assets/people.png)

1. Fare clic sulla scheda **[!UICONTROL Customer Attributes]**.

   ![Scheda Attributi del cliente](/help/main/c-target/c-visitor-profile/assets/customer-attributes-tab.png)

## Flusso di lavoro attributi cliente per [!DNL Target] {#section_00DAE94DA9BA41398B6FD170BC7D38A3}

Completa i passaggi seguenti per utilizzare i dati CRM in [!DNL Target], come illustrato di seguito:

![flusso di lavoro crm](/help/main/c-target/c-visitor-profile/assets/crm_workflow.png)

Le istruzioni dettagliate per il completamento di ciascuna delle seguenti attività sono disponibili in [Creare un&#39;origine attributo del cliente e caricare il file di dati](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/t-crs-usecase.html?lang=it) nella *documentazione dei servizi e dell&#39;amministrazione di Experience Cloud*.

1. Creazione di un file di dati.

   Esporta i dati dei clienti dal tuo CRM in formato CSV per creare un file .csv. In alternativa, puoi creare un file zip o gzip per il caricamento. Assicurati che la prima riga del file CSV sia l’intestazione e che tutte le righe (dati cliente) abbiano lo stesso numero di voci.

   Nell&#39;illustrazione seguente viene illustrato un esempio di file di dati di un cliente aziendale:

   ![esempio crs](/help/main/c-target/c-visitor-profile/assets/CRS_sample.png)

   La figura seguente mostra un esempio di file .csv di un cliente aziendale:

   ![esempio csv](/help/main/c-target/c-visitor-profile/assets/CRS_CSV_sample.png)

1. Creazione di una sorgente attributo e caricamento del file di dati.

   Specifica un nome e una descrizione dell&#39;origine dati e l&#39;ID dell&#39;alias. L&#39;ID alias è un ID univoco da utilizzare nel codice attributo cliente in `VisitorAPI.js`.

   >[!IMPORTANT]
   >
   >Il nome dell’origine dati e il nome dell’attributo non possono contenere un punto.

   Il file di dati deve essere conforme ai requisiti di caricamento del file e non deve superare i 100 MB. Se il file è troppo grande o se disponi di dati che devono essere caricati su base periodica, puoi invece inviare i file tramite FTP.

   * **HTTPS:** Puoi trascinare il file di dati .csv o fare clic su **[!UICONTROL Browse]** per caricarlo dal file system.
   * **FTP:** Fai clic sul collegamento FTP per [caricare il file tramite FTP](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-upload-attributes-ftp.html?lang=it). Il primo passo è quello di fornire una password per il server FTP fornito da Adobe. Specificare la password, quindi fare clic su **[!UICONTROL Done]**.

   Ora puoi trasferire il file CSV/ZIP/GZIP al server FTP. Dopo il trasferimento di questo file, creare un file con lo stesso nome e un&#39;estensione `.fin`. Trasferisci questo file vuoto al server. Questo indica la fine del trasferimento e [!DNL Experience Cloud] inizia a elaborare il file di dati.

1. Convalida dello schema.

   Il procedimento di convalida consente di mappare i nomi e le descrizioni visualizzati agli attributi caricati (stringhe, interi, numeri e così via). Mappa ogni attributo al tipo di dati corretto, al nome visualizzato e alla descrizione.

   Fare clic su **[!UICONTROL Save]** al termine della convalida dello schema. Il tempo di upload dei file varia a seconda delle dimensioni.

   ![Convalida schema](/help/main/c-target/c-visitor-profile/assets/SchemaValidate.png)

   ![Carica schema](/help/main/c-target/c-visitor-profile/assets/upload1.png)

1. Configurazione delle sottoscrizioni e attivazione dell&#39;origine attributo.

   Fai clic su **[!UICONTROL Add Subscription]**, quindi seleziona la soluzione per sottoscrivere questi attributi. [Configura sottoscrizioni](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/subscription.html?lang=it) imposta il flusso di dati tra [!DNL Experience Cloud] e le soluzioni. Attivando l&#39;origine attributo consenti la trasmissione dei dati alle soluzioni sottoscritte. I record cliente che hai caricato vengono fatti corrispondere ai segnali ID in ingresso provenienti dal sito Web o dall&#39;applicazione.

   ![Configura soluzione](/help/main/c-target/c-visitor-profile/assets/solution.png)

   ![Attiva](/help/main/c-target/c-visitor-profile/assets/activate.png)

   Durante l&#39;esecuzione di questo passaggio, tieni presente le limitazioni seguenti:

   * La dimensione massima del file per ogni caricamento tramite il metodo HTTP è 100 MB.
   * La dimensione massima del file per ogni caricamento tramite il metodo FTP è 4 GB.
   * Il numero di attributi ammessi per la sottoscrizione: 5 per [!DNL Target Standard] e 200 per [!DNL Target Premium].

## Usa attributi cliente in [!DNL Target] {#section_107E3A0F0EC7478E82E6DBD17B30B756}

È possibile utilizzare gli attributi del cliente in [!DNL Target] nei modi seguenti:

### Creazione di targeting di pubblico

In [!DNL Target] è possibile selezionare un attributo del cliente dalla sezione [!UICONTROL Visitor Profile] durante la creazione di un pubblico. Tutti gli attributi del cliente hanno il prefisso &lt; data_source_name > nell’elenco. Per creare di tipi di pubblico combina questi attributi con altri attributi di dati.

![Pubblico di Target](/help/main/c-target/c-visitor-profile/assets/TargetAudience.png)

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

Se utilizzi il servizio Experience Cloud ID, devi impostare un ID cliente e uno stato di autenticazione per utilizzare gli attributi del cliente nel targeting. Per ulteriori informazioni, consulta [ID cliente e stati di autenticazione](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html?lang=it) nella *Guida del servizio Experience Cloud ID*.

Per ulteriori informazioni sull&#39;utilizzo degli attributi del cliente in [!DNL Target], consulta le risorse seguenti:

* [Crea un&#39;origine attributo del cliente e carica il file di dati](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html?lang=it) nella *documentazione dei servizi e dell&#39;amministrazione di Experience Cloud*

## Problemi incontrati frequentemente dai clienti {#section_BE0F70E563F64294B17087DE2BC1E74C}

È possibile che si verifichino i seguenti problemi quando si utilizzano gli attributi del cliente e [!DNL Target].

>[!NOTE]
>
>I problemi 1 e 2 causano circa il 60% dei problemi in questo settore. Il numero 3 causa circa il 30% dei problemi. Il problema 4 causa circa il 5% dei problemi. Il restante 5% è dovuto a questioni varie.

### Problema 1: gli attributi del cliente vengono rimossi perché il profilo è troppo grande

Non è presente alcun limite di carattere in un determinato campo nel profilo dell&#39;utente, ma se il profilo diventa più grande di 64 K, viene troncato rimuovendo gli attributi meno recenti finché il profilo non è di nuovo inferiore a 64 K.

### Problema 2: gli attributi non vengono elencati nella libreria Pubblico in [!DNL Target], anche dopo alcuni giorni

Questo è di solito un problema di connessione della pipeline. Come risoluzione, chiedi al team degli Attributi dei clienti di ripubblicare il feed.

### Problema 3: la consegna non funziona in base all’attributo

Il profilo non è stato ancora aggiornato alla versione più recente. Come risoluzione, chiedi al team degli Attributi dei clienti di ripubblicare il feed.

### Problema 4: problemi di implementazione

Tieni conto dei seguenti problemi di implementazione:

* L&#39;ID del visitatore non è stato passato correttamente. L&#39;ID è stato passato in `mboxMCGVID` invece di `setCustomerId`.
* L&#39;ID del visitatore è stato passato correttamente, ma lo stato di autenticazione non è stato impostato su AUTENTICATO.
* `mbox3rdPartyId` non è stato passato correttamente.

### Problema 5: `mboxUpdate` non eseguito correttamente

`mboxUpdate` non eseguito correttamente con `mbox3rdPartyId`.

### Problema 6: gli attributi del cliente non vengono importati in [!DNL Target]

Se non riesci a trovare i dati Attributi del cliente in Target, accertati che l&#39;importazione sia avvenuta negli ultimi *x* giorni in cui *x* è il valore di Target [Durata profilo visitatore](/help/main/c-target/c-visitor-profile/visitor-profile-lifetime.md) (14 giorni per impostazione predefinita).

## Video di formazione: Caricare dati offline utilizzando gli attributi del cliente ![Icona esercitazione](/help/main/assets/tutorial.png) {#section_9A4E0FA0D0934D06BD8D5BFA673E9BD8}

In questo video viene illustrato come importare dati CRM offline, da help desk, punti vendita e altri dati di marketing nel servizio [!DNL Experience Cloud People] e associarli ai visitatori utilizzando i loro ID noti.

>[!VIDEO](https://video.tv.adobe.com/v/17802t1/)
