---
keywords: client care;cname;certificate program;canonical name;cookies;certificate;amc;adobe managed certificate;digicert;domain control validation;dcv
description: Informazioni sull’utilizzo di Adobe Client Care per implementare il supporto CNAME (Canonical Name) in Adobe Target.
title: CNAME e Adobe Target
feature: privacy and security
translation-type: tm+mt
source-git-commit: 677d5ed16377fc32b4506ca736084319e5643e67
workflow-type: tm+mt
source-wordcount: '1210'
ht-degree: 3%

---


# CNAME e Adobe Target {#cname-and-adobe-target}

Istruzioni per l&#39;uso con  Client Care di Adobe per implementare il supporto CNAME (Nome canonico) in [!DNL Adobe Target]. Per gestire al meglio i problemi di blocco degli annunci o i criteri dei cookie relativi a ITP, viene utilizzato un CNAME per cui le chiamate vengono effettuate a un dominio di proprietà del cliente anziché a un dominio di proprietà  Adobe.

## Richiedi supporto CNAME

Esegui la procedura seguente per richiedere il supporto CNAME in [!DNL Target]:

1. Determinate l’elenco dei nomi host necessari per il certificato SSL (consultate le domande frequenti).

1. Per ogni nome host, crea un record CNAME nel DNS indicando il normale [!DNL Target] nome host `clientcode.tt.omtrdc.net`.

   Ad esempio, se il codice client è &quot;nomecustomer&quot; e il nome host proposto è `target.example.com`, il record CNAME DNS deve essere simile al seguente:

   ```
   target.example.com.  IN  CNAME  cnamecustomer.tt.omtrdc.net.
   ```

   >[!NOTE]
   >
   > Adobe  autorità di certificazione DigiCert non può rilasciare un certificato finché il passaggio non viene completato. Pertanto,  Adobe non può soddisfare la richiesta di implementazione CNAME fino al completamento di questo passaggio.

