---
description: Informazioni su Target e lo standard SameSite IETF utilizzato a partire da Google Chrome versione 76.
keywords: google;samesite;cookie;chrome 80;ietf
seo-description: Informazioni su Adobe Target e lo standard IETF SameSite introdotto con Google Chrome versione 80.
seo-title: Criteri dei cookie di Adobe Target e Google SameSite
solution: Target
subtopic: Introduzione
title: Criteri per cookie SameSite di Google Chrome
topic: Standard
uuid: aaeda1e6-7b2c-4a00-b65d-bfc95ea796b5
translation-type: tm+mt
source-git-commit: df40d69676cea586451e3b64b56ef602da91173f

---


# Criteri per cookie SameSite di Google Chrome

Google inizierà a imporre nuove politiche di cookie per impostazione predefinita per gli utenti che iniziano con Chrome 80, che è previsto per essere rilasciato all'inizio del 2020. Questo articolo spiega tutto ciò che è necessario sapere sulle nuove policy sui cookie SameSite, come [!DNL Adobe Target] supporta queste policy e come puoi utilizzare [!DNL Target] per conformarsi alle nuove policy sui cookie SameSite di Google Chrome.

A partire da Chrome 80, gli sviluppatori web devono specificare esplicitamente quali cookie possono funzionare tra i siti web. Questo è il primo di molti annunci che Google intende fare per migliorare la privacy e la sicurezza sul web.

Dal momento che Facebook è stato sul posto per quanto riguarda la privacy e la sicurezza, altri attori principali come Apple, e ora Google, sono stati rapidi a sfruttare l'opportunità di creare nuove identità come campioni di privacy e sicurezza. Apple ha guidato il pacchetto annunciando le modifiche alle sue politiche sui cookie all'inizio di quest'anno attraverso ITP 2.1 e recentemente, ITP 2.2. In ITP 2.1, Apple blocca completamente i cookie di terze parti e mantiene i cookie creati sul browser per soli sette giorni. In ITP 2.2, i cookie vengono conservati per un solo giorno. L'annuncio di Google non è neanche lontanamente aggressivo come quello di Apple, ma è il primo passo verso lo stesso obiettivo finale. Per ulteriori informazioni sui criteri Apple, vedere [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).

## Cosa sono i cookie e come vengono utilizzati?

Prima di conoscere le modifiche apportate alle politiche sui cookie di Google, è necessario conoscere i cookie e le relative modalità di utilizzo. In poche parole, i cookie sono piccoli file di testo memorizzati nel browser Web che vengono utilizzati per ricordare gli attributi utente.

I cookie sono importanti perché migliorano l'esperienza dell'utente che naviga sul Web. Ad esempio, se effettui acquisti su un sito Web di eCommerce e aggiungi qualcosa al carrello ma non accedi o acquista in quella visita, i cookie memorizzano i tuoi articoli e li conservano nel carrello per la prossima visita. Oppure, immaginate di dover reinserire il vostro nome utente e la password ogni volta che visitate il vostro sito Web social media preferito. Anche i cookie risolvono questo problema, perché memorizzano informazioni che aiutano i siti a identificare chi siete. Questi tipi di cookie sono chiamati cookie di prime parti perché vengono creati e utilizzati dal sito Web visitato.

Esistono anche cookie di terze parti. Per comprenderli meglio, consideriamo questo esempio:

Supponiamo che un'ipotetica società di social media denominata "Amici" fornisca un pulsante Condividi implementato da altri siti per consentire agli utenti di condividere il contenuto del sito sul feed Friends. Ora, un utente legge un articolo di notizie su un sito Web di notizie che utilizza il pulsante Condividi e fa clic su di esso per pubblicare automaticamente il proprio account Amici.

A tal fine, il browser recupera il pulsante Condivisione amici da `platform.friends.com` quando viene caricato l’articolo della notizia. In questo processo, il browser allega i cookie Friends, che contengono le credenziali di accesso dell'utente, alla richiesta ai server Friends. Questo consente agli amici di pubblicare l’articolo nel proprio feed per conto dell’utente senza che l’utente debba effettuare l’accesso.

Tutto ciò è possibile utilizzando cookie di terze parti. In questo caso, il cookie di terza parte viene salvato nel browser per `platform.friends.com`, in modo che `platform.friends.com` possa pubblicare il post nell’app Amici per conto dell’utente.

Se si immagina per un momento come ottenere questo caso d'uso senza cookie di terze parti, l'utente dovrebbe seguire molti passaggi manuali. In primo luogo, l’utente deve copiare il collegamento all’articolo della notizia. Second, the user would have to log into the Friends app separately. Quindi, l'utente faceva clic sul pulsante Crea post. Then the user would copy and paste the link in the text field, and finally click Post. As you can see, third-party cookies immensely help the user experience as manual steps can be drastically reduced.

More generally, third-party cookies make it possible for data to be stored on a user’s browser without requiring that user to explicitly visit a website.

## Security concerns

