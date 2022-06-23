---
keywords: e-mail;ESP;provider di servizi di posta elettronica;rawbox;API di consegna;modello di solo download;modello di posta elettronica;elaborazione batch;e-mail build-time
description: Scopri come integrare le e-mail con le API di consegna di Adobe [!DNL Target Recommendations], including using the [!DNL Target] , modelli rawbox e modelli di solo download.
title: Come posso integrare Consigli con l’e-mail?
feature: Recommendations
exl-id: 08fcb507-2c91-444a-b8ac-26165e359f6f
source-git-commit: a0a20b99a76ba0346f00e3841a345e916ffde8ea
workflow-type: tm+mt
source-wordcount: '1715'
ht-degree: 99%

---

# ![PREMIUM](/help/main/assets/premium.png) Integrare [!DNL Recommendations] con l’e-mail 

[!DNL Adobe Target] supporta la personalizzazione in fase di invio dei consigli nelle e-mail.

Sono disponibili tre metodi di integrazione [!DNL Target Recommendations] con il provider di servizi e-mail (ESP). Il metodo scelto dipende dalle funzionalità del proprio ESP. L’account manager o il consulente di riferimento può aiutarti a scegliere l’opzione più adatta alle tue esigenze.

| Metodo | Dettagli |
| --- | --- |
| [Metodo 1: [!DNL Adobe Target Delivery API]](#delivery-api) (preferito) | Utilizza [!DNL Adobe Target Delivery API] per effettuare richieste per cliente/per e-mail per le attività Consigli. |
| [Metodo 2: [!DNL Adobe Rawbox API]](#rawbox) | Utilizza [!DNL Adobe Target Rawbox API] per effettuare richieste per cliente/per e-mail per le attività Consigli. |
| [Metodo 3: [!DNL Recommendations Download API]](#download-api) | Utilizza Recommendations Download API per richiedere consigli in serie per un elenco di prodotti o categorie in formato CSV. |

Per i metodi 1 e 2, il tuo ESP deve effettuare chiamate a un’API esterna per cliente/per e-mail e attendedere che venga restituito il contenuto appropriato. Questi metodi non sono supportati da tutt gli ESP; contatta il tuo ESP per determinare se è compatibile con questo modello di integrazione.

Per il metodo 3, il tuo ESP deve unre all’elenco delle e-mail un elenco di consigli per ID prodotto o ID categoria. Questo metodo può essere basato su un attribut, ad esempio ultimo prodotto visualizzato dal cliente, ultimo prodotto acquistato o la categoria più visualizzata. Tuttavia, per eseguire l’unione di tali elenchi, l’ESP deve avere accesso a questi dati nel suo profilo cliente. Contatta il tuo ESP per determinare se ha accesso a questi dati e se è compatibile con questo modello di integrazione.

La personalizzazione dei consigli in base all’ora di apertura non è supportata da [!DNL Adobe Target].

>[!IMPORTANT]
>
>Le seguenti linee guida sulla capacità si applicano ai metodi modelli e-mail con API di consegna e con modelli e-mail rawbox, descritti di seguito (metodi 1 e 2):
>
>* Le richieste devono essere limitate al minore tra i seguenti valori: 1.000 richieste al secondo o 25 volte il traffico giornaliero di picco.
>* Il traffico deve essere scaglionato in porzioni di 200 richieste al secondo al minuto.
> 
>Se desideri utilizzare limiti più elevati, contatta il tuo account manager.

## Metodo 1 - Utilizzare le API di consegna (preferito) {#delivery-api}

L&#39;API di consegna è una richiesta POST che funziona con e-mail di build-time. Questa opzione è il metodo preferito per l&#39;e-mail di build-time.

La maggior parte dei client di posta elettronica non consentono richieste POST. Questa API non è quindi consigliata per i casi di utilizzo a tempo aperto. Alcuni client di posta elettronica, come ad esempio Gmail o Outlook, potrebbero memorizzare nella cache il contenuto o bloccare l’immagine e richiedere al destinatario di consentire all’immagine di eseguire il rendering in modo attivo.

Non è possibile restituire il contenuto predefinito utilizzando l&#39;API di consegna.

Il codice seguente è una richiesta di distribuzione dell&#39;API di esempio:

```javascript
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

Dove `clientcode` è il codice del client [!DNL Target].

>[!NOTE]
>
>Assicurati di fornire un valore univoco per `sessionId` e uno tra `tntId` o `thirdPartyId` per ogni destinatario e-mail (ad esempio, per ogni chiamata API). Se non fornisci valori univoci per questi campi, la risposta API potrebbe risultare lenta o non riuscire a causa del numero elevato di eventi generati in un singolo profilo.

Vedi [Documentazione API di consegna](https://developer.adobe.com/target/implement/delivery-api/){target=_blank} per ulteriori informazioni.

## Metodo 2 - Utilizzare un modello di e-mail rawbox {#rawbox}

Un rawbox è simile a una richiesta mbox, ma per ambienti non web, come ad esempio i provider di servizi e-mail (ESP). Poiché non disponi di [!DNL Adobe Experience Platform Web SDK] o [!DNL at.js] da utilizzare nelle richieste rawbox, devi creare le richieste manualmente. Gli esempi qui sotto spiegano come lavorare con le richieste rawbox nell&#39;e-mail.

>[!NOTE]
>
>Quando utilizzi una rawbox e [!DNL Target], consulta l’importante avviso di sicurezza in [Creare elenchi di Consentiti che specificano gli host autorizzati per l’invio di chiamate mbox a [!DNL Target]](/help/main/administrating-target/hosts.md#allowlist).

Questo approccio ti consente di monitorare le prestazioni dei consigli nelle e-mail, sottoporli normalmente a test con un consiglio e continuare il monitoraggio sul sito.

Configura un’attività [!DNL Recommendations] in [!DNL Target] utilizzando l’opzione [Compositore esperienza basata su modulo](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E). Per il percorso, seleziona il nome dell&#39;elemento mbox che hai deciso di utilizzare nella richiesta rawbox proveniente dall&#39;ESP. Seleziona una progettazione con l&#39;aspetto che desideri per la tua e-mail. Al momento della compilazione dell&#39;e-mail, l&#39;ESP effettua una chiamata ai server di [!DNL Target] per ogni rawbox in ogni e-mail che viene generata. L&#39;ESP deve disporre di un modo per includere l&#39;HTML restituito nell&#39;e-mail quando viene inviato.

Il sistema e-mail utilizzato deve essere in grado di gestire i seguenti scenari:

### Viene ricevuta una risposta valida, ma non sono presenti consigli

* In questo caso, la risposta corrisponderà al valore impostato per il parametro `mboxDefault`. Vedi la spiegazione riportata di seguito su questo parametro.
* Il fornitore di posta elettronica deve disporre di un blocco HTML predefinito per i consigli da utilizzare in questo caso.

### Il server [!DNL Target] riceve un timeout e non restituisce dati

* In questo caso, il server [!DNL Target] restituisce il seguente contenuto:

   `//ERROR: application server timeout`

* L&#39;applicazione e-mail deve cercare quel testo ed essere in grado di gestire l&#39;errore. Il provider di posta elettronica dispone di più opzioni per gestire questo caso:

   * Provare immediatamente un&#39;altra chiamata del server (consigliato, possibilmente con un contatore di tentativi).
   * Escludere quella particolare e-mail e passare a quella successiva.
   * Metti in coda quella specifica e-mail ed esegui nuovamente le e-mail non riuscite come batch alla fine dell’esecuzione iniziale.

### URL di richiesta di esempio

```
https://client_code.tt.omtrdc.net/m2/client_code/ubox/raw?mbox=mbox_name&mboxSession=1396032094853-955654&mboxPC=1396032094853-955654&mboxXDomain=disabled&entity.event.detailsOnly=true&mboxDefault=nocontent&mboxNoRedirect=1&entity.id=2A229&entity.categoryId=5674
```

### Parametri richiesti: {#reqparams}

>[!NOTE]
>
>Per utilizzare [!DNL Recommendations] (Consigli) nelle e-mail, la chiamata rawbox di solito deve includere `entity.id`, `entity.categoryId` o entrambi, a seconda del tipo di criteri per i consigli. La chiamata di esempio qui sopra include entrambi.

| Parametro | Valore | Descrizione | Convalida |
|--- |--- |--- |--- |
| `client_code` | *client_code* | Il codice del client utilizzato nella funzione Consigli. Il tuo consulente Adobe può fornire questo valore. |  |
| `mbox` | *mboxName* | Il nome mbox che viene utilizzato per il targeting. | Stessa convalida come per tutte le chiamate mbox.<br>Limite di 250 caratteri.<br>Non può contenere i seguenti caratteri: `', ", %22, %27, <, >, %3C, %3E` |
| `mboxXDomain` | disabilitato | Impedisce che la risposta imposti un cookie in ambienti non Web. |  |
| `entity.id`<br>(Richiesto per determinati tipi di criteri: view/view, view/bought, bought/bought) | *entity_id* | Il productId sul quale il consiglio è basato, come ad esempio un prodotto abbandonato nel carrello o un acquisto precedente.<br>Se richiesto dai criteri, la chiamata rawbox deve includere `entity.id`. |  |
| `entity.event.detailsOnly` | true | Se viene passato `entity.id`, è consigliabile passare anche questo parametro per impedire che la richiesta incrementi il numero di visualizzazioni di pagina conteggiate per un elemento, in modo da non alterare gli algoritmi basati sulla visualizzazione del prodotto. |  |
| `entity.categoryId`<br>(Richiesto per determinati tipi di criteri: più visti per categoria e più venduti per categoria) | *category_id* | La categoria su cui si basa il consiglio, ad esempio i più venduti in una categoria.<br>Se richiesto dai criteri, la chiamata rawbox deve includere `entity.categoryId`. |  |
| `mboxDefault` | *`https://www.default.com`* | Se il parametro `mboxNoRedirect` non è presente, `mboxDefault` deve essere un URL assoluto che restituirà il contenuto predefinito se non è disponibile alcun consiglio. Può trattarsi di un’immagine o di un altro contenuto statico.<br>Se il parametro `mboxNoRedirect` è presente, `mboxDefault` può essere qualsiasi testo che indichi che non vi sono consigli, ad esempio `no_content`.<br>Il provider e-mail dovrà gestire il caso in cui questo valore venga restituito e inserire nell’e-mail il contenuto HTML predefinito. <br> **Best practice sulla sicurezza**: se il dominio utilizzato nell’URL `mboxDefault` non è inserito nell’elenco Consentiti, puoi essere esposto a un rischio di vulnerabilità di reindirizzamento aperto. Per evitare l’uso non autorizzato dei collegamenti redirector o di `mboxDefault` da terze parti, Adobe consiglia di utilizzare “host autorizzati” per inserire nell’elenco Consentiti i domini URL di reindirizzamento predefiniti. Target utilizza gli host per inserire nell&#39;elenco Consentiti i domini a cui desideri consentire i reindirizzamenti. Per ulteriori informazioni, consulta [Creare elenchi Consentiti che specificano gli host autorizzati per l’invio di chiamate mbox a  [!DNL Target]](/help/main/administrating-target/hosts.md#allowlist) in *Host*. |  |
| `mboxHost` | *mbox_host* | Si tratta del dominio che viene aggiunto all&#39;ambiente predefinito (gruppo di host) quando la chiamata viene attivata. |  |
| `mboxPC` | Vuoto | (Richiesto per i consigli che utilizzano il profilo di un visitatore.)<br>Se non è stato fornito alcun “thirdPartyId”, viene generato un nuovo tntId e viene restituito come parte della risposta. Altrimenti rimane vuoto.<br>**Nota**: assicurati di fornire un valore univoco di `mboxSession` e `mboxPC` per ciascun destinatario e-mail (ad esempio, per ogni chiamata API). Se non fornisci valori univoci per questi campi, la risposta API potrebbe risultare lenta o non riuscire a causa del numero elevato di eventi generati in un singolo profilo. | 1 &lt; Lunghezza &lt; 128<br>Non può contenere più di un singolo “.” (punto).<br>L&#39;unico punto consentito è per il suffisso di posizione del profilo. |

### Parametri opzionali

| Parametro | Valore | Descrizione | Convalida |
|--- |--- |--- |--- |
| `mboxPC`<br>(Facoltativo) | *mboxPCId* | ID visitatore di Target. Utilizza questo valore se desideri monitorare un utente in modo completo sul sito nell&#39;arco di più visite o quando utilizzi un parametro di profilo utente.<br>Questo valore deve essere l’effettivo PCID di [!DNL Adobe Target] per l’utente, che verrebbe esportato dal sito Web al CRM. Il provider di posta elettronica recupererà questo ID dal CRM o dal Data Warehouse e lo utilizzerà come valore di questo parametro.<br>Il valore `mboxPC` è utile anche per monitorare il comportamento dei visitatori sul sito nell&#39;arco di più visite per il tracciamento delle metriche quando un consiglio fa parte di un&#39;attività A/B.<br>**Nota**: assicurati di fornire un valore univoco di `mboxSession` e `mboxPC` per ciascun destinatario e-mail (ad esempio, per ogni chiamata API). Se non fornisci valori univoci per questi campi, la risposta API potrebbe risultare lenta o non riuscire a causa del numero elevato di eventi generati in un singolo profilo. | 1 &lt; Lunghezza &lt; 128<br>Non può contenere più di un singolo “.” (punto).<br>L&#39;unico punto consentito è per il suffisso di posizione del profilo. |
| `mboxNoRedirect`<br>(Facoltativo) | 1 | Per impostazione predefinita, il chiamante viene reindirizzato quando non viene trovato alcun contenuto finale. Utilizzalo per disabilitare il comportamento predefinito. |  |
| `mbox3rdPartyId` | *xxx* | Utilizza questa opzione se disponi di un ID visitatore personalizzato da utilizzare per il targeting di profilo. |  |

### Potenziali risposte del server [!DNL Target]

| Risposta | Descrizione |
|--- |--- |
| //ERRORE: | Generato dal bilanciamento del carico quando non può restituire il contenuto |
| Completato | Il parametro `mboxNoRedirect` è impostato su “true” e il server non restituisce alcun consiglio (ad esempio, non vi è alcuna corrispondenza per l’elemento mbox o la cache del server non è inizializzata). |
| richiesta errata | Il parametro `mbox` è mancante.<ul><li>Il parametro `mboxDefault` o `mboxNoRedirect` non è specificato.</li><li>Il parametro di richiesta `mboxTrace` è specificato ma `mboxNoRedirect` non lo è.</li><li>Il parametro `mboxTarget` non viene specificato quando i nomi mbox terminano con il suffisso `-clicked`.</li></ul> |
| `Cannot redirect to default content, please specify mboxDefault parameter` | `mboxDefault` non viene specificato quando non esiste alcuna corrispondenza per la richiesta e il parametro `mboxNoRedirect` non è specificato. |
| `Invalid mbox name:= MBOX_NAME` | Indica che il parametro `mbox` contiene caratteri non validi. |
| `Mbox name [MBOX_NAME] is too long` | Indica che il parametro `mbox` è più lungo di 250 caratteri. |

## Metodo 3: Utilizzare Recommendations Download API {#download-api}

Configura un consiglio come al solito, ma scegli **solo download** nella sezione di presentazione, anziché una combinazione di modello e mbox. Quindi, in ESP, indica al sistema l&#39;ID del consiglio creato. ESP accede ai dati del consiglio tramite API. Questi dati mostrano quali elementi devono essere consigliati per una particolare categoria o elemento chiave, come ad esempio gli elementi in un carrello abbandonato. ESP memorizza questi dati, li collega all&#39;aspetto e alle caratteristiche relativi, visualizza le informazioni su ciascun elemento e le distribuisce nelle e-mail.

Con questa opzione, il server dei consigli non è in grado di monitorare direttamente le prestazioni di un consiglio o di suddividere il traffico tra più combinazioni di algoritmo/modello. Inoltre, i consigli non sono legati al profilo di un visitatore.

Per ulteriori informazioni sull&#39;API di download, vedi [API Legacy > Download](/help/main/assets/adobe-recommendations-classic.pdf).
