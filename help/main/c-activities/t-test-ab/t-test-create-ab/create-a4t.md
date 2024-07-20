---
keywords: Targeting;analytics;server di tracciamento;analytics for target;a4t
description: Scopri come configurare un'attività in [!DNL Adobe Target] per utilizzare [!DNL Adobe Analytics] come origine per la generazione di rapporti (A4T).
title: Come posso usare  [!DNL Analytics] dati in [!DNL Target]?
feature: Analytics for Target (A4T)
exl-id: 85605ff9-c09a-4a1a-9784-bdacda377e1d
source-git-commit: 8682c24cf1740171dd2ce1862b3bdce1e2082869
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 16%

---

# Utilizzo dei dati di [!DNL Adobe Analytics]

È possibile configurare un&#39;attività in [!DNL Adobe Target] per utilizzare [!DNL Adobe Analytics] come origine per la generazione di rapporti (A4T).

Per informazioni dettagliate sulla configurazione di [!DNL Analytics] come origine dati per [!DNL Target], vedere [Adobe Analytics come Source di reporting per Adobe Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

Prima di impostare un&#39;attività che utilizza [!DNL Analytics] come origine per la generazione di rapporti, stabilisci l&#39;obiettivo dell&#39;attività, ad esempio il miglioramento dei ricavi per visitatore (RPV) o l&#39;aumento dei clic sul carrello. Scegli una metrica di successo finale per l’attività. Sebbene sia possibile selezionare metriche aggiuntive in qualsiasi momento in [!DNL Analytics], è necessario specificare una particolare metrica che si prevede verrà influenzata dal test.

>[!NOTE]
>
>L&#39;opzione [!DNL Adobe Analytics] è disponibile se l&#39;account [!DNL Adobe Experience Cloud] è stato collegato sia a [!DNL Analytics] che a [!DNL Target], anche se l&#39;integrazione tra [!DNL Target] e [!DNL Analytics] non è stata impostata per l&#39;account.

Quando selezioni [!DNL Analytics] come origine per la generazione di rapporti per [!DNL Target], selezioni una suite di rapporti [!DNL Analytics] per ricevere i dati dell&#39;attività [!DNL Target]. Per specificare un&#39;origine per la generazione di rapporti, scegliere innanzitutto una delle [!DNL Analytics] società associate al proprio account, quindi selezionare la suite di rapporti appropriata per l&#39;attività. È possibile selezionare solo le suite di rapporti predisposte per la connessione a [!DNL Adobe Target]. Se la suite di rapporti prevista non è visibile, disconnettersi e accedere nuovamente a [!DNL Adobe Experience Cloud] per riprovare. Se la suite di rapporti non è ancora presente nell’elenco, contatta l’Assistenza clienti.

[!UICONTROL Analytics for Target] (A4T) richiede un server di tracciamento per riportare correttamente i risultati. Nel campo [!UICONTROL Tracking Server] viene visualizzato un server di tracciamento predefinito. Se utilizzi più server di tracciamento, assicurati di includere in questo campo il server di tracciamento corretto. Per ulteriori informazioni, vedere [Utilizzo di un server di tracciamento di Analytics](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823).

>[!NOTE]
>
>Se utilizzi [!DNL Adobe Analytics] come origine per la generazione di rapporti dell&#39;attività, non è necessario specificare un server di tracciamento durante la creazione dell&#39;attività se utilizzi at.js versione 0.9.1 (o successiva). La libreria at.js invia automaticamente i valori del server di tracciamento a [!DNL Target]. Durante la creazione dell&#39;attività, è possibile lasciare vuoto il campo [!UICONTROL Tracking Server] nella pagina [!UICONTROL Goals & Settings].

Durante l&#39;impostazione dell&#39;attività dopo aver impostato [!DNL Analytics] come origine per la generazione di rapporti, non è possibile impostare tipi di pubblico per la generazione dei rapporti. [!DNL Analytics] segmenti sono disponibili nel report [!DNL Target] [!UICONTROL Activities].

Devi selezionare una metrica di successo da utilizzare come obiettivo per ogni attività. L&#39;obiettivo è l&#39;attività di conversione che indica un&#39;attività di successo. È buona norma non eseguire mai un test senza un obiettivo da migliorare in modo specifico. Puoi scegliere qualsiasi metrica [!DNL Analytics] disponibile nel selettore delle metriche [!DNL Analytics].

L&#39;impostazione di un obiettivo non impedisce di utilizzare un&#39;altra metrica per valutare i risultati dei test. L&#39;obiettivo, comunque, funge da promemoria rispetto all&#39;elemento da migliorare con il test.

Quando un visitatore completa l&#39;obiettivo, non viene più incluso nell&#39;attività. Se il visitatore rientra nell’attività dopo aver completato un’attività, viene conteggiato come un nuovo visitatore.
