---
description: 'Informazioni sulla funzione targetpageparams () per at. js. '
keywords: adobe.target.notification;element;selector;notification;extension
seo-description: Informazioni sulla funzione targetpageparams () per la libreria javascript di Adobe Target nella libreria javascript. js.
seo-title: Informazioni sulla funzione targetpageparams () per la libreria javascript di Adobe Target nella libreria javascript. js.
solution: Target
subtopic: Introduzione
title: targetPageParams()
topic: Standard
translation-type: tm+mt
source-git-commit: 1e2b435244294ccac5d852369f84003a54c18dc0

---


# targetPageParams() {#reference_B235C9F6DA79449ABE3E23F914FEABAE}

Questo metodo consente di allegare i parametri alla mbox globale dall’esterno del codice di richiesta.

Questa funzione è molto utile per includere lo stesso insieme di parametri su più chiamate alla mbox. La funzione deve essere definita dal cliente. Dovrebbe restituire un array di parametri che verranno passati solo alla richiesta mbox globale. Questa funzione può essere definita prima che at.js sia caricato o in **[!UICONTROL Configurazione]** &gt; **[!UICONTROL Implementazione]** &gt; **[!UICONTROL Modifica impostazioni at.js]** &gt; **[!UICONTROL Impostazioni codice]** &gt; **[!UICONTROL Intestazione della libreria]**.

Puoi trasmettere parametri a target-global-mbox utilizzando la funzione `targetPageParams()` in uno dei seguenti modi:

* Un elenco delimitato dal simbolo &amp;
* Un array
* Un oggetto JSON

## Esempi

Elenco delimitato dal simbolo &amp; (i valori devono avere la codifica URL):

```
function targetPageParams() { 
    return "param1=value1&param2=value2&p3=hello%20world"; 
}
```

Array (i valori non devono avere la codifica URL):

```
targetPageParams = function() { 
     return ["a=1", "b=2", "c=hello world"]; 
};
```

JSON (i valori non devono avere la codifica URL):

```
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
