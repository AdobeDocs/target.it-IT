---
keywords: automated traffic allocation;targeting;auto-allocate
description: L’allocazione automatica identifica un vincitore tra due o più esperienze e, di conseguenza, ridistribuisce automaticamente più traffico per aumentare le conversioni, mentre il test continua a essere eseguito e ad apprendere.
title: L'allocazione automatica consente di ottenere risultati di test più rapidi e ricavi maggiori rispetto a un test manuale
feature: auto-allocate
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 5%

---


# L&#39;allocazione automatica consente di ottenere risultati di test più rapidi e ricavi maggiori rispetto a un test manuale

Con un&#39;attività A/B manuale, potresti perdere conversioni perché non puoi distribuire l&#39;esperienza vincente a tutto il pubblico fino al completamento dell&#39;attività. La distribuzione del traffico rimane fissa anche dopo aver riconosciuto che alcune esperienze hanno prestazioni migliori di altre, e che l&#39;attività deve eseguire l&#39;intero corso prima di poter agire su un vincitore.

## Allocazione automatica del traffico

Se desiderate un&#39;opzione per distribuire l&#39;esperienza vincente più spesso e prima nell&#39;attività, rimuovendo o riducendo contemporaneamente il costo di configurazione e calcolo della raccolta delle dimensioni del campione, i livelli di confidenza e altri concetti statistici, [!UICONTROL Auto-Allocate] è la scelta migliore.

## Come funziona l&#39;allocazione automatica?

[!UICONTROL Auto-Allocate] utilizza il principio del bandit multi-armato. Se il termine non è familiare, un bandito monomarca è un termine colloquiale per una slot machine (pensare: Las Vegas). Visualizzare l&#39;allocazione automatica del traffico come se avesse più slot machine, in questo caso, varianti di test, e all&#39;inizio tirare tutti i handle in modo uguale. Nel tempo, una o più macchine, o varianti di test, potrebbero pagare più di altre. Quando questo accade, un giocatore naturalmente inizierebbe a tirare le maniglie di quelli che vincono più spesso. In termini di allocazione del traffico, [!DNL Adobe Target] sarà utile a più visitatori l&#39;esperienza o le esperienze che stanno vincendo di più.

Considerate la seguente illustrazione di un&#39;attività A/B di due settimane. Con [!UICONTROL Auto-Allocate], man mano che emerge un&#39;esperienza vincente, [!UICONTROL Target] trasferisce una parte maggiore del traffico a tale vincitore all&#39;inizio del test.

![Allocazione automatica dell&#39;illustrazione](/help/c-activities/automated-traffic-allocation/assets/Auto-Allocate-test.png)

## In che modo Auto-Allocate offre risultati più rapidi?

Il lato positivo è piuttosto chiaro: più visitatori visualizzano le varianti che offrono le migliori prestazioni. E man mano che una singola variante va avanti, ancora più visitatori vengono deviati verso quell&#39;esperienza vincente, mentre il test era ancora in corso. Questa funzione è particolarmente utile se l&#39;attività A/B in esecuzione avviene durante un momento di business principale, ad esempio una vacanza, un lancio di prodotti o un evento di notizie nel mondo.

## In che modo Auto-Allocate potrebbe fornire maggiori entrate?

[!UICONTROL Allocazione] automatica individua il vincitore più rapidamente di una suddivisione A/B manuale, e consente inoltre di sfruttare il vincitore immediatamente acquisendo le entrate positive che avrebbero perso con un approccio tradizionale o manuale. Poiché l&#39;allocazione [!UICONTROL automatica] indirizza più traffico all&#39;esperienza con il tasso di conversione più elevato, può aumentare le entrate mentre l&#39;attività viene eseguita e apprende.

Nell&#39;esempio seguente, [!UICONTROL Auto-Allocate] ha guadagnato più ricavi durante il test spingendo più traffico (40%) nell&#39;Esperienza D, che aveva il tasso di conversione più alto.

![L&#39;allocazione automatica fornisce un&#39;illustrazione delle entrate più elevata](/help/c-activities/automated-traffic-allocation/assets/five-experiences.png)

## In quali casi devo attenersi all&#39;allocazione manuale del traffico?

Per classificare in ordine le prestazioni di ogni esperienza rispetto agli altri, è più applicabile un test A/B manuale. [!UICONTROL L&#39;allocazione automatica] individua e sfrutta i migliori esecutori ma non garantisce la differenziazione tra le esperienze con prestazioni inferiori. È consigliabile utilizzare l&#39;allocazione manuale del traffico per controllare completamente la quantità di traffico dei visitatori che vede ogni variante di test e per personalizzare le soglie statistiche rilevanti per la propria attività.

## Guida introduttiva

Pronto per avviare la tua prima attività di allocazione [!UICONTROL automatica] ? [Scopri come](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md).

