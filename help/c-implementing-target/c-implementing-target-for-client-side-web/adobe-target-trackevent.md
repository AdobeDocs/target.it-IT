---
keywords: adobe.target.trackEvent;trackEvent;trackevent;tracccia evento;at.js;funzioni;funzione;preventDefault;preventdefault;disattivare impostazione predefinita
description: Utilizza la funzione adobe.target.trackEvent() per la libreria JavaScript Adobe [!DNL Target] at.js per attivare una richiesta per segnalare azioni dell'utente, ad esempio clic e conversioni sul sito.
title: Come si utilizza la funzione adobe.target.trackEvent()?
feature: at.js
role: Developer
exl-id: 36005236-ce18-4845-b4fb-e52056018bc7
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 70%

---

# adobe.target.trackEvent(options)

Questa funzione genera una richiesta per segnalare le azioni dell&#39;utente, ad esempio clic e conversioni. Non recapita le attività nella risposta.

Queste chiamate mbox registrazione eventi possono essere utilizzate per definire le metriche nelle attività. Per ulteriori informazioni, consulta [Metriche di successo](/help/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) e [Tracciare le conversioni](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#task_E85D2F64FEB84201A594F2288FABF053).

Di seguito sono riportati i dettagli API:

| Chiave | Tipo | Obbligatorio | Descrizione |
|--- |--- |--- |--- |
| mbox | Stringa | Sì | Nome mbox <br>**Nota**: Se una chiamata trackEvent() viene attivata con un nome mbox già attivato sulla pagina, l’identificatore SDID di trackEvent() viene reimpostato e sarà diverso dalle chiamate Target nella pagina. Tuttavia, l’attivazione di una chiamata trackEvent() con un nome mbox diverso mantiene l’identificatore SDID della chiamata trackEvent() coerente con le chiamate Page Load Request/triggerView() sulla pagina. |
| selector | Stringa | No | Selettori CSS utilizzati per trovare gli elementi HTML. I listener di eventi verranno allegati agli elementi trovati. |
| type | Stringa | No | Rappresenta un tipo di evento registrato. Può trattarsi sia di eventi HTML noti come: click, mouseown, ecc, così come di eventi HTML personalizzati. |
| preventDefault | Booleano | No | Indica se utilizzare `event.preventDefault()` nella chiamata di ritorno del listener di eventi. Predefinito su false.<br>**Nota**: sono supportati solo `form[submit] and `a[click]”. Altri scenari non sono supportati a causa della complessità e delle enormi quantità di scenari da supportare. |
| params | Oggetto | No | Parametri mbox. Un oggetto di coppie chiave-valore che presenta la struttura seguente:<br>`{ "param1": "value1", "param2": "value2"}` |
| timeout | Numero | No | Timeout in millisecondi.<br>Se non viene specificato, viene utilizzato il valore predefinito:<br>`...timeoutInSeconds: 0.15...}` |
| success | Funzione | No | Funzione di callback utilizzata per indicare che quell’evento è stato segnalato. |
| error | Funzione | No | Funzione di callback utilizzata per indicare che non è stato possibile segnalare quell’evento. |

## Esempio

```javascript
<a href="https://asite.com">click me!</a> 
```

più codice JavaScript per assegnare `trackEvent`:

```javascript
<script> 
$('a').click(function(event){ 
  adobe.target.trackEvent({'mbox':'homePageHero'}) 
}); 
</script> 
```

Oppure:

```javascript
adobe.target.trackEvent({ 
    "mbox": "clicked-cta", 
    "params": { 
        "param1": "value1" 
    } 
});
```

>[!NOTE]
>
>Nel caso in cui i campi obbligatori non siano impostati, non viene eseguita alcuna richiesta e viene generato un errore.
