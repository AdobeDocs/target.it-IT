---
description: È possibile utilizzare un redirector in modo simile a come si utilizza una mbox nei test.
keywords: Implementazione;mbox.js non JavaScript;redirector;costi per clic; ricavi per clic
seo-description: È possibile utilizzare un redirector in modo simile a come si utilizza una mbox nei test.
seo-title: Lavorare con i redirector
solution: Target
subtopic: Introduzione
title: Lavorare con i redirector
topic: Standard
uuid: 79d7caf6-5693-4bb3-9131-8d1ae420fa5e
translation-type: tm+mt
source-git-commit: ece87434c94501eeed1d6af9cb2a92f8585775b7

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

Per decidere la giusta configurazione, consulta  [Implementazioni non basate su JavaScript](../../c-implementing-target/c-non-javascript-based-implementation/non-javascript-based-implementation.md#concept_4799C58B081A43F6B3B8CC25A8D5D7C4).

## Creare un redirector {#task_76608B0F73FC45C4A9F125B894DCF821}

Prima di poter utilizzare un redirector, è necessario crearlo.

1. Determina le varianti di destinazione dell&#39;annuncio, inclusa la destinazione predefinita.
1. Crea l&#39;URL di redirector.

   ```
   https://<your_testandtarget_clientcode>.tt.omtrdc.net/​m2/yourclientcode/ubox
   /​page?mbox=redirectorlink_456
   &mboxDefault=http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2Fusualdestination%2Ehtm
   ```

   * Dove `yourclientcode` si trova il codice client della tua azienda. Il codice cliente della tua azienda è tutto minuscolo e non ha caratteri speciali.

      * **at.js**: il tuo codice cliente è disponibile nella parte superiore della pagina [!UICONTROL Configurazione &gt; Implementazione &gt; Modifica impostazioni at.js] nell’interfaccia di [!DNL Target].

      * **mbox.js**: il tuo codice cliente è disponibile nella parte superiore della pagina [!UICONTROL Configurazione &gt; Implementazione &gt; Modifica impostazioni mbox.js].
   * `redirectorlink_456` è il nome della mbox Redirector che viene visualizzata nel vostro account da utilizzare in campagne e test.

      I redirector operano in modo diverso rispetto agli altri elementi mbox, ma appaiono nel tuo account come qualsiasi altro mbox. Dai un nome al redirector in modo da poterlo distinguere facilmente dagli elementi mbox standard nel tuo account.  È buona norma iniziare il nome mbox con &quot;redirectorlink&quot;.

   * Dove `http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2Fusualdestination%2Ehtm` si trova la destinazione predefinita.

      Deve essere codificata in URL e deve essere un riferimento assoluto. Potete usare il [riferimento di codifica URL HTML](https://www.w3schools.com/tags/ref_urlencode.asp) per codificare rapidamente gli URL. |



1. Convalida il Redirector.
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

## Utilizzare un Redirector per trasmettere i costi per clic e i ricavi per clic {#concept_3078EF48E9C44B34992D62AAB9628853}

Informazioni su come utilizzare un redirector per trasmettere costi per clic e ricavi per clic.

### Trasmissione dei costi per clic {#section_DEB889470F7D4360B5CEA85FD05DEDFA}

Puoi utilizzare un redirector per trasmettere i costi per clic.

>[!NOTE]
>
>Si consiglia di determinare il valore costi utilizzando **la metrica Punteggio per visita,** come descritto in [Partecipazione](https://marketing.adobe.com/resources/help/en_US/tnt/help/c_Capturing_Engagement.html).

Aggiungi `&mboxPageValue=-value` all’URL. Nota il valore negativo.

Esempio: per un costo di 0,10 centesimi per clic:

```
https://<your_clientcode>.tt.omtrdc.net/​m2/yourclientcode/ubox/​page?mbox=redirectorlink_456
&mboxPageValue=-0.1&mboxDefault=​https://www.yourcompany.com/usualdestination.htm
```

### Trasmissione dei ricavi per clic  {#section_3E48AC465E7D42DAAC51B4BFF83F64B1}

Per utilizzare un redirector per trasmettere i ricavi per clic.

>[!NOTE]
>
>La best practice è determinare il valore delle entrate utilizzando **la metrica Punteggio per visita,** come descritto in [Partecipazione](https://marketing.adobe.com/resources/help/en_US/tnt/help/c_Capturing_Engagement.html).

Aggiungi `&mboxPageValue=value` all’URL.

Esempio: per un ricavo di 0,10 centesimi per clic.

```
https://<​your_clientcode>​​​​.tt​​.omtrdc​.net/​​m2/​yourclientcode/​ubox/​​​page?mbox=redirectorlink_456
&mboxPageValue=0.1​&mbox​Default=​​http%3A%2F%2Fwww%2E​yourcompany%2Ecom​%2Fusualdestination%2Ehtm
```
