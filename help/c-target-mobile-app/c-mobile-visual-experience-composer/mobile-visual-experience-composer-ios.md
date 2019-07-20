---
description: Il Compositore esperienza visivo (VEC) mobile di Adobe Target consente agli sviluppatori di effettuare una configurazione unica sulle app mobili iOS e permette agli addetti al marketing di utilizzare le funzionalità del Compositore esperienza visivo su app mobile.
keywords: VEC app mobile;compositore esperienza visivo mobile;opzioni compositore esperienza mobile;configurazione;ios;apple
seo-description: Il Compositore esperienza visivo (VEC) mobile di Adobe Target consente agli sviluppatori di effettuare una configurazione unica sulle app mobili iOS e permette agli addetti al marketing di utilizzare le funzionalità del Compositore esperienza visivo su app mobile.
seo-title: 'iOS: configurare l''app mobile'
solution: Target
title: 'iOS: configurare l''app mobile'
topic: Standard
uuid: 6db4f06a-d8f4-4192-af6f-917594e721e6
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# iOS: configurare l'app mobile{#ios-set-up-the-mobile-app}

Il Compositore esperienza visivo (VEC) per app mobile di Adobe Target consente agli sviluppatori di effettuare una configurazione unica sulle app mobili Android e permette agli addetti al marketing di utilizzare le funzionalità del Compositore esperienza visivo su app mobile.

Per ulteriori informazioni sull’abilitazione dell’estensione Adobe Target VEC, consulta la sezione sul [Compositore esperienza visivo di Adobe Target](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-target-vec) nell’*SDK di Adobe Experience Platform per dispositivi mobili*.

## Includere l’SDK mobile e la libreria di Target {#sdk-library}

1. Aggiungi la libreria al progetto tramite Cocoapods [!DNL Podfile] aggiungendo il pod “`ACPTargetVEC`”.

1. Apri il progetto dell'applicazione Objective-C in XCode.

1. Vai alle impostazioni della build del progetto e imposta l’opzione “Incorpora sempre le librerie Swift standard” su Sì, se non è già impostata.

1. Nelle impostazioni della build del progetto, individua “Altri flag del linker”. Aggiungi `$(inherited)` se è già presente.

1. Per progetti solo Objective-C: crea un file Swift per creare l’intestazione di bridging. Questo configurerà l’ambiente dell’applicazione per Swift.

1. Aggiungi il gestore deeplink:

   1. Nelle impostazioni del progetto dell'applicazione, fai clic su **[!UICONTROL Informazioni]**.
   1. In **[!UICONTROL Tipi di URL]**, fai clic sul triangolo per aprirlo, quindi sul segno più per aggiungere un nuovo campo.
   1. Aggiungi le seguenti informazioni:

      * Identificatore: `com.adobe.sdktest`
      * Schemi URL: `vectester`
      * Ruolo: Editor
   1. Fai clic lontano dalle impostazioni del progetto dell'applicazione &gt; **[!UICONTROL Generale]**.
   1. Fai clic sulle impostazioni del progetto dell'applicazione &gt; **[!UICONTROL Informazioni]** per salvare le impostazioni.

      Con il tipo di URL dell'esempio, lo schema URL dell'applicazione sarà:

      ```
      vectester://com.adobe.sdktest
      ```


1. In XCode, apri il file [!DNL AppDelegate].

1. Nella parte superiore del file, aggiungi la riga seguente alla fine delle importazioni:

   `#import "ACPTargetVEC.h"`

   Se stai utilizzando Swift, aggiungi la seguente riga:

   `import ACPTargetVEC`

1. Nel file [!DNL AppDelegate], aggiungi la seguente riga a `AppDelegate::application:didFinishLaunchingWithOptions:`. Se la funzione di delegato non è definita, creala e aggiungi la seguente riga per l'applicazione Objective-C o Swift, rispettivamente:

   ```
   // CONFIGURATION LINE FOR OBJECTIVE C ONLY
   - (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
     //Other Extensions that you need
     [ACPCore configureWithAppId:@"YOUR_ADOBE_LAUNCH_APP_ID"];
     [ACPCore setLogLevel:ACPMobileLogLevelDebug];
     [ACPTarget registerExtension];
     [ACPTargetVEC registerExtension];
     [ACPCore start:^{
       [ACPCore lifecycleStart:nil];
     }];
     // Override point for customization after application launch.
     return YES;
   }
   
   // CONFIGURATION LINE FOR SWIFT ONLY: 
   func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?) -> Bool {
     //Other Extensions that you need
     ACPCore.configure(withAppId: "YOUR_ADOBE_LAUNCH_APP_ID")
     ACPCore.setLogLevel(ACPMobileLogLevel.debug)
     ACPTarget.registerExtension()
     ACPTargetVEC.registerExtension()
     [ACPCore start:^{
       [ACPCore lifecycleStart:nil];
     }];
     return true
   }
   ```

