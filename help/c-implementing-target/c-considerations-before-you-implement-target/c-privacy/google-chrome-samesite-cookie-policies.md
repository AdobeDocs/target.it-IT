---
keywords: google;samesite;cookie;chrome 80;ietf
description: Scopri in che modo Adobe [!DNL Target] gestisce lo standard IETF SameSite introdotto con Google Chrome versione 80 e cosa devi fare per rispettare questi criteri.
title: In che modo [!DNL Target] gestisce i criteri dei cookie Samesite di Google?
feature: Privacy e sicurezza
role: Developer
exl-id: 5abd2065-3692-4a6d-9ac9-6d416604c2d2
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '2048'
ht-degree: 7%

---

# Criteri per cookie SameSite di Google Chrome

Google inizierà a imporre nuovi cookie policy per impostazione predefinita per gli utenti che iniziano con Chrome 80, che è previsto per essere rilasciato all&#39;inizio del 2020. Questo articolo spiega tutto ciò che devi sapere sui nuovi criteri per cookie SameSite, su come [!DNL Adobe Target] supporta questi criteri e su come puoi utilizzare [!DNL Target] per conformarsi ai nuovi criteri per cookie SameSite di Google Chrome.

A partire da Chrome 80, gli sviluppatori web devono specificare esplicitamente quali cookie possono funzionare tra siti web diversi. Questo è il primo di molti annunci che Google intende fare per migliorare la privacy e la sicurezza sul web.

Dato che Facebook è stato sul posto per quanto riguarda la privacy e la sicurezza, altri grandi giocatori come Apple, e ora Google, sono stati rapidi a sfruttare l&#39;opportunità di creare nuove identità come campioni di privacy e sicurezza. Apple ha guidato il pacchetto annunciando le modifiche ai suoi cookie policy all’inizio di quest’anno tramite ITP 2.1 e recentemente ITP 2.2. In ITP 2.1, Apple blocca completamente i cookie di terze parti e mantiene i cookie creati sul browser per soli sette giorni. In ITP 2.2, i cookie vengono conservati per un solo giorno. L’annuncio di Google non è affatto aggressivo come quello di Apple, ma è il primo passo verso lo stesso obiettivo finale. Per ulteriori informazioni sui criteri Apple, consulta [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).

## Cosa sono i cookie e come vengono utilizzati?

Prima di conoscere le modifiche apportate ai criteri dei cookie da Google, esaminiamo quali sono i cookie e come vengono utilizzati. In parole povere, i cookie sono piccoli file di testo memorizzati nel browser web che vengono utilizzati per ricordare gli attributi utente.

I cookie sono importanti perché migliorano l’esperienza dell’utente quando naviga sul web. Ad esempio, se effettui acquisti su un sito web eCommerce e aggiungi qualcosa al carrello ma non accedi o acquista in quella visita, i cookie ricordano i tuoi articoli e li tengono nel carrello per la tua prossima visita. Oppure, immagina di essere stato costretto a reinserire il tuo nome utente e password ogni volta che visiti il tuo sito web preferito di social media. Anche i cookie risolvono questo problema, perché memorizzano informazioni che aiutano i siti a identificare chi siete. Questi cookie sono chiamati cookie di prime parti perché vengono creati e utilizzati dal sito web visitato.

Esistono anche i cookie di terze parti. Per comprenderli meglio, consideriamo questo esempio:

Supponiamo che un&#39;ipotetica società di social media denominata &quot;Amici&quot; fornisca un pulsante Condividi implementato da altri siti per consentire agli utenti di amici di condividere i contenuti del sito sul feed Amici. Ora, un utente legge un articolo su un sito web di notizie che utilizza il pulsante Condividi e lo fa clic per pubblicare automaticamente sul proprio account Amici.

Per questo motivo, il browser recupera il pulsante Condivisione amici da `platform.friends.com` al caricamento dell&#39;articolo di notizie. All’interno di questo processo, il browser allega i cookie Friends, che contengono le credenziali di accesso dell’utente, alla richiesta ai server Friends. Questo consente agli amici di pubblicare l’articolo nel proprio feed per conto dell’utente senza richiedere all’utente di effettuare l’accesso.

