---
description: Informazioni su Target e lo standard SameSite IETF utilizzato a partire da Google Chrome versione 76.
keywords: google;samesite; cookie; chrome 80; ietf
seo-description: Informazioni su Adobe Target e lo standard IETF SameSite introdotto con Google Chrome versione 80.
seo-title: Criteri di cookie samesite di Adobe Target e Google
solution: Target
subtopic: Introduzione
title: Criteri per cookie SameSite di Google Chrome
topic: Standard
uuid: aaeda1e6-7b2c-4a00-b65d-bfc95ea796b5
translation-type: tm+mt
source-git-commit: df40d69676cea586451e3b64b56ef602da91173f

---


# Criteri per cookie SameSite di Google Chrome

Per impostazione predefinita, Google inizierà a imporre nuovi criteri di cookie per gli utenti che iniziano con Chrome 80, che verrà rilasciato per essere rilasciato all'inizio del 2020. Questo articolo descrive tutto ciò che è necessario sapere sui nuovi criteri di cookie samesite, su come [!DNL Adobe Target] supporta questi criteri e come è possibile utilizzare [!DNL Target] per rispettare i nuovi criteri di cookie samesite samesite.

A partire da Chrome 80, gli sviluppatori Web devono specificare esplicitamente quali cookie funzionano tra i siti Web. Questo è il primo di tanti annunci che Google pianifica di creare per migliorare la privacy e la sicurezza sul Web.

Dato che Facebook è stato messo in pratica in merito alla privacy e alla sicurezza, altri importanti lettori come Apple, e ora Google, hanno avuto modo di sfruttare rapidamente l'opportunità di creare nuove identità come "privacy" e "sicurezza". Apple ha portato il pacchetto inserendo prima le modifiche ai criteri dei cookie per l'anno precedente tramite ITP 2.1 e di recente, ITP 2.2. In ITP 2.1, Apple blocca completamente i cookie di terze parti e mantiene i cookie creati sul browser per soli sette giorni. In ITP 2.2, i cookie vengono conservati per un solo giorno. L'annuncio di Google non è più vicino a quello di Apple, ma è il primo passo verso lo stesso obiettivo finale. Per ulteriori informazioni sui criteri Apple, vedete [Apple Intelligent Tracking Prevention (ITP) 2. x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).

## Cosa sono i cookie e come vengono utilizzati?

Prima di immergerti nelle modifiche di Google ai suoi criteri dei cookie, vediamo quali sono i cookie e come vengono utilizzati. Semplicemente, i cookie sono piccoli file di testo memorizzati nel browser Web, utilizzati per ricordare gli attributi degli utenti.

I cookie sono importanti perché migliorano l'esperienza dell'utente durante la navigazione sul Web. Ad esempio, se stai effettuando acquisti su un sito Web ecommerce e aggiungi qualcosa al carrello ma non accedi o acquista in quella visita, i cookie memorizzano gli elementi e li tengono nel carrello per la visita successiva. Oppure, immagina di dover inserire nuovamente nome utente e password ogni volta che visita il tuo sito Web social preferito. I cookie risolvono anche tale problema, perché memorizzano informazioni utili per identificare chi sei. Questi tipi di cookie sono denominati cookie di prime parti perché vengono creati e utilizzati dal sito Web visitato.

Esistono anche cookie di terze parti. Per comprenderli meglio, prendiamo in considerazione questo esempio:

Supponiamo che un'ipotetica società social media denominata "Friends" fornisca un pulsante Condividi implementato da altri siti per consentire agli utenti di condividere il contenuto del sito sul feed Amici. Adesso, un utente legge un articolo di notizie su un sito Web di notizie che utilizza il pulsante Condividi e fa clic su di esso per pubblicarlo automaticamente sul suo account Amici.

