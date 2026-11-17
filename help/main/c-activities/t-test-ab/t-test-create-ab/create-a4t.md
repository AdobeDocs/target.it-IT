---
keywords: Targeting;analytics;server di tracciamento;analytics for target;a4t
description: Scopri come configurare un'attività in [!DNL Adobe Target] per utilizzare [!DNL Adobe Analytics] come origine per la generazione di rapporti (A4T).
title: Come posso usare i dati di [!DNL Analytics] in [!DNL Target]?
feature: Analytics for Target (A4T)
exl-id: 85605ff9-c09a-4a1a-9784-bdacda377e1d
TQID: 'https://experienceleague.adobe.com/x38YsYI4a6-92oOr6Fs3RfKrJHbSaLNj0cki5CInPPg'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: 891742a5-242d-5099-966a-ca76c17cd2d2
    internal-label: Analytics for Target (A4T)
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 4876228feee28031373f7e0abe62a66b05b15274
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%
---
# Utilizzo dei dati di [!DNL Adobe Analytics] {#create-a4t}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come configurare un&#39;attività per utilizzare [!DNL Adobe Analytics] come origine per la generazione di rapporti (A4T), cosa preparare prima di iniziare e come scegliere l&#39;obiettivo dell&#39;attività.

>[!ENDSHADEBOX]

Analytics for Target (A4T) misura i risultati di un&#39;attività [!DNL Adobe Target] con i dati e le metriche di [!DNL Adobe Analytics]. Per utilizzare A4T, configura l&#39;attività in modo che [!DNL Analytics] sia la sua origine per la generazione di rapporti. Per informazioni dettagliate sulla configurazione di [!DNL Analytics] come origine dati per [!DNL Target], vedere [Adobe Analytics come Source di reporting per Adobe Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

## Prima di iniziare {#before-you-begin}

>[!NOTE]
>
>L&#39;opzione **[!UICONTROL Adobe Analytics]** è disponibile quando l&#39;account [!DNL Adobe Experience Cloud] è collegato sia a [!DNL Analytics] che a [!DNL Target], anche se l&#39;integrazione tra [!DNL Target] e [!DNL Analytics] non è stata impostata per l&#39;account.

Prima di creare l’attività, stabilisci il relativo obiettivo, ad esempio il miglioramento dei ricavi per visitatore (RPV) o l’aumento dei clic sul carrello. Quindi scegli la metrica di successo finale che misura questo obiettivo. È possibile selezionare metriche aggiuntive in [!DNL Analytics] in qualsiasi momento, ma è comunque necessario specificare l&#39;unica metrica su cui si prevede di influenzare il test.

## Seleziona Analytics come origine per la generazione rapporti {#select-reporting-source}

>[!NOTE]
>
>Se si utilizza at.js versione 0.9.1 o successiva, non è necessario specificare un server di tracciamento quando si crea un&#39;attività che utilizza [!DNL Adobe Analytics] come origine per la generazione di rapporti. La libreria at.js invia automaticamente i valori del server di tracciamento a [!DNL Target]. Il campo **[!UICONTROL Server di monitoraggio]** nella pagina **[!UICONTROL Obiettivi e impostazioni]** può rimanere vuoto.

L&#39;origine per la generazione di rapporti è selezionata nella pagina **[!UICONTROL Obiettivi e impostazioni]** dell&#39;attività. In questa pagina è possibile scegliere una società [!DNL Analytics] e la suite di rapporti che riceve i dati dell&#39;attività [!DNL Target] e verificare il server di tracciamento.

➡️ Per i passaggi, i requisiti della suite di rapporti e i dettagli del server di tracciamento, vedere [Reporting di Source](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#reporting-source).

Quando [!DNL Analytics] è l&#39;origine per la generazione di rapporti, l&#39;attività non offre un&#39;opzione per impostare i tipi di pubblico per la generazione dei rapporti. [!DNL Analytics] segmenti sono disponibili nel report [!DNL Target] **[!UICONTROL Attività]**.

## Imposta l’obiettivo dell’attività {#set-goal}

Ogni attività richiede una metrica di successo come obiettivo. L’obiettivo è l’attività di conversione che segnala un’attività di successo. È possibile utilizzare qualsiasi metrica disponibile nel selettore di metriche [!DNL Analytics]. È consigliabile non eseguire mai un test senza un obiettivo di miglioramento in un modo specifico.

L’impostazione di un obiettivo non impedisce l’utilizzo di altre metriche per valutare i risultati del test. L’obiettivo, tuttavia, identifica l’unica cosa che desideri migliorare con il test.

Quando un visitatore completa l&#39;obiettivo, non viene più incluso nell&#39;attività. Se il visitatore accede nuovamente all’attività dopo averla completata, viene conteggiato come un nuovo visitatore.
