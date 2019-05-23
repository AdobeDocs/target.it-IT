---
description: La nuova libreria SDK di Target consente agli sviluppatori di eseguire la configurazione delle app mobili Android una volta sola e permette agli addetti al marketing di utilizzare le funzionalità del Compositore esperienza visivo mobile.
keywords: VEC mobile;compositore esperienza visivo mobile;opzioni compositore;configurazione;android
seo-description: La nuova libreria SDK di Target consente agli sviluppatori di eseguire la configurazione delle app mobili Android una volta sola e permette agli addetti al marketing di utilizzare le funzionalità del Compositore esperienza visivo mobile.
seo-title: 'Android: configurare l''app mobile'
solution: Target
title: 'Android: configurare l''app mobile'
topic: Standard
uuid: 39938ec2-b12e-44cf-9218-69195fba0ff7
translation-type: tm+mt
source-git-commit: e77022281fa03c8ff8bac111088bdfa4a600783f

---


# Android: configurare l&#39;app mobile{#android-set-up-the-mobile-app}

Adobe Target Mobile App Visual Composer (VEC) consente agli sviluppatori di effettuare una configurazione una tantum sulle app mobili Android e consente agli esperti di marketing di utilizzare le funzionalità della VEC App Mobile.

Per ulteriori informazioni sull&#39;abilitazione dell&#39;estensione VEC Adobe Target, vedi [Adobe Target - Visual Experience Composer](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-target-vec) (Compositore esperienza visivo) negli SDK per dispositivi mobili *Adobe Experience Platform*.

## Includere l&#39;SDK di Mobile e la libreria Target {#sdk-library}

1. Per informazioni sull&#39;inizializzazione di SDK V5, consulta [Inizializzare l&#39;SDK e configurare il tracciamento](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk).
1. Aggiungi la seguente riga alla sezione dipendenze:

   ```
   implementation 'com.adobe.marketing.mobile:target-vec:1.+'
   ```

1. The Mobile App VEC requires the following artifacts to be included as a dependency in `build.gradle`.

   ```
    implementation 'com.google.code.gson:gson:2.8.2'
    implementation 'android.arch.lifecycle:extensions:1.1.1'
    implementation('io.github.sac:SocketclusterClientJava:1.7.5')
    implementation 'com.android.support:support-annotations:28.0.0'
    implementation 'com.android.support:support-compat:28.0.0'
    implementation 'com.android.support:design:28.0.0'
   ```

1. Aggiungi un filtro di intento nel `AndroidManifest.XML` file, scegliendo uno schema di collegamento profondo per l&#39;authoring VEC App mobile (ad esempio, `[sdkbetabus://com.adobe.sdkbetabus](sdkbetabus://com.adobe.sdkbetabus)`):

   ```
   <activity 
       android:name=".listing.MoviesListingActivity" 
       android:launchMode="singleTask"> 
       <intent-filter> 
           <action android:name="android.intent.action.VIEW" /> 
   
           <category android:name="android.intent.category.DEFAULT" /> 
           <category android:name="android.intent.category.BROWSABLE" /> 
   
           <data 
               android:host="com.adobe.sdkbetabus" 
               android:scheme="sdkbetabus" /> 
       </intent-filter> 
   </activity>
   ```

1. Vai al progetto mobile e inserisci le righe che seguono alla fine di `Application::onCreate override`:

   ```
   public class SDKTest extends MultiDexApplication { 
   
       @Override 
       public void onCreate() { 
           /* Put Your App's implementation */ 
           MobileCore.setApplication(this); 
           MobileCore.setLogLevel(LoggingMode.DEBUG); 
           MobileCore.configureWithAppID("YOUR_ADOBE_LAUNCH_APP_ID"); 
   
           ... 
           try { 
               TargetVEC.registerExtension(); //Single line code to initialize TargetVEC
               Target.registerExtension();
               Identity.registerExtension();
               Lifecycle.registerExtension();
               Signal.registerExtension();
               MobileCore.start(new AdobeCallback () {
                  @Override
                  public void call(Object o) {
                     MobileCore.configureWithAppID("launch-EN4e833d644d1949e39e985ddad4f52bd4-development");
                  }
               });
           } catch (InvalidInitException e) { 
             .. 
           }
       }
   
   /* Rest of Application test goes here ... */
   ```

1. Se qualcosa non funziona, esamina i progetti di esempio forniti di seguito che dovrebbero essere pronti all’uso ed esamina le modifiche nelle seguenti posizioni:

   1. `Application::OnCreate override`
   1. `AndroidManifest.XML`
   1. `build.gradle` dell&#39;applicazione Android

## Configurare le visualizzazioni Target nell&#39;app mobile {#views}

L’SDK Adobe Mobile espone un nuovo metodo per gli sviluppatori da attivare ogni volta che viene effettuato il rendering di una nuova visualizzazione. In qualità di sviluppatore, devi assicurarti che le visualizzazioni siano denominate in modo univoco e che la chiamata `targetView` si trovi sul thread principale dell’interfaccia utente. In questa sezione, verrà innanzitutto mostrato come inserire queste chiamate con due applicazioni dimostrative diverse e discutere delle linee guida generali su come inserire correttamente le chiamate API di Target per qualsiasi app Android.

