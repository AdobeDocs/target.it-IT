---
keywords: visual experience composer;visual experience composer best practices;visual experience composer limitations;visual experience composer caveats;vec best practices;vec
description: Le best practice seguenti consentono di ottenere più facilmente il funzionamento previsto per le esperienze. Durante l’utilizzo del Compositore esperienza visivo è necessario considerare ulteriori suggerimenti e limitazioni.
title: Best practice e limitazioni del Compositore esperienza visivo
feature: null
topic: Classic
uuid: 8d1d199b-b3d7-4edb-ba05-bd97372a0b9e
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '2448'
ht-degree: 97%

---


# Best practice e limitazioni del Compositore esperienza visivo{#visual-experience-composer-best-practices-and-limitations}

Le best practice seguenti consentono di ottenere più facilmente il funzionamento previsto per le esperienze. Durante l’utilizzo del Compositore esperienza visivo è necessario considerare ulteriori suggerimenti e limitazioni.

Segui queste best practice per evitare che si verifichino problemi imprevisti con le esperienze che progetti.

## Best practice {#section_86CF28C99CFF40329E4CBAFE4DD78BB4}

**Per mbox.js versione 57 e successive e per at.js, inserisci il riferimento a mbox.js o at.js nella parte superiore della sezione`<head>`della pagina.**

Se utilizzi anche il servizio API visitatore, inserisci il relativo script prima di mbox.js o at.js.

**Per le versioni di mbox.js precedenti alla 57, posiziona il codice mbox.js il più in basso possibile nella sezione`<head>`della pagina.**

Inserisci mbox.js alla fine della sezione `<head>`, senza dichiarazioni aggiuntive successive. In caso contrario, eventuali tag di script o di collegamento verranno spostati nella sezione `<body>`.

**Puoi abilitare il Compositore esperienza avanzato a livello di account (abilitato per tutte le attività create nell’account) o a livello della singola attività.**

To enable the Enhanced Experience Composer at the account level, click [!UICONTROL Administration > Visual Experience Composer], then toggle the switch to the On position.

Per abilitare il Compositore esperienza avanzato a livello di attività durante la creazione di un&#39;attività nel Compositore esperienza visivo, fai clic su [!UICONTROL Configura > URL], quindi attiva il pulsante.

**Potete  inserire nell&#39;elenco Consentiti alcuni indirizzi IP se Enhanced Visual Experience Composer (Compositore esperienza visivo avanzato) non viene caricato sulle pagine sicure del sito.**

I problemi di caricamento di Enhanced Visual Experience Composer (Compositore esperienza visivo avanzato) possono essere risolti  inserire nell&#39;elenco Consentiti i seguenti indirizzi IP. Si tratta degli indirizzi IP per il server Adobe utilizzato per il proxy del Compositore esperienza avanzato. Sono necessari solo per modificare le attività. I visitatori del sito non necessitano di questi indirizzi IP inseriti nell&#39;elenco Consentiti.

Stati Uniti: 52.55.99.45, 54.80.158.92, e 54.204.197.253

Europa, Medio Oriente e Africa (EMEA): 52.51.238.221, 52.210.199.44, e 54.72.56.50

Asia-Pacifico (APAC): 52.193.67.35, 54.199.198.109, e 54.199.241.57

**Utilizza ID univoci per gli elementi di primo livello e per tutti gli altri elementi candidati ad attività di test o targeting.**

Qualsiasi elemento interno all&#39;elemento corpo deve presentare un ID univoco. Nel caso nuovi elementi vengano inseriti nel corpo e il codice cambi posizione, sarà possibile riconoscere con maggiore facilità almeno gli elementi padre.

Gli ID non sono obbligatori in Adobe Target, ma il loro utilizzo aumenta l&#39;affidabilità delle esperienze realizzate con il Compositore esperienza. In Target vengono utilizzati selettori CSS per modificare il contenuto quando l&#39;esperienza viene distribuita. Quando modifichi un&#39;esperienza, nel Compositore esperienza visivo viene eseguito l&#39;ancoraggio del selettore precedente più vicino con un attributo id non nullo all&#39;elemento HTML in fase di modifica. Di conseguenza si consiglia di non utilizzare meccanismi, comprese librerie JavaScript, che impostino o modifichino gli attributi ID HTML. Sebbene tali ID possano essere disponibili nel Compositore esperienza di Target per la creazione dell&#39;attività, se JavaScript li modifica, l&#39;ID utilizzato alla creazione dell&#39;esperienza potrebbe non essere disponibile al momento della sua esecuzione. Se l&#39;ID non è disponibile, l&#39;ancoraggio del selettore all&#39;ID avrà esito negativo.

