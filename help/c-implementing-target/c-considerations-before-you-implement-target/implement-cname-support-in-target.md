---
keywords: client care;cname;certificate program;canonic name;cookies;certificate;amc;adobe manage certificate;digicert;domain control validation;dcv
description: Consultate  Client Care di Adobe per implementare il supporto CNAME (Nome canonico) in  Adobe Target per gestire problemi di blocco degli annunci o le policy dei cookie relative a ITP.
title: Come si utilizza il CNAME in Target?
feature: Privacy e sicurezza
role: Sviluppatori
translation-type: tm+mt
source-git-commit: 69677b9d384d9817a39386fc1388a4aa42121713
workflow-type: tm+mt
source-wordcount: '1163'
ht-degree: 2%

---


# CNAME e Adobe Target

Istruzioni per l&#39;utilizzo di [!DNL Adobe] Client Care per implementare il supporto CNAME (Nome canonico) in [!DNL Adobe Target]. Utilizzate CNAME per gestire i problemi di blocco degli annunci o le politiche sui cookie di ITP (Intelligent Tracking Prevention). Con CNAME, le chiamate vengono effettuate a un dominio di proprietà del cliente anziché a un dominio di proprietà di [!DNL Adobe].

## Richiedi supporto CNAME in Target

1. Determinate l’elenco dei nomi host necessari per il certificato SSL (consultate le domande frequenti riportate di seguito).

1. Per ogni nome host, crea un record CNAME nel DNS indicando il normale [!DNL Target] nome host `clientcode.tt.omtrdc.net`.

   Ad esempio, se il codice client è &quot;nomecustomer&quot; e il nome host proposto è `target.example.com`, il record CNAME DNS sarà simile al seguente:

   ```
   target.example.com.  IN  CNAME  cnamecustomer.tt.omtrdc.net.
   ```

   >[!IMPORTANT]
   >
   > Adobe  autorità di certificazione DigiCert non può rilasciare un certificato finché il passaggio non viene completato. Di conseguenza, [!DNL Adobe] non può soddisfare la richiesta di implementazione CNAME fino al completamento di questo passaggio.

