---
solution: Target
product: target
title: Panoramica del server Adobe Target MCP
description: Scopri cos’è il server Adobe Target MCP, le sue funzionalità chiave e come si connette al tuo assistente AI.
feature: Integrations
topic: Experimentation, Personalization, Artificial Intelligence
badge: label="Beta" type="Informative"
role: User, Developer
level: Beginner, Intermediate
source-git-commit: 53dc7056ca62339a682756fe1b39e6af349f3ae6
workflow-type: tm+mt
source-wordcount: '985'
ht-degree: 0%

---

# Server MCP [!DNL Adobe Target] {#target-mcp}

L&#39;integrazione MCP [!DNL Adobe Target] consente di esaminare e analizzare test A/B e attività di personalizzazione direttamente dall&#39;assistente AI. Trasforma i dati di sperimentazione e personalizzazione di [!DNL Target] in flussi di lavoro in linguaggio semplice: controlla il tuo portfolio di esperimenti, rivedi i rapporti sulle prestazioni ed esplora tipi di pubblico e offerte senza navigare nell&#39;interfaccia utente o scrivere chiamate API.

>[!AVAILABILITY]
>
>Il server MCP [!DNL Adobe Target] è disponibile per tutti i clienti in **Beta pubblico**. Attualmente è supportato in **Claude Web**, **Claude Desktop**, **Claude Code**, **Cursor** e **ChatGPT**. Il supporto per ulteriori applicazioni compatibili con MCP verrà aggiunto nelle prossime versioni.


## Che cos&#39;è Model Context Protocol? {#mcp-overview}

I team di marketing e ottimizzazione si affidano sempre più alle applicazioni basate su chat e agli strumenti per sviluppatori, come Anthropic Claude, OpenAI ChatGPT, Cursor e Microsoft Copilot Studio, per semplificare il loro lavoro quotidiano. Queste applicazioni supportano **Model Context Protocol (MCP)**, uno standard aperto che consente alle applicazioni di esporre gli strumenti back-end a modelli LLM (Large Language Model) in modo uniforme.

[!DNL Adobe Target] fornisce ora un server MCP che affianca le operazioni di sperimentazione e personalizzazione direttamente all&#39;interno di qualsiasi applicazione compatibile con MCP. [!DNL Adobe Target] funge da livello di decisione ed esecuzione mentre l&#39;assistente AI gestisce il ragionamento e la spiegazione, consentendo ai team di accedere più rapidamente alle informazioni sull&#39;ottimizzazione senza navigare in più schermate di prodotto o scrivere query sull&#39;API REST [!DNL Adobe Target].


>[!IMPORTANT]
>
>Il Model Context Protocol (MCP) è uno standard open source emergente e può presentare rischi per la sicurezza o l&#39;affidabilità. Le integrazioni server MCP di Adobe e la relativa documentazione vengono fornite &quot;così come sono&quot;, senza garanzie di alcun tipo.
>
>La connessione di client o server MCP ai prodotti Adobe è una configurazione scelta dal cliente e i clienti sono responsabili della valutazione della sicurezza e dell’idoneità di qualsiasi integrazione MCP. Adobe non è responsabile dei problemi derivanti da configurazione errata, utilizzo errato di MCP, vulnerabilità in implementazioni di terze parti o azioni non intenzionali eseguite tramite flussi di lavoro abilitati per MCP.
>
>Per ridurre i rischi, Adobe incoraggia a testare le integrazioni in un ambiente sandbox prima di utilizzarle in modo produttivo e a rivedere e convalidare attentamente tutte le azioni e le risposte avviate da MCP prima di confermarle o di fare affidamento su di esse.

## Funzionalità principali {#mcp-capabilities}

Il server MCP [!DNL Adobe Target] fornisce accesso in lettura ad attività, tipi di pubblico, offerte e configurazione dell&#39;implementazione. Con l’integrazione di, puoi:

* **Esperimenti di ispezione e controllo** - Ottieni i collegamenti di stato, prestazioni, cronologia modifiche e anteprima Controllo di qualità per qualsiasi attività senza navigare nell&#39;interfaccia utente.
* **Analizza risultati** - Recupera i rapporti su prestazioni, ricavi e A4T per le attività A/B, XT, AP e Targeting automatico.
* **Esplora le attività** - Elenca, esamina e analizza le attività A/B e XT.
* **Esplora tipi di pubblico e offerte** - Elenca e analizza tipi di pubblico, offerte HTML e offerte JSON.
<!-- * **Explore Recommendations criteria** - List and inspect criteria and cart-based algorithms. -->
* **Implementazione dell&#39;audit** - Rivedi le impostazioni at.js, i token di risposta e la cronologia delle revisioni per entità.

>[!NOTE]
>
>Gli strumenti di scrittura (creazione, aggiornamento, attivazione, disattivazione) non sono esposti tramite il catalogo MCP pubblico in **Public Beta**. Tutti gli strumenti attualmente disponibili sono di sola lettura. L’accesso in scrittura sarà disponibile in una versione futura.

