---
keywords: adobe.target.getOffer;getOffer;getoffer;get offer;at.js;functions;function
description: Informazioni sulla funzione adobe.target.getOffer(options) per la libreria at.js JavaScript di Adobe Target.
title: adobe.target.getOffer(options)
feature: client-side
subtopic: Getting Started
topic: Standard
translation-type: tm+mt
source-git-commit: 8789d750e9e0245d88d54a8d3fe342e5b2e616fc
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 97%

---


# adobe.target.getOffer(options)

Questa funzione genera una richiesta per ottenere un’offerta di Target.

Puoi utilizzarlo con `adobe.target.applyOffer()` per elaborare la risposta o usare la tua gestione di successo. Il parametro delle opzioni è obbligatorio e ha la seguente struttura:

| Chiave | Tipo | Obbligatorio | Descrizione |
|--- |--- |--- |--- |
| mbox | Stringa | Sì | Nome Mbox |
| params | Oggetto | No | Parametri mbox. Un oggetto di coppie chiave-valore che presenta la struttura seguente:<br>`{ "param1": "value1", "param2": "value2"}` |
| success | Funzione | Sì | Callback da eseguire quando abbiamo ricevuto una risposta dal server. La funzione di callback di successo riceverà un singolo parametro che rappresenta un array di oggetti di offerta. Esempio di callback di successo:<br>`function handleSuccess(response){......}`<br>per informazioni dettagliate, consulta le risposte sottostanti. |
| error | Funzione | Sì | Callback da eseguire quando visualizziamo un errore. Ci sono alcuni casi che sono considerati di errore:<ul><li>Codice di stato HTTP diverso da 200 OK</li><li>La risposta non può essere analizzata. Ad esempio abbiamo generato in modo non corretto JSON o HTML invece di JSON.</li><li>La risposta contiene la chiave “Errore”. Ad esempio, è stata lanciata un&#39;eccezione sull&#39;Edge di una richiesta che non è stato possibile elaborare correttamente. Si può ricevere un errore se una mbox è bloccata e non è possibile recuperare alcun contenuto per essa, ecc. La funzione di callback di errore riceverà due parametri: stato ed errore. Ecco un esempio di callback di errore: `function handleError(status, error){......}`</li></ul>Vedi le risposte di errore qui sotto per i dettagli. |
| timeout | Numero | No | Timeout in millisecondi. Se non viene specificato, verrà utilizzato il timeout predefinito in at.js.<br>Il timeout predefinito può essere impostato dall’ [!DNL Target] interfaccia utente in [!UICONTROL Amministrazione > Implementazione]. |

## Esempi {#section_97C2D2E03E6549BEA7F4873E3F5E4A0D}

Aggiunta di parametri con getOffer() e utilizzo di applyOffer() per la gestione del successo:

```
adobe.target.getOffer({   
  "mbox": "target-global-mbox", 
  "params": { 
     "a": 1, 
     "b": 2 
  }, 
  "success": function(offer) {           
        adobe.target.applyOffer( {  
           "mbox": "target-global-mbox", 
           "offer": offer  
        } ); 
  },   
  "error": function(status, error) {           
      console.log('Error', status, error); 
  } 
});
```

Aggiunta di parametri e parametri di profilo con getOffer() e utilizzo di applyOffer () per la gestione del successo:

```
adobe.target.getOffer({   
  "mbox": "target-global-mbox", 
  "params": { 
     "a": 1, 
     "b": 2, 
     "profile.age": 27, 
     "profile.gender": "male" 
  }, 
  "success": function(offer) {           
        adobe.target.applyOffer( {  
           "mbox": "target-global-mbox", 
           "offer": offer  
        } ); 
  },   
  "error": function(status, error) {           
      console.log('Error', status, error); 
  } 
});
```

Utilizzo del timeout personalizzato e della gestione del successo personalizzato con getOffer():

“YOUR_OWN_CUSTOM_HANDLING_FUNCTION” è un segnaposto per una funzione che il cliente può definire.

```
adobe.target.getOffer({     
  "mbox": "target-global-mbox",   
  "success": function(offer) { 
    YOUR_OWN_CUSTOM_HANDLING_FUNCTION(offer);   
  }, 
  "error": function(status, error) {                 
    console.log('Error', status, error);   
  },   
  "timeout": 2000 
});
```

## Risposte {#section_CF9FD236EF794620BCBF84EB80160183}

Il parametro di risposta trasmesso al callback di successo sarà un array di azioni. Un&#39;azione è un oggetto che in genere presenta il formato seguente:

| Nome | Tipo | Descrizione |
|--- |--- |--- |
| action | Stringa | Tipo di azione da applicare all&#39;elemento identificato. |
| selector | Stringa | Rappresenta un selettore Sizzle. |
| cssSelector | Stringa | Selettore nativo DOM, utilizzato per l&#39;elemento che consente lo stato di pre-nascosto. |
| content | Stringa | Il contenuto da applicare all&#39;elemento identificato. |

## Esempio

```
{ 
    "sessionId": "1444512212156-384616", 
    "tntId": "1444512212156-384616.17_35", 
    "offers": [{ 
        "plugins": ["<script type=\"text/javascript\">\r\n/*mboxHighlight+ (1of2) v1 ==> Response Plugin*/\r\nwindow.ttMETA=(typeof(window.ttMETA)!='undefined')?window.ttMETA:[];window.ttMETA.push({'mbox':'target-global-mbox','campaign':'at: redirect ootb','experience':'Experience B','offer':'/at_redirect_ootb/experiences/1/pages/0/1442082890250'});window.ttMBX=function(x){var mbxList=[];for(i=0;i<ttMETA.length;i++){if(ttMETA[i].mbox==x.getName()){mbxList.push(ttMETA[i])}}return mbxList[x.getId()]}\r\n</script>"], 
        "actions": { 
            "content": [{ 
                "passMboxSession": false, 
                "selector": "body", 
                "action": "redirect", 
                "url": "https://example.com/04.html", 
                "includeAllUrlParameters": true 
            }] 
        } 
    }] 
}
```

## Risposte di errore {#section_1ACCE79AF2CB4FA2AD1371EA06AF129F}

I parametri “status” ed “error” trasmessi al callback di errore avranno il seguente formato:

| Nome | Tipo | Descrizione |
|--- |--- |--- |
| status | Stringa | Rappresenta lo stato di errore. Questo parametro può avere i seguenti valori:<ul><li>timeout: Indica che la richiesta è scaduta.</li><li>parseerror: indica che la risposta non può essere analizzata, ad esempio se si riceve HTML o testo normale anziché JSON.</li><li>error: indica un errore generale, ad esempio se si riceve uno stato HTTP diverso da 200 OK</li></ul> |
| error | Stringa | Contiene dati aggiuntivi come messaggi di eccezione o qualsiasi altra informazione utile per la risoluzione dei problemi. |