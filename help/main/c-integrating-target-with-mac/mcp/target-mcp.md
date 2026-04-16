---
solution: Target
product: target
title: Utilizzo dei client MCP
description: Scopri come collegare Adobe Target ai client MCP utilizzando il server MCP
feature: Integrations
topic: Experimentation, Personalization, Artificial Intelligence
badge: label="Beta" type="Informative"
role: User, Developer
level: Beginner, Intermediate
hide: true
source-git-commit: a0fbca3156a7d2a1c582ce591112a18b4a122a64
workflow-type: tm+mt
source-wordcount: '2267'
ht-degree: 1%

---

# Utilizzo dei client MCP {#target-mcp}

>[!BEGINSHADEBOX]

Sommario:

* **[Operazioni con i client MCP](target-mcp.md)**
* [Riferimento strumenti server MCP](target-mcp-tools-reference.md)
* [Hosting autonomo del server MCP](target-mcp-self-hosted.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Il server MCP [!DNL Adobe Target] è attualmente disponibile in **Claude Web**, **Claude Desktop**, **Claude Code** e **Cursor**. Il supporto per ulteriori applicazioni compatibili con MCP verrà aggiunto nelle prossime versioni.

L&#39;integrazione MCP [!DNL Adobe Target] ti consente di ispezionare, analizzare e gestire test A/B, attività di personalizzazione e criteri di Recommendations direttamente dall&#39;assistente AI. Trasforma le API di lettura e scrittura di [!DNL Target] in flussi di lavoro in linguaggio semplice: controlla il tuo portfolio di esperimenti, rivedi i rapporti sulle prestazioni, gestisci tipi di pubblico e offerte e intraprendi azioni regolamentate senza navigare nell&#39;interfaccia utente o scrivere chiamate API. Questa pagina spiega come funziona l’integrazione, cosa puoi farci e come iniziare.

## Che cos&#39;è Model Context Protocol? {#mcp-overview}

I team di marketing e ottimizzazione si affidano sempre più alle applicazioni basate su chat e agli strumenti per sviluppatori, come Anthropic Claude, OpenAI ChatGPT, Cursor e Microsoft Copilot Studio, per semplificare il loro lavoro quotidiano. Queste applicazioni supportano **Model Context Protocol (MCP)**, uno standard aperto che consente alle applicazioni di esporre gli strumenti back-end a modelli LLM (Large Language Model) in modo uniforme.

[!DNL Adobe Target] fornisce ora un server MCP che esegue operazioni di sperimentazione, personalizzazione e consigli direttamente all&#39;interno di qualsiasi applicazione compatibile con MCP. [!DNL Adobe Target] funge da livello di decisione ed esecuzione mentre l&#39;assistente AI gestisce il ragionamento e la spiegazione, consentendo ai team di accedere più rapidamente alle informazioni sull&#39;ottimizzazione senza navigare in più schermate di prodotto o scrivere query sull&#39;API REST [!DNL Adobe Target].

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

## Strumenti disponibili {#mcp-tools}

Il server MCP [!DNL Adobe Target] espone 52 strumenti. Gli strumenti di lettura sono disponibili per tutti gli utenti connessi con autorizzazioni di visualizzazione; gli strumenti di scrittura richiedono il ruolo di editor o approvatore.

### Strumenti di attività - lettura

| Strumento | Descrizione |
|---|---|
| `list_target_activities` | Elencare attività con filtro lato server per stato, tipo, nome, data, priorità, mbox e area di lavoro |
| `list_all_target_activities` | Recupera tutte le attività che corrispondono ai filtri, impaginazione automatica nei risultati |
| `get_ab_activity` | Ottenere dettagli completi su una specifica attività A/B |
| `get_xt_activity` | Ottieni dettagli completi su un’attività Targeting esperienza (XT) specifica |
| `get_abt_activity` | Ottieni dettagli completi su un’attività Automated Personalization (AP) specifica |

### Strumenti attività - scrittura

| Strumento | Descrizione |
|---|---|
| `create_ab_activity` | Creare una nuova attività di test A/B |
| `create_xt_activity` | Creare una nuova attività Targeting esperienza (XT) |
| `create_activity_from_modifications` | Creare un’attività Targeting esperienza dalle modifiche di JavaScript |
| `update_ab_activity` | Aggiornare un’attività A/B esistente |
| `update_xt_activity` | Aggiornare un’attività Targeting esperienza esistente |
| `update_abt_activity` | Aggiornare un’attività Automated Personalization esistente |
| `update_activity_state` | Attivare, disattivare, mettere in pausa o archiviare un’attività |
| `update_activity_schedule` | Aggiornare le date di inizio e fine di un’attività |
| `update_activity_priority` | Aggiornare la priorità di un’attività |
| `update_activity_name` | Rinominare un’attività |
| `add_activity_variant` | Aggiungere una nuova variante (esperienza) a un’attività |
| `update_traffic_split` | Aggiorna allocazione traffico tra varianti |
| `update_variant_offer` | Modificare l’offerta o le modifiche del Compositore esperienza visivo per una variante |
| `remove_activity_variant` | Rimuovere una variante da un’attività |

### Strumenti di offerta

| Strumento | Descrizione |
|---|---|
| `list_target_offers` | Elencare offerte con filtro e ordinamento lato server |
| `list_all_target_offers` | Recupera tutte le offerte che corrispondono ai filtri, impaginazione automatica |
| `get_target_offer` | Ottieni i dettagli di un’offerta specifica |
| `create_target_offer` | Crea una nuova offerta HTML |
| `create_target_json_offer` | Creare una nuova offerta JSON |
| `update_target_offer` | Aggiornare un’offerta HTML esistente |

### Strumenti per il pubblico

| Strumento | Descrizione |
|---|---|
| `list_target_audiences` | Elencare i tipi di pubblico con filtro e ordinamento lato server |
| `create_target_audience` | Creare un pubblico con regole di targeting facoltative |

### Strumenti per mbox e posizione

| Strumento | Descrizione |
|---|---|
| `list_target_mboxes` | Mbox di elenco con filtri e ordinamento |
| `list_all_target_mboxes` | Recupera tutte le mbox che corrispondono ai filtri, impaginazione automatica |
| `get_target_mbox` | Ottenere i dettagli di una mbox specifica per nome |
| `list_target_mbox_profile_attributes` | Elencare tutti gli attributi di profilo associati alle mbox |

### Proprietà

| Strumento | Descrizione |
|---|---|
| `list_target_properties` | Elenca tutte le proprietà di Target |

### Strumenti di reporting e approfondimenti

| Strumento | Descrizione |
|---|---|
| `get_ab_performance_report` | Ottieni un rapporto sulle prestazioni per un’attività A/B, Allocazione automatica o Targeting automatico |
| `get_ab_orders_report` | Ottieni rapporto ordini e ricavi per un’attività A/B o Targeting automatico |
| `get_xt_performance_report` | Ottenere un rapporto sulle prestazioni per un’attività XT |
| `get_xt_orders_report` | Ottenere un rapporto sugli ordini e sui ricavi per un’attività Targeting esperienza |
| `get_apt_performance_report` | Ottenere un rapporto sulle prestazioni per un’attività di AP o Targeting automatico |
| `get_activity_insights` | Cerca un’attività per nome e ottieni informazioni dettagliate sulle prestazioni |
| `get_a4t_report` | Ottenere un rapporto di Analytics for Target (A4T) per un’attività |

### Strumenti di Recommendations

| Strumento | Descrizione |
|---|---|
| `list_target_criteria` | Elenca tutti i criteri per la funzione Consigli |
| `get_target_criteria` | Ottieni dettagli di un criterio Consigli specifico |
| `update_target_criteria_cart` | Aggiornare un criterio basato sul carrello Consigli |

### Strumenti di implementazione e configurazione

| Strumento | Descrizione |
|---|---|
| `get_atjs_settings` | Ottieni impostazioni e configurazione AT.js |
| `get_atjs_versions` | Ottenere le versioni disponibili di AT.js |
| `list_target_response_tokens` | Elencare tutti i token di risposta nel tenant di Target |
| `create_target_response_token` | Crea un nuovo token di risposta personalizzato |

### Strumenti di revisione e audit

| Strumento | Descrizione |
|---|---|
| `get_target_revisions` | Ottieni registro di controllo per un tipo di risorsa, filtrato per autore |
| `get_target_entity_revisions` | Ottieni tutte le revisioni di un’entità specifica per ID |

### Servizi pubblici

| Strumento | Descrizione |
|---|---|
| `preview_activity` | Generare URL di anteprima controllo qualità per un’attività Target |
| `create_page_delivery_segment` | Creare un segmento di consegna pagina per il targeting delle attività del Compositore esperienza visivo |
| `list_target_templates` | Elenco delle risorse e dei modelli MCP disponibili |
| `debug_token_info` | Verifica gli ambiti e le attestazioni del token OAuth correnti |

## Casi d’uso {#mcp-use-cases}

Gli esempi seguenti mostrano come interagire con il server MCP [!DNL Adobe Target] utilizzando il linguaggio naturale:

| Obiettivo | Esempio di prompt |
|---|---|
| **Verifica stato esperimento** | &quot;Quali test A/B sono attualmente attivi nella home page? Mostrami lo stato, l’allocazione del traffico e per quanto tempo ciascuno è in esecuzione.&quot; |
| **Valutazione delle prestazioni** | &quot;Mostrami tutti i test attivi che hanno raggiunto una rilevanza statistica — quali esperienze sono vincenti?&quot; |
| **Analisi ricavi** | &quot;Ottieni il rapporto sugli ordini e sui ricavi per l’attività AT4821 e riepiloga quale esperienza genera il maggior numero di ricavi per visitatore.&quot; |
| **Generazione di rapporti per A4T** | &quot;Estrai il rapporto A4T per il test di ottimizzazione del pagamento e riepiloga i dati di conversione lato Analytics.&quot; |
| **Gestione attività** | &quot;Sospendi la 98765 dell’attività e aggiorna la priorità dell’attività 11111 a 200.&quot; |
| **Informazioni sull&#39;attività** | &quot;Ottieni informazioni sul test &#39;Banner per la vendita estiva&#39;: come sono le prestazioni e ci sono anomalie?&quot; |
| **Gestione dell&#39;audience** | &quot;Elenca tutti i tipi di pubblico destinati agli utenti di dispositivi mobili e mostra a quali attività sono associati.&quot; |
| **Controllo qualità e anteprima** | &quot;Genera URL di anteprima Controllo di qualità per le 12345 di attività in modo da poter esaminare tutte le varianti prima dell’attivazione.&quot; |
| **Revisione consigli** | &quot;Elenca tutti i criteri di Recommendations configurati in questo account e riepiloga i tipi di algoritmo in uso.&quot; |
| **Audit dell&#39;implementazione** | &quot;Quale versione di at.js è configurata e quali token di risposta sono attualmente attivi?&quot; |
| **Modifica controllo** | &quot;Mostra tutte le modifiche apportate alle 98765 attività negli ultimi 30 giorni e chi le ha apportate&quot;. |

## Procedure dettagliate sui casi d’uso {#mcp-use-case-walkthroughs}

Nelle procedure dettagliate seguenti viene illustrato come completare le attività comuni utilizzando prompt in linguaggio naturale con il server MCP [!DNL Adobe Target].

+++Creazione di un test A/B

**Prompt:**
&quot;Crea un test A/B denominato &quot;Homepage Hero Image Test&quot; con due esperienze: &quot;Control&quot; che mostra l’eroe corrente e &quot;Variant&quot; che mostra una nuova immagine protagonista a tema estivo. Eseguire il targeting della mbox della pagina home.&quot;

L&#39;assistente AI utilizza lo strumento `create_ab_activity` per creare l&#39;attività con la configurazione descritta. Lo strumento restituisce il nuovo ID attività e una conferma delle esperienze create.

+++

+++Verifica delle prestazioni dell’attività

**Prompt:**
&quot;Mostra le metriche delle prestazioni per l&#39;attività &#39;Ottimizzazione del flusso di cassa&#39; negli ultimi 30 giorni.&quot;

L&#39;assistente AI utilizza `get_ab_performance_report` o `get_xt_performance_report` (a seconda del tipo di attività) per recuperare i tassi di conversione, i conteggi dei visitatori e altre metriche per l&#39;intervallo di tempo specificato.

+++

+++Gestione delle offerte

**Prompt:**
&quot;Crea un&#39;offerta HTML denominata &#39;Banner sulla vendita estiva&#39; con un banner promozionale che riporta &#39;Sconto del 20% su tutti gli articoli estivi&#39;.&quot;

L&#39;assistente AI utilizza lo strumento `create_target_offer` per creare l&#39;offerta con il contenuto HTML specificato e restituisce una conferma con il nuovo ID offerta.

+++

+++Creazione di un pubblico

**Prompt:**
&quot;Crea un pubblico denominato &quot;Mobile Visitors from California&quot; (Visitatori mobili dalla California) che esegue il targeting degli utenti su dispositivi mobili situati in California.&quot;

L&#39;assistente AI utilizza lo strumento `create_target_audience` con le regole di targeting appropriate derivate dalla descrizione.

+++

+++Generazione di collegamenti di anteprima Controllo di qualità

**Prompt:**
&quot;Genera URL di anteprima per 12345 attività in modo da poter testare ogni esperienza.&quot;

L&#39;assistente AI utilizza lo strumento `preview_activity` per generare URL cliccabili che ignorano il targeting del pubblico, consentendo di visualizzare ogni esperienza direttamente nel browser.

+++

+++Creazione di un’attività Targeting esperienze

**Prompt:**
&quot;Crea un’attività Targeting esperienze denominata &quot;Geo Personalization&quot; che mostra diversi banner principali ai visitatori provenienti da aree geografiche diverse.&quot;

L&#39;assistente AI utilizza `create_xt_activity` per creare l&#39;attività con la mappatura dell&#39;esperienza basata sul pubblico in base alle aree che descrivi.

+++

+++Pianificazione di un’attività

**Prompt:**
&quot;Aggiornare la pianificazione delle 12345 di attività che inizieranno il 1° maggio e termineranno il 31 maggio.&quot;

L&#39;assistente AI utilizza lo strumento `update_activity_schedule` per applicare le nuove date di inizio e fine all&#39;attività.

+++

## Prerequisiti {#mcp-prerequisites}

Prima di collegare il server MCP [!DNL Adobe Target] al client MCP, verificare quanto segue:

* Hai una licenza [!DNL Adobe Target] attiva (abbonamento Adobe Experience Cloud) con un&#39;organizzazione Adobe Experience Platform.
* Hai un’applicazione compatibile con MCP supportata (attualmente Claude Web, Claude Desktop, Claude Code o Cursor).
* Hai [!DNL Adobe Target] autorizzazioni configurate in Adobe Admin Console:
   * **Ruolo osservatore**: strumenti di sola lettura
   * Ruolo **Editor**: lettura e creazione di strumenti
   * **Ruolo Approvatore**: lettura + creazione + attivazione/disattivazione strumenti

## Connetti il server MCP [!DNL Adobe Target] {#mcp-connect}

>[!NOTE]
>
>Il server MCP [!DNL Adobe Target] utilizza OAuth 2.0 per l&#39;autenticazione. Quando utilizzi uno strumento MCP di Target per la prima volta, vieni reindirizzato a Adobe Experience Cloud per accedere, selezionare la tua organizzazione e concedere le autorizzazioni richieste. Non sono richieste credenziali statiche.

**Per connettersi da Claude Desktop o Claude Web:**

1. Apri le impostazioni del client MCP e aggiungi un nuovo server MCP.
1. Immettere l&#39;URL del server: `https://targetmcp.adobe.io/mcp`
1. Quando richiesto, completa l’accesso Adobe IMS OAuth con le credenziali Adobe Experience Cloud.
1. Una volta autenticati, tutti gli strumenti sono immediatamente disponibili. Prova &quot;Elenca tutte le attività Target attive&quot; per verificare la connessione.

**Per connettersi da Claude Code:**

Aggiungi quanto segue alla configurazione di Claude Code MCP:

```json
{
  "mcpServers": {
    "adobe-target": {
      "url": "https://targetmcp.adobe.io/mcp"
    }
  }
}
```

Quando richiesto al primo utilizzo, completa il flusso del browser OAuth.

**Per connettersi dal cursore:**

1. Apri **Cursore** e passa a **Impostazioni** → **MCP** → **Aggiungi nuovo server MCP globale**.
1. Aggiungi la seguente configurazione:

```json
{
  "mcpServers": {
    "target": {
      "type": "streamable-http",
      "url": "https://targetmcp.adobe.io/mcp"
    }
  }
}
```

1. Salva la configurazione. Il server MCP [!DNL Target] verrà visualizzato nei server MCP disponibili.

>[!TIP]
>
>Se vengono visualizzate attività o dati dell’organizzazione errata, disconnetti completamente Adobe Experience Cloud, ricollega il server MCP e seleziona con attenzione l’organizzazione corretta durante la riautenticazione.

## Risoluzione dei problemi relativi al {#mcp-troubleshooting}

+++Il flusso OAuth non riesce o viene reindirizzato in modo errato

1. Disconnettersi completamente da Adobe Experience Cloud.
1. Cancella i cookie del browser per i domini adobe.com.
1. Riprovare il flusso di autenticazione.
1. Quando richiesto, assicurati di selezionare l’organizzazione corretta.
+++

+++Vengono visualizzate le attività o i dati dell’organizzazione errata

1. Disconnettersi completamente da Adobe Experience Cloud.
1. Disconnettere e riconnettere il server MCP nelle impostazioni client.
1. Selezionare con attenzione l&#39;organizzazione corretta durante la riautenticazione.
+++

+++Uno strumento restituisce un messaggio di errore

1. Verificare di disporre delle autorizzazioni necessarie in [!DNL Adobe Target] per l&#39;operazione (vedere [Prerequisiti](#mcp-prerequisites)).
1. Verifica che nell’organizzazione siano presenti le risorse, ovvero attività, offerte e tipi di pubblico, a cui si fa riferimento.
1. Verifica che gli ID attività e gli altri identificatori siano corretti.
+++

+++Impossibile connettersi al server MCP

1. Verifica la connessione Internet.
1. Verifica che l’URL del server MCP sia immesso correttamente nella configurazione client.
1. Provare a rimuovere e aggiungere nuovamente il server nelle impostazioni client MCP.
+++

## Sicurezza e autorizzazioni {#mcp-security}

Il server MCP [!DNL Adobe Target] può accedere solo ai dati per i quali l&#39;account utente Adobe dispone dell&#39;autorizzazione per visualizzare o modificare. Tutte le operazioni rispettano le assegnazioni di ruolo [!DNL Target] e le autorizzazioni dell&#39;area di lavoro.

Il server richiede i seguenti ambiti OAuth:

* `AdobeID` — Identità Adobe di base
* `openid` — Autenticazione di connessione OpenID
* `additional_info.projectedProductContext` — Individuazione tenant
* `read_organizations` — Operazioni a livello di organizzazione
* `additional_info.roles` — Controllo degli accessi basato sul ruolo

I token OAuth vengono convalidati su Adobe IMS a ogni richiesta, non vengono memorizzati in modo persistente dal server MCP e tutte le comunicazioni utilizzano HTTPS.

## Domande frequenti {#mcp-faq}

+++Quali client MCP sono supportati?

Il server MCP [!DNL Adobe Target] è attualmente disponibile per **Claude Web**, **Claude Desktop**, **Claude Code** e **Cursor**. Il supporto per ulteriori applicazioni compatibili con MCP potrà essere aggiunto nelle prossime versioni.
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

Quando si invia una richiesta, il client MCP può inviare il contesto rilevante (inclusi i dati [!DNL Adobe Target] restituiti dal server MCP) al proprio modello per l&#39;elaborazione. Rivedi le politiche sulla privacy e la gestione dei dati del provider client MCP prima di connetterti ai dati di produzione. La gestione dei dati di Adobe è disciplinata dalle [Informativa sulla privacy di Adobe](https://www.adobe.com/it/privacy.html) e dalle [Condizioni sulla protezione dei dati](https://www.adobe.com/go/dpt-ww).
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

* [Riferimento strumenti server MCP](target-mcp-tools-reference.md)
* [Hosting autonomo del server  [!DNL Adobe Target] MCP](target-mcp-self-hosted.md)
* [Documentazione di Model Context Protocol](https://modelcontextprotocol.io/introduction){target="_blank"}
* [[!DNL Adobe Target] Riferimento API amministratore](https://developers.adobe.com/target/administer/admin-api/){target="_blank"}
* [Documentazione del cursore](https://docs.cursor.com/){target="_blank"}
