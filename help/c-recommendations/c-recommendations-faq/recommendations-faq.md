---
keywords: risoluzione dei problemi;domande frequenti;FAQ;consigli;caratteri speciali;ponderazione degli attributi;somiglianza contenuti
description: Visualizza un elenco delle domande frequenti e delle risposte relative alle attività di Adobe Target Recommendations.
title: Dove posso trovare domande e risposte sui consigli di Target?
feature: Consigli
translation-type: tm+mt
source-git-commit: e4d7f9d6bd42343c5c5e591853a4fc70d1f49ee7
workflow-type: tm+mt
source-wordcount: '2031'
ht-degree: 57%

---


# ![PREMIUM](/help/assets/premium.png) Domande frequenti relative ai consigli

Elenco delle domande frequenti sulle attività di [!DNL Adobe Target] [!DNL Recommendations] .

## Perché la Ricerca nel catalogo non mostra i risultati corretti quando eseguo una ricerca su un attributo personalizzato con un valore numerico?

Quando esegui una ricerca di catalogo su un attributo personalizzato con un valore numerico, l’attributo personalizzato viene considerato come di tipo String anziché come valore numerico.

Attualmente, non è disponibile alcuna funzionalità che consenta ai clienti di modificare il tipo di un attributo. Per apportare una modifica, [apri un problema del cliente](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) facendo riferimento agli attributi che richiedono la modifica del tipo da stringa a numerico.

## Quanto tempo ci vuole perché gli aggiornamenti agli articoli del catalogo si riflettano sul mio sito?

Dopo aver importato un file di feed, o ricevuto aggiornamenti di entità tramite API o mbox, le seguenti modifiche verranno riportate in meno di 60 minuti:

* Attributi degli articoli restituiti nel modello Progettazione.
* Attributi degli articoli utilizzati nelle regole di esclusione globali che impediscono l’inclusione dell’articolo nei consigli restituiti.
* Attributi degli articoli utilizzati nelle regole di inclusione dei criteri che incidono sull’inclusione o esclusione dell’articolo dai consigli restituiti.

Le modifiche seguenti vengono applicate solo dopo l’esecuzione dell’algoritmo successivo (entro 12-24 ore):

* Attributi degli articoli utilizzati nelle regole di raccolta utilizzate per l’attività.
* Attributi degli articoli utilizzati in una promozione in base a una raccolta o un attributo associato all’attività.
* Categoria di articoli in cui l’articolo viene visualizzato, per “Categoria corrente” o “Categoria preferita” nell’algoritmo “Articoli più venduti” o “Articoli più visualizzati”.
* Classificazione degli articoli consigliati quando l’attributo modificato è un attributo personalizzato utilizzato come chiave personalizzata per un algoritmo.
* Classificazione degli elementi consigliati in base a uno o più attributi modificati quando la logica dei consigli è &quot;Articoli con attributi simili&quot;, quando vengono utilizzati i fattori di ponderazione &quot;Somiglianza del contenuto&quot; o quando vengono utilizzati i fattori &quot;Ponderazione degli attributi&quot;.

>[!NOTE]
>
>Un file di feed viene considerato importato quando il suo stato cambia da “Importazione elementi” a “Preparazione aggiornamenti indice di ricerca”. Gli aggiornamenti possono richiedere più di 60 minuti per riflettersi nell’interfaccia utente di Ricerca nel catalogo; La funzione Ricerca nel catalogo è aggiornata quando lo stato del feed diventa &quot;Aggiornamenti completati&quot;. Anche se la ricerca nel catalogo non è ancora aggiornata, il sito riflette gli aggiornamenti sui tempi elencati sopra. Nella pagina Ricerca nel catalogo viene indicata l’ora dell’ultimo aggiornamento dell’indice di Ricerca nel catalogo.

## Cosa devo fare se l’array è interrotto dalla presenza di caratteri speciali? {#section_D27214116EE443638A60887C7D1C534E}

Utilizza i valori di escape in JavaScript. Le virgolette (&quot;) possono interrompere l’array. Lo snippet di codice seguente è un esempio di valori di escape:

```
#set($String='') 
#set($escaper=$String.class.forName('org.apache.commons.lang.StringEscapeUtils')) 
<script type="text/javascript"> 
console.log("$escaper.escapeJavaScript($entity1.name)") 
console.log("$escaper.escapeJavaScript($entity2.name)") 
console.log('$escaper.escapeJavaScript($entity3.name)') 
names.push("$escaper.escapeJavaScript($entity4.name)") 
</script>
```

