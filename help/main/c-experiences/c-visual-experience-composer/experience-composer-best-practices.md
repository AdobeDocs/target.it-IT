---
keywords: compositore esperienza visivo;best practice compositore esperienza visivo;limitazioni compositore esperienza visivo;avvertenze compositore esperienza visivo;procedure ottimali compositore esperienza visivo;vec
description: Scopri le best practice per fare in modo che le tue esperienze funzionino come previsto quando utilizzi il [!UICONTROL Compositore esperienza visivo].
title: Quali sono le [!UICONTROL best practice e limitazioni del Compositore esperienza visivo]?
feature: Visual Experience Composer (VEC)
exl-id: cf51bfec-d7fa-4ec1-a5dc-35edefefd3e4
TQID: https://experienceleague.adobe.com/upZDSyuS9VqUmYskNXrlYazhwRHmZGBpSR-cR-qliRs
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: c93393a4-e558-47e1-992e-c91ed4d480ce
subfeature_v2: id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: c1579802-ddd4-4214-8a91-97b2066abe11id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 2552
ht-degree: 49%

---

# [!UICONTROL Best practice e limitazioni del Compositore esperienza visivo]

Per garantire che le esperienze funzionino come previsto, segui le best practice durante l&#39;utilizzo del [!DNL Adobe Target] [!UICONTROL Compositore esperienza visivo]. Presta attenzione a suggerimenti e limitazioni chiave per massimizzare le prestazioni ed evitare problemi comuni.

## Best practice {#section_86CF28C99CFF40329E4CBAFE4DD78BB4}

Di seguito sono riportate le best practice per l’utilizzo del Compositore esperienza visivo:

### Posiziona il riferimento at.js nella parte superiore della sezione `<head>` della pagina.

+++Vedi i dettagli
Se utilizzi anche il [!UICONTROL servizio API visitatore], inserisci lo script dell&#39;API visitatore sopra at.js.

+++

### Puoi abilitare il [!UICONTROL Compositore esperienza avanzato] a livello di account (abilitato per tutte le attività create nell’account) o a livello della singola attività.

+++Vedi i dettagli
Per abilitare il [!UICONTROL Compositore esperienza avanzato] a livello di account, fai clic su [!UICONTROL [!UICONTROL Amministrazione] > [!UICONTROL Compositore esperienza visivo]], quindi attiva il pulsante [!UICONTROL Abilita Compositore esperienza avanzato].

Per abilitare il [!UICONTROL Compositore esperienza avanzato] a livello di attività durante la creazione di un&#39;attività nel [!UICONTROL Compositore esperienza visivo], fai clic su [!UICONTROL Configura > [!UICONTROL Consegna pagine]], quindi attiva il pulsante [!UICONTROL Abilita Compositore esperienza avanzato].

+++

### Puoi determinati indirizzi IP se il [!UICONTROL Compositore esperienza avanzato] non si carica su pagine protette del tuo sito.

+++Vedi i dettagli
I problemi relativi al caricamento di [!UICONTROL Compositore esperienza avanzato] possono essere risolti inserendo nell&#39;elenco Consentiti i seguenti indirizzi IP. Questi indirizzi IP sono per i server [!DNL Adobe] utilizzati per il proxy [!UICONTROL Compositore esperienza avanzato]. Sono necessari solo per modificare le attività. I visitatori del tuo sito non hanno bisogno di inserire nell&#39;elenco Consentiti questi indirizzi IP.

