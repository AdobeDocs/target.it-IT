---
keywords: Adobe Experience Platform Web SDK;aep web sdk;aep sdk;SEO (Search Engine Optimization);SEO (Search Engine Optimization);seo;cluster edge, cluster centrali;at.js;mbox.js;
description: Scopri come le librerie JavaScript di Adobe [!DNL Target] works, including information about the [!DNL Target] at.js e AEP Web SDK), i centri dati di Adobe e i test SEO.
title: Come funziona [!DNL Target] ?
feature: Panoramica
exl-id: 8a93e061-0be7-4ecc-b511-2210094547f2
translation-type: tm+mt
source-git-commit: b673a925bd16c9f786b884dc36fbd7155f26f51c
workflow-type: tm+mt
source-wordcount: '2563'
ht-degree: 97%

---

# Come funziona l&#39;Adobe [!DNL Target]

Scopri come funziona [!DNL Adobe Target], comprese informazioni su [!DNL Adobe Experience Platform Web SDK] e le librerie JavaScript (at.js e mbox.js). Questo articolo introduce anche i vari tipi di attività che è possibile creare utilizzando [!DNL Target]. È inoltre possibile avere informazioni su rete Edge [!DNL Target], SEO (Search Engine Optimization) e sul modo in cui [!DNL Target] rileva i bot.

## [!DNL Target]SDK per web e librerie JavaScript di Platform {#libraries}

[!DNL Target] si integra con i siti web utilizzando [!DNL AEP Web SDK] o le librerie JavaScript:

* **Adobe Experience Platform Web SDK:**[AEP Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) è una nuova libreria JavaScript lato client. AEP Web SDK consente ai clienti di [!DNL Adobe Experience Cloud] di interagire con i vari servizi nel [!DNL Experience Cloud] (incluso [!DNL Target]) tramite la [!DNL AEP] rete Edge. Adobe consiglia a tutti i nuovi clienti [!DNL Target] di implementare [!DNL AEP Web SDK].
* **at.js:** la [libreria at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17) è una libreria di implementazione per [!DNL Target]. La libreria at.js migliora i tempi di caricamento delle pagine per le implementazioni Web e fornisce migliori opzioni di implementazione per le applicazioni a pagina singola. at.js viene aggiornato frequentemente con nuove funzionalità. Adobe consiglia a tutti i clienti che utilizzano at.js di aggiornare le implementazioni alla versione [più recente di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A).
* **mbox.js:** la [libreria mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md) è la libreria di implementazione legacy per [!DNL Target]. La libreria mbox.js è supportata fino al 31 marzo 2021; tuttavia, non ci saranno aggiornamenti di funzionalità.

>[!IMPORTANT]
>
>Tutti i clienti devono effettuare la migrazione a [!DNL AEP Web SDK] o all’ultima versione di at.js. Per ulteriori informazioni, consulta [Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) o [Migrare a at.js da mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA).

