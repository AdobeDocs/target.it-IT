---
keywords: faq at.js;domande frequenti at.js;faq;visualizzazione temporanea;caricatore;caricatore pagina;cross domain;dimensione file;dimensioni file;dominio x;at.js e mbox.js;solo x;diversi domini;safari;app a pagina singola;selettori mancanti;selettori;applicazione a pagina singola;tt.omtrdc.net;spa;Adobe Experience Manager;AEM;indirizzo ip;httponly;Httponly;protetto;ip;dominio cookie
description: Risposte alle domande frequenti sulla libreria JavaScript at.js di Adobe  [!DNL Target] .
title: Quali sono le domande più comuni su at.js, e le relative risposte?
feature: at.js
role: Developer
exl-id: 937f880a-1842-4655-be44-0a5614c2dbcc
source-git-commit: b1e8ea2370fc15f4bfcd960ab2960cafe2db92b8
workflow-type: tm+mt
source-wordcount: '2586'
ht-degree: 96%

---

# Domande frequenti su at.js

Risposte alle domande frequenti sulla libreria JavaScript at.js di [!DNL Adobe Target].

## Quali vantaggi offre at.js rispetto a mbox.js? {#section_FE30D01A577C46ACB0F787B85F5E0F6B}

La libreria [!DNL at.js] sostituisce [!DNL mbox.js]. La libreria [!DNL mbox.js] non è più supportata. Tuttavia, per la maggior parte delle persone, [!DNL at.js] offre vantaggi rispetto a [!DNL mbox.js].

Ad esempio, [!DNL at.js] migliora i tempi di caricamento delle pagine per le implementazioni web, migliora la sicurezza e fornisce migliori opzioni di implementazione per le applicazioni a pagina singola.

Nella figura seguente vengono illustrate le prestazioni di caricamento delle pagine utilizzando mbox.js e at.js.

![](assets/atjs_vesus_mboxjs.png)

Come illustrato in precedenza, utilizzando mbox.js il contenuto della pagina inizia a caricarsi solo una volta completata la richiesta di [!DNL Target]. Utilizzando at.js, il contenuto della pagina comincia a caricarsi quando viene avviata la richiesta di [!DNL Target], senza attenderne il completamento.

## Qual è l’impatto di at.js e mbox.js sui tempi di caricamento delle pagine? {#page-load}

Molti clienti e consulenti vogliono conoscere l&#39;impatto di [!DNL at.js] e di [!DNL mbox.js] sul tempo di caricamento delle pagine, soprattutto nel contesto di nuovi utenti rispetto a utenti di ritorno. Purtroppo, è difficile misurare e offrire numeri concreti per quanto riguarda l&#39;influenza di [!DNL at.js] o [!DNL mbox.js] sul tempo di caricamento della pagina, a causa delle implementazioni del singolo cliente.

Tuttavia, se sulla pagina è presente l&#39;API Visitor, [!DNL Target] può capire meglio in che modo [!DNL at.js] e [!DNL mbox.js] influenzano il tempo di caricamento delle pagine.

>[!NOTE]
>
>L’API dei visitatori e [!DNL at.js] o [!DNL mbox.js] hanno un impatto sul tempo di caricamento della pagina solo quando si utilizza la mbox globale (a causa della tecnica di celamento del corpo). Le mbox regionali non sono influenzate dall&#39;integrazione delle API dei visitatori.

Le sezioni seguenti illustrano la sequenza di azioni per i visitatori nuovi e per i visitatori di ritorno:

### Visitatori nuovi

1. L&#39;API dei visitatori viene caricata, analizzata ed eseguita.
1. at.js / mbox.js è caricato, analizzato ed eseguito.
1. Se la creazione automatica della mbox globale è abilitata, la libreria JavaScript di Target:

   * Crea un&#39;istanza dell&#39;oggetto Visitatore.
   * La libreria di [!DNL Target] tenta di recuperare i dati di [!DNL Experience Cloud Visitor ID].
   * Poiché si tratta di un nuovo visitatore, l’API Visitor genera una richiesta cross-domain a demdex.net.
   * Dopo il recupero dei dati di [!DNL Experience Cloud Visitor ID], viene avviata una richiesta a [!DNL Target].