Per ulteriori informazioni, vedere [Il Compositore esperienza avanzato non carica un URL di controllo qualità interno che non è accessibile nell&#39;IP pubblico](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshooting-issues-related-to-the-enhanced-experience-composer-eec.md) in *Risoluzione dei problemi relativi al Compositore esperienza avanzato*.

+++

### Utilizzare ID univoci per gli elementi di primo livello e per tutti gli altri elementi candidati ad attività di test o targeting.

+++Dettagli
Qualsiasi elemento interno all&#39;elemento corpo deve presentare un ID univoco. Nel caso nuovi elementi vengano inseriti nel corpo e il codice cambi posizione, sarà possibile riconoscere con maggiore facilità almeno gli elementi padre.

[!DNL Target] non richiede ID, ma l&#39;utilizzo degli ID aumenta l&#39;affidabilità delle esperienze create con il Compositore esperienza. [!DNL Target] utilizza i selettori CSS per modificare il contenuto quando viene distribuita l&#39;esperienza. Quando si modifica un&#39;esperienza, il [!UICONTROL Compositore esperienza visivo] ancora il selettore al predecessore più vicino con un attributo ID non nullo all&#39;elemento HTML che si sta modificando. Di conseguenza si consiglia di non utilizzare meccanismi, comprese librerie JavaScript, che impostino o modifichino gli attributi ID HTML. Anche se tali ID potrebbero essere disponibili per il Compositore esperienza [!DNL Target] per la creazione di attività, se JavaScript modifica gli ID, l&#39;ID utilizzato al momento della creazione dell&#39;esperienza potrebbe non essere disponibile durante l&#39;esecuzione dell&#39;esperienza. Se l&#39;ID non è disponibile, l&#39;ancoraggio del selettore all&#39;ID avrà esito negativo.

+++

### Denominare le classi CSS in modo che siano facilmente identificabili.

+++Dettagli
Quando si modificano le classi CSS in [!DNL Visual Experience Composer], è utile semplificare l&#39;identificazione delle classi utilizzando nomi descrittivi di classi. Questa operazione assicura che vengano modificate le classi CSS corrette e che le pagine vengano visualizzate come previsto.

Non utilizzare la proprietà CSS `!important` quando nascondi o rimuovi elementi.

Se la proprietà CSS `!important` è presente, le modifiche apportate da `target.js` durante la consegna vengono ignorate dalle regole CSS del sito.

+++

### Evitare l&#39;uso di tabelle HTML per i layout di pagina.

+++Dettagli
[!DNL Target] utilizza JavaScript per formattare una pagina. La modifica dei layout basati su tabelle con JavaScript risulta difficoltosa. Inoltre, i layout basati su tabelle potrebbero non essere visualizzati allo stesso modo in tutti i browser. Per ottenere i risultati ottimali, crea i layout di pagina con CSS.

+++

### Ridurre al minimo l&#39;utilizzo di iFrame.

+++Dettagli
Ridurre al minimo l&#39;uso di iFrame è una buona tecnica per semplificare la gestione delle pagine e dei test. Il Compositore esperienza visivo può applicare alcune azioni all’interno di un iFrame, ma alcune, come il ridimensionamento, non funzionano correttamente. Gestire e ridimensionare le pagine che utilizzano più iFrame risulta difficoltoso. Come risultato, il test delle pagine con molti elementi iFrame potrebbe creare problemi.

+++

### Dopo la preparazione di DOM, cerca di apportare tutte le modifiche DOM dinamiche il prima possibile.

+++Dettagli
Se le modifiche non vengono applicate prima dell&#39;applicazione di esperienza da `target.js`, la consegna del contenuto potrebbe essere interrotta. Questo avviene solo in caso di modifica DOM nella gerarchia di un elemento con targeting.

+++

### Utilizzare solo un tag testo normale o immagine negli elementi di ancoraggio.

+++Dettagli
`<a>Anchor Text</a>`

O

`<a href=""> <img src=""> </img> </a>`

+++

### Evitare elementi a livello di blocco all&#39;interno di un elemento in linea.

+++Dettagli
Gli elementi a livello di blocco non devono essere utilizzati all’interno di elementi in linea, ad esempio ancoraggio, estensione e così via. In questo modo gli elementi in linea perderanno altezza e larghezza, pertanto lo strumento di sovrapposizione nel [!UICONTROL Compositore esperienza visivo] potrebbe non funzionare come previsto.

+++

### Non utilizzare il tag di base nel sito web per risolvere URL e collegamenti.

+++Dettagli
Il Compositore esperienza visivo manipola il sito web dietro le quinte utilizzando un server proxy che aggiorna i collegamenti. Se aggiungi un tag di base, gli URL utilizzati dal server proxy verranno risolti nuovamente dal browser e risulteranno interrotti.

+++

### Modificare l&#39;HTML per manipolare la struttura DOM può interrompere i selettori.

+++Dettagli
Ad esempio, supponiamo che tu abbia eseguito due azioni:

* Aggiunta di una classe all&#39;elemento 1
* Modifica del codice HTML dell&#39;elemento 1

Ogni modifica crea un nuovo elemento nel Compositore esperienza visivo. La seconda azione modifica l&#39;elemento 1: se lo elimini, la seconda azione non avrà più niente da modificare, risultando nella mancata applicazione della modifica.

In altre parole, se aggiungi un elemento con testo e modifichi tale elemento con un testo diverso in un&#39;azione separata, l&#39;editor di codice mostrerà entrambe le azioni come elementi distinti. Durante la modifica dell&#39;elemento è stato creato un nuovo elemento, contenente il testo modificato, che modifica l&#39;elemento originale creato. Se elimini l&#39;elemento originale, il testo modificato non sarà in grado di trovare l&#39;elemento modificato e non verrà visualizzato. Il secondo elemento rimarrà nell&#39;elenco senza tuttavia influire sulla pagina, poiché l&#39;elemento da modificare non esiste più.

Consulta [Selettori di elementi utilizzati nel [!UICONTROL Compositore esperienza visivo]](/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md#concept_4EB7663E255F439B8D24079D23479337).

+++

### Utilizza i tag `<b>` e `<i>` per la formattazione di elementi di testo con l&#39;editor Rich Text.

+++Dettagli
* Per il testo in grassetto, utilizza `<b>` anziché `<strong>`.
* Per il testo in corsivo, utilizza `<i>` anziché `<em>`.

I tag `<strong>` e `<em>` potrebbero causare risultati imprevisti.

+++

### Presta attenzione durante la rimozione dei campi modulo.

+++Dettagli
Alcuni campi modulo potrebbero essere obbligatori per l&#39;invio. La loro eliminazione potrebbe influenzare gli invii.

+++

### Non includere `mboxCreate` all&#39;interno degli script.

+++Dettagli
Poiché `mboxCreate` utilizza `document.write`, si sconsiglia di includere `mboxCreate` negli script. Per tale scopo, utilizza invece `mboxDefine` e `mboxUpdate`.

+++

### Non aggiornare un frammento di codice HTML utilizzando [!DNL Target] se è necessario il codice JavaScript per l&#39;inizializzazione.


+++Dettagli
Quando si esegue un’azione (Modifica HTML) sui componenti della pagina (come cursori, caroselli e così via), la consegna potrebbe apparire interrotta. Il Compositore esperienza visivo esegue l’azione dopo che il componente Pagina è stato creato da JavaScript.

Tuttavia, quando il contenuto della pagina viene distribuito ai visitatori, l&#39;azione viene applicata prima di creare un&#39;istanza del componente. Per questo motivo, la funzionalità di questo componente rischia di interrompersi al momento della distribuzione. La funzionalità dipende dalla natura dello script utilizzato nella relativa pagina per definire il componente.

Se esegui il test della distribuzione ottenendo la prima volta un esito positivo, non è garantito che questa continuerà a funzionare. Può verificarsi una situazione di tipo “race condition”.

* In presenza di una situazione di tipo &quot;race condition&quot;, la consegna funziona a intermittenza.
* Se non c’è una situazione di tipo &quot;race condition&quot;, la consegna funziona sempre.

Sottoponi la tua pagina a test più volte per assicurarti che la distribuzione funzioni come previsto.

+++

### Non utilizzare un tag di base nel sito web per risolvere URL e collegamenti.

+++Dettagli
Quando si utilizza il [!UICONTROL Compositore esperienza avanzato], il sito Web viene manipolato dietro le quinte da un server proxy che aggiorna tutti gli URL di collegamento in modo che funzionino nel proxy. Se aggiungi un tag di base, tutti questi URL vengono risolti dal browser, in modo che risultino interrotti.

+++

### Il testo importante sul sito che può essere utilizzato per il targeting deve essere mantenuto nel codice HTML all&#39;interno di un elemento.

+++Dettagli
Ad esempio, non è possibile indirizzare il testo del carrello acquisti nel Compositore di esperienza visiva se il codice è simile al seguente:

```html
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

In questo esempio, nel Compositore esperienza visivo viene selezionato l’intero elemento di ancoraggio, che ha effetti negativi su altri elementi se viene eseguito il targeting.

+++

### Non utilizzare `top` o `self` variabili nel codice JavaScript.

+++Dettagli
Quando il [!UICONTROL Compositore esperienza avanzato] è abilitato, il valore della parte superiore e delle variabili self vengono aggiornati per disabilitare la non compatibilità con iframe. Per aggiungere il busting iframe, utilizza un&#39;intestazione X-frame-options invece dei codici JavaScript personalizzati.

+++

### Eseguire sempre il test del sito web all&#39;aggiunta di parametri al caricamento della pagina.

+++Dettagli
Ad esempio, per aprire `www.abc.com`, vengono utilizzati i seguenti parametri URL:

`www.abc.com?mboxEdit=1&mboxDisable=1`

Questi parametri consentono la modifica in un iframe.

Assicurati che il tuo sito web carichi come previsto dopo l&#39;aggiunta di parametri simili.

+++

### Assicurarsi che la pagina si apra come previsto in un iframe.

+++Dettagli
Disattiva le tecniche di busting iframe sul sito web e verifica se il sito web si apre come previsto all’interno di un iframe in una pagina fittizia. Ad esempio:

```html
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

+++

## Avvertenze {#section_A0436B7B85BA467FA9DE13A9A40E6A6E}

Quando utilizzi il [!UICONTROL Compositore esperienza visivo] per progettare l&#39;attività, considera le seguenti avvertenze.

### La funzionalità [!UICONTROL Sposta] non supporta la funzionalità z-index.

+++Dettagli
In assenza della funzionalità z-index, l&#39;elemento spostato non può essere spostato sopra un altro elemento. Per ulteriori dettagli, vedi [Limitazioni](/help/main/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#section_F33C2EA27F2E417AA036BC199DD6C721).

+++

### La ridisposizione degli elementi influenza il monitoraggio dei clic.

+++Dettagli
Se ridisponi un elemento contrassegnato per il rilevamento di clic, i percorsi degli elementi ridisposti vengono modificati. Come risultato, verrà eseguito il monitoraggio dei clic per l&#39;elemento nella posizione in cui si trovava l&#39;elemento originale prima della ridisposizione.

Ciò si verifica perché sia il codice per distribuire il contenuto dell&#39;attività sia il codice per tenere traccia dei clic è incluso in un segmento di codice recapitato alla pagina. Se passi a una pagina diversa e imposti il rilevamento dei clic, il codice del contenuto dell&#39;attività e il codice di monitoraggio dei clic vengono recapitati a tale pagina. Se la pagina di rilevamento dei clic ha una struttura simile alla pagina in cui viene eseguito il test, il contenuto del test può anche essere visualizzato nella pagina di rilevamento dei clic.

+++

### L&#39;inserimento di un elemento potrebbe non funzionare in un `<div>` che è una mbox.

+++Dettagli
Se una mbox contiene un&#39;offerta, l&#39;inserimento di un elemento potrebbe apparire come `insertBefore` e non come `insertAfter`, nel caso in cui la mbox non sia implementata correttamente.

+++

### Durante la modifica di un elemento padre e figlio, modificare innanzitutto il padre.

+++Dettagli
È possibile riscontrare problemi nella distribuzione se scambi un&#39;azione immagine su un elemento e modifichi quindi il testo o l&#39;HTML sul relativo elemento padre. Il flusso di lavoro migliore consiste nel modificare l&#39;elemento padre prima di scambiare l&#39;immagine sull&#39;elemento figlio.

+++

### Non è possibile selezionare un elemento di pagina che include una mbox come elemento figlio.

+++Dettagli
Ad esempio, se nella pagina è incluso quanto segue:

```html
<div> 
  <div class="mboxDefault" > 
  </div>
  <script>mboxCreate('myMbox'); 
</div>`
```

Il div esterno non deve essere selezionato in un&#39;esperienza perché la mbox codificata nella pagina effettua ancora una chiamata a [!DNL Target] e riceve una risposta. Questa risposta interferisce con la risposta prevista per l&#39;elemento di pagina più grande.

+++

### Gli IP proxy potrebbero essere bloccati negli ambienti cliente.

+++Dettagli
Se si utilizza [!UICONTROL Compositore esperienza avanzato] in un sito non attivo, ad esempio un ambiente di gestione temporanea, è possibile che vengano visualizzati timeout ed errori di accesso negato se il sito blocca i RIP.

+++

## Limitazioni {#section_F33C2EA27F2E417AA036BC199DD6C721}

Quando lavori con il Compositore esperienza visivo, tieni presente le seguenti limitazioni:

### Gestione della compatibilità del Compositore esperienza visivo con [!DNL Chrome] modifiche ai criteri di estensione. {#ext}

+++Dettagli
A causa dei criteri aggiornati del manifesto [V3 in Google Chrome](https://developer.chrome.com/docs/extensions/develop/migrate/what-is-mv3){target=_blank}, le estensioni non possono più modificare il DOM originale prima che venga analizzato dal browser. Di conseguenza, alcuni script di sicurezza, come le implementazioni non compatibili con iframe, potrebbero bloccare il caricamento delle pagine nel Compositore esperienza visivo.

Per garantire la compatibilità, questi script devono essere disabilitati in modo condizionale quando la pagina viene caricata nell&#39;iframe [!DNL Target]. Questo processo può essere eseguito senza problemi verificando la presenza dell&#39;oggetto `window.adobeVecExtension`, inserito da [!DNL Target] durante il caricamento del Compositore esperienza visivo.

I seguenti snippet di codice sono esempi di codice non compatibile con iframe che possono impedire il caricamento della pagina web nel Compositore esperienza visivo:

`window.top.location = window.self.location;`

`top.location.href = self.location.href;`

È possibile utilizzare un semplice controllo per verificare se una pagina Web è incorporata in [!DNL Target]. Un frammento di codice deve essere simile al seguente:

```
if(!window.adobeVecExtension) {
    // additional security logic
}
```

+++

### Non puoi spostare un elemento all’esterno di un contenitore seguito da una proprietà CSS.

+++Dettagli
Un elemento non può essere spostato all&#39;esterno di un contenitore seguito da una proprietà CSS.

+++

### Impossibile selezionare l&#39;elemento [!UICONTROL Button] per la ridisposizione.

+++Dettagli
Impossibile selezionare direttamente gli elementi [!UICONTROL Button] per la ridisposizione. Per abilitare la ridisposizione, posizionare i pulsanti all&#39;interno di un contenitore più grande.

+++

### Sulle mbox sono disponibili solo le offerte di sostituzione.

+++Dettagli
Azioni quali [!UICONTROL Modifica classe] e [!UICONTROL Ridisponi] non sono consentite all&#39;interno di una mbox.

+++

### Evitare di ridisporre e spostare lo stesso elemento.

+++Dettagli
Se hai spostato un elemento in un&#39;altra posizione e selezioni il contenitore padre cercando di ridisporre gli elementi figlio, l&#39;elemento spostato non viene interessato e rimane dove si trova. La ridisposizione potrebbe non essere visualizzata nel modo desiderato.

+++

### L&#39;azione [!UICONTROL Modifica immagine] non funziona su un&#39;immagine in un carosello.

+++Dettagli
Se, ad esempio, la pagina contiene un carosello con sei immagini e si desidera scambiare un&#39;immagine con la seconda immagine del carosello, l&#39;azione [!UICONTROL Modifica immagine] non funziona.

La soluzione consiste nel selezionare il contenitore principale e utilizzare l&#39;azione [!UICONTROL Modifica HTML] per modificare il HTML del carosello e aggiornare l&#39;origine immagine dell&#39;immagine desiderata.

+++

### Le immagini non possono essere ridimensionate in una mbox.

+++Dettagli
Se sostituisci un&#39;immagine in un elemento mbox e tenti quindi di ridimensionarla in base alle dimensioni dell&#39;elemento mbox, l&#39;azione non sarà consentita.

+++

### Dopo la sostituzione di un&#39;immagine, non è possibile selezionare l&#39;azione [!UICONTROL Modifica].

+++Dettagli
Dopo la sostituzione dell&#39;immagine, non puoi modificare l&#39;URL di Scene7.

+++

### Non è possibile modificare gli elementi HTML con un’origine esterna.

+++Dettagli
Ad esempio: video, tag audio, elementi incorporati, iFrame, frame.

+++

### Il monitoraggio dei clic non funziona per gli elementi di ancoraggio che contengono elementi diversi dai tag di testo normale o immagine.

+++Dettagli
Ad esempio, il monitoraggio dei clic non funziona se l&#39;elemento contiene JavaScript.

+++

### Affinché il Compositore esperienza visivo funzioni, le pagine devono accettare i parametri URL.

+++Dettagli
Alcuni siti rimuovono tutti i parametri URL per le loro pagine. Tuttavia, il Compositore esperienza visivo richiede tali parametri.

+++

### Durante l’utilizzo di uno script come parte di HTML, tutte le variabili e le funzioni a cui si accede dall’esterno devono essere dichiarate nello spazio dei nomi della finestra.

+++Dettagli
Lo script viene eseguito nell&#39;ambito di `target.js` dopo il caricamento della pagina. Pertanto, qualsiasi variabile o funzione dichiarata localmente non è accessibile dall&#39;esterno del blocco di script.

*Errato:*

```html
<script> 
  var myVar = 123; 
  function myFunc() { 
    // 
  } 
</script>`
```

*Corretto:*

```html
<script> 
  window.myVar = 123; 
  window.myFunc = function() { 
    // 
  }; 
</script>
```

+++

### L&#39;inserimento di un&#39;immagine dalla libreria [!UICONTROL Content] (Scene7) e la modifica del HTML interrompono l&#39;URL dell&#39;immagine.

+++Dettagli
Aggiungi un elemento di ancoraggio all&#39;interno del tag div &#39;customHeaderMessage&#39; con un testo fittizio:

```html
<a href="#"> 
<span> Dummy text </span>
</a>
```

Selezionare questo div utilizzando l&#39;azione [!UICONTROL Inserisci elemento] per inserire un&#39;immagine di pari livello di questo div di testo fittizio.

Dopo l&#39;inserimento dell&#39;immagine, verrà visualizzato in questo modo:

```html
<a href="#">  
<span> Dummy text </span> 
<img src=""> This is inserted Image. </img> 
</a>
```

Rimuovi l&#39;intervallo di testo fittizio.

+++

### L&#39;azione `customCode` nel Compositore esperienza visivo non funziona con [!DNL Internet Explorer] 8.

+++Dettagli
A causa delle limitazioni di Internet Explorer 8 relative alla gestione del contenuto dello script, `target.js` non supporta questa funzionalità in Internet Explorer 8. Come soluzione alternativa, se la pagina contiene jQuery ed è esposta sull&#39;oggetto finestra a livello globale, `target.js` può utilizzare l&#39;azione di consegna `customCode`. Assicurarsi che `window.jQuery` e `window.jQuery.fn.prepend` siano definiti.

+++

### Il monitoraggio dei clic è supportato solo nella pagina in cui vengono create le esperienze o nella pagina reindirizzata.

+++Dettagli
Sebbene la modalità [!UICONTROL Sfoglia] sia disponibile per il tracciamento dei clic nel Compositore esperienza visivo, non è possibile utilizzare la modalità [!UICONTROL Sfoglia] per aggiungere il tracciamento dei clic in una pagina.

+++
