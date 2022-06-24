---
keywords: implementare target;implementazione;implementare at.js;tag manager;decisionale su dispositivo;nelle decisioni sui dispositivi
description: Scopri come specificare le impostazioni (dettagli account, metodi di implementazione, ecc.) per implementare l’Adobe [!DNL Target] libreria at.js senza utilizzare un gestore di tag.
title: Posso Implementare? [!DNL Target] senza un Tag Manager?
feature: Implement Server-side
role: Developer
exl-id: cb57f6b8-43cb-485d-a7ea-12db8170013f
source-git-commit: 719eb95049dad3bee5925dff794871cd65969f79
workflow-type: tm+mt
source-wordcount: '1848'
ht-degree: 43%

---

# Implementare [!DNL Target] senza un gestore di tag

Informazioni sull’implementazione [!DNL Adobe Target] senza utilizzare un gestore di tag o tag in [!DNL Adobe Experience Platform].

>[!NOTE]
>
>Tag in [Adobe Experience Platform](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-using-adobe-launch/){target=_blank} è il metodo preferito per l&#39;implementazione [!DNL Target] e la libreria at.js. Le seguenti informazioni non sono applicabili quando si utilizzano tag in [!DNL Adobe Experience Platform] implementare [!DNL Target].

Per accedere al [!UICONTROL Implementazione] pagina, fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]**.

In questa pagina puoi specificare le seguenti impostazioni:

* Dettagli account
* Metodi di implementazione
* API del profilo
* Strumenti di debug
* Privacy

>[!NOTE]
>
>È possibile modificare le impostazioni nella libreria at.js anziché configurare le impostazioni nell’[!DNL Target Standard/Premium]interfaccia utente di   o con le API REST. Per ulteriori informazioni, consulta [targetGlobalSettings()](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/){target=_blank}.

## Dettagli account

Puoi visualizzare i seguenti dettagli account. Impossibile modificare queste impostazioni.

