---
keywords: adobe.target.applyOffer;applyOffer;applyoffer;applica offerta;at.js;funzioni;funzione
description: Utilizza la funzione adobe.target.applyOffer() per l'Adobe [!DNL Target] Libreria JavaScript at.js per applicare il contenuto della risposta.
title: Come si utilizza la funzione adobe.target.applyOffer()?
feature: at.js
role: Developer
exl-id: d230d48f-0d6c-4f55-96a0-681dd31e8d16
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 72%

---

# adobe.target.applyOffer(options)

Questa funzione consente di applicare il contenuto della risposta con [!DNL Adobe Target].

>[!NOTE]
>
>`applyOffer` richiede il parametro `mbox`. Se non viene specificato alcun nome mbox, si verificherà un errore.

Il parametro delle opzioni è obbligatorio e ha la seguente struttura:

| Chiave | Tipo | Obbligatorio | Descrizione |
|--- |--- |--- |--- |
| mbox | Stringa | Sì | Nome mbox<br>Con at.js 1.3.0 (e versioni successive), Target impone l’utilizzo della chiave mbox. Questa chiave era già richiesta in passato, ma Target ora ne impone l’utilizzo per garantire la corretta convalida di Target e il corretto utilizzo di questa funzione da parte dei clienti. |
| selector | Elemento Stringa o DOM | No | Elemento HTML o selettore CSS utilizzato per identificare l&#39;elemento HTML in cui Target deve inserire il contenuto dell&#39;offerta. Se il selettore non viene fornito, Target presuppone che l’elemento HTML utilizzi HTML HEAD. |
| Offerta | Array | Sì | Azioni di array che devono essere applicate all&#39;elemento. |

## Esempio  {#section_D8D6A17B73DE4542937CDB687193A5CC}

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
