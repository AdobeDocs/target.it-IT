---
keywords: criteria;algorithm;industry vertical;page type;recommendation key;recommendation logic;logic;data range;behavior data source;partial design;backup recommendations;inclusion rules;attribute weighting;current category;custom attribute;last purchased item;last viewed item;most viewed item;most viewed item;favorite category;popularity;recently viewed item;last purchased;last viewed;most viewed;favorite;recently viewed
description: I criteri controllano il contenuto delle attività di Adobe Recommendations. Crea dei criteri per visualizzare i consigli più appropriati per l’attività.
title: Creare criteri
feature: criteria
uuid: 603d4b02-cdb6-40aa-9654-0086c23b0c8e
translation-type: tm+mt
source-git-commit: 108bbe65732b7df20caf9df6b3e5b77e3c31c457
workflow-type: tm+mt
source-wordcount: '2422'
ht-degree: 66%

---


# ![PREMIUM](/help/assets/premium.png) Creare criteri{#create-criteria}

I criteri in [!UICONTROL Adobe Target] [!UICONTROL Recommendations] controllano il contenuto delle attività di [!UICONTROL Recommendations] . Crea dei criteri per visualizzare i consigli più appropriati per l’attività. Questi criteri utilizzano le azioni del visitatore per determinare il contenuto o i prodotti da visualizzare.

Nelle sezioni seguenti viene illustrato come creare un nuovo criterio.

## Accedere alla schermata Crea nuovo criterio

Esistono diversi modi per raggiungere la schermata [!UICONTROL Crea nuovo criterio]. Alcune opzioni dipendono dal modo in cui si raggiunge la schermata.

* On the **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** library screen, click **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**. I criteri creati vengono automaticamente resi disponibili per tutte le attività di [!DNL Recommendations].
* Quando create un&#39; [!DNL Recommendations] attività utilizzando Visual Experience Composer (VEC) (Compositore esperienza [!UICONTROL visivo] ), viene visualizzata immediatamente la schermata [!UICONTROL Select Criteria (Seleziona criteri] ) dopo che avete selezionato un elemento nella pagina e fate clic su [!UICONTROL Replace w/ Recommendations], [!UICONTROL Insert Recommendations Before](Inserisci prima [!UICONTROL ) o]Insert Recommendations After. Potete quindi selezionare un criterio disponibile oppure fare clic su **[!UICONTROL Crea criteri]**. Se create un nuovo criterio, potete salvare i criteri da usare con altre [!DNL Recommendations] attività. For more information, see [Create a Recommendations activity](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md).
* Quando modifichi un’attività di [!DNL Recommendations], fai clic su una casella di [!UICONTROL Posizione Consigli] nella pagina e seleziona **[!UICONTROL Cambia criteri]**. On the [!UICONTROL Select Criteria] screen, click **[!UICONTROL Create Criteria]**. Sarà possibile salvare i nuovi criteri da utilizzare per altre attività di [!DNL Recommendations].

Nella procedura seguente si presuppone che sia possibile accedere alla schermata [!UICONTROL Crea nuovo criterio] utilizzando il primo metodo: nella schermata Libreria **[!UICONTROL Recommendations]** > **[!UICONTROL Criteri]** .

1. Fate clic su **[!UICONTROL Recommendations]** > **[!UICONTROL Criteri]**.

1. Fate clic su **[!UICONTROL Crea criteri]** > **[!UICONTROL Crea criteri]**.

   ![Creare nuovi criteri](/help/c-recommendations/c-algorithms/assets/CreateNewCriteria_full-new.png)

1. Configurate le informazioni nelle sezioni seguenti.

## Informazioni di base {#info}

1. Inserisci un **[!UICONTROL Nome criterio]**.

   Si tratta del nome “interno” usato per descrivere i criteri. Ad esempio, potresti voler chiamare i tuoi criteri “prodotti di margine più alto”, ma non vuoi che questo titolo venga visualizzato pubblicamente. Vedi il passo successivo per impostare il titolo visualizzato dal pubblico.

   ![Sezione Informazioni di base](/help/c-recommendations/c-algorithms/assets/basic-information.png)

1. Inserisci un **[!UICONTROL Titolo da visualizzare]**, che verrà mostrato nella pagina per i consigli che utilizzano questo criterio.

   Ad esempio, potresti voler visualizzare “Le persone che hanno visto questo, hanno visto anche” o “Prodotti simili”, quando utilizzi questo criterio per mostrare i consigli.

