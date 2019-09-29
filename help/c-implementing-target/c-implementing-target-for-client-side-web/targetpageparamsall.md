---
description: 'Informazioni sulla funzione targetPageParamsAll() per at.js. '
keywords: targetPageParamsAll;targetpageparamsall;PageParamsAll;pageparamsall;parametri pagina;parametri page;at.js;funzioni;funzione
seo-description: Informazioni sulla funzione targetPageParamsAll() per la libreria JavaScript at.js di Adobe Target.
seo-title: Informazioni sulla funzione targetPageParamsAll() per la libreria JavaScript at.js di Adobe Target.
solution: Target
subtopic: Introduzione
title: targetPageParamsAll()
topic: Standard
translation-type: tm+mt
source-git-commit: ef2c4ac78fef5889d5a6e9e053dfd36b77919dd4

---


# targetPageParamsAll()

Questo metodo consente di allegare i parametri a tutte le mbox dall’esterno del codice di richiesta.

Questa funzione è molto utile per includere lo stesso insieme di parametri su più chiamate alla mbox. La funzione deve essere definita dal cliente. Dovrebbe restituire un array di parametri che verranno passati a tutte le richieste mbox nella pagina. Questa funzione può essere definita prima che at.js sia caricato o in **[!UICONTROL Configurazione]** &gt; **[!UICONTROL Implementazione]** &gt; **[!UICONTROL Modifica impostazioni at.js]** &gt; **[!UICONTROL Impostazioni codice]** &gt; **[!UICONTROL Intestazione della libreria]**.

Puoi trasmettere parametri a target-global-mbox utilizzando la funzione targetPageParamsAll() in uno dei seguenti modi:

* Un elenco delimitato dal simbolo &amp;
* Un array
* Un oggetto JSON

## Esempi

Elenco delimitato dal simbolo &amp; (i valori devono avere la codifica URL):

```
function targetPageParamsAll() { 
    return "param1=value1&param2=value2&p3=hello%20world"; 
}
```

Array (i valori non devono avere la codifica URL):

```
targetPageParamsAll = function() { 
     return ["a=1", "b=2", "c=hello world"]; 
};
```

JSON (i valori non devono avere la codifica URL):

```
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