### Visitatori di ritorno

1. L&#39;API dei visitatori viene caricata, analizzata ed eseguita.
1. at.js / mbox.js è caricato, analizzato ed eseguito.
1. Se la creazione automatica della mbox globale è abilitata, la libreria JavaScript di [!DNL Target]:

   * Crea un&#39;istanza dell&#39;oggetto Visitatore.
   * La libreria di [!DNL Target] tenta di recuperare i dati di [!DNL Experience Cloud Visitor ID].
   * L&#39;API dei visitatori recupera i dati dai cookie.
   * Dopo il recupero dei dati di [!DNL Experience Cloud Visitor ID], viene avviata una richiesta a [!DNL Target].

>[!NOTE]
>
>Per i nuovi visitatori, quando è presente l’API Visitor, [!DNL Target] deve connettersi più volte per assicurare che la richiesta [!DNL Target] includa i dati di [!DNL Experience Cloud Visitor ID]. Per i visitatori di ritorno, [!DNL Target] si connette a [!DNL Target] solo per recuperare il contenuto personalizzato.

## Perché mi sembra di notare tempi di risposta più lenti dopo l’aggiornamento da una versione precedente di at.js alla versione 1.0.0? {#section_DFBA5854FFD142B49AD87BFAA09896B0}

[!DNL at.js] versione 1.0.0 o successiva attiva tutte le richieste in parallelo. Le versioni precedenti eseguono le richieste in modo sequenziale, ovvero le richieste formano una coda e [!DNL Target] aspetta il completamento della richiesta corrente prima di passare alla successiva.

Il modo in cui le versioni precedenti di [!DNL at.js] eseguono le richieste è suscettibile al cosiddetto blocco del primo elemento. In [!DNL at.js] 1.0.0 o versione successiva, l’esecuzione delle richieste in avviene in parallelo.[!DNL Target]

Se controlli la cascata delle schede di rete di [!DNL at.js] 0.9.1, ad esempio, vedrai che la successiva richiesta di si avvia solo dopo che la precedente è stata completata. [!DNL Target] Diverso è il caso con [!DNL at.js] 1.0.0 e versioni successive, dove tutte le richieste partono essenzialmente nello stesso momento.

Per quanto riguarda il tempo di risposta, la sequenza può essere riassunta così:

<ul class="simplelist"> 
 <li> at.js 0.9.1: Tempo di risposta di tutti [!DNL Target] requests = somma dei tempi di risposta delle richieste </li> 
 <li> at.js 1.0.0 e versioni successive: Tempo di risposta di tutti [!DNL Target] requests = tempo di risposta massimo richieste </li> 
</ul>

La libreria [!DNL at.js] versione 1.0.0 completa le richieste più rapidamente. Inoltre, le richieste di [!DNL at.js] sono asincrone, pertanto non blocca il rendering della pagina. [!DNL Target] Anche se il completamento delle richieste impiega qualche secondo, la pagina renderizzata sarà comunque visibile, anche se alcune parti della pagina resteranno vuote finché [!DNL Target] non avrà ricevuto una risposta dal server Edge di [!DNL Target].

## È possibile caricare la libreria di [!DNL Target] in modo asincrono? {#section_AB9A0CA30C5440C693413F1455841470}

La versione di at.js 1.0.0 permette di caricare la libreria di [!DNL Target] in modo asincrono.

Per caricare at.js in modo asincrono:

* L’approccio consigliato è tramite tag in [!DNL Adobe Experience Platform].
* Puoi anche caricare at.js in modo asincrono aggiungendo l’attributo async al tag script che carica at.js. Ad esempio, puoi usare un codice simile al seguente:

   ```
   <script src="<URL to at.js>" async></script>
   ```

* Puoi anche caricare at.js in modo asincrono utilizzando questo codice:

   ```
   var script = document.createElement('script'); 
   script.async = true; 
   script.src = "<URL to at.js>"; 
   document.head.appendChild(script);
   ```

Caricare at.js in modo asincrono è un ottimo modo per evitare di bloccare il rendering del browser; tuttavia, questa tecnica può portare alla visualizzazione momentanea di altri contenuti della pagina web.

