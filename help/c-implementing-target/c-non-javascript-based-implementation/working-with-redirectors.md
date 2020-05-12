---
keywords: Implementation;mbox.js non javascript;redirector;costs per click;revenue per click
description: È possibile utilizzare un redirector in modo simile a come si utilizza una mbox nei test.
title: Lavorare con i redirector
subtopic: Getting Started
topic: Standard
uuid: 79d7caf6-5693-4bb3-9131-8d1ae420fa5e
translation-type: tm+mt
source-git-commit: d8f059565ff44646c99b284ffb765377f5e9d19d
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 73%

---


# Lavorare con i redirector{#work-with-redirectors}

È possibile utilizzare un redirector in modo simile a come si utilizza una mbox nei test.

I redirector vengono creati con un URL redirector speciale che carica una mbox redirector (redirector) nel tuo account. Puoi utilizzare un redirector in modo simile a come si utilizza una mbox nei test. Invia l’URL del redirector al tuo Ad Network come collegamento di destinazione dell’annuncio.

Utilizza il redirector per eseguire le operazioni seguenti:

* Tenere traccia dei clic dagli annunci display al sito
* Creare un singolo rapporto centralizzato per tenere traccia dei clic e visualizzare gli annunci su più ad network
* Variare le destinazioni degli annunci display

   Ad esempio, lo stesso banner porta alla home page, alla pagina delle categorie e alla pagina di un prodotto.

* Trovare la pagina di destinazione che genera il maggior numero di conversioni

