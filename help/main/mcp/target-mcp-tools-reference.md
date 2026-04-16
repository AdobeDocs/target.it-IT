---
solution: Target
product: target
title: Guida di riferimento per gli strumenti server Adobe Target MCP
description: Riferimento completo dei parametri per tutti i 39 strumenti pubblici esposti dal server MCP di Adobe Target.
feature: Integrations
topic: Experimentation, Personalization, Artificial Intelligence
badge: label="Beta" type="Informative"
role: Developer, User
level: Intermediate, Experienced
hide: true
source-git-commit: 17804b5f8cfce7033bffcad826e5510bfc42a832
workflow-type: tm+mt
source-wordcount: '2688'
ht-degree: 15%

---

# Riferimento per gli strumenti del server MCP [!DNL Adobe Target] {#target-mcp-tools-reference}

>[!BEGINSHADEBOX]

Sommario:

* [Utilizzo dei client MCP](target-mcp.md)
* **[Riferimento strumenti server MCP](target-mcp-tools-reference.md)**
* [Hosting autonomo del server MCP](target-mcp-self-hosted.md)

>[!ENDSHADEBOX]

Questa pagina è un riferimento completo per tutti gli strumenti pubblici esposti dal server MCP [!DNL Adobe Target]. Per ogni strumento troverai una descrizione, i dettagli dei parametri, il valore restituito e un esempio di prompt in linguaggio naturale. Per istruzioni di configurazione e casi di utilizzo, vedere [Operazioni con i client MCP](target-mcp.md).

>[!NOTE]
>
>Solo gli strumenti pubblici sono documentati qui. Sono esclusi gli strumenti interni e quelli di solo agente. Gli strumenti di lettura sono disponibili per tutti gli utenti connessi con il ruolo **Osservatore** o superiore; gli strumenti di scrittura richiedono il ruolo **Editor** o **Approvatore**.

## Strumenti di attività {#tools-activities}

### list_target_activities

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

### get_ab_activity

Ottieni informazioni dettagliate su un’attività A/B.

Recupera la configurazione completa di un test A/B specifico, incluse esperienze, posizioni, metriche e regole di targeting.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | Identificatore univoco dell’attività A/B |

**Restituisce:** Dettagli completi dell&#39;attività, inclusi metadati (nome, stato, priorità, date), esperienze, posizioni e offerte, obiettivi e metriche e regole di targeting.

**Prompt di esempio:** &quot;Ottieni dettagli per 12345 attività A/B&quot;.

### get_xt_activity

Ottieni informazioni dettagliate su un’attività Targeting esperienza.

Recupera la configurazione completa di una specifica attività XT, incluse le mappature esperienza-pubblico, le posizioni e le metriche.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | Identificatore univoco dell’attività XT |

**Restituisce:** dettagli completi sull&#39;attività, inclusi metadati, esperienze con mappature di pubblico, posizioni e offerte, obiettivi e metriche.

**Prompt di esempio:** &quot;Ottieni dettagli per 12345 attività Targeting esperienza.&quot;

### get_abt_activity

Ottieni informazioni dettagliate su un’attività di Automated Personalization (AP).

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | Identificatore univoco dell&#39;attività di Personalizzazione automatizzata |

**Restituisce:** Dettagli completi dell&#39;attività, inclusi metadati, esperienze, posizioni e impostazioni algoritmiche.

**Prompt di esempio:** &quot;Ottieni dettagli per 12345 attività di Auto-Personalization&quot;.

### create_ab_activity

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

### create_xt_activity

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

### update_ab_activity

Aggiornare un’attività A/B esistente.

Utilizza un pattern di lettura-modifica-scrittura: recupera lo stato corrente, unisce le modifiche, convalida e invia l’aggiornamento.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | Identificatore univoco dell&#39;attività da aggiornare |
| `activity` | oggetto | Sì | Campi da aggiornare (nome, priorità, esperienze, posizioni, obiettivi, ecc.) |

**Restituisce:** l&#39;oggetto attività aggiornato.

**Prompt di esempio:** &quot;12345 attività di aggiornamento per modificare l&#39;allocazione del traffico in 70/30&quot;.

### update_xt_activity

Aggiorna un&#39;attività Targeting esperienza esistente.

