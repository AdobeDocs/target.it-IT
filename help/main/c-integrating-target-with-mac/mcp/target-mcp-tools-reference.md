---
solution: Target
product: target
title: Guida di riferimento per gli strumenti server Adobe Target MCP
description: Riferimento parametro completo per tutti gli strumenti esposti dal server Adobe Target MCP, incluse le operazioni di lettura e scrittura.
feature: Integrations
topic: Experimentation, Personalization, Artificial Intelligence
badge: label="Beta" type="Informative"
role: Developer, User
level: Intermediate, Experienced
source-git-commit: 4b154f401cc9d31d99c169bf08781bcaa7ef5c8f
workflow-type: tm+mt
source-wordcount: '3804'
ht-degree: 14%
---
# Riferimento per gli strumenti del server MCP [!DNL Adobe Target] {#target-mcp-tools-reference}

>[!AVAILABILITY]
>
>Il server MCP [!DNL Adobe Target] è disponibile per tutti i clienti in **Beta pubblico**. Attualmente è supportato in **Claude Web**, **Claude Desktop**, **Claude Code**, **Cursor** e **ChatGPT**.

Questa pagina è un riferimento completo per tutti gli strumenti esposti dal server MCP [!DNL Adobe Target]. Per ogni strumento troverai una descrizione, i dettagli dei parametri, il valore restituito e un esempio di prompt in linguaggio naturale. Per le istruzioni di installazione e i casi di utilizzo, vedere [Introduzione](target-mcp-get-started.md) e [Casi di utilizzo e procedure dettagliate](target-mcp-use-cases.md).

>[!IMPORTANT]
>
>Il Model Context Protocol (MCP) è uno standard open source emergente e può presentare rischi per la sicurezza o l&#39;affidabilità. Le integrazioni server MCP di Adobe e la relativa documentazione vengono fornite &quot;così come sono&quot;, senza garanzie di alcun tipo.
>
>La connessione di client o server MCP ai prodotti Adobe è una configurazione scelta dal cliente e i clienti sono responsabili della valutazione della sicurezza e dell’idoneità di qualsiasi integrazione MCP. Adobe non è responsabile dei problemi derivanti da configurazione errata, utilizzo errato di MCP, vulnerabilità in implementazioni di terze parti o azioni non intenzionali eseguite tramite flussi di lavoro abilitati per MCP.
>
>Per ridurre i rischi, Adobe incoraggia a testare le integrazioni in un ambiente sandbox prima di utilizzarle in modo produttivo e a rivedere e convalidare attentamente tutte le azioni e le risposte avviate da MCP prima di confermarle o di fare affidamento su di esse.

## Prerequisiti {#tools-prerequisites}

Il tuo ruolo [!DNL Adobe Target] determina quali strumenti sono disponibili:

* **Ruolo osservatore** o superiore: accesso a tutti gli strumenti di sola lettura
* Ruolo **Editor** o superiore: accesso a strumenti di lettura e strumenti di scrittura (creazione, aggiornamento)
* Ruolo **Approvatore**: accesso a tutti gli strumenti, inclusi attivazione e disattivazione

Per istruzioni complete sull&#39;installazione, vedere [Introduzione](target-mcp-get-started.md).

## Strumenti di attività {#tools-activities}

>[!NOTE]
>
>Le operazioni di lettura e scrittura hanno un ambito diverso. `get_activity` recupera attività di tutti i tipi (test A/B, Targeting esperienza, Automated Personalization, Allocazione automatica, Test multivariato, Consigli). `update_activity` supporta test A/B, Targeting esperienza e Automated Personalization; le attività Allocazione automatica, Test multivariato e Consigli sono di sola lettura tramite il server MCP.

| Funzionalità | Test A/B | Targeting esperienza | Automated Personalization | Allocazione automatica | Test multivariato | Consigli |
|---|---|---|---|---|---|---|
| `get_activity` | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| `list_target_activities` | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| `get_activity_performance_report` | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| `get_activity_orders_report` | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| `update_activity` | ✓ | ✓ | ✓ | — | — | — |
| Modifiche del ciclo di vita (stato, priorità, nome, pianificazione) | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| Modifiche a varianti e traffico | ✓ | ✓ | ✓ | — | — | — |
| Crea | ✓ | ✓ | — | — | — | — |

+++Elencare attività

**Strumento:** `list_target_activities`

Elencare [!DNL Adobe Target] attività con filtro e ordinamento lato server.

