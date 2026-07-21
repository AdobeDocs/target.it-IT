---
title: Estensione dei flag per la guida all’integrazione web
description: Scopri come integrare l’estensione Flags con Adobe Experience Platform Web SDK (Alloy) per le applicazioni web.
hide: true
source-git-commit: 9c6f2b72f964b06da51e1f3655545147d7240a93
workflow-type: tm+mt
source-wordcount: '1180'
ht-degree: 7%

---

# Estensione flag per il web {#web-extension-integration-guide}

Questa guida descrive come integrare l’estensione Flags con Adobe Experience Platform Web SDK (Alloy) per le applicazioni web. L’estensione Flags abilita la gestione dei flag di funzione e i rollout controllati per le esperienze web.

## Prerequisiti {#prerequisites}

Prima di implementare l’estensione Flags, assicurati di disporre di:

* Una proprietà Web configurata in [Raccolta dati Adobe Experience Platform](https://experience.adobe.com/#/data-collection)
* Estensione Adobe Experience Platform Web SDK installata
* Un ID organizzazione Adobe Experience Cloud
* Accesso ai flag nella tua organizzazione

### Autorizzazioni richieste {#required-permissions}

Assicurati di disporre dei seguenti diritti di proprietà:

* Sviluppa
* Gestire le estensioni

## Dipendenze delle estensioni {#extension-dependencies}

L&#39;estensione Flags richiede la seguente estensione Adobe Experience Platform:

| Estensione | Descrizione | Obbligatorio |
|---|---|---|
| Adobe Experience Platform Web SDK | Fornisce funzionalità di base, tra cui la comunicazione e la gestione delle identità di Edge Network | Sì |

Prima di installare l’estensione Flags, assicurati che questa estensione sia installata nella tua proprietà Web Data Collection.

## Configurare l’estensione dei flag in Raccolta dati {#configure}

### Installare l’estensione {#install-extension}

1. Accedi a [experience.adobe.com](https://experience.adobe.com) utilizzando le credenziali Adobe ID.
1. Passa a **Raccolta dati** > **Tag**.
1. Seleziona la proprietà tag desiderata.
1. Passa a **Estensioni** > **Catalogo**.
1. Cerca **Flag** e seleziona la scheda dell&#39;estensione.
1. Selezionare **Installa**.

### Configurare le impostazioni dell’estensione {#configure-settings}

Quando installi l’estensione Flags, viene visualizzata la pagina di configurazione. Configura le seguenti impostazioni:

| Impostazione | Descrizione | Obbligatorio |
|---|---|---|
| ID client | Un identificatore univoco dell’applicazione nei flag. | Sì |

### Salva e pubblica {#save-publish}

1. Seleziona **Salva** per salvare la configurazione dell&#39;estensione.
1. Segui il flusso di pubblicazione per distribuire le modifiche:
   1. Aggiungi l&#39;estensione a una libreria.
   1. Genera nell’ambiente di sviluppo.
   1. Convalida con Adobe Experience Platform Debugger.
   1. Promuovi a staging e produzione.

## Aggiungi il codice di incorporamento dei tag al tuo sito web {#embed-code}

Dopo aver pubblicato la libreria Tag, devi aggiungere il codice di incorporamento al sito web. Il codice di incorporamento è un tag `<script>` che carica la libreria Tag e tutte le estensioni configurate, inclusa l&#39;estensione Flags.

### Copiare il codice di incorporamento {#copy-embed-code}

1. In Raccolta dati, passa alla proprietà web.
1. Seleziona **Ambienti** nel menu di navigazione a sinistra.
1. Nella riga dell&#39;ambiente di destinazione (Sviluppo, Staging o Produzione), seleziona l&#39;icona della casella nella colonna **Installa**.
1. Nella finestra di dialogo **Istruzioni di installazione Web**, Tag utilizza per impostazione predefinita il codice di incorporamento asincrono.
1. Seleziona l&#39;icona **Copia** per copiare il codice da incorporare negli Appunti.
1. Seleziona **Chiudi** per chiudere il modale.

>[!NOTE]
>
>Ogni ambiente ha un URL di codice di incorporamento univoco. Per ulteriori informazioni, consulta Ambienti.

### Implementare il codice di incorporamento {#implement-embed-code}

Aggiungere il codice di incorporamento nell&#39;elemento `<head>` delle pagine HTML. Il codice di incorporamento deve essere posizionato prima di altri script che dipendono dalla libreria Tag:

```html
<!DOCTYPE html>
<html>
<head>
  <title>My Website</title>

  <!-- Adobe Experience Platform Tags embed code -->
  <script src="https://assets.adobedtm.com/yourcompany/your-property/launchENxxxxxxxxxxx.min.js" async></script>
</head>
<body>
  <!-- Your page content -->
</body>
</html>
```

>[!NOTE]
>
>Sostituisci l&#39;URL `src` con il codice di incorporamento effettivo dalla pagina Ambienti. L&#39;URL contiene l&#39;identificatore società, la proprietà e l&#39;identificatore ambiente (ad esempio, `launch-EN123456789abcdef.min.js`).

### Valutare i flag con i componenti Tag {#tags-components}

L&#39;estensione Flags fornisce superfici di valutazione native per i tag.

| Componente | Tipo | Descrizione |
|---|---|---|
| Funzionalità abilitata | Condizione | Restituisce un valore che indica se una funzione è abilitata per l&#39;utente/contesto corrente |
| Flag di funzione | Elemento dati | Restituisce un oggetto booleano o a funzione completa |

## Inizializzare SDK {#initialize-sdk}

L’estensione Flags viene inizializzata automaticamente al caricamento della libreria Tags. L’estensione espone il client su:

```javascript
window._flagClient
```

### Attesa della preparazione del cliente {#client-readiness}

I tag vengono caricati in modo asincrono. Prima di chiamare i metodi SDK dal codice personalizzato, attendi che il client sia inizializzato:

```javascript
window.flagClientReady
  .then(function () {
    const enabled = window._flagClient.isFeatureEnabled('my-feature', context);
    // Use enabled to select the feature or fallback behavior.
  })
  .catch(function (error) {
    console.error('Flags initialization failed:', error);
  });
```

## Contesto di valutazione {#evaluation-context}

`FeatureEvaluationContext` include gli attributi di identità (necessari per la valutazione, bucket A/B e analisi) e gli attributi di targeting facoltativi (utilizzati per la corrispondenza delle regole).

| Proprietà | Obbligatorio | Descrizione |
|---|---|---|
| `identityNamespace` | Sì | Spazio dei nomi identità (vedi [Spazi dei nomi identità Adobe](https://experienceleague.adobe.com/it/docs/experience-platform/identity/features/namespaces)). Valori comuni: `ECID`, `Email`, `CRMId`. |
| `identityId` | Sì | Valore identità per l’utente corrente. |
| `attributes` | No | `Record<string, string[]>`. Chiave è il nome dell&#39;attributo di contesto utilizzato dalle regole del flag (ad esempio `locale`, `platform`). Valore è l&#39;elenco dei valori degli attributi candidati per la chiave. |

Nei componenti Tag, imposta i valori predefiniti di identità nell’interfaccia utente della condizione o dell’elemento dati. L&#39;elemento dati Flag di funzione accetta anche attributi di runtime tramite `getVar(name, attributes)` quando il secondo argomento è una mappa di attributi flat.

### Utilizzo {#usage}

```javascript
const context = {
  identityNamespace: 'ECID',
  identityId: 'your-visitor-ecid',
  attributes: {
    locale: ['en-US'],
    platform: ['web']
  }
};
```

## Documentazione sulle API {#api-reference}

### isFeatureEnabled {#is-feature-enabled}

`isFeatureEnabled` restituisce se una funzione Flag è attivata o disattivata per il contesto specificato. Passaggio `featureKey` e `FeatureEvaluationContext`. Vedi [Contesto di valutazione](#evaluation-context). Utilizza la condizione Tag **Funzionalità abilitata** o chiama `window._flagClient.isFeatureEnabled(...)` dal codice personalizzato dopo l&#39;inizializzazione.

**Firma**

```javascript
isFeatureEnabled(featureKey: string, context: FeatureEvaluationContext): boolean
```

**Parametri**

| Parametro | Tipo | Descrizione |
|---|---|---|
| `featureKey` | stringa | Chiave della funzione da valutare nei flag |
| `context` | FeatureEvaluationContext | Attributi di identità (obbligatori) e di targeting facoltativo. Vedi [Contesto di valutazione](#evaluation-context). |

### Creare un elemento dati per i flag di funzione {#create-data-element}

Utilizzare un elemento dati quando è necessario un valore di flag disponibile come `%Data Element Name%` nelle regole o nel codice personalizzato.

**Passaggi**

1. Nella tua proprietà, vai a **Elementi dati** e seleziona **Aggiungi elemento dati**.
1. Nella schermata **Crea elemento dati**, configura i campi Tag:

   | Campo | Valore |
   |---|---|
   | Nome | Un nome descrittivo (ad esempio `checkout flag`) |
   | Estensione | Flag |
   | Tipo di elemento dati | Flag di funzione |

1. Configura i campi dell&#39;estensione **Flag**:

   | Campo | Obbligatorio | Descrizione |
   |---|---|---|
   | Chiave funzione | Sì | Chiave flag univoca (ad esempio `checkout_flag`) |
   | Tipo restituito | Sì | **Booleano (true/false)** — abilitato/disabilitato o **Oggetto funzionalità (dettagli completi)** — payload completo che include `meta` |

1. Seleziona **Salva**.

**Tipi restituiti**

| Tipo restituito | Risolve in |
|---|---|
| Boolean (true/false) | `true` se abilitato, `false` altrimenti |
| Oggetto funzione (dettagli completi) | Payload completo della funzionalità valutato oppure `null` se non soddisfa le regole |

### Utilizzare l’elemento dati {#use-data-element}

In una regola: riferimento per nome, ad esempio `%Test Flag%`.

Nel codice personalizzato, utilizzare `_satellite.getVar`. Con gli attributi di runtime, passa una mappa di attributi piatta come secondo argomento da valutare:

```javascript
var isEnabled = _satellite.getVar('Test Flag', {
  locale: ['en-US'],
  platform: ['web']
});

if (isEnabled) {
  // your custom code
} else {
  // your default code
}
```

### getFeature {#get-feature}

`getFeature` restituisce il payload della funzionalità valutata quando sono necessari metadati oltre a abilitati/disabilitati.

Utilizza un elemento dati **Flag di funzionalità** con **Tipo restituito: oggetto funzionalità (dettagli completi)** — vedi [Creare un elemento dati Flag di funzionalità](#create-data-element) — oppure chiama `window._flagClient.getFeature(...)` dal codice personalizzato dopo la risoluzione di `flagClientReady`.

**Firma**

```javascript
getFeature(featureKey: string, context: FeatureEvaluationContext): FeatureResult | null
```

**Parametri**

| Parametro | Tipo | Descrizione |
|---|---|---|
| `featureKey` | stringa | Chiave della funzione da valutare nei flag |
| `context` | FeatureEvaluationContext | Identità (obbligatoria) e attributi di targeting. Vedi [Contesto di valutazione](#evaluation-context). |

**Risposta**

*RisultatoFunzionalità*

| Campo | Tipo | Descrizione |
|---|---|---|
| `id` | numero | Identificatore numerico di funzione. `-1` per la sentinella di controllo a livello di funzionalità. |
| `key` | string \| null | Chiave funzione. `null` per la sentinella di controllo a livello di funzionalità. |
| `featureGroupKey` | string \| null | Chiave gruppo di funzioni, se disponibile |
| `meta` | string \| null | Metadati delle funzioni, se disponibili |
| `analyticsParam` | AnalyticsParam \| null | Dettagli di Analytics per la funzione valutata |

*AnalyticsParam*

| Campo | Tipo | Descrizione |
|---|---|---|
| `featureGroupId` | numero | Identificatore gruppo di funzioni numerico |
| `featureId` | numero | Identificatore numerico di funzione |
| `variantId` | number \| null | Identificatore variante (`0` per il controllo) |

**Comportamento gruppo di controllo**

| Scenario | isFeatureEnabled | getFeature | L’evento Analytics è FeatureEnabled | GetFeature evento di Analytics |
|---|---|---|---|---|
| Trattamento | `true` | Risultato normale | Sì | Sì |
| Controllo a livello di funzionalità | `false` | Sentinella (`id: -1`, `key: null`) | Sì (`variantId: 0`) | Sì |
| Criterio non corrispondente/non trovato | `false` | `null` | No | No |

**Esempio**

```javascript
var feature = _flagClient.getFeature('new-testflag', {
  identityNamespace: 'ECID',
  identityId: visitorEcid,
  attributes: {
    locale: ['en-US']
  }
});

var meta = feature && feature.meta;
if (meta) {
  // your custom code
} else {
  // your default code
}
```

### extensionVersion {#extension-version}

Restituisce la stringa della versione dell&#39;estensione Flags.

**Firma**

```javascript
_flagClient.extensionVersion(): string
```

**Esempio**

```javascript
const version = _flagClient.extensionVersion();
console.log(`Flags extension version: ${version}`);
```

## Riepilogo API {#api-summary}

| API | Restituisce |
|---|---|
| Flag di funzione (elemento dati Tag, booleano) | booleano |
| Flag di funzione (elemento dati Tag, oggetto) | Oggetto funzionalità o `null` |
| `window.flagClientReady` | Promise — attende l&#39;inizializzazione dell&#39;estensione |
| `window._flagClient.isFeatureEnabled(featureKey, context)` | booleano |
| `window._flagClient.getFeature(featureKey, context)` | Oggetto funzionalità o `null` |
| `window._flagClient.extensionVersion()` | Stringa della versione dell’estensione |

## Gestione degli errori {#error-handling}

L&#39;estensione gestisce gli errori correttamente:

| Scenario | Comportamento |
|---|---|
| Rete non disponibile all&#39;inizializzazione | SDK ritenta il recupero iniziale tre volte con backoff e l’inizializzazione non riesce. `window.flagClientReady` e `_satellite.getVar(...)` rifiutano con `Failed to initialize Flag`; `window._flagClient` rimane `undefined`. |
| Identità mancante nel contesto | La valutazione genera un errore. Specificare `identityNamespace` e `identityId` |
| Funzione non trovata | `getFeature` restituisce `null`; `isFeatureEnabled` restituisce `false` |

```javascript
try {
  const isEnabled = _flagClient.isFeatureEnabled('my-feature', context);
  // Use the result
} catch (error) {
  console.error('Evaluation failed:', error.message);
  // Use default value
}
```

## Best practice {#best-practices}

### Fornire un’identità coerente {#consistent-identity}

Utilizza lo stesso ID e lo stesso spazio dei nomi delle identità nelle valutazioni per creare contenitori coerenti nei rollout percentuali.

```javascript
const context = {
  identityNamespace: 'ECID',
  identityId: identity,
  attributes: {
    locale: ['en-US'],
    platform: ['web']
  }
};

const isEnabled = _flagClient.isFeatureEnabled('my-feature', context);
```

### Gestione corretta delle feature mancanti {#handle-missing}

Fornisci sempre un comportamento di fallback quando una funzione non viene trovata o la valutazione non riesce.

```javascript
const feature = _flagClient.getFeature('new-testflag', context);

if (feature && feature.meta) {
  // your custom code
} else {
  // Feature not enabled - use default code
}
```

### Valuta dopo caricamento pagina {#evaluate-after-load}

Prima di richiamare le API, assicurati che la libreria Tag e l&#39;estensione Flags siano state inizializzate. Utilizza l&#39;evento **Library Loaded** nelle regole, in un elemento dati **Feature Flag** oppure attendi `flagClientReady`:

```javascript
window.flagClientReady.then(function () {
  var isEnabled = window._flagClient.isFeatureEnabled('my-feature', context);
  // Use the result
});
```

## Vedi anche {#see-also}

* [Creare il primo flag di funzione](../../feature-flags/create-your-first-feature-flag.md)
* [Pubblico nei flag di funzione e nei gruppi di funzioni](../../audience/audience-in-feature-flags-and-feature-groups.md)
* [Reporting](../../feature-flags/reporting.md)

<!-- -->
