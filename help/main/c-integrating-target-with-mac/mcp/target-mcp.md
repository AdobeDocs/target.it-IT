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
source-git-commit: 216b1103f501a3fcf955523d4bcc8254a8ea418d
workflow-type: tm+mt
source-wordcount: '1009'
ht-degree: 0%

---

# Server MCP [!DNL Adobe Target] {#target-mcp}

L&#39;integrazione MCP [!DNL Adobe Target] ti consente di ispezionare, analizzare e gestire test A/B, attività di personalizzazione e criteri di Recommendations direttamente dall&#39;assistente AI. Trasforma le API di lettura e scrittura di [!DNL Target] in flussi di lavoro in linguaggio semplice: controlla il tuo portfolio di esperimenti, rivedi i rapporti sulle prestazioni, gestisci tipi di pubblico e offerte e intraprendi azioni regolamentate senza navigare nell&#39;interfaccia utente o scrivere chiamate API.

>[!AVAILABILITY]
>
>Il server MCP [!DNL Adobe Target] è disponibile per tutti i clienti in **Beta pubblico**. Attualmente è supportato in **Claude Web**, **Claude Desktop**, **Claude Code**, **Cursor** e **ChatGPT**. Il supporto per ulteriori applicazioni compatibili con MCP verrà aggiunto nelle prossime versioni.


## Che cos&#39;è Model Context Protocol? {#mcp-overview}

I team di marketing e ottimizzazione si affidano sempre più alle applicazioni basate su chat e agli strumenti per sviluppatori, come Anthropic Claude, OpenAI ChatGPT, Cursor e Microsoft Copilot Studio, per semplificare il loro lavoro quotidiano. Queste applicazioni supportano **Model Context Protocol (MCP)**, uno standard aperto che consente alle applicazioni di esporre gli strumenti back-end a modelli LLM (Large Language Model) in modo uniforme.

[!DNL Adobe Target] fornisce ora un server MCP che esegue operazioni di sperimentazione, personalizzazione e consigli direttamente all&#39;interno di qualsiasi applicazione compatibile con MCP. [!DNL Adobe Target] funge da livello di decisione ed esecuzione mentre l&#39;assistente AI gestisce il ragionamento e la spiegazione, consentendo ai team di accedere più rapidamente alle informazioni sull&#39;ottimizzazione senza navigare in più schermate di prodotto o scrivere query sull&#39;API REST [!DNL Adobe Target].


>[!IMPORTANT]
>
>Il Model Context Protocol (MCP) è uno standard open source emergente e può presentare rischi per la sicurezza o l&#39;affidabilità. Le integrazioni server MCP di Adobe e la relativa documentazione vengono fornite &quot;così come sono&quot;, senza garanzie di alcun tipo.
>
>La connessione di client o server MCP ai prodotti Adobe è una configurazione scelta dal cliente e i clienti sono responsabili della valutazione della sicurezza e dell’idoneità di qualsiasi integrazione MCP. Adobe non è responsabile dei problemi derivanti da configurazione errata, utilizzo errato di MCP, vulnerabilità in implementazioni di terze parti o azioni non intenzionali eseguite tramite flussi di lavoro abilitati per MCP.
>
>Per ridurre i rischi, Adobe incoraggia a testare le integrazioni in un ambiente sandbox prima di utilizzarle in modo produttivo e a rivedere e convalidare attentamente tutte le azioni e le risposte avviate da MCP prima di confermarle o di fare affidamento su di esse.

## Funzionalità principali {#mcp-capabilities}

Il server MCP [!DNL Adobe Target] fornisce accesso in lettura e scrittura ad attività, tipi di pubblico, offerte, consigli e configurazione dell&#39;implementazione. Con l’integrazione di, puoi:

* **Esperimenti di ispezione e controllo** - Ottieni i collegamenti di stato, prestazioni, cronologia modifiche e anteprima Controllo di qualità per qualsiasi attività senza navigare nell&#39;interfaccia utente.
* **Analizza risultati** - Recupera i rapporti su prestazioni, ricavi e A4T per le attività A/B, XT, AP e Targeting automatico.
* **Gestisci attività** - Crea, aggiorna e attiva attività A/B e XT; regola le suddivisioni del traffico, le varianti, le pianificazioni e le priorità.
* **Gestione di tipi di pubblico e offerte**: elenca, esamina e crea tipi di pubblico, offerte HTML e offerte JSON.
* **Esplora i criteri di Recommendations**: elenca e controlla i criteri e gli algoritmi basati sul carrello.
* **Implementazione dell&#39;audit** - Rivedi le impostazioni at.js, i token di risposta e la cronologia delle revisioni per entità.

