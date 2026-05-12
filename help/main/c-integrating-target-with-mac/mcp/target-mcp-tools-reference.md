---
solution: Target
product: target
title: Guida di riferimento per gli strumenti server Adobe Target MCP
description: Riferimento parametro completo per tutti i 23 strumenti di sola lettura esposti dal server MCP di Adobe Target.
feature: Integrations
topic: Experimentation, Personalization, Artificial Intelligence
badge: label="Beta" type="Informative"
role: Developer, User
level: Intermediate, Experienced
source-git-commit: d5d7a57ce6a3188f02e680c24849d773cb53457a
workflow-type: tm+mt
source-wordcount: '1883'
ht-degree: 11%

---

# Riferimento per gli strumenti del server MCP [!DNL Adobe Target] {#target-mcp-tools-reference}

>[!AVAILABILITY]
>
>Il server MCP [!DNL Adobe Target] è disponibile per tutti i clienti in **Beta pubblico**. Attualmente è supportato in **Claude Web**, **Claude Desktop**, **Claude Code**, **Cursor** e **ChatGPT**.

Questa pagina è un riferimento completo per tutti gli strumenti di sola lettura esposti dal server MCP [!DNL Adobe Target]. Per ogni strumento troverai una descrizione, i dettagli dei parametri, il valore restituito e un esempio di prompt in linguaggio naturale. Per le istruzioni di installazione e i casi di utilizzo, vedere [Introduzione](target-mcp-get-started.md) e [Casi di utilizzo e procedure dettagliate](target-mcp-use-cases.md).

>[!IMPORTANT]
>
>Il Model Context Protocol (MCP) è uno standard open source emergente e può presentare rischi per la sicurezza o l&#39;affidabilità. Le integrazioni server MCP di Adobe e la relativa documentazione vengono fornite &quot;così come sono&quot;, senza garanzie di alcun tipo.
>
>La connessione di client o server MCP ai prodotti Adobe è una configurazione scelta dal cliente e i clienti sono responsabili della valutazione della sicurezza e dell’idoneità di qualsiasi integrazione MCP. Adobe non è responsabile dei problemi derivanti da configurazione errata, utilizzo errato di MCP, vulnerabilità in implementazioni di terze parti o azioni non intenzionali eseguite tramite flussi di lavoro abilitati per MCP.
>
>Per ridurre i rischi, Adobe incoraggia a testare le integrazioni in un ambiente sandbox prima di utilizzarle in modo produttivo e a rivedere e convalidare attentamente tutte le azioni e le risposte avviate da MCP prima di confermarle o di fare affidamento su di esse.

## Prerequisiti {#tools-prerequisites}

Il tuo ruolo [!DNL Adobe Target] determina quali strumenti sono disponibili:

* **Ruolo osservatore** o superiore: accesso a tutti i 23 strumenti di sola lettura

>[!NOTE]
>
>Gli strumenti di scrittura (creazione, aggiornamento, attivazione, disattivazione) non sono esposti tramite il catalogo MCP pubblico in Public Beta. Tutti i 23 strumenti elencati in questa pagina sono di sola lettura. L’accesso in scrittura sarà disponibile in una versione futura.

Per istruzioni complete sull&#39;installazione, vedere [Introduzione](target-mcp-get-started.md).

## Strumenti di attività {#tools-activities}

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
| `activity_type` | stringa | No | Filtra per tipo: `ab` (test A/B), `xt` (targeting esperienza), `abt` (Automated Personalization) |
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

+++Ottenere un’attività A/B

**Strumento:** `get_ab_activity`

Ottieni informazioni dettagliate su un’attività A/B.

Recupera la configurazione completa di un test A/B specifico, incluse esperienze, posizioni, metriche e regole di targeting.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | Identificatore univoco dell’attività A/B |

**Restituisce:** Dettagli completi dell&#39;attività, inclusi metadati (nome, stato, priorità, date), esperienze, posizioni e offerte, obiettivi e metriche e regole di targeting.

**Prompt di esempio:** &quot;Ottieni dettagli per 12345 attività A/B&quot;.

+++

+++Ottenere un’attività Targeting esperienze

**Strumento:** `get_xt_activity`

Ottieni informazioni dettagliate su un’attività Targeting esperienza.

Recupera la configurazione completa di una specifica attività XT, incluse le mappature esperienza-pubblico, le posizioni e le metriche.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | Identificatore univoco dell’attività XT |

**Restituisce:** dettagli completi sull&#39;attività, inclusi metadati, esperienze con mappature di pubblico, posizioni e offerte, obiettivi e metriche.

**Prompt di esempio:** &quot;Ottieni dettagli per 12345 attività Targeting esperienza.&quot;

+++

