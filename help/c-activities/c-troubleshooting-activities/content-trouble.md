---
keywords: debug mbox;risoluzione dei problemi di mbox;problemi di mbox;visualizzazione momentanea;mboxDebug;mboxTrace;token;debugger;priorità;priorità di attività;Adobe Experience Cloud Debugger;orderConfirmPage mbox;SiteCatalyst acquisto di mbox;articolo più venduto
description: Trovate suggerimenti per risolvere i problemi se nella pagina non viene visualizzato il contenuto previsto. Scoprite come eseguire il debug della distribuzione dei contenuti in  Adobe Target.
title: Come Posso Risolvere I Problemi Di Distribuzione Dei Contenuti?
feature: Activities
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '1413'
ht-degree: 60%

---


# Risolvere i problemi relativi alla distribuzione dei contenuti

Se nella pagina non viene visualizzato il contenuto previsto, puoi adottare alcune misure per eseguire il debug della distribuzione dei contenuti.

* Controlla con attenzione il codice relativo all’attività o alla campagna. Un errore di battitura o di altro tipo potrebbe causare la mancata visualizzazione del contenuto previsto.
* Utilizzate mboxTrace o mboxDebug per risolvere i problemi della richiesta [!DNL Target].
* Utilizzate Adobe Experience Cloud Debugger, uno strumento di facile utilizzo che fornisce molte delle stesse informazioni di mboxDebug, per risolvere i problemi della richiesta [!DNL Target].

mboxDebug è particolarmente utile quando si sta configurando [!DNL Target] sulla pagina per essere certi che la richiesta [!DNL Target] sia attiva e il cookie impostato. Tuttavia, non fornisce il livello di dettaglio necessario durante il debug della distribuzione dei contenuti. Se l’attività non viene visualizzata nella pagina o un contenuto indesiderato viene visualizzato, esamina ed esegui il debug della pagina nel dettaglio tramite mboxTrace.

## Recuperare il token di autorizzazione da utilizzare con gli strumenti di debug {#section_BED130298E794D1FA229DB7C3358BA54}

Dato che in mboxTrace e mboxDebug è possibile esporre dati sulla campagna e sul profilo a soggetti esterni, è necessario un token di autorizzazione. Il token di autorizzazione può essere recuperato nell’interfaccia utente di [!DNL Target]. Il token è valido per sei ore.

Per generare un token di autenticazione è necessario disporre di una delle seguenti autorizzazioni utente:

* Autorizzazione di almeno [!UICONTROL Editor] (o [!UICONTROL Approver])

   Per ulteriori informazioni per i clienti [!DNL Target Standard], vedere [Specificare ruoli e autorizzazioni](/help/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) in *Utenti*. Per ulteriori informazioni per i clienti [!DNL Target Premium], vedere [Configurare le autorizzazioni aziendali](/help/administrating-target/c-user-management/property-channel/properties-overview.md).

* Ruolo amministratore nell’area di lavoro/a livello di profilo di prodotto

   Le aree di lavoro sono disponibili solo per i clienti [!DNL Target Premium]. Per ulteriori informazioni, vedere [Configurare le autorizzazioni aziendali](/help/administrating-target/c-user-management/property-channel/properties-overview.md).

* Diritti di amministratore (autorizzazione Sysadmin) a livello di prodotto [!DNL Adobe Target]

Per recuperare il token di autorizzazione:

1. Fare clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]**.
1. Nella sezione Strumenti debugger, fare clic su **[!UICONTROL Genera nuovo token di autenticazione]**.

   ![Genera nuovo token di autenticazione](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/assets/debugger-auth-token.png)

1. Aggiungi il token generato come parametro nell’URL per abilitare uno degli strumenti di debug avanzati.

   ![Token di autorizzazione](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/assets/auth-token.png)

## mboxTrace {#section_256FCF7C14BB435BA2C68049EF0BA99E}

