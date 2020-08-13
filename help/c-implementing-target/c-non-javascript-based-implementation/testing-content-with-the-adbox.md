---
keywords: Implementation;mbox.js non javascript;mbox;adbox
description: Usate un AdBox per distribuire immagini in un’implementazione off-site, utilizzando  Adobe Target.
title: Creare un Adbox per un’immagine utilizzando  Adobe Target
feature: email implementation
subtopic: Getting Started
topic: Standard
uuid: 6b1763f7-08de-4bde-9e20-e79b92b02f20
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 77%

---


# Creare un AdBox per un’immagine{#create-an-adbox-for-an-image}

Utilizzate un AdBox per distribuire immagini in un&#39;implementazione off-site tramite  Adobe Target.

Un AdBox è come una mbox, ma è controllato da un URL piuttosto che da JavaScript. Gli AdBox sono creati con un URL AdBox speciale che carica una mbox di tipo annuncio (o AdBox) nel tuo account Adobe. Utilizza questo AdBox al posto della mbox nelle tue attività. Utilizza l&#39;URL AdBox anziché un riferimento diretto all&#39;immagine in email o altre implementazioni non JavaScript.

Per capire come selezionare la configurazione giusta vedi [Implementazioni non basate su JavaScript](../../c-implementing-target/c-non-javascript-based-implementation/non-javascript-based-implementation.md#concept_4799C58B081A43F6B3B8CC25A8D5D7C4).

1. Crea l&#39;URL AdBox:

   ```
   https://myClientCode.tt.omtrdc.net/m2/myClientCode/ubox/
   image?mbox=emailHeroImage123_320x200&
   mboxDefault=http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2Fimg%2Flogo%2Egif
   ```

   * Dove `myClientCode` è il codice client dell’azienda. Il codice cliente della tua azienda è tutto minuscolo e non ha caratteri speciali.

      Your client code is available at the top of the [!UICONTROL Administation > Implementation] page of the [!DNL Target] interface.

   * Dove `image` è il tipo di chiamata. In questo caso è un&#39;immagine.

   * Dove `emailHeroImage123_320x200` è il nome dell’AdBox.

   * Dove `http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2Fimg%2Flogo%2Egif` è il contenuto predefinito della mbox. Questa deve essere un&#39;immagine.

      Deve essere codificata in URL e deve essere un riferimento assoluto. You can use the [HTML URL Encoding Reference](https://www.w3schools.com/tags/ref_urlencode.asp) to quickly encode your URLs.

1. Crea [offerte di reindirizzamento](../../c-experiences/c-manage-content/offer-redirect.md#task_33C80CD722564303B687948261484F94) per ogni immagine alternativa.

   >[!NOTE]
   >
   >Le AdBox devono essere caricate con un’offerta di reindirizzamento o con l’offerta di contenuti predefinita. Altri tipi di offerte non funzioneranno. Poiché l&#39;AdBox è un URL, può soltanto visualizzare gli URL che riceve, quindi funziona solo Offerta di reindirizzamento.

1. Crea l&#39;attività.

   Consulta [Implementazioni non basate su JavaScript](../../c-implementing-target/c-non-javascript-based-implementation/non-javascript-based-implementation.md#concept_4799C58B081A43F6B3B8CC25A8D5D7C4) per l’installazione che permette di raggiungere gli obbiettivi.
1. Domande e risposte complete sull&#39;attività.

   Come best practice, crea una pagina fittizia e verifica che tutte le esperienze, il contenuto predefinito e i rapporti agiscano come previsto su tutti i tipi di browser, per tutti gli ambienti.

1. Avvia l’attività.
