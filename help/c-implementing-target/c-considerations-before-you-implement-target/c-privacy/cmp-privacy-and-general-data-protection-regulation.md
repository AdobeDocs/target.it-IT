---
keywords: gdpr;eu;european union;privacy;faq;frequently asked questions;california consumer privacy act;ccpa;privacy;data protection;opt-out;opt out;government;regulation
description: Informazioni sul regolamento generale sulla protezione dei dati (RGPD) dell’Unione Europea, sul California Consumer Privacy Act (CCPA) e altri requisiti internazionali sulla privacy, e come questi regolamenti influiscono sulla tua organizzazione e su Adobe Target.
title: Normative sulla privacy e la protezione dei dati
feature: privacy and security
topic: Standard
uuid: 5e67adcf-464c-495f-9ba5-15152d9a6a41
translation-type: tm+mt
source-git-commit: 8b722ea47119eb71df56209d53e0e34f4c14461a
workflow-type: tm+mt
source-wordcount: '2250'
ht-degree: 93%

---


# Normative sulla privacy e la protezione dei dati {#privacy-and-general-data-protection-regulation-gdpr}

Informazioni sul regolamento generale sulla protezione dei dati (RGPD) dell’Unione Europea, sul California Consumer Privacy Act (CCPA) e altri requisiti internazionali sulla privacy, e come questi regolamenti influiscono sulla tua organizzazione e su Adobe Target.

## Privacy e Regolamento generale sulla protezione dei dati (RGPD) - Panoramica {#topic_DE567ECB6C944695AEE5073889F1AEA9}

Il 25 maggio 2018 è entrato in vigore il regolamento RGPD dell’Unione Europea. Per ulteriori informazioni sulle implicazioni per l&#39;utente, consultare [RGPD e la tua azienda](https://www.adobe.com/privacy/general-data-protection-regulation.html).

Quando [!DNL Adobe] fornisce software e servizi alle aziende, [!DNL Adobe] agisce come Incaricato del trattamento dei dati, per ognuno dei dati personali trattati e memorizzati nell’ambito della fornitura di tali servizi. In qualità di Incaricato del trattamento dei dati, [!DNL Adobe] tratta i dati personali in conformità alle autorizzazioni e alle istruzioni dell’azienda (ad esempio, come stabilito nell’accordo con [!DNL Adobe]).

