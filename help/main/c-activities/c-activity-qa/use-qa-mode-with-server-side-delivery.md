---
keywords: qa;lato server;anteprima;collegamenti di anteprima
description: Scopri come utilizzare Adobe [!DNL Target] URL di controllo qualità con distribuzione lato server per eseguire facilmente il controllo qualità delle attività end-to-end con collegamenti di anteprima che restano invariati, targeting del pubblico facoltativo e rapporti di controllo qualità mantenuti segmentati dai dati delle attività live.
title: Utilizzare Posso eseguire il controllo qualità delle attività con la distribuzione lato server?
feature: Activities
exl-id: eb6965be-92a6-452d-ac01-7ae1533239cc
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 70%

---

# Utilizzare il Controllo qualità delle attività con la distribuzione lato server

Utilizzare gli URL di controllo qualità con la distribuzione lato server in [!DNL Adobe Target] per eseguire in modo semplice e completo il controllo qualità delle attività, con collegamenti di anteprima che restano invariati, targeting facoltativo del pubblico e rapporti di controllo qualità mantenuti segmentati dai dati delle attività live.

L&#39;implementazione standard del Controllo qualità delle attività supporta il passaggio di parametri `qa_mode` tramite i parametri di `pageUrl`. Questo approccio è conveniente per standard/ajax [!DNL Target] chiamate. Tuttavia, per le chiamate da server a server, questo non è l&#39;approccio migliore per un caso di SDK mobile quando `pageUrl` non è disponibile.

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
| evaluateAsTrueAudienceIds | Elenco di ID | Elenco vuoto. | Elenco di ID di pubblico che devono sempre essere valutati come true nell’ambito dell’evento [!DNL Target] richiesta. |
| evaluateAsFalseAudienceIds | Elenco di ID | Elenco vuoto. | Elenco di ID di pubblico che devono sempre essere valutati come falsi nell’ambito del [!DNL Target] richiesta. |
| activityIndex | Intero | Null.<br>Non può essere vuoto. | Indice di attività nel token crittografato. Se activityIndex è al di fuori dei limiti dell&#39;attività nel token o se null, verrà ignorato. L’indice inizia con 1.<br>Regole di convalida: deve esserci almeno un indice di attività e deve fare riferimento a un&#39;attività specificata nel token. |
| experienceIndex | Intero | Null. | Quando specificato, seleziona un&#39;esperienza a seconda dell’indice nella definizione dell&#39;attività. Se non specificato o al di fuori dei limiti, rientrerà nella strategia di selezione dell&#39;esperienza dell&#39;attività. L’indice inizia con 1 Regole di convalida: può essere null o deve fare riferimento a un&#39;esperienza nell&#39;attività. |
