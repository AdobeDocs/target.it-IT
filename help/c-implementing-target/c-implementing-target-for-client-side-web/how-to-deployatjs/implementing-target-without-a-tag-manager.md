---
keywords: implementare target;implementazione;implementare at.js;tag manager;decisionale su dispositivo;nelle decisioni sui dispositivi
description: Scopri come specificare le impostazioni (dettagli account, metodi di implementazione, ecc.) per implementare la libreria at.js di Adobe Target senza utilizzare un gestore di tag.
title: Posso implementare Target senza un Tag Manager?
feature: Implement Server-side
role: Developer
exl-id: cb57f6b8-43cb-485d-a7ea-12db8170013f
translation-type: tm+mt
source-git-commit: 20337e6e54108502b6397c73580b898cc91ebd9b
workflow-type: tm+mt
source-wordcount: '1697'
ht-degree: 52%

---

# Implementare Target senza un sistema per la gestione dei tag

Informazioni sull&#39;implementazione di [!DNL Adobe Target] senza l&#39;utilizzo di un gestore di tag ([!DNL Adobe Experience Platform Launch] o [!DNL Dynamic Tag Manager]).

>[!NOTE]
>
>[Adobe Experience Platform ](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) Launch è il metodo preferito per l’implementazione di Target e della libreria at.js. Le informazioni seguenti non sono applicabili quando si utilizza Adobe Platform launch per implementare Target.

Per accedere alla pagina [!UICONTROL Implementazione], fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]**.

In questa pagina puoi specificare le seguenti impostazioni:

* Dettagli account
* Metodi di implementazione
* API del profilo
* Strumenti di debug
* Privacy

>[!NOTE]
>
>È possibile modificare le impostazioni nella libreria at.js anziché configurare le impostazioni nell’interfaccia utente di Target Standard/Premium o con le API REST. Per ulteriori informazioni, consulta [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md).

## Dettagli account

Puoi visualizzare i seguenti dettagli account. Impossibile modificare queste impostazioni.

