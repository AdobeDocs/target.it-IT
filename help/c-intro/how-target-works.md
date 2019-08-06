---
description: Adobe Target si integra con i siti Web mediante una delle due librerie JavaScript. at.js o mbox.js
keywords: Panoramica e riferimento;SEO;ottimizzazione per motori di ricerca
seo-description: Adobe Target si integra con i siti Web mediante una delle due librerie JavaScript. at.js o mbox.js
seo-title: Come funziona Adobe Target
solution: Target
subtopic: Introduzione
title: Come funziona Adobe Target
topic: Standard
uuid: 01c0072d-f77d-4f14-935b-8633f220db7b
translation-type: tm+mt
source-git-commit: 5ca58dd62ba8c35eb96a50919fd02994c4dbff16

---


# Come funziona Adobe Target{#how-adobe-target-works}

Informazioni su come funziona Adobe Target, comprese informazioni sulle librerie JavaScript di Target (at.js e mbox.js) e sui vari tipi di attività inclusi in Target.

## Librerie JavaScript di Target {#libraries}

Adobe Target si integra con i siti Web tramite una delle due librerie javascript: at. js o mbox. js

* **at.js:** la [libreria at.js](../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17) è la nuova libreria di implementazione per Target. La libreria at.js migliora i tempi di caricamento delle pagine per le implementazioni Web e fornisce migliori opzioni di implementazione per le applicazioni a pagina singola. at.js è la libreria di implementazione consigliata e viene aggiornata frequentemente con nuove funzionalità. Si consiglia a tutti i clienti di implementare o eseguire la migrazione alla [versione più recente di at.js](../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A).
* **mbox.js:** la libreria mbox.js è la libreria di implementazione legacy per Target. La libreria mbox.js è ancora supportata, ma non ci saranno aggiornamenti di funzionalità.

>[!IMPORTANT]
>
>Tutti i clienti devono migrare a at.js. Per ulteriori informazioni, consulta [Migrazione a at.js da mbox.js](../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA)

È necessario fare riferimento al file di libreria javascript di Target in ogni pagina del sito. Ad esempio, puoi aggiungerlo all’intestazione globale. In alternativa, valutate l'utilizzo [di Adobe Launch tag manager](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md)

Ogni volta che un visitatore richiede una pagina ottimizzata per Target, viene inviata una richiesta al sistema di targeting per determinare quale contenuto distribuire al visitatore. Questo processo si verifica in tempo reale: ogni volta che viene caricata una pagina, viene effettuata e soddisfatta una richiesta di contenuto dal sistema. Il contenuto è gestito dalle regole delle attività e delle esperienze controllate dagli addetti al marketing, e ne viene eseguito il targeting per i singoli visitatori del sito. Per massimizzare i tassi di risposta e di acquisizione e il ricavo, viene distribuito il contenuto per il quale è più probabile che si verifichi una risposta, un’interazione e infine un acquisto da parte del visitatore del sito.

In Target, ogni elemento sulla pagina è parte di un’unica esperienza. Ogni esperienza può includere più elementi sulla pagina.

Il contenuto visualizzato ai visitatori dipende dal tipo di attività che create:

### Test A/B