>[!NOTE]
>
>Se non viene `targetView function` attivato, l&#39;estensione VEC tenta di identificare la Visualizzazione dall&#39;attività Android. Per le applicazioni che non dispongono di visualizzazioni dinamiche, questo può essere un passaggio facoltativo.

Una visualizzazione Target può essere attivata con una chiamata di funzione. Eventuali parametri di targeting possono essere facoltativamente forniti insieme alla vista.

```
public class TargetVEC { 
   
   /** 
    * Marks a view hierarchy for editing in Mobile App VEC.  Call must insert when the view hierarchy 
    * is memory and committed to being shown, but not yet shown on the screen. 
    * 
    * @param viewName the unique Target View Name 
    */ 
   public static void targetView(String viewName); 
  
  /** 
   * Trigger Target view 
   * Triggering a Target view may cause Target offers to be applied on the current container component. 
   * Note that Target offers are applied from local Target cache, so flicker should be negligible. 
   * 
   * @param viewName Mandatory Target View name, which must be unique at app level 
   * @param parameters Parameters to be included in the next Target call 
   */ 
  
    public static void targetView(String viewName, TargetParameters parameters); 
}
```

Il primo progetto di esempio è la simulazione di una semplice applicazione per gli orari dell’autobus. Per impostare questa applicazione per l&#39;utilizzo nella app mobile VEC:

