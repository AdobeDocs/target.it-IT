---
keywords: client care;cname;programma di certificato;nome canonico;cookie;certificato;amc;certificato gestito adobe;digicert;convalida del controllo del dominio;dcv
description: Utilizzare [!DNL Adobe] Assistenza clienti per implementare il supporto CNAME (Canonical Name) in [!DNL Adobe Target] per gestire i problemi di blocco degli annunci.
title: Come si utilizza il CNAME in Target?
feature: Privacy & Security
role: Developer
exl-id: bf533771-6d46-48ba-964c-3ad9ce9f7352
source-git-commit: b1e8ea2370fc15f4bfcd960ab2960cafe2db92b8
workflow-type: tm+mt
source-wordcount: '1183'
ht-degree: 1%

---

# CNAME e [!DNL Target]

Istruzioni per l’uso [!DNL Adobe] Assistenza clienti per implementare il supporto CNAME (Canonical Name) in [!DNL Adobe Target]. Utilizza CNAME per gestire i problemi di blocco degli annunci o i criteri dei cookie relativi a ITP (Intelligent Tracking Prevention). Con CNAME, le chiamate vengono effettuate a un dominio di proprietà del cliente anziché a un dominio di proprietà di [!DNL Adobe].

## Richiedi supporto CNAME in [!DNL Target]

1. Determina l’elenco dei nomi host necessari per il certificato SSL (consulta le domande frequenti riportate di seguito).

1. Per ogni nome host, crea un record CNAME nel DNS che punta al tuo normale [!DNL Target] hostname `clientcode.tt.omtrdc.net`.

   Ad esempio, se il tuo codice cliente è &quot;cannamecustomer&quot; e il tuo nome host proposto è `target.example.com`, il record CNAME DNS ha un aspetto simile al seguente:

   ```
   target.example.com.  IN  CNAME  cnamecustomer.tt.omtrdc.net.
   ```

   >[!IMPORTANT]
   >
   >[!DNL Adobe]L&#39;autorità di certificazione DigiCert non può rilasciare un certificato fino al completamento di questo passaggio. Pertanto, [!DNL Adobe] non è in grado di soddisfare la richiesta di implementazione CNAME fino al completamento di questo passaggio.

1. [Compila questo modulo](/help/main/assets/FPC_Request_Form.xlsx) e includerlo quando [aprire un [!DNL Adobe] Segnale per l’Assistenza clienti che richiede supporto CNAME](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C):

   * [!DNL Adobe Target] client code:
   * Nomi host del certificato SSL (esempio: `target.example.com target.example.org`):
   * Acquirente certificato SSL ([!DNL Adobe] è altamente consigliato, consulta le Domande frequenti): Adobe/cliente
   * Se il cliente sta acquistando il certificato, noto anche come &quot;Porta il tuo certificato&quot; (BYOC), compila questi dettagli aggiuntivi:
      * Organizzazione di certificati (esempio: Esempio di società Inc):
      * Unità organizzativa certificato (facoltativo, esempio: Marketing):
      * Paese del certificato (esempio: USA):
      * Stato/area geografica del certificato (esempio: California):
      * Città del certificato (esempio: San Jose):

1. Se [!DNL Adobe] acquista il certificato, [!DNL Adobe] Lavora con DigiCert per acquistare e distribuire il certificato su [!DNL Adobe]Server di produzione di .

   Se il cliente acquista il certificato (BYOC), [!DNL Adobe] L’Assistenza clienti ti invia la richiesta di firma del certificato (CSR, Certificate Sign Request). Utilizza la CSR quando acquisti il certificato tramite l’autorità di certificazione scelta. Dopo il rilascio del certificato, invia una copia del certificato ed eventuali certificati intermedi a [!DNL Adobe] Client Care per la distribuzione.

   [!DNL Adobe] L’Assistenza clienti ti notifica quando l’implementazione è pronta.

1. Aggiorna `serverDomain` ([documentazione](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/)) al nuovo nome host CNAME e imposta `overrideMboxEdgeServer` a `false` ([documentazione](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/)) nella configurazione at.js.

## Domande frequenti 

Le seguenti informazioni rispondono alle domande frequenti sulla richiesta e l’implementazione del supporto CNAME in [!DNL Target]:

