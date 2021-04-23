---
keywords: criteri;algoritmo;settore verticale;tipo di pagina;chiave di consiglio;logica di consiglio;intervallo di dati;origine dati comportamento;progettazione parziale;consigli di backup;regole di inclusione;ponderazione attributi;categoria corrente;attributo personalizzato;ultimo articolo acquistato;ultimo articolo visualizzato;articolo più visualizzato;articolo più visualizzato;categoria preferita;popolarità;ultimo articolo visualizzato;ultimo articolo acquistato;ultimo visualizzato;più visualizzato;preferito;visualizzato di recente
description: Scopri come creare criteri che controllano il contenuto delle attività di Adobe Recommendations per mostrare i consigli più appropriati per la tua attività.
title: Come si creano i criteri in Recommendations?
feature: Consigli
exl-id: 3f4f59b2-6637-4c33-bf17-bff11bef7173
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '2486'
ht-degree: 63%

---

# ![PREMIUM](/help/assets/premium.png) Creare criteri

I criteri in [!UICONTROL Adobe Target] [!UICONTROL Recommendations] controllano il contenuto delle attività [!UICONTROL Recommendations]. Crea dei criteri per visualizzare i consigli più appropriati per l’attività. Questi criteri utilizzano le azioni del visitatore per determinare quale contenuto o prodotto visualizzare.

Nelle sezioni seguenti viene illustrato come creare un nuovo criterio.

## Accedere alla schermata Crea nuovo criterio

Esistono diversi modi per raggiungere la schermata [!UICONTROL Crea nuovo criterio]. Alcune opzioni dipendono dal modo in cui si raggiunge la schermata.

* Nella schermata della libreria **[!UICONTROL Recommendations]** > **[!UICONTROL Criteri]**, fai clic su **[!UICONTROL Crea criteri]** > **[!UICONTROL Crea criteri]**. I criteri creati vengono automaticamente resi disponibili per tutte le attività di [!DNL Recommendations].
* Quando crei un&#39;attività [!DNL Recommendations] utilizzando il [!UICONTROL Compositore esperienza visivo] (VEC), vieni immediatamente portato alla schermata [!UICONTROL Seleziona criteri] dopo aver selezionato un elemento nella pagina e dopo aver fatto clic su [!UICONTROL Sostituisci con Recommendations], [!UICONTROL Inserisci Recommendations prima], o [!UICONTROL Recommendations Inserisci]. Puoi quindi selezionare un criterio disponibile oppure fare clic su **[!UICONTROL Crea criterio]**. Se crei un nuovo criterio, puoi salvare i criteri da utilizzare per altre attività [!DNL Recommendations]. Per ulteriori informazioni, consulta [Creare un’attività Recommendations](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md).
* Quando modifichi un’attività di [!DNL Recommendations], fai clic su una casella di [!UICONTROL Posizione Consigli] nella pagina e seleziona **[!UICONTROL Cambia criteri]**. Nella schermata [!UICONTROL Seleziona criteri], fai clic su **[!UICONTROL Crea criteri]**. Sarà possibile salvare i nuovi criteri da utilizzare per altre attività di [!DNL Recommendations].

I passaggi seguenti presuppongono l&#39;accesso alla schermata [!UICONTROL Crea nuovo criterio] utilizzando il primo metodo: la schermata della libreria **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** .

1. Fai clic su **[!UICONTROL Recommendations]** > **[!UICONTROL Criteri]**.

1. Fai clic su **[!UICONTROL Crea criteri]** > **[!UICONTROL Crea criteri]**.

   ![Creare nuovi criteri](/help/c-recommendations/c-algorithms/assets/CreateNewCriteria_full-new.png)

1. Configura le informazioni nelle sezioni seguenti.

## Informazioni di base {#info}

1. Inserisci un **[!UICONTROL Nome criterio]**.

   Si tratta del nome “interno” usato per descrivere i criteri. Ad esempio, potresti voler chiamare i tuoi criteri “prodotti di margine più alto”, ma non vuoi che questo titolo venga visualizzato pubblicamente. Vedi il passo successivo per impostare il titolo visualizzato dal pubblico.

   ![Sezione Informazioni di base](/help/c-recommendations/c-algorithms/assets/basic-information.png)

1. Inserisci un **[!UICONTROL Titolo da visualizzare]**, che verrà mostrato nella pagina per i consigli che utilizzano questo criterio.

   Ad esempio, potresti voler visualizzare “Le persone che hanno visto questo, hanno visto anche” o “Prodotti simili”, quando utilizzi questo criterio per mostrare i consigli.

1. Inserisci una breve **[!UICONTROL descrizione]** dei criteri.

   La descrizione dovrebbe aiutarti a identificare i criteri e potrebbe includere informazioni sullo scopo dei criteri.