A tal fine, il browser recupera il pulsante di condivisione degli amici dal `platform.friends.com` momento in cui l'articolo news viene caricato. In questo processo, il browser allega i cookie degli amici, che contengono le credenziali di accesso dell'utente, alla richiesta ai server di Friends. Questo consente agli amici di pubblicare l'articolo news nel feed a nome dell'utente senza richiedere l'accesso.

Tutto ciò è possibile mediante i cookie di terze parti. In questo caso, il cookie di terze parti viene salvato nel browser per `platform.friends.com`, in modo che `platform.friends.com` possa effettuare il post nell'app Friends a nome dell'utente.

Se pensate per un momento come ottenere questo caso di utilizzo senza cookie di terze parti, l'utente deve seguire molti passaggi manuali. Innanzitutto, l'utente deve copiare il collegamento all'articolo news. Secondo, l'utente deve effettuare l'accesso separatamente all'app Friends. Quindi, l'utente fa clic sul pulsante Crea post. Quindi, l'utente copia e incolla il collegamento nel campo di testo e infine fa clic su Post. Come potete vedere, i cookie di terze parti contribuiscono enormemente all'esperienza dell'utente come passaggi manuali.

Più in generale, i cookie di terze parti consentono di memorizzare i dati nel browser di un utente senza che l'utente debba visitare esplicitamente un sito Web.

## Problemi di sicurezza

Anche se i cookie migliorano le esperienze utente e la pubblicità, possono introdurre vulnerabilità di sicurezza come gli attacchi Cross-Site Request Forgery (CSRF). Ad esempio, se un utente accede a un sito bancario per pagare le bollette di credito e lasciare il sito senza uscire e quindi passare a un sito dannoso nella stessa sessione, può verificarsi un attacco CSRF. Il sito dannoso potrebbe includere codice che fa una richiesta al sito bancario che viene eseguito al caricamento della pagina. Poiché l'utente è ancora autenticato al sito bancario, il cookie di sessione può essere usato per avviare un attacco CSRF per avviare un evento di trasferimento di fondi fuori dall'account bancario dell'utente. Questo perché ogni volta che visitate un sito, tutti i cookie sono allegati nella richiesta HTTP. A causa di tali problemi di sicurezza, Google sta tentando di mitigarli.

## In che modo Target utilizza i cookie?

Inoltre, vediamo come [!DNL Target] vengono utilizzati i cookie. Per utilizzare [!DNL Target] in primo luogo, è necessario installare la libreria [!DNL Target] javascript sul sito. Questo consente di inserire un cookie di prime parti nel browser dell'utente che visita il sito. Man mano che l'utente interagisce con il tuo sito Web, puoi trasmettere i dati comportamentali e di interesse dell'utente tramite [!DNL Target] la libreria javascript. La [!DNL Target] libreria javascript utilizza i cookie di prime parti per estrarre informazioni di identificazione sull'utente per mappare i dati di comportamento e di interesse dell'utente. Questi dati vengono quindi utilizzati per [!DNL Target] abilitare le attività di personalizzazione.

Anche Target (a volte) utilizza cookie di terze parti. Se si possiedono più siti Web che si trovano su domini diversi e si desidera monitorare il percorso dell'utente attraverso i siti Web, è possibile utilizzare i cookie di terze parti sfruttando il monitoraggio tra più domini. Abilitando il monitoraggio tra domini nella libreria [!DNL Target] javascript, l'account inizierà a utilizzare i cookie di terze parti. Come un ancoraggio di un dominio da un dominio a un altro, il browser comunica con il server di backend di e [!DNL Target], in questo processo, viene creato un cookie di terze parti e inserito nel browser dell'utente. Tramite il cookie di terze parti che vive sul browser dell'utente, [!DNL Target] è in grado di fornire un'esperienza coerente nei diversi domini per un singolo utente.

## Nuovo cookie di Google