+++Ottenere un’attività Automated Personalization

**Strumento:** `get_abt_activity`

Ottieni informazioni dettagliate su un’attività di Automated Personalization (AP).

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | Identificatore univoco dell&#39;attività di Personalizzazione automatizzata |

**Restituisce:** Dettagli completi dell&#39;attività, inclusi metadati, esperienze, posizioni e impostazioni algoritmiche.

**Prompt di esempio:** &quot;Ottieni dettagli per 12345 attività di Auto-Personalization&quot;.

+++

<!--
+++Create an A/B activity

**Tool:** `create_ab_activity`

Create a new A/B test activity.

Creates a new A/B test with the specified configuration including experiences, offers, and targeting.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `name` | string | Yes | Name of the activity |
| `state` | string | No | Initial state: `approved`, `deactivated`, or `saved` (default: `saved`) |
| `priority` | integer | No | Activity priority (0–999, default: 0) |
| `starts_at` | string | No | Activity start date (ISO 8601) |
| `ends_at` | string | No | Activity end date (ISO 8601) |
| `experiences` | array | Yes | List of experience configurations |
| `locations` | array | Yes | List of location/mbox configurations |
| `goals` | object | No | Primary and secondary goal metrics |
| `audiences` | array | No | Target audience configurations |
| `workspace_id` | string | No | Workspace ID for the activity |

**Returns:** The created activity object with its assigned ID.

**Example prompt:** "Create an A/B test called 'Homepage Hero Test' with two experiences testing different hero images on the homepage-hero mbox."

+++
-->

<!--
+++Create an Experience Targeting activity

**Tool:** `create_xt_activity`

Create a new Experience Targeting (XT) activity.

Creates an XT activity that delivers different experiences to different audiences based on targeting rules.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `name` | string | Yes | Name of the activity |
| `state` | string | No | Initial state: `approved`, `deactivated`, or `saved` (default: `saved`) |
| `priority` | integer | No | Activity priority (0–999, default: 0) |
| `starts_at` | string | No | Activity start date (ISO 8601) |
| `ends_at` | string | No | Activity end date (ISO 8601) |
| `experiences` | array | Yes | List of experience configurations with audience mappings |
| `locations` | array | Yes | List of location/mbox configurations |
| `goals` | object | No | Primary and secondary goal metrics |
| `workspace_id` | string | No | Workspace ID for the activity |

**Returns:** The created activity object with its assigned ID.

**Example prompt:** "Create an Experience Targeting activity called 'Geo Personalization' that shows different content to visitors from different regions."

+++
-->

<!--
+++Update an A/B activity

**Tool:** `update_ab_activity`

Update an existing A/B activity.

Uses a read-modify-write pattern: fetches the current state, merges your changes, validates, and sends the update.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the activity to update |
| `activity` | object | Yes | Fields to update (name, priority, experiences, locations, goals, etc.) |

**Returns:** The updated activity object.

**Example prompt:** "Update activity 12345 to change the traffic allocation to 70/30."

+++
-->

<!--
+++Update an Experience Targeting activity

**Tool:** `update_xt_activity`

Update an existing Experience Targeting activity.

Uses a read-modify-write pattern.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the XT activity to update |
| `activity` | object | Yes | Fields to update |

**Returns:** The updated activity object.

**Example prompt:** "Update XT activity 12345 to add a new experience for mobile visitors."

+++
-->

<!--
+++Update an Automated Personalization activity

**Tool:** `update_abt_activity`

Update an existing Automated Personalization activity.

Uses a read-modify-write pattern.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the AP activity to update |
| `activity` | object | Yes | Fields to update |

**Returns:** The updated activity object.

**Example prompt:** "Update Auto-Personalization activity 12345 to change the optimization goal."

+++
-->

<!--
+++Update activity schedule

**Tool:** `update_activity_schedule`

Update activity start and end dates.

Updates the schedule for an activity without modifying other settings.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the activity |
| `activity_type` | string | Yes | Type of activity: `ab`, `xt`, or `abt` |
| `starts_at` | string | No | New start date (ISO 8601) |
| `ends_at` | string | No | New end date (ISO 8601) |

**Returns:** Confirmation of the schedule update.

**Example prompt:** "Update the schedule for A/B activity 12345 to run from May 1st to May 31st."

+++
-->

<!--
+++Change activity state

**Tool:** `update_activity_state`

Change activity state (activate, deactivate, or pause).

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the activity |
| `state` | string | Yes | New state: `approved` (live/active), `deactivated` (inactive), `paused`, or `saved` (draft) |

**Returns:** The updated activity state.

**Example prompt:** "Activate activity 12345" or "Pause the Homepage Hero Test."

+++
-->

<!--
+++Rename an activity