Puoi evitare sfarfallii utilizzando uno snippet che nasconde preventivamente la pagina (o specifiche porzioni), quindi la rivela dopo il caricamento di at.js e della richiesta globale. Lo snippet deve essere aggiunto prima del caricamento di at.js.

Se distribuisci at.js tramite un’implementazione asincrona di [!DNL Adobe Experience Platform], assicurati di includere lo snippet per nascondere le pagine direttamente, prima di implementare [!DNL Target] utilizzando il codice di incorporamento di [!DNL Adobe Experience Platform].

Durante l’implementazione di at.js tramite un’implementazione sincrona di DTM, puoi aggiungere lo snippet tramite una regola di caricamento della pagina attivata nella parte superiore della pagina.

Per ulteriori informazioni, consulta [Gestione at.js della visualizzazione momentanea di altri contenuti](https://developer.adobe.com/target/implement/client-side/atjs/how-atjs-works/manage-flicker-with-atjs/).

## at.js è compatibile con l’integrazione [!DNL Adobe Experience Manager] (Experience Manager)? {#section_6177AE10542344239753764C6165FDDC}

[!DNL Adobe Experience Manager] 6.2 con FP-11577 (o versioni successive) supporta ora le implementazioni di [!DNL at.js] con l’integrazione di [!UICONTROL Adobe Target Cloud Services].

## Come posso evitare la visualizzazione momentanea di altri contenuti al caricamento pagina, utilizzando at.js? {#section_4D78AAAE73C24E578C974743A3C65919}

Target consente di impedire la visualizzazione momentanea di altri contenuti al caricamento della pagina utilizzando uno dei seguenti metodi. Per ulteriori informazioni, consulta [Impedire la visualizzazione momentanea di altri contenuti con at.js](https://developer.adobe.com/target/implement/client-side/atjs/how-atjs-works/manage-flicker-with-atjs/).

## Qual è la dimensione del file di at.js? {#section_6A25C9A14C66441785A7635FEF5C4475}

Il file di at.js che scarichi è approssimativamente 109 KB. Tuttavia, poiché la maggior parte dei server comprime automaticamente i file per renderli di dimensioni più piccole, at.js è circa 34 KB quando è compresso (utilizzando GZIP o un altro metodo) sul server e caricato dagli utenti che visitano il tuo sito. Le impostazioni di compressione sul server in cui è stato installato at.js determinano la dimensione effettiva.

## Perché at.js è più grande di mbox.js? {#section_AA1C43897E46448FA3E26EEC10ED7E51}

Le implementazioni di at.js utilizzano una sola libreria ([!DNL at.js]), mentre quelle di mbox.js usano due librerie ([!DNL mbox.js] e [!DNL target.js]). Quindi un confronto più equo è quello tra at.js e mbox.js *più* `target.js`. Confrontando le dimensioni compresse con GZIP delle due versioni, at.js versione 1.2 è di 34 KB e mbox.js versione 63 è di 26,2 KB. ``

at.js è più grande perché effettua molta più analisi DOM rispetto a mbox.js. Questo è necessario perché at.js ottiene dati “grezzi” dalla risposta JSON e deve interpretarli. mbox.js utilizzava invece `document.write()` ed era il browser a eseguire l’analisi.

Nonostante le dimensioni più grandi del file, i nostri test indicano che le pagine vengono caricate più velocemente con at.js rispetto a mbox.js. Inoltre, at.js è superiore dal punto di vista della sicurezza perché non carica file aggiuntivi in modo dinamico né utilizza `document.write`.

## at.js include jQuery? Posso rimuovere questa parte di at.js se sul mio sito ho già jQuery? {#section_E4604E46E7B34460B8DD6A78D9B476F9}

at.js attualmente utilizza parti di jQuery e quindi vedrai la notifica della licenza MIT nella parte superiore di at.js. jQuery non è esposto e non interferisce con la libreria jQuery che hai già sulla pagina, che potrebbe essere una versione diversa. La rimozione del codice jQuery all’interno di at.js non è supportata.

## at.js supporta Safari e l’attraversamento di più domini impostato su “solo x”? {#section_114EC271A6E045E1B2183B66F1B71285}

No, se l’attraversamento di più domini è impostato su “solo x” e in Safari i cookie di terze parti sono disabilitati, allora sia [!DNL mbox.js] che at.js impostano un cookie disabilitato e non viene eseguita alcuna richiesta mbox per quel particolare dominio del client.

Per supportare i visitatori Safari, un dominio X migliore può essere “disabilitato” (viene impostato solo un cookie di prima parte) o “abilitato” (viene impostato solo un cookie di prima parte su Safari, e cookie di prima e di terze parti su altri browser).

## È possibile utilizzare il Compositore esperienza visivo di [!DNL Target] nelle applicazioni a pagina singola? {#section_459C1BEABD4B4A1AADA6CF4EC7A70DFB}

Sì, puoi utilizzare il Compositore esperienza visivo se utilizzi at.js 2.x. Per maggiori informazioni, consulta [Compositore esperienza visivo per applicazione a singola pagina (SPA)](/help/main/c-experiences/spa-visual-experience-composer.md).

## Posso utilizzare il debugger di [!DNL Adobe Experience Cloud] con le implementazioni di at.js? {#section_FF3CF4C5FD2F4DB1BF1A6B39DA161637}

Sì. È inoltre possibile utilizzare mboxTrace per il debug o gli Strumenti per sviluppatori del browser per controllare le richieste di rete, filtrando “mbox” per isolare le chiamate mbox.

## Posso usare caratteri speciali nei nomi delle mbox con at.js? {#section_8E31D2E8A27642098934D7DACFB2A600}

Sì, come con mbox.js.

## Perché le mie mbox non vengono lanciate sulle mie pagine web? {#section_4BA5DA424B734324AAB51E4588FA50F5}

I [!DNL Target] clienti di utilizzano talvolta istanze basate su cloud con [!DNL Target] per test o semplici prove di concetto. Questi domini, e molti altri, fanno parte dell’[elenco dei suffissi pubblici](https://publicsuffix.org/list/public_suffix_list.dat).

I browser moderni non salvano i cookie se usi questi domini, a meno che non personalizzi l’impostazione `cookieDomain` utilizzando targetGlobalSettings(). Per ulteriori informazioni, consulta [Utilizzo di istanze basate su Cloud con Target](https://developer.adobe.com/target/implement/client-side/target-debugging-atjs/targeting-using-cloud-based-instances/).

## Gli indirizzi IP possono essere utilizzati come dominio dei cookie quando si utilizza at.js? {#section_8BEEC91A3410459D9E442840A3C88AF7}

Sì, se utilizzi [at.js versione 1.2 o successive](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/). [!DNL Adobe] consiglia comunque vivamente di utilizzare sempre l’ultima versione.

>[!NOTE]
>
>Gli esempi seguenti non sono necessari se si utilizza at.js versione 1.2 o successiva.

A seconda di come utilizzi [targetGlobalSettings](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/), potrebbe essere necessario apportare ulteriori modifiche al codice dopo aver scaricato at.js. Ad esempio, se ti servivano impostazioni leggermente diverse per le tue implementazioni di [!DNL Target] su vari siti web e non hai potuto definirle in modo dinamico con JavaScript personalizzato, apporta tali personalizzazioni manualmente dopo aver scaricato il file e prima di caricarlo sul rispettivo sito web.

Gli esempi seguenti consentono di utilizzare la funzione di at.js `targetGlobalSettings()` per inserire uno snippet di codice per supportare gli indirizzi IP:

Esempio per un solo indirizzo IP:

```
if (window.location.hostname === '123.456.78.9') { 
    window.targetGlobalSettings = window.targetGlobalSettings || {}; 
    window.targetGlobalSettings.cookieDomain = window.location.hostname; 
}
```

Esempio per un intervallo di indirizzi IP:

```
if (/^123\.456\.78\..*/g.test(window.location.hostname)) { 
    window.targetGlobalSettings = window.targetGlobalSettings || {}; 
    window.targetGlobalSettings.cookieDomain = window.location.hostname; 
}
```

## Perché ricevo messaggi di avviso, ad esempio “azioni con selettori mancanti”? {#section_C36BED5B16634361A1BA46FCB731489D}

Questi messaggi non sono legati alla funzionalità [!DNL at.js]. La libreria [!DNL at.js] cerca di segnalare tutto ciò che non si trova nel DOM.

Di seguito sono riportate le possibili cause principali per questo messaggio di avviso:

* La pagina viene generata in modo dinamico e at.js non è in grado di trovare l’elemento.
* La pagina viene creata lentamente (a causa di una rete lenta) e at.js non riesce a trovare il selettore nel DOM.
* La struttura di pagina su cui è in esecuzione l’attività[!UICONTROL  è stata modificata. Se riapri l’attività nel ]Compositore esperienza visivo dovrebbe comparire un messaggio di avviso. È necessario aggiornare l’attività in modo che tutti gli elementi necessari possano essere trovati.
* La pagina sottostante fa parte di un’[!UICONTROL applicazione a pagina singola] oppure contiene elementi che appaiono più in basso e il “meccanismo di polling selettivo” di [!DNL at.js] non riesce a trovarli. Può essere utile aumentare il valore di `selectorsPollingTimeout`. Per ulteriori informazioni, consulta [targetGlobalSettings()](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/).
* Qualsiasi metrica di rilevamento dei clic tenta di aggiungersi a ogni pagina, indipendentemente dall’URL su cui è stata impostata la metrica. Anche se innocua, questa situazione fa apparire molti di questi messaggi.

   Per ottenere i migliori risultati, scarica e utilizza l’ultima versione di [!DNL at.js]. Per ulteriori informazioni, consulta [Dettagli della versione di at.js.](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/) e [Scaricare at.js](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-without-a-tag-manager/).

## Le chiamate server di [!DNL Target] sono indirizzate al dominio tt.omtrdc.net: di che si tratta? {#section_999C29940E8B4CAD8A957A6B1D440317}

[!DNL tt.omtrdc.net] è il nome di dominio della rete EDGE di Adobe, utilizzato per ricevere tutte le chiamate server per Target.

## Perché at.js non utilizza sempre i flag dei cookie HttpOnly e Secure? {#section_74527E3B41B54B0A83F217C3E664ED1F}

HttpOnly può essere impostato solo tramite codice basato su server. [!DNL Target]I cookie, come mbox, vengono creati e salvati tramite il codice JavaScript, quindi non può utilizzare il flag di [!DNL Target] cookie HttpOnly. [!DNL Target] utilizza il flag HttpOnly impostato per i cookie di terze parti impostati lato server quando è abilitato l’attraversamento di più domini.

È possibile impostare il flag Secure tramite JavaScript solo se la pagina è stata caricata tramite HTTPS. Se la pagina viene inizialmente caricata tramite HTTP, JavaScript non può impostare questo flag. Inoltre, se viene utilizzato il flag Secure, il cookie sarà disponibile solo nelle pagine HTTPS. Per le pagine caricate tramite HTTPS, [!DNL Target] imposta gli attributi Secure e SameSite=None.

Per garantire che [!DNL Target] possa tracciare correttamente gli utenti e che i cookie siano generati lato client, [!DNL Target] non utilizza nessuno di questi flag, tranne nelle situazioni sopra menzionate.

## Con quale frequenza at.js attiva una richiesta di rete? {#section_57C5235DF7694AF093A845D73EABADFD}

[!DNL Target] esegue tutte le sue decisioni sul lato server. Ciò significa che at.js at.js genera una richiesta di rete ogni volta che la pagina si ricarica o viene richiamata un&#39;API pubblica di at.js.

## Nel migliore dei casi, possiamo aspettarci che l&#39;utente non verifichi effetti visibili sul caricamento della pagina dovuti al fatto che si nasconde, sostituisce e visualizza il contenuto? {#section_CB3C566AD61F417FAC0EC5AC706723EB}

at.js cerca di evitare di nascondere anticipatamente HTML BODY o altri elementi DOM per un periodo di tempo prolungato, ma ciò dipende dalle condizioni di rete e dalla configurazione dell’attività. at.js offre [impostazioni](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/) che è possibile utilizzare per personalizzare lo stile CSS per nascondere il BODY, in modo tale che invece di svuotare l’intero BODY HTML sia possibile nascondere anticipatamente solo alcune parti della pagina. L&#39;aspettativa è che quelle parti contengano elementi DOM che devono essere “personalizzati”.

## Qual è la sequenza di eventi in uno scenario medio in cui un utente si qualifica per un’attività? {#section_56E6F448E901403FB77DF02F44C44452}

La richiesta at.js è un `XMLHttpRequest` asincrono, quindi eseguiamo i seguenti passaggi:

1. La pagina viene caricata.
1. at.js nasconde anticipatamente il BODY HTML. È presente un&#39;impostazione per nascondere anticipatamente un particolare contenitore invece del BODY HTML.
1. La richiesta at.js viene attivata.
1. Una volta ricevuta la risposta di [!DNL Target], [!DNL Target] estrae i selettori CSS.
1. Utilizzando i selettori CSS, [!DNL Target] crea tag STYLE per nascondere anticipatamente gli elementi DOM che saranno personalizzati.
1. Il BODY HTML che nasconde anticipatamente STYLE viene rimosso.
1. [!DNL Target] avvia il polling per gli elementi DOM.
1. Se viene trovato un elemento DOM, [!DNL Target] applica le modifiche DOM e l’elemento che nasconde anticipatamente STYLE viene rimosso.
1. Se gli elementi DOM non vengono trovati, un timeout globale rivela gli elementi per evitare di avere una pagina interrotta.

## Quanto spesso il contenuto della pagina è completamente caricato e visibile quando at.js rivela infine l’elemento che l’attività sta modificando? {#section_01AFF476EFD046298A2E17FE3ED85075}

Considerando lo scenario precedente, quanto spesso il contenuto della pagina è completamente caricato e visibile quando at.js rivela infine l’elemento che l’attività sta modificando? In altre parole, la pagina è completamente visibile ad eccezione del contenuto dell&#39;attività, che viene poi rivelato leggermente dopo il resto del contenuto.

at.js non blocca il rendering della pagina. Un utente potrebbe notare alcune aree vuote nella pagina che rappresentano elementi che verranno personalizzati da [!DNL Target]. Se il contenuto da applicare non contiene molte risorse remote, come SCRIPT o IMG, il rendering dovrebbe essere eseguito rapidamente.

## In che modo una pagina interamente salvata nella cache influirà sullo scenario precedente? Sarebbe più probabile che il contenuto dell’attività diventi visibile notevolmente dopo il caricamento del resto del contenuto della pagina? {#section_CE76335A3E0B41CB8253DEE5E060FCDA}

Se una pagina viene salvata nella cache in una rete CDN vicina alla posizione dell’utente, ma non vicina al server Edge di [!DNL Target], l’utente potrebbe notare alcuni ritardi. I server Edge di [!DNL Target] sono ben distribuiti in tutto il mondo, quindi nella maggior parte dei casi questo non è un problema.

## È possibile che un’immagine protagonista venga visualizzata e poi scambiata dopo un breve ritardo? {#section_C25B07B25B854AAE8DEE1623D0FA62A3}

Considerando lo scenario seguente:

Il timeout di [!DNL Target] è di cinque secondi. Un utente carica una pagina che ha un&#39;attività per personalizzare un&#39;immagine protagonista. at.js invia la richiesta per determinare se c&#39;è un&#39;attività da applicare, ma non è presente una risposta iniziale. Supponiamo che l’utente veda il contenuto regolare dell’immagine principale, perché non è stata ricevuta alcuna risposta da [!DNL Target] sull’esistenza di un’attività associata. Dopo quattro secondi, [!DNL Target] restituisce una risposta con il contenuto dell’attività.

A questo punto, è possibile che la versione alternativa venga mostrata? Perciò dopo quattro secondi, l&#39;immagine protagonista potrebbe essere scambiata e l&#39;utente potrebbe notare questo scambio di immagini?

Inizialmente, l&#39;elemento DOM dell’immagine protagonista è nascosto. Una volta ricevuta una risposta da [!DNL Target], at.js applica le modifiche DOM, come la sostituzione dell’IMG e la visualizzazione dell’immagine principale personalizzata.

## Quale doctype HTML richiede at.js?

at.js richiede il doctype HTML5.

La sintassi è:

`<!DOCTYPE html>`

Il doctype HTML5 assicura che la pagina venga caricata in modalità standard. Durante il caricamento in modalità quirks, alcune API JS dalle quali dipende at.js sono disabilitate. [!DNL Target] disabilita at.js in modalità quirks.
