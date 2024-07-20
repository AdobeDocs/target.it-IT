---
keywords: personalizzazione automatizzata;ap;pubblico;insieme;foresta casuale;slot multi-armed;thompson sampling;ml;machine learning
description: Scopri come utilizzare le attività [!UICONTROL Automated Personalization] (AP) in [!DNL Adobe Target] che utilizzano l'apprendimento automatico avanzato per abbinare diverse varianti di offerta a ogni visitatore.
title: Che cos'è un'attività [!UICONTROL Automated Personalization] (AP)?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."
feature: Automated Personalization
exl-id: 3654dce4-0d6c-42a3-8be7-e081ec478075
source-git-commit: d5b24f298ae405d57c2ba639082cbe99c4e358fd
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 28%

---

# [!UICONTROL Automated Personalization] (AP)

Le attività di [!UICONTROL Automated Personalization] (AP) in [!DNL Adobe Target] combinano offerte o messaggi e utilizzano l&#39;apprendimento automatico avanzato per abbinare diverse varianti di offerta a ogni visitatore in base al suo profilo cliente per personalizzare il contenuto e favorire l&#39;incremento.

>[!NOTE]
>
>[!UICONTROL Automated Personalization] è disponibile nella soluzione [!DNL Target Premium]. Questa funzione non è disponibile in [!DNL Target Standard] senza una licenza [!DNL Target Premium]. Per ulteriori informazioni sulle funzioni avanzate fornite da questa licenza, consulta [Target Premium](/help/main/c-intro/intro.md#premium).

Analogamente a [!UICONTROL Auto-Target], [!UICONTROL Automated Personalization] utilizza un [algoritmo Foresta casuale](/help/main/c-activities/t-automated-personalization/algo-random-forest.md), uno dei principali metodi di raccolta di dati scientifici, come algoritmo principale di personalizzazione per determinare l&#39;esperienza migliore da mostrare a un visitatore. [!UICONTROL Automated Personalization] può essere utile nella fase di individuazione dei test. È inoltre utile per consentire all&#39;apprendimento automatico di determinare il contenuto più efficace indirizzato a diversi visitatori. Nel corso del tempo, l&#39;algoritmo impara a prevedere il contenuto più efficace e visualizza il più probabile per raggiungere i tuoi obiettivi.

Per ulteriori informazioni sulle differenze tra [!UICONTROL Automated Personalization] e [!UICONTROL Auto-Target], vedere [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB).

Gli addetti al marketing implementano un file sul sito che consente loro di selezionare qualsiasi contenuto e quindi creare visivamente e selezionare opzioni di contenuto aggiuntive per tale area utilizzando il Compositore esperienza visivo [!UICONTROL Visual Experience Composer]. L&#39;algoritmo determina automaticamente quale parte di contenuto distribuire a ogni singolo visitatore, sulla base di tutti i dati comportamentali di cui il sistema dispone su di esso, così da fornire un&#39;esperienza personalizzata. Poiché [!UICONTROL Automated Personalization] può adattarsi ai cambiamenti nel comportamento del visitatore, può essere eseguito senza impostare una data di fine per fornire un incremento e una personalizzazione costanti. Questa modalità è talvolta indicata come &quot;sempre attiva&quot;. L’addetto al marketing non deve eseguire un test, analizzare i risultati e quindi stabilire un vincitore per un’idea dell’incremento ottenuto a partire dall’ottimizzazione, il quale è un ordine standard di operazioni per implementare il risultato di una attività A/B standard.

I seguenti termini sono utili quando si parla di [!UICONTROL Automated Personalization]:

| Termine | Definizione |
|---|---|
| Slot machine | Un approccio slot machine per l&#39;ottimizzazione equilibra l&#39;apprendimento esplorativo e lo sfruttamento di tale apprendimento. |
| Foresta casuale | Un approccio leader di apprendimento automatico. In termini di scienza dei dati, si tratta di una classificazione di insieme o di un metodo di regressione che funziona costruendo molti alberi decisionali in base agli attributi del visitatore e della visita. |
| Campionamento di Thompson | L’obiettivo del campionamento di Thompson è determinare quale esperienza è la migliore complessivamente (non personalizzata), riducendo al minimo il &quot;costo&quot; della ricerca di tale esperienza. Il campionamento di Thompson sceglie sempre un vincitore, anche in assenza di differenza statistica tra due esperienze. Per ulteriori informazioni, consulta [Campionamento di Thompson](https://en.wikipedia.org/wiki/Thompson_sampling). |

Considerare i dettagli seguenti quando si utilizza [!UICONTROL Automated Personalization]:

## [!UICONTROL Automated Personalization] utilizza un algoritmo Foresta casuale per personalizzare

Foresta casuale è uno dei principali metodi di apprendimento automatico. In termini di scienza dei dati, si tratta di una classificazione di insieme o di un metodo di regressione che funziona costruendo molti alberi decisionali in base agli attributi del visitatore e della visita. In [!DNL Target], Foresta casuale viene utilizzato per determinare quale esperienza dovrebbe avere la più alta probabilità di conversione (o il più alto ricavo per visita) per ogni visitatore specifico. Ad esempio, per i visitatori che utilizzano Chrome e sono membri fidelizzati e accedono al tuo sito il martedì, potrebbe essere più probabile la conversione con l’esperienza A. Per i visitatori provenienti da New York potrebbe essere più probabile la conversione con l’esperienza B. Per ulteriori informazioni sulla foresta casuale in [!DNL Target], vedere [Algoritmo foresta casuale](/help/main/c-activities/t-automated-personalization/algo-random-forest.md).

## Il modello di personalizzazione ottimizza per ogni visita

* L&#39;algoritmo prevede la probabilità di conversione di un visitatore (o i ricavi stimati dalla conversione) per fornire l&#39;esperienza migliore.
* Un visitatore è idoneo per una nuova esperienza al termine di una sessione esistente, a meno che non si trovi nel gruppo di controllo. Se il visitatore fa parte del gruppo di controllo, l’esperienza che vede alla prima visita è la stessa delle visite successive.
* L’esperienza presentata non cambia all’interno di una sessione per mantenere la coerenza visiva.

## Il modello di personalizzazione si adatta ai cambiamenti nel comportamento del visitatore

* La slot machine assicura che il modello &quot;spenda&quot; sempre una piccola frazione di traffico per continuare a imparare per tutta la durata dell&#39;attività e per prevenire lo sfruttamento eccessivo delle tendenze apprese in precedenza.
* I modelli sottostanti vengono ricreati ogni 24 ore utilizzando i dati di comportamento del visitatore più recenti per garantire che [!DNL Target] utilizzi sempre le preferenze del visitatore in modifica.
* Se l&#39;algoritmo non può determinare le esperienze vincenti per i singoli visitatori, mostra automaticamente l&#39;esperienza con i migliori risultati a livello generale, mentre continua a cercare vincitori personalizzati. L’esperienza che offre prestazioni migliori viene individuata tramite il [campione di Thompson](https://en.wikipedia.org/wiki/Thompson_sampling).

## Il modello ottimizza continuamente una singola metrica di obiettivo

* Questa metrica potrebbe essere basata sulla conversione o sui ricavi (nello specifico, [!UICONTROL Revenue per Visitor]).

## [!DNL Target] raccoglie automaticamente informazioni sui visitatori per generare i modelli di personalizzazione

* Per ulteriori informazioni sugli attributi utilizzati in [!UICONTROL Auto-Target] e [!UICONTROL Automated Personalization], vedere [Raccolta dati di Automated Personalization](/help/main/c-activities/t-automated-personalization/ap-data.md).

## [!DNL Target] utilizza automaticamente tutti i [!DNL Adobe Experience Cloud] tipi di pubblico condivisi per generare i modelli di personalizzazione

* Non è necessario eseguire alcuna operazione specifica per aggiungere tipi di pubblico al modello. Per informazioni sull’utilizzo di [!DNL Experience Cloud Audiences] con [!DNL Target], consulta [Audience di Experience Cloud](/help/main/c-integrating-target-with-mac/mmp.md).

## Gli addetti al marketing possono caricare dati offline, punteggi di propensione o altri dati personalizzati per creare modelli di personalizzazione

I dati offline, come le informazioni CRM o i punteggi di propensione in base alla customer churn, possono essere estremamente utili nella creazione di modelli di personalizzazione. Esistono diversi modi per immettere dati in algoritmi di personalizzazione [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Auto-Target].

* [parametri mbox](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=it){target=_blank}
* [Parametri profilo](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=it){target=_blank}
* [API lato server per l&#39;aggiornamento del profilo](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=it){target=_blank}

Per informazioni sui dati raccolti e utilizzati automaticamente dagli algoritmi di personalizzazione [!UICONTROL Automated Personalization] e [!UICONTROL Auto-Target], vedere [Raccolta dati di Automated Personalization](/help/main/c-activities/t-automated-personalization/ap-data.md).

## Video di formazione: Tipi di attività

Questo video spiega i tipi di attività disponibili in [!DNL Target]. [!UICONTROL Automated Personalization] è discusso a partire dalle 5:55.

* Descrizione dei tipi di attività inclusi in [!DNL Adobe Target]
* Selezionare il tipo di attività appropriato per i tuoi obiettivi
* Descrizione del flusso di lavoro guidato in tre passaggi da applicare a tutti i tipi di attività

>[!VIDEO](https://video.tv.adobe.com/v/17386)
