---
keywords: conferma d’ordine;orderConfirmPage
description: Scoprite l'implementazione legacy di mbox.js  Adobe Target. Esegui la migrazione all’SDK Web Adobe Experience Platform (AEP Web SDK) o all’ultima versione di at.js.
title: Come si crea una mbox di conferma dell'ordine utilizzando mbox.js?
feature: at.js
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 58%

---


# Creare una mbox di conferma d&#39;ordine - mbox.js

Con la mbox di conferma dell’ordine è possibile registrare i dettagli sugli ordini sul sito e generare rapporti in base a ricavi e ordini. Con la mbox di conferma dell’ordine è inoltre possibile determinare algoritmi per i consigli, come “Persone che hanno acquistato il prodotto x hanno acquistato anche il prodotto y”.

>[!IMPORTANT]
>
>**fine ciclo di vita** di mbox.js: Il 31 marzo 2021 non  [!DNL Adobe Target] supporterà più la libreria mbox.js. Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto positivo sulle pagine che hanno attività [!DNL Target] in esecuzione distribuendo contenuti predefiniti.
>
>È consigliabile che tutti i clienti effettuino la migrazione alla versione più recente della nuova [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js prima di tale data, per evitare potenziali problemi con i siti. Per ulteriori informazioni, vedere [Panoramica: implementate Target per Web lato client](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

>[!NOTE]
>
>* Se gli utenti effettuano acquisti sul tuo sito web, ti consigliamo di implementare una mbox di conferma d’ordine anche se per generare rapporti usi Analytics for Target (A4T).
   >
   >
* Potete anche creare una mbox di conferma dell&#39;ordine per at.js 1.** usando lo stesso metodo; tuttavia, il  [!DNL at.js] metodo è preferibile. Per ulteriori informazioni, consulta [Tracciare le conversioni](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#task_E85D2F64FEB84201A594F2288FABF053).
   >
   >
* Se utilizzi at.js 2.*x*, non  `mboxCreate` è più supportato. Per la conferma dell&#39;ordine utilizzando at.js 2.*x*, usa le seguenti API relative al tracciamento:  [trackEvent() ](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-trackevent.md) e  [sendNotifications()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe.target.sendnotifications-atjs-21.md).


1. Nella pagina dei dettagli dell’ordine, inserisci lo script mbox secondo il modello indicato di seguito.
1. Sostituisci le parole in lettere maiuscole con valori dinamici o statici provenienti dal catalogo.

   >[!NOTE]
   >
   >Utilizza le virgole per separare i diversi ID prodotto.

   **Suggerimento:** è possibile, inoltre, passare le informazioni di ordine in qualsiasi mbox (non deve per forza chiamarsi `orderConfirmPage`). Inoltre, puoi passare le informazioni di ordine in più mbox all&#39;interno della stessa campagna.

   ```
   <div class="mboxDefault"> 
      <!-- CONTENT TO SHOW IF NO OFFERS AVAILABLE. --> 
   </div> 
   <script type="text/javascript">    
      mboxCreate('orderConfirmPage', 
      'productPurchasedId=PRODUCT ID FROM YOUR ORDER PAGE, PRODUCT ID2, PRODUCT ID3', 
      'orderTotal=ORDER TOTAL FROM YOUR ORDER PAGE', 
      'orderId=ORDER ID FROM YOUR ORDER PAGE'); 
   </script> 
   ```

La mbox di conferma d&#39;ordine utilizza i seguenti parametri:

| Parametro | Descrizione |
|--- |--- |
| `orderId` | Valore univoco per identificare un ordine per il conteggio di conversione.<br>L’`orderId` deve essere univoco. Gli ordini duplicati vengono ignorati nei rapporti. |
| `orderTotal` | Valore monetario dell&#39;acquisto.<br>Non trasmettere il simbolo di valuta. Utilizza un punto decimale (non la virgola) per indicare i valori decimali. |
| `productPurchasedId` (Facoltativo) | Elenco degli ID dei prodotti acquistati nell&#39;ordine, separati da virgole.<br>Questi ID prodotto vengono visualizzati nel rapporto di revisione per supportare attività aggiuntive di analisi dei rapporti. |