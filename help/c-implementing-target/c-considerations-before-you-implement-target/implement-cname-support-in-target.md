---
keywords: client care;cname;certificate program;canonical name;cookies;certificate;amc;adobe managed certificate;digicert;domain control validation;dcv
description: Informazioni sull’utilizzo di Adobe Client Care per implementare il supporto CNAME (Canonical Name) in Adobe Target.
title: CNAME e Adobe Target
feature: privacy and security
topic: Standard
uuid: 3fb0ea31-e91d-4359-a8cc-64c547e6314e
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '1183'
ht-degree: 3%

---


# CNAME e Adobe Target {#cname-and-adobe-target}

Instructions for working with Adobe Client Care to implement CNAME (Canonical Name) support in [!DNL Adobe Target]. Per gestire al meglio i problemi di blocco degli annunci o i criteri dei cookie relativi a ITP, viene utilizzato un CNAME per cui le chiamate vengono effettuate a un dominio di proprietà del cliente anziché a un dominio di proprietà  Adobe.

## Richiedi supporto CNAME

Esegui la procedura seguente per richiedere il supporto CNAME in [!DNL Target]:

1. Determinate l’elenco dei nomi host necessari per il certificato SSL (consultate le domande frequenti).

1. Per ciascun nome host, crea un record CNAME nel DNS indicando il [!DNL Target] nome host normale `clientcode.tt.omtrdc.net`.

   Ad esempio, se il codice client è &quot;nomecustomer&quot; e il nome host proposto è `target.example.com`, il record CNAME DNS deve essere simile al seguente:

   ```
   target.example.com.  IN  CNAME  cnamecustomer.tt.omtrdc.net.
   ```

   >[!NOTE]
   >
   >*  Adobe  autorità di certificazione DigiCert non può rilasciare un certificato finché il passaggio non viene completato. Pertanto,  Adobe non può soddisfare la richiesta di implementazione CNAME fino al completamento di questo passaggio.


