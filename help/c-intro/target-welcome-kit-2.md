---
keywords: kit di benvenuto;kit di benvenuto di destinazione;introduzione;introduzione;guida introduttiva
description: ' kit di benvenuto Adobe Target - Capitolo 2 - Scoprire'
title: Kit di benvenuto - Capitolo 2 - Panoramica
feature: Overview
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '2510'
ht-degree: 16%

---


# Capitolo 2:  Adobe Target

Prima di iniziare a utilizzare [!DNL Adobe Target], potrebbe essere utile ottenere una panoramica di alto livello della soluzione. In questo capitolo, scopri le funzionalità chiave della soluzione, i punti di contatto del marchio su cui puoi utilizzarla, le opzioni di implementazione, le funzioni e i flussi di lavoro dell&#39;interfaccia utente importanti, le funzioni di governance e il ruolo che svolge nel [!DNL Adobe Experience Cloud] nel suo complesso. A meno che non venga indicato come funzionalità [!DNL Adobe Target Premium], gli elementi descritti in questo capitolo sono disponibili sia con [!DNL Adobe Target Premium] che con [!DNL Adobe Target Standard]. Per ulteriori informazioni, vedere [Introduzione a Target](/help/c-intro/intro.md).

## Capacità e attività

I test e la personalizzazione sono i due tipi più ampi di funzionalità offerte da [!DNL Target] e che potete utilizzare quando create un&#39;attività in [!DNL Target]. Potreste vedere il termine &quot;test&quot; utilizzato in modo intercambiabile con &quot;ottimizzazione&quot; e &quot;personalizzazione&quot; utilizzato in modo intercambiabile con &quot;targeting&quot;.

In un&#39;attività di test, confrontate una variante di un&#39;esperienza digitale con una o più altre varianti per scoprire che determinano l&#39;azione desiderata da parte del maggior numero di visitatori. [!DNL Target] offre le seguenti funzionalità di test: Test A/B, test multivariati (MVT) e allocazione automatica.

Con un&#39;attività di personalizzazione, puoi offrire un&#39;esperienza digitale personalizzata per un gruppo specifico di visitatori o per ogni singolo visitatore. [!DNL Target] offre le seguenti funzionalità di personalizzazione: Targeting delle esperienze, targeting automatico,  Automated Personalization e Recommendations.

Per una comprensione più dettagliata di quando e come utilizzare ciascuna funzionalità, vedete [Tipi di attività di destinazione](/help/c-activities/target-activities-guide.md).

| Tipo di attività | Dettagli |
| --- | --- |
| Test A/B | Confronta due o più varianti di esperienze o offerte sul tuo sito Web o su altri punti di contatto per clienti digitali per scoprire quale variazione migliora maggiormente le misure aziendali chiave durante un periodo di test prestabilito. I test A/B sono adatti per modifiche di grandi dimensioni, come nuovi layout di pagine Web, approcci diversi alla navigazione del sito o trattamenti drasticamente diversi di singoli elementi di un&#39;esperienza digitale come copia, immagini e pulsanti call-to-action. [Per saperne di più](/help/c-activities/t-test-ab/test-ab.md). |
| Allocazione automatica | Identificate l&#39;esperienza con le prestazioni migliori tra due o più esperienze, e riassegnate automaticamente più traffico al vincitore per aumentare le conversioni mentre il test continua a essere eseguito e imparare. Utilizza l&#39;intelligenza artificiale basata su [!DNL Adobe Sensei]. [Per saperne di più](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md). |
| Auto-Target<br>(Premium) | Sfruttate  Adobe Sensei AI in [!DNL Target] per determinare e fornire la migliore esperienza di diversi visitatori in base al proprio profilo cliente individuale e al comportamento dei visitatori precedenti con profili simili. Auto-Target consente la personalizzazione su larga scala. [Per saperne di più](/help/c-activities/auto-target/auto-target-to-optimize.md). |
|  Automated Personalization<br>(Premium) | Utilizzate algoritmi di machine learning avanzati e automazione basati su [!DNL Adobe Sensei] per rivedere diverse combinazioni di immagini, copie e altri elementi in un&#39;offerta e fornire la combinazione ottimale a ogni visitatore in base ai quali si conseguono i migliori obiettivi aziendali, ad esempio maggiori conversioni o ricavi per visitatore. [Per saperne di più](/help/c-activities/t-automated-personalization/automated-personalization.md). |
| Targeting esperienza (XT) | Distribuite i contenuti a un pubblico specifico in base a una serie di regole e criteri definiti dall&#39;utente. **[!UICONTROL Il]** targeting delle esperienze è utile per indirizzare un&#39;esperienza o un contenuto specifico a un pubblico particolare, se capisci che un pubblico è prezioso e ha un buon senso dell&#39;esperienza che risuona con loro. [Per saperne di più](/help/c-activities/t-experience-target/experience-target.md). |
| Test multivariato (MVT) | Confrontate tutte le possibili combinazioni di variazioni di elementi sulla pagina o esperienza digitale, ad esempio tre diverse immagini di sfondo, due varianti di copia e due diversi colori di pulsante. MVT determina quale combinazione esegue al meglio le prestazioni per un pubblico specifico e quali elementi influiscono maggiormente sui risultati. [Per saperne di più](/help/c-activities/c-multivariate-testing/multivariate-testing.md). |
| Recommendations<br>(Premium) | Utilizzate  Adobe Sensei AI per suggerire automaticamente prodotti o contenuti che potrebbero interessare i clienti in base alla loro attività precedente e a quella di altri clienti. [Per saperne di più](/help/c-recommendations/recommendations.md). |

