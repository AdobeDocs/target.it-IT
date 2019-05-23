---
description: Il compositore esperienza visivo (VEC) per app a pagina singola (SPA) consente agli addetti al marketing di creare test e di personalizzare contenuti nelle SPA in modalità fai-da-te senza dover dipendere sempre dagli sviluppatori. Il Compositore esperienza visivo può essere utilizzato per creare attività nei framework più popolari, come ad esempio React e Angular.
keywords: vec spa;react;angular;react.js;compositore esperienza visivo spa;opzioni compositore esperienza spa;app a pagina singola;app a pagina singola;spa;opzioni esperienza mobile;visualizzazione target
seo-description: Il compositore esperienza visivo (VEC) per app a pagina singola (SPA) in Adobe Target consente agli addetti al marketing di creare test e di personalizzare contenuti nelle SPA in modalità fai-da-te senza dover dipendere sempre dagli sviluppatori. Il Compositore esperienza visivo può essere utilizzato per creare attività nei framework più popolari, come ad esempio React e Angular.
seo-title: Compositore esperienza visivo per app a pagina singola (SPA)
solution: Target
title: Compositore esperienza visivo per app a pagina singola (SPA)
topic: Standard
uuid: 4dcd6d9c-b2e3-4759-a2e0-3696c572faba
translation-type: tm+mt
source-git-commit: 62552bfe5a6eb65dc1760b17543a0f5c84f0ecc5

---


# Compositore esperienza visivo per app a pagina singola (SPA){#single-page-app-spa-visual-experience-composer}

In [!DNL Adobe Target], il [!UICONTROL Compositore esperienza visivo] (VEC) offre agli addetti al marketing una funzionalità autonoma per creare attività e personalizzare esperienze da distribuire in modo dinamico sulle applicazioni a più pagine tradizionali tramite la mbox globale di Adobe Target. Tuttavia, questo fa affidamento sul recupero delle offerte al caricamento delle pagine o alle successive chiamate al server, il che provoca latenza, come illustrato nel diagramma seguente. Questo approccio non funziona al meglio con le applicazioni a pagina singola (SPA) perché rallenta l’esperienza utente e le prestazioni dell’applicazione.

![Ciclo di vita tradizionale rispetto al ciclo di vita di un’applicazione a pagina singola](/help/c-experiences/assets/trad-vs-spa.png)

Con la versione più recente si inaugura il Compositore esperienza visivo per le applicazioni a pagina singola (SPA). Il Compositore esperienza visivo per le applicazioni a pagina singola consente agli addetti al marketing di creare test e di personalizzare contenuti nelle SPA in modalità fai-da-te senza dover dipendere sempre dagli sviluppatori. Il Compositore esperienza visivo può essere utile per creare [test A/B](/help/c-activities/t-test-ab/test-ab.md) e attività di [Targeting delle esperienze](/help/c-activities/t-experience-target/experience-target.md) (XT) sui framework più diffusi, come React e Angular.

## Visualizzazioni di Adobe Target e applicazioni a pagina singola

Il Compositore esperienza visivo di Adobe Target per applicazioni a pagina singola (SPA) sfrutta un nuovo concetto chiamato Visualizzazioni: un gruppo logico di elementi visivi che insieme formano un’esperienza SPA. Un’applicazione a pagina singola può, infatti, essere considerata come transizione attraverso le visualizzazioni (al posto degli URL) basata sulle interazioni dell’utente. In genere, una visualizzazione può rappresentare un intero sito o elementi visivi raggruppati all&#39;interno di un sito.

Per spiegare ulteriormente cosa sono le visualizzazioni, navighiamo in questo ipotetico sito online di e-commerce implementato in React ed esploriamo alcune visualizzazioni di esempio. Fai clic sui collegamenti di seguito per aprire il sito in una nuova scheda del browser.