>[!NOTE]
>
>Le operazioni di scrittura (creazione, aggiornamento, attivazione, disattivazione) includono annotazioni di sicurezza. Non viene eseguita alcuna modifica senza una conferma esplicita da parte dell’utente.

Il server MCP [!DNL Adobe Target] espone 52 strumenti in 10 categorie, dalla gestione delle attività e il reporting alla creazione di tipi di pubblico e alle anteprime di controllo qualità. Per il riferimento completo ai parametri, vedere [Riferimento agli strumenti server MCP](target-mcp-tools-reference.md).

Per informazioni sulle operazioni che è possibile eseguire con il server MCP [!DNL Adobe Target], incluse le procedure dettagliate dettagliate dettagliate, vedere [Casi d&#39;uso e procedure dettagliate](target-mcp-use-cases.md).

Per connettere il server MCP [!DNL Adobe Target] all&#39;assistente AI, inclusi i prerequisiti, la configurazione specifica del client e la risoluzione dei problemi, vedere [Introduzione](target-mcp-get-started.md).

## Domande frequenti {#mcp-faq}

+++Quali client MCP sono supportati?

Il server MCP [!DNL Adobe Target] è attualmente disponibile per **Claude Web**, **Claude Desktop**, **Claude Code**, **Cursor** e **ChatGPT**. Il supporto per ulteriori applicazioni compatibili con MCP potrà essere aggiunto nelle prossime versioni.
+++

+++A quali [!DNL Adobe Target] oggetti posso accedere tramite MCP?

Puoi accedere alle attività (A/B, XT, AP), ai tipi di pubblico, alle offerte, alle proprietà, alle mbox, ai criteri di Recommendations, ai token di risposta, alla configurazione at.js, ai rapporti A4T e alla cronologia delle revisioni delle entità. Le operazioni di lettura e scrittura sono entrambe supportate in 52 strumenti: le operazioni di scrittura richiedono il ruolo appropriato e una conferma esplicita.
+++

+++Il server MCP può creare o modificare le attività?

Sì. Oltre alle operazioni di lettura, il server espone operazioni di scrittura che consentono di creare attività, metterle in pausa, aggiornare le priorità, regolare le suddivisioni del traffico e altro ancora. Le operazioni di scrittura seguono lo stesso modello di autorizzazione dell&#39;interfaccia utente [!DNL Adobe Target]. È necessario il ruolo appropriato per apportare modifiche e non viene eseguita alcuna azione senza la conferma esplicita dell&#39;utente.
+++

+++È necessario l&#39;accesso per sviluppatori per utilizzare il server MCP?

No. Il server MCP è progettato sia per utenti tecnici che di marketing. Gli addetti al marketing possono interagire con esso utilizzando prompt in linguaggio naturale in qualsiasi client MCP supportato, mentre gli sviluppatori possono utilizzarlo in strumenti come Claude Code o Cursor.
+++

+++I dati di [!DNL Adobe Target] vengono inviati al provider client MCP?

Quando si invia una richiesta, il client MCP può inviare il contesto rilevante (inclusi i dati [!DNL Adobe Target] restituiti dal server MCP) al proprio modello per l&#39;elaborazione. Rivedi le politiche sulla privacy e la gestione dei dati del provider client MCP prima di connetterti ai dati di produzione. La gestione dei dati di Adobe è disciplinata dalle [Informativa sulla privacy di Adobe](https://www.adobe.com/privacy.html) e dalle [Condizioni sulla protezione dei dati](https://www.adobe.com/go/dpt-ww).
+++

+++Le operazioni di scrittura possono causare modifiche non desiderate alle attività live?

Gli strumenti di scrittura includono annotazioni di sicurezza e gate di conferma. Prima di qualsiasi azione che modifichi lo stato, ad esempio l&#39;attivazione di un&#39;attività, la modifica della priorità o l&#39;aggiornamento dell&#39;allocazione del traffico, il server presenta una conferma strutturata che mostra l&#39;oggetto interessato, l&#39;impatto stimato sul traffico e un passaggio di approvazione esplicita richiesto. Non vengono apportate modifiche fino a quando non viene confermata.
+++

+++Di quali autorizzazioni ho bisogno in [!DNL Adobe Target]?

Come minimo, il ruolo **Osservatore** consente l&#39;accesso a tutti gli strumenti di lettura. Il ruolo **Editor** consente la creazione di attività, tipi di pubblico e offerte. Il ruolo **Approvatore** è necessario per attivare, disattivare o archiviare le attività. Contattare l&#39;amministratore [!DNL Adobe Target] in caso di dubbi sul livello di accesso corrente.
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
