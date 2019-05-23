---
description: Adobe Target Mobile Visual Experience Composer (VEC) consente agli sviluppatori di effettuare una configurazione una tantum sulle app mobili iOS e consente agli esperti di marketing di utilizzare le funzionalità della VEC App mobile.
keywords: App Mobile VEC; mobile visual experience composer; opzioni Experience Experience Composer (Compositore esperienza mobili); configurazione; ios; apple
seo-description: Adobe Target Mobile Visual Experience Composer (VEC) consente agli sviluppatori di effettuare una configurazione una tantum sulle app mobili iOS e consente agli esperti di marketing di utilizzare le funzionalità della VEC App mobile.
seo-title: 'iOS: configurare l''app mobile'
solution: Target
title: 'iOS: configurare l''app mobile'
topic: Standard
uuid: 6db4f06a-d8f4-4192-af6f-917594e721e6
translation-type: tm+mt
source-git-commit: 29e82d6bcb42b0f05b0b175be7df017184358c38

---


# iOS: configurare l&#39;app mobile{#ios-set-up-the-mobile-app}

Adobe Target Mobile App Visual Composer (VEC) consente agli sviluppatori di effettuare una configurazione una tantum sulle app mobili iOS e consente agli esperti di marketing di utilizzare le funzionalità della VEC App mobile.

Per ulteriori informazioni sull&#39;abilitazione dell&#39;estensione VEC Adobe Target, vedi [Adobe Target - Visual Experience Composer](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-target-vec) (Compositore esperienza visivo) negli SDK per dispositivi mobili *Adobe Experience Platform*.

## Includere l&#39;SDK di Mobile e la libreria Target {#sdk-library}

1. Aggiungete la libreria al progetto tramite i cocoapods [!DNL Podfile] aggiungendo un contenitore`ACPTargetVEC`.
1. Apri il progetto dell&#39;applicazione Objective-C in XCode.
1. Andate alle impostazioni della build del progetto e impostate «Incorpora sempre le librerie standard» su Sì se non è già impostata.
1. Nelle impostazioni della build del progetto, individua “Altri flag del linker”. Aggiungi `$(inherited)` se è già presente.
1. Per progetti solo Objective-C: crea un file Swift per creare l’intestazione di bridging. Questo configurerà l’ambiente dell’applicazione per Swift.
1. Aggiungi il gestore deeplink:

   1. Nelle impostazioni del progetto dell&#39;applicazione, fai clic su **[!UICONTROL Informazioni]**.
   1. In Tipi **[!UICONTROL URL]**, fate clic sul triangolo per aprirlo, quindi fate clic sul segno più per aggiungere un nuovo campo.
   1. Aggiungi le seguenti informazioni:

      * Identificatore: `com.adobe.sdktest`
      * Schemi URL: `vectester`
      * Ruolo: Editor
   1. Fai clic lontano dalle impostazioni del progetto dell&#39;applicazione &gt; **[!UICONTROL Generale]**.
   1. Fai clic sulle impostazioni del progetto dell&#39;applicazione &gt; **[!UICONTROL Informazioni]** per salvare le impostazioni.

      Con il tipo di URL dell&#39;esempio, lo schema URL dell&#39;applicazione sarà:

      ```
      vectester://com.adobe.sdktest
      ```


1. In XCode, apri il file [!DNL AppDelegate].
1. Nella parte superiore del file, aggiungi la riga seguente alla fine delle importazioni:

   `#import "ACPTargetVEC.h"`

   Se stai utilizzando Swift, aggiungi la seguente riga:

   `import ACPTargetVEC`

