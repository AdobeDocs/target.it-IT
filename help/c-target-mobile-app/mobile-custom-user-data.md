---
keywords: mobile app;mobile app send data;target mobile app;mobile custom user data;mobile app custom data
description: Puoi inviare a Target informazioni aggiuntive sulla posizione o sull’utente, sotto forma di coppie nome-valore.
title: iOS - Inviare dati utente personalizzati
feature: mobile implementation
topic: Target
uuid: 00baa1e2-4d1c-4835-ac55-47c9ac8985ac
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 100%

---


# iOS - Inviare dati utente personalizzati{#ios-send-custom-user-data}

Puoi inviare a Target informazioni aggiuntive sulla posizione o sull’utente, sotto forma di coppie nome-valore.

Queste informazioni possono essere utilizzate per creare tipi di pubblico personalizzati (ad esempio, utenti che distano oltre 25.000 km) e generare rapporti.

Esistono due tipi di parametri che è possibile inviare con una chiamata di Target:

* Parametri mbox

   I parametri mbox non sono costanti nelle sessioni.
* Parametri del profilo

   I parametri di profilo sono memorizzati nell&#39;archivio profili visitatori e sono costanti nelle sessioni. I parametri mbox non perdurano. Mentre alcuni tasti sono riservati, i parametri profilo e mbox possono essere coppie chiave-valore personalizzate.

Sebbene esistano alcune chiavi riservate, entrambi i parametri profilo e mbox possono contenere coppie chiave-valore personalizzate.

1. Crea dizionario.

   Innanzitutto, crea un dizionario con i valori inviati da passare a Target. Per motivi di convenienza, aggiungilo all&#39;interno del metodo `welcomeMessageCampaign` in modo da non doverti preoccupare dell&#39;obbiettivo.

   Di seguito è riportato un dizionario di esempio. Puoi copiarlo e incollarlo all’interno di `(void)welcomeMessageCampaign`. I valori per le chiavi come `userLevel` e `userMiles` sono inseriti direttamente in questo esempio. In generale, si passano le variabili corrispondenti.

   ```
   NSDictionary *targetParams = [[NSDictionary alloc] initWithObjectsAndKeys: 
                                 @"platinum",@"userLevel", 
                                 @26500,@"userMiles", 
                                 @"1067007",@"entity.id", 
                                 @"dealsapp.qa", @"host", 
                                 @"fashion",@"entity.categoryId", 
                                 @"millenial", @"profile.persona", 
                                 @"cohort_5", @"profile.cohort", 
                                 nil];
   ```

   * Le chiavi con il profilo prefisso (ad esempio, `profile.persona`) sono memorizzate nel profilo dell&#39;utente.

      Questi attributi di profilo possono essere utilizzati in diverse attività e canali.

   * Le chiavi che non hanno alcun prefisso (ad esempio, `userMiles`) sono parametri mbox.

      Questi parametri sono disponibili solo durante la sessione.

   * Le chiavi con l&#39;entità prefisso (ad esempio,`entity.category.id`) vengono utilizzate per i consigli di prodotti.

1. Verifica i dati.
   1. In applicazione `didFinishLaunchingWithOptions`, rimuovi il commento o aggiungi `[ADBMobile setDebugLogging:YES];`.

      Così vengono stampati dettagliati log di debug.
   1. Genera l’app.
   1. Verifica che i parametri vengano passati nella chiamata di destinazione.

      Cerca il nome della posizione di destinazione nella console di debug. Verrà visualizzata una chiamata a `YOUR-CLIENT-CODE.tt.omtrdc.net` con tutti i parametri appena passati.

      ![](assets/mobile-debug.png)
   Puoi creare tipi di pubblico e limitare o indirizzare la visualizzazione del contenuto utilizzando questi parametri in Target Standard.
