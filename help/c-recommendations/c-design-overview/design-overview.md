---
description: Informazioni generali sulle progettazioni che definiscono come verranno visualizzati i consigli su una pagina.
keywords: progettazione di consigli;modello;creare progettazione;consegna;output
seo-description: Informazioni generali sulle progettazioni che definiscono come verranno visualizzati i consigli su una pagina.
seo-title: Panoramica della progettazione
solution: Target
title: Panoramica della progettazione
topic: Premium
uuid: 82cc6a19-bfde-47b3-92b9-b862be70dd87
translation-type: tm+mt
source-git-commit: 3901aa72118adbc0862915da7c8b211090a4e7e7

---


# Panoramica della progettazione{#design-overview}

Informazioni generali sulle progettazioni che definiscono come verranno visualizzati i consigli su una pagina.

Target può fornire una visuale completa dei consigli, come illustrato nella figura seguente. La progettazione può includere HTML, JavaScript e CSS.

![](assets/velocity_example.png)

Target può anche inviare i consigli come oggetti JSON che possono essere utilizzati in messaggi di posta elettronica, dispositivi IoT (Internet of Things), console o i casi di utilizzo vocale (Amazon Alexa o Google Home).

## Esempio JSON {#section_75BFB2537CFF4FBD9B560F59EB32C8DD}

Nell&#39;esempio seguente viene illustrato come è possibile restituire risposte JSON quando si configura un&#39;attività tramite l&#39;editor basato su modelli.

1. Crea una progettazione dall&#39;interno della Libreria di progettazione o all&#39;interno del flusso di lavoro basato su modelli. Se tenti di eseguire questa operazione all’interno del flusso di lavoro Compositore esperienza visivo, non puoi creare elementi diversi da una struttura HTML, che viene racchiusa in un `<div>` a scopo di monitoraggio dei clic.
1. Assicurati che l&#39;opzione “Progettazione HTML” sia disattivata:

   ![](assets/html_design_toggle.png)

1. Il codice riportato di seguito è un esempio di ciò che è possibile incollare nella progettazione:

   ```
       #* 
       * "Return a simple list of recommended entity ids"   
       *#
   
       {   
         "notes":{   
         "purpose": "Return a simple list of recommended entity ids",   
         "use-case": "Use this approach if you prefer to do a real-time lookup of entity attribute details (such as inventory, price, rating) from another system (such as a CMS, PIM or ecommerce platform)",   
         "version": "01"   
         },   
         "recommendedItems": {   
           "key": "$key.id",   
           "slot-01": "$entity1.id",   
           "slot-02": "$entity2.id",   
           "slot-03": "$entity3.id",   
           "slot-04": "$entity4.id",   
           "slot-05": "$entity5.id",   
           "slot-06": "$entity6.id",   
           "slot-07": "$entity7.id",   
           "slot-08": "$entity8.id",   
           "slot-09": "$entity9.id",   
           "slot-10": "$entity10.id"   
         }   
       }  
   ```

1. Imposta un&#39;attività di Consigli basata su moduli che utilizzi questa progettazione.

   1. Passa alla pagina Attività.
   1. Fai clic su **[!UICONTROL Crea attività]**.
   1. Seleziona **[!UICONTROL Consigli]**.
   1. In **[!UICONTROL Scegli Compositore esperienza]**, seleziona **[!UICONTROL Modulo]**.

   1. In posizione, immetti il testo: “Sample_Recs_Response”
   1. In **[!UICONTROL Contenuto predefinito]** fai clic sulla freccia giù, poi su **[!UICONTROL Aggiungi consiglio]**.
   1. Scegli un Tipo di pagina. Questo determina il filtraggio iniziale della schermata successiva.
   1. Seleziona una scheda Criteri, poi fai clic su **[!UICONTROL Avanti]**.
   1. Seleziona la struttura creata nel passaggio precedente, poi fai clic su **[!UICONTROL Salva]**.
   1. Completa il processo di impostazione.
   1. Fai clic sulla freccia destra accanto a **[!UICONTROL Inattivo]**, poi seleziona **[!UICONTROL Attiva]**.