Fai riferimento a [!DNL AEP Web SDK] o at.js in ogni pagina del sito. Ad esempio, puoi aggiungere una di queste librerie all’intestazione globale. In alternativa, puoi utilizzare [Adobe Platform Launch](https://experienceleague.adobe.com/docs/launch/using/overview.html?lang=it) per implementare [!DNL Target].

Le risorse seguenti contengono informazioni dettagliate utili per implementare AEP Web SDK o at.js:

* [Adobe Experience Platform Web SDK Extension](https://experienceleague.adobe.com/docs/launch/using/extensions-ref/adobe-extension/aep-extension/overview.html?lang=it#configure-the-aep-web-sdk-extension)
* [ [!DNL Target] Implementazione con Adobe Experience Platform Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md)

Ogni volta che un visitatore richiede una pagina ottimizzata per [!DNL Target], viene inviata una richiesta al sistema di targeting. La richiesta aiuta a determinare quale contenuto distribuire al visitatore. Questo processo avviene in tempo reale. Il sistema elabora e soddisfa una richiesta di contenuto ogni volta che viene caricata una pagina. Il contenuto è gestito dalle regole delle attività e delle esperienze controllate dagli addetti al marketing, e ne viene eseguito il targeting per i singoli visitatori del sito. Viene distribuito il contenuto al quale è più probabile che ogni visitatore del sito risponda, interagisca o alla fine acquisti. I contenuti personalizzati consentono di massimizzare i tassi di risposta, i tassi di acquisizione e i ricavi.

In [!DNL Target], ogni elemento sulla pagina è parte di un’unica esperienza per l’intera pagina. Ciascuna esperienza può includere più elementi sulla pagina.

Il contenuto visualizzato dai visitatori dipende dal tipo di attività creata:

### [!UICONTROL Test A/B]

Il contenuto visualizzato in un test A/B di base viene scelto in modo casuale tra le esperienze assegnate all’attività. Puoi assegnare le percentuali di allocazione del traffico per ogni esperienza. Come risultato di questa suddivisione casuale del traffico, è possibile che sia richiesta una quantità notevole di traffico iniziale prima che le percentuali si livellino. Ad esempio, se crei due esperienze, quella di partenza verrà scelta in modo casuale. Se il traffico è limitato, è possibile che la percentuale di visitatori tenda in modo più netto verso una delle due esperienze. Con l’aumento del traffico, le percentuali si livellano.

Puoi specificare target basati su percentuali per ogni esperienza. In questo caso, viene generato un numero casuale, utilizzato per scegliere l’esperienza da visualizzare. Le percentuali risultanti potrebbero non corrispondere esattamente ai target specificati. Con l’aumentare del traffico, le esperienze risulteranno tuttavia suddivise in modo più rispondente agli obiettivi.

1. Un cliente richiede una pagina dal server e la visualizza nel browser.
1. Un cookie di prima parte viene impostato nel browser del cliente per memorizzarne il comportamento.
1. La pagina effettua una chiamata al sistema di targeting.
1. Il contenuto viene visualizzato in base alle regole della relativa attività.

Consulta [Creare un test A/B](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) per ulteriori informazioni.

### [!UICONTROL Allocazione automatica]

[!UICONTROL L’allocazione automatica identifica un vincitore tra due o più esperienze. ] [!UICONTROL L’allocazione automatica ridistribuisce automaticamente più traffico per l’esperienza vincente, il che consente di aumentare le conversioni mentre il test continua a essere eseguito e ad apprendere.]

Per ulteriori informazioni, consulta [[!UICONTROL Allocazione automatica]](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4).

### [!UICONTROL Targeting automatico] (AT)

La funzione Targeting automatico utilizza l’apprendimento automatico avanzato per scegliere tra più esperienze ad alte prestazioni definite dall’addetto al marketing. Il Targeting automatico fornisce l’esperienza più personalizzata a ogni visitatore. La distribuzione delle esperienze si basa sui profili dei singoli clienti e sul comportamento dei visitatori precedenti con profili simili. Utilizza il Targeting automatico per personalizzare il contenuto e favorire le conversioni.

Per ulteriori informazioni, consulta [Targeting automatico](/help/c-activities/auto-target/auto-target-to-optimize.md).

### [!UICONTROL Personalizzazione automatizzata] (AP)

Automated Personalization (AP) combina offerte o messaggi e utilizza l’apprendimento automatico avanzato per abbinare diverse varianti di offerta a ogni visitatore. La distribuzione delle esperienze si basa sui profili dei singoli clienti per personalizzare i contenuti e favorire l’incremento.

Per ulteriori informazioni, consulta [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9).

### Targeting esperienza (XT)

La funzione Targeting esperienza (XT) fornisce contenuti a un pubblico specifico basato su una serie di regole e criteri definiti dagli addetti al marketing.

Il Targeting dell’esperienza, tra cui il geotargeting, è utile per definire regole che rivolgono un’esperienza o un contenuto specifico a un determinato pubblico. È possibile definire diverse regole in un’attività per fornire diverse varianti di contenuto a tipi di pubblico diversi. Quando i visitatori visualizzano il tuo sito, la funzione Targeting esperienza (XT) li valuta per determinare se soddisfano i criteri impostati. Se soddisfano i criteri, vengono inclusi nell&#39;attività e viene visualizzata l&#39;esperienza progettata per i tipi di pubblico idonei. Puoi creare esperienze per più tipi di pubblico all&#39;interno di una singola attività.

Per ulteriori informazioni, consulta [Experience Targeting](/help/c-activities/t-experience-target/experience-target.md#task_A53DF336CB9F4D7BB87EF2106099EFC4).

### [!UICONTROL Test multivariato] (MVT)

Multivariate Testing (MVT) confronta le combinazioni di offerte tra gli elementi di una pagina per vedere quale combinazione funziona meglio per un pubblico specifico. MVT consente di identificare quale elemento influisce maggiormente sul successo dell’attività.

Per ulteriori informazioni, consulta [Test multivariato](/help/c-activities/c-multivariate-testing/multivariate-testing.md#concept_628695CDC71B449B8DCC2F5654C11499).

### [!UICONTROL Consigli]

Le attività di generazione dei consigli visualizzano automaticamente prodotti o contenuti che potrebbero interessare i clienti in base alle loro attività precedenti o ad altri algoritmi. I consigli aiutano a indirizzare i clienti verso elementi rilevanti di cui potrebbero non essere a conoscenza.

Consulta [Consigli](/help/c-recommendations/recommendations.md#concept_7556C8A4543942F2A77B13A29339C0C0) per ulteriori informazioni.

## La rete Edge {#concept_0AE2ED8E9DE64288A8B30FCBF1040934}

“Edge” è un’architettura di servizio geograficamente distribuita che garantisce tempi di risposta ottimali ai visitatori che richiedono contenuti, indipendentemente dall’area geografica in cui si trovano.

Per migliorare i tempi di risposta, [!DNL Target] Edge ospita solo logica di attività, profili memorizzati nella cache e informazioni sulle offerte.

I database di attività e contenuti, i dati [!DNL Analytics], le API e le interfacce utente per gli addetti al marketing si trovano negli ambienti di dati centrali di Adobe. Gli aggiornamenti vengono quindi inviati a Edge [!DNL Target]. Gli ambienti centrali e i nodi di Edge vengono sincronizzati automaticamente per aggiornare continuamente i dati delle attività memorizzati nella cache. Anche la modellazione 1:1 è memorizzata presso ogni nodo di Edge, dove è quindi possibile elaborare anche le richieste più complesse.

Ogni nodo di Edge include tutte le informazioni necessarie per rispondere alla richiesta di contenuto del visitatore e tenere traccia dei dati di analisi relativi a tale richiesta. Le richieste dei visitatori vengono indirizzate al nodo Edge più vicino.

Per ulteriori informazioni, vedi il documento [Panoramica sulla sicurezza di Adobe Target](https://www.adobe.com/content/dam/cc/en/security/pdfs/AdobeTargetSecurityOverview.pdf).

La soluzione [!DNL Target] è ospitata su data center di Adobe (propri o noleggiati) in tutto il mondo.

Le località del cluster centrale contengono sia un centro di raccolta dati sia un centro di elaborazione dati. Le posizioni del cluster Edge contengono solo un centro raccolta dati. Ogni suite di rapporti viene assegnata a un centro di elaborazione dati specifico.

I dati relativi all’attività del sito del cliente vengono raccolti dai sette cluster Edge più vicini. Questi dati vengono indirizzati alla destinazione cluster centrale predefinita di un cliente (una delle tre posizioni seguenti: Oregon, Dublino, Singapore) per la lavorazione. I dati del profilo del visitatore vengono memorizzati nel cluster Edge più vicino al visitatore del sito. Le posizioni dei cluster Edge includono le posizioni del cluster centrale e Virginia, Amsterdam, Sydney, Tokyo e Hong Kong.

Invece di rispondere a tutte le richieste di targeting da un’unica posizione, le richieste vengono elaborate dal cluster Edge più vicino al visitatore. Questo processo contribuisce a mitigare l’impatto del tempo di viaggio in rete/Internet.

![Mappa che mostra i diversi tipi di server Target](/help/c-intro/assets/target-servers.png)

[!DNL Target] I cluster centrali, ospitati su Amazon Web Services (AWS), includono:

* Oregon, USA
* Dublino, Irlanda
* Repubblica di Singapore

[!DNL Target] I cluster Edge, ospitati su AWS, includono:

* Mumbai, India
* Tokyo, Giappone
* Virginia, Stati Uniti
* Oregon, USA
* Sydney, Australia
* Dublino, Irlanda
* Repubblica di Singapore

Il servizio [!DNL Target Recommendations] è ospitato in un data center [!DNL Adobe] in Oregon.

>[!IMPORTANT]
>
>[!DNL Adobe Target] al momento non dispone di un cluster Edge in Cina e le prestazioni del visitatore rimangono limitate per i clienti [!DNL Target] in Cina. A causa del firewall e della mancanza di cluster Edge nel paese, le esperienze dei siti con [!DNL Target] implementato possono essere influenzate. Le esperienze possono essere lente per il rendering e possono essere influenzate dai caricamenti di pagina. Inoltre, gli addetti al marketing possono riscontrare una latenza durante l’utilizzo dell’interfaccia utente di creazione di [!DNL Target].

Se necessario, puoi inserire nell’elenco Consentiti i cluster di Edge [!DNL Target]. Per ulteriori informazioni, consulta [elenco Consentiti nodi edge di Target](/help/c-implementing-target/c-considerations-before-you-implement-target/allowlist-edges.md).

## Esperienza di utilizzo protetta {#concept_40A5E781D90A41E4955F80EA9E5F8F96}

Adobe garantisce un alto grado di affidabilità per la disponibilità e le prestazioni dell’infrastruttura di targeting. Tuttavia, un breakdown delle comunicazioni tra il browser di un visitatore e i server di Adobe può causare un’interruzione nella distribuzione del contenuto.

Per fornire protezione da interruzioni dei servizi e da problemi di connettività, tutte le posizioni sono impostate per includere il contenuto predefinito (definito dal cliente). Questo contenuto predefinito viene visualizzato se il browser dell’utente non è in grado di connettersi a [!DNL Target].

Non vengono apportate modifiche alla pagina se il browser dell’utente non riesce a collegarsi entro l’intervallo di timeout definito (per impostazione predefinita, 15 secondi). Se questa soglia di timeout viene raggiunta, viene visualizzato il contenuto di posizione predefinito.

Adobe tutela l’esperienza utente attraverso l’ottimizzazione e la salvaguardia delle prestazioni.

* Adobe garantisce i benchmark prestazionali basati sugli standard di settore, come garantiti dallo SLA di Adobe.
* La rete Edge assicura una distribuzione tempestiva dei dati.
* Adobe utilizza un approccio multilivello per garantire che le applicazioni forniscano il livello massimo di disponibilità e di affidabilità ai clienti.
* [!DNL Target] Consulting offre assistenza nell’implementazione e supporto continuo per il prodotto.

## Test di usabilità per l’ottimizzazione per i motori di ricerca (SEO) {#concept_C0C865663CAB4251B66A1F250FD25E6A}

Le funzionalità di test di [!DNL Adobe Target] sono conformi alle linee guida dei motori di ricerca.

Google incoraggia i test degli utenti. Google afferma nella sua documentazione che A/B e Multivariate Testing non danneggiano la classificazione dei motori di ricerca organica se si seguono determinate linee guida.

Per ulteriori informazioni, consulta le seguenti risorse di Google:

* [Website testing and Google Search (Test di sito web e ricerca Google)](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html)
* [Esperimenti e cloaking](https://support.google.com/analytics/answer/2576845?hl=it&amp;ref_topic=1745207)

Le linee guida sono state pubblicate su [Google Webmaster Central Blog](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html). Il post risale al 2012, ma rimane comunque la dichiarazione più recente di Google su questa questione e le linee guida restano valide.

* **Nessun cloaking**: per “cloaking” si intende mostrare un set di contenuti agli utenti e un diverso set di contenuti ai bot dei motori di ricerca. Il cloaking viene realizzato identificando specificamente i bot e fornendo loro intenzionalmente contenuti diversi.

   [!DNL Target]La piattaforma è configurata per trattare i bot dei motori di ricerca allo stesso modo di qualsiasi utente. Di conseguenza, i bot possono essere inclusi nelle attività se sono selezionati in modo casuale e “vedono” le varianti del test.

* **Usa rel=&quot;canonical&quot;**: a volte è necessario impostare un test A/B utilizzando URL diversi per le varianti. In questi casi, tutte le varianti devono contenere un tag `rel="canonical"` che fa riferimento all’URL originale (di controllo). Ad esempio, supponiamo che Adobe stia testando la propria home page utilizzando URL diversi per ogni variante. Il seguente tag canonico per la home page andrebbe nel tag `<head>` per ciascuna variante:

   `<link rel="canonical" href="https://www.adobe.com" />`

* **Usa reindirizzamenti 302 (temporanei)**: se vengono utilizzati URL diversi per le pagine delle varianti di un test, Google consiglia di indirizzare il traffico alle varianti del test mediante un reindirizzamento 302. Il reindirizzamento 302 indica ai motori di ricerca che il reindirizzamento è temporaneo ed è attivo solo finché il test è in esecuzione.

   Un reindirizzamento 302 è un reindirizzamento lato server e [!DNL Target], così come la maggior parte dei provider di ottimizzazione, utilizza funzionalità lato client. Pertanto, il reindirizzamento è un’area in cui [!DNL Target] non è pienamente conforme alle raccomandazioni di Google. Tuttavia, questo interessa solo una piccola frazione di test. L’approccio standard per l’esecuzione di test attraverso [!DNL Target] richiede la modifica dei contenuti all’interno di un singolo URL, quindi non sono necessari reindirizzamenti. Esistono casi in cui i client devono utilizzare più URL per rappresentare le varianti di test. In queste istanze, [!DNL Target] utilizza il comando JavaScript `window.location`. Questo comando indirizza gli utenti alle varianti di test, il che non indica esplicitamente se il reindirizzamento è di tipo 301 o 302.

   Adobe continua a cercare soluzioni valide per allinearsi completamente alle linee guida dei motori di ricerca. Per i client che devono utilizzare URL separati per i test, Adobe è sicuro che la corretta implementazione dei tag canonici attenui il rischio associato a questo approccio.

* **Esegui esperimenti solo per la durata strettamente necessaria**: Adobe ritiene che la “durata strettamente necessaria” sia il tempo necessario a raggiungere la rilevanza statistica. [!DNL Target][ fornisce best practice](https://docs.adobe.com/content/target-microsite/testcalculator.html) per determinare quando un test ha raggiunto questo obiettivo. Si consiglia di incorporare l’implementazione hardcoded dei test vincenti nel flusso di lavoro dei test e di assegnare le risorse appropriate.

   L’utilizzo della piattaforma [!DNL Target] per “pubblicare” i test vincenti non è consigliato come soluzione permanente. Se il test vincente viene pubblicato per il 100% degli utenti il 100% del tempo, questo approccio può essere utilizzato mentre il processo di codifica fissa del test vincente viene completato.

   È importante considerare anche le modifiche apportate dal test. Il semplice aggiornamento del colore dei pulsanti o di altri elementi non testuali minori presenti nella pagina non avrà alcuna influenza sulla classificazione organica. Tuttavia, le modifiche al testo devono essere hardcoded.

   È inoltre importante considerare l&#39;accessibilità della pagina che stai testando. Se la pagina non è accessibile ai motori di ricerca e non è mai stata progettata per essere classificata in ricerca organica in primo luogo, nessuna delle considerazioni di cui sopra si applica. Un esempio è una pagina di destinazione dedicata per una campagna e-mail.

Google afferma che seguendo queste linee guida “i test dovrebbero avere un impatto minimo o nullo sul tuo sito nei risultati di ricerca”.

Oltre a queste linee guida, Google fornisce anche una guida in più nella documentazione del suo strumento Esperimenti sui contenuti:

* “Le varianti di pagina devono conservare lo spirito dei contenuti delle pagine originali. e non devono alterare il significato o la percezione generale che gli utenti hanno dei contenuti originali.”

Google dichiara, a titolo di esempio, che “se la pagina originale di un sito presenta parole chiave non correlate alle combinazioni mostrate agli utenti, possiamo rimuovere il sito dal nostro indice”.

Adobe ritiene che sarebbe difficile modificare involontariamente il significato del contenuto originale all’interno delle varianti di test. Tuttavia, Adobe consiglia di essere consapevoli dei temi delle parole chiave in una pagina e di mantenere tali temi. Le modifiche al contenuto di una pagina, in particolare l’aggiunta o l’eliminazione di parole chiave rilevanti, possono influenzare la classificazione dell’URL nella ricerca organica. Adobe consiglia di coinvolgere il tuo partner SEO (Search Engine Optimization) come parte del protocollo di test.

## Bot {#bots}

Adobe [!DNL Target] utilizza la metrica [DeviceAtlas](https://deviceatlas.com/device-data/user-agent-tester/) “isRobot” per rilevare i bot noti in base alla stringa dell’agente utente passata nell’intestazione della richiesta.

>[!NOTE]
>
> Per le richieste [!DNL Server-Side], il valore passato nel nodo [“Context” della richiesta](https://developers.adobetarget.com/api/delivery-api/#tag/Delivery-API) ha la precedenza sulla stringa dell’agente utente per il rilevamento di bot.

Al traffico identificato come generato da un bot vengono comunque trasmessi i relativi contenuti. I bot vengono trattati come un utente normale per garantire che [!DNL Target] sia in linea con le linee guida SEO (Search Engine Optimization). Tuttavia, l’utilizzo di traffico da bot trattato come utenti normali può sfalsare i test A/B o gli algoritmi di personalizzazione. Pertanto, se nell’attività [!DNL Target] viene rilevato un bot noto, il relativo traffico viene trattato in modo leggermente diverso. La rimozione del traffico da bot genera misurazioni più accurate delle attività degli utenti effettivi.

In particolare, per il traffico proveniente da bot noti [!DNL Target] non:

* non crea né recupera un profilo visitatore;
* non registra eventuali attributi di profilo né esegue gli script di profilo;
* non consulta i segmenti Adobe Audience Manager (AAM) (se applicabile);
* Utilizzare il traffico da bot per modellare e fornire contenuti personalizzati per le attività di Recommendations, Targeting automatico, Automated Personalization o [!UICONTROL Allocazione automatica]
* non registra a fini di reporting una visita all’attività;
* Registra i dati da inviare alla piattaforma [!DNL Adobe Experience Cloud]
