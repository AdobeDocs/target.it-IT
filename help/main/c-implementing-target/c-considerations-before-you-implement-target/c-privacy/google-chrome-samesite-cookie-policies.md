---
keywords: google;samesite;cookie;chrome 80;ietf
description: Scopri come Adobe [!DNL Target] gestisce lo standard SameSite IETF introdotto con Google Chrome versione 80 e ciò che è necessario fare per rispettare questi criteri.
title: Come funziona [!DNL Target] Gestire le politiche dei cookie Samesite di Google?
feature: Privacy & Security
role: Developer
exl-id: 5abd2065-3692-4a6d-9ac9-6d416604c2d2
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '1948'
ht-degree: 7%

---

# Criteri per cookie SameSite di Google Chrome

Google inizierà a imporre nuovi criteri per i cookie per impostazione predefinita per gli utenti che iniziano con Chrome 80, che verrà rilasciato all&#39;inizio del 2020. Questo articolo spiega tutto ciò di cui hai bisogno per conoscere i nuovi criteri per i cookie SameSite e come [!DNL Adobe Target] supporta questi criteri e come utilizzare [!DNL Target] per rispettare i nuovi criteri per cookie SameSite di Google Chrome.

A partire da Chrome 80, gli sviluppatori web devono specificare esplicitamente quali cookie possono funzionare tra siti web diversi. Questo è il primo di molti annunci che Google prevede di fare per migliorare la privacy e la sicurezza sul web.

Dato che Facebook è stato sul posto per quanto riguarda la privacy e la sicurezza, altri importanti attori come Apple, e ora Google, sono stati rapidi a sfruttare l&#39;opportunità di creare nuove identità come campioni di privacy e sicurezza. Apple ha guidato il pacchetto annunciando all’inizio di quest’anno le modifiche ai suoi cookie policy tramite ITP 2.1 e recentemente ITP 2.2. In ITP 2.1, Apple blocca completamente i cookie di terze parti e conserva i cookie creati sul browser per soli sette giorni. In ITP 2.2, i cookie vengono conservati per un solo giorno. L’annuncio di Google non è altrettanto aggressivo di quello di Apple, ma è il primo passo verso lo stesso obiettivo finale. Per ulteriori informazioni sui criteri di Apple, vedi [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/main/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).

## Cosa sono i cookie e come vengono utilizzati?

Prima di conoscere le modifiche apportate ai criteri dei cookie da Google, è necessario verificare quali sono i cookie e come vengono utilizzati. In parole povere, i cookie sono piccoli file di testo memorizzati nel browser web che vengono utilizzati per ricordare gli attributi utente.

I cookie sono importanti perché migliorano l’esperienza dell’utente quando naviga sul web. Ad esempio, se effettui acquisti su un sito web eCommerce e aggiungi qualcosa al carrello ma non accedi o acquista in quella visita, i cookie ricordano i tuoi articoli e li tengono nel carrello per la tua prossima visita. Oppure, immagina di essere stato costretto a reinserire il tuo nome utente e password ogni volta che visiti il tuo sito web preferito di social media. Anche i cookie risolvono questo problema, perché memorizzano informazioni che aiutano i siti a identificare chi siete. Questi cookie sono chiamati cookie di prime parti perché vengono creati e utilizzati dal sito web visitato.

Esistono anche i cookie di terze parti. Per comprenderli meglio, consideriamo questo esempio:

Supponiamo che un&#39;ipotetica società di social media denominata &quot;Amici&quot; fornisca un pulsante Condividi implementato da altri siti per consentire agli utenti di amici di condividere i contenuti del sito sul feed Amici. Ora, un utente legge un articolo su un sito web di notizie che utilizza il pulsante Condividi e lo fa clic per pubblicare automaticamente sul proprio account Amici.

