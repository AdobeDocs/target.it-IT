---
keywords: Adobe Experience Platform Web SDK;aep web sdk;aep sdk;ottimizzazione motore di ricerca;seo;edge cluster, central cluster;at.js;mbox.js;
description: Scoprite come funziona  Adobe Target, comprese informazioni sulle librerie JavaScript di Target (at.js e AEP Web SDK),  centri dati di Adobe e test SEO.
title: Come funziona Target?
feature: Panoramica
translation-type: tm+mt
source-git-commit: 2a06eccf27ce214a9d43bced25b15afbc291d814
workflow-type: tm+mt
source-wordcount: '2567'
ht-degree: 32%

---


# Come funziona Adobe Target

Scoprite come funziona [!DNL Adobe Target], comprese informazioni sulle librerie [!DNL Adobe Experience Platform Web SDK] e JavaScript (at.js e mbox.js). Questo articolo introduce anche i vari tipi di attività che potete creare utilizzando [!DNL Target]. È inoltre possibile apprendere la rete [!DNL Target] edge, l&#39;ottimizzazione SEO (Search Engine Optimization) e come [!DNL Target] rileva i bot.

## SDK Web della piattaforma Target e librerie JavaScript {#libraries}

[!DNL Target] si integra con i siti Web utilizzando le librerie JavaScript  [!DNL AEP Web SDK] o

* **Adobe Experience Platform Web SDK:** L’ [AEP Web ](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) SDK è una nuova libreria JavaScript lato client. L&#39;SDK Web AEP consente ai clienti di [!DNL Adobe Experience Cloud] interagire con i vari servizi della [!DNL Experience Cloud] (incluso [!DNL Target]) tramite [!DNL AEP] Edge Network.  Adobe consiglia a tutti i nuovi clienti [!DNL Target] di implementare [!DNL AEP Web SDK].
* **at.js:** La libreria  [at.js ](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17) è una libreria di implementazione per  [!DNL Target]. La libreria at.js migliora i tempi di caricamento delle pagine per le implementazioni Web e fornisce migliori opzioni di implementazione per le applicazioni a pagina singola. at.js viene aggiornato frequentemente con le nuove funzionalità.  Adobe consiglia a tutti i clienti che utilizzano at.js di aggiornare le implementazioni alla [versione più recente di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A).
* **mbox.js:**[](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md) la libreria mbox.js è la libreria di implementazione legacy per [!DNL Target]. La libreria mbox.js è supportata fino al 31 marzo 2021; tuttavia, non saranno disponibili aggiornamenti di funzionalità.

>[!IMPORTANT]
>
>Tutti i clienti devono effettuare la migrazione alla [!DNL AEP Web SDK] o all&#39;ultima versione di at.js. Per ulteriori informazioni, vedere [Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) o [Migra a at.js da mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA).

