---
description: Il Compositore esperienza visivo (VEC) per app mobile native ti permette di creare attività e personalizzare contenuti in app mobile native in modo fai da te senza dover dipendere dalle continue modifiche degli sviluppatori e dai cicli di rilascio delle app.
seo-description: Il Compositore esperienza visivo (VEC) per app mobile native ti permette di creare attività e personalizzare contenuti in app mobile native in modo fai da te senza dover dipendere dalle continue modifiche degli sviluppatori e dai cicli di rilascio delle app.
seo-title: Compositore esperienza visivo per app mobile
solution: Target
title: Compositore esperienza visivo per app mobile
topic: Standard
uuid: 83702f9c-40ff-441b-b773-46b01155a6f2
translation-type: tm+mt
source-git-commit: 156587a0375fe2dbf8c461e310b2eae04b491b57

---


# Compositore esperienza visivo per app mobile{#mobile-app-visual-experience-composer}

Il Compositore esperienza visivo (VEC) per app mobile native ti permette di creare attività e personalizzare contenuti in app mobile native in modo fai da te senza dover dipendere dalle continue modifiche degli sviluppatori e dai cicli di rilascio delle app.

Il [Compositore esperienza visivo](../../c-experiences/experiences.md#section_34265986611B4AB8A0E4D6ACC25EF91D) esistente ti offre la possibilità, in modo del tutto autonomo, di creare attività e personalizzare esperienze che possono essere consegnate in maniera dinamica alle tue proprietà web tramite l&#39;mbox globale di Target senza alcun intervento degli sviluppatori. Da questo momento, puoi sfruttare il Compositore esperienza visivo per compiere la stessa azione con le applicazioni mobile native. Il Compositore esperienza visivo per app mobile, disponibile in [AEP SDK v5](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-target-vec), può essere utilizzato per creare [attività di test A/B](/help/c-activities/t-test-ab/test-ab.md) e [targeting delle esperienze (XT)](/help/c-activities/t-experience-target/experience-target.md) per le app mobili. Il supporto per gli altri tipi di attività sarà disponibile in futuro.

Il Compositore esperienza visivo per app mobile supporta i browser elencati in [Browser supportati](../../c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md#reference_01B4BF99E7D545A7998773202A2F6100).

## Utilizzo del Compositore esperienza visivo per le app mobile native {#using-the-mobile-vec}

La figura seguente rappresenta il processo di utilizzo del Compositore esperienza visivo per app mobile:

![](assets/mobile-vec-diagram.png)

| Processo | Dettagli |
|--- |--- |
| Associazione | Autorizza in modo sicuro la tua app e il tuo dispositivo mobile perché funzionino con Target. Questo passaggio è necessario solo una volta per un dispositivo. |
| Creazione | Creare un [Attività Target](/help/c-activities/activities.md) con una visualizzazione in anteprima e in tempo reale delle azioni eseguite nell’interfaccia utente di Target. |
| Consegna | Target consegna automaticamente le attività nella tua app mobile nativa. |

**Associazione:**

Il Compositore esperienza visivo per app mobile si connette in tempo reale all’app mobile dell’addetto al marketing per creare le attività di Target. Per poter abilitare questa funzione, il primo passo è associare in modo sicuro (autorizzare) il dispositivo e l’app mobile con Target.

1. Durante la creazione di un’attività di test A/B, ad esempio, seleziona **[!UICONTROL App mobile]**, seleziona **[!UICONTROL Visiva (predefinita)]**, quindi fai clic su **[!UICONTROL Successivo]**.

   ![](assets/mobile-vec-create-1.png)

1. Inserisci l’URL dell’app, quindi fai clic su **[!UICONTROL Crea collegamento diretto]**.

   ![](assets/mobile-vec-create-2.png)

Il processo di associazione contiene i seguenti passaggi:

1. Inserisci lo schema URL dell’app che può essere utilizzato per generare un collegamento diretto. Un tipico collegamento diretto potrebbe essere il seguente:

   `mymobileapp://path?params`

1. Il collegamento diretto è disponibile come codice QR o come URL. Gli utenti possono effettuare la scansione del codice QR dal telefono oppure inviarsi l’URL via e-mail o messaggio. L’URL del collegamento diretto possiede un token di autorizzazione che viene utilizzato per associare in modo sicuro l’app e il dispositivo mobile con Target.
1. Apri l’URL del collegamento diretto sul tuo dispositivo mobile. Questa operazione avvia l&#39;applicazione mobile. L’SDK rileva che l’app viene avviata per l’associazione e la creazione nel Compositore esperienza visivo.

   L’SDK fa una richiesta al server di Target e si auto-registra. Il server di Target autorizza il token e stabilisce una connessione in tempo reale con il dispositivo (attualmente utilizza WebSocket).

   Una volta che la connessione è stata stabilita, appare una visualizzazione dell’app in tempo reale nell’interfaccia di Target. L’app possiede una sovrapposizione con un limite rosso che indica la connessione dell’app a Target, come mostrato nella figura di seguito.

   ![](assets/mobile-vec-create-3.png)

   I dispositivi che sono già stati associati possono essere riconnessi avviando l’app e aprendo l’interfaccia di creazione.

**Creazione:**

una volta che l’app è stata connessa ed è apparsa una visualizzazione di questa in tempo reale nel Compositore esperienza visivo, puoi iniziare a creare l’attività. A questo punto vengono supportate le seguenti azioni:

| Azione | Dettagli |
|--- |--- |
| Scambia immagine | Puoi sostituire un’immagine con un’altra, facendo clic su un’altra offerta immagine o impostando direttamente l’URL del CDN di un’immagine. Le offerte di immagini in Target vengono servite tramite [Adobe Scene7](/help/administrating-target/scene7-settings.md). |
| Modifica testo | Modifica il contenuto del testo, il colore o le dimensioni del font in un elemento di testo, un pulsante o un’etichetta. |
| Modifica sfondo | Modifica il contenuto o lo sfondo dell’elemento per un’area di testo o un pulsante. |

Le azioni eseguite nel Compositore esperienza visivo sono visibili in tempo reale nell’app, consentendo quindi la funzionalità di visualizzazione in anteprima e in tempo reale durante la creazione. Le azioni sono associate con schermate o visualizzazioni mobile correlate in modo appropriato.

![](assets/mobile-vec-create-4.png)

**Gestire più versioni app**

Quando viene rilevata una nuova versione dell&#39;app, riceverete una notifica che la versione dell&#39;app è stata aggiunta all&#39;elenco di versioni mirate.

![Nuova notifica app](/help/c-target-mobile-app/c-mobile-visual-experience-composer/assets/manage-versions-notification-new.png)

Multiple mobile app versions can be added and removed manually from the [!UICONTROL Manage Versions] dialog box.

![Gestisci versione, finestra di dialogo](/help/c-target-mobile-app/c-mobile-visual-experience-composer/assets/manage-versions-dialog.png)

## Risoluzione dei problemi {#troubleshooting}

**Il Compositore esperienza visivo per app mobile notifica che l’app si è disconnessa.**

La tua connessione internet potrebbe essere scaduta. Riavvia l’applicazione quando internet ritorna disponibile e viene stabilita una nuova connessione. Consigliamo di creare un’attività in Compositore esperienza visivo per app mobile con una connessione Wi-Fi attiva.

**Il Compositore esperienza visivo per app mobile non è sincronizzato con la mia app mobile.**

Fai clic sul pulsante [!UICONTROL Aggiorna] nel Compositore esperienza visivo per sincronizzare la visualizzazione.

## Visualizzazioni di Target e applicazioni mobile {#target-views}

Il Compositore esperienza visivo per app mobile sfrutta una nuova concezione delle visualizzazioni: un gruppo logico di elementi visivi che insieme formano un’esperienza di app mobile.

**Introduzione alle visualizzazioni di Target**

Prendiamo come esempio un’app per l’acquisto di fiori. Questa app permette agli utenti di eseguire le seguenti attività:

* Elencare i fiori e i bouquet disponibili
* Visualizzare i dettagli
* Ordinare i fiori
* Controllare le impostazioni, ad esempio le opzioni di pagamento e gli indirizzi

In questa applicazione, ognuna di queste attività si può eseguire in uno schermo separato dell&#39;app mobile. Mentre gli utenti navigano all’interno dell’app, viene eseguito il rendering di uno schermo che consente loro di effettuare una delle seguenti attività. Se sei uno sviluppatore Android, molto probabilmente vorrai creare quattro diverse classi di attività, associando ognuna di queste a una delle attività.

In questo caso, ogni attività può essere considerata come una visualizzazione attraverso cui transita l’app mobile. Ci riferiremo a questi elementi come a visualizzazioni di Target, ognuna delle quali con una caratterizzazione univoca. Una visualizzazione di Target, o semplicemente visualizzazione, è un contenitore logico di elementi visivi che vengono mostrati sullo schermo mobile. Un esempio di visualizzazione è uno schermo o una classe di attività in Android.

Tuttavia, le app mobile sono raramente così semplici. Rendiamo l’esempio un po’ più realistico. Aggiungiamo alla prima attività, che elenca i fiori e i bouquet disponibili, la capacità di creare più layout e, quindi, diversi schermi. Ad esempio, aggiungiamo una funzione &quot;Ordina per&quot; con tre opzioni:

* Per popolarità
* Prezzo: da basso a alto
* Prezzo: da alto a basso

In questo esempio, ogni volta che un utente seleziona una diversa opzione di “Ordina per”, viene visualizzato un nuovo schermo, anche quando la classe di attività è la stessa. Ognuno di questi schermi può quindi essere considerato una visualizzazione di Target diversa.

In qualità di addetto al marketing, ti interessa creare diverse esperienze e lanciare diverse offerte in ognuna di queste visualizzazioni, senza dover chiedere agli sviluppatori di configurare mbox locali o utilizzare un ciclo di rilascio dell&#39;app.

## Configurazione del Compositore esperienza visivo per app mobile di Target {#setting-up}

Per abilitare il Compositore esperienza visivo per un’app mobile, gli sviluppatori devono effettuare le seguenti operazioni:

* Configurare l’estensione Adobe Target VEC in Launch
   * L’estensione VEC dipende dall’[estensione Adobe Target](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md). Verifica che l’estensione Adobe Target sia già configurata e abilitata.
* Aggiungi all’app l’estensione Adobe Target VEC.
   * [Android: configurazione dell&#39;app mobile](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-android.md)
   * [iOS: configurazione dell&#39;app mobile](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer-ios.md)

## Metodi di implementazione per il Compositore esperienza visivo di Target

L’estensione Adobe Target VEC recupera le esperienze Target rilevanti per l’app tramite una richiesta di rete. Le offerte vengono recuperate tramite questa chiamata di rete e applicate automaticamente sugli schermi di destinazione. Non vengono eseguite richieste di rete successive per recuperare esperienze VEC quando l’utente si sposta tra le diverse schermate dell’app.

Il comportamento predefinito dell’estensione consiste nell’effettuare una richiesta di rete sincrona (chiamata di blocco) al momento dell’avvio dell’applicazione. Puoi utilizzare Launch per controllare il comportamento di questa richiesta di rete per soddisfare il comportamento dell’applicazione.

### Attività di recupero automatico di Target

Questo è il comportamento predefinito in cui viene avviata automaticamente una richiesta di rete dall’estensione Adobe Target VEC. Puoi utilizzare una delle opzioni seguenti per richiedere una chiamata di blocco o una richiesta asincrona.

* Recupero in una chiamata sincrona (esecuzione in background disattivata)

   Quando è selezionata, l’estensione Adobe Target VEC effettua una richiesta di rete come chiamata di blocco all’avvio dell’applicazione. Le offerte vengono applicate immediatamente e nell’app non è presente alcuno sfarfallio. Questo è il comportamento predefinito dell’estensione.

* Recupero in una chiamata asincrona (esecuzione in background attivata)

   Quando è selezionata, l’estensione Adobe Target VEC effettua una richiesta di rete in background all’avvio dell’applicazione, ma non blocca il caricamento dell’app. Se le esperienze vengono create nella schermata iniziale dell’app, le offerte potrebbero non essere valide per la schermata iniziale se questa viene riprodotta prima del completamento della chiamata. Il rendering delle schermate dell’app viene generalmente identificato mediante gli eventi del ciclo di vita `didFinishLaunchingWithOptions` e `onActivityResumed` rispettivamente su iOS e Android. Le offerte si applicano automaticamente a tutte le schermate successive.

### Recuperare le attività Target a livello di programmazione

Puoi disattivare l’estensione Adobe Target VEC per effettuare automaticamente la richiesta di rete e decidere di richiamare l’estensione API a livello di programmazione. Questo offre agli sviluppatori il controllo su come desiderano integrare le offerte Adobe Target VEC nell’app. L’estensione Adobe Target VEC dispone di due metodi statici `prefetchOffers` e `prefetchOffersBackground` che possono essere utilizzati per recuperare in modo programmatico le offerte Adobe Target VEC.

* Il metodo `prefetchOffers` nasconde la schermata corrente fino al recupero delle offerte Adobe Target VEC. Le offerte vengono applicate automaticamente alla schermata corrente, se applicabile, e la schermata è nuovamente visibile.
* Il metodo `prefetchOffersBackground` non nasconde la schermata corrente e viene effettuata una chiamata per recuperare le offerte Target pertinenti. Le offerte di Target *non* vengono applicate alla schermata corrente e non si verifica alcuno sfarfallio. Quando l’utente passa alle schermate successive, le offerte vengono applicate automaticamente, a seconda delle necessità.

### Gestione delle limitazioni dell’area di lavoro di Target

Puoi impostare il valore `at_property` per l’area di lavoro utilizzando l’interfaccia di Launch. Questo garantisce che solo le attività in quell’area di lavoro vengano inviate all’app mobile.

## Linee guida generali per le chiamate API di Target {#section_C7276795F02540DCA230AEEDF882A833}

Per aggiungere in modo appropriato le visualizzazioni di Target per Android, qui trovi una semplice tabella che evidenzia le posizioni corrette in cui collocare le chiamate `targetView`:

| Posizioni accettabili per le TargetView | Sotto le aggiunte corrette |
|--- |--- |
| Alla fine di `Activity::onStart`, `Activity::onResume` | Spetta allo sviluppatore decidere se considerare `OnStart` e `OnResume` come `targetViews` uguali o diverse. Se vengono considerate uguali, utilizza lo stesso `viewName`. Se vengono considerate diverse, utilizza diversi `viewNames`. Questi eventi vengono aggiunti automaticamente dall’SDK. |
| Immediatamente dopo una chiamata `Activity::SetContent` | Se l&#39;interfaccia utente non viene modificata, possiamo inserire una chiamata `targetView`. |
| Dentro `View::willAppear` | Se la visualizzazione selezionata che appare si trova unicamente una specifica gerarchia di visualizzazione. |
| Immediatamente dopo una chiamata `Activity::SetContentView` | Se l&#39;attività non modifica uno dei suoi contenuti nel codice che segue. |

Per Android, qui trovi una tabella delle posizioni non corrette per le chiamate `targetView`:

| Posizioni per le TargetView non accettabili | Motivo |
|--- |--- |
| All’interno di `Activity::onCreate` | L’attività è stata creata ma la visualizzazione ad essa associata potrebbe non essere completa e/o collegata alla finestra. Questo posizionamento potrebbe fare sì che lo schermo di creazione non sia campionato o non lo sia in modo completo e/o che le offerte siano applicate in modo non deterministico. |
| Dentro `View::didAppear` | La visualizzazione è già apparsa e l&#39;applicazione dell&#39;offerta creerà un&#39;esperienza interfaccia utente di bassa qualità con visualizzazioni momentanee. |
| Dentro `View::didLoad` | La visualizzazione non è collegata alla gerarchia di visualizzazione principale e potrebbe essere creata un’istanza; tuttavia, è possibile che non venga mostrata sull’interfaccia utente dell&#39;app. |

## Consegna {#delivery}

Le attività Target create utilizzando il Compositore esperienza visivo per app mobile vengono consegnate automaticamente nelle app mobile. Queste attività vengono preacquisite all’avvio dell’app (basandosi sulla configurazione del lancio) e applicate mentre l’utente naviga attraverso diverse visualizzazioni di Target, che vengono spesso mappate direttamente sullo schermo.

Quando si chiama il metodo API `TargetVEC.prefetchOffersBackground()`, le offerte Target vengono recuperate da Target Edge e memorizzate nella cache locale. Ciò consente un’esperienza utente più fluida, poiché le offerte Target vengono immediatamente applicate dalla cache quando vengono attivate le visualizzazioni di Target con chiamate `targetView()`, anziché essere recuperate sulla rete.

Per una flessibilità aggiuntiva, puoi anche richiamare l’ API `TargetVEC.prefetchOffers()`, che prenasconde il layout corrente finché le offerte Target non vengono preacquisite e applicate alle visualizzazioni di Target visibili (con possibili sfarfallii).

`TargetVEC.prefetchOffersBackground()` può anche essere chiamato ripetutamente quando l&#39;utente sposta un&#39;applicazione per il cliente per aggiornare la cache dell&#39;offerta di Target locale con il contenuto più appropriato (seguendo gli ultimi aggiornamenti del profilo di Target dell&#39;utente corrente).

Tieni presente che ogni volta che un’offerta di Target viene precaricata, vengono applicate le offerte per l’ultima visualizzazione Target attivata con `AdobeTargetMobile.targetView()`, se possibile.

## Risoluzione dei problemi {#ts}

**Ho ricevuto un errore che indica che il valore &quot;context. application. name&quot; contiene caratteri non consentiti. What characters are allowed in mobile app names?**

I caratteri consentiti nei nomi degli app mobili includono:

| Caratteri consentiti | Descrizione |
| --- | --- |
| Lettere |  |
| Numeri |  |
| `-` | Trattino |
| `.` | Punto |
| `,` | Virgola |
| `:` | Due punti |
| `#` | Cancelletto |
| `(` | Parentesi aperta |
| `)` | Parentesi chiusura |
| `&` | Ampersand |
| `+` | Segno più |

Using a character that is not allowed, for example, an apostrophe ( `'` ) causes you to receive the following error message:

```
Target Response was received : {"status":400,"message":"Errors: field - [context.application.name] - Value contains prohibited chars;"}
```

## Limitazioni note {#limitations}

* Il Compositore esperienza visivo per app mobile, al momento, può essere utilizzato per creare attività [Test A/B](/help/c-activities/t-test-ab/test-ab.md) e [Targeting esperienze (XT)](/help/c-activities/t-experience-target/experience-target.md) per le app per dispositivi mobili. Il supporto per gli altri tipi di attività sarà disponibile in futuro.
* La funzione Anteprima non è ancora supportata. Sarà resa disponibile in una prossima versione.
* Quando tenti di ricollegare l’app al Compositore esperienza visivo per app mobile, devi uscire completamente dall’app e riavviarla.

   Se l&#39;applicazione mobile è già aperta durante uno degli scenari elencati di seguito, devi chiudere l&#39;applicazione e quindi riaprirla. Tuttavia, *è necessario* chiudere l&#39;applicazione dalla sezione delle applicazioni recenti e *senza* premere il pulsante Indietro. Se l&#39;applicazione viene chiusa premendo il pulsante Indietro, potrebbero verificarsi problemi di connessione.

   Per connettersi al Compositore esperienza visivo per app mobile, in alcune situazioni è necessario riavviare l’applicazione. Se l’applicazione è già aperta:

   * Quando crei una nuova attività, dopo aver selezionato l&#39;applicazione mobile, viene visualizzata la finestra di dialogo dell&#39;elenco dei dispositivi. Se l&#39;applicazione è già aperta, è necessario chiuderla e riavviarla per ottenere il proprio dispositivo disponibile per la selezione.
   * La finestra di dialogo del dispositivo viene visualizzata quando si inizia a modificare un&#39;attività. Se l&#39;applicazione è già aperta, è necessario chiuderla e riavviarla per ottenere il proprio dispositivo disponibile per la selezione.
   * La finestra di dialogo del dispositivo viene visualizzata quando si passa dal passaggio “Obiettivi e impostazioni” al passaggio “Creazione” (passaggio 1). Se l’applicazione è già aperta, è necessario chiuderla e riavviarla per riconnettersi al Compositore esperienza visivo per app mobile.
   Accertati di chiudere l&#39;applicazione dalla sezione delle applicazioni recenti e non premendo il pulsante [!UICONTROL Indietro].

## Training video: Adobe Target Mobile App Visual Experience Composer (3:33) {#video}

>[!VIDEO](https://video.tv.adobe.com/v/27528?captions=ita)