Per questo motivo, il browser recupera il pulsante Condivisione amici da `platform.friends.com` quando l&#39;articolo è caricato. All’interno di questo processo, il browser allega i cookie Friends, che contengono le credenziali di accesso dell’utente, alla richiesta ai server Friends. Questo consente agli amici di pubblicare l’articolo nel proprio feed per conto dell’utente senza richiedere all’utente di effettuare l’accesso.

Tutto ciò è possibile utilizzando cookie di terze parti. In questo caso, il cookie di terze parti viene salvato nel browser per `platform.friends.com`, affinché `platform.friends.com` può creare il post nell’app Amici per conto dell’utente.

Se immaginate per un momento come ottenere questo caso d’uso senza cookie di terze parti, l’utente dovrebbe seguire molti passaggi manuali. In primo luogo, l&#39;utente dovrebbe copiare il link all&#39;articolo della notizia. In secondo luogo, l’utente dovrebbe accedere all’app Amici separatamente. Quindi, l&#39;utente faceva clic sul pulsante Crea post . Quindi l&#39;utente copiava e incolla il collegamento nel campo di testo, e infine clicca su Post. Come puoi vedere, i cookie di terze parti aiutano enormemente l’esperienza dell’utente in quanto i passaggi manuali possono essere drasticamente ridotti.

Più in generale, i cookie di terze parti consentono di memorizzare i dati sul browser di un utente senza richiedere all’utente di visitare esplicitamente un sito web.

## Problemi di sicurezza

Anche se i cookie migliorano le esperienze degli utenti e la pubblicità dei contenuti, possono anche introdurre vulnerabilità di sicurezza come attacchi CSRF (Cross-Site Request Forgery). Ad esempio, se un utente accede a un sito bancario per pagare le fatture delle carte di credito e lascia il sito senza disconnettersi e poi accede a un sito dannoso nella stessa sessione, può verificarsi un attacco CSRF. Il sito dannoso potrebbe includere codice che invia una richiesta al sito bancario che viene eseguito al caricamento della pagina. Poiché l’utente è ancora autenticato nel sito bancario, il cookie di sessione può essere utilizzato per avviare un attacco CSRF per avviare un evento di trasferimento di fondi dal conto bancario dell’utente. Questo perché ogni volta che visiti un sito, tutti i cookie vengono allegati nella richiesta HTTP. E a causa di questi problemi di sicurezza, Google sta cercando di mitigarli.

## Come funziona [!DNL Target] utilizzare i cookie?

Detto questo, vediamo come [!DNL Target] utilizza i cookie. Per utilizzare [!DNL Target] in primo luogo, è necessario installare il [!DNL Target] Libreria JavaScript sul sito. Questo consente di inserire un cookie di prima parte nel browser dell’utente che visita il sito. Quando l’utente interagisce con il sito web, puoi trasmettere i dati comportamentali e di interesse dell’utente a [!DNL Target] tramite la libreria JavaScript. La [!DNL Target] La libreria JavaScript utilizza cookie di prime parti per estrarre informazioni di identificazione sull’utente da mappare ai dati di comportamento e interesse dell’utente. Questi dati vengono quindi utilizzati da [!DNL Target] per potenziare le attività di personalizzazione.

Target utilizza anche (a volte) cookie di terze parti. Se possiedi più siti web che vivono su domini diversi e desideri tenere traccia del percorso di utenti su tali siti web, puoi utilizzare i cookie di terze parti sfruttando il tracciamento tra domini diversi. Attivando il tracciamento tra più domini nel [!DNL Target] Libreria JavaScript, il tuo account inizierà a utilizzare cookie di terze parti. Quando un utente passa da un dominio all’altro, il browser comunica con il server back-end di [!DNL Target]e in questo processo viene creato e inserito un cookie di terze parti sul browser dell’utente. Tramite il cookie di terze parti presente nel browser dell’utente, [!DNL Target] è in grado di fornire un&#39;esperienza coerente tra domini diversi per un singolo utente.

## Nuova ricetta di cookie di Google