**Collegamento:[Site Site](https://target.enablementadobe.com/react/demo/#/)**

![home page](/help/c-experiences/assets/home.png)

Quando entriamo nella home page, notiamo subito un’immagine protagonista (hero image) che promuove un’offerta di Pasqua e gli ultimi prodotti venduti sul sito. In questo caso, si può definire una visualizzazione come l’intera home page. Questo è utile da sapere, ma torneremo sull&#39;argomento più avanti, nella sezione Implementazione di visualizzazioni di Adobe Target.

**Collegamento:[Site Site](https://target.enablementadobe.com/react/demo/#/products)**

![sito del prodotto](/help/c-experiences/assets/product-site.png)

Interessati ai prodotti, decidiamo di fare clic sul collegamento Prodotti. Come con la home page, l’intero sito dei prodotti può essere definito come visualizzazione. Possiamo denominare questa visualizzazione &quot;products&quot; come nel nome del percorso `https://target.enablementadobe.com/react/demo/#/products`.

![sito del prodotto 2](/help/c-experiences/assets/product-site-2.png)

All&#39;inizio di questa sezione, abbiamo definito visualizzazioni come l&#39;intero sito o anche un gruppo di elementi visivi sul sito. Come si vede qui sopra, è possibile raggruppare i quattro prodotti visibili sul sito e considerarli come una visualizzazione. Se vogliamo, possiamo denominare questa visualizzazione “Prodotti”.

![sito del prodotto 3](/help/c-experiences/assets/product-site-3.png)

Decidiamo di fare clic sul pulsante Carica altro per esplorare altri prodotti sul sito. In questo caso, l’URL del sito web non cambia. Tuttavia, una visualizzazione qui può rappresentare solo la seconda riga di prodotti visibili qui sopra. Possiamo chiamare questa visualizzazione “Pagina prodotti 2”.

**Collegamento:[Checkout](https://target.enablementadobe.com/react/demo/#/checkout)**

![pagina di checkout](/help/c-experiences/assets/checkout.png)

Visto che ci piacciono alcuni prodotti presenti sul sito, decidiamo di comprarne un paio. Ora, sulla pagina di checkout, sono disponibili alcune opzioni per scegliere la consegna normale o express. Poiché una visualizzazione può essere qualsiasi gruppo di elementi visivi su un sito, questa possiamo chiamarla “Preferenze di consegna”.

Il concetto di visualizzazioni si può estendere ulteriormente. Se gli esperti di marketing desiderano personalizzare il contenuto sul sito a seconda della preferenza di consegna selezionata, è possibile creare una visualizzazione per ogni opzione di consegna. In questo caso, quando selezioniamo Consegna normale, possiamo chiamare la visualizzazione “Consegna normale”. Se selezioniamo l’opzione Consegna express, la visualizzazione si può chiamare “Consegna express”.

Adesso, gli esperti di marketing potrebbero voler eseguire un test A/B per valutare se cambiare il colore da blu a rosso quando si seleziona l’opzione Consegna express per aumentare le conversioni, invece di mantenere il pulsante blu con entrambe le opzioni di consegna.

## Implementazione delle visualizzazioni di Adobe Target

Ora che abbiamo capito cosa sono le visualizzazioni di Adobe Target, possiamo sfruttare questo concetto in Target per consentire agli addetti al marketing di eseguire test A/B e XT sulle applicazioni a pagina singola tramite il Compositore esperienza visivo. Questo richiederà una configurazione per sviluppatori una tantum. Seguiamo i passaggi effettuare la configurazione.

1. Installate at. js 2. x.

   Innanzitutto, è necessario installare at. js 2. x. Questa versione di at. js è stata sviluppata con gli spas. Le versioni precedenti di at.js e mbox.js non supportano le viste di Adobe Target e il Compositore esperienza visivo per applicazioni a pagina singola.

   ![Finestra di dialogo dei dettagli dell’implementazione](/help/c-experiences/assets/imp-200.png)

   Scarica at. js 2. x tramite l&#39;interfaccia utente di Adobe Target disponibile in [!UICONTROL Configurazione &gt; Implementazione]. at. js 2. x può anche essere distribuito tramite [Adobe Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md). Tuttavia, le estensioni di Adobe Target non sono aggiornate e supportate al momento.

1. Implementa la funzione più recente di. js 2. x: [Triggerview ()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-triggerview-atjs-2.md) sui siti.

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

   In qualità di esperto di marketing, se desideri eseguire test A/B sull’intero sito principale, potrebbe essere utile assegnare alla visualizzazione il nome “home” estraendolo dall’URL:

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

   Ora vediamo un esempio un po’ più complicato. Diciamo che, in qualità di esperti di marketing, desideriamo personalizzare la seconda riga dei prodotti cambiando il colore dell’etichetta del prezzo in rosso dopo che un utente ha fatto clic sul pulsante Carica altro.

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

   Se gli esperti di marketing desiderano personalizzare il contenuto sul sito a seconda della preferenza di consegna selezionata, è possibile creare una visualizzazione per ogni opzione di consegna. In questo caso, quando selezioniamo Consegna normale, possiamo chiamare la visualizzazione “Consegna normale”. Se selezioniamo l’opzione Consegna express, la visualizzazione si può chiamare “Consegna express”.

   Adesso, gli esperti di marketing potrebbero voler eseguire un test A/B per valutare se cambiare il colore da blu a rosso quando si seleziona l’opzione Consegna express per aumentare le conversioni, invece di mantenere il pulsante blu con entrambe le opzioni di consegna.

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

1. Avviare le attività A/B o XT tramite il Compositore esperienza visivo.

   Quando si implementa `adobe.target.triggerView()` nell’applicazione a pagina singola con i nomi di visualizzazione passati come parametri, il Compositore esperienza visivo sarà in grado di rilevare tali visualizzazioni e consentire agli utenti di creare azioni e modifiche per le attività A/B o XT.

   >[!NOTE]
   >
   >Il Compositore esperienza visivo per le applicazioni a pagina singola è lo stesso Compositore esperienza visivo utilizzato nelle normali pagine web, ma con alcune funzionalità aggiuntive disponibili quando si apre un&#39;app a pagina singola con `triggerView()` implementato.

I due principali miglioramenti al pannello [Modifiche](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md) e alle azioni per il Compositore esperienza visivo consentono a quest’ultimo di funzionare correttamente con le applicazioni a pagina singola.

**Pannello delle modifiche**

Il pannello delle [!UICONTROL Modifiche], come si vede di seguito, acquisisce le azioni create per una visualizzazione specifica. Tutte le azioni per una visualizzazione sono raggruppate sotto di essa.

**Azioni**

Facendo clic su un’azione viene evidenziato l’elemento del sito dove questa verrà applicata. Ogni azione VEC creata in una visualizzazione presenta quattro icone come mostrato di seguito: Informazioni, Modifica, Sposta ed Elimina.

![Modifiche](/help/c-experiences/assets/modifications-new.png)

Nella tabella seguente viene descritta ogni azione:

| Pagina | Descrizione |
| --- | --- |
| Informazioni | Visualizza i dettagli dell’azione. |
| Modifica | Ti consente di modificare direttamente le proprietà dell’azione. |
| Sposta  | Sposta l&#39;azione in un evento di caricamento pagina o in qualsiasi altra visualizzazione già presente nel pannello delle modifiche.<br>[!UICONTROL Evento] di caricamento della pagina: tutte le azioni corrispondenti all&#39;evento di caricamento della pagina vengono applicate al caricamento iniziale della pagina dell&#39;applicazione Web.<br>**Nota** : per vedere se lo spostamento è un&#39;operazione valida, è necessario passare alla vista nell&#39;aula virtuale tramite Sfoglia. Se l&#39;azione non può essere applicata alla Vista, viene visualizzato un errore |
| Elimina | Elimina l’azione. |

>[!NOTE]
>
>È possibile eseguire numerose azioni prima che la pagina venga caricata nell&#39;aula virtuale o anche se la pagina non è in grado di caricarla completamente. Nell’interfaccia utente di , le azioni che possono essere modificate solo dopo il caricamento del sito risultano disabilitate.

**Esempio 1**

Facciamo riferimento all’esempio precedente, quando abbiamo creato la visualizzazione Home. Il nostro obiettivo per questa visualizzazione è doppio:

1. Cambiare il pulsante Aggiungi al carrello e il pulsante “Mi piace” in un colore blu più chiaro. Questo deve avvenire in un “Caricamento pagina” perché stiamo modificando i componenti dell’intestazione.
1. Modificare l’etichetta “Ultimi prodotti del 2019“ in “Migliori prodotto del 2019” con il colore del testo cambiato in viola.

Per eseguire questi obiettivi, nel Compositore esperienza visivo fai clic su [!UICONTROL Componi] e applica le modifiche nella visualizzazione Home.

![Esempio 1](/help/c-experiences/assets/example1.png)

**Esempio 2**

Facciamo riferimento all’esempio precedente, quando abbiamo creato la visualizzazione Pagina prodotti 2. L’obiettivo è quello di cambiare l’etichetta “Prezzo” in “Prezzo di vendita” con l’etichetta di colore rosso.

1. Fai clic su [!UICONTROL Sfoglia], quindi sul collegamento [!UICONTROL Prodotti] nell’intestazione.
1. Fai clic su [!UICONTROL Carica altro] una volta per passare alla seconda riga di prodotti.
1. Fai clic su [!UICONTROL Componi].
1. Applica le azioni per modificare l’etichetta di testo in “Prezzo di vendita” e il colore in rosso.

![Esempio 2](/help/c-experiences/assets/example2.png)

**Esempio 3**

Infine, come indicato precedentemente, le visualizzazioni si possono definire a livello granulare. Le visualizzazioni possono essere uno stato o anche un pulsante di opzione. In precedenza abbiamo creato le visualizzazioni Consegna express e Consegna normale. L’obiettivo è quello di cambiare il colore del pulsante in rosso per la visualizzazione Consegna express.

1. Fai clic su [!UICONTROL Sfoglia].
1. Aggiungi un paio di prodotti al carrello.
1. Fai clic sull’icona del carrello nell’angolo in alto a destra.
1. Fai clic su Concludi ordine.
1. Fai clic sul pulsante di opzione Consegna express.
1. Fai clic su [!UICONTROL Componi].
1. Modifica il testo del pulsante “Paga” in “Completa l’ordine” e cambia il colore in rosso.

![Esempio 3](/help/c-experiences/assets/example3.png)

>[!NOTE]
>
>La visualizzazione Consegna express non apparirà nel pannello di modifica finché non farai clic sul pulsante di opzione Consegna express. Questo perché la funzione `triggerView()` si attiva quando si seleziona il pulsante di opzione Consegna express. Solo in quel momento il Compositore esperienza visivo sa che è presente una visualizzazione da mostrare nel pannello delle modifiche.

## Approfondire at.js e le applicazioni a pagina singola

**Come posso recuperare le visualizzazioni per i dati del pubblico più recenti forniti dalle azioni dopo il caricamento della pagina iniziale nella mia applicazione a pagina singola?**

Il flusso di lavoro tipico di at. js 2. x è il momento in cui il sito viene caricato, tutte le viste e le azioni sono memorizzate nella cache, in modo che le azioni degli utenti successive sul sito non attivino le chiamate al server per recuperare le offerte. Se desideri recuperare le visualizzazioni in base ai dati di profilo più aggiornati, i quali potrebbero essere stati aggiornati a seconda delle azioni degli utenti successivi, richiama `getOffers()` e `applyOffers()` con gli utenti del pubblico o i dati di profilo passati più di recente.

Ad esempio, si consideri una società di telefonia e si dispone di una SPA che utilizza at. js 2. x. Come attività, vuoi raggiungere i seguenti obiettivi:

* Per un utente disconnesso o anonimo, mostrare la promozione più recente dell’azienda, ad esempio mostrare un’offerta “Primo mese gratis” come immagine protagonista (hero) su `http://www.telecom.com/home`.
* Per un utente registrato, mostrare un’offerta promozionale quando il suo contratto è in scadenza, ad esempio “Potresti avere un telefono gratis!” su `http://www.telecom.com/loggedIn/home`.

Ora, i tuoi sviluppatori chiamano le visualizzazioni e richiamano `triggerView()` nel modo seguente:

* Per `http://www.telecom.com/home` il nome della visualizzazione è “Logged Out Home”
   * Si richiama `triggerView(“Logged Out Home”)`.
* Per `http://www.telecom.com/loggedIn/home` il nome della visualizzazione è “Logged In Home”
   * `triggerView(“Logged In Home”)` viene richiamato alla modifica del percorso.

Gli addetti al marketing eseguono quindi le seguenti attività A/B tramite il Compositore esperienza visivo:

* Attività A/B con l’offerta “Primo mese gratuito” per i tipi di pubblico con il parametro “`loggedIn= false`” da mostrare in `http://www.telecom.com/home`, dove il nome della visualizzazione è Logged Out Home.
* Attività A/B con l’offerta “Potresti avere un telefono gratis!” per i tipi di pubblico con il parametro “`loggedIn=true`” da mostrare in `http://www.telecom.com/loggedIn/home`, dove il nome della visualizzazione Logged In Hero Offer.

Adesso, prendiamo in considerazione questo flusso utente:

1. Un utente non registrato anonimo arriva sulla tua pagina.
1. Poiché utilizzate at. js 2. x, trasmettete il parametro «`loggedIn = false`» al caricamento della pagina per recuperare tutte le visualizzazioni presenti nelle attività attive idonee quando l&#39;audience ha il parametro «`loggedIn = false`».
1. at. js 2. x quindi recupera la vista e l&#39;azione della Home out per mostrare l&#39;offerta &quot;Primo mese gratuito&quot; e la memorizza nella cache.
1. Quando si richiama `triggerView(“Logged Out Home”)`, si recupera l’offerta “Primo mese gratuito” dalla cache e l’offerta appare senza una chiamata al server.
1. L’utente ora fa clic su “Login” e fornisce le relative credenziali.
1. Poiché il tuo sito web è una applicazione a pagina singola, non si esegue un caricamento completo della pagina, ma si indirizza invece l’utente a `http://www.telecom.com/loggedIn/home`.

Il problema è qui. L’utente accede e trova `triggerView(“Logged In Home”)` perché abbiamo inserito questo codice in seguito alla modifica del percorso. In questo modo, all&#39;indirizzo. js 2. x viene richiesto di recuperare la visualizzazione e le azioni dalla cache, ma l&#39;unica visualizzazione presente nella cache è disconnesso.

Quindi, come si recupera la visualizzazione Logged In e si visualizza il messaggio “Puoi avere un telefono gratis!”? offerta? Inoltre, poiché tutte le azioni successive sul sito saranno da un punto di vista di un utente registrato, come fare per assicurarsi che tutte le azioni successive risultino in offerte personalizzate per utenti registrati?

Potete utilizzare le nuove `getOffers()` e `applyOffers()` le funzioni supportate in at. js 2. x:

```
adobe.target.getOffers({
  request: {
  prefetch: {
    "views": [
      {
        "parameters": {
          "loggedIn": true
        },
      }
    ]
  },
});
```

Passa la risposta di `getOffers()` a `applyOffers()` e ora tutte le visualizzazioni e azioni associate a “loggedin = true” aggiorneranno la cache di at.js.

In altre parole, at. js 2. x supporta un modo per recuperare viste, azioni e offerte con i dati del pubblico più aggiornati in modalità on-demand.

**At. js 2. x supporta A 4 T per applicazioni singole?**

Sì, at. js 2. x supporta A 4 T for SPA tramite `triggerView()` la funzione dato che hai implementato Adobe Analytics e il servizio ID visitatori di Experience Cloud. Consulta il diagramma seguente con le descrizioni dettagliate.

![Flusso di Target](/help/c-experiences/assets/atjs-spa-flow.png)

| Passaggio | Descrizione |
| --- | --- |
| 1 | Si richiama `triggerView()` nell’applicazione a pagina singola per eseguire il rendering di una visualizzazione e applicare azioni per modificare gli elementi visuali associati alla visualizzazione. |
| 2 | Il contenuto mirato per la visualizzazione viene letto dalla cache. |
| 3 | Il contenuto mirato viene mostrato il più rapidamente possibile senza che venga visualizzato momentaneamente il contenuto predefinito. |
| 4 | Si invia la richiesta di notifica all’archivio profili di Target per conteggiare il visitatore nell’attività e nelle metriche incrementali. |
| 5 | Dati di Analytics inviati ai server di raccolta dati. |
| 6 | I dati di Target vengono confrontati con i dati di Analytics tramite SDID e vengono elaborati nell’archivio dei rapporti di Analytics. È quindi possibile visualizzare i dati di Analytics sia in Analytics che in Target tramite i rapporti A4T. |

>[!NOTE]
>Se non desideri inviare notifiche ad Adobe Analytics per il conteggio delle impression ogni volta che si attiva una visualizzazione, passa `{page: false}` nella funzione `triggerView()` in modo che il conteggio delle impression non si gonfi quando una visualizzazione si attiva più volte per un componente riprodotto costantemente. Ad esempio:
>
>`adobe.target.triggerView(“PRODUCTS-PAGE-2”, {page:false})`

## Attività supportate

| Tipo di attività | Supportate? |
| --- | --- |
| [Test A/B](/help/c-activities/t-test-ab/test-ab.md) | Sì |
| [Consigli come offerta](/help/c-recommendations/recommendations-as-an-offer.md)<br>in attività di test A/B e targeting delle esperienze (XT) | Sì |
| [Allocazione automatica](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Sì |
| [Targeting esperienza](/help/c-activities/t-experience-target/experience-target.md) | Sì |
| [Test multivariato](/help/c-activities/c-multivariate-testing/multivariate-testing.md) | No |
| [Targeting automatico](/help/c-activities/auto-target-to-optimize.md) | No |
| [Personalizzazione automatizzata](/help/c-activities/t-automated-personalization/automated-personalization.md) | No |
| [Consigli](/help/c-recommendations/recommendations.md) | No |

**Se abbiamo installato at. js 2. x e implementato`triggerView()`sui nostri siti, come eseguiamo le attività Auto-Target A/B perché SPA VEC non supporta Auto-Target?**

Se desideri utilizzare le attività A/B di targeting automatico, sposta tutte le azioni da eseguire sull’evento caricamento pagina nel Compositore esperienza visivo. Passa il puntatore del mouse su ciascuna azione, quindi fai clic sul pulsante [!UICONTROL Sposta su evento “Caricamento pagina”]. Dopodiché, nel passaggio successivo, seleziona il targeting automatico come metodo di allocazione del traffico.

## Integrazioni supportate

| Integrazione | Supportate? |
| --- | --- |
| [Analytics for Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md) | Sì |
| [Experience Cloud Audiences](/help/c-integrating-target-with-mac/mmp.md) | Sì |
| [Attributi del cliente](/help/c-target/c-visitor-profile/working-with-customer-attributes.md) | Sì |
| [Frammenti esperienza AEM](/help/c-experiences/c-manage-content/aem-experience-fragments.md) | Sì |

## Funzioni supportate {#supported-features}

| Funzione | Supportate? |
| --- | --- |
| [Aree di lavoro e proprietà](/help/administrating-target/c-user-management/property-channel/property-channel.md) | Sì |
| [Collegamenti QA](/help/c-activities/c-activity-qa/activity-qa.md) | Sì |
| [Compositore esperienza basato su moduli](/help/c-experiences/form-experience-composer.md) | No |
| [Codice personalizzato ](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md) | Sì |
| [Opzioni VEC](/help/c-experiences/c-visual-experience-composer/viztarget-options.md) | Tutte |
| [Tracciamento dei clic](/help/c-activities/r-success-metrics/click-tracking.md) | Sì |
| [Consegna di più attività](/help/c-experiences/c-visual-experience-composer/multipage-activity.md) | Sì |

## Video di formazione: Utilizzo del Compositore esperienza visivo per le applicazioni a pagina singola in Adobe Target

>[!VIDEO](https://video.tv.adobe.com/v/26249)

Per ulteriori informazioni, consultate [Utilizzo di Visual Experience Composer (Compositore esperienza visivo) per App singola (SPA) in Adobe Target](https://helpx.adobe.com/target/kt/using/visual-experience-composer-for-single-page-applications-feature-video-use.html) .
