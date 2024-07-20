---
keywords: foresta casuale;albero decisionale;ap;Automated Personalization
description: Scopri come [!DNL Adobe Target] utilizza l'algoritmo Foresta casuale nelle attività [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Auto-Target].
title: In che modo  [!DNL Target]  utilizza l'algoritmo Foresta casuale?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."
feature: Automated Personalization
exl-id: 07a89525-4071-4434-ac96-c59a4f4422ad
source-git-commit: d5b24f298ae405d57c2ba639082cbe99c4e358fd
workflow-type: tm+mt
source-wordcount: '1413'
ht-degree: 41%

---

# Algoritmo Foresta casuale

L&#39;algoritmo di personalizzazione principale utilizzato in entrambe le attività (AP) e [!DNL Auto-Target] è Foresta casuale. I metodi di raggruppamento, come Foresta casuale, utilizzano più algoritmi di apprendimento per ottenere prestazioni predittive migliori rispetto a quelle ottenibili da uno qualsiasi degli algoritmi di apprendimento costituenti. L&#39;algoritmo Foresta casuale in [!UICONTROL Automated Personalization] e [!UICONTROL Auto-Target] è un metodo di classificazione o di regressione che funziona costruendo una moltitudine di alberi decisionali quando viene addestrato.

Quando si pensa alle statistiche, si potrebbe pensare a un unico modello di regressione utilizzato per prevedere un risultato. L&#39;ultima ricerca sui dati scientifici suggerisce che i “metodi di raggruppamento”, in cui vengono creati più modelli dallo stesso insieme di dati e quindi combinati in modo intelligente, producono risultati migliori di quanto prevedano in base a un solo modello.

L&#39;algoritmo Foresta casuale è l&#39;algoritmo chiave di personalizzazione sottostante utilizzato nelle attività [!UICONTROL Automated Personalization] e [!UICONTROL Auto-Target]. Foresta casuale combina centinaia di alberi decisionali per ottenere una previsione migliore di quanto un singolo albero possa fare da solo.

## Che cos&#39;è un albero decisionale? {#section_7F5865D8064447F4856FED426243FDAC}

L&#39;obiettivo di una struttura decisionale è quello di raggruppare tutti i dati di visita disponibili da cui un sistema può imparare e poi raggruppare tali dati, in cui le visite all&#39;interno di ogni gruppo sono più simili possibile l&#39;una all&#39;altra per quanto riguarda la metrica di obiettivo. Tra i gruppi, tuttavia, le visite sono il più possibile diverse, per quanto riguarda la metrica di obiettivo (ad esempio, il tasso di conversione). L’albero decisionale esamina le diverse variabili di cui dispone nel set di apprendimento per determinare come suddividere i dati in modo reciprocamente esclusivo collettivamente esaustivo (MECE) in questi gruppi (o &quot;foglie&quot;) per massimizzare questo obiettivo.

In un semplice esempio, supponiamo due variabili di input:

* Genere (con due valori potenziali, Maschio o Femmina)
* Codice postale (con cinque valori potenziali nel set di dati ridotto: 11111, 22222, 33333, 44444 o 55555)

Se la metrica di obiettivo è la conversione, la struttura determina innanzitutto quale delle due variabili spiega la maggiore quantità di variazione nel tasso di conversione dei dati della visita.

Diciamo che il codice postale è più predittivo. Questa variabile forma il primo “ramo” dell&#39;albero. L&#39;albero decisionale determinerebbe quindi come suddividere i dati di visita, ad esempio il tasso di conversione dei dati all&#39;interno di ogni suddivisione era il più simile possibile e il tasso di conversione tra le suddivisioni era il più diverso possibile. In questo esempio, si supponga 11111, 22222, 33333 siano una divisione e 44444 e 55555 una seconda divisione.

Questa azione determina il primo livello dell’albero decisionale:

![immagine struttura_decisioni_1](assets/decsion_tree_1.png)

