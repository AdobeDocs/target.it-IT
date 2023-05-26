---
keywords: Recommendations
description: Scopri i requisiti di implementazione per Analytics per [!DNL Target] (A4T) e cosa considerare prima di implementare questa integrazione.
title: Cosa Devo Sapere Prima Di Implementare A4T?
feature: Analytics for Target (A4T)
exl-id: 1c98b20b-4dd1-4011-b0cd-5096471af095
source-git-commit: 2fc704a1779414a370ffd00ef5442fce36e7a5dd
workflow-type: tm+mt
source-wordcount: '988'
ht-degree: 30%

---

# Prima di implementare Analytics for Target (A4T) con at.js

Diverse modifiche si verificano nel processo di raccolta dei dati quando si abilita [!DNL Adobe Analytics] come origine di reporting per [!DNL Adobe Target] (A4T).

Prima di decidere di utilizzare questa integrazione, consulta le sezioni seguenti e considera l&#39;impatto sui processi di reporting.

>[!NOTE]
>
>Questo articolo si applica solo alle implementazioni di at.js.

## Requisiti di implementazione {#section_A0D2EF18033D4C3997B08A6EBB34C17A}

>[!IMPORTANT]
>
>Prima di iniziare a utilizzare A4T, devi richiedere che il tuo account sia predisposto per l’integrazione. Utilizza il [Modulo di provisioning integrazioni di Marketing Cloud](https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y){target=_blank} per richiedere il provisioning.

Questa integrazione A4T richiede l’implementazione delle seguenti versioni della libreria (o più recenti), a seconda che si desideri utilizzare o meno le offerte di reindirizzamento con A4T.

>[!NOTE]
>
>I seguenti requisiti elencano *minimo* versioni di at.js necessarie per implementare A4T. Il [!DNL Target] il team gestisce solo due versioni di [!DNL at.js]- la versione corrente e la seconda versione più recente. Aggiorna [!DNL at.js] per assicurarti di eseguire una versione supportata. Per ulteriori informazioni su ogni versione, consulta [Dettagli sulla versione di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}.

### Requisiti necessari se *non* si utilizzano offerte di reindirizzamento con A4T

Questa integrazione richiede l&#39;implementazione delle seguenti versioni della libreria (o successive) se non si prevede di utilizzare le offerte di reindirizzamento con A4T. L’ordine nell’elenco corrisponde all’ordine delle operazioni.

* [!DNL Experience Cloud Visitor ID Service]: visitorAPI.js versione 1.8.0
* [!DNL Adobe Target]: versione at.js 0.9.1
* Adobe Analytics: appMeasurement.js versione 1.7.0

Per informazioni sull’implementazione di A4T con [!DNL Platform Web SDK], vedi [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank}.

### Requisiti necessari se si utilizzano offerte di reindirizzamento con A4T

Per utilizzare le offerte di reindirizzamento con A4T, devi implementare le seguenti versioni della libreria (o successive). L’ordine nell’elenco corrisponde all’ordine delle operazioni.

* [!DNL Experience Cloud Visitor ID Service]: visitorAPI.js versione 2.3.0

   >[!NOTE]
   >
   >at.js 1.8.0+ e at.js 2.x+ non funzionano più con le versioni dell’API Visitor precedenti alla 2.5.0 per la trasmissione dei parametri di Adobe Audience Manager (AAM).

* [!DNL Adobe Target]: versione at.js 1.6.2

* Adobe Analytics: appMeasurement.js versione 2.1

Le istruzioni di download e distribuzione sono elencate in [Implementazione di Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md).

Per informazioni sull’implementazione di A4T con [!DNL Platform Web SDK], vedi [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank}.

## Aspetti da considerare prima dell’implementazione {#section_50D49CC52E11414089C89FB67F9B88F5}

* Questa integrazione è abilitata sulle nuove attività quando selezioni per utilizzare [!DNL Analytics] come origine per la generazione di rapporti. Dopo avere apportato le modifiche all&#39;implementazione descritte in questo documento, le attività esistenti non vengono influenzate.
* Il processo di impostazione [!DNL Analytics] come origine di reporting per [!DNL Target] include diversi passaggi di implementazione, seguiti da un passaggio di provisioning. È opportuno rivedere l&#39;intero processo come descritto di seguito prima di procedere all&#39;implementazione. Dopo aver completato questi passaggi, puoi utilizzare [!DNL Analytics] come origine per la generazione di rapporti quando è abilitata per te. Il processo di previsionamento può richiedere fino a cinque giorni lavorativi.
* Il [!DNL Visitor ID service] crea una condivisione [!DNL Visitor ID] in tutto [!DNL Adobe Experience Cloud]. Anche se non sostituisce il [!DNL Target] mboxPC id o [!DNL Audience Manager] UUID, sostituisce il metodo [!DNL Analytics] identifica nuovi visitatori. Se configurato correttamente, verrà restituito [!DNL Analytics] i visitatori devono essere identificati anche tramite il [!DNL Analytics] ID Analogamente, poiché [!DNL Target] mboxPCid rimane intatto, no [!DNL Target] i dati del profilo del visitatore vengono persi quando si esegue l&#39;aggiornamento a [!DNL Visitor ID service].
* Il [!DNL Visitor ID service] deve essere eseguito prima del [!DNL Analytics] e [!DNL Target] codice della pagina. Assicurati che `VisitorAPI.js` viene visualizzato sopra i tag per tutti gli altri [!DNL Experience Cloud] soluzioni.