**Tool:** `update_activity_name`

Rename an activity.

Updates only the name without modifying the full configuration.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the activity |
| `name` | string | Yes | New activity name |

**Returns:** The updated activity object.

**Example prompt:** "Rename activity 12345 to 'Summer Campaign Hero Test'."

+++
-->

<!--
+++Change activity priority

**Tool:** `update_activity_priority`

Change activity priority.

Higher-priority activities take precedence when multiple activities target the same location.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The unique identifier of the activity |
| `priority` | integer | Yes | New priority value (0–999; higher = higher priority) |

**Returns:** The updated activity object.

**Example prompt:** "Set the priority of activity 12345 to 100."

+++
-->

<!--
+++Add a variant to an activity

**Tool:** `add_activity_variant`

Add a new experience/variant to an activity.

Handles all structural coordination including creating options, mapping to locations, and rebalancing traffic.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The ID of the activity to modify |
| `activity_type` | string | Yes | Activity type: `ab`, `xt`, or `abt` |
| `variant_name` | string | Yes | Name for the new experience/variant |
| `offer_id` | integer | No | (Form-based) Existing offer ID to use |
| `offer_content` | string | No | (Form-based) HTML content for a new inline offer |
| `traffic_percentage` | integer | No | Traffic % for the new variant (1–99). If omitted, traffic is rebalanced evenly |
| `audience_id` | integer | No | Audience ID for the variant (XT activities) |
| `modifications` | array | No | (VEC) List of CSS selector-based modifications |

**Returns:** The updated activity object.

**Example prompt:** "Add a new variant called 'Holiday Theme' to A/B activity 12345 using offer 67890."

+++
-->

<!--
+++Update traffic split

**Tool:** `update_traffic_split`

Update traffic allocation across variants.

The percentages must sum to exactly 100.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The ID of the activity to modify |
| `activity_type` | string | Yes | Activity type: `ab` or `abt` (XT not supported — audience-targeted) |
| `splits` | object | Yes | Dictionary mapping experience name to percentage. Must include all experiences and sum to 100 |

**Returns:** The updated activity object.

**Example prompt:** "Change the traffic split for activity 12345 to 70% Control and 30% Variant A."

+++
-->

<!--
+++Change a variant's offer

**Tool:** `update_variant_offer`

Change the offer for a specific variant.

Works for both form-based activities (using `offer_id`) and VEC activities (using `modifications`).

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The ID of the activity to modify |
| `activity_type` | string | Yes | Activity type: `ab`, `xt`, or `abt` |
| `variant_name` | string | Yes | Name of the experience/variant to update |
| `offer_id` | integer | No | (Form-based) New offer ID |
| `offer_content` | string | No | (Form-based) HTML content for a new inline offer |
| `modifications` | array | No | (VEC) New list of CSS selector-based modifications |

**Returns:** The updated activity object.

**Example prompt:** "Update the 'Variant A' experience in activity 12345 to use offer 99999."

+++
-->

<!--
+++Remove a variant from an activity

**Tool:** `remove_activity_variant`

Remove an experience/variant from an activity.

Removes the experience, cleans up orphaned options, and rebalances traffic evenly across remaining variants.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `activity_id` | integer | Yes | The ID of the activity to modify |
| `activity_type` | string | Yes | Activity type: `ab`, `xt`, or `abt` |
| `variant_name` | string | Yes | Name of the experience/variant to remove |

**Returns:** The updated activity object.

**Example prompt:** "Remove the 'Test Variant' experience from A/B activity 12345."

+++
-->

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

<!--
+++Create an HTML offer

**Tool:** `create_target_offer`

Create a new HTML content offer.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `name` | string | Yes | Name of the offer |
| `content` | string | Yes | HTML or text content for the offer |
| `workspace_id` | string | No | Workspace ID for the offer |

**Returns:** The created offer with its assigned ID.

**Example prompt:** "Create an HTML offer called 'Summer Sale Banner' with a promotional banner."

+++

+++Create a JSON offer

**Tool:** `create_target_json_offer`

Create a new JSON offer for delivering structured data.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `name` | string | Yes | Name of the offer |
| `content` | object | Yes | JSON content for the offer |
| `workspace_id` | string | No | Workspace ID for the offer |

**Returns:** The created offer with its assigned ID.

**Example prompt:** "Create a JSON offer called 'Feature Flags Config' with feature toggle settings."

+++

+++Update an offer

**Tool:** `update_target_offer`

Update an existing offer.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `offer_id` | integer | Yes | The unique identifier of the offer to update |
| `name` | string | No | Updated offer name |
| `content` | string or object | No | Updated offer content |

**Returns:** The updated offer object.

**Example prompt:** "Update offer 67890 with new promotional content."

