---
keywords: criteri;algoritmo;settore verticale;tipo di pagina;chiave consiglio;logica consiglio;logica consiglio;intervallo dati;intervallo di lookback;comportamento origine dati;progettazione parziale;backup consigli;regole di inclusione;ponderazione attributi;categoria corrente;attributo personalizzato;ultimo articolo acquistato;ultimo articolo visualizzato;ultimo articolo visualizzato;articolo più visualizzato;categoria preferita;popolarità;articolo visualizzato di recente;ultimo articolo acquistato;più visualizzato;preferito;visualizzato di recente
description: Scopri come creare criteri che controllano il contenuto delle attività di [!DNL Recommendations] per mostrare i consigli più appropriati per l'attività.
title: Come si creano [!UICONTROL criteri] in [!DNL Recommendations]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: 3f4f59b2-6637-4c33-bf17-bff11bef7173
TQID: 'https://experienceleague.adobe.com/r9FWgHWw6NX1CmhqI-7MLoamNFDepeCq1bpiJ8eyISM'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c4147b6e-073b-4d3c-9ab1-d60f2f4434ef
    internal-label: Behavioral data
source-git-commit: e8a9b6be04169ea3024673babb62085667fe8990
workflow-type: tm+mt
source-wordcount: '2840'
ht-degree: 17%
---
# Creare criteri {#create-criteria}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come creare criteri in [!DNL Adobe Target Recommendations] e come configurare ogni sezione di un criterio.

>[!ENDSHADEBOX]

I criteri in [!DNL Adobe Target] [!DNL Recommendations] controllano il contenuto di [!DNL Recommendations] attività. I criteri utilizzano le azioni del visitatore per determinare quale contenuto o prodotti visualizzare, in modo che i criteri appropriati mostrino i consigli più appropriati per l’attività.

## Accedere alla schermata Crea nuovo criterio {#access-create-criteria}

Esistono diversi modi per raggiungere la schermata **[!UICONTROL Crea nuovo criterio]**. Alcune opzioni di schermo variano a seconda di come viene raggiunta la schermata.

* Nella schermata della libreria **[!UICONTROL Recommendations]** > **[!UICONTROL Criteri]**, fai clic su **[!UICONTROL Crea criterio]** > **[!UICONTROL Crea criterio]**. I criteri creati vengono automaticamente resi disponibili per tutte le attività [!DNL Recommendations].

  ![Pagina Criteri con il menu Crea criteri aperto, che mostra Crea criteri e Crea sequenza criteri](../assets/criteria_create_1.png)

