---
keywords: global mbox parameters;targetPageParams;query string;array;json;dtm;dynamic tag management
description: La funzione targetPageParams di JavaScript viene utilizzata per trasmettere parametri alla mbox globale. È utile in tutte le situazioni in cui occorre passare a Target informazioni di targeting o di contesto aggiuntive.
title: Trasmettere i parametri a una mbox globale
feature: null
subtopic: Getting Started
topic: Standard
uuid: 058f0ef5-037a-4daf-8a1e-a9c7ecc7f0bd
translation-type: tm+mt
source-git-commit: 8bf89f30fec597b983067ec4604dba09a9ec2832
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 73%

---


# Trasmettere i parametri a una mbox globale{#pass-parameters-to-a-global-mbox}

La funzione `targetPageParams` di JavaScript viene utilizzata per trasmettere parametri alla mbox globale. This is needed in any scenario where additional targeting/context information is to be passed into [!DNL Target].

For example, in a [!DNL Recommendations] activity, use the parameters to represent the current product or category that is being viewed.

Il codice per chiamare la funzione JavaScript deve precedere la mbox globale sulla pagina, a prescindere dal fatto che la mbox globale venga attivata come parte di at.js o sia inclusa manualmente nel codice della pagina.

>[!NOTE]
>
>If you want to add parameters to all mboxes on the page, not just to the global mbox, use the [targetPageParamsAll()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparamsall.md) function.

Puoi trasmettere parametri a `target-global-mbox` utilizzando la funzione `targetPageParams()` in uno dei seguenti modi:

* Un array
* Un oggetto JSON
* Un elenco delimitato dal simbolo &amp;

Utilizza questi tre metodi per verificare che i parametri vengano trasferiti correttamente. Potresti anche essere in grado di verificare il trasferimento di parametri utilizzando il [debugger Adobe Experience Cloud](https://docs.adobe.com/content/help/en/debugger/using/experience-cloud-debugger.html).

È necessario definire la funzione JavaScript prima di aggiungere la mbox globale alla pagina. Il nome deve essere `targetPageParams`.

**Stringa di query**

```
p1=v1&p2=v2&p3=hello%20world
```

* Nome: `targetPageParams`
* Valore restituito: parametri delimitati da “&amp;”, con valori di parametro codificati tramite URL.

   Esempio:

   In questo esempio, p3 ha il valore `hello world`, il cui URL è codificato.

Quello che segue è un esempio dell&#39;aspetto potenziale del codice per la pagina:

```
<html> 
  <head> 
    <title>Title here..</title> 
    <script type="text/javascript"> 
        function targetPageParams() { 
           
<b>return "p1=v1&p2=v2&p3=hello%20world"</b>; 
        } 
    </script> 
    <script src="mbox.js" type="text/javascript"></script> 
  </head> 
  <body>Body here... 
  </body> 
</html>
```

In questo esempio vengono inviati i seguenti dati all&#39;edge della mbox:

* p1=v1
* p2=v2
* p3=hello world

**Array**

```
<!--window.-->targetPageParams = function() { 
  return ["a=1", "b=2", "c=hello world"]; 
}; 
```

I valori non devono avere la codifica URL. Ad esempio, se un valore contiene uno spazio, non è necessario codificare lo spazio.

In questo esempio vengono inviati i seguenti dati all&#39;edge della mbox:

* a=1
* b=2
* c=hello world

**JSON**

JSON è una potente modalità di trasferimento dei parametri. Target utilizza le chiavi oggetto di JSON per appiattire le strutture complesse in parametri semplici.

```
<!--window.-->targetPageParams = function() { 
  return { 
    "a": 1, 
    "b": 2, 
    "profile": { 
                  "memberStatus": Gold, 
                  "country": { 
                                "city": "San Francisco" 
                            } 
              } 
  }; 
}; 
```

I valori non devono avere la codifica URL. Ad esempio, “San Francisco” non richiede la codifica dello spazio. Lo spazio è sufficiente.

In questo esempio vengono inviati i seguenti dati all&#39;edge della mbox:

* a=1
* b=2
* `profile.age`=26
* `profile.country.city`=San Francisco