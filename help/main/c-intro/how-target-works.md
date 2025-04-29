---
keywords: Adobe Experience Platform Web SDK;aep web sdk;aep sdk;SEO (Search Engine Optimization);SEO (Search Engine Optimization);seo;cluster edge, cluster centrali;at.js;mbox.js;
description: Scopri come funziona [!DNL Adobe Target] e informazioni su librerie JavaScript (AEP Web SDK at.js), strategie di utilizzo delle chiamate al server, utilizzo, centri dati Adobe, test SEO e bot.
title: Come funziona  [!DNL Target] ?
feature: Overview
exl-id: 8a93e061-0be7-4ecc-b511-2210094547f2
source-git-commit: c5cca9b4b95289626ade1654bb508ee9f0bf35f3
workflow-type: tm+mt
source-wordcount: '2215'
ht-degree: 24%

---

# Come funziona [!DNL Adobe Target]

Scopri come funziona [!DNL Adobe Target], inclusi i dettagli sulle librerie JavaScript ([!DNL Adobe Experience Platform Web SDK] e at.js). In questo articolo vengono inoltre descritti i vari tipi di attività che è possibile creare, le strategie di conteggio dell&#39;utilizzo di [!DNL Target], l&#39;Edge Network di [!DNL Target], SEO e il rilevamento di bot.

I punti chiave includono:

* **Librerie JavaScript**: informazioni sulle librerie JavaScript [!DNL Target]: [!DNL Adobe Experience Platform Web SDK] e at.js.
* **Strategie di utilizzo delle chiamate al server**: scopri in che modo [!DNL Target] conta diverse chiamate al server, inclusi endpoint, mbox singola, mbox batch, esegui, recupero preventivo e chiamate di notifica.
* **Edge Network**: scopri come [!DNL Target] interagisce con [!DNL Adobe Experience Platform Edge Network].
* **Esperienza utente protetta**: scopri come [!DNL Adobe] garantisce la disponibilità e le prestazioni della propria infrastruttura di targeting.
* **Linee guida SEO**: segui le best practice per allineare [!DNL Target] attività alle linee guida SEO.
* **Traffico bot**: scopri come Target gestisce il traffico da bot per evitare di distorcere i test e gli algoritmi di personalizzazione.

## Librerie JavaScript di [!DNL Adobe Target] {#libraries}

Target si integra con i siti Web utilizzando [!DNL Experience Platform Web SDK] o at.js:

* **[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=it){target=_blank}**: questa libreria JavaScript lato client consente a [!DNL Adobe Experience Cloud] clienti di interagire con vari servizi tramite [!DNL Experience Platform Edge Network]. [!DNL Adobe] consiglia ai nuovi clienti [!DNL Target] di implementare [!DNL Experience Platform Web SDK].
* **[at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/overview.html?lang=it){target=_blank}**: questa libreria di implementazione per [!DNL Target] migliora i tempi di caricamento delle pagine per le implementazioni web e offre opzioni migliori per le applicazioni a pagina singola. Aggiornato spesso con nuove funzionalità, [!DNL Adobe] consiglia a tutti gli utenti di [at.js di eseguire l&#39;aggiornamento alla versione più recente](https://experienceleague-review.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}.

>[!NOTE]
>
>La libreria mbox.js è un&#39;implementazione legacy per [!DNL Target] e non è più supportata dopo il 31 marzo 2021. Esegui l’aggiornamento a [!UICONTROL Experience Platform Web SDK] (preferito) o alla versione più recente di at.js.

Fai riferimento a [!UICONTROL Experience Platform Web SDK] o at.js in ogni pagina del sito. Ad esempio, aggiungi una di queste librerie all’intestazione globale. In alternativa, utilizzare [tag in Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home){target=_blank} per implementare [!DNL Target].

Le risorse seguenti contengono informazioni dettagliate utili per implementare [!DNL Experience Platform Web SDK] o at.js:

* [[!DNL Adobe Experience Platform Web SDK] Estensione](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/sdk/overview.html?lang=it){target=_blank}
* [Implementare [!DNL Target] utilizzando [!DNL Adobe Experience Platform]](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/at-js-implementation/deploy-at-js/implement-target-using-adobe-launch){target=_blank}

Ogni volta che un visitatore richiede una pagina ottimizzata per [!DNL Target], viene inviata una richiesta in tempo reale al sistema di targeting per determinare il contenuto da distribuire. Questa richiesta viene effettuata ed evasa ogni volta che viene caricata una pagina, gestita da attività ed esperienze controllate dagli addetti al marketing. Il contenuto è destinato ai singoli visitatori del sito, ottimizzando i tassi di risposta, i tassi di acquisizione e i ricavi. I contenuti personalizzati garantiscono che i visitatori rispondano, interagiscano o effettuino acquisti.

In [!DNL Target], ogni elemento sulla pagina è parte di una singola esperienza, che può includere più elementi.

Il contenuto visualizzato dipende dal tipo di attività creata:

### [!UICONTROL A/B Test]

In un test A/B di base, il contenuto viene scelto in modo casuale tra le esperienze assegnate. Puoi impostare le percentuali di allocazione del traffico per ogni esperienza. Inizialmente, il traffico potrebbe essere distribuito in modo non uniforme a causa della suddivisione casuale, ma si equalizza con l’aumento del traffico. Ad esempio, con due esperienze, l’esperienza iniziale viene scelta in modo casuale. Un traffico ridotto può distorcere le percentuali di visitatori verso un’esperienza, ma questa situazione si compensa con un traffico maggiore.

Specifica i target percentuali per ogni esperienza. Viene generato un numero casuale per selezionare l’esperienza da visualizzare. Anche se le percentuali risultanti potrebbero non corrispondere esattamente ai target, un traffico più elevato porta a una suddivisione più vicina agli obiettivi target.

1. Un cliente richiede una pagina al server, che viene visualizzata nel browser.
1. Un cookie di prima parte viene impostato nel browser del cliente per memorizzarne il comportamento.
1. La pagina effettua una chiamata al sistema di targeting.
1. Il contenuto viene visualizzato in base alle regole di attività.

Consulta [Creare un test A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) per ulteriori informazioni.

### [!UICONTROL Auto-Allocate]

[!UICONTROL Auto-Allocate] identifica l&#39;esperienza vincente tra due o più opzioni. Quindi ridistribuisce automaticamente più traffico per il vincitore, aumentando le conversioni mentre il test continua a essere eseguito e ad apprendere.

Per ulteriori informazioni, vedere [[!UICONTROL Auto-Allocate]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4).

### [!UICONTROL Auto-Target] (AT)

[!UICONTROL Auto-Target] sfrutta l&#39;apprendimento automatico avanzato per scegliere tra più esperienze ad alte prestazioni definite dall&#39;addetto marketing. [!UICONTROL Auto-Target] offre l&#39;esperienza più personalizzata a ogni visitatore in base ai profili dei singoli clienti e al comportamento dei visitatori precedenti con profili simili. Utilizza [!UICONTROL Auto-Target] per personalizzare il contenuto e favorire le conversioni.

Per ulteriori informazioni, consulta [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md).

### [!UICONTROL Automated Personalization] (AP)

[!UICONTROL Automated Personalization] (AP) combina offerte o messaggi e utilizza l&#39;apprendimento automatico avanzato per abbinare diverse varianti a ciascun visitatore. AP personalizza i contenuti in base ai profili dei singoli clienti per favorire l’incremento.

Per ulteriori informazioni, consulta [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9).

### [!UICONTROL Experience Targeting] (XT)

[!UICONTROL Experience Targeting] (XT) fornisce contenuti a tipi di pubblico specifici in base a regole e criteri definiti dall&#39;addetto al marketing. Incluso il geotargeting, XT è utile per definire regole che rivolgono esperienze o contenuti specifici a tipi di pubblico particolari. È possibile impostare più regole in un’attività per fornire diverse varianti di contenuto a tipi di pubblico diversi. Quando i visitatori visualizzano il tuo sito, XT li valuta per determinare se soddisfano i criteri. Se si qualificano, accedono all’attività e visualizzano l’esperienza progettata per loro. Puoi creare esperienze per più tipi di pubblico all&#39;interno di una singola attività.

Per ulteriori informazioni, consulta [Targeting esperienza](/help/main/c-activities/t-experience-target/experience-target.md#task_A53DF336CB9F4D7BB87EF2106099EFC4).

### [!UICONTROL Multivariate Test] (MVT)

[!UICONTROL Multivariate Testing] (MVT) confronta le combinazioni di offerte negli elementi di pagina per determinare quale combinazione funziona meglio per un pubblico specifico. MVT consente di identificare quale elemento influisce maggiormente sul successo dell’attività.

Per ulteriori informazioni, consulta [Test multivariato](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md#concept_628695CDC71B449B8DCC2F5654C11499).

### [!UICONTROL Recommendations]

Le attività [!UICONTROL Recommendations] visualizzano automaticamente prodotti o contenuti che potrebbero interessare i clienti in base alla loro attività precedente o ad altri algoritmi. I consigli aiutano a indirizzare i clienti verso elementi rilevanti che altrimenti potrebbero non scoprire.

Consulta [Raccomandazioni](/help/main/c-recommendations/recommendations.md#concept_7556C8A4543942F2A77B13A29339C0C0) per ulteriori informazioni.

<!--
## How [!DNL Target] counts server-call usage {#usage}

[!DNL Target] counts only server calls that provide value to customers. The following table shows how [!DNL Target] counts endpoints, single mbox, batch mbox calls, execute, prefetch, and notification calls.

The following information helps you understand the counting strategy used for [!DNL Target] server calls, as shown in the table below:

* **Count Once**: Counts once per API call.
* **Count the Number of mboxes**: Counts the number of mboxes under the array in the payload of a single API call.
* **Ignore**: Is not counted at all.
* **Count the Number of Views (Once)**: Counts the number of views under the array in the payload. In a typical implementation, a view notification has only one view under the notifications array, making this equivalent to counting once in most implementations.

|Endpoint|Fetch type|Options|Counting strategy|
|--- |--- |--- |-- |
|`rest//v1/mbox`|Single|[!UICONTROL execute]|Count once|
|`rest/v2/batchmbox`|Batch|[!UICONTROL execute]|Count the number of mboxes|
||Batch|[!UICONTROL prefetch]|Ignore|
||Batch|[!UICONTROL notifications]|Count the number of mboxes|
|`/ubox/[raw\|image\|page]`|Single|[!UICONTROL execute]|Count once|
|`rest/v1/delivery`<p>`/rest/v1/target-upstream`|Single|[!UICONTROL execute] > [!UICONTROL pageLoad]|Count once|
||Single|[!UICONTROL prefetch] > [!UICONTROL pageLoad]|Ignore|
||Single|[!UICONTROL prefetch] > [!UICONTROL views]|Ignore|
||Batch|[!UICONTROL execute] > [!UICONTROL mboxes]|Count the number of mboxes|
||Batch|[!UICONTROL prefetch] > [!UICONTROL mboxes]|Ignore|
||Batch|[!UICONTROL notifications] > [!UICONTROL views]|Count the number of views (once)|
||Batch|[!UICONTROL notifications] > [!UICONTROL pageLoad]|Count once|
||Batch|[!UICONTROL notifications] > type ([!UICONTROL conversions])|Count once|
||Batch|[!UICONTROL notifications] > [!UICONTROL mboxes]|Count the number of mboxes|

-->

## La rete Edge {#concept_0AE2ED8E9DE64288A8B30FCBF1040934}

&quot;Edge&quot; è un’architettura di servizio geograficamente distribuita che garantisce tempi di risposta ottimali ai visitatori che richiedono contenuti, indipendentemente dalla loro posizione.

Per migliorare i tempi di risposta, l’ambiente Edge di [!DNL Target] ospita solo logica di attività, profili memorizzati nella cache e informazioni sulle offerte.

I database di attività e contenuti, i dati di [!DNL Analytics], le API e le interfacce utente per gli addetti al marketing si trovano in [!DNL Adobe] cluster centrali. Gli aggiornamenti vengono inviati a [!DNL Target] Edge, che vengono sincronizzati automaticamente con i cluster centrali per aggiornare continuamente i dati delle attività memorizzati nella cache. Anche la modellazione 1:1 è memorizzata su ogni server Edge di, consentendo l’elaborazione locale di richieste complesse.

Ogni cluster Edge contiene tutte le informazioni necessarie per rispondere alle richieste di contenuto dei visitatori e tenere traccia dei dati di analisi. Le richieste dei visitatori vengono indirizzate al nodo Edge più vicino.

Per ulteriori informazioni, consulta il white paper [Adobe Target Security Overview](https://www.adobe.com/content/dam/cc/it/security/pdfs/AdobeTargetSecurityOverview.pdf) (Panoramica sulla sicurezza di Adobe Target).

[!DNL Target] è ospitato su data center di Adobe Adobe (propri o noleggiati) in tutto il mondo.

Le posizioni del cluster centrale ospitano sia centri di raccolta dati che centri di elaborazione dati. Le posizioni del cluster Edge contengono solo centri di raccolta dati. Ogni suite di rapporti viene assegnata a un centro di elaborazione dati specifico.

I dati relativi all’attività del sito del cliente vengono raccolti dal più vicino dei sette cluster Edge. Questi dati vengono quindi indirizzati a una destinazione cluster centrale predefinita (Oregon, Dublino o Singapore) per l’elaborazione. I dati del profilo del visitatore vengono memorizzati nel cluster Edge più vicino al visitatore del sito. Le posizioni del cluster Edge includono le posizioni del cluster centrale, nonché Virginia, Mumbai, Sydney e Tokyo.

Invece di elaborare tutte le richieste di targeting da un’unica posizione, le richieste vengono gestite dal cluster Edge più vicino al visitatore. Questo approccio attenua l&#39;impatto del tempo di viaggio in rete e su Internet.

![Mappa che mostra i diversi tipi di server Target](/help/main/c-intro/assets/target-servers.png)

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
>[!DNL Target] non dispone attualmente di un cluster Edge in Cina, limitando le prestazioni dei visitatori per [!DNL Target] clienti nella regione. Il firewall e l’assenza di cluster Edge possono influire sulle esperienze del sito, rallentando i tempi di rendering e caricamento delle pagine. Inoltre, gli addetti al marketing possono riscontrare una latenza durante l&#39;utilizzo dell&#39;interfaccia utente di creazione di [!DNL Target].

Se necessario, puoi inserire nell’elenco Consentiti i cluster di Edge [!DNL Target]. Per ulteriori informazioni, consulta [elenco Consentiti nodi edge di Target](https://experienceleague.adobe.com/en/docs/target-dev/developer/implementation/privacy/allowlist-edges){target=_blank}.

## Esperienza di utilizzo protetta {#concept_40A5E781D90A41E4955F80EA9E5F8F96}

[!DNL Adobe] garantisce la disponibilità e le prestazioni della propria infrastruttura di targeting nel modo più affidabile possibile. Tuttavia, i problemi di comunicazione tra il browser di un visitatore e i server [!DNL Adobe] possono interrompere la distribuzione del contenuto.

Per fornire protezione da interruzioni dei servizi e da problemi di connettività, tutte le posizioni sono impostate per includere il contenuto predefinito (definito dal cliente). Questo contenuto predefinito viene visualizzato se il browser del visitatore non riesce a connettersi a [!DNL Target].

Non vengono apportate modifiche alla pagina se il browser del visitatore non riesce a connettersi entro un periodo di timeout definito (impostazione predefinita: 15 secondi). Se questa soglia di timeout viene raggiunta, viene visualizzato il contenuto di posizione predefinito.

[!DNL Adobe] tutela l’esperienza utente attraverso l’ottimizzazione e la salvaguardia delle prestazioni.

* [!DNL Adobe] garantisce i benchmark delle prestazioni basati sugli standard di settore, garantiti da [!UICONTROL Adobe Service Level Agreement].
* La rete Edge assicura una distribuzione tempestiva dei dati.
* [!UICONTROL Adobe] utilizza un approccio multilivello per proteggere le applicazioni, fornendo il massimo livello di disponibilità e affidabilità ai clienti.
* [!DNL Target] Consulting offre assistenza nell’implementazione e supporto continuo per il prodotto.

## Test di usabilità per l’ottimizzazione per i motori di ricerca (SEO) {#concept_C0C865663CAB4251B66A1F250FD25E6A}

[!DNL Adobe Target] si allinea alle linee guida dei motori di ricerca per i test. [!DNL Google] incoraggia i test degli utenti e afferma che A/B e [!UICONTROL Multivariate Testing] non danneggiano la classificazione dei motori di ricerca organica se vengono seguite determinate linee guida.

Le funzionalità di test di [!DNL Adobe Target] sono conformi alle linee guida dei motori di ricerca.

Per ulteriori informazioni, consulta le seguenti risorse di Google:

* [Website testing and Google Search (Test di sito web e ricerca Google)](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html)
* [Esperimenti e cloaking](https://support.google.com/analytics/answer/12979939?hl)


Le linee guida sono state pubblicate su [Google Webmaster Central Blog](https://webmasters.googleblog.com/2012/08/website-testing-google-search.html). Anche se il post risale al 2012, rimane la dichiarazione più recente di [!DNL Google] sull&#39;argomento, e le linee guida sono ancora rilevanti.

* **Nessun cloaking**: per &quot;cloaking&quot; si intende mostrare un set di contenuti agli utenti e un diverso set ai bot dei motori di ricerca, identificando in modo specifico i bot e fornendo loro contenuti diversi.

  [!DNL Target] è configurato per trattare i bot dei motori di ricerca allo stesso modo di qualsiasi utente. Di conseguenza, i bot possono essere inclusi nelle attività se sono selezionati in modo casuale e &quot;vedono&quot; le varianti di test.

* **Usa rel=&quot;canonical&quot;**: a volte un test A/B richiede URL diversi per le varianti. In questi casi, tutte le varianti devono includere un tag rel=&quot;canonical&quot; che fa riferimento all’URL originale (di controllo). Ad esempio, se [!DNL Adobe] sta testando la propria home page con URL diversi per ogni variante, il seguente tag canonical per la home page deve essere inserito nel tag `<head>` di ogni variante:

  `<link rel="canonical" href="https://www.adobe.com" />`

* **Usa reindirizzamenti 302 (temporanei)**: se vengono utilizzati URL diversi per le pagine delle varianti di un test, [!DNL Google] consiglia di indirizzare il traffico alle varianti del test mediante un reindirizzamento 302. Il reindirizzamento 302 informa i motori di ricerca che il reindirizzamento è temporaneo e attivo solo durante l’esecuzione del test.

  Un reindirizzamento 302 è un reindirizzamento lato server, mentre [!DNL Target] e la maggior parte dei provider di ottimizzazione utilizzano funzionalità lato client. Pertanto, [!DNL Target] non è pienamente conforme ai consigli di [!DNL Google] per i reindirizzamenti. Tuttavia, questo influisce solo su una piccola frazione di test. L&#39;approccio standard per l&#39;esecuzione dei test tramite [!DNL Target] prevede la modifica dei contenuti all&#39;interno di un singolo URL, eliminando la necessità di reindirizzamenti. Nei casi in cui sono necessari più URL per le varianti di test, [!DNL Target] utilizza il comando JavaScript `window.location`, che non specifica se il reindirizzamento è di tipo 301 o 302.

  [!DNL Adobe] sta cercando attivamente soluzioni per rispettare completamente le linee guida dei motori di ricerca. Per i client che necessitano di URL separati per il test, [!DNL Adobe] ritiene che la corretta implementazione dei tag canonici attenui i rischi associati.

* **Eseguire esperimenti solo per la durata strettamente necessaria**: [!DNL Adobe] definisce &quot;per la durata strettamente necessaria&quot; il tempo necessario per raggiungere la rilevanza statistica. [!DNL Target] offre le best practice e il [!DNL Adobe Target] [Calcolatore dimensioni campione](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6) per determinare quando il test ha raggiunto questo punto. [!DNL Adobe] consiglia di incorporare l&#39;implementazione hardcoded dei test vincenti nel flusso di lavoro dei test e di allocare le risorse appropriate.

  L&#39;utilizzo di [!DNL Target] per &quot;pubblicare&quot; i test vincenti non è consigliato come soluzione permanente. Se il test vincente viene pubblicato per il 100% degli utenti tutto il tempo, questo approccio può essere utilizzato temporaneamente durante la codifica fissa del test vincente.

  Considera le modifiche apportate al test. Aggiornamenti minori, come i colori dei pulsanti, non influiscono sulle classificazioni organiche. Tuttavia, le modifiche al testo devono essere codificate.

  Inoltre, considera l’accessibilità della pagina che stai testando. Se la pagina non è accessibile ai motori di ricerca e non è mai stata concepita per essere classificata nella ricerca organica, queste considerazioni non si applicano. Un esempio è una pagina di destinazione dedicata per una campagna e-mail.

Google afferma che seguendo queste linee guida “i test dovrebbero avere un impatto minimo o nullo sul tuo sito nei risultati di ricerca”.

Oltre a queste linee guida, Google fornisce anche una guida in più nella documentazione del suo strumento Esperimenti sui contenuti:

* “Le varianti di pagina devono conservare lo spirito dei contenuti delle pagine originali. e non devono alterare il significato o la percezione generale che gli utenti hanno dei contenuti originali.”

Google dichiara, a titolo di esempio, che “se la pagina originale di un sito presenta parole chiave non correlate alle combinazioni mostrate agli utenti, possiamo rimuovere il sito dal nostro indice”.

[!UICONTROL Adobe] ritiene che sarebbe difficile modificare involontariamente il significato del contenuto originale all&#39;interno delle varianti di test. Tuttavia, [!UICONTROL Adobe] consiglia di essere a conoscenza dei temi delle parole chiave in una pagina e di mantenere tali temi. Le modifiche al contenuto di una pagina, in particolare l’aggiunta o l’eliminazione di parole chiave rilevanti, possono influenzare la classificazione dell’URL nella ricerca organica. [!DNL Adobe] consiglia di coinvolgere il tuo partner SEO (Search Engine Optimization) come parte del protocollo di test.

## Bot {#bots}

[!DNL Target] utilizza la metrica [DeviceAtlas](https://deviceatlas.com/device-data/user-agent-tester/) &quot;isRobot&quot; per rilevare i bot noti in base alla stringa dell&#39;agente utente passata nell&#39;intestazione della richiesta.

>[!NOTE]
>
> Per le richieste [!DNL Server-Side], il valore passato nel nodo [“Context” della richiesta](https://developers.adobetarget.com/api/delivery-api/#tag/Delivery-API) ha la precedenza sulla stringa dell’agente utente per il rilevamento di bot.

Al traffico identificato come generato da bot vengono comunque trasmessi i relativi contenuti. I bot vengono trattati come utenti normali per garantire che [!DNL Target] sia allineato con le linee guida SEO (Search Engine Optimization). Tuttavia, il traffico da bot può distorcere i test A/B o gli algoritmi di personalizzazione se trattato come utenti normali. Pertanto, il traffico noto proveniente da bot nell&#39;attività [!DNL Target] viene trattato in modo diverso. La rimozione del traffico da bot fornisce una misurazione più precisa dell’attività dell’utente.

Per il traffico noto proveniente da bot, [!DNL Target]:

* non crea né recupera un profilo visitatore;
* Registra gli attributi del profilo o esegui gli script di profilo
* non consulta i segmenti di [!DNL Adobe Audience Manager] (AAM) (se applicabile);
* Utilizza il traffico da bot per modellare o trasmettere contenuti personalizzati per [!UICONTROL Recommendations], [!UICONTROL Auto-Target], [!UICONTROL Automated Personalization] o [!UICONTROL Auto-Allocate] attività
* non registra a fini di reporting una visita all’attività;
* Registra i dati da inviare alla piattaforma [!DNL Adobe Experience Cloud]

Per il traffico noto proveniente da bot, quando si utilizza [!UICONTROL Analytics for Target] (A4T), [!DNL Target]:

* non invia eventi a [!DNL Analytics].

Per il traffico noto proveniente da bot durante l&#39;utilizzo della registrazione `client_side`, [!DNL Target] non restituisce:

* `tnta payload`
