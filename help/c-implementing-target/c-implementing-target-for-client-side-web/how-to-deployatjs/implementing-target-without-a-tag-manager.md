---
keywords: implement target;implementation;implement at.js;tag manager
description: Informazioni sull’implementazione di Adobe Target senza l’utilizzo di un sistema per la gestione dei tag (Adobe Launch o Dynamic Tag Management).
title: Implementare Target senza un sistema per la gestione dei tag
feature: null
subtopic: Getting Started
topic: Standard
uuid: 3ecc041a-42d8-40f8-90be-7856e1d3d080
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '1537'
ht-degree: 66%

---


# Implementare Target senza un sistema per la gestione dei tag{#implement-target-without-a-tag-manager}

Information about implementing [!DNL Adobe Target] without using a tag manager ([!DNL Adobe Launch] or [!DNL Dynamic Tag Manager]).

>[!NOTE]
>
>[Adobe Launch](../../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) è il metodo preferito per l’implementazione di Target e della libreria at.js. Le seguenti informazioni non sono applicabili quando si utilizza Adobe Launch per implementare Target.

Per accedere alla pagina [!UICONTROL Implementazione] , fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]**.

In questa pagina potete specificare le seguenti impostazioni:

* Dettagli account
* Metodi di implementazione
* API profilo
* Strumenti debugger
* Privacy

>[!NOTE]
>
>È possibile modificare le impostazioni nella libreria at.js anziché configurare le impostazioni nell’interfaccia utente di Target Standard/Premium o con le API REST. Per ulteriori informazioni, consulta [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md).

## Dettagli account

Potete visualizzare i seguenti dettagli account. Queste impostazioni non possono essere modificate.

| Impostazione | Descrizione |
| --- | --- |
| Codice cliente | Il codice cliente è una sequenza di caratteri specifica del cliente spesso necessaria quando si utilizzano le API di Target. |
| ID organizzazione IMS | Questo ID collega l’implementazione al tuo account [!DNL Adobe Experience Cloud]. |

## Metodi di implementazione

Le seguenti impostazioni possono essere configurate nel pannello Metodi di implementazione:

### Impostazioni globali

>[!NOTE]
>
>Queste impostazioni vengono applicate a tutte le librerie [!DNL Target] .js. Dopo aver apportato le modifiche nella sezione Metodi [!UICONTROL di] implementazione è necessario scaricare la libreria e aggiornarla nell&#39;implementazione.

