---
keywords: compositore esperienza visivo;best practice compositore esperienza visivo;limitazioni compositore esperienza visivo;avvertenze compositore esperienza visivo;procedure ottimali compositore esperienza visivo;vec
description: Scopri le best practice per fare in modo che le tue esperienze funzionino come previsto quando utilizzi il [!UICONTROL Compositore esperienza visivo].
title: Quali sono le [!UICONTROL best practice e limitazioni del Compositore esperienza visivo]?
feature: Visual Experience Composer (VEC)
exl-id: cf51bfec-d7fa-4ec1-a5dc-35edefefd3e4
TQID: 'https://experienceleague.adobe.com/upZDSyuS9VqUmYskNXrlYazhwRHmZGBpSR-cR-qliRs'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
subfeature_v2:
  - id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
    internal-label: at.js
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '2420'
ht-degree: 8%
---
# [!UICONTROL Best practice e limitazioni del Compositore esperienza visivo] {#vec-best-practices}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri le best practice, le avvertenze e le limitazioni da considerare durante la creazione di esperienze nel **[!UICONTROL Compositore esperienza visivo]**.

>[!ENDSHADEBOX]

Seguire queste procedure aiuta le esperienze create nella funzione [!DNL Adobe Target] **[!UICONTROL Compositore esperienza visivo]** come previsto. Le avvertenze e le limitazioni descrivono i comportamenti che possono causare problemi comuni, pertanto la loro conoscenza aiuta a evitare i problemi e a mantenere le prestazioni.

## Best practice {#best-practices}

Le seguenti procedure si applicano quando si utilizza il Compositore esperienza visivo.

### Abilita [!UICONTROL Compositore esperienza avanzato] {#enable-eec}

Il **[!UICONTROL Compositore esperienza avanzato]** può essere abilitato a livello di account, che lo abilita per tutte le attività create nell&#39;account o a livello della singola attività.

* **Livello account:** Fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Compositore esperienza visivo]**, quindi attiva il pulsante **[!UICONTROL Abilita Compositore esperienza avanzato]**.
* **Livello di attività:** Durante la creazione di un&#39;attività nel **[!UICONTROL Compositore esperienza visivo]**, fai clic su **[!UICONTROL Configura]** > **[!UICONTROL Consegna pagine]**, quindi attiva il passaggio **[!UICONTROL Abilita Compositore esperienza avanzato]**.

### Impostazione e caricamento della pagina

+++ Inserisci il riferimento at.js nella parte superiore della sezione `<head>` della pagina.

Se viene utilizzato anche il **[!UICONTROL servizio API visitatore]**, inserisci lo script dell&#39;API visitatore sopra at.js.

+++

+++ Inserire nell&#39;elenco Consentiti indirizzi IP se [!UICONTROL Compositore esperienza avanzato] non viene caricato su pagine protette del sito.

La Inserire nell&#39;elenco Consentiti degli indirizzi IP dei server [!DNL Adobe] utilizzati per il proxy **[!UICONTROL Compositore esperienza avanzato]** risolve i problemi di caricamento. Questi indirizzi IP sono necessari solo per la modifica delle attività. I visitatori del sito non hanno bisogno che vengano inseriti nell&#39;elenco Consentiti. Gli indirizzi IP sono elencati in [Il Compositore esperienza avanzato non caricherà un URL di controllo qualità interno che non sia accessibile sull&#39;IP pubblico](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshooting-issues-related-to-the-enhanced-experience-composer-eec.md#eec-ip-addresses) in *Risoluzione dei problemi relativi al Compositore esperienza avanzato*.

+++

+++ Non utilizzare il tag di base nel sito web per risolvere URL e collegamenti.

Il Compositore esperienza visivo, incluso il **[!UICONTROL Compositore esperienza avanzato]**, manipola il sito Web dietro le quinte tramite un server proxy che aggiorna tutti gli URL di collegamento per farli funzionare nel proxy. Se viene aggiunto un tag di base, il browser risolve nuovamente questi URL, che appaiono interrotti.

+++

+++ Non utilizzare le variabili `top` o `self` nel codice JavaScript.

Quando il Compositore esperienza avanzato **[!UICONTROL è abilitato]**, i valori delle variabili `top` e `self` vengono aggiornati per disabilitare la non compatibilità con iframe. Utilizza un’intestazione X-Frame-Options per aggiungere busting iframe invece di un codice JavaScript personalizzato.

+++