Il server MCP [!DNL Adobe Target] espone 23 strumenti di sola lettura in 10 categorie, dall&#39;ispezione delle attività al reporting, all&#39;esplorazione del pubblico e alle anteprime di controllo qualità. Per il riferimento completo ai parametri, vedere [Riferimento agli strumenti server MCP](target-mcp-tools-reference.md).

Per informazioni sulle operazioni che è possibile eseguire con il server MCP [!DNL Adobe Target], incluse le procedure dettagliate dettagliate dettagliate, vedere [Casi d&#39;uso e procedure dettagliate](target-mcp-use-cases.md).

Per connettere il server MCP [!DNL Adobe Target] all&#39;assistente AI, inclusi i prerequisiti, la configurazione specifica del client e la risoluzione dei problemi, vedere [Introduzione](target-mcp-get-started.md).

## Domande frequenti {#mcp-faq}

+++Quali client MCP sono supportati?

Il server MCP [!DNL Adobe Target] è attualmente disponibile per **Claude Web**, **Claude Desktop**, **Claude Code**, **Cursor** e **ChatGPT**. Il supporto per ulteriori applicazioni compatibili con MCP potrà essere aggiunto nelle prossime versioni.
+++

+++A quali [!DNL Adobe Target] oggetti posso accedere tramite MCP?

Puoi accedere alle attività (A/B, XT, AP), ai tipi di pubblico, alle offerte, alle proprietà, alle mbox, ai token di risposta, alla configurazione at.js, ai rapporti A4T e alla cronologia delle revisioni delle entità. Tutti i 23 strumenti attualmente disponibili sono di sola lettura.
+++

+++Il server MCP può creare o modificare le attività?

Non in Public Beta. Il catalogo MCP pubblico espone attualmente 23 strumenti di sola lettura. Le operazioni di scrittura (creazione, aggiornamento, attivazione, disattivazione) non sono ancora disponibili tramite il server MCP pubblico. L’accesso in scrittura sarà disponibile in una versione futura.
+++

+++È necessario l&#39;accesso per sviluppatori per utilizzare il server MCP?

No. Il server MCP è progettato sia per utenti tecnici che di marketing. Gli addetti al marketing possono interagire con esso utilizzando prompt in linguaggio naturale in qualsiasi client MCP supportato, mentre gli sviluppatori possono utilizzarlo in strumenti come Claude Code o Cursor.
+++

+++I dati di [!DNL Adobe Target] vengono inviati al provider client MCP?

Quando si invia una richiesta, il client MCP può inviare il contesto rilevante (inclusi i dati [!DNL Adobe Target] restituiti dal server MCP) al proprio modello per l&#39;elaborazione. Rivedi le politiche sulla privacy e la gestione dei dati del provider client MCP prima di connetterti ai dati di produzione. La gestione dei dati di Adobe è disciplinata dalle [Informativa sulla privacy di Adobe](https://www.adobe.com/privacy.html) e dalle [Condizioni sulla protezione dei dati](https://www.adobe.com/go/dpt-ww).
+++

+++Le operazioni di scrittura possono causare modifiche non desiderate alle attività live?

Gli strumenti di scrittura non sono disponibili tramite il catalogo MCP pubblico in Public Beta: tutti i 23 strumenti attualmente esposti sono di sola lettura. Quando gli strumenti di scrittura verranno introdotti in una versione futura, includeranno annotazioni di sicurezza e gate di conferma in modo che non venga eseguita alcuna azione di modifica dello stato senza esplicita conferma da parte dell’utente.
+++

+++Di quali autorizzazioni ho bisogno in [!DNL Adobe Target]?

Il ruolo **Osservatore** o superiore consente l&#39;accesso a tutti i 23 strumenti di sola lettura disponibili in Beta pubblico. Gli strumenti di scrittura non sono ancora esposti tramite il catalogo MCP pubblico, pertanto i privilegi del ruolo Editor e Approvatore non sbloccano strumenti MCP aggiuntivi in questo momento. Contattare l&#39;amministratore [!DNL Adobe Target] in caso di dubbi sul livello di accesso corrente.
+++

+++Posso utilizzare il server MCP per più organizzazioni o proprietà di Target?

Il server MCP esegue le operazioni nell’organizzazione associata alle credenziali Adobe IMS autenticate. Se hai accesso a più proprietà all&#39;interno di tale organizzazione, puoi eseguire query per proprietà utilizzando lo strumento `list_target_properties` e filtrare di conseguenza le richieste successive.
+++

## Risorse correlate {#mcp-related}

* [Introduzione](target-mcp-get-started.md)
* [Casi d’uso e procedure dettagliate](target-mcp-use-cases.md)
* [Riferimento strumenti server MCP](target-mcp-tools-reference.md)
* [Documentazione di Model Context Protocol](https://modelcontextprotocol.io/introduction){target="_blank"}
* [Riferimento API amministratore [!DNL Adobe Target]](https://developers.adobe.com/target/administer/admin-api/){target="_blank"}
* [Documentazione del cursore](https://docs.cursor.com/){target="_blank"}