1. In Android Studio, apri il progetto con il file `build.gradle` nella sottodirectory del pacchetto `BusBooking`.
1. Nel metodo `DemoApplication::OnCreate`, aggiungi `TargetVEC.registerExtension()` per registrare l’estensione Compositore esperienza visivo di Target, insieme ad altre estensioni.
1. Genera ed esegui l’applicazione.
1. Per passare alla modalità di authoring VEC App mobile, usa il [!DNL sdkbetabus://com.adobe.sdkbetabus] relativo schema URL e apri il collegamento profondo generato sul dispositivo (vedi le indicazioni sotto).

In questa semplice applicazione per la prenotazione dell’autobus, utilizziamo tutte le Visualizzazioni di destinazione generate automaticamente e associate con il ciclo di vita dell’attività. Inoltre dimostriamo la flessibilità dell’API chiamando l’API della Visualizzazione di destinazione su un elemento con visualizzazione personalizzata che viene aggiunto dinamicamente quando si fa clic su un pulsante nascosto (l’immagine dell’offerta sullo schermo). Questa nuova Visualizzazione di destinazione è implementata inserendo una chiamata API nel codice di `OfferDetailsActivity.java:40`. Quando si fa clic sul pulsante nascosto, viene attivato un nuovo evento Visualizzazione di destinazione denominato “SURPRISE_VIEW”, consentendo all’addetto al marketing di modificare in modo più mirato l’esperienza dell’applicazione.

Inserimento Visualizzazione dinamica di destinazione:

```
package com.adobe.target.examples.bus; 
   
import android.app.DialogFragment; 
import android.os.Bundle; 
import android.os.Handler; 
import android.support.v7.app.AppCompatActivity; 
import android.support.v7.widget.Toolbar; 
import android.view.View; 
import android.view.ViewGroup; 
import android.widget.LinearLayout; 
import android.widget.Toast; 
   
import com.adobe.target.mobile.TargetVEC; 
   
/** 
 * This activity class is responsible to show offer details 
 */ 
public class OfferDetailsActivity extends AppCompatActivity { 
    @Override 
    protected void onCreate(Bundle savedInstanceState) { 
        super.onCreate(savedInstanceState); 
        setContentView(R.layout.activity_offer_details); 
        setUpToolBar(); 
        final Handler mainHandler = new Handler(getApplicationContext().getMainLooper()); 
   
        final View surpriseView = getLayoutInflater().inflate(R.layout.suprise_layout, 
                (ViewGroup) findViewById(android.R.id.content), false); 
   
        final View imagePresentView = this.findViewById(R.id.image_present); 
        final LinearLayout currentLayout = this.findViewById(R.id.offer_layout); 
   
        imagePresentView.setOnClickListener(new View.OnClickListener() { 
            @Override 
            public void onClick(View v) { 
                Toast.makeText(getApplicationContext(),"Surprise!", Toast.LENGTH_SHORT).show(); 
                mainHandler.post(new Runnable() { 
                    @Override 
                    public void run() { 
                        currentLayout.addView(surpriseView); 
                        TargetVEC.targetView("SURPRISE_VIEW"); 
                        currentLayout.invalidate(); 
                    } 
                }); 
                // One-shot.  Remove clicker afterwards. 
                imagePresentView.setOnClickListener(null); 
            } 
        }); 
    } 
   
    private void setUpToolBar() { 
        Toolbar toolbar = findViewById(R.id.toolbar); 
        toolbar.setNavigationIcon(R.drawable.abc_ic_ab_back_material); 
        toolbar.setTitle("Buy 1 Get 1"); 
        toolbar.setNavigationOnClickListener(new View.OnClickListener() { 
            @Override 
            public void onClick(View v) { 
                onBackPressed(); 
            } 
        }); 
    } 
   
    @Override 
    protected void onPause() { 
        super.onPause();
        MobileCore.lifecyclePause();
    } 
   
    @Override 
    protected void onResume() { 
        super.onResume();
        MobileCore.lifecycleStart(null);
    } 
}
```

## Impostazione dei parametri di profilo e altri parametri globali {#parameters}

Ora supportiamo l&#39;impostazione di parametri globali che verranno trasmessi in ciascuna chiamata API, oltre a passare parametri mbox/view alle visualizzazioni corrispondenti.

I parametri includono:

* parametri mbox/di visualizzazione
* parametri del profilo
* Parametri del prodotto
* Parametri dell’ordine

**Supporto globale dei parametri:**

```
Map<String, String> mboxParams = new HashMap<>();  //Mbox or view params 
mboxParams.put("mboxparam1", "mboxvalue1"); 
Map<String, String> profileParams = new HashMap<>();  //Profile params 
profileParams.put("profilekey1", "profilevalue1"); 
  
TargetVEC.setGlobalRequestParameters(new TargetParameters.Builder() 
        .parameters(mboxParams) 
        .profileParameters(profileParams) 
        .product(new TargetProduct("1234", "furniture")) 
        .order(new TargetOrder("12343", 123.45, Arrays.asList("100", "200"))) 
        .build());
```

**Trasferimento dei parametri per l’attivazione della vista successiva:**

Sono state fornite alcune visualizzazioni automatiche create per impostazione predefinita, ad esempio &quot;`AUTO_<activity|fragment name>`per ogni attività e frammento presente nell&#39;app. Se si desidera trasferire questi parametri, è possibile chiamare la seguente API:

```
Map<String, String> mboxParams = new HashMap<>();  //Mbox or view params 
mboxParams.put("viewKey1", "viewparam1"); 
Map<String, String> profileParams = new HashMap<>();  //Profile params 
profileParams.put("profilekeyforview1", "profilevalueforview1"); 
  
TargetVEC.setRequestParameters(new TargetParameters.Builder() 
        .parameters(mboxParams) 
        .profileParameters(profileParams) 
        .product(new TargetProduct("1234", "furniture")) 
        .order(new TargetOrder("12343", 123.45, Arrays.asList("100", "200"))) 
        .build());
```

**Passare parametri a una visualizzazione specifica:**

Abbiamo visto l&#39;attivazione delle visualizzazioni tramite `TargetVEC.targetView("view_name")`le API. È inoltre possibile trasferire parametri specifici a una particolare visualizzazione, come illustrato di seguito:

```
Map<String, String> profileParams = new HashMap<>(); 
profileParams.put("surprisekey1", "surprisevalue1");  //ProfileParams 
TargetVEC.targetView("SURPRISE_VIEW", 
        new TargetParameters.Builder() 
                .profileParameters(profileParams) 
                .product(new TargetProduct("3354", "kitchen")) 
                .build());
```

## Chiamata in modo esplicito dell&#39;API Prefetch {#section_2D02B74558474D3BA9F25E4D25E7C7E3}

Potrebbero esserci alcuni scenari in cui si potrebbe voler chiamare nuovamente l&#39;API di preacquisizione per aggiornare le offerte archiviate nella cache. Vengono esposte le seguenti API, descritte come:

* **prefetchOffers**

   ```
   /** 
    * Prefetch Target offers. 
    * Note that calling this will pre-hide the current layout, until Target offers are prefetched 
    * and applied to currently visible Target views, possibly causing flicker, thus it's recommended 
    * to call this method inside the containing component's onCreate() lifecycle method 
    */ 
   public static void prefetchOffers();
   ```

* **prefetchOffersBackground**

   ```
   /** 
    * Prefetch Target offers in the background. 
    * Note, that in contrast to prefetchOffers(), calling this method will NOT pre-hide 
    * the current layout, instead prefetched Target offers will be only be cached and will subsequently 
    * be applied as Target Views are being triggered. 
    */ 
   public static void prefetchOffersBackground();
   ```

## Esercitazione: Implementazione di Experience Cloud nelle applicazioni Android mobile {#tutorial}

* [Implementazione di Experience Cloud nelle applicazioni Android mobile](https://docs.adobe.com/content/help/en/experience-cloud/implementing-in-mobile-android-apps-with-launch/index.html)

Dopo aver completato questa esercitazione potrete:

* Creare una proprietà di avvio mobile
* Installazione di una proprietà Launch in un&#39;app Android
* Implementa le seguenti soluzioni Adobe Experience Cloud:
   * Servizio Experience Cloud ID
   * Adobe Target
   * Adobe Analytics 
   * Adobe Audience Manager

* Pubblicare le modifiche in Launch tramite ambienti di sviluppo, staging e produzione
