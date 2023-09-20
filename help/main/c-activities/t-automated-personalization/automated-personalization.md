---
keywords: personalizzazione automatizzata;ap;pubblico;insieme;foresta casuale;slot multi-armed;thompson sampling;ml;machine learning
description: Scopri come utilizzare [!UICONTROL Automated Personalization] Attività di (AP) in [!DNL Adobe Target] che utilizzano l’apprendimento automatico avanzato per abbinare diverse varianti di offerta a ogni visitatore.
title: Che cos’è un’ [!UICONTROL Automated Personalization] Attività (AP)?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."
feature: Automated Personalization
exl-id: 3654dce4-0d6c-42a3-8be7-e081ec478075
source-git-commit: d5b24f298ae405d57c2ba639082cbe99c4e358fd
workflow-type: tm+mt
source-wordcount: '1010'
ht-degree: 46%

---

# [!UICONTROL Automated Personalization] (AP)

[!UICONTROL Automated Personalization] Attività di (AP) in [!DNL Adobe Target] combina offerte o messaggi e utilizza l’apprendimento automatico avanzato per abbinare diverse varianti di offerta a ogni visitatore in base al suo profilo cliente, per personalizzare il contenuto e favorire l’incremento.

>[!NOTE]
>
>La [!UICONTROL personalizzazione automatizzata] è disponibile come parte della soluzione [!DNL Target Premium]. Questa funzione non è disponibile in [!DNL Target Standard] senza una licenza [!DNL Target Premium]. Per ulteriori informazioni sulle funzioni avanzate fornite da questa licenza, consulta [Target Premium](/help/main/c-intro/intro.md#premium).

Simile a [!UICONTROL Targeting automatico], [!UICONTROL Automated Personalization] utilizza un [Algoritmo Foresta casuale](/help/main/c-activities/t-automated-personalization/algo-random-forest.md), uno dei principali metodi di raccolta di dati scientifici, come algoritmo principale di personalizzazione per determinare l’esperienza migliore da mostrare a un visitatore. La [!UICONTROL Personalizzazione automatizzata] può essere utile nella fase di individuazione dei test. È inoltre utile per consentire all&#39;apprendimento automatico di determinare il contenuto più efficace indirizzato a diversi visitatori. Nel corso del tempo, l&#39;algoritmo impara a prevedere il contenuto più efficace e visualizza il più probabile per raggiungere i tuoi obiettivi.

Per ulteriori informazioni su come [!UICONTROL Automated Personalization] differisce da [!UICONTROL Targeting automatico], vedi [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB).

Gli addetti al marketing implementano un file sul sito che consente loro di selezionare qualsiasi contenuto e quindi creare visivamente e selezionare opzioni di contenuto aggiuntive per tale area utilizzando [!UICONTROL Compositore esperienza visivo] (VEC). L&#39;algoritmo determina automaticamente quale parte di contenuto distribuire a ogni singolo visitatore, sulla base di tutti i dati comportamentali di cui il sistema dispone su di esso, così da fornire un&#39;esperienza personalizzata. Poiché la [!UICONTROL Personalizzazione automatizzata] può adattarsi ai cambiamenti del comportamento del visitatore, può essere eseguita senza impostare una data di termine per produrre un incremento e una personalizzazione costanti. Questa modalità è talvolta indicata come &quot;sempre attiva&quot;. L’addetto al marketing non deve eseguire un test, analizzare i risultati e quindi stabilire un vincitore per un’idea dell’incremento ottenuto a partire dall’ottimizzazione, il quale è un ordine standard di operazioni per implementare il risultato di una attività A/B standard.

I seguenti termini sono utili quando si parla della [!UICONTROL Personalizzazione automatizzata]:

| Termine | Definizione |
|---|---|
| Slot machine | Un approccio slot machine per l&#39;ottimizzazione equilibra l&#39;apprendimento esplorativo e lo sfruttamento di tale apprendimento. |
| Foresta casuale | Un approccio leader di apprendimento automatico. In termini di scienza dei dati, si tratta di una classificazione di insieme o di un metodo di regressione che funziona costruendo molti alberi decisionali in base agli attributi del visitatore e della visita. |
| Campionamento di Thompson | L’obiettivo del campionamento di Thompson è determinare quale esperienza è la migliore complessivamente (non personalizzata), riducendo al minimo il &quot;costo&quot; della ricerca di tale esperienza. Il campionamento di Thompson sceglie sempre un vincitore, anche in assenza di differenza statistica tra due esperienze. Per ulteriori informazioni, consulta [Campionamento di Thompson](https://en.wikipedia.org/wiki/Thompson_sampling). |

Quando utilizzi la [!UICONTROL personalizzazione automatizzata], considera i dettagli seguenti:

## La [!UICONTROL personalizzazione automatizzata] utilizza un algoritmo Foresta casuale da personalizzare

Foresta casuale è uno dei principali metodi di apprendimento automatico. In termini di scienza dei dati, si tratta di una classificazione di insieme o di un metodo di regressione che funziona costruendo molti alberi decisionali in base agli attributi del visitatore e della visita. Entro [!DNL Target], Foresta casuale viene utilizzato per determinare quale esperienza dovrebbe avere la più alta probabilità di conversione (o il più alto ricavo per visita) per ogni visitatore specifico. Ad esempio, per i visitatori che utilizzano Chrome, sono membri fidelizzati e accedono al tuo sito il martedì, potrebbe essere più probabile la conversione con l’esperienza A. Per i visitatori provenienti da New York potrebbe essere più probabile la conversione con l’esperienza B. Per ulteriori informazioni su Foresta casuale in [!DNL Target], vedi [Algoritmo Foresta casuale](/help/main/c-activities/t-automated-personalization/algo-random-forest.md).

## Il modello di personalizzazione ottimizza il processo per ogni visita

* L&#39;algoritmo prevede la probabilità di conversione di un visitatore (o i ricavi stimati dalla conversione) per fornire l&#39;esperienza migliore.
* Un visitatore è idoneo per una nuova esperienza al termine di una sessione esistente, a meno che non si trovi nel gruppo di controllo. Se il visitatore fa parte del gruppo di controllo, l’esperienza che vede alla prima visita è la stessa delle visite successive.
* L’esperienza presentata non cambia all’interno di una sessione per mantenere la coerenza visiva.

## Il modello di personalizzazione si adatta ai cambiamenti del comportamento dei visitatori

* La slot machine assicura che il modello &quot;spenda&quot; sempre una piccola frazione di traffico per continuare a imparare per tutta la durata dell&#39;attività e per prevenire lo sfruttamento eccessivo delle tendenze apprese in precedenza.
* I modelli sottostanti vengono ricreati ogni 24 ore utilizzando i dati di comportamento dei visitatori più recenti per garantire che [!DNL Target] utilizza sempre la modifica delle preferenze del visitatore.
* Se l&#39;algoritmo non può determinare le esperienze vincenti per i singoli visitatori, mostra automaticamente l&#39;esperienza con i migliori risultati a livello generale, mentre continua a cercare vincitori personalizzati. L’esperienza che offre prestazioni migliori viene individuata tramite il [campione di Thompson](https://en.wikipedia.org/wiki/Thompson_sampling).

## Il modello esegue l’ottimizzazione continua per una singola metrica dell’obiettivo

* Questa metrica potrebbe essere basata sulla conversione o sui ricavi (nello specifico, [!UICONTROL ricavo per visitatore]).

## [!DNL Target] raccoglie automaticamente informazioni sui visitatori per generare modelli di personalizzazione

* Per ulteriori informazioni sugli attributi utilizzati in [!UICONTROL Targeting automatico] e [!UICONTROL Personalizzazione automatizzata], consulta [Raccolta dati di Personalizzazione automatizzata](/help/main/c-activities/t-automated-personalization/ap-data.md).

## [!DNL Target] utilizza automaticamente tutti i tipi di [!DNL Adobe Experience Cloud] pubblico di condivisi, per generare i modelli di personalizzazione

* Non è necessario eseguire alcuna operazione specifica per aggiungere tipi di pubblico al modello. Per informazioni sull’utilizzo di [!DNL Experience Cloud Audiences] con [!DNL Target], consulta [Audience di Experience Cloud](/help/main/c-integrating-target-with-mac/mmp.md).

## Gli addetti al marketing possono caricare dati offline, punteggi di propensione o altri dati personalizzati per creare modelli di personalizzazione

I dati offline, come le informazioni CRM o i punteggi di propensione in base alla customer churn, possono essere estremamente utili nella creazione di modelli di personalizzazione. Sono disponibili diversi modi per immettere dati in algoritmi di [!UICONTROL Personalizzazione automatizzata] (AP) e [!UICONTROL Targeting automatico].

* [Parametri mbox](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html){target=_blank}
* [Parametri del profilo](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html){target=_blank}
* [API lato server per lʼaggiornamento del profilo](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html){target=_blank}

Per informazioni sui dati raccolti e utilizzati automaticamente dagli algoritmi di [!UICONTROL personalizzazione automatizzata] e [!UICONTROL targeting automatico], consulta [Raccolta dati di Personalizzazione automatizzata](/help/main/c-activities/t-automated-personalization/ap-data.md).

## Video di formazione: Tipi di attività

Questo video spiega i tipi di attività disponibili in [!DNL Target]. La [!UICONTROL personalizzazione automatizzata] è discussa a partire dal minuto 5:55.

* Descrizione dei tipi di attività inclusi in [!DNL Adobe Target]
* Selezionare il tipo di attività appropriato per i tuoi obiettivi
* Descrizione del flusso di lavoro guidato in tre passaggi da applicare a tutti i tipi di attività

>[!VIDEO](https://video.tv.adobe.com/v/17386)
