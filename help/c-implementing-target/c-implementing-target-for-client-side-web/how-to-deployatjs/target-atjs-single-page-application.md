---
description: Informazioni da utilizzare in. js 2. x per implementare le applicazioni singole (SPAS).
keywords: implementazione dell'applicazione pagina singola; implementazione dell'applicazione a pagina singola; spa; at. js 2. x
seo-description: Informazioni su come utilizzare Adobe Target at. js 2. x per implementare applicazioni singole di pagina (SPAS).
seo-title: Implementazione di un’applicazione a pagina singola
solution: Target
title: Implementazione di un’applicazione a pagina singola
topic: Standard
uuid: 5887ec53-e5b1-40f9-b469-33685f5c6cd6
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Implementazione di un&#39;applicazione a pagina singola{#single-page-application-implementation}

I siti Web tradizionali funzionavano su modelli di navigazione «Pagina a pagina», altrimenti noti come Applicazioni multipagina, in cui le progettazioni dei siti Web erano strettamente collegate a URL e transizioni da una pagina Web a un&#39;altra, per un caricamento di pagina diverso. Le applicazioni web moderne, come le applicazioni a pagina singola, adottano invece un modello che attiva rapidamente il rendering dell’interfaccia utente del browser, spesso indipendente dalla pagina. Queste esperienze si attivano spesso tramite le interazioni dei clienti, ad esempio lo scorrimento, clic e movimenti del cursore. Con l’evoluzione dei paradigmi del web moderno, la rilevanza degli eventi generici tradizionali, come il caricamento delle pagine, per distribuire personalizzazione e sperimentazione non funziona più.

![Ciclo di vita di una pagina tradizionale rispetto al ciclo di vita di un’applicazione a pagina singola](/help/c-experiences/assets/trad-vs-spa.png)

at. js 2. x fornisce funzioni avanzate che consentono all&#39;azienda di eseguire personalizzazioni su tecnologie lato client e lato client. Questa versione si concentra sul miglioramento di at.js per garantire interazioni in sintonia con le applicazioni a pagina singola.

Di seguito sono riportati alcuni vantaggi per l&#39;utilizzo at. js 2. x non disponibile nelle versioni precedenti:

* Capacità di memorizzare nella cache tutte le offerte al caricamento di pagina per ridurre più chiamate al server a una singola chiamata al server.
* Migliorate enormemente le esperienze degli utenti finali sul sito, in quanto le offerte appaiono immediatamente tramite la cache senza intervalli dovuti alle chiamate al server tradizionali.
* Una semplice riga di codice e una configurazione per sviluppatori una tantum per consentire agli esperti di marketing di creare ed eseguire attività A/B e Targeting esperienza (XT) tramite il Compositore esperienza visivo sull’applicazione a pagina singola.

## Visualizzazioni di destinazione e applicazioni a pagina singola di Adobe Target

Il Compositore esperienza visivo di Adobe Target per applicazioni a pagina singola (SPA) sfrutta un nuovo concetto chiamato Visualizzazioni: un gruppo logico di elementi visivi che insieme formano un’esperienza SPA. Un’applicazione a pagina singola può, infatti, essere considerata come transizione attraverso le visualizzazioni (al posto degli URL) basata sulle interazioni dell’utente. In genere, una visualizzazione può rappresentare un intero sito o elementi visivi raggruppati all&#39;interno di un sito.

Per spiegare ulteriormente cosa sono le visualizzazioni, navighiamo in questo ipotetico sito online di e-commerce implementato in React ed esploriamo alcune visualizzazioni di esempio. Fai clic sui collegamenti di seguito per aprire il sito in una nuova scheda del browser.

