---
keywords: Progettazione consigli;creare progettazione;copia progettazione
description: Scopri come creare un design Adobe [!DNL Target] Recommendations utilizzando una progettazione predefinita o creando una progettazione personalizzata per adattarla al meglio al layout della pagina.
title: Come si crea un design in Recommendations?
feature: Consigli
exl-id: 0f10ee9d-7210-4e02-9342-e4f85cf46e8c
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '1018'
ht-degree: 34%

---

# ![PREMIUM](/help/assets/premium.png) Creare una progettazione

Una progettazione definisce come i consigli verranno visualizzati su una pagina.

È possibile creare una progettazione [!UICONTROL Consigli] utilizzando una progettazione predefinita o creandone una personalizzata. La schermata **[!UICONTROL Recommendations > Progettazioni]** visualizza sia le schede di progettazione predefinite che le progettazioni create nel tuo account.

Quando lavori con le progettazioni, ricorda quanto segue:

* Potete creare una progettazione di consigli utilizzando una progettazione predefinita oppure una progettazione personalizzata.
* Non è possibile modificare o eliminare una progettazione predefinita.
* È possibile modificare, copiare o eliminare una progettazione personalizzata.
* Per creare una progettazione basata su una progettazione predefinita, dovete prima copiare la progettazione e quindi modificare la copia.

Questa illustrazione mostra la progettazione predefinita di 1 x 4:

![Design predefinito 1 x 4](/help/c-recommendations/c-design-overview/assets/default-design.png)

Questa illustrazione mostra una progettazione personalizzata:

![Progettazione personalizzata](/help/c-recommendations/c-design-overview/assets/custom-design.png)

Puoi creare una progettazione durante il processo di creazione dell’attività direttamente dal Compositore esperienza visivo o dalla libreria di progettazione, all’esterno della creazione dell’attività. Le sezioni seguenti presuppongono la creazione di progettazioni dalla libreria, ma i passaggi sono simili.

## Creare progettazioni

Potete creare una progettazione basata su una progettazione predefinita oppure una progettazione personalizzata.

### Creare una progettazione basata su una progettazione predefinita

1. Fai clic su **[!UICONTROL Recommendations]** > **[!UICONTROL Progettazioni]** per visualizzare la libreria [!UICONTROL Progettazioni].

   ![Libreria progettazione](/help/c-recommendations/c-design-overview/assets/design-library.png)

1. Passa il puntatore del mouse sulla scheda della progettazione che desideri creare, quindi fai clic sull&#39;icona **[!UICONTROL Copia]**.

   ![](assets/Card_CopyDesign.png)

   Viene visualizzata la finestra di dialogo [!UICONTROL Crea progettazione].

   ![](assets/createDesign.png)

1. Nel pannello **[!UICONTROL Informazioni]**, aggiungi un **[!UICONTROL Nome contenuto]** e un&#39;immagine di anteprima opzionale da visualizzare sulla scheda di progettazione.

   Quando si utilizza una progettazione predefinita, il nome della progettazione e la &quot;copia&quot; vengono visualizzati nel campo **[!UICONTROL Nome contenuto]** . È possibile modificare il nome. Potete anche selezionare un&#39;immagine da visualizzare sulla scheda di progettazione.

1. (Condizionale) Modifica la progettazione **[!UICONTROL Codice]**, come desiderato.

   Le progettazioni per consigli utilizzano il linguaggio di progettazione open-source Velocity. Le informazioni su Velocity sono disponibili all&#39;indirizzo [https://velocity.apache.org](https://velocity.apache.org) e in [Personalizzare una progettazione con Velocity](/help/c-recommendations/c-design-overview/customizing-a-template.md).

   Una progettazione può essere HTML o non HTML. Per impostazione predefinita, le progettazioni HTML sono racchiuse da un tag `<div>` per consentire il tracciamento dei clic in un ambiente web. Le progettazioni non HTML sono per ambienti non web in cui non è possibile effettuare il monitoraggio dei clic. Fai scorrere l&#39;interruttore [!UICONTROL Progettazione HTML] nella posizione &quot;off&quot; per utilizzare codice non HTML.

   >[!NOTE]
   >
   >Il numero massimo di entità a cui è possibile fare riferimento in una progettazione, tramite codifica fissa o cicli, è 99.

1. Fai clic su **[!UICONTROL Salva]**.

### Creare una progettazione personalizzata

1. Fai clic su **[!UICONTROL Recommendations]** > **[!UICONTROL Progettazioni]** per visualizzare la libreria [!UICONTROL Progettazioni].

1. Fare clic su **[!UICONTROL Crea progettazione]**.

   Se desideri basare la nuova progettazione personalizzata su una progettazione esistente, passa il puntatore del mouse sulla progettazione desiderata, quindi fai clic sull&#39;icona [!UICONTROL Copia] . Puoi quindi modificare la copia per creare una nuova progettazione personalizzata.

