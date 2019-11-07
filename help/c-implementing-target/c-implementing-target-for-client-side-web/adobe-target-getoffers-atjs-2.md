---
keywords: adobe.target.getOffers;getOffers;getoffers;ottieni offerte;at.js;funzioni;funzione
description: Informazioni sulla funzione adobe.target.getOffers(options) per la libreria JavaScript at.js di Adobe Target.
title: Informazioni sulla funzione adobe.target.getOffers() per la libreria JavaScript at.js di Adobe Target.
subtopic: Introduzione
topic: Standard
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# adobe.target.getOffers(options) - at.js 2.x

Questa funzione ti consente di recuperare più offerte passando più mbox. Inoltre, è possibile recuperare più offerte per tutte le visualizzazioni nelle attività attive.

>[!NOTE]
>
>Questa funzione è stata introdotta con at.js 2.x e non è disponibile per at.js versione 1.*x*.

| Chiave | Tipo | Obbligatorio | Descrizione |
| --- | --- | --- | --- |
| consumerId | Stringa | No | Il valore predefinito è la mbox globale del client, se non specificato. Questa chiave si utilizza per generare l’ID dati supplementare utilizzato per l’integrazione A4T. Questa chiave è una stringa univoca per visitatore. |
| richiesta | Oggetto | Sì | Vedi la tabella Richieste di seguito. |
| timeout | Numero | No | timeout richiesta. Se non specificato, si utilizza il timeout predefinito di at.js. |

## Richiesta

