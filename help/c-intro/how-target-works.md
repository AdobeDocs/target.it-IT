---
keywords: Adobe Experience Platform Web SDK;aep web sdk;aep sdk;seo;search engine optimization;edge clusters, central clusters;at.js;mbox.js;
description: Informazioni sul funzionamento  Adobe Target, comprese informazioni sull'SDK per Adobe Experience Platform Web, sulle librerie JavaScript di Target (at.js e mbox.js) e sui vari tipi di attività che è possibile creare in Target.
title: Come funziona Adobe Target
feature: Overview
translation-type: tm+mt
source-git-commit: 1b426e0b2004e729ba75d218a9b6ccd5195449cd
workflow-type: tm+mt
source-wordcount: '2530'
ht-degree: 70%

---


# Come funziona Adobe Target

Informazioni sul funzionamento di [!DNL Adobe Target], comprese informazioni sulle [!DNL Adobe Experience Platform Web SDK], le [!DNL Target] librerie JavaScript (at.js e mbox.js) e i vari tipi di attività che è possibile creare utilizzando Target.

## SDK Web della piattaforma Target e librerie JavaScript {#libraries}

 Adobe Target si integra con i siti Web mediante le librerie [!DNL AEP Web SDK] o JavaScript:

* **Adobe Experience Platform Web SDK:** L&#39; [AEP Web ](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) SDK è una nuova libreria JavaScript lato client che consente  [!DNL Adobe Experience Cloud] ai clienti di interagire con i vari servizi dell&#39; [!DNL Experience Cloud] (incluso  [!DNL Target]) tramite  [!DNL Adobe Experience Platform] Edge Network. Per informazioni specifiche su [Target overview](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/adobe-target/target-overview.html), vedere [!DNL Target].
* **at.js:** la [libreria at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17) è la nuova libreria di implementazione per Target. La libreria at.js migliora i tempi di caricamento delle pagine per le implementazioni Web e fornisce migliori opzioni di implementazione per le applicazioni a pagina singola. at.js è la libreria di implementazione consigliata e viene aggiornata frequentemente con nuove funzionalità. Si consiglia a tutti i clienti di implementare o eseguire la migrazione alla [versione più recente di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A).
* **mbox.js:**[ la libreria mbox.js è la libreria di implementazione legacy per Target. ](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md) La libreria mbox.js è supportata fino al 31 marzo 2021, ma non saranno disponibili aggiornamenti di funzionalità.

>[!IMPORTANT]
>
>Tutti i clienti devono effettuare la migrazione alla [!DNL AEP Web SDK] o all&#39;ultima versione di at.js. Per ulteriori informazioni, vedere [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) o [Migra a at.js da mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA).

È necessario fare riferimento a [!DNL AEP Web SDK] o at.js in ogni pagina del sito. Ad esempio, potete aggiungere uno di questi all’intestazione globale. In alternativa, prendere in considerazione l&#39;utilizzo di [ piattaforma di Adobe Launch](https://experienceleague.adobe.com/docs/launch/using/overview.html).

Le seguenti risorse sono utili per implementare AEP Web SDK o at.js:

