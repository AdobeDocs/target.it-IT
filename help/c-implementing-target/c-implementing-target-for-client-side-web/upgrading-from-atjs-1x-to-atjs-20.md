---
description: Aggiornamento da at.js 1.x a at.js 2.x
keywords: versioni di at.js;rilascio at.js; app a pagina singola;spa
seo-description: Informazioni dettagliate su come effettuare l’aggiornamento da Adobe Target at.js 1.x alla versione 2.0.0
seo-title: 'Aggiornare da Adobe Target at.js versione 1.x alla versione 2.0.0 '
solution: Target
subtopic: Introduzione
title: Aggiornamento da at.js 1.x a at.js 2.x
uuid: 3586af55-db15-4e68-90a7-d552338ec5e8
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Aggiornamento da at.js 1.x a at.js 2.x {#upgrading-from-atjs-1x-to-atjs-200}

La versione più recente di at.js in [!DNL Adobe Target] offre set di funzioni avanzate che consentono di eseguire personalizzazioni su tecnologie lato client di nuova generazione. Questa nuova versione si concentra sull&#39;aggiornamento di at.js per garantire interazioni in sintonia con le applicazioni a pagina singola.

Di seguito sono riportati alcuni vantaggi dell’utilizzo di at.js 2.x che non sono disponibili nelle versioni precedenti:

* La capacità di memorizzare nella cache tutte le offerte al caricamento di pagina per ridurre più chiamate al server a una singola chiamata al server.
* Migliora enormemente le esperienze degli utenti finali sul sito, in quanto le offerte appaiono immediatamente tramite la cache senza l’implementazione di chiamate al server tradizionali.
* Una semplice riga di codice e una configurazione per sviluppatori una tantum per consentire agli esperti di marketing di creare ed eseguire attività A/B e XT tramite il Compositore esperienza visivo sull’applicazione a pagina singola.

## Diagrammi di sistema di at.js 2.x

I seguenti diagrammi ti aiutano a comprendere il flusso di lavoro di at.js 2.x tramite Visualizzazioni e come questo migliori l’integrazione con le applicazioni a pagina singola. Per una migliore introduzione dei concetti utilizzati in at.js 2.x, consulta [Implementazione di un’applicazione a pagina singola](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md).

![Flusso di Target con at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/system-diagram-atjs-20.png)

| Chiamata | Dettagli |
| --- | --- |
| 1 | La chiamata restituisce l&#39;[!DNL Experience Cloud ID] se l’utente è autenticato; un’altra chiamata sincronizza l’ID cliente. |
| 2 | La libreria at.js viene caricata in modo sincrono e nasconde il corpo del documento.<br>at.js si carica anche in modo asincrono con un&#39;opzione che nasconde lo snippet implementato sulla pagina. |
| 3 | Si effettua una richiesta di caricamento della pagina, con tutti i parametri configurati (MCID, SDID e ID cliente). |
| 4 | Gli script di profilo vengono eseguiti e quindi inseriti nell’archivio profili. L’archivio richiede un pubblico idoneo dalla libreria Pubblico (ad esempio, pubblico condiviso da Adobe Analytics, Audience Manager, ecc.).<br>Gli attributi del cliente vengono inviati all’archivio profili in un processo batch. |
| 5 | In base ai parametri di richiesta dell’URL e ai dati di profilo, [!DNL Target] determina le attività ed esperienze da restituire al visitatore per la pagina corrente e le visualizzazioni future. |
| 6 | Il contenuto di destinazione viene rinviato alla pagina, includendo facoltativamente i valori di profilo per ulteriore personalizzazione.<br>Il contenuto mirato sulla pagina corrente viene mostrato il più rapidamente possibile senza che venga visualizzato momentaneamente il contenuto predefinito.<br>Contenuto mirato per le viste mostrate come risultato delle azioni dell&#39;utente in un’applicazione a pagina singola memorizzata nella cache del browser, in modo da applicarla immediatamente senza una chiamata al server aggiuntiva quando si attivano le viste tramite `triggerView()`. |
| 7 | I dati Analytics vengono inviati ai server di raccolta dati. |
| 8 | I dati di Target vengono confrontati con i dati di Analytics tramite SDID ed elaborati nell’archivio dei rapporti di Analytics.<br>I dati di Analytics possono quindi essere visualizzati sia in Analytics che in Target tramite i rapporti Analytics for Target (A4T). |

Ora, ovunque si implementi `triggerView()` nell’applicazione a pagina singola, le visualizzazioni e le azioni vengono recuperate dalla cache e mostrate all’utente senza una chiamata al server. `triggerView()` invia anche una richiesta di notifica al backend [!DNL Target] per incrementare e registrare i conteggi delle impression.

![Flusso di Target triggerView at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/atjs-20-triggerview.png)

| Chiamata | Dettagli |
| --- | --- |
| 1 | Si richiama `triggerView()` nell’applicazione a pagina singola per eseguire il rendering della visualizzazione e applicare azioni per modificare gli elementi visuali. |
| 2 | Il contenuto mirato per la visualizzazione viene letto dalla cache. |
| 3 | Il contenuto mirato viene mostrato il più rapidamente possibile senza che venga visualizzato momentaneamente il contenuto predefinito. |
| 4 | Si invia la richiesta di notifica all&#39;archivio profili di [!DNL Target] per conteggiare il visitatore nell&#39;attività e nelle metriche incrementali. |
| 5 | Dati di Analytics inviati ai server di raccolta dati. |
| 6 | I dati di Target vengono confrontati con i dati di Analytics tramite SDID e vengono elaborati nell’archivio dei rapporti di Analytics. È quindi possibile visualizzare i dati di Analytics sia in Analytics che in Target tramite i rapporti A4T. |

## Implementare at.js 2.x {#deploy-atjs-200}

1. Deploy at.js 2.x via the [Adobe Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md) extension.

   >[!NOTE]
   >
   > È preferibile distribuire at. js utilizzando Adobe Launch.

   Oppure

   Manually download at.js 2.x using the Target UI and deploy it using the [method of your choice](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/how-to-deployatjs.md).

## Funzioni at.js disattivate

In at.js 2.x sono state rimosse diverse funzioni.

>[!IMPORTANT]
>
>Se queste funzioni obsolete sono ancora in uso sul tuo sito quando viene implementato at.js 2.x, verranno visualizzati degli avvisi nella console. L’approccio consigliato durante l’aggiornamento consiste nel testare la distribuzione di at.js 2.x in un ambiente di verifica, assicurarsi di controllare tutti gli avvisi registrati nella console e tradurre le funzioni obsolete in nuove funzioni introdotte in at.js 2.x.

Di seguito puoi trovare le funzioni obsolete e i loro equivalenti. Per un elenco completo delle funzioni, consulta [Funzioni di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md).

>[!NOTE]
>at.js 2.x non nasconde più preventivamente in automatico gli elementi contrassegnati da `mboxDefault`. I clienti dovranno quindi nasconderli manualmente sul sito o tramite uno strumento di gestione dei tag.

### mboxCreate(mbox,params)

**Descrizione**:

Esegue una richiesta e applica l’offerta all’elemento DIV più vicino con il nome della classe `mboxDefault`.

**Esempio**:

```
<div class="mboxDefault">
  default content to replace by offer
</div>
<script>
  mboxCreate('mboxName','param1=value1','param2=value2');
</script>
```

**Equivalente in at.js 2.x**

Un’alternativa a `mboxCreate(mbox, params)` è `getOffer()` e `applyOffer()`.

**Esempio**:

```
<div class="mboxDefault"> 
  default content to replace by offer 
</div> 
<script> 
  var el = document.currentScript.previousElementSibling;
  adobe.target.getOffer({
    mbox: "mboxName",
    params: {
      param1: "value1",
      param2: "value2"
    },
    success: function(offer) {
      adobe.target.applyOffer({
        mbox: "mboxName",
        selector: el,
        offer: offer
      });
    },
    error: function(error) {
      console.error(error);
      el.style.visibility = "visible";
    }
  });
</script> 
```

### mboxDefine() e mboxUpdate()

**Descrizione**:

Crea una mappatura interna tra un elemento e un nome mbox, ma non esegue la richiesta. Utilizzata insieme a `mboxUpdate()`, che esegue la richiesta e applica l’offerta all’elemento identificato dal nodeId in `mboxDefine()`. Può essere utilizzato anche per aggiornare una mbox iniziata da `mboxCreate`.

**Esempio**:

```
<div id="someId" class="mboxDefault"></div>
<script>
 mboxDefine('someId','mboxName','param1=value1','param2=value2');
 mboxUpdate('mboxName','param3=value3','param4=value4');
</script>
```

**Equivalente in at.js 2.x**:

Un’alternativa a `mboxDefine()` e `mboxUpdate` è `getOffer()` e `applyOffer()`, con l’opzione del selettore utilizzata in `applyOffer()`. Questo approccio consente di mappare l’offerta su un elemento utilizzando qualsiasi selettore CSS, non solo uno con un ID.

**Esempio**:

```
<div id="someId" class="mboxDefault"> 
  default content to replace by offer 
</div> 
<script> 
  adobe.target.getOffer({
    mbox: "mboxName",
    params: {
      param1: "value1",
      param2: "value2",
      param3: "value3",
      param4: "value4" 
    },
    success: function(offer) {
      adobe.target.applyOffer({
        mbox: "mboxName",
        selector: "#someId",
        offer: offer
      });
    },
    error: function(error) {
      console.error(error);
      var el = document.getElementById("someId");
      el.style.visibility = "visible";
    }
  });
</script>
```

### adobe.target.registerExtension()

**Descrizione**:

Fornisce un metodo standard per registrare un’estensione specifica.

Questa funzione non è più supportata. Non utilizzarla.

## Riepilogo delle funzioni obsolete, nuove e supportate in at.js 2.0

| Metodo | Supportate? | Nuovo? | Obsoleta?<br>(apparirà il contenuto predefinito) |
| --- | --- | --- | --- |
| `getOffer()` | Sì |  |  |
| `getOffers()` |  | Sì |  |
| `applyOffer()` | Sì |  |  |
| `applyOffers()` |  | Sì |  |
| `triggerView()` |  | Sì |  |
| `trackEvent()` | Sì |  |  |
| `mboxCreate()` |  |  | Sì |
| `mboxDefine()`<br>`mboxUpdate()` |  |  | Sì |
| `targetGlobalSettings()` | Sì |  |  |
| `Data Providers` | Sì |  |  |
| `targetPageParams()` | Sì |  |  |
| `targetPageParamsAll()` | Sì |  |  |
| `registerExtension()` |  |  | Sì |
| `At.js Custom Events` | Sì |  |  |

## Limitazioni e callout

Tieni presente le limitazioni e i callout seguenti:

**Tracciamento delle conversioni**

I clienti che usano `mboxCreate()` per il tracciamento delle conversione devono utilizzare `trackEvent()` o `getOffer()`.

**Consegna delle offerte**

I clienti che non sostituiscono `mboxCreate()` con `getOffer()` o `applyOffer()` rischiano di riuscire a consegnare offerte.

**È possibile utilizzare at.js 2.x in alcune pagine e at.js 1.*x*o mbox.js in altre pagine?**

Sì, il profilo del visitatore è mantenuto su più pagine utilizzando diverse versioni e librerie. Il formato del cookie è lo stesso.

**Nuovo utilizzo dell’API in at.js 2.x**

at.js 2.x utilizza una nuova API, che chiamiamo API Delivery. Per eseguire il debug se at.js sta chiamando correttamente il server perimetrale [!DNL Target], filtra la scheda Rete degli strumenti per sviluppatori del tuo browser con “delivery”, “`tt.omtrdc.net`” o con il tuo codice client. Noterai inoltre che [!DNL Target] invia un payload JSON invece di coppie chiave-valore.

**Non si utilizza più la Mbox globale di Target**

In at.js 2.x, non vedrai più “`target-global-mbox`” chiaramente nelle chiamate di rete. Abbiamo invece sostituito la sintassi “`target-global-mbox`” con “`execute > pageLoad`” nel payload JSON inviato ai server [!DNL Target], come mostrato di seguito:

```
{
  "id": {
    // ...
  },
  "context": {
    "channel": "web",
    // ...
  },
  "execute": {
    "pageLoad": {}
  }
}
```

In sostanza, il concetto di mbox globale era stato introdotto per comunicare a [!DNL Target] se recuperare o meno offerte e contenuti al caricamento delle pagine. Nella nostra versione più recente, lo abbiamo reso più esplicito.

**Il nome della mbox globale in at.js ha ancora importanza?**

I clienti possono specificare un nome per la mbox globale tramite [!UICONTROL Target &gt; Configurazione &gt; Implementazione &gt; Modifica impostazioni at.js]. I server perimetrali [!DNL Target] utilizzano questa impostazione per tradurre execute &gt; pageload nel nome della mbox globale visualizzato nell’interfaccia utente [!DNL Target]. Questo consente ai clienti di continuare a utilizzare le API lato server, il compositore basato su moduli, gli script di profilo e creare tipi di pubblico utilizzando il nome della mbox globale. Inoltre, consigliamo vivamente di configurare lo stesso nome della mbox globale anche nella pagina [!UICONTROL Configurazione &gt; Preferenze], nel caso in cui si disponga di pagine che utilizzano ancora at.js 1.*x* o mbox.js, come mostrato nelle illustrazioni di seguito.

![Modificare la finestra di dialogo at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/modify-atjs.png)

e

![Mbox globale personalizzata](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/custom-global-mbox.png)

**È necessario attivare l’impostazione di creazione automatica di una mbox globale con at.js 2.x?**

Nella maggior parte dei casi, sì. Questa impostazione comunica a at.js 2.x di attivare una richiesta ai server perimetrali [!DNL Target] al momento del caricamento della pagina. Questa impostazione deve essere attiva perché la mbox globale si traduce in execution &gt; pageLoad, ma anche se desideri attivare una richiesta al caricamento della pagina.

**Le attività del Compositore esperienza visivo esistenti continueranno a funzionare, anche se il nome della mbox globale di Target non è specificato a partire da at.js 2.x?**

Sì, perché execute &gt; pageLoad è trattato sul backend [!DNL Target] come `target-global-mbox`.

**Se le mie attività basate su moduli sono mirate per`target-global-mbox`, queste continueranno a funzionare?**

Sì, perché execute &gt; pageLoad è trattato sui server perimetrali [!DNL Target] come `target-global-mbox`.

**Impostazioni di at.js 2.x supportate e non supportate**

| Impostazione | Supportate? |
| --- | --- |
| X-Domain | No |
| Creazione automatica di una mbox globale | Sì |
| Nome mbox globale | Sì |

**Il supporto per il monitoraggio tra più domini*non*è disponibile**

Il monitoraggio tra più domini consente di visualizzare sessioni su due siti correlati, ma con domini diversi, come una sessione singola. Ad esempio, potresti creare un’attività [!DNL Target] che si espande su `siteA.com` e `siteB.com` con il visitatore che resta nella stessa esperienza quando passa da un dominio all’altro. Questa funzionalità è legata al comportamento di cookie di terze parti e di prima parte di Target.

In [!DNL Target], il cookie di terze parti è memorizzato in `[CLIENTCODE].tt.omtrdc.net`, il cookie di prima parte in `clientdomain.com`. La prima richiesta restituisce intestazioni di risposta HTTP che tentano di impostare cookie di terze parti denominati `mboxSession` e `mboxPC`, mentre viene inviata nuovamente una richiesta di reindirizzamento con un parametro aggiuntivo (`mboxXDomainCheck=true`). Se il browser accetta cookie di terze parti, la richiesta di reindirizzamento li include e viene restituita l’offerta. Questo flusso di lavoro è possibile perché utilizziamo il metodo HTTP GET.

Tuttavia, con at.js 2.x non si utilizza più HTTP GET, ma HTTP POST. Il nuovo metodo serve a inviare payload JSON ai server perimetrali [!DNL Target]. Questo significa che ora la richiesta di reindirizzamento per verificare se un browser supporta i cookie di terze parti si interrompe. Questo perché le richieste HTTP GET sono transazioni idempotenti, mentre HTTP POST non lo è e non deve ripetersi arbitrariamente. Pertanto, il supporto del monitoraggio tra più domini non è più disponibile in at.js 2.x.

**È disponibile il supporto della creazione automatica di una mbox globale**

Questa impostazione comunica a at.js 2.x di attivare una richiesta ai server perimetrali [!DNL Target] al momento del caricamento della pagina. Poiché la mbox globale è convertita in execute &gt; pageLoad e interpretata dai server perimetrali [!DNL Target], i clienti devono attivarla se desiderano avviare una richiesta al caricamento della pagina.

**Supporto del nome mbox globale disponibile**

I clienti possono specificare un nome per la mbox globale tramite [!UICONTROL Target &gt; Configurazione &gt; Implementazione &gt; Modifica impostazioni at.js]. I server perimetrali [!DNL Target] utilizzano questa impostazione per tradurre execute &gt; pageLoad nel nome della mbox globale immesso. Questo consente ai clienti di continuare a utilizzare le API lato server, il compositore basato su moduli, gli script di profilo e creare tipi di pubblico mirati per la mbox globale.

**I seguenti eventi personalizzati at.js sono applicabili a`triggerView()`o valgono solo per`applyOffer()`o`applyOffers()`?**

* `adobe.target.event.CONTENT_RENDERING_FAILED`
* `adobe.target.event.CONTENT_RENDERING_SUCCEEDED`
* `adobe.target.event.CONTENT_RENDERING_NO_OFFERS`
* `adobe.target.event.CONTENT_RENDERING_REDIRECT`

Sì, gli eventi personalizzati at.js sono applicabili anche a `triggerView()`.

**Quando richiamo`triggerView()`con`{“page” : “true”}`, dice che invierà una notifica al backend[!DNL Target]e aumenterà le impression. Questo provocherà anche l’esecuzione degli script di profilo?**

Quando si effettua una chiamata di preacquisizione al backend [!DNL Target], avviene l’esecuzione degli script di profilo. Successivamente, i dati del profilo interessati saranno crittografati e trasmessi nuovamente al lato client. Dopo la chiamata di `triggerView()` con `{"page": "true"}`, si invierà una notifica insieme ai dati di profilo codificati. Questo si verifica quando il backend [!DNL Target] deciderà di decodificare i dati di profilo e archiviarli nei database.

**Per gestire la visualizzazione temporanea di altri contenuti è necessario aggiungere codice per nasconderli anticipatamente prima di richiamare`triggerView()`?**

No, non è necessario aggiungere codice per nascondere contenuti anticipatamente prima di richiamare `triggerView()`. at.js 2.x gestisce la logica relativa ai contenuti nascosti anticipatamente e visualizzati temporaneamente prima di mostrare e applicare la visualizzazione.

## Compatibilità di at.js

Le tabelle seguenti contengono una spiegazione di at.js. Compatibilità della versione 2.0.0 con tipi di attività, integrazioni, funzionalità e funzioni di at.js diverse.

### Tipi di attività {#types}

| Type (Tipo) | Supportate? |
| --- | --- |
| Test A/B | Sì |
| Allocazione automatica | Sì |
| Targeting automatico | Sì |
| Targeting esperienza | Sì |
| Test multivariato | Sì |
| Personalizzazione automatizzata | Sì |
| Consigli | Sì |

>[!NOTE]
>
>Quando tutte le modifiche vengono applicate al `Page Load Event`, le attività di targeting automatico sono supportate tramite at.js 2.x e il Compositore esperienza visivo. Quando vengono aggiunte modifiche a particolari viste, sono supportate solo le attività A/B Test, Allocazione automatica e Targeting esperienze (XT).

### Integrazioni {#integrations}

| Type (Tipo) | Supportate? |
| --- | --- |
| Analytics for Target (A4T) | Sì |
| Tipi di pubblico | Sì |
| Attributi del cliente | Sì |
| Frammenti esperienza AEM | Sì |
| Estensione Adobe Launch | [Sì](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md) |
| Strumento di debug | Sì |
| Auditor | Le regole per at.js 2.x non sono ancora state aggiornate |
| Dynamic Tag Manager (DTM) | Sì |
| Opt-in | No. Opt-in support for [GDPR](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md) is supported in [at.js version 2.1.0](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md). |
| Personalizzazione avanzata AEM fornita da Adobe Target | No |

### Funzioni

| Funzione | Supportate? |
| --- | --- |
| X-Domain | No |
| Proprietà/Aree di lavoro | Sì |
| Collegamenti QA | Sì |
| Compositore esperienza basato su moduli | Sì |
| Compositore esperienza visivo | Sì |
| Codice personalizzato | Sì |
| Token di risposta | [Sì](#response-tokens) |
| Tracciamento dei clic | Sì |
| Consegna di più attività | Sì |
| targetGlobalSettings | Sì (ma non dominio x) |
| Metodi at.js | È disponibile il supporto per tutto, a eccezione di<br>`mboxCreate()`<br>`mboxUpdate()`<br>`mboxDefine()`<br>che visualizzeranno il contenuto predefinito. |

### Parametri stringa di query

| Parametro | Supportate? |
| --- | --- |
| `?mboxDisable` | Sì |
| `?mboxDisable` | Sì |
| `?mboxTrace` | Sì |
| `?mboxSession` | No |
| `?mboxOverride.browserIp` | No |

## Token di risposta {#response-tokens}

at.js 2.*x*, esattamente come at.js 1.*x*, utilizza l’evento personalizzato `at-request-succeeded` per ottenere i token di risposta. Per esempi di codice con l’evento `at-request-succeeded` personalizzato, consulta [Token di risposta](/help/administrating-target/response-tokens.md).

## Parametri di at.js 1.x in corrispondenza della mappatura payload di at.js 2.x {#payload-mapping}

Questa sezione delinea le mappature tra at.js 1.*x* e at.js 2.x.

Prima di passare alla mappatura dei parametri, gli endpoint utilizzati da queste versioni della libreria sono cambiati:

* at.js 1.*x* - `http://<client code>.tt.omtrdc.net/m2/<client code>/mbox/json`
* at.js 2.x - `http://<client code>.tt.omtrdc.net/rest/v1/delivery`

Un’altra differenza significativa è che:

* at.js 1.*x* - Il codice client è parte del percorso
* at.js 2.x - Il codice client viene inviato come parametro della stringa query, ad esempio:
   `http://<client code>.tt.omtrdc.net/rest/v1/delivery?client=democlient`

Le seguenti sezioni riportano tutte nell’elenco il parametro di at.js 1.*x*, la sua descrizione e il corrispondente payload JSON 2.0.0 (se applicabile):

### at_property

(parametro di at.js 1.*x*)

Utilizzato per le [autorizzazioni per gli utenti Enterprise](/help/administrating-target/c-user-management/property-channel/property-channel.md).

```
{
  ....
  "property": {
    "token": "1213213123122313121"
  }
  ....
}
```

### browserHeight

(parametro di at.js 1.*x*)

Altezza della finestra del browser del visitatore.

Payload JSON di at.js 2.x:

```
{
  "context": {
    "window": {
       "height": 200
    }
  }
}
```

### browserWidth

(parametro di at.js 1.*x*)

Larghezza della finestra del browser del visitatore.

Payload JSON di at.js 2.x:

```
{
  "context": {
    "window": {
       "width": 200
    }
  }
}
```

### browserTimeOffset

(parametro di at.js 1.*x*)

Offset fuso orario.

Payload JSON di at.js 2.x:

```
{
  "context": {
    "timeOffsetInMinutes": -480
  }
}
```

### screenHeight

(parametro di at.js 1.*x*)

Altezza della schermata del visitatore.

Payload JSON di at.js 2.x:

```
{
  "context": {
    "screen": {
       "height": 200
    }
  }
}
```

### screenWidth

(parametro di at.js 1.*x*)

Larghezza della schermata del visitatore.

Payload JSON di at.js 2.x:

```
{
  "context": {
    "screen": {
       "width": 200
    }
  }
}
```

### colorDepth

(parametro di at.js 1.*x*)

Profondità colore della schermata del visitatore.

Payload JSON di at.js 2.x:

```
{
  "context": {
    "screen": {
       "colorDepth": 24
    }
  }
}
```

### mboxHost

(parametro di at.js 1.*x*)

Dominio della pagina in cui viene eseguita la libreria di Target.

Payload JSON di at.js 2.x:

```
{
  "context": {
    "browser": {
       "host": "test.com"
    }
  }
}
```

### webGLRenderer

(parametro di at.js 1.*x*)

Funzionalità del rendering GL WEB del browser. Questo viene usato dal nostro meccanismo di rilevamento del dispositivo per determinare se il dispositivo del visitatore è un computer desktop, un iPhone, un dispositivo Android, ecc.

Payload JSON di at.js 2.x:

```
{
  "context": {
    "browser": {
       "webGLRenderer": "AMD Radeon Pro 560X OpenGL Engine"
    }
  }
}
```

### mboxURL

(parametro di at.js 1.*x*)

URL della pagina.

Payload JSON di at.js 2.x:

```
{
  "context": {
    "address": {
       "url": "http://test.com"
    }
  }
}
```

### mboxReferrer

(parametro di at.js 1.*x*)

Riferimento (provenienza) della pagina.

Payload JSON di at.js 2.x:

```
{
  "context": {
    "address": {
       "referringUrl": "http://google.com"
    }
  }
}
```

### mbox (il nome) è uguale a mbox globale

(parametro di at.js 1.*x*)

L’API della consegna non dispone più di un concetto mbox globale. Nel payload JSON devi usare `execute > pageLoad`.

Payload JSON di at.js 2.x:

```
{
  "execute": {
    "pageLoad": {
       "parameters": ....
       "profileParameters": ...
       .....
    }
  }
}
```

### mbox (il nome) *non* è uguale a mbox globale

(parametro di at.js 1.*x*)

Per utilizzare il nome di una mbox, trasmettilo a `execute > mboxes`. Una mbox richiede un indice e un nome.

Payload JSON di at.js 2.x:

```
{
  "execute": {
    "mboxes": [{
       "index": 0,
       "name": "some-mbox",
       "parameters": ....
       "profileParameters": ...
       .....
    }]
  }
}
```

### mboxId

(parametro di at.js 1.*x*)

Non più utilizzato.

### mboxCount

(parametro di at.js 1.*x*)

Non più utilizzato.

### mboxRid

(parametro di at.js 1.*x*)

ID della richiesta utilizzato dai sistemi a valle per facilitare il debug.

Payload JSON di at.js 2.x:

```
{
  "requestId": "2412234442342"
  ....
}
```

### mboxTime

(parametro di at.js 1.*x*)

Non più utilizzato.

### mboxSession

(parametro di at.js 1.*x*)

L’ID della sessione viene inviato come parametro della stringa di query (`sessionId`) all’endpoint API di consegna.

### mboxPC

(parametro di at.js 1.*x*)

L’ID TNT viene trasmesso in `id > tntId`.

Payload JSON di at.js 2.x:

```
{
  "id": {
    "tntId": "ca5ddd7e33504c58b70d45d0368bcc70.21_3"
  }
  ....
}
```

### mboxMCGVID

(parametro di at.js 1.*x*)

L’ID del visitatore di Experience Cloud viene trasmesso in `id > marketingCloudVisitorId`.

Payload JSON di at.js 2.x:

```
{
  "id": {
    "marketingCloudVisitorId": "797110122341429343505"
  }
  ....
}
```

### vst.aaaa.id e vst.aaaa.authState

(parametro di at.js 1.*x*)

Gli ID cliente devono essere trasmessi in `id > customerIds`.

Payload JSON di at.js 2.x:

```
{
  "id": {
    "customerIds": [{
       "id": "1232131",
       "integrationCode": "aaaa",
       "authenticatedState": "....."
     }]
  }
  ....
}
```

### mbox3rdPartyId

(parametro di at.js 1.*x*)

ID di terze parti del cliente utilizzato per collegare diversi ID di Target.

Payload JSON di at.js 2.x:

```
{
  "id": {
    "thirdPartyId": "1232312323123"
  }
  ....
}
```

### mboxMCSDID

(parametro di at.js 1.*x*)

SDID, noto anche come ID di dati supplementari. Deve essere trasmesso in `experienceCloud > analytics > supplementalDataId`.

Payload JSON di at.js 2.x:

```
{
  "experienceCloud": {
    "analytics": {
      "supplementalDataId": "1212321132123131"
    }
  }
  ....
}
```

### vst.trk

(parametro di at.js 1.*x*)

Server di tracciamento di Analytics. Deve essere trasmesso in `experienceCloud > analytics > trackingServer`.

Payload JSON di at.js 2.x:

```
{
  "experienceCloud": {
    "analytics": {
      "trackingServer": "analytics.test.com"
    }
  }
  ....
}
```

### vst.trks

(parametro di at.js 1.*x*)

Server di tracciamento sicuro di Analytics. Deve essere trasmesso in `experienceCloud > analytics > trackingServerSecure`.

Payload JSON di at.js 2.x:

```
{
  "experienceCloud": {
    "analytics": {
      "trackingServerSecure": "secure-analytics.test.com"
    }
  }
  ....
}
```

### mboxMCGLH

(parametro di at.js 1.*x*)

Hint di posizione di Audience Manager. Deve essere trasmesso in `experienceCloud > audienceManager > locationHint`.

Payload JSON di at.js 2.x:

```
{
  "experienceCloud": {
    "audienceManager": {
      "locationHint": 9
    }
  }
  ....
}
```

### mboxAAMB

(parametro di at.js 1.*x*)

Blob Audience Manager. Deve essere trasmesso in `experienceCloud > audienceManager > blob`.

Payload JSON di at.js 2.x:

```
{
  "experienceCloud": {
    "audienceManager": {
      "blob": "2142342343242342"
    }
  }
  ....
}
```

### mboxVersion

(parametro di at.js 1.*x*)

La versione viene inviata come parametro della stringa di query tramite il parametro della versione.

## Video di formazione: diagramma architetturale di at.js 2.x

at.js 2.x migliora il supporto di Adobe Target per le applicazioni a pagina singola e consente l’integrazione con altre soluzioni Experience Cloud. Questo video spiega come sono stati uniti questi elementi.

>[!VIDEO](https://video.tv.adobe.com/v/26250?captions=ita)

See [Understanding how at.js 2.x works](https://helpx.adobe.com/target/kt/using/atjs20-diagram-technical-video-understand.html) for more information.