1. [Compila questo ](https://experienceleague.adobe.com/docs/core-services/assets/FPC_Request_Form.xlsx?lang=en) modulo e includilo quando  [apri un ticket Client Care  Adobe che richiede il supporto](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) CNAME:

   *  codice client [!DNL Target] Adobe:
   * Nomi host del certificato SSL (esempio: `target.example.com target.example.org`):
   * Acquirente certificato SSL ( Adobe è altamente consigliato, consultare le domande frequenti: Adobe/cliente 
   * Se il cliente sta acquistando il certificato, noto anche come &quot;Porta il tuo certificato personale&quot; (BYOC), compila i seguenti dettagli aggiuntivi:
      * Organizzazione dei certificati (esempio: Esempio Azienda Inc):
      * Unità organizzativa certificato (facoltativo, esempio: Marketing):
      * Paese del certificato (esempio: US):
      * Stato/regione del certificato (esempio: California):
      * Città certificato (esempio: San Jose):

1. Se [!DNL Adobe] sta acquistando il certificato, [!DNL Adobe] funziona con DigiCert per acquistare e distribuire il certificato  server  produzione di Adobi.

   Se il cliente acquista il certificato (BYOC), [!DNL Adobe] Client Care invia la richiesta di firma del certificato (CSR). Utilizzate il CSR quando acquistate il certificato tramite la vostra autorità di certificazione. Dopo il rilascio del certificato, inviate una copia del certificato ed eventuali certificati intermedi all&#39;Assistenza clienti [!DNL Adobe] per la distribuzione.

   [!DNL Adobe] Client Care invia una notifica quando l&#39;implementazione è pronta.

1. Aggiorna `serverDomain` nel nuovo CNAME in at.js.

## Domande frequenti 

Le seguenti informazioni rispondono alle domande frequenti su come richiedere e implementare il supporto CNAME in [!DNL Target]:

### Posso fornire il mio certificato personale (portare il tuo certificato personale o BYOC)?

Potete fornire il vostro certificato. Tuttavia, [!DNL Adobe] non consiglia questa pratica. La gestione del ciclo di vita del certificato SSL è più semplice sia per [!DNL Adobe] che per gli acquisti e i controlli del certificato da parte di [!DNL Adobe]. I certificati SSL devono essere rinnovati ogni anno. Di conseguenza, [!DNL Adobe] Client Care deve contattarvi ogni anno per ottenere un nuovo certificato in modo tempestivo. Alcuni clienti potrebbero avere difficoltà a produrre un certificato rinnovato in modo tempestivo. L&#39;implementazione [!DNL Target] viene compromessa alla scadenza del certificato perché i browser rifiutano le connessioni.

>[!IMPORTANT]
>
>Se richiedete un&#39;implementazione CNAME [!DNL Target] con certificato personale, dovete fornire certificati rinnovati a [!DNL Adobe] Client Care ogni anno. Consentendo al certificato CNAME di scadere prima che [!DNL Adobe] possa distribuire un certificato rinnovato, si verifica un&#39;interruzione dell&#39;implementazione [!DNL Target] specifica.

### Fino a quando scade il mio nuovo certificato SSL?

I certificati rilasciati prima del 1° settembre 2020 sono certificati biennali. I certificati rilasciati a partire dal 1° settembre 2020 sono certificati annuali. Per ulteriori informazioni sul passaggio ai certificati a un anno, vedere [qui](https://www.digicert.com/position-on-1-year-certificates).

### Quali nomi host scegliere? Quanti nomi host per dominio devo scegliere?

[!DNL Target] Le implementazioni CNAME richiedono un solo nome host per dominio nel certificato SSL e nel DNS del cliente.  Adobe consiglia un nome host. Alcuni clienti richiedono più nomi host per dominio per i propri scopi (ad esempio, test in fase di pre-produzione), che è supportato.

La maggior parte dei clienti sceglie un nome host come `target.example.com`.  Adobe raccomanda di seguire questa pratica, ma la scelta è in definitiva tutta tua. Non richiedere un nome host di un record DNS esistente. In questo modo si verifica un conflitto e si ritarda il tempo necessario per risolvere la richiesta CNAME [!DNL Target].

### Ho già implementato un CNAME per [!DNL Adobe Analytics], possiamo utilizzare lo stesso certificato o nome host?

No, [!DNL Target] richiede un nome host e un certificato separati.

### L&#39;implementazione corrente di Target viene influenzata da ITP 2.x?

In un browser Safari, accedi al tuo sito web contenente una libreria JavaScript di [!DNL Target]. Se viene visualizzato un cookie [!DNL Target] impostato nel contesto di un CNAME, ad esempio `analytics.company.com`, ITP 2.x non viene interessato.

I problemi ITP possono essere risolti per [!DNL Target] con un CNAME [!DNL Analytics]. È necessario un CNAME [!DNL Target] separato solo negli scenari di blocco annunci in cui [!DNL Target] è bloccato.

Per ulteriori informazioni sull&#39;ITP, vedere [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).

### Che tipo di interruzione del servizio posso aspettarmi quando viene implementata l’implementazione CNAME?

Non si verifica alcuna interruzione del servizio quando il certificato viene distribuito (compresi i rinnovi di certificati).

Tuttavia, dopo aver modificato il nome host nel codice di implementazione [!DNL Target] (`serverDomain` in at.js) nel nuovo nome host CNAME (`target.example.com`), i browser Web gestiscono i visitatori di ritorno come nuovi visitatori. La restituzione dei dati del profilo dei visitatori viene persa perché il cookie precedente non è accessibile con il vecchio nome host (`clientcode.tt.omtrdc.net`). Il cookie precedente è inaccessibile a causa dei modelli di protezione del browser. Questa interruzione si verifica solo sul cut-over iniziale del nuovo CNAME. I rinnovi di certificati non hanno lo stesso effetto perché il nome host non cambia.

### Che tipo di chiave e algoritmo di firma certificato vengono utilizzati per l&#39;implementazione CNAME?

Tutti i certificati sono RSA SHA-256 e le chiavi sono RSA a 2048 bit, per impostazione predefinita. Le dimensioni chiave superiori a 2048 bit non sono attualmente supportate.

### Come posso verificare che l’implementazione CNAME sia pronta per il traffico?

Utilizzate il seguente set di comandi (nel terminale della riga di comando macOS o Linux, utilizzando bash e curl 7.49+):

1. Incollate questa funzione bash nel terminale:

   ```
   function validateEdgeFpsslSni {
       domain=$1
       for edge in mboxedge{31,32,{34..38}}.tt.omtrdc.net; do
           echo "$edge: $(curl -sSv --connect-to $domain:443:$edge:443 https://$domain 2>&1 | grep subject:)"
       done
   }
   ```

1. Incolla questo comando (sostituendo `target.example.com` con il nome host):

   ```
   validateEdgeFpsslSni target.example.com
   ```

   Se l&#39;implementazione è pronta, viene visualizzato l&#39;output come indicato di seguito. La parte importante è che tutte le righe includono `CN=target.example.com`, che corrisponde al nome host desiderato. Se una qualsiasi riga include `CN=*.tt.omtrdc.net`, l&#39;implementazione è **not** pronta.

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
   >Se questo comando non riesce ma il comando `validateEdgeFpsslSni` precedente ha esito positivo, attendete che gli aggiornamenti DNS si propaghino completamente. Ai record DNS è associato un [TTL (time-to-live)](https://en.wikipedia.org/wiki/Time_to_live#DNS_records) che specifica il tempo di scadenza della cache per le risposte DNS di tali record. Di conseguenza, potrebbe essere necessario attendere almeno fino a quando il TTL è impostato. È possibile utilizzare il comando `dig target.example.com` o [G Suite Toolbox](https://toolbox.googleapps.com/apps/dig/#CNAME) per ricercare specifici TTL.

## Limitazioni note

* La modalità QA non è fissa quando si dispone di CNAME e at.js 1.x perché è basata su un cookie di terze parti. La soluzione alternativa consiste nell’aggiungere i parametri di anteprima a ciascun URL a cui ci si sposta. La modalità QA è fissa quando si dispone di CNAME e a.js 2.x.
* Attualmente l&#39;impostazione `overrideMboxEdgeServer` non funziona correttamente con CNAME quando si utilizzano le versioni at.js precedenti a at.js 1.8.2 e a.js 2.3.1. Se utilizzi una versione precedente di at.js, questa impostazione deve essere impostata su `false` per evitare richieste non riuscite. In alternativa, è consigliabile aggiornare [at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) a una versione supportata più recente.
* Quando si utilizza CNAME, è più probabile che la dimensione dell&#39;intestazione del cookie per le chiamate [!DNL Target] aumenti. [!DNL Adobe] consiglia di mantenere la dimensione del cookie inferiore a 8 KB.