+++
-->

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

<!--
+++Create an audience

**Tool:** `create_target_audience`

Create a new audience with targeting rules.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `name` | string | Yes | Name of the audience |
| `description` | string | No | Description of the audience |
| `targetRule` | object | No | Targeting rules (geo, browser, custom attributes, etc.) |
| `workspace_id` | string | No | Workspace ID for the audience |

**Returns:** The created audience with its assigned ID.

**Example prompt:** "Create an audience called 'Mobile Visitors from California' targeting mobile users in CA."

+++
-->

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

+++Ottieni un rapporto sulle prestazioni A/B

**Strumento:** `get_ab_performance_report`

Ottieni un rapporto sulle prestazioni per un’attività A/B.

Recupera i tassi di conversione, l’incremento e i livelli di affidabilità.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | Identificatore univoco dell’attività A/B |
| `report_interval` | stringa | No | Periodo di tempo per il report (ad esempio `last7days`, `last30days` o un intervallo di date personalizzato) |

**Restituisce:** metriche a livello di esperienza (visitatori, conversioni, tasso di conversione), calcoli di incremento, livelli di affidabilità statistica e metriche dei ricavi (se configurate).

**Prompt di esempio:** &quot;Visualizza il report delle prestazioni per i 12345 di test A/B negli ultimi 30 giorni.&quot;

+++

+++Ottieni un rapporto ordini A/B

**Strumento:** `get_ab_orders_report`

Ottieni un rapporto ordini/ricavi per un’attività A/B.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | Identificatore univoco dell’attività A/B |
| `report_interval` | stringa | No | Periodo di tempo per il rapporto |

**Restituisce:** i conteggi, le entrate e il valore medio dell&#39;ordine in base all&#39;esperienza.

**Prompt di esempio:** &quot;Ottieni il report ordini per 12345 attività&quot;.

+++

+++Ottieni un rapporto sulle prestazioni di Targeting esperienza

**Strumento:** `get_xt_performance_report`

Ottieni un rapporto sulle prestazioni per un’attività Targeting esperienza.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | Identificatore univoco dell’attività XT |
| `report_interval` | stringa | No | Periodo di tempo per il rapporto |

**Restituisce:** metriche delle prestazioni a livello di esperienza.

**Prompt di esempio:** &quot;Mostra le prestazioni per la mia 54321 di attività Targeting esperienze.&quot;

+++

+++Ottieni un rapporto sugli ordini di targeting esperienza

**Strumento:** `get_xt_orders_report`

Ottieni un rapporto ordini/ricavi per un’attività Targeting esperienza.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | Identificatore univoco dell’attività XT |
| `report_interval` | stringa | No | Periodo di tempo per il rapporto |

**Restituisce:** Ordina le metriche in base all&#39;esperienza.

**Prompt di esempio:** &quot;Ottieni dati di ordini per 54321 attività XT&quot;.

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

<!--
+++Create a response token

**Tool:** `create_target_response_token`

Create a new custom response token for collecting additional data in [!DNL Target] responses.

| Parameter | Type | Required | Description |
|---|---|---|---|
| `token_name` | string | Yes | Name of the response token |
| `token_type` | string | Yes | Type of token: `SCRIPT`, `ACTIVITY`, `MBOX`, `GEO`, or `CRS` |

**Returns:** The created response token object.

**Example prompt:** "Create a custom response token called 'campaign_id' of type ACTIVITY."

+++
-->

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

## Riepilogo strumenti {#tools-summary}

| Categoria | Conteggio | Strumenti |
|---|---|---|
| Attività | 4 | `list_target_activities`, `get_ab_activity`, `get_xt_activity`, `get_abt_activity` |
| Offerta | 2 | `list_target_offers`, `get_target_offer` |
| Pubblico | 2 | `list_target_audiences`, `get_target_audience` |
| Mbox | 3 | `list_target_mboxes`, `get_target_mbox`, `list_target_mbox_profile_attributes` |
| Proprietà | 1 | `list_target_properties` |
| Generazione di rapporti | 6 | `get_ab_performance_report`, `get_ab_orders_report`, `get_xt_performance_report`, `get_xt_orders_report`, `get_activity_report_by_name`, `get_a4t_report` |
| Anteprima | 1 | `preview_activity` |
| Token di risposta | 1 | `list_target_response_tokens` |
| Revisione | 2 | `get_target_revisions`, `get_target_entity_revisions` |
| Modello | 1 | `list_target_templates` |
| **Totale** | **23** | |

## Risorse correlate {#tools-related}

* [Utilizzo dei client MCP](target-mcp.md)
* [Riferimento API amministratore [!DNL Adobe Target]](https://developers.adobe.com/target/administer/admin-api/){target="_blank"}