1. Aggiungi la riga seguente all’inizio di `AppDelegate:application:openURL`. Se la funzione di delegato non è definita, creala e aggiungi la seguente riga.

   ```
   // URL HANDLER LINE FOR OBJECTIVE C ONLY: 
   - (BOOL)application:(UIApplication *)application openURL:(NSURL *)url options:(NSDictionary<NSString *, id> *)options {
     [ACPCore collectLaunchInfo:@ {@"adb_deeplink": url.absoluteString}];
     return YES;
   }
   
   // URL HANDLER LINE FOR SWIFT ONLY: 
   func application(_ app: UIApplication, open url: URL, options: [UIApplicationOpenURLOptionsKey : Any] = [:]) -> Bool {
     ACPCore.collectLaunchInfo(["adb_deeplink": url.absoluteString])
     return true
   }
   ```

   Crea ed esegui l’applicazione per verificare le funzionalità del Compositore esperienza visivo su app mobile.


## Configurare le visualizzazioni di Target nell’app mobile {#views}

L’SDK Adobe Mobile espone un nuovo metodo per gli sviluppatori da attivare ogni volta che viene effettuato il rendering di una nuova visualizzazione. Leggi le linee guida generali su come inserire correttamente le chiamate API per viste Target per un’app iOS. In iOS, tutte le visualizzazioni di Target sono definite in base al `UIViewController` in cui compaiono. Pertanto, a differenza di Android, l'inserimento di `TargetViews` è limitato alle seguenti chiamate.

Il componente Adobe Mobile VEC Extension genera automaticamente dei nomi per dei `UIViewControllers` per interagire all’interno del framework del Compositore esperienza visivo per app mobile, in base al nome della classe del `UIViewController` sottoclassificato. Se desideri ignorare questi nomi, puoi chiamare il metodo seguente in `viewWillAppear` di `ViewController`.

```
// TARGET VIEW LINE FOR OBJECTIVE C ONLY 
[ACPTargetVEC setTargetView:@"exampleViewController"]; 
   
// TARGET VIEW LINE FOR SWIFT ONLY 
ACPTargetVEC.setTargetView("exampleViewController")
```

Adobe Mobile SDK espone inoltre un metodo alternativo agli sviluppatori per indirizzare le viste personalizzate durante il runtime. Come sviluppatore, devi verificare che le visualizzazioni siano denominate in modo univoco. Chiama il metodo seguente prima di aggiungere la vista a `superview`:

```
// EXAMPLE TARGET VIEW FOR A CUSTOM VIEW IN OBJECTIVE C 
CustomPopupView *popupView = [[CustomPopupView alloc] initWithFrame:CGRectMake(0, 0, 300, 200)]; 
[ACPTargetVEC setTargetView:@"myCustomPopupView" forView:popupView];

// EXAMPLE TARGET VIEW FOR A CUSTOM VIEW IN SWIFT 
let popupView = CustomPopupView.init(frame: CGRect(x: 0, y: 0, width: 300, height: 200)) 
ACPTargetVEC.setTargetView("myCustomPopupView", for: popupView)
```

## Configurazione dei parametri del profilo e di altri parametri globali {#parameters}

Sono ora supportati l’impostazione di parametri globali che vengono trasmessi in ogni chiamata API e la trasmissione di parametri mbox/di visualizzazione alle viste corrispondenti.

I parametri includono:

* parametri mbox/di visualizzazione
* parametri del profilo
* Parametri del prodotto
* Parametri dell’ordine

**Supporto globale dei parametri:**

```
//For Objective-c 
NSDictionary *mboxParams = @{@"mboxparam1":@"mboxvalue1"}; //mbox or view params 
NSDictionary *profileParams = @{@"profilekey1":@"profilevalue1"}; //profile params 
  
ACPTargetProduct *product = [ACPTargetProduct targetProductWithId:@"1234" categoryId:@"furniture"]; 
ACPTargetOrder *order = [ACPTargetOrder targetOrderWithId:@"12343" total:@(123.45) purchasedProductIds:@[@"100",@"200"]]; 
ACPTargetParameters *targetParams = [ACPTargetParameters targetParametersWithParameters: mboxParams
                      profileParameters: profileParams
                      product: product
                      order: order];
[ACPTargetVEC setGlobalRequestParameters:targetParams];

//For Swift 
var mboxParams = ["mboxparam1":"mboxvalue1"] 
var profileParams = ["profilekey1":"profilevalue1"] 
var product = ACPTargetProduct(id: "1234", categoryId: "furniture")
var order = ACPTargetOrder(id: "12345", total: 123.45, purchasedProductIds: ["100", "200"])
var targetParams = ACPTargetParameters(parameters: mboxParams, profileParameters: profileParams, product: product, order: order)
ACPTargetVEC.setGlobalRequest(targetParams)
```