## Canali

Potete utilizzare [!DNL Target] per testare e personalizzare le esperienze digitali praticamente ovunque: punti di contatto digitali tradizionali come il vostro sito Web, sito mobile e app mobili, ma anche su punti di contatto come chioschi, e-mail, dispositivi IoT, console di gioco e persino su assistenti vocali come  Alexa e Cortana. Molte aziende iniziano a utilizzare [!DNL Target] sul proprio sito Web. Tuttavia, ricerche recenti indicano che più persone visitano i marchi dai loro dispositivi mobili. È ora essenziale ottimizzare i canali mobili. Idealmente, metterai in contatto le esperienze del visitatore con tutti i punti di contatto per offrire un’esperienza coerente e senza soluzione di continuità.

| Canale | Dettagli |
| --- | --- |
| Sito Web | [!DNL Target] può essere utilizzato per eseguire attività di test A/B, Multivariate Testing, Targeting delle esperienze, allocazione automatica, targeting automatico, Automated Personalization  e Recommendations su pagine di applicazioni a pagina singola (SPA) e siti Web per dispositivi mobili, per migliorare il coinvolgimento dei visitatori e dei clienti, aumentare le conversioni e aumentare i ricavi. |
| Mobile Web | [!DNL Target] può essere utilizzato per eseguire tutti gli stessi tipi di attività che si esegue sul sito Web sulle pagine del sito Web per dispositivi mobili per migliorare in modo simile il coinvolgimento di visitatori e clienti, aumentare le conversioni e aumentare i ricavi. |
| App mobile | [!DNL Target] può essere utilizzata per testare e personalizzare le esperienze delle app mobili in base al comportamento degli utenti e al contesto dei dispositivi mobili. [!DNL Target] consente di fornire interazioni che coinvolgono e si convertono attraverso test iterativi, nonché Experience Targeting e personalizzazione basata sull&#39;intelligenza artificiale. Per utilizzare [!DNL Target] nell&#39;app mobile, devi utilizzare l&#39;SDK di Mobile Services  Adobe. |
| IoT/Everywhere | [!DNL Target] offre un&#39;implementazione lato server che consente di utilizzare le stesse funzionalità di test e personalizzazione nelle attività utilizzate nel sito Web, nel sito mobile e nelle app mobili tradizionali nelle e-mail e nei punti di contatto privi di browser o che non utilizzano codice JavaScript. Ad esempio, potete testare e personalizzare chioschi, set-top box, console per videogiochi, assistenti vocali e altri punti di contatto non tradizionali. |

## Implementazioni

Molti di voi potrebbero voler utilizzare [!DNL Target] per eseguire test e personalizzare i diversi punti di contatto digitali, inclusi i punti di contatto Web e mobili tradizionali, ma anche i punti di contatto privi di browser o che non utilizzano codice JavaScript. In alcuni casi, la politica interna o esterna richiede livelli aggiuntivi di controllo e sicurezza. È inoltre possibile che siano necessari processi da eseguire su un server back-end per motivi di prestazioni. Per soddisfare questa ampia varietà di usi, abbiamo la possibilità di implementare [!DNL Target] in modi diversi: lato client, lato server o una combinazione di entrambi.