Although cookies enhance user experiences and power advertising, they can also introduce security vulnerabilities like Cross-Site Request Forgery (CSRF) attacks. For example, if a user logs in to a banking site to pay credit card bills and leaves the site without logging out and then browses to a malicious site in the same session, a CSRF attack can occur. The malicious site could include code that makes a request to the banking site that executes when the page loads. Because the user is still authenticated to the banking site, the session cookie can be used to launch a CSRF attack to initiate a funds transfer event out of the user’s bank account. This is because whenever you visit a site, all the cookies are attached in the HTTP request. And because of these security concerns, Google is now attempting to mitigate them.

## In che modo Target utilizza i cookie?

With all that said, let’s see how  uses cookies. [!DNL Target] Per poter essere utilizzato [!DNL Target] in primo luogo, è necessario installare la libreria [!DNL Target] JavaScript sul sito. This enables you to place a first-party cookie on the browser of the user that visits your site. As your user interacts with your website, you can pass the user’s behavioral and interest data to  through the JavaScript library. [!DNL Target] La libreria [!DNL Target] JavaScript utilizza cookie di prime parti per estrarre informazioni identificative sull'utente da mappare ai dati di comportamento e interesse dell'utente. Questi dati vengono quindi utilizzati [!DNL Target] per potenziare le attività di personalizzazione.

Target utilizza anche (a volte) cookie di terze parti. Se possedete più siti Web che vivono su domini diversi e desiderate monitorare il percorso utente attraverso tali siti, potete utilizzare cookie di terze parti sfruttando il monitoraggio tra domini diversi. Attivando il tracciamento tra domini nella libreria [!DNL Target] JavaScript, l'account inizierà a utilizzare cookie di terze parti. Quando un utente passa da un dominio all’altro, il browser comunica con il server di back-end di [!DNL Target]e, in questo processo, viene creato e inserito nel browser dell’utente un cookie di terza parte. Grazie al cookie di terze parti presente nel browser dell'utente, [!DNL Target] è possibile fornire un'esperienza coerente tra domini diversi per un singolo utente.

## La nuova ricetta di cookie di Google

Per fornire protezione in caso di invio di cookie tra siti in modo da proteggere gli utenti, Google pianifica di aggiungere il supporto per uno standard IETF denominato SameSite, che richiede agli sviluppatori Web di gestire i cookie con il componente attributo SameSite nell’intestazione Set-Cookie.

Tre valori diversi possono essere passati nell’attributo SameSite: Strict, Lax o None (Rigoroso, Tollerante, Nessuno).

| Valore | Descrizione |
| --- | --- |
| Strict (Rigoroso) | I cookie con questa impostazione sono accessibili solo quando si visita il dominio in cui sono stati inizialmente impostati. In altre parole, Strict impedisce completamente che il cookie possa essere utilizzato tra siti diversi. Questa opzione è ideale per le applicazioni che richiedono elevata sicurezza, come le banche. |
| Lax (Tollerante) | Cookies with this setting are sent only on same-site requests or top-level navigation with non-idempotent HTTP requests, like `HTTP GET`. Therefore, this option would be used if the cookie can be used by third-parties, but with an added security benefit that protects users from being victimized by CSRF attacks. |
| None (Nessuno) | I cookie con questa impostazione funzioneranno come i cookie di oggi. |

Keeping the above in mind, Chrome 80 introduces two independent settings for users: "SameSite by default cookies" and "Cookies without SameSite must be secure." Queste impostazioni verranno abilitate per impostazione predefinita in Chrome 80.

![StessoSito, finestra di dialogo](/help/c-implementing-target/c-considerations-before-you-implement-target/assets/samesite.png)

* **SameSite per cookie** predefiniti: Se impostato, tutti i cookie che non specificano l'attributo SameSite saranno automaticamente costretti a utilizzare `SameSite = Lax`.
* **I cookie senza SameSite devono essere protetti**: Se impostati, i cookie senza l'attributo SameSite o con `SameSite = None` necessità di essere protetti. In questo contesto, protetto significa che tutte le richieste del browser devono seguire il protocollo HTTPS. I cookie che non aderiscono a questo requisito vengono rifiutati. Tutti i siti Web devono utilizzare HTTPS per soddisfare questo requisito.

## Target segue le best practice di sicurezza di Google

In Adobe, desideriamo sempre supportare le ultime best practice del settore per la sicurezza e la privacy. We are happy to announce that [!DNL Target] supports the new security and privacy settings introduced by Google.

Per l'impostazione "SameSite by default cookies", [!DNL Target] continuerà a fornire personalizzazione senza alcun impatto e intervento da parte tua. [!DNL Target] utilizza i cookie di prima parte che continueranno a funzionare correttamente in quanto il flag `SameSite = Lax` viene applicato da Google Chrome.

Per l'opzione "Cookie senza SameSite devono essere protetti", se non si opta per la funzione di tracciamento tra domini in [!DNL Target], i cookie di prime parti in [!DNL Target] continueranno a funzionare.