Fate riferimento a [!DNL AEP Web SDK] o at.js in ogni pagina del sito. Ad esempio, potete aggiungere una di queste librerie all’intestazione globale. In alternativa, è consigliabile utilizzare [ Platform Launch Adobe](https://experienceleague.adobe.com/docs/launch/using/overview.html) per implementare [!DNL Target].

Le seguenti risorse contengono informazioni dettagliate utili per implementare AEP Web SDK o at.js:

* [Estensione Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/launch/using/extensions-ref/adobe-extension/aep-extension/overview.html?lang=en#configure-the-aep-web-sdk-extension)
* [Implementare Target con Adobe Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md)

Ogni volta che un visitatore richiede una pagina ottimizzata per [!DNL Target], viene inviata una richiesta al sistema di targeting. La richiesta consente di determinare il contenuto da distribuire a tale visitatore. Questo processo avviene in tempo reale. Ogni volta che una pagina viene caricata, il sistema effettua e soddisfa una richiesta per il contenuto. Il contenuto è gestito dalle regole delle attività e delle esperienze controllate dagli addetti al marketing, e ne viene eseguito il targeting per i singoli visitatori del sito. Viene distribuito il contenuto al quale ogni visitatore del sito ha più probabilità di rispondere, di interagire con o di acquistare. I contenuti personalizzati consentono di massimizzare i tassi di risposta, i tassi di acquisizione e le entrate.

In [!DNL Target], ogni elemento della pagina è parte di un&#39;unica esperienza per l&#39;intera pagina. Ogni esperienza può includere più elementi sulla pagina.

Il contenuto visualizzato dai visitatori dipende dal tipo di attività creata:

### Test A/B

Il contenuto visualizzato in un test A/B di base viene scelto in modo casuale tra le esperienze assegnate all&#39;attività. Potete assegnare le percentuali di allocazione del traffico per ogni esperienza. Come risultato di questa suddivisione casuale del traffico, può richiedere una quantità significativa di traffico iniziale prima che le percentuali si livellino. Ad esempio, se crei due esperienze, quella di partenza verrà scelta in modo casuale. Se il traffico è limitato, è possibile che la percentuale di visitatori tenda in modo più netto verso una delle due esperienze. Con l&#39;aumento del traffico, le percentuali sono pari.

Puoi specificare target basati su percentuali per ogni esperienza. In questo caso, viene generato un numero casuale, utilizzato per scegliere l’esperienza da visualizzare. Le percentuali risultanti potrebbero non corrispondere esattamente ai target specificati. Con l’aumentare del traffico, le esperienze risulteranno tuttavia suddivise in modo più rispondente agli obiettivi.

1. Un cliente richiede una pagina dal server e la visualizza nel browser.
2. Un cookie di prime parti viene impostato nel browser del cliente per memorizzare il comportamento del cliente.
3. La pagina effettua una chiamata al sistema di targeting.
4. Il contenuto viene visualizzato in base alle regole della relativa attività.

Consulta [Creare un test A/B](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) per ulteriori informazioni.

### Allocazione automatica

Allocazione automatica identifica un vincitore tra due o più esperienze. Allocazione automatica riassegna automaticamente più traffico all&#39;esperienza vincente per aumentare le conversioni mentre il test continua a essere eseguito e imparare.

Per ulteriori informazioni, consulta [ Allocazione automatica](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4).

### Targeting automatico (AT)

Auto-Target utilizza l&#39;apprendimento automatico avanzato per selezionare tra più esperienze definite dall&#39;esperto di marketing ad alte prestazioni. Mediante il targeting automatico, ogni visitatore offre l&#39;esperienza più personalizzata. La distribuzione delle esperienze si basa sui profili dei singoli clienti e sul comportamento dei visitatori precedenti con profili simili. Utilizzate Auto-Target per personalizzare il contenuto e stimolare le conversioni.

Per ulteriori informazioni, consulta [Targeting automatico](/help/c-activities/auto-target/auto-target-to-optimize.md).

### Personalizzazione automatizzata

 Automated Personalization (AP) combina offerte o messaggi e utilizza l&#39;apprendimento automatico avanzato per far corrispondere diverse varianti di offerta a ciascun visitatore. La distribuzione delle esperienze si basa sui profili dei clienti individuali per personalizzare i contenuti e promuovere l&#39;incremento.

Per ulteriori informazioni, consulta [Personalizzazione automatizzata](/help/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9).

### Targeting esperienza (XT)

La funzione Targeting esperienza (XT) fornisce contenuti a un pubblico specifico basato su una serie di regole e criteri definiti dagli addetti al marketing.

Il Targeting dell’esperienza, tra cui il geotargeting, è utile per definire regole che rivolgono un’esperienza o un contenuto specifico a un determinato pubblico. È possibile definire diverse regole in un’attività per fornire diverse varianti di contenuto a tipi di pubblico diversi. Quando i visitatori visualizzano il tuo sito, la funzione Targeting esperienza (XT) li valuta per determinare se soddisfano i criteri impostati. Se soddisfano i criteri, vengono inclusi nell&#39;attività e viene visualizzata l&#39;esperienza progettata per i tipi di pubblico idonei. Puoi creare esperienze per più tipi di pubblico all&#39;interno di una singola attività.

Per ulteriori informazioni, vedere [Targeting delle esperienze](/help/c-activities/t-experience-target/experience-target.md#task_A53DF336CB9F4D7BB87EF2106099EFC4).

### Test multivariato (MVT)

Multivariate Testing (MVT) confronta combinazioni di offerte in elementi di una pagina per determinare quale combinazione offre le prestazioni migliori per un pubblico specifico. MVT aiuta a identificare quale elemento influisce maggiormente sul successo dell&#39;attività.

Per ulteriori informazioni, consulta [Test multivariato](/help/c-activities/c-multivariate-testing/multivariate-testing.md#concept_628695CDC71B449B8DCC2F5654C11499).

### Consigli

Le attività di generazione dei consigli visualizzano automaticamente prodotti o contenuti che potrebbero interessare i clienti in base alle loro attività precedenti o ad altri algoritmi. I consigli aiutano a indirizzare i clienti verso elementi rilevanti di cui potrebbero non essere a conoscenza.

Consulta [Consigli](/help/c-recommendations/recommendations.md#concept_7556C8A4543942F2A77B13A29339C0C0) per ulteriori informazioni.

## Rete periferica {#concept_0AE2ED8E9DE64288A8B30FCBF1040934}

Un &quot;Edge&quot; è un&#39;architettura di servizio geograficamente distribuita che assicura tempi di risposta ottimali ai visitatori che richiedono contenuti, indipendentemente da dove si trovano in tutto il mondo.

Per migliorare i tempi di risposta, [!DNL Target] Bordi la logica di attività solo host, i profili memorizzati nella cache e le informazioni sulle offerte.

I database delle attività e dei contenuti, i dati [!DNL Analytics], le API e le interfacce utente degli esperti di marketing sono memorizzati  cluster centrali del Adobe. Gli aggiornamenti vengono quindi inviati ai bordi [!DNL Target]. I cluster centrali e i cluster Edge vengono sincronizzati automaticamente per aggiornare continuamente i dati dell&#39;attività memorizzati nella cache. Tutti i modelli 1:1 sono inoltre memorizzati su ciascun bordo, per cui anche le richieste più complesse possono essere elaborate sul bordo.

Ogni cluster Edge dispone di tutte le informazioni necessarie per rispondere alla richiesta di contenuto del visitatore e tenere traccia dei dati di analisi su tale richiesta. Le richieste dei visitatori vengono indirizzate al cluster Edge più vicino.

Per ulteriori informazioni, vedi il documento [Panoramica sulla sicurezza di Adobe Target](https://www.adobe.com/content/dam/cc/en/security/pdfs/AdobeTargetSecurityOverview.pdf).

La soluzione [!DNL Target] è ospitata  centri dati di proprietà del Adobe e  affittati dal Adobe in tutto il mondo.

Le posizioni cluster centrali contengono sia un centro di raccolta dati che un centro di elaborazione dati. Le posizioni cluster Edge contengono solo un centro di raccolta dati. Ogni suite di rapporti viene assegnata a un centro di elaborazione dati specifico.

I dati dell&#39;attività del sito cliente vengono raccolti dai sette cluster Edge più vicini. Questi dati vengono indirizzati alla destinazione cluster centrale predeterminata del cliente (una delle tre posizioni seguenti: Oregon, Dublino, Singapore) per l&#39;elaborazione. I dati del profilo del visitatore vengono memorizzati nel cluster Edge più vicino al visitatore del sito. Le posizioni dei cluster periferici includono la Central Cluster e Virginia, Amsterdam, Sydney, Tokyo e Hong Kong.

Invece di rispondere a tutte le richieste di targeting da una singola posizione, le richieste vengono elaborate dal cluster Edge più vicino al visitatore. Questo processo contribuisce a ridurre l&#39;impatto dei tempi di viaggio in rete/su Internet.

![Mappa dei tipi di server di Target](/help/c-intro/assets/target-servers.png)

[!DNL Target] I cluster centrali, ospitati  Amazon Web Services (AWS), includono:

* Oregon, USA
* Dublin (Irlanda)
* Repubblica di Singapore

[!DNL Target] Edge Clusters, ospitato su AWS, include:

* Mumbai, India
* Tokyo, Giappone
* Virginia, Stati Uniti
* Oregon, USA
* Sydney, Australia
* Dublin (Irlanda)
* Repubblica di Singapore

Il servizio [!DNL Target Recommendations] è ospitato in un centro dati [!DNL Adobe] dell&#39;Oregon.

>[!IMPORTANT]
>
>[!DNL Adobe Target] al momento non dispone di un cluster Edge in Cina e le prestazioni del visitatore continuano a essere limitate per  [!DNL Target] i clienti in Cina. A causa del firewall e dell&#39;assenza di Edge Clusters nel paese, le esperienze dei siti con [!DNL Target] implementato possono essere influenzate. Le esperienze possono essere lente per il rendering e i caricamenti di pagina possono essere influenzati. Inoltre, gli esperti di marketing potrebbero rilevare la latenza durante l&#39;utilizzo dell&#39;interfaccia di authoring [!DNL Target].

Se necessario,   [!DNL Target] Edge Clusters. Per ulteriori informazioni, vedere [ inserire nell&#39;elenco Consentiti nodi periferici di Target](/help/c-implementing-target/c-considerations-before-you-implement-target/allowlist-edges.md).

## Esperienza utente protetta {#concept_40A5E781D90A41E4955F80EA9E5F8F96}

Adobe garantisce un alto grado di affidabilità per la disponibilità e le prestazioni dell’infrastruttura di targeting. Tuttavia, un&#39;interruzione delle comunicazioni tra il browser di un visitatore e  server del Adobe può causare un&#39;interruzione nella distribuzione dei contenuti.

Per evitare interruzioni del servizio e problemi di connettività, tutte le posizioni sono configurate in modo da includere il contenuto predefinito (definito dal client). Questo contenuto predefinito viene visualizzato se il browser dell&#39;utente non è in grado di connettersi a [!DNL Target].

Non vengono apportate modifiche alla pagina se il browser dell’utente non riesce a collegarsi entro l’intervallo di timeout definito (per impostazione predefinita, 15 secondi). Se questa soglia di timeout viene raggiunta, viene visualizzato il contenuto di posizione predefinito.

Adobe tutela l’esperienza utente attraverso l’ottimizzazione e la salvaguardia delle prestazioni.

* Adobe garantisce i benchmark prestazionali basati sugli standard di settore, come garantiti dallo SLA di Adobe.
* La rete Edge assicura una distribuzione tempestiva dei dati.
* Adobe utilizza un approccio multilivello per garantire che le applicazioni forniscano il livello massimo di disponibilità e di affidabilità ai clienti.
* [!DNL Target] Consulting offre assistenza nell’implementazione e supporto continuo per il prodotto.

## Test di usabilità per l’ottimizzazione per i motori di ricerca (SEO){#concept_C0C865663CAB4251B66A1F250FD25E6A}

Le funzionalità di test di [!DNL Adobe Target] sono conformi alle linee guida dei motori di ricerca.

Google incoraggia il test degli utenti. Google afferma nella sua documentazione che A/B e Multivariate Testing non danneggia le classificazioni dei motori di ricerca biologici se si seguono determinate linee guida.

Per ulteriori informazioni, consulta le seguenti risorse di Google:

* [Website testing and Google Search (Test di sito web e ricerca Google)](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html)
* [Esperimenti e cloaking](https://support.google.com/analytics/answer/2576845?hl=en&amp;ref_topic=1745207)

Le linee guida sono state pubblicate su [Google Webmaster Central Blog](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html). Il post risale al 2012, ma rimane comunque la dichiarazione più recente di Google su questa questione e le linee guida restano valide.

* **Nessun occultamento**: Il mascheramento mostra un set di contenuti agli utenti e un set di contenuti diverso ai bot dei motori di ricerca. Il rivestimento viene realizzato identificando specificamente i bots e somministrando loro intenzionalmente contenuti diversi.

   [!DNL Target]La piattaforma è configurata per trattare i bot dei motori di ricerca allo stesso modo di qualsiasi utente. Di conseguenza, i bot possono essere inclusi nelle attività se i bot sono selezionati in modo casuale e &quot;vedere&quot; le variazioni del test.

* **Use rel=&quot;canonico&quot;**: A volte un test A/B deve essere impostato utilizzando URL diversi per le varianti. In questi casi, tutte le varianti devono contenere un tag `rel="canonical"` che fa riferimento all’URL originale (di controllo). Ad esempio, supponete che  Adobe stia eseguendo il test della propria home page utilizzando URL diversi per ciascuna variante. Il seguente tag canonico per la pagina principale viene inserito nel tag `<head>` per ciascuna delle varianti:

   `<link rel="canonical" href="https://www.adobe.com" />`

* **Utilizzare i reindirizzamenti** 302 (temporanei): Nei casi in cui sono utilizzati URL separati per le pagine di variazione in un test, Google consiglia di utilizzare un reindirizzamento 302 per indirizzare il traffico verso le varianti di test. Il reindirizzamento 302 indica ai motori di ricerca che il reindirizzamento è temporaneo ed è attivo solo finché il test è in esecuzione.

   Un reindirizzamento 302 è un reindirizzamento lato server e [!DNL Target], insieme alla maggior parte dei provider di ottimizzazione, utilizza funzionalità lato client. Pertanto, si tratta di un&#39;area in cui [!DNL Target] non è completamente conforme alle raccomandazioni di Google. Questa pratica, tuttavia, interessa solo una piccola parte dei test. L&#39;approccio standard per l&#39;esecuzione di test tramite [!DNL Target] chiamate per la modifica del contenuto all&#39;interno di un singolo URL, pertanto non è necessario eseguire un reindirizzamento. In alcuni casi, i client devono usare più URL per rappresentare le loro varianti di test. In questi casi, [!DNL Target] utilizza il comando JavaScript `window.location`. Questo comando indirizza gli utenti al test delle varianti, il che non indica esplicitamente se il reindirizzamento è 301 o 302.

    Adobe continua a cercare soluzioni valide per allinearsi completamente con le linee guida dei motori di ricerca. Per i client che devono utilizzare URL separati per il test,  Adobe è convinto che la corretta implementazione dei tag canonici riduca il rischio associato a questo approccio.

* **Eseguire esperimenti solo se necessario**:  Adobe ritiene &quot;necessario il tempo necessario&quot; per raggiungere la rilevanza statistica. [!DNL Target][ fornisce best practice](https://docs.adobe.com/content/target-microsite/testcalculator.html) per determinare quando un test ha raggiunto questo obiettivo.  Adobe consiglia di includere l’implementazione hardcoded dei test vincenti nel flusso di lavoro di test e di allocare le risorse appropriate.

   L&#39;utilizzo della piattaforma [!DNL Target] per &quot;pubblicare&quot; i test vincenti non è consigliato come soluzione permanente. Se il test vincente viene pubblicato per il 100% degli utenti il 100% del tempo, questo approccio può essere utilizzato mentre il processo di hardcoding del test vincente viene completato.

   È importante considerare anche le modifiche apportate dal test. Il semplice aggiornamento del colore dei pulsanti o di altri elementi secondari non basati su testo sulla pagina non influenza le classificazioni organiche. Tuttavia, le modifiche al testo devono essere hardcoded.

   È inoltre importante considerare l&#39;accessibilità della pagina che stai testando. Se la pagina non è accessibile ai motori di ricerca e non è mai stata progettata per classificare nella ricerca organica, non si applica nessuna delle considerazioni di cui sopra. Ad esempio, una pagina di destinazione dedicata per una campagna e-mail.

Google afferma che seguendo queste linee guida “i test dovrebbero avere un impatto minimo o nullo sul tuo sito nei risultati di ricerca”.

Oltre a queste linee guida, Google fornisce anche una guida in più nella documentazione del suo strumento Esperimenti sui contenuti:

* “Le varianti di pagina devono conservare lo spirito dei contenuti delle pagine originali. e non devono alterare il significato o la percezione generale che gli utenti hanno dei contenuti originali.”

Google dichiara, a titolo di esempio, che “se la pagina originale di un sito presenta parole chiave non correlate alle combinazioni mostrate agli utenti, possiamo rimuovere il sito dal nostro indice”.

 Adobe ritiene che sarebbe difficile modificare involontariamente il significato del contenuto originale nelle varianti di prova. Tuttavia,  Adobe consiglia di conoscere i temi delle parole chiave presenti in una pagina e di mantenerli aggiornati. Le modifiche al contenuto di una pagina, in particolare l’aggiunta o l’eliminazione di parole chiave rilevanti, possono influenzare la classificazione dell’URL nella ricerca organica.  Adobe consiglia di interagire con il partner SEO come parte del protocollo di test.

## Bot {#bots}

 Adobe [!DNL Target] utilizza la metrica [DeviceAtlas](https://deviceatlas.com/device-data/user-agent-tester/) &quot;isRobot&quot; per rilevare i bot noti in base alla stringa agente utente passata nell&#39;intestazione della richiesta.

>[!NOTE]
>
> Per le richieste [!DNL Server-Side], il valore passato nel nodo &quot;Contesto&quot; della richiesta [è precedenza rispetto alla stringa agente utente per il rilevamento di bot.](https://developers.adobetarget.com/api/delivery-api/#tag/Delivery-API)

Il traffico identificato come generato da un bot continua a ricevere contenuto. I robot vengono trattati come un utente normale per garantire che [!DNL Target] sia in linea con le linee guida SEO. Tuttavia, l’utilizzo di traffico da bot trattato come utenti normali può sfalsare i test A/B o gli algoritmi di personalizzazione. Pertanto, se nell&#39;attività [!DNL Target] viene rilevato un bot noto, il traffico viene trattato in modo leggermente diverso. La rimozione del traffico da bot genera misurazioni più accurate delle attività degli utenti effettivi.

Nello specifico, per il traffico bot noto [!DNL Target] non:

* non crea né recupera un profilo visitatore;
* non registra eventuali attributi di profilo né esegue gli script di profilo;
* non consulta i segmenti Adobe Audience Manager (AAM) (se applicabile);
* Utilizzate il traffico bot per la modellazione e la distribuzione di contenuti personalizzati per attività Recommendations, Auto-Target,  Automated Personalization o Auto-Allocate
* non registra a fini di reporting una visita all’attività;
* I dati di registro da inviare alla piattaforma [!DNL Adobe Experience Cloud]
