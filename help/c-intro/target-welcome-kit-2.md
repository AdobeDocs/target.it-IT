---
keywords: kit di benvenuto;kit di benvenuto target;introduzione;introduzione;guida introduttiva
description: Dai un'occhiata di alto livello ad Adobe Target. Scopri le attività, i canali, l’implementazione, le integrazioni e altro ancora disponibili.
title: Dove posso trovare un'introduzione di alto livello a Target?
feature: Panoramica
exl-id: 19238d4c-b7e1-418d-96e5-c46a3769f7bf
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '2520'
ht-degree: 16%

---

# Capitolo 2: Adobe [!DNL Target]

Prima di iniziare a utilizzare [!DNL Adobe Target], potrebbe essere utile ottenere una panoramica di alto livello della soluzione. In questo capitolo, scopri le funzionalità chiave della soluzione, i punti di contatto del brand su cui puoi utilizzarla, le opzioni di implementazione, le funzioni e i flussi di lavoro importanti dell’interfaccia utente, le funzioni di governance e il suo ruolo nel [!DNL Adobe Experience Cloud] complessivo. A meno che non sia indicato come funzionalità [!DNL Adobe Target Premium], gli elementi descritti in questo capitolo sono disponibili sia con [!DNL Adobe Target Premium] che con [!DNL Adobe Target Standard]. Per ulteriori informazioni, consulta [Introduzione a Target](/help/c-intro/intro.md).

## Capacità e attività

I test e la personalizzazione sono i due tipi di funzionalità che [!DNL Target] offre e che puoi utilizzare quando crei un’attività in [!DNL Target]. Potresti vedere il termine &quot;test&quot; utilizzato in modo intercambiabile con &quot;ottimizzazione&quot; e &quot;personalizzazione&quot; utilizzato in modo intercambiabile con &quot;targeting&quot;.

In un’attività di test, confronta una variante di un’esperienza digitale con una o più altre varianti per scoprire quella che determina l’azione desiderata dal maggior numero di visitatori. [!DNL Target] offre le seguenti funzionalità di test: Test A/B, test multivariati (MVT) e allocazione automatica.

Con un’attività di personalizzazione, distribuisci un’esperienza digitale personalizzata per un gruppo specifico di visitatori o per ogni singolo visitatore. [!DNL Target] offre le seguenti funzionalità di personalizzazione: Targeting esperienza, Targeting automatico, Automated Personalization e Recommendations.

Per informazioni più approfondite su quando e come utilizzare ciascuna funzionalità, consulta [Tipi di attività di Target](/help/c-activities/target-activities-guide.md).

| Tipo di attività | Dettagli |
| --- | --- |
| Test A/B | Confronta due o più varianti di esperienze o offerte sul tuo sito web o altri punti di contatto digitali per vedere quale variazione migliora maggiormente le misure aziendali chiave durante un periodo di test pre-specificato. I test A/B sono particolarmente adatti per modifiche di grandi dimensioni, come i nuovi layout di pagine web, diversi approcci alla navigazione del sito o per trattamenti drasticamente diversi dei singoli elementi di un’esperienza digitale come copia, immagini e pulsanti di invito all’azione. [Per saperne di più](/help/c-activities/t-test-ab/test-ab.md). |
| Allocazione automatica | Identifica l’esperienza con le prestazioni migliori tra due o più esperienze e riassegna automaticamente più traffico al vincitore per aumentare le conversioni, mentre il test continua a essere eseguito e ad apprendere. Utilizza l&#39;intelligenza artificiale fornita da [!DNL Adobe Sensei]. [Per saperne di più](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md). |
| Targeting automatico<br>(Premium) | Sfrutta l’intelligenza artificiale di Adobe Sensei in [!DNL Target] per determinare e fornire la migliore esperienza di diversi visitatori in base al loro profilo cliente individuale e al comportamento dei visitatori precedenti con profili simili. Il Targeting automatico consente la personalizzazione su larga scala. [Per saperne di più](/help/c-activities/auto-target/auto-target-to-optimize.md). |
| Automated Personalization<br>(Premium) | Utilizza algoritmi di machine learning avanzati e automazione basati su [!DNL Adobe Sensei] per rivedere diverse combinazioni di immagini, copie e altri elementi in un&#39;offerta e fornire la migliore combinazione a ogni visitatore in base a quali obiettivi aziendali migliori, come un aumento delle conversioni o dei ricavi per visitatore. [Per saperne di più](/help/c-activities/t-automated-personalization/automated-personalization.md). |
| Targeting esperienza (XT) | Distribuisci contenuti a un pubblico specifico in base a una serie di regole e criteri definiti dall’utente. **[!UICONTROL Il]** targeting delle esperienze è utile per indirizzare un’esperienza o un contenuto specifico a un determinato pubblico quando si capisce che un pubblico è prezioso e si ha un buon senso delle ripercussioni dell’esperienza su di esso. [Per saperne di più](/help/c-activities/t-experience-target/experience-target.md). |
| Test multivariato (MVT) | Confronta tutte le possibili combinazioni di varianti di elementi sulla pagina o esperienza digitale, ad esempio tre diverse immagini di sfondo, due varianti di copia e due diversi colori di pulsante. MVT determina quale combinazione funziona al meglio per un pubblico specifico e quali elementi influiscono maggiormente sui risultati. [Per saperne di più](/help/c-activities/c-multivariate-testing/multivariate-testing.md). |
| Recommendations<br>(Premium) | Utilizza Adobe Sensei AI per suggerire automaticamente prodotti o contenuti che potrebbero interessare ai clienti in base alla loro attività precedente e a quella di altri clienti. [Per saperne di più](/help/c-recommendations/recommendations.md). |

