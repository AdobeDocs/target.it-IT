---
keywords: Targeting;analytics;tracking server
description: È possibile configurare un’attività in Target Standard per utilizzare Adobe Analytics come origine per la generazione di rapporti (A4T).
title: Utilizzo dei dati di Analytics
feature: a4t general
uuid: 4ac0c181-030b-4cf5-b138-acf02c7af4f6
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 95%

---


# Utilizzo dei dati di Analytics{#using-analytics-data}

È possibile configurare un’attività in Target Standard per utilizzare Adobe Analytics come origine per la generazione di rapporti (A4T).

For detailed information about setting up Analytics as the data source for Target, see [Adobe Analytics as the Reporting Source for Adobe Target](/help/c-integrating-target-with-mac/a4t/a4t.md).

Prima di impostare un’attività che utilizza Analytics come origine per la generazione di rapporti, stabilisci l’obiettivo dell’attività, ad esempio il miglioramento dei ricavi per visitatore (RPV) o l’aumento dei clic sul carrello acquisti. Scegli una metrica finale di successo per la campagna. Anche se in Analytics puoi selezionare metriche aggiuntive in qualsiasi momento, è comunque necessario indicare una metrica specifica che si prevede verrà interessata dal test.

>[!NOTE]
>
>L’opzione Adobe Analytics è disponibile se hai collegato l’account Adobe Experience Cloud sia a Analytics che a Target, anche se l’integrazione tra Target e Analytics non è stata impostata per l’account.

Quando si seleziona Analytics come origine per la generazione di rapporti per Target, si seleziona la suite di rapporti di Analytics che dovrà ricevere i dati relativi all’attività di Target. Scegli innanzitutto una delle società Analytics associate al tuo account, quindi, seleziona la suite di rapporti idonea all’attività. Puoi selezionare solo le suite di rapporti impostate per la connessione ad Adobe Target. Se non visualizzi la suite di rapporti desiderata, disconnettiti, accedi di nuovo ad Adobe Experience Cloud e riprova. Se la suite di rapporti continua a non essere elencata, contatta l’Assistenza clienti.

Analytics for Target richiede un server di tracciamento per riportare correttamente i risultati. Un server di tracciamento predefinito verrà visualizzato nel campo Server di tracciamento. Se si utilizzano più server di tracciamento, è necessario verificare di aver inserito in questo campo quello corretto. Consulta [Utilizzo di un server di tracciamento di Analytics](/help/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) per ulteriori informazioni.

>[!NOTE]
>
>Se utilizzi Adobe Analytics come origine per la generazione di rapporti dell’attività e la versione 61 (o successiva) di mbox.js o la versione 0.9.1 (o successiva) di at.js, non è necessario specificare un server di tracciamento durante la creazione di attività. La libreria mbox.js o at.js invia automaticamente i valori del server di tracciamento a [!DNL Target]. Durante la creazione di attività, puoi lasciare vuoto il campo [!UICONTROL Server di tracciamento] nella pagina [!UICONTROL Obiettivi e impostazioni].

Durante l&#39;impostazione di un&#39;attività dopo aver impostato Analytics come origine per la generazione di rapporti, non è possibile impostare tipi di pubblico per la generazione dei rapporti. I segmenti di Analytics sono disponibili nel rapporto Attività di Target.

È necessario selezionare una metrica di successo da utilizzare come obiettivo per ogni test. L&#39;obiettivo dell&#39;attività è l&#39;attività di conversione che indica una campagna di successo. È buona norma non eseguire mai un test senza un obiettivo da migliorare in modo specifico. È possibile scegliere qualsiasi metrica di Analytics disponibile nel selettore delle metriche di Analytics.

L&#39;impostazione di un obiettivo non impedisce di utilizzare un&#39;altra metrica per valutare i risultati dei test. L&#39;obiettivo, comunque, funge da promemoria rispetto all&#39;elemento da migliorare con il test.

Quando un visitatore completa l&#39;obiettivo, non è più incluso nella campagna. Se il visitatore viene incluso nuovamente nella campagna dopo aver completato un&#39;attività, sarà conteggiato come nuovo visitatore.