However, when you opt-in to use cross-domain tracking to leverage [!DNL Target] across multiple domains, Chrome requires `SameSite = None` and Secure flags to be used for third-party cookies. Ciò significa che è necessario assicurarsi che i siti utilizzino il protocollo HTTPS. Le librerie lato client in [!DNL Target] utilizzeranno automaticamente il protocollo HTTPS e allegheranno i flag `SameSite = None` e Secure ai cookie di terze parti in [!DNL Target] modo da garantire che tutte le attività continuino a distribuire.

## Cosa devi fare?

Per capire cosa devi fare per avere [!DNL Target] continuare a lavorare per gli utenti Google Chrome 80+, consulta la tabella seguente, di cui vedrai le seguenti colonne:

* **Libreria** JavaScript di destinazione: Se utilizzate mbox.js, at.js 1.*x* o at.js 2.*x* sui siti.
* **SameSite per cookie predefiniti = Enabled**: Se i vostri utenti dispongono di "SameSite by default cookies" abilitati, in che modo vi interessa ed è presente tutto ciò che dovete fare per [!DNL Target] continuare a funzionare.
* **Cookies without SameSite must be secure = Enabled**: If your users have "Cookies without SameSite must be secure" enabled, how does it impact you and is there anything you need to do to have [!DNL Target] continue to work.

| Libreria JavaScript di destinazione | “SameSite by default cookies” = Abilitato | “Cookies without SameSite must be secure” = Abilitato |
| --- | --- | --- |
| mbox.js con solo cookie di prime parti. | Nessun impatto. | Nessun impatto se non utilizzi il tracciamento tra domini diversi. |
| mbox.js con il tracciamento tra domini abilitato. | Nessun impatto. | È necessario abilitare il protocollo HTTPS per il sito.<br>[!DNL Target] uses a third-party cookie to track users and Google requires third-party cookies to have  and Secure flag. `SameSite = None` Il flag Secure richiede che i siti utilizzino il protocollo HTTPS. |
| Mappatura payload dei parametri at.js 1.*x with first-party cookie.* | No impact. | No impact if you are not using cross-domain tracking. |
| Mappatura payload dei parametri at.js 1.*x with cross-domain tracking enabled.* | Nessun impatto. | You must enable the HTTPS protocol for your site.<br>[!DNL Target] uses a third-party cookie to track users and Google requires third-party cookies to have  and Secure flag. `SameSite = None` The Secure flag requires your sites must use the HTTPS protocol. |
| Payload JSON di at.js 2.*x* | No impact. | No impact. |

## Cosa deve fare Target?

Quindi, cosa abbiamo dovuto fare nella nostra piattaforma per aiutarti a rispettare le nuove politiche Google Chrome 80+ SameSite cookie?

| Libreria JavaScript di destinazione | “SameSite by default cookies” = Abilitato | “Cookies without SameSite must be secure” = Abilitato |
| --- | --- | --- |
| mbox.js with first-party cookie only. | Nessun impatto. | No impact if you are not using cross-domain tracking. |
| mbox.js con il tracciamento tra domini abilitato. | Nessun impatto. | [!DNL Target] aggiunge `SameSite = None` e protegge il flag al cookie di terza parte quando [!DNL Target] i server vengono chiamati. |
| Mappatura payload dei parametri at.js 1.*x* con cookie di prime parti. | Nessun impatto. | No impact if you are not using cross-domain tracking. |
| Mappatura payload dei parametri at.js 1.*x* con il tracciamento tra domini abilitato. | Nessun impatto. | Mappatura payload dei parametri at.js 1.*x* con il tracciamento tra domini abilitato. |
| Payload JSON di at.js 2.*x* | Nessun impatto. | Nessun impatto. |

## Qual è l'impatto se non passate all'uso del protocollo HTTPS?

L’unico caso d’uso che può avere un impatto è l’utilizzo della funzione di tracciamento tra domini in [!DNL Target] mbox.js o at.js 1.*x*. Senza passare a HTTPS, che è un requisito di Google, vedrete un picco di visitatori unici nei vostri domini, perché il cookie di terza parte che usiamo sarà rilasciato da Google. E poiché il cookie di terza parte verrà eliminato, [!DNL Target] non sarà in grado di fornire un'esperienza coerente e personalizzata per quell'utente mentre l'utente passa da un dominio all'altro. Il cookie di terza parte viene utilizzato principalmente per identificare un singolo utente che naviga tra i domini di cui disponete.

## Conclusione

Poiché il settore fa passi avanti per creare un web più sicuro per i consumatori, [!DNL Adobe] è assolutamente impegnato ad aiutare i nostri clienti a fornire esperienze personalizzate in modo da garantire la sicurezza e la privacy degli utenti finali. Tutto quello che devi fare è seguire le best practice di cui sopra e sfruttare [!DNL Target] per conformarsi alle nuove Regole Cookie StessoSite di Google Chrome.
