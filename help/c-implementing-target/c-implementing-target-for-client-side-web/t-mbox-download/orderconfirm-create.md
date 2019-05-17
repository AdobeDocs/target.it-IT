---
description: Con la mbox di conferma dell’ordine è possibile registrare i dettagli sugli ordini sul sito e generare rapporti in base a ricavi e ordini. Con la mbox di conferma dell’ordine è inoltre possibile determinare algoritmi per i consigli, come “Persone che hanno acquistato il prodotto x hanno acquistato anche il prodotto y”.
keywords: conferma d’ordine;orderConfirmPage
seo-description: Con la mbox di conferma dell’ordine è possibile registrare i dettagli sugli ordini sul sito e generare rapporti in base a ricavi e ordini. Con la mbox di conferma dell’ordine è inoltre possibile determinare algoritmi per i consigli, come “Persone che hanno acquistato il prodotto x hanno acquistato anche il prodotto y”.
seo-title: Creare una mbox di conferma d'ordine - mbox.js
solution: Target
subtopic: Introduzione
title: Creare una mbox di conferma d'ordine - mbox.js
uuid: 001da2bd-2ccf-490b-ba84-ac9b9a2a5451
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Creare una mbox di conferma d’ordine - mbox.js{#create-an-order-confirmation-mbox-mbox-js}

Con la mbox di conferma dell’ordine è possibile registrare i dettagli sugli ordini sul sito e generare rapporti in base a ricavi e ordini. Con la mbox di conferma dell’ordine è inoltre possibile determinare algoritmi per i consigli, come “Persone che hanno acquistato il prodotto x hanno acquistato anche il prodotto y”.

>[!NOTE]
>
>Se gli utenti effettuano acquisti sul tuo sito web, ti consigliamo di implementare una mbox di conferma d’ordine anche se per generare rapporti usi Analytics for Target (A4t).

>[!NOTE]
>
>Puoi anche creare una mbox di conferma d’ordine per at.js utilizzando lo stesso metodo. Tuttavia, si consiglia il metodo [!DNL at.js]. Per ulteriori informazioni, consulta [Tracciare le conversioni](../../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#task_E85D2F64FEB84201A594F2288FABF053).

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