## Perché non tutti i criteri, inclusi i criteri personalizzati, sono disponibili per la selezione durante la creazione di un’attività Consigli? {#section_B2265AC8B8A94E0298D495A05C5D817F}

I criteri disponibili si basano sulla categoria corrente. Quando crei offerte di consigli, il selettore degli algoritmi visualizza i criteri in base all’ID della categoria.

Se la posizione in cui stai applicando questo criterio non contiene l’ID di categoria, sono disponibili solo alcuni criteri nella selezione algoritmi.

Se utilizzi una posizione in cui l’ID categoria è presente nella mbox, il selettore dei criteri contiene tutti i criteri applicabili.

L’impostazione [Filtra criteri incompatibili](/help/c-recommendations/plan-implement.md#concept_C1E1E2351413468692D6C21145EF0B84) di Target consente di controllare il filtraggio intelligente del selettore dell’algoritmo.

>[!NOTE]
>
>Questa impostazione è valida solo per le attività create nel Compositore esperienza visivo. Non è applicabile alle attività create nel Compositore esperienza basato su moduli (Target non dispone di contesto di posizione).

Per accedere all’impostazione [!UICONTROL Filtra criteri incompatibili], fai clic su [!UICONTROL Consigli] > [!UICONTROL Impostazioni]:

![](assets/recs_settings_filter.png)

Se l’impostazione [!UICONTROL Filtra criteri incompatibili] non è abilitata, Target non filtra gli algoritmi nel Selettore degli algoritmi e vengono visualizzati tutti gli algoritmi.

Se l’impostazione [!UICONTROL Filtra criteri incompatibili] è abilitata, nelle attività del Compositore esperienza visivo, Target legge il codice entityId e l’ID di categoria dalla posizione selezionata, quindi visualizza gli algoritmi basati su `currentItem|currentCategory` (se i rispettivi valori sono presenti in tale posizione). Di conseguenza, per impostazione predefinita, solo gli algoritmi compatibili per la posizione selezionata vengono visualizzati nel selettore algoritmi.

Se l’impostazione [!UICONTROL Filtra criteri incompatibili] è abilitata, è comunque possibile visualizzare gli algoritmi non compatibili deselezionando la casella [!UICONTROL Compatibile] durante la selezione dei criteri.

![](assets/compatible_checkbox.png)

L’elenco seguente contiene casi speciali in cui target non visualizza la casella [!UICONTROL Compatibile]:

* Sia entityId che l’ID di categoria sono presenti nella posizione, quindi non viene filtrato nulla.
* Stai utilizzando [!DNL mbox.js] versione 55 o precedente.
* La pagina non genera chiamate mbox (!config.isAutoCreateGlobalMbox &amp;&amp; !config.isRegionalMbox)
* I parametri di Target non sono definiti.

## Cosa devo fare se una raccolta in Consigli va a zero (0)?  {#section_E2DB2FE67CF24EEC81412BFF3FA6385D}

Considera le seguenti informazioni se noti che una raccolta, che in precedenza non lo era, va a zero:

* Puoi salvare nuovamente la raccolta e vedere se aggiorna il numero. Salvando nuovamente, la raccolta esegue tutti gli algoritmi che utilizzano tale raccolta.
* Stai guardando nell’ambiente giusto? Vai su [!DNL /target/products.html#recsSettings] e controlla (come mostrato di seguito).

   ![](assets/product_catalog.png)

* L’indice è aggiornato? Vai su [!DNL /target/products.html#productSearch] e controlla da quante ore esiste l’indice (ad esempio, &quot;indicizzato 3 ore fa&quot;). Se necessario, puoi aggiornare l’indice.
* Hai modificato qualcosa nel livello di feed o di dati che ha comportato la mancata corrispondenza delle entità alle regole di raccolta? Assicurati che le maiuscole e le minuscole corrispondano.
* Il feed è stato eseguito correttamente? Qualcuno ha cambiato la directory FTP, la password e così via?
* In Target gli aggiornamenti alla consegna (sulla pagina o nell’app del cliente) accadono il più rapidamente possibile. Tuttavia, Target deve anche fornire una qualche rappresentazione nell’interfaccia utente per l’addetto al marketing. Target non ritarda gli aggiornamenti di consegna per attendere che gli aggiornamenti dell’interfaccia utente siano sincronizzati. Puoi usare [mboxTrace](/help/c-activities/c-troubleshooting-activities/content-trouble.md) per vedere cosa c’è nel sistema nel momento in cui arriva una richiesta.

## Qual è la differenza tra Ponderazione attributi generale e Ponderazione attributi relativa alle somiglianze di contenuti? {#section_FCD96598CBB44B16A4C6C084649928FF}

La ponderazione degli attributi esiste in due forme: “ponderazione attributi standard” e “ponderazione attributi per somiglianza di contenuti”.

La “ponderazione attributi standard” si applica, se non a tutti, alla maggior parte di tipi di criteri (non solo alla Somiglianza contenuti). Questo tipo di ponderazione dà più peso a determinati valori di attributo. Nell’esempio seguente, i prodotti Nike ottengono un errore nei consigli di output.

![](assets/attribute_weighting_example.png)

La “ponderazione attributi per somiglianza contenuto” si applica solo ai criteri di Somiglianza contenuti.

Questo tipo di ponderazione è più dinamico e si basa sull’attuale “chiave dei consigli” (l’elemento attualmente visualizzato). Nel seguente esempio (marca x 16), a un visitatore che ha visualizzato le sneaker Nike, verranno probabilmente consigliati altri prodotti Nike (non necessariamente solo sneaker), invece di scarpe di altre marche. Se un visitatore sta visualizzando sneaker Adidas, è più probabile che i prodotti Adidas consigliati vengano visualizzati.

![](assets/content_similarity_example.png)

## Perché Target talvolta non è in grado di mostrare i consigli?  {#section_DB3F40673AED42228E407C05437D99E9}

Target a volte non può mostrare consigli a causa del basso numero di consigli disponibili.

Il numero di valori generati per criterio è tre volte il numero di entità specificato nel progetto. Il filtro runtime (ad esempio inventario, corrispondenza degli attributi mbox) viene applicato dopo la generazione di valori 3x, quindi è possibile finire con meno di 3x valori al momento della consegna. Per attenuare questa situazione, aumenta il numero di entità nella progettazione nascondendo altre entità.

Il seguente JavaScript può essere utilizzato all&#39;inizio del modello per aumentare il numero di entità richieste. In questo esempio, il numero di entità richieste è 30 (3x10).

```
#foreach($entity in $entities) 
 #if( $foreach.count > 10 ) 
  #break 
 #end 
 #set ($foo = $entity.id) 
#end 
```

## Qual è il limite di dimensione di una chiamata API per inserire/aggiornare prodotti? È possibile aggiornare 50.000 prodotti con una chiamata utilizzando l’API al posto di un feed?  {#section_434FE1F187B7436AA39B7C14C7895168}

Target impone un limite per i post di 50 MB a livello di applicazione; tuttavia, questo accade solo quando trasmetti l’intestazione del tipo di contenuto `application/x-www-form-urlencoded` .

Potresti sicuramente provare a inviare 50.000 prodotti con una sola chiamata. Se non riesce, puoi suddividerlo in batch. Adobe consiglia ai clienti di suddividere le chiamate in 5.000 o 10.000 batch di prodotti per ridurre la probabilità di un timeout dovuto al caricamento del sistema.

## È necessario specificare il nome mbox per la creazione di criteri di Consigli, promozioni o regole di test di modelli? {#section_FFA42ABCC5954B48A46526E32A3A88A2}

Durante la creazione di un criterio di Consigli, promozioni o una regola di test di modelli basato su un parametro mbox, `mboxParameter` non richiede più di specificare `mboxName`. Il nome dell’elemento mbox è ora facoltativo. Questa modifica consente di utilizzare parametri da più elementi mbox o di fare riferimento a un parametro che non è ancora stato registrato nella rete Edge.

Per selezionare il parametro desiderato:

* Durante la creazione di un criterio, una promozione o una regola di test del modello, seleziona un nome di parametro dall’elenco. Inizia a digitare i primi caratteri del nome del parametro desiderato o il nome completo del parametro desiderato.
* Se ricordi il nome mbox ma non il nome del parametro, usa la casella di controllo per filtrare una mbox nota trasmettendo il parametro desiderato.

Con uno di questi metodi, non esiste alcun collegamento tra mbox e il parametro. La regola di test di criteri, promozioni o modelli funziona in base al parametro su tutte le mbox che trasmettono tale parametro.

Se modifichi una regola di test di criteri, una promozione o un criterio, i criteri di filtraggio vengono visualizzati con il nome mbox fornito durante la creazione.

## Perché non riesco a salvare la mia attività di consigli legacy dopo aver definito un nuovo pubblico?  {#section_1E47C40B1FE7479BAC3EE0F50CE7C2C4}

Assicurati che il pubblico abbia un nome univoco. Se hai assegnato al pubblico lo stesso nome di un pubblico esistente, non puoi salvare l&#39;attività di Consigli legacy (attività di Consigli creata prima di ottobre 2016).

## Qual è la dimensione massima di un file CSV per un caricamento del feed?  {#section_20F1AF4839A447B9889B246D6E873538}

Non vi è alcun limite stabilito sul numero di righe o sulle dimensioni del file per il caricamento del file CSV di un feed. Tuttavia, come best practice, Adobe consiglia di limitare la dimensione del file CSV a 1 GB per evitare errori durante il processo di caricamento dei file. Se la dimensione del file supera 1 GB, può idealmente essere suddiviso in più file di feed. Il numero massimo di colonne di attributi personalizzati è 100 e gli attributi personalizzati sono limitati a 4096 caratteri. Nella pagina [Limitazioni di Target](/help/r-troubleshooting-target/target-limits.md#reference_BEFE60C3AAA442FF94D4EBFB9D3CC9B1) sono disponibili altri limiti alla lunghezza delle colonne richieste.

## È possibile escludere un’entità in modo dinamico? {#exclude}

Nella stringa di query, puoi trasmettere gli ID per le entità da escludere dai consigli. Ad esempio, puoi escludere gli articoli già presenti nel carrello.

Per abilitare la funzionalità di esclusione, utilizzate il parametro mbox `excludedIds`. Questo parametro punta a un elenco di ID di entità separati da virgola. Ad esempio, `mboxCreate(..., "excludedIds=1,2,3,4,5")`. Il valore viene inviato al momento della richiesta delle raccomandazioni.

L’esclusione viene eseguita solo per la chiamata Target corrente; Gli elementi non vengono esclusi nelle chiamate di Target successive a meno che il valore `excludedIds` non venga nuovamente trasmesso. Per escludere gli elementi nel carrello dai consigli su ogni pagina, continua a trasmettere il valore `excludedIds` su ogni pagina.

>[!NOTE]
>
>Se escludi troppe entità, i consigli si comportano come se non ci fossero abbastanza entità per riempire il modello di consigli.

Per escludere `entityIds`, aggiungi il token `&excludes=${mbox.excludedIds}` all’URL di contenuto dell’offerta. Quando l&#39;URL di contenuto viene estratto, i parametri necessari vengono sostituiti mediante i parametri di richiesta mbox correnti.

Per impostazione predefinita, questa funzione è attiva per i consigli appena creati. I consigli esistenti devono essere salvati per supportare le entità a esclusione dinamica.

## Cosa significa la risposta NO_CONTENT a volte restituita nella traccia di contenuto di Recommendations?

NO_CONTENT viene restituito quando i consigli non sono disponibili per l’algoritmo e la combinazione di chiavi richiesti. In generale, questa situazione si verifica quando i backup vengono disabilitati per l&#39;algoritmo e una o più delle seguenti situazioni sono ugualmente vere:

* I risultati non sono ancora pronti.

   Questa situazione si verifica in genere quando si salva un’attività appena creata o dopo che sono state apportate modifiche alla raccolta, ai criteri o alle promozioni utilizzate nell’attività.

* I risultati sono pronti, ma non ancora memorizzati nella cache del server perimetrale più vicino, per la combinazione di algoritmo/chiave richiesta.

   La richiesta avvia un&#39;operazione di caching, quindi questo problema dovrebbe risolversi da solo dopo alcuni ricaricamenti delle pagine e/o dopo pochi minuti.

* I risultati sono pronti, ma non disponibili per il valore chiave fornito.

   Questa situazione si verifica in genere quando si richiedono raccomandazioni per un elemento aggiunto al catalogo dopo l’esecuzione dell’algoritmo più recente e si risolve da solo dopo l’esecuzione dell’algoritmo successivo.

* Il rendering parziale del modello è disabilitato e non sono disponibili risultati sufficienti per riempire il modello.

   Questa situazione si verifica in genere quando si dispone di una regola di inclusione dinamica, che filtra in modo aggressivo molti elementi dai possibili risultati. Per evitare situazioni, abilitare i backup e non applicare la regola di inclusione ai backup, o utilizzare i criteri in sequenza con criteri filtrati in modo meno aggressivo.