Per garantire la protezione quando i cookie vengono inviati tra siti diversi in modo da proteggere gli utenti, Google prevede di aggiungere il supporto per uno standard IETF denominato SameSite, che richiede agli sviluppatori web di gestire i cookie con il componente attributo SameSite nell’intestazione Set-Cookie.

Tre valori diversi possono essere passati nell’attributo SameSite: Strict, Lax o None (Rigoroso, Tollerante, Nessuno).

| Valore | Descrizione |
| --- | --- |
| Strict (Rigoroso) | I cookie con questa impostazione sono accessibili solo quando si visita il dominio in cui sono stati inizialmente impostati. In altre parole, Strict impedisce completamente che il cookie possa essere utilizzato tra siti diversi. Questa opzione è ideale per le applicazioni che richiedono elevata sicurezza, come le banche. |
| Lax (Tollerante) | I cookie con questa impostazione vengono inviati solo su richieste dello stesso sito o nella navigazione di livello superiore con richieste HTTP non idempotenti, come `HTTP GET`. Pertanto, questa opzione viene utilizzata se il cookie può essere utilizzato da terze parti, ma con un ulteriore vantaggio in termini di sicurezza che protegge gli utenti dal essere vittime degli attacchi CSRF. |
| None (Nessuno) | I cookie con questa impostazione funzioneranno come i cookie di oggi. |

Tenendo presente quanto sopra, Chrome 80 introduce due impostazioni indipendenti per gli utenti: &quot;SameSite by default cookies&quot; e &quot;Cookies without SameSite must be secure&quot; devono essere protetti.&quot; Queste impostazioni saranno abilitate per impostazione predefinita in Chrome 80.

![Finestra di dialogo SameSite](/help/main/c-implementing-target/c-considerations-before-you-implement-target/assets/samesite.png)

* **Cookie SameSite per impostazione predefinita**: Con questa impostazione, tutti i cookie che non specificano l’attributo SameSite verranno automaticamente costretti a utilizzare `SameSite = Lax`.
* **I cookie senza SameSite devono essere protetti**: Con questa impostazione, i cookie privi dell’attributo SameSite o con `SameSite = None` devono essere sicure. In questo contesto, protetto significa che tutte le richieste del browser devono seguire il protocollo HTTPS. I cookie che non aderiscono a questo requisito vengono rifiutati. Per soddisfare questo requisito, tutti i siti web devono utilizzare HTTPS.

## Target segue le best practice di sicurezza di Google

Ad Adobe, desideriamo sempre supportare le ultime best practice del settore per la sicurezza e la privacy. Siamo felici di annunciare che [!DNL Target] supporta le nuove impostazioni di protezione e privacy introdotte da Google.

Per l’impostazione &quot;SameSite by default cookies&quot; (Cookie SameSite per impostazione predefinita), [!DNL Target] continuerà a fornire personalizzazione senza alcun impatto e intervento da parte tua. [!DNL Target] utilizza i cookie di prima parte che continueranno a funzionare correttamente in quanto il flag `SameSite = Lax` viene applicato da Google Chrome.

Per l’opzione &quot;Cookies without SameSite must be secure&quot;, se non si opta per la funzione di tracciamento tra domini diversi in [!DNL Target], i cookie di prime parti in [!DNL Target] continuerà a lavorare.

Tuttavia, quando scegli di utilizzare il tracciamento tra più domini per sfruttare [!DNL Target] tra più domini, Chrome richiede `SameSite = None` e flag Secure da utilizzare per i cookie di terze parti. Ciò significa che devi assicurarti che i tuoi siti utilizzino il protocollo HTTPS. Librerie lato client in [!DNL Target] utilizzerà automaticamente il protocollo HTTPS e allegherà il `SameSite = None` e flag Secure ai cookie di terze parti in [!DNL Target] per garantire che tutte le attività continuino a essere eseguite.

## Cosa devi fare?

