---
description: Questa sezione descrive come inviare informazioni sulle attività delle app mobili di Target ad Adobe Analytics per la segmentazione postAdHoc.
seo-description: Questa sezione descrive come inviare informazioni sulle attività delle app mobili di Target ad Adobe Analytics per la segmentazione postAdHoc.
seo-title: Inviare informazioni sull’attività ad Adobe Analytics
title: Inviare informazioni sull’attività ad Adobe Analytics
uuid: 2ca1ebfe-5008-4a73-a032-1ad81f062925
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Inviare informazioni sull’attività ad Adobe Analytics{#send-activity-information-to-adobe-analytics}

Questa sezione descrive come inviare informazioni sulle attività delle app mobili di Target ad Adobe Analytics per la segmentazione postAdHoc.

**Prerequisiti**

* Questa integrazione richiede che Analytics e Target vengano implementati mediante l’SDK per dispositivi mobili.
* Assicurati che la suite di rapporti sia abilitata per ricevere informazioni sull’attività da Target.

   In genere, questo è possibile aggiungendo il codice client di Target alla suite di rapporti di Analytics. L’impostazione potrebbe essere già attiva se utilizzi l’integrazione SiteCatalyst/Test&amp;Target per le attività web. Per domande relative a questo passaggio, contatta l’Assistenza clienti di Adobe.

1. Ottenere le informazioni sull’attività.

   Se includi una stringa come quella riportata di seguito nel contenuto dell’esperienza, Target restituisce informazioni sulla campagna da inviare ad Analytics:

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

   In questo esempio, viene aggiunto un nodo con la variabile “ `tntVal`” per ottenere le informazioni relative all’attività. Aggiungi un codice simile per le altre esperienze, con un titolo e un messaggio appropriati.

   Questa stringa distribuisce un numero (ad esempio 115110:0:0) nella risposta di Target. Questo indica l’ID attività, l’ID esperienza e il tipo di traffico. Di seguito è riportato un esempio di risposta di Target:

   ```
   { 
     "tntVal": 115110:0:0", 
     "title":"Welcome Message", 
     "message":"Get Free Shipping Today!" 
   }
   ```

1. Analizzare l’oggetto JSON.

   Analizza la risposta restituita da Target nella chiamata di ritorno. Utilizza NSJSONSerialization per analizzare questa risposta e memorizzarla in una dipendenza o un array.

   Refer to the [NSJSONSerialization documentation](https://developer.apple.com/library/ios/documentation/Foundation/Reference/NSJSONSerialization_Class/#//apple_ref/occ/clm/NSJSONSerialization/JSONObjectWithData:options:error) for more information.
1. Inviare i dati ad Analytics.

   Aggiungi le informazioni sull’attività analizzate (come `tntVal` nella risposta precedente) all’oggetto dati contestuali in una chiamata di Analytics. Questa chiamata di Analytics contenente i dati contestuali può essere attivata immediatamente oppure può attendere finché non viene avviata la chiamata di Analytics successiva.

   Ad esempio, questa chiamata può essere attivata nel callback della chiamata `targetLoadRequest`:

   ```
   [ADBMobile trackAction:@"Welcome Screen"  
         data:@{@"&&tnt" : tntVal from response}];
   ```

   >[!NOTE]
   >
   >`&&tnt`è una chiave evento riservata nell’SDK per dispositivi mobili. La post-classificazione della variabile `tntVal` in Analytics funziona nell’SDK per dispositivi mobili come nel web (JavaScript). Una volta elaborate le informazioni in Analytics, dovresti vedere i nomi delle attività e delle esperienze nell’interfaccia di Analytics.