+++ Esegui sempre il test del sito web se vengono aggiunti parametri al caricamento della pagina.

Ad esempio, i seguenti parametri URL vengono utilizzati per aprire `www.abc.com` per la modifica in un iframe:

`www.abc.com?mboxEdit=1&mboxDisable=1`

Assicurati che il sito web venga caricato come previsto dopo l’aggiunta di parametri come questi.

+++

+++ Assicurati che la pagina si apra come previsto in un iframe.

Disattiva le tecniche di busting iframe sul sito web e controlla se il sito web si apre come previsto in un iframe su una pagina fittizia. Ad esempio:

```html
<!DOCTYPE html>
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

### Markup pagina

+++ Utilizza ID univoci per gli elementi di primo livello e per tutti gli altri elementi candidati ad attività di test o targeting.

Qualsiasi elemento all’interno dell’elemento body deve avere un ID univoco, in modo che almeno gli elementi principali siano facili da riconoscere quando nuovi elementi vengono inseriti nel corpo e il codice si sposta.

[!DNL Target] non richiede ID, ma gli ID aumentano l&#39;affidabilità delle esperienze create con il Compositore esperienza. [!DNL Target] utilizza i selettori CSS per modificare il contenuto quando viene distribuita l&#39;esperienza. Quando si modifica un&#39;esperienza, il **[!UICONTROL Compositore esperienza visivo]** ancora il selettore al predecessore più vicino dell&#39;elemento HTML modificato con un attributo ID non null. Non è pertanto consigliabile utilizzare meccanismi, incluse le librerie JavaScript, che impostino o modifichino gli attributi HTML ID. Questi ID potrebbero essere disponibili per il Compositore esperienza al momento della creazione dell&#39;attività, ma se JavaScript li modifica, l&#39;ID utilizzato al momento della creazione potrebbe non essere disponibile durante l&#39;esecuzione dell&#39;esperienza. Se un ID non è disponibile, il selettore ancorato a tale ID ha esito negativo.

+++

+++ Utilizza nomi descrittivi di classi CSS.

I nomi descrittivi delle classi consentono di identificare facilmente le classi quando vengono modificate classi CSS nel **[!UICONTROL Compositore esperienza visivo]**. In questo modo è possibile garantire che le classi CSS corrette vengano modificate e che le pagine vengano visualizzate come previsto.

+++

+++ Non utilizzare la proprietà CSS `!important` quando si nascondono o si rimuovono elementi.

Se la proprietà CSS `!important` è presente, le regole CSS del sito sovrascrivono le modifiche apportate da `target.js` durante la distribuzione.

+++

+++ Evita tabelle HTML per layout di pagina.

[!DNL Target] utilizza JavaScript per formattare una pagina e i layout basati su tabelle sono difficili da modificare con JavaScript. Inoltre, i layout basati su tabelle potrebbero non essere visualizzati nello stesso modo in tutti i browser. Per ottenere i risultati ottimali, crea i layout di pagina con CSS.

+++

+++ Ridurre al minimo l&#39;utilizzo di iFrame.

La riduzione a icona di iFrame semplifica la gestione delle pagine e dei test. Il **[!UICONTROL Compositore esperienza visivo]** può applicare alcune azioni all&#39;interno di un iFrame, ma alcune, ad esempio il ridimensionamento, non funzionano correttamente. Le pagine che utilizzano più iFrame sono difficili da gestire e ridimensionare, pertanto il test di pagine iFrame-pesanti può creare problemi.

+++

+++ Utilizza solo un tag testo normale o immagine negli elementi di ancoraggio.

Un elemento di ancoraggio contiene testo normale:

`<a>Anchor Text</a>`

o un tag immagine:

`<a href=""> <img src=""> </img> </a>`

+++

+++ Evitare elementi a livello di blocco all&#39;interno di un elemento in linea.

Gli elementi a livello di blocco non devono essere utilizzati all’interno di elementi in linea, ad esempio elementi di ancoraggio e estensione. In questo modo gli elementi in linea perderanno altezza e larghezza, pertanto lo strumento di sovrapposizione nel **[!UICONTROL Compositore esperienza visivo]** potrebbe non funzionare come previsto.

+++

+++ Presta attenzione durante la rimozione dei campi modulo.

Alcuni campi modulo potrebbero essere obbligatori per l’invio, pertanto la loro rimozione potrebbe influire sugli invii.

+++

+++ Mantieni all’interno di un elemento il testo importante che potrebbe essere utilizzato per il targeting nel codice HTML.

Ad esempio, non è possibile eseguire il targeting del testo del carrello nel Compositore esperienza visivo se il codice è simile al seguente:

```html
<a href="https://www.botanicchoice.com/shop.axd/Cart">
   <img alt="Shopping Cart" src="/images/ico-cart.gif"></img>
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