Per capire cosa devi fare per avere [!DNL Target] continua a funzionare per gli utenti di Google Chrome 80+, consulta la tabella seguente, di cui vedrai le seguenti colonne:

* **Libreria JavaScript di Target**: Se utilizzi at.js 1.*x* o at.js 2.*x* sui siti.
* **SameSite per cookie predefiniti = Abilitato**: Se i tuoi utenti dispongono di &quot;SameSite by default cookies&quot; abilitato, quale impatto ha su di te ed è disponibile tutto ciò che devi fare per [!DNL Target] per continuare a lavorare.
* **I cookie senza SameSite devono essere protetti = Abilitati**: Se gli utenti dispongono dell’opzione &quot;Cookies without SameSite must be secure&quot;, quale impatto ha su di te ed è disponibile qualsiasi operazione da eseguire per [!DNL Target] continua a lavorare.

| Libreria JavaScript di Target | “SameSite by default cookies” = Abilitato | “Cookies without SameSite must be secure” = Abilitato |
| --- | --- | --- |
| Mappatura payload dei parametri at.js 1.*x* con cookie di prime parti. | Nessun impatto. | Nessun impatto se non utilizzi il tracciamento tra domini diversi. |
| Mappatura payload dei parametri at.js 1.*x* con il tracciamento tra domini diversi abilitato. | Nessun impatto. | Devi abilitare il protocollo HTTPS per il tuo sito.<br>[!DNL Target] utilizza un cookie di terze parti per tenere traccia degli utenti e Google richiede che i cookie di terze parti abbiano `SameSite = None` e flag Secure. Il flag Secure richiede che i siti utilizzino il protocollo HTTPS. |
| Payload JSON di at.js 2.*x* | Nessun impatto. | Nessun impatto. |

## Cosa fa? [!DNL Target] Devo fare?

Quindi, cosa abbiamo dovuto fare nella nostra piattaforma per aiutarti a rispettare i nuovi criteri per i cookie SameSite di Google Chrome 80+?

| Libreria JavaScript di Target | “SameSite by default cookies” = Abilitato | “Cookies without SameSite must be secure” = Abilitato |
| --- | --- | --- |
| Mappatura payload dei parametri at.js 1.*x* con cookie di prime parti. | Nessun impatto. | Nessun impatto se non utilizzi il tracciamento tra domini diversi. |
| Mappatura payload dei parametri at.js 1.*x* con il tracciamento tra domini diversi abilitato. | Nessun impatto. | Mappatura payload dei parametri at.js 1.*x* con il tracciamento tra domini diversi abilitato. |
| Payload JSON di at.js 2.*x* | Nessun impatto. | Nessun impatto. |

## Qual è l’impatto se non passi all’utilizzo del protocollo HTTPS?

L’unico caso d’uso che influisce su di te è l’utilizzo della funzione di tracciamento tra più domini in [!DNL Target] da at.js 1.*x*. Senza passare a HTTPS, un requisito di Google, vedrai un picco di visitatori univoci nei tuoi domini perché il cookie di terze parti utilizzato verrà rilasciato da Google. E poiché il cookie di terze parti verrà eliminato, [!DNL Target] non sarà in grado di fornire un&#39;esperienza coerente e personalizzata per quell&#39;utente mentre l&#39;utente si sposta da un dominio all&#39;altro. Il cookie di terze parti viene utilizzato principalmente per identificare un singolo utente che naviga tra i domini che possiedi.

## Conclusione

Come il settore fa grandi progressi nella creazione di un web più sicuro per i consumatori, [!DNL Adobe] è assolutamente impegnato ad aiutare i nostri clienti a fornire esperienze personalizzate in modo da garantire sicurezza e privacy agli utenti finali. Tutto quello che devi fare è seguire le best practice di cui sopra e sfruttare [!DNL Target] per rispettare i nuovi criteri per cookie SameSite di Google Chrome.