| Tipo di implementazione | Dettagli |
| --- | --- |
| Lato client | Con questa implementazione di [!DNL Target], [!DNL Target] distribuisce le esperienze associate a un&#39;attività direttamente al browser client. Il browser determina quale esperienza visualizzare e la visualizza. Dal lato client, potete utilizzare un editor WYSIWYG, **[!UICONTROL Visual Experience Composer]** (VEC) o un&#39;interfaccia non visiva, il **[!UICONTROL Experience Composer basato su moduli]**, per creare esperienze di test e personalizzazione. [Per saperne di più](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md). |
| Lato server | In questo tipo di implementazione [!DNL Target], un dispositivo client effettua una richiesta per un&#39;esperienza attraverso il server, il server invia la richiesta a [!DNL Target], [!DNL Target] invia di nuovo la risposta al server e il server prende la decisione sull&#39;esperienza da distribuire al dispositivo client affinché venga eseguito il rendering. L’esperienza non deve necessariamente essere visualizzata in un browser; può essere visualizzata in un’e-mail o un chiosco, tramite un assistente vocale oppure tramite altre esperienze non visive o su un dispositivo non basato su browser. Poiché il server risiede tra il client e [!DNL Target], questo tipo di implementazione è ideale anche se hai bisogno di maggiore controllo e sicurezza oppure in presenza di processi di backend complessi che devono essere eseguiti sul server. [Per saperne di più](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md). |
| Implementazione ibrida | In questa implementazione, scegli l’approccio di implementazione più adatto a un determinato caso di utilizzo. Ad esempio, potete utilizzare un&#39;implementazione lato client per sottoporre a test A/B un&#39;offerta in un banner hero sulla pagina principale, ma anche un&#39;implementazione lato server per determinare i risultati della ricerca interna da visualizzare su un browser client, un&#39;esperienza da visualizzare su un dashboard smart car o una risposta vocale da fornire da un assistente vocale. |

## Elementi dell&#39;attività

In [!DNL Target], puoi creare un&#39;attività di personalizzazione, un&#39;attività di ottimizzazione o un&#39;attività che ottimizza il tuo approccio di personalizzazione. Ogni attività ha elementi chiave: le esperienze o le offerte che state testando o personalizzando, i tipi di pubblico o i singoli destinatari di un&#39;esperienza, le metriche con cui misurate l&#39;impatto dell&#39;attività e i rapporti che visualizzano visivamente tale impatto.

| Tipo elemento | Dettagli |
| --- | --- |
| Esperienze | Un’offerta, un’immagine, un testo, un pulsante, un video, una combinazione di questi vari elementi su una pagina, un’intera pagina web o un set di pagine, ad esempio un percorso di acquisto o altra sequenza logica di pagine. Può essere anche la risposta di un assistente vocale o di uno script di servizio clienti, o addirittura un gusto personalizzato da un distributore di bevande. Puoi testare o personalizzare le esperienze nelle attività di [!DNL Target]. [Per saperne di più](/help/c-experiences/experiences.md). |
| Offerte | Un blocco di contenuto che può contenere immagini, testo, HTML, collegamenti, video, un pulsante di chiamata all&#39;azione, una risposta di Assistente vocale o qualsiasi altro tipo di contenuto. Un&#39;offerta potrebbe essere per uno sconto, spedizione gratuita e così via. Un&#39;offerta può essere visualizzata su una pagina Web, ma può anche essere utilizzata da qualsiasi punto di contatto del cliente, ad esempio un assistente vocale o una console di gioco. Quando sottoponete a test un&#39;offerta, misurate il suo successo rispetto ad altre offerte o a nessuna offerta. [Per saperne di più](/help/c-experiences/c-manage-content/manage-content.md). |
| Tipi di pubblico | Gruppo di persone con le stesse caratteristiche, ad esempio nuovi visitatori, visitatori di ritorno o visitatori provenienti da una specifica area geografica. La funzione Pubblico consente di indirizzare contenuti ed esperienze diversi a tipi di pubblico specifici per ottimizzare le attività di marketing digitale presentando al momento giusto i messaggi più appropriati ai vari visitatori. Se un visitatore viene identificato come parte di un&#39;audience di destinazione, [!DNL Target] determina quale esperienza visualizzare, in base ai criteri definiti durante la creazione dell&#39;attività. [Per saperne di più](/help/c-target/target.md). |
| Metriche di successo | Misure aziendali chiave che consentono di determinare il successo di una determinata esperienza o offerta in un&#39;attività [!DNL Target]. Ad esempio, puoi determinare se una nuova offerta o l’aggiunta di un articolo al carrello può aumentare il tuo ricavo per visitatore. Le metriche di successo possono essere utili per individuare problemi a livello di registrazione, ordini o percorsi di acquisto, o anche semplicemente il livello di coinvolgimento di visitatori o clienti. [Per saperne di più](/help/c-activities/r-success-metrics/success-metrics.md). |
| Rapporti | Informazioni sull&#39;avanzamento e sui risultati delle attività che consentono di prendere decisioni in base ai dati. I dati dei rapporti possono aiutarti a decidere quando terminare un test, a individuare l’esperienza o l’offerta vincente e a ottenere informazioni o risultati utili per determinare le azioni successive. [Per saperne di più](/help/c-reports/reports.md). |

