---
keywords: Targeting;analytics;server di tracciamento;analytics for target;a4t
description: Scopri come configurare un’attività in [!DNL Adobe Target] da utilizzare [!DNL Adobe Analytics] come origine per la generazione di rapporti (A4T)
title: Come posso utilizzare [!DNL Analytics] Ingresso dati [!DNL Target]?
feature: Analytics for Target (A4T)
exl-id: 85605ff9-c09a-4a1a-9784-bdacda377e1d
source-git-commit: 8682c24cf1740171dd2ce1862b3bdce1e2082869
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 19%

---

# Utilizzo di [!DNL Adobe Analytics] dati

Puoi configurare un’attività in [!DNL Adobe Target] da utilizzare [!DNL Adobe Analytics] come origine per la generazione di rapporti (A4T)

Per informazioni dettagliate sulla configurazione [!DNL Analytics] come origine di dati per [!DNL Target], vedi [Adobe Analytics come origine per la generazione di rapporti per Adobe Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

Prima di impostare un’attività che utilizza [!DNL Analytics] come origine per la generazione di rapporti, stabilisci l’obiettivo dell’attività, ad esempio il miglioramento dei ricavi per visitatore (RPV) o l’aumento dei clic sul carrello. Scegli una metrica di successo finale per l’attività. Anche se è possibile selezionare metriche aggiuntive in qualsiasi momento in [!DNL Analytics], è comunque necessario specificare una particolare metrica su cui si prevede che il test abbia effetto.

>[!NOTE]
>
>Il [!DNL Adobe Analytics] è disponibile se hai collegato il tuo [!DNL Adobe Experience Cloud] account con entrambi [!DNL Analytics] e [!DNL Target], anche se l&#39;integrazione tra [!DNL Target] e [!DNL Analytics] non è stato configurato per il tuo account.

Durante la selezione [!DNL Analytics] come origine di reporting per [!DNL Target], si seleziona un [!DNL Analytics] suite di rapporti da ricevere [!DNL Target] dati attività. Per specificare un&#39;origine per la generazione di rapporti, scegliere una delle opzioni [!DNL Analytics] aziende a cui è associato il tuo account, quindi seleziona la suite di rapporti appropriata per l’attività. Solo le suite di rapporti per le quali è stato eseguito il provisioning [!DNL Adobe Target] sono disponibili per la selezione. Se non trovi la suite di rapporti desiderata, disconnettiti e accedi di nuovo al [!DNL Adobe Experience Cloud] per riprovare. Se la suite di rapporti non è ancora presente nell’elenco, contatta l’Assistenza clienti.

[!UICONTROL Analytics for Target] (A4T) richiede un server di tracciamento per riportare correttamente i risultati. Un server di tracciamento predefinito viene visualizzato in [!UICONTROL Server di tracciamento] campo. Se utilizzi più server di tracciamento, assicurati di includere in questo campo il server di tracciamento corretto. Consulta [Utilizzo di un server di tracciamento di Analytics](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) per ulteriori informazioni.

>[!NOTE]
>
>Se usa [!DNL Adobe Analytics] come origine per la generazione di rapporti dell’attività, non è necessario specificare un server di tracciamento durante la creazione di attività se si utilizza at.js versione 0.9.1 (o successiva). La libreria at.js invia automaticamente i valori del server di tracciamento a [!DNL Target]. Durante la creazione di attività, puoi lasciare vuoto il campo [!UICONTROL Server di monitoraggio] nella pagina [!UICONTROL Obiettivi e impostazioni].

Durante l’impostazione di un’attività dopo l’impostazione [!DNL Analytics] come origine per la generazione di rapporti, non è possibile impostare tipi di pubblico per la generazione dei rapporti. [!DNL Analytics] i segmenti sono disponibili nel [!DNL Target] [!UICONTROL Attività] rapporto.

Devi selezionare una metrica di successo da utilizzare come obiettivo per ogni attività. L&#39;obiettivo è l&#39;attività di conversione che indica un&#39;attività di successo. È buona norma non eseguire mai un test senza un obiettivo da migliorare in modo specifico. Puoi scegliere qualsiasi [!DNL Analytics] metrica disponibile nella [!DNL Analytics] selettore delle metriche.

L&#39;impostazione di un obiettivo non impedisce di utilizzare un&#39;altra metrica per valutare i risultati dei test. L&#39;obiettivo, comunque, funge da promemoria rispetto all&#39;elemento da migliorare con il test.

Quando un visitatore completa l&#39;obiettivo, non viene più incluso nell&#39;attività. Se il visitatore rientra nell’attività dopo aver completato un’attività, viene conteggiato come un nuovo visitatore.
