---
description: 'Informazioni sulla funzione adobe. target. applyoffer (options) per at. js. '
keywords: adobe.target.notification;element;selector;notification;extension
seo-description: Informazioni sulla funzione adobe. target. applyoffer (options) per la libreria javascript di Adobe Target nella libreria javascript. js.
seo-title: Informazioni sulla funzione adobe. target. applyoffer (options) per la libreria javascript di Adobe Target nella libreria javascript. js.
solution: Target
subtopic: Introduzione
title: adobe.target.applyOffers(options)
topic: Standard
translation-type: tm+mt
source-git-commit: 126f62d8966beb8157f54f87cf68b092fe976c51

---


# adobe. target. applybid (options) - at. js 2. x

Questa funzione ti consente di applicare più di un’offerta recuperata da `adobe.target.getOffers()`.

>[!NOTE]
>
>Questa funzione è stata introdotta con at. js 2. x. Questa funzione non è disponibile per at. js versione 1.*x*.

| Chiave | Type (Tipo) | Obbligatorio | Descrizione |
| --- | --- | --- | --- |
| selector | Stringa | No | Elemento HTML o selettore CSS utilizzato per identificare l’elemento HTML in cui [!DNL Target] deve inserire il contenuto dell’offerta. Se non si fornisce un selettore, [!DNL Target] suppone che l’elemento HTML da usare sia HTML HEAD. |
| Risposta | Oggetto | Sì | Oggetto di risposta da `getOffers()`.<br>Vedi la tabella Richieste di seguito. |

## Risposta