**Collegamento:[Site Site](https://target.enablementadobe.com/react/demo/#/)**

![home page](/help/c-experiences/assets/home.png)

Quando entriamo nella home page, notiamo subito un’immagine protagonista (hero image) che promuove un’offerta di Pasqua e gli ultimi prodotti venduti sul sito. In questo caso, si può definire una visualizzazione come l&#39;intera home page. Questo è utile da sapere, ma torneremo sull&#39;argomento più avanti, nella sezione Implementazione di visualizzazioni di Adobe Target.

**Collegamento:[Site Site](https://target.enablementadobe.com/react/demo/#/products)**

![sito del prodotto](/help/c-experiences/assets/product-site.png)

Interessati ai prodotti venduti dall’azienda, decidiamo di fare clic sul collegamento Prodotti. Come con la home page, l&#39;intero sito dei prodotti può essere definito come visualizzazione. Possiamo denominare questa visualizzazione &quot;products&quot; come nel nome del percorso `https://target.enablementadobe.com/react/demo/#/products)`.

![sito del prodotto 2](/help/c-experiences/assets/product-site-2.png)

All&#39;inizio di questa sezione, abbiamo definito visualizzazioni come l&#39;intero sito o anche un gruppo di elementi visivi sul sito. Come si vede qui sopra, è possibile raggruppare i quattro prodotti visibili sul sito e considerarli come una visualizzazione. Se vogliamo, possiamo denominare questa visualizzazione “Products”.

![sito del prodotto 3](/help/c-experiences/assets/product-site-3.png)

Decidiamo di fare clic sul pulsante Carica altro per esplorare altri prodotti sul sito. In questo caso, l&#39;URL del sito web non cambia. Tuttavia, una visualizzazione qui può rappresentare solo la seconda riga di prodotti visibili qui sopra. Possiamo chiamare questa visualizzazione “PRODUCTS-PAGE-2”.

**Collegamento:[Checkout](https://target.enablementadobe.com/react/demo/#/checkout)**

![pagina di checkout](/help/c-experiences/assets/checkout.png)

Visto che ci piacciono alcuni prodotti presenti sul sito, decidiamo di comprarne un paio. Ora, sulla pagina di checkout, sono disponibili alcune opzioni per scegliere la consegna normale o express. Poiché una visualizzazione può essere qualsiasi gruppo di elementi visivi su un sito, questa possiamo chiamarla “Preferenze di consegna”.

Il concetto di visualizzazioni si può estendere ulteriormente. Se gli esperti di marketing desiderano personalizzare il contenuto sul sito a seconda della preferenza di consegna selezionata, è possibile creare una visualizzazione per ogni opzione di consegna. In questo caso, quando selezioniamo Consegna normale, possiamo chiamare la visualizzazione “Consegna normale”. Se selezioniamo l’opzione Consegna Express, la visualizzazione si può chiamare “Consegna express”.

Adesso, gli esperti di marketing potrebbero voler eseguire un test A/B per valutare se cambiare il colore da blu a rosso quando si seleziona l’opzione Consegna express per aumentare le conversioni, invece di mantenere il pulsante blu con entrambe le opzioni di consegna.

## Implementazione delle visualizzazioni di Adobe Target

Ora che abbiamo capito cosa sono le visualizzazioni di Adobe Target, possiamo sfruttare questo concetto in Target per consentire agli addetti al marketing di eseguire test A/B e XT sulle applicazioni a pagina singola tramite il Compositore esperienza visivo. Questo richiederà una configurazione per sviluppatori una tantum. Seguiamo i passaggi effettuare la configurazione.

1. Installate at. js 2. x.

   Innanzitutto, è necessario installare at. js 2. x. Questa versione di at. js è stata sviluppata con gli spas. Le versioni precedenti di at.js e mbox.js non supportano le viste Adobe Target e il Compositore esperienza visivo per le applicazioni a pagina singola.

   Scarica at. js 2. x tramite l&#39;interfaccia utente di Adobe Target disponibile in [!UICONTROL Configurazione &gt; Implementazione]. at. js 2. x può anche essere distribuito tramite Adobe Launch. Tuttavia, le estensioni di Adobe Target non sono aggiornate e supportate al momento.

1. Implementa la funzione più recente di. js 2. x `triggerView()` sui tuoi siti.

   Dopo aver definito le visualizzazioni della SPA in cui desiderate eseguire un test A/B o XT, implementate la `triggerView()` funzione at. js 2. x con le visualizzazioni trasmesse come parametro. Questo consente agli esperti di marketing di utilizzare il Compositore esperienza visivo per progettare ed eseguire i test A/B e XT per queste visualizzazioni definite. Se la funzione `triggerView()` non è definita per tali visualizzazioni, il Compositore esperienza visivo non le rileva e, pertanto, gli addetti al marketing non possono utilizzarlo per progettare ed eseguire test A/B e XT.

   **`adobe.target.triggerView(viewName, options)`**

   | Parametro | Type (Tipo) | Obbligatorio | Convalida | Descrizione |
   | --- | --- | --- | --- | --- |
   | viewName | Stringa | Sì | 1. Senza spazi finali.<br>2. Non può essere vuoto.<br>3. Il nome della visualizzazione deve essere univoco per tutte le pagine.<br>4. **Avviso**: il nome della visualizzazione non deve iniziare o finire con &quot;`/`&quot;. Questo perché il cliente in genere estrae il nome della visualizzazione dal percorso URL. Per noi, &quot;home&quot; e &quot;`/home`&quot; sono diversi.<br>5. **Avviso**: non attivare la stessa visualizzazione in sequenza più volte con l&#39;opzione `{page: true}`. | Passa un nome qualsiasi come tipo di stringa che desideri rappresenti la tua visualizzazione. Questo nome della visualizzazione appare nel pannello [!UICONTROL Modifiche] del Compositore esperienza visivo per consentire agli addetti al marketing di creare azioni ed eseguire le attività A/B e XT. |
   | options | Oggetto | No |
   | options &gt; page | Booleano | No | **TRUE**: il valore predefinito della pagina è vero. Con `page=true`, si inviano notifiche ai server perimetrali per incrementare il conteggio delle impression.<br>**FALSE**: con `page=false`, non si inviano notifiche per incrementare il conteggio delle impression. Da utilizzare solo per eseguire nuovamente il rendering di un componente su una pagina con un&#39;offerta. |

   Ora vediamo alcuni esempi d’uso su come invocare la funzione `triggerView()` in React per la nostra ipotetica applicazione a pagina singola per e-commerce:

   **Collegamento:[Site Site](https://target.enablementadobe.com/react/demo/#/)**

   ![home-react-1](/help/c-experiences/assets/react1.png)

   In qualità di esperto di marketing, se desideri eseguire test A/B sull’intero sito principale, potrebbe essere utile assegnare alla visualizzazione il nome “home”:

```
 function targetView() {
   var viewName = window.location.hash; // or use window.location.pathName if router works on path and not hash

   viewName = viewName || 'home'; // view name cannot be empty

   // Sanitize viewName to get rid of any trailing symbols derived from URL
   if (viewName.startsWith('#') || viewName.startsWith('/')) {
     viewName = viewName.substr(1);
   }

   // Validate if the Target Libraries are available on your website
   if (typeof adobe != 'undefined' && adobe.target && typeof adobe.target.triggerView === 'function') {
     adobe.target.triggerView(viewName);
   }
 }

 // react router v4
 const history = syncHistoryWithStore(createBrowserHistory(), store);
 history.listen(targetView);

 // react router v3
 <Router history={hashHistory} onUpdate={targetView} >
```

**Collegamento:[Sito prodotti](https://target.enablementadobe.com/react/demo/#/products)**

Ora vediamo un esempio un po&#39; più complicato. Diciamo che, in qualità di esperti di marketing, desideriamo personalizzare la seconda riga dei prodotti cambiando il colore dell’etichetta “Prezzo” in rosso dopo che un utente ha fatto clic sul pulsante Carica altro.

![react prodotti](/help/c-experiences/assets/react4.png)

```
 function targetView(viewName) {
   // Validate if the Target Libraries are available on your website
   if (typeof adobe != 'undefined' && adobe.target && typeof adobe.target.triggerView === 'function') {
     adobe.target.triggerView(viewName);
   }
 }

 class Products extends Component {
   render() {
     return (
       <button type="button" onClick={this.handleLoadMoreClicked}>Load more</button>
     );
   }

   handleLoadMoreClicked() {
     var page = this.state.page + 1; // assuming page number is derived from component’s state
     this.setState({page: page});
     targetView('PRODUCTS-PAGE-' + page);
   }
 }
```

**Collegamento:[Checkout](https://target.enablementadobe.com/react/demo/#/checkout)**

![react checkout](/help/c-experiences/assets/react6.png)

Se gli esperti di marketing desiderano personalizzare il contenuto sul sito a seconda della preferenza di consegna selezionata, è possibile creare una visualizzazione per ogni opzione di consegna. In questo caso, quando selezioniamo Consegna normale, possiamo chiamare la visualizzazione “Consegna normale”. Se selezioniamo l’opzione Consegna Express, la visualizzazione si può chiamare “Consegna express”.

Adesso, gli esperti di marketing potrebbero voler eseguire un test A/B per valutare se cambiare il colore da blu a rosso quando si seleziona l&#39;opzione Consegna express per aumentare le conversioni, invece di mantenere il pulsante blu con entrambe le opzioni di consegna.

```
 function targetView(viewName) {
   // Validate if the Target Libraries are available on your website
   if (typeof adobe != 'undefined' && adobe.target && typeof adobe.target.triggerView === 'function') {
     adobe.target.triggerView(viewName);
   }
 }

 class Checkout extends Component {
   render() {
     return (
       <div onChange={this.onDeliveryPreferenceChanged}>
         <label>
           <input type="radio" id="normal" name="deliveryPreference" value={"Normal Delivery"} defaultChecked={true}/>
           <span> Normal Delivery (7-10 business days)</span>
         </label>

         <label>
           <input type="radio" id="express" name="deliveryPreference" value={"Express Delivery"}/>
           <span> Express Delivery* (2-3 business days)</span>
         </label>
       </div>
     );
   }
   onDeliveryPreferenceChanged(evt) {
     var selectedPreferenceValue = evt.target.value;
     targetView(selectedPreferenceValue);
   }
 }
```

## diagrammi di sistema. js 2. x

I seguenti diagrammi ti aiutano a capire il flusso di lavoro di at. js 2. x con Visualizzazioni e il modo in cui questo migliora l&#39;integrazione con SPA. Per una migliore introduzione dei concetti utilizzati in at. js 2. x, consultate [Implementazione delle applicazioni per pagina singola](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md).

![Target flow with at. js 2. x](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/system-diagram-atjs-20.png)

| Passaggio | Dettagli |
| --- | --- |
| 1 | La chiamata restituisce l&#39;[!DNL Experience Cloud ID] se l’utente è autenticato; un’altra chiamata sincronizza l’ID cliente. |
| 2 | La libreria at.js viene caricata in modo sincrono e nasconde il corpo del documento.<br>at.js si carica anche in modo asincrono con un&#39;opzione che nasconde lo snippet implementato sulla pagina. |
| 3 | Si effettua una richiesta di caricamento della pagina, con tutti i parametri configurati (MCID, SDID e ID cliente). |
| 4 | Gli script di profilo vengono eseguiti e quindi inseriti nell’archivio profili. L’archivio richiede un pubblico idoneo dalla libreria Pubblico (ad esempio, pubblico condiviso da Adobe Analytics, Audience Manager, ecc.).<br>Gli attributi del cliente vengono inviati all’archivio profili in un processo batch. |
| 5 | In base ai parametri di richiesta dell&#39;URL e ai dati di profilo, [!DNL Target] determina le attività ed esperienze da restituire al visitatore per la pagina corrente e le viste future. |
| 6 | Il contenuto di destinazione viene rinviato alla pagina, includendo facoltativamente i valori di profilo per ulteriore personalizzazione.<br>Il contenuto mirato sulla pagina corrente viene mostrato il più rapidamente possibile senza che venga visualizzato momentaneamente il contenuto predefinito.<br>Contenuto mirato per le viste mostrate come risultato delle azioni dell&#39;utente in un’applicazione a pagina singola memorizzata nella cache del browser, in modo da applicarla immediatamente senza una chiamata al server aggiuntiva quando si attivano le viste tramite `triggerView()`. |
| 7 | I dati Analytics vengono inviati ai server di raccolta dati. |
| 8 | I dati di Target vengono confrontati con i dati di Analytics tramite SDID ed elaborati nell’archivio dei rapporti di Analytics.<br>I dati di Analytics possono quindi essere visualizzati sia in Analytics che in Target tramite i rapporti Analytics for Target (A4T). |

Ora, ovunque si implementi `triggerView()` nell’applicazione a pagina singola, le visualizzazioni e le azioni vengono recuperate dalla cache e mostrate all’utente senza una chiamata al server. `triggerView()` invia anche una richiesta di notifica al backend [!DNL Target] per incrementare e registrare i conteggi delle impression.

![Target flow at. js 2. x triggerview](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/atjs-20-triggerview.png)

| Passaggio | Dettagli |
| --- | --- |
| 1 | Si richiama `triggerView()` nell’applicazione a pagina singola per eseguire il rendering della visualizzazione e applicare azioni per modificare gli elementi visuali. |
| 2 | Il contenuto mirato per la visualizzazione viene letto dalla cache. |
| 3 | Il contenuto mirato viene mostrato il più rapidamente possibile senza che venga visualizzato momentaneamente il contenuto predefinito. |
| 4 | Si invia la richiesta di notifica all&#39;archivio profili di [!DNL Target] per conteggiare il visitatore nell&#39;attività e nelle metriche incrementali. |
| 5 | Dati di Analytics inviati ai server di raccolta dati. |
| 6 | I dati di Target vengono confrontati con i dati di Analytics tramite SDID e vengono elaborati nell’archivio dei rapporti di Analytics. È quindi possibile visualizzare i dati di Analytics sia in Analytics che in Target tramite i rapporti A4T. |

## Compositore esperienza visivo per app a pagina singola

Dopo aver installato all&#39;indirizzo. js 2. x e aggiunto `triggerView()` al sito, utilizzate la VEC per eseguire attività A/B e XT. Per ulteriori informazioni, consulta [Compositore esperienza visivo per app a pagina singola](/help/c-experiences/spa-visual-experience-composer.md).

>[!NOTE]
>
>Il Compositore esperienza visivo per le applicazioni a pagina singola è lo stesso Compositore esperienza visivo utilizzato nelle normali pagine web, ma con alcune funzionalità aggiuntive disponibili quando si apre un&#39;app a pagina singola con `triggerView()` implementato.

## Utilizzate triggerview per garantire che A 4 T funzioni correttamente con at. js 2. x e spas {#triggerview}

Per fare in modo che [Analytics per Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A 4 T) funzioni correttamente con at. js 2. x, assicurati di inviare lo stesso codice SDID nella richiesta di Target e nella richiesta Analytics.

Come best practice relative agli spas:

* Utilizzare eventi personalizzati per notificare che si verificano elementi interessanti nell&#39;applicazione
* Attivare un evento personalizzato prima che la visualizzazione inizi il rendering
* Attivazione di un evento personalizzato al termine del rendering

at. js 2. x ha aggiunto una nuova funzione API [triggerview ()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-triggerview-atjs-2.md) . Utilizzate `triggerView()` per notificare all&#39;indirizzo. js che una visualizzazione avvia il rendering.

Per vedere come combinare eventi personalizzati, at. js 2. x e Analytics, vediamo un esempio. Questo esempio presuppone che la pagina HTML contenga l&#39;API Visitor, seguita da at. js 2. x, seguita da appmeasurement.

Supponiamo che siano presenti i seguenti eventi personalizzati:

* `at-view-start` - Quando la visualizzazione avvia il rendering
* `at-view-end` - Al termine del rendering

Per fare in modo che A 4 T funzioni con at. js 2. x,

Il gestore di avvio della visualizzazione dovrebbe avere un aspetto simile al seguente:

```
document.addEventListener("at-view-start", function(e) {
  var visitor = Visitor.getInstance("<your Adobe Org ID>");
  
  visitor.resetState();
  adobe.target.triggerView("<view name>");
});
```

Il gestore di fine visualizzazione dovrebbe essere simile a quello che segue:

```
document.addEventListener("at-view-end", function(e) {
  // s - is the AppMeasurement tracker object
  s.t();
});
```

>[!NOTE]
>
>È necessario attivare ed `at-view-start``at-view-end` eventi. Questi eventi non fanno parte degli eventi personalizzati at. js.

Anche se questi esempi utilizzano il codice javascript, tutto questo può essere semplificato se utilizzate un gestore tag, come [Adobe Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md).

Se si seguono la procedura precedente, per gli SPAS dovreste disporre di una soluzione A 4 T solida.

## Video di formazione

I video che seguono contengono ulteriori informazioni:

### Come funziona at. js 2. x

>[!VIDEO](https://video.tv.adobe.com/v/26250)

Consultate [in che modo at. js 2. x funziona](https://helpx.adobe.com/target/kt/using/atjs20-diagram-technical-video-understand.html) per ulteriori informazioni.

### Implementa at. js 2. x in una SPA

>[!VIDEO](https://video.tv.adobe.com/v/26248)

Consulta [Implementazione di Adobe Target at. js 2. x in un&#39;applicazione pagina singola (SPA)](https://helpx.adobe.com/target/kt/using/atjs2-single-page-application-technical-video-implement.html) per ulteriori informazioni.

### Utilizzo del Compositore esperienza visivo per le applicazioni a pagina singola in Adobe Target

>[!VIDEO](https://video.tv.adobe.com/v/26249)

Per ulteriori informazioni, consultate [Utilizzo di Visual Experience Composer (Compositore esperienza visivo) per App singola (SPA) in Adobe Target](https://helpx.adobe.com/target/kt/using/visual-experience-composer-for-single-page-applications-feature-video-use.html) .