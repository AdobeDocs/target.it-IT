---
keywords: Implementazione;mbox.js non JavaScript;redirector;costi per clic; ricavi per clic
description: Scopri come utilizzare i redirector nelle implementazioni e-mail, in modo simile a come utilizzi una mbox nelle attività di Adobe [!DNL Target] .
title: Come si lavora con i redirector?
feature: Implementa e-mail
role: Developer
exl-id: 1e7b99e4-857b-4d0f-afbd-2c5ce6bf0557
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 66%

---

# Lavorare con i redirector

È possibile utilizzare un redirector in modo simile a come si utilizza una mbox nei test.

I redirector vengono creati con un URL redirector speciale che carica una mbox redirector (redirector) nel tuo account. Puoi utilizzare un redirector in modo simile a come si utilizza una mbox nei test. Invia l’URL del redirector al tuo Ad Network come collegamento di destinazione dell’annuncio.

Utilizza il redirector per eseguire le operazioni seguenti:

* Tenere traccia dei clic dagli annunci display al sito
* Creare un singolo rapporto centralizzato per tenere traccia dei clic e visualizzare gli annunci su più ad network
* Variare le destinazioni degli annunci display

   Ad esempio, lo stesso banner porta alla home page, alla pagina delle categorie e alla pagina di un prodotto.

* Trovare la pagina di destinazione che genera il maggior numero di conversioni

Per decidere la giusta configurazione, consulta [Implementazioni non basate su JavaScript](/help/c-implementing-target/c-non-javascript-based-implementation/non-javascript-based-implementation.md#concept_4799C58B081A43F6B3B8CC25A8D5D7C4).

## Creare un redirector {#redirector}

Prima di poter utilizzare un redirector, è necessario crearlo.

1. Determina le varianti di destinazione dell&#39;annuncio, inclusa la destinazione predefinita.
1. Crea l&#39;URL di redirector.

   ```
   https://<your_testandtarget_clientcode>.tt.omtrdc.net/​m2/yourclientcode/ubox
   /​page?mbox=redirectorlink_456
   &mboxDefault=http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2Fusualdestination%2Ehtm
   ```

   * Dove `yourclientcode` è il codice client dell’azienda. Il codice cliente della tua azienda è tutto minuscolo e non ha caratteri speciali.

      Il codice cliente è disponibile nella parte superiore della pagina [!UICONTROL Amministrazione > Implementazione] dell’ interfaccia [!DNL Target] .

   * `redirectorlink_456` è il nome dell’elemento mbox redirector che appare nel tuo account, da utilizzare nelle campagne e nei test.

      I redirector operano in modo diverso rispetto agli altri elementi mbox, ma appaiono nel tuo account come qualsiasi altro mbox. Dai un nome al redirector in modo da poterlo distinguere facilmente dagli elementi mbox standard nel tuo account.  È buona norma iniziare il nome mbox con &quot;redirectorlink&quot;.

   * Dove `http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2Fusualdestination%2Ehtm` è la destinazione predefinita.

      Deve essere codificata in URL e deve essere un riferimento assoluto. Puoi utilizzare il [riferimento HTML per la codifica degli URL](https://www.w3schools.com/tags/ref_urlencode.asp) per codificare rapidamente i tuoi URL.

      >[!IMPORTANT]
      >
      >Tieni presente che con Redirector puoi essere esposto a un rischio di vulnerabilità di reindirizzamento aperto. Per evitare l’uso non autorizzato di collegamenti redirector da parte di terze parti, si consiglia di utilizzare &quot;host autorizzati&quot; per inserire nell&#39;elenco Consentiti i domini URL di reindirizzamento predefiniti. Target utilizza gli host per inserire nell&#39;elenco Consentiti i domini a cui desideri consentire i reindirizzamenti. Per ulteriori informazioni, consulta [Creare Inseriti nell&#39;elenco Consentiti che specificano gli host autorizzati per l’invio di chiamate mbox a Target](/help/administrating-target/hosts.md#allowlist) in *Host*.

1. Convalida il Redirector.
   1. *Best practice* sulla sicurezza: Assicurati che il dominio utilizzato nel redirector sia inserito nell&#39;elenco Consentiti, come indicato sopra. Se utilizzi un dominio non inserito nell&#39;elenco Consentiti, Adobe bloccherà le chiamate a tale dominio per impedire agli attori dannosi di utilizzare il Redirector per reindirizzare a domini potenzialmente dannosi.
   1. Inserisci l&#39;URL del redirector in un browser e aggiornalo.
   1. Accedi all&#39;account, aggiorna l’elenco di mbox e verifica che il nuovo redirector sia presente nell&#39;elenco come una mbox.
1. Se esegui il test di destinazioni diverse per un annuncio, crea [offerte di reindirizzamento](/help/c-experiences/c-visual-experience-composer/redirect-offer.md#task_9578678D42784F5EB9638F8AC8C911FA) per ogni versione.
1. Creare la campagna.

   Consulta [Implementazioni non basate su JavaScript](/help/c-implementing-target/c-non-javascript-based-implementation/non-javascript-based-implementation.md#concept_4799C58B081A43F6B3B8CC25A8D5D7C4) per l’installazione che permette di raggiungere gli obbiettivi.
1. Controllo qualità completo sulla campagna.

   Crea una pagina fittizia con un tag `<a href>` contenente l’URL del redirector. Esempio:

   ```
   <a href=https://<your_clientcode>.tt.omtrdc.net/​m2/yourclientcode/ubox/​page?mbox=
   
   redirectorlink_456&mboxDefault=http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2F​usualdestination%2Ehtm>
   ```

1. Verifica che tutte le esperienze, il contenuto predefinito e i rapporti agiscano come previsto su tutti i tipi di browser, per tutti gli ambienti.

   >[!NOTE]
   >
   >* I redirector non sono supportati dalla funzione Offerta anteprima o Sfoglia per mbox. Guarda in anteprima le esperienze direttamente in un browser.
   >* `mboxDebug` non funziona con i redirector.


1. Invia l&#39;URL completo del redirector alla tua rete di visualizzazione annunci come destinazione dell&#39;annuncio.

## Utilizzare un redirector per trasmettere i costi per clic e i ricavi per clic {#concept_3078EF48E9C44B34992D62AAB9628853}

Informazioni su come utilizzare un redirector per trasmettere costi per clic e ricavi per clic.

### Trasmissione dei costi per clic {#section_DEB889470F7D4360B5CEA85FD05DEDFA}

Puoi utilizzare un redirector per trasmettere i costi per clic.

>[!NOTE]
>
>Si consiglia di determinare il valore del costo utilizzando la metrica di coinvolgimento **Punteggio per visita** .

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
>Si consiglia di determinare il valore dei ricavi utilizzando la metrica di coinvolgimento **Punteggio per visita** .

Aggiungi `&mboxPageValue=value` all’URL.

Esempio: per un ricavo di 0,10 centesimi per clic.

```
https://<​your_clientcode>​​​​.tt​​.omtrdc​.net/​​m2/​yourclientcode/​ubox/​​​page?mbox=redirectorlink_456
&mboxPageValue=0.1​&mbox​Default=​​http%3A%2F%2Fwww%2E​yourcompany%2Ecom​%2Fusualdestination%2Ehtm
```
