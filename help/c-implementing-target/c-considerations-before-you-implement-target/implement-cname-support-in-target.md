---
keywords: client care;cname;certificate program;canonic name;cookies;certificate;amc;adobe manage certificate;digicert;domain control validation;dcv
description: Informazioni sull’utilizzo di Adobe Client Care per implementare il supporto CNAME (Canonical Name) in Adobe Target.
title: CNAME e Adobe Target
topic: Standard
uuid: 3fb0ea31-e91d-4359-a8cc-64c547e6314e
translation-type: tm+mt
source-git-commit: 117e4c8712d49a284331552268cec42bb34cf013

---


# CNAME e Adobe Target {#cname-and-adobe-target}

Instructions about working with Adobe Client Care to implement CNAME (Canonical Name) support in [!DNL Adobe Target]. Per gestire al meglio i problemi di blocco degli annunci o i criteri dei cookie relativi a ITP, viene utilizzato un CNAME per cui le chiamate vengono effettuate a un dominio di proprietà del cliente anziché a un dominio di proprietà di Adobe.

## Richiedi supporto CNAME

Esegui la procedura seguente per richiedere il supporto CNAME in [!DNL Target]:

1. L'autorità di certificazione di Adobe (DigiCert) deve verificare che Adobe sia autorizzato a generare certificati all'interno del tuo dominio.

   DigiCert chiama questo processo DCV ( [Domain Control Validation](https://docs.digicert.com/manage-certificates/dv-certificate-enrollment/domain-control-validation-dcv-methods/) ) e Adobe non potrà generare un certificato nel dominio fino al completamento del processo.

   DCV utilizza alcuni metodi e alcune operazioni possono essere eseguite prima di aprire un ticket Adobe Client Care (passaggio 3) per accelerare il processo DCV:

   * DigiCert proverà innanzitutto il metodo email, in cui inviano e-mail agli indirizzi che si trovano nelle informazioni WHOIS del dominio così come indirizzi e-mail predeterminati (amministratore, amministratore, webmaster, hostmaster e postmaster `@[domain_name]`). See the [DCV methods documentation](https://docs.digicert.com/manage-certificates/dv-certificate-enrollment/domain-control-validation-dcv-methods/) for more information.

      Per accelerare il processo di e-mail DCV, DigiCert fornisce la seguente raccomandazione:

      "Verificare che il provider di registrazione/WHOIS non abbia mascherato o rimosso gli indirizzi [e-mail]pertinenti. In caso affermativo, scoprite se forniscono un modo (ad es. un indirizzo e-mail anonimo, un modulo Web) per consentire alle autorità [di] certificazione di accedere ai dati WHOIS del vostro dominio."

   * Se il metodo e-mail DCV non è un'opzione, il metodo successivo è il metodo TXT DNS, in cui si aggiunge un record TXT DNS al dominio con un valore hash. Questo record TXT indica a DigiCert che Adobe è autorizzato a generare il certificato. Se devi usare questo metodo, fai sapere ad Adobe Client Care quando apri un ticket (passaggio 3). In questo modo sarà possibile accelerare il processo DCV.

1. Crea un record CNAME nel DNS del dominio indicando il tuo nome host normale `clientcode.tt.omtrdc.net`. Ad esempio, se il codice client è un cliente e il nome host proposto è `target.example.com`, il record CNAME DNS deve essere simile al seguente:

   ```
   target.example.com  IN  CNAME  cnamecustomer.tt.omtrdc.net.
   ```

1. Apri un ticket [Adobe Client Care che richiede il supporto](https://docs.adobe.com/content/help/en/target/using/cmp-resources-and-contact-information.html#reference_ACA3391A00EF467B87930A450050077C) CNAME per le tue [!DNL Target] chiamate.

   Adobe collaborerà con DigiCert per acquistare e distribuire il certificato sui server di produzione Adobe. DigiCert avvia il processo DCV e Adobe Client Care ti avviserà quando la tua implementazione sarà pronta.

1. Dopo aver completato le attività precedenti e dopo che Adobe Client Care ha notificato che l'implementazione è pronta, devi aggiornare il CNAME `serverDomain` al nuovo CNAME in at.js.

## Domande frequenti

Le seguenti informazioni rispondono alle domande frequenti su come richiedere e implementare il supporto CNAM in [!DNL Target]:

### Posso fornire il mio certificato? In caso affermativo, qual è il processo?

Sì, puoi fornire il tuo certificato personale, per farlo:

1. Ignora il punto 1, ma completa i punti 2 e 3. Quando aprite un ticket Adobe Client Care (passaggio 3), informateli che state fornendo il vostro certificato.

   Adobe genererà e invierà una richiesta di firma del certificato (CSR).

1. Utilizzate il CSR per acquistare il certificato tramite l'autorità di certificazione scelta.

1. Inviate il nuovo certificato pubblico ad Adobe. I rappresentanti Adobe distribuiranno il certificato pubblico sui propri server di produzione.

1. Completa il passaggio 4 dopo che Adobe Client Care ha notificato che l'implementazione è pronta.

### Ho già implementato un CNAME per [!DNL Adobe Analytics], possiamo usare lo stesso certificato o nome host?

No, [!DNL Target] richiede un nome host e un certificato separati.

### Come posso convalidare la mia implementazione CNAME è pronta per il traffico?

Utilizzate il seguente set di comandi (nel terminale della riga di comando MacOs o Linux, utilizzando bash e curl 7.49+):

1. Incollare prima questa funzione bash nel terminale:

   ```
   function validateEdgeFpsslSni {
       domain=$1
       for edge in mboxedge{17,21,22,26,{28..33}}.tt.omtrdc.net; do
           echo "$edge: $(curl -sSv --connect-to $domain:443:$edge:443 https://$domain 2>&1 | grep subject:)"
       done
   }
   ```

1. Incollare quindi questo comando (sostituendo `target.example.com` con il nome host):

   ```
   validateEdgeFpsslSni target.example.com
   ```

   Se l'implementazione è pronta, dovresti vedere l'output come di seguito. La parte importante è che tutte le righe mostrano `CN=target.example.com`, che corrisponde al nostro nome host desiderato. Se ne viene mostrato uno `CN=*.tt.omtrdc.net`, l'implementazione **non** è pronta.

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
   mboxedge33.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   ```

1. Convalida il nuovo CNAME DNS con un'altra richiesta curl, che dovrebbe mostrare anche `CN=target.example.com`:

   ```
   curl -sSv https://target.example.com 2>&1 | grep subject:
   ```

   >[!NOTE]
   >
   >Se questo comando ha esito negativo ma il `validateEdgeFpsslSni` comando precedente ha esito positivo, potrebbe essere necessario attendere la propagazione completa degli aggiornamenti DNS.
