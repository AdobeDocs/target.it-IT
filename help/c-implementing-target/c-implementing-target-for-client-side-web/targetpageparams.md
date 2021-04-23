---
keywords: targetPageParams;targetpageparams;pageParams;pageparams;parametri pagina;parametri page;at.js;funzioni;funzione
description: Utilizza la funzione targetPageParams() per la libreria JavaScript Adobe [!DNL Target] at.js per allegare parametri alla mbox globale dall'esterno del codice di richiesta.
title: Come si utilizza la funzione targetPageParams()?
feature: at.js
role: Developer
exl-id: 0772b400-626c-45d8-a4b5-a12691978cf3
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 72%

---

# targetPageParams()

Questo metodo consente di allegare i parametri alla mbox globale dall’esterno del codice di richiesta.

Questa funzione è molto utile per includere lo stesso insieme di parametri su più chiamate alla mbox. La funzione deve essere definita dal cliente. Dovrebbe restituire un array di parametri che verranno passati solo alla richiesta mbox globale. Questa funzione può essere definita prima che at.js sia caricato o in **[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]** > **[!UICONTROL Modifica]** > **[!UICONTROL Intestazione libreria]**.

Puoi trasmettere parametri a target-global-mbox utilizzando la funzione `targetPageParams()` in uno dei seguenti modi:

* Un elenco delimitato dal simbolo &amp;
* Un array
* Un oggetto JSON

## Esempi

Elenco delimitato dal simbolo &amp; (i valori devono avere la codifica URL):

```javascript
function targetPageParams() { 
    return "param1=value1&param2=value2&p3=hello%20world"; 
}
```

Array (i valori non devono avere la codifica URL):

```javascript
targetPageParams = function() { 
     return ["a=1", "b=2", "c=hello world"]; 
};
```

JSON (i valori non devono avere la codifica URL):

```javascript
targetPageParams = function() { 
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
