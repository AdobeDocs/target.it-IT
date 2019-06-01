---
description: 'Informazioni sulla funzione adobe. target. sendnotifications (options) per at. js. '
seo-description: Informazioni sulla funzione adobe. target. sendnotifications (options) per la libreria javascript di Adobe Target nella libreria javascript. js.
seo-title: Informazioni sulla funzione adobe. target. sendnotifications (options) per la libreria javascript di Adobe Target nella libreria javascript. js.
solution: Target
subtopic: Introduzione
title: adobe. target. sendnotifications (options)
topic: Standard
translation-type: tm+mt
source-git-commit: f3d4963da631c668fb53a3939df53c80adff468b

---


# adobe. target. sendnotifications (options)

Questa funzione invia una notifica al Edge Target quando viene eseguito il rendering di un&#39;esperienza senza utilizzare `adobe.target.applyOffer()` o `adobe.target.applyOffers()`.

>[!NOTE]
>
>Questa funzione è stata introdotta in at. js 2.1.0 e sarà disponibile per qualsiasi versione precedente alle 2.1.0.

| Chiave | Type (Tipo) | Obbligatorio | Descrizione |
| --- | --- | --- | --- |
| consumerId | Stringa | No | Il valore predefinito è la mbox globale del client, se non specificato. Questa chiave si utilizza per generare l’ID dati supplementare utilizzato per l’integrazione A4T. |
| Richiesta | Oggetto | Sì | Vedi la tabella Richieste di seguito. |
| timeout | Numero | No | Timeout richiesta. Se non specificato, si utilizza il timeout predefinito di at.js. |

## Richiesta

| Nome campo | Type (Tipo) | Obbligatorio | Limitazione | Descrizione |
| --- | --- | --- | --- | --- |
| Request &gt; notifications | Array di oggetti | Sì |  | Notifiche per il contenuto visualizzato, selettori con clic e/o visualizzazioni visitate o mbox. |
| Request &gt; notifications &gt; address | Oggetto | No |  |  |
| Request &gt; notifications &gt; address &gt; url | Stringa | No |  | URL da cui è stata avviata la notifica. |
| Request &gt; notifications &gt; address &gt; referringurl | Stringa | No |  | L&#39;URL di riferimento da cui è stata avviata la notifica. |
| Request &gt; notifications &gt; parameters | Oggetto | No | I seguenti nomi non sono consentiti per i parametri:<ul><li>orderId</li><li>orderTotal</li><li>Productpurchasedids</li></ul>Valuta quanto segue:<ul><li>Limite massimo di 50 parametri.</li><li>Il nome del parametro non deve essere vuoto.</li><li>Nome parametro max 128.</li><li>Il nome del parametro non deve iniziare con «profilo».</li><li>Lunghezza valore parametro max 5000.</li></ul> |  |
| Request &gt; notifications &gt; profileparameters | Oggetto | No | I seguenti nomi non sono consentiti per i parametri:<ul><li>orderId</li><li>orderTotal</li><li>Productpurchasedids</li></ul>Valuta quanto segue:<ul><li>Limite massimo di 50 parametri.</li><li>Il nome del parametro non deve essere vuoto.</li><li>Nome parametro max 128.</li><li>Il nome del parametro non deve iniziare con «profilo».</li><li>Lunghezza valore parametro max 5000.</li></ul> |  |
| Request &gt; notifications &gt; order | Oggetto | No |  | Oggetto che descrive i dettagli dell&#39;ordine. |
| Request &gt; notifications &gt; order &gt; id | Stringa | No | `<=` 250 caratteri. | ID ordine. |
| Request &gt; notifications &gt; order &gt; total | Stringa | No | `>=` 0 | Totale ordine. |
| Request &gt; notifications &gt; order &gt; purchasedproductids | Array di stringa | No | <ul><li>Nessun valore vuoto consentito.</li><li>Ogni ID prodotto è lunghezza max 50.</li><li>Gli ID prodotto, separati da virgole e concatenati, non devono superare il 250.</li></ul> | Ordinare ID prodotto. |
| Request &gt; notifications &gt; product | Oggetto | No |  |  |
| Request &gt; notifications &gt; product &gt; id | Stringa | No | `<=` 128 caratteri; non può essere vuoto. | ID prodotto. |
| Request &gt; notifications &gt; product &gt; categoryid | Stringa | No | `<=` 128 caratteri; non può essere vuoto. | ID categoria. |
| Request &gt; notifications &gt; id | Stringa | Sì | `<=` 200 caratteri. | L&#39;ID notifica verrà restituito in risposta e indicherà che la notifica è stata elaborata correttamente. |
| Request &gt; notifications &gt; impressionid | Stringa | No | `<= 128` caratteri. | L&#39;ID impression viene utilizzato per unire (collegare) la notifica corrente con una notifica precedente o eseguire una richiesta. Se entrambi corrispondono, il secondo e altre richieste successive non genereranno una nuova impression all&#39;attività o all&#39;esperienza. |
| Request &gt; notifications &gt; type | Stringa | Sì | «click» o «display» è supportato. | Tipo di notifica. |
| Request &gt; notifications &gt; timestamp | Numero`<int64>` | Sì |  | Marca temporale della notifica, in millisecondi trascorsi dall&#39;epoch UNIX. |
| Request &gt; notifications &gt; tokens | Array di stringa | Sì |  | Un elenco di token per il contenuto visualizzato o per i selettori con clic, in base al tipo di notifica. |
| Request &gt; notifications &gt; mbox | Oggetto | No |  | Notifiche per la mbox. |
| Request &gt; notifications &gt; mbox &gt; name | Stringa | No | Nessun valore vuoto consentito.<br>Caratteri consentiti: Consultate la nota seguente. | Nome Mbox. |
| Request &gt; notifications &gt; mbox &gt; state | Stringa | No |  | token di stato mbox. |
| Request &gt; notifications &gt; view | Oggetto | No |  |  |
| Request &gt; notifications &gt; view &gt; id | Intero `<int64>` | No |  | Visualizza id. L&#39;ID assegnato alla visualizzazione quando la visualizzazione è stata creata tramite l&#39;API view. |
| Request &gt; notifications &gt; view &gt; name | Stringa | No | `<= 128` caratteri. | Nome della visualizzazione. |
| Request &gt; notifications &gt; view &gt; key | Stringa | No | `<=` 512 caratteri. | Visualizza chiave. Chiave impostata con la visualizzazione tramite l&#39;API. |
| Request &gt; notifications &gt; view &gt; state | Stringa | No |  | Visualizza token stato. |