In qualità di titolare del trattamento, dovrai individuare i dati personali elaborati e archiviati da [!DNL Adobe] per tuo conto. Se usi le soluzioni [!DNL Adobe Experience Cloud], [!DNL Adobe] potrebbe conservare per tuo conto i dati personali, in base alle soluzioni che usi e alle informazioni che scegli di inviare al tuo account di [!DNL Adobe Experience Cloud]. Per un elenco dettagliato di esempi, consultare [Adobe Experience Cloud Privacy](https://www.adobe.com/privacy/marketing-cloud.html#collect).

[!DNL Adobe Experience Cloud] fornisce API a supporto del regolamento RGPD che consentono ai titolari del trattamento di completare le attività seguenti:

* Accedere alle informazioni relative all’interessato memorizzate in [!DNL Target]
* Cancellare le informazioni relative all’interessato memorizzate in [!DNL Target]

Per ulteriori informazioni, consulta:

* [Sito web API di Adobe del regolamento generale sulla protezione dei dati](https://www.adobe.io/apis/cloudplatform/gdpr.html)
* [Documentazione RGPD](https://www.adobe.io/apis/cloudplatform/gdpr/docs.html)

## California Consumer Privacy Act (CCPA) - Panoramica

Il California Consumer Privacy Act (CCPA) offre ai consumatori della California nuovi diritti relativi alle informazioni personali e impone responsabilità di protezione dei dati a determinate entità che operano in California. Il CCPA entra in vigore il 1° gennaio 2020.

Ad alto livello, la legge tutela i californiani con diversi diritti chiave, compreso il diritto a:

* Richiedere informazioni (accesso ai dati)
* Non acconsentire alla vendita di informazioni personali (diritto con definizione molto ampia sulla possibilità di non acconsentire alla condivisione di informazioni con terze parti)
* Richiedere la cancellazione dei dati personali
* Ricevere informazioni sui dati personali che vengono divulgati o venduti

Se ti sei già preparato alla legge europea sulla privacy (RGPD), alcuni di questi diritti ti potrebbero essere familiari e molto del lavoro già svolto potrebbe essere adattato per questi nuovi requisiti.

>[!NOTE]
>
>L’accesso e l’eliminazione dei dati applicati all’APP seguono lo stesso processo applicato al GDPR.

## Adobe Target e la funzionalità opt-in di [!DNL Experience Platform Launch] {#section_6F7B53F5E40C4425934627B653E831B0}

[!DNL Target] fornisce supporto per la funzionalità opt-in tramite [!DNL Launch] per supportare la strategia di gestione dei consensi. La funzionalità opt-in consente ai clienti di controllare come e quando viene attivato il tag di [!DNL Target]. È inoltre presente un’opzione tramite [!DNL Launch] per pre-approvare il tag di [!DNL Target]. Per abilitare la capacità di utilizzare la funzione di opt-in in [!DNL Target] at.js, utilizza `targetGlobalSettings` e aggiungi l’impostazione `optinEnabled=true`. In [!DNL Launch], è necessario selezionare “abilita” dall’elenco a discesa [!UICONTROL Opt-in RGPD] nella visualizzazione di installazione dell’estensione [!DNL Launch]. Per ulteriori informazioni, consulta la [documentazione di Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md).

Il seguente snippet di codice mostra come abilitare l’impostazione `optinEnabled=true`:

```
window.targetGlobalSettings = {
  optinEnabled: true
};
```

>[!NOTE]
>
>La funzionalità opt-in è supportata in at.js 1.7.0 e in at.js 2.1.0 o versione successiva. La funzionalità opt-in non è supportata in at.js 2.0.0 e 2.0.1.
>
>L’utilizzo di [!DNL Experience Platform Launch] per gestire l’opt-in rappresenta l’approccio consigliato. Esiste un ulteriore controllo granulare in [!DNL Launch] per nascondere elementi selezionati della pagina prima dell’attivazione di [!DNL Target] che è utile da sfruttare come parte della strategia di consenso.

Esistono tre scenari da considerare quando si utilizza l’opt-in:

1. **Il tag di[!DNL Target]è pre-approvato tramite[!DNL Launch](oppure l’interessato ha già approvato[!DNL Target]in precedenza):** il tag di [!DNL Target] non viene trattenuto per il consenso e funziona come previsto.
1. **Il tag di[!DNL Target]NON è pre-approvato e`bodyHidingEnabled`è FALSE:** il tag di [!DNL Target] viene attivato solo dopo il consenso del cliente. Prima della raccolta del consenso, è disponibile solo il contenuto predefinito. Dopo aver ricevuto il consenso, [!DNL Target] viene chiamato e il contenuto personalizzato è disponibile per l’interessato (il visitatore). Poiché solo i contenuti predefiniti sono disponibili prima del consenso, è importante sfruttare una strategia appropriata, come ad esempio una pagina iniziale che copre qualsiasi parte della pagina o del contenuto che potrebbe essere personalizzata. Ciò garantisce che l&#39;esperienza rimanga coerente per l&#39;interessato (visitatore).
1. **Il tag di[!DNL Target]NON è pre-approvato e`bodyHidingEnabled`è TRUE:** il tag di [!DNL Target] viene attivato solo dopo il consenso del cliente. Prima della raccolta del consenso, è disponibile solo il contenuto predefinito. Tuttavia, poiché `bodyHidingEnabled` è impostato su true, `bodyHiddenStyle` determina quale contenuto della pagina è nascosto fino a quando il tag di [!DNL Target] non viene attivato (o l’interessato rifiuta di effettuare l’opt-in, nel qual caso viene visualizzato il contenuto predefinito). By default, `bodyHiddenStyle` is set to `body { opacity:0;}`, which hides the HTML body tag. Di seguito si trova la configurazione di pagina consigliata affinché l’intero corpo della pagina, a eccezione della finestra di dialogo di gestione del consenso, sia nascosto inserendo il contenuto della pagina in un contenitore e la finestra di dialogo di gestione del consenso in un contenitore separato. Questa configurazione imposta [!DNL Target] affinché nasconda solo il contenitore del contenuto della pagina. Consulta la [documentazione di Launch per ulteriori informazioni su come configurare queste impostazioni](https://www.adobe.io/apis/cloudplatform/gdpr/services/allservices.html).

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

## Domande frequenti sulla privacy e la protezione dei dati {#concept_41F88DE95D2943178BEC382736B5C038}

Domande frequenti sul Regolamento generale sulla protezione dei dati (RGPD) dell’Unione Europea, sul California Consumer Privacy Act (CCPA) e su altri requisiti internazionali relativi alla privacy che interessano Target.

### Qual è la politica di Adobe in merito a questi regolamenti? {#section_A6849628D6524C80A6E16946DC5D25A9}

[!DNL Adobe] adempie o sta adempiendo ai propri obblighi in qualità di Incaricato del trattamento dei dati. Abbiamo una solida base di sicurezza certificata e controlli sulla privacy in base alla progettazione e abbiamo introdotto miglioramenti nei prodotti con anticipo sulla scadenza di maggio 2018. I clienti aziendali avranno la responsabilità di implementare questi miglioramenti e di aggiornare le politiche e le procedure necessarie.

### La mia azienda, Titolare del trattamento dei dati, dovrà inviare una richiesta relativa al RGPD o CCPA per ciascuna soluzione [!DNL Adobe Experience Cloud] utilizzata? {#section_1DCFA9387D0C4506B14DCE04C49AC22A}

No, [!DNL Adobe] sta implementando una modalità unica per consentire ai Titolari del trattamento dei dati di soddisfare i requisiti RGPD e CCPA. Non è necessario che i Titolari del trattamento dei dati inviino la richiesta per ciascuna soluzione.

Tutte le richieste relative ai requisiti RGPD per le soluzioni [!DNL Experience Cloud], incluso [!DNL Target], saranno effettuate tramite un’API Adobe centralizzata, attualmente denominata API RGPD. L’API completa quindi la richiesta nella suite di soluzioni [!DNL Experience Cloud] per il titolare del trattamento dei dati.

### Quali sono le informazioni che [!DNL Adobe] consente ai nostri clienti di eliminare, in risposta a una richiesta dell’interessato/utente? {#section_4B51D00924EC4166B2442218B69214F0}

Le informazioni relative a un singolo visitatore all’interno di [!DNL Target] sono contenute nel Profilo del visitatore di [!DNL Target]. [!DNL Target] consentirà ai nostri clienti di eliminare tutti i dati associati a un ID nel loro profilo visitatore. Per esempi dei dati del profilo memorizzati da [!DNL Target], consulta [Profilo visitatore](../../../c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E).

I dati aggregati o anonimi (ad esempio, i dati di segnalazione) che non identificano una persona particolare oppure i dati che non sono correlati a una persona specifica (ad esempio, i dati sul contenuto) esulano dall’ambito di una richiesta di cancellazione da parte dell’utente.

Anche i profili dei visitatori di [!DNL Target] che sono stati inattivi per 90 giorni vengono cancellati per impostazione predefinita, senza che sia necessaria alcuna azione.

### Quali ID sono supportati per consentire ai clienti di completare una richiesta RGPD o CCPA di accesso e cancellazione per [!DNL Target]? {#section_F7D0EE4E6A28490FB20056A0D26118BC}

[!DNL Target] supporta i seguenti tipi di ID per individuare un profilo cliente:

| ID utente | Tipo ID dello spazio dei nomi | ID dello spazio dei nomi | Definizione |
|--- |--- |--- |--- |
| Experience Cloud ID (ECID) | Standard | 4 | Adobe Experience Cloud ID, precedentemente conosciuto come ID visitatore o Marketing Cloud ID. È possibile utilizzare l&#39;API JavaScript per individuare questo ID (consulta i dettagli di seguito). |
| ID TnT/ID cookie(TNTID) | Standard | 9 | Identificativo di Target impostato come cookie nel browser del visitatore. È possibile utilizzare l&#39;API JavaScript per individuare questo ID (consulta i dettagli di seguito). |
| ID di terze parti/ID CRM (THIRDPARTYID) | Specifico di Target | N/D | Se si fornisce a Target il proprio CRM o altre informazioni di identificazione univoche per i propri clienti. |

>[!NOTE]
>
>Sebbene [!DNL Target] supporti sia cookie di prima parte sia di terze parti di diversi domini, i cookie di prima parte sono consigliati solo per il RGPD e CCPA.[!DNL Target]

### Come avviene la gestione del consenso da parte di [!DNL Target]? {#section_C86BF5EE4FAA47039659850E7594A6BA}

I regolamenti RGPD e CCPA non cambiano i requisiti in merito a “quando” è necessario ottenere il consenso, ma piuttosto “come” ottenerlo. La strategia di consenso di ciascun cliente dipende dalle sue modalità di raccolta e utilizzo dei dati e dalla sua politica sulla privacy. La gestione del consenso non è supportata e non deve essere ottenuta tramite [!DNL Target] per RGPD e CCPA.

Attualmente, [!DNL Adobe] non offre una soluzione per la gestione dei consensi, ma sul mercato sono in fase di sviluppo diversi strumenti per soddisfare alcuni dei nuovi requisiti. For more information on privacy tools in general, including consent managers, see the [2017 Privacy Tech Vendor Report](https://iapp.org/media/pdf/resource_center/Tech-Vendor-Directory-1.4.1-electronic.pdf) on the *International Association of Privacy Professionals (iaap)* website.

[!DNL Target] fornisce supporto per la funzionalità opt-in tramite [!DNL Launch] per supportare la strategia di gestione dei consensi. La funzionalità opt-in consente ai clienti di controllare come e quando viene attivato il tag di [!DNL Target]. È inoltre presente un’opzione tramite [!DNL Launch] per pre-approvare il tag di [!DNL Target]. L’utilizzo di [!DNL Launch] per gestire l’opt-in rappresenta l’approccio consigliato. Esiste un ulteriore controllo granulare in [!DNL Launch] per nascondere alcuni elementi della pagina prima dell’attivazione di [!DNL Target] che potrebbe essere utile da sfruttare come parte della strategia di consenso.

For more information on GDPR, CCPA, and [!DNL Launch], see [The Adobe Privacy JavaScript Library and GDPR](https://www.adobe.io/apis/cloudplatform/gdpr/services/allservices.html). Inoltre, consulta la sezione precedente *Adobe Target e la funzionalità opt-in di Experience Platform Launch*.

### AdobePrivacy.js invia informazioni all&#39;API RGPD? {#section_1EB8A2BAAD31474C97C1D455F41DA739}

[!DNL AdobePrivacy.js] *non* invia tali informazioni all&#39;API. Farlo è compito del cliente. Questa libreria fornisce solo gli ID memorizzati nel browser per un visitatore specifico.

### Che cosa elimina l’azione removeIdentities? {#section_D3A1591EA1B84C499CE1563DEAF32448}

[!DNL removeIdentities] rimuove tali identità *solo* dal browser, e solo nel caso in cui la soluzione [!DNL Adobe] sia stata implementata.

Ad esempio, [!DNL Target] elimina i cookie che memorizzano gli ID, ma [!DNL Adobe Audience Manager] (AAM) non elimina l’ID demdex memorizzato in un cookie di terze parti.

### Quali informazioni devono essere incluse in una richiesta RGPD o CCPA di Target? {#section_D29A4744AE6344E68AD7710B185FD6D0}

Oltre ai requisiti del Servizio centrale di privacy, un messaggio RGPD o CCPA valido per [!DNL Target] contiene:

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
| Processing (Completa elaborazione) | Processing (Completa elaborazione) | Target ha ricevuto la richiesta RGPD o CCPA e la sta elaborando. |
| Completa | Non applicabile; contesto aziendale non applicabile | L’ID IMS nella richiesta RGPD o CCPA non viene mappato su alcun client di Target.<br>Tieni presente che alcune società hanno più ID IMS. Devi inviare l&#39;ID IMS in cui è stato fornito Target. |
| Completa | Non applicabile; contesto utente non trovato | L’ID fornito nella richiesta RGPD o CCPA per il visitatore o l’oggetto dati specifico non è presente nell’archivio dei profili di Target.<br>Nota che questo risultato si ottiene anche se si tenta di inviare un tipo di ID spazio dei nomi non supportato da Target (vedi sopra per gli ID supportati). |
| Errore | Messaggio di errore (i dettagli dipendono dal tipo di errore) | Errore durante il recupero o l&#39;eliminazione del profilo dati richiesto.<br>Errore durante il caricamento su Azure della richiesta di accesso. |

### Quale risposta invia Target all&#39;API RGPD per una richiesta di accesso? {#section_D96D8FBEAF9C4BDAA638215FAFE00763}

Le risposte alle richieste di accesso ai dati contengono un riassunto del profilo di [!DNL Target] per il visitatore in questione. Si noti che questo ritorno è inviato all’API RGPD di [!DNL Experience Cloud], che a sua volta invia una risposta ai Titolari del trattamento dei dati.

Un esempio di risposta API di accesso a [!DNL Target] potrebbe essere il seguente:

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
| jobId | Indica l’ID del lavoro RGPD o CCPA dall’API centrale RGPD. |
| imsOrgID | Fornisce un identificatore univoco per la tua azienda. |
| namespace | Denominato anche fonte di dati. Consulta “Quali ID sono supportati per aiutare i clienti a completare una richiesta di accesso e cancellazione RGPD o CCPA per Target?” in questo argomento. |
| type | Tipo di ID per il quale è stato richiesto l’accesso ai dati RGPD o CCPA. Target accetta diversi tipi di ID, alcuni dei quali sono standard e altri specifici di Target. Consulta “Quali ID sono supportati per aiutare i clienti a completare una richiesta di accesso e cancellazione RGPD o CCPA per Target?” in questo argomento. |
| value | L&#39;ID spazio dei nomi/sorgente dei dati. Consulta “Quali ID sono supportati per aiutare i clienti a completare una richiesta di accesso e cancellazione RGPD o CCPA per Target?” per i valori accettati. |
| integration code | I codici di integrazione sono nomi semplici per le origini dati e consentono di tracciarle più facilmente rispetto agli ID delle origini dati. |

Quando vengono forniti più valori per identificare i profili, ogni identificatore valido ha un file di profilo. I file di profilo sono inviati al Azure Blob centrale per RGPD attraverso l’API centrale RGPD, sotto forma di risposta JSON per il profilo di [!DNL Target].

Un esempio di codice JSON per un profilo di [!DNL Target] potrebbe avere l’aspetto seguente:

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
| Sample_Parameter | Molte informazioni nel profilo di [!DNL Target] sono caricate o fornite direttamente dal Titolare del trattamento dei dati. In questo esempio, è stato caricato un parametro nel profilo di [!DNL Target], utilizzando l’API di aggiornamento del profilo. Per ulteriori informazioni, consulta [Metodi per ottenere dati in Target](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md). |
| user.ReturnTimeOfDay | Questo campo standard include l&#39;ora del giorno dell&#39;ultima visita di ritorno dell&#39;utente. |
| firstSessionStart | Questo campo standard include l&#39;ora del giorno in cui è iniziata la prima sessione dell&#39;utente. |
| user.sessionCountScript | Molte informazioni nel profilo di [!DNL Target] sono caricate o fornite direttamente dal Titolare del trattamento dei dati. In questo esempio, uno script di profilo incrementa il numero di sessioni che il visitatore ha effettuato sul sito del Titolare del trattamento dei dati. Per ulteriori informazioni, consulta [Attributi del profilo](/help/c-target/c-visitor-profile/profile-parameters.md). |

>[!NOTE]
>
>La seguente è una versione ridotta di un profilo JSON di [!DNL Target], presentata a scopo illustrativo. Molti campi del profilo di [!DNL Target] non sono standard. Ciò che viene restituito dipende da quali informazioni si trovano in quel profilo specifico di visitatore.

### Target supporta l’omissione dell’IP? {#section_428907B0CD9842D9B245B38C66A53C6A}

Se scegli di utilizzarla come parte della strategia di implementazione RGPD o CCPA, [!DNL Target] supporta l’omissione dell’IP. Per ulteriori informazioni, consulta [Privacy](../../../c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md#concept_639482A343DB4963A6144378E1D8D7F0).

### Devo fare qualcosa per evitare che i miei dati vengano condivisi o venduti a terzi?

Target non è in grado di consentire ai clienti di condividere o vendere dati direttamente da Target a terzi, pertanto non esiste alcuna rinuncia alla vendita per Target.