| Impostazione | Descrizione |
| --- | --- |
| [!UICONTROL Codice client] | Il codice cliente è una sequenza di caratteri specifica del cliente spesso necessaria quando si utilizzano le API di Target. |
| [!UICONTROL ID organizzazione IMS] | Questo ID collega l’implementazione al tuo account [!DNL Adobe Experience Cloud]. |
| [!UICONTROL Decisioning su dispositivo] | Per abilitare le decisioni sul dispositivo, sposta l’interruttore nella posizione &quot;on&quot;.<br>Le decisioni sul dispositivo consentono di memorizzare nella cache le campagne A/B e Experience Targeting (XT) sul server ed eseguire le decisioni in memoria a latenza vicina allo zero. Per ulteriori informazioni, consulta [Introduzione alle decisioni sui dispositivi](https://adobetarget-sdks.gitbook.io/docs/on-device-decisioning/introduction-to-on-device-decisioning) nella guida *SDK per Adobe Target* . |
| [!UICONTROL Include nell&#39;artefatto tutte le attività qualificate per le decisioni sul dispositivo esistenti.] | (Condizionale) Questa opzione viene visualizzata se abiliti le decisioni sul dispositivo.<br>Fai scorrere l’interruttore nella posizione &quot;attivato&quot; se desideri che tutte le attività di Target live idonee per le decisioni sul dispositivo siano incluse automaticamente nell’artefatto.<br>Se questa opzione è disattivata, è necessario ricreare e attivare tutte le attività di decisione sul dispositivo per includerle nell’artefatto delle regole generato. |

## Metodi di implementazione

Le seguenti impostazioni possono essere configurate nel pannello Metodi di implementazione :

### Impostazioni globali

>[!NOTE]
>
>Queste impostazioni vengono applicate a tutte le librerie [!DNL Target] .js . Dopo aver eseguito le modifiche nella sezione Metodi di implementazione , devi scaricare la libreria e aggiornarla nell’implementazione.

| Impostazione | Descrizione |
| --- | --- |
| Caricamento pagina abilitato (Creazione automatica mbox globale) | Seleziona se incorporare la chiamata mbox globale nel file at.js in modo che si attivi automaticamente al caricamento di ogni pagina. |
| Mbox globale | Seleziona un nome per la mbox globale. Per impostazione predefinita, il nome è target-global-mbox.<br>Nei nomi delle mbox in at.js puoi usare caratteri speciali, tra cui il simbolo &amp;. |
| Timeout (secondi) | Se [!DNL Target] non risponde con il contenuto entro il periodo definito, la chiamata al server riceve un timeout e viene visualizzato il contenuto predefinito. Durante la sessione del visitatore vengono ripetuti ulteriori tentativi di chiamata. Il valore predefinito è 5 secondi.<br>La libreria at.js utilizza l’impostazione di timeout in `XMLHttpRequest`. Il timeout viene avviato quando parte la richiesta e si interrompe quando [!DNL Target] riceve una risposta dal server. Per ulteriori informazioni, consulta [XMLHttpRequest.timeout](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/timeout) in Mozilla Developer Network.<br>Se il timeout specificato si verifica prima della ricezione della risposta, viene visualizzato il contenuto predefinito e il visitatore può essere conteggiato come partecipante a un’attività, poiché la raccolta dei dati viene eseguita sul server Edge di [!DNL Target]. Se la richiesta raggiunge il server Edge di [!DNL Target], il visitatore viene conteggiato.<br>Quando configuri l’impostazione di timeout, tieni presente quanto segue:<ul><li>Se il valore è troppo basso, gli utenti potrebbero visualizzare il contenuto predefinito la maggior parte delle volte, nonostante il visitatore venga conteggiato come partecipante all’attività.</li><li>Se il valore è troppo alto, i visitatori potrebbero visualizzare aree vuote nella pagina web o pagine vuote (se utilizzi la funzione per nascondere il corpo) per periodi di tempo prolungati.</li></ul>Per comprendere meglio i tempi di risposta della mbox, guarda la scheda Rete negli strumenti di sviluppo del tuo browser. Puoi anche utilizzare strumenti di terze parti per il monitoraggio delle prestazioni web, ad esempio Catchpoint.<br>**Nota**: l’impostazione [visitorApiTimeout](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) evita che [!DNL Target] attenda troppo a lungo la risposta dell’API visitatore. Questa impostazione e l’impostazione Timeout per at.js qui descritta non entrano in contrasto. |
| Durata del profilo | Questa impostazione determina per quanto tempo vengono memorizzati i profili visitatore. Per impostazione predefinita, i profili vengono memorizzati per due settimane. Questa impostazione può essere aumentata fino a 90 giorni.<br>Per modificare l’impostazione Durata del profilo, contatta l’[Assistenza clienti](https://helpx.adobe.com/it/contact/enterprise-support.ec.html). |

### Metodo di implementazione principale

>[!IMPORTANT]
>
>Il team di Target supporta entrambi at.js 1.*x* e at.js 2.*x*. Esegui l’aggiornamento più recente di una delle versioni principali di at.js per assicurarti di eseguire una versione supportata.

Per scaricare la versione at.js desiderata, fai clic sul pulsante **[!UICONTROL Scarica]** appropriato.

Per modificare le impostazioni di at.js, fai clic su **[!UICONTROL Modifica]** accanto alla versione at.js desiderata.

>[!IMPORTANT]
>
>Prima di modificare queste impostazioni predefinite, consulta l’ [Assistenza clienti](/help/cmp-resources-and-contact-information.md) in modo da non influenzare l’implementazione corrente.

Oltre alle impostazioni precedentemente illustrate, sono disponibili anche le seguenti impostazioni specifiche di at.js:

| Impostazione | Descrizione |
|--- |--- |
| Intestazione libreria personalizzata | Aggiungi un JavaScript personalizzato da includere nella parte superiore della libreria. |
| Piè di pagina libreria personalizzato | Aggiungi un JavaScript personalizzato da includere nella parte inferiore della libreria. |

### API del profilo

Puoi abilitare o disabilitare l’autenticazione per gli aggiornamenti collettivi tramite API e generare un token di autenticazione del profilo.

Per ulteriori informazioni, consulta [Impostazioni API del profilo](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/profile-api-settings.md).

### Strumenti di debug

Genera un token di autorizzazione per utilizzare gli strumenti di debug [!DNL Target] avanzati. Fai clic su **[!UICONTROL Genera nuovo token di autenticazione]**.

![Genera nuovo token di autenticazione](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/assets/debugger-auth-token.png)

### Privacy

Queste impostazioni ti consentono di utilizzare [!DNL Target] in conformità alle leggi sulla privacy dei dati applicabili.

Scegli l’impostazione desiderata dall’elenco a discesa Indirizzo IP visitatore offuscato :

* Ultima offuscamento dell&#39;ottetto
* Intera offuscamento dell’IP
* None (Nessuno)

Per ulteriori informazioni, consulta [Privacy](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md).

>[!NOTE]
>
>L’opzione Supporto di browser legacy era disponibile nelle versioni 0.9.3 e precedenti di at.js . Questa opzione è stata rimossa in at.js versione 0.9.4. Per un elenco di browser supportati da at.js, consulta [Browser supportati](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md).<br>I browser legacy sono browser meno recenti che non supportano completamente la condivisione delle risorse tra diverse origini (Cross Origin Resource Sharing, CORS). Questi browser includono: Internet Explorer nelle versioni precedenti alla versione 11; Safari versione 6 e precedenti. Se il supporto del browser legacy è stato disabilitato, Target non distribuiva contenuti o contava i visitatori nei rapporti su questi browser. Se questa opzione è stata abilitata, si consiglia di eseguire il controllo qualità tra i browser più datati per garantire una buona esperienza del cliente.

## Scaricare at.js {#concept_1E1F958F9CCC4E35AD97581EFAF659E2}

Istruzioni per scaricare la libreria utilizzando l&#39;interfaccia [!DNL Target] o l&#39;API di download.

>[!NOTE]
>
>* [Adobe Experience Platform ](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) Launch è il metodo preferito per l’implementazione di Target e della libreria at.js. Le informazioni seguenti non sono applicabili quando si utilizza Adobe Platform launch per implementare Target.
   >
   >
* Il team di Target supporta entrambi at.js 1.*x* e at.js 2.*x*. Esegui l’aggiornamento più recente di una delle versioni principali di at.js per assicurarti di eseguire una versione supportata. Per ulteriori informazioni su ogni versione, consulta [Dettagli sulla versione di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A).


### Scaricare at.js utilizzando l’interfaccia di Target {#section_1F5EE401C2314338910FC57F9592894E}

Per scaricare [!DNL at.js] dall&#39;interfaccia di [!DNL Target]:

1. Fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]**.
1. Nella sezione [!UICONTROL Metodi di implementazione] , fai clic sul pulsante **[!UICONTROL Scarica]** accanto alla versione at.js desiderata.

### Scaricare at.js utilizzando l’API di download di Target {#section_C0D9D2A9068144708D08526BA5CA10D0}

Per scaricare [!DNL at.js] utilizzando l&#39;API.

1. Ottieni il tuo codice cliente.

   Il codice cliente è disponibile nella parte superiore della pagina **[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]** dell&#39;interfaccia [!DNL Target].

1. Ottieni il tuo numero di amministratore.

   Carica l&#39;URL:

   ```
   https://admin.testandtarget.omniture.com/rest/v1/endpoint/<varname>client code</varname>
   ```

   Sostituisci `client code` con il codice client del passaggio 1.

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

   * Sostituisci `admin number` con il tuo numero di amministratore.
   * Sostituisci `client code` con il codice client del passaggio 1.
   * Sostituisci `version number` con il numero di versione desiderato di at.js (ad esempio, 2.2).

   >[!IMPORTANT]
   >
   >Il team di Target gestisce solo due versioni di [!DNL at.js], la versione corrente e quella immediatamente precedente. Aggiorna [!DNL at.js] per assicurarti di eseguire una versione supportata. Per ulteriori informazioni su ogni versione, consulta [Dettagli sulla versione di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A).

   Il caricamento di questa URL avvia il download del file [!DNL at.js] personalizzato.

## Implementazione at.js {#concept_03CFA86973A147839BEB48A06FEE5E5A}

at.js dovrebbe essere implementato nell’elemento `<head>` di ogni pagina del sito Web.

Un&#39;implementazione tipica di Target che non utilizza un gestore di tag come [Platform launch di Adobi](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) o [Dynamic Tag Management](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-using-dynamic-tag-management.md#concept_3A40AF6FFC0E4FD2AA81B303A79D0B96) si presenta così:

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

* Deve essere utilizzato il doctype HTML5 (ad esempio, `<!doctype html>`). I doctype non supportati o meno recenti potrebbero impedire a Target di effettuare una richiesta.
* Preconnessione e Preacquisizione sono opzioni che potrebbero consentire di caricare più rapidamente le pagine Web. Se si utilizzano queste configurazioni, assicurarsi di sostituire `<client code>` con il proprio codice cliente, che è possibile ottenere dalla pagina **[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione].
* Se si dispone di un livello di dati, è ottimale definirlo il più possibile nel `<head>` delle pagine prima di caricare at.js. Questo posizionamento offre la massima capacità di utilizzare queste informazioni in Target per la personalizzazione.
* Funzioni speciali di Target, come ad esempio `targetPageParams()`, `targetPageParamsAll()`, Data Providers e `targetGlobalSettings()` devono essere definite dopo il livello di dati e prima di caricare at.js. In alternativa, queste funzioni possono essere salvate nella sezione [!UICONTROL Intestazione libreria] della pagina [!UICONTROL Modifica impostazioni at.js] e salvate come parte della libreria at.js stessa. Per ulteriori informazioni su queste funzioni, vedi [Funzioni di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md).
* Se utilizzi librerie di supporto JavaScript, come jQuery, includerle prima di Target in modo da poterne utilizzare la sintassi e i metodi durante la creazione di esperienze Target.
* Includere at.js nei `<head>` delle pagine.

## Tracciare le conversioni {#task_E85D2F64FEB84201A594F2288FABF053}

Con la mbox di conferma dell’ordine è possibile registrare i dettagli sugli ordini sul sito e generare rapporti in base a ricavi e ordini. Con la mbox di conferma dell’ordine è inoltre possibile determinare algoritmi per i consigli, come “Persone che hanno acquistato il prodotto x hanno acquistato anche il prodotto y”.

>[!NOTE]
>
>Se gli utenti effettuano acquisti sul tuo sito web, Adobe consiglia di implementare una mbox di conferma d’ordine anche se per generare rapporti utilizzi Analytics for Target (A4T).

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
