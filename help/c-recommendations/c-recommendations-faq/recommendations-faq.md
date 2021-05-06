---
keywords: risoluzione dei problemi;domande frequenti;FAQ;consigli;caratteri speciali;ponderazione degli attributi;somiglianza contenuti
description: Visualizza un elenco delle domande frequenti e delle risposte relative alle attività di Adobe [!DNL Target] Recommendations.
title: Dove posso trovare domande e risposte su [!DNL Target] Recommendations?
feature: Consigli
exl-id: aaa52923-1c2d-44ae-bd89-671329222077
translation-type: tm+mt
source-git-commit: 32eeec786af7aba747881ac84ef17d7a0124a45a
workflow-type: tm+mt
source-wordcount: '2940'
ht-degree: 33%

---

# ![PREMIUM](/help/assets/premium.png) Domande frequenti relative ai consigli

Elenco delle domande frequenti sulle attività di [!DNL Adobe Target] [!DNL Recommendations] .

## Perché [!UICONTROL Ricerca nel catalogo] non mostra i risultati corretti quando eseguo una ricerca su un attributo personalizzato con un valore numerico?

Quando esegui una ricerca di catalogo su un attributo personalizzato con un valore numerico, l’attributo personalizzato viene considerato come un tipo di stringa anziché come valore numerico.

Attualmente, non è disponibile alcuna funzionalità che consenta ai clienti di modificare il tipo di un attributo. Per apportare una modifica, [apri un problema del cliente](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) facendo riferimento agli attributi che richiedono la modifica del tipo da stringa a numerico.

## Quanto tempo ci vuole perché gli aggiornamenti agli articoli del catalogo si riflettano sul mio sito?

L’intervallo di tempo e i risultati variano a seconda di come vengono aggiornati gli elementi.

| Origine | Dettagli |
| --- | --- |
| Attributi degli articoli aggiornati tramite mbox o API | <ul><li>Recommendations viene aggiornato entro 15 minuti.</li><li>I consigli e gli attributi degli elementi esistenti vengono visualizzati finché non sono disponibili aggiornamenti.</li><li>La ricerca nel catalogo viene aggiornata dopo l&#39;indice del catalogo (3-8 ore).</li></ul> |
| Attributi degli articoli aggiornati tramite feed | <ul><li>Recommendations viene aggiornato dopo l’acquisizione dei feed (2-8 ore).</li><li>I consigli e gli attributi degli elementi esistenti vengono visualizzati finché non sono disponibili aggiornamenti.</li><li>La ricerca nel catalogo viene aggiornata dopo l’acquisizione dei feed (2-8 ore) e dopo l’indice del catalogo successivo (3-8 ore). La ricerca nel catalogo viene aggiornata entro 5-16 ore totali.</li></ul> |
| Elemento eliminato dal catalogo tramite [!DNL Target] interfaccia utente o API | <ul><li>Recommendations viene aggiornato entro 15 minuti.</li><li>I consigli e gli attributi degli elementi esistenti vengono visualizzati finché non sono disponibili aggiornamenti.</li><li>La ricerca nel catalogo viene aggiornata dopo l&#39;indice del catalogo (3-8 ore).</li></ul> |
| Elemento aggiunto al catalogo tramite mbox o API | <ul><li>Recommendations viene aggiornato dopo l’esecuzione dell’algoritmo. Le esecuzioni degli algoritmi sono pianificate ogni 12 ore per gli algoritmi a 1-2 giorni e ogni 24 ore per gli algoritmi a 7+ giorni.</li><li>I consigli esistenti vengono visualizzati finché non sono disponibili aggiornamenti se l’elemento aggiunto non è una chiave richiesta.</li><li>I consigli di backup vengono visualizzati finché non sono disponibili aggiornamenti se l’elemento aggiunto è una chiave richiesta.</li><li>La ricerca nel catalogo viene aggiornata dopo l&#39;indice del catalogo (3-8 ore).</li></ul> |
| Elemento aggiunto al catalogo tramite feed | <ul><li>Recommendations viene aggiornato dopo l’acquisizione del feed (2-8 ore). Le esecuzioni successive degli algoritmi vengono pianificate ogni 12 ore per gli algoritmi a 1-2 giorni e ogni 24 ore per gli algoritmi a 7+ giorni. Recommendations viene aggiornato entro 2-32 ore totali.</li><li>I consigli esistenti vengono visualizzati finché non sono disponibili aggiornamenti se l’elemento aggiunto non è una chiave richiesta.</li><li>I consigli di backup vengono visualizzati finché non sono disponibili aggiornamenti se l’elemento aggiunto è una chiave richiesta.</li><li>La ricerca nel catalogo viene aggiornata dopo l’inserimento dei feed (2-8 ore) e dopo l’indice del catalogo (3-8 ore). La ricerca nel catalogo viene aggiornata entro 5-16 ore totali.</li></ul> |

