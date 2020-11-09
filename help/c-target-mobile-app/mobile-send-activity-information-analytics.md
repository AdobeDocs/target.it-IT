---
keywords: mobile;tntVal;analytics;adobe analytics;integration;sdk;mobile sdk;
description: Questa sezione descrive come inviare  informazioni sulle attività delle app mobili Adobe Target a  Adobe Analytics per la segmentazione postAhoc.
title: Inviare  informazioni sull'attività Adobe Target a  Adobe Analytics
feature: mobile implementation
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 40%

---


# Inviare informazioni sull’attività ad Adobe Analytics{#send-activity-information-to-adobe-analytics}

This section describes how to send [!DNL Target] mobile app activity information to Adobe [!DNL Analytics] for post hoc segmentation.

**Prerequisiti**

* This integration requires that [!DNL Analytics] and [!DNL Target] are implemented using the mobile SDK.
* Ensure that your report suite is enabled to receive activity information from [!DNL Target].

   This is usually done by adding the [!DNL Target] client code to the [!DNL Analytics] report suite. L’impostazione potrebbe essere già attiva se utilizzi l’integrazione SiteCatalyst/Test&amp;Target per le attività web. Per domande relative a questo passaggio, contatta l’Assistenza clienti di Adobe.

1. Ottenere le informazioni sull’attività.

   If you include a string like the following in your experience content, [!DNL Target] returns the activity information that you can send to [!DNL Analytics]:

   ```
   ${campaign.id}:${campaign.recipe.id}:${campaign.recipe.trafficType}
   ```

   Sostituisci il testo nel codice json dell’esperienza con un elemento simile al seguente esempio:

   ```
   { 
     "tntVal": ${campaign.id}:${campaign.recipe.id}:${campaign.recipe.trafficType}", 
     "title":"Welcome Message", 
     "message":"Get Free Shipping Today!" 
   }
   ```

   In this example, a node with the variable `tntVal` is added to obtain the activity information. Aggiungi un codice simile per le altre esperienze, con un titolo e un messaggio appropriati.

   Questa stringa distribuisce un numero (ad esempio 115110:0:0) nella risposta di [!DNL Target]. Indica l&#39;ID attività, l&#39;ID esperienza e il tipo di traffico. The following is a sample response from [!DNL Target]:

   ```
   { 
     "tntVal": 115110:0:0", 
     "title":"Welcome Message", 
     "message":"Get Free Shipping Today!" 
   }
   ```

1. Analizzare l’oggetto JSON.

   Parse the response that came back from [!DNL Target] in the callback. You can use `NSJSONSerialization` to parse this response and store it in a dictionary or an array.

   Per ulteriori informazioni, consulta la documentazione [](https://developer.apple.com/library/ios/documentation/Foundation/Reference/NSJSONSerialization_Class/#//apple_ref/occ/clm/NSJSONSerialization/JSONObjectWithData:options:error) NSJSONSerialization.

1. Inviare i dati ad [!DNL Analytics].

   Aggiungi le informazioni sull’attività analizzate (come `tntVal` nella risposta precedente) all’oggetto dati contestuali in una chiamata di [!DNL Analytics] This [!DNL Analytics] call containing the context data can be fired immediately or it can wait until the next [!DNL Analytics] call is fired.

   Ad esempio, questa chiamata può essere attivata nel callback della chiamata `targetLoadRequest`:

   ```
   [ADBMobile trackAction:@"Welcome Screen"  
         data:@{@"&&tnt" : tntVal from response}];
   ```

   >[!NOTE]
   >
   >`&&tnt`è una chiave evento riservata nell’SDK per dispositivi mobili. La post-classificazione della variabile `tntVal` funziona nell’SDK per dispositivi mobili come nel web (JavaScript). [!DNL Analytics] After the information is processed in [!DNL Analytics], you should see activity and experience names in the [!DNL Analytics] interface.