**Denomina le classi CSS in modo che siano facilmente identificabili.**

Quando modifichi le classi CSS nel Compositore esperienza visivo, è utile renderle facilmente identificabili utilizzando nomi di classe descrittivi. Questa operazione assicura che vengano modificate le classi CSS corrette e che le pagine vengano visualizzate come previsto.

Non utilizzare la proprietà CSS `!important` quando nascondi o rimuovi elementi.

Se la proprietà CSS 1!important1 è presente, sulle modifiche apportate da target.js durante la distribuzione avranno priorità le regole CSS del sito.

**Evita l&#39;uso di tabelle HTML per i layout di pagina.**

Per la formattazione di una pagina, in Target Standard e Premium viene utilizzato JavaScript. La modifica dei layout basati su tabelle con JavaScript risulta difficoltosa. Inoltre, i layout basati su tabelle potrebbero non essere visualizzati allo stesso modo in tutti i browser. Per ottenere i risultati ottimali, crea i layout di pagina con CSS.

**Riduci al minimo l&#39;utilizzo di iFrame.**

Ridurre al minimo l&#39;uso di iFrame è una buona tecnica per semplificare la gestione delle pagine e dei test. Nel Compositore esperienza visivo è possibile applicare alcune azioni all&#39;interno di un iFrame, mentre altre (come il ridimensionamento) non funzionano correttamente. Gestire e ridimensionare le pagine che utilizzano più iFrame risulta difficoltoso. Come risultato, il test delle pagine con molti elementi iFrame potrebbe creare problemi.

**Dopo la preparazione di DOM, cerca di apportare tutte le modifiche DOM dinamiche il prima possibile.**

Se le modifiche non vengono apportate prima dell&#39;applicazione dell&#39;esperienza da parte di target.js, la distribuzione dei contenuti potrebbe non riuscire. Questo avviene solo in caso di modifica DOM nella gerarchia di un elemento con targeting.

**Utilizza solo un tag testo normale o immagine negli elementi di ancoraggio.**

`<a>Anchor Text</a>`

O

`<a href=""> <img src=""> </img> </a>`

**Evita elementi a livello di blocco all&#39;interno di un elemento in linea.**

Gli elementi a livello di blocco non devono essere utilizzati all&#39;interno di elementi in linea come tag di ancoraggio, span e così via. Questo potrebbe causare la perdita di altezza e larghezza degli elementi in linea. Lo strumento di sovrapposizione nel Compositore esperienza visivo potrebbe quindi non funzionare come previsto.

**Non utilizzare il tag di base nel sito web per risolvere URL e collegamenti.**

Mediante il Compositore esperienza visivo è possibile manipolare il sito web dietro le quinte, utilizzando un server proxy che aggiorna i collegamenti. Se aggiungi un tag di base, gli URL utilizzati dal server proxy verranno risolti nuovamente dal browser e risulteranno interrotti.

**Modifica l&#39;HTML per manipolare la struttura DOM può interrompere i selettori.**

Ad esempio, supponiamo che tu abbia eseguito due azioni:

* Aggiunta di una classe all&#39;elemento 1
* Modifica del codice HTML dell&#39;elemento 1

Ogni modifica crea un nuovo elemento nel Compositore esperienza visivo. La seconda azione modifica l&#39;elemento 1: se lo elimini, la seconda azione non avrà più niente da modificare, risultando nella mancata applicazione della modifica.

In altre parole, se aggiungi un elemento con testo e modifichi tale elemento con un testo diverso in un&#39;azione separata, l&#39;editor di codice mostrerà entrambe le azioni come elementi distinti. Durante la modifica dell&#39;elemento è stato creato un nuovo elemento, contenente il testo modificato, che modifica l&#39;elemento originale creato. Se elimini l&#39;elemento originale, il testo modificato non sarà in grado di trovare l&#39;elemento modificato e non verrà visualizzato. Il secondo elemento rimarrà nell&#39;elenco senza tuttavia influire sulla pagina, poiché l&#39;elemento da modificare non esiste più.