L&#39;albero decisionale pone la domanda: &quot;Qual è la variabile più predittiva?&quot; In questo esempio, ci sono solo due variabili, quindi la risposta qui è chiaramente di genere. L&#39;albero ora cerca di completare un esercizio simile per dividere i dati *in ogni ramo*. Per prima cosa, consideriamo il ramo 11111, 22222 e 33333. In questi codici di avviamento postale, se ci fosse una differenza di conversione tra uomini e donne, ci sarebbero due foglie (uomini e donne) e questo ramo sarebbe completo. Negli altri rami, 44444 e 55555, supponiamo che non ci sia differenza statistica tra le conversioni di donne e uomini. In questo caso, il primo ramo diventa la divisione finale.

L’esempio si tradurrebbe nella struttura seguente:

![immagine_albero_delle_decisioni_2](assets/decsion_tree_2.png)

## Come vengono utilizzati gli alberi decisionali da Foresta casuale? {#section_536C105EF9F540C096D60450CAC6F627}

Gli alberi decisionali possono essere un potente strumento statistico. Tuttavia, hanno alcuni svantaggi. Il problema maggiore è che si adattano “troppo” ai dati, in questo modo un singolo albero predice male i dati futuri che non sono stati utilizzati per generare l&#39;albero iniziale. Questa sfida è conosciuta come il [compromesso bias-variance](https://en.wikipedia.org/wiki/Bias%E2%80%93variance_tradeoff) nell&#39;apprendimento statistico. Le foreste casuali aiutano a superare questa sfida. Al livello più alto, una Foresta casuale è una raccolta di alberi decisionali che vengono generati in modo leggermente diverso sullo stesso insieme di dati che “vota” insieme per produrre un modello migliore rispetto a un singolo albero. Gli alberi vengono costruiti selezionando in modo casuale un sottoinsieme di record di visita con la sostituzione (nota come insaccamento) e selezionando in modo casuale un sottoinsieme di attributi, in modo che la foresta sia costituita da alberi decisionali leggermente diversi. Questo metodo introduce piccole variazioni nelle strutture create in Foresta casuale. L&#39;aggiunta in questa quantità controllata di varianza consente di migliorare la precisione predittiva dell&#39;algoritmo.

## In che modo gli algoritmi di personalizzazione [!DNL Target] utilizzano Foresta casuale? {#section_32FB53CAD8DF40FB9C0F1217FBDBB691}

### Come vengono generati i modelli

Il diagramma seguente riepiloga il modo in cui i modelli vengono generati per le attività [!UICONTROL Auto-Target] e [!UICONTROL Automated Personalization]:

![immagine flusso_foresta_casuale](assets/random_forest_flow.png){width="650" zoomable="yes"}

1. Target raccoglie dati sui visitatori mentre distribuisce esperienze o offerte in modo casuale
1. Dopo che [!DNL Target] ha raggiunto una massa critica di dati, [!DNL Target] esegue la progettazione delle funzionalità
1. [!DNL Target] genera modelli Foresta casuale per ogni esperienza o offerta
1. [!DNL Target] verifica se il modello soddisfa un punteggio di qualità di soglia
1. [!DNL Target] invia il modello in produzione per personalizzare il traffico futuro

[!DNL Target] utilizza i dati raccolti automaticamente e i dati personalizzati forniti dall&#39;utente per creare gli algoritmi di personalizzazione. Questi modelli prevedono la migliore esperienza o offerta da mostrare ai visitatori. In genere, un modello viene generato per esperienza (se un&#39;attività [!UICONTROL Auto-Target]) o per offerta (se un&#39;attività [!UICONTROL Automated Personalization]). [!DNL Target] visualizza quindi l&#39;esperienza o l&#39;offerta che produce la metrica di successo più alta prevista (ad esempio, il tasso di conversione). Questi modelli devono essere appresi su visite fornite casualmente prima di poter essere utilizzati per la previsione. Di conseguenza, quando un&#39;attività inizia prima, anche ai visitatori che si trovano nel gruppo personalizzato vengono mostrate casualmente diverse esperienze o offerte fino a quando gli algoritmi di personalizzazione sono pronti.

