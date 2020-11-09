---
keywords: google;samesite;cookies;chrome 80;ietf
description: Informazioni su Adobe Target e lo standard IETF SameSite introdotto con Google Chrome versione 80.
title: ' i criteri dei cookie di Adobe Target e Google SameSite'
feature: privacy and security
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '2033'
ht-degree: 8%

---


# Criteri per cookie SameSite di Google Chrome

Google inizierà a imporre nuove politiche di cookie per impostazione predefinita per gli utenti che iniziano con Chrome 80, che è previsto per essere rilasciato all&#39;inizio del 2020. Questo articolo spiega tutto ciò che è necessario sapere sulle nuove policy sui cookie SameSite, come [!DNL Adobe Target] supporta queste policy e come puoi utilizzare [!DNL Target] per conformarsi alle nuove policy sui cookie SameSite di Google Chrome.

A partire da Chrome 80, gli sviluppatori web devono specificare esplicitamente quali cookie possono funzionare tra i siti web. Questo è il primo di molti annunci che Google intende fare per migliorare la privacy e la sicurezza sul web.

Dal momento che Facebook è stato sul posto per quanto riguarda la privacy e la sicurezza, altri attori principali come Apple, e ora Google, sono stati rapidi a sfruttare l&#39;opportunità di creare nuove identità come campioni di privacy e sicurezza. Apple ha guidato il pacchetto annunciando le modifiche alle sue politiche sui cookie all&#39;inizio di quest&#39;anno attraverso ITP 2.1 e recentemente, ITP 2.2. In ITP 2.1, Apple blocca completamente i cookie di terze parti e mantiene i cookie creati sul browser per soli sette giorni. In ITP 2.2, i cookie vengono conservati per un solo giorno. L&#39;annuncio di Google non è neanche lontanamente aggressivo come quello di Apple, ma è il primo passo verso lo stesso obiettivo finale. Per ulteriori informazioni sui criteri Apple, consulta [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).

## Cosa sono i cookie e come vengono utilizzati?

Prima di conoscere le modifiche apportate alle politiche sui cookie di Google, è necessario conoscere i cookie e le relative modalità di utilizzo. In poche parole, i cookie sono piccoli file di testo memorizzati nel browser Web che vengono utilizzati per ricordare gli attributi utente.

I cookie sono importanti perché migliorano l&#39;esperienza dell&#39;utente che naviga sul Web. Ad esempio, se effettui acquisti su un sito Web di eCommerce e aggiungi qualcosa al carrello ma non accedi o acquista in quella visita, i cookie memorizzano i tuoi articoli e li conservano nel carrello per la prossima visita. Oppure, immaginate di dover reinserire il vostro nome utente e la password ogni volta che visitate il vostro sito Web social media preferito. Anche i cookie risolvono questo problema, perché memorizzano informazioni che aiutano i siti a identificare chi siete. Questi tipi di cookie sono chiamati cookie di prime parti perché vengono creati e utilizzati dal sito Web visitato.

Esistono anche cookie di terze parti. Per comprenderli meglio, consideriamo questo esempio:

Supponiamo che un&#39;ipotetica società di social media denominata &quot;Amici&quot; fornisca un pulsante Condividi implementato da altri siti per consentire agli utenti di condividere il contenuto del sito sul feed Amici. Ora, un utente legge un articolo di notizie su un sito Web di notizie che utilizza il pulsante Condividi e fa clic su di esso per pubblicare automaticamente il proprio account Amici.

A tal fine, il browser recupera il pulsante Condivisione amici da `platform.friends.com` quando viene caricato l’articolo della notizia. In questo processo, il browser allega i cookie Friends, che contengono le credenziali di accesso dell&#39;utente, alla richiesta ai server Friends. Questo consente agli amici di pubblicare l’articolo nel proprio feed per conto dell’utente senza che l’utente debba effettuare l’accesso.

Tutto ciò è possibile utilizzando cookie di terze parti. In questo caso, il cookie di terza parte viene salvato nel browser per `platform.friends.com`, in modo che `platform.friends.com` possa pubblicare il post nell’app Amici per conto dell’utente.