Dopo aver importato un file di feed o ricevuto aggiornamenti di entità tramite API o mbox, le seguenti modifiche si riflettono in meno di 60 minuti:

* Se un elemento è stato escluso in precedenza ma ora deve essere incluso, verrà incluso nella prossima esecuzione dell’algoritmo (12-24 ore).

   Questa situazione si verifica perché [!DNL Target] applica esclusioni sia online che offline. Quando un elemento viene escluso di recente, l’esclusione online viene applicata rapidamente. Quando un elemento è stato incluso di recente, l’esclusione online scompare rapidamente ma l’esclusione offline non scompare fino all’esecuzione dell’algoritmo successivo.

* Se un elemento è stato incluso in precedenza ma ora deve essere escluso, l’elemento viene escluso secondo &quot;Attributi articolo aggiornati...&quot;. la linea temporale di cui sopra a seconda della sorgente dei feed (15 minuti tramite mbox/API o 12-24 ore tramite feed).

Le modifiche seguenti vengono applicate solo dopo l’esecuzione dell’algoritmo successivo (entro 12-24 ore):

* Attributi degli articoli utilizzati nelle regole di raccolta utilizzate per l’attività.
* Attributi degli articoli utilizzati in una promozione in base a una raccolta o un attributo associato all’attività.
* Categoria di articoli in cui l’articolo viene visualizzato, per “Categoria corrente” o “Categoria preferita” nell’algoritmo “Articoli più venduti” o “Articoli più visualizzati”.
* Classificazione degli articoli consigliati quando l’attributo modificato è un attributo personalizzato utilizzato come chiave personalizzata per un algoritmo.
* Classificazione degli elementi consigliati in base a uno o più attributi modificati quando la logica dei consigli è &quot;Articoli con attributi simili&quot;, quando vengono utilizzati i fattori di ponderazione &quot;Somiglianza del contenuto&quot; o quando vengono utilizzati i fattori &quot;Ponderazione degli attributi&quot;.

>[!NOTE]
>
>Un file di feed viene considerato importato quando il suo stato cambia da “Importazione elementi” a “Preparazione aggiornamenti indice di ricerca”. Gli aggiornamenti possono richiedere più di 60 minuti per riflettersi nell’interfaccia utente di Ricerca nel catalogo; La funzione Ricerca nel catalogo è aggiornata quando lo stato del feed diventa &quot;Aggiornamenti completati&quot;. Anche se la funzione Ricerca nel catalogo non è ancora aggiornata, il sito riflette gli aggiornamenti sui tempi elencati sopra. Nella pagina Ricerca nel catalogo viene indicata l’ora dell’ultimo aggiornamento dell’indice di Ricerca nel catalogo.

## Quanto tempo ci vuole affinché una modifica alla configurazione delle impostazioni di attività, offerte, promozioni o criteri di Recommendations  si rifletta sul sito?

* Una modifica alle impostazioni di promozione può richiedere fino a cinque ore per essere visualizzata sul sito.
* Una modifica alle impostazioni di altri criteri potrebbe non essere applicata fino all’esecuzione dell’algoritmo successivo:

   * Alcune impostazioni di criteri (ad esempio, &quot;aggiunta di una regola di inclusione dinamica&quot;) vengono riflesse istantaneamente.
   * Non è possibile incorporare altre impostazioni di criteri (ad esempio &quot;rimozione di una regola di inclusione dinamica&quot;, modifica dell’intervallo di lookback e così via) finché non viene eseguito l’algoritmo successivo.
   * Le esecuzioni dell’algoritmo vengono attivate da queste modifiche ma possono richiedere fino a 24 ore per essere completate. Anche gli algoritmi vengono eseguiti su base pianificata ogni 12-24 ore.

## Quanto tempo ci vuole affinché il comportamento di un utente (ad esempio, facendo clic sul prodotto A e acquistando il prodotto B) si rifletta nei consigli *ricevuti dall&#39;utente*?

