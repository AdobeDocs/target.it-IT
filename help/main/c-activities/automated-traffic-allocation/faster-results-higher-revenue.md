---
keywords: allocazione automatica del traffico;targeting;allocazione automatica;allocazione automatica;automated traffic allocation;targeting;auto-allocate;auto-allocate
description: Scopri in che modo un'attività di [!UICONTROL Allocazione automatica] in [!DNL Adobe Target] identifica un vincitore tra due o più esperienze e ridistribuisce automaticamente più traffico per il vincitore.
title: Le attività di [!UICONTROL Allocazione automatica] possono ottenere risultati più rapidi e ricavi più elevati?
feature: Auto-Allocate
exl-id: 104ad88f-044b-4c2f-bdaf-f023fd1787a5
TQID: 'https://experienceleague.adobe.com/aSxZ0Zp3cm0x-fVBXHWW4OiXd3Riz-tuhBiw0f8m4lk'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: f2d0aafb-18af-41a0-a32e-2788eafacc2b
    internal-label: Auto-allocate
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 878df20c7fb08c893239135c20f358b5606d0c6f
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 0%
---
# Prestazioni di [!UICONTROL Allocazione automatica] superiori a un test manuale {#faster-results-higher-revenue}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri perché un&#39;attività di **[!UICONTROL Allocazione automatica]** può fornire risultati più rapidi e ricavi più elevati rispetto a un test A/B manuale, come funziona e quando l&#39;allocazione manuale del traffico rimane la scelta migliore.

>[!ENDSHADEBOX]

Con un’attività A/B manuale, potresti perdere le conversioni perché non puoi fornire l’esperienza vincente all’intero pubblico fino al completamento dell’attività. La distribuzione del traffico rimane fissa anche dopo che si riconosce che alcune esperienze stanno superando le altre e l&#39;attività deve eseguire l&#39;intero corso prima di poter agire su un vincitore.

## Allocazione automatica del traffico {#auto-allocating-traffic}

**[!UICONTROL Allocazione automatica]** è l&#39;opzione migliore se desideri fornire l&#39;esperienza vincente più spesso e prima nell&#39;attività, rimuovendo o riducendo al contempo i costi di configurazione e calcolo della selezione delle dimensioni del campione, dei livelli di affidabilità e di altri concetti statistici.

## Come funziona [!UICONTROL Allocazione automatica]? {#how-it-works}

**[!UICONTROL Allocazione automatica]** utilizza il principio del slot machine. Una slot machine è un termine colloquiale che indica una slot machine. Pensate all&#39;allocazione automatica del traffico come un insieme di slot machine, in questo caso varianti di test, i cui handle vengono tirati equamente in un primo momento. Nel tempo, una o più macchine, o varianti di test, potrebbero pagare più di altre. Quando questa situazione si verifica, un giocatore d&#39;azzardo inizia naturalmente a tirare le maniglie delle macchine che vincono più spesso. In termini di allocazione del traffico, [!DNL Target] fornisce a più visitatori l&#39;esperienza o le esperienze che stanno vincendo di più.

L’illustrazione seguente mostra un’attività A/B di due settimane. Con **[!UICONTROL Allocazione automatica]**, quando emerge un&#39;esperienza vincente, [!DNL Target] devia più traffico a tale vincitore all&#39;inizio del test.

![Illustrazione di allocazione automatica](/help/main/c-activities/automated-traffic-allocation/assets/Auto-Allocate-test.png)

## In che modo [!UICONTROL Allocazione automatica] fornisce risultati più rapidi? {#faster-results}

Più visitatori visualizzano le varianti più efficaci. Man mano che una singola variante avanza, sempre più visitatori vengono dirottati verso l’esperienza vincente mentre il test è ancora in esecuzione. Questo metodo è particolarmente utile se l&#39;attività A/B viene eseguita durante un momento di business principale, ad esempio una vacanza, il lancio di un prodotto o un evento di notizie internazionali.

## In che modo [!UICONTROL Allocazione automatica] può fornire ricavi più elevati? {#higher-revenue}

**[!UICONTROL Allocazione automatica]** trova il vincitore più rapidamente di una suddivisione A/B manuale e ti consente di sfruttarlo immediatamente, acquisendo ricavi al rialzo che sarebbero stati persi in un approccio tradizionale o manuale. **[!UICONTROL Allocazione automatica]** indirizza più traffico all&#39;esperienza con il tasso di conversione più alto, in modo da aumentare i ricavi mentre l&#39;attività viene eseguita e appresa.

Nell&#39;esempio seguente, **[!UICONTROL Allocazione automatica]** ha aumentato i ricavi durante il test inviando più traffico (40%) all&#39;esperienza D, che aveva il tasso di conversione più alto.

![L&#39;allocazione automatica fornisce un&#39;illustrazione dei ricavi più elevata](/help/main/c-activities/automated-traffic-allocation/assets/five-experiences.png)

## In quali casi devo attenermi all’allocazione manuale del traffico? {#manual-allocation}

Un test A/B manuale è l’opzione più applicabile quando è necessario ordinare in ordine crescente il modo in cui ogni esperienza è stata eseguita rispetto alle altre. **[!UICONTROL L&#39;allocazione automatica]** trova e sfrutta i migliori esecutori, ma non garantisce la differenziazione tra le esperienze con prestazioni inferiori. Utilizza l’allocazione manuale del traffico per controllare completamente la quantità di traffico del visitatore che vede ogni variante di test e per personalizzare le soglie statistiche rilevanti per la tua azienda.

## Introduzione {#get-started}

Sei pronto ad avviare la tua prima attività di **[!UICONTROL Allocazione automatica]**? Consulta [Creare un&#39;attività di allocazione automatica](/help/main/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md) e la [panoramica di allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md).