## Canali

Puoi utilizzare [!DNL Target] per testare e personalizzare le esperienze digitali praticamente ovunque: punti di contatto digitali tradizionali come il tuo sito web, sito mobile e app mobile, ma anche su punti di contatto come chioschi, e-mail, dispositivi IoT, console di gioco e persino assistenti vocali come Alexa e Cortana. Molte aziende iniziano a utilizzare [!DNL Target] sul proprio sito web. Tuttavia, ricerche recenti indicano che più persone visitano i brand dai loro dispositivi mobili. L’ottimizzazione dei canali mobili è ora essenziale. Idealmente, puoi collegare le esperienze del visitatore a tutti i tuoi punti di contatto per fornire un’esperienza fluida e coerente.

| Canale | Dettagli |
| --- | --- |
| Sito Web | [!DNL Target] può essere utilizzato per eseguire attività di test A/B, Multivariate Testing, Targeting esperienza, Allocazione automatica, Targeting automatico, Automated Personalization e Recommendations su pagine di siti web mobili e applicazioni a pagina singola (SPA) e multipagina per migliorare il coinvolgimento di visitatori e clienti, aumentare le conversioni e aumentare i ricavi. |
| Web per dispositivi mobili | [!DNL Target] può essere utilizzato per eseguire tutti gli stessi tipi di attività che esegui sul sito web sulle pagine del sito web mobile in modo da migliorare in modo simile il coinvolgimento di visitatori e clienti, aumentare le conversioni e aumentare i ricavi. |
| App mobile | [!DNL Target] può essere utilizzato per testare e personalizzare le esperienze delle app mobili in base al comportamento degli utenti e al contesto mobile. [!DNL Target] ti consente di fornire interazioni che coinvolgono e convertono tramite test iterativi, targeting delle esperienze e personalizzazione basata sull’intelligenza artificiale. Per utilizzare [!DNL Target] nella tua app mobile, devi usare l’SDK di Adobe Mobile Services. |
| IoT/Ovunque | [!DNL Target] offre un’implementazione lato server in modo da poter utilizzare le stesse funzionalità di test e personalizzazione nelle attività utilizzate sul sito web tradizionale, sul sito mobile e sulle app mobili nelle e-mail e nei punti di contatto privi di browser o privi di codice JavaScript. Ad esempio, puoi testare e personalizzare chioschi, set-top box, console di gioco, assistenti vocali e altri punti di contatto non tradizionali. |

## Implementazioni

Molti di voi potrebbero voler utilizzare [!DNL Target] per testare e personalizzare i diversi punti di contatto digitali, inclusi i punti di contatto web e mobili tradizionali, ma anche i punti di contatto privi di browser o privi di codice JavaScript. In alcuni casi, la politica interna o esterna richiede livelli aggiuntivi di controllo e sicurezza. È inoltre possibile che siano presenti processi che devono essere eseguiti su un server back-end per motivi di prestazioni. Per soddisfare questa ampia varietà di utilizzi, è possibile implementare [!DNL Target] in diversi modi: lato client, lato server o una combinazione dei due.