## Strumenti per la creazione di attività

[!DNL Target] offre tre modi principali per configurare le attività di test e personalizzazione,  [!UICONTROL Visual Experience Composer]  (VEC), Experience Composer (Compositore esperienza visivo) basato su  [!UICONTROL moduli] e  [!UICONTROL Single Page Application (SPA) Visual Experience Composer (Compositore esperienza visivo)]. Entrambe le procedure guidano l&#39;utente attraverso il processo di configurazione dell&#39;attività in tre fasi: definire le esperienze, selezionare o definire i tipi di pubblico e selezionare le metriche di successo primarie e secondarie in base alle quali misurare i risultati dell&#39;attività.

| Strumento | Dettagli |
| --- | --- |
| Compositore esperienza visivo | Interfaccia utente WYSIWYG che consente di creare e testare facilmente esperienze e offerte personalizzate nel contesto del sito. Potete creare esperienze e offerte per le attività [!DNL Target] trascinando, sostituendo e modificando il layout e il contenuto di una pagina Web (o offerta) o di una pagina Web per dispositivi mobili. [Per saperne di più](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md). |
| [!UICONTROL Compositore esperienza basato su moduli] | Un&#39;interfaccia per la creazione di esperienze e offerte non visive che è utile per creare esperienze da utilizzare nei test A/B, nel targeting delle esperienze  nelle attività Automated Personalization e Recommendations quando Visual Experience Composer (Compositore esperienza visivo) non è disponibile o pratico per l&#39;uso. Ad esempio, puoi utilizzare il compositore basato su moduli per creare esperienze e offerte da distribuire tramite e-mail, chioschi e assistenti vocali. [Per saperne di più](/help/c-experiences/form-experience-composer.md). |
| [!UICONTROL Visual Experience Composer (Compositore esperienza visivo SPA pagina singola)] | Il Compositore esperienza visivo per le applicazioni a pagina singola consente agli addetti al marketing di creare test e di personalizzare contenuti nelle SPA in modalità fai-da-te senza dover dipendere sempre dagli sviluppatori. Il Compositore esperienza visivo può essere utile per creare test A/B e attività di Targeting delle esperienze (XT) sui framework più diffusi, come React e Angular. [Per saperne di più](/help/c-experiences/spa-visual-experience-composer.md). |

## Governance e controllo

Per fornire alle persone giuste i ruoli giusti e i livelli associati di accesso e autorizzazioni a [!DNL Target], abbiamo una console amministrativa. Per gli utenti di [!UICONTROL Target Premium], offriamo una gestione e un controllo più dettagliati
con [!UICONTROL Enterprise Permissions].

| Strumento | Dettagli |
| --- | --- |
| [!UICONTROL Adobe Admin Console per Enterprise] | Aggiungete utenti a  Adobe Target e assegnate le autorizzazioni dall’Adobe Admin Console. [Per saperne di più](/help/administrating-target/c-user-management/c-user-management/user-management.md). |
| [!UICONTROL Enterprise ]Permissions<br>(Premium) | Un mezzo per amministrare formalmente l&#39;accesso dell&#39;utente a livello aziendale a [!DNL Target]. Aggiungi utenti a [!DNL Target], assegna autorizzazioni in base ai loro ruoli e crea aree di lavoro per team in base a diversi reparti, posizioni globali, canali e altri raggruppamenti logici. È possibile assegnare agli utenti i ruoli di Osservatore, Editor, Editore o Approver. [Per saperne di più](/help/administrating-target/c-user-management/property-channel/property-channel.md). |

## Integrazioni

