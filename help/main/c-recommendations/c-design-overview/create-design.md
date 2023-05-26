---
keywords: Progettazione consigli;creare progettazione;copia progettazione
description: Scopri come creare un Adobe [!DNL Target] Progettazione Recommendations utilizzando una progettazione predefinita o creando una progettazione personalizzata che si adatti al meglio al layout della pagina.
title: Come si crea una progettazione in Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: 0f10ee9d-7210-4e02-9342-e4f85cf46e8c
source-git-commit: bde5506033fbca1577fad1cda1af203702fc4bb3
workflow-type: tm+mt
source-wordcount: '1026'
ht-degree: 35%

---

# Creare una progettazione

Una progettazione definisce come i consigli verranno visualizzati su una pagina.

È possibile creare una progettazione [!UICONTROL Consigli] utilizzando una progettazione predefinita o creandone una personalizzata. Il **[!UICONTROL Recommendations > Progettazioni]** nella schermata vengono visualizzate le schede di progettazione predefinite e le progettazioni create nel tuo account.

Quando si lavora con le progettazioni, tenere presenti le seguenti informazioni:

* Puoi creare una progettazione di consigli utilizzando una progettazione predefinita oppure puoi creare una progettazione personalizzata.
* Non è possibile modificare o eliminare una progettazione predefinita.
* Puoi modificare, copiare o eliminare una progettazione personalizzata.
* Per creare una progettazione basata su una progettazione predefinita, è necessario innanzitutto copiare la progettazione e quindi modificare la copia.

Questa illustrazione mostra la progettazione predefinita 1 x 4:

![Design predefinito 1 x 4](/help/main/c-recommendations/c-design-overview/assets/default-design.png)

Questa illustrazione mostra una progettazione personalizzata:

![Progettazione personalizzata](/help/main/c-recommendations/c-design-overview/assets/custom-design.png)

Puoi creare una progettazione durante il processo di creazione delle attività dall’interno del Compositore esperienza visivo o dalla libreria di progettazione al di fuori della creazione delle attività. Le sezioni seguenti presuppongono la creazione di progetti dalla libreria, ma i passaggi sono simili.

## Creare progettazioni

È possibile creare una progettazione basata su una progettazione predefinita oppure una progettazione personalizzata.

### Creare una progettazione basata su una progettazione predefinita

1. Clic **[!UICONTROL Recommendations]** > **[!UICONTROL Progettazioni]** per visualizzare [!UICONTROL Progettazioni] libreria.

   ![Libreria progettazioni](/help/main/c-recommendations/c-design-overview/assets/design-library.png)

1. Passa il puntatore del mouse sulla scheda della progettazione che desideri creare, quindi fai clic su **[!UICONTROL Copia]** icona.

   ![Immagine Card_CopyDesign](assets/Card_CopyDesign.png)

   Il [!UICONTROL Crea design] viene visualizzata.

   ![immagine createDesign](assets/createDesign.png)

1. In **[!UICONTROL Informazioni]** , aggiungi un **[!UICONTROL Nome contenuto]** e l&#39;immagine di anteprima opzionale da visualizzare sulla scheda di progettazione.

   Quando si utilizza una progettazione predefinita, il nome della progettazione e la &quot;copia&quot; vengono visualizzati nel **[!UICONTROL Nome contenuto]** campo. È possibile modificare il nome. È inoltre possibile selezionare un&#39;immagine da visualizzare nella scheda di progettazione.

