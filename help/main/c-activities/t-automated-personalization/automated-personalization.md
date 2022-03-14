---
keywords: personalizzazione automatizzata;app;tipi di pubblico;insieme;foresta casuale;slot machine;campionamento;campionamento thompson;ml;apprendimento automatico
description: Scopri come utilizzare le attività di Automated Personalization (AP) in Adobe [!DNL Target] che utilizzano l’apprendimento automatico avanzato per abbinare diverse varianti di offerta a ogni visitatore.
title: Che cos’è un’attività Automated Personalization (AP)?
feature: Automated Personalization
exl-id: 3654dce4-0d6c-42a3-8be7-e081ec478075
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '1031'
ht-degree: 89%

---

# ![PREMIUM](/help/main/assets/premium.png) Automated Personalization (AP)

[!UICONTROL Automated Personalization] (AP) attività [!DNL Adobe Target] combinare offerte o messaggi e utilizza l’apprendimento automatico avanzato per abbinare diverse varianti di offerta a ogni visitatore in base al suo profilo cliente individuale, al fine di personalizzare il contenuto e favorire l’incremento.

>[!NOTE]
>
>La [!UICONTROL personalizzazione automatizzata] è disponibile come parte della soluzione [!DNL Target Premium]. Non è disponibile in [!DNL Target Standard] senza una licenza [!DNL Target Premium]. Se si dispone di una licenza [!DNL Target Premium], la scheda di [!DNL Target Premium] sostituisce la scheda di [!DNL Target Standard] in [!DNL Adobe Experience Cloud].

Analogamente al [!UICONTROL Targeting automatico], la [!UICONTROL Personalizzazione automatizzata] utilizza un algoritmo Foresta casuale, uno dei principali metodi di raccolta di dati scientifici, come algoritmo principale di personalizzazione per determinare l’esperienza migliore da mostrare a un visitatore. La [!UICONTROL Personalizzazione automatizzata] può essere utile nella fase di individuazione dei test. È inoltre utile per consentire all&#39;apprendimento automatico di determinare il contenuto più efficace indirizzato a diversi visitatori. Nel corso del tempo, l&#39;algoritmo impara a prevedere il contenuto più efficace e visualizza il più probabile per raggiungere i tuoi obiettivi.

Per ulteriori informazioni su come [!UICONTROL Automated Personalization] differisce da [!UICONTROL Targeting automatico], vedi [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md).

Gli addetti al marketing implementano un file sul sito che permette loro di selezionare rapidamente qualsiasi contenuto e quindi creare visivamente e selezionare le opzioni di contenuto aggiuntivo per tale area, utilizzando il Compositore esperienza visivo ([!UICONTROL Visual Experience Composer, VEC]). L&#39;algoritmo determina automaticamente quale parte di contenuto distribuire a ogni singolo visitatore, sulla base di tutti i dati comportamentali di cui il sistema dispone su di esso, così da fornire un&#39;esperienza personalizzata. Poiché la [!UICONTROL Personalizzazione automatizzata] può adattarsi ai cambiamenti del comportamento del visitatore, può essere eseguita senza impostare una data di termine per produrre un incremento e una personalizzazione costanti. Tale funzione è talvolta indicata come modalità di “connessione permanente”. L’addetto al marketing non deve eseguire un test, analizzare i risultati e quindi stabilire un vincitore per un’idea dell’incremento ottenuto a partire dall’ottimizzazione, il quale è un ordine standard di operazioni per implementare il risultato di una attività A/B standard.

I seguenti termini sono utili quando si parla della [!UICONTROL Personalizzazione automatizzata]:

| Termine | Definizione |
|---|---|
| Slot machine | Un approccio slot machine per l&#39;ottimizzazione equilibra l&#39;apprendimento esplorativo e lo sfruttamento di tale apprendimento. |
| Foresta casuale | Foresta casuale è uno dei principali metodi di apprendimento automatico. Nel linguaggio della scienza dei dati, indica una classificazione di raccolta, o metodo di regressione, che funziona costruendo un gran numero di alberi decisionali basati su visitatori e attributi di visita. In Target, l’algoritmo Foresta casuale determina quale esperienza possa avere la più alta probabilità di conversione (o il più alto ricavo per visita) per ogni visitatore specifico. Per ulteriori informazioni sulla foresta casuale in Target, consulta [Algoritmo Foresta casuale](/help/main/c-activities/t-automated-personalization/algo-random-forest.md). |
| Campionamento di Thompson | L’obiettivo del campionamento di Thompson è quello di determinare quale esperienza è la migliore complessivamente (non personalizzata), minimizzando il “costo” della ricerca dell’esperienza. Il campionamento di Thompson sceglie sempre un vincitore, anche in assenza di differenza statistica tra due esperienze. Per ulteriori informazioni, consulta [Campionamento di Thompson](https://en.wikipedia.org/wiki/Thompson_sampling). |

Quando utilizzi la [!UICONTROL personalizzazione automatizzata], considera i dettagli seguenti:

La **[!UICONTROL personalizzazione automatizzata]** utilizza un algoritmo Foresta casuale da personalizzare.

Foresta casuale è uno dei principali metodi di apprendimento automatico. Nel linguaggio della scienza dei dati, indica una classificazione di raccolta, o metodo di regressione, che funziona costruendo un gran numero di alberi decisionali basati su visitatori e attributi di visita. In Target, l’algoritmo Foresta casuale determina quale esperienza possa avere la più alta probabilità di conversione (o il più alto ricavo per visita) per ogni visitatore specifico. Ad esempio, per i visitatori che utilizzano Chrome, sono membri fidelizzati e accedono al tuo sito il martedì, potrebbe essere più probabile la conversione con l’esperienza A; mentre per i visitatori provenienti da New York potrebbe essere più probabile la conversione con l’esperienza B. Per ulteriori informazioni su Foresta casuale in Target, consulta [Algoritmo Foresta casuale](/help/main/c-activities/t-automated-personalization/algo-random-forest.md).

**Il modello di personalizzazione ottimizza il processo per ogni visita.**

* L&#39;algoritmo prevede la probabilità di conversione di un visitatore (o di ricavi stimati dalla conversione) al fine di fornire l&#39;esperienza migliore.
* Un visitatore ha diritto a una nuova esperienza al termine di una sessione esistente (a meno che sia nel gruppo di controllo, nel qual caso l&#39;esperienza che il visitatore vede nella prima visita è la stessa rimane la stessa per le visite successive).
* All&#39;interno di una sessione, l&#39;esperienza presentata non cambia, in modo da mantenere la coerenza visiva.

**Il modello di personalizzazione si adatta ai cambiamenti del comportamento dei visitatori.**

* La slot machine assicura che il modello “spenda” sempre una piccola frazione di traffico per continuare ad apprendere per tutta la durata dell&#39;attività e per prevenire lo sfruttamento eccessivo delle tendenze precedentemente apprese.
* I modelli sottostanti vengono rigenerati ogni 24 ore, utilizzando i dati di comportamento dei visitatori più recenti per garantire che Target sfrutti sempre le preferenze mutevoli dei visitatori.
* Se l&#39;algoritmo non può determinare le esperienze vincenti per i singoli visitatori, mostra automaticamente l&#39;esperienza con i migliori risultati a livello generale, mentre continua a cercare vincitori personalizzati. L’esperienza che offre prestazioni migliori viene individuata tramite il [campione di Thompson](https://en.wikipedia.org/wiki/Thompson_sampling).

**Il modello esegue l’ottimizzazione continua per una singola metrica dell’obiettivo.**

* Questa metrica potrebbe essere basata sulla conversione o sui ricavi (nello specifico, [!UICONTROL ricavo per visitatore]).

**Target raccoglie automaticamente informazioni sui visitatori per generare modelli di personalizzazione.**

* Per ulteriori informazioni sugli attributi utilizzati in [!UICONTROL Targeting automatico] e [!UICONTROL Personalizzazione automatizzata], consulta [Raccolta dati di Personalizzazione automatizzata](/help/main/c-activities/t-automated-personalization/ap-data.md).

**Target utilizza automaticamente tutti i tipi di [!DNL Adobe Experience Cloud] pubblico di condivisi, per generare i modelli di personalizzazione.**

* Non è necessario eseguire alcuna operazione specifica per aggiungere i tipi di pubblico al modello. Per informazioni sull’utilizzo di [!DNL Experience Cloud Audiences] con [!DNL Target], consulta [Audience di Experience Cloud](/help/main/c-integrating-target-with-mac/mmp.md).

**Gli addetti al marketing possono caricare dati offline, punteggi di propensione o altri dati personalizzati per generare modelli di personalizzazione.**

I dati offline, ad esempio le informazioni CRM o i punteggi di propensione di abbandono dei clienti, possono essere estremamente utili nella generazione di modelli di personalizzazione. Sono disponibili diversi modi per immettere dati in algoritmi di [!UICONTROL Personalizzazione automatizzata] (AP) e [!UICONTROL Targeting automatico].

* [Parametri mbox](/help/main/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md#concept_0069C0EFB56C4700BB33F2F35C2B9B17)
* [Parametri del profilo](/help/main/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md#concept_0069C0EFB56C4700BB33F2F35C2B9B17)
* [API lato server per lʼaggiornamento del profilo](/help/main/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md#concept_0069C0EFB56C4700BB33F2F35C2B9B17)

Per informazioni sui dati raccolti e utilizzati automaticamente dagli algoritmi di [!UICONTROL personalizzazione automatizzata] e [!UICONTROL targeting automatico], consulta [Raccolta dati di Personalizzazione automatizzata](/help/main/c-activities/t-automated-personalization/ap-data.md).

## ![Badge panoramica](/help/main/assets/overview.png) Video di formazione: Tipi di attività

Questo video spiega i tipi di attività disponibili in [!DNL Target Standard/Premium]. La [!UICONTROL personalizzazione automatizzata] è discussa a partire dal minuto 5:55.

* Descrizione dei tipi di attività inclusi in [!DNL Adobe Target]
* Selezionare il tipo di attività appropriato per i tuoi obiettivi
* Descrizione del flusso di lavoro guidato in tre passaggi da applicare a tutti i tipi di attività

>[!VIDEO](https://video.tv.adobe.com/v/17386)
