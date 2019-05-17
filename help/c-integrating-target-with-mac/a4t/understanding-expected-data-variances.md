---
description: Informazioni sulle varianze di dati previste tra Target e Adobe Analytics quando non si utilizza Analytics come origine per la generazione di rapporti (A4T). Questo elimina completamente la varianza di dati.
keywords: varianze di dati;analytics;differenze;varianza;a4t;analytics for target;analytics come origine per la generazione di rapporti;discrepanze;discrepanza
seo-description: Informazioni sulle varianze di dati previste tra Target e Adobe Analytics quando non si utilizza Analytics come origine per la generazione di rapporti (A4T). Questo elimina completamente la varianza di dati.
seo-title: Varianze di dati previste quando non si utilizza A4T
solution: Target
title: Varianze di dati previste quando non si utilizza A4T
topic: Advanced
uuid: 61bef460-8613-4251-b1b2-b6226ec86d9b
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Variabilità dei dati previste tra Target e Analytics durante l’utilizzo e non utilizzo A4T{#expected-data-variances-when-not-using-a-t}

Informazioni sulle varianti di dati previste tra [!DNL Target] e Adobe [!DNL Analytics] quando *si utilizza* e *non* utilizzano Analytics come Origine di reporting (A 4 T). A4T riduce in modo significativo la varianza dei dati.

## Varianza dati prevista quando si utilizza A 4 T {#expected-using-a4t}

Con A4T, i rapporti delle attività di Analytics e di Target utilizzano esclusivamente i dati di Analytics, in modo che non ci sia varianza tra le soluzioni nei rapporti delle attività di Target. In alcuni casi, tuttavia, i clienti potrebbero confrontare i dati di Target con quelli di Analytics al di fuori dell’ambito dell’integrazione di A4T e, quindi, riscontrare i problemi di varianza descritti sotto.

Di seguito sono riportati alcuni scenari in cui potrebbe verificarsi la varianza dei dati prevista:

* A 4 T consente la possibilità che un hit Target (parte superiore della pagina) si verifichi, ma non si verifichi alcun hit Analytics (in fondo alla pagina). Un esempio di ciò è se l&#39;utente carica la pagina, ma chiude il browser prima che venga attivata la chiamata Analytics. In questi casi, A 4 T esclude l&#39;hit di Target dai nostri dati. Il motivo è che consentendo a Target (di nuovo, all&#39;inizio della pagina) di contare come hit Analytics in assenza di una chiamata Analytics effettiva, verrebbero creati incoerenze con i dati impostati in Analytics (inflazione visitatore, ecc.).

   Se in Target è configurato un test di reindirizzamento per dividere il traffico 50/50 (o 25/25/25/25, ecc.), il comportamento dell&#39;utente potrebbe non essere diviso in modo uniforme. Se visualizzi una suddivisione non uniforme, significa semplicemente che un gruppo di utenti non ha eseguito una chiamata Analytics sulla pagina di destinazione più degli altri gruppi. Questo mancato esecuzione della chiamata di Analytics per un gruppo causava l&#39;esclusione dell&#39;hit Target per tale utente, creando l&#39;uniformità.

   Questo è un problema che speriamo di poter affrontare in futuro mentre lavoriamo verso A 4 T su Adobe Experience Platform. I nostri team stanno lavorando attraverso il modo migliore per gestire questi eventi diversi in momenti diversi sulla pagina.

* Supponete di creare un&#39;attività di allocazione automatica aperta a tutti i visitatori a una particolare pagina. Dato che le attività di allocazione automatica non supportano A4T, tutti i dati delle attività vengono raccolti per [!DNL Target]. Potresti aspettarti che i visitatori dell’attività corrispondano, nei rapporti di [!DNL Target], ai visitatori di quella pagina nei rapporti di [!DNL Analytics] considerando stesso intervallo di date. È uno scenario in cui la varianza descritta sotto è prevista.

   Per un elenco completo dei tipi di attività che supportano A4T, consulta [Tipi di attività supportate](../../c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA).

## Varianza dei dati prevista quando *non si utilizza* A4T {#expected-not-using-a4t}

Varianze del 15-20% sono normali, anche con set di dati simili. I sistemi che contano in modo diverso possono riportare varianze di dati molto più elevate, fino al 35-50%. In alcuni casi, le varianze possono essere ancora più elevate.

Anche se i dati reali possono variare significativamente, le tendenze di solito sono costanti. Fintanto che le differenze e le tendenze rimangono coerenti, i dati rimangono preziosi e utili. Se le differenze e le tendenze sono incoerenti, potrebbe significare che qualcosa è impostato in modo errato. In questo caso, rivolgiti al rappresentante del tuo account per richiedere assistenza.

[!DNL Analytics] utilizza un sistema basato su visite e transazioni, mentre [!DNL Target] utilizza metriche basate sui visitatori. Ciò significa che, ogni volta che un visitatore apre una pagina, [!DNL Analytics] conta una visita. [!DNL Target], invece, la conteggia solo se vengono soddisfatte le condizioni stabilite nell’attività.

I rapporti di [!DNL Target] descrivono le prestazioni in base alla mbox di conversione selezionata al momento della definizione dell’attività, ma i dati di tale mbox di conversione non vengono inviati ad [!DNL Analytics], che dispone di proprie variabili di conversione definite dallʼimplementazione dei tag di [!DNL Analytics]. Nei casi in cui ci si potrebbero aspettare dati identici (ad esempio, se nella pagina di conferma dellʼordine di un venditore sono presenti sia una mbox di conversione che un evento di acquisto [!DNL Analytics]), i dati potrebbero essere diversi a causa del posizionamento di tali tag. In generale, le tendenze evidenziate nei rapporti dei due prodotti dovrebbero essere simili.

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
* Una singola mbox può essere posizionata su più pagine e contare i visitatori su ciascuna di esse
* Le priorità dell’attività potrebbero includere alcuni visitatori ed escluderne altri in una pagina
* I visitatori che sono stati convertiti una volta possono essere conteggiati di nuovo quando accedono nuovamente all’attività
* [!DNL Analytics] conta tutte le conversioni per tutte le visite e i visitatori, mentre [!DNL Target] conta solo le conversioni per le visite e i visitatori inclusi nell’attività