1. (Condizionale) Modifica la progettazione **[!UICONTROL Codice]**, come desiderato.

   Le progettazioni per consigli utilizzano il linguaggio di progettazione open-source Velocity. Le informazioni su Velocity sono disponibili all’indirizzo [https://velocity.apache.org](https://velocity.apache.org) e in [Personalizzare una progettazione con Velocity](/help/main/c-recommendations/c-design-overview/customizing-a-template.md).

   Una progettazione può essere HTML o non HTML. Per impostazione predefinita, le progettazioni HTML sono racchiuse da un tag `<div>` per consentire il tracciamento dei clic in un ambiente web. Le progettazioni non HTML sono per ambienti non web in cui non è possibile effettuare il monitoraggio dei clic. Scorri il [!UICONTROL Progettazione HTML] passa alla posizione &quot;off&quot; per utilizzare codice non HTML.

   >[!NOTE]
   >
   >Il numero massimo di entità a cui puoi fare riferimento in una progettazione, tramite codifica fissa o cicli, è 99.

1. Fai clic su **[!UICONTROL Salva]**.

### Creare una progettazione personalizzata

1. Clic **[!UICONTROL Recommendations]** > **[!UICONTROL Progettazioni]** per visualizzare [!UICONTROL Progettazioni] libreria.

1. Clic **[!UICONTROL Crea design]**.

   Se desideri basare la nuova progettazione personalizzata su una progettazione esistente, passa il puntatore del mouse sulla progettazione desiderata, quindi fai clic su [!UICONTROL Copia] icona. Puoi quindi modificare la copia per creare una nuova progettazione personalizzata.

1. Aggiungi un **[!UICONTROL Nome contenuto]** e l&#39;immagine di anteprima opzionale.

1. (Condizionale) Modifica la progettazione **[!UICONTROL Codice]**, come desiderato.

   Per ulteriori informazioni, consulta le informazioni nel passaggio 4 precedente.

1. Fai clic su **[!UICONTROL Salva]**.

## Modificare, copiare o eliminare una progettazione

Non è possibile modificare o copiare una progettazione predefinita; è possibile copiare solo le progettazioni predefinite.

Passa il puntatore del mouse sulla progettazione desiderata nella [!UICONTROL Progettazione] , quindi fare clic sull&#39;icona appropriata: modifica, copia o elimina.

![Icone al passaggio del mouse per una progettazione](/help/main/c-recommendations/c-design-overview/assets/hover-icons-design.png)

Potete copiare una progettazione esistente per creare una progettazione duplicata che potete quindi modificare. Questo consente di creare un design simile con meno sforzo.

Tieni presente che le progettazioni sono disponibili a livello dell’intero account. Prima di eliminare una progettazione, è necessario considerare questa possibilità. Non è possibile recuperare le progettazioni eliminate.

## Esempio JSON {#section_75BFB2537CFF4FBD9B560F59EB32C8DD}

L’esempio seguente mostra come le risposte JSON possono essere restituite durante la configurazione di un’attività tramite l’editor basato su moduli.

1. Creare una progettazione dall&#39;interno della Libreria di progettazione o all&#39;interno del flusso di lavoro basato su moduli. Se tenti di eseguire questa operazione all’interno del flusso di lavoro del Compositore esperienza visivo, puoi creare solo una struttura HTML, che viene racchiusa in un elemento `<div>` a scopo di tracciamento dei clic.

1. Assicurati che l&#39;opzione “Progettazione HTML” sia disattivata:

   ![immagine html_design_toggle](assets/html_design_toggle.png)

1. Il codice seguente è un esempio di ciò che puoi incollare nella progettazione:

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

1. Configurare un modulo [!DNL Recommendations] attività che utilizza questo design.

   1. Accedi a **[!UICONTROL Attività]** pagina.
   1. Fai clic su **[!UICONTROL Crea attività]** > **[!UICONTROL Consigli]**.
   1. Sotto **[!UICONTROL Scegli Compositore esperienza]**, seleziona **[!UICONTROL Modulo]**, quindi fai clic su **[!UICONTROL Successivo]**.
   1. In posizione, immetti il testo: “Sample_Recs_Response”
   1. In **[!UICONTROL Contenuto predefinito]** fai clic sulla freccia giù, poi su **[!UICONTROL Aggiungi consiglio]**.
   1. Scegli un Tipo di pagina. Questo determina il filtraggio iniziale della schermata successiva.
   1. Seleziona una scheda Criteri, poi fai clic su **[!UICONTROL Avanti]**.
   1. Seleziona la struttura creata nel passaggio precedente, quindi fai clic su **[!UICONTROL Successivo]**.
   1. Completa il processo di impostazione.
   1. Fai clic sulla freccia destra accanto a **[!UICONTROL Inattivo]**, poi seleziona **[!UICONTROL Attiva]**.

1. Dopo aver impostato e attivato l&#39;attività, è possibile impostare una richiesta di esempio per ottenere la risposta JSON pulita.

   Dal momento in cui salvi l’attività, [!DNL Target] dovrà generare un modello per supportare la configurazione dei criteri selezionati. A seconda di una serie di fattori, questo potrebbe richiedere del tempo. Una volta generato il modello vengono visualizzati i risultati.

   Ad esempio:

   ```
   https://[YOUR_CLIENT_CODE].tt.omtrdc.net/m2/YOUR_CLIENT_CODE/ubox/raw?mbox=[YOUR_MBOX_NAME]&mboxContentType=text/html&mboxXDomain=disabled&entity.id=[ENTITY_ID]&mboxHost=rawbox_sample&at_property=[AT_PROPERTY_TOKEN]&mboxNoRedirect=true&mboxPC=1234-4321&mboxSession=9876-7000
   ```

   dove

   | Parametro | Valore |
   |--- |--- |
   | `[YOUR_CLIENT_CODE]` | Codice client di Target (disponibile in /help/target/products.html#recsSettings > Token API di Recommendations > Codice client. |
   | `[YOUR_MBOX_NAME]` | Il nome selezionato nella sezione &quot;locations&quot; del Recommendations basato su moduli, in questo caso Sample_Recs_Response. |
   | `[ENTITY_ID` | L&#39;`entity.id` di un elemento nel catalogo. |
   | `[AT_PROPERTY_TOKEN]` | (Facoltativo) Aggiungi se hai selezionato una Proprietà (parte delle autorizzazioni dell&#39;azienda) durante l&#39;impostazione dell&#39;attività. |

Dopo che l&#39;algoritmo è stato eseguito e si dispone dei risultati, la risposta dovrebbe essere simile a questa:

![immagine json_recommendations](assets/json_recommendation.png){width="575px"}

## Suggerimenti e trucchi aggiuntivi per oggetti JSON {#section_C305673C68944749969DB239E3221DC2}

È inoltre possibile inviare un semplice elenco di elementi delimitato da virgole impostando una progettazione con la seguente sintassi:

```
entity1.id, $entity2.id, $entity3.id, $entity4.id, $entity5.id, 
```

In alternativa, è possibile inviare ulteriori informazioni nella risposta. Il file di codice seguente è un esempio più complesso che restituisce molto di più degli ID di entità con gli spazi associati (ordine). Questo esempio di progettazione restituisce anche i dettagli dell’attività, del Profilo di Target (come applicabile) e altri `entity.attributes` associati agli elementi restituiti.

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

## Video di formazione: Creare progettazioni personalizzate in Recommendations (3:20) ![Badge panoramica](/help/main/assets/overview.png)

Questo video contiene le seguenti informazioni:

* Creare una progettazione personalizzata
* Comprendere come inserire nelle progettazioni un riferimento a variabili di visualizzazione

>[!VIDEO](https://video.tv.adobe.com/v/27687)