### Modifica e consegna

+++ Dopo la preparazione di DOM, disponi tutte le modifiche DOM dinamiche il prima possibile.

Se le modifiche non vengono applicate prima che `target.js` applichi l&#39;esperienza, la distribuzione del contenuto potrebbe essere interrotta. Questo avviene solo in caso di modifica DOM nella gerarchia di un elemento con targeting.

+++

+++ Modifica HTML per manipolare la struttura DOM può interrompere i selettori.

Ad esempio, vengono eseguite due azioni:

* All&#39;elemento 1 viene aggiunta una classe.
* Viene modificato il HTML dell’elemento 1.

Ogni modifica crea un nuovo elemento nel Compositore esperienza visivo. La seconda azione modifica l’elemento 1, quindi se l’elemento 1 viene eliminato, la seconda azione non ha più nulla da modificare e la modifica non funziona più.

Allo stesso modo, se un elemento viene aggiunto con del testo e un’azione separata modifica tale elemento con del testo diverso, l’editor di codice mostra entrambe le azioni come elementi separati. La modifica crea un nuovo elemento che modifica quello originale e contiene il testo modificato. Se l’elemento originale viene quindi eliminato, il testo modificato non riesce a trovare l’elemento da modificare e non viene visualizzato. Il secondo elemento rimane nell’elenco degli elementi, ma non ha alcun effetto sulla pagina perché l’elemento che modifica non esiste più.

