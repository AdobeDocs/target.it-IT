---
keywords: client care;cname;programma di certificato;nome canonico;cookie;certificato;amc;certificato gestito adobe;digicert;convalida del controllo del dominio;dcv
description: Lavora con Adobe Client Care per implementare il supporto CNAME (Canonical Name) in Adobe [!DNL Target] per gestire i problemi di blocco degli annunci o i criteri dei cookie relativi a ITP.
title: Come si utilizza il CNAME in Target?
feature: Privacy e sicurezza
role: Developer
exl-id: bf533771-6d46-48ba-964c-3ad9ce9f7352
translation-type: tm+mt
source-git-commit: 85a17944c7d5924edb1bbabb7531274249ceaaa8
workflow-type: tm+mt
source-wordcount: '1150'
ht-degree: 2%

---

# CNAME e Adobe Target

Istruzioni per lavorare con [!DNL Adobe] Client Care per implementare il supporto CNAME (Canonical Name) in [!DNL Adobe Target]. Utilizza CNAME per gestire i problemi di blocco degli annunci o i criteri dei cookie relativi a ITP (Intelligent Tracking Prevention). Con CNAME, le chiamate vengono effettuate a un dominio di proprietà del cliente anziché a un dominio di proprietà di [!DNL Adobe].

## Richiedere il supporto CNAME in Target

1. Determina l’elenco dei nomi host necessari per il certificato SSL (consulta le domande frequenti riportate di seguito).

1. Per ogni nome host, crea un record CNAME nel DNS che punta al nome host [!DNL Target] normale `clientcode.tt.omtrdc.net`.

   Ad esempio, se il codice client è &quot;cannamecustomer&quot; e il nome host proposto è `target.example.com`, il record CNAME DNS sarà simile al seguente:

   ```
   target.example.com.  IN  CNAME  cnamecustomer.tt.omtrdc.net.
   ```

   >[!IMPORTANT]
   >
   >L’autorità di certificazione di Adobe, DigiCert, non può rilasciare un certificato fino al completamento di questo passaggio. Pertanto, [!DNL Adobe] non può soddisfare la richiesta di implementazione CNAME fino al completamento di questo passaggio.

1. [Compila questo ](/help/assets/FPC_Request_Form.xlsx) modulo e includilo quando  [apri un ticket di assistenza clienti Adobe per richiedere il supporto](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) CNAME:

   * Adobe di codice client [!DNL Target]:
   * Nomi host del certificato SSL (esempio: `target.example.com target.example.org`):
   * Acquirente certificato SSL (Adobe vivamente consigliato, consulta le Domande frequenti): Adobe/cliente
   * Se il cliente sta acquistando il certificato, noto anche come &quot;Porta il tuo certificato&quot; (BYOC), compila questi dettagli aggiuntivi:
      * Organizzazione di certificati (esempio: Esempio di società Inc):
      * Unità organizzativa certificato (facoltativo, esempio: Marketing):
      * Paese del certificato (esempio: USA):
      * Stato/area geografica del certificato (esempio: California):
      * Città del certificato (esempio: San Jose):

1. Se [!DNL Adobe] acquista il certificato, [!DNL Adobe] collabora con DigiCert per acquistare e distribuire il certificato sui server di produzione di Adobe.

   Se il cliente sta acquistando il certificato (BYOC), [!DNL Adobe] l’Assistenza clienti ti invia la richiesta di firma del certificato (CSR, Certificate Sign Request). Utilizza la CSR quando acquisti il certificato tramite l’autorità di certificazione scelta. Dopo il rilascio del certificato, invia una copia del certificato ed eventuali certificati intermedi all’ [!DNL Adobe] Client Care per la distribuzione.

   [!DNL Adobe] L’Assistenza clienti ti notifica quando l’implementazione è pronta.

1. Aggiorna `serverDomain` al nuovo CNAME in at.js.

## Domande frequenti 

Le seguenti informazioni rispondono alle domande più frequenti sulla richiesta e sull&#39;implementazione del supporto CNAME in [!DNL Target]:

### Posso fornire il mio certificato personale (porta il tuo certificato o BYOC)?

Puoi fornire il tuo certificato. Tuttavia, [!DNL Adobe] non consiglia questa pratica. La gestione del ciclo di vita del certificato SSL è più semplice sia per [!DNL Adobe] che per gli acquisti e i controlli del certificato da parte di [!DNL Adobe]. I certificati SSL devono essere rinnovati ogni anno. Pertanto, [!DNL Adobe] l’Assistenza clienti deve contattarti ogni anno per ottenere un nuovo certificato in modo tempestivo. Alcuni clienti possono avere difficoltà a produrre un certificato rinnovato in modo tempestivo. L’implementazione [!DNL Target] viene compromessa alla scadenza del certificato perché i browser rifiutano le connessioni.

>[!IMPORTANT]
>
>Se richiedi un’implementazione CNAME di [!DNL Target] porta-il-tuo certificato, ogni anno devi fornire nuovi certificati all’ [!DNL Adobe] Assistenza clienti. Consentire alla scadenza del certificato CNAME prima che [!DNL Adobe] possa distribuire un certificato rinnovato, si verifica un’interruzione dell’implementazione [!DNL Target] specifica.

### Per quanto tempo scade il nuovo certificato SSL?

