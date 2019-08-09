---
description: Informazioni sul Regolamento generale sulla protezione dei dati (GDPR) dell'Unione Europea e sulla California Consumer Privacy Act (CCPA) e sul modo in cui tali normative influiscono sulla vostra organizzazione e Adobe Target.
keywords: gdpr; eu; unione europea; privacy; faq; domande frequenti; California consumer privacy act; ccpa; privacy; protezione dei dati; opt-out; rifiuto; government; regulation
seo-description: Informazioni sul Regolamento generale sulla protezione dei dati (GDPR) dell'Unione Europea e sulla California Consumer Privacy Act (CCPA) e sul modo in cui tali normative influiscono sulla vostra organizzazione e Adobe Target.
seo-title: Regolamento generale sulla protezione dei dati (GDPR), la California Consumer Privacy Act (CCPA) e Adobe Target
solution: Target
title: Normativa sulla privacy e sulla protezione dei dati
topic: Standard
uuid: 5e67adcf-464c-495f-9ba5-15152d9a6a41
translation-type: tm+mt
source-git-commit: db45081ac256f6727fa08606cb1aa47a20aa233e

---


# Normativa sulla privacy e sulla protezione dei dati {#privacy-and-general-data-protection-regulation-gdpr}

Informazioni sul Regolamento generale sulla protezione dei dati (GDPR) dell'Unione Europea e sulla California Consumer Privacy Act (CCPA) e sul modo in cui tali normative influiscono sulla vostra organizzazione e [!DNL Adobe Target]su.

## Privacy and General Data Protection Regulation (GDPR) overview {#topic_DE567ECB6C944695AEE5073889F1AEA9}

