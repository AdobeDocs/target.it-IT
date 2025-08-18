---
keywords: Recommendations
description: Scopri i requisiti di implementazione per Analytics per  [!DNL Target]  (A4T) e cosa considerare prima di implementare questa integrazione.
title: Cosa Devo Sapere Prima Di Implementare A4T?
feature: Analytics for Target (A4T)
exl-id: 1c98b20b-4dd1-4011-b0cd-5096471af095
source-git-commit: 656f728ba890f1f5afc0404e22f6acb1a2565fe6
workflow-type: tm+mt
source-wordcount: '957'
ht-degree: 23%

---

# Prima di implementare Analytics for Target (A4T) con at.js

Diverse modifiche si verificano nel processo di raccolta dati quando si abilita [!DNL Adobe Analytics] come origine per la generazione di rapporti per [!DNL Adobe Target] (A4T).

Prima di decidere di utilizzare questa integrazione, esamina le sezioni seguenti e considera l’impatto sui processi di reporting.

>[!NOTE]
>
>Questo articolo si applica solo alle implementazioni di at.js. Per informazioni sull&#39;implementazione di [!UICONTROL Analytics for Target] (A4T) con [!DNL Adobe Experience Platform Web SDK], vedere [Registrazione di Adobe Analytics for Target (A4T) in Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/a4t/overview-a4t.html?lang=it){target=_blank}.

## Requisiti di implementazione {#section_A0D2EF18033D4C3997B08A6EBB34C17A}

>[!IMPORTANT]
>
>Prima di iniziare a utilizzare A4T, devi richiedere che il tuo account sia predisposto per l’integrazione. Utilizza il [Modulo di provisioning integrazioni Marketing Cloud](https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y){target=_blank} per richiedere il provisioning.

Questa integrazione A4T richiede l’implementazione delle seguenti versioni della libreria (o successive), a seconda che si desideri utilizzare o meno le offerte di reindirizzamento con A4T.

>[!NOTE]
>
>I seguenti requisiti elencano le *versioni minime* di at.js necessarie per implementare A4T. Il team [!DNL Target] gestisce solo due versioni di [!DNL at.js], ovvero la versione corrente e quella immediatamente precedente. Aggiorna [!DNL at.js] per assicurarti di eseguire una versione supportata. Per ulteriori informazioni su ogni versione, consulta [Dettagli sulla versione di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank}.

### Requisiti necessari se *non* si utilizzano offerte di reindirizzamento con A4T

Questa integrazione richiede l&#39;implementazione delle seguenti versioni della libreria (o successive) se non si prevede di utilizzare le offerte di reindirizzamento con A4T. L’ordine nell’elenco corrisponde all’ordine delle operazioni.

* [!DNL Experience Cloud Visitor ID Service]: visitorAPI.js versione 1.8.0
* [!DNL Adobe Target]: at.js versione 0.9.1
* Adobe Analytics: appMeasurement.js versione 1.7.0

Per informazioni sull&#39;implementazione di A4T con [!DNL Platform Web SDK], vedere [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=it){target=_blank}.

### Requisiti necessari se si utilizzano offerte di reindirizzamento con A4T

Per utilizzare le offerte di reindirizzamento con A4T, devi implementare le seguenti versioni della libreria (o successive). L’ordine nell’elenco corrisponde all’ordine delle operazioni.

* [!DNL Experience Cloud Visitor ID Service]: visitorAPI.js versione 2.3.0

  >[!NOTE]
  >
  >at.js 1.8.0+ e at.js 2.x+ non funzionano più con le versioni dell’API Visitor precedenti alla 2.5.0 per la trasmissione dei parametri di Adobe Audience Manager (AAM).

* [!DNL Adobe Target]: at.js versione 1.6.2

* Adobe Analytics: appMeasurement.js versione 2.1

Le istruzioni di download e distribuzione sono elencate in [Implementazione di Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md).

Per informazioni sull&#39;implementazione di A4T con [!DNL Platform Web SDK], vedere [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=it){target=_blank}.

## Aspetti da considerare prima dell’implementazione {#section_50D49CC52E11414089C89FB67F9B88F5}