>[!NOTE]
>
>Per informazioni sui tipi accettabili per tutti i campi elencati di seguito, consulta la documentazione [API di](http://developers.adobetarget.com/api/delivery-api/#tag/Delivery-API) consegna.

| Nome campo | Obbligatorio | Limitazioni | Descrizione |
| --- | --- | --- | --- |
| request &gt; id | No |  | Uno tra `tntId`, `thirdPartyId` e `marketingCloudVisitorId` è obbligatorio. |
| Request &gt; id &gt; thirdPartyId | No | Dimensione massima = 128 |  |  |
| Request &gt; experienceCloud | No |  |  |
| Request &gt; experienceCloud &gt; analytics | No |  | Integrazione di Adobe Analytics |
| Request &gt; experienceCloud &gt; analytics &gt; logging | No | I seguenti elementi devono essere implementati sulla pagina:<ul><li>Servizio ID visitatori</li><li>Appmeasurement.js</li></ul> | Sono supportati i seguenti valori:<br>**client_side**: se specificato, viene restituito un payload di Analytics al chiamante che deve essere utilizzato l’invio ad Adobe Analytics tramite l’API di inserimento dati.<br>**server_side**: questo è il valore predefinito, con cui il backend di Target e Analytics utilizzerà l’identificatore SDID per unire le chiamate a scopo di reporting. |
| Request &gt; prefetch | No |  |  |
| Request &gt; prefetch &gt; views | No | Numero massimo: 50<br>Nome non vuoto<br>Lunghezza nome `<=` 128<br>Lunghezza valore `<=` 5000<br>Il nome deve iniziare con “profile”<br>Nomi non consentiti: “orderId”, “orderTotal”, “productPurchasedId” | Passa i parametri da utilizzare per recuperare le visualizzazioni rilevanti nelle attività attive. |
| Request &gt; prefetch &gt; views &gt; profileParameters | No | Numero massimo: 50<br>Nome non vuoto<br>Lunghezza nome `<=` 128<br>Lunghezza valore `<=` 5000<br>Il nome deve iniziare con “profile” | Passa i parametri di profilo da utilizzare per recuperare le visualizzazioni rilevanti nelle attività attive. |
| Request &gt; prefetch &gt; views &gt; product | No |  |  |
| Request &gt; prefetch &gt; views &gt; product -&gt; id | No | Non vuoto<br>Dimensione massima = 128 | Passa gli ID prodotto da utilizzare per recuperare le visualizzazioni rilevanti nelle attività attive. |
| Request &gt; prefetch &gt; views &gt; product &gt; categoryId | No | Non vuoto<br>Dimensione massima = 128 | Passa gli ID categoria prodotto da utilizzare per recuperare le visualizzazioni rilevanti nelle attività attive. |
| Request &gt; prefetch &gt; views &gt; order | No |  |  |
| Request &gt; prefetch &gt; views &gt; order &gt; id | No | Lunghezza massima = 250 | Passa gli ID ordine da utilizzare per recuperare le visualizzazioni rilevanti nelle attività attive. |
| Request &gt; prefetch &gt; views &gt; order &gt; total | No | Totale `>=` 0 | Passa i totali dell’ordine da utilizzare per recuperare le visualizzazioni rilevanti nelle attività attive. |
| Request &gt; prefetch &gt; views &gt; order &gt; purchasedProductIds | No | Nessun valore vuoto<br>Lunghezza max di ogni valore: 50<br>Concatenata e separata da virgole<br>Lunghezza totale ID prodotto `<=` 250 | Passa gli ID prodotti acquistati da utilizzare per recuperare le visualizzazioni rilevanti nelle attività attive. |
| Request &gt; execute | No |  |  |
| Request &gt; execute &gt; pageLoad | No |  |  |
| Request &gt; execute &gt; pageLoad &gt; parameters | No | Numero massimo: 50<br>Nome non vuoto<br>Lunghezza nome `<=` 128<br>Lunghezza valore `<=` 5000<br>Il nome non deve iniziare con “profile”.<br>Nomi non consentiti: “orderId”, “orderTotal”, “productPurchasedId” | Recupera le offerte con i parametri specificati al caricamento della pagina. |
| Request &gt; execute &gt; pageLoad &gt; profileParameters | No | Numero massimo: 50<br>Nome non vuoto<br>Lunghezza nome `<=` 128<br>Lunghezza valore `<=`256<br>Il nome non deve iniziare con “profile”. | Recupera le offerte con i parametri del profilo specificati al caricamento della pagina. |
| Request &gt; execute &gt; pageLoad &gt; product | No |  |  |
| Request &gt; execute &gt; pageLoad &gt; product -&gt; id | No | Non vuoto<br>Dimensione massima = 128 | Recupera le offerte con gli ID prodotto specificati al caricamento della pagina. |
| Request &gt; execute &gt; pageLoad &gt; product &gt; categoryId | No | Non vuoto<br>Dimensione massima = 128 | Recupera le offerte con gli ID categoria prodotto specificati al caricamento della pagina. |
| Request &gt; execute &gt; pageLoad &gt; order | No |  |  |
| Request &gt; execute &gt; pageLoad &gt; order &gt; id | No | Lunghezza massima = 250 | Recupera le offerte con gli ID ordine specificati al caricamento della pagina. |
| Request &gt; execute &gt; pageLoad &gt; order &gt; total | No | `>=` 0 | Recupera le offerte con i totali dell’ordine specificati al caricamento della pagina. |
| Request &gt; execute &gt; pageLoad &gt; order &gt; purchasedProductIds | No | Nessun valore vuoto<br>Lunghezza max di ogni valore: 50<br>Concatenata e separata da virgole<br>Lunghezza totale ID prodotto `<=` 250 | Recupera le offerte con gli ID prodotti acquistati specificati al caricamento della pagina. |
| Request &gt; execute &gt; mboxes | No | Dimensione massima = 50<br>Nessun elemento null |  |
| Request &gt; execute &gt; mboxes&gt;mbox | Sì | Non vuoto<br>No suffisso ’-clicked’<br>Dimensione massima = 250<br>Caratteri consentiti: `'-, ._\/=:;&!@#$%^&*()_+|?~[]{}'` | Nome della mbox. |
| Request &gt; execute &gt; mboxes&gt;mbox&gt;index | Sì | No null<br>Univoco<br>`>=` 0 | Nota che l’indice non rappresenta l’ordine di elaborazione delle mbox. Come in una pagina web con diverse mbox regionali, non è possibile specificarne l’ordine di elaborazione. |
| Request &gt; execute &gt; mboxes &gt; mbox &gt; parameters | No | Numero massimo = 50<br>Nome non vuoto<br>Lunghezza nome `<=` 128<br>Lunghezza valore `<=` 5000<br>Il nome non deve iniziare con “profile”.<br>Nomi non consentiti: “orderId”, “orderTotal”, “productPurchasedId” | Recupera le offerte per una data mbox con i parametri specificati. |
| Request &gt; execute &gt; mboxes&gt;mbox&gt;profileParameters | No | Numero massimo = 50<br>Nome non vuoto<br>Lunghezza nome `<=` 128<br>Lunghezza valore `<=`256<br>Il nome non deve iniziare con “profile”. | Recupera le offerte per una data mbox con i parametri del profilo specificati. |
| Request &gt; execute &gt; mboxes&gt;mbox &gt; product | No |  |  |
| Request &gt; execute &gt; mboxes &gt; mbox &gt; product &gt; id | No | Non vuoto<br>Dimensione massima = 128 | Recupera le offerte per una data mbox con gli ID prodotto specificati. |
| Request &gt; execute &gt; mboxes &gt; mbox &gt; product &gt; categoryId | No | Non vuoto<br>Dimensione massima = 128 | Recupera le offerte per una data mbox con gli ID categoria prodotto specificati. |
| Request &gt; execute &gt; mboxes &gt; mbox &gt; order | No |  |  |
| Request &gt; execute &gt; mboxes&gt;mbox &gt; order &gt; id | No | Lunghezza massima = 250 | Recupera le offerte per una data mbox con gli ID dell’ordine specificati. |
| Request &gt; execute &gt; mboxes &gt; mbox &gt; order &gt; total | No | `>=` 0 | Recupera le offerte per una data mbox con i totali dell’ordine specificati. |
| Request &gt; execute &gt; mboxes &gt; mbox &gt; order &gt; purchasedProductIds | No | Nessun valore vuoto<br>Lunghezza massima di ogni valore = 50<br>Concatenata e separata da virgole<br>Lunghezza totale ID prodotto `<=` 250 | Recupera le offerte per una data mbox con gli ID dei prodotti acquistati dell’ordine specificati. |

## Richiama `getOffers()` per tutte le visualizzazioni

```
adobe.target.getOffers({
    request: {
      prefetch: {
        views: [{}]
    }
  }
});
```

## Richiama `getOffers()` per recuperare le visualizzazioni più recenti con i parametri e i parametri del profilo passati

```
adobe.target.getOffers({
  request: {
    "prefetch": {
      "views": [
        {
          "parameters": {
            "ad": "1"
          },
          "profileParameters": {
            "age": 23
          }
        }
      ]
    }
  }
});
```

## Richiama `getOffers()` per recuperare mbox con parametri e parametri di profilo passati.

```
adobe.target.getOffers({
  request: {
    execute: {
      mboxes: [
        {
          index: 0,
          name: "first-mbox"
        },
        {
          index: 1,
          name: "second-mbox",
          parameters: {
            a: 1
          },
          profileParameters: {
            b: 2
          }
        }
      ]
    }
  }
});
```

## Richiama getOffers() per recuperare il payload di Analytics dal lato client

```
adobe.target.getOffers({
      request: {
        experienceCloud: {
          analytics: {
            logging: "client_side"
          }
        },
        prefetch: {
          mboxes: [{
            index: 0,
            name: "a1-serverside-xt"
          }]
        }
      }
    })
    .then(console.log)
```

**Risposta**:

```
{
  "prefetch": {
    "mboxes": [{
      "index": 0,
      "name": "a1-serverside-xt",
      "options": [{
        "content": "<img src=\"http://s7d2.scene7.com/is/image/TargetAdobeTargetMobile/L4242-xt-usa?tm=1490025518668&fit=constrain&hei=491&wid=980&fmt=png-alpha\"/>",
        "type": "html",
        "eventToken": "n/K05qdH0MxsiyH4gX05/2qipfsIHvVzTQxHolz2IpSCnQ9Y9OaLL2gsdrWQTvE54PwSz67rmXWmSnkXpSSS2Q==",
        "responseTokens": {
          "profile.memberlevel": "0",
          "geo.city": "bucharest",
          "activity.id": "167169",
          "experience.name": "USA Experience",
          "geo.country": "romania"
        }
      }],
      "analytics": {
        "payload": {
          "pe": "tnt",
          "tnta": "167169:0:0|0|100,167169:0:0|2|100,167169:0:0|1|100"
        }
      }
    }]
  }
}
```

Il payload può quindi essere inoltrato ad Adobe Analytics tramite l'API [di inserimento](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html)dati.

## Recupera ed esegui il rendering di dati da più mbox tramite getOffers() e applyOffers() {#multiple}

at.js 2.x consente di recuperare più mbox tramite l’API `getOffers()`. Puoi anche recuperare dati per più mbox e quindi utilizzare `applyOffers()` per eseguire il rendering dei dati in posti diversi identificati da un selettore CSS.

L’esempio seguente mostra una semplice pagina HTML con at.js 2.x implementata:

```
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>at.js 2.x, multiple selectors and multiple mboxes</title>
  <script src="at.js"></script>
</head>
<body>
  <div id="container1">Default content 1</div>
  
  <div id="container2">Default content 2</div>

  <div id="container3">Default content 3</div>
</body>
</html>
```

Supponi di disporre di tre contenitori che desideri modificare tramite il contenuto ricevuto da [!DNL Target]. Puoi creare una singola richiesta per tre mbox in cui ogni mbox ha del contenuto da riprodurre nel rispettivo contenitore.

La richiesta e il codice di rendering possono avere il seguente aspetto:

```
adobe.target.getOffers({
  request: {
    prefetch: {
      mboxes: [
        {
          index: 0,
          name: "mbox1"
        },
        {
          index: 1,
          name: "mbox2"
        },
        {
          index: 2,
          name: "mbox3"
        }
      ]
    }
  }
})
.then(response => {
  // get all mboxes from response
  const mboxes = response.prefetch.mboxes;
  let count = 1;

  mboxes.forEach(el => {
    adobe.target.applyOffers({
      selector: "#container" + count,
      response: {
        prefetch: {
          mboxes: [el]
        }
      }
    });

    count += 1;
  });
});
```

Nella sezione `request > prefetch > mboxes` sono disponibili tre mbox diverse. Riceverai la risposta per ogni mbox da `response > prefetch > mboxes` se la richiesta è stata completata con successo. Una volta che possiedi le risposte e le posizioni da utilizzare per il rendering, puoi richiamare `applyOffers()` per riprodurre il contenuto recuperato da [!DNL Target]. In questo esempio abbiamo la seguente mappatura:

* mbox1 &gt; Selettore CSS #container1
* mbox2 &gt; Selettore CSS #container2
* mbox3 &gt; Selettore CSS #container3

Questo esempio utilizza la variabile count per creare i selettori CSS. In uno scenario reale puoi utilizzare una mappatura diversa tra il selettore CSS e la mbox.

Questo esempio utilizza `prefetch > mboxes`, ma puoi anche utilizzare `execute > mboxes`. Se utilizzi la preacquisizione in `getOffers()`, devi anche usare la preacquisizione nella chiamata di `applyOffers()`.
