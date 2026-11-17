---
keywords: foresta casuale;albero decisionale;ap;Automated Personalization
description: Scopri come [!DNL Adobe Target] utilizza l'algoritmo Foresta casuale nelle attività [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Targeting automatico].
title: In che modo [!DNL Target] utilizza l'algoritmo Foresta casuale?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Automated Personalization
exl-id: 07a89525-4071-4434-ac96-c59a4f4422ad
TQID: 'https://experienceleague.adobe.com/Ui8E8CkiiJSdqim9fzIgPDdsKG1MMtuu3EUuAqgmm0M'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
    internal-label: Automated personalization
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: ddd4fa83540294ee229b87f041bc2245ba9a3464
workflow-type: tm+mt
source-wordcount: '1313'
ht-degree: 7%
---
# Algoritmo Foresta casuale {#random-forest-algorithm}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come [!DNL Target] utilizza l&#39;algoritmo Foresta casuale per generare i modelli di personalizzazione delle attività **[!UICONTROL Automated Personalization]** e **[!UICONTROL Targeting automatico]**.

>[!ENDSHADEBOX]

L&#39;algoritmo di personalizzazione principale utilizzato nelle attività **[!UICONTROL Automated Personalization]** (AP) e **[!UICONTROL Targeting automatico]** è Foresta casuale. Si tratta di un metodo di classificazione o regressione che opera costruendo una moltitudine di alberi decisionali durante la formazione.

Foresta casuale è un metodo di insieme. Quando si pensa alle statistiche, si potrebbe pensare a un unico modello di regressione utilizzato per prevedere un risultato. Le ricerche più recenti sulla scienza dei dati suggeriscono che i &quot;metodi di raccolta&quot;, in cui più modelli vengono creati dallo stesso set di dati e poi combinati in modo intelligente, producono risultati migliori rispetto alla previsione basata su un singolo modello da solo, o che potrebbero essere ottenuti da qualsiasi algoritmo di apprendimento costitutivo.

## Che cos&#39;è un albero decisionale? {#section_7F5865D8064447F4856FED426243FDAC}

Un albero decisionale suddivide in gruppi tutti i dati sulle visite da cui un sistema può imparare. Le visite all’interno di ciascun gruppo sono il più possibile simili tra loro per quanto riguarda la metrica di obiettivo (ad esempio, il tasso di conversione) e le visite tra gruppi sono le più diverse possibili. A questo scopo, l’albero esamina le variabili nel set di apprendimento e divide i dati in modo reciprocamente esclusivo ed esaustivo collettivamente (MECE) in gruppi (o &quot;foglie&quot;) che massimizzano questo obiettivo.

Nel seguente semplice esempio, la metrica di obiettivo è la conversione e sono disponibili due variabili di input:

* Genere (con due valori potenziali, Maschio o Femmina)
* Codice postale (con cinque valori potenziali nel set di dati ridotto: 11111, 22222, 33333, 44444 o 55555)

### Prima suddivisione {#first-split}

La struttura determina innanzitutto quale delle due variabili spiega la maggiore variazione nel tasso di conversione dei dati della visita. Supponiamo che il codice postale sia più predittivo. Questa variabile forma il primo &quot;ramo&quot; dell&#39;albero. La struttura suddivide quindi i dati della visita in gruppi, come descritto in precedenza. Supponiamo che 11111, 22222 e 33333 siano una divisione e 44444 e 55555 una seconda divisione.