Utilizza un pattern di lettura-modifica-scrittura.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | Identificatore univoco dell’attività XT da aggiornare |
| `activity` | oggetto | Sì | Campi da aggiornare |

**Restituisce:** l&#39;oggetto attività aggiornato.

**Prompt di esempio:** &quot;Aggiorna l&#39;attività Targeting esperienza 12345 aggiungere una nuova esperienza per i visitatori di dispositivi mobili.&quot;

### update_abt_activity

Aggiorna un’attività Automated Personalization esistente.

Utilizza un pattern di lettura-modifica-scrittura.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | Identificatore univoco dell&#39;attività AP da aggiornare |
| `activity` | oggetto | Sì | Campi da aggiornare |

**Restituisce:** l&#39;oggetto attività aggiornato.

**Prompt di esempio:** &quot;Aggiorna 12345 attività di Auto-Personalization per modificare l&#39;obiettivo di ottimizzazione.&quot;

### update_activity_schedule

Aggiorna le date di inizio e fine dell’attività.

Aggiorna la pianificazione di un&#39;attività senza modificare altre impostazioni.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | Identificatore univoco dell’attività |
| `activity_type` | stringa | Sì | Tipo di attività: `ab`, `xt` o `abt` |
| `starts_at` | stringa | No | Nuova data di inizio (ISO 8601) |
| `ends_at` | stringa | No | Nuova data di fine (ISO 8601) |

**Restituisce:** conferma dell&#39;aggiornamento della pianificazione.

**Prompt di esempio:** &quot;Aggiornare la pianificazione dell&#39;attività A/B 12345 eseguire dal 1° maggio al 31 maggio.&quot;

### update_activity_state

Modifica lo stato dell’attività (attivazione, disattivazione o pausa).

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | Identificatore univoco dell’attività |
| `state` | stringa | Sì | Nuovo stato: `approved` (live/active), `deactivated` (inactive), `paused` o `saved` (draft) |

**Restituisce:** lo stato dell&#39;attività aggiornato.

**Prompt di esempio:** &quot;Attiva 12345 attività&quot; o &quot;Sospendi test principale homepage&quot;.

### update_activity_name

Rinominare un’attività.

Aggiorna solo il nome senza modificare la configurazione completa.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | Identificatore univoco dell’attività |
| `name` | stringa | Sì | Nome nuova attività |

**Restituisce:** l&#39;oggetto attività aggiornato.

**Prompt di esempio:** &quot;Rinominare l&#39;attività 12345 a &#39;Test eroe della campagna estiva&#39;.&quot;

### update_activity_priority

Modifica la priorità dell’attività.

Le attività con priorità più alta hanno la precedenza quando più attività sono indirizzate alla stessa posizione.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | Identificatore univoco dell’attività |
| `priority` | numero intero | Sì | Nuovo valore di priorità (0-999; più alto = priorità più alta) |

**Restituisce:** l&#39;oggetto attività aggiornato.

**Prompt di esempio:** &quot;Imposta la priorità dell&#39;attività 12345 su 100&quot;.

### add_activity_variant

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

### update_traffic_split

Aggiorna l’allocazione del traffico tra le varianti.

La somma delle percentuali deve essere esattamente 100.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | ID dell’attività da modificare |
| `activity_type` | stringa | Sì | Tipo di attività: `ab` o `abt` (XT non supportato — con targeting di pubblico) |
| `splits` | oggetto | Sì | Mappatura del dizionario del nome dell’esperienza in percentuale. Deve includere tutte le esperienze e sommare a 100 |

**Restituisce:** l&#39;oggetto attività aggiornato.

**Prompt di esempio:** &quot;Cambia la suddivisione del traffico per il 12345 attività in Controllo al 70% e Variante A al 30%.&quot;

### update_variant_offer

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

### remove_activity_variant

Rimuovi un’esperienza/variante da un’attività.

Rimuove l’esperienza, ripulisce le opzioni orfane e riequilibra il traffico in modo uniforme tra le varianti rimanenti.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | ID dell’attività da modificare |
| `activity_type` | stringa | Sì | Tipo di attività: `ab`, `xt` o `abt` |
| `variant_name` | stringa | Sì | Nome dell&#39;esperienza/variante da rimuovere |

**Restituisce:** l&#39;oggetto attività aggiornato.

