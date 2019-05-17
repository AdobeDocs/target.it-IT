---
description: 'Informazioni sulla funzione adobe. target. getoffer (options) per at. js. '
keywords: adobe.target.notification;element;selector;notification;extension
seo-description: Informazioni sulla funzione adobe. target. getoffer (options) per la libreria javascript di Adobe Target nella libreria javascript. js.
seo-title: Informazioni sulla funzione adobe. target. getoffer (options) per la libreria javascript di Adobe Target nella libreria javascript. js.
solution: Target
subtopic: Introduzione
title: adobe.target.getOffers(options)
topic: Standard
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# adobe. target. getoffer (options) - at. js 2. x

Questa funzione ti consente di recuperare più offerte passando più mbox. Inoltre, è possibile recuperare più offerte per tutte le visualizzazioni nelle attività attive.

>[!NOTE]
>
>Questa funzione è stata introdotta con at. js 2. x. Questa funzione non è disponibile per at. js versione 1.*x*.

| Chiave | Type (Tipo) | Obbligatorio | Descrizione |
| --- | --- | --- | --- |
| consumerId | Stringa | No | Il valore predefinito è la mbox globale del client, se non specificato. Questa chiave si utilizza per generare l’ID dati supplementare utilizzato per l’integrazione A4T. |
| richiesta | Oggetto | Sì | Vedi la tabella Richieste di seguito. |
| timeout | Numero | No | timeout richiesta. Se non specificato, si utilizza il timeout predefinito di at.js. |

## Richiesta

| Nome campo | Obbligatorio | Limitazioni | Descrizione |
| --- | --- | --- | --- |
| request &gt; id | No | Uno tra `tntId`, `thirdPartyId` e `marketingCloudVisitorId` è obbligatorio. |
| Request &gt; id &gt; thirdPartyId | No | Dimensione massima = 128 |
| Request &gt; prefetch | No |
| Request &gt; prefetch &gt; views | No | Numero massimo: 50<br>Nome non vuoto<br>Lunghezza nome `<=` 128<br>Lunghezza valore `<=` 5000<br>Il nome deve iniziare con “profile”<br>Nomi non consentiti: “orderId”, “orderTotal”, “productPurchasedId” | Passa i parametri da utilizzare per recuperare le visualizzazioni rilevanti nelle attività attive. |
| Request &gt; prefetch &gt; views &gt; profileParameters | No | Numero massimo: 50<br>Nome non vuoto<br>Lunghezza nome `<=` 128<br>Lunghezza valore `<=` 5000<br>Il nome deve iniziare con “profile” | Passa i parametri di profilo da utilizzare per recuperare le visualizzazioni rilevanti nelle attività attive. |
| Request &gt; prefetch &gt; views &gt; product | No |
| Request &gt; prefetch &gt; views &gt; product -&gt; id | No | Non vuoto<br>Dimensione massima = 128 | Passa gli ID prodotto da utilizzare per recuperare le visualizzazioni rilevanti nelle attività attive. |
| Request &gt; prefetch &gt; views &gt; product &gt; categoryId | No | Non vuoto<br>Dimensione massima = 128 | Passa gli ID categoria prodotto da utilizzare per recuperare le visualizzazioni rilevanti nelle attività attive. |
| Request &gt; prefetch &gt; views &gt; order | No |
| Request &gt; prefetch &gt; views &gt; order &gt; id | No | Lunghezza massima = 250 | Passa gli ID ordine da utilizzare per recuperare le visualizzazioni rilevanti nelle attività attive. |
| Request &gt; prefetch &gt; views &gt; order &gt; total | No | Totale `>=` 0 | Passa i totali dell’ordine da utilizzare per recuperare le visualizzazioni rilevanti nelle attività attive. |
| Request &gt; prefetch &gt; views &gt; order &gt; purchasedProductIds | No | Nessun valore vuoto<br>Lunghezza max di ogni valore: 50<br>Concatenata e separata da virgole<br>Lunghezza totale ID prodotto `<=` 250 | Passa gli ID prodotti acquistati da utilizzare per recuperare le visualizzazioni rilevanti nelle attività attive. |
| Request &gt; execute | No |
| Request &gt; execute &gt; pageLoad | No |
| Request &gt; execute &gt; pageLoad &gt; parameters | No | Numero massimo: 50<br>Nome non vuoto<br>Lunghezza nome `<=` 128<br>Lunghezza valore `<=` 5000<br>Il nome non deve iniziare con “profile”.<br>Nomi non consentiti: “orderId&quot;, “orderTotal&quot;, “productPurchasedId&quot; | Recupera le offerte con i parametri specificati al caricamento della pagina. |
| Request &gt; execute &gt; pageLoad &gt; profileParameters | No | Numero massimo: 50<br>Nome non vuoto<br>Lunghezza nome `<=` 128<br>Lunghezza valore `<=`256<br>Il nome non deve iniziare con “profile&quot;. | Recupera le offerte con i parametri del profilo specificati al caricamento della pagina. |
| Request &gt; execute &gt; pageLoad &gt; product | No |
| Request &gt; execute &gt; pageLoad &gt; product -&gt; id | No | Non vuoto<br>Dimensione massima = 128 | Recupera le offerte con gli ID prodotto specificati al caricamento della pagina. |
| Request &gt; execute &gt; pageLoad &gt; product &gt; categoryId | No | Non vuoto<br>Dimensione massima = 128 | Recupera le offerte con gli ID categoria prodotto specificati al caricamento della pagina. |
| Request &gt; execute &gt; pageLoad &gt; order | No |
| Request &gt; execute &gt; pageLoad &gt; order &gt; id | No | Lunghezza massima = 250 | Recupera le offerte con gli ID ordine specificati al caricamento della pagina. |
| Request &gt; execute &gt; pageLoad &gt; order &gt; total | No | `>=` 0 | Recupera le offerte con i totali dell’ordine specificati al caricamento della pagina. |
| Request &gt; execute &gt; pageLoad &gt; order &gt; purchasedProductIds | No | Nessun valore vuoto<br>Lunghezza max di ogni valore: 50<br>Concatenata e separata da virgole<br>Lunghezza totale ID prodotto `<=` 250 | Recupera le offerte con gli ID prodotti acquistati specificati al caricamento della pagina. |
| Request &gt; execute &gt; mboxes | No | Dimensione massima = 50<br>Nessun elemento null |
| Request &gt; execute &gt; mboxes&gt;mbox | Sì | Non vuoto<br>No suffisso ’-clicked’<br>Dimensione massima = 250<br>Caratteri consentiti: `'-, ._\/=:;&!@#$%^&*()_+|?~[]{}'` | Nome della mbox. |
| Request &gt; execute &gt; mboxes&gt;mbox&gt;index | Sì | No null<br>Univoco<br>`>=` 0 | Nota che l’indice non rappresenta l’ordine di elaborazione delle mbox. Come in una pagina web con diverse mbox regionali, non è possibile specificarne l’ordine di elaborazione. |
| Request &gt; execute &gt; mboxes &gt; mbox &gt; parameters | No | Numero massimo = 50<br>Nome non vuoto<br>Lunghezza nome `<=` 128<br>Lunghezza valore `<=` 5000<br>Il nome non deve iniziare con “profile&quot;.<br>Nomi non consentiti: “orderId”, “orderTotal”, “productPurchasedId” | Recupera le offerte per una data mbox con i parametri specificati. |
| Request &gt; execute &gt; mboxes&gt;mbox&gt;profileParameters | No | Numero massimo = 50<br>Nome non vuoto<br>Lunghezza nome `<=` 128<br>Lunghezza valore `<=`256<br>Il nome non deve iniziare con “profile&quot;. | Recupera le offerte per una data mbox con i parametri del profilo specificati. |
| Request &gt; execute &gt; mboxes&gt;mbox &gt; product | No |
| Request &gt; execute &gt; mboxes &gt; mbox &gt; product &gt; id | No | Non vuoto<br>Dimensione massima = 128 | Recupera le offerte per una data mbox con gli ID prodotto specificati. |
| Request &gt; execute &gt; mboxes &gt; mbox &gt; product &gt; categoryId | No | Non vuoto<br>Dimensione massima = 128 | Recupera le offerte per una data mbox con gli ID categoria prodotto specificati. |
| Request &gt; execute &gt; mboxes &gt; mbox &gt; order | No |
| Request &gt; execute &gt; mboxes&gt;mbox &gt; order &gt; id | No | Lunghezza massima = 250 | Recupera le offerte per una data mbox con gli ID dell’ordine specificati. |
| Request &gt; execute &gt; mboxes &gt; mbox &gt; order &gt; total | No | `>=` 0 | Recupera le offerte per una data mbox con i totali dell’ordine specificati. |
| Request &gt; execute &gt; mboxes &gt; mbox &gt; order &gt; purchasedProductIds | No | Nessun valore vuoto<br>Lunghezza massima di ogni valore = 50<br>Concatenata e separata da virgole<br>Lunghezza totale ID prodotto `<=` 250 | Recupera le offerte per una data mbox con gli ID dei prodotti acquistati dell’ordine specificati. |