Per fornire protezione quando i cookie vengono inviati tra siti in modo che gli utenti siano protetti, Google pianifica di aggiungere il supporto per uno standard IETF chiamato samesite, che richiede agli sviluppatori Web di gestire i cookie con il componente attributo samesite nell'intestazione Set-Cookie.

Tre valori diversi possono essere passati nell’attributo SameSite: Strict, Lax o None (Rigoroso, Tollerante, Nessuno).

| Valore | Descrizione |
| --- | --- |
| Strict (Rigoroso) | I cookie con questa impostazione sono accessibili solo quando si visita il dominio in cui sono stati inizialmente impostati. In altre parole, Strict impedisce completamente che il cookie possa essere utilizzato tra siti diversi. Questa opzione è ideale per le applicazioni che richiedono una protezione elevata, ad esempio le banche. |
| Lax (Tollerante) | Cookies with this setting are sent only on same-site requests or top-level navigation with non-idempotent HTTP requests, like `HTTP GET`. Pertanto, questa opzione viene utilizzata se il cookie può essere utilizzato da terze parti, ma con un vantaggio di sicurezza aggiunto che protegge gli utenti da attacchi CSRF. |
| None (Nessuno) | I cookie con questa impostazione funzionano allo stesso modo dei cookie che funzionano oggi stesso. |

Tenendo a mente quanto sopra, Chrome 80 introduce due impostazioni indipendenti per gli utenti: " Samesite per cookie predefiniti "e" Cookie senza samesite devono essere protetti ". Queste impostazioni saranno attivate per impostazione predefinita in Chrome 80.

![Samesite, finestra di dialogo](/help/c-implementing-target/c-considerations-before-you-implement-target/assets/samesite.png)

* **Samesite per cookie predefiniti**: Quando impostato, tutti i cookie che non specificano l'attributo samesite verranno automaticamente forzati.`SameSite = Lax`
* **I cookie senza samesite devono essere protetti**: Quando impostato, i cookie senza l'attributo samesite o con `SameSite = None` necessità di essere protetti. In questo contesto, protetto significa che tutte le richieste del browser devono seguire il protocollo HTTPS. I cookie che non aderiscono a questo requisito vengono rifiutati. Per soddisfare questo requisito, tutti i siti Web devono utilizzare HTTPS.

## Target segue le best practice di sicurezza di Google

In Adobe, desideriamo sempre supportare le best practice più recenti del settore per la sicurezza e la privacy. We are happy to announce that [!DNL Target] supports the new security and privacy settings introduced by Google.

Per l'impostazione "samesite per cookie predefiniti", [!DNL Target] continueranno a distribuire personalizzazioni senza alcun impatto e intervento da parte dell'Utente. [!DNL Target] utilizza i cookie di prima parte che continueranno a funzionare correttamente in quanto il flag `SameSite = Lax` viene applicato da Google Chrome.

Per l'opzione "Cookie senza samesite", se non effettui l'accesso per la funzione di tracciamento tra domini in, [!DNL Target]i cookie di prime parti continueranno [!DNL Target] a funzionare.

However, when you opt-in to use cross-domain tracking to leverage [!DNL Target] across multiple domains, Chrome requires `SameSite = None` and Secure flags to be used for third-party cookies. È quindi necessario assicurarsi che i siti utilizzino il protocollo HTTPS. Le librerie lato client in [!DNL Target] utilizzeranno automaticamente il protocollo HTTPS e allegano i flag `SameSite = None` e protetti ai cookie di terze parti in [!DNL Target] modo da assicurare che tutte le attività continuino a essere distribuite.

## Cosa devi fare?

Per capire cosa devi fare per [!DNL Target] continuare a lavorare per Google Chrome 80 +, consulta la tabella seguente, di cui vedrai le colonne seguenti:

* **Libreria javascript di Target**: Se utilizzate mbox. js, at. js 1.*x* o at.js 2.*x* sui siti.
* **Samesite by default cookies = Enabled**: Se i vostri utenti dispongono di "samesite per cookie predefiniti" abilitata, come vi interessa ed è presente tutto ciò che dovete fare [!DNL Target] per continuare a lavorare.
* **I cookie senza samesite devono essere protetti = Enabled**: Se gli utenti dispongono di "Cookie senza samesite", è necessario che sia protetto. In che modo l'utente può avere un impatto su di esso ed è presente tutto ciò che occorre fare per [!DNL Target] continuare a lavorare.

| Libreria javascript di Target | “SameSite by default cookies” = Abilitato | “Cookies without SameSite must be secure” = Abilitato |
| --- | --- | --- |
| mbox. js con cookie first-party. | Nessun impatto. | Nessun impatto se non utilizzi tracciamento tra domini. |
| mbox. js con tracciamento tra domini abilitato. | Nessun impatto. | È necessario abilitare il protocollo HTTPS per il sito.<br>[!DNL Target] utilizza un cookie di terze parti per tenere traccia degli utenti e Google richiede che i cookie di terze parti abbiano `SameSite = None` e flag Protetto. Il flag Protetto richiede che i siti utilizzino il protocollo HTTPS. |
| at.js 1.*x* con cookie di prime parti. | Nessun impatto. | Nessun impatto se non utilizzi tracciamento tra domini. |
| at.js 1.*x* con tracciamento tra più domini abilitato. | Nessun impatto. | È necessario abilitare il protocollo HTTPS per il sito.<br>[!DNL Target] utilizza un cookie di terze parti per tenere traccia degli utenti e Google richiede che i cookie di terze parti abbiano `SameSite = None` e flag Protetto. Il flag Protetto richiede che i siti utilizzino il protocollo HTTPS. |
| at.js 2.*x* | Nessun impatto. | Nessun impatto. |

## Cosa devo fare in Target?

Cosa devo fare per aiutarti a rispettare i nuovi criteri di cookie Google Chrome 80 + samesite?

| Libreria javascript di Target | “SameSite by default cookies” = Abilitato | “Cookies without SameSite must be secure” = Abilitato |
| --- | --- | --- |
| mbox. js con cookie first-party. | Nessun impatto. | Nessun impatto se non utilizzi tracciamento tra domini. |
| mbox. js con tracciamento tra domini abilitato. | Nessun impatto. | [!DNL Target] aggiunge `SameSite = None` e protegge il flag di terze parti al cookie [!DNL Target] di terze parti. |
| at.js 1.*x* con cookie di prime parti. | Nessun impatto. | Nessun impatto se non utilizzi tracciamento tra domini. |
| at.js 1.*x* con tracciamento tra più domini abilitato. | Nessun impatto. | at.js 1.*x* con tracciamento tra più domini abilitato. |
| at.js 2.*x* | Nessun impatto. | Nessun impatto. |

## Qual è l'impatto se non si passa all'utilizzo del protocollo HTTPS?

L'unico caso d'uso che avrà impatto su di te è se utilizzi la funzione di tracciamento tra domini in [!DNL Target] mbox. js o at. js 1.*x*. Senza passare a HTTPS, come per Google, vedrai un picco in visitatori unici tra i tuoi domini, perché il cookie di terze parti utilizzato verrà ignorato da Google. Poiché il cookie di terze parti verrà interrotto, [!DNL Target] non sarà in grado di fornire un'esperienza coerente e personalizzata per quell'utente quando l'utente passa da un dominio all'altro. Il cookie di terze parti viene utilizzato principalmente per identificare un singolo utente che naviga tra i domini di tua proprietà.

## Conclusione

Poiché il settore si impegna a creare un Web più sicuro per i consumatori, [!DNL Adobe] si impegna costantemente ad aiutare i clienti a fornire esperienze personalizzate in modo da garantire protezione e privacy agli utenti finali. È sufficiente seguire le best practice riportate di seguito e sfruttare i [!DNL Target] nuovi criteri di cookie samesite samesite di Google Chrome.