Recupera un elenco impaginato di attività. Tutti i filtri vengono applicati lato server dall&#39;API di amministrazione [!DNL Target]. Il server restituisce un massimo di 200 attività per pagina.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `limit` | numero intero | No | Numero massimo di attività da restituire (server max: 200) |
| `offset` | numero intero | No | Numero di attività da saltare per l’impaginazione |
| `sort_by` | stringa | No | Campo in base al quale eseguire l&#39;ordinamento. Prefisso con `-` per ordine decrescente (ad esempio, `-modifiedAt`). Opzioni: `id`, `name`, `state`, `priority`, `startsAt`, `endsAt`, `lifetimeStart`, `lifetimeEnd`, `createdAt`, `createdBy`, `modifiedAt`, `modifiedBy`, `type`, `thirdPartyId` |
| `state` | stringa | No | Filtra per stato attività: `approved` (live/active), `deactivated` (inactive), `paused`, `saved` (draft) |
| `activity_type` | stringa | No | Filtra per tipo: `ab` (test A/B), `xt` (targeting esperienza), `abt` (Automated Personalization), `auto_allocate` (allocazione automatica), `mvt` (test multivariato), `recs` (consigli) |
| `name_contains` | stringa | No | Filtra le attività il cui nome contiene questa stringa (senza distinzione maiuscole/minuscole) |
| `starts_after` | stringa | No | Data ISO 8601 — attività che iniziano dopo tale data |
| `starts_before` | stringa | No | Data ISO 8601 — attività che hanno inizio prima di tale data |
| `modified_after` | stringa | No | Data ISO 8601 — Attività modificate dopo tale data |
| `ends_after` | stringa | No | Data ISO 8601 — attività che terminano dopo tale data |
| `ends_before` | stringa | No | Data ISO 8601 — attività che terminano prima di tale data |
| `workspace` | stringa | No | Filtra per ID area di lavoro |
| `segment_id` | stringa | No | Filtra per ID segmento di pubblico |
| `profile_attribute_id` | stringa | No | Filtra per ID attributo profilo |
| `priority` | numero intero | No | Filtra per valore di priorità esatto (0-999) |
| `mbox` | stringa | No | Filtra per nome mbox/posizione |
| `offer_id` | stringa | No | Filtra per ID offerta |
| `view_id` | stringa | No | Filtra per ID visualizzazione SPA |

**Restituisce:** oggetto JSON con `activities` (elenco di oggetti inclusi `id`, `name`, `state`, `type`, `priority`, `modifiedAt`, `startsAt`, `endsAt`) e `total` (il conteggio totale potrebbe superare le dimensioni di pagina restituite).

**Prompt di esempio:** &quot;Elenca tutti i test A/B attivi ordinati in base all&#39;ultima modifica.&quot;

+++

+++Ottenere un’attività

**Strumento:** `get_activity`

Ottieni informazioni dettagliate su un’attività di qualsiasi tipo.

Recupera la configurazione completa di un’attività specifica, rilevando automaticamente il tipo di attività. Supporta le attività Test A/B, Targeting esperienza, Automated Personalization, Allocazione automatica, Test multivariato e Consigli.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | Identificatore univoco dell’attività |

**Restituisce:** Dettagli completi dell&#39;attività, inclusi metadati (nome, stato, priorità, date), esperienze, posizioni e offerte, obiettivi e metriche e regole di targeting.

**Prompt di esempio:** &quot;Ottieni dettagli per 12345 attività&quot;.

+++

+++Creare un’attività A/B

**Strumento:** `create_ab_activity`

Crea una nuova attività di test A/B.

Crea un nuovo test A/B con la configurazione specificata, incluse esperienze, offerte e targeting.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `name` | stringa | Sì | Nome dell’attività |
| `state` | stringa | No | Stato iniziale: `approved`, `deactivated` o `saved` (impostazione predefinita: `saved`) |
| `priority` | numero intero | No | Priorità attività (0-999, impostazione predefinita: 0) |
| `starts_at` | stringa | No | Data di inizio attività (ISO 8601) |
| `ends_at` | stringa | No | Data di fine attività (ISO 8601) |
| `experiences` | array | Sì | Elenco delle configurazioni esperienza |
| `locations` | array | Sì | Elenco configurazioni posizione/mbox |
| `goals` | oggetto | No | Metriche dell’obiettivo primario e secondario |
| `audiences` | array | No | Configurazioni del pubblico di destinazione |
| `workspace_id` | stringa | No | ID Workspace per l&#39;attività |

**Restituisce:** l&#39;oggetto attività creato con il relativo ID assegnato.

**Esempio di prompt:** &quot;Crea un test A/B denominato &#39;Test Hero della homepage&#39; con due esperienze che testano diverse immagini hero sulla mbox homepage-hero.&quot;

+++

+++Creare un’attività Targeting esperienze

**Strumento:** `create_xt_activity`

Crea una nuova attività Targeting esperienza.

Crea un’attività Targeting esperienza che fornisce esperienze diverse a tipi di pubblico diversi in base a regole di targeting.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `name` | stringa | Sì | Nome dell’attività |
| `state` | stringa | No | Stato iniziale: `approved`, `deactivated` o `saved` (impostazione predefinita: `saved`) |
| `priority` | numero intero | No | Priorità attività (0-999, impostazione predefinita: 0) |
| `starts_at` | stringa | No | Data di inizio attività (ISO 8601) |
| `ends_at` | stringa | No | Data di fine attività (ISO 8601) |
| `experiences` | array | Sì | Elenco di configurazioni di esperienza con mappature pubblico |
| `locations` | array | Sì | Elenco configurazioni posizione/mbox |
| `goals` | oggetto | No | Metriche dell’obiettivo primario e secondario |
| `workspace_id` | stringa | No | ID Workspace per l&#39;attività |

**Restituisce:** l&#39;oggetto attività creato con il relativo ID assegnato.

**Esempio di richiesta:** &quot;Crea un&#39;attività Targeting esperienze denominata &#39;Geo Personalization&#39; che mostra contenuti diversi a visitatori da aree geografiche diverse.&quot;

+++

+++Aggiornare un’attività

**Strumento:** `update_activity`

Aggiorna un test A/B, un targeting delle esperienze o un’attività Automated Personalization esistente.