Se si immagina per un momento come ottenere questo caso d&#39;uso senza cookie di terze parti, l&#39;utente dovrebbe seguire molti passaggi manuali. In primo luogo, l’utente deve copiare il collegamento all’articolo della notizia. In secondo luogo, l&#39;utente dovrebbe accedere all&#39;app Amici separatamente. Quindi, l&#39;utente faceva clic sul pulsante Crea post. Quindi l&#39;utente copiava e incollava il collegamento nel campo di testo, quindi faceva clic su Post. Come si può vedere, i cookie di terze parti aiutano enormemente l&#39;utente a sperimentare come i passaggi manuali possono essere drasticamente ridotti.

Più in generale, i cookie di terze parti consentono di memorizzare i dati nel browser dell&#39;utente senza che tale utente debba esplicitamente visitare un sito Web.

## Problemi di sicurezza

Anche se i cookie migliorano le esperienze utente e la pubblicità di potenza, possono anche introdurre vulnerabilità di sicurezza come attacchi CSRF (Cross-Site Request Forgery). Ad esempio, se un utente accede a un sito bancario per pagare le fatture della carta di credito e lascia il sito senza disconnettersi e poi naviga in un sito dannoso nella stessa sessione, si può verificare un attacco CSRF. Il sito dannoso potrebbe includere codice che invia una richiesta al sito bancario che viene eseguito al caricamento della pagina. Poiché l&#39;utente è ancora autenticato nel sito bancario, il cookie di sessione può essere utilizzato per avviare un attacco CSRF per avviare un evento di trasferimento di fondi dal conto bancario dell&#39;utente. Questo perché ogni volta che visitate un sito, tutti i cookie vengono allegati nella richiesta HTTP. E a causa di questi problemi di sicurezza, Google sta cercando di mitigarli.

## In che modo Target utilizza i cookie?

Detto questo, vediamo come [!DNL Target] utilizzano i cookie. Per poter essere utilizzato [!DNL Target] in primo luogo, è necessario installare la libreria [!DNL Target] JavaScript sul sito. Questo consente di inserire un cookie di prima parte nel browser dell&#39;utente che visita il sito. Quando l&#39;utente interagisce con il sito Web, è possibile trasmettere i dati comportamentali e di interesse dell&#39;utente [!DNL Target] tramite la libreria JavaScript. La libreria [!DNL Target] JavaScript utilizza cookie di prime parti per estrarre informazioni identificative sull&#39;utente da mappare ai dati di comportamento e interesse dell&#39;utente. Questi dati vengono quindi utilizzati [!DNL Target] per potenziare le attività di personalizzazione.

Target utilizza anche (a volte) cookie di terze parti. Se possedete più siti Web che vivono su domini diversi e desiderate monitorare il percorso utente attraverso tali siti, potete utilizzare cookie di terze parti sfruttando il monitoraggio tra domini diversi. Attivando il tracciamento tra domini nella libreria [!DNL Target] JavaScript, l&#39;account inizierà a utilizzare cookie di terze parti. Quando un utente passa da un dominio all’altro, il browser comunica con il server di back-end di [!DNL Target]e, in questo processo, viene creato e inserito nel browser dell’utente un cookie di terza parte. Grazie al cookie di terze parti presente nel browser dell&#39;utente, [!DNL Target] è possibile fornire un&#39;esperienza coerente tra domini diversi per un singolo utente.

## La nuova ricetta di cookie di Google

Per fornire protezione in caso di invio di cookie tra siti in modo da proteggere gli utenti, Google pianifica di aggiungere il supporto per uno standard IETF denominato SameSite, che richiede agli sviluppatori Web di gestire i cookie con il componente attributo SameSite nell’intestazione Set-Cookie.

Tre valori diversi possono essere passati nell’attributo SameSite: Strict, Lax o None (Rigoroso, Tollerante, Nessuno).