* Durante la creazione di un&#39;attività [!DNL Recommendations] tramite il **[!UICONTROL Compositore esperienza visivo]** (VEC), la schermata **[!UICONTROL Seleziona criteri]** viene visualizzata subito dopo la selezione di un elemento nella pagina e la schermata **[!UICONTROL Sostituisci con consigli]**, **[!UICONTROL Inserisci consigli prima]** o **[!UICONTROL Inserisci consigli dopo]** è stata selezionata. Selezionare un criterio disponibile o fare clic su **[!UICONTROL Crea criterio]**. È possibile salvare un nuovo criterio per utilizzarlo con altre attività di [!DNL Recommendations]. Per ulteriori informazioni, vedere [Creare un&#39;attività Consigli](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md).

  ![Schermata Seleziona criteri di un&#39;attività Consigli con il pulsante Crea criteri](../assets/criteria_create_2.png)

* Durante la modifica di un&#39;attività [!DNL Recommendations], fare clic in una casella **[!UICONTROL Posizione consigli]** nella pagina e selezionare **[!UICONTROL Cambia criteri]**. Nella schermata **[!UICONTROL Seleziona criteri]**, fai clic su **[!UICONTROL Crea criteri]**. I nuovi criteri possono essere salvati per l&#39;utilizzo con altre attività di [!DNL Recommendations].

## [!UICONTROL Informazioni di base] {#info}

Le informazioni di base identificano i criteri e li classificano per il riutilizzo in altre attività.

1. Digita un **[!UICONTROL Nome criterio]**.

   Questo è il nome interno utilizzato per descrivere i criteri. Ad esempio, è possibile denominare un criterio &quot;Prodotti con margine più alto&quot; senza che il titolo venga visualizzato pubblicamente. Il titolo rivolto al pubblico viene impostato nel passaggio successivo.

1. Digitare un **[!UICONTROL Titolo visualizzato]** rivolto al pubblico da visualizzare nella pagina per i consigli che utilizzano questo criterio.

   Ad esempio, &quot;Le persone che hanno visualizzato questo hanno visualizzato&quot; o &quot;Prodotti simili&quot; possono essere visualizzati quando questo criterio viene utilizzato per mostrare i consigli.

1. Digitare una breve **[!UICONTROL Descrizione]** dei criteri.

   La descrizione dovrebbe aiutare a identificare i criteri e potrebbe includere informazioni sul suo scopo.

1. Seleziona un settore verticale in base agli obiettivi dell’attività Consigli.

   | Settore verticale | Obiettivo |
   |--- |--- |
   | **[!UICONTROL Vendita al dettaglio/e-commerce]** | Conversione con conseguente acquisto |
   | **[!UICONTROL Generazione lead/B2B/Servizi finanziari]** | Conversione senza acquisto |
   | **[!UICONTROL File multimediali/Pubblicazione]** | Coinvolgimento |

   Altre opzioni di criteri cambiano in base al settore verticale selezionato.

   ![Sezione Informazioni di base della finestra di dialogo Crea criterio con l&#39;elenco Settore/Verticale aperto e le tre opzioni evidenziate](../assets/criteria_create_3.png)

1. Seleziona un **[!UICONTROL tipo di pagina]**.

   È possibile selezionare più tipi di pagina. Insieme, il settore verticale e i tipi di pagina consentono di categorizzare i criteri salvati, semplificandone il riutilizzo per altre attività di [!DNL Recommendations].

## [!UICONTROL Algoritmo consigli] {#rec-algo}

L’algoritmo determina la modalità di selezione degli elementi per i consigli.

>[!CONTEXTUALHELP]
>id="target_recommendations_profile_attribute"
>title="Attributo di profilo"
>abstract="Puoi creare un attributo del profilo utilizzando gli script di profilo."

1. Seleziona un **[!UICONTROL Tipo di algoritmo]** e **[!UICONTROL Algoritmo]**:

   ![Sezione algoritmo consigliata](assets/recommended-algorithm.png)

   | Tipo di algoritmo | Quando utilizzare / Algoritmi disponibili |
   | --- | --- |
   | **[!UICONTROL Basato su carrello]** | Creare consigli in base al contenuto del carrello dell’utente. <ul><li>**[!UICONTROL Persone Che Hanno Visualizzato Questi, Hanno Visualizzato Anche]** </li><li>**[!UICONTROL Chi ha visualizzato questi elementi ha acquistato anche]**</li><li>**[!UICONTROL Chi ha acquistato questi, ha acquistato anche]**</li></ul> |
   | **[!UICONTROL Basato Sulla Popolarità]** | Puoi formulare raccomandazioni in base alla popolarità complessiva di un elemento nel sito o alla popolarità degli elementi nella categoria, nel brand, nel genere e così via preferiti o più visualizzati dall’utente. <ul><li>**[!UICONTROL Più visualizzati nel sito]**</li><li>**[!UICONTROL Più visualizzati per categoria]**</li><li>**[!UICONTROL Più visualizzati per attributo elemento]**</li><li>**[!UICONTROL Più visualizzati per attributo profilo]**</li><li>**[!UICONTROL Più venduti nel sito]**</li><li>**[!UICONTROL Più venduti per categoria]**</li><li>**[!UICONTROL Più venduti per attributo articolo]**</li><li>**[!UICONTROL Più venduti per attributo profilo]**</li><li>**[!UICONTROL Primi per metrica di Analytics]**</li></ul> |
   | **[!UICONTROL Basato su elemento]** | Creare consigli in base a elementi simili a un elemento attualmente visualizzato o visualizzato di recente dall’utente. <ul><li>**[!UICONTROL Chi ha visualizzato questo ha visualizzato anche quello]**</li><li>**[!UICONTROL Chi ha visualizzato questo ha acquistato anche quello]**</li><li>**[!UICONTROL Chi ha acquistato questo ha acquistato anche quello]**</li><li>**[!UICONTROL Elementi con attributi simili]**</li></ul> |
   | **[!UICONTROL Basato su utente]** | Creare consigli in base al comportamento dell’utente.<ul><li>**[!UICONTROL Elementi visualizzati di recente]**</li><li>**[!UICONTROL Consigliato per te]**</li></ul> |
   | **[!UICONTROL Criteri personalizzati]** | Formulare raccomandazioni in base a un file personalizzato caricato.<ul><li>Algoritmo personalizzato</li></ul> |

   >[!NOTE]
   >
   >Se è selezionata l&#39;opzione **[!UICONTROL Elementi]**/**[!UICONTROL Elementi multimediali con attributi simili]**, è possibile impostare [regole di somiglianza dei contenuti](#similarity).

1. Configura l&#39;algoritmo come richiesto selezionando una **[!UICONTROL Chiave consiglio]**, **[!UICONTROL Chiave filtro]**, **[!UICONTROL Base co-occorrenza]**, **[!UICONTROL Metrica analisi]** e/o **[!UICONTROL Attributo elemento]** e **[!UICONTROL Attributo profilo da abbinare]**. Le opzioni di configurazione disponibili variano a seconda dell’algoritmo selezionato.

   Per ulteriori informazioni sulla scelta di una **[!UICONTROL Chiave consiglio]**, vedere [Basare il consiglio su una chiave consiglio](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md).

1. (Condizionale) Per **[!UICONTROL Più visualizzati per attributo profilo]** o **[!UICONTROL Più venduti per attributo profilo]**, seleziona un **[!UICONTROL attributo profilo]** per raggruppare i dati di interazione in base a.

   Gli attributi del profilo provengono da uno script di profilo che acquisisce una caratteristica del visitatore, ad esempio regione o paese. Il nome dello script deve contenere il prefisso `recsAttribute`, quindi viene memorizzato come `user.recsAttribute<Name>`, ad esempio `user.recsAttributeRegion`. Al momento della consegna, [!DNL Target] fornisce a ogni visitatore l&#39;elenco classificato che corrisponde al proprio valore di tale attributo.

## [!UICONTROL Contenuto backup] {#content}

**[!UICONTROL Le regole di backup del contenuto]** determinano ciò che accade se il numero di elementi consigliati non riempie la [progettazione dei consigli](/help/main/c-recommendations/c-design-overview/design-overview.md). I criteri possono restituire un numero inferiore di consigli rispetto alle richieste di progettazione. Ad esempio, se la progettazione dispone di slot per quattro elementi ma i criteri determinano solo due elementi da consigliare, gli slot rimanenti possono essere lasciati vuoti o riempiti con consigli di backup, oppure non è possibile visualizzare alcun consiglio.

1. (Facoltativo) Abilita l&#39;opzione **[!UICONTROL Rendering design parziale]**.

   Vengono riempiti il maggior numero possibile di slot, ma il modello di progettazione potrebbe includere uno spazio vuoto per gli slot rimanenti. Se questa opzione è disabilitata e il contenuto non è sufficiente per riempire tutti gli slot disponibili, i consigli non vengono trasmessi e viene visualizzato il contenuto predefinito.

   Abilita questa opzione per distribuire i consigli con slot vuoti. Per riempire gli slot vuoti con contenuti simili o popolari dal sito, utilizza i consigli di backup, come spiegato nel passaggio successivo.

1. (Facoltativo) Abilita l&#39;opzione **[!UICONTROL Mostra contenuto di backup]**.

   I consigli di backup riempiono gli eventuali slot vuoti rimanenti nella progettazione con una selezione casuale dei prodotti più visualizzati dall’intero sito, in modo che la progettazione riempia sempre tutti gli slot disponibili. L&#39;esempio seguente utilizza un design 4 x 1:

   ![4 x 1 design](../assets/velocity_example.png)

   Se in base ai criteri vengono consigliati solo due elementi e l&#39;opzione **[!UICONTROL Rendering design parziale]** è abilitata, i primi due slot vengono riempiti e i due slot rimanenti rimangono vuoti. Se l&#39;opzione **[!UICONTROL Mostra contenuto di backup]** è abilitata, i primi due slot vengono riempiti in base ai criteri specificati e i due slot rimanenti vengono riempiti in base ai consigli di backup.

   +++ La matrice seguente mostra il risultato per ogni combinazione delle opzioni **[!UICONTROL Rendering design parziale]** e **[!UICONTROL Contenuto backup]**

   | Rendering parziale della progettazione | Contenuto di backup | Risultato |
   |--- |--- |--- |
   | Disabilitato | Disabilitato | Se vengono restituiti meno consigli rispetto alle richieste di progettazione, la progettazione dei consigli viene sostituita dal contenuto predefinito e non vengono visualizzate indicazioni. |
   | Abilitato | Disabilitato | Viene eseguito il rendering della progettazione, ma potrebbe includere uno spazio vuoto se vengono restituiti meno consigli di quanto richiesto dalla progettazione. |
   | Abilitato | Abilitato | I consigli di backup riempiono gli &quot;slot&quot; di progettazione disponibili, riproducendo completamente la progettazione.<br>Se l&#39;applicazione di regole di inclusione ai consigli di backup limita il numero di quelle qualificate al punto che la progettazione non può essere riempita, la progettazione viene parzialmente sottoposta a rendering.<br>Se i criteri non restituiscono alcun consiglio e le regole di inclusione limitano i consigli di backup a zero, la progettazione viene sostituita con il contenuto predefinito. |
   | Disabilitato | Abilitato | I consigli di backup riempiono gli &quot;slot&quot; di progettazione disponibili, riproducendo completamente la progettazione.<br>Se l&#39;applicazione di regole di inclusione limita il numero di consigli di backup qualificate al punto che la progettazione non può essere riempita, la progettazione viene sostituita dal contenuto predefinito e non vengono visualizzati consigli. |

   Per ulteriori informazioni, vedere [Utilizzare un consiglio di backup](/help/main/c-recommendations/c-algorithms/backup-recs.md).
   +++

1. (Condizionale) Se **[!UICONTROL Mostra contenuto di backup]** è abilitato, è possibile abilitare anche **[!UICONTROL Applica regole di inclusione ai consigli di backup]**.

   Le regole di inclusione determinano quali elementi vengono inclusi nei consigli. Le opzioni disponibili dipendono dal settore verticale.

   Per ulteriori dettagli, vedere [Specificare le regole di inclusione](#inclusion) di seguito.

## [!UICONTROL Source dati] {#data-source}

L’origine dati determina i dati comportamentali utilizzati dal criterio e l’intervallo di tempo di tali dati.

1. Seleziona il **[!UICONTROL Source dei dati comportamentali]** desiderato: **[!UICONTROL Adobe Target]** o **[!UICONTROL Analytics]**.

   >[!NOTE]
   >
   >La sezione **[!UICONTROL Behavioral Data Source]** viene visualizzata solo se l&#39;implementazione utilizza [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T).

   ![Sezione Data Source con le opzioni del Source di dati comportamentali Adobe Target e Analytics evidenziate](../assets/criteria_create_4.png)

   Per **[!UICONTROL Analytics]**, seleziona la suite di rapporti desiderata.

   +++ Disponibilità dei criteri quando Analytics è l’origine dati

   Quando [!DNL Adobe Analytics] è l&#39;origine dei dati comportamentali, il tempo fino a quando non è disponibile un nuovo criterio dipende dal fatto che la suite di rapporti e l&#39;intervallo di lookback selezionati siano stati utilizzati o meno per altri criteri:

   * **Configurazione una tantum della suite di rapporti**: la prima volta che una suite di rapporti viene utilizzata con una specifica finestra di lookback dei dati, [!DNL Target Recommendations] può richiedere da due a sette giorni per scaricare completamente i dati comportamentali della suite di rapporti selezionata da [!DNL Analytics]. Questo intervallo di tempo dipende dal caricamento del sistema [!DNL Analytics].
   * **Criteri nuovi o modificati che utilizzano una suite di rapporti già disponibile**: se crei un nuovo criterio o ne modifichi uno esistente e la suite di rapporti selezionata è già utilizzata per [!DNL Target Recommendations], con un intervallo di dati uguale o maggiore di quello selezionato, i dati diventano immediatamente disponibili e non è richiesta alcuna configurazione una tantum. In questo caso, oppure se le impostazioni di un algoritmo vengono modificate senza che si modifichi la suite di rapporti o l’intervallo di dati selezionato, l’algoritmo viene eseguito o rieseguito entro 12 ore.
   * **Viene eseguito un algoritmo continuo**: i dati scorrono da [!DNL Analytics] a [!DNL Target Recommendations] su base giornaliera. Ad esempio, per il consiglio **[!UICONTROL Affinità visualizzata]**, quando un utente visualizza un prodotto, a [!DNL Analytics] viene passata una chiamata di tracciamento per la visualizzazione del prodotto quasi in tempo reale. I dati [!DNL Analytics] vengono inviati a [!DNL Target] all’inizio del giorno successivo e [!DNL Target] esegue l’algoritmo in meno di 12 ore.

   Per ulteriori informazioni, vedere [Utilizzare Adobe Analytics con Target Recommendations](/help/main/c-recommendations/c-algorithms/use-adobe-analytics-with-recommendations.md).

   +++



1. Imposta **[!UICONTROL Intervallo di lookback]** per determinare l&#39;intervallo di tempo dei dati cronologici disponibili sul comportamento dell&#39;utente da utilizzare per determinare quali consigli visualizzare. Questa opzione è disponibile per tutti gli algoritmi ad eccezione di **[!UICONTROL Elementi con attributi simili]** e **[!UICONTROL Algoritmi personalizzati]**.

   Per un sito con molto traffico in cui i comportamenti cambiano frequentemente, scegli una finestra di dati più breve. Una finestra più breve rende [!DNL Recommendations] più reattivo ai cambiamenti nel mercato e nel business. Ad esempio, [!DNL Recommendations] rileva le modifiche nel comportamento dei visitatori quando questi iniziano lo shopping stagionale, ad esempio quello natalizio o per il rientro a scuola, e consiglia gli articoli appropriati per tali periodi di shopping.

   Se il sito non contiene molti dati o se il comportamento del visitatore non cambia frequentemente, seleziona una finestra più lunga. Tuttavia, per molti siti, una finestra più breve genera consigli di qualità superiore.

   +++ Intervalli di dati disponibili

   | Opzione finestra di lookback | Frequenza aggiornata (visualizzata al passaggio del mouse) | Algoritmi supportati |
   | --- | --- | --- |
   | Sei ore | L’algoritmo viene eseguito ogni 3-6 ore | **[!UICONTROL Algoritmi basati sulla popolarità]** quando il **[!UICONTROL Source dei dati comportamentali]** selezionato è [!DNL Adobe Target] |
   | Un giorno | L’algoritmo viene eseguito ogni 12-24 ore | **[!UICONTROL Algoritmi basati sulla popolarità]** |
   | Due giorni | L’algoritmo viene eseguito ogni 12-24 ore | <ul><li>**[!UICONTROL Algoritmi basati sulla popolarità]**</li><li>**[!UICONTROL Algoritmi basati su elementi]**</li><li>**[!UICONTROL Algoritmi basati sull&#39;utente]**</li><li>**[!UICONTROL Algoritmi basati su carrello]**</li></ul> |
   | Una settimana | L’algoritmo viene eseguito ogni 24-48 ore | <ul><li>**[!UICONTROL Algoritmi basati sulla popolarità]**</li><li>**[!UICONTROL Algoritmi basati su elementi]**</li><li>**[!UICONTROL Algoritmi basati sull&#39;utente]**</li><li>**[!UICONTROL Algoritmi basati su carrello]**</li></ul> |
   | Due settimane | L’algoritmo viene eseguito ogni 24-48 ore | <ul><li>**[!UICONTROL Algoritmi basati sulla popolarità]**</li><li>**[!UICONTROL Algoritmi basati su elementi]**</li><li>Tutti gli algoritmi **[!UICONTROL basati su utente]**</li><li>**[!UICONTROL Algoritmi basati su carrello]**</li></ul> |
   | Un mese (30 giorni) | L’algoritmo viene eseguito ogni 24-48 ore | <ul><li>**[!UICONTROL Algoritmi basati sulla popolarità]**</li><li>**[!UICONTROL Algoritmi basati su elementi]**</li><li>**[!UICONTROL Algoritmi basati sull&#39;utente]**</li><li>**[!UICONTROL Algoritmi basati su carrello]**</li></ul> |
   | Due mesi (61 giorni) | L’algoritmo viene eseguito ogni 24-48 ore | <ul><li>**[!UICONTROL Algoritmi basati sulla popolarità]**</li><li>**[!UICONTROL Algoritmi basati su elementi]**</li><li>**[!UICONTROL Algoritmi basati sull&#39;utente]**</li><li>**[!UICONTROL Algoritmi basati su carrello]**</li></ul> |

   +++

## Somiglianza del contenuto {#similarity}

Utilizza le regole di **[!UICONTROL somiglianza del contenuto]** per formulare consigli basati su attributi di elemento o file multimediale.

![Sezione Somiglianza del contenuto con una regola entity.name ed evidenziati i pulsanti Aggiungi regola e Cancella regole](../assets/criteria_create_5.png)

Le regole di somiglianza del contenuto confrontano le parole chiave dell&#39;attributo dell&#39;elemento e formulano consigli basati su quante parole chiave hanno in comune diversi elementi. I consigli basati sulla somiglianza dei contenuti non richiedono dati passati.

La somiglianza dei contenuti è efficace per i nuovi elementi, che probabilmente non saranno visualizzati nei consigli utilizzando *Persone che hanno visualizzato questo/a, hanno visualizzato anche* e altra logica basata sul comportamento passato. Può anche generare consigli per i nuovi visitatori, che non hanno acquisti precedenti o altri dati storici.

Quando è selezionata l&#39;opzione **[!UICONTROL Basata su elemento]**/ **[!UICONTROL Elemento con attributi simili]**, è possibile creare regole per aumentare o diminuire l&#39;importanza degli attributi di elementi specifici nella determinazione dei consigli. Per elementi come libri, l&#39;importanza di attributi come *genre*, *author*, *series* e così via può essere aumentata per consigliare libri simili.

Poiché la somiglianza dei contenuti utilizza parole chiave per confrontare gli elementi, alcuni attributi, ad esempio *message* o *description*, possono introdurre elementi non significativi nel confronto. È possibile creare regole per ignorare questi attributi.

Per impostazione predefinita, tutti gli attributi sono impostati su *Riferimento*. Una regola è necessaria solo per modificare questa impostazione.

>[!NOTE]
>
>L’algoritmo di somiglianza dei contenuti potrebbe utilizzare il campionamento casuale nel calcolo della somiglianza tra gli elementi. Di conseguenza, le valutazioni della similarità tra gli elementi potrebbero variare tra le esecuzioni dell’algoritmo.

## Regole di inclusione {#inclusion}

Le regole di inclusione limitano gli elementi visualizzati nei consigli. Possono essere utilizzati durante la creazione di criteri o promozioni. Le regole di inclusione sono facoltative; tuttavia, l’impostazione di questi dettagli offre un maggiore controllo sugli elementi visualizzati nei consigli. Ogni dettaglio configurato limita ulteriormente i criteri di visualizzazione.

Ad esempio, è possibile visualizzare solo le scarpe da donna con un inventario superiore a 50 e un prezzo compreso tra 25 e 45 dollari. Ciascun attributo può anche essere ponderato in modo che le voci più importanti per l&#39;azienda abbiano la maggiore probabilità di apparire. Un altro esempio: le opportunità di lavoro possono essere mostrate solo ai visitatori che visitano il sito da determinate città e che dispongono dei gradi universitari richiesti.

Le opzioni di regola di inclusione variano secondo il settore verticale. Per impostazione predefinita, le regole di inclusione vengono applicate ai consigli di backup. Le regole di inclusione sono unite con un AND, pertanto è necessario che tutte le regole siano soddisfatte per includere un elemento in un consiglio.

>[!IMPORTANT]
>
>Utilizza le regole di inclusione con cautela. Sono utili se, ad esempio, l’organizzazione dispone di regole che richiedono che un marchio non sia consigliato durante la visualizzazione di un altro marchio. Tuttavia, questa funzione ha un costo di opportunità: limitare gli articoli che i criteri di attività mostrerebbero normalmente potrebbe perdere una percentuale di incremento.

I passaggi seguenti creano una semplice regola di inclusione che visualizza solo le scarpe da donna con un inventario superiore a 50 e un prezzo compreso tra 25 e 45 dollari:

1. (Condizionale) Abilita **[!UICONTROL Consenti agli articoli acquistati di recente di essere consigliati]**.

   Questa impostazione è basata su `productPurchasedId`. Il comportamento predefinito è quello di sconsigliare gli articoli acquistati in precedenza. Nella maggior parte dei casi, gli articoli acquistati di recente da un cliente non devono essere promossi. L’impostazione è utile per gli elementi che in genere vengono acquistati una sola volta, ad esempio i kayak. Abilita questa opzione per gli articoli che le persone acquistano ripetutamente, ad esempio shampoo o altri articoli personali.

1. Imposta una fascia di prezzo per i prodotti da consigliare.

1. Imposta la quantità minima di scorte per i prodotti da consigliare.

1. Configura il consiglio perché mostri gli articoli solo quando sono soddisfatti determinati criteri.

   È possibile includere gli elementi solo se uno degli attributi dell&#39;elenco soddisfa o non soddisfa una o più condizioni specificate.

   I valutatori disponibili dipendono dal valore scelto nel primo elenco a discesa. È possibile elencare più elementi che vengono valutati con l’operatore OR. Più regole sono collegate tra loro mediante l&#39;operatore “AND” (E).

   >[!NOTE]
   >
   >Questa opzione limita gli elementi visualizzati nel consiglio. Non interessa le pagine in cui viene visualizzato il consiglio. Per limitare le posizioni di visualizzazione per il consiglio, seleziona le pagine in Compositore esperienza.

Per ulteriori informazioni, vedere [Utilizzare regole di inclusione dinamiche e statiche](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md).

## Ponderazione degli attributi {#weighting}

È possibile aggiungere più regole per &quot;indirizzare&quot; l’algoritmo in base a informazioni o metadati importanti sul catalogo dei contenuti, in modo che sia più probabile visualizzare alcuni elementi.

Ad esempio, è possibile applicare una ponderazione più elevata agli articoli in offerta, in modo che vengano visualizzati più spesso nei consigli. Gli articoli non in offerta non vengono esclusi del tutto, ma sono visualizzati con minore frequenza. È possibile applicare più attributi di ponderazione allo stesso algoritmo, e sottoporli a test con traffico suddiviso nel consiglio.

1. Scegli un valore.

   Il valore determina il tipo di elemento che è più probabile visualizzare, in base a uno dei diversi criteri disponibili.

1. Scegli un valutatore.

1. Inserisci la parola chiave per completare gli attributi della regola.

   Ad esempio, la regola completa potrebbe essere &quot;La categoria contiene scarpe di sottostringa&quot;.

1. Selezionare il peso da assegnare alla regola.

   Le opzioni variano da 0 a 100 con incrementi di 25.

1. Se desiderato, aggiungi ulteriori regole.

Al termine, fare clic su **[!UICONTROL Crea]**.

Quando viene creata una nuova attività di **[!UICONTROL Consigli]** o ne viene modificata una esistente, la casella di controllo **[!UICONTROL Salva criteri per dopo]** è selezionata per impostazione predefinita. Per impedire l’utilizzo dei criteri in altre attività, deseleziona la casella di controllo prima di salvare.