## Richiama `getOffers()` per tutte le visualizzazioni

```
adobe.target.getOffers({
    prefetch: {
      views: []
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

## Recupera ed esegui il rendering di dati da più mbox tramite getoffers () e applyoffers () {#multiple}

at. js 2. x consente di recuperare più mbox tramite l&#39; `getOffers()` API. Potete anche recuperare dati per più mbox e quindi utilizzare `applyOffers()` per eseguire il rendering dei dati in posizioni diverse identificati da un selettore CSS.

L&#39;esempio seguente mostra una semplice pagina HTML con implementazione. js 2. x implementata:

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

Si supponga di disporre di tre contenitori che si desidera modificare tramite il contenuto ricevuto [!DNL Target]. Potete creare una singola richiesta per tre mbox in cui ogni mbox ha contenuto da rappresentare nel rispettivo contenitore.

La richiesta e il codice di rendering possono avere l&#39;aspetto seguente:

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

Nella `request > prefetch > mboxes` sezione sono disponibili tre mbox diverse. Se la richiesta è stata completata correttamente, riceverete la risposta per ogni mbox da `response > prefetch > mboxes`. Una volta fornite le risposte e le posizioni da utilizzare per il rendering, potete richiamare `applyOffers()` il rendering del contenuto recuperato [!DNL Target]. In questo esempio abbiamo la seguente mappatura:

* mbox 1 &gt; Selettore CSS # container 1
* mbox 2 &gt; Selettore CSS # container 2
* mbox 3 &gt; Selettore CSS # container 3

Questo esempio utilizza la variabile count per creare i selettori CSS. In uno scenario reale potete utilizzare una mappatura diversa tra il selettore CSS e la mbox.

Questo esempio può essere utilizzato `prefetch > mboxes`anche `execute > mboxes`da questo esempio. Verifica che se utilizzi la preacquisizione in `getOffers()`, devi anche usare la preacquisizione nella `applyOffers()` chiamata.