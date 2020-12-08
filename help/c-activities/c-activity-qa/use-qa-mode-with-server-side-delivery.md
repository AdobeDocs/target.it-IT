---
keywords: qa;server side;server-side;preview;preview links
description: Utilizzate  URL di QA Adobe Target con distribuzione lato server per eseguire attività QA end-to-end in modo semplice con collegamenti di anteprima che non cambiano mai, targeting del pubblico facoltativo e reporting di QA che rimane segmentato dai dati dell'attività live.
title: Utilizzare il Controllo qualità delle attività con la distribuzione lato server
feature: qa
translation-type: tm+mt
source-git-commit: c2769c0fcf7a05c10405ec855468c829aca785c0
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 80%

---


# Utilizzare il Controllo qualità delle attività con la distribuzione lato server{#use-activity-qa-with-server-side-delivery}

Gli URL di controllo qualità con distribuzione lato server consentono di verificare in modo facile e completo la qualità delle attività tramite collegamenti di anteprima che restano invariati, l’eventuale definizione di un pubblico di destinazione e rapporti di controllo qualità mantenuti separati dai dati delle attività live.

L&#39;implementazione standard del Controllo qualità delle attività supporta il passaggio di parametri `qa_mode` tramite i parametri di `pageUrl`. This approach is convenient for standard/ajax [!DNL Target] calls. Tuttavia, per le chiamate da server a server, questo non è l&#39;approccio migliore per un caso di SDK mobile quando `pageUrl` non è disponibile.

Nell&#39;esempio di codice seguente viene illustrato il Controllo qualità delle attività in una chiamata lato server:

```json
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
| token | Token crittografato | Nessuno.<br>Non può essere vuoto. | Un&#39;entità cifrata che contiene l&#39;elenco degli ID delle attività che possono essere eseguite in Controllo qualità delle attività.<br>[!DNL Target]Regole di convalida: deve trattarsi di un token crittografato appartenente al client specificato nella richiesta Tutte le attività specificate nel token devono appartenere al client. |
| bypassEntryAudience | Booleano | False | Specifica se gli obiettivi dei passaggi di ingresso per le attività di controllo qualità devono essere valutati o se devono essere considerati come corrispondenti. |
| listedActivitiesOnly | Booleano | False | Specifica se le attività di controllo qualità devono essere eseguite in isolamento o se devono essere valutate come attività attive per l&#39;ambiente corrente. |
| evaluateAsTrueAudienceIds | Elenco di ID | Elenco vuoto. | List of audience IDs that should always be evaluated as true in the scope of the [!DNL Target] request. |
| evaluateAsFalseAudienceIds | Elenco di ID | Elenco vuoto. | List of audience IDs that should always be evaluated as false in the scope of the [!DNL Target] request. |
| activityIndex | Intero | Null.<br>Non può essere vuoto. | Indice di attività nel token crittografato. Se activityIndex è al di fuori dei limiti dell&#39;attività nel token o se null, verrà ignorato. L’indice inizia con 1.<br>Regole di convalida: deve esserci almeno un indice di attività e deve fare riferimento a un&#39;attività specificata nel token. |
| experienceIndex | Intero | Null. | Quando specificato, seleziona un&#39;esperienza a seconda dell’indice nella definizione dell&#39;attività. Se non specificato o al di fuori dei limiti, rientrerà nella strategia di selezione dell&#39;esperienza dell&#39;attività. L’indice inizia con 1 Regole di convalida: può essere null o deve fare riferimento a un&#39;esperienza nell&#39;attività. |