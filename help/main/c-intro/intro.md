---
keywords: Target Standard;Recommendations;consigli;Target Premium;Automated Personalization;personalizzazione automatizzata;targeting automatico;auto-targeting;autorizzazioni;cos’è adobe target;
description: Scopri le nozioni di base di Adobe [!DNL Target] Standard e Adobe [!DNL Target] Premium. [!DNL Target] Premium include funzioni avanzate non disponibili nel prodotto Standard.
landing-page-description: Personalizza l’esperienza dei clienti per massimizzare le entrate tramite siti web, app mobili, social media e altri canali digitali.
short-description: Personalizza l’esperienza dei clienti per massimizzare le entrate tramite siti web, app mobili, social media e altri canali digitali.
title: Cos’è Target?
feature: Overview
exl-id: 0e729c71-618b-4ab8-93a3-d37e73ec2740
TQID: https://experienceleague.adobe.com/Mr8fwY1FNfJShSezC50YX1QeBagmuovUySsQUO8jPqo
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
    internal-label: Machine learning
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
    internal-label: Customer profiles
source-git-commit: 9a55efe5570867a822e4f6c0494a505e456bd536
workflow-type: tm+mt
source-wordcount: '1644'
ht-degree: 33%
---
# Introduzione a [!DNL Target]

[!DNL Adobe Target], parte di [!DNL Adobe Experience Cloud], offre strumenti completi per personalizzare le esperienze dei clienti su siti Web, mobili, app, social media e altri canali digitali.

[!DNL Target] consente di massimizzare i ricavi e può essere concesso in licenza come [!DNL Target Standard] o [!DNL Target Premium].

## [!UICONTROL Target Standard] {#section_ACD5EFF17AAB4E979CBEFA0145CCD905}

[!DNL Target Standard] è il front-end di [!DNL Adobe Target], che consente la creazione e la gestione visiva di test A/B e attività di targeting basate su regole. [!DNL Target] supporta l&#39;inserimento di codice personalizzato all&#39;interno e all&#39;esterno del flusso di lavoro [[!UICONTROL Compositore esperienza visivo]](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md). [!DNL Target Standard] offre una strategia di implementazione semplificata per le proprietà digitali, con una sola riga di codice in ogni pagina per gestire tutte le comunicazioni tra il sito e [!DNL Target].

Le best practice di settore sono integrate in [!DNL Target Standard], rendendolo adatto sia agli utenti nuovi che a quelli esperti. Puoi condividere facilmente dati, risultati e collaborare con i membri del gruppo utilizzando [!DNL Adobe Experience Cloud].

## [!DNL Target Premium] {#premium}

[!BADGE Premium]{type=Positive}

[!DNL Target Premium] è un&#39;offerta avanzata che richiede una licenza per aggiungere funzionalità Premium a [!DNL Target Standard]. Tutti gli articoli [!DNL Target Premium] nelle guide di [!DNL Target] includono il contrassegno [!UICONTROL Premium] nella parte superiore di ogni pagina o in linea vicino al testo interessato. È possibile fare clic sul badge [!UICONTROL Premium] e creare collegamenti a questa sezione.

**[!DNL Target Premium]include le seguenti funzionalità:**

### [!UICONTROL Personalizzazione automatizzata]