### Posso fornire il mio certificato personale (porta il tuo certificato o BYOC)?

Puoi fornire il tuo certificato. Tuttavia, [!DNL Adobe] non consiglia questa pratica. La gestione del ciclo di vita del certificato SSL è più semplice per entrambe le applicazioni [!DNL Adobe] e se [!DNL Adobe] acquista e controlla il certificato. I certificati SSL devono essere rinnovati ogni anno. Pertanto, [!DNL Adobe] L’Assistenza clienti deve contattarti ogni anno per ottenere un nuovo certificato in modo tempestivo. Alcuni clienti possono avere difficoltà a produrre un certificato rinnovato in modo tempestivo. Le [!DNL Target] l’implementazione viene compromessa quando il certificato scade perché i browser rifiutano le connessioni.

>[!IMPORTANT]
>
>Se richiedi un [!DNL Target] implementa CNAME con il tuo certificato, sei responsabile di fornire certificati rinnovati a [!DNL Adobe] Assistenza clienti ogni anno. Consentire la scadenza del certificato CNAME prima di [!DNL Adobe] può distribuire un nuovo certificato con risultati in un’interruzione specifica [!DNL Target] implementazione.

### Per quanto tempo scade il nuovo certificato SSL?

Tutto [!DNL Adobe]- i certificati acquistati sono validi per un anno. Vedi [Articolo di DigiCert su certificati di 1 anno](https://www.digicert.com/blog/position-on-1-year-certificates) per ulteriori informazioni.

### Quali nomi host dovrei scegliere? Quanti nomi host per dominio devo scegliere?

[!DNL Target] Le implementazioni CNAME richiedono un solo nome host per dominio sul certificato SSL e nel DNS del cliente. [!DNL Adobe] consiglia un nome host per dominio. Alcuni clienti richiedono più nomi host per dominio per i propri scopi (ad esempio, test in staging), che è supportato.

La maggior parte dei clienti sceglie un nome host come `target.example.com`. [!DNL Adobe] consiglia di seguire questa pratica, ma la scelta è in definitiva tua. Non richiedere un nome host di un record DNS esistente. In questo modo si crea un conflitto e si ritarda il tempo per la risoluzione del tuo [!DNL Target] Richiesta CNAME.

### Ho già un&#39;implementazione CNAME per [!DNL Adobe Analytics], posso usare lo stesso certificato o nome host?

No, [!DNL Target] richiede un nome host e un certificato separati.

### È la mia attuale implementazione di [!DNL Target] interessato da ITP 2.x?

La versione 2.3 di Apple Intelligent Tracking Prevention (ITP) introduce la funzione di attenuazione del rischio di blocco dei CNAME, che è in grado di rilevare [!DNL Adobe Target] Implementazioni CNAME e la scadenza del cookie viene ridotta a sette giorni. Attualmente [!DNL Target] non offre alcuna soluzione alternativa per la mitigazione del blocco CNAME di ITP. Per ulteriori informazioni su ITP, consulta [Apple Intelligent Tracking Prevention (ITP) 2.x](https://developer.adobe.com/target/before-implement/privacy/apple-itp-2x/).

### Che tipo di interruzioni del servizio posso aspettarmi quando viene implementata l’implementazione CNAME?

Non vi è alcuna interruzione del servizio quando il certificato viene distribuito (inclusi i rinnovi di certificato).

Tuttavia, dopo aver modificato il nome host nel [!DNL Target] codice di implementazione (`serverDomain` in at.js) al nuovo nome host CNAME (`target.example.com`), i browser web considerano i visitatori di ritorno come nuovi visitatori. I dati di profilo dei visitatori di ritorno vengono persi perché il cookie precedente è inaccessibile con il vecchio nome host (`clientcode.tt.omtrdc.net`). Il cookie precedente è inaccessibile a causa dei modelli di sicurezza del browser. Questa interruzione si verifica solo sul cut-over iniziale al nuovo CNAME. I rinnovi del certificato non hanno lo stesso effetto perché il nome host non cambia.

### Quale tipo di chiave e algoritmo di firma del certificato viene utilizzato per l’implementazione CNAME?

Tutti i certificati sono RSA SHA-256 e le chiavi sono RSA a 2048 bit, per impostazione predefinita. Le dimensioni chiave superiori a 2048 bit non sono attualmente supportate.

### Come posso verificare che la mia implementazione CNAME sia pronta per il traffico?

Utilizza il seguente set di comandi (nel terminale della riga di comando macOS o Linux, utilizzando bash e curl >=7.49):

1. Copia e incolla questa funzione bash nel terminale o incolla la funzione nel file script di avvio bash (in genere `~/.bash_profile` o `~/.bashrc`) in modo che la funzione sia disponibile in tutte le sessioni terminali:

   ```
   function adobeTargetCnameValidation {
     local hostname="$1"
     if [ -z "$hostname" ]; then
       echo "ERROR: no hostname specified"
       return 1
     fi
   
     local service="Adobe Target CNAME implementation"
     local edges="31 32 34 35 36 37 38"
     local edgeDomain="tt.omtrdc.net"
     local edgeFormat="mboxedge%d%s.$edgeDomain"
     local shardFormat="-alb%02d"
     local shards=5
     local shardsFoundCount=0
     local shardsFound
     local shardsFoundOutput
     local curlRegex="subject:.*CN=|expire date:|issuer:"
     local curlValidation="SSL certificate verify ok"
     local curlResponseValidation='"OK"'
     local curlEndpoint="/uptime?mboxClient=uptime3"
     local url="https://$hostname$curlEndpoint"
     local sslLabsUrl="https://ssllabs.com/ssltest/analyze.html?hideResults=on&latest&d=$hostname"
     local success="✅"
     local failure="🚫"
     local info="🔎"
     local rule="="
     local horizontalRule="$(seq ${COLUMNS:-30} | xargs printf "$rule%.0s")"
     local miniRule="$(seq 5 | xargs printf "$rule%.0s")"
     local curlVersion="$(curl --version | head -1 | cut -d' ' -f2 )"
     local curlVersionRequired=">=7.49"
     local edgeCount="$(wc -w <<< "$edges" | tr -d ' ')"
     local edge
     local shard
     local currEdgeShard
     local dnsOutput
     local cnameExists
     local endToEndTestSucceeded
     local curlResult
   
     for shard in $(seq $shards); do
       if [ "$shardsFoundCount" -eq 0 ]; then
         for edge in $edges; do
           if [ "$shard" -eq 1 ]; then
             currEdgeShard="$(printf "$edgeFormat" "$edge" "")"
           else
             currEdgeShard="$(
               printf "$edgeFormat" "$edge" "$(
                 printf -- "$shardFormat" "$shard"
               )"
             )"
           fi
           curlResult="$(curl -vsm20 --connect-to "$hostname:443:$currEdgeShard:443" "$url" 2>&1)"
           if grep -q "$curlValidation" <<< "$curlResult"; then
             shardsFound+=" $currEdgeShard"
             if grep -q "$curlResponseValidation" <<< "$curlResult"; then
               shardsFoundCount=$((shardsFoundCount+1))
               shardsFoundOutput+="\n\n$miniRule $success $hostname [edge shard: $currEdgeShard] $miniRule\n"
             else
               shardsFoundOutput+="\n\n$miniRule $failure $hostname [edge shard: $currEdgeShard] $miniRule\n"
             fi
             shardsFoundOutput+="$(grep -E "$curlRegex" <<< "$curlResult" | sort)"
             if ! grep -q "$curlResponseValidation" <<< "$curlResult"; then
               shardsFoundOutput+="\nERROR: unexpected HTTP response from this shard using $url"
             fi
           fi
         done
       fi
     done
   
     echo
     echo "$horizontalRule"
     echo
     echo "$service validation for hostname $hostname:"
     dnsOutput="$(dig -t CNAME +short "$hostname" 2>&1)"
     if grep -qFi ".$edgeDomain" <<< "$dnsOutput"; then
       echo "$success $hostname passes DNS CNAME validation"
       cnameExists=true
     else
       echo -n "$failure $hostname FAILED DNS CNAME validation -- "
       if [ -n "$dnsOutput" ]; then
         echo -e "$dnsOutput is not in the subdomain $edgeDomain"
       else
         echo "required DNS CNAME record pointing to <target-client-code>.$edgeDomain not found"
       fi
     fi
   
     curlResult="$(curl -vsm20 "$url" 2>&1)"
     if grep -q "$curlValidation" <<< "$curlResult"; then
       if grep -q "$curlResponseValidation" <<< "$curlResult"; then
         echo -en "$success $hostname passes TLS and HTTP response validation"
         if [ -n "$cnameExists" ]; then
           echo
         else
           echo " -- the DNS CNAME is not pointing to the correct subdomain for ${service}s with Adobe-managed certificates" \
             "(bring-your-own-certificate implementations don't have this requirement), but this test passes as configured"
         fi
         endToEndTestSucceeded=true
       else
         echo -n "$failure $hostname FAILED HTTP response validation --" \
           "unexpected response from $url -- "
         if [ -n "$cnameExists" ]; then
           echo "DNS is NOT pointing to the correct shard, notify Adobe Client Care"
         else
           echo "the required DNS CNAME record is missing, see above"
         fi
       fi
     else
   
       echo -n "$failure $hostname FAILED TLS validation -- "
       if [ -n "$cnameExists" ]; then
         echo "DNS is likely NOT pointing to the correct shard or there's a validation issue with the certificate or" \
           "protocols, see curl output below and optionally SSL Labs ($sslLabsUrl):"
         echo ""
         echo "$horizontalRule"
         echo "$curlResult" | sed 's/^/    /g'
         echo "$horizontalRule"
         echo ""
       else
         echo "the required DNS CNAME record is missing, see above"
       fi
     fi
   
     if [ "$shardsFoundCount" -ge "$edgeCount" ]; then
       echo -n "$success $hostname passes shard validation for the following $shardsFoundCount edge shards:"
       echo -e "$shardsFoundOutput"
       echo
   
       if [ -n "$cnameExists" ] && [ -n "$endToEndTestSucceeded" ]; then
         echo "$horizontalRule"
         echo ""
         echo "  For additional TLS/SSL validation, including detailed browser/client support,"
         echo "  see SSL Labs (click the first IP address if prompted):"
         echo ""
         echo "    $info  $sslLabsUrl"
         echo ""
         echo "  To check DNS propagation around the world, see whatsmydns.net:"
         echo ""
         echo "    $info  DNS A records:     https://whatsmydns.net/#A/$hostname"
         echo "    $info  DNS CNAME record:  https://whatsmydns.net/#CNAME/$hostname"
       fi
     else
       echo -n "$failure $hostname FAILED shard validation -- shards found: $shardsFoundCount," \
         "expected: $edgeCount"
       if bc -l <<< "$(cut -d. -f1,2 <<< "$curlVersion") $curlVersionRequired" 2>/dev/null | grep -q 0; then
         echo -n " -- insufficient curl version installed: $curlVersion, but this script requires curl version" \
           "$curlVersionRequired because it uses the curl --connect-to flag to bypass DNS and directly test" \
           "each Adobe Target edge shards' SNI confirguation for $hostname"
       fi
       if [ -n "$shardsFoundOutput" ]; then
         echo -e ":\n$shardsFoundOutput"
       fi
       echo
     fi
     echo
     echo "$horizontalRule"
     echo
   }
   ```

1. Incolla questo comando (sostituzione `target.example.com` con il tuo nome host):

   ```
   adobeTargetCnameValidation target.example.com
   ```

   Se l&#39;implementazione è pronta, puoi visualizzare l&#39;output come segue. La parte importante è che tutte le linee dello stato di convalida mostrano `✅` piuttosto che `🚫`. Ogni [!DNL Target] la condivisione Edge CNAME deve essere visualizzata `CN=target.example.com`, che corrisponde al nome host principale nel certificato richiesto (i nomi host SAN aggiuntivi nel certificato non vengono stampati in questo output).

   ```
   $ adobeTargetCnameValidation target.example.com
   
   ==========================================================
   
   Adobe Target CNAME implementation validation for hostname target.example.com:
   ✅ target.example.com passes DNS CNAME validation
   ✅ target.example.com passes TLS and HTTP response validation
   ✅ target.example.com passes shard validation for the following 7 edge shards:
   
   ===== ✅ target.example.com [edge shard: mboxedge31-alb02.tt.omtrdc.net] =====
   *  expire date: Jul 22 23:59:59 2022 GMT
   *  issuer: C=US; O=DigiCert Inc; CN=DigiCert TLS RSA SHA256 2020 CA1
   *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   
   ===== ✅ target.example.com [edge shard: mboxedge32-alb02.tt.omtrdc.net] =====
   *  expire date: Jul 22 23:59:59 2022 GMT
   *  issuer: C=US; O=DigiCert Inc; CN=DigiCert TLS RSA SHA256 2020 CA1
   *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   
   ===== ✅ target.example.com [edge shard: mboxedge34-alb02.tt.omtrdc.net] =====
   *  expire date: Jul 22 23:59:59 2022 GMT
   *  issuer: C=US; O=DigiCert Inc; CN=DigiCert TLS RSA SHA256 2020 CA1
   *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   
   ===== ✅ target.example.com [edge shard: mboxedge35-alb02.tt.omtrdc.net] =====
   *  expire date: Jul 22 23:59:59 2022 GMT
   *  issuer: C=US; O=DigiCert Inc; CN=DigiCert TLS RSA SHA256 2020 CA1
   *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   
   ===== ✅ target.example.com [edge shard: mboxedge36-alb02.tt.omtrdc.net] =====
   *  expire date: Jul 22 23:59:59 2022 GMT
   *  issuer: C=US; O=DigiCert Inc; CN=DigiCert TLS RSA SHA256 2020 CA1
   *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   
   ===== ✅ target.example.com [edge shard: mboxedge37-alb02.tt.omtrdc.net] =====
   *  expire date: Jul 22 23:59:59 2022 GMT
   *  issuer: C=US; O=DigiCert Inc; CN=DigiCert TLS RSA SHA256 2020 CA1
   *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   
   ===== ✅ target.example.com [edge shard: mboxedge38-alb02.tt.omtrdc.net] =====
   *  expire date: Jul 22 23:59:59 2022 GMT
   *  issuer: C=US; O=DigiCert Inc; CN=DigiCert TLS RSA SHA256 2020 CA1
   *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   
   ==========================================================
   
     For additional TLS/SSL validation, including detailed browser/client support,
     see SSL Labs (click the first IP address if prompted):
   
       🔎  https://ssllabs.com/ssltest/analyze.html?hideResults=on&latest&d=target.example.com
   
     To check DNS propagation around the world, see whatsmydns.net:
   
       🔎  DNS A records:     https://whatsmydns.net/#A/target.example.com
       🔎  DNS CNAME record:  https://whatsmydns.net/#CNAME/target.example.com
   
   ==========================================================
   ```

   >[!NOTE]
   >
   >Se questo comando di convalida non riesce durante la convalida DNS ma sono già state apportate le modifiche DNS necessarie, potrebbe essere necessario attendere che gli aggiornamenti DNS si propaghino completamente. I record DNS sono associati a un [TTL (time-to-live)](https://en.wikipedia.org/wiki/Time_to_live#DNS_records) che determina il tempo di scadenza della cache per le risposte DNS di tali record. Di conseguenza, potrebbe essere necessario attendere almeno quanto i TTL. È possibile utilizzare `dig target.example.com` comando o [Casella degli strumenti di G Suite](https://toolbox.googleapps.com/apps/dig/#CNAME) per cercare i TTL specifici. Per controllare la propagazione DNS in tutto il mondo, vedi [whatsmydns.net](https://whatsmydns.net/#CNAME).

### Come si utilizza un collegamento di rinuncia con CNAME

Se utilizzi CNAME, il collegamento di rinuncia deve contenere &quot;client=`clientcode` ad esempio:
`https://my.cname.domain/optout?client=clientcode`.

Sostituisci `clientcode` con il tuo codice client, quindi aggiungi il testo o l’immagine da collegare al [URL di rinuncia](https://developer.adobe.com/target/before-implement/privacy/privacy/).

## Limitazioni note

* La modalità Controllo qualità non è persistente quando disponi di CNAME e at.js 1.x perché è basata su un cookie di terze parti. La soluzione consiste nell’aggiungere i parametri di anteprima a ciascun URL a cui accedi. La modalità Controllo qualità è persistente quando si dispone di CNAME e at.js 2.x.
* Quando si utilizza CNAME, è più probabile che la dimensione dell’intestazione del cookie per [!DNL Target] le chiamate aumentano. [!DNL Adobe] consiglia di mantenere la dimensione del cookie sotto gli 8 KB.
