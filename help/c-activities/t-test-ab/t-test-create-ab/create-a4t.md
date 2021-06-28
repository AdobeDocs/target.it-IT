---
keywords: Targeting;analytics;server di tracciamento;analytics for target;a4t
description: Scopri come configurare un’attività in Adobe [!DNL Target] to use Adobe Analytics as the reporting source. This integration is called Analytics for [!DNL Target] (A4T).
title: Come posso utilizzare i dati di Analytics in Target?
feature: Analytics for Target (A4T)
exl-id: 85605ff9-c09a-4a1a-9784-bdacda377e1d
source-git-commit: f028d2b439fee5c2a622748126bb0a34d550a395
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 80%

---

# Utilizzo dei dati di Analytics

Puoi configurare un’attività in [!DNL Adobe Target] per utilizzare [!DNL Adobe Analytics] come origine per la generazione di rapporti (A4T).

Per informazioni dettagliate sulla configurazione di Analytics come origine dati per Target, consulta [Adobe Analytics come origine per la generazione di rapporti per Adobe Target](/help/c-integrating-target-with-mac/a4t/a4t.md).

Prima di impostare un’attività che utilizza Analytics come origine per la generazione di rapporti, stabilisci l’obiettivo dell’attività, ad esempio il miglioramento dei ricavi per visitatore (RPV) o l’aumento dei clic sul carrello acquisti. Scegli una metrica finale di successo per la campagna. Anche se in Analytics puoi selezionare metriche aggiuntive in qualsiasi momento, è comunque necessario indicare una metrica specifica che si prevede verrà interessata dal test.

>[!NOTE]
>
>L’opzione Adobe Analytics è disponibile se hai collegato l’account Adobe Experience Cloud sia a Analytics che a Target, anche se l’integrazione tra Target e Analytics non è stata impostata per l’account.

Quando si seleziona Analytics come origine per la generazione di rapporti per Target, si seleziona la suite di rapporti di Analytics che dovrà ricevere i dati relativi all’attività di Target. Scegli innanzitutto una delle società Analytics associate al tuo account, quindi, seleziona la suite di rapporti idonea all’attività. Puoi selezionare solo le suite di rapporti impostate per la connessione ad Adobe Target. Se non visualizzi la suite di rapporti desiderata, disconnettiti, accedi di nuovo ad Adobe Experience Cloud e riprova. Se la suite di rapporti continua a non essere elencata, contatta l’Assistenza clienti.

Analytics for Target richiede un server di tracciamento per riportare correttamente i risultati. Un server di tracciamento predefinito verrà visualizzato nel campo Server di tracciamento. Se si utilizzano più server di tracciamento, è necessario verificare di aver inserito in questo campo quello corretto. Consulta [Utilizzo di un server di tracciamento di Analytics](/help/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) per ulteriori informazioni.

>[!NOTE]
>
>Se utilizzi Adobe Analytics come origine per la generazione di rapporti dell’attività, non è necessario specificare un server di tracciamento durante la creazione dell’attività se utilizzi at.js versione 0.9.1 (o successiva). La libreria at.js invia automaticamente i valori del server di tracciamento a [!DNL Target]. Durante la creazione di attività, puoi lasciare vuoto il campo [!UICONTROL Server di tracciamento] nella pagina [!UICONTROL Obiettivi e impostazioni].

Durante l&#39;impostazione di un&#39;attività dopo aver impostato Analytics come origine per la generazione di rapporti, non è possibile impostare tipi di pubblico per la generazione dei rapporti. I segmenti di Analytics sono disponibili nel rapporto Attività di Target.

È necessario selezionare una metrica di successo da utilizzare come obiettivo per ogni test. L&#39;obiettivo dell&#39;attività è l&#39;attività di conversione che indica una campagna di successo. È buona norma non eseguire mai un test senza un obiettivo da migliorare in modo specifico. È possibile scegliere qualsiasi metrica di Analytics disponibile nel selettore delle metriche di Analytics.

L&#39;impostazione di un obiettivo non impedisce di utilizzare un&#39;altra metrica per valutare i risultati dei test. L&#39;obiettivo, comunque, funge da promemoria rispetto all&#39;elemento da migliorare con il test.

Quando un visitatore completa l&#39;obiettivo, non è più incluso nella campagna. Se il visitatore viene incluso nuovamente nella campagna dopo aver completato un&#39;attività, sarà conteggiato come nuovo visitatore.