Tutto ciò è possibile utilizzando cookie di terze parti. In questo caso, il cookie di terze parti viene salvato nel browser per `platform.friends.com`, in modo che `platform.friends.com` possa creare il post nell’app Amici per conto dell’utente.

Se immaginate per un momento come ottenere questo caso d’uso senza cookie di terze parti, l’utente dovrebbe seguire molti passaggi manuali. In primo luogo, l&#39;utente dovrebbe copiare il link all&#39;articolo della notizia. In secondo luogo, l’utente dovrebbe accedere all’app Amici separatamente. Quindi, l&#39;utente faceva clic sul pulsante Crea post . Quindi l&#39;utente copiava e incolla il collegamento nel campo di testo, e infine clicca su Post. Come puoi vedere, i cookie di terze parti aiutano enormemente l’esperienza dell’utente in quanto i passaggi manuali possono essere drasticamente ridotti.

Più in generale, i cookie di terze parti consentono di memorizzare i dati sul browser di un utente senza richiedere all’utente di visitare esplicitamente un sito web.

## Problemi di sicurezza

Anche se i cookie migliorano le esperienze degli utenti e la pubblicità dei contenuti, possono anche introdurre vulnerabilità di sicurezza come attacchi CSRF (Cross-Site Request Forgery). Ad esempio, se un utente accede a un sito bancario per pagare le fatture delle carte di credito e lascia il sito senza disconnettersi e poi accede a un sito dannoso nella stessa sessione, può verificarsi un attacco CSRF. Il sito dannoso potrebbe includere codice che invia una richiesta al sito bancario che viene eseguito al caricamento della pagina. Poiché l’utente è ancora autenticato nel sito bancario, il cookie di sessione può essere utilizzato per avviare un attacco CSRF per avviare un evento di trasferimento di fondi dal conto bancario dell’utente. Questo perché ogni volta che visiti un sito, tutti i cookie vengono allegati nella richiesta HTTP. E a causa di questi problemi di sicurezza, Google sta cercando di mitigarli.

## In che modo [!DNL Target] utilizza i cookie?

Detto questo, vediamo come [!DNL Target] utilizza i cookie. Per poter utilizzare [!DNL Target] in primo luogo, è necessario installare la libreria JavaScript [!DNL Target] sul sito. Questo consente di inserire un cookie di prima parte nel browser dell’utente che visita il sito. Quando l’utente interagisce con il sito web, è possibile trasmettere i dati comportamentali e di interesse dell’utente a [!DNL Target] tramite la libreria JavaScript. La libreria JavaScript [!DNL Target] utilizza cookie di prime parti per estrarre informazioni di identificazione sull’utente da mappare ai dati di comportamento e interesse dell’utente. Questi dati vengono quindi utilizzati da [!DNL Target] per potenziare le attività di personalizzazione.

Target utilizza anche (a volte) cookie di terze parti. Se possiedi più siti web che vivono su domini diversi e desideri tenere traccia del percorso di utenti su tali siti web, puoi utilizzare i cookie di terze parti sfruttando il tracciamento tra domini diversi. Attivando il tracciamento tra domini diversi nella libreria JavaScript [!DNL Target], il tuo account inizierà a utilizzare cookie di terze parti. Quando un utente passa da un dominio all’altro, il browser comunica con il server back-end di [!DNL Target] e in questo processo viene creato e posizionato un cookie di terze parti sul browser dell’utente. Grazie al cookie di terze parti presente nel browser dell’utente, [!DNL Target] è in grado di fornire un’esperienza coerente tra domini diversi per un singolo utente.

## Nuova ricetta di cookie di Google

Per garantire la protezione quando i cookie vengono inviati tra siti diversi in modo da proteggere gli utenti, Google prevede di aggiungere il supporto per uno standard IETF denominato SameSite, che richiede agli sviluppatori web di gestire i cookie con il componente attributo SameSite nell’intestazione Set-Cookie.

Tre valori diversi possono essere passati nell’attributo SameSite: Strict, Lax o None (Rigoroso, Tollerante, Nessuno).