I certificati rilasciati prima del 1° settembre 2020 sono certificati biennali. I certificati rilasciati a partire dal 1° settembre 2020 sono certificati annuali. Per ulteriori informazioni sul passaggio a certificati annuali [qui](https://www.digicert.com/position-on-1-year-certificates), consulta la sezione dedicata al passaggio a certificati annuali.

### Quali nomi host dovrei scegliere? Quanti nomi host per dominio devo scegliere?

[!DNL Target] Le implementazioni CNAME richiedono un solo nome host per dominio sul certificato SSL e nel DNS del cliente. Adobe consiglia un nome host. Alcuni clienti richiedono più nomi host per dominio per i propri scopi (ad esempio, test in staging), che è supportato.

La maggior parte dei clienti sceglie un nome host come `target.example.com`. L&#39;Adobe consiglia di seguire questa pratica, ma la scelta è in definitiva tua. Non richiedere un nome host di un record DNS esistente. In questo modo si crea un conflitto e si ritarda il tempo per la risoluzione della richiesta [!DNL Target] CNAME.

### Ho già un&#39;implementazione CNAME per [!DNL Adobe Analytics], possiamo usare lo stesso certificato o nome host?

No, [!DNL Target] richiede un nome host e un certificato separati.

### L’implementazione corrente di [!DNL Target] è interessata da ITP 2.x?

In un browser Safari, accedi al tuo sito web contenente una libreria JavaScript di [!DNL Target]. Se trovi un cookie [!DNL Target] impostato nel contesto di un CNAME, ad esempio `analytics.company.com`, non sei interessato da ITP 2.x.

I problemi ITP possono essere risolti per [!DNL Target] con un solo CNAME [!DNL Analytics]. È necessario un CNAME separato [!DNL Target] solo in scenari di blocco degli annunci in cui [!DNL Target] è bloccato.

Per ulteriori informazioni su ITP, consulta [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).

### Che tipo di interruzioni del servizio posso aspettarmi quando viene implementata l’implementazione CNAME?

Non vi è alcuna interruzione del servizio quando il certificato viene distribuito (inclusi i rinnovi di certificato).

Tuttavia, dopo aver modificato il nome host nel codice di implementazione [!DNL Target] (`serverDomain` in at.js) nel nuovo nome host CNAME (`target.example.com`), i browser web considerano i visitatori di ritorno come nuovi visitatori. I dati del profilo dei visitatori di ritorno vengono persi perché il cookie precedente è inaccessibile con il vecchio nome host (`clientcode.tt.omtrdc.net`). Il cookie precedente è inaccessibile a causa dei modelli di sicurezza del browser. Questa interruzione si verifica solo sul cut-over iniziale al nuovo CNAME. I rinnovi del certificato non hanno lo stesso effetto perché il nome host non cambia.

### Quale tipo di chiave e algoritmo di firma del certificato viene utilizzato per l’implementazione CNAME?

Tutti i certificati sono RSA SHA-256 e le chiavi sono RSA a 2048 bit, per impostazione predefinita. Le dimensioni chiave superiori a 2048 bit non sono attualmente supportate.

### Come posso verificare che la mia implementazione CNAME sia pronta per il traffico?

Utilizza il seguente set di comandi (nel terminale della riga di comando macOS o Linux, utilizzando bash e curl 7.49+):

1. Incolla questa funzione bash nel terminale:

   ```
   function validateEdgeFpsslSni {
       domain=$1
       for edge in mboxedge{31,32,{34..38}}.tt.omtrdc.net; do
           echo "$edge: $(curl -sSv --connect-to $domain:443:$edge:443 https://$domain 2>&1 | grep subject:)"
       done
   }
   ```

1. Incolla questo comando (sostituendo `target.example.com` con il tuo nome host):

   ```
   validateEdgeFpsslSni target.example.com
   ```

   Se l&#39;implementazione è pronta, puoi visualizzare l&#39;output come segue. La parte importante è che tutte le righe includono `CN=target.example.com`, che corrisponde al nome host desiderato. Se una qualsiasi riga include `CN=*.tt.omtrdc.net`, l&#39;implementazione è **not** ready.

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

1. Convalida il tuo nuovo CNAME DNS con un&#39;altra richiesta curl che dovrebbe mostrare anche `CN=target.example.com`:

   ```
   curl -sSv https://target.example.com 2>&1 | grep subject:
   ```

   >[!NOTE]
   >
   >Se questo comando non riesce ma il comando `validateEdgeFpsslSni` precedente ha esito positivo, attendi che gli aggiornamenti DNS si propaghino completamente. Ai record DNS è associato [TTL (time-to-live)](https://en.wikipedia.org/wiki/Time_to_live#DNS_records) che determina il tempo di scadenza della cache per le risposte DNS di tali record. Di conseguenza, potrebbe essere necessario attendere almeno quanto i TTL. È possibile utilizzare il comando `dig target.example.com` o [la Casella degli strumenti di G Suite](https://toolbox.googleapps.com/apps/dig/#CNAME) per cercare i TTL specifici.

## Limitazioni note

* La modalità Controllo qualità non è persistente quando disponi di CNAME e at.js 1.x perché è basata su un cookie di terze parti. La soluzione consiste nell’aggiungere i parametri di anteprima a ciascun URL a cui accedi. La modalità Controllo qualità è persistente quando si dispone di CNAME e at.js 2.x.
* Attualmente l’impostazione `overrideMboxEdgeServer` non funziona correttamente con CNAME quando si utilizzano versioni at.js precedenti a at.js 1.8.2 e at.js 2.3.1. Se si utilizza una versione precedente di at.js, questa impostazione deve essere impostata su `false` per evitare errori nelle richieste. In alternativa, è consigliabile [aggiornare at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) a una versione più recente e supportata.
* Quando si utilizza CNAME, è più probabile che le dimensioni dell&#39;intestazione del cookie per le chiamate [!DNL Target] aumentino. [!DNL Adobe] consiglia di mantenere la dimensione del cookie sotto gli 8 KB.
