---
description: Gli URL di controllo qualità con distribuzione lato server consentono di verificare in modo facile e completo la qualità delle attività tramite collegamenti di anteprima che restano invariati, l’eventuale definizione di un pubblico di destinazione e rapporti di controllo qualità mantenuti separati dai dati delle attività live.
keywords: qa;lato server;anteprima;collegamenti di anteprima
seo-description: Gli URL di controllo qualità con distribuzione lato server consentono di verificare in modo facile e completo la qualità delle attività tramite collegamenti di anteprima che restano invariati, l’eventuale definizione di un pubblico di destinazione e rapporti di controllo qualità mantenuti separati dai dati delle attività live.
seo-title: Utilizzare il Controllo qualità delle attività con la distribuzione lato server
solution: Target
title: Utilizzare il Controllo qualità delle attività con la distribuzione lato server
topic: Advanced,Standard,Classic
uuid: c1875243-e37f-4205-9e6b-6e96cadf4a7f
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Utilizzare il Controllo qualità delle attività con la distribuzione lato server{#use-activity-qa-with-server-side-delivery}

Gli URL di controllo qualità con distribuzione lato server consentono di verificare in modo facile e completo la qualità delle attività tramite collegamenti di anteprima che restano invariati, l’eventuale definizione di un pubblico di destinazione e rapporti di controllo qualità mantenuti separati dai dati delle attività live.

L'implementazione standard del Controllo qualità delle attività supporta il passaggio di parametri `qa_mode` tramite i parametri mbox di `pageUrl`. Questo approccio è conveniente per le chiamate mbox standard/ajax. Tuttavia, per le chiamate da server a server, questo non è l'approccio migliore per un caso di SDK mobile quando `pageUrl` non è disponibile.

Nell'esempio di codice seguente viene illustrato il Controllo qualità delle attività in una chiamata lato server:

```
{
  "mbox" : "orderConfirmPage",
  "clientSideAnalyticsLogging": true,
  "clicked" : true,
  "tntId" : "12121212.17_01",
  "order" : {
    ...
  },
  "profileParameters" : {
    ...
  },
  "mboxParameters" : {
    ...
  },
  "requestLocation" : {
    ...
  },
  "qaMode" : {
    "token" : "<encrypted token string>",
    "bypassEntryAudience" : true,
    "listedActivitiesOnly" : true,
    "evaluateAsTrueAudienceIds" : [audienceId1, audienceId2...],
    "evaluateAsFalseAudienceIds" : [audienceId3, audienceId4...],
    "previewIndexes" : [
       {
         "activityIndex" : 1,
         "experienceIndex" : 1
       }
     ],
  },
  "mboxTrace" : true
}
```

Nella tabella seguente vengono illustrati i dettagli di una richiesta lato server:

| Parametro | Tipo | Valore predefinito | Descrizione |
|--- |--- |--- |--- |
| token | Token crittografato | Nessuno.<br>Non può essere vuoto. | Un'entità cifrata che contiene l'elenco degli ID delle attività che possono essere eseguite in Controllo qualità delle attività.<br>Regole di convalida: deve trattarsi di un token crittografato appartenente al client specificato nella richiesta mbox. Tutte le attività specificate nel token devono appartenere al client. |
| bypassEntryAudience | Booleano | False | Specifica se gli obiettivi dei passaggi di ingresso per le attività di controllo qualità devono essere valutati o se devono essere considerati come corrispondenti. |
| listedActivitiesOnly | Booleano | False | Specifica se le attività di controllo qualità devono essere eseguite in isolamento o se devono essere valutate come attività attive per l'ambiente corrente. |
| evaluateAsTrueAudienceIds | Elenco di ID | Elenco vuoto. | Elenco degli ID di pubblico che devono essere sempre valutati come true nell'ambito della richiesta mbox. |
| evaluateAsFalseAudienceIds | Elenco di ID | Elenco vuoto. | Elenco degli ID di pubblico che devono essere sempre valutati come false nell'ambito della richiesta mbox. |
| activityIndex | Intero | Null.<br>Non può essere vuoto. | Indice di attività nel token crittografato. Se activityIndex è al di fuori dei limiti dell'attività nel token o se null, verrà ignorato. L’indice inizia con 1.<br>Regole di convalida: deve esserci almeno un indice di attività e deve fare riferimento a un'attività specificata nel token. |
| experienceIndex | Intero | Null. | Quando specificato, seleziona un'esperienza a seconda dell’indice nella definizione dell'attività. Se non specificato o al di fuori dei limiti, rientrerà nella strategia di selezione dell'esperienza dell'attività. L’indice inizia con 1 Regole di convalida: può essere null o deve fare riferimento a un'esperienza nell'attività. |