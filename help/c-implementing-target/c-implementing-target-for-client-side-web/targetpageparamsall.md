---
keywords: targetPageParamsAll;targetpageparamsall;PageParamsAll;pageparamsall;parametri pagina;parametri page;at.js;funzioni;funzione
description: Utilizzate la funzione targetPageParamsAll() per la libreria JavaScript di Adobe Target at.js  per allegare parametri a tutte le mbox dall'esterno del codice della richiesta.
title: Come si utilizza la funzione targetPageParamsAll()?
feature: at.js
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 71%

---


# targetPageParamsAll()

Questo metodo consente di allegare i parametri a tutte le mbox dall’esterno del codice di richiesta.

Questa funzione è molto utile per includere lo stesso insieme di parametri su più chiamate alla mbox. La funzione deve essere definita dal cliente. Dovrebbe restituire un array di parametri che verranno passati a tutte le richieste mbox nella pagina. Questa funzione può essere definita prima del caricamento di at.js oppure in **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** > **[!UICONTROL Edit]** > **[!UICONTROL Code Settings]** > **[!UICONTROL Library Header]**.

Puoi trasmettere parametri a target-global-mbox utilizzando la funzione targetPageParamsAll() in uno dei seguenti modi:

* Un elenco delimitato dal simbolo &amp;
* Un array
* Un oggetto JSON

## Esempi

Elenco delimitato dal simbolo &amp; (i valori devono avere la codifica URL):

```javascript
function targetPageParamsAll() { 
    return "param1=value1&param2=value2&p3=hello%20world"; 
}
```

Array (i valori non devono avere la codifica URL):

```javascript
targetPageParamsAll = function() { 
     return ["a=1", "b=2", "c=hello world"]; 
};
```

JSON (i valori non devono avere la codifica URL):

```javascript
targetPageParamsAll = function() { 
  return { 
    "a": 1, 
    "b": 2, 
    "profile": { 
        "age": 26, 
        "country": { 
          "city": "San Francisco" 
        } 
      } 
  }; 
};
```
