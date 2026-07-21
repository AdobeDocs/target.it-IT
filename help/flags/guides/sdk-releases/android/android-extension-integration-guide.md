---
title: Guida all’integrazione di Flag per l’estensione Android
description: Scopri come integrare l’estensione Flags con Adobe Experience Platform Mobile SDK su Android.
hide: true
exl-id: 683ef4d4-e637-4b7b-b694-689c7e65a99e
source-git-commit: eeba7af62ab101e687852ce993a001832ce4a83b
workflow-type: tm+mt
source-wordcount: '983'
ht-degree: 4%

---

# Estensione flag per Android {#android-extension-integration-guide}

Questa guida descrive come integrare l’estensione Flags con Adobe Experience Platform Mobile SDK su Android.

## Prerequisiti {#prerequisites}

Prima di implementare l’estensione Flags, assicurati di disporre di:

* Una proprietà mobile configurata in [Raccolta dati di Adobe Experience Platform](https://experience.adobe.com/#/data-collection)
* L&#39;estensione Flags installata e configurata nella proprietà mobile
* Un ID organizzazione Adobe Experience Cloud
* SDK minimo: API 21 (Android 5.0 Lollipop)

## Dipendenze delle estensioni {#extension-dependencies}

L&#39;estensione Flags richiede le seguenti estensioni Adobe Experience Platform:

| Estensione | Descrizione | Obbligatorio |
|---|---|---|
| Core mobile | Offre funzionalità di base, tra cui configurazione ed elaborazione degli eventi | Sì |
| Ciclo di vita | Raccoglie i dati del ciclo di vita dell&#39;applicazione e della sessione per Mobile SDK | Sì |
| Edge Network | Abilita la comunicazione con Adobe Experience Platform Edge Network | Sì |
| Edge Identity | Abilita la gestione delle identità da un’app mobile quando si utilizza l’estensione Edge Network | Sì |

Assicurati che queste estensioni siano installate nella proprietà mobile di Data Collection e incluse nelle dipendenze dell’app.

## Configurare l’estensione dei flag in Raccolta dati {#configure}

### Installare l’estensione {#install-extension}

1. Accedi a [Raccolta dati Adobe Experience Platform](https://experience.adobe.com/#/data-collection).
1. Seleziona la scheda **Tag** e scegli la tua proprietà mobile.
1. Passa a **Estensioni** > **Catalogo**.
1. Cerca **Estensione flag** e seleziona **Installa**.
1. Configura le impostazioni dell&#39;estensione:

   | Impostazione | Descrizione |
   |---|---|
   | ID applicazione | Un identificatore univoco per l’applicazione nei flag |

1. Seleziona **Salva**.
1. Segui il [processo di pubblicazione](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/overview) per aggiornare la configurazione.

### Ottieni l’ID del file di ambiente {#environment-file-id}

1. Nella tua proprietà mobile, passa a **Ambienti**.
1. Seleziona l&#39;icona della casella nella colonna **Installa** dell&#39;ambiente.
1. Nella finestra di dialogo **Istruzioni di installazione per dispositivi mobili**, copia **ID file ambiente**.

## Aggiungere l’estensione Flags all’app {#add-to-app}

### Aggiungi dipendenze {#add-dependencies}

Aggiungi le dipendenze di Mobile SDK al progetto. L&#39;estensione Flags richiede Mobile Core e le estensioni relative ad Edge elencate di seguito.

#### Utilizzo di Gradle con DBA (scelta consigliata) {#gradle-bom}

Aggiungi le dipendenze seguenti al file `build.gradle.kts` dell&#39;app:

```kotlin
dependencies {
    // Adobe Experience Platform Mobile SDK BOM
    implementation(platform("com.adobe.marketing.mobile:sdkbom:3.+"))

    // Required extensions
    implementation("com.adobe.marketing.mobile:core")
    implementation("com.adobe.marketing.mobile:lifecycle")
    implementation("com.adobe.marketing.mobile:edge")
    implementation("com.adobe.marketing.mobile:edgeidentity")
}
```

#### Utilizzo di Gradle (Groovy) {#gradle-groovy}

```groovy
dependencies {
    // Adobe Experience Platform Mobile SDK BOM
    implementation platform('com.adobe.marketing.mobile:sdkbom:3.+')

    // Required extensions
    implementation 'com.adobe.marketing.mobile:core'
    implementation 'com.adobe.marketing.mobile:lifecycle'
    implementation 'com.adobe.marketing.mobile:edge'
    implementation 'com.adobe.marketing.mobile:edgeidentity'
}
```

>[!IMPORTANT]
>
>Per le applicazioni di produzione, Adobe consiglia di utilizzare numeri di versione espliciti anziché versioni dinamiche. Per ulteriori informazioni, vedere [Gestione delle dipendenze Gradle](https://docs.gradle.org/current/userguide/dependency_management.html).

### Aggiungere la dipendenza Flag {#add-flags-dependency}

#### Utilizzo dell’archivio Maven in hosting (consigliato) {#hosted-maven}

Aggiungere l&#39;archivio Maven dei flag al blocco `repositories` in `settings.gradle.kts`:

```kotlin
maven {
    url = uri("<HTTPS Flags Maven repository URL>")
}
```

Per un file Groovy `settings.gradle`:

```groovy
maven {
    url = uri('<HTTPS Flags Maven repository URL>')
}
```

Sostituire `<HTTPS Flags Maven repository URL>` con l&#39;URL dell&#39;archivio protetto fornito per l&#39;estensione Flags.

Quindi aggiungi la dipendenza dei flag con versione a `build.gradle.kts` dell&#39;app:

```kotlin
implementation("com.adobe.marketing.mobile:flags:<version>")
```

Per un file Groovy `build.gradle`:

```groovy
implementation 'com.adobe.marketing.mobile:flags:<version>'
```

Sostituisci `<version>` con la versione esatta dell&#39;estensione Flags fornita per la tua versione.

#### Utilizzo del pacchetto di distribuzione Contrassegni {#distribution-package}

Il pacchetto di distribuzione dell’estensione Flags include:

* `flags-3.x.aar`
* `flags-3.x.module`
* `flags-3.x.pom`

Rendi l’estensione disponibile per il progetto Android utilizzando uno dei seguenti metodi:

* Pubblica tutti i file dal pacchetto di distribuzione in un archivio Maven locale o privato e configura il progetto per l’utilizzo di tale archivio.
* Aggiungi `flags-3.x.aar` direttamente al progetto e dichiara le dipendenze transitive specificate in `flags-3.x.pom`.

### Aggiungere autorizzazioni {#add-permissions}

Aggiungi le seguenti autorizzazioni al file `AndroidManifest.xml`:

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

### Inizializzare SDK {#initialize-sdk}

Inizializza Mobile SDK nella classe `Application` prima di richiamare le API dell&#39;estensione Flags. Utilizza l&#39;ID file dell&#39;ambiente dalla tua proprietà mobile con `MobileCore.initialize` in modo che l&#39;app selezioni le impostazioni dei flag pubblicate in Raccolta dati.

#### Utilizzo di MobileCore.initialize {#mobile-core-initialize}

Disponibile a partire dalla versione DBA 3.8.0 di Android, questa API inizializza il SDK con il file dell’ambiente di raccolta dati.

>[!IMPORTANT]
>
>Per le app di produzione, utilizza solo `LoggingMode.ERROR`; non utilizzare `DEBUG` o `VERBOSE` nelle build delle versioni.

**Cotlino**

```kotlin
import android.app.Application
import com.adobe.marketing.mobile.LoggingMode
import com.adobe.marketing.mobile.MobileCore

class MainApplication : Application() {

    override fun onCreate() {
        super.onCreate()

        // Production: use LoggingMode.ERROR only. Do not use DEBUG or VERBOSE in release builds.
        MobileCore.setLogLevel(LoggingMode.ERROR)

        // Initialize with your Environment File ID from Data Collection
        MobileCore.initialize(this, "YOUR_ENVIRONMENT_FILE_ID")
    }
}
```

**Java**

```java
import android.app.Application;
import com.adobe.marketing.mobile.LoggingMode;
import com.adobe.marketing.mobile.MobileCore;

public class MainApplication extends Application {

    @Override
    public void onCreate() {
        super.onCreate();

        // Production: use LoggingMode.ERROR only. Do not use DEBUG or VERBOSE in release builds.
        MobileCore.setLogLevel(LoggingMode.ERROR);

        // Initialize with your Environment File ID from Data Collection
        MobileCore.initialize(this, "YOUR_ENVIRONMENT_FILE_ID", null);
    }
}
```

### Registrare la classe Application {#register-application}

Registra la classe `Application` in `AndroidManifest.xml`:

```xml
<application
    android:name=".MainApplication"
    ... >
</application>
```

## Contesto di valutazione {#evaluation-context}

La classe `FeatureEvaluationContext` include gli attributi di targeting (utilizzati per la corrispondenza delle regole dei flag).

| Metodo | Obbligatorio | Descrizione |
|---|---|---|
| `withAttributes(map)` | No | `Map<String, List<String>>`. Chiave è il nome dell&#39;attributo di contesto utilizzato dalle regole del flag (ad esempio `locale`, `platform`, `appVersion`, `deviceType`). Valore è l&#39;elenco dei valori degli attributi candidati per la chiave per l&#39;utente/sessione corrente (ad esempio `["en_US"]` o `["phone"]`). |

**Cotlino**

```kotlin
import com.adobe.marketing.mobile.flags.FeatureEvaluationContext

val attrs = mapOf(
    "locale" to listOf("en_US"),
    "platform" to listOf("ANDROID")
)

val ctx = FeatureEvaluationContext.builder()
    .withAttributes(attrs)
    .build()
```

**Java**

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

### Identità personalizzata {#custom-identity}

L&#39;estensione Flags utilizza l&#39;estensione Identity for Edge Network per la risoluzione delle identità. Un flag di funzione può essere associato a un’identità personalizzata (ad esempio, un ID del sistema di gestione delle relazioni con i clienti o un ID fedeltà) in modo che le suddivisioni e le analisi delle varianti siano legate all’identità rilevante per l’applicazione.

Lo spazio dei nomi delle identità personalizzate deve essere selezionato nell’interfaccia utente Flag quando viene creato il flag di funzione. Per valutare un flag rispetto a tale identità, la stessa identità deve essere presente nell&#39;identità Edge `identityMap` sul dispositivo, utilizzando lo spazio dei nomi corrispondente. Fornirla in fase di esecuzione con l&#39;API Identity for Edge Network `updateIdentities`.

#### Aggiungere l’identità personalizzata a Identity Map {#add-identity}

Aggiungi l’identità nello stesso spazio dei nomi configurato sul flag della funzione.

**Cotlino**

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

**Java**

```java
import com.adobe.marketing.mobile.edge.identity.AuthenticatedState;
import com.adobe.marketing.mobile.edge.identity.Identity;
import com.adobe.marketing.mobile.edge.identity.IdentityItem;
import com.adobe.marketing.mobile.edge.identity.IdentityMap;

final IdentityItem item = new IdentityItem("1111", AuthenticatedState.AUTHENTICATED, true);
final IdentityMap identityMap = new IdentityMap();
identityMap.addItem(item, "userCRMId"); // must match the namespace configured on the feature flag
Identity.updateIdentities(identityMap);
```

## Documentazione sulle API {#api-reference}

### isFeatureEnabled {#is-feature-enabled}

`isFeatureEnabled` restituisce se una funzione Flag è attivata o disattivata per il contesto specificato. Passa `featureKey`, un `FeatureEvaluationContext` (attributi di targeting facoltativi) e un callback. Vedi [Contesto di valutazione](#evaluation-context).

**Firma**

*Cotlino*

```kotlin
Flag.isFeatureEnabled(
    featureKey: String,
    evaluationContext: FeatureEvaluationContext,
    callback: AdobeCallback<Boolean>
)
```

*Java*

```java
Flag.isFeatureEnabled(
    String featureKey,
    FeatureEvaluationContext evaluationContext,
    AdobeCallback<Boolean> callback);
```

**Parametri**

| Parametro | Tipo | Descrizione |
|---|---|---|
| `featureKey` | Stringa | Chiave della funzione da valutare nei flag |
| `evaluationContext` | FeatureEvaluationContext | Includere gli attributi di targeting in base alle esigenze; utilizzare `FeatureEvaluationContext.builder().build()` per un contesto vuoto. Vedi [Contesto di valutazione](#evaluation-context). |
| `callback` | AdobeCallback&lt;Booleano> | Richiamato con `true` se la funzionalità è abilitata, `false` in caso contrario. È inoltre possibile passare `AdobeCallbackWithError<Boolean>` per gestire `fail(...)`. |

**Esempi**

*Cotlino*

```kotlin
import com.adobe.marketing.mobile.AdobeCallback
import com.adobe.marketing.mobile.flags.Flag

Flag.isFeatureEnabled(
    "new-flag",
    ctx,
    object : AdobeCallback<Boolean> {
        override fun call(isEnabled: Boolean?) {
            if (isEnabled == true) {
                // run the feature-specific behavior
            } else {
                // fall back to the default behavior
            }
        }
    }
)
```

*Java*

```java
import com.adobe.marketing.mobile.AdobeCallback;
import com.adobe.marketing.mobile.flags.Flag;

Flag.isFeatureEnabled(
    "new-flag",
    ctx,
    new AdobeCallback<Boolean>() {
        @Override
        public void call(Boolean isEnabled) {
            if (Boolean.TRUE.equals(isEnabled)) {
                // run the feature-specific behavior
            } else {
                // fall back to the default behavior
            }
        }
    }
);
```

### getFeature {#get-feature}

`getFeature` restituisce il payload della funzionalità valutata per il contesto specificato. Utilizza questa API quando hai bisogno di più di abilitato/disabilitato e desideri metadati o valori di funzionalità.

**Firma**

*Cotlino*

```kotlin
Flag.getFeature(
    featureKey: String,
    evaluationContext: FeatureEvaluationContext,
    callback: AdobeCallback<FeatureEvaluationResult>
)
```

*Java*

```java
Flag.getFeature(
    String featureKey,
    FeatureEvaluationContext evaluationContext,
    AdobeCallback<FeatureEvaluationResult> callback);
```

**Parametri**

| Parametro | Tipo | Descrizione |
|---|---|---|
| `featureKey` | Stringa | Chiave della funzione da valutare nei flag |
| `evaluationContext` | FeatureEvaluationContext | Includere gli attributi di targeting in base alle esigenze; utilizzare `FeatureEvaluationContext.builder().build()` per un contesto vuoto. Vedi [Contesto di valutazione](#evaluation-context). |
| `callback` | AdobeCallback&lt;RisultatoValutazioneFunzionalità> | Richiamato con il payload della funzionalità valutata; potrebbe essere `null` quando la funzionalità non viene trovata. È inoltre possibile passare `AdobeCallbackWithError<FeatureEvaluationResult>` per gestire `fail(...)`. |

**Risposta**

*RisultatoValutazioneFunzionalità*

| Campo | Tipo | Descrizione |
|---|---|---|
| `id` | Intero | Identificatore numerico di funzione |
| `key` | Stringa | Chiave funzione |
| `featureGroupKey` | Stringa? | Chiave gruppo di funzioni, se disponibile |
| `meta` | Stringa? | Metadati delle funzioni come stringa JSON, se disponibili |
| `analyticsParam` | AnalyticsParam? | Dettagli di Analytics per la funzione valutata |

*AnalyticsParam*

| Campo | Tipo | Descrizione |
|---|---|---|
| `featureGroupId` | Intero | Identificatore gruppo di funzioni numerico |
| `featureId` | Intero | Identificatore numerico di funzione |
| `variantId` | Stringa? | Identificatore variante |

**Esempi**

*Cotlino*

```kotlin
import com.adobe.marketing.mobile.AdobeCallback
import com.adobe.marketing.mobile.flags.FeatureEvaluationResult
import com.adobe.marketing.mobile.flags.Flag

Flag.getFeature(
    "new-flag",
    ctx,
    object : AdobeCallback<FeatureEvaluationResult> {
        override fun call(feature: FeatureEvaluationResult?) {
            val meta = feature?.meta
            if (!meta.isNullOrEmpty()) {
                // Feature metadata is available: use it to drive the feature behavior
            } else {
                // No metadata available: fall back to the default behavior
            }
        }
    }
)
```

*Java*

```java
import com.adobe.marketing.mobile.AdobeCallback;
import com.adobe.marketing.mobile.flags.FeatureEvaluationResult;
import com.adobe.marketing.mobile.flags.Flag;

Flag.getFeature(
    "new-flag",
    ctx,
    new AdobeCallback<FeatureEvaluationResult>() {
        @Override
        public void call(FeatureEvaluationResult feature) {
            String meta = feature != null ? feature.getMeta() : null;
            if (meta != null && !meta.isEmpty()) {
                // Feature metadata is available: use it to drive the feature behavior
            } else {
                // No metadata available: fall back to the default behavior
            }
        }
    }
);
```

### extensionVersion {#extension-version}

Restituisce la stringa della versione dell&#39;estensione Flags.

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
| `isFeatureEnabled(featureKey, evaluationContext, callback)`. `FeatureEvaluationContext` contiene attributi di targeting per le regole. Consulta [Valutazione delle funzionalità](#is-feature-enabled). | Booleano tramite callback |
| `getFeature(featureKey, evaluationContext, callback)`. Restituisce il payload della funzione valutato per il contesto specificato. Vedi [getFeature](#get-feature). | FeatureEvaluationResult tramite callback |
| `extensionVersion()` | Stringa |

## Vedi anche {#see-also}

* [Applicazioni mobili](../../integrate/mobile-applications.md)
* [SDK](../../integrate/sdks.md)

<!-- -->