1. [Compila questo modulo](https://docs.adobe.com/content/help/en/core-services/interface/ec-cookies/assets/FPC_Request_Form.xlsx) e includilo quando [apri un ticket Client Care  Adobe che richiede il supporto](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)CNAME:

   * Adobe [!DNL Target] client code:
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

1. Dopo aver completato le attività precedenti e  Client Care di Adobe ti ha notificato che l&#39;implementazione è pronta, devi aggiornare il CNAME `serverDomain` al nuovo CNAME in at.js.

## Domande frequenti 

Le seguenti informazioni rispondono alle domande frequenti su come richiedere e implementare il supporto CNAME in [!DNL Target]:

### Posso fornire il mio certificato personale (ovvero portare il tuo certificato personale o BYOC)?

Sì, è possibile fornire il proprio certificato; tuttavia, non è consigliato. La gestione del ciclo di vita del certificato SSL è notevolmente più semplice sia per  Adobe che per l’utente quando  Adobe acquista e controlla il certificato. I certificati SSL devono essere rinnovati ogni anno, il che significa che  Client Care di Adobe deve contattarvi ogni anno per inviare  Adobe un nuovo certificato in modo tempestivo. Alcuni clienti potrebbero avere difficoltà a produrre un certificato rinnovato in modo tempestivo ogni anno, il che compromette la loro [!DNL Target] implementazione perché i browser rifiuteranno le connessioni alla scadenza del certificato.

>[!IMPORTANT]
>
>Se richiedi un’implementazione CNAME [!DNL Target] con certificato personale, devi fornire certificati rinnovati a  Adobe Client Care ogni anno. Consentendo al certificato CNAME di scadere prima  Adobe di distribuire un certificato rinnovato, si verificherà un&#39;interruzione dell&#39; [!DNL Target] implementazione specifica.

### Fino a quando scade il mio nuovo certificato SSL?

I certificati rilasciati prima del 1° settembre 2020 saranno certificati biennali. I certificati rilasciati a partire dal 1° settembre 2020 saranno certificati annuali. Per ulteriori informazioni sul passaggio ai certificati a un anno, consultate [questo](https://www.digicert.com/position-on-1-year-certificates)articolo.

### Quali nomi host scegliere? Quanti nomi host per dominio devo scegliere?

[!DNL Target] Le implementazioni CNAME richiedono un solo nome host per dominio nel certificato SSL e nel DNS del cliente, per questo è consigliabile. Alcuni clienti potrebbero richiedere nomi host aggiuntivi per dominio per i propri scopi (ad esempio, test in fase di pre-produzione), che è supportato.

La maggior parte dei clienti scelgono un nome host come `target.example.com`, quindi questo è quello che consigliamo, ma la scelta è in definitiva vostra. Accertatevi di non richiedere un nome host di un record DNS esistente in quanto ciò causerebbe un conflitto e un ritardo nella risoluzione della richiesta [!DNL Target] CNAME.

### Ho già implementato un CNAME per [!DNL Adobe Analytics], possiamo usare lo stesso certificato o nome host?

No, [!DNL Target] richiede un nome host e un certificato separati.

### L&#39;implementazione corrente di Target viene influenzata da ITP 2.x?

In un browser Safari, accedete al sito Web in cui è presente una libreria JavaScript di Target. If you see a Target cookie set in the context of a CNAME, such as `analytics.company.com`, then you are not impacted by ITP 2.x.

I problemi ITP possono essere risolti per Target con un CNAME Analytics. Avrete bisogno di un CNAME Target separato solo per gli scenari di blocco degli annunci in cui Target viene bloccato.

Per ulteriori informazioni sull&#39;ITP, vedere [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).

### Che tipo di interruzione del servizio posso aspettarmi quando viene implementata l’implementazione CNAME?

Non si verifica alcuna interruzione del servizio quando il certificato viene distribuito (compresi i rinnovi di certificati). Tuttavia, quando si modifica il nome host nel codice di [!DNL Target] implementazione (`serverDomain` in at.js) nel nuovo nome host CNAME (`target.example.com`), i browser Web tratteranno i visitatori di ritorno come nuovi visitatori e i loro dati di profilo andranno persi perché il cookie precedente sarà inaccessibile sotto il vecchio nome host (`clientcode.tt.omtrdc.net`) a causa dei modelli di protezione del browser. Si tratta di un’interruzione una tantum solo per il cut-over iniziale del nuovo CNAME. I rinnovi di certificati non hanno lo stesso effetto in quanto il nome host non viene modificato.

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

1. Incollate quindi questo comando (sostituendo `target.example.com` con il vostro nome host):

   ```
   validateEdgeFpsslSni target.example.com
   ```

   Se l&#39;implementazione è pronta, dovresti vedere l&#39;output come di seguito. La parte importante è che tutte le righe mostrano `CN=target.example.com`, che corrisponde al nostro nome host desiderato. Se ne viene mostrato uno `CN=*.tt.omtrdc.net`, l&#39;implementazione **non** è pronta.

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

1. Convalida il nuovo CNAME DNS con un&#39;altra richiesta curl, che dovrebbe mostrare anche `CN=target.example.com`:

   ```
   curl -sSv https://target.example.com 2>&1 | grep subject:
   ```

   >[!NOTE]
   >
   >Se questo comando ha esito negativo ma il `validateEdgeFpsslSni` comando precedente ha esito positivo, potrebbe essere necessario attendere la propagazione completa degli aggiornamenti DNS. Ai record DNS è associato un [TTL (time-to-live)](https://en.wikipedia.org/wiki/Time_to_live#DNS_records) che specifica il tempo di scadenza della cache per le risposte DNS di tali record, pertanto potrebbe essere necessario attendere almeno fino a quando i TTL non saranno disponibili. È possibile utilizzare il `dig target.example.com` comando o [la Casella degli strumenti](https://toolbox.googleapps.com/apps/dig/#CNAME) di G Suite per cercare i TTL specifici.

## Limitazioni note

* La modalità QA non sarà fissa se hai CNAME e at.js 1.x perché è basata su un cookie di terze parti. La soluzione alternativa consiste nell’aggiungere i parametri di anteprima a ciascun URL a cui ci si sposta. La modalità QA è fissa quando si dispone di CNAME e a.js 2.x.
* Al momento l’ `overrideMboxEdgeServer` impostazione non funziona correttamente con CNAME. Deve essere impostato come `false` per evitare richieste non riuscite.
* Quando si utilizza CNAME, è più probabile che la dimensione dell&#39;intestazione del cookie per le chiamate a Target aumenti. Consigliamo di mantenere la dimensione del cookie sotto gli 8 KB.