![Primo livello dell&#39;albero delle decisioni](assets/decsion_tree_1.png){width="440" align="center"}

### Dividi all&#39;interno di ogni ramo {#second-split}

L&#39;albero pone la domanda: &quot;Qual è la variabile più predittiva?&quot; e completa un esercizio simile per dividere i dati *all&#39;interno di ogni ramo*. Solo il genere rimane, quindi è la risposta qui. Nel 11111, 22222, e 33333 ramo, presumono che ci sia una differenza nella conversione tra uomini e donne. Ci sono poi due foglie (uomini e donne), e questo ramo è completo. Nel ramo 44444 e 55555, supponiamo che non ci sia differenza statistica tra le conversioni di donne e uomini. In questo caso, la prima suddivisione è quella finale.

![Completare l&#39;albero delle decisioni](assets/decsion_tree_2.png){width="480" align="center"}

## Come vengono utilizzati gli alberi decisionali da Foresta casuale? {#section_536C105EF9F540C096D60450CAC6F627}

Gli alberi decisionali possono essere un potente strumento statistico. Tuttavia, hanno alcuni svantaggi. La cosa più importante è che possono &quot;adattare eccessivamente&quot; i dati, in modo che un singolo albero predice male i dati futuri che non sono stati utilizzati per costruire l&#39;albero iniziale. Questa sfida è conosciuta come il [compromesso bias-variance](https://en.wikipedia.org/wiki/Bias%E2%80%93variance_tradeoff) nell&#39;apprendimento statistico.

Le foreste casuali aiutano a superare questa sfida. Una foresta casuale è una raccolta di centinaia di alberi decisionali che sono costruiti in modo leggermente diverso sullo stesso insieme di dati e che &quot;votano&quot; insieme per produrre un modello migliore di un singolo albero. Gli alberi vengono costruiti selezionando in modo casuale un sottoinsieme di record di visita con la sostituzione (nota come insaccamento) e selezionando in modo casuale un sottoinsieme di attributi, in modo che la foresta sia costituita da alberi decisionali leggermente diversi. Questo metodo introduce piccole variazioni negli alberi. L&#39;aggiunta di questa quantità di varianza controllata consente di migliorare la precisione predittiva dell&#39;algoritmo.

## In che modo gli algoritmi di personalizzazione [!DNL Target] utilizzano Foresta casuale? {#section_32FB53CAD8DF40FB9C0F1217FBDBB691}

### Come vengono generati i modelli

[!DNL Target] utilizza i dati raccolti automaticamente e i dati personalizzati forniti dall&#39;utente per creare gli algoritmi di personalizzazione. Il diagramma seguente riepiloga il modo in cui i modelli vengono generati per le attività **[!UICONTROL Targeting automatico]** e **[!UICONTROL Automated Personalization]**:

![Flusso che riepiloga la modalità di generazione dei modelli Foresta casuale](assets/random_forest_flow.png){width="850" zoomable="yes"}

1. [!DNL Target] raccoglie dati sui visitatori mentre distribuisce esperienze o offerte in modo casuale.
1. Dopo che [!DNL Target] ha raggiunto una massa critica di dati, [!DNL Target] esegue la progettazione delle funzionalità.
1. [!DNL Target] genera modelli Foresta casuale per ogni esperienza o offerta.
1. [!DNL Target] convalida il modello verificando che soddisfi un punteggio di qualità di soglia.
1. [!DNL Target] invia il modello in produzione per personalizzare il traffico futuro.

Questi modelli prevedono la migliore esperienza o offerta da mostrare ai visitatori. In genere, un modello viene generato per esperienza (in un&#39;attività **[!UICONTROL Targeting automatico]**) o per offerta (in un&#39;attività **[!UICONTROL Automated Personalization]**). [!DNL Target] visualizza quindi l&#39;esperienza o l&#39;offerta che produce la metrica di successo più alta prevista (ad esempio, il tasso di conversione). I modelli devono essere addestrati su visite fornite in modo casuale prima di poter essere utilizzati per la previsione. Di conseguenza, anche i visitatori che fanno parte del gruppo personalizzato vengono mostrati in modo casuale in diverse esperienze o offerte all’inizio di un’attività, fino a quando gli algoritmi di personalizzazione non sono pronti.

I modelli vengono convalidati in base alla rispettiva area sotto la curva (AUC), per garantire che ogni modello sia in grado di prevedere il comportamento dei visitatori prima che venga utilizzato nell’attività. L’ora esatta in cui un modello inizia a fornire esperienze personalizzate dipende dai dettagli dei dati, in quanto il modello deve essere convalidato per primo. In pratica, per scopi di pianificazione del traffico, di solito richiede più del numero minimo di conversioni prima che ogni modello sia valido.

Quando un modello diventa valido per un’esperienza o un’offerta, l’icona dell’orologio a sinistra del nome dell’esperienza o dell’offerta diventa una casella di controllo verde. In presenza di modelli validi per almeno due esperienze o offerte, alcune visite iniziano a essere personalizzate.

### Trasformazione delle feature

Prima che i dati passino attraverso l’algoritmo di personalizzazione, subisce una trasformazione funzionale che può essere considerata come la preparazione dei dati raccolti nei record di formazione per l’utilizzo da parte dei modelli di personalizzazione. La trasformazione dipende dal tipo di attributo (o &quot;funzione&quot;, come talvolta lo descrivono i data scientist):

| Tipo di funzionalità | Descrizione | Trasformazione |
|---|---|---|
| **Categorico** | Non può essere conteggiato ma può essere ordinato in gruppi diversi, ad esempio per paese, genere o codice postale. | Viene mantenuto un set di tutte le funzionalità possibili e la probabilità di trasformazione viene utilizzata per ridurre la dimensione dei dati. |
| **Numerico** | Possono essere misurate o conteggiate, ad esempio età o reddito. | Il ridimensionamento garantisce che le funzioni siano confrontabili in tutti i punti. |

### Equilibrio tra apprendimento e personalizzazione con la slot machine

Dopo che [!DNL Target] ha creato i modelli di personalizzazione, devi affrontare un compromesso per i futuri visitatori della tua attività. Puoi personalizzare tutto il traffico in base al modello corrente oppure continuare a imparare dai nuovi visitatori distribuendo loro offerte casuali. L’algoritmo di personalizzazione deve sempre scoprire le nuove tendenze nei visitatori, mentre personalizza la maggior parte del traffico. [!DNL Target] risponde a questo obiettivo in modo da garantire che il modello &quot;spenda&quot; sempre una piccola frazione di traffico per continuare a imparare per tutta la durata dell&#39;attività e per evitare un eccessivo sfruttamento delle tendenze apprese in precedenza.

Nel mondo della scienza dei dati, il problema della slot machine è un classico esempio di esplorazione contro il dilemma dello sfruttamento, in cui viene data una raccolta di slot machine, ognuna con probabilità di vincita sconosciuta. L&#39;idea chiave è quella di sviluppare una strategia che porti al gioco con la più alta probabilità di successo, in modo che la ricompensa totale ottenuta sia massimizzata. La slot machine viene utilizzata nel sistema per il punteggio online dopo la generazione dei modelli online. Questo processo facilita l’apprendimento online durante l’esplorazione. L’attuale algoritmo multi-armato è un algoritmo epsilon () greedy. In questo algoritmo, con una probabilità di 1 - μ, viene scelto il braccio migliore. Con probabilità, viene scelto in modo casuale qualsiasi altro braccio.