| Nome campo | Descrizione |
| --- | --- |
| response &gt; prefetch &gt; views &gt; options &gt; content | Nota che il contenuto di “option&quot; non è definito e dipende direttamente dalla struttura tipo/modello dell’opzione. |
| response &gt; prefetch &gt; views &gt; options &gt; type | Tipo di opzione. Riflette il tipo del campo “content&quot;. Il tipo supportato è “actions&quot;. |
| response &gt; prefetch &gt; views &gt; state | Un token opaco da inoltrare con la notifica sul display per la visualizzazione |
| response &gt; prefetch  &gt; views &gt; options &gt; responseTokens | Contiene la mappa dei valori `responseTokens` raccolti quando l’opzione corrente era in fase di elaborazione. |
| response &gt; prefetch  &gt; views &gt; analytics &gt; payload | Payload di Analytics per l’integrazione sul lato client da inviare ad Analytics dopo l’applicazione della visualizzazione. |
| response &gt; prefetch  &gt; views &gt; trace | L’oggetto contenente tutti i dati di trace per la chiamata di preacquisizione per la visualizzazione.<br>L’oggetto trace includerà anche una versione per la traccia.<br>L’oggetto trace includerà anche i dettagli della visualizzazione corrente. |
| response &gt; prefetch  &gt; views &gt; options &gt; eventToken | La registrazione degli eventi è eseguita per opzione. Per ogni opzione applicata, il rispettivo token evento deve essere aggiunto all’elenco dei token di notifica. Una visualizzazione è composta da più opzioni. Se sono state applicate e visualizzate tutte le opzioni, è necessario includere tutti i valori `eventTokens` nella notifica. |
| response &gt; prefetch  &gt; views &gt; name | Il nome della visualizzazione leggibile dall’utente. |
| response &gt; prefetch  &gt; views &gt; metrics | Metriche di reporting da controllare e segnalare a [!DNL Target]. Al momento, è disponibile il supporto alla metrica di solo clic. Se si verifica un clic sull’elemento, è necessario raccogliere il valore `eventTokens` adeguato e inviare una notifica. |
| response &gt; prefetch  &gt; views &gt; key | Chiave o impronta digitale che identifica la visualizzazione. |
| response &gt; prefetch  &gt; views &gt; id | ID della visualizzazione. |
| response &gt; notifications &gt; id | ID notifica. |
| response &gt; notifications &gt; events &gt; type | Tipo di notifica, clic o visualizzazione. |
| response &gt; notifications &gt; events &gt; trace | La traccia per l’evento di notifica. |
| response &gt; notifications &gt; events &gt; token | Token inviato con l’evento di notifica. |
| response &gt; notifications &gt; events &gt; timestamp | La marca temporale inviata con l’evento di notifica. |
| response &gt; notifications &gt; events &gt; errorCode | Se la notifica non riesce, il codice indica il motivo dell’errore. |
| response &gt; notifications &gt; events | Gli eventi registrati o non registrati per la notifica corrente. |
| response &gt; notifications | Indica le notifiche registrate o non riuscite. |
| response &gt; execute &gt; mboxes &gt; mbox &gt; trace | L’oggetto contenente tutti i dati di trace per la singola richiesta mbox. |
| response &gt; execute &gt; mboxes &gt; mbox &gt; responseTokens | Contiene la mappa di `responseTokens` per un’esecuzione specifica della richiesta mbox. |
| response &gt; execute &gt; mboxes &gt; mbox &gt; option &gt; content | Nota che il contenuto di “option&quot; non è definito e dipende direttamente dalla struttura tipo/modello dell’opzione. |
| response &gt; execute &gt; mboxes &gt; mbox &gt; option &gt; type | Tipo di opzione. Riflette il tipo del campo “content&quot;. I tipi supportati sono: html, redirect, JSON e dinamico. |
| response &gt; execute &gt; mboxes &gt; mbox &gt; options | Opzione Risposta. |
| response &gt; execute &gt; mboxes &gt; mbox &gt; metrics &gt; eventToken | Token dell’evento di clic. |
| response &gt; execute &gt; mboxes &gt; mbox &gt; metrics &gt; type | &quot;click&quot; |
| response &gt; execute &gt; mboxes &gt; mbox &gt; metrics | Contiene l’elenco `clickThrough` delle metriche. |
| response &gt; execute &gt; mboxes &gt; mbox &gt; mbox | Nome della mbox. |
| response &gt; execute &gt; mboxes &gt; mbox &gt;index | Indica che la risposta è per la mbox con questo indice della richiesta. |
| response &gt; execute &gt; mboxes &gt; mbox &gt; analytics &gt; payload | Payload di Analytics per l’integrazione sul lato client da inviare ad Analytics dopo l’applicazione della mbox. (Vedi la sezione Campagne abilitate per A4T.) |
| response &gt; execute &gt; mboxes | Elenco delle mbox eseguite. |
| response &gt; execute &gt; pageLoad &gt; options &gt; content | Nota che il contenuto di “option&quot; non è definito e dipende direttamente dalla struttura tipo/modello dell’opzione. |
| response &gt; execute &gt; pageLoad &gt; options &gt; type | Tipo di opzione. Riflette il tipo del campo “content&quot;. I tipi supportati sono: html, redirect, JSON, dinamico e “action&quot;. |
| response &gt; execute &gt; pageLoad &gt; options | Opzioni non raggruppate per visualizzazioni (target-global-mbox + opzioni di attività con viste non raggruppate per viste). |
| response &gt; execute &gt; pageLoad &gt; metrics | Metriche di clic che non erano impostate per appartenere a una visualizzazione specifica. |
| response &gt; execute &gt; pageLoad &gt; trace | L’oggetto contenente tutti i dati trace per la richiesta pageload. |
| response &gt; execute &gt; pageLoad &gt; analytics &gt; payload | Payload di Analytics per l’integrazione sul lato client da inviare ad Analytics dopo l’applicazione del contenuto “pageLoad&quot;. (Vedi la sezione Campagne abilitate per A4T.) |

## Esempio di chiamata applyOffers()

```
adobe.target.applyOffers({response:{
  "execute": {
    "pageLoad": {
      "options": [{
        "type": "html",
        "content": "page-load"
      },
      {
        "type": "actions",
        "content": [{
          "type": "setHtml",
          "content": "<h1>Container 1</h1>",
          "selector": "#container1",
          "cssSelector": "#container1"
        },
        {
          "type": "setHtml",
          "content": "<h3>Container 3</h3>",
          "selector": "#container3",
          "cssSelector": "#container3"
        }]
      }],
 
 
      "metrics": [{
        "type": "click",
        "selector": "#container1",
        "eventToken": "page-load-click-metric" 
      }]
    }
  }
}});
```

## Esempio di chiamata della catena di promesse con `getOffers()` e `applyOffers()`, perché queste funzioni si basano su promesse

```
adobe.target.getOffers({...})
.then(response => adobe.target.applyOffers({ response: response }))
.then(() => console.log("Success"))
.catch(error => console.log("Error", error));
```
