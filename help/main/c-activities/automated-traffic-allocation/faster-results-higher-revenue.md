---
keywords: allocazione automatica del traffico;targeting;allocazione automatica;allocazione automatica;automated traffic allocation;targeting;auto-allocate;auto-allocate
description: Scopri in che modo un'attività [!UICONTROL Auto Allocate] in [!DNL Adobe Target] identifica un vincitore tra due o più esperienze e ridistribuisce automaticamente più traffico per il vincitore.
title: Le attività [!UICONTROL Auto-Allocate] possono ottenere risultati più rapidi e ricavi più elevati?
feature: Auto-Allocate
exl-id: 104ad88f-044b-4c2f-bdaf-f023fd1787a5
source-git-commit: e9976135c46f6658030b07fce384364f0c9ff0ed
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---

# [!UICONTROL Auto-Allocate] offre risultati di test più rapidi e ricavi più elevati rispetto a un test manuale

Con un’attività A/B manuale, potresti perdere le conversioni perché non puoi fornire l’esperienza vincente all’intero pubblico fino al completamento dell’attività. La distribuzione del traffico rimane fissa anche dopo che si riconosce che alcune esperienze stanno superando le altre e l&#39;attività deve eseguire l&#39;intero corso prima di poter agire su un vincitore.

## Allocazione automatica del traffico

Se si desidera un&#39;opzione che consenta di gestire l&#39;esperienza vincente più spesso e più precocemente nell&#39;attività rimuovendo o riducendo contemporaneamente i costi di configurazione e calcolo per la scelta delle dimensioni del campione, dei livelli di affidabilità e di altri concetti statistici, [!UICONTROL Auto-Allocate] rappresenta l&#39;opzione migliore.

## Come funziona [!UICONTROL Auto-Allocate]?

[!UICONTROL Auto-Allocate] utilizza il principio della slot machine. Se il termine non è familiare, una slot machine è un termine colloquiale (si pensi a Las Vegas). Visualizzare l&#39;allocazione automatica del traffico come se fossero presenti più slot machine, in questo caso varianti di test, e all&#39;inizio tirare tutti gli handle allo stesso modo. Nel tempo, una o più macchine, o varianti di test, potrebbero pagare più di altre. Quando questa situazione si verifica, un giocatore d&#39;azzardo inizierebbe naturalmente a tirare le maniglie di quelli che vincono più spesso. In termini di allocazione del traffico, [!DNL Target] fornisce a più visitatori l&#39;esperienza o le esperienze che stanno vincendo di più.

Prendi in considerazione la seguente illustrazione di un’attività A/B di due settimane. Con [!UICONTROL Auto-Allocate], man mano che emerge un&#39;esperienza vincente, [!UICONTROL Target] devia una maggiore parte del traffico verso quel vincitore all&#39;inizio del test.

![Illustrazione di allocazione automatica](/help/main/c-activities/automated-traffic-allocation/assets/Auto-Allocate-test.png)

## In che modo [!UICONTROL Auto-Allocate] fornisce risultati più veloci?

L’aspetto positivo è chiaro: più visitatori visualizzano le varianti più efficaci. E man mano che una singola variante avanza, sempre più visitatori vengono deviati verso quell&#39;esperienza vincente, mentre il test era ancora in corso. Questo metodo è particolarmente utile se l’attività A/B in esecuzione si verifica durante un momento di business principale, ad esempio una vacanza, il lancio di un prodotto o un evento di notizie internazionali.

## In che modo [!UICONTROL Auto-Allocate] può fornire ricavi più elevati?

[!UICONTROL Auto-Allocate] trova il vincitore più rapidamente di una divisione A/B manuale e ti consente inoltre di sfruttarlo immediatamente, acquisendo ricavi al rialzo che sarebbero stati persi in un approccio tradizionale o manuale. Poiché [!UICONTROL Auto-Allocate] indirizza più traffico all&#39;esperienza con il tasso di conversione più alto, può aumentare i ricavi mentre l&#39;attività viene eseguita e apprende.

Nell&#39;esempio seguente, [!UICONTROL Auto-Allocate] ha ottenuto più ricavi durante il test inviando più traffico (40%) all&#39;esperienza D, che aveva il tasso di conversione più alto.

![L&#39;allocazione automatica fornisce un&#39;illustrazione dei ricavi più elevata](/help/main/c-activities/automated-traffic-allocation/assets/five-experiences.png)

## In quali casi devo attenermi all’allocazione manuale del traffico?

Quando è necessario classificare le prestazioni di ogni esperienza rispetto alle altre, è più appropriato un test A/B manuale. [!UICONTROL Auto-Allocate] trova e sfrutta i migliori esecutori, ma non garantisce la differenziazione tra le esperienze con prestazioni inferiori. Utilizza l’allocazione manuale del traffico per controllare completamente la quantità di traffico del visitatore che vede ogni variante di test e per personalizzare le soglie statistiche rilevanti per la tua azienda.

## Introduzione

Intendete avviare la vostra prima attività [!UICONTROL Auto-Allocate]? [Scopri come](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md).