Utilizza un pattern di lettura-modifica-scrittura: recupera lo stato corrente, unisce le modifiche, convalida e invia l’aggiornamento. Supporta le attività Test A/B, Targeting esperienza e Automated Personalization; le attività Allocazione automatica, Test multivariato e Consigli sono di sola lettura. I parametri strutturati `goal`, `audience_ids` e `additional_metrics` sono supportati solo per test A/B e Targeting esperienza; le attività di Automated Personalization accettano semplici aggiornamenti di unione campi.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | Identificatore univoco dell&#39;attività da aggiornare |
| `activity` | oggetto | Sì | Campi da aggiornare (nome, priorità, esperienze, posizioni, obiettivi, ecc.) |

**Restituisce:** l&#39;oggetto attività aggiornato.

**Prompt di esempio:** &quot;12345 attività di aggiornamento per modificare l&#39;allocazione del traffico in 70/30&quot;.

+++

+++Aggiorna pianificazione attività

**Strumento:** `update_activity_schedule`

Aggiorna le date di inizio e fine dell’attività.

Aggiorna la pianificazione di un&#39;attività senza modificare altre impostazioni.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | Identificatore univoco dell’attività |
| `starts_at` | stringa | No | Nuova data di inizio (ISO 8601) |
| `ends_at` | stringa | No | Nuova data di fine (ISO 8601) |

**Restituisce:** conferma dell&#39;aggiornamento della pianificazione.

**Prompt di esempio:** &quot;Aggiornare la pianificazione dell&#39;attività A/B 12345 eseguire dal 1° maggio al 31 maggio.&quot;

+++

+++Cambia stato attività

**Strumento:** `update_activity_state`

Modifica lo stato dell’attività (attivazione, disattivazione o pausa).

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | Identificatore univoco dell’attività |
| `state` | stringa | Sì | Nuovo stato: `approved` (live/active), `deactivated` (inactive), `paused` o `saved` (draft) |

**Restituisce:** lo stato dell&#39;attività aggiornato.

**Prompt di esempio:** &quot;Attiva 12345 attività&quot; o &quot;Sospendi test principale homepage&quot;.

+++

+++Rinominare un’attività

**Strumento:** `update_activity_name`

Rinominare un’attività.

Aggiorna solo il nome senza modificare la configurazione completa.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | Identificatore univoco dell’attività |
| `name` | stringa | Sì | Nome nuova attività |

**Restituisce:** l&#39;oggetto attività aggiornato.

**Prompt di esempio:** &quot;Rinominare l&#39;attività 12345 a &#39;Test eroe della campagna estiva&#39;.&quot;

+++

+++Cambia priorità attività

**Strumento:** `update_activity_priority`

Modifica la priorità dell’attività.

Le attività con priorità più alta hanno la precedenza quando più attività sono indirizzate alla stessa posizione.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | Identificatore univoco dell’attività |
| `priority` | numero intero | Sì | Nuovo valore di priorità (0-999; più alto = priorità più alta) |

**Restituisce:** l&#39;oggetto attività aggiornato.

**Prompt di esempio:** &quot;Imposta la priorità dell&#39;attività 12345 su 100&quot;.

+++

+++Aggiungere una variante a un’attività

**Strumento:** `add_activity_variant`

Aggiungi una nuova esperienza/variante a un’attività.

Gestisce tutto il coordinamento strutturale, inclusa la creazione di opzioni, la mappatura alle posizioni e il ribilanciamento del traffico.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | ID dell’attività da modificare |
| `activity_type` | stringa | Sì | Tipo di attività: `ab`, `xt` o `abt` |
| `variant_name` | stringa | Sì | Nome della nuova esperienza/variante |
| `offer_id` | numero intero | No | (Basato su modulo) ID offerta esistente da utilizzare |
| `offer_content` | stringa | No | Contenuto HTML (basato su modulo) per una nuova offerta in linea |
| `traffic_percentage` | numero intero | No | % traffico per la nuova variante (1-99). Se omesso, il traffico viene riequilibrato in modo uniforme |
| `audience_id` | numero intero | No | ID pubblico per la variante (attività XT) |
| `modifications` | array | No | (VEC) Elenco di modifiche basate su selettori CSS |

**Restituisce:** l&#39;oggetto attività aggiornato.

**Prompt di esempio:** &quot;Aggiungere una nuova variante denominata &quot;Tema festività&quot; all&#39;attività A/B 12345 utilizzando il 67890 di offerta.&quot;

+++

+++Aggiorna suddivisione traffico

**Strumento:** `update_traffic_split`

Aggiorna l’allocazione del traffico tra le varianti.

La somma delle percentuali deve essere esattamente 100.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | ID dell’attività da modificare |
| `activity_type` | stringa | Sì | Tipo di attività: `ab` o `abt` (XT non supportato — con targeting di pubblico) |
| `splits` | oggetto | Sì | Mappatura del dizionario del nome dell’esperienza in percentuale. Deve includere tutte le esperienze e sommare a 100 |

**Restituisce:** l&#39;oggetto attività aggiornato.

**Prompt di esempio:** &quot;Cambia la suddivisione del traffico per il 12345 attività in Controllo al 70% e Variante A al 30%.&quot;

+++

+++Modificare l’offerta di una variante

**Strumento:** `update_variant_offer`

Modifica l’offerta per una variante specifica.

Funziona sia per le attività basate su moduli (utilizzando `offer_id`) che per le attività VEC (utilizzando `modifications`).

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | ID dell’attività da modificare |
| `activity_type` | stringa | Sì | Tipo di attività: `ab`, `xt` o `abt` |
| `variant_name` | stringa | Sì | Nome dell’esperienza/variante da aggiornare |
| `offer_id` | numero intero | No | (Basato su modulo) Nuovo ID offerta |
| `offer_content` | stringa | No | Contenuto HTML (basato su modulo) per una nuova offerta in linea |
| `modifications` | array | No | (VEC) Nuovo elenco di modifiche basate su selettori CSS |