1. Dopo aver impostato e attivato l&#39;attività, è possibile impostare una richiesta di esempio per ottenere la risposta JSON pulita.

   Dal momento in cui salvi l&#39;attività, Target dovrà generare un modello per supportare la configurazione dei criteri selezionati. A seconda di una serie di fattori, questo potrebbe richiedere del tempo. Una volta generato il modello vengono visualizzati i risultati.

   Ad esempio:

   ```
   https://[YOUR_CLIENT_CODE].tt.omtrdc.net/m2/YOUR_CLIENT_CODE/ubox/raw?mbox=[YOUR_MBOX_NAME]&mboxContentType=text/html&mboxXDomain=disabled&entity.id=[ENTITY_ID]&mboxHost=rawbox_sample&at_property=[AT_PROPERTY_TOKEN]&mboxNoRedirect=true&mboxPC=1234-4321&mboxSession=9876-7000
   ```

   dove

| Parametro | Valore |
|--- |--- |
| `[YOUR_CLIENT_CODE]` | Codice client Target (disponibile in ../target/products.html # recssettings &gt; Token API di Recommendations &gt; Codice client. |
| `[YOUR_MBOX_NAME]` | Il nome selezionato nella sezione “Posizioni” dei consigli basati su moduli, in questo caso YOUR_CLIENT_CODE. |
| `[ENTITY_ID`] | L&#39;`entity.id` di un elemento nel catalogo. |
| `[AT_PROPERTY_TOKEN]` | (Facoltativo) Aggiungi se hai selezionato una Proprietà (parte delle autorizzazioni dell&#39;azienda) durante l&#39;impostazione dell&#39;attività. |

Dopo che l&#39;algoritmo è stato eseguito e si dispone dei risultati, la risposta dovrebbe essere simile a questa:

![](assets/json_recommendation.png){width=“575px”}

## Ulteriori suggerimenti sugli oggetti JSON {#section_C305673C68944749969DB239E3221DC2}

È inoltre possibile inviare un semplice elenco di elementi delimitato da virgole impostando una progettazione con la seguente sintassi:

```
entity1.id, $entity2.id, $entity3.id, $entity4.id, $entity5.id, 
```

In alternativa, è possibile inviare ulteriori informazioni nella risposta. Il file di codice seguente è un esempio più complesso che restituisce molto di più degli ID di entità con gli spazi associati (ordine). In questo esempio di progettazione vengono inoltre restituiti i dettagli dell&#39;attività, del Profilo di Target (come applicabile) e altri attributi `entity.attributes` associati agli elementi restituiti.

```
    {   
     "adobeRecommendations": {   
      "notes": {   
       "purpose": "Return a list of entity ids with their associated entity.attributes",   
       "use-case": "Use this approach to avoid looking up attribute details after receiving a response from Target",   
       "version": "01"   
      },   
      "recommendedItems": {   
       "slot-01": "$entity1.id",   
       "slot-02": "$entity2.id",   
       "slot-03": "$entity3.id",   
       "slot-04": "$entity4.id",   
       "slot-05": "$entity5.id",   
       "slot-06": "$entity6.id",   
       "slot-07": "$entity7.id",   
       "slot-08": "$entity8.id",   
       "slot-09": "$entity9.id",   
       "slot-10": "$entity10.id"   
      },   
      "activityDetails": {   
       "mbox.name": "email-mbox",   
       "campaign.name": "\${campaign.name}",   
       "campaign.id": "\${campaign.id}",   
       "campaign.recipe.name": "\${campaign.recipe.name}",   
       "campaign.recipe.id": "\${campaign.recipe.id}",   
       "offer.name": "\${offer.name}",   
       "offer.id": "\${offer.id}",   
       "criteria.title": "$criteria.title",   
       "algorithm.name": "$algorithm.name",   
       "algorithm.dayCount": "$algorithm.dayCount"   
      },   
      "visitorProfile": {   
       "profile.favorite-category": "\${profile.favorite-category}",   
       "profile.test": "\${profile.test}",   
       "user.endpoint.lastPurchasedEntity": "\${user.endpoint.lastPurchasedEntity}",   
       "user.endpoint.lastViewedEntity": "\${user.endpoint.lastViewedEntity}",   
       "user.endpoint.mostViewedEntity": "\${user.endpoint.mostViewedEntity}",   
       "user.endpoint.categoryAffinity": "\${user.endpoint.categoryAffinity}",   
       "profile.geolocation.city": "\${profile.geolocation.city}",   
       "profile.geolocation.dma": "\${profile.geolocation.dma}",   
       "profile.geolocation.state": "\${profile.geolocation.state}",   
       "profile.geolocation.country": "\${profile.geolocation.country}",   
       "profile.sessionCount": "\${profile.sessionCount}",   
       "profile.averageDaysBetweenVisits": "\${profile.averageDaysBetweenVisits}",   
       "profile.browserTime": "\${profile.browserTime}",   
       "user.activeActivities": "\${user.activeActivities}",   
       "user.pcId": "\${user.pcId}",   
       "user.isFirstSession": "\${user.isFirstSession}",   
       "user.isNewSession": "\${user.isNewSession}",   
       "user.header": "\${user.header}",   
       "user.parameter": "\${user.parameter}"   
      },   
      "recKey": {   
       "recKeyDetails": {   
        "id": "$key.id",   
        "name": "$key.name",   
        "category": "$key.category",   
        "pageUrl": "$key.pageUrl",   
        "thumbnailUrl": "$key.thumbnailUrl"   
       }   
      },   
      "recDetailedResults": {   
       "recEntity1Details": {   
        "id": "$entity1.id",   
        "name": "$entity1.name",   
        "category": "$entity1.category",   
        "pageUrl": "$entity1.pageUrl",   
        "thumbnailUrl": "$entity1.thumbnailUrl"   
       },   
       "recEntity2Details": {   
        "id": "$entity2.id",   
        "name": "$entity2.name",   
        "category": "$entity2.category",   
        "pageUrl": "$entity2.pageUrl",   
        "thumbnailUrl": "$entity2.thumbnailUrl"   
       },   
       "recEntity3Details": {   
        "id": "$entity3.id",   
        "name": "$entity3.name",   
        "category": "$entity3.category",   
        "pageUrl": "$entity3.pageUrl",   
        "thumbnailUrl": "$entity3.thumbnailUrl"   
       },   
       "recEntity4Details": {   
        "id": "$entity4.id",   
        "name": "$entity4.name",   
        "category": "$entity4.category",   
        "pageUrl": "$entity4.pageUrl",   
        "thumbnailUrl": "$entity4.thumbnailUrl"   
       },   
       "recEntity5Details": {   
        "id": "$entity5.id",   
        "name": "$entity5.name",   
        "category": "$entity5.category",   
        "pageUrl": "$entity5.pageUrl",   
        "thumbnailUrl": "$entity5.thumbnailUrl"   
       },   
       "recEntity6Details": {   
        "id": "$entity6.id",   
        "name": "$entity6.name",   
        "category": "$entity6.category",   
        "pageUrl": "$entity6.pageUrl",   
        "thumbnailUrl": "$entity6.thumbnailUrl"   
       },   
       "recEntity7Details": {   
        "id": "$entity7.id",   
        "name": "$entity7.name",   
        "category": "$entity7.category",   
        "pageUrl": "$entity7.pageUrl",   
        "thumbnailUrl": "$entity7.thumbnailUrl"   
       },   
       "recEntity8Details": {   
        "id": "$entity8.id",   
        "name": "$entity8.name",   
        "category": "$entity8.category",   
        "pageUrl": "$entity8.pageUrl",   
        "thumbnailUrl": "$entity8.thumbnailUrl"   
       },   
       "recEntity9Details": {   
        "id": "$entity9.id",   
        "name": "$entity9.name",   
        "category": "$entity9.category",   
        "pageUrl": "$entity9.pageUrl",   
        "thumbnailUrl": "$entity9.thumbnailUrl"   
       },   
       "recEntity10Details": {   
        "id": "$entity10.id",   
        "name": "$entity10.name",   
        "category": "$entity10.category",   
        "pageUrl": "$entity10.pageUrl",   
        "thumbnailUrl": "$entity10.thumbnailUrl"   
       }   
      }   
     }   
    }  
```

