---
description: 'Informazioni sulla funzione adobe.target.sendNotifications(options) per at.js. '
keywords: adobe.target.sendNotifications;sendNotifications;sendnotifications;invia bnotifiche;notifiche;at.js;funzioni;funzione
seo-description: Informazioni sulla funzione adobe.target.sendNotifications(options) per la libreria at.js JavaScript di Adobe Target.
seo-title: Informazioni sulla funzione adobe.target.sendNotifications(options) per la libreria at.js JavaScript di Adobe Target.
solution: Target
subtopic: Introduzione
title: adobe.target.sendNotifications(options)
topic: Standard
translation-type: tm+mt
source-git-commit: ef2c4ac78fef5889d5a6e9e053dfd36b77919dd4

---


# adobe.target.sendNotifications(options)

Questa funzione invia una notifica al server Edge di Target quando viene eseguito il rendering di un’esperienza senza utilizzare `adobe.target.applyOffer()` o `adobe.target.applyOffers()`.

>[!NOTE]
>
>Questa funzione è stata introdotta in at.js 2.1.0 e sarà disponibile per tutte le versioni successive alla versione 2.1.0.

| Chiave | Tipo | Obbligatorio | Descrizione |
| --- | --- | --- | --- |
| consumerId | Stringa | No | Il valore predefinito è la mbox globale del client, se non specificato. Questa chiave si utilizza per generare l’ID dati supplementare utilizzato per l’integrazione A4T. |
| Richiesta | Oggetto | Sì | Vedi la tabella Richieste di seguito. |
| timeout | Numero | No | Timeout richiesta. Se non specificato, si utilizza il timeout predefinito di at.js. |

## Richiesta

| Nome campo | Tipo | Obbligatorio | Limitazione | Descrizione |
| --- | --- | --- | --- | --- |
| Request &gt; notifications | Array di oggetti | Sì |  | Notifiche per il contenuto visualizzato, i selettori su cui è stato fatto clic e/o le visualizzazioni o le mbox visitate. |
| Request &gt; notifications &gt; address | Oggetto | No |  |  |
| Request &gt; notifications &gt; address &gt; url | Stringa | No |  | URL da cui è stata avviata la notifica. |
| Request &gt; notifications &gt; address &gt; referringUrl | Stringa | No |  | URL di riferimento da cui è stata avviata la notifica. |
| Request &gt; notifications &gt; parameters | Oggetto | No | I seguenti nomi non sono consentiti per i parametri:<ul><li>orderId</li><li>orderTotal</li><li>productPurchasedIds</li></ul>Considera i seguenti aspetti:<ul><li>Limite massimo di parametri: 50.</li><li>Il nome del parametro non può restare vuoto.</li><li>Lunghezza massima del nome del parametro: 128.</li><li>Il nome del parametro non può iniziare con “profile”.</li><li>Lunghezza massima del valore parametro: 5000.</li></ul> |  |
| Request &gt; notifications &gt; profileParameters | Oggetto | No | I seguenti nomi non sono consentiti per i parametri:<ul><li>orderId</li><li>orderTotal</li><li>productPurchasedIds</li></ul>Considera i seguenti aspetti:<ul><li>Limite massimo di parametri: 50.</li><li>Il nome del parametro non può restare vuoto.</li><li>Lunghezza massima del nome del parametro: 128.</li><li>Il nome del parametro non può iniziare con “profile”.</li><li>Lunghezza massima del valore parametro: 5000.</li></ul> |  |
| Request &gt; notifications &gt; order | Oggetto | No |  | Oggetto che descrive i dettagli dell’ordine. |
| Request &gt; notifications &gt; order &gt; id | Stringa | No | `<=` 250 caratteri. | ID ordine. |
| Request &gt; notifications &gt; order &gt; total | Stringa | No | `>=` 0 | Totale ordine. |
| Request &gt; notifications &gt; order &gt; purchasedProductIds | Array di stringa | No | <ul><li>Non sono consentiti valori vuoti.</li><li>Lunghezza massima di ogni ID prodotto: 50.</li><li>Lunghezza massima degli ID dei prodotti, separati da virgole e concatenati: 250.</li></ul> | ID dei prodotti di un ordine. |
| Request &gt; notifications &gt; product | Oggetto | No |  |  |
| Request &gt; notifications &gt; product &gt; id | Stringa | No | `<=` 128 caratteri; non può essere vuoto. | ID prodotto. |
| Request &gt; notifications &gt; product &gt; categoryId | Stringa | No | `<=` 128 caratteri; non può essere vuoto. | ID categoria. |
| Request &gt; notifications &gt; id | Stringa | Sì | `<=` 200 caratteri. | L’ID della notifica viene restituito nella risposta e indica che la notifica è stata elaborata correttamente. |
| Request &gt; notifications &gt; impressionId | Stringa | No | `<= 128` caratteri. | L’ID dell’impression viene utilizzato per unire (collegare) la notifica corrente con una notifica precedente o per eseguire una richiesta. Se entrambi corrispondono, la seconda e altre richieste successive non genereranno una nuova impression per l’attività o l’esperienza. |
| Request &gt; notifications &gt; type | Stringa | Sì | È supportato il tipo “click” o “display”. | Tipo di notifica. |
| Request &gt; notifications &gt; timestamp | Numero`<int64>` | Sì |  | Marca temporale della notifica, in millisecondi trascorsi dall’epoca UNIX. |
| Request &gt; notifications &gt; tokens | Array di stringa | Sì |  | Elenco di token per i contenuti visualizzati o i selettori su cui è stato fatto clic, in base al tipo di notifica. |
| Request &gt; notifications &gt; mbox | Oggetto | No |  | Notifiche per la mbox. |
| Request &gt; notifications &gt; mbox &gt; name | Stringa | No | Non sono consentiti valori vuoti.<br>Caratteri consentiti: vedi la nota in calce alla tabella. | Nome Mbox. |
| Request &gt; notifications &gt; mbox &gt; state | Stringa | No |  | Token dello stato della mbox. |
| Request &gt; notifications &gt; view | Oggetto | No |  |  |
| Request &gt; notifications &gt; view &gt; id | Intero `<int64>` | No |  | ID visualizzazione. ID assegnato alla visualizzazione al momento della creazione della stessa tramite l’API per le visualizzazioni. |
| Request &gt; notifications &gt; view &gt; name | Stringa | No | `<= 128` caratteri. | Nome della visualizzazione. |
| Request &gt; notifications &gt; view &gt; key | Stringa | No | `<=` 512 caratteri. | Chiave visualizzazione. Chiave impostata per la visualizzazione tramite l’API. |
| Request &gt; notifications &gt; view &gt; state | Stringa | No |  | Token dello stato della visualizzazione. |

**Nota**: i seguenti caratteri sono consentiti per `Request > notifications > mbox > name`:

```
- '-, ./=`:;&!@#$%^&*()+|?~[]{}'
```

## Chiamata sendNotifications() dopo il rendering delle mbox preacquisite

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
>Se utilizzi Adobe Analytics, `getOffers()` esegue solo la preacquisizione e `sendNotifications()`, la richiesta di Analytics deve essere attivata dopo l’esecuzione di `sendNotifications()`. In tal modo l’identificatore SDID generato da `sendNotifications()` corrisponderà all’identificatore SDID inviato ad Analytics e Target.