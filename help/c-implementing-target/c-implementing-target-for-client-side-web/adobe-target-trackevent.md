---
description: 'Informazioni sulla funzione adobe.target.trackEvent(options) per at.js. '
keywords: adobe.target.notification;element;selector;notification;extension
seo-description: Informazioni sulla funzione adobe.target.trackEvent(options) per la libreria at.js JavaScript di Adobe Target.
seo-title: Informazioni sulla funzione adobe.target.trackEvent(options) per la libreria at.js JavaScript di Adobe Target.
solution: Target
subtopic: Introduzione
title: adobe.target.trackEvent(options)
topic: Standard
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# adobe.target.trackEvent(options)

Questa funzione genera una richiesta per segnalare le azioni dell&#39;utente, ad esempio clic e conversioni. Non recapita le attività nella risposta.

Queste chiamate mbox registrazione eventi possono essere utilizzate per definire le metriche nelle attività. Per ulteriori informazioni, consulta [Metriche di successo](../../c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) e [Tracciare le conversioni](../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#task_E85D2F64FEB84201A594F2288FABF053).

Di seguito sono riportati i dettagli API:

| Chiave | Tipo | Obbligatorio | Descrizione |
|--- |--- |--- |--- |
| mbox | Stringa | Sì | Nome Mbox |
| selector | Stringa | No | Selettori CSS utilizzati per trovare gli elementi HTML. I listener di eventi verranno allegati agli elementi trovati. |
| type | Stringa | No | Rappresenta un tipo di evento registrato. Può trattarsi sia di eventi HTML noti come: click, mouseown, ecc, così come di eventi HTML personalizzati. |
| preventDefault | Booleano | No | Indica se utilizzare `event.preventDefault()` nella chiamata di ritorno del listener di eventi. Predefinito su false.<br>**Nota**: sono supportati solo `form[submit] and `a[click]”. Altri scenari non sono supportati a causa della complessità e delle enormi quantità di scenari da supportare. |
| params | Oggetto | No | Parametri mbox. Un oggetto di coppie chiave-valore che presenta la struttura seguente:<br>`{ "param1": "value1", "param2": "value2"}` |
| timeout | Numero | No | Timeout in millisecondi.<br>Se non viene specificato, viene utilizzato il valore predefinito:<br>`...timeoutInSeconds: 0.15...}` |
| success | Funzione | No | Funzione di callback utilizzata per indicare che quell’evento è stato segnalato. |
| error | Funzione | No | Funzione di callback utilizzata per indicare che non è stato possibile segnalare quell’evento. |

## Esempio

```
<a href="https://asite.com">click me!</a> 
```

più codice JavaScript per assegnare `trackEvent`:

```
<script> 
$('a').click(function(event){ 
  adobe.target.trackEvent({'mbox':'homePageHero'}) 
}); 
</script> 
```

Oppure:

```
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