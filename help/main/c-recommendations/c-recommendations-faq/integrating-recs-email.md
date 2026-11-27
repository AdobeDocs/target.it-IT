---
keywords: e-mail;ESP;provider di servizi di posta elettronica;rawbox;API di consegna;modello di solo download;modello di posta elettronica;elaborazione batch;e-mail build-time
description: Scopri come integrare le e-mail con Adobe [!DNL Target Recommendations], incluso l’utilizzo dell’API di consegna [!DNL Target], dei modelli rawbox e dei modelli di solo download.
title: Come posso integrare Consigli con l’e-mail?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: 08fcb507-2c91-444a-b8ac-26165e359f6f
TQID: 'https://experienceleague.adobe.com/ZyeOl6ysM03a0mMiNgHuicOLPfgpXnrdqXJE1gHRRvE'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '1741'
ht-degree: 26%
---
# Integrare [!DNL Recommendations] con l&#39;e-mail {#integrate-recs-email}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri i metodi di integrazione di [!DNL Target Recommendations] con un provider di servizi e-mail (ESP) per la personalizzazione in fase di invio dei consigli nelle e-mail.

>[!ENDSHADEBOX]

[!DNL Adobe Target] supporta la personalizzazione in fase di invio dei consigli nelle e-mail. La personalizzazione dei consigli in base all’ora di apertura non è supportata.

Sono disponibili tre metodi per integrare [!DNL Target Recommendations] con un ESP. Le funzionalità dell&#39;ESP determinano il metodo da utilizzare e l&#39;account manager o il consulente può aiutare a scegliere l&#39;opzione migliore.