**Prompt di esempio:** &quot;Rimuovere l&#39;esperienza &#39;Variante test&#39; dal 12345 attività A/B.&quot;

## Strumenti di offerta {#tools-offers}

### list_target_offers

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

### get_target_offer

Informazioni dettagliate su un’offerta specifica.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `offer_id` | numero intero | Sì | Identificatore univoco dell’offerta |

**Restituisce:** dettagli completi dell&#39;offerta, inclusi `id`, `name`, `type`, `content`, `workspace` e `modifiedAt`.

**Prompt di esempio:** &quot;Ottieni dettagli per 67890 offerte&quot;.

### create_target_offer

Crea una nuova offerta di contenuti HTML.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `name` | stringa | Sì | Nome dell’offerta |
| `content` | stringa | Sì | HTML o contenuto di testo per l’offerta |
| `workspace_id` | stringa | No | Workspace ID per l’offerta |

**Restituisce:** l&#39;offerta creata con il relativo ID assegnato.

**Prompt di esempio:** &quot;Creare un&#39;offerta HTML denominata &#39;Banner di vendita estivo&#39; con un banner promozionale.&quot;

### create_target_json_offer

Crea una nuova offerta JSON per la distribuzione di dati strutturati.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `name` | stringa | Sì | Nome dell’offerta |
| `content` | oggetto | Sì | Contenuto JSON per l’offerta |
| `workspace_id` | stringa | No | Workspace ID per l’offerta |

**Restituisce:** l&#39;offerta creata con il relativo ID assegnato.

**Prompt di esempio:** &quot;Creare un&#39;offerta JSON denominata &#39;Configurazione flag di funzionalità&#39; con le impostazioni di attivazione/disattivazione della funzionalità.&quot;

### update_target_offer

Aggiornare un’offerta esistente.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `offer_id` | numero intero | Sì | Identificatore univoco dell’offerta da aggiornare |
| `name` | stringa | No | Nome offerta aggiornato |
| `content` | stringa o oggetto | No | Contenuto dell’offerta aggiornato |

**Restituisce:** L&#39;oggetto offerta aggiornato.

**Prompt di esempio:** &quot;Aggiorna 67890 di offerta con nuovi contenuti promozionali&quot;.

## Strumenti per il pubblico {#tools-audiences}

### list_target_audiences

Elenca tutti i tipi di pubblico nel tenant [!DNL Target].

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `limit` | numero intero | No | Numero massimo di tipi di pubblico da restituire |
| `offset` | numero intero | No | Numero di tipi di pubblico da saltare per l’impaginazione |

**Restituisce:** oggetto JSON con `audiences` (elenco di oggetti inclusi `id`, `name`, `description`, `origin`, `modifiedAt`) e `total`.

**Esempio di prompt:** &quot;Elenca tutti i tipi di pubblico&quot;.

### create_target_audience

Crea un nuovo pubblico con regole di targeting.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `name` | stringa | Sì | Nome del pubblico |
| `description` | stringa | No | Descrizione del pubblico |
| `targetRule` | oggetto | No | Regole di targeting (geo, browser, attributi personalizzati, ecc.) |
| `workspace_id` | stringa | No | Workspace ID per il pubblico |

**Restituisce:** il pubblico creato con il relativo ID assegnato.

**Esempio di prompt:** &quot;Crea un pubblico denominato &quot;Visitatori mobili dalla California&quot; destinato agli utenti mobili in CA.&quot;

## Strumenti Mbox {#tools-mboxes}

### list_target_mboxes

Elencare tutte le mbox nel tenant [!DNL Target].

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `limit` | numero intero | No | Numero massimo di mbox da restituire |
| `offset` | numero intero | No | Numero di mbox da saltare per l’impaginazione |
| `name` | stringa | No | Filtra per nome mbox (corrispondenza parziale) |
| `status` | stringa | No | Filtra per stato |

**Restituisce:** oggetto JSON con `mboxes` (elenco di oggetti inclusi `name`, `status`, `lastRequestTime`) e `total`.

**Prompt di esempio:** &quot;Elenca tutte le mbox contenenti &#39;homepage&#39;.&quot;

### get_target_mbox

Ottieni informazioni dettagliate su una mbox specifica.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `mbox_name` | stringa | Sì | Nome della mbox |