1. Seleziona un settore verticale in base agli obiettivi dell’attività di consigli.

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

   Per ulteriori informazioni sulle opzioni di logica per i consigli, consulta [Criteri](/help/c-recommendations/c-algorithms/algorithms.md).

   >[!NOTE]
   >
   >Se selezioni **[!UICONTROL Articoli]**/ **[!UICONTROL Media con attributi simili]**, avrai la possibilità di impostare [regole di somiglianza del contenuto](#similarity).

## Origine dati {#data-source}

1. Imposta l’**[!UICONTROL Intervallo di dati]** per determinare l’intervallo di tempo dei dati cronologici disponibili sul comportamento dell’utente da utilizzare per determinare quali consigli visualizzare.

   ![Cursore della gamma di dati](/help/c-recommendations/c-algorithms/assets/data-range.png)

   Se il sito genera molto traffico e i comportamenti si modificano spesso, scegli una finestra dati più breve. Una finestra più breve consente a [!DNL Recommendations] di essere più reattivo alle modifiche all’interno del mercato e della tua attività. Ad esempio, una finestra più breve implica che [!DNL Recommendations] rileverà le modifiche nel comportamento dei visitatori quando questi iniziano lo shopping stagionale, ad esempio quello natalizio o per il rientro a scuola, raccomandando gli articoli appropriati.

   In presenza di un volume limitato di dati, o se il comportamento dei visitatori non si modifica di frequente, puoi selezionare una finestra più ampia. Tuttavia, per molti siti, una finestra più breve determinerà i consigli migliori.

   Gli intervalli di dati disponibili sono:

   * Due giorni
   * Una settimana
   * Due settimane
   * Un mese
   * Due mesi

1. (Condizionale) Seleziona la **[!UICONTROL Origine dati comportamentali]** desiderata: [!UICONTROL mbox] o [!UICONTROL Analytics].

   >[!NOTE]
   >
   >La sezione [!UICONTROL Origine dati comportamentali] viene visualizzata solo se l&#39;implementazione utilizza [Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T).

   ![Sezione Origine dati comportamentali](/help/c-recommendations/c-algorithms/assets/behavioural-data-source.png)

   Se si sceglie [!UICONTROL Analytics], selezionare la suite di rapporti desiderata.

   Se i criteri utilizzano [!DNL Adobe Analytics] come origine dei dati comportamentali, una volta creati, il tempo per la disponibilità dei criteri dipende dal fatto che la suite di rapporti e l’intervallo di lookback selezionati siano stati utilizzati o meno per altri criteri, come illustrato di seguito:

   * **Configurazione una tantum della suite di rapporti**: la prima volta che una suite di rapporti viene utilizzata con una specifica finestra di lookback dei dati, [!DNL Target Recommendations] può richiedere da due a sette giorni per scaricare completamente i dati comportamentali della suite di rapporti selezionata da [!DNL Analytics]. Questo intervallo di tempo dipende dal carico del sistema [!DNL Analytics].
   * **Criteri nuovi o modificati che utilizzano una suite di rapporti già disponibile**: se crei un nuovo criterio o ne modifichi uno esistente e la suite di rapporti selezionata è già utilizzata per [!DNL Target Recommendations] con un intervallo di dati uguale o inferiore a quello selezionato, i dati diventano subito disponibili e non è richiesta alcuna configurazione una tantum. In questo caso, oppure se le impostazioni di un algoritmo vengono modificate senza che si modifichi la suite di rapporti o l’intervallo di dati selezionato, l’algoritmo viene eseguito o rieseguito entro 12 ore.
   * **Viene eseguito un algoritmo continuo**: i dati scorrono da [!DNL Analytics] a [!DNL Target Recommendations] su base giornaliera. Ad esempio, per un consiglio di tipo [!UICONTROL Affinità per articoli visualizzati], quando un utente visualizza un prodotto, a [!DNL Analytics] viene trasmessa una chiamata di tracciamento per visualizzazione prodotto quasi in tempo reale. I dati [!DNL Analytics] vengono inviati a [!DNL Target] all’inizio del giorno successivo e [!DNL Target] esegue l’algoritmo in meno di 12 ore.

   Per ulteriori informazioni, consulta [Utilizzare Adobe Analytics con Target Recommendations](/help/c-recommendations/c-algorithms/use-adobe-analytics-with-recommendations.md).

## Contenuto {#content}

Le regole di contenuto determinano cosa succede se il numero di elementi consigliati non corrisponde alla [progettazione di consigli](/help/c-recommendations/c-design-overview/design-overview.md). È possibile che i criteri [!DNL Recommendations] restituiscano un numero inferiore di consigli rispetto alle richieste di progettazione. Ad esempio, se la progettazione dispone di slot per quattro elementi, ma i criteri determinano solo due elementi da consigliare, puoi lasciare vuoti gli slot rimanenti o utilizzare i consigli di backup per riempirli.

![Sezione Contenuto](/help/c-recommendations/c-algorithms/assets/content.png)

1. (Facoltativo) Far scorrere l&#39;interruttore **[!UICONTROL Rendering progettazione parziale]** in posizione &quot;on&quot;.

   Il maggior numero possibile di slot verrà riempito, ma il modello di progettazione potrebbe includere spazio vuoto per gli slot rimanenti. Se questa opzione è disabilitata e il contenuto non è sufficiente per popolare tutti gli slot disponibili, i consigli non vengono serviti e viene invece visualizzato il contenuto predefinito.

   Abilita questa opzione se desideri che i consigli siano serviti con slot vuoti. Utilizza i consigli di backup se desideri che gli slot per consigli siano riempiti con contenuto in base ai criteri con slot vuoti riempiti con contenuti simili o popolari dal sito, come spiegato nel passaggio successivo.

1. (Facoltativo) Far scorrere l&#39;interruttore **[!UICONTROL Mostra Recommendations di backup]** in posizione &quot;on&quot;.

   Riempire gli slot vuoti rimanenti nel progetto con una selezione casuale dei prodotti più visualizzati da tutto il sito.

   L’utilizzo dei consigli di backup garantisce che la progettazione dei consigli riempia tutti gli slot disponibili. Supponiamo di avere un design 4 x 1, come illustrato di seguito:

   ![Design 4 x 1](/help/c-recommendations/c-design-overview/assets/velocity_example.png)

   Supponiamo che i criteri facciano sì che vengano consigliati solo due elementi. Se abiliti l&#39;opzione [!UICONTROL Rendering progettazione parziale], i primi due slot vengono riempiti, ma i due rimanenti rimangono vuoti. Tuttavia, se si abilita l&#39;opzione [!UICONTROL Mostra Recommendations di backup], i primi due slot vengono riempiti in base ai criteri specificati e i due slot rimanenti vengono riempiti in base ai consigli di backup.

   La seguente matrice mostra il risultato che osserverai quando utilizzi le opzioni [!UICONTROL Rendering progettazione parziale] e [!UICONTROL Recommendations di backup] :

   | Rendering parziale della progettazione | Consigli di backup | Risultato |
   |--- |--- |--- |
   | Disabilitato | Disabilitato | Se vengono restituiti meno consigli rispetto alle richieste di progettazione, la progettazione dei consigli viene sostituita dal contenuto predefinito e non vengono visualizzate indicazioni. |
   | Abilitato | Disabilitato | La progettazione viene sottoposta a rendering, ma può includere spazio vuoto se vengono restituite meno consigli rispetto al numero richiesto dalla progettazione. |
   | Abilitato | Abilitato | I consigli di backup riempiranno le “posizioni” disponibili della progettazione, eseguendone il rendering completo.<br>Se l&#39;applicazione di regole di inclusione ai consigli di backup limita il numero di quelle qualificate al punto che la progettazione non può essere riempita, la progettazione viene parzialmente sottoposta a rendering.<br>Se i criteri non restituiscono alcun consiglio e le regole di inclusione limitano i consigli di backup a zero, la progettazione viene sostituita con il contenuto predefinito. |
   | Disabilitato | Abilitato | I consigli di backup riempiranno le “posizioni” disponibili della progettazione, eseguendone il rendering completo.<br>Se l&#39;applicazione di regole di inclusione limita il numero di consigli di backup qualificate al punto che la progettazione non può essere riempita, la progettazione viene sostituita dal contenuto predefinito e non vengono visualizzati consigli. |

   Per ulteriori informazioni, consulta [Utilizzare un consiglio di backup](/help/c-recommendations/c-algorithms/backup-recs.md).

1. (Condizionale) Se hai selezionato **[!UICONTROL Mostra Recommendations di backup]** nel passaggio precedente, puoi abilitare **[!UICONTROL Applica regole di inclusione ai consigli di backup]**.

   Le regole di inclusione determinano quali elementi vengono inclusi nei consigli. Le opzioni disponibili dipendono dal tuo settore verticale.

   Per ulteriori dettagli consulta  [Specifica le ](#inclusion) regole di inclusione riportate di seguito.

1. (Facoltativo) Fai scorrere l&#39;interruttore **[!UICONTROL Consiglia articoli acquistati in precedenza]** nella posizione &quot;on&quot;.

   Questa impostazione è basata su `productPurchasedId`. Il comportamento predefinito è quello di sconsigliare gli articoli acquistati in precedenza. Nella maggior parte dei casi non si desidera promuovere articoli che un cliente ha recentemente acquistato. È utile se si vendono oggetti che le persone solitamente acquistano una sola volta, ad esempio nel caso di un kayak. Se vendi oggetti che le persone ritornano per acquistare di nuovo su base ripetuta, come shampoo o altri oggetti personali, devi abilitare questa opzione.

## Somiglianza del contenuto {#similarity}

Utilizza le regole di [!UICONTROL somiglianza del contenuto] per formulare consigli basati su attributi di elemento o file multimediale.

>[!NOTE]
>
>Se hai selezionato **[!UICONTROL Articoli]**/ **[!UICONTROL Media con attributi simili]** come [logica per i consigli](#info), avrai la possibilità di impostare regole per la similarità dei contenuti.

Le regole di somiglianza del contenuto confrontano le parole chiave dell&#39;attributo dell&#39;elemento e formulano consigli basati su quante parole chiave hanno in comune diversi elementi. I consigli basati sulla somiglianza del contenuto non richiedono dati precedenti per fornire risultati significativi.

Utilizzare la somiglianza di contenuto per generare consigli è particolarmente efficace per i nuovi elementi, i quali non possono essere mostrati nei consigli utilizzando il criterio *Le persone che hanno visto questo, hanno visto anche* e altre logiche basate sul comportamento precedente. È inoltre possibile utilizzare la somiglianza del contenuto per generare consigli utili per i nuovi visitatori, che non hanno effettuato acquisti in precedenza o non possiedono altri dati storici.

Quando si selezionano **[!UICONTROL elementi]**/**[!UICONTROL supporti con attributi simili]**, è possibile creare regole per aumentare o diminuire l&#39;importanza degli attributi di elementi specifici nella determinazione dei consigli. Per gli articoli quali i libri, si potrebbe voler aumentare l&#39;importanza di attributi come *genere*, *autore*, *serie*, e così via, per consigliare libri simili.

![](assets/ContentSimilarity.png)

Poiché la somiglianza del contenuto utilizza parole chiave per confrontare elementi, alcuni attributi, ad esempio *messaggio* o *descrizione*, possono introdurre “rumore” nel confronto. È possibile creare regole per ignorare questi attributi.

Per impostazione predefinita, tutti gli attributi sono impostati su *Riferimento*. Non è necessario creare una regola a meno che non si desideri modificare questa impostazione.

>[!NOTE]
>
>L’algoritmo di somiglianza del contenuto può utilizzare il campionamento casuale nel calcolo della somiglianza tra gli elementi. Di conseguenza, le valutazioni di similarità tra gli elementi potrebbero variare tra le esecuzioni degli algoritmi.

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

Per ulteriori informazioni, consulta [Utilizzare regole di inclusione dinamiche e statiche](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md).

## Ponderazione degli attributi  {#weighting}

Puoi aggiungere più regole per &quot;spostare&quot; l’algoritmo in base a informazioni importanti o metadati sul catalogo dei contenuti, in modo che alcuni elementi abbiano più probabilità di essere visualizzati.

Ad esempio, è possibile applicare una ponderazione più elevata agli articoli in vendita in modo che vengano visualizzati più spesso nei consigli. Gli articoli non in offerta non vengono esclusi del tutto, ma sono visualizzati con minore frequenza. È possibile applicare più attributi di ponderazione allo stesso algoritmo, e sottoporli a test con traffico suddiviso nel consiglio.

1. Scegli un valore.

   Il valore determina il tipo di elemento che è più probabile visualizzare, in base a uno dei diversi criteri disponibili.

1. Scegli un valutatore.

1. Inserisci la parola chiave per completare gli attributi della regola.

   Ad esempio, la regola completa potrebbe essere &quot;Categoria contiene scarpe sottostringhe&quot;.

   ![](assets/Recs_AttributeWeighting.png)

1. Selezionare il peso da assegnare alla regola.

   Le opzioni variano da 0 a 100 con incrementi di 25.

1. Se desiderato, aggiungi ulteriori regole.

Al termine, fai clic su **[!UICONTROL Salva]**.

Se stai creando una nuova attività di [!UICONTROL Consigli] o ne stai modificando una esistente, per impostazione predefinita viene selezionata la casella di controllo **[!UICONTROL Salva criteri per un&#39;altra volta]**. Se non desideri utilizzare i criteri in altre attività, deseleziona la casella di controllo prima di salvarla.

## Video di formazione: Creare criteri in Recommendations (12:33) ![Badge tutorial](/help/assets/tutorial.png)

Questo video contiene le seguenti informazioni:

* Creare criteri
* Creare sequenze di criteri
* Caricare criteri personalizzati

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)
