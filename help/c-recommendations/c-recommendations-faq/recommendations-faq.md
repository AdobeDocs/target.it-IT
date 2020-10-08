---
keywords: troubleshooting;frequently asked questions;FAQ;FAQs;recommendations;special characters;attribute weighting;content similarity
description: Elenco delle domande frequenti sulle  attività di Adobe Target Recommendations.
title: ' Adobe Target Recommendations FAQ'
feature: recommendations general
uuid: 27752811-0ffe-4d60-83d1-39e18b1953d5
translation-type: tm+mt
source-git-commit: e603c623b47c3c5391ba76da811f2e72daf22616
workflow-type: tm+mt
source-wordcount: '2019'
ht-degree: 80%

---


# ![PREMIUM](/help/assets/premium.png) Domande frequenti relative ai consigli{#recommendations-faq}

Elenco delle domande frequenti sulle  attività di Adobe Target Recommendations.

## Perché Catalog Search non visualizza i risultati corretti quando si esegue una ricerca su un attributo personalizzato con un valore numerico?

Quando si esegue una ricerca di catalogo su un attributo personalizzato con un valore numerico, l&#39;attributo personalizzato viene considerato come tipo String anziché come valore numerico.

Al momento, non è disponibile alcuna funzionalità che consenta ai clienti di modificare il tipo di un attributo. Per apportare una modifica, [aprire un problema](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) del cliente che fa riferimento agli attributi che richiedono la modifica del tipo da stringa a numerico.

## Quanto tempo trascorre prima che gli aggiornamenti degli articoli nel catalogo vengano rispecchiati nel sito?

Dopo aver importato un file di feed, o ricevuto aggiornamenti di entità tramite API o mbox, le seguenti modifiche verranno riportate in meno di 60 minuti:

* Attributi degli articoli restituiti nel modello Progettazione.
* Attributi degli articoli utilizzati nelle regole di esclusione globali che impediscono l’inclusione dell’articolo nei consigli restituiti.
* Attributi degli articoli utilizzati nelle regole di inclusione dei criteri che incidono sull’inclusione o esclusione dell’articolo dai consigli restituiti.

Le modifiche seguenti vengono applicate solo dopo l’esecuzione dell’algoritmo successivo (entro 12-24 ore):

* Attributi degli articoli utilizzati nelle regole di raccolta utilizzate per l’attività.
* Attributi degli articoli utilizzati in una promozione in base a una raccolta o un attributo associato all’attività.
* Categoria di articoli in cui l’articolo viene visualizzato, per “Categoria corrente” o “Categoria preferita” nell’algoritmo “Articoli più venduti” o “Articoli più visualizzati”.
* Classificazione degli articoli consigliati quando l’attributo modificato è un attributo personalizzato utilizzato come chiave personalizzata per un algoritmo.
* Classificazione degli articoli consigliati in base agli attributi modificati quando la logica dei consigli è “Articoli con attributi simili”, quando vengono utilizzati i fattori di ponderazione “Somiglianza del contenuto” o quando vengono utilizzati i fattori “Ponderazione degli attributi”.

>[!NOTE]
>
>Un file di feed viene considerato importato quando il suo stato cambia da “Importazione elementi” a “Preparazione aggiornamenti indice di ricerca”. Possono trascorrere più di 60 minuti prima che gli aggiornamenti vengano rispecchiati nell’interfaccia utente di Ricerca nel catalogo. La funzione Ricerca nel catalogo è aggiornata quando lo stato del feed diventa “Aggiornamenti completati”. Anche se la funzione Ricerca catalogo non risulta ancora aggiornata, gli aggiornamenti vengono rispecchiati nel sito in base alle tempistiche riportate qui sopra. Nella pagina Ricerca nel catalogo viene indicata l’ora dell’ultimo aggiornamento dell’indice di Ricerca nel catalogo.

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

I criteri disponibili si basano sulla categoria corrente. Quando si creano offerte di consigli, il selettore di algoritmi visualizza i criteri in base all’ID di categoria.

Se la posizione in cui stai applicando questo criterio non contiene l’ID di categoria, sono disponibili solo alcuni criteri nella selezione algoritmi.

Se utilizzi una posizione in cui l’ID di categoria è presente nella mbox, il selettore di criteri contiene tutti i criteri applicabili.

