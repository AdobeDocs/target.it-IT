---
description: 'Informazioni sulla funzione adobe. target. applyoffer (options) per at. js. '
keywords: adobe.target.notification;element;selector;notification;extension
seo-description: Informazioni sulla funzione adobe. target. applyoffer (options) per la libreria javascript di Adobe Target nella libreria javascript. js.
seo-title: Informazioni sulla funzione adobe. target. applyoffer (options) per la libreria javascript di Adobe Target nella libreria javascript. js.
solution: Target
subtopic: Introduzione
title: adobe.target.applyOffer(options)
topic: Standard
translation-type: tm+mt
source-git-commit: 15da223709bfceecb094b6c9f9e78ba5ce0d8256

---


# adobe.target.applyOffer(options) {#reference_BBE83F513B5B4E03BBC3F50D90864245}

Questa funzione applica il contenuto di risposta.

>[!NOTE]
>
>`applyOffer` richiede il parametro `mbox`. Se non viene specificato alcun nome mbox, si verificherà un errore.

Il parametro delle opzioni è obbligatorio e ha la seguente struttura:

| Chiave | Type (Tipo) | Obbligatorio | Descrizione |
|--- |--- |--- |--- |
| mbox | Stringa | Sì | Nome mbox con<br>at. js 1.3.0 (e versione successiva) in cui viene richiesto di applicare il tasto mbox. Questa chiave era già richiesta in passato, ma Target ora ne impone l’utilizzo per garantire la corretta convalida di Target e il corretto utilizzo di questa funzione da parte dei clienti. |
| selector | Elemento Stringa o DOM | No | Elemento HTML o selettore CSS utilizzato per identificare l&#39;elemento HTML in cui Target deve inserire il contenuto dell&#39;offerta. Se il selettore non viene fornito, target presuppone che l&#39;elemento HTML che dovremmo usare sia HTML HEAD. |
| offerta | Array | Sì | Azioni di array che devono essere applicate all&#39;elemento. |

## Esempio {#section_D8D6A17B73DE4542937CDB687193A5CC}

Nell&#39;esempio seguente viene illustrato come utilizzare insieme `getOffer` e `applyOffer`:

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