* [Estensione Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/launch/using/extensions-ref/adobe-extension/aep-extension/overview.html?lang=en#configure-the-aep-web-sdk-extension)
* [Implementare Target con Adobe Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md)

Ogni volta che un visitatore richiede una pagina ottimizzata per [!DNL Target], viene inviata una richiesta al sistema di targeting per determinare il contenuto da distribuire a un visitatore. Questo processo si verifica in tempo reale, ogni volta che una pagina viene caricata, una richiesta per il contenuto viene effettuata e soddisfatta dal sistema. Il contenuto è gestito dalle regole delle attività e delle esperienze controllate dagli addetti al marketing, e ne viene eseguito il targeting per i singoli visitatori del sito. Per massimizzare i tassi di risposta e di acquisizione e il ricavo, viene distribuito il contenuto per il quale è più probabile che si verifichi una risposta, un’interazione e infine un acquisto da parte del visitatore del sito.

In [!DNL Target], ogni elemento della pagina è parte di un&#39;unica esperienza per l&#39;intera pagina. Ciascuna esperienza può includere più elementi sulla pagina.

Il contenuto visualizzato dai visitatori dipende dal tipo di attività creata:

### Test A/B

Consulta [Creare un test A/B](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) per ulteriori informazioni.

Il contenuto visualizzato in un test A/B di base viene scelto in modo casuale tra le risorse assegnate alle attività, in base alle percentuali selezionate per ogni esperienza. Come risultato di questa suddivisione casuale del traffico, è possibile che sia richiesta una quantità notevole di traffico iniziale prima che le percentuali si livellino. Ad esempio, se crei due esperienze, quella di partenza verrà scelta in modo casuale. Se il traffico è limitato, è possibile che la percentuale di visitatori tenda in modo più netto verso una delle due esperienze. Con l’aumento del traffico, le percentuali tendono a equilibrarsi.

Puoi specificare target basati su percentuali per ogni esperienza. In questo caso, viene generato un numero casuale, utilizzato per scegliere l’esperienza da visualizzare. Le percentuali risultanti potrebbero non corrispondere esattamente ai target specificati. Con l’aumentare del traffico, le esperienze risulteranno tuttavia suddivise in modo più rispondente agli obiettivi.

1. Un cliente richiede una pagina dal server e la visualizza nel browser.
2. Nel browser del cliente viene impostato un cookie di prime parti che ne memorizza il comportamento.
3. La pagina effettua una chiamata al sistema di targeting.
4. Il contenuto viene visualizzato in base alle regole della relativa attività.

### Allocazione automatica

Per ulteriori informazioni, consulta [ Allocazione automatica](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4).

L’allocazione automatica identifica un vincitore tra due o più esperienze e, di conseguenza, ridistribuisce automaticamente più traffico per aumentare le conversioni, mentre il test continua a essere eseguito e ad apprendere.

### Targeting automatico (AT)

Per ulteriori informazioni, consulta [Targeting automatico](/help/c-activities/auto-target/auto-target-to-optimize.md).

La funzione Targeting automatico utilizza l’apprendimento automatico avanzato per selezionare tra più esperienze ad alte prestazioni definite dall’addetto al marketing. Inoltre, indica l’esperienza più adatta per ogni visitatore in base al suo profilo cliente individuale e al comportamento dei visitatori precedenti con profili simili, al fine di personalizzare contenuti e favorire le conversioni.

### Personalizzazione automatizzata

Per ulteriori informazioni, consulta [Personalizzazione automatizzata](/help/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9).

La Personalizzazione automatizzata (AP) combina offerte o messaggi e utilizza l’apprendimento automatico avanzato per abbinare diverse varianti di offerta ad ogni visitatore in base al suo profilo cliente, al fine di personalizzare il contenuto e favorire l’incremento.

### Targeting esperienza (XT)

[Targeting esperienza](/help/c-activities/t-experience-target/experience-target.md#task_A53DF336CB9F4D7BB87EF2106099EFC4)

La funzione Targeting esperienza (XT) fornisce contenuti a un pubblico specifico basato su una serie di regole e criteri definiti dagli addetti al marketing.

Il Targeting dell’esperienza, tra cui il geotargeting, è utile per definire regole che rivolgono un’esperienza o un contenuto specifico a un determinato pubblico. È possibile definire diverse regole in un’attività per fornire diverse varianti di contenuto a tipi di pubblico diversi. Quando i visitatori visualizzano il tuo sito, la funzione Targeting esperienza (XT) li valuta per determinare se soddisfano i criteri impostati. Se soddisfano i criteri, vengono inclusi nell&#39;attività e viene visualizzata l&#39;esperienza progettata per i tipi di pubblico idonei. Puoi creare esperienze per più tipi di pubblico all&#39;interno di una singola attività.

### Test multivariato (MVT)

Per ulteriori informazioni, consulta [Test multivariato](/help/c-activities/c-multivariate-testing/multivariate-testing.md#concept_628695CDC71B449B8DCC2F5654C11499).

Il test multivariato (Multivariate Testing, MVT) confronta le combinazioni di offerte negli elementi di una pagina per determinare quale combinazione funziona al meglio per un pubblico specifico e identifica quale elemento influisce maggiormente sul successo dell’attività.

### Consigli

Consulta [Consigli](/help/c-recommendations/recommendations.md#concept_7556C8A4543942F2A77B13A29339C0C0) per ulteriori informazioni.

Le attività di generazione dei consigli visualizzano automaticamente prodotti o contenuti che potrebbero interessare i clienti in base alle loro attività precedenti o ad altri algoritmi. I consigli aiutano a indirizzare i clienti verso elementi rilevanti di cui potrebbero non essere a conoscenza.

## Rete periferica {#concept_0AE2ED8E9DE64288A8B30FCBF1040934}

Un &quot;Edge&quot; è un&#39;architettura di servizio geograficamente distribuita che garantisce tempi di risposta ottimali agli utenti finali che richiedono contenuti, indipendentemente da dove si trovano in tutto il mondo.

Per migliorare i tempi di risposta, Target Edge ospita solo la logica di attività, i profili memorizzati nella cache e le informazioni sulle offerte.

I database delle attività e dei contenuti, i dati [!DNL Analytics], le API e le interfacce utente degli esperti di marketing sono memorizzati  cluster centrali del Adobe. Gli aggiornamenti vengono quindi inviati ai bordi di Target. I cluster centrali e i cluster Edge vengono sincronizzati automaticamente per aggiornare continuamente i dati dell&#39;attività memorizzati nella cache. Tutti i modelli 1:1 sono inoltre memorizzati su ciascun bordo, per cui anche le richieste più complesse possono essere elaborate sul bordo.

Ogni cluster Edge dispone di tutte le informazioni necessarie per rispondere alla richiesta di contenuto dell&#39;utente e tenere traccia dei dati di analisi su tale richiesta. Le richieste degli utenti vengono indirizzate al cluster Edge più vicino.

Per ulteriori informazioni, vedi il documento [Panoramica sulla sicurezza di Adobe Target](https://www.adobe.com/content/dam/cc/en/security/pdfs/AdobeTargetSecurityOverview.pdf).

La soluzione [!DNL Adobe Target] è ospitata  centri dati di proprietà del Adobe e affittati  Adobe in tutto il mondo.

Le posizioni cluster centrali contengono sia un centro di raccolta dati che un centro di elaborazione dati. Le posizioni cluster Edge contengono solo un centro di raccolta dati. Ogni suite di rapporti viene assegnata a un centro di elaborazione dati specifico.

I dati dell&#39;attività del sito del cliente vengono raccolti dai sette cluster Edge più vicini e indirizzati alla destinazione del cluster centrale predeterminata del cliente (una delle tre posizioni: Oregon, Dublino, Singapore) per l&#39;elaborazione. I dati del profilo del visitatore sono memorizzati nel cluster Edge più vicino al visitatore del sito (le posizioni del cluster Central e Virginia, Amsterdam, Sydney, Tokyo e Hong Kong).

Invece di rispondere a tutte le richieste di targeting da un&#39;unica posizione, le richieste vengono elaborate dal cluster Edge più vicino al visitatore, mitigando in tal modo l&#39;impatto dei tempi di viaggio di rete/Internet.

![Mappa dei tipi di server di Target](/help/c-intro/assets/target-servers.png)

Target Central Clusters, ospitato  Amazon Web Services (AWS), si trova in:

* Oregon, USA
* Dublin (Irlanda)
* Repubblica di Singapore

Target Edge Clusters, ospitato su AWS, si trova in:

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
>[!DNL Adobe Target] al momento non dispone di un cluster Edge in Cina e le prestazioni dell&#39;utente finale continueranno a essere limitate per  [!DNL Target] i clienti in Cina. A causa del firewall e della mancanza di Edge Clusters nel paese, le esperienze dei siti con [!DNL Target] implementato risulteranno lente e i carichi delle pagine ne risulteranno influenzati. Inoltre, gli esperti di marketing potrebbero rilevare la latenza durante l&#39;utilizzo dell&#39;interfaccia di authoring [!DNL Target].

Se necessario, potete  inserire nell&#39;elenco Consentiti i cluster Edge di Target. Per ulteriori informazioni, vedere [ inserire nell&#39;elenco Consentiti nodi periferici di Target](/help/c-implementing-target/c-considerations-before-you-implement-target/allowlist-edges.md).

## Esperienza utente protetta {#concept_40A5E781D90A41E4955F80EA9E5F8F96}

Adobe garantisce un alto grado di affidabilità per la disponibilità e le prestazioni dell’infrastruttura di targeting. Tuttavia, un&#39;interruzione delle comunicazioni tra il browser di un utente finale e il server di Adobe può causare un’interruzione nella distribuzione dei contenuti.

Per fornire protezione da interruzioni dei servizi e da problemi di connettività, tutte le posizioni sono impostate per includere il contenuto predefinito (definito dal cliente), che viene utilizzato se il browser dell’utente non è in grado di connettersi a [!DNL Target].

Non vengono apportate modifiche alla pagina se il browser dell’utente non riesce a collegarsi entro l’intervallo di timeout definito (per impostazione predefinita, 15 secondi). Se questa soglia di timeout viene raggiunta, viene visualizzato il contenuto di posizione predefinito.

Adobe tutela l’esperienza utente attraverso l’ottimizzazione e la salvaguardia delle prestazioni.

* Adobe garantisce i benchmark prestazionali basati sugli standard di settore, come garantiti dallo SLA di Adobe.
* La rete Edge assicura una distribuzione tempestiva dei dati.
* Adobe utilizza un approccio multilivello per garantire che le applicazioni forniscano il livello massimo di disponibilità e di affidabilità ai clienti.
* [!DNL Target] Consulting offre assistenza nell’implementazione e supporto continuo per il prodotto.

## Test di usabilità per l’ottimizzazione per i motori di ricerca (SEO){#concept_C0C865663CAB4251B66A1F250FD25E6A}

Le funzionalità di test di [!DNL Adobe Target] sono conformi alle linee guida dei motori di ricerca.

Google incoraggia i test sugli utenti e, nella sua documentazione, afferma che i test A/B e multivariati non danneggiano il posizionamento organico nei motori di ricerca, purché vengano seguite alcune semplici linee guida.

Per ulteriori informazioni, consulta le seguenti risorse di Google:

* [Website testing and Google Search (Test di sito web e ricerca Google)](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html)
* [Esperimenti e cloaking](https://support.google.com/analytics/answer/2576845?hl=en&amp;ref_topic=1745207)

Le linee guida sono state pubblicate su [Google Webmaster Central Blog](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html). Il post risale al 2012, ma rimane comunque la dichiarazione più recente di Google su questa questione e le linee guida restano valide.

* **Nessun cloaking**: per “cloaking” si intende mostrare un insieme di contenuti agli utenti e un diverso insieme di contenuti ai bot dei motori di ricerca, identificandoli in modo specifico e fornendo loro intenzionalmente contenuti diversi.

   La piattaforma Target è configurata per trattare i bot dei motori di ricerca allo stesso modo di qualsiasi utente. Ciò significa che i bot potrebbero essere inclusi nei test che esegui, se selezionati in modo casuale, e quindi “vedere” le varianti dei test.

* **Usare rel = &quot;canonical&quot;**: a volte è necessario impostare un test A/B utilizzando URL diversi per le varianti. In questi casi, tutte le varianti devono contenere un tag `rel="canonical"` che fa riferimento all’URL originale (di controllo). Ad esempio, supponiamo che Adobe voglia eseguire un test per la propria home page utilizzando URL diversi per ogni variante: il seguente tag canonical per la home page andrebbe nel tag `<head>` di ciascuna variante:

   `<link rel="canonical" href="https://www.adobe.com" />`

* **Usare reindirizzamenti 302 (temporanei)**: se vengono utilizzati URL diversi per le pagine delle varianti di un test, Google consiglia di indirizzare il traffico alle varianti del test mediante un reindirizzamento 302. Questo indica ai motori di ricerca che il reindirizzamento è temporaneo e sarà attivo solo finché il test è in esecuzione.

   Un reindirizzamento 302 è un reindirizzamento lato server e Target, così come la maggior parte dei provider di ottimizzazione, utilizza funzionalità lato client. Pertanto, questa è un’area in cui Target non è pienamente conforme ai consigli di Google. Tuttavia, questo interessa solo una piccola frazione di test. L&#39;approccio standard per l&#39;esecuzione di test attraverso Target richiede la modifica dei contenuti all&#39;interno di un singolo URL, quindi non sono necessari reindirizzamenti. Esistono casi in cui i client devono utilizzare più URL per rappresentare le varianti di test. In queste istanze, Target utilizza il comando `window.location` di JavaScript per indirizzare gli utenti alle varianti di test, che non indica in modo esplicito se il reindirizzamento è di tipo 301 o 302.

   Continuiamo a cercare soluzioni valide per un allineamento completo alle linee guida per i motori di ricerca; tuttavia per i clienti che devono utilizzare URL separati per i test, siamo fiduciosi che l&#39;implementazione corretta dei tag “canonical” di cui sopra attenui il rischio associato a questo approccio.

* **Eseguire esperimenti solo per la durata strettamente necessaria**: riteniamo che per “durata strettamente necessaria” si intenda il tempo necessario a raggiungere la rilevanza statistica. Target [fornisce best practice](https://docs.adobe.com/content/target-microsite/testcalculator.html) per determinare quando un test ha raggiunto questo obiettivo. Si consiglia di incorporare l&#39;implementazione hardcoded dei test vincenti nel flusso di lavoro dei test e di assegnare le risorse appropriate.

   L’utilizzo della piattaforma Target per “pubblicare” i test vincenti non è una soluzione permanente consigliata, ma fintanto che il test vincente venga pubblicato per il 100% degli utenti e per il 100% delle volte, questo approccio può essere utilizzato fino al completamento del processo di hardcoding del test vincente.

   È importante considerare anche le modifiche apportate dal test. Il semplice aggiornamento del colore dei pulsanti o di altri elementi non testuali minori presenti nella pagina non avrà alcuna influenza sulla classificazione organica. Tuttavia, le modifiche al testo devono essere hardcoded.

   È inoltre importante considerare l&#39;accessibilità della pagina che stai testando. Se la pagina non è accessibile ai motori di ricerca e non è comunque mai stata progettata per essere classificata in una ricerca organica, come una pagina di destinazione dedicata per una campagna e-mail, le considerazioni di cui sopra non sono applicabili.

Google afferma che seguendo queste linee guida “i test dovrebbero avere un impatto minimo o nullo sul tuo sito nei risultati di ricerca”.

Oltre a queste linee guida, Google fornisce anche una guida in più nella documentazione del suo strumento Esperimenti sui contenuti:

* “Le varianti di pagina devono conservare lo spirito dei contenuti delle pagine originali. e non devono alterare il significato o la percezione generale che gli utenti hanno dei contenuti originali.”

Google dichiara, a titolo di esempio, che “se la pagina originale di un sito presenta parole chiave non correlate alle combinazioni mostrate agli utenti, possiamo rimuovere il sito dal nostro indice”.

Riteniamo che sarebbe difficile cambiare involontariamente il significato del contenuto originale all&#39;interno di varianti di test, ma si consiglia di essere consapevoli dei temi delle parole chiave di una pagina e di mantenerli. Le modifiche al contenuto di una pagina, in particolare l’aggiunta o l’eliminazione di parole chiave rilevanti, possono influenzare la classificazione dell’URL nella ricerca organica. Consigliamo di coinvolgere il tuo partner SEO come parte del protocollo di test.

## Bot {#bots}

 Adobe Target utilizza [DeviceAtlas](https://deviceatlas.com/) per rilevare i bot noti. Al traffico che viene identificato come traffico generato da un bot vengono comunque trasmessi i contenuti, come per il traffico proveniente da utenti regolari, nel rispetto delle linee guida SEO. Tuttavia, l’utilizzo di traffico da bot trattato come utenti normali può sfalsare i test A/B o gli algoritmi di personalizzazione. Pertanto, se nell’attività Target viene rilevato un bot noto, il relativo traffico viene trattato in modo leggermente diverso. La rimozione del traffico da bot genera misurazioni più accurate delle attività degli utenti effettivi.

In particolare, per il traffico proveniente da bot noti, Target:

* non crea né recupera un profilo visitatore;
* non registra eventuali attributi di profilo né esegue gli script di profilo;
* non consulta i segmenti Adobe Audience Manager (AAM) (se applicabile);
* non utilizza il traffico da bot per modellare e trasmettere contenuti personalizzati per le attività di Consigli, Targeting automatico, Personalizzazione automatizzata e Allocazione automatica;
* non registra a fini di reporting una visita all’attività;
* non registra i dati da inviare alla piattaforma Adobe Experience Cloud.
