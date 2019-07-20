---
description: Dettagli sulle modifiche apportate in ogni versione di at.js.
keywords: versioni at.js;versione at.js
seo-description: Dettagli sulle modifiche apportate in ogni versione di at.js.
seo-title: Dettagli sulle versioni di at.js
solution: Target
subtopic: Introduzione
title: Dettagli sulle versioni di at.js
uuid: 3586af55-db15-4e68-90a7-d552338ec5e8
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Dettagli sulle versioni di at.js {#at-js-version-details}

Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js [!DNL Adobe Target].

>[!IMPORTANT]
>
>Il team di Target gestisce solo due versioni di [!DNL at.js], la versione corrente e quella immediatamente precedente. Aggiorna [!DNL at.js] per assicurarti di eseguire una versione supportata.

## at. js versione 2.1.0 (3 giugno 2019)

Questa versione include i miglioramenti e le funzioni seguenti:

* **Supporto Adobe Consenso**: Adobe Consenso è un modo per semplificare le integrazioni delle soluzioni Adobe con le piattaforme di gestione del consenso. Per ulteriori informazioni su Adobe Opt-in, consulta [Privacy e Regolamento generale sulla protezione dei dati (RGPD)](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md).

* **Conformità standard di settore CSP**: at. js no uses eval () to execute javascript.

* **Registrazione analisi lato client**: Fornisci ai clienti un controllo completo su come desiderano inviare dati analitici ad Adobe Analytics, sia sul lato client che sul lato server.

   For more information, see [Client-side Analytics logging](/help/c-integrating-target-with-mac/a4t/before-implement.md#client-side) in *Before you implement*.

* **Invia notifiche**: Consentite agli sviluppatori di inviare notifiche quando un'esperienza viene sottoposta a rendering dal codice anziché utilizzare `applyOffer()` o `applyOffers()`.

   For more information, see [adobe.target.sendNotifications(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe.target.sendnotifications-atjs-21.md).

* **at. js size reduce by ~ 24%**: La dimensione di at. js viene ridotta di ~ 24%. Le dimensioni del file più piccole migliorano le prestazioni di caricamento delle pagine e riducono il tempo di download su. js sulla pagina.

## at.js versione 2.0.1 (19 marzo 2019)

Questa è una versione di manutenzione e include i miglioramenti e le correzioni seguenti:

(I codici tra parentesi sono per uso interno di [!DNL Adobe].)

* È stata risolta una situazione di tipo “race condition” nel codice di polling DOM che causava eccezioni JavaScript per alcuni clienti. (TNT-31869)
* Le notifiche di rendering delle visualizzazioni sono state disaccoppiate dai gestori di eventi di tracciamento dei clic. Inizialmente, Target non inviava notifiche se non era possibile allegare gestori di eventi di tracciamento dei clic a una visualizzazione riprodotta. Target invia ora una notifica della visualizzazione anche quando non vengono trovati elementi di clic. (TNT-31969)
* È stato risolto un problema per cui il flag di reindirizzamento dell’evento della richiesta riuscita era sempre impostato su true. (TNT-31907)
* È stato risolto un problema che causava la registrazione con successo dell’azione di riorganizzazione del Compositore esperienza visivo, anche quando mancavano elementi. (TNT-31924)
* È stato risolto un problema che causava la mancata inclusione del token di proprietà delle Autorizzazioni Enterprise per alcuni clienti. (TNT-31999)

## at.js versione 1.7.1 (19 marzo 2019)

Questa è una versione di manutenzione e include la seguente correzione:

(I codici tra parentesi sono per uso interno di [!DNL Adobe].)

* È stata risolta una situazione di tipo “race condition” nel codice di polling DOM che causava eccezioni JavaScript per alcuni clienti. (TNT-31869)

## at.js versione 2.0.0 {#at-js-200}

at.js 2.x offre set di funzioni avanzate che consentono di eseguire personalizzazioni su tecnologie lato client di nuova generazione. Questa nuova versione si concentra sull'aggiornamento di at.js per garantire interazioni in sintonia con le applicazioni a pagina singola.

Di seguito sono riportati alcuni vantaggi dell’utilizzo di at.js 2.x che non sono disponibili nelle versioni precedenti:

* La capacità di memorizzare nella cache tutte le offerte al caricamento di pagina per ridurre più chiamate al server a una singola chiamata al server.
* Migliora enormemente le esperienze degli utenti finali sul sito, in quanto le offerte appaiono immediatamente tramite la cache senza l’implementazione di chiamate al server tradizionali.
* Una semplice riga di codice e una configurazione per sviluppatori una tantum per consentire agli esperti di marketing di creare ed eseguire attività A/B e di esperienza (XT) tramite il Compositore esperienza visivo sulle applicazioni a pagina singola.

at.js 2.x introduce le seguenti nuove funzioni:

* getOffers()
* applyOffers()
* triggerView()

Le seguenti funzioni sono state rese obsolete con l’introduzione di at.js 2.x:

* mboxCreate()
* mboxDefine
* registerExtension()

Per ulteriori informazioni, consulta [Aggiornamento da at.js 1.x a at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md) e [Funzioni di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md).

>[!NOTE]
>
>If you require Adobe Opt-in support for the [General Data Protection Regulation](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md) (GDPR), you must currently use at.js 1.7.0 or at.js 2.1.0.

## at.js versione 1.7.0 {#at-js-170}

at.js 1.7.0 include il supporto di Adobe Opt-In. Adobe Opt-in è un metodo per semplificare le integrazioni delle soluzioni Adobe con le piattaforme di gestione del consenso.

Per ulteriori informazioni su Adobe Opt-in, consulta [Privacy e Regolamento generale sulla protezione dei dati](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md) (RGPD).

Questa versione risolve anche un problema in cui Target potrebbe sostituire i parametri degli URL reindirizzati con parametri provenienti dall’URL di reindirizzamento.

>[! NOTA]
>
>If you require Adobe Opt-in support for GDPR, you must currently use at.js 1.7.0 or 2.1.0.<br>For a list of all versions, see [at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

## at.js versione 1.6.4 {#at-js-164}

at.js 1.6.4 è una versione di manutenzione e risolve il seguente problema:

* È stata corretta una situazione di tipo “race condition” critica in Microsoft Internet Explorer 11 che causava l’applicazione di offerte duplicate.

## at.js versione 1.6.3 {#section_484A56774E004282B98FFFF851E4E670}

at.js versione 1.6.3 include le correzioni e i miglioramenti seguenti:

* I selettori sono ora in sequenza CSS se contengono ID o classi CSS che iniziano con una cifra, due trattini o un trattino seguito da una cifra (ad esempio #-123). (TNT-31061)
* Risolto un problema introdotto con at.js 1.6.2 per cui le offerte del Compositore esperienza visivo di diverse attività che si applicavano allo stesso selettore CSS non rispettavano la priorità delle attività. (TNT-31052)
* Corretto un problema con il timeout di una promessa in ambienti in cui non era presente alcun supporto nativo per le promesse. (TNT-30974)
* L’acquisizione e la segnalazione dei problemi ora avviene correttamente tramite l’evento di rendering del contenuto non riuscito. In precedenza, il sistema poteva segnalare la corretta esecuzione di JavaScript anche in caso contrario. (TNT-30599)

## at.js versione 1.6.2 {#section_88BE2F69943D4280B8170F377886B58E}

Questa è una versione di manutenzione e risolve il seguente problema:

* Risolto un problema che portava a un ciclo “async” infinito in alcuni siti clienti.

>[!IMPORTANT]
>
>Inoltre, la versione 1.6.2 di at.js contiene tutti i miglioramenti e le correzioni inclusi nelle versioni 1.6.1 e 1.6.0 di at.js. Queste versioni non sono più disponibili per il download. Si consiglia di eseguire l'aggiornamento alla versione 1.6.2 se si utilizza la versione 1.6.1 o 1.6.0

Ecco i miglioramenti e le correzioni che sono stati inclusi nella versione 1.6.1 di at.js:

* Risolto un problema in at.js 1.6.0 che causava la duplicazione delle esperienze dei consigli in Microsoft Internet Explorer 11. (TNT-30593)
* at.js ora assicura che la logica di sovrascrittura Edge verifichi l'esistenza di un cookie del cluster Edge per evitare un numero di bordi diverso se un utente salta i bordi durante una sessione. (TNT-30563)
* Risolto un problema che impediva ad at.js di eseguire azioni successive se il contenuto HTML conteneva codice JS non valido. at.js ora registra l'errore ed effettua il rendering delle azioni rimanenti senza problemi. (TNT-30546)
* Modifiche apportate affinché vi sia un'eccezione quando una pagina di reindirizzamento si riqualifica per un'attività di reindirizzamento. (TNT-30532)
* Risolto un problema che impediva la propagazione del timeout della richiesta corretta dalla richiesta API getOffer(). (TNT-30498)
* Risolto un problema che impediva ad at.js 1.6.0 di salvare i cookie durante l'utilizzo del protocollo file. (TNT-30454)
* Risolto un problema che faceva sembrare che non tutte le esperienze venissero consegnate con reindirizzamenti quando si utilizzava Analytics for Target (A4T). (TNT-30444)
* Risolto un problema per il quale la pagina era nascosta dopo il successo della chiamata Target. (TNT-30358)

Ecco i miglioramenti e le correzioni che sono stati inclusi nella versione 1.6.0 di at.js:

* Le offerte di reindirizzamento sono ora supportate automaticamente nell'integrazione Analytics for Target (A4T). La soluzione lato client è stata rimossa. (TNT-30247)
* Il routing Edge lato client è ora abilitato per impostazione predefinita. (TNT-30261)
* Risolto un problema con il rendering delle azioni del Compositore esperienza visivo in presenza di dipendenze tra le azioni. (TNT-30248)

## at.js versione 1.5.0 {#section_128C6761884C4DA8AE50D6A605FF6F55}

È ora disponibile la versione 1.5.0 di at.js.

* I dettagli dell’evento `at-request-succeeded` contengono il flag di reindirizzamento. Questo flag può essere utilizzato per determinare se la pagina verrà reindirizzata a un URL diverso. Se desideri conoscere l'URL, abbonati a `at-content-rendering-redirect`. (TNT-29834)
* È stato risolto un problema che ha causato il mancato funzionamento di `window.targetGlobalSettings.enabled` con un'eccezione di esecuzione se è stato impostato su falso. (TNT-29829)
* È stato risolto un problema che ha causato un errore durante il caricamento nel Compositore esperienza visivo se si utilizza il codice personalizzato per una richiesta mbox globale di abilitazione e si nasconde il corpo. (TNT-29795)
* È stato aggiunto il supporto per `screenOrientation`, `devicePixelRatio` e `webGLRenderer`. Questi nuovi parametri di richiesta di Target vengono utilizzati per iPhone X e altri sistemi di rilevamento dispositivi moderni. Per ulteriori informazioni, consulta [Mobile](../../c-target/c-audiences/c-target-rules/mobile.md#concept_2A794199DC1A4D349FFFBC7DCF1FEB89). (TNT-29781)
* È stato risolto un problema per cui il suggerimento di posizione di Adobe Audience Manager (AAM) non veniva sempre inviato. (TNT-29695)
* Per i browser che lo supportano, at.js 1.5.0 passa a MutationObserver per la votazione del selettore. Le versioni precedenti a at.js 1.0.0 utilizzavano un polyfill MutationObserver, che si è dimostrato problematico. Per evitare problemi di polyfill, la versione 1.5.0 utilizza il seguente pseudo codice per decidere quale meccanismo di programmazione utilizzare:

   ```
   if MutationObserver is supported
     scheduler = MutationObserver
   else if document is visible
     scheduler = requestAnimationFrame
   else
     scheduler = setTimeout
   ```

## at.js versione 1.3.0 {#section_24EAAE1CFA814EF8B19E61842F4D8321}

È ora disponibile la versione 1.3.0 di at.js.

* I seguenti nuovi eventi sono disponibili per facilitare il tracciamento, il debug e la personalizzazione dell’interazione con at.js:

   * LIBRARY_LOADED
   * REQUEST_START
   * CONTENT_RENDERING_START
   * CONTENT_RENDERING_NO_OFFERS
   * CONTENT_RENDERING_REDIRECT
   Per ulteriori informazioni, consulta [Eventi personalizzati at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/atjs-custom-events.md).

* È possibile integrare una richiesta at.js con parametri aggiuntivi provenienti da provider di dati. Aggiungi i provider di dati a `window.targetGlobalSettings` nella `dataProviders key`.

   Per ulteriori informazioni, vedi [Provider di dati](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers).

* Le richieste at.js ora utilizzano GET, ma passeranno a POST quando la dimensione dell’URL supererà i 2048 caratteri. La nuova proprietà `urlSizeLimit` consente di aumentare questo limite, se necessario. Questa modifica consente di allineare Target at.js ad AppMeasurement, che utilizza la stessa tecnica.
* Target ora impone di utilizzare la chiave `mbox` nella funzione `adobe.target.applyOffer(options)`. Questa chiave era già richiesta in passato, ma Target ora ne impone l’utilizzo per garantire la corretta convalida di Target e il corretto utilizzo di questa funzione da parte dei clienti.
* at.js offre una funzionalità migliorata per il tracciamento di eventi e clic. at.js utilizza `navigator.sendBeacon()` per inviare i dati di tracciamento degli eventi; se `navigator.sendBeacon()` non è supportato, si basa su richieste XHR sincrone. Questa alternativa riguarda principalmente Internet Explorer 10 e 11 e alcune versioni di Safari. Con iOS 11.3, in Safari verrà aggiunto il supporto di `navigator.sendBeacon()`.
* at.js ora può renderizzare le offerte anche quando una pagina viene aperta nelle schede in background. Alcuni utenti di Target hanno riscontrato problemi quando `requestAnimationFrame()` è stato disattivato a causa del comportamento di limitazione del browser per le schede in background.
* In questa versione sono stati aggiunti svariati miglioramenti a livello di prestazioni, tra cui call stack più brevi durante l’ispezione di un profilo CPU in Chrome.
* at.js 1.3.0 non supporta più la consegna di contenuti in Microsoft Internet Explorer 9. Per un elenco dei browser supportati, consulta [Browser supportati](../../c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md#reference_01B4BF99E7D545A7998773202A2F6100). Da adesso in poi, tutte le richieste vengono eseguite tramite `XMLHttpRequest` con supporto CORS, senza richieste JSONP. Questa modifica migliora notevolmente la sicurezza.

## at.js versione 1.2.3 {#section_CE4D14AF00D04F4C8A2F0513F5EA1A84}

È ora disponibile la versione 1.2.3 di [!DNL at.js].

* Aggiunge il supporto per le offerte JSON. Le offerte JSON sono supportate solo nelle attività create utilizzando il Compositore esperienza basato su moduli. Attualmente le offerte JSON possono essere utilizzate solo tramite chiamate API dirette. Consulta [Creare offerte JSON](../../c-experiences/c-manage-content/create-json-offer.md#concept_63C7BEE1F0DB4A7596D997219B7C136D).

## at.js versione 1.2.2 {#section_4E96D13F2DFE4F1F81A1089877D53649}

È ora disponibile la versione 1.2.2 di [!DNL at.js].

* È stato risolto un problema a causa del quale veniva restituito un errore di JavaScript se la libreria di Target era caricata in una pagina che utilizzava la modalità non standard. (TNT-28312)
* È stato risolto un problema a causa del quale il tracciamento dei clic di Target impediva il corretto funzionamento delle chiamate di raccolta dati di Analytics. (TNT-28261)
* È stato corretto un problema che impediva il corretto funzionamento di `getOffer() params` se `targetPageParams()` restituiva una stringa vuota. (TNT-28359)
* È stato risolto un problema nella generazione dell’ID di sessione quando si utilizza solo x. (TNT-28361)

## at.js versione 1.2.1 {#section_F757C8174BBA4F68AC5524ADC3D9C5E3}

È ora disponibile la versione 1.2.1 di [!DNL at.js].

* È stato risolto un problema che impediva a Target di aprire il collegamento in una nuova scheda durante il tracciamento dei clic su un collegamento con target="_blank".

## at.js versione 1.2.0 {#section_1C3A18C595C34B25A14A440D213F3B9C}

La versione 1.2 di [!DNL at.js] è ora disponibile come una versione di manutenzione che contiene per lo più correzioni di bug.

* È stato risolto un problema che impediva azioni predefinite per i casi speciali di tracciamento dei clic. (TNT-28089)
* È stato risolto un problema che impediva a Target di aprire il collegamento in una nuova scheda durante il tracciamento dei clic con un collegamento contenente `target="_blank"`. (TNT-28072)
* Gli indirizzi IP possono essere utilizzati come dominio dei cookie. (TNT-28002)
* È stato risolto un problema che causava la visualizzazione momentanea di altro contenuto nelle offerte di reindirizzamento aventi una mbox globale o altre mbox regionali. (TNT-27978)
* È stato risolto un problema che causava un errore nell’impostazione di attività Targeting esperienza nel Compositore esperienza visivo durante il passaggio da Sfoglia a Componi e viceversa. (TNT-27942)
* È stata risolta la gestione errata delle classi di stile che causava la visualizzazione momentanea di altro contenuto sugli elementi contrassegnati per il monitoraggio dei clic. (TNT-27896)
* È stato corretto un problema a causa del quale i parametri mbox globali si mescolavano con gli altri parametri mbox. (TNT-27846)
* Sono state apportate modifiche per garantire che Handlebar, Mustache e altre librerie di modelli lato client siano gestite correttamente da [!DNL at.js]. (TNT-27831)
* Sono state apportate modifiche per garantire che `sdidParamExpiry` sia inizializzato correttamente e passato all’API visitatore. Questa è una regressione che è stata aggiunta a `at.js 1.1.0`. Non influisce sulle versioni precedenti di [!DNL at.js]. Questa modifica riguarda soltanto i clienti che usano offerte di reindirizzamento e A4T. (TNT-27791)
* Sono state apportate modifiche per garantire che `SCRIPT` venga eseguito indipendentemente dal tipo di attributo utilizzato. (TNT-27865)

## at.js versione 1.1.0 {#section_8F494E1EA94E48A9B169F5CF9FE6DC56}

**Data:** 2 agosto 2017

I seguenti miglioramenti e correzioni sono inclusi nella versione 1.1 di [!DNL at.js]:

* È stata aggiunta la gestione dei token di risposta. Per ulteriori informazioni, consulta [Token di risposta](../../administrating-target/response-tokens.md#concept_2B21B222F6A344D68CA5929817E836C4).
* È stato risolto un problema in modo che `document.currentScript polyfill` non interferisca con Angular 1.X.
* Sono state apportate modifiche per garantire che il tracciamento dei clic non interferisca con la proprietà di visibilità. Gli elementi di tracciamento dei clic sono contrassegnati con la classe CSS `at-element-click-tracking` anziché `at-element-marker`.

## at.js versione 1.0.0 {#section_37A3D23FC4AD42A68AA831B89E03E725}

**Data:** 7 luglio 2017

I miglioramenti e le correzioni seguenti sono inclusi nella versione 1.0 di at.js:

* Supporto per il caricamento in modo asincrono di at.js per caricare le pagine più velocemente.
* Supporto che consente di pre-nascondere il contenuto della pagina durante il caricamento di at.js in modo asincrono.
* Miglioramento della messaggistica di errore quando la consegna del contenuto è disattivata.
* Miglioramenti delle prestazioni durante la distribuzione di più attività.
* Supporto per il compressore YUI.
* Segnalazione di bug ed errori per eventi personalizzati durante la consegna delle attività.
* Correzione di problemi di prestazione in Microsoft Internet Explorer 11.
* Risoluzione della funzione `getOffer()` che dava un errore su alcuni siti web.
* È possibile caricare la libreria di Target in modo asincrono. Per ulteriori informazioni, consulta [Domande frequenti su at.js](../../c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/target-atjs-faq.md#concept_D6EFE8D84A06476DB5ABD494D7E8C769).

## at.js versione 0.9.7 {#section_6C7B698BE21E40E495FD2850EFBF3E80}

**Data:** 22 maggio 2017

I seguenti miglioramenti e correzioni sono inclusi nella versione 0.9.7 di [!DNL at.js]:

* Correzione di un problema relativo a una chiave di asset mancante dalle azioni `insertAfter` e `insertBefore` nel Compositore esperienza visivo. Questi problemi erano correlati alla migrazione da offerte visive a modelli di offerte.

## at.js versione 0.9.6 {#section_EEFA6413F2F947AD8C4A88128B90245D}

**Data:** 13 aprile 2017

I seguenti miglioramenti e correzioni sono inclusi nella versione 0.9.6 di [!DNL at.js]:

* Supporto per le offerte di reindirizzamento per A4T. Dopo aver scaricato e installato la versione 0.9.6 di [!DNL at.js], è possibile utilizzare le offerte di reindirizzamento in attività che utilizzano [!DNL Adobe Analytics] come origine per la generazione di rapporti per [!DNL Target] (A4T). Oltre alla versione 0.9.6 di [!DNL at.js], l’implementazione deve soddisfare altri requisiti minimi al fine di usare le offerte di reindirizzamento e A4T. Per ulteriori informazioni e importanti informazioni aggiuntive che dovresti conoscere, consulta [Offerte di reindirizzamento: domande frequenti su A4T](../../c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905).
* Prima della versione 0.9.6 di [!DNL at.js], se l’API visitatore era presente nella pagina e l’impostazione `visitorApiTimeout` era troppo aggressiva, poteva capitare che i dati MCID non venissero inviati nella richiesta di [!DNL Target]. Questo poteva portare a problemi come la presenza di dati parziali in [!DNL Analytics] durante l’utilizzo di A4T.

   Questo comportamento è stato modificato nella versione 0.9.6 di [!DNL at.js]: anche se l’impostazione `visitorApiTimeout` è impostata su 1 ms, ad esempio, Target tenterà di raccogliere SDID, server di tracciamento e dati degli ID cliente, per inviarli nella richiesta di Target.

* È stata aggiunta l’impostazione `selectorsPollingTimeout`. Per ulteriori informazioni, consulta [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md).
* Il formato della risposta da `getOffer()` è stato modificato. Per ulteriori informazioni, consulta [adobe.target.getOffer(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffer.md).
* La funzione di log della console è stata aggiunta per le dichiarazioni `<!DOCTYPE>` non supportate.
* È stato risolto un problema a causa del quale i plug-in di [!DNL Target Classic] non venivano applicati correttamente quando venivano distribuite offerte multiple predefinite a un singolo mbox. (TGT-22664) Per ulteriori informazioni, vedi [Plug-in](https://marketing.adobe.com/resources/help/en_US/tnt/help/t_Using_Plug-Ins.html) nella documentazione di Adobe Target Classic.
* È stata migliorata la configurazione dei cookie per i domini di primo livello a due lettere (TLD) per garantire che il cookie mbox venga configurato correttamente per questi domini (ad esempio [!DNL test.no], [!DNL autodrives.ca] e così via).
* L’algoritmo per l’estrazione del dominio di primo livello che deve essere utilizzato quando si salvano i cookie è stato modificato nella versione 0.9.6. di at.js. A causa di questa modifica, i cookie non possono essere salvati in indirizzi IP. Il più delle volte, gli indirizzi IP vengono utilizzati per scopi di test, ma come soluzioni alternative è possibile utilizzare le voci DNS, regolare il file host in una casella locale.
* Risolta la gestione delle azioni Sposta e Ridisponi nel caso in cui le proprietà siano valori stringa anziché numeri interi.

## at.js versione 0.9.4 {#section_A15B12F12CD94F07B3F56613A79A815F}

**Data:** 19 gennaio 2017

* I nomi mbox possono ora contenere caratteri speciali, tra cui il simbolo &amp;, per essere coerenti con i requisiti di denominazione per i nomi mbox che utilizzano mbox.js.

   Per un elenco dei caratteri speciali consentiti, consulta [Configurazioni at.js](../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#concept_2FA0456607D04F82B0539C5BF5309812).

* È stata aggiunta l’impostazione `secureOnly` che indica se at.js deve utilizzare solo HTTPS o può passare da HTTP a HTTPS in base al protocollo della pagina. Si tratta di un’impostazione avanzata con impostazione predefinita False e può essere bypassata tramite `targetGlobalSettings`.
* L'opzione [!UICONTROL Supporto di browser legacy] è disponibile nelle versioni 0.9.3 e precedenti di at.js. Questa opzione è stata rimossa nella versione 0.9.4 di at.js.

## at.js versione 0.9.3 {#section_DF13BC1D7C994AE7A36B81937A699DF4}

**Data:** 10 ottobre 2016

* Le chiamate mbox si attivano in Microsoft Internet Explorer 11 quando i browser legacy sono disabilitati nelle impostazioni at.js.
* Il contenuto predefinito viene renderizzato in caso di mancata riuscita di un’offerta remota dinamica (ad esempio, se l’URL non è corretto e genera un errore 404).
* Garantisce che gli elementi vengano rivelati rapidamente quando è impossibile trovare i selettori di tracciamento clic del Compositore esperienza visivo nel DOM.

## at.js versione 0.9.2 {#section_148549CBB4F046BAA8F79C79B64EC889}

**Data:** 21 settembre 2016

* È stata aggiunta un’impostazione `optoutEnabled` per abilitare o disabilitare la rinuncia a Device Graph. Se questa impostazione si trova su `true` e il visitatore ha rinunciato al monitoraggio, il browser del visitatore non effettuerà chiamate mbox. Device Graph è attualmente in versione beta. Questa impostazione si trova su `false` come impostazione predefinita ma deve trovarsi su `true` se si sta utilizzando Device Graph (Grafico dispositivo). Un’opzione simile è disponibile anche in mbox.js v.61.
* È stato aggiunto il supporto di `CustomEvent` per il meccanismo di notifica. In precedenza, il meccanismo di notifica degli eventi at.js non poteva essere utilizzato tramite API DOM standard, come ad esempio `document.addEventListener()`. Ora è possibile utilizzare `document.addEventListener()` per effettuare la sottoscrizione a eventi at.js, come ad esempio eventi di richiesta e di rendering del contenuto.
* È stato risolto un problema relativo alle offerte create nel Compositore esperienza visivo. Prima di questa versione, Target nascondeva i selettori e li mostrava solo in caso di corrispondenza di tutti i selettori. In at.js 0.9.2 Target mostra i selettori non appena corrispondono.

## at.js versione 0.9.1 {#section_DAFB99114D604CFB8416C1BC7DEEAEEE}

**Data:** 14 luglio 2016

* Fornisce a at.js un timeout per il servizio ID visitatore, indipendente dal timeout proprio del servizio.
* Corregge un problema in 0.9.0 che influenzava le implementazioni che usavano at.js su alcune pagine e mbox.js su altre.
* Se utilizzi Adobe Analytics come origine per la generazione di rapporti dell’attività e la versione 61 (o successiva) di mbox.js o la versione 0.9.1 (o successiva) di at.js, non è necessario specificare un server di tracciamento durante la creazione di attività. La libreria mbox.js o at.js invia automaticamente i valori del server di tracciamento a [!DNL Target]. Durante la creazione di attività, puoi lasciare vuoto il campo [!UICONTROL Server di tracciamento] nella pagina [!UICONTROL Obiettivi e impostazioni].

## at.js versione 0.9.0 {#section_2981CC9792F245389B39BB5B69F84C4E}

**Versione di Target:** 16.6.1

**Data:** 23 giugno 2016

* Corregge un problema di schermo bianco quando si utilizzano le offerte di Compositore esperienza visivo. Chiunque utilizzi [!DNL at.js] dovrebbe effettuare l’aggiornamento a questa nuova versione.
* Nuova API `registerExtension`.

   Questa nuova API fornisce agli sviluppatori l’accesso a determinati moduli jQuery utilizzati in [!DNL at.js] per sviluppare estensioni (plug-in) per la libreria. Ci sono alcune implicazioni per questo cambiamento. Questo impatta solo gli utenti che utilizzano le seguenti funzionalità:

   * L’API `getSettings()` è stata rimossa, ma la stessa funzionalità è disponibile utilizzando `registerExtension()`.
   * L’API `getTracking()` è stata rimossa, ma la stessa funzionalità è disponibile utilizzando `registerExtension()`.

   * Le estensioni esistenti (ad esempio le estensioni AngularJS) devono essere aggiornate per utilizzare l’approccio `registerExtension()`.

* Nuova API di notifica at.js.

   L'obiettivo di questo sistema di notifica è quello di fornire ulteriori informazioni su ciò che [!DNL at.js] sta facendo sulla pagina e quando si verificano dei problemi. Un problema comune riscontrato con Compositore esperienza visivo si verifica quando una nuova versione IT modifica la pagina, un selettore del compositore non funziona più correttamente e il test smette di consegnare correttamente il contenuto. Un obiettivo di questo sistema di notifica è quello di rendere noto alla pagina questo problema di consegna, così gli sviluppatori possono accedere a tali informazioni, passarle a un sistema come [!DNL Adobe Analytics] e avvisare i responsabili business che il loro test non ha funzionato.

* Nuovo metodo API `targetGlobalSettings()`.

   È possibile modificare le impostazioni nella libreria at.js anziché configurare le impostazioni nell’[!DNL Target Standard/Premium UI]o con le API REST.

## at.js versione 0.8.0 {#section_E1C7B08EC0494388A022C28A8B8FE807}

**Data:** 5 maggio 2016.

Questa è la prima versione ufficiale della libreria [!DNL at.js].

[!DNL at.js] è una nuova libreria di implementazione per [!DNL Target], progettata sia per le tipiche implementazioni web sia per le applicazioni a pagina singola.

[!DNL at.js] sostituisce [!DNL mbox.js] per le implementazioni di [!DNL Adobe Target].

>[!NOTE]
>
>Anche se [!DNL at.js] sostituisce [!DNL mbox.js], mbox.js continuerà a essere supportato. Tuttavia, per la maggior parte delle persone, [!DNL at.js] offre alcuni vantaggi in più rispetto a [!DNL mbox.js]. Questo ti dà il tempo di provare [!DNL at.js] e di cambiarne l’implementazione nelle pagine.

Ad esempio, [!DNL at.js] migliora i tempi di caricamento delle pagine per le implementazioni web, migliora la sicurezza e fornisce migliori opzioni di implementazione per le applicazioni a pagina singola.

La libreria [!DNL at.js] include anche i componenti inclusi in [!DNL target.js], quindi cessano le chiamate a [!DNL target.js].

Quando implementi [!DNL at.js], tieni presente quanto segue:

* Le versioni di Internet Explorer precedenti a 8 non sono supportate.
* L’implementazione asincrona potrebbe impedire il funzionamento delle integrazioni legacy come il plug-in [!DNL Test&Target] a [!DNL SiteCatalyst].
* [!DNL Target]I plug-in che fanno riferimento a oggetti e metodi non sono supportati.[!DNL mbox.js]
* Tutte le chiamate a [!DNL Target] vengono effettuate tramite XMLHTTPRequest e il contenuto viene restituito tramite JSON.