1. Aggiungi un **[!UICONTROL Nome contenuto]** e un&#39;immagine di anteprima opzionale.

1. (Condizionale) Modifica la progettazione **[!UICONTROL Codice]**, come desiderato.

   Per ulteriori informazioni, consulta le informazioni del precedente passaggio 4 .

1. Fai clic su **[!UICONTROL Salva]**.

## Modificare, copiare o eliminare una progettazione

Non è possibile modificare o copiare una progettazione predefinita; è possibile copiare solo le progettazioni predefinite.

Passa il puntatore del mouse sulla progettazione desiderata nella libreria [!UICONTROL Progettazione] , quindi fai clic sull&#39;icona appropriata: modificare, copiare o eliminare elementi.

![Icone al passaggio del mouse per una progettazione](/help/c-recommendations/c-design-overview/assets/hover-icons-design.png)

Potete copiare una progettazione esistente per creare una progettazione duplicata da modificare. Questo consente di creare un design simile con meno sforzo.

Tieni presente che le progettazioni sono disponibili nell’intero account. Considerate questo aspetto prima di eliminare una progettazione. I disegni eliminati non possono essere recuperati.

## Esempio JSON {#section_75BFB2537CFF4FBD9B560F59EB32C8DD}

L’esempio seguente mostra come è possibile restituire le risposte JSON durante la configurazione di un’attività tramite l’editor basato su moduli.

1. Crea una progettazione dall’interno della libreria di progettazione o all’interno del flusso di lavoro basato su moduli. Se tenti di eseguire questa operazione all’interno del flusso di lavoro del Compositore esperienza visivo, puoi creare solo una struttura HTML, che viene racchiusa in un elemento `<div>` a scopo di tracciamento dei clic.

1. Assicurati che l&#39;opzione “Progettazione HTML” sia disattivata:

   ![](assets/html_design_toggle.png)

1. Il codice seguente è un esempio di ciò che è possibile incollare nella progettazione:

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

1. Imposta un&#39;attività [!DNL Recommendations] basata su moduli che utilizza questa progettazione.

   1. Passa alla pagina **[!UICONTROL Attività]** .
   1. Fai clic su **[!UICONTROL Crea attività]** > **[!UICONTROL Consigli]**.
   1. In **[!UICONTROL Scegli Compositore esperienza]**, seleziona **[!UICONTROL Modulo]**, quindi fai clic su **[!UICONTROL Avanti]**.
   1. In posizione, immetti il testo: “Sample_Recs_Response”
   1. In **[!UICONTROL Contenuto predefinito]** fai clic sulla freccia giù, poi su **[!UICONTROL Aggiungi consiglio]**.
   1. Scegli un Tipo di pagina. Questo determina il filtraggio iniziale della schermata successiva.
   1. Seleziona una scheda Criteri, poi fai clic su **[!UICONTROL Avanti]**.
   1. Seleziona la progettazione creata nel passaggio precedente, quindi fai clic su **[!UICONTROL Avanti]**.
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
   | `[YOUR_CLIENT_CODE]` | Codice client di Target (disponibile su /help/target/products.html#recsSettings > Token API di Recommendations > Codice client. |
   | `[YOUR_MBOX_NAME]` | Nome selezionato nella sezione &quot;Posizioni&quot; del Recommendations basato su moduli, in questo caso Sample_Recs_Response. |
   | `[ENTITY_ID` | L&#39;`entity.id` di un elemento nel catalogo. |
   | `[AT_PROPERTY_TOKEN]` | (Facoltativo) Aggiungi se hai selezionato una Proprietà (parte delle autorizzazioni dell&#39;azienda) durante l&#39;impostazione dell&#39;attività. |

Dopo che l&#39;algoritmo è stato eseguito e si dispone dei risultati, la risposta dovrebbe essere simile a questa:

![](assets/json_recommendation.png){width=&quot;575px&quot;}

## Ulteriori suggerimenti sugli oggetti JSON {#section_C305673C68944749969DB239E3221DC2}

È inoltre possibile inviare un semplice elenco di elementi delimitato da virgole impostando una progettazione con la seguente sintassi:

```
entity1.id, $entity2.id, $entity3.id, $entity4.id, $entity5.id, 
```

In alternativa, è possibile inviare ulteriori informazioni nella risposta. Il file di codice seguente è un esempio più complesso che restituisce molto di più degli ID di entità con gli spazi associati (ordine). In questo esempio di progettazione vengono inoltre restituiti i dettagli dell’attività, del profilo di Target (come applicabile) e altri `entity.attributes` associati agli elementi restituiti.

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

## Video di formazione: Creare progettazioni personalizzate in Recommendations (3:20) ![Badge panoramica](/help/assets/overview.png)

Questo video contiene le seguenti informazioni:

* Creare una progettazione personalizzata
* Comprendere come inserire nelle progettazioni un riferimento a variabili di visualizzazione

>[!VIDEO](https://video.tv.adobe.com/v/27687)