1. Inserisci una breve **[!UICONTROL descrizione]** dei criteri.

   La descrizione dovrebbe facilitare l&#39;identificazione dei criteri e potrebbe includere informazioni sullo scopo dei criteri.

1. Selezionate un settore verticale in base agli obiettivi dell&#39;attività delle raccomandazioni.

   | Settore verticale | Obiettivo |
   |--- |--- |
   | Retail/E-commerce | Conversione con conseguente acquisto |
   | Generazione di lead/B2B/servizi finanziari | Conversione senza acquisto |
   | Media/Editoria | Coinvolgimento |

   Altre opzioni di criteri cambieranno in base al verticale di settore selezionato.

1. Seleziona un **[!UICONTROL tipo di pagina]**.

   Puoi selezionare più tipi di pagina.

   Insieme, tipi di pagina e verticali del settore vengono utilizzati per categorizzare i criteri salvati, semplificandone il riutilizzo per altre attività di [!DNL Recommendations].

1. Seleziona una **[!UICONTROL Chiave consiglio]**.

   Per ulteriori informazioni sui criteri basati su una chiave, consulta [Basare il consiglio su una Chiave consiglio](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md).

1. Seleziona la **[!UICONTROL Logica consigli]**.

   Per ulteriori informazioni sulle opzioni di logica per i consigli, consulta [Criteri](../../c-recommendations/c-algorithms/algorithms.md).

   >[!NOTE]
   >
   >If you select **[!UICONTROL Items]**/ **[!UICONTROL Media with Similar Attributes]**, you will have the option to set [content similarity rules](#similarity).

## Origine dati {#data-source}

1. Imposta l’**[!UICONTROL Intervallo di dati]** per determinare l’intervallo di tempo dei dati cronologici disponibili sul comportamento dell’utente da utilizzare per determinare quali consigli visualizzare.

   ![Cursore intervallo dati](/help/c-recommendations/c-algorithms/assets/data-range.png)

   Se il sito genera molto traffico e i comportamenti si modificano spesso, scegli una finestra dati più breve. Una finestra più breve consente a [!DNL Recommendations] di essere più reattivo alle modifiche all’interno del mercato e della tua attività. Ad esempio, una finestra più breve implica che [!DNL Recommendations] rileverà le modifiche nel comportamento dei visitatori quando questi iniziano lo shopping stagionale, ad esempio quello natalizio o per il rientro a scuola, raccomandando gli articoli appropriati.

   In presenza di un volume limitato di dati, o se il comportamento dei visitatori non si modifica di frequente, puoi selezionare una finestra più ampia. Tuttavia, per molti siti, una finestra più breve determinerà i consigli migliori.

   Gli intervalli di dati disponibili sono:

   * Due giorni
   * Una settimana
   * Due settimane
   * Un mese
   * Due mesi

1. (Conditional) Select the desired **[!UICONTROL Behavioral Data Source]**: [!UICONTROL mboxes] or [!UICONTROL Analytics].

   >[!NOTE]
   >
   >La sezione Origine [!UICONTROL dati] comportamentali viene visualizzata solo se l&#39;implementazione utilizza [Analytics per Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T).

   ![Sezione Origine dati comportamentale](/help/c-recommendations/c-algorithms/assets/behavioural-data-source.png)

   Se si sceglie [!UICONTROL Analytics], selezionare la suite di rapporti desiderata.

   If the criteria uses [!DNL Adobe Analytics] as the behavioral data source, once created, the time for criteria availability depends on whether the selected report suite and lookback window has been used for any other criteria, as explained below:

   * **Configurazione una tantum della suite di rapporti**: la prima volta che una suite di rapporti viene utilizzata con una specifica finestra di lookback dei dati, [!DNL Target Recommendations] può richiedere da due a sette giorni per scaricare completamente i dati comportamentali della suite di rapporti selezionata da [!DNL Analytics]. This time frame is dependent on the [!DNL Analytics] system load.
   * **Criteri nuovi o modificati che utilizzano una suite di rapporti già disponibile**: se crei un nuovo criterio o ne modifichi uno esistente e la suite di rapporti selezionata è già utilizzata per [!DNL Target Recommendations] con un intervallo di dati uguale o inferiore a quello selezionato, i dati diventano subito disponibili e non è richiesta alcuna configurazione una tantum. In questo caso, oppure se le impostazioni di un algoritmo vengono modificate senza che si modifichi la suite di rapporti o l’intervallo di dati selezionato, l’algoritmo viene eseguito o rieseguito entro 12 ore.
   * **Viene eseguito un algoritmo continuo**: i dati scorrono da [!DNL Analytics] a [!DNL Target Recommendations] su base giornaliera. Ad esempio, per un consiglio di tipo [!UICONTROL Affinità per articoli visualizzati], quando un utente visualizza un prodotto, a [!DNL Analytics] viene trasmessa una chiamata di tracciamento per visualizzazione prodotto quasi in tempo reale. I dati [!DNL Analytics] vengono inviati a [!DNL Target] all’inizio del giorno successivo e [!DNL Target] esegue l’algoritmo in meno di 12 ore.

   Per ulteriori informazioni, consultate [Usare  Adobe Analytics con Target Recommendations](/help/c-recommendations/c-algorithms/use-adobe-analytics-with-recommendations.md).

## Contenuto {#content}

Content rules determine what happens if the number of recommended items does not fill your [recommendations design](/help/c-recommendations/c-design-overview/design-overview.md). It is possible for [!DNL Recommendations] criteria to return fewer recommendations than your design calls for. Ad esempio, se la progettazione include slot per quattro elementi, ma i criteri consigliano solo due elementi, potete lasciare vuoti gli slot rimanenti o utilizzare le raccomandazioni di backup per riempire gli slot aggiuntivi.

![Sezione Contenuto](/help/c-recommendations/c-algorithms/assets/content.png)

1. (Facoltativo) Fate scorrere l&#39;interruttore di rendering **[!UICONTROL della struttura]** parziale nella posizione &quot;attivato&quot;.

   Verranno compilati tutti gli slot possibili, ma il modello di progettazione potrebbe includere spazio vuoto per gli slot rimanenti. Se questa opzione è disabilitata e il contenuto non è sufficiente per popolare tutti gli slot disponibili, le raccomandazioni non vengono servite e viene invece visualizzato il contenuto predefinito.

   Abilitate questa opzione se desiderate che le raccomandazioni siano servite con slot vuoti. Utilizzate le raccomandazioni di backup se desiderate che gli slot delle raccomandazioni siano compilati con contenuto in base ai criteri specificati, con slot vuoti riempiti con contenuto simile o popolare dal sito, come spiegato nel passaggio successivo.

1. (Facoltativo) Fate scorrere l’opzione **[!UICONTROL Mostra Recommendations]** backup nella posizione &quot;attivato&quot;.

   Riempite tutti gli slot vuoti rimanenti nel progetto con una selezione casuale di prodotti più visualizzati da tutto il sito.

   L&#39;utilizzo delle raccomandazioni di backup garantisce che la progettazione delle raccomandazioni occupi tutti gli slot disponibili. Supponete di avere una progettazione 4 x 1, come illustrato di seguito:

   ![Design 4 x 1](/help/c-recommendations/c-design-overview/assets/velocity_example.png)

   Supponiamo che i criteri in uso comportino la raccomandazione di due soli elementi. Se abilitate l&#39;opzione Rendering [!UICONTROL progettazione] parziale, i primi due slot vengono riempiti, ma i due slot rimanenti rimangono vuoti. Tuttavia, se abilitate l&#39;opzione [!UICONTROL Mostra Recommendations] backup, i primi due slot vengono compilati in base ai criteri specificati e i due slot rimanenti vengono compilati in base alle raccomandazioni di backup.

   La seguente matrice mostra il risultato che osserverete quando utilizzate le opzioni [!UICONTROL Parziale Design Rendering] e [!UICONTROL Backup Recommendations] :

   | Rendering parziale della progettazione | Consigli di backup | Risultato |
   |--- |--- |--- |
   | Disabilitato | Disabilitato | Se vengono restituiti meno consigli rispetto alle richieste di progettazione, la progettazione dei consigli viene sostituita dal contenuto predefinito e non vengono visualizzate indicazioni. |
   | Abilitato | Disabilitato | La progettazione viene sottoposta a rendering, ma può includere spazio vuoto se vengono restituite meno consigli rispetto al numero richiesto dalla progettazione. |
   | Abilitato | Abilitato | I consigli di backup riempiranno le “posizioni” disponibili della progettazione, eseguendone il rendering completo.<br>Se l&#39;applicazione di regole di inclusione ai consigli di backup limita il numero di quelle qualificate al punto che la progettazione non può essere riempita, la progettazione viene parzialmente sottoposta a rendering.<br>Se i criteri non restituiscono alcun consiglio e le regole di inclusione limitano i consigli di backup a zero, la progettazione viene sostituita con il contenuto predefinito. |
   | Disabilitato | Abilitato | I consigli di backup riempiranno le “posizioni” disponibili della progettazione, eseguendone il rendering completo.<br>Se l&#39;applicazione di regole di inclusione limita il numero di consigli di backup qualificate al punto che la progettazione non può essere riempita, la progettazione viene sostituita dal contenuto predefinito e non vengono visualizzati consigli. |

   Per ulteriori informazioni, consultate [Utilizzare una raccomandazione](/help/c-recommendations/c-algorithms/backup-recs.md)di backup.

1. (Condizionale) Se avete selezionato **[!UICONTROL Mostra Recommendations]** di backup nel passaggio precedente, potete abilitare **[!UICONTROL Applica regole di inclusione alle raccomandazioni]** di backup.

   Le regole di inclusione determinano quali elementi vengono inclusi nelle raccomandazioni. Le opzioni disponibili dipendono dal tuo settore verticale.

   Per ulteriori dettagli consulta [Specificate le regole](#inclusion) di inclusione di seguito.

1. (Facoltativo) Fate scorrere il **[!UICONTROL suggerimento Articoli]** acquistati in precedenza nella posizione &quot;attivato&quot;.

   Questa impostazione è basata su `productPurchasedId`. Il comportamento predefinito è quello di sconsigliare gli articoli acquistati in precedenza. Nella maggior parte dei casi non si desidera promuovere articoli che un cliente ha recentemente acquistato. È utile se si vendono oggetti che le persone solitamente acquistano una sola volta, ad esempio nel caso di un kayak. Se vendete gli articoli che le persone tornano ad acquistare nuovamente su base ripetuta, come shampoo o altri articoli personali, dovreste abilitare questa opzione.

## Somiglianza del contenuto {#similarity}

Utilizza le regole di [!UICONTROL somiglianza del contenuto] per formulare consigli basati su attributi di elemento o file multimediale.

>[!NOTE]
>
>If you selected **[!UICONTROL Items]**/ **[!UICONTROL Media with Similar Attributes]** as your [recommendation logic](#info), you will have the option to set content similarity rules.

Le regole di somiglianza del contenuto confrontano le parole chiave dell&#39;attributo dell&#39;elemento e formulano consigli basati su quante parole chiave hanno in comune diversi elementi. I consigli basati sulla somiglianza del contenuto non richiedono dati precedenti per fornire risultati significativi.

Utilizzare la somiglianza di contenuto per generare consigli è particolarmente efficace per i nuovi elementi, i quali non possono essere mostrati nei consigli utilizzando il criterio *Le persone che hanno visto questo, hanno visto anche* e altre logiche basate sul comportamento precedente. È inoltre possibile utilizzare la somiglianza del contenuto per generare consigli utili per i nuovi visitatori, che non hanno effettuato acquisti in precedenza o non possiedono altri dati storici.

Quando si selezionano **[!UICONTROL elementi]**/**[!UICONTROL supporti con attributi simili]**, è possibile creare regole per aumentare o diminuire l&#39;importanza degli attributi di elementi specifici nella determinazione dei consigli. Per gli articoli quali i libri, si potrebbe voler aumentare l&#39;importanza di attributi come *genere*, *autore*, *serie*, e così via, per consigliare libri simili.

![](assets/ContentSimilarity.png)

Poiché la somiglianza del contenuto utilizza parole chiave per confrontare elementi, alcuni attributi, ad esempio *messaggio* o *descrizione*, possono introdurre “rumore” nel confronto. È possibile creare regole per ignorare questi attributi.

Per impostazione predefinita, tutti gli attributi sono impostati su *Riferimento*. Non è necessario creare una regola a meno che non si desideri modificare questa impostazione.

>[!NOTE]
>
>L&#39;algoritmo di similarità del contenuto potrebbe utilizzare il campionamento casuale nel calcolo della similarità tra gli elementi. Di conseguenza, le valutazioni delle similarità tra gli elementi potrebbero variare a seconda dell&#39;esecuzione dell&#39;algoritmo.

## Regole di inclusione {#inclusion}

Varie opzioni consentono di limitare gli articoli visualizzati nei consigli. Puoi utilizzare le regole di inclusione durante la creazione di criteri o promozioni.

![Regole di inclusione](/help/c-recommendations/c-algorithms/assets/inclusion-rules.png)

Le regole di inclusione sono facoltative. Tuttavia, l&#39;impostazione di questi dettagli consente un maggiore controllo sugli elementi visualizzati nei consigli. Ogni dettaglio configurato restringe ulteriormente i criteri di visualizzazione.

Ad esempio, è possibile scegliere di visualizzare solo le scarpe da donna con una disponibilità di oltre 50 pezzi e un prezzo tra 25 $ e 45 $. È anche possibile ponderare ogni attributo in modo che la probabilità di comparire sia maggiore per gli elementi più importanti per la tua attività.

Per fornire un altro esempio, puoi scegliere di mostrare le posizioni di lavoro disponibili ai visitatori che accedono al sito soltanto da determinate città e che possiedono i titoli universitari richiesti.

Le opzioni di regola di inclusione variano secondo il settore verticale. Per impostazione predefinita, le regole di inclusione vengono applicate ai consigli di backup.

>[!IMPORTANT]
>
>È consigliabile utilizzare le regole di inclusione con cautela. Questi criteri sono utili se, ad esempio, all&#39;interno dell&#39;organizzazione sono utilizzate regole che richiedano di evitare la visualizzazione di un marchio quando ne viene visualizzato un altro. Tuttavia, questa funzione comporta un costo opportunità. Potresti perdere una percentuale di incremento limitando la visualizzazione di alcuni elementi che verrebbero visualizzati normalmente in base ai criteri dell&#39;attività.

Le regole di inclusione sono unite con l&#39;operatore “AND” (E). Gli articoli verranno inclusi in un consiglio solo se vengono soddisfatte tutte le regole.

Per creare una semplice regola di inclusione, come accennato in precedenza, per visualizzare solo le scarpe da donna con una disponibilità di oltre 50 pezzi e un prezzo tra 25 $ e 45 $, attieniti alla seguente procedura:

1. Imposta la fascia di prezzo per i prodotti da consigliare.
1. Imposta la quantità di disponibilità minima i prodotti da consigliare.
1. Configura il consiglio perché mostri gli articoli solo quando sono soddisfatti determinati criteri.

   ![](assets/Recs_InclusionRules.png)

   Puoi specificare che gli articoli siano inclusi solo quando uno degli attributi nell&#39;elenco viene soddisfatto o non corrisponde a uno o più condizioni specificate.

   I valutatori disponibili dipendono dal valore scelto nel primo elenco a discesa. È possibile elencare più elementi. Questi elementi sono valutati con l&#39;operatore “OR”.

   Più regole sono collegate tra loro mediante l&#39;operatore “AND” (E).

   >[!NOTE]
   >
   >Questa opzione limita gli elementi visualizzati nel consiglio. Non interessa le pagine in cui viene visualizzato il consiglio. Per limitare le posizioni di visualizzazione per il consiglio, seleziona le pagine in Compositore esperienza.

For more information, see [Use dynamic and static inclusion rules](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md).

## Ponderazione degli attributi {#weighting}

Potete aggiungere più regole per &quot;indirizzare&quot; l’algoritmo in base a informazioni importanti o metadati relativi al catalogo dei contenuti, in modo che alcuni elementi possano essere visualizzati con maggiore probabilità.

Ad esempio, è possibile applicare una ponderazione più elevata agli articoli in vendita in modo che vengano visualizzati più spesso nei consigli. Gli articoli non in offerta non vengono esclusi del tutto, ma sono visualizzati con minore frequenza. È possibile applicare più attributi di ponderazione allo stesso algoritmo, e sottoporli a test con traffico suddiviso nel consiglio.

1. Scegli un valore.

   Il valore determina il tipo di elemento che è più probabile visualizzare, in base a uno dei diversi criteri disponibili.

1. Scegli un valutatore.

1. Inserisci la parola chiave per completare gli attributi della regola.

   Ad esempio, la regola completa potrebbe essere &quot;Category contains substring shoes&quot; (Categoria contiene le sottostringhe).

   ![](assets/Recs_AttributeWeighting.png)

1. Selezionare il peso da assegnare alla regola.

   Le opzioni variano da 0 a 100 con incrementi di 25.

1. Se desiderato, aggiungi ulteriori regole.

Al termine, fai clic su **[!UICONTROL Salva]**.

Se stai creando una nuova attività di [!UICONTROL Consigli] o ne stai modificando una esistente, per impostazione predefinita viene selezionata la casella di controllo **[!UICONTROL Salva criteri per un&#39;altra volta]**. Se non desideri utilizzare i criteri in altre attività, deseleziona la casella di controllo prima di salvarla.

## Training video: Create criteria in Recommendations (12:33) ![Tutorial badge](/help/assets/tutorial.png)

Questo video contiene le seguenti informazioni:

* Creare criteri
* Creare sequenze di criteri
* Caricare criteri personalizzati

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)