**Restituisce:** dettagli Mbox inclusi `name`, `status` ed elenco di attività che utilizzano Mbox.

**Prompt di esempio:** &quot;Ottieni dettagli per mbox &#39;homepage-hero&#39;.&quot;

### list_target_mbox_profile_attributes

Elenca tutti gli attributi di profilo mbox disponibili per il targeting.

Nessun parametro richiesto.

**Restituisce:** array JSON di oggetti attributo profilo.

**Esempio di prompt:** &quot;Quali attributi di profilo sono disponibili per il targeting?&quot;

## Strumenti proprietà {#tools-properties}

### list_target_properties

Elenca tutte le proprietà nel tenant [!DNL Target].

Le proprietà organizzano le attività e controllano l&#39;accesso.

Nessun parametro richiesto.

**Restituisce:** Elenco di oggetti proprietà, inclusi `id`, `name`, `description` e `channel`.

**Prompt di esempio:** &quot;Elenca tutte le proprietà di Target&quot;.

## Strumenti di reporting {#tools-reporting}

### get_ab_performance_report

Ottieni un rapporto sulle prestazioni per un’attività A/B.

Recupera i tassi di conversione, l’incremento e i livelli di affidabilità.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | Identificatore univoco dell’attività A/B |
| `report_interval` | stringa | No | Periodo di tempo per il report (ad esempio `last7days`, `last30days` o un intervallo di date personalizzato) |

**Restituisce:** metriche a livello di esperienza (visitatori, conversioni, tasso di conversione), calcoli di incremento, livelli di affidabilità statistica e metriche dei ricavi (se configurate).

**Prompt di esempio:** &quot;Visualizza il report delle prestazioni per i 12345 di test A/B negli ultimi 30 giorni.&quot;

### get_ab_orders_report

Ottieni un rapporto ordini/ricavi per un’attività A/B.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | Identificatore univoco dell’attività A/B |
| `report_interval` | stringa | No | Periodo di tempo per il rapporto |

**Restituisce:** i conteggi, le entrate e il valore medio dell&#39;ordine in base all&#39;esperienza.

**Prompt di esempio:** &quot;Ottieni il report ordini per 12345 attività&quot;.

### get_xt_performance_report

Ottieni un rapporto sulle prestazioni per un’attività Targeting esperienza.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | Identificatore univoco dell’attività XT |
| `report_interval` | stringa | No | Periodo di tempo per il rapporto |

**Restituisce:** metriche delle prestazioni a livello di esperienza.

**Prompt di esempio:** &quot;Mostra le prestazioni per la mia 54321 di attività Targeting esperienze.&quot;

### get_xt_orders_report

Ottieni un rapporto ordini/ricavi per un’attività Targeting esperienza.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | Identificatore univoco dell’attività XT |
| `report_interval` | stringa | No | Periodo di tempo per il rapporto |

**Restituisce:** Ordina le metriche in base all&#39;esperienza.

**Prompt di esempio:** &quot;Ottieni dati di ordini per 54321 attività XT&quot;.

### get_activity_report_by_name

Cerca un’attività per nome e ottieni il relativo rapporto sulle prestazioni.