[!DNL Target] può essere integrato con molti sistemi di prime, seconde e di terze parti. Queste
le integrazioni possono essere utili per consentirvi di accedere ai dati di visitatori e clienti disponibili da tali sistemi per la creazione di audience da sottoporre a test e per la personalizzazione. Come parte di [!DNL Adobe Experience Cloud], [!DNL Target] si integra strettamente con le soluzioni [!DNL Experience Cloud] e con i relativi servizi di base.

| Integrazione | Dettagli |
| --- | --- |
| Adobe Experience Cloud | [!DNL Target] dispone di funzionalità incorporate con altre  [!DNL Adobe Experience Cloud] soluzioni per personalizzare le esperienze su larga scala. Sfruttate la potenza di [!DNL Target] insieme a [ Adobe Analytics](/help/c-integrating-target-with-mac/a4t/a4t.md), [ pubblico di Experienci Cloud](/help/c-integrating-target-with-mac/mmp.md), [ Adobe Campaign](/help/c-integrating-target-with-mac/campaign-and-target.md), [Adobe Audience Manager](/help/c-integrating-target-with-mac/audience-manager-target-integration.md) (AAM) e [Adobe Experience Manager](/help/c-experiences/c-manage-content/aem-experience-fragments.md) (AEM). |
| API Target (Premium) |  Target offre più di 40 API che potete utilizzare per integrare  Adobe Target con sistemi di prime, seconde e terze parti. [Per saperne di più](/help/api/api-overview.md). |

## Nota bene

Considerate le seguenti idee prima di passare al prossimo capitolo: &quot;Sviluppa le tue idee di test e personalizzazione.&quot;

### Best practice per l&#39;ottimizzazione

* **Buona strategia**: Qual è il nostro obiettivo e le nostre ipotesi? Sono allineati? Ad esempio, vogliamo aumentare le richieste di prestito, quindi ipotizziamo che la riduzione del numero di campi nel modulo di domanda lo farà.
* **Metodologia** DisciplinataStiamo iniziando a testare nei posti giusti? Ad esempio, hai bisogno di posizioni con un traffico sufficiente e che abbiano un impatto sulle metriche rilevanti    agli affari.
* **Adeguata** configurazioneLa nostra attività è impostata per raggiungere il nostro obiettivo? Ad esempio, se stiamo cercando di aumentare le richieste di prestito, dovremmo rivolgerci alle persone interessate ai prestiti e misurare i clic del pulsante &quot;Invia&quot;.
* **Analisi** approfondita: L&#39;attività di test è stata eseguita al completamento? Cosa dicono i risultati? Eseguite l&#39;attività fino a raggiungere un livello di confidenza statistica compreso tra il 95% e il 99%. Documentate il motivo per cui pensate che l&#39;esperienza vincente abbia vinto e applicate l&#39;apprendimento altrove.
* **Test** iterativo: Ci stiamo basando sugli insegnamenti delle attività precedenti? Se trovate una tattica vincente, cercate di migliorarla o di apportare modifiche che vi consentano di migliorare ulteriormente la metrica di successo.

### Le opinioni possono influenzare negativamente i risultati

* Opinioni che possono avere un impatto negativo sulla vostra efficacia. Opinioni, atteggiamenti e pregiudizi della persona maggiormente pagata. Ad esempio, l’amministratore delegato desidera ridurre le dimensioni della casella di ricerca per lasciare più spazio a ciascuna pagina. È consigliabile verificare che non riduca il numero di ricerche.
* State agendo sulle opinioni? Non mi piace l&#39;aspetto del test. Al cliente non piacerà per nulla questa esperienza. Anche se l&#39;intuizione è utile, i test A/B hanno dimostrato più volte che non è sempre visibile.
* O avete una mentalità di ottimizzazione? Sono emozionato di vedere quale esperienza vince. Abbiamo abbastanza opzioni da testare?

### Le supposizioni possono anche influenzare negativamente i risultati

* Ipotesi che possono avere un impatto negativo sulla tua efficacia. La mentalità della terra (è così che lo fanno i nostri concorrenti). Per esempio, tutti i nostri concorrenti usano striscioni eroici con immagini a rotazione, quindi anche noi dovremmo.
* Presupponendo che sappiamo perché qualcosa funziona o meno. Presupponendo che non sia necessario testare qualcosa. Ad esempio, elencamo sempre le stanze in ordine di prezzo più alto-più basso come impostazione predefinita.
* State facendo dei presupposti? Non è necessario testarlo, abbiamo controllato i dati di analisi. (Sì, ma la storia può essere più complicata di quanto rivelino le analisi.)
* O avete una mentalità di ottimizzazione? Noi testiamo tutto.