**Restituisce:** l&#39;oggetto attività aggiornato.

**Prompt di esempio:** &quot;Aggiornare l&#39;esperienza &#39;Variante A&#39; in 12345 attività per utilizzare il 99999 delle offerte.&quot;

+++

+++Rimuovere una variante da un’attività

**Strumento:** `remove_activity_variant`

Rimuovi un’esperienza/variante da un’attività.

Rimuove l’esperienza, ripulisce le opzioni orfane e riequilibra il traffico in modo uniforme tra le varianti rimanenti.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | ID dell’attività da modificare |
| `activity_type` | stringa | Sì | Tipo di attività: `ab`, `xt` o `abt` |
| `variant_name` | stringa | Sì | Nome dell&#39;esperienza/variante da rimuovere |

**Restituisce:** l&#39;oggetto attività aggiornato.

**Prompt di esempio:** &quot;Rimuovere l&#39;esperienza &#39;Variante test&#39; dal 12345 attività A/B.&quot;

+++

## Strumenti di offerta {#tools-offers}

+++Elencare offerte

**Strumento:** `list_target_offers`

Elencare tutte le offerte nel tenant [!DNL Target].

Recupera un elenco impaginato di offerte di contenuti con filtro opzionale.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `limit` | numero intero | No | Numero massimo di offerte da restituire |
| `offset` | numero intero | No | Numero di offerte da saltare per l’impaginazione |
| `type` | stringa | No | Filtra per tipo di offerta: `content` (HTML), `json` o `redirect` |
| `name` | stringa | No | Filtra per nome dell’offerta (corrispondenza parziale) |

**Restituisce:** oggetto JSON con `offers` (elenco di oggetti inclusi `id`, `name`, `type`, `content`, `modifiedAt`) e `total`.

**Prompt di esempio:** &quot;Elenca tutte le offerte JSON&quot;.

+++

+++Ottieni un’offerta

**Strumento:** `get_target_offer`

Informazioni dettagliate su un’offerta specifica.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `offer_id` | numero intero | Sì | Identificatore univoco dell’offerta |

**Restituisce:** dettagli completi dell&#39;offerta, inclusi `id`, `name`, `type`, `content`, `workspace` e `modifiedAt`.

**Prompt di esempio:** &quot;Ottieni dettagli per 67890 offerte&quot;.

+++

+++Creare un’offerta HTML

**Strumento:** `create_target_offer`

Crea una nuova offerta di contenuti HTML.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `name` | stringa | Sì | Nome dell’offerta |
| `content` | stringa | Sì | HTML o contenuto di testo per l’offerta |
| `workspace_id` | stringa | No | Workspace ID per l’offerta |

**Restituisce:** l&#39;offerta creata con il relativo ID assegnato.

**Prompt di esempio:** &quot;Creare un&#39;offerta HTML denominata &#39;Banner di vendita estivo&#39; con un banner promozionale.&quot;

+++

+++Creare un’offerta JSON

**Strumento:** `create_target_json_offer`

Crea una nuova offerta JSON per la distribuzione di dati strutturati.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `name` | stringa | Sì | Nome dell’offerta |
| `content` | oggetto | Sì | Contenuto JSON per l’offerta |
| `workspace_id` | stringa | No | Workspace ID per l’offerta |

**Restituisce:** l&#39;offerta creata con il relativo ID assegnato.

**Prompt di esempio:** &quot;Creare un&#39;offerta JSON denominata &#39;Configurazione flag di funzionalità&#39; con le impostazioni di attivazione/disattivazione della funzionalità.&quot;

+++

+++Aggiornare un’offerta

**Strumento:** `update_target_offer`

Aggiornare un’offerta esistente.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `offer_id` | numero intero | Sì | Identificatore univoco dell’offerta da aggiornare |
| `name` | stringa | No | Nome offerta aggiornato |
| `content` | stringa o oggetto | No | Contenuto dell’offerta aggiornato |

**Restituisce:** L&#39;oggetto offerta aggiornato.

**Prompt di esempio:** &quot;Aggiorna 67890 di offerta con nuovi contenuti promozionali&quot;.

+++

## Strumenti per il pubblico {#tools-audiences}

+++Elencare tipi di pubblico

**Strumento:** `list_target_audiences`

Elenca tutti i tipi di pubblico nel tenant [!DNL Target].

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `limit` | numero intero | No | Numero massimo di tipi di pubblico da restituire |
| `offset` | numero intero | No | Numero di tipi di pubblico da saltare per l’impaginazione |

**Restituisce:** oggetto JSON con `audiences` (elenco di oggetti inclusi `id`, `name`, `description`, `origin`, `modifiedAt`) e `total`.

**Esempio di prompt:** &quot;Elenca tutti i tipi di pubblico&quot;.

+++

+++Ottenere un pubblico

**Strumento:** `get_target_audience`

Ottieni i dettagli del pubblico, incluse le regole di targeting.

Recupera la configurazione completa di un pubblico specifico, incluse le relative regole e condizioni di targeting.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `audience_id` | numero intero | Sì | Identificatore univoco del pubblico |

**Restituisce:** dettagli completi sul pubblico, inclusi `id`, `name`, `description`, `origin`, regole di targeting e conteggio attività associato.

