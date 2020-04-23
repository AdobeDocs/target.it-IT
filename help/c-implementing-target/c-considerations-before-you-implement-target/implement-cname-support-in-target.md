---
keywords: client care;cname;certificate program;canonical name;cookies;certificate;amc;adobe managed certificate;digicert;domain control validation;dcv
description: Informazioni sull’utilizzo di Adobe Client Care per implementare il supporto CNAME (Canonical Name) in Adobe Target.
title: CNAME e Adobe Target
topic: Standard
uuid: 3fb0ea31-e91d-4359-a8cc-64c547e6314e
translation-type: tm+mt
source-git-commit: 113a48f2f06730d637049538cf617f386d9ba4bd

---


# CNAME e Adobe Target {#cname-and-adobe-target}

Instructions for working with Adobe Client Care to implement CNAME (Canonical Name) support in [!DNL Adobe Target]. Per gestire al meglio i problemi di blocco degli annunci o i criteri dei cookie relativi a ITP, viene utilizzato un CNAME per cui le chiamate vengono effettuate a un dominio di proprietà del cliente anziché a un dominio di proprietà di Adobe.

## Richiedi supporto CNAME

Esegui la procedura seguente per richiedere il supporto CNAME in [!DNL Target]:

1. L&#39;autorità di certificazione di Adobe (DigiCert) deve verificare che Adobe sia autorizzato a generare certificati all&#39;interno del tuo dominio.

   DigiCert chiama questo processo DCV ( [Domain Control Validation)](https://docs.digicert.com/manage-certificates/dv-certificate-enrollment/domain-control-validation-dcv-methods/)e Adobe non sarà autorizzato a generare un certificato nel dominio fino al completamento di questo processo per almeno uno dei seguenti metodi DCV:

   * Il metodo DCV più rapido è il metodo CNAME DNS, in cui si aggiunge un record CNAME DNS (contenente un token) al dominio che punta al nome host DCV di DigiCert (`dcv.digicert.com`). Questo record CNAME indica a DigiCert che Adobe è autorizzato a generare il certificato. Adobe Client Care invierà le istruzioni insieme ai record DNS necessari. Esempio:

      ```
      3b0332e02daabf31651a5a0d81ba830a.target.example.com.  IN  CNAME  dcv.digicert.com.
      ```

      >[!NOTE]
      >
      >* Questi token DCV scadono dopo 30 giorni, dopodiché Adobe Client Care ti contatterà con i token aggiornati. Per la risoluzione più rapida della richiesta CNAME, preparatevi a effettuare queste modifiche DNS su tutti i domini richiesti prima di inviare la richiesta.
         >
         >
      * Se il dominio dispone di record [CAA](https://en.wikipedia.org/wiki/DNS_Certification_Authority_Authorization)DNS, è necessario aggiungere `digicert.com` se non è già stato aggiunto. Questo record DNS indica quali autorità di certificazione sono autorizzate a rilasciare certificati per il dominio. Il record DNS risultante sarà simile al seguente: `example.com. IN CAA 0 issue "digicert.com"`. È possibile utilizzare [la Casella degli strumenti](https://toolbox.googleapps.com/apps/dig/#CAA) di G Suite per determinare se il dominio principale dispone di un record CAA esistente. Per ulteriori informazioni sulla gestione dei record CAA da parte di DigiCert, [consultate](https://docs.digicert.com/manage-certificates/dns-caa-resource-record-check).


   * DigiCert prova anche il metodo email, in cui invia messaggi e-mail agli indirizzi trovati nelle informazioni WHOIS del dominio e agli indirizzi e-mail predeterminati (amministratore, amministratore, webmaster, hostmaster e postmaster `@[domain_name]`). See the [DCV methods documentation](https://docs.digicert.com/manage-certificates/dv-certificate-enrollment/domain-control-validation-dcv-methods/) for more information.

      Per accelerare il processo di e-mail DCV, DigiCert fornisce la seguente raccomandazione:

      &quot;Verificare che il provider di registrazione/WHOIS non abbia mascherato o rimosso gli indirizzi [e-mail]pertinenti. In caso affermativo, scoprite se forniscono un modo (ad es. un indirizzo e-mail anonimo, un modulo Web) per consentire alle autorità [di] certificazione di accedere ai dati WHOIS del vostro dominio.&quot;

1. Crea un record CNAME nel DNS del dominio indicando il tuo nome host normale `clientcode.tt.omtrdc.net`. Ad esempio, se il codice client è un cliente e il nome host proposto è `target.example.com`, il record CNAME DNS deve essere simile al seguente:

   ```
   target.example.com.  IN  CNAME  cnamecustomer.tt.omtrdc.net.
   ```

1. Apri un ticket [Adobe Client Care che richiede il supporto](https://docs.adobe.com/content/help/en/target/using/cmp-resources-and-contact-information.html#reference_ACA3391A00EF467B87930A450050077C) CNAME per le tue [!DNL Target] chiamate.

   Adobe collaborerà con DigiCert per acquistare e distribuire il certificato sui server di produzione Adobe. DigiCert avvia il processo DCV e Adobe Client Care ti avviserà quando la tua implementazione sarà pronta.

1. Dopo aver completato le attività precedenti e dopo che Adobe Client Care ha notificato che l&#39;implementazione è pronta, devi aggiornare il CNAME `serverDomain` al nuovo CNAME in at.js.

## Domande frequenti 

Le seguenti informazioni rispondono alle domande frequenti su come richiedere e implementare il supporto CNAME in [!DNL Target]:

### Posso fornire il mio certificato personale (ovvero portare il tuo certificato personale o BYOC)? In caso affermativo, qual è il processo?

Sì, è possibile fornire il proprio certificato; tuttavia, non è consigliato. La gestione del ciclo di vita del certificato SSL è notevolmente più semplice sia per Adobe che per gli utenti quando Adobe acquista e controlla il certificato. I certificati SSL devono essere rinnovati ogni anno, il che significa che Adobe Client Care deve contattarvi ogni anno per inviare un nuovo certificato ad Adobe in tempo utile. Alcuni clienti potrebbero avere difficoltà a produrre un certificato rinnovato in modo tempestivo ogni anno, il che compromette la loro [!DNL Target] implementazione perché i browser rifiuteranno le connessioni alla scadenza del certificato.

>[!IMPORTANT]
>
>Se richiedi un’implementazione CNAME [!DNL Target] con certificato personale, devi fornire ogni anno certificati rinnovati ad Adobe Client Care. Consentendo al certificato CNAME di scadere prima che Adobe possa distribuire un certificato rinnovato, si verificherà un&#39;interruzione dell&#39; [!DNL Target] implementazione specifica.

1. Saltate il punto 1, ma completate i punti 2 e 3. Quando aprite un ticket Adobe Client Care (passaggio 3), informateli che state fornendo il vostro certificato.

   Adobe genererà e invierà una richiesta di firma del certificato (CSR).

1. Utilizzate il CSR per acquistare il certificato tramite l&#39;autorità di certificazione scelta.

1. Inviate il nuovo certificato pubblico ad Adobe. I rappresentanti Adobe distribuiranno il certificato pubblico sui propri server di produzione.

1. Completa il passaggio 4 dopo che Adobe Client Care ha notificato che l&#39;implementazione è pronta.

### Fino a quando scade il mio nuovo certificato SSL?

I certificati rilasciati prima del 1° settembre 2020 saranno certificati biennali. I certificati rilasciati a partire dal 1° settembre 2020 saranno certificati annuali. Per ulteriori informazioni sul passaggio ai certificati a un anno, consultate [questo](https://www.digicert.com/position-on-1-year-certificates)articolo.

### Quali nomi host scegliere? Quanti nomi host per dominio devo scegliere?

[!DNL Target] Le implementazioni CNAME richiedono un solo nome host per dominio nel certificato SSL e nel DNS del cliente, per questo è consigliabile. Alcuni clienti potrebbero richiedere nomi host aggiuntivi per dominio per i propri scopi (ad esempio, test in fase di pre-produzione), che è supportato.

La maggior parte dei clienti scelgono un nome host come `target.example.com`, quindi questo è quello che consigliamo, ma la scelta è in definitiva vostra. Accertatevi di non richiedere un nome host di un record DNS esistente in quanto ciò causerebbe un conflitto e un ritardo nella risoluzione della richiesta [!DNL Target] CNAME.

### Ho già implementato un CNAME per [!DNL Adobe Analytics], possiamo usare lo stesso certificato o nome host?

No, [!DNL Target] richiede un nome host e un certificato separati.

### L&#39;implementazione corrente di Target viene influenzata da ITP 2.1 o 2.2?

In un browser Safari, accedete al sito Web in cui è presente una libreria JavaScript di Target. If you see a Target cookie set in the context of a CNAME, such as `analytics.company.com`, then you are not impacted by ITP 2.1 or 2.2.

I problemi ITP possono essere risolti per Target con un CNAME Analytics. Avrete bisogno di un CNAME Target separato solo per gli scenari di blocco degli annunci in cui Target viene bloccato.

Per ulteriori informazioni sull&#39;ITP, vedere [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).

### Adobe/DigiCert può inviare le e-mail DCV a un altro indirizzo `<someone>@example.com`?

No, DigiCert (o qualsiasi autorità di certificazione) non permetterà a chiunque abbia un indirizzo e-mail in un dominio di autorizzare un certificato SSL nello stesso dominio a meno che tale indirizzo e-mail non sia incluso anche nelle informazioni WHOIS del dominio o nell&#39;elenco di indirizzi prestabiliti (vedi sopra). In questo modo solo gli utenti autorizzati possono approvare il DCV per un determinato dominio. Se non è possibile, si consiglia di utilizzare il metodo DCV CNAME DNS (vedi sopra).

### Come posso convalidare la mia implementazione CNAME è pronta per il traffico?

Utilizzate il seguente set di comandi (nel terminale della riga di comando MacOs o Linux, utilizzando bash e curl 7.49+):

1. Incollare prima questa funzione bash nel terminale:

   ```
   function validateEdgeFpsslSni {
       domain=$1
       for edge in mboxedge{17,21,22,26,{28..32},34,35,37,38}.tt.omtrdc.net; do
           echo "$edge: $(curl -sSv --connect-to $domain:443:$edge:443 https://$domain 2>&1 | grep subject:)"
       done
   }
   ```

1. Incollate quindi questo comando (sostituendo `target.example.com` con il vostro nome host):

   ```
   validateEdgeFpsslSni target.example.com
   ```

   Se l&#39;implementazione è pronta, dovresti vedere l&#39;output come di seguito. La parte importante è che tutte le righe mostrano `CN=target.example.com`, che corrisponde al nostro nome host desiderato. Se ne viene mostrato uno `CN=*.tt.omtrdc.net`, l&#39;implementazione **non** è pronta.

   ```
   $ validateEdgeFpsslSni target.example.com
   mboxedge17.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge21.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge22.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge26.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge28.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge29.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge30.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge31.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge32.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge34.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge35.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge37.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge38.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   ```

1. Convalida il nuovo CNAME DNS con un&#39;altra richiesta curl, che dovrebbe mostrare anche `CN=target.example.com`:

   ```
   curl -sSv https://target.example.com 2>&1 | grep subject:
   ```

   >[!NOTE]
   >
   >Se questo comando ha esito negativo ma il `validateEdgeFpsslSni` comando precedente ha esito positivo, potrebbe essere necessario attendere la propagazione completa degli aggiornamenti DNS. Ai record DNS è associato un [TTL (time-to-live)](https://en.wikipedia.org/wiki/Time_to_live#DNS_records) che specifica il tempo di scadenza della cache per le risposte DNS di tali record, pertanto potrebbe essere necessario attendere almeno fino a quando i TTL non saranno disponibili. È possibile utilizzare il `dig target.example.com` comando o [la Casella degli strumenti](https://toolbox.googleapps.com/apps/dig/#CNAME) di G Suite per cercare i TTL specifici.
