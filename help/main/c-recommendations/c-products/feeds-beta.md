---
keywords: feed consigli;feed;feed;SAINT;ftp;csv;classificazioni;classificazioni analytics
description: Scopri come i feed importano le entità in [!DNL Adobe Target] [!DNL Recommendations] utilizzando i file CSV, [!DNL Google Product Search] formato di feed, e [!DNL Analytics] classificazioni di prodotto.
title: Come si utilizza [!UICONTROL Feeds] in [!DNL Target Recommendations]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."
feature: Recommendations
hide: true
hidefromtoc: true
source-git-commit: f3b1281cfbfb70703ac33776b3ed964360b3db3a
workflow-type: tm+mt
source-wordcount: '2423'
ht-degree: 38%

---

# Feed

Utilizzare i feed per importare le entità in [!DNL Adobe Target] [!DNL Recommendations]. Le entità possono essere inviate tramite file CSV, il [!DNL Google Product Search] formato di feed, e [!DNL Adobe Analytics] classificazioni di prodotto.

## Panoramica sui feed {#concept_D1E9C7347C5D4583AA69B02E79607890}

I feed consentono di trasmettere [Entità](/help/main/c-recommendations/c-products/products.md) oppure puoi aggiungere ai dati mbox informazioni non disponibili nella pagina o per le quali l’invio diretto dalla pagina non è sicuro. Ad esempio, margine, costo merce venduta (Costo merce venduta, COGS) e così via.

I feed consentono inoltre di trasmettere informazioni dettagliate sull’oggetto a [!DNL Recommendations], ad esempio ID prodotto, categoria, nome, messaggio e altri attributi.

È possibile selezionare le colonne dal [!DNL Target] file di classificazioni di prodotto o [!DNL Google Product Search] file da inviare al [!DNL Recommendations] server.

Questi dati su ciascun elemento possono quindi essere utilizzati per:

* Visualizza valori nelle progettazioni
* Definire le regole di inclusione dei criteri
* Ordinare gli elementi in diverse raccolte
* Applicare esclusioni ai consigli

Le descrizioni degli articoli possono essere trasmesse in [!DNL Target] utilizzando feed o mbox. Se [!DNL Target] raccoglie dati utilizzando sia un feed di entità che una mbox; in tal caso, prevalgono i dati più recenti. Solitamente i dati più recenti provengono da una mbox, in quanto questa viene visualizzata più spesso. Nel raro caso in cui i dati del feed di entità e i dati della mbox vengano inviati contemporaneamente, verranno utilizzati i secondi.

Il [!UICONTROL Feeds] list ( **[!UICONTROL Recommendations]** > **[!UICONTROL Feeds]**) fornisce informazioni su eventuali feed creati.

![Pagina Feed](/help/main/c-recommendations/c-products/assets/feeds-page-new.png)

Il [!UICONTROL Feeds] La pagina contiene le colonne seguenti:

* **Nome**: nome del feed specificato durante la creazione. Per modificare il nome di un feed, dovrai modificare il feed stesso. Quando salvi il feed con il nuovo nome, il feed viene aggiornato.
* **Stato**: lo [stato](/help/main/c-recommendations/c-products/feeds.md#concept_E475986720D1400999868B3DFD14A7A0) corrente del feed.
* **Tipo**: i tipi includono [CSV](/help/main/c-recommendations/c-products/feeds.md#section_65CC1148C7DD448FB213FDF499D35FCA), [[!DNL Google Product Feed]](/help/main/c-recommendations/c-products/feeds.md#section_8EFA98B5BC064140B3F74534AA93AFFF), e [Classificazioni di Analytics](/help/main/c-recommendations/c-products/feeds.md#section_79E430D2C75443BEBC9AA0916A337E0A).
* **Elementi**: visualizza il numero di elementi presenti nel feed.
* **Pianificazione**: visualizza la pianificazione di aggiornamento per il feed: [!UICONTROL Daily], [!UICONTROL Weekly], [!DNL Every 2 Weeks], o [!UICONTROL Never].
* **Ultimo aggiornamento**: visualizza la data e l’ora dell’ultimo aggiornamento del feed e il nome della persona che lo ha eseguito.

Fai clic su [!UICONTROL Customize Table] icona ( ![Icona Personalizza tabella](/help/main/c-recommendations/c-products/assets/customize-table-icon.png) ) per selezionare o deselezionare le colonne da visualizzare.

Fai clic su [!UICONTROL Information] per visualizzare una scheda che mostra la data dell’ultimo caricamento e l’URL del feed.

Fai clic sull’icona dei puntini di sospensione per accedere alle azioni seguenti: [!UICONTROL Deactivate], [!DNL Edit], [!UICONTROL Copy], e [!UICONTROL Delete].

>[!IMPORTANT]
>
>Le entità e gli attributi di entità caricati scadono dopo 61 giorni. Ciò significa che:
>
>* Il feed deve essere eseguito almeno una volta al mese per garantire che il contenuto del catalogo non scada.
>* La rimozione di un elemento dal file di feed non ne comporta la rimozione dal catalogo. Per rimuovere l&#39;articolo dal catalogo, eliminarlo manualmente tramite [!DNL Target] Interfaccia utente o API. In alternativa, modificare gli attributi dell&#39;articolo (ad esempio l&#39;inventario) per assicurarsi che l&#39;articolo sia escluso dal corrispettivo.

## Tipi di origine

Le entità possono essere inviate tramite file CSV, il [!DNL Google Product Search] formato di feed, e [!DNL Adobe Analytics] classificazioni di prodotto.

### CSV {#section_65CC1148C7DD448FB213FDF499D35FCA}

È possibile creare un file .csv utilizzando [!DNL Adobe] formato di caricamento CSV proprietario. Nel file sono contenute informazioni sulla visualizzazione degli attributi riservati e personalizzati per i prodotti. Per caricare attributi specifici nell’implementazione, sostituisci `CustomN` nella riga di intestazione con il nome dell’attributo che desideri utilizzare. Nell’esempio di seguito, `entity.Custom1` è stato sostituito da: `entity.availability`. Successivamente, puoi utilizzare il metodo di caricamento collettivo per caricare il file nel server della funzionalità [!DNL Recommendations].

L&#39;utilizzo del formato .csv presenta i seguenti vantaggi rispetto al [!DNL Google] formato feed:

* Il formato .csv non richiede mappature di campi.
* Il formato .csv supporta attributi con più valori (vedi l’esempio di seguito).
* Il formato .csv supporta fino a 100 attributi personalizzati. Se ti servono più di 100 attributi personalizzati, puoi specificarne un altro set con un secondo file di feed.

Utilizza il metodo di caricamento in blocco per inviare informazioni di visualizzazione se non disponi di mbox sulla pagina o se desideri integrare le informazioni di visualizzazione con elementi non disponibili sul sito. Ad esempio, puoi inviare informazioni di inventario non pubblicate sul sito.

Qualsiasi dato caricato utilizzando il file .csv, il feed di prodotto Google o [!DNL Analytics] Il feed di classificazione del prodotto sovrascrive il valore dell’attributo dell’entità esistente nel database. Se invii informazioni sul prezzo tramite richieste mbox e poi invii diversi valori prezzo nel file, questi valori sovrascrivono quelli impostati con la richiesta mbox. Fa eccezione l’attributo dell’entità `categoryId` dove i valori della categoria vengono aggiunti invece di essere sovrascritti fino al limite di 250 caratteri.

>[!IMPORTANT]
>
>Non racchiudere i valori tra virgolette doppie (&quot;) nel file .csv, a meno che queste non siano intenzionali. Se racchiudi i valori tra virgolette doppie, devi racchiuderli in un altro insieme di virgolette doppie. In caso contrario, il feed dei consigli non verrà caricato correttamente.

Ad esempio, la sintassi seguente non è corretta:

```
"Apples "Bananas" Grapes"",
```

La sintassi corretta è:

```
"Apples ""Bananas"" Grapes""",
```

>[!NOTE]
>
>Non è possibile sovrascrivere un valore esistente con un valore vuoto. Passa un altro valore al suo posto per sovrascrivere il valore esistente. Nel caso di un prezzo di vendita, una soluzione comune è quella di passare un &quot;NULL&quot; effettivo o qualche altro messaggio. Puoi quindi scrivere una regola di modello per escludere gli elementi con tale valore.

Il prodotto è disponibile nell’interfaccia di amministrazione circa due ore dopo il corretto caricamento della relativa entità.

Di seguito è riportato un codice di esempio per un file .csv:

```
## RECSRecommendations Upload File 
## RECS''## RECS'' indicates a Recommendations pre-process header. Please do not remove these lines. 
## RECS 
## RECSUse this file to upload product display information to Recommendations. Each product has its own row. Each line must contain 19 values and if not all are filled a space should be left. 
## RECSThe last 100 columns (entity.custom1 - entity.custom100) are custom. The name 'customN' can be replaced with a custom name such as 'onSale' or 'brand'. 
## RECSIf the products already exist in Recommendations then changes uploaded here will override the data in Recommendations. Any new attributes entered here will be added to the product''s entry in Recommendations. 
## RECSentity.id,entity.name,entity.categoryId,entity.message,entity.thumbnailUrl,entity.value,entity.pageUrl,entity.inventory,entity.margin,entity.last_updated_by,entity.multi_english,entity.availability,entity.tax_country,entity.tax_region,entity.tax_rate,entity.product_type,entity.item_group_id,entity.color,entity.size,entity.brand,entity.gtin 
na3456,RipCurl Watch with Titanium Dial,Watches & Sport,Cutting edge titanium with round case,https://example.com/s7/na3456_Viewer,425,https://example.com/shop/en-us/na3456_RipCurl,24,0.25,csv,"[""New"",""Web"",""Sales"",""[1,2,34,5]""]",in stock,US,CA,9.25,Shop by Category > Watches,dz1,Titanium,44mm,RipCurl,"075380 01050 5" 
na3457,RipCurl Watch with Black Dial,Watches & Sport,Cutting edge matte black with round case,https://example.com/s7/na3457_Viewer,275,https://example.com/shop/en-us/na3457_RipCurl,24,0.27,csv,"[""New"",""Web"",""Sales"",""[1,2,34,5]""]",in stock,US,CA,9.25,Shop by Category > Watches,dz1,Black,44mm,RipCurl,"075340 01060 7"
```

### [!DNL Google] {#section_8EFA98B5BC064140B3F74534AA93AFFF}

Il [!DNL Google Product Search] il tipo di feed utilizza [!DNL Google] formato. Questo è diverso dal [!DNL Adobe] formato di caricamento CSV proprietario.

Se disponi di un [!DNL Google Product Feed], puoi utilizzarlo come file di importazione.

>[!NOTE]
>
>Non è necessario utilizzare [!DNL Google] dati. [!DNL Recommendations] utilizza lo stesso formato di [!DNL Google]. Puoi utilizzare questo metodo per caricare qualsiasi dato a tua disposizione e utilizzare le funzioni di pianificazione disponibili. Tuttavia, è necessario mantenere [!DNL Google] nomi di attributi predefiniti quando si imposta il file.

La maggior parte dei retailer carica i prodotti in [!DNL Google], quindi quando un visitatore utilizza [!DNL Google] ricerca di prodotti, vengono visualizzati i relativi prodotti. [!DNL Recommendations] segue la [!DNL Google] specifica esatta per i feed di entità. I feed di entità possono essere inviati a [!DNL Recommendations] tramite .xml, .txt o .tsv e può utilizzare [attributi definiti da Google](https://support.google.com/merchants/answer/188494?hl=en&amp;topic=2473824&amp;ctx=topic#US). È possibile cercare i risultati in [[!DNL Google] pagine acquisti](https://www.google.com/prdhp).

>[!NOTE]
>
>Il metodo POST deve essere consentito nel server che ospita il [!DNL Google] contenuto del feed.

Perché [!DNL Recommendations] gli utenti configurano già feed .xml o .txt da inviare a [!DNL Google] tramite URL o FTP, i feed di entità accettano tali dati di prodotto e li utilizzano per creare il catalogo dei consigli. Specifica la posizione di tale feed per fare in modo che il server dei consigli recuperi i dati.

Se usa [!DNL Google Product Search] per il caricamento del feed di entità, è comunque necessario disporre di una mbox per pagina di prodotto nella pagina se desideri mostrare i consigli o tenere traccia delle visualizzazioni di prodotto per la distribuzione dell’algoritmo in base alle visualizzazioni.

[!DNL Google] i feed non supportano più valori per un attributo personalizzato.

Il feed viene eseguito al momento del salvataggio e dell’attivazione. Viene eseguito al momento del salvataggio del feed, quindi ogni giorno un’ora dopo.

Di seguito è riportato un codice di esempio per [!DNL Google Product Search] file xml feed:

```
<?xml version="1.0" encoding="UTF-8" standalone="yes"?> 
<feed xmlns="https://www.w3.org/2005/Atom" xmlns:ns2="https://base.google.com/ns/1.0" xmlns:ns3="https://base.google.com/cns/1.0"> 
    <title>Product Feed</title> 
    <link href="https://example.com"/> 
    <updated>2017-12-13T08:45:04.918-08:00</updated> 
    <author> 
        <name>Product Feed Author</name> 
    </author> 
    <id>https://example.com</id> 
    <entry> 
        <title>RipCurl Watch with Titanium Dial</title> 
        <description>Cutting edge Titanium with Round case</description> 
        <ns2:id>na3452</ns2:id> 
        <ns2:link>https://example.com/shop/en-us/na3452_RipCurl</ns2:link> 
        <ns2:availability>in stock</ns2:availability> 
        <ns2:condition>NEW</ns2:condition> 
        <ns2:google_product_category>Watches &amp; Sport</ns2:google_product_category> 
        <ns2:gtin>075380 01050 5</ns2:gtin> 
        <ns2:image_link>https://example.com/s7/na3452_Viewer</ns2:image_link> 
        <ns2:mobile_link>https://m.example.com/s7/na3452_Viewer</ns2:mobile_link> 
        <ns2:mpn>71050</ns2:mpn> 
        <ns2:price>425</ns2:price> 
        <ns2:product_review_average>5.0</ns2:product_review_average> 
        <ns2:product_review_count>30</ns2:product_review_count> 
        <ns2:product_type>Shop by Category > Watches </ns2:product_type> 
        <ns2:brand>RipCurl</ns2:brand> 
        <ns2:sale_price>375</ns2:sale_price> 
        <ns2:tax> 
          <ns2:country>US</ns2:country> 
          <ns2:region>CA</ns2:region> 
          <ns2:rate>9.25</ns2:rate> 
          <ns2:tax_ship>y</ns2:tax_ship> 
        </ns2:tax> 
        <ns2:is_bundle>N</ns2:is_bundle> 
    </entry> 
    <entry> 
        <title>RipCurl Watch with Black Dial</title> 
        <description>Cutting edge matte black with Round case</description> 
        <ns2:id>na3453</ns2:id> 
        <ns2:link>https://example.com/shop/en-us/na3453_RipCurl</ns2:link> 
        <ns2:availability>in stock</ns2:availability> 
        <ns2:condition>NEW</ns2:condition> 
        <ns2:google_product_category>Watches &amp; Sport</ns2:google_product_category> 
        <ns2:gtin>075380 013450 5</ns2:gtin> 
        <ns2:image_link>https://example.com/s7/na3453_Viewer</ns2:image_link> 
        <ns2:mobile_link>https://m.example.com/s7/na3453_Viewer</ns2:mobile_link> 
        <ns2:mpn>71050</ns2:mpn> 
        <ns2:price>275</ns2:price> 
        <ns2:product_review_average>4.8</ns2:product_review_average> 
        <ns2:product_review_count>23</ns2:product_review_count> 
        <ns2:product_type>Shop by Category > Watches </ns2:product_type> 
        <ns2:brand>RipCurl</ns2:brand> 
        <ns2:sale_price>249</ns2:sale_price> 
        <ns2:tax> 
          <ns2:country>US</ns2:country> 
          <ns2:region>CA</ns2:region> 
          <ns2:rate>9.25</ns2:rate> 
          <ns2:tax_ship>y</ns2:tax_ship> 
        </ns2:tax> 
        <ns2:is_bundle>N</ns2:is_bundle> 
    </entry> 
</feed> 
```

Di seguito è riportato un codice di esempio per [!DNL Google Product Search] file .tsv feed:

```
id    title    description    link    price    condition    availability    image_link    tax    shipping_weight    shipping    google_product_category    product_type    item_group_id    color    size    gender    age_group    pattern    brand    gtin    mpn 
na3454    RipCurl Watch with Titanium Dial    Cutting edge titanium with round case    https://example.com/shop/en-us/na3454_RipCurl    425    new    in stock    https://example.com/s7/na3452_Viewer    US:CA:9.25:y    1.5 oz    US:::0.00 USD    Watches & Sport    Shop by Category > Watches    dz1    Black    44mm    male    adult    Solid    RipCurl    075380 01050 5    DZ1437 
na3455    RipCurl Watch with Black Dial    Cutting edge matte black with round case    https://example.com/shop/en-us/na3455_RipCurl    275    new    in stock    https://example.com/s7/na3452_Viewer    US:CA:9.25:y    1.5 oz    US:::0.00 USD    Watches & Sport    Shop by Category > Watches    dz1    Black    44mm    male    adult    Solid    RipCurl    075340 01060 7    DZ1446
```

### [!DNL Analytics] Classificazioni prodotto {#section_79E430D2C75443BEBC9AA0916A337E0A}

Il [!DNL Adobe Analytics] La classificazione del prodotto è l’unica classificazione disponibile per i consigli. Per ulteriori informazioni su questo file di classificazione, consulta [Informazioni sulle classificazioni](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) nel *Componenti di Analytics* guida. È possibile che non tutte le informazioni necessarie per i consigli siano disponibili nell’implementazione corrente. Per aggiungere elementi al file delle classificazioni, consulta quindi questa guida utente.

>[!IMPORTANT]
>
>Prima di importare i dati di entità in [!DNL Recommendations] utilizzo [!DNL Analytics] classificazioni di prodotto, tieni presente che questo non è il metodo preferito.
>
> In particolare, tieni conto dei seguenti aspetti:
>
>* Gli aggiornamenti agli attributi di entità subiscono un ritardo aggiuntivo fino a 24 ore.
>* [!DNL Target] supporta [!UICONTROL Product Classifications] solo. Il [!DNL Analytics] lo SKU del prodotto deve essere mappato sullo stesso livello del [!DNL Recommendations] `entity.id`. Personalizzato [!DNL Analytics] Le classificazioni possono essere progettate utilizzando [!UICONTROL Adobe Consulting Services]. Per qualsiasi domanda, contatta il tuo Account Manager.

## Creazione di un feed {#steps}

Crea un feed per inserire le informazioni sui prodotti o i servizi in [!DNL Recommendations].

1. Dall&#39;interno del [!DNL Target] , fare clic su **[!UICONTROL Recommendations]** > **[!UICONTROL Feeds]** > **[!UICONTROL Create Feed]**.

   ![Finestra di dialogo Crea feed](assets/CreateFeed.png)

1. Specifica un nome descrittivo per il feed.
1. Seleziona un **[!UICONTROL Source Type]**.

   * [!UICONTROL CSV]
   * [!UICONTROL Google Product Feed]
   * [!UICONTROL Analytics Classifications]

   Per informazioni su [!UICONTROL CSV] e [!UICONTROL Google Product Feed] tipi di feed, vedi [Panoramica dei feed](/help/main/c-recommendations/c-products/feeds.md#concept_D1E9C7347C5D4583AA69B02E79607890). È inoltre possibile [scarica una guida ai modelli CSV](/help/main/c-recommendations/c-products/assets/EntityFileUploadTemplate.csv) per formattare correttamente il feed.

1. (Condizionale) Se hai selezionato **[!UICONTROL CSV]** o **[!UICONTROL Google Product Feed]**, specifica il percorso in cui il feed è accessibile.

   * **FTP**: se hai selezionato FTP, indica le informazioni relative al server FTP, le credenziali di accesso, il nome del file e la directory FTP. Per caricamenti più sicuri, puoi utilizzare l’FTP con SSL (FTPS).

     Impostazioni del server FTP supportate:

      * FTP e FTPS devono essere impostati per FTP passivo.
      * Per FTPS, configura il server per accettare connessioni FTPS esplicite.
      * SFTP non è supportato.
      * È possibile specificare manualmente una porta su cui avviare la connessione (ad esempio, `ftp://ftp.yoursite.com:2121`). Se non specifichi una porta, viene usata la porta FTP o FTPS predefinita.

   * **URL**: se selezioni [!UICONTROL URL], specifica l’URL.

1. (Condizionale) Se hai selezionato **[!UICONTROL Analytics Classifications]**, scegli la suite di rapporti dall’elenco a discesa.

1. Fai clic su **[!UICONTROL Next]** freccia per visualizzare [!UICONTROL Schedule] opzioni.

   ![Risultato passaggio](assets/CreateFeedSchedule.png)

1. Seleziona un’opzione di aggiornamento:

   * [!UICONTROL Daily]
   * [!UICONTROL Weekly]
   * [!UICONTROL Every 2 Weeks]
   * [!UICONTROL Never]: non pianificare un aggiornamento. Scegli questa opzione se non desideri eseguire il feed.

1. Specifica l’ora in cui desideri eseguire il feed.

   Questa opzione si basa sul fuso orario utilizzato nel browser. Se desideri utilizzare l’orario di un fuso orario diverso, dovrai calcolarlo in base al tuo fuso orario attuale.

1. Fai clic su **[!UICONTROL Next]** freccia per visualizzare [!UICONTROL Mapping] , quindi specificare la modalità di mappatura dei dati [!DNL Target] definizioni.

   ![Risultato passaggio](assets/CreatFeedMapping.png)

1. (Facoltativo) Se desideri che il feed appartenga a un ambiente (gruppo di host), seleziona il gruppo di host.

   Per impostazione predefinita, il feed appartiene a tutti i gruppi di host. Gli elementi contenuti in questo feed saranno quindi sempre disponibili, in qualsiasi ambiente. Per ulteriori informazioni, consulta [Host](/help/main/administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E).

1. Clic **[!UICONTROL Save]**.

Dopo aver creato o modificato un feed, questo viene eseguito immediatamente. Il feed viene quindi aggiornato in base ai parametri impostati. La disponibilità delle informazioni richiede del tempo. Innanzitutto, prima di essere pubblicato e reso disponibile, il feed deve essere sincronizzato, elaborato e indicizzato. Lo stato corrente viene visualizzato in [Stato feed](/help/main/c-recommendations/c-products/feeds.md#status) nel [!UICONTROL Feeds] elenco. È possibile chiudere [!DNL Target] prima del completamento del processo; questo continuerà ad essere in esecuzione.

Durante l’indicizzazione, prodotti e intestazioni dei feed vengono visualizzati prima dell’effettiva indicizzazione dei singoli valori. Questo consente di cercare e visualizzare i prodotti in modo da poter creare raccolte, esclusioni, progettazioni e attività prima che l’indicizzazione sia stata completata.

Lo stato “Completato” indica che il file è stato trovato e analizzato correttamente. Le informazioni non sono disponibili per l’utilizzo all’interno di [!DNL Recommendations] finché il file non viene indicizzato, operazione che può richiedere un po’ di tempo, a seconda della dimensione del file. Se il processo non riesce, significa che il file non è stato trovato. Ad esempio, hai utilizzato un URL errato o informazioni FTP errate oppure si è verificato un errore di analisi.

## Stati e indicatori dei feed {#concept_E475986720D1400999868B3DFD14A7A0}

Informazioni sui possibili stati dei feed e sui relativi indicatori.

### Stato dei feed {#status}

Di seguito sono riportati gli stati possibili per un feed:

| Stato | Descrizione |
|--- |--- |
| [!UICONTROL Syncing] | I dettagli della configurazione dei feed vengono salvati in [!DNL Target]. |
| [!UICONTROL Sync Failed] | Impossibile salvare i dettagli di configurazione dei feed in [!DNL Target]. Riprova. |
| [!UICONTROL No Feed Run] | Hai creato un feed che non è stato pianificato (la frequenza è impostata su Mai). |
| Pianificato per *data e ora* | Il feed non è stato eseguito, ma è pianificato per essere eseguito alla data e all’ora specificate. |
| [!UICONTROL Waiting for Download] | [!DNL Target] si sta preparando per il download del file di feed. |
| [!UICONTROL Downloading Feed File] | [!DNL Target] sta scaricando il file di feed. |
| [!UICONTROL Importing Items] | [!DNL Target] sta importando elementi dal file di feed. |
| Feed importato correttamente alle *ora* | [!DNL Target] ha importato il file di feed nel suo sistema di distribuzione dei contenuti. Le modifiche apportate agli attributi degli elementi sono state inserite nel sistema di distribuzione dei contenuti e presto saranno applicate ai consigli consegnati. Se non visualizzi le modifiche previste, riprova e aggiorna la pagina contenente i consigli.<br>Note:<ul><li>Se le modifiche apportate agli attributi di un elemento ne determinano l’esclusione dai consigli, tale esclusione viene applicata immediatamente. Se un elemento è stato aggiunto di recente, oppure se le modifiche apportate agli attributi causano l&#39;aggiunta di un elemento *non più* escluso dai consigli, viene applicato al successivo aggiornamento dell’algoritmo, che si verifica entro 24 ore.</li><li>Quando viene visualizzato questo stato, è possibile che gli aggiornamenti non risultino ancora visibili nel [!UICONTROL Catalog Search] UI. Uno stato separato è elencato in [!UICONTROL Catalog Search] che indica l’ultimo aggiornamento del catalogo ricercabile.</li></ul> |
| [!UICONTROL Failed to Index] | L’operazione di indicizzazione non è riuscita. Riprova. |
| [!UICONTROL Server Not Found] | I percorsi FTP o URL non sono validi o sono irraggiungibili. |

Per aggiornare un feed (ad esempio, per apportare modifiche alla configurazione del feed o al file di feed), aprilo, apporta le modifiche desiderate e fai clic su **[!UICONTROL Save]**.

>[!IMPORTANT]
>
>Le entità caricate scadono dopo 61 giorni. Significa che il file di feed deve essere caricato almeno ogni 60 giorni per evitare un’interruzione delle attività di Consigli. Se un elemento non è incluso in un file di feed (o in un altro metodo di aggiornamento entità) almeno una volta ogni 60 giorni, [!DNL Target] deduce che l&#39;elemento non è più rilevante e lo rimuove dal catalogo.

### Indicatori di stato dei feed {#section_3C8A236C5CB84C769A9E9E36B8BFABA4}

I seguenti indicatori di stato dei feed vengono visualizzati nel [!UICONTROL Status] colonna:

| Indicatore di stato | Descrizione |
|--- |--- |
| Indicatore di stato verde | Quando l’indicizzazione del feed viene terminata con successo, viene visualizzato un indicatore di stato verde. |
| Indicatore di stato giallo | Quando un feed o l’indice di un feed viene ritardato del 25% rispetto alla sua frequenza, viene visualizzato un indicatore di stato giallo. Ad esempio, viene visualizzato un punto giallo per una serie di feed da eseguire giornalmente se l’indice non è stato completato sei ore dopo l’ora pianificata. Nota: una volta che lo stato del feed è &quot;In attesa della coda indice&quot;, i valori appena aggiornati sono disponibili nell’elaborazione della consegna e dei criteri. |
| Indicatore di stato bianco | Quando un feed non è pianificato, viene visualizzato un indicatore di stato bianco a indicare che il feed non è ancora stato eseguito. |
| Indicatore di stato rosso | Se il feed non riesce a caricare i dati sul server, viene visualizzato un indicatore di stato rosso. |

Prendi in considerazione gli esempi seguenti:

**Esempio 1:**

* Primo giorno: i processi di alimentazione giornalieri sono effettuati alle 9.00 PST.
* Giorno 2: sono le 15.30 e il feed non viene eseguito da ieri alle 09.00.

Lo stato visualizzato sarà giallo, perché l’indice doveva essere eseguito circa 6 ore e 30 minuti fa. 6 ore e 30 minuti + 24 ore rappresentano il 127% della finestra del feed.

**Esempio 2:**

* 1 gennaio: processi di feed mensili alle 9:00 PST.
* 3 febbraio: sono le 10:00 e il feed non viene eseguito da un mese, un giorno e un’ora.

Lo stato visualizzato sarà giallo, perché l’indice doveva essere eseguito circa un giorno e un’ora fa. Anche se questo rappresenta solo l’1,03% delle impostazioni di frequenza [(31 + (1/25))/30 = 1,03%], il ritardo massimo di un giorno è stato superato.

## Video di formazione

I video seguenti contengono ulteriori informazioni sui concetti descritti in questo articolo.

### Informazioni sui feed in Recommendations (3:01) ![Badge panoramica](/help/main/assets/overview.png)

Questo video contiene le seguenti informazioni:

* Comprendere lo scopo dei feed
* Comprendere il valore dei feed

>[!VIDEO](https://video.tv.adobe.com/v/27695)

### Creare un feed (6:44) ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video contiene le seguenti informazioni:

* Impostare un feed
* Quale tipo di feed usare

>[!VIDEO](https://video.tv.adobe.com/v/27696)