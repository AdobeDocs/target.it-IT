---
keywords: targetPageParams;targetpageparams;pageParams;pageparams;parametri pagina;parametri page;at.js;funzioni;funzione
description: Informazioni sulla funzione targetPageParams() per la libreria JavaScript at.js di Adobe Target.
title: Targetpageparams()
feature: at.js
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 88%

---


# targetPageParams() {#reference_B235C9F6DA79449ABE3E23F914FEABAE}

Questo metodo consente di allegare i parametri alla mbox globale dall’esterno del codice di richiesta.

Questa funzione è molto utile per includere lo stesso insieme di parametri su più chiamate alla mbox. La funzione deve essere definita dal cliente. Dovrebbe restituire un array di parametri che verranno passati solo alla richiesta mbox globale. Questa funzione può essere definita prima del caricamento di at.js oppure in **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** > **[!UICONTROL Edit]** > **[!UICONTROL Library Header]**.

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