| Valore | Descrizione |
| --- | --- |
| Strict (Rigoroso) | I cookie con questa impostazione sono accessibili solo quando si visita il dominio in cui sono stati inizialmente impostati. In altre parole, Strict impedisce completamente che il cookie possa essere utilizzato tra siti diversi. Questa opzione è ideale per le applicazioni che richiedono elevata sicurezza, come le banche. |
| Lax (Tollerante) | I cookie con questa impostazione vengono inviati solo su richieste dello stesso sito o nella navigazione di livello superiore con richieste HTTP non idempotenti, come `HTTP GET`. Pertanto, questa opzione viene utilizzata se il cookie può essere utilizzato da terze parti, ma con un ulteriore vantaggio in termini di sicurezza che protegge gli utenti dal essere vittime degli attacchi CSRF. |
| None (Nessuno) | I cookie con questa impostazione funzioneranno come i cookie di oggi. |

Tenendo presente quanto sopra, Chrome 80 introduce due impostazioni indipendenti per gli utenti: &quot;SameSite by default cookies&quot; e &quot;Cookies without SameSite must be secure&quot; devono essere protetti.&quot; Queste impostazioni saranno abilitate per impostazione predefinita in Chrome 80.

![Finestra di dialogo SameSite](/help/c-implementing-target/c-considerations-before-you-implement-target/assets/samesite.png)

* **Cookie** SameSite per impostazione predefinita: Con questa impostazione, tutti i cookie che non specificano l’attributo SameSite verranno forzati automaticamente a utilizzare  `SameSite = Lax`.
* **I cookie senza SameSite devono essere protetti**: Se impostato, i cookie privi dell’attributo SameSite o con  `SameSite = None` bisogno di essere protetti. In questo contesto, protetto significa che tutte le richieste del browser devono seguire il protocollo HTTPS. I cookie che non aderiscono a questo requisito vengono rifiutati. Per soddisfare questo requisito, tutti i siti web devono utilizzare HTTPS.

## Target segue le best practice di sicurezza di Google

Ad Adobe, desideriamo sempre supportare le ultime best practice del settore per la sicurezza e la privacy. Siamo lieti di annunciare che [!DNL Target] supporta le nuove impostazioni di sicurezza e privacy introdotte da Google.

Per l’impostazione &quot;SameSite by default cookies&quot;, [!DNL Target] continuerà a fornire la personalizzazione senza alcun impatto e intervento da parte tua. [!DNL Target] utilizza i cookie di prima parte che continueranno a funzionare correttamente in quanto il flag `SameSite = Lax` viene applicato da Google Chrome.

Per l’opzione &quot;Cookies without SameSite must be secure&quot;, se non si opta per la funzione di tracciamento tra domini diversi in [!DNL Target], i cookie di prime parti in [!DNL Target] continueranno a funzionare.

Tuttavia, quando scegli di utilizzare il tracciamento tra domini diversi per sfruttare [!DNL Target], Chrome richiede `SameSite = None` e i flag Secure per essere utilizzati per i cookie di terze parti. Ciò significa che devi assicurarti che i tuoi siti utilizzino il protocollo HTTPS. Le librerie lato client in [!DNL Target] utilizzeranno automaticamente il protocollo HTTPS e allegano i flag `SameSite = None` e Secure ai cookie di terze parti in [!DNL Target] per garantire che tutte le attività continuino a essere distribuite.

## Cosa devi fare?

Per capire cosa devi fare affinché [!DNL Target] continui a funzionare per gli utenti di Google Chrome 80+, consulta la tabella seguente, di cui vedrai le seguenti colonne:

* **Libreria** JavaScript di Target: Se utilizzi mbox.js, at.js 1.*x* o at.js 2.** prendete i vostri siti.
* **SameSite per cookie predefiniti = Abilitato**: Se gli utenti dispongono di &quot;SameSite by default cookies&quot; abilitato, che impatto ha su di voi ed è necessario eseguire le operazioni necessarie  [!DNL Target] per continuare a funzionare.
* **I cookie senza SameSite devono essere protetti = Abilitato**: Se gli utenti dispongono dell’opzione &quot;Cookies without SameSite must be secure&quot;, quale impatto ha su di te ed è necessario eseguire tutte le operazioni per  [!DNL Target] continuare a funzionare.

