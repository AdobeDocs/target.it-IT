---
keywords: parametri mbox globali;targetPageParams;stringa query;array;json;dtm
description: Scopri come utilizzare la funzione targetPageParams per passare informazioni di targeting o di contesto aggiuntive alla mbox globale Adobe [!DNL Target] .
title: Come faccio a trasmettere parametri a una mbox globale?
feature: at.js
role: Developer
exl-id: 37d143af-83a8-48fd-91eb-58f21f8c7b94
translation-type: tm+mt
source-git-commit: 824743300725bbd39077882a0971a9ccb4f753ab
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 60%

---

# Trasmettere i parametri a una mbox globale

La funzione JavaScript `targetPageParams` viene utilizzata per trasmettere parametri alla mbox globale in [!DNL Adobe Target]. Questo è necessario in qualsiasi scenario in cui informazioni di targeting/contesto aggiuntive devono essere trasmesse in [!DNL Target].

Ad esempio, in un’attività [!DNL Recommendations] , utilizza i parametri per rappresentare il prodotto o la categoria corrente che viene visualizzata.

Il codice per chiamare la funzione JavaScript deve precedere la mbox globale sulla pagina, sia che la mbox globale sia attivata come parte di at.js o sia inclusa manualmente nel codice della pagina.

>[!NOTE]
>
>Se desideri aggiungere parametri a tutte le mbox sulla pagina e non solo alla mbox globale, utilizza la funzione [targetPageParamsAll()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparamsall.md) .

Puoi trasmettere parametri a `target-global-mbox` utilizzando la funzione `targetPageParams()` in uno dei seguenti modi:

* Un array
* Un oggetto JSON
* Un elenco delimitato dal simbolo &amp;

Utilizza questi tre metodi per verificare che i parametri vengano trasferiti correttamente. Potresti anche essere in grado di verificare il trasferimento di parametri utilizzando il [debugger Adobe Experience Cloud](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html).

È necessario definire la funzione JavaScript prima di aggiungere la mbox globale alla pagina. Il nome deve essere `targetPageParams`.

## Stringa di query

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
          return "p1=v1&p2=v2&p3=hello%20world";
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

## Array

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

## JSON

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
* `profile.memberStatus`=Oro
* `profile.country.city`=San Francisco
