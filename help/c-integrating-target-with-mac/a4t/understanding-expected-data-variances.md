---
keywords: data variances;analytics;differences;variance;a4t;analytics for target;analytics as the reporting source;discrepancies;discrepancy
description: Informazioni sulle varianze di dati previste tra Target e Adobe Analytics quando non si utilizza Analytics come origine per la generazione di rapporti (A4T). Questo elimina completamente la varianza di dati.
title: Varianze di dati previste quando non si utilizza A4T
feature: null
topic: Advanced
uuid: 61bef460-8613-4251-b1b2-b6226ec86d9b
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 100%

---


# Varianze di dati previste tra Target e Analytics durante l’utilizzo con e senza A4T{#expected-data-variances-when-not-using-a-t}

Informazioni sulle varianze di dati previste tra [!DNL Target] e Adobe [!DNL Analytics] quando vengono utilizzati *con* e *senza* Analytics come origine per la generazione di rapporti (A4T). A4T riduce in modo significativo la varianza dei dati.

## Varianza dei dati prevista quando si utilizza A4T {#expected-using-a4t}

Con A4T, i rapporti delle attività di Analytics e di Target utilizzano esclusivamente i dati di Analytics, in modo che non ci sia varianza tra le soluzioni nei rapporti delle attività di Target. In alcuni casi, tuttavia, i clienti potrebbero confrontare i dati di Target con quelli di Analytics al di fuori dell’ambito dell’integrazione di A4T e, quindi, riscontrare i problemi di varianza descritti sotto.

Di seguito sono riportati alcuni scenari in cui potresti riscontrare una varianza dei dati prevista:

* In A4T è possibile che si verifichi un hit di Target (nella parte superiore della pagina), ma che non si verifichi un hit di Analytics (nella parte inferiore della pagina). Un esempio potrebbe essere quando l’utente carica la pagina, ma chiude il browser prima che venga attivata la chiamata Analytics. In questi casi, A4T esclude l’hit di Target dai nostri dati. Il motivo è che consentendo agli hit di Target (nella parte superiore della pagina) di essere considerati come hit di Analytics in assenza di una chiamata Analytics effettiva, verrebbero creati incoerenze con i dati impostati in Analytics (visitatori in eccesso, ecc.).

   Se è configurato un test di reindirizzamento in Target per dividere il traffico 50/50 (o 25/25/25/25, ecc.), il comportamento utente potrebbe non essere diviso in modo uniforme. Se visualizzi una suddivisione non uniforme, significa semplicemente che, per un gruppo di utenti, si è verificata una maggiore incidenza di mancata esecuzione della chiamata Analytics sulla pagina di destinazione, rispetto agli altri gruppi. La mancata esecuzione della chiamata di Analytics per un gruppo ha causato l’esclusione dell’hit di Target per tali utenti, creando così una discrepanza nei dati.

   È un problema che speriamo di poter affrontare in futuro, con A4T su Adobe Experience Platform. I nostri team stanno lavorando sul modo migliore di gestire eventi diversi che si verificano in momenti diversi della pagina.

   >[!NOTE]
   >
   >A causa di un problema noto, un numero limitato di clienti con reindirizzamenti A4T ottengono una percentuale più alta di hit non uniti. Consulta [Problemi noti e problemi risolti](/help/r-release-notes/known-issues-resolved-issues.md#redirect).

* Supponi di creare un’attività di allocazione automatica aperta a tutti i visitatori di una pagina particolare. Dato che le attività di allocazione automatica non supportano A4T, tutti i dati delle attività vengono raccolti per [!DNL Target]. Potresti aspettarti che i visitatori dell’attività corrispondano, nei rapporti di [!DNL Target], ai visitatori di quella pagina nei rapporti di [!DNL Analytics] considerando stesso intervallo di date. È uno scenario in cui la varianza descritta sotto è prevista.

   Per un elenco completo dei tipi di attività che supportano A4T, consulta [Tipi di attività supportate](../../c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA).

## Varianza dei dati prevista quando *non si utilizza* A4T {#expected-not-using-a4t}

Varianze del 15-20% sono normali, anche con set di dati simili. I sistemi che contano in modo diverso possono riportare varianze di dati molto più elevate, fino al 35-50%. In alcuni casi, le varianze possono essere ancora più elevate.

Anche se i dati reali possono variare significativamente, le tendenze di solito sono costanti. Fintanto che le differenze e le tendenze rimangono coerenti, i dati rimangono preziosi e utili. Se le differenze e le tendenze sono incoerenti, potrebbe significare che qualcosa è impostato in modo errato. In questo caso, rivolgiti al rappresentante del tuo account per richiedere assistenza.

[!DNL Analytics] utilizza un sistema basato su visite e transazioni, mentre [!DNL Target] utilizza metriche basate sui visitatori. Ciò significa che, ogni volta che un visitatore apre una pagina, [!DNL Analytics] conta una visita. [!DNL Target], invece, la conteggia solo se vengono soddisfatte le condizioni stabilite nell’attività.

I rapporti di [!DNL Target] descrivono le prestazioni in base alla mbox di conversione selezionata al momento della definizione dell’attività, ma i dati di tale mbox di conversione non vengono inviati ad [!DNL Analytics], che dispone di proprie variabili di conversione definite dallʼimplementazione dei tag di [!DNL Analytics]. Nei casi in cui ci si potrebbero aspettare dati identici (ad esempio, se nella pagina di conferma dellʼordine di un venditore sono presenti sia una mbox di conversione che un evento di acquisto [!DNL Analytics]), i dati potrebbero essere diversi a causa del posizionamento di tali tag. In generale, le tendenze evidenziate nei rapporti dei due prodotti dovrebbero essere simili.

Le varianze di dati previste possono essere causate da differenze tecniche e di business.

### Esempi di varianze tecniche {#section_C3B50ED2E2F9416FAC91437CF1A87369}

I seguenti elementi possono causare varianze di dati in base a differenze tecniche:

* I visitatori di [!DNL Target] devono consentire i cookie e JavaScript
* I cookie di prime e di terze parti vengono elaborati in modo diverso; di conseguenza, i dati di questi tipi di cookie non corrispondono
* Posizione relativa dei tag sulle pagine e “perdita” causata da visitatori che escono dalla pagina prima che questa sia stata caricata completamente
* Considerazioni sul fuso orario
* Differenze nel conteggio dei dispositivi

### Esempi di varianze di business {#section_2E1EB5E15BB64A1A80E4CDB1A5062AEE}

I seguenti elementi possono causare varianze di dati in base a differenze di business:

* Differenze tra metriche di visitatori e visite
* Il targeting sulle attività esclude alcuni visitatori
* Una singola mbox può essere posizionata su più pagine e contare i visitatori su ciascuna di esse
* Le priorità dell’attività potrebbero includere alcuni visitatori ed escluderne altri in una pagina
* I visitatori che sono stati convertiti una volta possono essere conteggiati di nuovo quando accedono nuovamente all’attività
* [!DNL Analytics] conta tutte le conversioni per tutte le visite e i visitatori, mentre [!DNL Target] conta solo le conversioni per le visite e i visitatori inclusi nell’attività