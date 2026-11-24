---
keywords: Progettazione consigli;creare progettazione;copia progettazione
description: Scopri come creare una progettazione di [!DNL Target Recommendations] utilizzando una progettazione predefinita o creando una progettazione personalizzata che si adatti al meglio al layout di una pagina.
title: Creare una progettazione
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: 0f10ee9d-7210-4e02-9342-e4f85cf46e8c
TQID: 'https://experienceleague.adobe.com/GLWcKaQGl6TmL9i7LYUiYepg6SkAjBtL-78-zlaWCTk'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: d5030abcda38bbc6d33b88ce3bb5d64f69e4e492
workflow-type: tm+mt
source-wordcount: '912'
ht-degree: 11%
---
# Creare una progettazione {#create-design}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come creare, modificare, copiare ed eliminare le progettazioni in [!DNL Adobe Target Recommendations] e come restituire i consigli come JSON.

>[!ENDSHADEBOX]

Una progettazione definisce come i consigli verranno visualizzati su una pagina. Una progettazione può essere basata su una progettazione predefinita o creata come progettazione personalizzata. Nella schermata **[!UICONTROL Recommendations]** > **[!UICONTROL Designs]** vengono visualizzate le schede di progettazione predefinite e le progettazioni create nell&#39;account.

* Impossibile modificare o eliminare una progettazione predefinita.
* Una progettazione personalizzata può essere modificata, copiata o eliminata.
* Per creare una progettazione basata su una progettazione predefinita, copiate innanzitutto la progettazione, quindi modificate la copia.

È possibile creare una progettazione durante il processo di creazione delle attività dall&#39;interno del **[!UICONTROL Compositore esperienza visivo]** o dalla libreria di progettazione all&#39;esterno della creazione delle attività. I passaggi seguenti presuppongono che la progettazione venga creata dalla libreria, ma sono simili.

## Creare una progettazione dalla libreria {#steps}

1. Fai clic su **[!UICONTROL Consigli]** > **[!UICONTROL Progettazioni]** per visualizzare la libreria **[!UICONTROL Progettazioni]**.

1. Iniziare la progettazione in uno dei modi seguenti:

   * Per basare la progettazione su una progettazione predefinita o su una progettazione esistente, fai clic sull&#39;icona Altre azioni ( ![Icona Altre azioni](/help/main/assets/icons/MoreSmallList.svg) ) per la progettazione, quindi fai clic su **[!UICONTROL Copia]**. Viene visualizzata la finestra di dialogo **[!UICONTROL Crea design]**. La copia modificata diventa una nuova progettazione personalizzata.
   * Per creare una progettazione personalizzata da zero, fare clic su **[!UICONTROL Crea progettazione]**.

     ![Libreria progettazioni con il pulsante Crea progettazione evidenziato](../assets/design_1.png)

1. Digita un **[!UICONTROL Nome]** e seleziona un&#39;immagine di anteprima opzionale da visualizzare sulla scheda di progettazione.

   Quando si utilizza una progettazione predefinita, nel campo **[!UICONTROL Nome contenuto]** viene visualizzato il nome della progettazione seguito da &quot;Copia&quot;. Il nome può essere modificato.

