---
keywords: Implementazione;mbox.js non JavaScript;mbox;AdBox
description: Usate un AdBox per distribuire immagini in un’implementazione off-site, utilizzando  Adobe Target.
title: Creare un AdBox per un’immagine
feature: Implement Email
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 80%

---


# Creare un AdBox per un’immagine{#create-an-adbox-for-an-image}

Utilizzate un AdBox per distribuire immagini in un&#39;implementazione off-site tramite  Adobe Target.

Un AdBox è come una mbox, ma è controllato da un URL piuttosto che da JavaScript. Gli AdBox sono creati con un URL AdBox speciale che carica una mbox di tipo annuncio (o AdBox) nel tuo account Adobe. Utilizza questo AdBox al posto della mbox nelle tue attività. Utilizza l&#39;URL AdBox anziché un riferimento diretto all&#39;immagine in email o altre implementazioni non JavaScript.

Per capire come selezionare la configurazione giusta vedi [Implementazioni non basate su JavaScript](/help/c-implementing-target/c-non-javascript-based-implementation/non-javascript-based-implementation.md#concept_4799C58B081A43F6B3B8CC25A8D5D7C4).

1. Crea l&#39;URL AdBox:

   ```
   https://myClientCode.tt.omtrdc.net/m2/myClientCode/ubox/
   image?mbox=emailHeroImage123_320x200&
   mboxDefault=http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2Fimg%2Flogo%2Egif
   ```

   * Dove `myClientCode` è il codice client dell’azienda. Il codice cliente della tua azienda è tutto minuscolo e non ha caratteri speciali.

      Il codice client è disponibile nella parte superiore della pagina [!UICONTROL Amministrazione > Implementazione] dell&#39;interfaccia [!DNL Target].

   * Dove `image` è il tipo di chiamata. In questo caso è un&#39;immagine.

   * Dove `emailHeroImage123_320x200` è il nome dell’AdBox.

   * Dove `http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2Fimg%2Flogo%2Egif` è il contenuto predefinito della mbox. Questa deve essere un&#39;immagine.

      Deve essere codificata in URL e deve essere un riferimento assoluto. Per codificare rapidamente gli URL, potete utilizzare il [Riferimento codifica URL HTML](https://www.w3schools.com/tags/ref_urlencode.asp).

1. Crea [offerte di reindirizzamento](/help/c-experiences/c-manage-content/offer-redirect.md#task_33C80CD722564303B687948261484F94) per ogni immagine alternativa.

   >[!NOTE]
   >
   >Le AdBox devono essere caricate con un’offerta di reindirizzamento o con l’offerta di contenuti predefinita. Altri tipi di offerte non funzioneranno. Poiché l&#39;AdBox è un URL, può soltanto visualizzare gli URL che riceve, quindi funziona solo Offerta di reindirizzamento.

1. Crea l&#39;attività.

   Consulta [Implementazioni non basate su JavaScript](/help/c-implementing-target/c-non-javascript-based-implementation/non-javascript-based-implementation.md#concept_4799C58B081A43F6B3B8CC25A8D5D7C4) per l’installazione che permette di raggiungere gli obbiettivi.
1. Domande e risposte complete sull&#39;attività.

   Come best practice, crea una pagina fittizia e verifica che tutte le esperienze, il contenuto predefinito e i rapporti agiscano come previsto su tutti i tipi di browser, per tutti gli ambienti.

1. Avvia l’attività.
