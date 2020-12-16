---
keywords: mobile;tntVal;analytics;adobe analytics;integration;sdk;mobile sdk;
description: Questa sezione descrive come inviare  informazioni sulle attività delle app mobili Adobe Target a  Adobe Analytics per la segmentazione postAhoc.
title: Inviare  informazioni sull'attività Adobe Target a  Adobe Analytics
feature: mobile implementation
translation-type: tm+mt
source-git-commit: 6704ac2ec73361ad95e110e9182485537d0de642
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 40%

---


# Inviare informazioni sull’attività ad Adobe Analytics{#send-activity-information-to-adobe-analytics}

Questa sezione descrive come inviare [!DNL Target] informazioni sulle attività delle app mobili al Adobe [!DNL Analytics]  per la segmentazione post-hoc.

**Prerequisiti**

* Questa integrazione richiede che [!DNL Analytics] e [!DNL Target] siano implementati utilizzando l&#39;SDK di Mobile.
* Verifica che la suite di rapporti sia abilitata per ricevere informazioni sull&#39;attività da [!DNL Target].

   In genere questo viene fatto aggiungendo il codice client [!DNL Target] alla suite di rapporti [!DNL Analytics]. L’impostazione potrebbe essere già attiva se utilizzi l’integrazione SiteCatalyst/Test&amp;Target per le attività web. Per domande relative a questo passaggio, contatta l’Assistenza clienti di Adobe.

1. Ottenere le informazioni sull’attività.

   Se includete una stringa come quella riportata di seguito nel contenuto dell&#39;esperienza, [!DNL Target] restituisce le informazioni sull&#39;attività che potete inviare a [!DNL Analytics]:

   ```javascript
   ${campaign.id}:${campaign.recipe.id}:${campaign.recipe.trafficType}
   ```

   Sostituisci il testo nel codice json dell’esperienza con un elemento simile al seguente esempio:

   ```javascript
   { 
     "tntVal": ${campaign.id}:${campaign.recipe.id}:${campaign.recipe.trafficType}", 
     "title":"Welcome Message", 
     "message":"Get Free Shipping Today!" 
   }
   ```

   In questo esempio, viene aggiunto un nodo con la variabile `tntVal` per ottenere le informazioni sull&#39;attività. Aggiungi un codice simile per le altre esperienze, con un titolo e un messaggio appropriati.

   Questa stringa distribuisce un numero (ad esempio 115110:0:0) nella risposta di [!DNL Target]. Indica l&#39;ID attività, l&#39;ID esperienza e il tipo di traffico. Segue un esempio di risposta da [!DNL Target]:

   ```javascript
   { 
     "tntVal": 115110:0:0", 
     "title":"Welcome Message", 
     "message":"Get Free Shipping Today!" 
   }
   ```

1. Analizzare l’oggetto JSON.

   Analizzare la risposta ricevuta da [!DNL Target] nel callback. È possibile utilizzare `NSJSONSerialization` per analizzare la risposta e memorizzarla in un dizionario o in un array.

   Per ulteriori informazioni, fare riferimento alla [Documentazione sulla serializzazione NSJSONS](https://developer.apple.com/library/ios/documentation/Foundation/Reference/NSJSONSerialization_Class/#//apple_ref/occ/clm/NSJSONSerialization/JSONObjectWithData:options:error).

1. Inviare i dati ad [!DNL Analytics].

   Aggiungi le informazioni sull’attività analizzate (come `tntVal` nella risposta precedente) all’oggetto dati contestuali in una chiamata di [!DNL Analytics] Questa chiamata [!DNL Analytics] contenente i dati contestuali può essere attivata immediatamente oppure può attendere fino all&#39;avvio della successiva chiamata [!DNL Analytics].

   Ad esempio, questa chiamata può essere attivata nel callback della chiamata `targetLoadRequest`:

   ```javascript
   [ADBMobile trackAction:@"Welcome Screen"  
         data:@{@"&&tnt" : tntVal from response}];
   ```

   >[!NOTE]
   >
   >`&&tnt`è una chiave evento riservata nell’SDK per dispositivi mobili. La post-classificazione della variabile `tntVal` funziona nell’SDK per dispositivi mobili come nel web (JavaScript). [!DNL Analytics] Dopo l&#39;elaborazione delle informazioni in [!DNL Analytics], è necessario visualizzare i nomi delle attività e delle esperienze nell&#39;interfaccia [!DNL Analytics].