Ogni modello deve essere convalidato per garantire che sia in grado di prevedere il comportamento dei visitatori prima che venga utilizzato nell’attività. I modelli vengono convalidati in base alla rispettiva area sotto la curva (AUC). A causa della necessità di convalida, il momento esatto in cui un modello inizia a fornire esperienze personalizzate dipende dai dettagli dei dati. In pratica, per scopi di pianificazione del traffico, di solito richiede più del numero minimo di conversioni prima che ogni modello sia valido.

Quando un modello diventa valido per un&#39;esperienza o un&#39;offerta, l&#39;icona dell&#39;orologio a sinistra del nome dell&#39;esperienza/offerta diventa una spunta verde. In presenza di modelli validi per almeno due esperienze o offerte, alcune visite iniziano a essere personalizzate.

### Trasformazione delle feature

Prima che i dati passino attraverso l&#39;algoritmo di personalizzazione, subisce una trasformazione di funzionalità, che può essere pensata come la preparazione dei dati raccolti tra quelli di apprendimento per l&#39;utilizzo da parte dei modelli di personalizzazione.

Le trasformazioni di funzionalità dipendono dal tipo di attributo. Pricipalmente, esistono due tipi di attributi (o “funzionalità” come sono descritti a volte dagli scienziati di dati):

* **Categoriche:** le funzionalità categoriche non possono essere conteggiate ma possono essere ordinate in gruppi diversi. Potrebbero essere caratteristiche come paese, genere, o codice postale.
* **Numeriche:** le funzionalità numeriche possono essere misurate o conteggiate, ad esempio età, reddito e così via.

Per le funzionalità categoriche, viene mantenuto un insieme di tutte le funzionalità possibili e la probabilità di trasformazione viene utilizzata per ridurre la dimensione dei dati. Per le feature numeriche, il ridimensionamento garantisce la comparabilità delle feature a livello generale.

### Equilibrio tra apprendimento e personalizzazione con la slot machine

Dopo che [!DNL Target] avrà creato modelli di personalizzazione per personalizzare il traffico, c&#39;è un chiaro compromesso che devi affrontare per i futuri visitatori della tua attività. Dovresti personalizzare tutto il traffico in base al modello corrente o continuare a imparare dai nuovi visitatori fornendo loro offerte casuali? Vuoi assicurarti che l&#39;algoritmo di personalizzazione apprenda sempre nuove tendenze nei visitatori, personalizzando contemporaneamente la maggior parte del traffico.

La slot machine è il modo in cui [!DNL Target] ti aiuta a raggiungere questo obiettivo. La slot machine assicura che il modello &quot;spenda&quot; sempre una piccola frazione di traffico per continuare a imparare per tutta la vita dell&#39;attività di apprendimento e per prevenire un eccessivo sfruttamento delle tendenze apprese in precedenza.

Nel mondo della scienza dei dati, il problema della slot machine è un classico esempio di esplorazione contro il dilemma di sfruttamento in cui viene data una raccolta di slot machine, ognuna con probabilità di vincita sconosciuta. L&#39;idea fondamentale consiste nello sviluppare una strategia, che si traduce nel giocare con la leva con la probabilità più elevata di successo, in modo da massimizzare la vincita totale ottenuta. Il slot machine viene utilizzato nel sistema per il punteggio online dopo la generazione dei modelli online. Questo processo facilita l’apprendimento online durante l’esplorazione. L’attuale algoritmo multi-armato è un algoritmo epsilon () greedy. In questo algoritmo viene scelta la leva migliore con probabilità 1- ε. Inoltre, qualsiasi altra leva viene scelta a caso con probabilità ε.