Il 25 maggio 2018, il GDPR dell'Unione Europea ha avuto effetto. Per ulteriori informazioni sulle implicazioni per l'utente, consultare [RGPD e la tua azienda](https://www.adobe.com/privacy/general-data-protection-regulation.html).

When [!DNL Adobe] is providing software and services to an enterprise, [!DNL Adobe] is acting as a Data Processor for any personal data it processes and stores as part of providing these services. As a Data Processor, [!DNL Adobe] processes personal data in accordance with your company's permission and instructions (for example, as set out in your agreement with [!DNL Adobe]).

As the Data Controller, you determine the personal data that [!DNL Adobe] processes and stores on your behalf. If you use [!DNL Adobe Experience Cloud] solutions, [!DNL Adobe] might host personal data for you, depending on the solutions you use and the information you choose to send to your [!DNL Adobe Experience Cloud] account. Per un elenco dettagliato di esempi, consultare [Adobe Experience Cloud Privacy](https://www.adobe.com/privacy/marketing-cloud.html#collect).

[!DNL Adobe Experience Cloud] fornire API GDPR pronte per i dati che consentono loro di completare le attività seguenti:

* Accedere alle informazioni relative all'interessato memorizzate in [!DNL Target]
* Cancellare le informazioni relative all'interessato memorizzate in [!DNL Target]

Per ulteriori informazioni, consulta:

* [Sito web API di Adobe del regolamento generale sulla protezione dei dati](https://www.adobe.io/apis/cloudplatform/gdpr.html)
* [Documentazione RGPD](https://www.adobe.io/apis/cloudplatform/gdpr/docs.html)

## Panoramica della California Consumer Privacy Act (CCPA)

The California Consumer Privacy Act (CCPA) is a effective January 1, 2020. Grazie alla progettazione, la legge consente al campo di modifica della California di apportare modifiche e definire i dettagli, il che significa che potreste avere domande diverse. In caso di domande, non sei solo un'azienda che sta lavorando attraverso le incertezze della legge e cerca di comprendere e sviluppare un approccio per rispondere ai requisiti legali, operativi e tecnici.

CCPA offre ai consumatori della California nuovi diritti relativi alle informazioni personali e impone responsabilità sulla protezione dei dati relativamente a determinate entità che operano in California. Ad alto livello, la legge offre a Californians diversi diritti chiave, compresi i diritti per:

* Informazioni su richiesta (accesso ai dati)
* Rifiuto della vendita di informazioni personali (un diritto molto definito per rifiutare la condivisione di informazioni con terze parti)
* Eliminazione di dati personali
* Notifica che le informazioni personali sono state divulgate o vendute

Se l'anno scorso sei stato occupato per la legge sulla privacy dell'Europa (GDPR), alcuni di questi diritti potrebbero avere familiarità con e molti dei lavori che hai fatto potrebbero essere in grado di essere ripristinati.

## Adobe Target and [!DNL Experience Platform Launch] opt-in {#section_6F7B53F5E40C4425934627B653E831B0}

[!DNL Target] fornisce il supporto per le funzionalità di consenso tramite [!DNL Launch] per supportare la strategia di gestione del consenso. Opt-in functionality lets customers control how and when the [!DNL Target] tag is fired. There is also an option via [!DNL Launch] to pre-approve the [!DNL Target] tag. To enable the ability to use Opt-In in the [!DNL Target] at.js library, you should use `targetGlobalSettings` and add the `optinEnabled=true` setting. In [!DNL Launch] you'll need to select "enable" from the [!UICONTROL GDPR Opt-In] drop-down list in the [!DNL Launch] extension installation view. Per ulteriori informazioni, consulta la [documentazione di Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md).

Il seguente snippet di codice mostra come abilitare l’impostazione `optinEnabled=true`:

```
window.targetGlobalSettings = {
  optinEnabled: true
};
```

>[!NOTE]
>
>La funzionalità di consenso è supportata in. js versione 1.7.0 e at. js 2.1.0 o versione successiva. La funzione di consenso non è supportata in. js versione 2.0.0 e 2.0.1.
>
>Using [!DNL Experience Platform Launch] to manage opt-in is the recommended approach. Further granular control exists in [!DNL Launch] to hide selected elements of your page prior to [!DNL Target] firing that are helpful to leverage as part of your consent strategy.

Esistono tre scenari da considerare quando si utilizza l’opt-in:

1. **[!DNL Target]Il tag è preapprovato tramite[!DNL Launch](o i dati precedentemente approvati[!DNL Target]):** [!DNL Target] Il tag non viene tenuto per il consenso e funziona come previsto.
1. **[!DNL Target]Il tag di NON è pre-approvato e`bodyHidingEnabled`è FALSE:** il tag di viene attivato solo dopo il consenso del cliente. [!DNL Target] Prima della raccolta del consenso, è disponibile solo il contenuto predefinito. After consent is received, [!DNL Target] is called and personalized content is available to the data subject (visitor). Poiché solo i contenuti predefiniti sono disponibili prima del consenso, è importante sfruttare una strategia appropriata, come ad esempio una pagina iniziale che copre qualsiasi parte della pagina o del contenuto che potrebbe essere personalizzata. Ciò garantisce che l'esperienza rimanga coerente per l'interessato (visitatore).
1. **[!DNL Target]Il tag di NON è pre-approvato e`bodyHidingEnabled`è TRUE:** il tag di viene attivato solo dopo il consenso del cliente. [!DNL Target] Prima della raccolta del consenso, è disponibile solo il contenuto predefinito. Tuttavia, poiché `bodyHidingEnabled` è impostato su true, `bodyHiddenStyle` determina quale contenuto della pagina è nascosto fino a quando il tag di non viene attivato (o l'interessato rifiuta di effettuare l’opt-in, nel qual caso viene visualizzato il contenuto predefinito). [!DNL Target] Per impostazione predefinita, `bodyHiddenStyle` è impostato su `body { opacity:0;`}, che nasconde il tag HTML body. Di seguito si trova la configurazione di pagina consigliata affinché l'intero corpo della pagina, a eccezione della finestra di dialogo di gestione del consenso, sia nascosto inserendo il contenuto della pagina in un contenitore e la finestra di dialogo di gestione del consenso in un contenitore separato. This setup configures [!DNL Target] so that it hides the page content container only. Consulta la [documentazione di Launch per ulteriori informazioni su come configurare queste impostazioni](https://www.adobe.io/apis/cloudplatform/gdpr/services/allservices.html).

   La configurazione consigliata della pagina per lo scenario 3 è:

   ```
   <html> 
   <head> 
   //visitor, at.js 
   </head> 
   
   <body> 
   <div id = "consentManagerDialog"> 
   
   //consent manager html dialog goes here 
   </div> 
   
   <div id="pageContent"> 
   // page content goes here 
   </div> 
   
   </body> 
   </html> 
   ```

   Supponendo `bodyHiddenStyle` di:

   ```
   #pageContent { opacity:0;}
   ```

## Domande frequenti sulla privacy e sulla protezione dei dati {#concept_41F88DE95D2943178BEC382736B5C038}

Domande frequenti sul Regolamento generale sulla protezione dei dati (GDPR) e sulla California Consumer Privacy Act (CCPA) di [!DNL Target].

### Qual è il criterio di Adobe per questi regolamenti? {#section_A6849628D6524C80A6E16946DC5D25A9}

[!DNL Adobe] adempie o sta adempiendo ai propri obblighi in qualità di Incaricato del trattamento dei dati. La progettazione dei controlli per la sicurezza e la privacy è fortemente basata sulla progettazione e i miglioramenti apportati al prodotto sono stati introdotti anticipatamente rispetto alla scadenza del 2018 maggio. I clienti aziendali avranno la responsabilità di implementare questi miglioramenti e di aggiornare le politiche e le procedure necessarie.

### Will my company, the Data Controller, need to submit a GDPR or CCPA request to each [!DNL Adobe Experience Cloud] solution that it uses? {#section_1DCFA9387D0C4506B14DCE04C49AC22A}

No, [!DNL Adobe] is providing a central way to help Data Controllers meet their GDPR and CCPA requirements. Non è necessario che i Titolari del trattamento dei dati inviino la richiesta per ciascuna soluzione.

All GDPR and CCPA requests across [!DNL Experience Cloud] solutions, including [!DNL Target], will be made through a central Adobe API, currently called the GDPR API. The API will then complete the request across the Data Controller's [!DNL Experience Cloud] solution suite.

### What information will [!DNL Adobe] enable our customers to delete in response to a data subject/user request? {#section_4B51D00924EC4166B2442218B69214F0}

The information related to an individual visitor within [!DNL Target] is contained within the [!DNL Target] Visitor Profile. [!DNL Target] consentirà ai nostri clienti di eliminare tutti i dati associati a un ID nel loro profilo visitatore. Per esempi degli store di dati [!DNL Target] di profilo, vedi [Profilo visitatore](../../../c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E).

I dati aggregati o anonimi (ad esempio, i dati di segnalazione) che non identificano una persona particolare oppure i dati che non sono correlati a una persona specifica (ad esempio, i dati sul contenuto) esulano dall'ambito di una richiesta di cancellazione da parte dell'utente.

[!DNL Target]Anche i profili dei visitatori di che sono stati inattivi per 90 giorni vengono cancellati per impostazione predefinita, senza che sia necessaria alcuna azione.

### What IDs are supported to help customers complete a GDPR or CCPA access and deletion request for [!DNL Target]? {#section_F7D0EE4E6A28490FB20056A0D26118BC}

[!DNL Target] supporta i seguenti tipi di ID per individuare un profilo cliente:

| ID utente | Tipo ID dello spazio dei nomi | ID dello spazio dei nomi | Definizione |
|--- |--- |--- |--- |
| Experience Cloud ID (ECID) | Standard | 4 | Adobe Experience Cloud ID, precedentemente conosciuto come ID visitatore o Marketing Cloud ID. È possibile utilizzare l'API JavaScript per individuare questo ID (consulta i dettagli di seguito). |
| ID TnT/ID cookie(TNTID) | Standard | 9 | Identificativo di Target impostato come cookie nel browser del visitatore. È possibile utilizzare l'API JavaScript per individuare questo ID (consulta i dettagli di seguito). |
| ID di terze parti/ID CRM (THIRDPARTYID) | Specifico di Target | N/D | Se si fornisce a Target il proprio CRM o altre informazioni di identificazione univoche per i propri clienti. |

>[!NOTE]
>
>Although [!DNL Target] supports both first-party and third-party cross-domain cookies, first-party [!DNL Target] cookies only are recommended for GDPR and CCPA.

### How does [!DNL Target] handle consent management? {#section_C86BF5EE4FAA47039659850E7594A6BA}

GDPR e CCPA non cambiano quando devi ottenere il consenso, ma come ottenerlo. La strategia di consenso di ciascun cliente dipende dalle sue modalità di raccolta e utilizzo dei dati e dalla sua politica sulla privacy. Consent management isn’t supported by and shouldn’t be achieved via [!DNL Target] for GDPR and CCPA.

[!DNL Adobe]Attualmente,  non offre una soluzione per la gestione dei consensi, ma sul mercato sono in fase di sviluppo diversi strumenti per soddisfare alcuni dei nuovi requisiti. For more information on privacy tools in general, including consent managers, see the [2017 Privacy Tech Vendor Report](https://iapp.org/media/pdf/resource_center/Tech-Vendor-Directory-1.4.1-electronic.pdf) on the *International Association of Privacy Professionals (iaap)* website.

[!DNL Target] fornisce il supporto per le funzionalità di consenso tramite [!DNL Launch] per fornire supporto per la strategia di gestione del consenso. Opt-in functionality lets customers control how and when the [!DNL Target] tag is fired. There is also an option via [!DNL Launch] to pre-approve the [!DNL Target] tag. Using [!DNL Launch] to manage opt-in is the recommended approach. Further granular control exists in [!DNL Launch] to hide select elements of your page prior to the [!DNL Target] firing that might be helpful to leverage as part of your consent strategy.

For more information on GDPR, CCPA, and [!DNL Launch], see [The Adobe Privacy JavaScript Library and GDPR](https://www.adobe.io/apis/cloudplatform/gdpr/services/allservices.html). Also, see the *Adobe Target and Experience Platform Launch opt-in* section above.

### AdobePrivacy.js invia informazioni all'API RGPD? {#section_1EB8A2BAAD31474C97C1D455F41DA739}

[!DNL AdobePrivacy.js] *non* invia tali informazioni all'API. Farlo è compito del cliente. Questa libreria fornisce solo gli ID memorizzati nel browser per un visitatore specifico.

### Che cosa elimina l’azione removeIdentities? {#section_D3A1591EA1B84C499CE1563DEAF32448}

[!DNL removeIdentities] rimuove identità *solo*[!DNL Adobe] dal browser, e solo nel caso in cui la soluzione sia stata implementata.

For example, [!DNL Target] deletes the cookies storing its IDs, but [!DNL Adobe Audience Manager] (AAM) does not delete the demdex ID that is stored in a third-party cookie.

### What information needs to be included in a Target GDPR or CCPA request? {#section_D29A4744AE6344E68AD7710B185FD6D0}

In addition to the requirements from Central Privacy Service, a valid GDPR or CCPA message for [!DNL Target] contains:

```
{ 
    "jobId":"12345AD43E", 
    ... 
    "products":["Target",...], 
    "companyContexts":[ 
        { 
            "namespace":"imsOrgID", 
            "value":"123456789@AdobeOrg" 
        }, 
        ... 
    ], 
    "userContexts":[ 
        { 
            "namespace":"ECID", 
            "namespaceId":4, 
            "type":"standard", 
            "value":"53792210477379708453829363835595041181" 
        } 
        And/OR: 
        { 
            "namespace":"TNTID", 
            "namespaceId":9, 
            "type":"standard", 
            "value":"1234567890" 
        } 
        And/OR: 
        { 
            "namespace":"THIRDPARTYID", 
            "type":"target", 
            "value":"thirdPartyIdName" 
        }, 
        ... 
    ] 
}
```

### Quali tipi di risposte è possibile prevedere da Target mediante l’API RGPD? {#section_F67263D2A72B4641A47CE36729CCAE8F}

| Stato richiesta | Messaggio risposta Target | Scenario |
|--- |--- |--- |
| Processing (Completa elaborazione) | Processing (Completa elaborazione) | Target ha ricevuto la richiesta GDPR o CCPA e sta elaborando. |
| Completa | Non applicabile; contesto aziendale non applicabile | L'ID IMS nella richiesta GDPR o CCPA non viene mappato su alcun client di Target.<br>Tieni presente che alcune società hanno più ID IMS. Devi inviare l'ID IMS in cui è stato fornito Target. |
| Completa | Non applicabile; contesto utente non trovato | L'ID fornito nella richiesta GDPR o CCPA per il visitatore o l'oggetto di dati specifico non è presente nell'archivio del profilo di Target.<br>Nota che questo risultato si ottiene anche se si tenta di inviare un tipo di ID spazio dei nomi non supportato da Target (vedi sopra per gli ID supportati). |
| Errore | Messaggio di errore (i dettagli dipendono dal tipo di errore) | Errore durante il recupero o l'eliminazione del profilo dati richiesto.<br>Errore durante il caricamento su Azure della richiesta di accesso. |

### Quale risposta invia Target all'API RGPD per una richiesta di accesso? {#section_D96D8FBEAF9C4BDAA638215FAFE00763}

Responses to access data requests contain a summary of the [!DNL Target] profile for the visitor in question. Note that this return is sent to the [!DNL Experience Cloud] GDPR API, which in turn sends Data Controllers a response.

A sample [!DNL Target] access API response could look like this:

```
{ 
    "jobId":"12345AD43E", 
    ... 
    "products":["Target",...], 
    "companyContexts":[ 
        { 
            "namespace":"imsOrgID", 
            "value":"123456789@AdobeOrg" 
        }, 
        ... 
    ], 
    "userContexts":[ 
        { 
            ~"namespace":"ECID", 
            "namespaceId":4, 
            "type":"standard", 
            "value":"53792210477379708453829363835595041181" 
        } 
        And/OR: 
        { 
            ~"namespace":"tntId", 
            "namespaceId":9, 
            "type":"standard", 
            "value":"1234567890" 
        } 
        And/OR: 
        { 
            "namespace":"thirdPartyId", 
            "type":"target", 
            "value":"thirdPartyIdName" 
        }, 
        ... 
    ] 
} 
```

| Campo | Descrizione |
|--- |--- |
| jobId | Indica l'ID processo GDPR o CCPA dall'API centrale GDPR. |
| imsOrgID | Fornisce un identificatore univoco per la tua azienda. |
| namespace | Denominato anche fonte di dati. Consultate "Quali ID sono supportati per aiutare i clienti a completare una richiesta di accesso e di eliminazione di CCPA per Target?" in questo argomento. |
| type | Il tipo di ID per il quale hai richiesto l'accesso ai dati GDPR o CCPA. Target accetta diversi tipi di ID, alcuni dei quali sono standard e altri specifici di Target. Consultate "Quali ID sono supportati per aiutare i clienti a completare una richiesta di accesso e di eliminazione di CCPA per Target?" in questo argomento. |
| value | L'ID spazio dei nomi/sorgente dei dati. Consultate "Quali ID sono supportati per aiutare i clienti a completare una richiesta di accesso e di eliminazione di CCPA per Target?" per i valori accettati. |
| integration code | I codici di integrazione sono nomi semplici per le origini dati e consentono di tracciarle più facilmente rispetto agli ID delle origini dati. |

Quando vengono forniti più valori per identificare i profili, ogni identificatore valido ha un file di profilo. The profile file(s) are sent to the central GDPR Azure Blob through the GDPR Central API, in the format of [!DNL Target] Profile JSON response.

A sample [!DNL Target] Profile JSON could look like the following example:

```
{"profileAttributes": 
 
"Sample_Parameter":{"value":"Gold Loyalty Status","modifiedAt":"2018-04-11T21:44:14.000-04:00"}, 
 
"user.ReturnTimeOfDay":{"value":"44.0","modifiedAt":"2018-04-11T21:44:14.000-04:00"}, 
 
"firstSessionStart":{"value":"1523497450602","modifiedAt":"2018-04-11T21:44:10.000-04:00"}, 
 
"user.sessionCountScript":{"value":"1","modifiedAt":"2018-04-11T21:44:14.000-04:00"} 
   } 
} 
```

La tabella seguente contiene la descrizione dei campi JSON del profilo illustrativo:

| Campo | Descrizione |
|--- |--- |
| Sample_Parameter | Many pieces of information in the [!DNL Target] profile are uploaded or directly provided by the Data Controller. In this example, a parameter was uploaded into the [!DNL Target] profile using the Profile Update API. Per ulteriori informazioni, vedi [Metodi per ottenere dati in Target](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md). |
| user.ReturnTimeOfDay | Questo campo standard include l'ora del giorno dell'ultima visita di ritorno dell'utente. |
| firstSessionStart | Questo campo standard include l'ora del giorno in cui è iniziata la prima sessione dell'utente. |
| user.sessionCountScript | Many pieces of information in the [!DNL Target] profile are uploaded or directly provided by the Data Controller. In questo esempio, uno script di profilo incrementa il numero di sessioni che il visitatore ha effettuato sul sito del Titolare del trattamento dei dati. Per ulteriori informazioni, consulta [Attributi del profilo](/help/c-target/c-visitor-profile/profile-parameters.md). |

>[!NOTE]
>
>This is a shortened version of a [!DNL Target] profile JSON for the purpose of illustration. Many of the fields of the [!DNL Target] profile are not standard. Ciò che viene restituito dipende da quali informazioni si trovano in quel profilo specifico di visitatore.

### Target supporta l’omissione dell’IP? {#section_428907B0CD9842D9B245B38C66A53C6A}

[!DNL Target] supporta offuscamento IP se scegliete di utilizzarlo come parte della strategia di implementazione GDPR o CCPA. Per ulteriori informazioni, consulta [Privacy](../../../c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md#concept_639482A343DB4963A6144378E1D8D7F0).