| Metodo | Dettagli |
| --- | --- |
| [Metodo 1: [!DNL Adobe Target Delivery API]](#delivery-api) (preferito) | Utilizza [!DNL Adobe Target Delivery API] per effettuare richieste per cliente e per e-mail per i consigli. |
| [Metodo 2: [!DNL Adobe Rawbox API]](#rawbox) | Utilizza [!DNL Adobe Target Rawbox API] per effettuare richieste per cliente e per e-mail per i consigli. |
| [Metodo 3: [!DNL Recommendations Download API]](#download-api) | Utilizza [!DNL Recommendations Download API] per richiedere consigli in blocco per un elenco di prodotti o categorie in formato CSV. |

I metodi 1 e 2 richiedono che l&#39;ESP effettui chiamate a un&#39;API esterna per cliente, per e-mail, e attenda che venga restituito il contenuto. Non tutti gli ESP supportano questi metodi, pertanto è necessario contattare l’ESP per determinare se è compatibile con questo modello di integrazione.

Il metodo 3 richiede che l’ESP unisca all’elenco delle e-mail un elenco di consigli per ID prodotto o ID categoria. Questo join può essere basato su un attributo come ultimo prodotto visualizzato, ultimo prodotto acquistato o la categoria più visualizzata del cliente. Per eseguire l’unione, l’ESP deve avere accesso a questi dati nel suo profilo cliente, pertanto deve essere contattato per determinare se ha accesso a questi dati e se è compatibile con questo modello di integrazione.

>[!IMPORTANT]
>
>Le seguenti linee guida sulla capacità si applicano ai metodi Modello e-mail API di consegna e rawbox (metodi 1 e 2):
>
>* Le richieste devono essere limitate al minore tra i seguenti valori: 1.000 richieste al secondo o 25 volte il traffico giornaliero di picco.
>* Il traffico deve essere incrementato di 200 richieste al secondo al minuto.
>
>Per utilizzare limiti di tariffa più elevati, contatta l’account manager.

## Metodo 1: utilizzare l’API di consegna (preferito) {#delivery-api}

L’API di consegna è una richiesta POST che funziona con l’e-mail in fase di generazione. Questa opzione è il metodo preferito per l&#39;e-mail di build-time.

La maggior parte dei client di posta elettronica non consentono richieste POST, pertanto questa API non è consigliata per i casi di utilizzo a tempo aperto. Alcuni client di posta elettronica, come ad esempio Gmail o Outlook, possono memorizzare in cache il contenuto o bloccare l’immagine e richiedere al destinatario di consentire in modo proattivo il rendering dell’immagine.

Il contenuto predefinito non può essere restituito con l’API di consegna.

Il codice seguente è una richiesta di consegna API di esempio, dove `clientcode` è il codice client [!DNL Target]:

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

>[!NOTE]
>
>Fornisci un valore univoco per `sessionId` e uno tra `tntId` o `thirdPartyId` per ogni destinatario e-mail (per ogni chiamata API). Senza valori univoci per questi campi, la risposta API potrebbe risultare lenta o non riuscire a causa del numero elevato di eventi generati in un singolo profilo.

Per ulteriori informazioni, consulta la [documentazione sulle API di consegna](https://experienceleague.adobe.com/docs/target-dev/developer/api/delivery-api/overview.html?lang=it){target=_blank}.

## Metodo 2 - Utilizzare un modello di e-mail rawbox {#rawbox}

Un rawbox è simile a una richiesta mbox, ma per ambienti non web, come ad esempio i provider di servizi e-mail (ESP). [!DNL Adobe Experience Platform Web SDK] e [!DNL at.js] non sono disponibili per le richieste rawbox, pertanto le richieste devono essere create manualmente. Gli esempi seguenti spiegano come lavorare con le richieste rawbox nelle e-mail.

Questo approccio consente di monitorare le prestazioni dei consigli nelle e-mail, testarli normalmente con un consiglio e continuare il tracciamento sul sito.

>[!NOTE]
>
>Quando utilizzi una rawbox e [!DNL Target], consulta l’importante avviso di sicurezza in [Creare elenchi di Consentiti che specificano gli host autorizzati per l’invio di chiamate mbox a [!DNL Target]](/help/main/administrating-target/hosts.md#allowlist).

1. Configura un&#39;attività [!DNL Recommendations] in [!DNL Target] con l&#39;opzione [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md).

1. Per la posizione, seleziona il nome della mbox utilizzata nella richiesta rawbox proveniente dall’ESP.

1. Seleziona una progettazione con l’aspetto desiderato per l’e-mail.

Al momento della compilazione dell&#39;e-mail, l&#39;ESP effettua una chiamata ai server di [!DNL Target] per ogni rawbox in ogni e-mail che viene generata. L’ESP deve disporre di un modo per includere il HTML restituito nell’e-mail quando viene inviato.

Il sistema e-mail deve essere in grado di gestire i seguenti scenari.

### Viene ricevuta una risposta valida, ma non sono presenti consigli

* La risposta è il valore impostato nel parametro `mboxDefault`. Vedere la descrizione di questo parametro nella tabella dei parametri richiesti.
* Il fornitore di posta elettronica deve disporre di un blocco HTML predefinito per i consigli da utilizzare in questo caso.

### Il server [!DNL Target] riceve un timeout e non restituisce dati

* Il server [!DNL Target] restituisce il seguente contenuto:

  `//ERROR: application server timeout`

* L&#39;applicazione e-mail deve cercare quel testo ed essere in grado di gestire l&#39;errore. Il provider di posta elettronica dispone di più opzioni per gestire questo caso:

  * Provare immediatamente un&#39;altra chiamata del server (consigliato, possibilmente con un contatore di tentativi).
  * Ignora quella particolare e-mail e continua con quella successiva.
  * Inserisci in coda quella particolare e-mail ed esegui nuovamente le e-mail non riuscite come batch alla fine dell’esecuzione iniziale.

### URL di richiesta di esempio

```
https://client_code.tt.omtrdc.net/m2/client_code/ubox/raw?mbox=mbox_name&mboxSession=1396032094853-955654&mboxPC=1396032094853-955654&mboxXDomain=disabled&entity.event.detailsOnly=true&mboxDefault=nocontent&mboxNoRedirect=1&entity.id=2A229&entity.categoryId=5674
```

### Parametri richiesti {#reqparams}

>[!NOTE]
>
>Per utilizzare [!DNL Recommendations] nelle e-mail, la chiamata rawbox deve in genere includere `entity.id`, `entity.categoryId` o entrambi, a seconda del tipo di criteri per i consigli. La chiamata di esempio qui sopra include entrambi.

| Parametro | Valore | Descrizione | Convalida |
|--- |--- |--- |--- |
| `client_code` | *client_code* | Codice client utilizzato in [!DNL Recommendations]. Il consulente Adobe può fornire questo valore. |  |
| `mbox` | *mboxName* | Il nome mbox che viene utilizzato per il targeting. | Stessa convalida di tutte le chiamate mbox.<br>Limite di 250 caratteri.<br>Non può contenere i seguenti caratteri: `', ", %22, %27, <, >, %3C, %3E` |
| `mboxXDomain` | disabilitato | Impedisce che la risposta imposti un cookie in ambienti non Web. |  |
| `entity.id`<br>(Richiesto per determinati tipi di criteri: view/view, view/bought, bought/bought) | *entity_id* | Il productId su cui si basa il consiglio, ad esempio un prodotto abbandonato nel carrello o un acquisto precedente.<br>Se richiesto dai criteri, la chiamata rawbox deve includere `entity.id`. |  |
| `entity.event.detailsOnly` | true | Se viene passato `entity.id`, si consiglia vivamente di trasmettere questo parametro, per evitare che la richiesta incrementi il numero di visualizzazioni di pagina conteggiate per un elemento, in modo da non alterare gli algoritmi basati sulla visualizzazione del prodotto. |  |
| `entity.categoryId`<br>(Richiesto per determinati tipi di criteri: più visti per categoria e più venduti per categoria) | *category_id* | La categoria su cui si basa il consiglio, ad esempio gli articoli più venduti di una categoria.<br>Se richiesto dai criteri, la chiamata rawbox deve includere `entity.categoryId`. |  |
| `mboxDefault` | *`https://www.default.com`* | Se il parametro `mboxNoRedirect` non è presente, `mboxDefault` deve essere un URL assoluto che restituirà il contenuto predefinito se non è disponibile alcun consiglio. Può trattarsi di un’immagine o di un altro contenuto statico.<br>Se il parametro `mboxNoRedirect` è presente, `mboxDefault` può essere qualsiasi testo che indichi che non sono presenti consigli, ad esempio `no_content`.<br>Il provider di posta elettronica deve gestire il caso in cui questo valore viene restituito e inserire HTML predefinito nell&#39;e-mail.<br>Vedere le procedure consigliate per la protezione sotto le tabelle. |  |
| `mboxHost` | *mbox_host* | Si tratta del dominio che viene aggiunto all&#39;ambiente predefinito (gruppo di host) quando la chiamata viene attivata. |  |
| `mboxPC` | Vuoto | (Obbligatorio per i consigli che utilizzano il profilo di un visitatore.)<br>Se non è stato fornito alcun &quot;thirdPartyId&quot;, viene generato un nuovo tntId e viene restituito come parte della risposta. In caso contrario, il valore rimane vuoto.<br>Vedere la nota sui valori univoci sotto le tabelle. | 1 &lt; Lunghezza &lt; 128<br>Non può contenere più di un singolo “.” (punto).<br>L&#39;unico punto consentito è per il suffisso di posizione del profilo. |

### Parametri opzionali

| Parametro | Valore | Descrizione | Convalida |
|--- |--- |--- |--- |
| `mboxPC`<br>(Facoltativo) | *mboxPCId* | ID visitatore [!DNL Target]. Utilizza questo valore per tenere traccia di un cerchio completo di utenti che ritornano al sito attraverso più visite o quando utilizzi un parametro di profilo utente.<br>Questo valore deve essere l&#39;effettivo PCID [!DNL Adobe Target] dell&#39;utente, che viene esportato dal sito Web al CRM. Il provider di posta elettronica recupera questo ID dal CRM o dal data warehouse e lo utilizza come valore di questo parametro.<br>Il valore `mboxPC` è utile anche per monitorare il comportamento dei visitatori sul sito nell&#39;arco di più visite per il tracciamento delle metriche, quando un consiglio fa parte di un&#39;attività A/B.<br>Vedere la nota sui valori univoci sotto le tabelle. | 1 &lt; Lunghezza &lt; 128<br>Non può contenere più di un singolo “.” (punto).<br>L&#39;unico punto consentito è per il suffisso di posizione del profilo. |
| `mboxNoRedirect`<br>(Facoltativo) | 1 | Per impostazione predefinita, il chiamante viene reindirizzato quando non viene trovato alcun contenuto finale. Utilizzare questo parametro per disattivare il comportamento predefinito. |  |
| `mbox3rdPartyId` | *xxx* | Utilizza questa opzione per specificare un ID visitatore personalizzato per il targeting del profilo. |  |

Per `mboxSession` e `mboxPC`, fornisci un valore univoco per ogni destinatario e-mail (per ogni chiamata API). Senza valori univoci per questi campi, la risposta API potrebbe risultare lenta o non riuscire a causa del numero elevato di eventi generati in un singolo profilo.

Come best practice per la sicurezza di `mboxDefault`, utilizza host autorizzati per inserire nell&#39;elenco Consentiti i domini URL di reindirizzamento predefiniti. Se il dominio utilizzato nell&#39;URL `mboxDefault` non è inserito nell&#39;elenco Consentiti, è possibile esporre un rischio di vulnerabilità di reindirizzamento aperto. Gli host autorizzati evitano l&#39;utilizzo non autorizzato dei collegamenti redirector o di `mboxDefault` da terze parti. [!DNL Target] utilizza gli host per i domini ai quali sono consentiti i reindirizzamenti. Per ulteriori informazioni, vedere l&#39;avviso di protezione all&#39;inizio di questa sezione.

### Potenziali risposte del server [!DNL Target]

| Risposta | Descrizione |
|--- |--- |
| //ERRORE: | Generato dal load balancer quando non può restituire contenuto. |
| Operazione riuscita | Il parametro `mboxNoRedirect` è impostato su &#39;true&#39; e il server non restituisce alcun consiglio (non esiste alcuna corrispondenza per l&#39;elemento mbox o la cache del server non è inizializzata). |
| richiesta errata | Il parametro `mbox` è mancante.<ul><li>Il parametro `mboxDefault` o `mboxNoRedirect` non è specificato.</li><li>Il parametro di richiesta `mboxTrace` è specificato, ma `mboxNoRedirect` non lo è.</li><li>Il parametro `mboxTarget` non è specificato quando i nomi mbox terminano con il suffisso `-clicked`.</li></ul> |
| `Cannot redirect to default content, please specify mboxDefault parameter` | `mboxDefault` non è specificato quando non esiste alcuna corrispondenza per la richiesta e il parametro `mboxNoRedirect` non è specificato. |
| `Invalid mbox name:= MBOX_NAME` | Il parametro `mbox` contiene caratteri non validi. |
| `Mbox name [MBOX_NAME] is too long` | Il parametro `mbox` supera i 250 caratteri. |

## Metodo 3: Utilizzare l’API Download per la funzione Consigli {#download-api}

Configura un consiglio come al solito, ma scegli **solo download** nella sezione di presentazione, anziché una combinazione di modello e mbox. Quindi fornisci all’ESP l’ID del consiglio creato. L’ESP accede ai dati dei consigli tramite l’API. Questi dati mostrano quali elementi devono essere consigliati per una particolare categoria o elemento chiave, come ad esempio gli elementi in un carrello abbandonato. L&#39;ESP memorizza questi dati, li collega con il proprio look and feel, visualizza informazioni su ciascun elemento e li consegna nelle e-mail.

Con questa opzione, il server Recommendations non può tenere traccia direttamente delle prestazioni di un consiglio o suddividere il traffico tra più combinazioni di algoritmi e modelli. Inoltre, i consigli non sono legati al profilo di un visitatore.

Per ulteriori informazioni sull&#39;API di download, vedi [API Legacy > Download](/help/main/assets/adobe-recommendations-classic.pdf).
