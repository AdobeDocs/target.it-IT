---
keywords: personalizzazione automatizzata;ap;pubblico;insieme;foresta casuale;slot multi-armed;thompson sampling;ml;machine learning
description: Scopri come utilizzare le attività di [!UICONTROL Automated Personalization] (AP) in [!DNL Adobe Target] che utilizzano l'apprendimento automatico avanzato per abbinare diverse varianti di offerta a ogni visitatore.
title: Cos'è un'attività [!UICONTROL Automated Personalization] (AP)?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Automated Personalization
exl-id: 3654dce4-0d6c-42a3-8be7-e081ec478075
TQID: 'https://experienceleague.adobe.com/BBtKgNRTlqNFFoAjr1LQkhHyZeAlXG2h8D7bsndh4kQ'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: fff07a91-d479-45f4-ae95-9762e79b1b7c
    internal-label: Shared audiences
  - id: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
    internal-label: Automated personalization
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c4147b6e-073b-4d3c-9ab1-d60f2f4434ef
    internal-label: Behavioral data
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
    internal-label: Machine learning
source-git-commit: ddd4fa83540294ee229b87f041bc2245ba9a3464
workflow-type: tm+mt
source-wordcount: '906'
ht-degree: 15%
---
# [!UICONTROL Automated Personalization] (AP) {#automated-personalization-overview}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri in che modo un&#39;attività di **[!UICONTROL Automated Personalization]** associa le varianti di offerta a ogni visitatore e cosa considerare quando la utilizzi.

>[!ENDSHADEBOX]