| Libreria JavaScript di Target | “SameSite by default cookies” = Abilitato | “Cookies without SameSite must be secure” = Abilitato |
| --- | --- | --- |
| mbox.js solo con cookie di prime parti. | Nessun impatto. | Nessun impatto se non utilizzi il tracciamento tra domini diversi. |
| mbox.js con monitoraggio tra più domini abilitato. | Nessun impatto. | Devi abilitare il protocollo HTTPS per il tuo sito.<br>[!DNL Target] utilizza un cookie di terze parti per tenere traccia degli utenti e Google richiede che i cookie di terze parti abbiano  `SameSite = None` e flag Secure. Il flag Secure richiede che i siti utilizzino il protocollo HTTPS. |
| Mappatura payload dei parametri at.js 1.** xwith cookie di prime parti. | Nessun impatto. | Nessun impatto se non utilizzi il tracciamento tra domini diversi. |
| Mappatura payload dei parametri at.js 1.** con il tracciamento tra domini diversi abilitato. | Nessun impatto. | Devi abilitare il protocollo HTTPS per il tuo sito.<br>[!DNL Target] utilizza un cookie di terze parti per tenere traccia degli utenti e Google richiede che i cookie di terze parti abbiano  `SameSite = None` e flag Secure. Il flag Secure richiede che i siti utilizzino il protocollo HTTPS. |
| Payload JSON di at.js 2.*x* | Nessun impatto. | Nessun impatto. |

## Cosa deve fare [!DNL Target]?

Quindi, cosa abbiamo dovuto fare nella nostra piattaforma per aiutarti a rispettare i nuovi criteri per i cookie SameSite di Google Chrome 80+?

| Libreria JavaScript di Target | “SameSite by default cookies” = Abilitato | “Cookies without SameSite must be secure” = Abilitato |
| --- | --- | --- |
| mbox.js solo con cookie di prime parti. | Nessun impatto. | Nessun impatto se non utilizzi il tracciamento tra domini diversi. |
| mbox.js con monitoraggio tra più domini abilitato. | Nessun impatto. | [!DNL Target] aggiunge  `SameSite = None` e flag Secure al cookie di terze parti quando vengono chiamati  [!DNL Target] i server. |
| Mappatura payload dei parametri at.js 1.** xwith cookie di prime parti. | Nessun impatto. | Nessun impatto se non utilizzi il tracciamento tra domini diversi. |
| Mappatura payload dei parametri at.js 1.** con il tracciamento tra domini diversi abilitato. | Nessun impatto. | Mappatura payload dei parametri at.js 1.** con il tracciamento tra domini diversi abilitato. |
| Payload JSON di at.js 2.*x* | Nessun impatto. | Nessun impatto. |

## Qual è l’impatto se non passi all’utilizzo del protocollo HTTPS?

L’unico caso d’uso che influisce su di te è l’utilizzo della funzione di tracciamento tra domini diversi in [!DNL Target] tramite mbox.js o at.js 1.*x*. Senza passare a HTTPS, un requisito di Google, vedrai un picco di visitatori univoci nei tuoi domini perché il cookie di terze parti utilizzato verrà rilasciato da Google. Inoltre, poiché il cookie di terze parti verrà rilasciato, [!DNL Target] non sarà in grado di fornire un’esperienza coerente e personalizzata per l’utente che si sposta da un dominio all’altro. Il cookie di terze parti viene utilizzato principalmente per identificare un singolo utente che naviga tra i domini che possiedi.

## Conclusione

Nel settore si fanno grandi progressi nella creazione di un web più sicuro per i consumatori, [!DNL Adobe] è assolutamente impegnata ad aiutare i nostri clienti a fornire esperienze personalizzate in modo da garantire sicurezza e privacy agli utenti finali. Tutto quello che devi fare è seguire le best practice sopra indicate e sfruttare [!DNL Target] per conformarsi alle nuove policy per cookie SameSite di Google Chrome.