Per decidere la giusta configurazione, consulta [Implementazioni non basate su JavaScript](../../c-implementing-target/c-non-javascript-based-implementation/non-javascript-based-implementation.md#concept_4799C58B081A43F6B3B8CC25A8D5D7C4).

## Create a redirector {#redirector}

Prima di poter utilizzare un redirector, è necessario crearlo.

1. Determina le varianti di destinazione dell&#39;annuncio, inclusa la destinazione predefinita.
1. Crea l&#39;URL di redirector.

   ```
   https://<your_testandtarget_clientcode>.tt.omtrdc.net/​m2/yourclientcode/ubox
   /​page?mbox=redirectorlink_456
   &mboxDefault=http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2Fusualdestination%2Ehtm
   ```

   * Dove `yourclientcode` è il codice client dell’azienda. Il codice cliente della tua azienda è tutto minuscolo e non ha caratteri speciali.

      * **at.js**: il tuo codice cliente è disponibile nella parte superiore della pagina [!UICONTROL Configurazione > Implementazione > Modifica impostazioni at.js] nell’interfaccia di [!DNL Target].

      * **mbox.js**: il tuo codice cliente è disponibile nella parte superiore della pagina [!UICONTROL Configurazione > Implementazione > Modifica impostazioni mbox.js].
   * `redirectorlink_456` è il nome dell’elemento mbox redirector che appare nel tuo account, da utilizzare nelle campagne e nei test.

      I redirector operano in modo diverso rispetto agli altri elementi mbox, ma appaiono nel tuo account come qualsiasi altro mbox. Dai un nome al redirector in modo da poterlo distinguere facilmente dagli elementi mbox standard nel tuo account.  È buona norma iniziare il nome mbox con &quot;redirectorlink&quot;.

   * Dove `http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2Fusualdestination%2Ehtm` è la destinazione predefinita.

      Deve essere codificata in URL e deve essere un riferimento assoluto. You can use the [HTML URL Encoding Reference](https://www.w3schools.com/tags/ref_urlencode.asp) to quickly encodes your URLs.

      >[!IMPORTANT]
      >
      >Si noti che con Redirector è possibile essere esposti al rischio di una vulnerabilità di reindirizzamento aperto. Per evitare l&#39;uso non autorizzato di collegamenti Redirector da parte di terzi, si consiglia di utilizzare &quot;host autorizzati&quot; per inserire nella whitelist i domini URL di reindirizzamento predefiniti. In Target gli host vengono utilizzati per inserire nella whitelist i domini ai quali si desidera consentire i reindirizzamenti. Per ulteriori informazioni, consultate [Creare whitelist che specificano gli ospitanti autorizzati a inviare chiamate mbox a Target](/help/administrating-target/hosts.md#whitelist) in *ospitanti*.


1. Convalida il Redirector.
   1. *Best practice* di protezione: Assicurarsi che il dominio utilizzato nel redirector sia inserito nella white list, come indicato sopra. Se utilizzi un dominio non inserito nella white list, Adobe bloccherà qualsiasi chiamata a tale dominio per impedire agli attori malintenzionati di utilizzare il redirector per reindirizzare a domini potenzialmente dannosi.
   1. Inserisci l&#39;URL del redirector in un browser e aggiornalo.
   1. Accedi all&#39;account, aggiorna l’elenco di mbox e verifica che il nuovo redirector sia presente nell&#39;elenco come una mbox.
1. Se esegui il test di destinazioni diverse per un annuncio, crea [offerte di reindirizzamento](../../c-experiences/c-visual-experience-composer/redirect-offer.md#task_9578678D42784F5EB9638F8AC8C911FA) per ogni versione.
1. Creare la campagna.

   Consulta [Implementazioni non basate su JavaScript](../../c-implementing-target/c-non-javascript-based-implementation/non-javascript-based-implementation.md#concept_4799C58B081A43F6B3B8CC25A8D5D7C4) per l’installazione che permette di raggiungere gli obbiettivi.
1. Controllo qualità completo sulla campagna.

   Crea una pagina fittizia con un tag `<a href>` contenente l’URL del redirector. Esempio:

   ```
   <a href=https://<your_clientcode>.tt.omtrdc.net/​m2/yourclientcode/ubox/​page?mbox=
   
   redirectorlink_456&mboxDefault=http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2F​usualdestination%2Ehtm>
   ```

1. Verifica che tutte le esperienze, il contenuto predefinito e i rapporti agiscano come previsto su tutti i tipi di browser, per tutti gli ambienti.

   >[!NOTE] {class=“- topic/note ”}
   >
   >* I redirector non sono supportati dalla funzione Offerta anteprima o Sfoglia per mbox. Guarda in anteprima le esperienze direttamente in un browser.
   >* `mboxDebug` non funziona con i redirector.


1. Invia l&#39;URL completo del redirector alla tua rete di visualizzazione annunci come destinazione dell&#39;annuncio.

## Use a redirector to pass Costs per Click and Revenue Per Click {#concept_3078EF48E9C44B34992D62AAB9628853}

Informazioni su come utilizzare un redirector per trasmettere costi per clic e ricavi per clic.

### Trasmissione dei costi per clic {#section_DEB889470F7D4360B5CEA85FD05DEDFA}

Puoi utilizzare un redirector per trasmettere i costi per clic.

>[!NOTE]
>
>La best practice consiste nel determinare il valore del costo utilizzando la metrica di coinvolgimento **Valutazione per visita** .

Aggiungi `&mboxPageValue=-value` all’URL. Nota il valore negativo.

Esempio: per un costo di 0,10 centesimi per clic:

```
https://<your_clientcode>.tt.omtrdc.net/​m2/yourclientcode/ubox/​page?mbox=redirectorlink_456
&mboxPageValue=-0.1&mboxDefault=​https://www.yourcompany.com/usualdestination.htm
```

### Trasmissione dei ricavi per clic {#section_3E48AC465E7D42DAAC51B4BFF83F64B1}

Per utilizzare un redirector per trasmettere i ricavi per clic.

>[!NOTE]
>
>La best practice consiste nel determinare il valore delle entrate utilizzando la metrica di coinvolgimento **Valutazione per visita** .

Aggiungi `&mboxPageValue=value` all’URL.

Esempio: per un ricavo di 0,10 centesimi per clic.

```
https://<​your_clientcode>​​​​.tt​​.omtrdc​.net/​​m2/​yourclientcode/​ubox/​​​page?mbox=redirectorlink_456
&mboxPageValue=0.1​&mbox​Default=​​http%3A%2F%2Fwww%2E​yourcompany%2Ecom​%2Fusualdestination%2Ehtm
```