| Valore | Descrizione |
| --- | --- |
| Strict (Rigoroso) | I cookie con questa impostazione sono accessibili solo quando si visita il dominio in cui sono stati inizialmente impostati. In altre parole, Strict impedisce completamente che il cookie possa essere utilizzato tra siti diversi. Questa opzione è ideale per le applicazioni che richiedono elevata sicurezza, come le banche. |
| Lax (Tollerante) | Cookies with this setting are sent only on same-site requests or top-level navigation with non-idempotent HTTP requests, like `HTTP GET`. Pertanto, questa opzione viene utilizzata se il cookie può essere utilizzato da terzi, ma con un vantaggio in termini di sicurezza che protegge gli utenti da attacchi CSRF. |
| None (Nessuno) | I cookie con questa impostazione funzioneranno come i cookie di oggi. |

Tenendo presente quanto sopra, Chrome 80 introduce due impostazioni indipendenti per gli utenti: &quot;Per impostazione predefinita, SameSite cookie&quot; e &quot;Cookies senza SameSite devono essere protetti.&quot; Queste impostazioni verranno abilitate per impostazione predefinita in Chrome 80.

![StessoSito, finestra di dialogo](/help/c-implementing-target/c-considerations-before-you-implement-target/assets/samesite.png)

* **SameSite per cookie** predefiniti: Se impostato, tutti i cookie che non specificano l&#39;attributo SameSite saranno automaticamente costretti a utilizzare `SameSite = Lax`.
* **I cookie senza SameSite devono essere protetti**: Se impostati, i cookie senza l&#39;attributo SameSite o con `SameSite = None` necessità di essere protetti. In questo contesto, protetto significa che tutte le richieste del browser devono seguire il protocollo HTTPS. I cookie che non aderiscono a questo requisito vengono rifiutati. Tutti i siti Web devono utilizzare HTTPS per soddisfare questo requisito.

## Target segue le best practice di sicurezza di Google

Ad  Adobe, desideriamo sempre supportare le ultime best practice del settore per la sicurezza e la privacy. We are happy to announce that [!DNL Target] supports the new security and privacy settings introduced by Google.

Per l&#39;impostazione &quot;SameSite by default cookies&quot;, [!DNL Target] continuerà a fornire la personalizzazione senza alcun impatto e intervento da parte tua. [!DNL Target] utilizza i cookie di prima parte che continueranno a funzionare correttamente in quanto il flag `SameSite = Lax` viene applicato da Google Chrome.

Per l&#39;opzione &quot;Cookie senza SameSite devono essere protetti&quot;, se non si opta per la funzione di tracciamento tra domini in [!DNL Target], i cookie di prime parti in [!DNL Target] continueranno a funzionare.

However, when you opt-in to use cross-domain tracking to leverage [!DNL Target] across multiple domains, Chrome requires `SameSite = None` and Secure flags to be used for third-party cookies. Ciò significa che è necessario assicurarsi che i siti utilizzino il protocollo HTTPS. Le librerie lato client in [!DNL Target] utilizzeranno automaticamente il protocollo HTTPS e allegheranno i flag `SameSite = None` e Secure ai cookie di terze parti in [!DNL Target] modo da garantire che tutte le attività continuino a distribuire.

## Cosa devi fare?

Per capire cosa devi fare per avere [!DNL Target] continuare a lavorare per gli utenti Google Chrome 80+, consulta la tabella di seguito, di cui vedrai le seguenti colonne:

* **Libreria** JavaScript di destinazione: Se utilizzate mbox.js, at.js 1.*x* o at.js 2.*x* sui siti.
* **SameSite per cookie predefiniti = Enabled**: Se i vostri utenti dispongono di &quot;SameSite by default cookies&quot; abilitati, in che modo vi interessa ed è presente tutto ciò che dovete fare per [!DNL Target] continuare a funzionare.
* **I cookie senza SameSite devono essere protetti = Abilitati**: Se gli utenti dispongono di &quot;Cookies senza SameSite deve essere protetto&quot; abilitato, in che modo ciò influirà su di voi ed è presente tutto ciò che è necessario fare per [!DNL Target] continuare a funzionare.

