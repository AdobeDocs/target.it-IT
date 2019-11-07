---
keywords: e-mail;ESP;provider di servizi di posta elettronica;rawbox;API di consegna;modello di solo download;modello di posta elettronica;elaborazione batch;e-mail build-time
description: Informazioni su come integrare le e-mail con i Consigli.
title: Integrare i Consigli con l’e-mail
topic: Consigli
uuid: ae137d7c-58c5-4601-92fc-2dc5548760fd
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# ![PREMIUM](/help/assets/premium.png) Integrare Consigli con l’e-mail{#integrate-recommendations-with-email}

Informazioni su come integrare le e-mail con i Consigli.

Le capacità del fornitore di servizi di posta elettronica determinano il metodo da utilizzare. Il responsabile commerciale di riferimento o consulente di riferimento può aiutarti a scegliere l'opzione che funzionerà al meglio per te.

## Opzione 1: utilizzare l'API di consegna {#section_9F00D271BABA4B7390B461F4C44EC319}

L'API di consegna è una richiesta POST che funziona con e-mail di build-time. Questa opzione è il metodo preferito per l'e-mail di build-time.

La maggior parte dei client di posta elettronica non consentono richieste POST; pertanto, questa API non è consigliata per i casi di utilizzo a tempo aperto. Alcuni client di posta elettronica, come ad esempio Gmail o Outlook, potrebbero memorizzare nella cache il contenuto o bloccare l'immagine e richiedere al destinatario di consentire all'immagine di eseguire il rendering in modo attivo.

Non è possibile restituire il contenuto predefinito utilizzando l'API di consegna.

Il codice seguente è una richiesta di distribuzione dell'API di esempio:

```
curl -X POST \ 
  'https://clientcode.tt.omtrdc.net/rest/v1/mbox/?client=clientcode' \ 
  -H 'authorization: Bearer 3423614b-4843-4664-83c4-c6c3f6c8869b' \ 
  -H 'cache-control: no-cache' \ 
  -H 'content-type: application/json' \ 
  -d '{ 
  "mbox" : "email-mbox", 
  "tntId" : "111499796294071-449025.28_44", 
  "requestLocation" : { 
    "host" : "prod" 
  }, 
   "profileParameters" : { 
   }, 
  "mboxParameters" : { 
    "at_property": "b468a242-64a4-32a0-ca0c-890bddd78789", 
    "entity.id": "article-123", 
    "entity.event.detailsOnly" : "true" 
  } 
  "contentAsJson":  true 
}'
```

Dove `clientcode` è il codice del client Target.

>[!NOTE]
>
>Assicurati di fornire un valore univoco per `sessionId` e uno tra `tntId` o `thirdPartyId` per ogni destinatario e-mail (ad esempio, per ogni chiamata API). Se non fornisci valori univoci per questi campi, la risposta API potrebbe rallentare o non riuscire a causa del numero elevato di eventi generati in un singolo profilo.

