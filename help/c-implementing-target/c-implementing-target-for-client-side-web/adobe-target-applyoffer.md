---
keywords: adobe.target.applyOffer;applyOffer;applyoffer;applica offerta;at.js;funzioni;funzione
description: Utilizza la funzione adobe.target.applyOffer() per la libreria JavaScript at.js di Adobe Target per applicare il contenuto della risposta.
title: Come si utilizza la funzione adobe.target.applyOffer()?
feature: at.js
role: Sviluppatori
translation-type: tm+mt
source-git-commit: 3a71ae60a89a802ca469fa7acd583157221bdeee
workflow-type: tm+mt
source-wordcount: '177'
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
| selector | Elemento Stringa o DOM | No | Elemento HTML o selettore CSS utilizzato per identificare l&#39;elemento HTML in cui Target deve inserire il contenuto dell&#39;offerta. Se il selettore non viene fornito, Target presuppone che l&#39;elemento HTML utilizzi HTML HEAD. |
| Offerta | Array | Sì | Azioni di array che devono essere applicate all&#39;elemento. |

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
