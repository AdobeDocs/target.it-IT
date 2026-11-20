---
keywords: qa;lato server;anteprima;collegamenti di anteprima
description: Scopri come utilizzare gli URL di controllo qualità di Adobe [!DNL Target] con distribuzione lato server per eseguire in modo semplice il controllo qualità delle attività end-to-end con collegamenti di anteprima che restano invariati, targeting facoltativo del pubblico e rapporti di controllo qualità mantenuti segmentati dai dati delle attività live.
title: Utilizzare Posso eseguire il controllo qualità delle attività con la distribuzione lato server?
feature: Activities
exl-id: eb6965be-92a6-452d-ac01-7ae1533239cc
TQID: 'https://experienceleague.adobe.com/zZJmFqpXtAigTiEWMZhRqXBJqvG3ANLussSPE3-NoDA'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: 6efa6b7a-8062-5c41-aef4-b4853cc306ae
    internal-label: Activities
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 0a683f6e68bb7481b9e45c91a275a46b84a1ffd8
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 18%
---
# Utilizzare il Controllo qualità delle attività con la distribuzione lato server {#qa-server-side}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come passare i parametri di controllo qualità delle attività in una chiamata [!DNL Adobe Target] lato server, in modo da poter testare le attività quando `pageUrl` non è disponibile.

>[!ENDSHADEBOX]

L&#39;implementazione standard del Controllo qualità delle attività supporta il passaggio di `qa_mode` parametri tramite `pageUrl` parametri. Questo approccio è conveniente per le chiamate standard/AJAX [!DNL Target]. Tuttavia, non è adatto per chiamate server-to-server, come l&#39;implementazione di Mobile SDK, dove `pageUrl` non è disponibile. In questi casi, passa i parametri di controllo qualità nella richiesta stessa, che mantiene gli stessi collegamenti di anteprima, il targeting facoltativo del pubblico e il reporting di controllo qualità segmentati dai dati delle attività live.

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

La tabella seguente descrive i parametri di una richiesta lato server:

| Parametro | Tipo | Valore predefinito | Descrizione |
|--- |--- |--- |--- |
| token | Token crittografato | Nessuno. Non può essere vuoto. | Un&#39;entità crittografata contenente l&#39;elenco degli ID attività che possono essere eseguiti nel Controllo qualità attività.<br>Regole di convalida: il token deve essere un token crittografato appartenente al client specificato nella richiesta [!DNL Target]. Tutte le attività specificate nel token devono appartenere al client. |
| bypassEntryAudience | Booleano | False | Specifica se i target dei passaggi di ingresso per le attività di controllo qualità vengono valutati o considerati corrispondenti. |
| listedActivitiesOnly | Booleano | False | Specifica se le attività di controllo qualità vengono eseguite in isolamento o vengono valutate come attività attive per l’ambiente corrente. |
| evaluateAsTrueAudienceIds | Elenco di ID | Elenco vuoto | Elenco di ID di pubblico sempre valutati come true nell&#39;ambito della richiesta [!DNL Target]. |
| evaluateAsFalseAudienceIds | Elenco di ID | Elenco vuoto | Elenco di ID di pubblico che vengono sempre valutati come falsi nell&#39;ambito della richiesta [!DNL Target]. |
| activityIndex | Intero | Null. Non può essere vuoto. | Indice di attività nel token crittografato. Se `activityIndex` è null o esce dai limiti delle attività nel token, viene ignorato. L&#39;indice inizia con 1.<br>Regole di convalida: è necessario almeno un indice di attività e deve fare riferimento a un&#39;attività specificata nel token. |
| experienceIndex | Intero | Null | Quando specificato, seleziona un&#39;esperienza a seconda dell’indice nella definizione dell&#39;attività. Se non è specificato o è al di fuori dei limiti, viene applicata la strategia del selettore di esperienza dell’attività. L&#39;indice inizia con 1.<br>Regole di convalida: il valore può essere null o deve fare riferimento a un&#39;esperienza nell&#39;attività. |
