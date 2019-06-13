---
description: Informazioni sull’implementazione di Adobe Target senza l’utilizzo di un sistema per la gestione dei tag (Adobe Launch o Dynamic Tag Management).
keywords: conferma d’ordine;orderConfirmPage
seo-description: Informazioni sull’implementazione di Adobe Target senza l’utilizzo di un sistema per la gestione dei tag (Adobe Launch o Dynamic Tag Management).
seo-title: Implementare Target senza un sistema per la gestione dei tag
solution: Target
subtopic: Introduzione
title: Implementare Target senza un sistema per la gestione dei tag
topic: Standard
uuid: 3ecc041a-42d8-40f8-90be-7856e1d3d080
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Implementare Target senza un sistema per la gestione dei tag{#implement-target-without-a-tag-manager}

Informazioni sull’implementazione di [!DNL Adobe Target] senza l’utilizzo di un sistema per la gestione dei tag (Adobe Launch o Dynamic Tag Management).

## Implementare Target senza un sistema per la gestione dei tag {#topic_397FFA3D6918456BBE02A9FBE9537894}

Informazioni sull’implementazione di Adobe Target senza l’utilizzo di un sistema per la gestione dei tag (Adobe Launch o Dynamic Tag Management).

>[!NOTE]
>
>[Adobe Launch](../../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) è il metodo preferito per l’implementazione di Target e della libreria at.js. Le seguenti informazioni non sono applicabili quando si utilizza Adobe Launch per implementare Target.

## Configurazioni at.js {#concept_2FA0456607D04F82B0539C5BF5309812}

Informazioni utili per scegliere diverse impostazioni nella pagina Impostazioni di at.js.

>[!NOTE]
>
>[Adobe Launch](../../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) è il metodo preferito per l’implementazione di Target e della libreria at.js. Le seguenti informazioni non sono applicabili quando si utilizza Adobe Launch per implementare Target.

>[!NOTE]
>
>È possibile modificare le impostazioni nella libreria at.js anziché configurare le impostazioni nell’interfaccia utente di Target Standard/Premium o con le API REST. Per ulteriori informazioni, consulta [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md).

Per aprire la pagina [!UICONTROL Impostazioni]:

1. Fai clic su **[!UICONTROL Configurazione]** &gt; **[!UICONTROL Implementazione]**.
1. Seleziona **[!UICONTROL at. js]** &gt; **[!UICONTROL Modifica impostazioni at.js]**.

## Impostazioni di erogazione contenuto {#section_118D290DFC444509AD8E4AE86C9D92C0}

Prima di cambiare queste impostazioni, rivolgiti all’Assistenza clienti. Queste impostazioni sono necessarie per la maggior parte delle implementazioni.

| Impostazione | Descrizione |
|--- |--- |
| Creazione automatica mbox globale | Seleziona se incorporare la chiamata mbox globale nel file at.js in modo che si attivi automaticamente al caricamento di ogni pagina.<br>La modifica di questa impostazione ha effetto sia su at.js che su mbox.js. |
| Nome mbox globale | Seleziona un nome per la mbox globale. Per impostazione predefinita, il nome è target-global-mbox.<br>Nei nomi delle mbox in at.js puoi usare caratteri speciali, tra cui il simbolo &amp;.<br>La modifica di questa impostazione ha effetto sia su at.js che su mbox.js. |

## Impostazioni avanzate {#section_33B697B77BA64A01B5939D7EC75231F2}

| Impostazione | Descrizione |
|--- |--- |
| Codice cliente | Il codice cliente è una sequenza di caratteri specifica del cliente spesso necessaria quando si utilizzano le API di Target.<br>Non è possibile modificare questa impostazione. |
| ID organizzazione IMS | Questo ID collega l’implementazione al tuo account [!DNL Adobe Experience Cloud].<br>Non è possibile modificare questa impostazione. |
| Durata del profilo | Questa impostazione determina per quanto tempo vengono memorizzati i profili visitatore. Per impostazione predefinita, i profili vengono memorizzati per due settimane. Questa operazione può essere prolungata fino a 90 giorni.<br>Per modificare l’impostazione della durata del profilo, contatta l’[assistenza al cliente](https://helpx.adobe.com/it/contact/enterprise-support.ec.html). |
| X-Domain | Determina se il browser imposta i cookie nel proprio dominio (cookie di prima parte), nel dominio di Target o entrambi.<br>La modifica di questa impostazione ha effetto sia su at.js che su mbox.js. |
| Timeout | Se [!DNL Target] non risponde con il contenuto entro il periodo definito, la chiamata al server riceve un timeout e viene visualizzato il contenuto predefinito. Durante la sessione del visitatore vengono ripetuti ulteriori tentativi di chiamata. Il valore predefinito è 5 secondi.<br>La modifica di questa impostazione ha effetto sia su at.js che su mbox.js.<br>La libreria at.js utilizza l’impostazione di timeout in `XMLHttpRequest`. Il timeout viene avviato quando parte la richiesta e si interrompe quando Target riceve una risposta dal server. Per ulteriori informazioni, consulta [XMLHttpRequest.timeout](https://developer.mozilla.org/it-IT/docs/Web/API/XMLHttpRequest/timeout) su Mozilla Developer Network.<br>Se il timeout specificato si verifica prima della ricezione della risposta, viene visualizzato il contenuto predefinito e il visitatore può essere conteggiato come partecipante a un’attività, poiché la raccolta dei dati viene eseguita sul server Edge di [!DNL Target]. Se la richiesta raggiunge il server Edge di [!DNL Target], il visitatore viene conteggiato.<br>Quando configuri l’impostazione di timeout, tieni presente quanto segue:<ul><li>Se il valore è troppo basso, gli utenti potrebbero visualizzare il contenuto predefinito la maggior parte delle volte, nonostante il visitatore venga conteggiato come partecipante all’attività.</li><li>Se il valore è troppo alto, i visitatori potrebbero visualizzare aree vuote nella pagina web o pagine vuote (se utilizzi la funzione per nascondere il corpo) per periodi di tempo prolungati.</li></ul>Per comprendere meglio i tempi di risposta della mbox, guarda la scheda Rete negli strumenti di sviluppo del tuo browser. Puoi anche utilizzare strumenti di terze parti per il monitoraggio delle prestazioni web, ad esempio Catchpoint.<br>**Nota**: l’impostazione [visitorApiTimeout](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) evita che [!DNL Target] attenda troppo a lungo la risposta dell’API visitatore. Questa impostazione e l’impostazione Timeout per at.js qui descritta non entrano in contrasto. |
| Supporto di browser legacy | **Nota**: l’opzione Supporto di browser legacy è disponibile nelle versioni 0.9.3 e precedenti di at.js. Questa opzione è stata rimossa in at.js versione 0.9.4. Per un elenco di browser supportati da at.js, consulta [Browser supportati](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md).<br>I browser legacy sono browser meno recenti che non supportano completamente la condivisione delle risorse tra diverse origini (Cross Origin Resource Sharing, CORS). Questi browser includono: Internet Explorer nelle versioni precedenti alla versione 11; Safari versione 6 e precedenti. Se il supporto di browser legacy è disattivato, Target non recapita i contenuti né conta i visitatori nei rapporti per questi browser. Se questa opzione è abilitata, si consiglia di eseguire test di controllo qualità su diversi browser più datati, per assicurarsi che sia possibile fornire agli utenti un’esperienza positiva. |

## Impostazioni codice {#section_D41C905D0F8149949F525C85F2CCFF7F}

| Impostazione | Descrizione |
|--- |--- |
| Intestazione libreria | Aggiungi un JavaScript personalizzato da includere nella parte superiore della libreria. |
| Piè di pagina libreria | Aggiungi un JavaScript personalizzato da includere nella parte inferiore della libreria. |

## Scaricare at.js {#concept_1E1F958F9CCC4E35AD97581EFAF659E2}

Istruzioni per scaricare la libreria utilizzando l’interfaccia di Target o l’API di download.

<!-- 

ov2/c_target-configure-atjs.xml

 -->

>[!NOTE]
>
>[Adobe Launch](../../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) è il metodo preferito per l’implementazione di Target e della libreria at.js. Le seguenti informazioni non sono applicabili quando si utilizza Adobe Launch per implementare Target.

>[!IMPORTANT]
>
>Il team di Target gestisce solo due versioni di [!DNL at.js], la versione corrente e quella immediatamente precedente. Aggiorna [!DNL at.js] per assicurarti di eseguire una versione supportata. Per ulteriori informazioni su ogni versione, consulta [Dettagli sulla versione di at.js](../../../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A).

## Scaricare at.js utilizzando l’interfaccia di Target {#section_1F5EE401C2314338910FC57F9592894E}

Per scaricare [!DNL at.js] dall&#39;interfaccia di [!DNL Target]:

1. Fai clic su **[!UICONTROL Configurazione]** &gt; **[!UICONTROL Implementazione]**.
1. Seleziona **[!UICONTROL at.js]**.
1. Fai clic su **[!UICONTROL Scarica at.js]**.

## Scaricare at.js utilizzando l’API di download di Target {#section_C0D9D2A9068144708D08526BA5CA10D0}

Per scaricare [!DNL at.js] utilizzando l&#39;API.

1. Ottieni il tuo codice cliente.

   Il codice cliente è disponibile nella parte superiore della pagina **[!UICONTROL Configurazione]** &gt; **[!UICONTROL Implementazione]** &gt; **[!UICONTROL Modifica impostazioni at.js]** dell’interfaccia di [!DNL Target].

1. Ottieni il tuo numero di amministratore.

   Carica l&#39;URL:

   ```
   https://admin.testandtarget.omniture.com/rest/v1/endpoint/<varname>client code</varname>
   ```

   Sostituisci il ` < *`codice cliente`*>` con il codice cliente ottenuto nel passaggio 1.

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
   https://admin<varname>admin number</varname>>.testandtarget.omniture.com/admin/rest/v1/libraries/atjs/download?client=<varname>client code </varname>version=<version number>
   ```

   * Sostituisci il ` < *`numero di amministratore`*>` con il tuo numero di amministratore.
   * Sostituisci il ` < *`codice cliente`*>` con il codice cliente ottenuto nel passaggio 1.
   * Sostituisci il ` < *`numero di versione`*>` con il [ numero di versione [!DNL at. js] ](../../../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A) desiderato (ad esempio, 1.6.2).
   >[!IMPORTANT]
   >
   >Il team di Target gestisce solo due versioni di [!DNL at.js], la versione corrente e quella immediatamente precedente. Aggiorna [!DNL at.js] per assicurarti di eseguire una versione supportata. Per ulteriori informazioni su ogni versione, consulta [Dettagli sulla versione di at.js](../../../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A).

   Il caricamento di questa URL avvia il download del file [!DNL at.js] personalizzato.

## Implementazione di at.js {#concept_03CFA86973A147839BEB48A06FEE5E5A}

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
* Preconnessione e Preacquisizione sono opzioni che potrebbero consentire di caricare più rapidamente le pagine Web. Se si utilizzano queste configurazioni, assicurarsi di sostituire `<client code>` con il proprio codice cliente, che si può ottenere dalla pagina **[!UICONTROL Configurazione]** &gt; **[!UICONTROL Implementazione]** &gt; **[!UICONTROL Modifica impostazioni at.js]**.
* Se si dispone di un livello di dati, è ottimale definirlo il più possibile nel `<head>` delle pagine prima di caricare at.js. Questo posizionamento offre la massima capacità di sfruttare queste informazioni in Target per la personalizzazione.
* Funzioni speciali di Target, come ad esempio `targetPageParams()`, `targetPageParamsAll()`, Data Providers e `targetGlobalSettings()` devono essere definite dopo il livello di dati e prima di caricare at.js. In alternativa, possono venire salvate nella sezione [!UICONTROL Intestazione libreria] della pagina [!UICONTROL Modifica impostazioni at.js] e salvate come parte della libreria at.js stessa. Per ulteriori informazioni su queste funzioni, vedi [Funzioni di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md).
* Se si utilizzano librerie di supporto di JavaScript, come ad esempio jQuery, includerle prima di Target così da poterne sfruttare la sintassi e i metodi durante la creazione di esperienze Target.
* Includere at.js nei `<head>` delle pagine.

## Tracciare le conversioni {#task_E85D2F64FEB84201A594F2288FABF053}

Con la mbox di conferma dell’ordine è possibile registrare i dettagli sugli ordini sul sito e generare rapporti in base a ricavi e ordini. Con la mbox di conferma dell’ordine è inoltre possibile determinare algoritmi per i consigli, come “Persone che hanno acquistato il prodotto x hanno acquistato anche il prodotto y”.

<!-- 

ov/t_create_orderconfirm-page-mbox-atjs.xml

 -->

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