---
keywords: Consigli
description: Scopri i requisiti di implementazione per Analytics for [!DNL Target] (A4T) e cosa considerare prima di implementare questa integrazione.
title: Cosa Devo Sapere Prima Di Implementare A4T?
feature: Analytics for Target (A4T)
exl-id: 1c98b20b-4dd1-4011-b0cd-5096471af095
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 34%

---

# Prima dell’implementazione

Diverse modifiche si verificano nel processo di raccolta dei dati quando si abilita [!DNL Adobe Analytics] come origine per la generazione di rapporti per [!DNL Adobe Target] (A4T).

Prima di decidere di utilizzare questa integrazione, consulta le sezioni seguenti e considera l&#39;impatto sui processi di reporting:

## Requisiti di implementazione {#section_A0D2EF18033D4C3997B08A6EBB34C17A}

>[!IMPORTANT]
>
>Prima di poter iniziare a utilizzare A4T, è necessario richiedere il provisioning dell’account per l’integrazione. Utilizza il [modulo di provisioning integrazioni di Marketing Cloud](https://www.adobe.com/go/audiences) per richiedere il provisioning.

Questa integrazione A4T richiede l’implementazione delle seguenti versioni della libreria (o più recenti), a seconda che si desideri utilizzare o meno le offerte di reindirizzamento con A4T:

### Requisiti necessari se *non* si utilizzano offerte di reindirizzamento con A4T

Questa integrazione richiede l&#39;implementazione delle seguenti versioni della libreria (o successive) se non si prevede di utilizzare le offerte di reindirizzamento con A4T. L’ordine nell’elenco corrisponde all’ordine delle operazioni.

* [!DNL Experience Cloud Visitor ID Service]: visitorAPI.js versione 1.8.0
* [!DNL Adobe Target] (a seconda dell&#39;implementazione): at.js versione 0.9.1 o mbox.js versione 61
* Adobe Analytics: appMeasurement.js versione 1.7.0

### Requisiti necessari se si utilizzano offerte di reindirizzamento con A4T

Per utilizzare le offerte di reindirizzamento con A4T, devi implementare le seguenti versioni della libreria (o successive). L’ordine nell’elenco corrisponde all’ordine delle operazioni.

* [!DNL Experience Cloud Visitor ID Service]: visitorAPI.js versione 2.3.0
* [!DNL Adobe Target]: at.js versione 1.6.2

   **Nota:** la libreria mbox.js non supporta le offerte di reindirizzamento con A4T. L’implementazione deve utilizzare at.js.

* Adobe Analytics: appMeasurement.js versione 2.1

Le istruzioni di download e distribuzione sono elencate in [Implementazione di Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4timplementation.md).

## Aspetti da considerare prima dell’implementazione {#section_50D49CC52E11414089C89FB67F9B88F5}

* Questa integrazione è abilitata sulle nuove attività quando selezioni di utilizzare [!DNL Analytics] come origine per la generazione di rapporti. Dopo avere apportato le modifiche all&#39;implementazione descritte in questo documento, le attività esistenti non vengono influenzate.
* Il processo di configurazione di [!DNL Analytics] come origine per la generazione di rapporti per [!DNL Target] include diverse fasi di implementazione, seguite da una fase di provisioning. È opportuno rivedere l&#39;intero processo come descritto di seguito prima di procedere all&#39;implementazione. Dopo aver completato questi passaggi, puoi utilizzare [!DNL Analytics] come origine per la generazione di rapporti quando è abilitata. Il processo di previsionamento può richiedere fino a cinque giorni lavorativi.
* Il [!DNL Visitor ID service] crea un [!DNL Visitor ID] condiviso in [!DNL Adobe Experience Cloud]. Sebbene non sostituisca l’ [!DNL Target] mboxPC id o [!DNL Audience Manager] UUID, sostituisce il modo in cui [!DNL Analytics] identifica i nuovi visitatori. Se impostato correttamente, anche i visitatori di ritorno [!DNL Analytics] devono essere identificati tramite il loro vecchio [!DNL Analytics] ID. Allo stesso modo, poiché il [!DNL Target] mboxPCid rimane intatto, nessun dato di profilo visitatore [!DNL Target] viene perso quando si esegue l&#39;aggiornamento a [!DNL Visitor ID service].
* Il codice di pagina [!DNL Visitor ID service] deve essere eseguito prima del codice di pagina [!DNL Analytics] e [!DNL Target]. Assicurati che `VisitorAPI.js` sia visualizzato sopra i tag per tutte le altre soluzioni [!DNL Experience Cloud].

## Latenza {#section_9489BE6FD21641A4844E591711E3F813}

Dopo l’abilitazione di questa integrazione, si verifica una latenza supplementare di 5-10 minuti in [!DNL Analytics]. Questo aumento della latenza consente la memorizzazione dei dati di [!DNL Analytics] e [!DNL Target] sullo stesso hit, consentendo di suddividere le attività per pagina e sezione del sito.

Questo aumento si riflette in tutti i servizi e gli strumenti [!DNL Analytics], inclusi i rapporti in tempo reale e in tempo reale, e si applica nei seguenti scenari:

* Per lo streaming live, i rapporti in tempo reale e le richieste API e per i dati correnti per le variabili di traffico, vengono ritardati solo gli insiemi con ID di dati supplementari.
* Per i dati correnti sulle metriche di conversione, i dati finalizzati e i feed di dati, tutti gli hit vengono ritardati di 5-7 minuti in più.

L&#39;aumento della latenza inizia dopo l&#39;implementazione del servizio ID visitatore [!DNL Experience Cloud], anche se questa integrazione non è stata completamente implementata.

## ID supplementare {#section_2C1F745A2B7D41FE9E30915539226E3A}

Tutte le chiamate [!DNL Target] utilizzate da un’attività A4T per consegnare il contenuto o registrare la metrica di obiettivo devono avere un hit corrispondente [!DNL Analytics] che condivide l’ID supplementare per A4T per funzionare correttamente.

Gli hit che contengono dati di [!DNL Analytics] e [!DNL Target] contengono un ID di dati supplementare. Puoi visualizzare questo ID in [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html) come parametro `sdid`. Ad esempio: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`. Questo ID viene generato in qualsiasi momento siano presenti i seguenti criteri:

* È implementato il servizio ID visitatore
* È implementata una versione di [!DNL mbox.js] che supporta questa integrazione.

Quando [si risolve il problema](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md), assicurati di confermare che l&#39;ID supplementare sia presente negli hit [!DNL Analytics].

## Registrazione Analytics lato client {#client-side}

Se at.js, i valori [!DNL Experience Cloud Visitor ID Service] e appMeasurement.js si trovano nella pagina, [!DNL Analytics] e [!DNL Target] uniscono correttamente gli eventi a scopo di reporting e analisi nel backend, purché l’ID supplementare corretto sia incluso dalla pagina. Non è necessario gestire ed eseguire altre operazioni affinché A4T funzioni correttamente.

In alcuni casi potrebbe essere utile avere maggiore controllo su quando e come inviare dati analitici relativi a [!DNL Target] a [!DNL Analytics] a scopo di reporting. È possibile che tu disponga di uno strumento di analisi interno che utilizzi per scopi interni. Tuttavia, desideri anche inviare i dati di analisi a [!DNL Analytics] tramite il prodotto di analisi aziendale in modo che altri membri dell’organizzazione possano continuare a utilizzare [!DNL Analytics] come origine di reporting visiva. Per ulteriori informazioni, consulta [Passaggio 7: Includere un riferimento a at.js o mbox.js in tutte le pagine del sito](/help/c-integrating-target-with-mac/a4t/a4timplementation.md#step7) nella sezione *Implementazione di Analytics for Target*.

## Pubblico condiviso

Durante la compilazione del [modulo di provisioning integrazioni di Marketing Cloud](https://www.adobe.com/go/audiences), tieni presente le seguenti informazioni importanti relative all&#39;opzione [!UICONTROL Pubblico condiviso] elencata in &quot;[!UICONTROL Per quali funzionalità stai richiedendo il provisioning]?&quot;

![Modulo di richiesta](/help/c-integrating-target-with-mac/a4t/assets/request-form.png)

Quando richiedi [!UICONTROL Tipi di pubblico condivisi], abilita [!UICONTROL Target] e [!UICONTROL Adobe Audience Manager] (AAM) per condividere informazioni, in questo caso tipi di pubblico.

>[!IMPORTANT]
>
>Questa integrazione tra [!UICONTROL Target] e AAM comporta costi aggiuntivi. Sei fatturato per ogni chiamata [!UICONTROL Target] in AAM.