Consulta [Creare un test A/B](../c-activities/t-test-ab/t-test-create-ab/test-create-ab.md#task_68C8079BF9FF4625A3BD6680D554BB72) per ulteriori informazioni.

Il contenuto visualizzato in un test A/B di base viene scelto in modo casuale tra le risorse assegnate alle attività, in base alle percentuali selezionate per ogni esperienza. Come risultato di questa suddivisione casuale del traffico, è possibile che sia richiesta una quantità notevole di traffico iniziale prima che le percentuali si livellino. Ad esempio, se crei due esperienze, quella di partenza verrà scelta in modo casuale. Se il traffico è limitato, è possibile che la percentuale di visitatori tenda in modo più netto verso una delle due esperienze. Con l’aumento del traffico, le percentuali tendono a equilibrarsi.

Puoi specificare target basati su percentuali per ogni esperienza. In questo caso, viene generato un numero casuale, utilizzato per scegliere l’esperienza da visualizzare. Le percentuali risultanti potrebbero non corrispondere esattamente ai target specificati. Con l’aumentare del traffico, le esperienze risulteranno tuttavia suddivise in modo più rispondente agli obiettivi.

1. Un cliente richiede una pagina dal server e la visualizza nel browser.
2. Nel browser del cliente viene impostato un cookie di prime parti che ne memorizza il comportamento.
3. La pagina effettua una chiamata al sistema di targeting.
4. Il contenuto viene visualizzato in base alle regole dell'attività.

### Allocazione automatica

Per ulteriori informazioni, consulta [ Allocazione automatica](../c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4).

L’allocazione automatica identifica un vincitore tra due o più esperienze e, di conseguenza, ridistribuisce automaticamente più traffico per aumentare le conversioni, mentre il test continua a essere eseguito e ad apprendere.

### Targeting automatico (AT)

Per ulteriori informazioni, consulta [Targeting automatico](../c-activities/auto-target-to-optimize.md#concept_67779E5B7F67427A97D7EA2A6FB919B3).

Auto-Target utilizza un machine learning avanzato per selezionare esperienze definite dall'esperto di marketing più alte e distribuisce l'esperienza più personalizzata a ogni visitatore in base al suo profilo singolo e al comportamento dei visitatori precedenti con profili simili, per personalizzare i contenuti e stimolare le conversioni.

### Personalizzazione automatizzata

Per ulteriori informazioni, consulta [Personalizzazione automatizzata](../c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9).

La Personalizzazione automatizzata (AP) combina offerte o messaggi e utilizza l’apprendimento automatico avanzato per abbinare diverse varianti di offerta ad ogni visitatore in base al suo profilo cliente, al fine di personalizzare il contenuto e favorire l’incremento.

### Targeting esperienza (XT)

[Targeting esperienza](../c-activities/t-experience-target/experience-target.md#task_A53DF336CB9F4D7BB87EF2106099EFC4)

La funzione Targeting esperienza (XT) fornisce contenuti a un pubblico specifico basato su una serie di regole e criteri definiti dagli addetti al marketing.

Il Targeting dell’esperienza, tra cui il geotargeting, è utile per definire regole che rivolgono un’esperienza o un contenuto specifico a un determinato pubblico. È possibile definire diverse regole in un'attività per fornire diverse varianti di contenuto a tipi di pubblico diversi. Quando i visitatori visualizzano il tuo sito, la funzione Targeting esperienza (XT) li valuta per determinare se soddisfano i criteri impostati. Se soddisfano i criteri, vengono inclusi nell'attività e viene visualizzata l'esperienza progettata per i tipi di pubblico idonei. Puoi creare esperienze per più tipi di pubblico all'interno di una singola attività.

### Test multivariato (MVT)

Per ulteriori informazioni, consulta [Test multivariato](../c-activities/c-multivariate-testing/multivariate-testing.md#concept_628695CDC71B449B8DCC2F5654C11499).

Il test multivariato (Multivariate Testing, MVT) confronta le combinazioni di offerte negli elementi di una pagina per determinare quale combinazione funziona al meglio per un pubblico specifico e identifica quale elemento influisce maggiormente sul successo dell’attività.

### Consigli

Consulta [Consigli](../c-recommendations/recommendations.md#concept_7556C8A4543942F2A77B13A29339C0C0) per ulteriori informazioni.

Le attività di generazione dei consigli visualizzano automaticamente prodotti o contenuti che potrebbero interessare i clienti in base alle loro attività precedenti o ad altri algoritmi. I consigli aiutano a indirizzare i clienti verso elementi rilevanti di cui potrebbero non essere a conoscenza.

## La rete Edge {#concept_0AE2ED8E9DE64288A8B30FCBF1040934}

“Edge” è un’architettura di servizio geograficamente distribuita che garantisce agli utenti finali che richiedono contenuti in tempi di risposta ottimali, indipendentemente dall’area geografica in cui si trovano.

Per migliorare i tempi di risposta, gli ambienti Edge ospitano solo logica di attività e profilo memorizzato nella cache e informazioni sulle offerte. I database di attività e contenuti, i dati di [!DNL Analytics], le API e le interfacce utente per gli addetti al marketing si trovano negli ambienti di dati centrali di Adobe. Gli aggiornamenti vengono quindi inviati ai nodi di Edge. Gli ambienti centrali e i nodi Edge vengono sincronizzati automaticamente per aggiornare continuamente i dati dell'attività memorizzati nella cache. La modellazione 1:1 è memorizzata anche su ciascun bordo, per cui anche le richieste più complesse possono essere elaborate su Edge.

Ogni nodo di Edge include tutte le informazioni necessarie per rispondere alla richiesta di contenuto dell'utente e tenere traccia dei dati di analisi relativi a tale richiesta. Le richieste degli utenti vengono indirizzate al nodo di Edge più vicino.

![Mappa con siti periferici principali e siti periferici](assets/edge_network.png)

The source for this mage is the [Adobe Target Security Overview](https://www.adobe.com/content/dam/acom/en/security/pdfs/AdobeTargetSecurityOverview.pdf) white.

La soluzione Adobe Target è ospitata sui centri dati di proprietà di Adobe e Adobe in tutto il mondo. I server di amministrazione sono ospitati interamente all'interno dei centri dati di proprietà di Adobe a Londra, Singapore e in più posizioni negli Stati Uniti, compresi Oregon e Virginia. I server periferici sono ospitati sia sui server di proprietà Adobe che sui server con licenza Adobe nei centri dati Amazon AWS a Londra, Hong Kong, Singapore, Tokyo e Sydney.

Le posizioni del server amministratore contengono sia un centro raccolta dati che un centro di elaborazione dati. Le posizioni del sito Edge contengono solo un centro raccolta dati. Ogni suite di rapporti viene assegnata a un centro di elaborazione dati specifico.

Anziché rispondere a tutte le richieste di targeting da una singola posizione, le richieste vengono elaborate dall'ambiente Edge più vicino al visitatore, riducendo in questo modo l'impatto derivante dal tempo di trasferimento di rete/Internet.

>[!IMPORTANT]
>
>[!DNL Adobe Target] al momento non dispone di una rete Edge in Cina e le prestazioni dell'utente finale continueranno a essere limitate per [!DNL Target] i clienti in Cina. A causa del Firewall Great Firewall e della mancanza di nodi Edge nel paese, le esperienze dei siti con [!DNL Target] distribuzione risulteranno rallentate e verranno caricate le relative pagine. Inoltre, gli addetti al marketing possono verificare la latenza quando utilizzano l'interfaccia utente [!DNL Target] di authoring.

## Esperienza utente protetta {#concept_40A5E781D90A41E4955F80EA9E5F8F96}

Adobe garantisce un alto grado di affidabilità per la disponibilità e le prestazioni dell’infrastruttura di targeting. Tuttavia, un'interruzione delle comunicazioni tra il browser di un utente finale e il server di Adobe può causare un’interruzione nella distribuzione dei contenuti.

To safeguard against service interruptions and connectivity issues, all locations are set up to include default content (defined by the client), which is displayed if the user’s browser cannot connect to [!DNL Target].

Non viene apportata alcuna modifica alla pagina se il browser dell'utente non è in grado di connettersi entro un periodo di timeout definito (per impostazione predefinita: 15 secondi). Se questa soglia di timeout viene raggiunta, viene visualizzato il contenuto di posizione predefinito.

Adobe tutela l’esperienza utente attraverso l’ottimizzazione e la salvaguardia delle prestazioni.

* Adobe garantisce i benchmark prestazionali basati sugli standard di settore, come garantiti dallo SLA di Adobe.
* La rete Edge assicura una distribuzione tempestiva dei dati.
* Adobe utilizza un approccio multilivello per garantire che le applicazioni forniscano il livello massimo di disponibilità e di affidabilità ai clienti.
* [!DNL Target] Consulting offre assistenza nell’implementazione e supporto continuo per il prodotto.

## Test di usabilità per l’ottimizzazione per motori di ricerca (SEO){#concept_C0C865663CAB4251B66A1F250FD25E6A}

Le funzionalità di test di [!DNL Adobe Target] sono conformi alle linee guida dei motori di ricerca.

Google incoraggia i test sugli utenti e, nella sua documentazione, afferma che i test A/B e multivariati non danneggiano il posizionamento organico nei motori di ricerca, purché vengano seguite alcune semplici linee guida.

Per ulteriori informazioni, consulta le seguenti risorse di Google:

* [Website testing and Google Search (Test di sito web e ricerca Google)](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html)
* [Esperimenti e cloaking](https://support.google.com/analytics/answer/2576845?hl=en&ref_topic=1745207)

Le linee guida sono state pubblicate su [Google Webmaster Central Blog](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html). Il post risale al 2012, ma rimane comunque la dichiarazione più recente di Google su questa questione e le linee guida restano valide.

* **Nessun cloaking**: per “cloaking” si intende mostrare un insieme di contenuti agli utenti e un diverso insieme di contenuti ai bot dei motori di ricerca, identificandoli in modo specifico e fornendo loro intenzionalmente contenuti diversi.

   La piattaforma Target è configurata per trattare i bot dei motori di ricerca allo stesso modo di qualsiasi utente. Ciò significa che i bot potrebbero essere inclusi nei test che esegui, se selezionati in modo casuale, e quindi “vedere” le varianti dei test.

* **Usare rel = "canonical"**: a volte è necessario impostare un test A/B utilizzando URL diversi per le varianti. In questi casi, tutte le varianti devono contenere un tag `rel="canonical"` che fa riferimento all’URL originale (di controllo). Ad esempio, supponiamo che Adobe voglia eseguire un test per la propria home page utilizzando URL diversi per ogni variante: il seguente tag canonical per la home page andrebbe nel tag `<head>` di ciascuna variante:

   `<link rel="canonical" href="https://www.adobe.com" />`

* **Usare reindirizzamenti 302 (temporanei)**: se vengono utilizzati URL diversi per le pagine delle varianti di un test, Google consiglia di indirizzare il traffico alle varianti del test mediante un reindirizzamento 302. Questo indica ai motori di ricerca che il reindirizzamento è temporaneo e sarà attivo solo finché il test è in esecuzione.

   Un reindirizzamento 302 è un reindirizzamento lato server e Target, così come la maggior parte dei provider di ottimizzazione, utilizza funzionalità lato client. Pertanto, questa è un’area in cui Target non è pienamente conforme ai consigli di Google. Tuttavia, questo interessa solo una piccola frazione di test. L'approccio standard per l'esecuzione di test attraverso Target richiede la modifica dei contenuti all'interno di un singolo URL, quindi non sono necessari reindirizzamenti. Esistono casi in cui i client devono utilizzare più URL per rappresentare le varianti di test. In queste istanze, Target utilizza il comando `window.location` di JavaScript per indirizzare gli utenti alle varianti di test, che non indica in modo esplicito se il reindirizzamento è di tipo 301 o 302.

   Continuiamo a cercare soluzioni valide per un allineamento completo alle linee guida per i motori di ricerca; tuttavia per i clienti che devono utilizzare URL separati per i test, siamo fiduciosi che l'implementazione corretta dei tag “canonical” di cui sopra attenui il rischio associato a questo approccio.

* **Eseguire esperimenti solo per la durata strettamente necessaria**: riteniamo che per “durata strettamente necessaria” si intenda il tempo necessario a raggiungere la rilevanza statistica. Target [fornisce best practice](https://docs.adobe.com/content/target-microsite/testcalculator.html) per determinare quando un test ha raggiunto questo obiettivo. Si consiglia di incorporare l'implementazione hardcoded dei test vincenti nel flusso di lavoro dei test e di assegnare le risorse appropriate.

   L’utilizzo della piattaforma Target per “pubblicare” i test vincenti non è una soluzione permanente consigliata, ma fintanto che il test vincente venga pubblicato per il 100% degli utenti e per il 100% delle volte, questo approccio può essere utilizzato fino al completamento del processo di hardcoding del test vincente.

   È importante considerare anche le modifiche apportate dal test. Il semplice aggiornamento del colore dei pulsanti o di altri elementi non testuali minori presenti nella pagina non avrà alcuna influenza sulla classificazione organica. Tuttavia, le modifiche al testo devono essere hardcoded.

   È inoltre importante considerare l'accessibilità della pagina che stai testando. Se la pagina non è accessibile ai motori di ricerca e non è comunque mai stata progettata per essere classificata in una ricerca organica, come una pagina di destinazione dedicata per una campagna e-mail, le considerazioni di cui sopra non sono applicabili.

Google afferma che seguire queste linee guida deve avere un impatto minimo o nessun impatto sul sito nei risultati della ricerca. "

Oltre a queste linee guida, Google fornisce anche una guida in più nella documentazione del suo strumento Esperimenti sui contenuti:

* “Le varianti di pagina devono conservare lo spirito dei contenuti delle pagine originali. e non devono alterare il significato o la percezione generale che gli utenti hanno dei contenuti originali.”

Google dichiara, a titolo di esempio, che “se la pagina originale di un sito presenta parole chiave non correlate alle combinazioni mostrate agli utenti, possiamo rimuovere il sito dal nostro indice”.

Riteniamo che sarebbe difficile cambiare involontariamente il significato del contenuto originale all'interno di varianti di test, ma si consiglia di essere consapevoli dei temi delle parole chiave di una pagina e di mantenerli. Le modifiche al contenuto di una pagina, in particolare l’aggiunta o l’eliminazione di parole chiave rilevanti, possono influenzare la classificazione dell’URL nella ricerca organica. Consigliamo di coinvolgere il tuo partner SEO come parte del protocollo di test.

## Bot {#bots}

Adobe Target utilizza [deviceatlas](https://deviceatlas.com/) per rilevare i bot noti. Al traffico identificato come generato da un bot viene ancora distribuito contenuto, come un utente regolare, per essere certi che sia in linea con le linee guida SEO. L'utilizzo del traffico bot può inclinare test A/B o algoritmi di personalizzazione se sono trattati come utenti normali. Pertanto, se nell'attività Target viene rilevato un bot noto, il traffico viene trattato in modo leggermente diverso. La rimozione del traffico bot fornisce una misura più accurata dell'attività dell'utente.

In modo specifico, per il traffico noto dei bot Target non è:

* Creazione o recupero di un profilo visitatore
* Registrare eventuali attributi di profilo o eseguire script di profilo
* Cercare segmenti di Adobe Audience Manager (AAM) (se applicabile)
* Utilizzare il traffico bot per modellare e fornire contenuti personalizzati per le attività di Recommendations, Auto Target, Automated Personalization (Personalizzazione automatizzata) o Auto Allocate (Allocazione automatica)
* Registrare una visita dell'attività per il reporting
* Dati del registro da inviare alla piattaforma Adobe Experience Cloud