| Impostazione | Descrizione |
| --- | --- |
| [!UICONTROL Codice client] | Il codice cliente è una sequenza di caratteri specifica del cliente spesso necessaria quando si utilizzano le API di [!DNL Target]. |
| [!UICONTROL ID organizzazione IMS] | Questo ID collega l’implementazione al tuo account [!DNL Adobe Experience Cloud]. |
| [!UICONTROL Decisioning su dispositivo] | Per abilitare le decisioni sul dispositivo, sposta l’interruttore nella posizione &quot;on&quot;.<br>Le decisioni sul dispositivo consentono di memorizzare nella cache I/B e [!UICONTROL Targeting esperienza] (XT) campagne sul server ed esegui decisioni in memoria a latenza quasi zero. Per ulteriori informazioni, consulta [Introduzione alle decisioni sul dispositivo](https://developer.adobe.com/target/implement/server-side/sdk-guides/on-device-decisioning/){target=_blank} nel *[!DNL Adobe Target]SDK* guida. |
| [!UICONTROL Include nell&#39;artefatto tutte le attività qualificate per le decisioni sul dispositivo esistenti.] | (Condizionale) Questa opzione viene visualizzata se abiliti le decisioni sul dispositivo.<br>Fai scorrere l’interruttore nella posizione &quot;attivato&quot; se desideri che tutte le attività di Target live idonee per le decisioni sul dispositivo siano incluse automaticamente nell’artefatto.<br>Se questa opzione è disattivata, è necessario ricreare e attivare tutte le attività di decisione sul dispositivo per includerle nell’artefatto delle regole generato. |

## Metodi di implementazione

Le seguenti impostazioni possono essere configurate nel pannello Metodi di implementazione :

### Impostazioni globali

>[!NOTE]
>
>Queste impostazioni vengono applicate a tutti [!DNL Target] librerie .js. Dopo aver eseguito le modifiche nella sezione Metodi di implementazione , devi scaricare la libreria e aggiornarla nell’implementazione.

| Impostazione | Descrizione |
| --- | --- |
| Caricamento pagina abilitato (Creazione automatica mbox globale) | Seleziona se incorporare la chiamata mbox globale nel file at.js in modo che si attivi automaticamente al caricamento di ogni pagina. |
| Mbox globale | Seleziona un nome per la mbox globale. Per impostazione predefinita, il nome è target-global-mbox.<br>Nei nomi delle mbox in at.js puoi usare caratteri speciali, tra cui il simbolo &amp;. |
| Timeout (secondi) | Se [!DNL Target] non risponde con il contenuto entro il periodo definito, la chiamata al server riceve un timeout e viene visualizzato il contenuto predefinito. Durante la sessione del visitatore vengono ripetuti ulteriori tentativi di chiamata. Il valore predefinito è 5 secondi.<br>La libreria at.js utilizza l’impostazione di timeout in `XMLHttpRequest`. Il timeout viene avviato quando parte la richiesta e si interrompe quando [!DNL Target] riceve una risposta dal server. Per ulteriori informazioni, consulta [XMLHttpRequest.timeout](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/timeout) in Mozilla Developer Network.<br>Se il timeout specificato si verifica prima della ricezione della risposta, viene visualizzato il contenuto predefinito e il visitatore può essere conteggiato come partecipante a un’attività, poiché la raccolta dei dati viene eseguita sul server Edge di [!DNL Target]. Se la richiesta raggiunge il server Edge di [!DNL Target], il visitatore viene conteggiato.<br>Quando configuri l’impostazione di timeout, tieni presente quanto segue:<ul><li>Se il valore è troppo basso, gli utenti potrebbero visualizzare il contenuto predefinito la maggior parte delle volte, nonostante il visitatore venga conteggiato come partecipante all’attività.</li><li>Se il valore è troppo alto, i visitatori potrebbero visualizzare aree vuote nella pagina web o pagine vuote (se utilizzi la funzione per nascondere il corpo) per periodi di tempo prolungati.</li></ul>Per comprendere meglio i tempi di risposta della mbox, guarda la scheda Rete negli strumenti di sviluppo del tuo browser. Puoi anche utilizzare strumenti di terze parti per il monitoraggio delle prestazioni web, ad esempio Catchpoint.<br>**Nota**: La [visitorApiTimeout](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/)L&#39;impostazione {target=_blank} assicura che [!DNL Target] non attende la risposta API del visitatore per troppo tempo. Questa impostazione e l’impostazione Timeout per at.js qui descritta non entrano in contrasto. |
| Durata del profilo | Questa impostazione determina per quanto tempo vengono memorizzati i profili visitatore. Per impostazione predefinita, i profili vengono memorizzati per due settimane. Questa impostazione può essere aumentata fino a 90 giorni.<br>Per modificare l’impostazione Durata del profilo, contatta l’[Assistenza clienti](https://helpx.adobe.com/it/contact/enterprise-support.ec.html). |

### Metodo di implementazione principale

>[!IMPORTANT]
>
>Il team di Target supporta entrambi at.js 1.*x* e at.js 2.*x*. Esegui l’aggiornamento più recente di una delle versioni principali di at.js per assicurarti di eseguire una versione supportata.

Per scaricare la versione at.js desiderata, fai clic sul pulsante appropriato **[!UICONTROL Scarica]** pulsante .

Per modificare le impostazioni di at.js, fai clic su **[!UICONTROL Modifica]** accanto alla versione at.js desiderata.

>[!IMPORTANT]
>
>Prima di modificare queste impostazioni predefinite, consulta [Assistenza clienti](/help/main/cmp-resources-and-contact-information.md) in modo da non influenzare l&#39;implementazione corrente.

Oltre alle impostazioni precedentemente illustrate, sono disponibili anche le seguenti impostazioni specifiche di at.js:

| Impostazione | Descrizione |
|--- |--- |
| Intestazione libreria personalizzata | Aggiungi un JavaScript personalizzato da includere nella parte superiore della libreria. |
| Piè di pagina libreria personalizzato | Aggiungi un JavaScript personalizzato da includere nella parte inferiore della libreria. |

### Metodi di implementazione con On-Device Decisioning

A partire dalla versione 2.5.0, at.js offre funzioni decisionali sul dispositivo. Le decisioni sul dispositivo consentono di memorizzare nella cache [Test A/B](/help/main/c-activities/t-test-ab/test-ab.md) e [Targeting esperienza](/help/main/c-activities/t-experience-target/experience-target.md) (XT) attività sul browser per eseguire decisioni in memoria senza una richiesta di rete di blocco al [!DNL Adobe Target] Rete Edge.

Per ulteriori informazioni, consulta gli argomenti:

* [Decisioni sul dispositivo per lato client](https://developer.adobe.com/target/implement/client-side/){target=_blank}
* [Decisioni sul dispositivo per lato server](https://developer.adobe.com/target/implement/server-side/sdk-guides/on-device-decisioning/){target=_blank}

### API del profilo

Puoi abilitare o disabilitare l’autenticazione per gli aggiornamenti collettivi tramite API e generare un token di autenticazione del profilo.

Per ulteriori informazioni, consulta [Impostazioni API del profilo](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/profile-api-settings/){target=_blank}.

### Strumenti di debug

Generare un token di autorizzazione per utilizzare [!DNL Target] strumenti di debug. Fai clic su **[!UICONTROL Genera nuovo token di autenticazione]**.

![Generare un nuovo token di autenticazione](/help/main/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/assets/debugger-auth-token.png)

### Privacy

Queste impostazioni consentono di utilizzare [!DNL Target] in conformità alle leggi sulla privacy dei dati applicabili.

Scegli l’impostazione desiderata dall’elenco a discesa Indirizzo IP visitatore offuscato :

* Ultima offuscamento dell&#39;ottetto
* Intera offuscamento dell’IP
* None (Nessuno)

Per ulteriori informazioni, consulta [Privacy](https://developer.adobe.com/target/before-implement/privacy/privacy/){target=_blank}.

>[!NOTE]
>
>L’opzione Supporto di browser legacy era disponibile nelle versioni 0.9.3 e precedenti di at.js . Questa opzione è stata rimossa in at.js versione 0.9.4. Per un elenco di browser supportati da at.js, consulta [Browser supportati](https://developer.adobe.com/target/before-implement/supported-browsers/){target=_blank}.<br>I browser legacy sono browser meno recenti che non supportano completamente la condivisione delle risorse tra diverse origini (Cross Origin Resource Sharing, CORS). Questi browser includono: Internet Explorer nelle versioni precedenti alla versione 11; Safari versione 6 e precedenti. Se il supporto del browser legacy è stato disabilitato, Target non distribuiva contenuti o contava i visitatori nei rapporti su questi browser. Se questa opzione è stata abilitata, si consiglia di eseguire il controllo qualità tra i browser più datati per garantire una buona esperienza del cliente.

## Scaricare at.js {#concept_1E1F958F9CCC4E35AD97581EFAF659E2}

Istruzioni per scaricare la libreria utilizzando [!DNL Target] Interfaccia o API di download.

>[!NOTE]
>
>* [[!DNL Adobe Experience Platform]](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-using-adobe-launch/){target=_blank} è il metodo preferito per l&#39;implementazione [!DNL Target] e la libreria at.js. Le seguenti informazioni non sono applicabili quando si utilizzano tag in [!DNL Adobe Experience Platform] implementare [!DNL Target].
>
>* La [!DNL Target] Il team supporta sia at.js 1 che at.js 1.*x* e at.js 2.*x*. Esegui l’aggiornamento più recente di una delle versioni principali di at.js per assicurarti di eseguire una versione supportata. Per ulteriori informazioni su ogni versione, consulta [Dettagli sulle versioni di at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank}.


### Scaricare at.js utilizzando [!DNL Target] interfaccia {#section_1F5EE401C2314338910FC57F9592894E}

Per scaricare [!DNL at.js] dall&#39;interfaccia di [!DNL Target]:

1. Fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]**.
1. Da [!UICONTROL Metodi di implementazione] fai clic sulla sezione **[!UICONTROL Scarica]** accanto alla versione at.js desiderata.

### Scaricare at.js utilizzando [!DNL Target] API di download {#section_C0D9D2A9068144708D08526BA5CA10D0}

Per scaricare [!DNL at.js] utilizzando l&#39;API.

1. Ottieni il tuo codice cliente.

   Il codice cliente è disponibile nella parte superiore della **[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]** della pagina [!DNL Target] interfaccia.

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
   >Il team di Target gestisce solo due versioni di [!DNL at.js], la versione corrente e quella immediatamente precedente. Aggiorna [!DNL at.js] per assicurarti di eseguire una versione supportata. Per ulteriori informazioni su ogni versione, consulta [Dettagli sulle versioni di at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank}.

   Il caricamento di questa URL avvia il download del file [!DNL at.js] personalizzato.

## Implementazione di at.js {#concept_03CFA86973A147839BEB48A06FEE5E5A}

at.js dovrebbe essere implementato nell’elemento `<head>` di ogni pagina del sito Web.

Una tipica implementazione di Target che non utilizza un gestore di tag, ad esempio i tag in [[!DNL Adobe Experience Platform]](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-using-adobe-launch/){target=_blank} si presenta così:

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

* Il tipo di documento HTML5 (ad esempio, `<!doctype html>`). I doctype non supportati o meno recenti potrebbero impedire a Target di effettuare una richiesta.
* Preconnessione e Preacquisizione sono opzioni che potrebbero consentire di caricare più rapidamente le pagine Web. Se utilizzi queste configurazioni, assicurati di sostituire `<client code>` con il tuo codice cliente, che puoi ottenere dal **[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione] pagina.
* Se si dispone di un livello di dati, è ottimale definirlo il più possibile nel `<head>` delle pagine prima di caricare at.js. Questo posizionamento offre la massima capacità di utilizzare queste informazioni in Target per la personalizzazione.
* Funzioni speciali di Target, come ad esempio `targetPageParams()`, `targetPageParamsAll()`, Data Providers e `targetGlobalSettings()` devono essere definite dopo il livello di dati e prima di caricare at.js. In alternativa, queste funzioni possono essere salvate nel [!UICONTROL Intestazione libreria] della sezione [!UICONTROL Modificare le impostazioni di at.js] e salvati come parte della libreria at.js stessa. Per ulteriori informazioni su queste funzioni, consulta [Funzioni di at.js](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/atjs-functions/){target=_blank}.
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
