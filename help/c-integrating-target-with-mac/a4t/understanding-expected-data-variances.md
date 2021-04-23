---
keywords: varianze di dati;analytics;differenze;varianza;a4t;analytics for target;analytics come origine per la generazione di rapporti;discrepanze;discrepanza
description: Scopri le varianze di dati previste tra Adobe [!DNL Target] and Analytics when not using Analytics for [!DNL Target] (A4T), che elimina completamente la varianza di dati.
title: Qual è la varianza di dati prevista tra Analytics e A4T?
feature: Analytics for Target (A4T)
exl-id: 9e63f309-8ec1-4ed5-a1f9-6c3098a7b8f6
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '763'
ht-degree: 49%

---

# Varianze di dati previste tra Adobe [!DNL Target] e Adobe Analytics durante l’utilizzo con e senza A4T

Informazioni sulle varianze di dati previste tra [!DNL Target] e Adobe [!DNL Analytics] quando vengono utilizzati *con* e *senza* Analytics come origine per la generazione di rapporti (A4T). A4T riduce in modo significativo la varianza dei dati.

## Varianza dei dati prevista quando si utilizza A4T {#expected-using-a4t}

Con A4T, i rapporti delle attività di Analytics e di Target utilizzano esclusivamente i dati di Analytics, in modo che non ci sia varianza tra le soluzioni nei rapporti delle attività di Target. In alcuni casi, tuttavia, i clienti confrontano i dati di Target con quelli di Analytics al di fuori dell’ambito dell’integrazione A4T e, quindi, riscontrano i problemi di varianza descritti di seguito.

Di seguito sono riportati alcuni scenari in cui è possibile verificare la varianza dei dati prevista:

* In A4T è possibile che si verifichi un hit di Target (nella parte superiore della pagina), ma che non si verifichi un hit di Analytics (nella parte inferiore della pagina). Ad esempio, supponiamo che un visitatore carichi la pagina, ma chiuda il browser prima che venga attivata la chiamata di Analytics. In questi casi, A4T esclude l’hit di Target dai dati. Consentire agli hit di Target (di nuovo, nella parte superiore della pagina) di essere conteggiati come hit di Analytics in assenza di una chiamata Analytics effettiva crea incongruenze con i dati impostati in Analytics (inflazione dei visitatori e così via).

   Se in Target è impostato un test di reindirizzamento per dividere il traffico 50/50 (o 25/25/25/25 e così via), il comportamento dell’utente potrebbe non essere suddiviso in modo uniforme. Se visualizzi una suddivisione non uniforme, significa semplicemente che un gruppo di utenti non è riuscito a eseguire una chiamata Analytics sulla pagina di destinazione più di quanto non abbiano fatto gli altri gruppi. La mancata esecuzione della chiamata di Analytics per un gruppo ha causato l’esclusione dell’hit di Target per tali utenti, creando così una discrepanza nei dati.

   Adobe spera di affrontare questo problema in futuro, poiché i team di Adobe lavorano per A4T su Adobe Experience Platform. I team di Adobe stanno determinando come gestire questi diversi eventi che si verificano in momenti diversi della pagina.

   >[!NOTE]
   >
   >A causa di un problema noto, un numero limitato di clienti con reindirizzamenti A4T ottengono una percentuale più alta di hit non uniti. Consulta [Problemi noti e problemi risolti](/help/r-release-notes/known-issues-resolved-issues.md#redirect).

## Varianza dei dati prevista quando *non si utilizza* A4T {#expected-not-using-a4t}

Varianze del 15-20% sono normali, anche con set di dati simili. I sistemi che contano in modo diverso possono riportare varianze di dati molto più elevate, fino al 35-50%. A volte le varianze possono essere anche più alte.

Anche se i dati reali possono variare significativamente, le tendenze di solito sono costanti. Fintanto che le differenze e le tendenze rimangono coerenti, i dati rimangono preziosi e utili. Se le differenze e le tendenze sono incoerenti, potrebbe significare che qualcosa è impostato in modo errato. In questo caso, rivolgiti al rappresentante del tuo account per richiedere assistenza.

[!DNL Analytics] utilizza un sistema basato su visite e transazioni, mentre [!DNL Target] utilizza metriche basate sui visitatori. Ogni volta che un visitatore apre una pagina, conta una visita in [!DNL Analytics], ma [!DNL Target] non la conteggia finché non vengono soddisfatte le condizioni stabilite nell’attività.

I rapporti in [!DNL Target] mostrano le prestazioni in base alla mbox di conversione selezionata al momento della definizione dell’attività. Tuttavia, questi dati mbox di conversione non vengono inviati a [!DNL Analytics], che dispone di proprie variabili di conversione definite dall’ implementazione dei tag [!DNL Analytics] . Se si attendono dati identici (ad esempio, se l&#39;ordine di un venditore conferma che la pagina contiene sia una mbox di conversione che un evento di acquisto [!DNL Analytics]), i dati possono essere diversi a causa del posizionamento di tali tag. In generale, le tendenze nelle relazioni dei due prodotti sono simili.

Le varianze di dati previste possono essere causate da differenze tecniche e di business.

### Esempi di varianze tecniche  {#section_C3B50ED2E2F9416FAC91437CF1A87369}

I seguenti elementi possono causare varianze di dati in base a differenze tecniche:

* I visitatori di [!DNL Target] devono consentire i cookie e JavaScript
* I cookie di prime e di terze parti vengono elaborati in modo diverso; di conseguenza, i dati di questi tipi di cookie non corrispondono
* Posizione relativa dei tag sulle pagine e “perdita” causata da visitatori che escono dalla pagina prima che questa sia stata caricata completamente
* Considerazioni sul fuso orario
* Differenze nel conteggio dei dispositivi

### Esempi di varianze di business  {#section_2E1EB5E15BB64A1A80E4CDB1A5062AEE}

I seguenti elementi possono causare varianze di dati in base a differenze di business:

* Differenze tra metriche di visitatori e visite
* Il targeting sulle attività esclude alcuni visitatori
* Una singola mbox su più pagine, contando i visitatori su ciascuna di queste pagine
* Le priorità di attività possono includere alcuni visitatori ed escluderne altri in una pagina
* I visitatori che si sono convertiti una volta possono essere conteggiati di nuovo quando accedono nuovamente all’attività
* [!DNL Analytics] conta tutte le conversioni per tutte le visite e i visitatori, mentre [!DNL Target] conta solo le conversioni per le visite e i visitatori inclusi nell’attività