**Nota**: I seguenti caratteri sono consentiti `Request > notifications > mbox > name`per:

```
- '-, ./=`:;&!@#$%^&*()+|?~[]{}'
```

## Chiamata sendnotifications () dopo il rendering delle mbox preacquisite

```
function createTokens(options) {
  return options.map(e => e.eventToken);
}

function createNotification(mbox, type, tokens) {
  const id = 11111; // here we should use a random ID like UUID
  const timestamp = Date.now();
  const { name, state, parameters, profileParameters, order, product } = mbox;
  const result = {
    id,
    type,
    timestamp,
    parameters,
    profileParameters,
    order,
    product
  };

  result.mbox = { name, state };
  result.tokens = tokens;

  return result;
}

adobe.target.getOffers({
  request: {
    prefetch: {
      mboxes: [
        {
          index: 0,
          name: "a1-serverside-ab"
        }
      ]
    }
  }
})
.then(response => {
  const mboxes = response.prefetch.mboxes;
  const notifications = mboxes.map(mbox => {
    const type = "display";
    const tokens = createTokens(mbox.options);

    return createNotification(mbox, type, tokens);
  });
  
  adobe.target.sendNotifications({
    request: { notifications }
  });
})
```

>[!NOTE]
>
>Se utilizzi Adobe Analytics, `getOffers()` con solo preacquisizione e `sendNotifications()`la richiesta di Analytics deve essere attivata dopo `sendNotifications()` l&#39;esecuzione. Lo scopo di questo problema è fare in modo che l&#39;identificatore SDID generato corrisponda `sendNotifications()` al codice SDID inviato ad Analytics e Target.