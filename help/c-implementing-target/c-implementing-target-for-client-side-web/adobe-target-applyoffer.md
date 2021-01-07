---
keywords: adobe.target.applyOffer;applyOffer;applyoffer;apply offer;at.js;functions;function
description: Informazioni sulla funzione adobe.target.applyOffer(options) per la libreria at.js JavaScript di Adobe Target.
title: adobe.target.applyOffer(options)
feature: at.js
translation-type: tm+mt
source-git-commit: 6bb75e3b818a71af323614d9150e50e3e9f611b7
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 100%

---


# adobe.target.applyOffer(options)

Questa funzione applica il contenuto di risposta.

>[!NOTE]
>
>`applyOffer` richiede il parametro `mbox`. Se non viene specificato alcun nome mbox, si verificherà un errore.

Il parametro delle opzioni è obbligatorio e ha la seguente struttura:

| Chiave | Tipo | Obbligatorio | Descrizione |
|--- |--- |--- |--- |
| mbox | Stringa | Sì | Nome mbox<br>Con at.js 1.3.0 (e versioni successive), Target impone l’utilizzo della chiave mbox. Questa chiave era già richiesta in passato, ma Target ora ne impone l’utilizzo per garantire la corretta convalida di Target e il corretto utilizzo di questa funzione da parte dei clienti. |
| selector | Elemento Stringa o DOM | No | Elemento HTML o selettore CSS utilizzato per identificare l&#39;elemento HTML in cui Target deve inserire il contenuto dell&#39;offerta. Se il selettore non viene fornito, target presuppone che l&#39;elemento HTML che dovremmo usare sia HTML HEAD. |
| offerta | Array | Sì | Azioni di array che devono essere applicate all&#39;elemento. |

## Esempio {#section_D8D6A17B73DE4542937CDB687193A5CC}

Nell&#39;esempio seguente viene illustrato come utilizzare insieme `getOffer` e `applyOffer`:

```javascript
adobe.target.getOffer({   
  "mbox": "mbox",   
  "success": function(offers) {           
        adobe.target.applyOffer( {  
           "mbox": "mbox", 
           "offer": offers  
        } ); 
  },   
  "error": function(status, error) {           
      if (console && console.log) { 
        console.log(status); 
        console.log(error); 
      } 
  }, 
 "timeout": 5000 
}); 
```