Utile quando conosci il nome dell’attività ma non il relativo ID.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_name` | stringa | Sì | Nome dell’attività da cercare |
| `report_interval` | stringa | No | Periodo di tempo per il rapporto |

**Restituisce:** Dettagli attività e metriche delle prestazioni.

**Prompt di esempio:** &quot;Ottieni il report sulle prestazioni per l&#39;attività &#39;Homepage Hero Test&#39;.&quot;

## Strumenti di anteprima {#tools-preview}

### preview_activity

Genera URL di anteprima Controllo di qualità del browser per un&#39;attività [!DNL Target].

Crea collegamenti di anteprima cliccabili che forzano la visualizzazione di esperienze specifiche, ignorando le regole di targeting del pubblico. Funziona per attività A/B, XT e Automated Personalization.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `activity_id` | numero intero | Sì | L&#39;ID attività [!DNL Target] da visualizzare in anteprima |
| `experience_index` | numero intero | No | Indice delle esperienze basato su 0. Se omesso, restituisce gli URL per tutte le esperienze |
| `url` | stringa | No | URL della pagina per l’anteprima. Obbligatorio per le attività basate su moduli. Per le attività del Compositore esperienza visivo, se fornito, sostituisce la posizione creata |

**Restituisce:** informazioni sull&#39;attività (nome, tipo, stato), URL di anteprima per ogni esperienza e nomi e indici di esperienza.

**Esempio di prompt:** &quot;Genera URL di anteprima per 12345 attività in modo che sia possibile testare ogni esperienza nel browser.&quot;

## Strumenti token di risposta {#tools-response-tokens}

### list_target_response_tokens

Elenca tutti i token di risposta nel tenant [!DNL Target].

Recupera tutti i token di risposta configurati, sia incorporati che personalizzati.

Nessun parametro richiesto.

**Restituisce:** array JSON di oggetti token di risposta con stato `name`, `type` e `enabled`.

**Prompt di esempio:** &quot;Elenca tutti i token di risposta.&quot;

### create_target_response_token

Crea un nuovo token di risposta personalizzato per la raccolta di dati aggiuntivi nelle risposte [!DNL Target].

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `token_name` | stringa | Sì | Nome del token di risposta |
| `token_type` | stringa | Sì | Tipo di token: `SCRIPT`, `ACTIVITY`, `MBOX`, `GEO` o `CRS` |

**Restituisce:** L&#39;oggetto token di risposta creato.

**Esempio di prompt:** &quot;Creare un token di risposta personalizzato denominato &#39;campaign_id&#39; di tipo ACTIVITY.&quot;

## Strumenti di revisione {#tools-revisions}

### get_target_revisions

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

### get_target_entity_revisions

Ottieni tutte le revisioni di un’entità specifica per ID.

| Parametro | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `revision_resource_type` | stringa | Sì | Tipo di risorsa: `activity`, `offer` o `audience` |
| `entity_id` | numero intero | Sì | Identificatore univoco dell’entità |

**Restituisce:** array JSON di tutte le revisioni per l&#39;entità specificata.

**Prompt di esempio:** &quot;Mostra tutte le modifiche apportate al 12345 attività&quot;.

## Strumenti modello {#tools-templates}

### list_target_templates

Elencare le risorse MCP disponibili e i modelli per la creazione di attività e offerte.

Nessun parametro richiesto.

**Restituisce:** oggetto JSON in cui sono elencati i modelli e le risorse disponibili.

**Esempio di prompt:** &quot;Quali modelli sono disponibili per la creazione di attività?&quot;

## Riepilogo strumenti {#tools-summary}

| Categoria | Conteggio | Strumenti |
|---|---|---|
| Attività | 17 | `list_target_activities`, `get_ab_activity`, `get_xt_activity`, `get_abt_activity`, `create_ab_activity`, `create_xt_activity`, `update_ab_activity`, `update_xt_activity`, `update_abt_activity`, `update_activity_schedule`, `update_activity_state`, `update_activity_name`, `update_activity_priority`, `add_activity_variant`, `update_traffic_split`, `update_variant_offer`, `remove_activity_variant` |
| Offerta | 5 | `list_target_offers`, `get_target_offer`, `create_target_offer`, `create_target_json_offer`, `update_target_offer` |
| Pubblico | 2 | `list_target_audiences`, `create_target_audience` |
| Mbox | 3 | `list_target_mboxes`, `get_target_mbox`, `list_target_mbox_profile_attributes` |
| Proprietà | 1 | `list_target_properties` |
| Generazione di rapporti | 5 | `get_ab_performance_report`, `get_ab_orders_report`, `get_xt_performance_report`, `get_xt_orders_report`, `get_activity_report_by_name` |
| Anteprima | 1 | `preview_activity` |
| Token di risposta | 2 | `list_target_response_tokens`, `create_target_response_token` |
| Revisione | 2 | `get_target_revisions`, `get_target_entity_revisions` |
| Modello | 1 | `list_target_templates` |
| **Totale** | **39** | |

## Risorse correlate {#tools-related}

* [Utilizzo dei client MCP](target-mcp.md)
* [Hosting autonomo del server  [!DNL Adobe Target] MCP](target-mcp-self-hosted.md)
* [[!DNL Adobe Target] Riferimento API amministratore](https://developers.adobe.com/target/administer/admin-api/){target="_blank"}