1. [Compila questo ](https://experienceleague.adobe.com/docs/core-services/assets/FPC_Request_Form.xlsx?lang=en) modulo e includilo quando  [apri un ticket Client Care  Adobe che richiede il supporto](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) CNAME:

   *  codice client [!DNL Target] Adobe:
   * Nomi host del certificato SSL (esempio: `target.example.com target.example.org`):
   * Acquirente certificato SSL ( Adobe è altamente consigliato, consultare le domande frequenti: Adobe/cliente 
   * Se il cliente sta acquistando il certificato (alias BYOC), compilare i seguenti dettagli aggiuntivi:
      * Organizzazione dei certificati (esempio: Esempio Azienda Inc):
      * Unità organizzativa certificato (facoltativo, esempio: Marketing):
      * Paese del certificato (esempio: US):
      * Stato/regione del certificato (esempio: California):
      * Città certificato (esempio: San Jose):

1. Se  Adobe sta acquistando il certificato,  Adobe collaborerà con DigiCert per acquistare e distribuire il certificato  Adobe server di produzione .

   Se il cliente sta acquistando il certificato (BYOC),  Client Care di Adobe vi invierà la richiesta di firma del certificato (CSR), che dovrete utilizzare per acquistare il certificato tramite la vostra autorità di certificazione. Dopo il rilascio del certificato, è necessario inviare una copia del certificato ed eventuali certificati intermedi a  Client Care Adobe per la distribuzione.

    Client Care di Adobe ti avviserà quando sarà pronta l&#39;implementazione.

1. Dopo aver completato le attività precedenti e  Adobe Client Care ha notificato che l&#39;implementazione è pronta, devi aggiornare `serverDomain` al nuovo CNAME in at.js.

## Domande frequenti 

Le seguenti informazioni rispondono alle domande frequenti su come richiedere e implementare il supporto CNAME in [!DNL Target]:

### Posso fornire il mio certificato personale (ovvero portare il tuo certificato personale o BYOC)?

Sì, è possibile fornire il proprio certificato; tuttavia, non è consigliato. La gestione del ciclo di vita del certificato SSL è notevolmente più semplice sia per  Adobe che per l’utente quando  Adobe acquista e controlla il certificato. I certificati SSL devono essere rinnovati ogni anno, il che significa che  Client Care di Adobe deve contattarvi ogni anno per inviare  Adobe un nuovo certificato in modo tempestivo. Alcuni clienti potrebbero avere difficoltà a produrre un certificato rinnovato in modo tempestivo ogni anno, il che compromette la loro [!DNL Target] implementazione perché i browser rifiuteranno le connessioni alla scadenza del certificato.

>[!IMPORTANT]
>
>Se richiedi un&#39;implementazione CNAME [!DNL Target] completa il tuo certificato, devi fornire certificati rinnovati a  Adobe Client Care ogni anno. Consentendo al certificato CNAME di scadere prima che  Adobe possa distribuire un certificato rinnovato, si verificherà un&#39;interruzione dell&#39;implementazione [!DNL Target] specifica.

### Fino a quando scade il mio nuovo certificato SSL?

I certificati rilasciati prima del 1° settembre 2020 saranno certificati biennali. I certificati rilasciati a partire dal 1° settembre 2020 saranno certificati annuali. Per ulteriori informazioni sul passaggio ai certificati a un anno, vedere [qui](https://www.digicert.com/position-on-1-year-certificates).

### Quali nomi host scegliere? Quanti nomi host per dominio devo scegliere?

[!DNL Target] Le implementazioni CNAME richiedono un solo nome host per dominio nel certificato SSL e nel DNS del cliente, per questo è consigliabile. Alcuni clienti potrebbero richiedere nomi host aggiuntivi per dominio per i propri scopi (ad esempio, test in fase di pre-produzione), che è supportato.

La maggior parte dei clienti sceglie un nome host come `target.example.com`, quindi è quello che consigliamo, ma la scelta è in definitiva tutta tua. Assicurarsi di non richiedere un nome host di un record DNS esistente in quanto ciò causerebbe un conflitto e un ritardo nella risoluzione della richiesta CNAME [!DNL Target].

### Ho già implementato un CNAME per [!DNL Adobe Analytics], possiamo utilizzare lo stesso certificato o nome host?

No, [!DNL Target] richiede un nome host e un certificato separati.

### L&#39;implementazione corrente di Target viene influenzata da ITP 2.x?

In un browser Safari, accedete al sito Web in cui è presente una libreria JavaScript di Target. Se viene visualizzato un cookie di Target impostato nel contesto di un CNAME, ad esempio `analytics.company.com`, ITP 2.x non ha effetto.

I problemi ITP possono essere risolti per Target con un CNAME Analytics. Avrete bisogno di un CNAME Target separato solo per gli scenari di blocco degli annunci in cui Target viene bloccato.

Per ulteriori informazioni sull&#39;ITP, vedere [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).

### Che tipo di interruzione del servizio posso aspettarmi quando viene implementata l’implementazione CNAME?

Non si verifica alcuna interruzione del servizio quando il certificato viene distribuito (compresi i rinnovi di certificati). Tuttavia, quando si modifica il nome host nel codice di implementazione [!DNL Target] (`serverDomain` in at.js) nel nuovo nome host CNAME (`target.example.com`), i browser Web tratteranno i visitatori di ritorno come nuovi visitatori e i loro dati di profilo andranno persi perché il cookie precedente non sarà accessibile sotto il nome host precedente (`clientcode.tt.omtrdc.net`) a causa dei modelli di protezione del browser. Si tratta di un’interruzione una tantum solo per il cut-over iniziale del nuovo CNAME. I rinnovi di certificati non hanno lo stesso effetto in quanto il nome host non viene modificato.

### Che tipo di chiave e algoritmo di firma certificato verranno utilizzati per l&#39;implementazione CNAME?

Tutti i certificati sono RSA SHA-256 e le chiavi sono RSA a 2048 bit, per impostazione predefinita. Le dimensioni chiave superiori a 2048 bit non sono attualmente supportate.

### Come posso convalidare la mia implementazione CNAME è pronta per il traffico?

Utilizzate il seguente set di comandi (nel terminale della riga di comando MacOs o Linux, utilizzando bash e curl 7.49+):

1. Incollare prima questa funzione bash nel terminale:

   ```
   function validateEdgeFpsslSni {
       domain=$1
       for edge in mboxedge{31,32,{34..38}}.tt.omtrdc.net; do
           echo "$edge: $(curl -sSv --connect-to $domain:443:$edge:443 https://$domain 2>&1 | grep subject:)"
       done
   }
   ```

1. Incollate quindi questo comando (sostituendo `target.example.com` con il nome host):

   ```
   validateEdgeFpsslSni target.example.com
   ```

   Se l&#39;implementazione è pronta, dovresti vedere l&#39;output come di seguito. La parte importante è che tutte le righe mostrano `CN=target.example.com`, che corrisponde al nostro nome host desiderato. Se uno di essi mostra `CN=*.tt.omtrdc.net`, l&#39;implementazione è **not** pronta.

   ```
   $ validateEdgeFpsslSni target.example.com
   mboxedge31.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge32.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge34.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge35.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge36.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge37.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge38.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   ```

1. Convalidate il nuovo CNAME DNS con un&#39;altra richiesta curl, che dovrebbe mostrare anche `CN=target.example.com`:

   ```
   curl -sSv https://target.example.com 2>&1 | grep subject:
   ```

   >[!NOTE]
   >
   >Se questo comando ha esito negativo ma il comando `validateEdgeFpsslSni` precedente ha esito positivo, potrebbe essere necessario attendere la propagazione completa degli aggiornamenti DNS. Ai record DNS è associato un [TTL (time-to-live)](https://en.wikipedia.org/wiki/Time_to_live#DNS_records) che specifica il tempo di scadenza della cache per le risposte DNS di tali record, pertanto potrebbe essere necessario attendere almeno fino a quando i TTL non saranno disponibili. È possibile utilizzare il comando `dig target.example.com` o [G Suite Toolbox](https://toolbox.googleapps.com/apps/dig/#CNAME) per ricercare specifici TTL.

## Limitazioni note

* La modalità QA non sarà fissa se hai CNAME e at.js 1.x perché è basata su un cookie di terze parti. La soluzione alternativa consiste nell’aggiungere i parametri di anteprima a ciascun URL a cui ci si sposta. La modalità QA è fissa quando si dispone di CNAME e a.js 2.x.
* Attualmente l&#39;impostazione `overrideMboxEdgeServer` non funziona correttamente con CNAME quando si utilizzano versioni at.js precedenti a at.js 1.8.2 e a.js 2.3.1. Se utilizzi una versione precedente di at.js, devi impostarla come `false` per evitare richieste non riuscite. In alternativa, è consigliabile aggiornare [at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) a una versione supportata più recente.
* Quando si utilizza CNAME, è più probabile che la dimensione dell&#39;intestazione del cookie per le chiamate a Target aumenti. Consigliamo di mantenere la dimensione del cookie sotto gli 8 KB.
