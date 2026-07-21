---
title: Guida all’integrazione di Flag per l’estensione iOS
description: Scopri come integrare l’estensione Flags con Adobe Experience Platform Mobile SDK su iOS.
hide: true
source-git-commit: eeba7af62ab101e687852ce993a001832ce4a83b
workflow-type: tm+mt
source-wordcount: '1035'
ht-degree: 5%

---

# Estensione flag per iOS {#ios-extension-integration-guide}

Questa guida descrive come integrare l’estensione Flags con Adobe Experience Platform Mobile SDK su iOS.

## Prerequisiti {#prerequisites}

Prima di implementare l’estensione Flags, assicurati di disporre di:

* Una proprietà mobile configurata in [Raccolta dati di Adobe Experience Platform](https://experience.adobe.com/#/data-collection)
* L&#39;estensione Flags installata e configurata nella proprietà mobile
* Un ID organizzazione Adobe Experience Cloud
* Destinazione minima di distribuzione: iOS 12.0

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
1. Segui il [processo di pubblicazione](https://experienceleague.adobe.com/it/docs/experience-platform/tags/publish/overview) per aggiornare la configurazione.

### Ottieni l’ID del file di ambiente {#environment-file-id}

1. Nella tua proprietà mobile, passa a **Ambienti**.
1. Seleziona l&#39;icona della casella nella colonna **Installa** dell&#39;ambiente.
1. Nella finestra di dialogo **Istruzioni di installazione per dispositivi mobili**, copia **ID file ambiente**.

## Aggiungere l’estensione Flags all’app {#add-to-app}

### Aggiungi dipendenze {#add-dependencies}

Aggiungi le dipendenze di Mobile SDK al progetto. L&#39;estensione Flags richiede Mobile Core e le estensioni relative ad Edge elencate di seguito.

#### Utilizzo di Gestione pacchetti Swift {#swift-package-manager}

In Xcode, seleziona **File** > **Aggiungi pacchetti** e aggiungi i seguenti URL del pacchetto Adobe Experience Platform Mobile SDK:

| Pacchetto | URL |
|---|---|
| AEPCore | `https://github.com/adobe/aepsdk-core-ios.git` |
| AEPdge | `https://github.com/adobe/aepsdk-edge-ios.git` |
| AEPEdgeIdentity | `https://github.com/adobe/aepsdk-edgeidentity-ios.git` |

Quando richiesto, seleziona le seguenti librerie da aggiungere alla destinazione:

* `AEPCore`, `AEPLifecycle` (da `aepsdk-core-ios`)
* `AEPEdge` (da `aepsdk-edge-ios`)
* `AEPEdgeIdentity` (da `aepsdk-edgeidentity-ios`)

Utilizzare AEPCore 5.8.0 o versione successiva.

>[!NOTE]
>
>Quando aggiungi un pacchetto in Xcode, scegli una regola di dipendenza per ciascun pacchetto (ad esempio **Fino alla successiva versione principale**), che seleziona automaticamente le nuove versioni secondarie e di patch escludendo la successiva versione principale. Per le ultime versioni rilasciate, controlla la pagina delle versioni di ogni estensione su GitHub.

### Aggiungere il pacchetto Flag {#add-flags-package}

Utilizza il pacchetto Swift o il metodo di integrazione XCFramework per un’app target, non entrambi.

#### Per un progetto Xcode senza un file Package.swift {#xcode-project}

1. In Xcode, selezionare **File** > **Aggiungi pacchetti**.
1. Selezionare **Aggiungi locale**.
1. Selezionare la directory `Packages/AEPFlags` fornita contenente `Package.swift`.
1. Aggiungi la libreria `AEPFlags` alla destinazione dell&#39;applicazione.

Xcode memorizza il riferimento al pacchetto locale nel progetto, pertanto l&#39;applicazione non necessita del proprio file `Package.swift`.

#### Per un progetto con un file Package.swift {#package-swift-project}

Nel manifesto esistente, aggiungi `AEPFlags` alle dipendenze della destinazione dell&#39;applicazione e aggiungi la destinazione binaria utilizzando l&#39;URL e il checksum dal manifesto fornito:

```swift
targets: [
    .target(
        name: "YourApp",
        dependencies: [
            "AEPFlags"
        ]
    ),
    .binaryTarget(
        name: "AEPFlags",
        url: "<AEPFlags binary URL>",
        checksum: "<AEPFlags binary checksum>"
    )
]
```

Swift Package Manager risolve la destinazione binaria per le build Xcode, CI e di archivio locali.

#### Aggiungere direttamente XCFramework {#xcframework}

In alternativa, trascina `AEPFlags.xcframework` fornito nel Navigatore progetti Xcode e aggiungilo alla destinazione dell&#39;applicazione. In **Generale** > **Framework, Librerie e Contenuto incorporato**, impostare il framework su **Incorpora e firma**.

### Inizializzare SDK {#initialize-sdk}

Registra le estensioni Mobile SDK in `AppDelegate` prima di richiamare le API dei flag. Registra `Flag` dopo Identity, Edge e Lifecycle, quindi configura SDK utilizzando l&#39;ID file di ambiente dalla proprietà mobile.

#### Registrare e configurare le estensioni {#register-configure}

>[!IMPORTANT]
>
>Per le app di produzione, utilizza solo il livello di registro `.error`; non utilizzare `.debug` o `.trace` nelle build delle versioni.

**Swift**

```swift
// AppDelegate.swift
import AEPCore
import AEPLifecycle
import AEPEdge
import AEPEdgeIdentity
import AEPFlags
import UIKit

final class AppDelegate: NSObject, UIApplicationDelegate {

    func application(_: UIApplication,
                      didFinishLaunchingWithOptions _: [UIApplication.LaunchOptionsKey: Any]? = nil) -> Bool {
        // Production: use .error only. Do not use .debug or .trace in release builds.
        MobileCore.setLogLevel(.error)

        MobileCore.registerExtensions([
            Identity.self,
            Edge.self,
            Lifecycle.self,
            Flag.self
        ]) {
            MobileCore.configureWith(appId: "YOUR_ENVIRONMENT_FILE_ID")
            MobileCore.lifecycleStart(additionalContextData: nil)
        }

        return true
    }
}
```

**Objective-C**

```objc
// AppDelegate.m
#import "AppDelegate.h"
@import AEPCore;
@import AEPLifecycle;
@import AEPEdge;
@import AEPEdgeIdentity;
@import AEPFlags;

@implementation AppDelegate

- (BOOL)application:(UIApplication *)application
    didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {

    // Production: use AEPLogLevelError only. Do not use Debug or Trace in release builds.
    [AEPMobileCore setLogLevel:AEPLogLevelError];

    [AEPMobileCore registerExtensions:@[
        AEPMobileEdgeIdentity.class,
        AEPMobileEdge.class,
        AEPMobileLifecycle.class,
        AEPMobileFlag.class
    ] completion:^{
        [AEPMobileCore configureWithAppId:@"YOUR_ENVIRONMENT_FILE_ID"];
        [AEPMobileCore lifecycleStart:nil];
    }];

    return YES;
}

@end
```

## Contesto di valutazione {#evaluation-context}

`FeatureEvaluationContext` include attributi di targeting (utilizzati per la corrispondenza della regola del flag).

| Parametro | Obbligatorio | Descrizione |
|---|---|---|
| `attributes` | No | `[String: [String]]`. Chiave è il nome dell&#39;attributo di contesto utilizzato dalle regole del flag (ad esempio `locale`, `platform`, `appVersion`, `deviceType`). Valore è l&#39;elenco dei valori degli attributi candidati per la chiave per l&#39;utente/sessione corrente (ad esempio `["en_US"]` o `["phone"]`). |

**Swift**

```swift
import AEPFlags

let attrs: [String: [String]] = [
    "locale": ["en_US"],
    "platform": ["IOS"],
    "appVersion": ["3.0.0"]
]

let ctx = FeatureEvaluationContext.builder()
    .withAttributes(attrs)
    .build()
```

**Objective-C**

```objc
@import AEPFlags;

NSDictionary<NSString *, NSArray<NSString *> *> *attrs = @{
    @"locale": @[@"en_US"],
    @"platform": @[@"IOS"],
    @"appVersion": @[@"3.0.0"]
};

AEPFeatureEvaluationContextBuilder *builder = [AEPFeatureEvaluationContext builder];
AEPFeatureEvaluationContext *ctx = [[builder withAttributes:attrs] build];
```

### Attributi di targeting di esempio {#sample-attributes}

| Attributo | Descrizione | Valori di esempio |
|---|---|---|
| `locale` | Lingua/lingua dell&#39;utente | `["en_US"]`, `["fr_FR"]` |
| `platform` | Identificatore della piattaforma | `["IOS"]` |
| `appVersion` | Versione applicazione | `["3.0.0"]` |
| `deviceType` | Tipo di dispositivo | `["phone"]`, `["tablet"]` |

### Identità personalizzata {#custom-identity}

L&#39;estensione Flags utilizza l&#39;estensione Identity for Edge Network per la risoluzione delle identità. Un flag di funzione può essere associato a un’identità personalizzata (ad esempio, un ID del sistema di gestione delle relazioni con i clienti o un ID fedeltà) in modo che le suddivisioni e le analisi delle varianti siano legate all’identità rilevante per l’applicazione.

Lo spazio dei nomi delle identità personalizzate deve essere selezionato nell’interfaccia utente Flag quando viene creato il flag di funzione. Per valutare un flag rispetto a tale identità, la stessa identità deve essere presente nell&#39;identità Edge `identityMap` sul dispositivo, utilizzando lo spazio dei nomi corrispondente. Fornirla in fase di esecuzione con l&#39;API Identity for Edge Network `updateIdentities`.

#### Aggiungere l’identità personalizzata a Identity Map {#add-identity}

Aggiungi l’identità nello stesso spazio dei nomi configurato sul flag della funzione.

**Swift**

```swift
import AEPEdgeIdentity

let identityMap = IdentityMap()
identityMap.add(item: IdentityItem(id: "1111", authenticatedState: .authenticated, primary: true),
                 withNamespace: "userCRMId") // must match the namespace configured on the feature flag
Identity.updateIdentities(with: identityMap)
```

**Objective-C**

```objc
@import AEPEdgeIdentity;

AEPIdentityItem *item = [[AEPIdentityItem alloc]
    initWithId:@"1111"
    authenticatedState:AEPAuthenticatedStateAuthenticated
    primary:YES];
AEPIdentityMap *identityMap = [[AEPIdentityMap alloc] init];
[identityMap addItem:item withNamespace:@"userCRMId"]; // must match the namespace configured on the feature flag
[AEPMobileEdgeIdentity updateIdentities:identityMap];
```

## Documentazione sulle API {#api-reference}

### isFeatureEnabled {#is-feature-enabled}

`isFeatureEnabled` restituisce se una funzione Flag è attivata o disattivata per il contesto specificato. Passa `featureKey`, un `FeatureEvaluationContext` (attributi di targeting facoltativi) e una chiusura di completamento. Vedi [Contesto di valutazione](#evaluation-context).

**Firma**

*Swift*

```swift
static func isFeatureEnabled(
    _ featureKey: String,
    evaluationContext: FeatureEvaluationContext,
    completion: @escaping (Bool) -> Void
)
```

*Objective-C*

```objc
+ (void)isFeatureEnabled:(NSString *)featureKey
       evaluationContext:(AEPFeatureEvaluationContext *)evaluationContext
               completion:(void (^)(BOOL))completion;
```

**Parametri**

| Parametro | Tipo | Descrizione |
|---|---|---|
| `featureKey` | Stringa | Chiave della funzione da valutare nei flag |
| `evaluationContext` | FeatureEvaluationContext | Includere gli attributi di targeting in base alle esigenze; utilizzare `FeatureEvaluationContext.builder().build()` per un contesto vuoto. Vedi [Contesto di valutazione](#evaluation-context). |
| `completion` | `(Bool) -> Void` | Chiamata eseguita con `true` se la funzionalità è abilitata, `false` in caso contrario. |

**Esempi**

*Swift*

```swift
import AEPFlags

Flag.isFeatureEnabled(
    "new-flag",
    evaluationContext: ctx
) { isEnabled in
    if isEnabled {
        // Feature is enabled: run the feature-specific behavior
    } else {
        // Feature is disabled: fall back to the default behavior
    }
}
```

*Objective-C*

```objc
@import AEPFlags;

[AEPMobileFlag isFeatureEnabled:@"new-flag"
              evaluationContext:ctx
                      completion:^(BOOL isEnabled) {
    if (isEnabled) {
        // Feature is enabled: run the feature-specific behavior
    } else {
        // Feature is disabled: fall back to the default behavior
    }
}];
```

### getFeature {#get-feature}

`getFeature` restituisce il payload della funzionalità valutata per il contesto specificato. Utilizza questa API quando hai bisogno di più di abilitato/disabilitato e desideri metadati o valori di funzionalità.

**Firma**

*Swift*

```swift
static func getFeature(
    _ featureKey: String,
    evaluationContext: FeatureEvaluationContext,
    completion: @escaping (FeatureEvaluationResult?) -> Void
)
```

*Objective-C*

```objc
+ (void)getFeature:(NSString *)featureKey
 evaluationContext:(AEPFeatureEvaluationContext *)evaluationContext
        completion:(void (^)(AEPFeatureEvaluationResult * _Nullable))completion;
```

**Parametri**

| Parametro | Tipo | Descrizione |
|---|---|---|
| `featureKey` | Stringa | Chiave della funzione da valutare nei flag |
| `evaluationContext` | FeatureEvaluationContext | Includere gli attributi di targeting in base alle esigenze; utilizzare `FeatureEvaluationContext.builder().build()` per un contesto vuoto. Vedi [Contesto di valutazione](#evaluation-context). |
| `completion` | `(FeatureEvaluationResult?) -> Void` | Chiamata eseguita con il payload della funzionalità valutata. `nil` quando la funzionalità non è stata trovata. |

**Risposta**

*RisultatoValutazioneFunzionalità*

| Campo | Tipo | Descrizione |
|---|---|---|
| `id` | Intero | Identificatore numerico di funzione |
| `key` | Stringa | Chiave funzione |
| `featureGroupKey` | Stringa? | Chiave gruppo di funzioni, se disponibile |
| `meta` | Stringa? | Metadati opachi delle funzioni, se disponibili |
| `analyticsParam` | AnalyticsParam? | Dettagli di Analytics per la funzione valutata |

*AnalyticsParam*

| Campo | Tipo | Descrizione |
|---|---|---|
| `featureGroupId` | Intero | Identificatore gruppo di funzioni numerico |
| `featureId` | Intero | Identificatore numerico di funzione |
| `variantId` | Stringa? | Identificatore variante |

**Esempi**

*Swift*

```swift
import AEPFlags

Flag.getFeature(
    "new-flag",
    evaluationContext: ctx
) { feature in
    guard let meta = feature?.meta, !meta.isEmpty else {
        // No metadata available: fall back to the default behavior
        return
    }
    // Feature metadata is available: use it to drive the feature behavior
}
```

*Objective-C*

```objc
@import AEPFlags;

[AEPMobileFlag getFeature:@"new-flag"
        evaluationContext:ctx
                completion:^(AEPFeatureEvaluationResult * _Nullable feature) {
    NSString *meta = feature.meta;
    if (meta.length > 0) {
        // Feature metadata is available: use it to drive the feature behavior
    } else {
        // No metadata available: fall back to the default behavior
    }
}];
```

### extensionVersion {#extension-version}

Restituisce la stringa della versione dell&#39;estensione Flags.

**Sintassi**

*Swift*

```swift
static var extensionVersion: String
```

*Objective-C*

```objc
+ (nonnull NSString *)flagExtensionVersion;
```

**Esempio**

*Swift*

```swift
let version = Flag.extensionVersion
```

*Objective-C*

```objc
NSString *version = [AEPMobileFlag flagExtensionVersion];
```

## Riepilogo API {#api-summary}

| API | Restituisce |
|---|---|
| `isFeatureEnabled(_:evaluationContext:completion:)`. `FeatureEvaluationContext` contiene attributi di targeting per le regole. Vedi [isFeatureEnabled](#is-feature-enabled). | Bool tramite chiusura di completamento |
| `getFeature(_:evaluationContext:completion:)`. Restituisce il payload della funzione valutato per il contesto specificato. Vedi [getFeature](#get-feature). | FeatureEvaluationResult? tramite chiusura |
| `extensionVersion` | Stringa |

## Vedi anche {#see-also}

* [Applicazioni mobili](../../integrate/mobile-applications.md)
* [SDK](../../integrate/sdks.md)
* [guida all’integrazione delle estensioni Android](../android/android-extension-integration-guide.md)

<!-- -->