**Prompt di esempio:** &quot;Ottieni i dettagli per l&#39;12345 del pubblico e mostrami le relative regole di targeting.&quot;

+++

+++Creare un tipo di pubblico

**Strumento:** `create_target_audience`

Crea un nuovo pubblico con regole di targeting.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `name` | stringa | Sì | Nome del pubblico |
| `description` | stringa | No | Descrizione del pubblico |
| `targetRule` | oggetto | No | Regole di targeting (geo, browser, attributi personalizzati, ecc.) |
| `workspace_id` | stringa | No | Workspace ID per il pubblico |

**Restituisce:** il pubblico creato con il relativo ID assegnato.

**Esempio di prompt:** &quot;Crea un pubblico denominato &quot;Visitatori mobili dalla California&quot; destinato agli utenti mobili in CA.&quot;

+++

## Strumenti Mbox {#tools-mboxes}

+++Mbox di elenco

**Strumento:** `list_target_mboxes`

Elencare tutte le mbox nel tenant [!DNL Target].

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `limit` | numero intero | No | Numero massimo di mbox da restituire |
| `offset` | numero intero | No | Numero di mbox da saltare per l’impaginazione |
| `name` | stringa | No | Filtra per nome mbox (corrispondenza parziale) |
| `status` | stringa | No | Filtra per stato |

**Restituisce:** oggetto JSON con `mboxes` (elenco di oggetti inclusi `name`, `status`, `lastRequestTime`) e `total`.

**Prompt di esempio:** &quot;Elenca tutte le mbox contenenti &#39;homepage&#39;.&quot;

+++

+++Ottieni una mbox

**Strumento:** `get_target_mbox`

Ottieni informazioni dettagliate su una mbox specifica.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `mbox_name` | stringa | Sì | Nome della mbox |

**Restituisce:** dettagli Mbox inclusi `name`, `status` ed elenco di attività che utilizzano Mbox.

**Prompt di esempio:** &quot;Ottieni dettagli per mbox &#39;homepage-hero&#39;.&quot;

+++

+++Attributi di profilo della mbox di elenco

**Strumento:** `list_target_mbox_profile_attributes`

Elenca tutti gli attributi di profilo mbox disponibili per il targeting.

Nessun parametro richiesto.

**Restituisce:** array JSON di oggetti attributo profilo.

**Esempio di prompt:** &quot;Quali attributi di profilo sono disponibili per il targeting?&quot;

+++

## Strumenti proprietà {#tools-properties}

+++Proprietà elenco

**Strumento:** `list_target_properties`

Elenca tutte le proprietà nel tenant [!DNL Target].

Le proprietà organizzano le attività e controllano l&#39;accesso.

Nessun parametro richiesto.

**Restituisce:** Elenco di oggetti proprietà, inclusi `id`, `name`, `description` e `channel`.

**Prompt di esempio:** &quot;Elenca tutte le proprietà di Target&quot;.

+++

## Strumenti di reporting {#tools-reporting}

+++Ottieni un rapporto sulle prestazioni dell’attività

**Strumento:** `get_activity_performance_report`

Ottieni un rapporto sulle prestazioni per un’attività di qualsiasi tipo.

Recupera i tassi di conversione, l’incremento e i livelli di affidabilità. Supporta le attività Test A/B, Targeting esperienza, Automated Personalization, Allocazione automatica, Test multivariato e Consigli.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | Identificatore univoco dell’attività |
| `report_interval` | stringa | No | Periodo di tempo per il report (ad esempio `last7days`, `last30days` o un intervallo di date personalizzato) |

**Restituisce:** metriche a livello di esperienza (visitatori, conversioni, tasso di conversione), calcoli di incremento, livelli di affidabilità statistica e metriche dei ricavi (se configurate).

**Prompt di esempio:** &quot;Visualizza il report delle prestazioni per le 12345 dell&#39;attività negli ultimi 30 giorni.&quot;

+++

+++Ottenere un rapporto sugli ordini di attività

**Strumento:** `get_activity_orders_report`

Ottieni un rapporto ordini/ricavi per un’attività di qualsiasi tipo.

Supporta le attività Test A/B, Targeting esperienza, Automated Personalization, Allocazione automatica, Test multivariato e Consigli.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | Identificatore univoco dell’attività |
| `report_interval` | stringa | No | Periodo di tempo per il rapporto |

**Restituisce:** i conteggi, le entrate e il valore medio dell&#39;ordine in base all&#39;esperienza.

**Prompt di esempio:** &quot;Ottieni il report ordini per 12345 attività&quot;.

+++

+++Ottieni un rapporto sulle prestazioni per nome attività

**Strumento:** `get_activity_report_by_name`

Cerca un’attività per nome e ottieni il relativo rapporto sulle prestazioni.

