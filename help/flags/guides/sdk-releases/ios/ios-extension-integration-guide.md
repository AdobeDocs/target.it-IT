---
title: Guida all’integrazione di Flag per l’estensione iOS
description: Scopri come integrare l’estensione Flags con Adobe Experience Platform Mobile SDK su iOS.
badge: label="Beta" type="Informative"
hide: true
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
source-git-commit: c1fafcfcd7d5d22781abdd10e6eb3c2b84136c2d
workflow-type: tm+mt
source-wordcount: '1313'
ht-degree: 3%
---
# Estensione flag per iOS {#ios-extension-integration-guide}

Questa guida descrive come integrare l’estensione Flags con Adobe Experience Platform Mobile SDK su iOS. Il codice sorgente è disponibile nell&#39;archivio [aepsdk-flags-ios](https://github.com/adobe/aepsdk-flags-ios).

## Prerequisiti {#prerequisites}

Prima di iniziare, assicurati di avere:

* iOS 12.0 o versione successiva e Swift 5.7 o versione successiva
* Una proprietà mobile in [Raccolta dati Adobe Experience Platform](https://experience.adobe.com/#/data-collection)
* Queste estensioni sono installate e configurate nella proprietà mobile:

  | Estensione | Descrizione | Versione minima SDK |
  |---|---|---|
  | [Core mobile](https://developer.adobe.com/client-sdks/home/base/mobile-core/) | Configurazione ed elaborazione degli eventi | AEPCore 5.8.0 |
  | [Ciclo di vita](https://developer.adobe.com/client-sdks/home/base/mobile-core/lifecycle/) | Dati del ciclo di vita dell&#39;applicazione | Come AEPCore |
  | [Edge Network](https://developer.adobe.com/client-sdks/edge/edge-network/) | Comunicazione con Adobe Experience Platform Edge Network. Richiede un flusso di dati. | AEPEdge 5.0.2 |
  | [Identità per Edge Network](https://developer.adobe.com/client-sdks/edge/identity-for-edge-network/) | Gestione delle identità per Edge Network | AEPEdgeIdentity 5.0.0 |
  | [Contrassegni](https://experienceleague.adobe.com/en/docs/target/flags/home) | Valutazione flag di funzione | Vedi [Installazione](#installation) |

## Configurare i flag nella raccolta dati {#configure}

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

## Installazione {#installation}

Aggiungi l’estensione con Swift Package Manager o XCFramework. Utilizza un metodo per ogni destinazione dell’app.

### Gestione pacchetti Swift {#swift-package-manager}

In Xcode:

1. Selezionare **File** > **Aggiungi dipendenze pacchetto**.

1. Immettere l&#39;URL del pacchetto: `https://github.com/adobe/aepsdk-flags-ios.git`

1. Per la regola di versione, selezionare **Versione esatta** e immettere la versione più recente dalla [pagina delle versioni](https://github.com/adobe/aepsdk-flags-ios/releases).

1. Aggiungi la libreria `AEPFlags` alla destinazione dell&#39;app.

1. Aggiungi i pacchetti Adobe da cui dipende l’estensione e le relative librerie alla destinazione dell’app:

   * `https://github.com/adobe/aepsdk-core-ios.git`: `AEPCore`, `AEPLifecycle` e `AEPServices`
   * `https://github.com/adobe/aepsdk-edge-ios.git`: `AEPEdge`
   * `https://github.com/adobe/aepsdk-edgeidentity-ios.git`: `AEPEdgeIdentity`

Se il progetto utilizza un file `Package.swift`, aggiungere le dipendenze. Sostituisci `<latest-version>` con la versione più recente dalla pagina delle versioni.

```swift
dependencies: [
    .package(url: "https://github.com/adobe/aepsdk-flags-ios.git", exact: "<latest-version>"),
    .package(url: "https://github.com/adobe/aepsdk-core-ios.git", .upToNextMajor(from: "5.8.0")),
    .package(url: "https://github.com/adobe/aepsdk-edge-ios.git", .upToNextMajor(from: "5.0.2")),
    .package(url: "https://github.com/adobe/aepsdk-edgeidentity-ios.git", .upToNextMajor(from: "5.0.0"))
],
targets: [
    .target(
        name: "YourTarget",
        dependencies: [
            .product(name: "AEPFlags", package: "aepsdk-flags-ios"),
            .product(name: "AEPCore", package: "aepsdk-core-ios"),
            .product(name: "AEPLifecycle", package: "aepsdk-core-ios"),
            .product(name: "AEPServices", package: "aepsdk-core-ios"),
            .product(name: "AEPEdge", package: "aepsdk-edge-ios"),
            .product(name: "AEPEdgeIdentity", package: "aepsdk-edgeidentity-ios")
        ]
    )
]
```

### XCFramework {#xcframework}

1. Dalla pagina delle [versioni](https://github.com/adobe/aepsdk-flags-ios/releases), scarica `AEPFlags-<version>.xcframework.zip` e decomprimi.

1. Scarica XCFrameworks da cui dipende l’estensione dalla pagina delle versioni di ciascun archivio:

   * [versioni aepsdk-core-ios](https://github.com/adobe/aepsdk-core-ios/releases): `AEPCore`, `AEPServices`, `AEPLifecycle` e `AEPRulesEngine`
   * [versioni aepsdk-edge-ios](https://github.com/adobe/aepsdk-edge-ios/releases): `AEPEdge`
   * [versioni aepsdk-edgeidentity-ios](https://github.com/adobe/aepsdk-edgeidentity-ios/releases): `AEPEdgeIdentity`

1. In Xcode, seleziona la destinazione dell&#39;app, quindi apri **Generale** > **Framework, Librerie e Contenuto incorporato**.

1. Aggiungere `AEPFlags.xcframework` e tutti i XCFrameworks dipendenti.

1. Imposta ogni framework su **Incorpora e firma**.

## Inizializzare SDK {#initialize-sdk}

Registra l&#39;estensione Flags, quindi inizializza SDK con l&#39;ID file di ambiente dalla proprietà mobile. `MobileCore.initialize` non registra l&#39;estensione Flags per te, quindi registrala prima.

>[!BEGINTABS]

>[!TAB Swift]

```swift
import AEPCore
import AEPFlags
import UIKit

class AppDelegate: UIResponder, UIApplicationDelegate {
    func application(
        _ application: UIApplication,
        didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?
    ) -> Bool {
        MobileCore.registerExtensions([Flag.self])
        MobileCore.initialize(appId: "<your-environment-file-id>")
        return true
    }
}
```

>[!TAB Objective-C]

```objc
@import AEPCore;
@import AEPFlags;

- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
    [AEPMobileCore registerExtensions:@[AEPMobileFlag.class] completion:nil];
    [AEPMobileCore initializeWithAppId:@"<your-environment-file-id>" completion:nil];
    return YES;
}
```

>[!ENDTABS]

### Registrare manualmente le estensioni {#register-manually}

Se registri tu stesso le estensioni, registrale tutte. Chiamare `MobileCore.lifecycleStart` quando l&#39;app entra in primo piano e `MobileCore.lifecyclePause` quando entra in background.

Se l&#39;app utilizza scene, effettua queste chiamate in `sceneWillEnterForeground(_:)` e `sceneDidEnterBackground(_:)`.

>[!BEGINTABS]

>[!TAB Swift]

```swift
import AEPCore
import AEPEdge
import AEPEdgeIdentity
import AEPFlags
import AEPLifecycle
import UIKit

class AppDelegate: UIResponder, UIApplicationDelegate {
    func application(
        _ application: UIApplication,
        didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?
    ) -> Bool {
        MobileCore.registerExtensions([
            Lifecycle.self,
            Edge.self,
            AEPEdgeIdentity.Identity.self,
            Flag.self
        ]) {
            MobileCore.configureWith(appId: "<your-environment-file-id>")
            DispatchQueue.main.async {
                if application.applicationState != .background {
                    MobileCore.lifecycleStart(additionalContextData: nil)
                }
            }
        }
        return true
    }

    func applicationWillEnterForeground(_ application: UIApplication) {
        MobileCore.lifecycleStart(additionalContextData: nil)
    }

    func applicationDidEnterBackground(_ application: UIApplication) {
        MobileCore.lifecyclePause()
    }
}
```

>[!TAB Objective-C]

```objc
@import AEPCore;
@import AEPEdge;
@import AEPEdgeIdentity;
@import AEPFlags;
@import AEPLifecycle;

- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
    [AEPMobileCore registerExtensions:@[
        AEPMobileLifecycle.class,
        AEPMobileEdge.class,
        AEPMobileEdgeIdentity.class,
        AEPMobileFlag.class
    ] completion:^{
        [AEPMobileCore configureWithAppId:@"<your-environment-file-id>"];
        dispatch_async(dispatch_get_main_queue(), ^{
            if (application.applicationState != UIApplicationStateBackground) {
                [AEPMobileCore lifecycleStart:nil];
            }
        });
    }];
    return YES;
}

- (void)applicationWillEnterForeground:(UIApplication *)application {
    [AEPMobileCore lifecycleStart:nil];
}

- (void)applicationDidEnterBackground:(UIApplication *)application {
    [AEPMobileCore lifecyclePause];
}
```

>[!ENDTABS]

## Contesto di valutazione {#evaluation-context}

Ogni chiamata di valutazione richiede un `FeatureEvaluationContext`. Contiene gli attributi utilizzati dalle regole di targeting dei flag.

| Parametro | Obbligatorio | Descrizione |
|---|---|---|
| `attributes` | No | `[String: [String]]`. Ogni chiave è un nome di attributo utilizzato dalle regole di targeting dei flag. Ogni valore rappresenta l&#39;elenco di valori per l&#39;utente corrente. |

* Utilizza nomi e valori di attributi che corrispondono alle regole di targeting definite in Flag.
* Chiamare `withAttributes` al massimo una volta per ogni generatore. Una seconda chiamata termina l’app.
* Per valutare senza attributi, chiamare `build()` senza chiamare `withAttributes`.

>[!BEGINTABS]

>[!TAB Swift]

```swift
import AEPFlags

let context = FeatureEvaluationContext.builder()
    .withAttributes([
        "locale": ["en_US"],
        "appVersion": ["3.0.0"]
    ])
    .build()
```

>[!TAB Objective-C]

```objc
@import AEPFlags;

AEPFeatureEvaluationContext *context = [[[AEPFeatureEvaluationContext builder]
    withAttributes:@{
        @"locale": @[@"en_US"],
        @"appVersion": @[@"3.0.0"]
    }]
    build];
```

>[!ENDTABS]

## Identità personalizzata {#custom-identity}

L&#39;estensione Flags utilizza l&#39;estensione Identity for Edge Network per la risoluzione delle identità. Un flag di funzione può essere associato a un’identità personalizzata (ad esempio, un ID del sistema di gestione delle relazioni con i clienti o un ID fedeltà) in modo che le suddivisioni e le analisi delle varianti siano legate all’identità rilevante per l’applicazione.

Lo spazio dei nomi delle identità personalizzate deve essere selezionato nell’interfaccia utente Flag quando viene creato il flag di funzione. Per valutare un flag rispetto a tale identità, la stessa identità deve essere presente nell&#39;identità Edge `identityMap` sul dispositivo, utilizzando lo spazio dei nomi corrispondente. Fornirla in fase di esecuzione con l&#39;API Identity for Edge Network `updateIdentities`.

### Aggiungere l’identità personalizzata a Identity Map {#add-identity}

Aggiungi l’identità nello stesso spazio dei nomi configurato sul flag della funzione.

Osserva il seguente comportamento:

* Lo spazio dei nomi deve corrispondere esattamente a quello configurato sul flag, comprese le lettere maiuscole e minuscole.
* Se lo spazio dei nomi contiene più identità, viene utilizzato quello contrassegnato come primario. Se nessuno è contrassegnato come primario, viene utilizzato il primo.
* Se manca l’identità, la chiamata non avrà esito negativo. L’utente viene assegnato a una variante a caso solo per la sessione dell’app corrente e può essere assegnato a una variante diversa dopo il riavvio dell’app. Impostare l&#39;identità prima di valutare i flag che la utilizzano.

>[!BEGINTABS]

>[!TAB Swift]

```swift
import AEPEdgeIdentity

let identityMap = IdentityMap()
identityMap.add(
    item: IdentityItem(id: "1111", authenticatedState: .authenticated, primary: true),
    withNamespace: "userCRMId" // must match the namespace configured on the feature flag
)
Identity.updateIdentities(with: identityMap)
```

>[!TAB Objective-C]

```objc
@import AEPEdgeIdentity;

AEPIdentityItem *item = [[AEPIdentityItem alloc] initWithId:@"1111"
                                         authenticatedState:AEPAuthenticatedStateAuthenticated
                                                    primary:YES];
AEPIdentityMap *identityMap = [[AEPIdentityMap alloc] init];
[identityMap addItem:item withNamespace:@"userCRMId"]; // must match the namespace configured on the feature flag
[AEPMobileEdgeIdentity updateIdentities:identityMap];
```

>[!ENDTABS]


## Documentazione sulle API {#api-reference}

### isFeatureEnabled {#is-feature-enabled}

Controlla se una funzione è abilitata per l’utente corrente. Il risultato è `true` quando la funzionalità esiste, l&#39;utente corrisponde alle relative regole di targeting e l&#39;utente non fa parte di un gruppo di controllo. In caso contrario, il risultato è `false`.

>[!BEGINTABS]

>[!TAB Swift]

```swift
static func isFeatureEnabled(
    _ featureKey: String,
    evaluationContext: FeatureEvaluationContext,
    completion: @escaping (Bool) -> Void,
    errorCallback: ((AEPError) -> Void)?
)
```

>[!TAB Objective-C]

```objc
+ (void)isFeatureEnabled:(NSString *)featureKey
       evaluationContext:(AEPFeatureEvaluationContext *)evaluationContext
              completion:(void (^)(BOOL))completion
           errorCallback:(void (^ _Nullable)(enum AEPError))errorCallback;
```

>[!ENDTABS]

**Parametri**

| Parametro | Tipo | Descrizione |
|---|---|---|
| `featureKey` | Stringa | Chiave della funzione da valutare nei flag |
| `evaluationContext` | FeatureEvaluationContext | Includere gli attributi di targeting in base alle esigenze; utilizzare `FeatureEvaluationContext.builder().build()` per un contesto vuoto. Vedi [Contesto di valutazione](#evaluation-context). |
| `completion` | `(Bool) -> Void` | Chiamata eseguita con `true` se la funzionalità è abilitata, `false` in caso contrario. |
| `errorCallback` | `((AEPError) -> Void)?` | Facoltativo. Chiamata eseguita solo per errori reali, ad esempio una chiave vuota, una configurazione mancante, una valutazione non riuscita o un timeout. |

**Esempi**

>[!BEGINTABS]

>[!TAB Swift]

```swift
Flag.isFeatureEnabled("new-flag", evaluationContext: context) { isEnabled in
    DispatchQueue.main.async {
        if isEnabled {
            // Run the feature-specific behavior
        } else {
            // Run the default behavior
        }
    }
} errorCallback: { _ in
    DispatchQueue.main.async {
        // Run the default behavior
    }
}
```

>[!TAB Objective-C]

```objc
[AEPMobileFlag isFeatureEnabled:@"new-flag"
              evaluationContext:context
                     completion:^(BOOL isEnabled) {
    dispatch_async(dispatch_get_main_queue(), ^{
        if (isEnabled) {
            // Run the feature-specific behavior
        } else {
            // Run the default behavior
        }
    });
} errorCallback:^(enum AEPError error) {
    dispatch_async(dispatch_get_main_queue(), ^{
        // Run the default behavior
    });
}];
```

>[!ENDTABS]

### getFeature {#get-feature}

>[!IMPORTANT]
>
>Nelle versioni precedenti è stato chiamato il callback di errore con `AEPError.unexpected` quando non è stata fornita una funzionalità. Se l&#39;app ha trattato l&#39;errore come &quot;funzionalità mancante&quot;, al suo posto gestisci `nil` nel completamento.

Restituisce i dettagli di una funzione per l’utente corrente, inclusi i metadati e la variante a cui l’utente è assegnato. Utilizzalo quando ne hai bisogno più di abilitato o disabilitato.

Il completamento viene chiamato con un risultato solo quando la funzione viene fornita all&#39;utente. Se la funzionalità non viene fornita, il completamento viene chiamato con `nil`. Si tratta di un risultato normale, non di un errore, e il callback di errore non viene chiamato. Il completamento viene chiamato con `nil` quando:

* Nessuna funzione dispone di questa chiave.
* L’utente non corrisponde alle regole di targeting.
* L&#39;utente fa parte di un gruppo di controllo.

Il callback di errore viene chiamato con `AEPError.unexpected` (o un altro `AEPError`) solo quando si verifica un errore: la chiave della funzionalità è vuota, manca un valore di configurazione obbligatorio, la valutazione non riesce, la risposta non può essere letta o la richiesta scade.

>[!BEGINTABS]

>[!TAB Swift]

```swift
static func getFeature(
    _ featureKey: String,
    evaluationContext: FeatureEvaluationContext,
    completion: @escaping (FeatureEvaluationResult?) -> Void,
    errorCallback: ((AEPError) -> Void)?
)
```

>[!TAB Objective-C]

```objc
+ (void)getFeature:(NSString *)featureKey
 evaluationContext:(AEPFeatureEvaluationContext *)evaluationContext
        completion:(void (^)(AEPFeatureEvaluationResult * _Nullable))completion
     errorCallback:(void (^ _Nullable)(enum AEPError))errorCallback;
```

>[!ENDTABS]

**Parametri**

| Parametro | Tipo | Descrizione |
|---|---|---|
| `featureKey` | Stringa | Chiave della funzione da valutare nei flag |
| `evaluationContext` | FeatureEvaluationContext | Includere gli attributi di targeting in base alle esigenze; utilizzare `FeatureEvaluationContext.builder().build()` per un contesto vuoto. Vedi [Contesto di valutazione](#evaluation-context). |
| `completion` | `(FeatureEvaluationResult?) -> Void` | Chiamata eseguita con il payload della funzione valutata. Chiamata eseguita con `nil` quando la funzionalità non viene fornita all&#39;utente (chiave sconosciuta, targeting non corrispondente o gruppo di controllo). `nil` non è un errore. |
| `errorCallback` | `((AEPError) -> Void)?` | Facoltativo. Chiamata eseguita solo per errori reali, ad esempio una chiave vuota, una configurazione mancante, una valutazione non riuscita o un timeout. Non viene chiamato quando la funzione non viene fornita. |

**Risposta**

*RisultatoValutazioneFunzionalità*

| Campo | Tipo | Descrizione |
|---|---|---|
| `id` | Intero | ID della funzione |
| `key` | Stringa | La chiave della funzione |
| `featureGroupKey` | Stringa? | Chiave del gruppo di feature che contiene la feature |
| `meta` | Stringa? | I metadati configurati per la funzione, come testo. Se i metadati sono JSON, decodificali nell’app. |
| `analyticsParam` | AnalyticsParam? | Identificatori della funzione e della variante dell’utente |

**Esempi**

>[!BEGINTABS]

>[!TAB Swift]

```swift
Flag.getFeature("new-flag", evaluationContext: context) { feature in
    DispatchQueue.main.async {
        guard let meta = feature?.meta, !meta.isEmpty else {
            // The feature is not served to this user (feature is nil), or it has no metadata.
            // Run the default behavior
            return
        }
        // Use the metadata to drive the feature behavior
    }
} errorCallback: { _ in
    DispatchQueue.main.async {
        // A genuine failure occurred. Run the default behavior
    }
}
```

>[!TAB Objective-C]

```objc
[AEPMobileFlag getFeature:@"new-flag"
        evaluationContext:context
               completion:^(AEPFeatureEvaluationResult * _Nullable feature) {
    dispatch_async(dispatch_get_main_queue(), ^{
        if (feature.meta.length > 0) {
            // Use the metadata to drive the feature behavior
        } else {
            // Run the default behavior
        }
    });
} errorCallback:^(enum AEPError error) {
    dispatch_async(dispatch_get_main_queue(), ^{
        // Run the default behavior
    });
}];
```

>[!ENDTABS]

### extensionVersion {#extension-version}

Restituisce la versione dell&#39;estensione Flags.

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
| `isFeatureEnabled(_:evaluationContext:completion:errorCallback:)` | Booleano fino al completamento |
| `getFeature(_:evaluationContext:completion:errorCallback:)` | FeatureEvaluationResult? fino al completamento |
| `extensionVersion` | Stringa |