* Questa integrazione è abilitata nelle nuove attività quando si seleziona l&#39;utilizzo di [!DNL Analytics] come origine per la generazione di rapporti. Dopo avere apportato le modifiche all&#39;implementazione descritte in questo documento, le attività esistenti non vengono influenzate.
* Il processo di configurazione di [!DNL Analytics] come origine per la generazione di rapporti per [!DNL Target] include diversi passaggi di implementazione, seguiti da un passaggio di provisioning. È opportuno rivedere l&#39;intero processo come descritto di seguito prima di procedere all&#39;implementazione. Dopo aver completato questi passaggi, sei pronto a utilizzare [!DNL Analytics] come origine per la generazione di rapporti quando sarà abilitato. Il processo di previsionamento può richiedere fino a cinque giorni lavorativi.
* [!DNL Visitor ID service] crea un [!DNL Visitor ID] condiviso in [!DNL Adobe Experience Cloud]. Anche se non sostituisce l&#39;ID mboxPC [!DNL Target] o l&#39;UUID [!DNL Audience Manager], sostituisce il modo in cui [!DNL Analytics] identifica i nuovi visitatori. Se configurato correttamente, anche i visitatori di ritorno [!DNL Analytics] devono essere identificati tramite il loro vecchio ID [!DNL Analytics]. Analogamente, poiché il mboxPCid [!DNL Target] rimane intatto, nessun dato del profilo visitatore [!DNL Target] viene perso quando si esegue l&#39;aggiornamento a [!DNL Visitor ID service].
* [!DNL Visitor ID service] deve essere eseguito prima del codice di pagina [!DNL Analytics] e [!DNL Target]. Assicurarsi che `VisitorAPI.js` venga visualizzato sopra i tag per tutte le altre soluzioni [!DNL Experience Cloud].

## Latenza {#section_9489BE6FD21641A4844E591711E3F813}

Dopo l&#39;abilitazione di questa integrazione, si verificherà una latenza aggiuntiva di 5-10 minuti in [!DNL Analytics]. Questo aumento di latenza consente di memorizzare i dati da [!DNL Analytics] e [!DNL Target] sullo stesso hit, consentendo di suddividere le attività per pagina e sezione del sito.

Questo aumento si riflette in tutti i servizi e gli strumenti di [!DNL Analytics], inclusi i rapporti in tempo reale e in tempo reale, e si applica nei seguenti scenari:

* Per lo streaming live, i rapporti in tempo reale e le richieste API e per i dati correnti per le variabili di traffico, vengono ritardati solo gli insiemi con ID di dati supplementari.
* Per i dati correnti sulle metriche di conversione, i dati finalizzati e i feed di dati, tutti gli hit subiscono un ritardo di 5-7 minuti.

L&#39;aumento della latenza inizia dopo l&#39;implementazione del servizio ID visitatore [!DNL Experience Cloud], anche se questa integrazione non è stata completamente implementata.

## ID supplementare {#section_2C1F745A2B7D41FE9E30915539226E3A}

Tutte le chiamate [!DNL Target] utilizzate da un&#39;attività A4T per inviare contenuto o registrare la metrica di obiettivo devono avere un hit [!DNL Analytics] corrispondente che condivida l&#39;ID supplementare affinché A4T funzioni correttamente.

Gli hit che contengono i dati di [!DNL Analytics] e [!DNL Target] contengono un ID dati supplementare. Questo ID è visibile nel [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html?lang=it) come parametro `sdid`. Ad esempio: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`. Questo ID viene generato in qualsiasi momento siano presenti i seguenti criteri:

* È implementato il servizio ID visitatore

Durante la [risoluzione dei problemi](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md), assicurati di confermare che l&#39;ID supplementare sia presente in [!DNL Analytics] hit.

## Registrazione Analytics lato client {#client-side}

Se at.js, [!DNL Experience Cloud Visitor ID Service] e appMeasurement.js si trovano nella pagina, [!DNL Analytics] e [!DNL Target] uniscono correttamente gli eventi a scopo di reporting e analisi, nel backend, purché l&#39;ID supplementare corretto sia incluso dalla pagina. Per il corretto funzionamento di A4T non è necessario gestire ed eseguire altre operazioni.

In alcuni casi potrebbe essere necessario avere maggiore controllo su quando e come inviare dati analitici relativi a [!DNL Target] a [!DNL Analytics] a scopo di reporting. Potresti avere uno strumento di analisi interno da utilizzare per scopi interni. Tuttavia, desideri anche inviare i dati di analisi a [!DNL Analytics] tramite il tuo prodotto di analisi interno in modo che altri membri della tua organizzazione possano continuare a utilizzare [!DNL Analytics] come origine per la generazione di rapporti visivi. Per ulteriori informazioni, consulta [Passaggio 7: Includere un riferimento a at.js in tutte le pagine del sito](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md#step7) in *Implementazione di Analytics for Target*.

## Pubblico condiviso

Durante la compilazione del [Modulo di provisioning integrazioni Marketing Cloud](https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y){target=_blank}, tieni presente le seguenti informazioni importanti relative all&#39;opzione [!UICONTROL Shared Audiences] elencata in &quot;[!UICONTROL For which capabilities are you requesting provisioning]?&quot;

![Modulo di richiesta](/help/main/c-integrating-target-with-mac/a4t/assets/request-form.png)

Quando si richiede [!UICONTROL Shared Audiences], si abilita [!UICONTROL Target] e [!UICONTROL Adobe Audience Manager] (AAM) per condividere informazioni, in questo caso audience.

>[!IMPORTANT]
>
>Questa integrazione tra [!UICONTROL Target] e AAM comporta costi aggiuntivi. Viene addebitata ogni chiamata [!UICONTROL Target] in AAM.