| Tipo di implementazione | Dettagli |
| --- | --- |
| Lato client | Con questa implementazione di [!DNL Target], [!DNL Target] distribuisce le esperienze associate a un’attività direttamente al browser client. Il browser determina quale esperienza visualizzare e la visualizza. Per creare esperienze di test e personalizzazione, puoi utilizzare un editor WYSIWYG, il **[!UICONTROL Compositore esperienza visivo]** (VEC) o un&#39;interfaccia non visiva, il **[!UICONTROL Compositore esperienza basato su moduli]**. [Per saperne di più](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md). |
| Lato server | In questo tipo di implementazione [!DNL Target], un dispositivo client richiede un’esperienza tramite il server, il server invia la richiesta a [!DNL Target], [!DNL Target] invia nuovamente la risposta al server e il server decide quale esperienza distribuire al dispositivo client affinché esegua il rendering. L’esperienza non deve necessariamente essere visualizzata in un browser; può essere visualizzata in un’e-mail o un chiosco, tramite un assistente vocale oppure tramite altre esperienze non visive o su un dispositivo non basato su browser. Poiché il server risiede tra il client e [!DNL Target], questo tipo di implementazione è ideale anche se hai bisogno di maggiore controllo e sicurezza oppure in presenza di processi di backend complessi che devono essere eseguiti sul server. [Per saperne di più](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md). |
| Implementazione ibrida | In questa implementazione, scegli l’approccio di implementazione più adatto per un dato caso d’uso. Ad esempio, puoi utilizzare un’implementazione lato client per testare un’offerta in un banner eroe sulla home page, ma anche un’implementazione lato server per determinare i risultati della ricerca interna da visualizzare su un browser client, un’esperienza da visualizzare su un dashboard smart car o una risposta vocale da consegnare da un assistente vocale. |

## Elementi dell&#39;attività

In [!DNL Target] puoi creare un’attività di personalizzazione, un’attività di ottimizzazione o un’attività che ottimizza il tuo approccio di personalizzazione. Ogni attività dispone di elementi chiave: le esperienze o le offerte che stai testando o personalizzando, i tipi di pubblico o i singoli destinatari di un’esperienza, le metriche in base alle quali misuri l’impatto dell’attività e i rapporti che visualizzano visivamente tale impatto.

| Tipo di elemento | Dettagli |
| --- | --- |
| Esperienze | Un’offerta, un’immagine, un testo, un pulsante, un video, una combinazione di questi vari elementi su una pagina, un’intera pagina web o un set di pagine, ad esempio un percorso di acquisto o altra sequenza logica di pagine. Può essere anche la risposta di un assistente vocale o di uno script di servizio clienti, o addirittura un gusto personalizzato da un distributore di bevande. Puoi testare o personalizzare le esperienze nelle attività di [!DNL Target]. [Per saperne di più](/help/c-experiences/experiences.md). |
| Offerte | Un blocco di contenuto che può contenere immagini, testo, HTML, collegamenti, video, un pulsante di chiamata all’azione, una risposta dell’assistente vocale o qualsiasi altro tipo di contenuto. Un&#39;offerta potrebbe essere per uno sconto, spedizione gratuita e così via. Un’offerta può essere visualizzata su una pagina web, ma può anche essere sperimentata su qualsiasi punto di contatto del cliente, come un assistente vocale o console di gioco. Quando sottoponi a test un’offerta, ne misurerai il successo rispetto ad altre offerte o a nessuna offerta. [Per saperne di più](/help/c-experiences/c-manage-content/manage-content.md). |
| Tipi di pubblico | Gruppo di persone con le stesse caratteristiche, ad esempio nuovi visitatori, visitatori di ritorno o visitatori provenienti da una specifica area geografica. La funzione Pubblico consente di indirizzare contenuti ed esperienze diversi a tipi di pubblico specifici per ottimizzare le attività di marketing digitale presentando al momento giusto i messaggi più appropriati ai vari visitatori. Se un visitatore è identificato come parte di un pubblico di destinazione, [!DNL Target] determina quale esperienza mostrare, in base ai criteri definiti durante la creazione dell&#39;attività. [Per saperne di più](/help/c-target/target.md). |
| Metriche di successo | Misure aziendali chiave che ti consentono di determinare il successo di una determinata esperienza o offerta in un’attività [!DNL Target]. Ad esempio, puoi determinare se una nuova offerta o l’aggiunta di un articolo al carrello può aumentare il tuo ricavo per visitatore. Le metriche di successo possono essere utili per individuare problemi a livello di registrazione, ordini o percorsi di acquisto, o anche semplicemente il livello di coinvolgimento di visitatori o clienti. [Per saperne di più](/help/c-activities/r-success-metrics/success-metrics.md). |
| Rapporti | Informazioni sull’avanzamento e i risultati delle attività che consentono di prendere decisioni basate sui dati. I dati dei rapporti possono aiutarti a decidere quando terminare un test, a individuare l’esperienza o l’offerta vincente e a ottenere informazioni o risultati utili per determinare le azioni successive. [Per saperne di più](/help/c-reports/reports.md). |