* Il prodotto/contenuto attualmente visualizzato/acquistato influisce sui consigli che l&#39;utente riceve sulla stessa richiesta di contenuto pageview/[!DNL Target].
* Con tale richiesta viene aggiornato il comportamento storico degli utenti, ad esempio &quot;ultimo prodotto visualizzato&quot;, &quot;prodotto più visualizzato&quot; e la cronologia generale di visualizzazione/acquisto, influenzando i consigli ricevuti dall’utente sulla successiva richiesta di contenuto pageview/[!DNL Target]. Ad esempio, gli algoritmi &quot;Articoli visualizzati di recente&quot; e &quot;Consigliati per te&quot; vengono aggiornati con ogni visualizzazione/acquisto del prodotto e si riflettono sulla successiva richiesta di contenuto.

## Quanto tempo ci vuole affinché il comportamento di un utente (ad esempio, facendo clic sul prodotto A e acquistando il prodotto B) si rifletta nei consigli *ricevuti dagli altri utenti*?

Il comportamento degli utenti in aggregato viene incorporato nell’elaborazione di algoritmi offline, con ogni esecuzione di algoritmi che si verifica ogni 12-24 ore.

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

[!DNL Target] dispone di un’impostazione  [Filter Incompatible ](/help/c-recommendations/plan-implement.md#concept_C1E1E2351413468692D6C21145EF0B84) Criteria (Filtra criteri incompatibili) per controllare il filtraggio intelligente del selettore dell’algoritmo.

>[!NOTE]
>
>Questa impostazione è valida solo per le attività create nel Compositore esperienza visivo. Questa impostazione non si applica alle attività create nel Compositore esperienza basato su moduli ([!DNL Target] non ha contesto di posizione).

Per accedere all’impostazione [!UICONTROL Filtra criteri incompatibili], fai clic su [!UICONTROL Consigli] > [!UICONTROL Impostazioni]:

![](assets/recs_settings_filter.png)

Se l’impostazione [!UICONTROL Filtra criteri incompatibili] non è abilitata,  non filtra gli algoritmi nel Selettore degli algoritmi e vengono visualizzati tutti gli algoritmi.[!DNL Target]

Se l’impostazione [!UICONTROL Filtra criteri incompatibili] è abilitata, nelle attività del Compositore esperienza visivo [!DNL Target] legge entityId e category Id dalla posizione selezionata, quindi visualizza gli algoritmi basati su `currentItem|currentCategory` (se i rispettivi valori sono presenti in tale posizione). Di conseguenza, per impostazione predefinita, solo gli algoritmi compatibili per la posizione selezionata vengono visualizzati nel selettore algoritmi.

Se l’impostazione [!UICONTROL Filtra criteri incompatibili] è abilitata, è comunque possibile visualizzare gli algoritmi non compatibili deselezionando la casella [!UICONTROL Compatibile] durante la selezione dei criteri.

![](assets/compatible_checkbox.png)

Il seguente elenco contiene casi speciali in cui [!DNL Target] non visualizza la casella di controllo [!UICONTROL Compatibile]:

* Sia entityId che l’ID di categoria sono presenti nella posizione, quindi non viene filtrato nulla.
* Stai utilizzando [!DNL mbox.js] versione 55 o precedente.
* La pagina non genera chiamate mbox (!config.isAutoCreateGlobalMbox &amp;&amp; !config.isRegionalMbox)
* [!DNL Target] i parametri non sono definiti.

## Cosa devo fare se una raccolta in Consigli va a zero (0)?  {#section_E2DB2FE67CF24EEC81412BFF3FA6385D}

Considera le seguenti informazioni se noti che una raccolta, che in precedenza non lo era, va a zero:

* Puoi salvare nuovamente la raccolta e vedere se aggiorna il numero. Salvando nuovamente, la raccolta esegue tutti gli algoritmi che utilizzano tale raccolta.
* Stai guardando nell’ambiente giusto? Vai su [!DNL /target/products.html#recsSettings] e controlla (come mostrato di seguito).

   ![](assets/product_catalog.png)

* L’indice è aggiornato? Vai su [!DNL /target/products.html#productSearch] e controlla da quante ore esiste l’indice (ad esempio, &quot;indicizzato 3 ore fa&quot;). Se necessario, puoi aggiornare l’indice.
* Hai modificato qualcosa nel livello di feed o di dati che ha comportato la mancata corrispondenza delle entità alle regole di raccolta? Assicurati che le maiuscole e le minuscole corrispondano.
* Il feed è stato eseguito correttamente? Qualcuno ha cambiato la directory FTP, la password e così via?
* [!DNL Target]In gli aggiornamenti alla consegna (sulla pagina o nell’app del cliente) accadono il più rapidamente possibile. Tuttavia, [!DNL Target] deve anche fornire una qualche rappresentazione nell’interfaccia utente per l’addetto al marketing. [!DNL Target] non ritarda gli aggiornamenti di consegna per attendere che gli aggiornamenti dell’interfaccia utente siano sincronizzati. Puoi usare [mboxTrace](/help/c-activities/c-troubleshooting-activities/content-trouble.md) per vedere cosa c’è nel sistema nel momento in cui arriva una richiesta.

## Qual è la differenza tra Ponderazione attributi generale e Ponderazione attributi relativa alle somiglianze di contenuti? {#section_FCD96598CBB44B16A4C6C084649928FF}

La ponderazione degli attributi esiste in due forme: “ponderazione attributi standard” e “ponderazione attributi per somiglianza di contenuti”.

La “ponderazione attributi standard” si applica, se non a tutti, alla maggior parte di tipi di criteri (non solo alla Somiglianza contenuti). Questo tipo di ponderazione dà più peso a determinati valori di attributo. Nell’esempio seguente, i prodotti Nike ottengono un errore nei consigli di output.

![](assets/attribute_weighting_example.png)

La “ponderazione attributi per somiglianza contenuto” si applica solo ai criteri di Somiglianza contenuti.

Questo tipo di ponderazione è più dinamico e si basa sull’attuale “chiave dei consigli” (l’elemento attualmente visualizzato). Nel seguente esempio (marca x 16), a un visitatore che ha visualizzato le sneaker Nike, verranno probabilmente consigliati altri prodotti Nike (non necessariamente solo sneaker), invece di scarpe di altre marche. Se un visitatore sta visualizzando sneaker Adidas, è più probabile che i prodotti Adidas consigliati vengano visualizzati.

![](assets/content_similarity_example.png)

## Perché a volte [!DNL Target] non è in grado di mostrare i consigli? {#section_DB3F40673AED42228E407C05437D99E9}

[!DNL Target] a volte non può mostrare consigli a causa del basso numero di consigli disponibili.

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

[!DNL Target] impone un limite per i post di 50 MB a livello di applicazione; tuttavia, questo accade solo quando trasmetti l’intestazione del tipo di  `application/x-www-form-urlencoded` contenuto.

Potresti sicuramente provare a inviare 50.000 prodotti con una sola chiamata. Se non riesce, puoi suddividerlo in batch. Adobe consiglia ai clienti di suddividere le chiamate in 5.000 o 10.000 batch di prodotti per diminuire la probabilità di un timeout a causa del carico di sistema.

## È necessario specificare il nome mbox per la creazione di criteri, promozioni o regole di test di modelli Recommendations? {#section_FFA42ABCC5954B48A46526E32A3A88A2}

Durante la creazione di un criterio di Consigli, promozioni o una regola di test di modelli basato su un parametro mbox, `mboxParameter` non richiede più di specificare `mboxName`. Il nome dell’elemento mbox è ora facoltativo. Questa modifica consente di utilizzare parametri da più elementi mbox o di fare riferimento a un parametro che non è ancora stato registrato nella rete Edge.

Per selezionare il parametro desiderato:

* Durante la creazione di un criterio, una promozione o una regola di test del modello, seleziona un nome di parametro dall’elenco. Inizia a digitare i primi caratteri del nome del parametro desiderato o il nome completo del parametro desiderato.
* Se ricordi il nome mbox ma non il nome del parametro, usa la casella di controllo per filtrare una mbox nota trasmettendo il parametro desiderato.

Con uno di questi metodi, non esiste alcun collegamento tra mbox e il parametro. La regola di test di criteri, promozioni o modelli funziona in base al parametro su tutte le mbox che trasmettono tale parametro.

Se modifichi una regola di test di criteri, una promozione o un criterio, i criteri di filtraggio vengono visualizzati con il nome mbox fornito durante la creazione.

## Perché non riesco a salvare la mia attività di consigli legacy dopo aver definito un nuovo pubblico?  {#section_1E47C40B1FE7479BAC3EE0F50CE7C2C4}

Assicurati che il pubblico abbia un nome univoco. Se hai assegnato al pubblico lo stesso nome di un pubblico esistente, non puoi salvare l&#39;attività di Consigli legacy (attività di Consigli creata prima di ottobre 2016).

## Qual è la dimensione massima di un file CSV per un caricamento del feed?  {#section_20F1AF4839A447B9889B246D6E873538}

Non vi è alcun limite stabilito sul numero di righe o sulle dimensioni del file per il caricamento del file CSV di un feed. Tuttavia, come best practice, Adobe consiglia di limitare la dimensione del file CSV a 1 GB per evitare errori durante il processo di caricamento dei file. Se la dimensione del file supera 1 GB, può idealmente essere suddiviso in più file di feed. Il numero massimo di colonne di attributi personalizzati è 100 e gli attributi personalizzati sono limitati a 4096 caratteri. Nella pagina [[!DNL Target] Limitazioni](/help/r-troubleshooting-target/target-limits.md#reference_BEFE60C3AAA442FF94D4EBFB9D3CC9B1) sono disponibili altri limiti alla lunghezza delle colonne richieste.

## È possibile escludere un’entità in modo dinamico? {#exclude}

Nella stringa di query, puoi trasmettere gli ID per le entità da escludere dai consigli. Ad esempio, puoi escludere gli articoli già presenti nel carrello.

Per abilitare la funzionalità di esclusione, utilizzate il parametro mbox `excludedIds`. Questo parametro punta a un elenco di ID di entità separati da virgola. Ad esempio, `mboxCreate(..., "excludedIds=1,2,3,4,5")`. Il valore viene inviato al momento della richiesta delle raccomandazioni.

L’esclusione viene eseguita solo per la chiamata corrente [!DNL Target]; gli elementi non vengono esclusi nelle chiamate successive [!DNL Target] a meno che il valore `excludedIds` non venga nuovamente passato. Per escludere gli elementi nel carrello dai consigli su ogni pagina, continua a trasmettere il valore `excludedIds` su ogni pagina.

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

## I consigli basati sugli elementi visualizzati di recente persistono su più dispositivi per un singolo visitatore? {#persist-across-devices}

Quando un visitatore avvia una sessione, l’ID della sessione è associato a un singolo computer Edge e su questo computer Edge viene memorizzata una cache di profilo temporanea. Le richieste successive dalla stessa sessione leggono questa cache del profilo, inclusi gli elementi visualizzati di recente.

Al termine della sessione (generalmente, quando scade dopo 30 minuti di nessuna attività), lo stato della sessione, inclusi gli elementi visualizzati di recente, viene quindi mantenuto in un archivio di profilo più permanente nello stesso margine geografico.

Le sessioni successive da diversi dispositivi possono quindi accedere a questi elementi visualizzati di recente, purché la nuova sessione sia collegata al profilo del cliente tramite lo stesso ID Marketing Cloud (MCID), ID Experience Cloud (ECID) o CustomerID/mbox3rdPartyId.

Se un visitatore ha due sessioni attive contemporaneamente, gli elementi visualizzati di recente su un dispositivo non aggiornano gli elementi visualizzati di recente sull&#39;altro dispositivo, a meno che i dispositivi non siano costretti a condividere l&#39;ID sessione. Esiste una soluzione potenziale per il problema, ma [!DNL Target] non supporta direttamente la condivisione di un ID sessione su più dispositivi. Il cliente deve gestire autonomamente questa condivisione ID.

Questo comportamento si verifica ancora se un visitatore è attivo su un dispositivo e poi diventa attivo sull&#39;altro dispositivo qualche minuto dopo. La sessione del primo dispositivo non scade per 30 minuti e può trascorrere fino a cinque minuti prima che lo stato del profilo sia scritto nello stato permanente ed elaborato. Consenti 35 minuti per la scadenza della sessione e il profilo da memorizzare durante il test di questo comportamento.

Se il visitatore non dispone di due sessioni attive contemporaneamente, gli elementi visualizzati di recente su un dispositivo aggiornano gli elementi visualizzati di recente sull&#39;altro dispositivo, purché la sessione sia terminata. Consenti la scadenza di 35 minuti per la sessione durante il test di questo comportamento.
