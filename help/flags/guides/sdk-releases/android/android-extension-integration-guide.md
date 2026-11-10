---
title: Guida all’integrazione di Flag per l’estensione Android
description: Scopri come integrare l’estensione Flags con Adobe Experience Platform Mobile SDK su Android.
badge: label="Beta" type="Informative"
hide: true
exl-id: 683ef4d4-e637-4b7b-b694-689c7e65a99e
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
source-git-commit: c1fafcfcd7d5d22781abdd10e6eb3c2b84136c2d
workflow-type: tm+mt
source-wordcount: '1379'
ht-degree: 4%
---
# Estensione flag per Android {#android-extension-integration-guide}

Questa guida descrive come integrare l’estensione Flags con Adobe Experience Platform Mobile SDK su Android.

## Prerequisiti {#prerequisites}

Prima di implementare l’estensione Flags, assicurati di disporre di:

* Una proprietà mobile configurata in [Raccolta dati di Adobe Experience Platform](https://experience.adobe.com/#/data-collection)
* L&#39;estensione Adobe Flags installata e configurata nella proprietà mobile
* Un ID organizzazione Adobe Experience Cloud
* Un flusso di dati Edge Network configurato nella tua proprietà mobile, per ricevere analisi dell’esposizione
* Android API 21 (Android 5.0 Lollipop) o versione successiva
* Mobile Core 3.6.0 o versione successiva (incluso in `sdk-bom` 3.17.0 e versioni successive)

## Dipendenze delle estensioni {#extension-dependencies}

L&#39;estensione Flags richiede le seguenti estensioni Adobe Experience Platform:

| Estensione | Descrizione | Obbligatorio |
|---|---|---|
| [Core mobile](https://developer.adobe.com/client-sdks/home/base/mobile-core/) | Fornisce configurazione, elaborazione di eventi e inizializzazione di SDK | Sì |
| [Ciclo di vita](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/) | Segnala quando l’app si sposta in primo piano o in background | Sì |
| [Edge Network](https://developer.adobe.com/client-sdks/edge/edge-network/) | Invia l&#39;analisi dell&#39;esposizione a Adobe Experience Platform | Sì |
| [Identità per Edge Network](https://developer.adobe.com/client-sdks/edge/identity-for-edge-network/) | Fornisce le identità utilizzate per assegnare gli utenti alle varianti | Sì |

Assicurati che queste estensioni siano installate nella proprietà mobile di Data Collection e incluse nelle dipendenze dell’app.

## Configurare l’estensione dei flag in Raccolta dati {#configure}

### Installare l’estensione {#install-extension}

1. Accedi a [Raccolta dati Adobe Experience Platform](https://experience.adobe.com/#/data-collection).

1. Seleziona il menu **[!UICONTROL Tag]** e scegli la tua proprietà mobile.

1. Passa a **[!UICONTROL Estensioni]** > **[!UICONTROL Catalogo]**.

1. Cerca **[!DNL Adobe Flags]** e seleziona **[!UICONTROL Installa]**.

   ![](../assets/extension-install.png)

1. Configura le impostazioni dell&#39;estensione:

   * **[!UICONTROL Sandbox]**: la sandbox Adobe Experience Platform contenente la configurazione dei flag.
   * **[!UICONTROL ID applicazione]**: l&#39;identificatore dell&#39;applicazione nei flag.

1. Seleziona **[!UICONTROL Salva]**.

1. Segui il [processo di pubblicazione](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/overview) per aggiornare la configurazione.

### Ottieni l’ID del file di ambiente {#environment-file-id}

1. Nella tua proprietà mobile, passa a **[!UICONTROL Ambienti]**.

1. Seleziona l&#39;icona della casella nella colonna **[!UICONTROL Installa]** dell&#39;ambiente selezionato.

   ![](../assets/extension-install-2.png)

1. Nella finestra di dialogo **[!UICONTROL Istruzioni di installazione per dispositivi mobili]**, copia **[!UICONTROL ID file ambiente]**.

   ![](../assets/extension-install-3.png)

## Aggiungere l’estensione Flags all’app {#add-to-app}

### Aggiungi dipendenze {#add-dependencies}

>[!IMPORTANT]
>
>L&#39;estensione Flags non fa parte della DBA di Mobile SDK. Sostituisci `<latest-version>` con la versione più recente da Maven Central. Senza una versione, Gradle non può risolvere la dipendenza.
>
></br>
>&gt;Per le applicazioni di produzione, Adobe consiglia di utilizzare numeri di versione espliciti invece delle versioni dinamiche come "3.+". Per ulteriori informazioni, vedere [Gestione delle dipendenze Gradle](https://docs.gradle.org/current/userguide/dependency_management.html).

Aggiungi le dipendenze seguenti al file `build.gradle.kts` (Cotlin) o `build.gradle` (Groovy) dell&#39;app:

>[!BEGINTABS]

>[!TAB Cotlino]

```kotlin
dependencies {
    // Adobe Experience Platform Mobile SDK BOM (3.17.0 or later)
    implementation(platform("com.adobe.marketing.mobile:sdk-bom:3.+"))

    // Required extensions (versions managed by the BOM)
    implementation("com.adobe.marketing.mobile:core")
    implementation("com.adobe.marketing.mobile:lifecycle")
    implementation("com.adobe.marketing.mobile:edge")
    implementation("com.adobe.marketing.mobile:edgeidentity")

    // Flags extension (not managed by the BOM; specify the version)
    implementation("com.adobe.marketing.mobile:flags:<latest-version>")
}
```

>[!TAB Scanalatura]

```groovy
dependencies {
    // Adobe Experience Platform Mobile SDK BOM (3.17.0 or later)
    implementation platform('com.adobe.marketing.mobile:sdk-bom:3.+')

    // Required extensions (versions managed by the BOM)
    implementation 'com.adobe.marketing.mobile:core'
    implementation 'com.adobe.marketing.mobile:lifecycle'
    implementation 'com.adobe.marketing.mobile:edge'
    implementation 'com.adobe.marketing.mobile:edgeidentity'

    // Flags extension (not managed by the BOM; specify the version)
    implementation 'com.adobe.marketing.mobile:flags:<latest-version>'
}
```

>[!ENDTABS]

### Inizializzare SDK {#initialize-sdk}

>[!IMPORTANT]
>
>Per le app di produzione, utilizza solo `LoggingMode.ERROR`. Non utilizzare `DEBUG` o `VERBOSE` nelle build delle versioni.

Inizializza Mobile SDK nella classe `Application` prima di richiamare le API dell&#39;estensione Flags. Utilizza l’ID file dell’ambiente dalla tua proprietà mobile in modo che l’app selezioni le impostazioni dei flag pubblicate in Raccolta dati.

`MobileCore.initialize` registra ogni estensione Adobe inclusa nelle dipendenze Gradle, inclusa l&#39;estensione Flags.

Quando si utilizza `MobileCore.initialize`, non chiamare anche `MobileCore.registerExtensions`, `MobileCore.lifecycleStart` o `MobileCore.lifecyclePause`. Questi vengono gestiti per te.

>[!BEGINTABS]

>[!TAB Cotlino]

```kotlin
import android.app.Application
import com.adobe.marketing.mobile.LoggingMode
import com.adobe.marketing.mobile.MobileCore

class MainApplication : Application() {

    override fun onCreate() {
        super.onCreate()

        MobileCore.setLogLevel(LoggingMode.ERROR)

        // Initialize with your Environment File ID from Data Collection
        MobileCore.initialize(this, "YOUR_ENVIRONMENT_FILE_ID")
    }
}
```

>[!TAB Java]

```java
import android.app.Application;
import com.adobe.marketing.mobile.LoggingMode;
import com.adobe.marketing.mobile.MobileCore;

public class MainApplication extends Application {

    @Override
    public void onCreate() {
        super.onCreate();

        MobileCore.setLogLevel(LoggingMode.ERROR);

        // Initialize with your Environment File ID from Data Collection
        MobileCore.initialize(this, "YOUR_ENVIRONMENT_FILE_ID");
    }
}
```

>[!ENDTABS]

### Registrare la classe Application {#register-application}

Registra la classe `Application` in `AndroidManifest.xml`:

```xml
<application
    android:name=".MainApplication"
    ... >
</application>
```

### Se si registrano manualmente le estensioni {#register-manually}

Se l&#39;app non può utilizzare `MobileCore.initialize` e registra le estensioni con `MobileCore.registerExtensions`, aggiungi `Flag.EXTENSION` all&#39;elenco. Utilizzare la classe Identity for Edge Network, `com.adobe.marketing.mobile.edge.identity.Identity`, non la precedente `com.adobe.marketing.mobile.Identity`.

```kotlin
import com.adobe.marketing.mobile.Edge
import com.adobe.marketing.mobile.Lifecycle
import com.adobe.marketing.mobile.MobileCore
import com.adobe.marketing.mobile.edge.identity.Identity
import com.adobe.marketing.mobile.flags.Flag

MobileCore.setApplication(this)
MobileCore.configureWithAppID("YOUR_ENVIRONMENT_FILE_ID")
MobileCore.registerExtensions(
    listOf(Lifecycle.EXTENSION, Identity.EXTENSION, Edge.EXTENSION, Flag.EXTENSION)
) { }
```

In questa configurazione, il ciclo di vita non viene tracciato automaticamente. Chiama `MobileCore.lifecycleStart(null)` in ogni attività di `onResume` e `MobileCore.lifecyclePause()` nel relativo `onPause`. Senza queste chiamate, l&#39;estensione aggiorna i flag mentre l&#39;app è in background e l&#39;analisi dell&#39;esposizione viene inviata in un secondo momento.

## Contesto di valutazione {#evaluation-context}

`FeatureEvaluationContext` contiene gli attributi di targeting utilizzati dalle regole dei flag. Non trasmetti un’identità: l’estensione la legge da Identity for Edge Network a ogni valutazione. Vedi [Identità personalizzata](#custom-identity).

| Metodo | Obbligatorio | Descrizione |
|---|---|---|
| `withAttributes(map)` | No | `Map<String, List<String>>`. Ogni chiave è un nome di attributo utilizzato dalle regole del flag (ad esempio, `locale` o `appVersion`). Ogni valore è l&#39;elenco di valori per l&#39;utente corrente (ad esempio, `["en_US"]`). |

* Per ogni valutazione è necessario specificare un contesto. Se non hai attributi, passa `FeatureEvaluationContext.builder().build()`.
* Chiamare `withAttributes` al massimo una volta per ogni generatore.
* Un contesto generato non può essere modificato, pertanto puoi riutilizzarlo tra le valutazioni.

### Utilizzo {#evaluation-context-usage}

>[!BEGINTABS]

>[!TAB Cotlino]

```kotlin
import com.adobe.marketing.mobile.flags.FeatureEvaluationContext

val ctx = FeatureEvaluationContext.builder()
    .withAttributes(
        mapOf(
            "locale" to listOf("en_US"),
            "platform" to listOf("ANDROID")
        )
    )
    .build()
```

>[!TAB Java]

```java
import com.adobe.marketing.mobile.flags.FeatureEvaluationContext;
import java.util.Arrays;
import java.util.HashMap;
import java.util.List;
import java.util.Map;

Map<String, List<String>> attrs = new HashMap<>();
attrs.put("locale", Arrays.asList("en_US"));
attrs.put("platform", Arrays.asList("ANDROID"));

FeatureEvaluationContext ctx = FeatureEvaluationContext.builder()
        .withAttributes(attrs)
        .build();
```

>[!ENDTABS]

### Attributi di targeting di esempio {#sample-attributes}

| Attributo | Descrizione | Valori di esempio |
|---|---|---|
| `locale` | Impostazioni locali dell&#39;utente | `["en_US"]`, `["fr_FR"]` |
| `platform` | Piattaforma | `["ANDROID"]` |
| `appVersion` | Versione app | `["3.0.0"]` |
| `deviceType` | Tipo di dispositivo | `["phone"]`, `["tablet"]` |

I nomi e i valori degli attributi devono corrispondere a quelli utilizzati nelle regole dei flag.

## Identità personalizzata {#custom-identity}

L&#39;estensione Flags utilizza Identity per [l&#39;estensione Edge Network](https://developer.adobe.com/client-sdks/edge/identity-for-edge-network/) per la risoluzione delle identità. Un flag di funzione può essere associato a un’identità personalizzata, ad esempio un ID del sistema di gestione delle relazioni con i clienti o un ID fedeltà, in modo che le suddivisioni e le analisi delle varianti siano legate all’identità rilevante per l’applicazione.

Lo spazio dei nomi delle identità personalizzate deve essere selezionato nell’interfaccia utente Flag quando viene creato il flag di funzione. Per valutare un flag rispetto a tale identità, la stessa identità deve essere presente nell&#39;identità Edge `identityMap` sul dispositivo, utilizzando lo spazio dei nomi corrispondente. Fornirla in fase di esecuzione con l&#39;API Identity for Edge Network `updateIdentities`.

### Aggiungere l’identità personalizzata alla mappa delle identità {#add-identity}

Aggiungi l’identità nello stesso spazio dei nomi configurato nel flag della funzione, prima di valutare il flag.

Quando aggiungi l’identità, tieni presente quanto segue:

* Lo spazio dei nomi deve corrispondere esattamente, comprese le maiuscole e minuscole.
* Se lo spazio dei nomi ha più identità, viene utilizzato quello contrassegnato come primario. In caso contrario, viene utilizzato il primo.
* Se durante la valutazione del flag manca l’identità, all’utente viene assegnato un ID temporaneo che cambia ogni volta che inizia l’app. La variante dell’utente può quindi cambiare tra un avvio dell’app e l’altro. Imposta sempre l’identità prima di valutare i flag che la utilizzano.

>[!BEGINTABS]

>[!TAB Cotlino]

```kotlin
import com.adobe.marketing.mobile.edge.identity.AuthenticatedState
import com.adobe.marketing.mobile.edge.identity.Identity
import com.adobe.marketing.mobile.edge.identity.IdentityItem
import com.adobe.marketing.mobile.edge.identity.IdentityMap

val identityMap = IdentityMap()
identityMap.addItem(
    IdentityItem("1111", AuthenticatedState.AUTHENTICATED, true),
    "userCRMId" // must match the namespace configured on the feature flag
)
Identity.updateIdentities(identityMap)
```

>[!TAB Java]

```java
import com.adobe.marketing.mobile.edge.identity.AuthenticatedState;
import com.adobe.marketing.mobile.edge.identity.Identity;
import com.adobe.marketing.mobile.edge.identity.IdentityItem;
import com.adobe.marketing.mobile.edge.identity.IdentityMap;

IdentityMap identityMap = new IdentityMap();
identityMap.addItem(
        new IdentityItem("1111", AuthenticatedState.AUTHENTICATED, true),
        "userCRMId"); // must match the namespace configured on the feature flag
Identity.updateIdentities(identityMap);
```

>[!ENDTABS]

## Documentazione sulle API {#api-reference}

### Callback e gestione degli errori {#callbacks-errors}

Queste regole si applicano a `isFeatureEnabled` e `getFeature`:

* Fornisci sempre un’esperienza predefinita. Passa un `AdobeCallbackWithError` e mostra la tua esperienza predefinita in `fail`. Con un `AdobeCallback` semplice, non viene chiamato nulla quando si verifica un errore.

* L&#39;estensione precarica le definizioni dei flag all&#39;avvio dell&#39;app. Successivamente, i flag vengono valutati sul dispositivo.

* Altri errori: `fail` è chiamato con `AdobeError.UNEXPECTED_ERROR` quando:

  * il tasto funzione è vuoto,
  * le impostazioni dei flag o l&#39;ID organizzazione Experience Cloud non sono presenti nella configurazione pubblicata, oppure
  * Impossibile scaricare le definizioni dei flag all’avvio dell’app (ad esempio, se il dispositivo non era in linea). L’estensione riprova al successivo aggiornamento della configurazione, in genere al successivo avvio dell’app.

### isFeatureEnabled {#is-feature-enabled}

Restituisce un valore che indica se una funzione è abilitata per l&#39;utente corrente.

**Firma**

>[!BEGINTABS]

>[!TAB Cotlino]

```kotlin
Flag.isFeatureEnabled(
    featureKey: String,
    evaluationContext: FeatureEvaluationContext,
    callback: AdobeCallback<Boolean>
)
```

>[!TAB Java]

```java
Flag.isFeatureEnabled(
    String featureKey,
    FeatureEvaluationContext evaluationContext,
    AdobeCallback<Boolean> callback);
```

>[!ENDTABS]

**Parametri**

| Parametro | Tipo | Descrizione |
|---|---|---|
| `featureKey` | Stringa | Chiave della funzione da valutare |
| `evaluationContext` | FeatureEvaluationContext | Attributi di targeting. Usa `FeatureEvaluationContext.builder().build()` se non ne hai. Vedi [Contesto di valutazione](#evaluation-context). |
| `callback` | AdobeCallback&lt;Booleano> | Chiamata eseguita con `true` se la funzionalità è abilitata per l&#39;utente. Chiamata eseguita con `false` se la funzionalità non viene trovata, le regole di targeting non corrispondono oppure l&#39;utente si trova nel gruppo di controllo. Passa un `AdobeCallbackWithError<Boolean>` per ricevere anche gli errori. |

**Esempi**

>[!BEGINTABS]

>[!TAB Cotlino]

```kotlin
import com.adobe.marketing.mobile.AdobeCallbackWithError
import com.adobe.marketing.mobile.AdobeError
import com.adobe.marketing.mobile.flags.Flag

Flag.isFeatureEnabled(
    "new-checkout",
    ctx,
    object : AdobeCallbackWithError<Boolean> {
        override fun call(isEnabled: Boolean?) {
            runOnUiThread {
                if (isEnabled == true) showNewCheckout() else showDefaultCheckout()
            }
        }

        override fun fail(error: AdobeError?) {
            runOnUiThread { showDefaultCheckout() }
        }
    }
)
```

>[!TAB Java]

```java
import com.adobe.marketing.mobile.AdobeCallbackWithError;
import com.adobe.marketing.mobile.AdobeError;
import com.adobe.marketing.mobile.flags.Flag;

Flag.isFeatureEnabled(
    "new-checkout",
    ctx,
    new AdobeCallbackWithError<Boolean>() {
        @Override
        public void call(Boolean isEnabled) {
            runOnUiThread(() -> {
                if (Boolean.TRUE.equals(isEnabled)) {
                    showNewCheckout();
                } else {
                    showDefaultCheckout();
                }
            });
        }

        @Override
        public void fail(AdobeError error) {
            runOnUiThread(() -> showDefaultCheckout());
        }
    }
);
```

>[!ENDTABS]

### getFeature {#get-feature}

Restituisce la funzione valutata per l’utente corrente, inclusi i metadati. Utilizza questa API quando devi attivarla o disattivarla.

**Firma**

>[!BEGINTABS]

>[!TAB Cotlino]

```kotlin
Flag.getFeature(
    featureKey: String,
    evaluationContext: FeatureEvaluationContext,
    callback: AdobeCallback<FeatureEvaluationResult>
)
```

>[!TAB Java]

```java
Flag.getFeature(
    String featureKey,
    FeatureEvaluationContext evaluationContext,
    AdobeCallback<FeatureEvaluationResult> callback);
```

>[!ENDTABS]

**Parametri**

| Parametro | Tipo | Descrizione |
|---|---|---|
| `featureKey` | Stringa | Chiave della funzione da valutare |
| `evaluationContext` | FeatureEvaluationContext | Attributi di targeting. Usa `FeatureEvaluationContext.builder().build()` se non ne hai. Vedi [Contesto di valutazione](#evaluation-context). |
| `callback` | AdobeCallback&lt;RisultatoValutazioneFunzionalità> | Chiamata eseguita con la funzionalità valutata o con `null` quando la funzionalità non viene fornita all&#39;utente: la chiave è sconosciuta, i criteri di targeting non sono soddisfatti o l&#39;utente si trova in una coorte di controllo. `null` è un risultato normale, non un errore. Le esposizioni della coorte di controllo sono ancora segnalate ad Analytics. Passa un `AdobeCallbackWithError<FeatureEvaluationResult>` per ricevere `fail(...)` per errori autentici, ad esempio timeout. |

Considera un risultato di `null` come &quot;funzionalità disattivata&quot; e mostra la tua esperienza predefinita. Mostra anche l&#39;esperienza predefinita quando viene chiamato `fail`, che si verifica solo in caso di errori autentici, ad esempio timeout.

**Risposta**

*RisultatoValutazioneFunzionalità*

| Campo | Tipo | Descrizione |
|---|---|---|
| `id` | Intero | ID funzione |
| `key` | Stringa | Chiave funzione |
| `featureGroupKey` | Stringa? | Chiave gruppo di feature, se la feature appartiene a un gruppo |
| `meta` | Stringa? | Metadati configurati per la funzione come testo normale o `null` se non è impostato alcun. Se hai memorizzato JSON, analizza la stringa nell’app. |
| `analyticsParam` | AnalyticsParam? | Dettagli di Analytics per la valutazione |

*AnalyticsParam*

| Campo | Tipo | Descrizione |
|---|---|---|
| `featureGroupId` | Intero | ID gruppo di funzioni |
| `featureId` | Intero | ID funzione |
| `variantId` | Stringa? | ID della variante a cui è stato assegnato l’utente |

**Esempi**

>[!BEGINTABS]

>[!TAB Cotlino]

```kotlin
import com.adobe.marketing.mobile.AdobeCallbackWithError
import com.adobe.marketing.mobile.AdobeError
import com.adobe.marketing.mobile.flags.FeatureEvaluationResult
import com.adobe.marketing.mobile.flags.Flag

Flag.getFeature(
    "new-checkout",
    ctx,
    object : AdobeCallbackWithError<FeatureEvaluationResult> {
        override fun call(feature: FeatureEvaluationResult?) {
            val meta = feature?.meta
            runOnUiThread {
                if (!meta.isNullOrEmpty()) applyExperience(meta) else showDefaultExperience()
            }
        }

        override fun fail(error: AdobeError?) {
            runOnUiThread { showDefaultExperience() }
        }
    }
)
```

>[!TAB Java]

```java
import com.adobe.marketing.mobile.AdobeCallbackWithError;
import com.adobe.marketing.mobile.AdobeError;
import com.adobe.marketing.mobile.flags.FeatureEvaluationResult;
import com.adobe.marketing.mobile.flags.Flag;

Flag.getFeature(
    "new-checkout",
    ctx,
    new AdobeCallbackWithError<FeatureEvaluationResult>() {
        @Override
        public void call(FeatureEvaluationResult feature) {
            final String meta = feature != null ? feature.getMeta() : null;
            runOnUiThread(() -> {
                if (meta != null && !meta.isEmpty()) {
                    applyExperience(meta);
                } else {
                    showDefaultExperience();
                }
            });
        }

        @Override
        public void fail(AdobeError error) {
            runOnUiThread(() -> showDefaultExperience());
        }
    }
);
```

>[!ENDTABS]

### extensionVersion {#extension-version}

Restituisce la versione dell&#39;estensione Flags.

**Sintassi**

```kotlin
Flag.extensionVersion(): String
```

**Esempio**

*Cotlino*

```kotlin
val version = Flag.extensionVersion()
```

*Java*

```java
String version = Flag.extensionVersion();
```

## Riepilogo API {#api-summary}

| API | Restituisce |
|---|---|
| `isFeatureEnabled(featureKey, evaluationContext, callback)`. Vedi [isFeatureEnabled](#is-feature-enabled). | Booleano tramite callback |
| `getFeature(featureKey, evaluationContext, callback)`. Vedi [getFeature](#get-feature). | FeatureEvaluationResult tramite callback |
| `extensionVersion()` | Stringa |

## Eseguire il debug {#debugging}

Per eseguire il debug, impostare `MobileCore.setLogLevel(LoggingMode.DEBUG)` in una build di debug e filtrare Logcat per `Flags`. Dovresti visualizzare un messaggio `Discovered extension` da MobileCore per `com.adobe.marketing.mobile.flags.FlagExtension`.