**Trasferimento dei parametri per l’attivazione della vista successiva:**

Sono fornite alcune viste automatiche create per impostazione predefinita, ad esempio “`AUTO_<viewControllerName>`” per ogni controller di visualizzazione presente nell’app. Se si desidera trasferire questi parametri, è possibile chiamare la seguente API:

```
//For Objective-c 
NSDictionary *mboxParams = @{@"viewparam1":@"viewvalue1"}; //mbox or view params 
NSDictionary *profileParams = @{@"profilekeyforview1":@"profilevalueforview1"}; //profile params 
  
ACPTargetProduct *product = [ACPTargetProduct targetProductWithId:@"1234" categoryId:@"furniture"]; 
ACPTargetOrder *order = [ACPTargetOrder targetOrderWithId:@"12343" total:@(123.45) purchasedProductIds:@[@"100",@"200"]]; 
ACPTargetParameters *targetParams = [ACPTargetParameters targetParametersWithParameters:mboxParams 
                                                                      profileParameters:profileParams 
                                                                                product:product 
                                                                                  order:order]; 
[ACPTargetVEC setGlobalRequestParameters:targetParams];

//For Swift 
var mboxParams = ["mboxparam1":"mboxvalue1"] 
var profileParams = ["profilekey1":"profilevalue1"] 
var product = ACPTargetProduct(id: "1234", categoryId: "furniture")
var order = ACPTargetOrder(id: "12345", total: 123.45, purchasedProductIds: ["100", "200"])
var targetParams = ACPTargetParameters(parameters: mboxParams, profileParameters: profileParams, product: product, order: order)
ACPTargetVEC.setRequest(targetParams)
```

**Trasferimento dei parametri a una visualizzazione specifica:**

Abbiamo visto l’API attivare le Viste tramite `TargetVEC.targetView("view_name")`. È inoltre possibile trasferire parametri specifici a una particolare visualizzazione, come illustrato di seguito:

```
//For Objective-c 
[ACPTargetVEC setTargetView:@"VIEW_NAME" withParameters:TARGET_PARAMS];

//FOR SWIFT 
ACPTargetVEC.setTargetView("VIEW_NAME", with: TARGET_PARAMS)
```

## Chiamare esplicitamente l’API di preacquisizione {#section_373DB4527FC649C58FBA3DF0C18C9836}

Potrebbero esserci alcuni scenari in cui si potrebbe voler chiamare nuovamente l'API di preacquisizione per aggiornare le offerte archiviate nella cache. Vengono esposte le seguenti API, descritte come:

**Preacquisire offerte:**

```
/** 
 * Prefetch all offers for all views in the cache. It will remove existing offers and changes for the current view will be 
 refreshed only when the view is triggered. This call happens on the main thread blocking the UI. 
 */ 
+ (void) prefetchOffers;
```

**Preacquisire offerte in background:**

```
/** 
 * Prefetch all offers for all views in the cache. It will remove existing offers and changes for the current view will be 
 refreshed only when the view is triggered. This call happens on the background thread so doesn't block UI. 
 */ 
+ (void) prefetchOffersBackground;
```

## Tutorials: Implement the Experience Cloud in Mobile iOS Objective-C and Swift applications {#tutorial}

* [Implementazione di Experience Cloud nelle applicazioni Objective-C di iOS](https://docs.adobe.com/content/help/en/experience-cloud/implementing-in-mobile-ios-objective-c-apps-with-launch/index.html)
* [Implementazione di Experience Cloud nelle applicazioni Ios Swift per dispositivi mobili](https://docs.adobe.com/content/help/en/experience-cloud/implementing-in-mobile-ios-swift-apps-with-launch/index.html)

Al termine di queste esercitazioni, potrete:

* Creare una proprietà di avvio mobile
* Installare una proprietà Launch in un'app Objective-C o Swift
* Implementa le seguenti soluzioni Adobe Experience Cloud:
   * Servizio Experience Cloud ID
   * Adobe Target
   * Adobe Analytics
   * Adobe Audience Manager

* Pubblicare le modifiche in Launch tramite ambienti di sviluppo, staging e produzione