>[!NOTE]
>
>**[!UICONTROL Automated Personalization]** è disponibile nella soluzione [!DNL Target Premium]. Questa funzione non è disponibile in [!DNL Target Standard] senza una licenza [!DNL Target Premium]. Per ulteriori informazioni sulle funzioni avanzate fornite da questa licenza, consulta [Target Premium](/help/main/c-intro/intro.md#premium).

Le attività di **[!UICONTROL Automated Personalization]** (AP) in [!DNL Adobe Target] combinano offerte o messaggi e utilizzano l&#39;apprendimento automatico avanzato per abbinare diverse varianti di offerta a ogni visitatore in base al suo profilo cliente, per personalizzare il contenuto e favorire l&#39;incremento.

Gli addetti al marketing implementano un file sul sito che consente loro di selezionare qualsiasi contenuto e quindi creare visivamente opzioni di contenuto aggiuntive per tale area utilizzando il **[!UICONTROL Compositore esperienza visivo]**. L’algoritmo determina quindi automaticamente quale contenuto distribuire a ogni visitatore, in base a tutti i dati comportamentali di cui il sistema dispone su quel visitatore.

**[!UICONTROL Automated Personalization]** si adatta ai cambiamenti nel comportamento del visitatore, quindi può essere eseguito senza impostare una data di fine per fornire un incremento e una personalizzazione costanti. Questa modalità è talvolta indicata come &quot;sempre attiva&quot;. L’addetto al marketing non deve eseguire un test, analizzare i risultati e quindi fornire un vincitore prima di realizzare l’incremento. **[!UICONTROL Automated Personalization]** è utile anche nella fase di individuazione dei test e quando esegui il targeting di visitatori diversi. Per ulteriori informazioni sulle differenze rispetto a **[!UICONTROL Targeting automatico]**, vedere [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB).

I seguenti termini sono utili quando si parla di **[!UICONTROL Automated Personalization]**:

| Termine | Definizione |
|---|---|
| Slot machine | Un approccio slot machine per l&#39;ottimizzazione equilibra l&#39;apprendimento esplorativo e lo sfruttamento di tale apprendimento. |
| Foresta casuale | Un approccio leader di apprendimento automatico. In termini di scienza dei dati, si tratta di una classificazione di insieme o di un metodo di regressione che funziona costruendo molti alberi decisionali in base agli attributi del visitatore e della visita. |
| Campionamento di Thompson | L’obiettivo del campionamento di Thompson è determinare quale esperienza è la migliore complessivamente (non personalizzata), riducendo al minimo il &quot;costo&quot; della ricerca di tale esperienza. Il campionamento di Thompson sceglie sempre un vincitore, anche se non c’è differenza statistica tra due esperienze. Per ulteriori informazioni, consulta [Campionamento di Thompson](https://en.wikipedia.org/wiki/Thompson_sampling). |

## Funzionamento del modello di personalizzazione {#how-ap-works}

**[!UICONTROL Automated Personalization]** utilizza un algoritmo Foresta casuale da personalizzare. Foresta casuale è uno dei principali metodi di apprendimento automatico. In termini di scienza dei dati, si tratta di una classificazione di insieme o di un metodo di regressione che funziona costruendo molti alberi decisionali in base agli attributi del visitatore e della visita. In [!DNL Target], Foresta casuale viene utilizzato per determinare quale esperienza dovrebbe avere la più alta probabilità di conversione (o il più alto ricavo per visita) per ogni visitatore specifico.

Ad esempio, per i visitatori che utilizzano Chrome e sono membri fidelizzati e accedono al tuo sito il martedì, potrebbe essere più probabile la conversione con l’esperienza A. Per i visitatori provenienti da New York potrebbe essere più probabile la conversione con l’esperienza B.

Per ulteriori informazioni sulla foresta casuale in [!DNL Target], vedere [Algoritmo foresta casuale](/help/main/c-activities/t-automated-personalization/algo-random-forest.md).

| Formato | Come funziona |
|---|---|
| **Ottimizzazione per ogni visita** | L’algoritmo prevede la probabilità che un visitatore converta (o i ricavi stimati dalla conversione) per fornire l’esperienza migliore. Un visitatore è idoneo per una nuova esperienza al termine di una sessione esistente, a meno che non si trovi nel gruppo di controllo. Un visitatore nel gruppo di controllo visualizza la stessa esperienza della prima visita. L’esperienza non cambia all’interno di una sessione, per mantenere la coerenza visiva. |
| **Adattamento ai cambiamenti nel comportamento del visitatore** | La slot machine spende sempre una piccola frazione di traffico per continuare a imparare per tutta la vita dell&#39;attività e per prevenire lo sfruttamento eccessivo delle tendenze apprese in precedenza. I modelli sottostanti vengono ricreati ogni 24 ore utilizzando i dati di comportamento dei visitatori più recenti. Se l&#39;algoritmo non è in grado di determinare le esperienze vincenti per i singoli visitatori, mostra l&#39;esperienza complessiva con le prestazioni migliori, trovata utilizzando il [Campionamento di Thompson](https://en.wikipedia.org/wiki/Thompson_sampling), mentre continua a cercare vincitori personalizzati. |
| **Metrica per obiettivo** | Il modello ottimizza continuamente una singola metrica dell&#39;obiettivo, che può essere basata sulla conversione o sui ricavi (nello specifico, **[!UICONTROL Ricavo per visita]**). |
| **Dati e pubblico** | [!DNL Target] raccoglie automaticamente informazioni sui visitatori per generare i modelli di personalizzazione. Per ulteriori informazioni sugli attributi utilizzati in **[!UICONTROL Targeting automatico]** e **[!UICONTROL Automated Personalization]**, vedi [Raccolta dati di Automated Personalization](/help/main/c-activities/t-automated-personalization/ap-data.md). [!DNL Target] utilizza inoltre automaticamente tutti i [!DNL Adobe Experience Cloud] tipi di pubblico condivisi, pertanto non è necessario eseguire alcuna operazione specifica per aggiungere tipi di pubblico al modello. Per ulteriori informazioni, consulta [Tipi di pubblico di Experience Cloud](/help/main/c-integrating-target-with-mac/mmp.md). |
| **Dati personalizzati** | Gli addetti al marketing possono caricare dati offline, ad esempio informazioni CRM o punteggi di propensione in base alla customer churn, oppure altri dati personalizzati per creare modelli di personalizzazione. I dati possono essere immessi con [parametri mbox](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=it){target=_blank}, [parametri profilo](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=it){target=_blank} o [API lato server per l&#39;aggiornamento profilo](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=it){target=_blank}. |

## Video di formazione: Tipi di attività {#training-video}

Questo video spiega i tipi di attività disponibili in [!DNL Target]. **[!UICONTROL Automated Personalization]** è discusso a partire dal minuto 5:55.

* Descrizione dei tipi di attività inclusi in [!DNL Adobe Target]
* Selezionare il tipo di attività appropriato per i tuoi obiettivi
* Descrizione del flusso di lavoro guidato in tre passaggi da applicare a tutti i tipi di attività

>[!VIDEO](https://video.tv.adobe.com/v/36365?captions=ita)