1. (Condizionale) Modificare la struttura **[!UICONTROL Codice]** come desiderato.

   Le progettazioni per consigli utilizzano il linguaggio di progettazione open-source Velocity. Per informazioni su Velocity, vedere [https://velocity.apache.org](https://velocity.apache.org) e [Personalizzare una progettazione utilizzando Velocity](/help/main/c-recommendations/c-design-overview/customizing-a-template.md).

   Una progettazione può essere HTML o non HTML. Per impostazione predefinita, le progettazioni di HTML sono racchiuse con un tag `<div>` per consentire il tracciamento dei clic in un ambiente Web. Le progettazioni non HTML sono per ambienti non web in cui non è possibile effettuare il monitoraggio dei clic. Far scorrere l&#39;interruttore **[!UICONTROL HTML Design]** in posizione &quot;off&quot; per utilizzare codice non HTML.

   >[!NOTE]
   >
   >Il numero massimo di entità a cui è possibile fare riferimento in una progettazione, tramite codifica fissa o cicli, è 99.

1. Fai clic su **[!UICONTROL Crea]**.

1. Fai clic sull&#39;icona Altre azioni ( ![Icona Altre azioni](/help/main/assets/icons/MoreSmallList.svg) ) per la progettazione da modificare, copiare o eliminare, quindi fai clic sull&#39;opzione appropriata: **[!UICONTROL Modifica]**, **[!UICONTROL Copia]** o **[!UICONTROL Elimina]**.

   ![Progetta la libreria con il menu Altre azioni aperto, che mostra Modifica, Copia ed Elimina](../assets/design_2.png)

I design sono disponibili a livello dell&#39;intero account. L’utilizzo tra account diversi deve essere considerato prima che la progettazione venga eliminata. Non è possibile recuperare le progettazioni eliminate.

## Esempio JSON {#json-example}

L&#39;esempio seguente mostra come è possibile restituire le risposte JSON quando un&#39;attività è configurata con l&#39;[editor basato su moduli](/help/main/c-experiences/form-experience-composer.md).

1. Crea una progettazione dall&#39;interno della **[!UICONTROL Libreria di progettazione]** o all&#39;interno del flusso di lavoro basato su moduli. Una progettazione creata all&#39;interno del flusso di lavoro **[!UICONTROL Compositore esperienza visivo]** può essere solo una progettazione HTML, racchiusa in `<div>` a scopo di tracciamento dei clic.

1. Verificare che l&#39;opzione **[!UICONTROL HTML Design]** sia disattivata:

   ![Disattiva progettazione HTML](/help/main/c-recommendations/c-design-overview/assets/html_design_toggle.png)

1. Incolla nella progettazione codice come il seguente esempio:

   +++ Codice di progettazione di esempio che restituisce un elenco di ID entità

   ```javascript
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

   +++

1. Configurare un&#39;attività [!DNL Recommendations] basata su modulo che utilizza questa struttura.

   +++ Scopri come impostare un&#39;attività [!DNL Recommendations] basata su moduli 

   1. Passa alla pagina **[!UICONTROL Attività]**.
   1. Fai clic su **[!UICONTROL Crea attività]** > **[!UICONTROL Consigli]**.
   1. In **[!UICONTROL Scegli Compositore esperienza]**, seleziona **[!UICONTROL Modulo]**, quindi fai clic su **[!UICONTROL Successivo]**.
   1. Nella casella di gruppo Posizione immettere il testo &quot;Sample_Recs_Response&quot;.
   1. In **[!UICONTROL Contenuto predefinito]** fai clic sulla freccia giù, poi su **[!UICONTROL Aggiungi consiglio]**.
   1. Scegli un Tipo di pagina. Questo determina il filtraggio iniziale della schermata successiva.
   1. Seleziona una scheda Criteri, poi fai clic su **[!UICONTROL Avanti]**.
   1. Seleziona la struttura creata nel passaggio precedente, quindi fai clic su **[!UICONTROL Successivo]**.
   1. Completa il processo di impostazione.
   1. Fai clic sulla freccia destra accanto a **[!UICONTROL Inattivo]**, poi seleziona **[!UICONTROL Attiva]**.

   +++

1. Dopo che l’attività è stata configurata e attivata, è possibile impostare una richiesta di esempio per recuperare la risposta JSON pulita.

   Dal momento in cui l&#39;attività viene salvata, [!DNL Target] deve generare un modello per supportare la configurazione dei criteri selezionati. A seconda di una serie di fattori, questo processo potrebbe richiedere del tempo. I risultati vengono visualizzati dopo la generazione del modello.

   Ad esempio:

   ```
   https://[YOUR_CLIENT_CODE].tt.omtrdc.net/m2/YOUR_CLIENT_CODE/ubox/raw?mbox=[YOUR_MBOX_NAME]&mboxContentType=text/html&mboxXDomain=disabled&entity.id=[ENTITY_ID]&mboxHost=rawbox_sample&at_property=[AT_PROPERTY_TOKEN]&mboxNoRedirect=true&mboxPC=1234-4321&mboxSession=9876-7000
   ```

   dove

   | Parametro | Valore |
   |--- |--- |
   | `[YOUR_CLIENT_CODE]` | Il codice client [!DNL Target] (disponibile in /help/target/products.html#recsSettings > Token API per i consigli > Codice client). |
   | `[YOUR_MBOX_NAME]` | Il nome selezionato nella sezione &quot;locations&quot; dell’attività Consigli basata su moduli, in questo caso Sample_Recs_Response. |
   | `[ENTITY_ID]` | `entity.id` di un elemento nel catalogo. |
   | `[AT_PROPERTY_TOKEN]` | (Facoltativo) Aggiunto quando una Proprietà (parte di Autorizzazioni Enterprise) veniva selezionata durante l’impostazione dell’attività. |

Dopo l’esecuzione dell’algoritmo e la disponibilità dei risultati, la risposta sarà simile alla seguente:

![Risposta JSON con gli elementi consigliati](/help/main/c-recommendations/c-design-overview/assets/json_recommendation.png){width="575px"}

## Ulteriori suggerimenti sugli oggetti JSON {#json-tips}

È inoltre possibile restituire un semplice elenco di elementi delimitato da virgole impostando una progettazione con la seguente sintassi:

```
$entity1.id, $entity2.id, $entity3.id, $entity4.id, $entity5.id, 
```

Ulteriori informazioni possono essere inviate anche nella risposta. Il codice seguente è un esempio più complesso che restituisce molto di più degli ID entità con gli slot associati (ordine). In questo esempio di progettazione vengono inoltre restituiti i dettagli dell&#39;attività, **[!UICONTROL Profilo di destinazione]** (come applicabile) e altri `entity.attributes` associati agli elementi restituiti.

+++ Codice di progettazione di esempio che restituisce i dettagli di attività, profilo ed entità

```javascript
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

+++