mboxTrace consente di ricevere le informazioni di traccia allegate alle risposte [!DNL Target]. Le informazioni di trace riflettono il risultato di una [!DNL Target] chiamata (ad esempio, una conversione o un&#39;impressione) ed eventuali dati aggiuntivi che possono aiutare a determinare il motivo per cui questo particolare risultato è stato ottenuto, ad esempio un insieme di rami disponibili tra i quali è stata effettuata la selezione in una campagna. Esegui il debug della distribuzione dei contenuti con queste informazioni.

Sono disponibili i seguenti parametri:

| Opzioni mboxTrace | Risultato |
|--- |--- |
| `?mboxTrace=console` | Visualizzazione nel registro della console come oggetti.<br>Per at.js, invece di aprire una nuova finestra del browser o di eseguire l’output sulla console come in mbox.js, sarà necessario controllare la richiesta di rete e guardare in Anteprima (Chrome) o Risposta (Firefox). |
| `?mboxTrace=json` | Visualizzazione nel registro della console come stringa letterale JSON |
| `?mboxTrace=window` | Visualizzazione in una finestra popup come stringa JSON |
| `?mboxTrace=disable` | Disattiva la modalità di sessione di tracciamento |

**Esempio di chiamata mboxTrace**

`https://www.mysite.com/page.html?mboxTrace=window&authorization=f543abf-0111-4061-9619-d41d665c59a6`

Il risultato mostra informazioni estremamente dettagliate sul contenuto. mboxTrace mostra i dettagli sulla tua campagna o attività e profilo. Inoltre, fornisce uno snapshot del profilo prima dell’esecuzione e uno snapshot di ciò che è stato modificato dopo l’esecuzione. In aggiunta, mostra quali campagne o attività sono state valutate per ogni posizione.

Alcune delle informazioni includono ID di destinazione e di segmento associati e non associati:

* **SegmentId**: ID dei segmenti, dalla libreria di segmenti riutilizzabili o anonimi, creati per la campagna specifica.
* **TargetId**: ID delle destinazione, dalla libreria delle espressioni di destinazione o da destinazioni anonime, per tutti i segmenti della campagna.
* **Unmatched** (nessuna corrispondenza): in questa chiamata la richiesta non era qualificata per i segmenti o le destinazioni specificati.
* **Matched** (con corrispondenza): la richiesta era qualificata per i segmenti o le destinazioni specificati.

**Utilizzo di mboxTrace nelle pagine** delle raccomandazioni: L&#39;aggiunta di mboxTrace come parametro di query sulle pagine con raccomandazioni sostituisce la progettazione Recommendations sulla pagina con una finestra di dettagli mboxTrace, che visualizza informazioni approfondite sulle raccomandazioni, tra cui:

* Consigli restituiti e consigli richiesti
* Chiave utilizzata, e se sta generando consigli
* Consigli generati da criteri e consigli di backup
* Configurazione dei criteri
* Esclusioni e inclusioni applicate
* Regole di raccolta

Non devi includere `=console`, `=json` o `=window` nel parametro di query. Una volta completati i dettagli mboxTrace, aggiungi `=disable` e premi **[!UICONTROL Invio]** per tornare alla modalità di visualizzazione normale.

mboxTrace non influenza il normale funzionamento e aspetto del tuo sito. I visitatori vedranno la tua solita struttura dei consigli.

## mboxDebug {#mboxdebug}

Per utilizzare mboxDebug, aggiungi un parametro mboxDebug alla fine dell’URL. La tabella seguente contiene informazioni sui parametri URL relativi alla risposta [!DNL Target].

>[!NOTE]
>
>Alcuni parametri mboxDebug sono disponibili con o senza autenticazione.

| Parametri URL | Finalità |
|--- |--- |
| `mboxDebug=1` | Debugger<br>L&#39;aggiunta di questo parametro a qualsiasi URL con richieste Target definite apre una finestra a comparsa con preziosi dettagli di debug. Vengono inserite informazioni sui cookie, valori PCid e ID di sessione e sono visibili tutti gli URL Fate clic su un URL di richiesta Target per visualizzare la risposta per la richiesta [!DNL Target]. Maggiori dettagli sono disponibili in [mbox_debug.pdf](/help/assets/mbox_debug.pdf). |
| `mboxDebug=x-cookie` | Modifica il cookie |
| `mboxDisable=1` | Disattiva le mbox sulla pagina |
| `mboxDebug=x-profile` | Visualizza i profili impostati. |
| `mboxDebug=x-time` | Mostra il tempo di risposta per ogni richiesta [!DNL Target] |
| `mboxOverride.browserIp=<Insert IP address>` | Testa geotargeting<br>Testa il geotargeting con questo parametro URL. Digita un indirizzo IP come valore per questo attributo e il geotargeting di Test&amp;Target valuterà tale indirizzo IP rispetto a qualsiasi geotargeting o segmentazione impostata in una campagna. |

>[!NOTE]
>
>Verificare che il frammento URL sia dopo i parametri della stringa di query. Tutto ciò che segue la prima `#` è un identificatore di frammento e causa il mancato funzionamento dei parametri di debug.

## Adobe Experience Cloud Debugger {#section_A2798ED3A431409690A4BE08A1BFCF17}

Il debugger di Adobe Experience Cloud facilita e velocizza la comprensione dell&#39;implementazione di Target. Puoi visualizzare rapidamente la configurazione della libreria, esaminare le richieste per verificare che i parametri personalizzati vengano passati correttamente, attivare la registrazione della console e disattivare tutte le richieste Target. Effettuate l&#39;autenticazione nel Experience Cloud  e potete utilizzare il potente strumento MboxTrace per ispezionare le qualifiche dell&#39;attività e dell&#39;audience nonché il profilo del visitatore.

Per ulteriori informazioni, vedi i video di formazione seguenti:

Per ulteriori informazioni, vedere [Debug at.js utilizzando Adobe Experience Cloud Debugger](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-debugging-atjs/target-debugging-atjs.md).

## Se target.js non viene caricato durante la distribuzione {#section_ABBA5EFDFFB749D8BEE172DB1F973058}

Se target.js non viene caricato durante la distribuzione, mbox.js invia al visitatore il cookie “em-disabled”. Questo cookie impedisce alle offerte create tramite il Compositore esperienza visivo di essere visualizzate sul sito. I visitatori con questo cookie non vedono il contenuto del test né vengono conteggiati in tali rapporti di attività. Tutti gli altri contenuti dell’offerta (da campagne in Target Classic per esempio) continuano ad essere caricati. Il cookie ha una durata di 30 minuti dal momento del caricamento non riuscito.

## Gli articoli più venduti non compaiono in Consigli  {#section_3920C857270A406C80BE6CBAC8221ECD}

La chiamata *`SiteCatalyst: purchase`* non può essere utilizzata per i dati di traffico dell&#39;algoritmo di acquisto. Utilizzate invece la chiamata *`orderConfirmPage`*.

## Verifica priorità attività {#section_3D0DD07240F0465BAF655D0804100AED}

Le attività basate su moduli create con [!DNL Target Standard/Premium] potrebbero entrare in conflitto con le attività create nell&#39;interfaccia [!DNL Target Classic] che hanno la stessa priorità e utilizzano la stessa richiesta [!DNL Target].

## Il codice personalizzato non produce i risultati previsti in Internet Explorer 8. {#section_FAC3651F19144D12A37A3E4F14C06945}

Target non supporta più Internet Explorer 8.

## Il contenuto JavaScript fornito dalla richiesta [!DNL Target] globale non viene caricato quando si utilizza mbox.js. {#section_03EC9B9C410B4F52A7FCD81840311709}

Effettua l’aggiornamento a [!DNL mbox.js] versione 58 o successiva.

mbox.js versione 58 e successive esegue contenuto non JavaScript per la richiesta globale [!DNL Target] subito dopo la presenza del tag HTML `BODY`. Il contenuto JavaScript all&#39;interno dei tag `<script>` per la richiesta globale [!DNL Target] viene eseguito dopo l&#39;attivazione dell&#39;evento `DOMContentLoaded`. Questo ordine di distribuzione dei contenuti garantisce che il contenuto JavaScript per la richiesta globale [!DNL Target] sia consegnato e rappresentato correttamente.

## Il cookie di destinazione non viene impostato {#section_77AFEB541C0B495EB67E29A4475DF960}

Se nel sito è presente un sottodominio, ad esempio [!DNL us.domain.com], ma è necessario impostare il cookie di Target su [!DNL domain.com] (anziché [!DNL us.domain.com]), devi sovrascrivere l’impostazione `cookieDomain`. Per ulteriori informazioni, consulta [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md).

## Il contenuto di Target viene visualizzato momentaneamente o non viene visualizzato se un elemento fa anche parte della personalizzazione AEM. {#section_9E1DABEB75AB431FB9F09887E6DD07D3}

Il contenuto di Target potrebbe essere visualizzato momentaneamente o non essere visualizzato, se un elemento DOM fa parte del targeting di personalizzazione di Adobe Experience Manager (AEM) e di un’attività di Target.

Per ovviare a questo problema, puoi disabilitare la personalizzazione AEM nelle pagine in cui Target è in esecuzione.

## Errore nella consegna di offerte di reindirizzamento e offerte remote a causa di un URL non valido.  {#section_7D09043B687F43B39DAEDF17D00375AC}

Se l’offerta di reindirizzamento o l’offerta remota utilizza un URL non valido, la sua consegna potrebbe non riuscire.

Per le offerte di reindirizzamento, la risposta [!DNL Target] può contenere `/* invalid redirect offer URL */`

Oppure

Per le offerte remote, la risposta [!DNL Target] può contenere `/* invalid remote offer URL */`

È possibile controllare la risposta [!DNL Target] nel browser o utilizzando mboxTrace. Per ulteriori informazioni sugli URL validi, consulta [https://tools.ietf.org/html/std66](https://tools.ietf.org/html/std66).

## Le richieste Target non vengono attivate sul sito.

at.js non attiva le richieste Target se utilizzi un doctype non valido. at.js richiede il doctype HTML5.

## Video di formazione

I video seguenti contengono ulteriori informazioni sui concetti descritti in questo articolo.

### Aggiungi estensione  ![Badge di esercitazione](/help/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/23114t2/)

### Debug di destinazione di base ![badge di esercitazione](/help/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/23115t2/)

### Traccia mbox ![Badge delle esercitazioni](/help/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/23113t2/)