L’impostazione [Filtra criteri incompatibili](../../c-recommendations/plan-implement.md#concept_C1E1E2351413468692D6C21145EF0B84) di Target consente di controllare il filtraggio intelligente del selettore dell’algoritmo.

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

## Cosa devo fare se una raccolta in Consigli va a zero (0)? {#section_E2DB2FE67CF24EEC81412BFF3FA6385D}

Considera le seguenti informazioni se noti che una raccolta, che in precedenza non lo era, va a zero:

* Puoi salvare nuovamente la raccolta e vedere se il numero si aggiorna. Nota che, salvando nuovamente, la raccolta eseguirà nuovamente tutti gli algoritmi che la utilizzano.
* Stai guardando nell’ambiente giusto? Vai su [!DNL /target/products.html#recsSettings] e controlla (come mostrato di seguito).

   ![](assets/product_catalog.png)

* L’indice è aggiornato? Vai su [!DNL /target/products.html#productSearch] e controlla da quante ore esiste l’indice (per esempio, “indicizzato 3 ore fa”). Se necessario, puoi aggiornare l’indice.
* Hai modificato qualcosa nel livello di feed o di dati che ha comportato la mancata corrispondenza delle entità alle regole di raccolta? Assicurati che le maiuscole e le minuscole corrispondano.
* Il feed è stato eseguito correttamente? Qualcuno ha cambiato la directory FTP, la password ecc.?
* In Target gli aggiornamenti alla consegna (sulla pagina o nell’app del cliente) accadono il più rapidamente possibile. Tuttavia, dobbiamo anche fornire qualche rappresentazione nell’interfaccia utente per l’addetto al marketing. Non ritardiamo necessariamente gli aggiornamenti di consegna per attendere la sincronizzazione con gli aggiornamenti dell’interfaccia utente. Puoi usare [mboxTrace](/help/c-activities/c-troubleshooting-activities/content-trouble.md) per vedere cosa c’è nel sistema nel momento in cui arriva una richiesta.

## Qual è la differenza tra Ponderazione attributi generale e Ponderazione attributi relativa alle somiglianze di contenuti? {#section_FCD96598CBB44B16A4C6C084649928FF}

La ponderazione degli attributi esiste in due forme: “ponderazione attributi standard” e “ponderazione attributi per somiglianza di contenuti”.

La “ponderazione attributi standard” si applica, se non a tutti, alla maggior parte di tipi di criteri (non solo alla Somiglianza contenuti). Questo tipo di ponderazione dà più peso a determinati valori di attributo. Nell’esempio seguente, i prodotti Nike ottengono un aumento dei consigli in uscita.

![](assets/attribute_weighting_example.png)

La “ponderazione attributi per somiglianza contenuto” si applica solo ai criteri di Somiglianza contenuti.

Questo tipo di ponderazione è più dinamico e si basa sull’attuale “chiave dei consigli” (l’elemento attualmente visualizzato). Nel seguente esempio (marca x 16), a un visitatore che ha visualizzato le sneaker Nike, verranno probabilmente consigliati altri prodotti Nike (non necessariamente solo sneaker), invece di scarpe di altre marche. A un visitatore che ha visualizzato delle sneaker Adidas, verranno probabilmente consigliati prodotti Adidas.

![](assets/content_similarity_example.png)

## Perché Target talvolta non è in grado di mostrare i consigli? {#section_DB3F40673AED42228E407C05437D99E9}

Target a volte non può mostrare consigli a causa del basso numero di consigli disponibili.

Il numero di valori generati per criterio è pari a 3 volte il numero di entità specificato nel modello. Il filtro runtime (ad esempio inventario, corrispondenza degli attributi mbox) viene applicato dopo la generazione di valori 3x, quindi è possibile finire con meno di 3x valori al momento della consegna. Per limitare questa situazione, aumenta il numero di entità nel modello nascondendo altre entità.

Il seguente JavaScript può essere utilizzato all&#39;inizio del modello per aumentare il numero di entità richieste. In questo esempio, il numero di entità richieste è 30 (3x10).

```
#foreach($entity in $entities) 
 #if( $foreach.count > 10 ) 
  #break 
 #end 
 #set ($foo = $entity.id) 
#end 
```

## Qual è il limite di dimensione di una chiamata API per inserire/aggiornare prodotti? È possibile aggiornare 50.000 prodotti con una chiamata utilizzando l’API al posto di un feed? {#section_434FE1F187B7436AA39B7C14C7895168}

Target impone un limite per i post di 50 MB a livello di applicazione; tuttavia, ciò si verifica solo quando trasmetti l’intestazione del tipo di contenuto `application/x-www-form-urlencoded`.

Potresti sicuramente provare a inviare 50.000 prodotti con una sola chiamata. Se questa avesse esito negativo, dovresti suddividerla in batch. Di solito consigliamo ai clienti di suddividere le chiamate in 5.000 o 10.000 batch di prodotto per diminuire la possibilità di un timeout dovuto al carico del sistema.

## È necessario specificare il nome mbox per creare i criteri per i Consigli, le promozioni o le regole di test di modelli? {#section_FFA42ABCC5954B48A46526E32A3A88A2}

Durante la creazione di un criterio di Consigli, promozioni o una regola di test di modelli basato su un parametro mbox, `mboxParameter` non richiede più di specificare `mboxName`. Il nome dell’elemento mbox è ora facoltativo. Questa modifica consente di utilizzare parametri da più elementi mbox o di fare riferimento a un parametro che non è ancora stato registrato nella rete Edge.

Per selezionare il parametro desiderato:

* Mentre crei un nuovo criterio, una promozione o una regola di test di modelli, seleziona il nome di un parametro dall&#39;elenco, comincia a digitare i primi caratteri del parametro desiderato o il nome intero.
* Se ricordi il nome mbox ma non il nome del parametro, usa la casella di controllo per filtrare una mbox nota trasmettendo il parametro desiderato.

Con uno di questi metodi, non esiste alcun collegamento tra mbox e il parametro. Il criterio, la promozione o la regola di test di modelli funzioneranno sulla base del parametro su tutte le mboxes che trasmettono tale parametro.

Se modifichi una regola di test di criteri, una promozione o un criterio, i criteri di filtraggio vengono visualizzati con il nome mbox fornito durante la creazione.

## Perché non riesco a salvare la mia attività di consigli legacy dopo aver definito un nuovo pubblico? {#section_1E47C40B1FE7479BAC3EE0F50CE7C2C4}

Assicurati che il pubblico abbia un nome univoco. Se hai assegnato al pubblico lo stesso nome di un pubblico esistente, non puoi salvare l&#39;attività di Consigli legacy (attività di Consigli creata prima di ottobre 2016).

## Qual è la dimensione massima di un file CSV per un caricamento del feed? {#section_20F1AF4839A447B9889B246D6E873538}

Non vi è alcun limite stabilito sul numero di righe o sulle dimensioni del file per il caricamento del file CSV di un feed. Tuttavia, come best practice, si consiglia di limitare le dimensioni del file CSV a 1 GB per evitare errori durante il processo di caricamento dei file. Se le dimensioni del file superano 1 GB, idealmente dovrebbe essere suddiviso in più file di feed. Il numero massimo di colonne di attributi personalizzati è 100 e gli attributi personalizzati sono limitati a 4096 caratteri. Ulteriori limiti sulla lunghezza delle colonne richieste sono disponibili nella [pagina Limitazioni di Target](../../r-troubleshooting-target/target-limits.md#reference_BEFE60C3AAA442FF94D4EBFB9D3CC9B1).

## È possibile escludere un’entità in modo dinamico?

Nella stringa di query, puoi trasmettere gli ID per le entità da escludere dai consigli. Ad esempio, potreste voler escludere gli articoli già presenti nel carrello.

Per abilitare la funzionalità di esclusione, utilizzate il parametro mbox `excludedIds`. Questo parametro punta a un elenco di ID di entità separati da virgola. Ad esempio, `mboxCreate(..., "excludedIds=1,2,3,4,5")`. Il valore viene inviato al momento della richiesta delle raccomandazioni.

L&#39;esclusione viene eseguita solo per la chiamata Target corrente; gli elementi non sono esclusi dalle chiamate Target successive, a meno che il `excludedIds` valore non venga nuovamente passato. Per escludere gli elementi nel carrello dalle raccomandazioni su ogni pagina, continuate a trasmettere il `excludedIds` valore su ogni pagina.

>[!NOTE]
>
>Se escludi troppe entità, i consigli si comportano come se non ci fossero abbastanza entità per riempire il modello di consigli.

To exclude `entityIds`, append the `&excludes=${mbox.excludedIds}` token to the offer content url. Quando l&#39;URL di contenuto viene estratto, i parametri necessari vengono sostituiti mediante i parametri di richiesta mbox correnti.

Per impostazione predefinita, questa funzione è attiva per i consigli appena creati. I consigli esistenti devono essere salvati per supportare le entità a esclusione dinamica.

## Cosa significa la risposta NO_CONTENT restituita talvolta nella traccia di contenuto Recommendations?

NO_CONTENT viene restituito quando le raccomandazioni non sono disponibili per l&#39;algoritmo e la combinazione di chiavi richiesti. In genere, ciò si verifica quando i backup vengono disabilitati per l&#39;algoritmo e anche una o più delle seguenti situazioni è vera:

* I risultati non sono ancora pronti.

   Ciò si verifica in genere quando si salva per la prima volta un&#39;attività appena creata o dopo che sono state apportate modifiche alla raccolta, ai criteri o alle promozioni utilizzate nell&#39;attività.

* I risultati sono pronti, ma non ancora memorizzati nella cache del server periferico più vicino, per la combinazione di tasti/algoritmo richiesta.

   La richiesta appena effettuata avvierà un&#39;operazione di caching, quindi questa si risolve automaticamente dopo alcuni ricarichi di pagina e/o pochi minuti.

* I risultati sono pronti, ma non sono disponibili per il valore chiave fornito.

   Ciò si verifica in genere quando si richiedono raccomandazioni per un elemento aggiunto al catalogo dopo l&#39;esecuzione dell&#39;algoritmo più recente e si risolve automaticamente dopo l&#39;esecuzione dell&#39;algoritmo successivo.

* Il rendering parziale del modello è disattivato e non sono disponibili risultati sufficienti per compilare il modello.

   Ciò si verifica in genere quando si dispone di una regola di inclusione dinamica, che filtra in modo aggressivo molti elementi dai possibili risultati. Per evitare questo problema, abilitate i backup e non applicate la regola di inclusione ai backup, né utilizzate i criteri in sequenza con criteri filtrati meno aggressivi.