Consulta [Selettori di elementi utilizzati nel Compositore esperienza visivo](../../c-experiences/c-visual-experience-composer/vec-selectors.md#concept_4EB7663E255F439B8D24079D23479337).

**Utilizza i tag`<b>`e`<i>`per la formattazione di elementi di testo con l’editor di testo RTF.**

* Per il testo in grassetto, utilizza `<b>` anziché `<strong>`.
* Per il testo in corsivo, utilizza `<i>` anziché `<em>`.

I tag `<strong>` e `<em>` potrebbero causare risultati imprevisti.

**Presta attenzione durante la rimozione dei campi modulo.**

Alcuni campi modulo potrebbero essere obbligatori per l&#39;invio. La loro eliminazione potrebbe influenzare gli invii.

**Non includere`mboxCreate`all’interno degli script.**

Poiché `mboxCreate` utilizza `document.write`, si sconsiglia di includere `mboxCreate` negli script. Per tale scopo, utilizza invece `mboxDefine` e `mboxUpdate`.

**Non aggiornare un frammento HTML utilizzando Target Standard se viene richiesto il codice JavaScript per l&#39;inizializzazione.**

Quando un&#39;azione (modifica HTML) viene eseguita sui componenti della pagina (come cursori, caroselli e così via), la distribuzione potrebbe non riuscire. Con il Compositore esperienza visivo è possibile eseguire l&#39;azione dopo la creazione di un&#39;istanza del componente della pagina da parte di JavaScript.

Tuttavia, quando il contenuto della pagina viene distribuito ai visitatori, l&#39;azione viene applicata prima di creare un&#39;istanza del componente. Per questo motivo, la funzionalità di questo componente rischia di interrompersi al momento della distribuzione. La funzionalità dipende dalla natura dello script utilizzato nella relativa pagina per definire il componente.

Se esegui il test della distribuzione ottenendo la prima volta un esito positivo, non è garantito che questa continuerà a funzionare. Può verificarsi una situazione di tipo “race condition”.

* Nel caso si verifichi una situazione di tipo “race condition”, la distribuzione funzionerà a intermittenza.
* In assenza di una situazione di tipo “race condition”, la distribuzione funzionerà sempre.

Sottoponi la tua pagina a test più volte per assicurarti che la distribuzione funzioni come previsto.

**Non utilizzare un tag di base nel sito web per risolvere URL e collegamenti.**

Quando utilizzi il Compositore esperienza avanzato, il sito web viene manipolato da dietro le quinte da un server proxy, che aggiorna tutti i collegamenti agli URL per farli funzionare nel proxy. Se aggiungi un tag di base, tutti questi URL vengono risolti dal browser e risulteranno interrotti.

**Il testo importante sul sito che può essere utilizzato per il targeting deve essere mantenuto nel codice HTML all&#39;interno di un elemento.**

Ad esempio, non è possibile indirizzare il testo del carrello acquisti nel Compositore di esperienza visiva se il codice è simile al seguente:

```
<a href="https://www.botanicchoice.com/shop.axd/Cart"> 
   <img alt="Shopping Cart"src="/images/ico-cart.gif"></img> 
   Shopping Cart: 
   <span id="HeaderCartQtyTotal">
      0 
  </span> 
  Items 
  <span id="HeaderCartPriceTotal"></span> 
</a>
```

In questo esempio, nel Compositore di esperienza visiva viene selezionato tutto l&#39;elemento di ancoraggio, che causa un&#39;influenza negativa su altri elementi in caso di esecuzione del targeting.

**Non utilizzare le variabili`top`o`self`nel codice JavaScript.**

Quando il Compositore esperienza avanzato è abilitato, il valore della parte superiore e delle variabili self vengono aggiornati per annullare la non compatibilità con iframe. Per aggiungere il busting iframe, utilizza un&#39;intestazione X-frame-options invece dei codici JavaScript personalizzati.

**Eseguire sempre il test del sito web all&#39;aggiunta di parametri al caricamento della pagina.**

Ad esempio, per aprire www.abc.com, vengono utilizzati i seguenti parametri URL:

`www.abc.com?mboxEdit=1&mboxDisable=1`

Questi parametri consentono la modifica in un iframe.

Assicurati che il tuo sito web carichi come previsto dopo l&#39;aggiunta di parametri simili.

**Assicurarsi che la pagina si apra come previsto in un iframe.**

Disattiva le tecniche di busting iframe sul sito web e verifica se questo si apre come previsto all&#39;interno di un iframe su una pagina fittizia. Ad esempio:

```
<!DOCTYPE 
<html> 
<html> 
<head> 
  <meta charset="utf-8"> 
  <meta name="viewport" content="width=device-width"> 
  <title>JS Bin</title> 
</head> 
<body> 
  <iframe src="https://www.homedepot.com"</iframe> 
</body> 
</html>
```

## Avvertenze {#section_A0436B7B85BA467FA9DE13A9A40E6A6E}

È necessario prestare attenzione alle seguenti avvertenze durante l&#39;utilizzo del Compositore esperienza visivo per la progettazione delle attività.

**La funzione Sposta non supporta la funzionalità z-index.**

In assenza della funzionalità z-index, l&#39;elemento spostato non può essere spostato sopra un altro elemento. Per ulteriori dettagli, vedi [Limitazioni](../../c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#section_F33C2EA27F2E417AA036BC199DD6C721).

**La ridisposizione degli elementi influenza il monitoraggio dei clic.**

Se ridisponi un elemento contrassegnato per il rilevamento di clic, i percorsi degli elementi ridisposti vengono modificati. Come risultato, verrà eseguito il monitoraggio dei clic per l&#39;elemento nella posizione in cui si trovava l&#39;elemento originale prima della ridisposizione.

Ciò si verifica perché sia il codice per distribuire il contenuto dell&#39;attività sia il codice per tenere traccia dei clic è incluso in un segmento di codice recapitato alla pagina. Se passi a una pagina diversa e imposti il rilevamento dei clic, il codice del contenuto dell&#39;attività e il codice di monitoraggio dei clic vengono recapitati a tale pagina. Se la pagina di rilevamento dei clic ha una struttura simile alla pagina in cui viene eseguito il test, il contenuto del test può anche essere visualizzato nella pagina di rilevamento dei clic.

**L’inserimento di un elemento potrebbe non funzionare in un`<div>`costituito da una mbox.**

Se nella mbox è contenuta un&#39;offerta e questa è implementata in modo errato, inserendo un elemento è possibile che venga visualizzato come insertBefore e non come insertAfter.

**Durante la modifica di un elemento padre e figlio, modificare innanzitutto il padre.**

È possibile riscontrare problemi nella distribuzione se scambi un&#39;azione immagine su un elemento e modifichi quindi il testo o l&#39;HTML sul relativo elemento padre. Il flusso di lavoro migliore consiste nel modificare l&#39;elemento padre prima di scambiare l&#39;immagine sull&#39;elemento figlio.

**Non è possibile selezionare un elemento di pagina che include una mbox come elemento figlio.**

Ad esempio, se nella pagina è incluso quanto segue:

```
<div> 
  <div class="mboxDefault" > 
  </div>
  <script>mboxCreate('myMbox'); 
</div>`
```

Il div esterno non deve essere selezionato in un&#39;esperienza, in quanto la mbox con valori prefissati nel codice della pagina continua a eseguire una chiamata a Target e a ricevere una risposta. Questa risposta interferisce con la risposta prevista per l&#39;elemento di pagina più grande.

**Gli IP proxy potrebbero essere bloccati negli ambienti cliente.**

Se utilizzi il Compositore esperienza avanzato su un sito non attivo, ad esempio un ambiente di pre-produzione, è possibile che vengano visualizzati timeout ed errori di accesso negato al blocco dei protocolli RIP da parte del sito.

**All&#39;aggiunta di più pagine, la barra dell&#39;esperienza e della pagina vengono aperte in contemporanea. In questo modo viene ridotta la larghezza del Compositore esperienza visivo per visualizzare il sito per le ottimizzazioni. Di conseguenza, nello spazio ridotto i siti fluidi potrebbero essere visualizzati in modo diverso rispetto a quanto previsto.**

La soluzione consiste nel comprimere la barra dell&#39;esperienza e della pagina facendo clic sulle icone con freccia sinistra nella parte superiore.

## Limitazioni {#section_F33C2EA27F2E417AA036BC199DD6C721}

**Funzione Sposta**

Un elemento non può essere spostato all&#39;esterno di un contenitore seguito da una proprietà CSS.

**Sulle mbox sono disponibili solo le offerte di sostituzione.**

Azioni come Modifica classe e Ridisponi non sono consentite all&#39;interno di una mbox. Il contenuto di una mbox viene distribuito da mbox.js.

**Evitare di ridisporre e spostare lo stesso elemento.**

Se hai spostato un elemento in un&#39;altra posizione e selezioni il contenitore padre cercando di ridisporre gli elementi figlio, l&#39;elemento spostato non viene interessato e rimane dove si trova. La ridisposizione potrebbe non essere visualizzata nel modo desiderato.

**L&#39;azione Sostituisci immagine non funziona su un&#39;immagine inclusa in un carosello.**

Ad esempio, se la pagina include un carosello con sei immagini e intendi sostituire un&#39;immagine alla seconda del carosello, l&#39;azione Sostituisci immagine non funzionerà.

La soluzione consiste nel selezionare il contenitore padre e utilizzare l&#39;azione Modifica HTML per modificare l&#39;HTML del carosello, al fine di aggiornare l&#39;origine dell&#39;immagine desiderata.

**Le immagini non possono essere ridimensionate in una mbox.**

Se sostituisci un&#39;immagine in un elemento mbox e tenti quindi di ridimensionarla in base alle dimensioni dell&#39;elemento mbox, l&#39;azione non sarà consentita.

**Dopo la sostituzione di un&#39;immagine, non puoi selezionare l&#39;azione Modifica.**

Dopo la sostituzione dell&#39;immagine, non puoi modificare l&#39;URL di Scene7.

**Non è possibile modificare gli elementi HTML con origine esterna.**

Ad esempio: video, tag audio, elementi incorporati, iFrame, frame.

**Il monitoraggio dei clic non funziona per gli elementi di ancoraggio che contengono elementi diversi dai tag di testo normale o immagine.**

Ad esempio, il monitoraggio dei clic non funziona se l&#39;elemento contiene JavaScript.

**Per far sì che il Compositore esperienza visivo funzioni, le pagine devono accettare i parametri URL.**

Alcuni siti rimuovono tutti i parametri URL per le loro pagine. Tuttavia, tali parametri sono necessari per il Compositore esperienza visivo.

**Durante l&#39;utilizzo di uno script come parte di HTML, tutte le variabili e le funzioni a cui si accede dall&#39;esterno devono essere dichiarate nello spazio dei nomi della finestra.**

Lo script viene eseguito all&#39;interno dell&#39;ambito di target.js dopo il caricamento della pagina. Pertanto, qualsiasi variabile o funzione dichiarata localmente non è accessibile dall&#39;esterno del blocco di script.

*Errato:*

```
<script> 
  var myVar = 123; 
  function myFunc() { 
    // 
  } 
</script>`
```

*Corretto:*

```
<script> 
  window.myVar = 123; 
  window.myFunc = function() { 
    // 
  }; 
</script>
```

**L&#39;inserimento di un&#39;immagine dalla libreria del contenuto (Scene7) e la modifica del codice HTML causano l&#39;interruzione dell&#39;URL dell&#39;immagine.**

Aggiungi un elemento di ancoraggio all&#39;interno del tag div &#39;customHeaderMessage&#39; con un testo fittizio:

```
<a href="#"> 
<span> Dummy text </span>
</a>
```

Seleziona questo tag div utilizzando l&#39;azione Inserisci elemento per inserire un&#39;immagine di pari livello di questo tag div con testo fittizio.

Dopo l&#39;inserimento dell&#39;immagine, verrà visualizzato in questo modo:

```
<a href="#">  
<span> Dummy text </span> 
<img src=""> This is inserted Image. </img> 
</a>
```

Rimuovi l&#39;intervallo di testo fittizio.

**L&#39;azione customCode del Compositore esperienza visivo non è compatibile con Internet Explorer 8.**

A causa delle limitazioni di Internet Explorer 8 relative alla gestione del contenuto dello script, target.js non ne garantisce il supporto per Internet Explorer 8. Come soluzione, se la pagina contiene jQuery ed è esposta sull&#39;oggetto finestra a livello globale, con target.js è possibile utilizzare l&#39;azione per distribuire il codice personalizzato (customCode). Assicurati di aver definito window.jQuery e window.jQuery.fn.prepend.

**Il monitoraggio dei clic è supportato solo nella pagina in cui vengono create le esperienze o nella pagina reindirizzata.**

Sebbene la modalità Sfoglia sia disponibile nel monitoraggio dei clic del Compositore di esperienza visiva, non può essere usata per aggiungere il monitoraggio dei clic su una pagina.
