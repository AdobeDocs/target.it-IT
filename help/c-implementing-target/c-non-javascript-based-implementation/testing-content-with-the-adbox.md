---
description: Utilizza un AdBox per consegnare le immagini in un'implementazione off-site.
keywords: Implementazione;mbox.js non JavaScript;mbox;AdBox
seo-description: Utilizza un AdBox per consegnare le immagini in un'implementazione off-site.
seo-title: Creare un AdBox per un’immagine
solution: Target
subtopic: Introduzione
title: Creare un AdBox per un’immagine
topic: Standard
uuid: 6b1763f7-08de-4bde-9e20-e79b92b02f20
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Creare un AdBox per un’immagine{#create-an-adbox-for-an-image}

Utilizza un AdBox per consegnare le immagini in un'implementazione off-site.

Un AdBox è come una mbox, ma è controllato da un URL piuttosto che da JavaScript. Gli AdBox sono creati con un URL AdBox speciale che carica una mbox di tipo annuncio (o AdBox) nel tuo account Adobe. Utilizza questo AdBox al posto della mbox nelle tue attività. Utilizza l'URL AdBox anziché un riferimento diretto all'immagine in email o altre implementazioni non JavaScript.

Per capire come selezionare la configurazione giusta vedi [Implementazioni non basate su JavaScript](../../c-implementing-target/c-non-javascript-based-implementation/non-javascript-based-implementation.md#concept_4799C58B081A43F6B3B8CC25A8D5D7C4).

1. Crea l'URL AdBox:

   ```
   https://myClientCode.tt.omtrdc.net/m2/myClientCode/ubox/
   image?mbox=emailHeroImage123_320x200
   mboxDefault=http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2Fimg%2Flogo%2Egif
   ```

   * Dove `myClientCode` è il codice client dell’azienda. Il codice cliente della tua azienda è tutto minuscolo e non ha caratteri speciali.

      * **at.js**: il tuo codice cliente è disponibile nella parte superiore della pagina [!UICONTROL Configurazione &gt; Implementazione &gt; Modifica impostazioni at.js] nell’interfaccia di [!DNL Target].

      * **mbox.js**: il tuo codice cliente è disponibile nella parte superiore della pagina [!UICONTROL Configurazione &gt; Implementazione &gt; Modifica impostazioni mbox.js].
   * Dove `image` è il tipo di chiamata. In questo caso è un'immagine.

   * Dove `emailHeroImage123_320x200` è il nome dell’AdBox.

   * Dove `http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2Fimg%2Flogo%2Egif` è il contenuto predefinito della mbox. Questa deve essere un'immagine.

      Deve essere codificata in URL e deve essere un riferimento assoluto. You can use the [HTML URL Encoding Reference](https://www.w3schools.com/tags/ref_urlencode.asp) to quickly encode your URLs.


1. Crea [offerte di reindirizzamento](../../c-experiences/c-manage-content/offer-redirect.md#task_33C80CD722564303B687948261484F94) per ogni immagine alternativa.

   >[!NOTE] {class=“- topic/note ”}
   >
   >Le AdBox devono essere caricate con un’offerta di reindirizzamento o con l’offerta di contenuti predefinita. Altri tipi di offerte non funzioneranno. Poiché l'AdBox è un URL, può soltanto visualizzare gli URL che riceve, quindi funziona solo Offerta di reindirizzamento.

1. Crea l'attività.

   Consulta [Implementazioni non basate su JavaScript](../../c-implementing-target/c-non-javascript-based-implementation/non-javascript-based-implementation.md#concept_4799C58B081A43F6B3B8CC25A8D5D7C4) per l’installazione che permette di raggiungere gli obbiettivi.
1. Domande e risposte complete sull'attività.

   Come best practice, crea una pagina fittizia e verifica che tutte le esperienze, il contenuto predefinito e i rapporti agiscano come previsto su tutti i tipi di browser, per tutti gli ambienti. 1. Avvia l’attività.