## Strumenti per la creazione di attività

[!DNL Target] offre tre modi principali per configurare le attività di test e personalizzazione, il Compositore esperienza  [!UICONTROL visivo] , il Compositore esperienza basato su  [!UICONTROL moduli] e il Compositore esperienza visivo per applicazione a pagina  [!UICONTROL singola (SPA)]. Entrambi ti guidano attraverso il processo di configurazione dell’attività in tre passaggi: definire le esperienze, selezionare o definire i tipi di pubblico e selezionare le metriche di successo primarie e secondarie in base alle quali misurare i risultati dell’attività.

| Strumento | Dettagli |
| --- | --- |
| Compositore esperienza visivo | Interfaccia utente WYSIWYG che consente di creare e testare offerte ed esperienze personalizzate nel contesto del sito. Puoi creare esperienze e offerte per le attività [!DNL Target] trascinando e rilasciando, scambiando e modificando il layout e il contenuto di una pagina web (o offerta) o di una pagina web mobile. [Per saperne di più](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md). |
| [!UICONTROL Compositore esperienza basato su moduli] | Interfaccia non visiva per la creazione di esperienze, utile per creare esperienze da utilizzare in test A/B, targeting delle esperienze, Automated Personalization e attività Recommendations quando il Compositore esperienza visivo non è disponibile o se non risulta pratico. Ad esempio, puoi utilizzare il compositore basato su moduli per creare esperienze e offerte da distribuire tramite e-mail, chioschi e assistenti vocali. [Per saperne di più](/help/c-experiences/form-experience-composer.md). |
| [!UICONTROL Compositore esperienza visivo per applicazione a pagina singola (SPA)] | Il Compositore esperienza visivo per le applicazioni a pagina singola consente agli addetti al marketing di creare test e di personalizzare contenuti nelle SPA in modalità fai-da-te senza dover dipendere sempre dagli sviluppatori. Il Compositore esperienza visivo può essere utile per creare test A/B e attività di Targeting delle esperienze (XT) sui framework più diffusi, come React e Angular. [Per saperne di più](/help/c-experiences/spa-visual-experience-composer.md). |

## Governance e controllo

Per fornire alle persone giuste i ruoli giusti e i livelli associati di accesso e autorizzazioni a [!DNL Target], disponiamo di una console amministrativa. Per gli utenti [!UICONTROL Target Premium] offriamo governance e controllo più dettagliati
con [!UICONTROL Autorizzazioni Enterprise].

| Strumento | Dettagli |
| --- | --- |
| [!UICONTROL Adobe Admin Console per Enterprise] | Aggiungi utenti ad Adobe Target e assegna le autorizzazioni da Adobe Admin Console. [Per saperne di più](/help/administrating-target/c-user-management/c-user-management/user-management.md). |
| Autorizzazioni Enterprise<br> (Premium) | Un mezzo per amministrare formalmente l&#39;accesso degli utenti a [!DNL Target] a livello aziendale. Aggiungi gli utenti a [!DNL Target], assegna le autorizzazioni in base ai loro ruoli e crea aree di lavoro per i team in base a reparto, posizione globale, canale e altri raggruppamenti logici. Puoi assegnare agli utenti i ruoli di Osservatore, Editor, Editore o Approvatore. [Per saperne di più](/help/administrating-target/c-user-management/property-channel/property-channel.md). |

## Integrazioni

[!DNL Target] può integrarsi con molti sistemi di prima, seconda e terze parti. Tali
Le integrazioni possono essere utili per consentirti di accedere ai dati dei visitatori e dei clienti disponibili da tali sistemi per utilizzarli nella creazione di tipi di pubblico per test e personalizzazione. Come parte di [!DNL Adobe Experience Cloud], [!DNL Target] si integra strettamente con le soluzioni [!DNL Experience Cloud] e i relativi servizi di base.