Utile quando conosci il nome dell’attività ma non il relativo ID.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_name` | stringa | Sì | Nome dell’attività da cercare |
| `report_interval` | stringa | No | Periodo di tempo per il rapporto |

**Restituisce:** Dettagli attività e metriche delle prestazioni.

**Prompt di esempio:** &quot;Ottieni il report sulle prestazioni per l&#39;attività &#39;Homepage Hero Test&#39;.&quot;

+++

+++Ottenere un rapporto Analytics for Target (A4T)

**Strumento:** `get_a4t_report`

Recupera un report Analytics for Target (A4T) per un&#39;attività [!DNL Target].

Convalida la configurazione A4T per l&#39;attività, quindi esegue query GraphQL su [!DNL Adobe Analytics] per recuperare le metriche lato Analytics. Disponibile solo per le attività con reporting A4T configurato.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | Identificatore univoco dell&#39;attività [!DNL Target] |
| `report_interval` | stringa | No | Periodo di tempo per il report (ad esempio `last7days`, `last30days` o un intervallo di date personalizzato) |

**Restituisce:** metriche lato Analytics per l&#39;attività, inclusi conteggi di visitatori, conversioni, ricavi e incremento in base all&#39;esperienza, originati direttamente da [!DNL Adobe Analytics].

**Prompt di esempio:** &quot;Recupera il rapporto A4T per il test di ottimizzazione dell&#39;estrazione e riepiloga i dati di conversione lato Analytics.&quot;

+++

## Strumenti di anteprima {#tools-preview}

+++Visualizzare l’anteprima di un’attività

**Strumento:** `preview_activity`

Genera URL di anteprima Controllo di qualità del browser per un&#39;attività [!DNL Target].

Crea collegamenti di anteprima cliccabili che forzano la visualizzazione di esperienze specifiche, ignorando le regole di targeting del pubblico. Funziona per attività A/B, XT e Automated Personalization.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | L&#39;ID attività [!DNL Target] da visualizzare in anteprima |
| `experience_index` | numero intero | No | Indice delle esperienze basato su 0. Se omesso, restituisce gli URL per tutte le esperienze |
| `url` | stringa | No | URL della pagina per l’anteprima. Obbligatorio per le attività basate su moduli. Per le attività del Compositore esperienza visivo, se fornito, sostituisce la posizione creata |

**Restituisce:** informazioni sull&#39;attività (nome, tipo, stato), URL di anteprima per ogni esperienza e nomi e indici di esperienza.

**Esempio di prompt:** &quot;Genera URL di anteprima per 12345 attività in modo che sia possibile testare ogni esperienza nel browser.&quot;

+++

## Strumenti token di risposta {#tools-response-tokens}

+++Elencare i token di risposta

**Strumento:** `list_target_response_tokens`

Elenca tutti i token di risposta nel tenant [!DNL Target].

Recupera tutti i token di risposta configurati, sia incorporati che personalizzati.

Nessun parametro richiesto.

**Restituisce:** array JSON di oggetti token di risposta con stato `name`, `type` e `enabled`.

**Prompt di esempio:** &quot;Elenca tutti i token di risposta.&quot;

+++

+++Creare un token di risposta

**Strumento:** `create_target_response_token`

Crea un nuovo token di risposta personalizzato per la raccolta di dati aggiuntivi nelle risposte [!DNL Target].

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `token_name` | stringa | Sì | Nome del token di risposta |
| `token_type` | stringa | Sì | Tipo di token: `SCRIPT`, `ACTIVITY`, `MBOX`, `GEO` o `CRS` |

**Restituisce:** L&#39;oggetto token di risposta creato.

**Esempio di prompt:** &quot;Creare un token di risposta personalizzato denominato &#39;campaign_id&#39; di tipo ACTIVITY.&quot;

+++

## Strumenti di revisione {#tools-revisions}

+++Ottieni il registro di audit

**Strumento:** `get_target_revisions`

Ottiene il registro di controllo per un tipo di risorsa.

Recupera le modifiche apportate alle risorse [!DNL Target] con filtro facoltativo per autore.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `revision_resource_type` | stringa | Sì | Tipo di risorsa: `activity`, `offer` o `audience` |
| `modified_by` | stringa | No | Filtra per utente che ha apportato modifiche |
| `limit` | numero intero | No | Numero massimo di revisioni da restituire |
| `offset` | numero intero | No | Numero di revisioni da saltare per l’impaginazione |

**Restituisce:** la cronologia delle revisioni con marche temporali, utenti e descrizioni delle modifiche.

**Prompt di esempio:** &quot;Visualizza il registro di controllo per le modifiche delle attività&quot;.

+++

+++Ottieni revisioni per un’entità specifica

**Strumento:** `get_target_entity_revisions`

Ottieni tutte le revisioni di un’entità specifica per ID.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `revision_resource_type` | stringa | Sì | Tipo di risorsa: `activity`, `offer` o `audience` |
| `entity_id` | numero intero | Sì | Identificatore univoco dell’entità |

**Restituisce:** array JSON di tutte le revisioni per l&#39;entità specificata.

**Prompt di esempio:** &quot;Mostra tutte le modifiche apportate al 12345 attività&quot;.

+++

## Strumenti modello {#tools-templates}

+++Elencare i modelli disponibili

**Strumento:** `list_target_templates`

Elencare le risorse MCP disponibili e i modelli per la creazione di attività e offerte.

Nessun parametro richiesto.

**Restituisce:** oggetto JSON in cui sono elencati i modelli e le risorse disponibili.

**Esempio di prompt:** &quot;Quali modelli sono disponibili per la creazione di attività?&quot;

+++

## Strumenti di Recommendations {#tools-recommendations}

>[!NOTE]
>
>* Gli strumenti di Recommendations richiedono un tenant abilitato per Recommendations con **Target Premium**. Sugli account non Premium, questi strumenti non vengono visualizzati nell’elenco degli strumenti del client e l’API sottostante restituisce un errore 403.
>* Questi strumenti supportano le operazioni di elenco, recupero, creazione e aggiornamento per criteri, raccolte, progettazioni, promozioni ed esclusioni. Le operazioni di eliminazione non vengono esposte tramite il server MCP.

+++Criteri

**Strumenti:** `list_target_criteria`, `get_target_criteria`, `list_target_criteria_by_type`, `get_target_criteria_by_type`, `create_target_criteria`, `update_target_criteria`

I criteri sono regole che determinano gli elementi da consigliare, in base a un set predeterminato di comportamenti dei visitatori. I criteri sono raggruppati in 9 famiglie digitate: `category`, `custom`, `item`, `cart`, `popularity`, `profileattribute`, `recent`, `sequence`, `userhistory`.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `criteria_id` | numero intero | Per ottenere/aggiornare | Identificatore univoco dei criteri |
| `criteria_type` | stringa | Per operazioni tipizzate | Una delle 9 famiglie di criteri |
| `limit` / `offset` | numero intero | No | Paginazione |
| `name` | stringa | Sì (crea) | Nome univoco del criterio |
| `criteriaTitle` | stringa | No | Visualizza titolo utilizzato nella progettazione tramite `$criteria.title` |
| `description` | stringa | No | Descrizione dei criteri |
| `key` | stringa | Sì (crea/aggiorna, la maggior parte dei tipi) | Chiave consiglio (ad esempio `CURRENT`, `LAST_VIEWED`, `LAST_PURCHASED`, `MOST_VIEWED`, `PROFILE_ATTRIBUTE`) |
| `type` | stringa | Sì (crea/aggiorna, la maggior parte dei tipi) | Logica consigli (esempio: `VIEWED_BOUGHT`, `BOUGHT_CF`, `VIEWED_CF`, `SITE_AFFINITY`, `SIMILARITY`) |
| `configuration` | oggetto | Sì (crea/aggiorna) | Regole di inclusione, ponderazione degli attributi, filtro prezzi e altre impostazioni specifiche per la famiglia |
| `daysCount` | stringa | Varia | Intervallo di tempo storico considerato (ad esempio da `ONE_DAY` a `TWO_MONTHS`) |

`list_target_criteria` e `get_target_criteria` restituiscono metadati minimi di criteri per più famiglie (`id`, `name`, `criteriaTitle`, `criteriaGroup`). Utilizza `list_target_criteria_by_type` / `get_target_criteria_by_type` (o `create_target_criteria` / `update_target_criteria`) con un `criteria_type` per lavorare con la configurazione completa specifica per il tipo. I requisiti dei campi sono diversi a seconda della famiglia. Per informazioni sullo schema completo per tipo, vedere [!DNL Adobe] [Riferimento API per i consigli](https://developer.adobe.com/target/administer/recommendations-api/){target="_blank"}.

**Restituisce:** l&#39;oggetto criteri o un elenco impaginato con `offset`, `limit`, `total` e `list`.

**Esempio di prompt:** &quot;Elenca tutti i criteri di Recommendations configurati in questo account e riepiloga i tipi di algoritmo in uso.&quot;

+++

+++Raccolte

**Strumenti:** `list_target_collections`, `get_target_collection`, `create_target_collection`, `update_target_collection`

Le raccolte raggruppano le entità catalogo in base alle regole di corrispondenza, per l&#39;utilizzo in criteri e promozioni.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `collection_id` | numero intero | Per ottenere/aggiornare | Identificatore univoco della raccolta |
| `limit` / `offset` | numero intero | No | Paginazione |
| `name` | stringa | Sì | Nome univoco della raccolta (massimo 250 caratteri) |
| `description` | stringa | No | Descrizione della raccolta (massimo 1000 caratteri) |
| `rules` | array | Sì | 1-1000 regole (`attribute` + operatore/operando) che determinano l&#39;appartenenza al catalogo |

**Restituisce:** l&#39;oggetto della raccolta, inclusi `id`, `name`, `description`, `rules` e i metadati dell&#39;ultima modifica.

**Esempio di prompt:** &quot;Quali raccolte sono disponibili e su quali attributi di catalogo filtrano?&quot;

+++

+++Progettazioni

**Strumenti:** `list_target_designs`, `get_target_design`, `create_target_design`, `update_target_design`

Le progettazioni sono modelli Velocity o HTML che controllano il rendering delle entità consigliate.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `design_id` | numero intero | Per ottenere/aggiornare | Identificatore univoco della progettazione |
| `limit` / `offset` | numero intero | No | Paginazione |
| `includeScript` | booleano | No | Se includere il contenuto del modello della progettazione |
| `name` | stringa | Sì | Nome univoco del design (massimo 250 caratteri) |
| `script` | stringa | Sì | Modello Velocity che fa riferimento ad almeno un oggetto entità (massimo 65.000 caratteri) |
| `type` | stringa | No | Tipo di contenuto dello script: `HTML`, `JSON` o `OTHER` (impostazione predefinita) |

**Restituisce:** l&#39;oggetto di progettazione, inclusi `id`, `name`, `script` e `type`.

**Prompt di esempio:** &quot;Quali progetti e raccolte ho configurato per Recommendations?&quot;

+++

+++Promozioni

**Strumenti:** `list_target_promotions`, `get_target_promotion`, `create_target_promotion`, `update_target_promotion`

Le promozioni forzano entità specifiche nei risultati dei consigli, dando la precedenza sui criteri e i consigli di backup.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `promotion_id` | numero intero | Per ottenere/aggiornare | Identificatore univoco della promozione |
| `limit` / `offset` | numero intero | No | Paginazione |
| `name` | stringa | Sì | Nome univoco della promozione (massimo 250 caratteri) |
| `type` | stringa | Sì | Attualmente è supportato solo `EXTERNAL` |
| `key` | stringa | No | Chiave promozione: `CURRENT`, `LAST_VIEWED`, `LAST_PURCHASED`, `MOST_VIEWED` o `PROFILE_ATTRIBUTE` |
| `attribute` | stringa | No | Nome attributo profilo, applicabile quando `key` è `PROFILE_ATTRIBUTE` |
| `schedule` | oggetto | No | Intervallo di tempo di inizio/fine durante il quale viene applicata la promozione |
| `order` | oggetto | No | Configurazione dell’ordine per le entità promosse |
| `configuration` | oggetto | No | Riferimento raccolta per gli elementi promossi (utilizzato quando `rules` è vuoto) |
| `rules` | array | No | Regole di inclusione che identificano le entità da promuovere |

**Restituisce:** L&#39;oggetto della promozione.

**Prompt di esempio:** &quot;Creare una promozione esterna che includa la raccolta &#39;Backpacking Tents&#39; fino alla fine di agosto.&quot;

+++

+++Esclusioni

**Strumenti:** `list_target_exclusions`, `get_target_exclusion`, `create_target_exclusion`, `update_target_exclusion`

Le esclusioni rimuovono le entità corrispondenti dai risultati dei consigli. Le esclusioni si applicano a livello di account, in tutti i criteri e le attività.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `exclusion_id` | numero intero | Per ottenere/aggiornare | Identificatore univoco dell’esclusione |
| `name` | stringa | Sì | Nome univoco dell’esclusione (massimo 250 caratteri) |
| `description` | stringa | No | Descrizione dell’esclusione (massimo 1000 caratteri) |
| `rule` | oggetto | No | Una singola regola (`attribute` + operatore/operando) che identifica le entità da escludere |

**Restituisce:** l&#39;oggetto di esclusione.

**Esempio di richiesta:** &quot;Sono attualmente configurate esclusioni a livello di account e su cosa si filtrano?&quot;

+++

+++Catalogo

**Strumenti:** `get_target_entity`, `search_target_catalog`

Strumenti di sola lettura per l’ispezione del catalogo di prodotti/contenuti Consigli. Non è disponibile alcuno strumento di creazione, aggiornamento o eliminazione per le entità catalogo tramite il server MCP.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `catalog_entity_id` | stringa | Sì (get) | ID dell’entità catalogo (ad esempio SKU) |
| `environment_id` | stringa | No | Ambiente in cui cercare l’entità |
| `query` | oggetto | Sì (ricerca) | Un blocco `meta` (richiede `environmentId`, facoltativo `displayFields`) più un blocco `query` (`simple` o `compound`); le query semplici utilizzano `queryFields`, un `operator` (`eq`, `lt`, `gt`, `le`, `ge`, `contains`) e un `matchValue` |

**Restituisce:** `get_target_entity` restituisce gli attributi del catalogo dell&#39;entità. `search_target_catalog` restituisce corrispondenze in un array `entities`. I nomi dei campi in `query` devono essere attributi di catalogo reali configurati per il tenant.

**Prompt di esempio:** &quot;Cerca nel catalogo prodotti con inventario inferiore a 1000&quot;.

+++

## Riepilogo strumenti {#tools-summary}

| Categoria | Conteggio | Strumenti |
|---|---|---|
| Attività | 13 | `list_target_activities`, `get_activity`, `create_ab_activity`, `create_xt_activity`, `update_activity`, `update_activity_schedule`, `update_activity_state`, `update_activity_name`, `update_activity_priority`, `add_activity_variant`, `update_traffic_split`, `update_variant_offer`, `remove_activity_variant` |
| Offerta | 5 | `list_target_offers`, `get_target_offer`, `create_target_offer`, `create_target_json_offer`, `update_target_offer` |
| Pubblico | 4 | `list_target_audiences`, `get_target_audience`, `create_target_audience`, `update_target_audience` |
| Mbox | 3 | `list_target_mboxes`, `get_target_mbox`, `list_target_mbox_profile_attributes` |
| Proprietà | 1 | `list_target_properties` |
| Generazione di rapporti | 4 | `get_activity_performance_report`, `get_activity_orders_report`, `get_activity_report_by_name`, `get_a4t_report` |
| Anteprima | 1 | `preview_activity` |
| Token di risposta | 2 | `list_target_response_tokens`, `create_target_response_token` |
| Revisione | 2 | `get_target_revisions`, `get_target_entity_revisions` |
| AT.js | 2 | `get_atjs_settings`, `get_atjs_versions` |
| Modello | 1 | `list_target_templates` |
| Consigli | 24 | `list_target_criteria`, `get_target_criteria`, `list_target_criteria_by_type`, `get_target_criteria_by_type`, `create_target_criteria`, `update_target_criteria`, `list_target_collections`, `get_target_collection`, `create_target_collection`, `update_target_collection`, `list_target_designs`, `get_target_design`, `create_target_design`, `update_target_design`, `list_target_promotions`, `get_target_promotion`, `create_target_promotion`, `update_target_promotion`, `list_target_exclusions`, `get_target_exclusion`, `create_target_exclusion`, `update_target_exclusion`, `get_target_entity`, `search_target_catalog` |
| **Totale** | **62** | |

## Risorse correlate {#tools-related}

* [Utilizzo dei client MCP](target-mcp.md)
* [Riferimento API amministratore [!DNL Adobe Target]](https://developers.adobe.com/target/administer/admin-api/){target="_blank"}