|Caricamento pagina abilitato (creazione automatica di mbox globale|Specifica se incorporare la chiamata mbox globale nel file at.js per attivare automaticamente il caricamento di ogni pagina.|
|Mbox globale|Selezionate un nome per la mbox globale. Per impostazione predefinita, il nome è target-global-mbox.<br>Nei nomi delle mbox in at.js puoi usare caratteri speciali, tra cui il simbolo &amp;.|
|Timeout (seconds)|If [!DNL Target] does not respond with content within the defined period, the server call times out and default content is displayed. Durante la sessione del visitatore vengono ripetuti ulteriori tentativi di chiamata. Il valore predefinito è 5 secondi.<br>La libreria at.js utilizza l’impostazione di timeout in `XMLHttpRequest`. Il timeout viene avviato quando parte la richiesta e si interrompe quando [!DNL Target] riceve una risposta dal server. Per ulteriori informazioni, consulta [XMLHttpRequest.timeout](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/timeout) in Mozilla Developer Network.<br>Se il timeout specificato si verifica prima della ricezione della risposta, viene visualizzato il contenuto predefinito e il visitatore può essere conteggiato come partecipante a un’attività, poiché la raccolta dei dati viene eseguita sul server Edge di [!DNL Target]. Se la richiesta raggiunge il server Edge di [!DNL Target], il visitatore viene conteggiato.<br>Quando configuri l’impostazione di timeout, tieni presente quanto segue:<ul><li>Se il valore è troppo basso, gli utenti potrebbero visualizzare il contenuto predefinito la maggior parte delle volte, nonostante il visitatore venga conteggiato come partecipante all’attività.</li><li>Se il valore è troppo alto, i visitatori potrebbero visualizzare aree vuote nella pagina web o pagine vuote (se utilizzi la funzione per nascondere il corpo) per periodi di tempo prolungati.</li></ul>Per comprendere meglio i tempi di risposta della mbox, guarda la scheda Rete negli strumenti di sviluppo del tuo browser. Puoi anche utilizzare strumenti di terze parti per il monitoraggio delle prestazioni web, ad esempio Catchpoint.<br>**Nota **: l’impostazione[visitorApiTimeout](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md)evita che[!DNL Target]attenda troppo a lungo la risposta dell’API visitatore. Questa impostazione e l’impostazione Timeout per at.js qui descritta non entrano in contrasto.|
|Durata profilo|Questa impostazione determina per quanto tempo vengono memorizzati i profili dei visitatori. Per impostazione predefinita, i profili vengono memorizzati per due settimane. Questa operazione può essere prolungata fino a 90 giorni.<br>Per modificare l’impostazione Durata del profilo, contatta l’[Assistenza clienti](https://helpx.adobe.com/it/contact/enterprise-support.ec.html).|

### Metodo di implementazione principale

>[!IMPORTANT]
>
>Il team Target supporta entrambi at.js 1.*x* e at.js 2.*x*. Esegui l&#39;aggiornamento all&#39;aggiornamento più recente di una delle versioni principali di at.js per assicurarti che sia in esecuzione una versione supportata.

Per scaricare la versione at.js desiderata, fate clic sul pulsante **[!UICONTROL Scarica]** appropriato.

Per modificare le impostazioni at.js, fate clic su **[!UICONTROL Modifica]** accanto alla versione at.js desiderata.

>[!IMPORTANT]
>
>Prima di modificare queste impostazioni predefinite, consulta [Client Care](/help/cmp-resources-and-contact-information.md) per non influenzare l&#39;implementazione corrente.

Oltre alle impostazioni descritte in precedenza, sono disponibili anche le seguenti impostazioni at.js specifiche:

| Impostazione | Descrizione |
|--- |--- |
| Intestazione libreria personalizzata | Aggiungi un JavaScript personalizzato da includere nella parte superiore della libreria. |
| Piè di pagina libreria personalizzata | Aggiungi un JavaScript personalizzato da includere nella parte inferiore della libreria. |

### API profilo

Puoi abilitare o disabilitare l’autenticazione per gli aggiornamenti collettivi tramite API e generare un token di autenticazione del profilo.

For more information, see [Profile API settings](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/profile-api-settings.md).

### Strumenti debugger

Generare un token di autorizzazione per utilizzare strumenti [!DNL Target] di debug avanzati. Click **[!UICONTROL Generate New Authentication Token]**.

![Genera nuovo token di autenticazione](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/assets/debugger-auth-token.png)

### Privacy

Queste impostazioni consentono di utilizzare [!DNL Target] in conformità alle leggi sulla privacy dei dati.

Scegli l&#39;impostazione desiderata dall&#39;elenco a discesa Indirizzo IP visitatore offuscato:

* Ultima offuscamento ottetto
* Intera offuscamento IP
* None (Nessuno)

Per ulteriori informazioni, consulta [Privacy](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md).

>[!NOTE]
>
>L&#39;opzione Supporto browser legacy era disponibile in at.js versione 0.9.3 e precedenti. Questa opzione è stata rimossa in at.js versione 0.9.4. Per un elenco di browser supportati da at.js, consulta [Browser supportati](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md).<br>I browser legacy sono browser meno recenti che non supportano completamente la condivisione delle risorse tra diverse origini (Cross Origin Resource Sharing, CORS). Questi browser includono: Internet Explorer nelle versioni precedenti alla versione 11; Safari versione 6 e precedenti. Se l&#39;opzione Supporto browser legacy è stata disabilitata, Target non distribuiva il contenuto o non contava i visitatori nei rapporti su questi browser. Se questa opzione è stata attivata, si consiglia di garantire la qualità tra i browser più datati per garantire una buona esperienza cliente.

## Scaricare at.js {#concept_1E1F958F9CCC4E35AD97581EFAF659E2}

Instructions to download the library using the [!DNL Target] interface or the Download API.

>[!NOTE]
>
>* [Adobe Launch](../../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) è il metodo preferito per l’implementazione di Target e della libreria at.js. Le seguenti informazioni non sono applicabili quando si utilizza Adobe Launch per implementare Target.
   >
   >
* Il team Target supporta entrambi at.js 1.*x* e at.js 2.*x*. Esegui l&#39;aggiornamento all&#39;aggiornamento più recente di una delle versioni principali di at.js per assicurarti che sia in esecuzione una versione supportata. Per ulteriori informazioni su ogni versione, consulta [Dettagli sulla versione di at.js](../../../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A).


### Download at.js using the Target interface {#section_1F5EE401C2314338910FC57F9592894E}

Per scaricare [!DNL at.js] dall&#39;interfaccia di [!DNL Target]:

1. Fate clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]**.
1. Nella sezione Metodi [!UICONTROL di] implementazione, fate clic sul pulsante **[!UICONTROL Scarica]** accanto alla versione at.js desiderata.

### Download at.js using the Target Download API {#section_C0D9D2A9068144708D08526BA5CA10D0}

Per scaricare [!DNL at.js] utilizzando l&#39;API.

1. Ottieni il tuo codice cliente.

   Your client code is available at the top of the **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** page of the [!DNL Target] interface.

1. Ottieni il tuo numero di amministratore.

   Carica l&#39;URL:

   ```
   https://admin.testandtarget.omniture.com/rest/v1/endpoint/<varname>client code</varname>
   ```

   Replace `client code` with the client code from Step 1.

   Il risultato del caricamento dell&#39;URL deve essere simile al seguente:

   ```
   { 
     "api": "https://admin6.testandtarget.omniture.com/admin/rest/v1" 
   }
   ```

   In questo esempio, “6” è il numero di amministratore.

1. Scarica [!DNL at.js].

   Caricare questa URL con la seguente struttura:

   ```
   https://admin<varname>admin number</varname>.testandtarget.omniture.com/admin/rest/v1/libraries/atjs/download?client=<varname>client code</varname>&version=<version number>
   ```

   * Replace `admin number` with your admin number.
   * Replace `client code` with the client code from Step 1.
   * Replace `version number` with the desired at.js version number (for example, 2.2).

   >[!IMPORTANT]
   >
   >Il team di Target gestisce solo due versioni di [!DNL at.js], la versione corrente e quella immediatamente precedente. Aggiorna [!DNL at.js] per assicurarti di eseguire una versione supportata. Per ulteriori informazioni su ogni versione, consulta [Dettagli sulla versione di at.js](../../../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A).

   Il caricamento di questa URL avvia il download del file [!DNL at.js] personalizzato.

## at.js implementation {#concept_03CFA86973A147839BEB48A06FEE5E5A}

at.js dovrebbe essere implementato nell’elemento `<head>` di ogni pagina del sito Web.

Un’implementazione tipica di Target che non utilizza un gestore di tag come [Adobe Launch](../../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) o [Dynamic Tag Management](../../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-using-dynamic-tag-management.md#concept_3A40AF6FFC0E4FD2AA81B303A79D0B96) ha un aspetto simile al seguente:

```
<!doctype html> 
<html> 
 
<head> 
    <meta charset="utf-8"> 
    <title>Title of the Page</title> 
    <!--Preconnect and DNS-Prefetch to improve page load time--> 
    <link rel="preconnect" href="//<client code>.tt.omtrdc.net"> 
    <link rel="dns-prefetch" href="//<client code>.tt.omtrdc.net"> 
    <!--/Preconnect and DNS-Prefetch--> 
    <!--Data Layer to enable rich data collection and targeting--> 
    <script> 
        var digitalData = { 
            "page": { 
                "pageInfo": { 
                    "pageName": "Home" 
                } 
            } 
        }; 
    </script> 
    <!--/Data Layer--> 
    <!-- targetPageParams(), targetPageParamsAll(), Data Providers or targetGlobalSettings() functions to enrich the visitor profile or modify the library settings--> 
    <script> 
        targetPageParams = function() { 
            return { 
                "a": 1, 
                "b": 2, 
                "pageName": digitalData.page.pageInfo.pageName, 
                "profile": { 
                    "age": 26, 
                    "country": { 
                        "city": "San Francisco" 
                    } 
                } 
            }; 
        }; 
    </script> 
    <!--/targetPageParams()--> 
 
    <!--jQuery or other helper libraries should be implemented before at.js if you would like to use their methods in Target--> 
    <script src="jquery-3.3.1.min.js"></script> 
    <!--/jQuery--> 
    <!--Target's JavaScript SDK, at.js--> 
    <script src="at.js"></script> 
    <!--/at.js--> 
</head> 
 
<body> 
    The default content of the page 
</body> 
 
</html>
```

Considera le seguenti note importanti:

* Deve essere utilizzato il tipo di documento HTML5 (ad esempio, `<!doctype html>`). I doctype non supportati o meno recenti potrebbero impedire a Target di effettuare una richiesta.
* Preconnessione e Preacquisizione sono opzioni che potrebbero consentire di caricare più rapidamente le pagine Web. If you use these configurations, ensure that you replace `<client code>` with your own client code, which you can obtain from the **[!UICONTROL Administration]** > **[!UICONTROL Implementation] page.
* Se si dispone di un livello di dati, è ottimale definirlo il più possibile nel `<head>` delle pagine prima di caricare at.js. Questo posizionamento offre la massima capacità di sfruttare queste informazioni in Target per la personalizzazione.
* Funzioni speciali di Target, come ad esempio `targetPageParams()`, `targetPageParamsAll()`, Data Providers e `targetGlobalSettings()` devono essere definite dopo il livello di dati e prima di caricare at.js. In alternativa, possono venire salvate nella sezione [!UICONTROL Intestazione libreria] della pagina [!UICONTROL Modifica impostazioni at.js] e salvate come parte della libreria at.js stessa. Per ulteriori informazioni su queste funzioni, vedi [Funzioni di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md).
* Se si utilizzano librerie di supporto di JavaScript, come ad esempio jQuery, includerle prima di Target così da poterne sfruttare la sintassi e i metodi durante la creazione di esperienze Target.
* Includere at.js nei `<head>` delle pagine.

## Track conversions {#task_E85D2F64FEB84201A594F2288FABF053}

Con la mbox di conferma dell’ordine è possibile registrare i dettagli sugli ordini sul sito e generare rapporti in base a ricavi e ordini. Con la mbox di conferma dell’ordine è inoltre possibile determinare algoritmi per i consigli, come “Persone che hanno acquistato il prodotto x hanno acquistato anche il prodotto y”.

>[!NOTE]
>
>Se gli utenti effettuano acquisti sul tuo sito web, ti consigliamo di implementare una mbox di conferma d’ordine anche se per generare rapporti usi Analytics for Target (A4T).

1. Nella pagina dei dettagli dell’ordine, inserisci lo script mbox secondo il modello indicato di seguito.
1. Sostituisci le parole in lettere maiuscole con valori dinamici o statici provenienti dal catalogo.

   >[!NOTE]
   >
   >Utilizza le virgole per separare i diversi ID prodotto.

   **Suggerimento:** è possibile, inoltre, passare le informazioni di ordine in qualsiasi mbox (non deve per forza chiamarsi `orderConfirmPage`). Inoltre, puoi passare le informazioni di ordine in più mbox all&#39;interno della stessa campagna.

   ```
   <script type="text/javascript"> 
   adobe.target.trackEvent({ 
       "mbox": "orderConfirmPage", 
       "params":{  
           "orderId": "ORDER ID FROM YOUR ORDER PAGE",  
           "orderTotal": "ORDER TOTAL FROM YOUR ORDER PAGE",  
           "productPurchasedId": "PRODUCT ID FROM YOUR ORDER PAGE, PRODUCT ID2, PRODUCT ID3"  
       } 
   }); 
   </script> 
   ```

La mbox di conferma d&#39;ordine utilizza i seguenti parametri:

| Parametro | Descrizione |
|--- |--- |
| orderId | Valore univoco per identificare un ordine per il conteggio di conversione.<br>L’`orderId` deve essere univoco. Gli ordini duplicati vengono ignorati nei rapporti. |
| orderTotal | Valore monetario dell&#39;acquisto.<br>Non trasmettere il simbolo di valuta. Utilizza un punto decimale (non la virgola) per indicare i valori decimali. |
| productPurchasedId  (facoltativo) | Elenco degli ID dei prodotti acquistati nell&#39;ordine, separati da virgole.<br>Questi ID prodotto vengono visualizzati nel rapporto di revisione per supportare attività aggiuntive di analisi dei rapporti. |