| Integrazione | Dettagli |
| --- | --- |
| Adobe Experience Cloud | [!DNL Target] dispone di funzionalità incorporate con altre  [!DNL Adobe Experience Cloud] soluzioni per personalizzare le esperienze su larga scala. Sfrutta la potenza di [!DNL Target] insieme a [Adobe Analytics](/help/c-integrating-target-with-mac/a4t/a4t.md), [Experience Cloud Audiences](/help/c-integrating-target-with-mac/mmp.md), [Adobe Campaign](/help/c-integrating-target-with-mac/campaign-and-target.md), [Adobe Audience Manager](/help/c-integrating-target-with-mac/audience-manager-target-integration.md) (AAM) e [Adobe Experience Manager](/help/c-experiences/c-manage-content/aem-experience-fragments.md) (AEM). |
| API di Target (Premium) |  Target offre più di 40 API che puoi utilizzare per integrare Adobe Target con sistemi di prime, seconde e terze parti. [Per saperne di più](/help/api/api-overview.md). |

## Nota bene

Considera le seguenti idee prima di passare al prossimo capitolo: &quot;Sviluppa le tue idee di test e personalizzazione.&quot;

### Best practice per l’ottimizzazione

* **Buona strategia**: Qual è il nostro obiettivo e le nostre ipotesi? Sono allineate? Ad esempio, vogliamo aumentare le richieste di prestito, quindi ipotizziamo che la riduzione del numero di campi nel modulo di richiesta di prestito lo farà.
* **** Metodologia DisciplinataStiamo cominciando a testare nei posti giusti? Ad esempio, sono necessarie posizioni con traffico sufficiente e con un impatto sulle metriche rilevanti    agli affari.
* **Configurazione** correttaLa nostra attività è impostata per raggiungere il nostro obiettivo? Ad esempio, se stiamo cercando di aumentare le richieste di prestiti, dovremmo rivolgerci alle persone interessate ai prestiti e misurare i clic del pulsante &quot;Invia&quot;.
* **Analisi** approfondita: L’attività di test è stata eseguita al completamento? Cosa dicono i risultati? Esegui l’attività fino a raggiungere un’affidabilità statistica compresa tra il 95% e il 99%. Documentare il motivo per cui pensi che l&#39;esperienza vincente abbia vinto e applicare l&#39;apprendimento altrove.
* **Test iterativi**: Ci stiamo basando sugli insegnamenti delle attività precedenti? Se trovi una tattica vincente, prova a migliorarla o a apportare modifiche che funzionino con essa per migliorare ulteriormente la metrica di successo.

### Le opinioni possono influenzare negativamente i risultati

* Opinioni che possono avere un impatto negativo sulla tua efficacia. Parere, atteggiamenti e pregiudizi della persona a pagamento più elevata (HIPPO). Ad esempio, l’amministratore delegato vuole ridurre le dimensioni della casella di ricerca per liberare spazio su ogni pagina. È necessario eseguire un test per assicurarci che non riduca il numero di ricerche.
* State agendo sulle opinioni? Non mi piace l&#39;aspetto di quel test. Al cliente non piacerà per nulla questa esperienza. Anche se l’intuizione è utile, i test A/B hanno dimostrato più volte che non è sempre evidente.
* O avete una mentalità di ottimizzazione? Sono emozionato di vedere quale esperienza vince. Abbiamo abbastanza opzioni per testare?

### Le supposizioni possono anche influenzare negativamente i risultati

* Ipotesi che possono avere un impatto negativo sulla tua efficacia. La mentalità del mandriano (è così che lo fanno i nostri concorrenti). Ad esempio, tutti i nostri concorrenti usano striscioni eroici con immagini rotanti, quindi anche noi dovremmo.
* Supponendo di sapere perché qualcosa funziona o no. Supponendo che non sia necessario testare qualcosa. Ad esempio, elenciamo sempre le camere dell&#39;hotel in ordine dal più alto al più basso prezzo come impostazione predefinita.
* State facendo dei presupposti? Non è necessario testarlo, abbiamo controllato l’analisi. (Sì, ma la storia può avere più cose di quanto ci rivela analytics.)
* O avete una mentalità di ottimizzazione? Noi testiamo tutto.