| Libreria JavaScript di destinazione | “SameSite by default cookies” = Abilitato | “Cookies without SameSite must be secure” = Abilitato |
| --- | --- | --- |
| mbox.js con solo cookie di prime parti. | Nessun impatto. | Nessun impatto se non utilizzi il tracciamento tra domini diversi. |
| mbox.js con il tracciamento tra domini abilitato. | Nessun impatto. | È necessario abilitare il protocollo HTTPS per il sito.<br>[!DNL Target] utilizza un cookie di terze parti per monitorare gli utenti e Google richiede cookie di terze parti per avere `SameSite = None` e il flag Secure. Il flag Secure richiede che i siti utilizzino il protocollo HTTPS. |
| Mappatura payload dei parametri at.js 1.*x* con cookie di prime parti. | Nessun impatto. | Nessun impatto se non utilizzi il tracciamento tra domini diversi. |
| Mappatura payload dei parametri at.js 1.*x* con il tracciamento tra domini abilitato. | Nessun impatto. | È necessario abilitare il protocollo HTTPS per il sito.<br>[!DNL Target] utilizza un cookie di terze parti per monitorare gli utenti e Google richiede cookie di terze parti per avere `SameSite = None` e il flag Secure. Il flag Secure richiede che i siti utilizzino il protocollo HTTPS. |
| Payload JSON di at.js 2.*x* | Nessun impatto. | Nessun impatto. |

## Cosa deve fare Target?

Quindi, cosa abbiamo dovuto fare nella nostra piattaforma per aiutarti a rispettare le nuove politiche Google Chrome 80+ SameSite cookie?

| Libreria JavaScript di destinazione | “SameSite by default cookies” = Abilitato | “Cookies without SameSite must be secure” = Abilitato |
| --- | --- | --- |
| mbox.js con solo cookie di prime parti. | Nessun impatto. | Nessun impatto se non utilizzi il tracciamento tra domini diversi. |
| mbox.js con il tracciamento tra domini abilitato. | Nessun impatto. | [!DNL Target] aggiunge `SameSite = None` e protegge il flag al cookie di terza parte quando [!DNL Target] i server vengono chiamati. |
| Mappatura payload dei parametri at.js 1.*x* con cookie di prime parti. | Nessun impatto. | Nessun impatto se non utilizzi il tracciamento tra domini diversi. |
| Mappatura payload dei parametri at.js 1.*x* con il tracciamento tra domini abilitato. | Nessun impatto. | Mappatura payload dei parametri at.js 1.*x* con il tracciamento tra domini abilitato. |
| Payload JSON di at.js 2.*x* | Nessun impatto. | Nessun impatto. |

## Qual è l&#39;impatto se non passate all&#39;uso del protocollo HTTPS?

L’unico caso d’uso che può avere un impatto è l’utilizzo della funzione di tracciamento tra domini in [!DNL Target] mbox.js o at.js 1.*x*. Senza passare a HTTPS, che è un requisito di Google, vedrete un picco di visitatori unici nei vostri domini, perché il cookie di terza parte che usiamo sarà rilasciato da Google. E poiché il cookie di terza parte verrà eliminato, [!DNL Target] non sarà in grado di fornire un&#39;esperienza coerente e personalizzata per quell&#39;utente mentre l&#39;utente passa da un dominio all&#39;altro. Il cookie di terza parte viene utilizzato principalmente per identificare un singolo utente che naviga tra i domini di cui disponete.

## Conclusione

Poiché il settore fa passi avanti per creare un web più sicuro per i consumatori, [!DNL Adobe] è assolutamente impegnato ad aiutare i nostri clienti a fornire esperienze personalizzate in modo da garantire la sicurezza e la privacy per gli utenti finali. Tutto quello che devi fare è seguire le best practice di cui sopra e sfruttare [!DNL Target] per conformarsi alle nuove Regole Cookie StessoSite di Google Chrome.