## Latenza {#section_9489BE6FD21641A4844E591711E3F813}

Dopo l’abilitazione di questa integrazione, si verifica una latenza aggiuntiva di 5-10 minuti in [!DNL Analytics]. Questo aumento di latenza consente di [!DNL Analytics] e [!DNL Target] essere memorizzate sullo stesso hit, consentendoti di suddividere le attività per pagina e sezione del sito.

Questo aumento si riflette in tutti [!DNL Analytics] servizi e strumenti, tra cui la generazione di rapporti in tempo reale e in tempo reale, e si applica nei seguenti scenari:

* Per lo streaming live, i rapporti in tempo reale e le richieste API e per i dati correnti per le variabili di traffico, vengono ritardati solo gli insiemi con ID di dati supplementari.
* Per i dati correnti sulle metriche di conversione, i dati finalizzati e i feed di dati, tutti gli hit subiscono un ritardo di 5-7 minuti.

L&#39;aumento della latenza inizia dopo l&#39;implementazione di [!DNL Experience Cloud] servizio ID visitatore, anche se non hai implementato completamente questa integrazione.

## ID supplementare {#section_2C1F745A2B7D41FE9E30915539226E3A}

Tutti [!DNL Target] le chiamate utilizzate da un’attività A4T per consegnare contenuti o registrare che la metrica di obiettivo deve avere un valore [!DNL Analytics] hit che condivide l’ID supplementare affinché A4T funzioni correttamente.

Hit che contengono i dati di [!DNL Analytics] e [!DNL Target] contiene un ID dati supplementare. Puoi visualizzare questo ID in [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html) come `sdid` parametro. Ad esempio: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`. Questo ID viene generato in qualsiasi momento siano presenti i seguenti criteri:

* È implementato il servizio ID visitatore

Quando [risoluzione dei problemi](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md), assicurati di confermare che l’ID supplementare sia presente in [!DNL Analytics] hit.

## Registrazione Analytics lato client {#client-side}

Se at.js, il [!DNL Experience Cloud Visitor ID Service], e appMeasurement.js si trovano sulla pagina, [!DNL Analytics], e [!DNL Target] unisce correttamente gli eventi a scopo di reporting e analisi nel backend, purché l’ID supplementare corretto sia incluso dalla pagina. Per il corretto funzionamento di A4T non è necessario gestire ed eseguire altre operazioni.

In alcuni casi potrebbe essere necessario avere maggiore controllo su quando e come inviare dati analitici relativi a [!DNL Target] a [!DNL Analytics] a scopo di reporting. Potresti avere uno strumento di analisi interno da utilizzare per scopi interni. Tuttavia, desideri anche inviare i dati di analisi a [!DNL Analytics] tramite il prodotto di analisi interna, in modo che altri membri dell’organizzazione possano continuare a utilizzare [!DNL Analytics] come origine di reporting visiva. Consulta [Passaggio 7: Includere un riferimento a at.js in tutte le pagine del sito](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md#step7) in *Implementazione di Analytics for Target* per ulteriori informazioni.

## Pubblico condiviso

Durante la compilazione del [Modulo di provisioning integrazioni di Marketing Cloud](https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y){target=_blank}, siano a conoscenza delle seguenti informazioni importanti relative [!UICONTROL Pubblico condiviso] opzione elencata in &quot;[!UICONTROL Per quali funzionalità si richiede il provisioning]?&quot;

![Modulo di richiesta](/help/main/c-integrating-target-with-mac/a4t/assets/request-form.png)

Quando richiedi [!UICONTROL Pubblico condiviso], si attiva [!UICONTROL Target] e [!UICONTROL Adobe Audience Manager] (AAM) condividere informazioni, in questo caso audience.

>[!IMPORTANT]
>
>Questa integrazione tra [!UICONTROL Target] e l&#39;AAM comporta costi aggiuntivi. Viene addebitato per ogni [!UICONTROL Target] nell’AAM.
