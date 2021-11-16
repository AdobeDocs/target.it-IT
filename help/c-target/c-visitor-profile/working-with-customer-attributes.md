---
keywords: gestione delle relazioni con i clienti;servizio record cliente;crs;crm;mbox3rdpartyid;attributi cliente;targeting;csv;crm;adobe experience cloud people
description: Scopri come utilizzare i dati dei clienti aziendali da un database di gestione delle relazioni con i clienti (Customer Relationship Management, CRM) per il targeting dei contenuti in [!DNL Adobe Target].
title: Cosa sono gli attributi del cliente e come li utilizzo?
feature: Audiences
exl-id: 4a36230a-ae86-42a2-b6fe-60e7ab45e1a8
source-git-commit: 19b012a0fcbf5195b12990f0a634a90597850899
workflow-type: tm+mt
source-wordcount: '1571'
ht-degree: 35%

---

# [non definito](/help/c-target/c-visitor-profile/working-with-customer-attributes.md)

Informazioni sull&#39;utilizzo dei dati dei clienti aziendali dai database Customer Relationship Management (CRM) per il targeting del contenuto in [!DNL Adobe Target] utilizzando gli attributi del cliente nella sezione [!DNL Adobe Enterprise Cloud People] servizio.

I dati dei clienti aziendali raccolti attraverso più fonti e memorizzati all&#39;interno di database CRM possono essere utilizzati in [!DNL Target] fornire in modo strategico i contenuti più rilevanti ai clienti, concentrandosi in particolare sui clienti fidelizzati. Tipi di pubblico e attributi del cliente nel [!DNL People] (già Profili e pubblico) unisce le funzioni di raccolta e analisi dei dati a quelle di test e ottimizzazione, rendendo immediatamente fruibili i dati e le informazioni.

## Panoramica degli attributi del cliente {#section_B4099971FA4B48598294C56EAE86B45A}

[Attributi del cliente](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/attributes.html) in [!DNL People] fa parte del [!DNL Adobe Experience Cloud] e fornisce alle aziende uno strumento per spingere i dati dei propri clienti verso [!DNL Experience Cloud] piattaforma.

I dati inseriti nell&#39;[!DNL Experience Cloud] sono disponibili per tutti i flussi di lavoro di [!DNL Experience Cloud]. [!DNL Target] utilizza questi dati per il targeting dei clienti fidelizzati in base agli attributi. [!DNL Adobe Analytics] utilizza questi attributi che possono essere utili per l&#39;analisi e la segmentazione.

![esempio di crs](/help/c-target/c-visitor-profile/assets/crs.png)

Considera le seguenti informazioni mentre lavori con gli attributi del cliente e [!DNL Target]:

