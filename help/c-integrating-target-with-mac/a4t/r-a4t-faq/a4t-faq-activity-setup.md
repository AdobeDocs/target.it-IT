---
keywords: FAQ;domande frequenti;analytics for target;a4t;configurazione delle attività
description: Trova le risposte alle domande sulla configurazione delle attività durante l’utilizzo di Analytics for Target (A4T). A4T consente di utilizzare i rapporti di Analytics per le attività di Target.
title: Dove posso trovare le domande frequenti sulle impostazioni delle attività con A4T?
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: e45f0d2d2370f9c7aba2c2bd26afdd4c0e401db8
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 22%

---


# Impostazioni delle attività - Domande frequenti su A4T

Questo argomento contiene le risposte alle domande più frequenti sulla configurazione delle attività e sull’utilizzo di [!DNL Analytics] come origine per la generazione di rapporti per [!DNL Target] (A4T).

## Quali tipi di attività supportano Analytics come origine per la generazione di rapporti (A4T)? {#section_5E4F58CD25A5424E869E6FE0803968EF}

Per un elenco completo, consulta “Tipi di attività supportati” in [Adobe Analytics come origine per la generazione di rapporti per Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE).

## Durante la configurazione delle metriche obiettivo, perché non posso accedere alle impostazioni avanzate?

Per le attività che utilizzano [!DNL Analytics] come origine per la generazione di rapporti (A4T), la metrica obiettivo utilizza le impostazioni &quot;[!UICONTROL Incrementa il conteggio e mantieni l’utente in attività]&quot; e &quot;[!UICONTROL Su ogni impression]&quot;. Queste impostazioni sono *non* configurabili.

Per ulteriori informazioni, consulta &quot;Durante la configurazione delle metriche dell’obiettivo, perché non posso accedere alle opzioni Impostazioni avanzate?&quot; in [Definizioni delle metriche - Domande frequenti su A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-metric-definition.md).

## Ho appena creato un’attività. Perché non vedo dati in arrivo? {#section_9F8092BE4225442896F926540292F221}

Quando viene creata un&#39;attività, [!DNL Target] invia un file di classificazione a [!DNL Analytics]. Anche se [!DNL Analytics] acquisisce ed elabora i dati, nei rapporti questo non viene visualizzato finché il file di classificazione non viene aggiornato. Questo processo può richiedere fino a 24 ore. Se dopo 48 ore non vedi i tuoi dati, [contatta l’assistenza clienti](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C). In alternativa, se sai che lancerai un’attività, puoi crearla con qualche giorno di anticipo e le classificazioni vengono inviate quando l’attività viene salvata. e in questo modo al momento dell’avvio i dati potranno essere visualizzati nei rapporti. Tieni presente che l’elaborazione dei dati in [!DNL Analytics] richiede 45-90 minuti.

## Perché non è possibile selezionare Analytics come origine per la generazione di rapporti quando si crea un’attività? {#section_9F4F69C3085F4C2480AF439127EB27CD}

Puoi modificare le opzioni [!UICONTROL Impostazioni reporting] in [!UICONTROL Amministrazione].

1. In [!DNL Target], fai clic su **[!UICONTROL Amministrazione]**.
1. Nell’elenco a discesa **[!UICONTROL Soluzione Experience Cloud utilizzata per i rapporti]**, fai clic su **[!UICONTROL Seleziona per attività]**.

![](assets/select-per-activity.png)

L’elenco a discesa **[!UICONTROL Origine per i rapporti]** è abilitato nella schermata **[!UICONTROL Obiettivi e impostazioni]** per la creazione e la modifica delle attività.

Per utilizzare sempre [!DNL Analytics] come origine per la generazione di rapporti, seleziona **[!UICONTROL Adobe Analytics]** dall’elenco a discesa in [!UICONTROL Amministrazione].

## Un visitatore può passare da un’esperienza con targeting a un’esperienza controllata in visite diverse in un’attività di Targeting automatico che utilizza A4T?

Di seguito è true supponendo che visitorId non cambi per un visitatore tra una visita e l&#39;altra.

Se la percentuale di allocazione del traffico viene regolata a metà attività, è possibile che un visitatore possa spostarsi tra le esperienze di targeting e quelle di controllo.

Se le percentuali non vengono corrette a metà attività, un visitatore che inizialmente vede il controllo viene sempre inviato al controllo. Un visitatore inviato a esperienze con targeting viene sempre inviato a esperienze con targeting.

* Dopo essere stato nel &quot;bucket&quot; di traffico mirato, il visitatore può essere inviato a un’esperienza diversa da quella da visita per visitare se i modelli di apprendimento automatico determinano che una diversa esperienza è rilevante per la nuova visita.
* Dopo essere stato assegnato al &quot;bucket&quot; di traffico di controllo, un visitatore visualizzerà sempre la stessa esperienza perché l’assegnazione dell’esperienza è basata su un hash pseudo-casuale deterministico del visitorId del visitatore.