[[!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) (AP) utilizza algoritmi avanzati di apprendimento automatico per fornire esperienze personalizzate e migliorare i tassi di conversione per le interazioni digitali.

AP registra l’attività dei visitatori e crea profili per eseguire il targeting dei contenuti a visitatori simili. AP tiene traccia delle risposte ai contenuti per i singoli utenti e la popolazione, utilizzando una modellazione sofisticata per eseguire automaticamente il targeting di ogni visitatore in base a tutto ciò che sa su di lui.

AP è completamente automatizzato, apprendimento continuo con analisi umane minime. Crea modelli per determinare quali prodotti un visitatore potrebbe essere interessato, raccogliendo e memorizzando le informazioni nei profili dei visitatori. Gli algoritmi multipli garantiscono il modello migliore per il sistema.

### [!UICONTROL Targeting automatico]

[Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) utilizza l&#39;apprendimento automatico avanzato per identificare esperienze ad alte prestazioni definite dall&#39;addetto al marketing. In seguito, distribuisce a ogni visitatore l’esperienza più personalizzata in base ai profili dei singoli clienti e al comportamento dei visitatori precedenti con profili simili. [!UICONTROL Targeting automatico] consente di personalizzare il contenuto e favorire le conversioni.

### Consigli

Mediante le attività [Consigli](/help/main/c-recommendations/recommendations.md#concept_7556C8A4543942F2A77B13A29339C0C0) vengono visualizzati automaticamente prodotti o contenuti che potrebbero interessare ai clienti sulla base delle loro precedenti attività. [!UICONTROL Consigli] aiutano a indirizzare i clienti verso elementi rilevanti di cui potrebbero non essere a conoscenza.

Un consiglio determina in che modo un prodotto viene suggerito a un cliente, in base alle sue attività sul sito. Ad esempio:

* Incoraggiare chi acquista uno zaino a considerare l’acquisto di scarpe e bastoncini da trekking.

  Creare un consiglio che mostra gli elementi acquistati spesso insieme, utilizzando i criteri “Chi ha acquistato questo ha acquistato anche”.

* Aumentare il tempo di permanenza dei visitatori sul sito multimediale consigliando contenuti video simili a quelli che stanno visualizzando al momento.

  Creare un consiglio che suggerisce altri video, utilizzando i criteri “Chi ha visualizzato questo ha visualizzato anche”.

* Suggerire ai clienti che hanno visualizzato informazioni su piani di risparmio di una banca di consultare anche le informazioni sui conti IRA.

  Mostrare altri elementi acquistati dai visitatori dopo aver visualizzato un prodotto, senza mostrare il primo prodotto nei consigli, utilizzando i criterio “Chi ha visualizzato questo ha acquistato anche”.

### Consigli come offerta

[Consigli come offerta](/help/main/c-recommendations/recommendations-as-an-offer.md) consente di includere i consigli nelle attività [!UICONTROL Test A/B], [!UICONTROL Allocazione automatica], [!UICONTROL Targeting automatico] e [!UICONTROL Targeting esperienza] (XT).

Questo apre a funzionalità tutte nuove, ad esempio:

* Contenuto relativo e non relativo a consigli di test e targeting all’interno della stessa attività.
* Facile sperimentazione con il posizionamento di consigli sulla pagina, tra cui l’ordine di più consigli.
* Invio automatico di traffico all&#39;esperienza di consigli con le prestazioni migliori tramite [!UICONTROL Allocazione automatica].
* Assegnazione dinamica di visitatori a esperienze di consigli su misura in base ai singoli profili tramite [!UICONTROL Targeting automatico].

### Autorizzazioni per gli utenti Enterprise

La funzionalità [Autorizzazioni per gli utenti aziendali](/help/main/administrating-target/c-user-management/property-channel/property-channel.md#concept_E396B16FA2024ADBA27BC056138F9838) consente di creare progetti diversi (denominati “profili di prodotto” in [!DNL Adobe Admin Console for Enterprise]). [!UICONTROL Autorizzazioni per gli utenti aziendali] ti consente di assegnare a un singolo utente diverse autorizzazioni che ne determinano i diritti di accesso per ciascun progetto. Questi progetti distinti possono essere paragonati al modo in cui le suite di rapporti funzionano in [!DNL Adobe Analytics]. In ogni progetto possono essere inclusi utenti specifici con ruoli specifici applicabili a un insieme di proprietà. Il risultato è che i clienti possono limitare l’accesso alla visualizzazione, alla modifica, all’approvazione e alla pubblicazione ai propri utenti. È possibile limitare gli utenti in base all’area geografica, all’ambiente (dev/stage/prod), al canale o ad altri criteri personalizzati.

## Funzioni di Beta {#beta}

[!BADGE Beta]{type=Informative}

Il team [!DNL Adobe Target] spesso abilita nuove funzionalità per determinati clienti a scopo di test e feedback. Al termine del periodo di test, queste funzioni vengono abilitate per tutti i clienti nelle prossime versioni di [!DNL Target Standard/Premium] e annunciate nelle note sulla versione.

Gli articoli nelle guide di [!DNL Target] che descrivono le funzionalità di Beta includono il badge Beta nella parte superiore di ogni pagina o in linea vicino al testo interessato. Il badge Beta è cliccabile e include un collegamento a questa sezione.

## Recommendations Classic {#section_9554068100054D2DBDB298CBE5A0E413}

>[!IMPORTANT]
>
>[!DNL Recommendations Classic] è un prodotto legacy e non dispone più della licenza per i nuovi clienti. Per una migliore esperienza [!DNL Recommendations], effettua l’aggiornamento alle attività [!DNL Recommendations] disponibili in [!DNL Adobe Target Premium], come descritto in precedenza.

Con [!DNL Recommendations Classic] vengono visualizzati automaticamente prodotti o contenuti di potenziale interesse per i clienti sulla base della precedente attività dell&#39;utente sul sito web. Con la funzionalità Consigli è possibile indirizzare i clienti verso articoli di cui potrebbero ignorare l’esistenza, incrementando le vendite generate sul sito.

Per ulteriori informazioni, consulta la [documentazione di Recommendations Classic](/help/main/assets/adobe-recommendations-classic.pdf).

## Experience League: kit di benvenuto per Adobe [!DNL Target] {#kit}

Crea il tuo programma di ottimizzazione e personalizzazione su [!DNL Adobe Target] con questo kit di benvenuto. Il kit di benvenuto include informazioni chiave, strumenti e risorse utili per preparare e avviare la prima attività [!DNL Target]. Il kit include idee per ottenere risultati in breve tempo e strategie di ottimizzazione a lungo termine.

[Kit di benvenuto Adobe Target](/help/main/c-intro/target-welcome-kit.md)

## Video di formazione: Tipi di attività (9:03) ![Icona panoramica](/help/main/assets/overview.png)

Il seguente video spiega i tipi di attività disponibili in [!DNL Target Standard/Premium] e come raggiungere gli obiettivi del sito con il flusso di lavoro guidato in tre passaggi [!DNL Target].

* Descrizione dei tipi di attività inclusi in [!DNL Adobe Target]
* Selezionare il tipo di attività appropriato per i tuoi obiettivi
* Descrizione del flusso di lavoro guidato in tre passaggi da applicare a tutti i tipi di attività

>[!VIDEO](https://video.tv.adobe.com/v/17386)

>[!CONTEXTUALHELP]
>id="target_sample_size_ab_daily_traffic"
>title="Traffico giornaliero"
>abstract="Quanti utenti entrano ogni giorno nell’esperimento. Se non conosci il traffico giornaliero, scegli \&quot;Volume di traffico\&quot; qui sopra e il calcolatore lo risolverà utilizzando gli altri input."

>[!CONTEXTUALHELP]
>id="target_sample_size_setup"
>title="Configurare il test"
>abstract="Questi campi definiscono il test A/B, ciò che ci si aspetta di vedere e quanto è sicuro di avere nel risultato. Il campo associato a quello selezionato in precedenza verrà risolto automaticamente per. Compila il resto con i valori previsti."

>[!CONTEXTUALHELP]
>id="target_sample_size_number_experiences"
>title="Numero di esperienze"
>abstract="Numero di varianti nell’esperimento, incluso il controllo. Un test A/B ha 2 bracci. Cinque varianti più un controllo è uguale a 6. Più armi richiedono proporzionalmente più traffico per mantenere la potenza statistica."

>[!CONTEXTUALHELP]
>id="target_sample_size_duration"
>title="Durata del test A/B"
>abstract="Quanti giorni eseguirà l’esperimento. Durate più lunghe danno all’esperimento più tempo per raccogliere i dati, consentendo di rilevare in modo affidabile effetti più piccoli. Durate più brevi richiedono effetti maggiori o più traffico giornaliero per raggiungere un risultato affidabile."

>[!CONTEXTUALHELP]
>id="target_sample_size_minimum_detectable_effect"
>title="Effetto rilevabile minimo"
>abstract="Il miglioramento più piccolo che vale la pena rilevare, la modifica minima nella metrica su cui agire. Si tratta della dimensione dell&#39;incremento in punti percentuali, non della variazione percentuale relativa alla linea di base. Ad esempio, se la previsione è pari al 5% e un incremento di 1 punto percentuale è rilevante, immettere 1."

>[!CONTEXTUALHELP]
>id="target_sample_size_expected_improvement"
>title="Miglioramento previsto"
>abstract="Il miglioramento che ci si aspetta dall’esperimento."

>[!CONTEXTUALHELP]
>id="target_sample_size_variance"
>title="Varianza"
>abstract="Distribuzione dei valori della metrica, non della media. Una metrica come il click rate (per lo più 0 e 1 s) ha una varianza bassa, una metrica come il ricavo per utente (pochi spenditori elevati, molti bassi) può avere una varianza molto più elevata. In caso di dubbi, lascia il valore predefinito 1."

>[!CONTEXTUALHELP]
>id="target_sample_size_confidence_level"
>title="Livello di affidabilità"
>abstract="Quanto devi essere sicuro che un risultato non sia solo un caso casuale prima di chiamarlo reale, la soglia della significatività statistica. Un livello di affidabilità del 95% significa che c’è al massimo un 5% di possibilità di un falso positivo. Valori più alti riducono i falsi positivi ma richiedono più dati."

>[!CONTEXTUALHELP]
>id="target_sample_size_statistical_power"
>title="Potenza statistica"
>abstract="La probabilità di rilevare un effetto se uno esiste veramente, la sensibilità dell&#39;esperimento. 80% di potenza significa che c&#39;è una probabilità dell&#39;80% di rilevare un effetto reale. Una potenza più elevata riduce i falsi negativi ma richiede più traffico o un runtime più lungo."

>[!CONTEXTUALHELP]
>id="target_sample_size_traffic_mode"
>title="Modalità Traffico"
>abstract="Come gli utenti inseriscono l’esperimento. Continuo: gli utenti immettono giornalmente per tutta la durata dell’esperimento. Con l’arrivo dei risultati, il traffico si sposta automaticamente verso varianti con prestazioni migliori."

>[!CONTEXTUALHELP]
>id="target_sample_size_metric_type"
>title="Tipo di metrica"
>abstract="Che tipo di metrica stai misurando. Percentuale: utilizzalo per risultati binari come clic o conversioni, in cui ogni utente esegue o meno un’operazione. Numero: utilizzalo per metriche quali entrate o visualizzazioni di pagina, in cui il valore può variare notevolmente da utente a utente."

>[!CONTEXTUALHELP]
>id="target_sample_size_auto_daily_traffic"
>title="Traffico giornaliero"
>abstract="Quanti utenti entrano ogni giorno nell’esperimento. Utilizzato per esperimenti continui che si svolgono su più giorni, con il traffico che si sposta automaticamente verso varianti con prestazioni migliori man mano che arrivano i risultati."

>[!CONTEXTUALHELP]
>id="target_sample_size_baseline_metric_rate"
>title="Tasso metrico linea di base"
>abstract="Le prestazioni correnti prima dell’inizio dell’esperimento, la media del braccio di controllo. Sempre obbligatorio. Per le metriche percentuali, immetti come percentuale: se il 5% dei visitatori fa clic su Acquista oggi, immetti 5. Per le metriche di conteggio, inserisci il valore decimale non elaborato."

>[!CONTEXTUALHELP]
>id="target_ai_insights_primary_metric"
>title="Metrica primaria"
>abstract="La metrica principale viene estratta automaticamente dalle impostazioni di reporting. Per apportare modifiche, modifica la metrica dell’obiettivo in Obiettivi e impostazioni."

>[!CONTEXTUALHELP]
>id="target_ai_insights_hypothesis"
>title="Ipotesi"
>abstract="L’ipotesi è un’istruzione da te definita che spiega il risultato atteso dell’esperimento. Includi una descrizione di cosa viene modificato e dove, quindi specifica la metrica da modificare e come."

>[!CONTEXTUALHELP]
>id="target_ai_insights_insights"
>title="Insight"
>abstract="Gli insight sugli esperimenti sono le conoscenze individuate dall’IA quando i dati dell’esperimento hanno raggiunto la significatività statistica."

>[!CONTEXTUALHELP]
>id="target_ai_insights_opportunities"
>title="Opportunità"
>abstract="Le opportunità di esperimento sono idee di trattamento suggerite dall’intelligenza artificiale basate sui pattern che si trovano nelle schermate e nei risultati dell’esperimento."

>[!CONTEXTUALHELP]
>id="target_ai_insights_treatment_details"
>title="Dettagli trattamento"
>abstract="I dettagli del trattamento mostrano immagini di come appare un trattamento quando un utente ne è idoneo. Puoi rivedere queste immagini per tutti gli esperimenti. Alcuni esperimenti potrebbero chiederti di confermare l’immagine o sostituirla, se necessario."