Per ulteriori informazioni, consulta [Documentazione sulle API di consegna](https://developers.adobetarget.com/api/#server-side-delivery).

## Opzione 2: utilizzare un modello di e-mail Rawbox {#section_C0D48A42BCCE45D6A68852F722C7C352}

Un rawbox è simile a una richiesta mbox, ma per ambienti non Web, come ad esempio provider di servizi di posta elettronica (ESP). Poiché non disponi di [!DNL mbox.js] o [!DNL at.js] da utilizzare nelle richieste rawbox, devi creare le richieste manualmente. Gli esempi qui sotto spiegano come lavorare con le richieste rawbox in e-mail.

Questo approccio ti consente di monitorare le prestazioni dei consigli nelle e-mail, sottoporli normalmente a test con un consiglio e continuare il monitoraggio sul sito.

Configura un’attività [!DNL Recommendations] in [!DNL Adobe Target] utilizzando l’opzione [Compositore esperienza basata su modulo](../../c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E). Per il percorso, seleziona il nome dell'elemento mbox che hai deciso di utilizzare nella richiesta rawbox proveniente dall'ESP. Seleziona una progettazione con l'aspetto che desideri per la tua e-mail. Al momento della compilazione dell'e-mail, l'ESP effettua una chiamata ai server di [!DNL Adobe Target] per ogni rawbox in ogni e-mail che viene generata. L'ESP deve disporre di un modo per includere l'HTML restituito nell'e-mail quando viene inviato.

Il sistema di posta elettronica utilizzato deve essere in grado di gestire questi scenari:

**Viene ricevuta una risposta valida, ma non sono presenti consigli.**

* In questo caso, la risposta sarà qualsiasi cosa impostata come valore del parametro mboxDefault. Vedi la spiegazione riportata di seguito su questo parametro.
* Il fornitore di posta elettronica deve disporre di un blocco HTML predefinito per i consigli da utilizzare in questo caso.

**Il server Target riceve un timeout e restituisce senza dati.**

* In questo caso, il server Target restituirà il seguente contenuto:

   `//ERROR: application server timeout`

* L'applicazione di posta elettronica deve cercare quel testo ed essere in grado di gestire l'errore. Il provider di posta elettronica dispone di più opzioni per gestire questo caso:

   * Provare immediatamente un'altra chiamata del server (consigliato, possibilmente con un contatore di tentativi).
   * Escludere quella particolare e-mail e passare a quella successiva.
   * Mettere in coda quella particolare e-mail ed eseguire nuovamente le e-mail fallite come batch alla fine dell'esecuzione iniziale.

**URL di richiesta di esempio:**

```
https://client_code.tt.omtrdc.net/m2/client_code/ubox/raw?mbox=mbox_name&mboxSession=1396032094853-955654&mboxPC=1396032094853-955654&mboxXDomain=disabled&entity.event.detailsOnly=true&mboxDefault=nocontent&mboxNoRedirect=1&entity.id=2A229&entity.categoryId=5674
```

**Parametri richiesti:**

>[!NOTE]
>
>Per utilizzare [!DNL Recommendations] nelle e-mail, la chiamata rawbox di solito deve includere `entity.id` o `entity.categoryId` o entrambi, a seconda del tipo di criteri per i consigli. La chiamata di esempio qui sopra include entrambi.

| Parametro | Valore | Descrizione | Convalida |
|--- |--- |--- |--- |
| `client_code` | *client_code* | Il codice del client utilizzato nella funzione Consigli. Il tuo consulente Adobe può fornire questo valore. |  |
| `mbox` | *mboxName* | Il nome mbox che viene utilizzato per il targeting. | Stessa convalida come per tutte le chiamate mbox.<br>Limite di 250 caratteri.<br>Non può contenere i seguenti caratteri: `', ", %22, %27, <, >, %3C, %3E` |
| `mboxXDomain` | disabilitato | Impedisce che la risposta imposti un cookie in ambienti non Web. |  |
| `entity.id`<br>(Richiesto per determinati tipi di criteri: view/view, view/bought, bought/bought) | *entity_id* | Il productId sul quale il consiglio è basato, come ad esempio un prodotto abbandonato nel carrello o un acquisto precedente.<br>Se richiesto dai criteri, la chiamata rawbox deve includere `entity.id`. |  |
| `entity.event.detailsOnly` | true | Se viene passato `entity.id`, è consigliabile passare anche questo parametro per impedire che la richiesta incrementi il numero di visualizzazioni di pagina conteggiate per un elemento, in modo da non alterare gli algoritmi basati sulla visualizzazione del prodotto. |  |
| `entity.categoryId`<br>(Richiesto per determinati tipi di criteri: più visti per categoria e più venduti per categoria) | *category_id* | La categoria su cui si basa il consiglio, ad esempio i più venduti in una categoria.<br>Se richiesto dai criteri, la chiamata rawbox deve includere `entity.categoryId`. |  |
| `mboxDefault` | *`https://www.default.com`* | Se il parametro `mboxNoRedirect` non è presente, `mboxDefault` deve essere un URL assoluto che restituirà contenuto predefinito se non è disponibile alcun consiglio. Può trattarsi di un'immagine o di un altro contenuto statico.<br>Se il parametro `mboxNoRedirect` è presente, `mboxDefault` può essere qualsiasi testo che indichi che non vi sono consigli, ad esempio `no_content`.<br>Il provider di posta elettronica dovrà gestire il caso in cui questo valore viene restituito e inserire un HTML predefinito nell'e-mail. |  |
| `mboxHost` | *mbox_host* | Si tratta del dominio che viene aggiunto all'ambiente predefinito (gruppo di host) quando la chiamata viene attivata. |  |
| `mboxPC` | Vuoto | (Richiesto per i consigli che utilizzano il profilo di un visitatore.)<br>Se non è stato fornito alcun “thirdPartyId”, viene generato un nuovo tntId e viene restituito come parte della risposta. Altrimenti rimane vuoto.<br>**Nota**: assicurati di fornire un valore univoco di `mboxSession` e `mboxPC` per ciascun destinatario e-mail (ad esempio, per ogni chiamata API). Se non fornisci valori univoci per questi campi, la risposta API potrebbe rallentare o non riuscire a causa del numero elevato di eventi generati in un singolo profilo. | 1 &lt; Lunghezza &lt; 128<br>Non può contenere più di un singolo “.” (punto).<br>L'unico punto consentito è per il suffisso di posizione del profilo. |

**Parametri opzionali**:

| Parametro | Valore | Descrizione | Convalida |
|--- |--- |--- |--- |
| `mboxPC`<br>(Facoltativo) | *mboxPCId* | ID visitatore di Target. Utilizza questo valore se desideri monitorare un utente in modo completo sul sito nell'arco di più visite o quando utilizzi un parametro di profilo utente.<br>Questo valore deve essere l'effettivo PCID di Adobe Target per l'utente, che verrebbe esportato dal sito Web al CRM. Il provider di posta elettronica recupererà questo ID dal CRM o dal data warehouse e lo utilizzerà per il valore di questo parametro.<br>Il valore `mboxPC` è utile anche per monitorare il comportamento dei visitatori sul sito nell'arco di più visite per il tracciamento delle metriche quando un consiglio fa parte di un'attività A/B.<br>**Nota**: assicurati di fornire un valore univoco di `mboxSession` e `mboxPC` per ciascun destinatario e-mail (ad esempio, per ogni chiamata API). Se non fornisci valori univoci per questi campi, la risposta API potrebbe rallentare o non riuscire a causa del numero elevato di eventi generati in un singolo profilo. | 1 &lt; Lunghezza &lt; 128<br>Non può contenere più di un singolo “.” (punto).<br>L'unico punto consentito è per il suffisso di posizione del profilo. |
| `mboxNoRedirect`<br>(Facoltativo) | 1 | Per impostazione predefinita, il chiamante viene reindirizzato quando non viene trovato alcun contenuto finale. Utilizzalo per disabilitare il comportamento predefinito. |  |
| `mbox3rdPartyId` | *xxx* | Utilizzalo se disponi di un ID visitatore personalizzato da utilizzare per il targeting del profilo. |  |

**Potenziali risposte del server Target**:

| Risposta | Descrizione |
|--- |--- |
| //ERRORE: | Generato dal bilanciamento del carico quando non può restituire il contenuto |
| success | Il parametro `mboxNoRedirect` è impostato su “true” e il server non restituisce alcun consiglio (ad esempio, non vi è alcuna corrispondenza per l’elemento mbox o la cache del server non è inizializzata). |
| richiesta errata | Il parametro `mbox` è mancante.<ul><li>Il parametro `mboxDefault` o `mboxNoRedirect` non è specificato.</li><li>Il parametro di richiesta `mboxTrace` è specificato ma `mboxNoRedirect` non lo è.</li><li>Il parametro `mboxTarget` non viene specificato quando i nomi mbox terminano con il suffisso `-clicked`.</li></ul> |
| `Cannot redirect to default content, please specify mboxDefault parameter` | `mboxDefault` non viene specificato quando non esiste alcuna corrispondenza per la richiesta e il parametro `mboxNoRedirect` non è specificato. |
| `Invalid mbox name:= MBOX_NAME` | Indica che il parametro `mbox` contiene caratteri non validi. |
| `Mbox name [MBOX_NAME] is too long` | Indica che il parametro `mbox` è più lungo di 250 caratteri. |

## Opzione 3: utilizzare il modello di solo download {#section_518C279AF0094BE780F4EA40A832A164}

Configura un consiglio come al solito, ma scegli **solo download** nella sezione di presentazione, anziché una combinazione di modello e mbox. Quindi, in ESP, indica al sistema l'ID del consiglio creato. ESP accede ai dati del consiglio tramite API. Questi dati mostrano quali elementi devono essere consigliati per una particolare categoria o elemento chiave, come ad esempio gli elementi in un carrello abbandonato. ESP memorizza questi dati, li collega all'aspetto e alle caratteristiche relativi, visualizza le informazioni su ciascun elemento e le distribuisce nelle e-mail.

Con questa opzione, il server dei consigli non è in grado di monitorare direttamente le prestazioni di un consiglio o di suddividere il traffico tra più combinazioni di algoritmo/modello. Inoltre, i consigli non sono legati al profilo di un visitatore.

Per ulteriori informazioni sull'API di download, vedi [API Legacy &gt; Download](../../assets/adobe-recommendations-classic.pdf).
