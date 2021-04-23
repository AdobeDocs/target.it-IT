---
keywords: mobile;tntVal;analytics;adobe analytics;integrazione;sdk;sdk mobile;
description: Scopri come inviare informazioni sulle attività delle app mobili Adobe [!DNL Target] ad Adobe Analytics per la segmentazione post Ad Hoc.
title: Posso inviare informazioni sull’attività dell’app mobile ad Analytics?
feature: Implementare Mobile
role: Developer
exl-id: 33812f14-320f-40c3-8234-d6006fb4d6bc
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 39%

---

# Inviare informazioni sull’attività ad Adobe Analytics

Questa sezione descrive come inviare [!DNL Target] informazioni sulle attività delle app mobili ad Adobe [!DNL Analytics] per la segmentazione post-hoc.

**Prerequisiti**

* Questa integrazione richiede che [!DNL Analytics] e [!DNL Target] siano implementati utilizzando l&#39;SDK mobile.
* Assicurati che la suite di rapporti sia abilitata per ricevere informazioni sull’attività da [!DNL Target].

   In genere questo viene fatto aggiungendo il codice client [!DNL Target] alla suite di rapporti [!DNL Analytics] . L’impostazione potrebbe essere già attiva se utilizzi l’integrazione SiteCatalyst/Test&amp;Target per le attività web. Per domande relative a questo passaggio, contatta l’Assistenza clienti di Adobe.

1. Ottenere le informazioni sull’attività.

   Se nel contenuto dell&#39;esperienza includi una stringa come la seguente, [!DNL Target] restituisce le informazioni sull&#39;attività che puoi inviare a [!DNL Analytics]:

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

   In questo esempio, viene aggiunto un nodo con la variabile `tntVal` per ottenere le informazioni sull’attività. Aggiungi un codice simile per le altre esperienze, con un titolo e un messaggio appropriati.

   Questa stringa distribuisce un numero (ad esempio 115110:0:0) nella risposta di [!DNL Target]. Indica l’ID attività, l’ID esperienza e il tipo di traffico. Di seguito è riportato un esempio di risposta da [!DNL Target]:

   ```javascript
   { 
     "tntVal": 115110:0:0", 
     "title":"Welcome Message", 
     "message":"Get Free Shipping Today!" 
   }
   ```

1. Analizzare l’oggetto JSON.

   Analizza la risposta restituita da [!DNL Target] nel callback. È possibile utilizzare `NSJSONSerialization` per analizzare questa risposta e memorizzarla in un dizionario o in una matrice.

   Per ulteriori informazioni, consulta la documentazione [NSJSONSerialization](https://developer.apple.com/library/ios/documentation/Foundation/Reference/NSJSONSerialization_Class/#//apple_ref/occ/clm/NSJSONSerialization/JSONObjectWithData:options:error) .

1. Inviare i dati ad [!DNL Analytics].

   Aggiungi le informazioni sull’attività analizzate (come `tntVal` nella risposta precedente) all’oggetto dati contestuali in una chiamata di [!DNL Analytics] Questa chiamata [!DNL Analytics] contenente i dati contestuali può essere attivata immediatamente oppure può attendere che venga attivata la successiva chiamata [!DNL Analytics] .

   Ad esempio, questa chiamata può essere attivata nel callback della chiamata `targetLoadRequest`:

   ```javascript
   [ADBMobile trackAction:@"Welcome Screen"  
         data:@{@"&&tnt" : tntVal from response}];
   ```

   >[!NOTE]
   >
   >`&&tnt`è una chiave evento riservata nell’SDK per dispositivi mobili. La post-classificazione della variabile `tntVal` funziona nell’SDK per dispositivi mobili come nel web (JavaScript). [!DNL Analytics] Dopo l&#39;elaborazione delle informazioni in [!DNL Analytics], dovresti vedere i nomi delle attività e delle esperienze nell&#39;interfaccia [!DNL Analytics].