* Sono necessari alcuni requisiti prerequisiti da soddisfare prima di poter utilizzare il [!UICONTROL Attributi del cliente] nella [!DNL People] servizio. Per ulteriori informazioni, consulta &quot;Prerequisiti per il caricamento di attributi del cliente&quot; in [Attributi del cliente](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/attributes.html#section_BD38693AFBF34926BA28E964963B4EA0) in *Documentazione su servizi e amministrazione di Experience Cloud*.
* Tieni presente le limitazioni relative al caricamento dei file, come documentato in [Informazioni su file di dati e origini dati per Attributi del cliente](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/crs-data-file.html?lang=en) in *Guida ai componenti dell’interfaccia centrale di Experience Cloud*. Come best practice:

   * Caricare singoli file di grandi dimensioni (all&#39;interno del [limiti](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/crs-data-file.html?lang=en)). I file singoli di grandi dimensioni sono preferiti rispetto a più file più piccoli.
   * Se devi dividere il caricamento in più file, assicurati che i file siano completamente elaborati prima di inviare i nuovi file. Verificare che ogni file di un batch sia completamente elaborato prima di inviare il batch successivo.

* [!DNL Adobe] non garantisce che il 100% dei dati dell’attributo del cliente (profilo visitatore) provenienti dai database CRM sia integrato nel [!DNL Experience Cloud] e, quindi, possono essere utilizzati per il targeting in [!DNL Target]. Nella progettazione attuale, è possibile che una piccola percentuale di dati (fino allo 0,1% dei batch di produzione di grandi dimensioni) potrebbe non essere integrata.
* Durata dei dati degli attributi del cliente importati da [!DNL Experience Cloud] a [!DNL Target] dipende dalla durata del profilo del visitatore, che per impostazione predefinita è di 14 giorni. Per ulteriori informazioni, consulta [Durata del profilo del visitatore](/help/c-target/c-visitor-profile/visitor-profile-lifetime.md#concept_D9F21B416F1F49159F03036BA2DD54FD).
* Se la `vst.*` i parametri sono l’unica cosa che identifica il visitatore, il profilo &quot;autenticato&quot; esistente non verrà recuperato fintanto che `authState` NON AUTENTICATO (0). Il profilo entra in gioco solo se `authState` viene modificato in AUTENTICATO (1).

   Ad esempio, se `vst.myDataSource.id` viene utilizzato per identificare il visitatore (dove `myDataSource` è l&#39;alias dell&#39;origine dati) e non esiste un MCID o un ID di terze parti, utilizzando il parametro `vst.myDataSource.authState=0` non recupera il profilo che potrebbe essere stato creato tramite un’importazione Attributi del cliente. Se il comportamento desiderato è quello di recuperare il profilo autenticato, la `vst.myDataSource.authState` deve avere il valore 1 (AUTENTICATO).

* Non puoi inviare i seguenti caratteri in `mbox3rdPartyID`: segno più (+) e barra (/).

## Accedere agli attributi del cliente nel servizio Persone

1. In [!DNL Adobe Experience Cloud], fai clic sull’icona del menu ( ![icona del menu](/help/c-target/c-visitor-profile/assets/menu-icon.png) ), quindi fai clic su **[!UICONTROL Persone]**.

   ![Persone](/help/c-target/c-visitor-profile/assets/people.png)

1. Fai clic sul pulsante **[!UICONTROL Attributi del cliente]** scheda .

   ![Scheda Attributi del cliente](/help/c-target/c-visitor-profile/assets/customer-attributes-tab.png)

## Flusso di lavoro degli attributi del cliente per [!DNL Target] {#section_00DAE94DA9BA41398B6FD170BC7D38A3}

Completa i passaggi seguenti per utilizzare i dati CRM in [!DNL Target], come illustrato di seguito:

![flusso di lavoro crm](/help/c-target/c-visitor-profile/assets/crm_workflow.png)

Le istruzioni dettagliate per il completamento di ciascuna delle seguenti attività sono disponibili in [Crea un&#39;origine attributo del cliente e carica il file di dati](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/t-crs-usecase.html) in *Documentazione su servizi e amministrazione di Experience Cloud*.

1. Creazione di un file di dati.

   Esporta i dati dei clienti dal tuo CRM in formato CSV per creare un file .csv. In alternativa, puoi creare un file zip o gzip per il caricamento. Assicurati che la prima riga del file CSV sia l’intestazione e che tutte le righe (dati cliente) abbiano lo stesso numero di voci.

   L’illustrazione seguente mostra un esempio di file di dati relativi ai clienti aziendali:

   ![campione crs](/help/c-target/c-visitor-profile/assets/CRS_sample.png)

   La figura seguente mostra un esempio di file .csv del cliente Enterprise:

   ![campione csv](/help/c-target/c-visitor-profile/assets/CRS_CSV_sample.png)

1. Creazione di una sorgente attributo e caricamento del file di dati.

   Specifica un nome e una descrizione dell&#39;origine dati e l&#39;ID dell&#39;alias. L&#39;ID alias è un ID univoco da utilizzare nel codice dell&#39;attributo del cliente in `VisitorAPI.js`.

   >[!IMPORTANT]
   >
   >Il nome dell’origine dati e il nome dell’attributo non possono contenere un punto.

   Il file di dati deve soddisfare i requisiti per il caricamento del file e non deve superare i 100 MB. Se il tuo file è troppo grande o hai dei dati che devono essere caricati su base ricorrente, puoi invece FTP i tuoi file.

   * **HTTPS:** Puoi trascinare il file di dati .csv o fare clic su **[!UICONTROL Sfoglia]** da caricare dal file system.
   * **FTP:** Fai clic sul collegamento FTP a [caricare il file tramite FTP](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-upload-attributes-ftp.html). Il primo passo è quello di fornire una password per il server FTP fornito da Adobe. Specifica la password, quindi fai clic su **[!UICONTROL Fine]**.

   Ora puoi trasferire il file CSV/ZIP/GZIP al server FTP. Una volta che questo trasferimento di file è riuscito, crea un file con lo stesso nome e un `.fin` estensione. Trasferisci questo file vuoto al server. Indica la fine del trasferimento e la [!DNL Experience Cloud] inizia a elaborare il file di dati.

1. Convalida dello schema.

   Il procedimento di convalida consente di mappare i nomi e le descrizioni visualizzati agli attributi caricati (stringhe, interi, numeri e così via). Mappa ogni attributo al tipo di dati corretto, al nome visualizzato e alla descrizione.

   Fai clic su **[!UICONTROL Salva]** al termine della convalida dello schema. Il tempo di upload dei file varia a seconda delle dimensioni.

   ![Convalida schema](/help/c-target/c-visitor-profile/assets/SchemaValidate.png)

   ![Carica schema](/help/c-target/c-visitor-profile/assets/upload1.png)

1. Configurazione delle sottoscrizioni e attivazione dell&#39;origine attributo.

   Fai clic su **[!UICONTROL Aggiungi sottoscrizione]**, quindi seleziona la soluzione per sottoscrivere questi attributi. [Configurazione delle sottoscrizioni](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/subscription.html) imposta il flusso di dati tra [!DNL Experience Cloud] e soluzioni. Attivando l&#39;origine attributo consenti la trasmissione dei dati alle soluzioni sottoscritte. I record cliente che hai caricato vengono fatti corrispondere ai segnali ID in ingresso provenienti dal sito Web o dall&#39;applicazione.

   ![Configurare la soluzione](/help/c-target/c-visitor-profile/assets/solution.png)

   ![Attiva](/help/c-target/c-visitor-profile/assets/activate.png)

   Durante l&#39;esecuzione di questo passaggio, tieni presente le limitazioni seguenti:

   * La dimensione massima del file per ogni caricamento tramite il metodo HTTP è 100 MB.
   * La dimensione massima del file per ogni caricamento tramite il metodo FTP è 4 GB.
   * Il numero di attributi ammessi per la sottoscrizione: 5 per [!DNL Target Standard] e 200 per [!DNL Target Premium].

## Usa gli attributi del cliente in [!DNL Target] {#section_107E3A0F0EC7478E82E6DBD17B30B756}

È possibile utilizzare gli attributi del cliente in [!DNL Target] nei modi seguenti:

### Creazione di targeting di pubblico

In [!DNL Target] puoi selezionare un attributo del cliente dalla sezione Profilo visitatore al momento della creazione di un tipo di pubblico.  Tutti gli attributi del cliente hanno il prefisso &lt; data_source_name > nell’elenco. Per creare di tipi di pubblico combina questi attributi con altri attributi di dati.

![Pubblico di Target](/help/c-target/c-visitor-profile/assets/TargetAudience.png)

### Creazione di script di profilo tramite token

Gli attributi dei clienti possono essere referenziati negli script di profilo utilizzando il formato `crs.get('<Datasource Name>.<Attribute name>')`.

Questo script di profilo può essere utilizzato direttamente nelle offerte per la consegna degli attributi che appartengono al visitatore corrente.

### Utilizzo di mbox3rdPartyID nel sito Web per una corretta implementazione e utilizzo

Pass `mbox3rdPartyId` come parametro per la mbox globale all’interno di `targetPageParams()` metodo . Il valore di `mbox3rdPartyId` deve essere impostato sull&#39;ID cliente presente nel file di dati CSV.

```javascript
<script type="text/javascript">
            function targetPageParams() {
               return 'mbox3rdPartyId=2000578';
            }
</script>
```

### Utilizzo del servizio Experience Cloud ID

Se utilizzi il servizio ID Experience Cloud, devi impostare un ID cliente e uno stato di autenticazione per utilizzare gli attributi del cliente nel targeting. Per ulteriori informazioni, consulta [ID cliente e stato di autenticazione](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html) in *Guida del servizio ID di Experience Cloud*.

Per ulteriori informazioni sull&#39;utilizzo degli attributi del cliente in [!DNL Target], consulta le risorse seguenti:

* [Crea un&#39;origine attributo del cliente e carica il file di dati](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html) in *Documentazione su servizi e amministrazione di Experience Cloud*

## Problemi frequenti riscontrati dai clienti {#section_BE0F70E563F64294B17087DE2BC1E74C}

È possibile che si verifichino i seguenti problemi quando si utilizzano gli attributi del cliente e [!DNL Target].

>[!NOTE]
>
>Le questioni 1 e 2 causano circa il 60% dei problemi in questo settore. Il numero 3 causa circa il 30% dei problemi. Il problema 4 causa circa il 5% dei problemi. Il restante 5% è dovuto a questioni varie.

### Problema 1: Gli attributi del cliente vengono rimossi perché il profilo è troppo grande

Non è presente alcun limite di carattere in un determinato campo nel profilo dell&#39;utente, ma se il profilo diventa più grande di 64 K, viene troncato rimuovendo gli attributi meno recenti finché il profilo non è di nuovo inferiore a 64 K.

### Numero 2: Attributi non elencati nella libreria del pubblico in [!DNL Target]anche dopo diversi giorni

Questo è di solito un problema di connessione della pipeline. Come risoluzione, chiedi al team degli Attributi dei clienti di ripubblicare il feed.

### Numero 3: La consegna non funziona in base all&#39;attributo

Il profilo non è stato ancora aggiornato alla versione più recente. Come risoluzione, chiedi al team degli Attributi dei clienti di ripubblicare il feed.

### Numero 4: Problemi di implementazione

Tieni conto dei seguenti problemi di implementazione:

* L&#39;ID del visitatore non è stato passato correttamente. L&#39;ID è stato passato `mboxMCGVID` anziché `setCustomerId`.
* L&#39;ID del visitatore è stato passato correttamente, ma lo stato di autenticazione non è stato impostato su AUTENTICATO.
* `mbox3rdPartyId` non è stato passato correttamente.

### Numero 5: `mboxUpdate` non eseguito correttamente

`mboxUpdate` non è stato eseguito correttamente con `mbox3rdPartyId`.

### Numero 6: Gli attributi del cliente non vengono importati in [!DNL Target]

Se non riesci a trovare i dati Attributi del cliente in Target, assicurati che l&#39;importazione sia avvenuta nell&#39;ultimo *x* giorni in cui *x* è Target [Durata del profilo del visitatore](/help/c-target/c-visitor-profile/visitor-profile-lifetime.md) (14 giorni per impostazione predefinita).

## Video di formazione: Caricare dati offline utilizzando gli attributi del cliente ![Badge tutorial](/help/assets/tutorial.png) {#section_9A4E0FA0D0934D06BD8D5BFA673E9BD8}

Questo video mostra come importare dati CRM offline, help desk, punti vendita e altri dati di marketing nel [!DNL Experience Cloud People] e associalo ai visitatori utilizzando i loro ID noti.

>[!VIDEO](https://video.tv.adobe.com/v/17802t1/)
