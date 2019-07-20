---
description: 'Informazioni sulla funzione adobe.target.applyOffer(options) per at.js. '
keywords: adobe.target.notification;element;selector;notification;extension
seo-description: Informazioni sulla funzione adobe.target.applyOffer(options) per la libreria at.js JavaScript di Adobe Target.
seo-title: Informazioni sulla funzione adobe.target.applyOffer(options) per la libreria at.js JavaScript di Adobe Target.
solution: Target
subtopic: Introduzione
title: adobe.target.applyOffer(options)
topic: Standard
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# adobe.target.applyOffer(options) {#reference_BBE83F513B5B4E03BBC3F50D90864245}

Questa funzione applica il contenuto di risposta.

>[!NOTE]
>
>`applyOffer` richiede il parametro `mbox`. Se non viene specificato alcun nome mbox, si verificherà un errore.

Il parametro delle opzioni è obbligatorio e ha la seguente struttura:

| Chiave | Tipo | Obbligatorio | Descrizione |
|--- |--- |--- |--- |
| mbox | Stringa | Sì | Nome mbox<br>Con at.js 1.3.0 (e versioni successive), Target impone l’utilizzo della chiave mbox. Questa chiave era già richiesta in passato, ma Target ora ne impone l’utilizzo per garantire la corretta convalida di Target e il corretto utilizzo di questa funzione da parte dei clienti. |
| selector | Elemento Stringa o DOM | No | Elemento HTML o selettore CSS utilizzato per identificare l'elemento HTML in cui Target deve inserire il contenuto dell'offerta. Se il selettore non viene fornito, target presuppone che l'elemento HTML che dovremmo usare sia HTML HEAD. |
| offerta | Array | Sì | Azioni di array che devono essere applicate all'elemento. |

## Esempio {#section_D8D6A17B73DE4542937CDB687193A5CC}

Nell'esempio seguente viene illustrato come utilizzare insieme `getOffer` e `applyOffer`:

```
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