Consulta [Selettori di elementi utilizzati nel **[!UICONTROL Compositore esperienza visivo]**](/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md#vec-selectors).

+++

+++ Utilizza i tag `<b>` e `<i>` per la formattazione di elementi di testo con l&#39;editor Rich Text.

* Per il testo in grassetto, utilizza `<b>` anziché `<strong>`.
* Per il testo in corsivo, utilizza `<i>` anziché `<em>`.

I tag `<strong>` e `<em>` potrebbero causare risultati imprevisti.

+++

+++ Non includere `mboxCreate` all&#39;interno degli script.

`mboxCreate` utilizza `document.write`, pertanto non è consigliabile includerlo negli script. Utilizzare `mboxDefine` e `mboxUpdate` per lo stesso scopo.

+++

+++ Non aggiornare un frammento di codice HTML con [!DNL Target] se per l&#39;inizializzazione è necessario il codice JavaScript.

Quando si esegue un’azione (Modifica HTML) su componenti della pagina come cursori e caroselli, la consegna potrebbe apparire interrotta. Il Compositore esperienza visivo esegue l’azione dopo che JavaScript ha creato un’istanza del componente Pagina. Tuttavia, quando il contenuto della pagina viene distribuito ai visitatori, l’azione viene applicata prima della creazione dell’istanza del componente. Di conseguenza, la funzionalità del componente potrebbe non funzionare più alla consegna, a seconda dello script che definisce il componente sulla pagina.

Un test di consegna che funziona la prima volta non garantisce che la consegna continui a funzionare, perché potrebbe esistere una situazione di tipo &quot;race condition&quot;:

* In presenza di una situazione di tipo &quot;race condition&quot;, la consegna funziona a intermittenza.
* Se non c’è una situazione di tipo &quot;race condition&quot;, la consegna funziona sempre.

Verifica la pagina più volte per assicurarti che la consegna funzioni come previsto.

+++

## Avvertenze {#caveats}

Le seguenti avvertenze si applicano quando si utilizza il **[!UICONTROL Compositore esperienza visivo]** per progettare un&#39;attività.

+++ La funzionalità [!UICONTROL Sposta] non supporta la funzionalità z-index.

Senza la funzionalità z-index, un elemento spostato non può essere posizionato sopra un altro elemento. Per ulteriori dettagli, vedi [Limitazioni](/help/main/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#section_F33C2EA27F2E417AA036BC199DD6C721).

+++

+++ La ridisposizione degli elementi influenza il monitoraggio dei clic.

Se un elemento contrassegnato per il tracciamento dei clic viene ridisposto, i percorsi degli elementi ridisposti cambiano. Di conseguenza, i clic vengono tracciati sull’elemento nella posizione in cui si trovava l’elemento originale prima che fosse ridisposto.

Ciò si verifica perché il codice che distribuisce il contenuto dell’attività e il codice che tiene traccia dei clic sono inclusi in una parte di codice che viene distribuita alla pagina. Se una pagina viene visitata e il tracciamento dei clic è impostato, entrambe le parti di codice vengono recapitate alla pagina. Se la pagina di tracciamento dei clic ha una struttura di pagina simile a quella della pagina in cui viene eseguito il test, il contenuto del test potrebbe essere visualizzato anche nella pagina di tracciamento dei clic.

+++

+++ L&#39;inserimento di un elemento potrebbe non funzionare in un `<div>` che è una mbox.

Se una mbox contiene un&#39;offerta e la mbox non è implementata correttamente, un elemento inserito potrebbe apparire come `insertBefore` e non come `insertAfter`.

+++

+++ Durante la modifica di un elemento padre e di un elemento figlio, modificare innanzitutto il padre.

Se un’azione immagine viene scambiata su un elemento e il testo o il HTML del relativo elemento padre viene quindi modificato, possono verificarsi problemi di consegna. Il flusso di lavoro migliore consiste nel modificare l&#39;elemento padre prima di scambiare l&#39;immagine sull&#39;elemento figlio.

+++

+++ Non selezionare un elemento di pagina che includa una mbox come elemento figlio.

Ad esempio, se la pagina contiene il seguente codice:

```html
<div>
  <div class="mboxDefault" >
  </div>
  <script>mboxCreate('myMbox');
</script>
</div>
```

Il div esterno non deve essere selezionato in un&#39;esperienza, perché la mbox codificata nella pagina effettua ancora una chiamata a [!DNL Target] e riceve una risposta. Questa risposta interferisce con la risposta prevista per l&#39;elemento di pagina più grande.

+++

+++ Gli indirizzi IP proxy potrebbero essere bloccati nell’ambiente del cliente.

Se si utilizza il **[!UICONTROL Compositore esperienza avanzato]** in un sito non attivo, ad esempio un ambiente di gestione temporanea, potrebbero verificarsi timeout ed errori di accesso negato se il sito blocca gli indirizzi IP proxy.

+++

## Limitazioni {#section_F33C2EA27F2E417AA036BC199DD6C721}

Quando si lavora con il Compositore esperienza visivo, si applicano le seguenti limitazioni.

### Requisiti della pagina

+++ Gestire la compatibilità del Compositore esperienza visivo con [!DNL Chrome] modifiche ai criteri di estensione.

In base ai criteri aggiornati del manifesto [V3 in Google Chrome](https://developer.chrome.com/docs/extensions/develop/migrate/what-is-mv3){target=_blank}, le estensioni non possono più modificare il DOM originale prima che venga analizzato dal browser. Di conseguenza, alcuni script di sicurezza, come le implementazioni non compatibili con iframe, potrebbero bloccare il caricamento delle pagine nel Compositore esperienza visivo.

Per garantire la compatibilità, disabilitare questi script in modo condizionale quando la pagina viene caricata nell&#39;iframe [!DNL Target]. Questa operazione può essere eseguita in modo sicuro verificando la presenza dell&#39;oggetto `window.adobeVecExtension`, che [!DNL Target] inserisce durante il caricamento del Compositore esperienza visivo.

I seguenti snippet di codice sono esempi di codice non compatibile con iframe che possono impedire il caricamento di una pagina web nel Compositore esperienza visivo:

`window.top.location = window.self.location;`

`top.location.href = self.location.href;`

Un semplice controllo consente di verificare se una pagina Web è incorporata in [!DNL Target]. Lo snippet di codice si presenta così:

```
if(!window.adobeVecExtension) {
    // additional security logic
}
```

+++

+++ Affinché il Compositore esperienza visivo funzioni, le pagine devono accettare i parametri URL.

Alcuni siti rimuovono eventuali parametri URL dalle proprie pagine, ma il Compositore esperienza visivo richiede tali parametri.

+++

+++ Quando uno script viene utilizzato come parte di HTML, dichiarare tutte le variabili e le funzioni a cui si accede dall&#39;esterno nello spazio dei nomi della finestra.

Lo script viene eseguito nell&#39;ambito di `target.js` dopo il caricamento della pagina, pertanto qualsiasi variabile o funzione dichiarata localmente non è accessibile dall&#39;esterno del blocco di script.

*Errato:*

```html
<script>
  var myVar = 123;
  function myFunc() {
    //
  }
</script>
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

+++ L&#39;azione `customCode` nel Compositore esperienza visivo non funziona con [!DNL Internet Explorer] 8.

`target.js` non supporta questa azione in IE8 a causa delle limitazioni di IE8 durante la gestione del contenuto dello script. Come soluzione alternativa, se la pagina contiene jQuery e jQuery è esposta globalmente sull&#39;oggetto finestra, `target.js` può distribuire l&#39;azione `customCode`. Assicurarsi che `window.jQuery` e `window.jQuery.fn.prepend` siano definiti.

+++

### Ridisposizione delle mbox e

**Impossibile spostare un elemento all&#39;esterno di un contenitore seguito da una proprietà CSS.**

+++ Impossibile selezionare l&#39;elemento [!UICONTROL Button] per la ridisposizione.

Impossibile selezionare direttamente gli elementi **[!UICONTROL Button]** per la ridisposizione. Per abilitare la ridisposizione, posizionare i pulsanti all&#39;interno di un contenitore più grande.

+++

+++ Non ridisporre e spostare lo stesso elemento.

Se un elemento è stato spostato in un’altra posizione e il contenitore principale viene quindi selezionato per ridisporre gli elementi secondari, l’elemento spostato non viene interessato e rimane dove si trova. La ridisposizione potrebbe non essere visualizzata nel modo desiderato.

+++

+++ Sulle mbox sono disponibili solo le offerte di sostituzione.

Azioni quali **[!UICONTROL Modifica classe]** e **[!UICONTROL Ridisponi]** non sono consentite all&#39;interno di una mbox.

+++

### immagini

+++ L&#39;azione [!UICONTROL Modifica immagine] non funziona su un&#39;immagine in un carosello.

Ad esempio, se la pagina contiene un carosello con sei immagini e un&#39;immagine deve essere scambiata con la seconda immagine del carosello, l&#39;azione **[!UICONTROL Modifica immagine]** non funziona.

Come soluzione alternativa, selezionare il contenitore principale e utilizzare l&#39;azione **[!UICONTROL Modifica HTML]** per modificare il HTML del carosello e aggiornare l&#39;origine immagine dell&#39;immagine desiderata.

+++

+++ Le immagini non possono essere ridimensionate in una mbox.

Se un’immagine viene scambiata in un elemento mbox e poi ridimensionata in base alle dimensioni dell’elemento mbox, il ridimensionamento non è consentito.

+++

+++ Dopo lo scambio di un&#39;immagine, non è possibile selezionare l&#39;azione [!UICONTROL Modifica].

Dopo lo scambio dell&#39;immagine, non è possibile modificare l&#39;URL di Scene7.

+++

+++ L&#39;inserimento di un&#39;immagine dalla libreria [!UICONTROL Content] (Scene7) e la modifica del HTML interrompono l&#39;URL dell&#39;immagine.

Aggiungi un elemento di ancoraggio nel div `customHeaderMessage` con testo fittizio:

```html
<a href="#">
<span> Dummy text </span>
</a>
```

Selezionare questo div utilizzando l&#39;azione **[!UICONTROL Inserisci elemento]** per inserire un&#39;immagine di pari livello del testo fittizio.

Dopo aver inserito l’immagine, il codice si presenta così:

```html
<a href="#">
<span> Dummy text </span>
<img src=""> This is inserted Image. </img>
</a>
```

Rimuovi l&#39;intervallo di testo fittizio.

+++

### Tracciamento dei clic e contenuto esterno

+++ Il monitoraggio dei clic non funziona per gli elementi di ancoraggio che contengono elementi diversi dai tag di testo normale o immagine.

Ad esempio, il monitoraggio dei clic non funziona se l&#39;elemento contiene JavaScript.

+++

+++ Il monitoraggio dei clic è supportato solo nella pagina in cui vengono create le esperienze o nella pagina reindirizzata.

Sebbene la modalità **[!UICONTROL Sfoglia]** sia disponibile per il tracciamento dei clic nel Compositore esperienza visivo, non è possibile utilizzare la modalità **[!UICONTROL Sfoglia]** per aggiungere il tracciamento dei clic su una pagina.

+++

+++ Non è possibile modificare gli elementi HTML con un’origine esterna.

Ad esempio: video, tag audio, incorporamento, iFrame e frame.

+++