1. Nel file [!DNL AppDelegate], aggiungi la seguente riga a `AppDelegate::application:didFinishLaunchingWithOptions:`. Se la funzione di delegato non è definita, creala e aggiungi la seguente riga per l&#39;applicazione Objective-C o Swift, rispettivamente:

   ```
   // CONFIGURATION LINE FOR OBJECTIVE C ONLY (Skip any framework which is not applicable for you): 
   [ACPCore configureWithAppId:@"YOUR_ADOBE_LAUNCH_APP_ID"]; 
   [ACPCore setLogLevel:ACPMobileLogLevelDebug]; 
   [ACPLifecycle registerExtension]; 
   [ACPIdentity registerExtension]; 
   [ACPUserProfile registerExtension]; 
   [ACPTarget registerExtension];
   
   [ACPTargetVEC registerExtension];
   [ACPCore start:^{
        [ACPCore lifecycleStart:nil];
   }];
   
   // CONFIGURATION LINE FOR SWIFT ONLY: 
   ACPCore.configure(withAppId: "YOUR_ADOBE_LAUNCH_APP_ID") 
   ACPCore.setLogLevel(ACPMobileLogLevel.debug) 
   ACPLifecycle.registerExtension() 
   ACPIdentity.registerExtension() 
   ACPUserProfile.registerExtension() 
   ACPTarget.registerExtension() 
   
   ACPTargetVEC.registerExtension() 
   
   ACPCore.start {
     ACPCore.lifecycleStart(nil)
   }
   ```

   Ad esempio, il metodo dovrebbe essere simile al seguente:

   ```
   // EXAMPLE OVERRIDE METHOD FOR OBJECTIVE C ONLY: 
   - (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions { 
        // Override point for customization after application launch. 
       [ACPCore configureWithAppId:@"YOUR_ADOBE_LAUNCH_APP_ID"]; 
       [ACPCore setLogLevel:ACPMobileLogLevelDebug]; 
       [ACPLifecycle registerExtension]; 
       [ACPIdentity registerExtension]; 
       [ACPUserProfile registerExtension]; 
       [ACPTarget registerExtension]; 
   
       [ACPTargetVEC registerExtension]; 
   
       [ACPCore start:nil]; 
       [ACPCore lifecycleStart:nil]; 
   
      return YES; 
   } 
   
   // EXAMPLE OVERRIDE METHOD FOR SWIFT ONLY: 
   func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey : Any]? = nil) 
   { 
       ACPCore.configure(withAppId: "YOUR_ADOBE_LAUNCH_APP_ID") 
       ACPCore.setLogLevel(ACPMobileLogLevel.debug) 
       ACPLifecycle.registerExtension() 
       ACPIdentity.registerExtension() 
       ACPUserProfile.registerExtension() 
       ACPTarget.registerExtension() 
   
       ACPTargetVEC.registerExtension() 
   
       ACPCore.start(nil) 
       ACPCore.lifecycleStart(nil)
   
       return true 
   
   }
   ```

1. Aggiungi la riga seguente all’inizio di `AppDelegate:application:openURL`. Se la funzione di delegato non è definita, creala e aggiungi la seguente riga.

   ```
   // URL HANDLER LINE FOR OBJECTIVE C ONLY: 
   [ACPTargetVEC handleDeepLink:url];
   
   // URL HANDLER LINE FOR SWIFT ONLY: 
   ACPTargetVEC.handleDeepLink(url)
   ```

   Ad esempio, il metodo dovrebbe essere simile al seguente:

   ```
   // EXAMPLE OVERRIDE METHOD FOR OBJECTIVE C ONLY:
   -  (BOOL)application:(UIApplication *)application openURL:(NSURL *)url options:(NSDictionary<NSString *, id> *)options {
    [ACPTargetVEC handleDeepLink:url];
    return YES;
   }
   
   // EXAMPLE OVERRIDE METHOD FOR SWIFT ONLY:
   func application(_ app: UIApplication, open url: URL, options: [UIApplication.OpenURLOptionsKey : Any] = [:]) -> Bool {
      ACPTargetVEC.handleDeepLink(url)
      return true;
   }
   ```

1. Crea ed esegui l&#39;applicazione e utilizzala per testare le funzionalità VEC App mobile.

## Configurare le visualizzazioni Target nell&#39;app mobile {#views}

L’SDK Adobe Mobile espone un nuovo metodo per gli sviluppatori da attivare ogni volta che viene effettuato il rendering di una nuova visualizzazione. Leggi le linee guida generali su come inserire correttamente le chiamate API di Target per un&#39;app iOS. In iOS, tutte le visualizzazioni di Target sono definite in base al `UIViewController` in cui compaiono. Pertanto, a differenza di Android, l&#39;inserimento di `TargetViews` è limitato alle seguenti chiamate.

L&#39;app Adobe Mobile App VEC Extension genera automaticamente i nomi per `UIViewControllers` l&#39;interazione all&#39;interno della framework Mobile App VEC, in base al nome classe delle sottoclassi `UIViewController`. Se desiderate sovrascrivere questi nomi, potete richiamare il seguente metodo in `viewWillAppear``ViewController`.

```
// TARGET VIEW LINE FOR OBJECTIVE C ONLY 
[ACPTargetVEC setTargetView:@"exampleViewController"]; 
   
// TARGET VIEW LINE FOR SWIFT ONLY 
ACPTargetVEC.setTargetView("exampleViewController")
```

Adobe Mobile SDK espone inoltre un metodo alternativo agli sviluppatori per indirizzare le viste personalizzate durante il runtime. Come sviluppatore, devi verificare che le visualizzazioni siano denominate in modo univoco. Chiama il metodo seguente prima di aggiungere la visualizzazione a `superview`:

```
// EXAMPLE TARGET VIEW FOR A CUSTOM VIEW IN OBJECTIVE C 
CustomPopupView *popupView = [[CustomPopupView alloc] initWithFrame:CGRectMake(0, 0, 300, 200)]; 
[ACPTargetVEC setTargetView:@"myCustomPopupView" forView:popupView];

// EXAMPLE TARGET VIEW FOR A CUSTOM VIEW IN SWIFT 
let popupView = CustomPopupView.init(frame: CGRect(x: 0, y: 0, width: 300, height: 200)) 
ACPTargetVEC.setTargetView("myCustomPopupView", for: popupView)
```

## Impostazione dei parametri di profilo e altri parametri globali {#parameters}

Ora supportiamo l&#39;impostazione di parametri globali che vengono passati in ciascuna chiamata API, oltre a passare i parametri mbox/view alle visualizzazioni corrispondenti.

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
ACPTargetParameters *targetParams = [ACPTargetParameters targetParametersWithParameters:mboxParams 
                                                                      profileParameters:profileParams 
                                                                                product:product 
                                                                                  order:order]; 
[ACPTargetVEC setGlobalRequestParameters:targetParams];

//For Swift 
var mboxParams = ["mboxparam1":"mboxvalue1"] 
var profileParams = ["profilekey1":"profilevalue1"] 
var product : ACPTargetProduct = ACPTargetProduct.init(id: "1234", categoryId: "furniture") 
var order : ACPTargetOrder = ACPTargetOrder.init(id: "12345", total: 123.45, purchasedProductIds: ["100", "200"]) 
var targetParams : ACPTargetParameters = ACPTargetParameters.init(parameters: mboxParams, profileParameters: profileParams, product: product, order: order) 
ACPTargetVEC.setGlobalRequest(targetParams)
```

**Trasferimento dei parametri per l’attivazione della vista successiva:**

Sono state fornite alcune visualizzazioni automatiche create per impostazione predefinita, ad esempio &quot;`AUTO_<viewControllerName>`per ciascun controller di visualizzazione presente nell&#39;app. Se si desidera trasferire questi parametri, è possibile chiamare la seguente API:

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
var product : ACPTargetProduct = ACPTargetProduct.init(id: "1234", categoryId: "furniture") 
var order : ACPTargetOrder = ACPTargetOrder.init(id: "12345", total: 123.45, purchasedProductIds: ["100", "200"]) 
var targetParams : ACPTargetParameters = ACPTargetParameters.init(parameters: mboxParams, profileParameters: profileParams, product: product, order: order) 
ACPTargetVEC.setRequest(targetParams)
```

**Trasferimento dei parametri a una visualizzazione specifica:**

Abbiamo visto l&#39;attivazione delle visualizzazioni tramite `TargetVEC.targetView("view_name")`le API. È inoltre possibile trasferire parametri specifici a una particolare visualizzazione, come illustrato di seguito:

```
//For Objective-c 
[ACPTargetVEC setTargetView:@"VIEW_NAME" withParameters:TARGET_PARAMS];

//FOR SWIFT 
ACPTargetVEC.setTargetView("VIEW_NAME", with: TARGET_PARAMS)
```

## Chiamata in modo esplicito dell&#39;API Prefetch {#section_373DB4527FC649C58FBA3DF0C18C9836}

Potrebbero esserci alcuni scenari in cui si potrebbe voler chiamare nuovamente l&#39;API di preacquisizione per aggiornare le offerte archiviate nella cache. Vengono esposte le seguenti API, descritte come:

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

## Esercitazioni: Implementazione delle applicazioni Experience Cloud per dispositivi mobili iOS-C e Swift {#tutorial}

* [Implementazione di Experience Cloud nelle applicazioni Objective-C di iOS](https://docs.adobe.com/content/help/en/experience-cloud/implementing-in-mobile-ios-objective-c-apps-with-launch/index.html)
* [Implementazione di Experience Cloud nelle applicazioni Ios Swift per dispositivi mobili](https://docs.adobe.com/content/help/en/experience-cloud/implementing-in-mobile-ios-swift-apps-with-launch/index.html)

Al termine di queste esercitazioni, potrete:

* Creare una proprietà di avvio mobile
* Installare una proprietà Launch in un&#39;app Objective-C o Swift
* Implementa le seguenti soluzioni Adobe Experience Cloud:
   * Servizio Experience Cloud ID
   * Adobe Target
   * Adobe Analytics 
   * Adobe Audience Manager

* Pubblicare le modifiche in Launch tramite ambienti di sviluppo, staging e produzione