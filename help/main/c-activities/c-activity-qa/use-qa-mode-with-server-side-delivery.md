---
keywords: qa;lato server;anteprima;collegamenti di anteprima
description: Scopri come utilizzare gli URL di controllo qualità di Adobe [!DNL Target] con distribuzione lato server per eseguire in modo semplice e completo il controllo qualità delle attività con collegamenti di anteprima che restano invariati, targeting facoltativo del pubblico e rapporti di controllo qualità mantenuti segmentati dai dati delle attività live.
title: Utilizzare Posso eseguire il controllo qualità delle attività con la distribuzione lato server?
feature: Activities
exl-id: eb6965be-92a6-452d-ac01-7ae1533239cc
TQID: https://experienceleague.adobe.com/zZJmFqpXtAigTiEWMZhRqXBJqvG3ANLussSPE3-NoDA
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 408
ht-degree: 47%

---

# Utilizzare il Controllo qualità delle attività con la distribuzione lato server

Utilizza gli URL di controllo qualità con distribuzione lato server in [!DNL Adobe Target] per eseguire facilmente il controllo qualità delle attività end-to-end con collegamenti di anteprima che non cambiano mai, targeting facoltativo del pubblico e rapporti di controllo qualità mantenuti segmentati dai dati delle attività live.

L&#39;implementazione standard del Controllo qualità delle attività supporta il passaggio di `qa_mode` parametri tramite `pageUrl` parametri. Questo approccio è conveniente per le chiamate standard/AJAX [!DNL Target]. Tuttavia, per le chiamate da server a server, questo non è l&#39;approccio migliore per un caso di SDK mobile quando `pageUrl` non è disponibile.

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
| token | Token crittografato | Nessuno.<br>Non può essere vuoto. | Un&#39;entità crittografata contenente l&#39;elenco degli ID attività che possono essere eseguiti nel Controllo qualità attività.<br>Regole di convalida: deve essere un token crittografato appartenente al client specificato nella richiesta [!DNL Target]. Tutte le attività specificate nel token devono appartenere al client. |
| bypassEntryAudience | Booleano | False | Specifica se gli obiettivi dei passaggi di ingresso per le attività di controllo qualità devono essere valutati o se devono essere considerati come corrispondenti. |
| listedActivitiesOnly | Booleano | False | Specifica se le attività di controllo qualità devono essere eseguite in isolamento o se devono essere valutate come attività attive per l&#39;ambiente corrente. |
| evaluateAsTrueAudienceIds | Elenco di ID | Elenco vuoto. | Elenco di ID di pubblico che devono sempre essere valutati come true nell&#39;ambito della richiesta [!DNL Target]. |
| evaluateAsFalseAudienceIds | Elenco di ID | Elenco vuoto. | Elenco di ID di pubblico che devono sempre essere valutati come falsi nell&#39;ambito della richiesta [!DNL Target]. |
| activityIndex | Intero | Null.<br>Non può essere vuoto. | Indice di attività nel token crittografato. Se activityIndex è al di fuori dei limiti dell&#39;attività nel token o se null, verrà ignorato. L&#39;indice inizia con 1.<br>Regole di convalida: deve essere almeno un indice di attività e deve fare riferimento a un&#39;attività specificata nel token. |
| experienceIndex | Intero | Null. | Quando specificato, seleziona un&#39;esperienza a seconda dell’indice nella definizione dell&#39;attività. Se non specificato o al di fuori dei limiti, rientrerà nella strategia di selezione dell&#39;esperienza dell&#39;attività. L’indice inizia con 1 regole di convalida: può essere nullo o deve fare riferimento a un’esperienza nell’attività. |
