---
keywords: faq;frequently asked questions;analytics for target;a4T;activity setup
description: Questo argomento contiene le risposte alle domande più frequenti sulla configurazione delle attività e sull’utilizzo di Analytics come origine per la generazione di rapporti per Target (A4T).
title: Impostazioni delle attività - Domande frequenti su A4T
feature: a4t troubleshooting
translation-type: tm+mt
source-git-commit: a12eea60aa3e66cdb54ab284fa3f942be4d56178
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 36%

---


# Impostazioni delle attività - Domande frequenti su A4T

This topic contains answers to questions that are frequently asked about activity setup and using [!DNL Analytics] as the reporting source for [!DNL Target] (A4T).

## Quali tipi di attività supportano Analytics come origine per la generazione di rapporti (A4T)? {#section_5E4F58CD25A5424E869E6FE0803968EF}

Per un elenco completo, consulta “Tipi di attività supportati” in [Adobe Analytics come origine per la generazione di rapporti per Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE).

## Durante la configurazione delle metriche obiettivo, perché non è possibile accedere alle impostazioni avanzate?

Per le attività che utilizzano [!DNL Analytics] come origine di reporting (A4T), la metrica obiettivo utilizzerà sempre le impostazioni &quot;[!UICONTROL Increment Count &amp; Keep User in Activity]&quot; (Conteggio incrementi e Mantieni utente in attività[!UICONTROL ) e &quot;]On Every Impression&quot; (Su ogni impressione). Questo *non* è configurabile.

Per ulteriori informazioni, vedere &quot;Durante la configurazione delle metriche degli obiettivi, perché non è possibile accedere alle opzioni delle impostazioni avanzate?&quot; in [Metric definitions - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-metric-definition.md).

## Ho appena creato un’attività. Perché non vedo dati in arrivo? {#section_9F8092BE4225442896F926540292F221}

When an activity is created, [!DNL Target] sends a classification file to [!DNL Analytics]. Although [!DNL Analytics] is capturing the and processing the data, it does not show in the reports until the classification file has been updated. Questa operazione può richiedere fino a 24 ore. Se dopo 48 ore non vedi i tuoi dati, [contatta l’assistenza clienti](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C). In alternativa, se sai che lancerai un’attività, puoi crearla con qualche giorno di anticipo: le classificazioni vengono infatti inviate quando l’attività viene salvata. e in questo modo al momento dell’avvio i dati potranno essere visualizzati nei rapporti. Please note that it takes 45-90 minutes for data to be processed in [!DNL Analytics].

## Perché non è possibile selezionare Analytics come origine per la generazione di rapporti quando si crea una nuova attività? {#section_9F4F69C3085F4C2480AF439127EB27CD}

You can change your [!UICONTROL Reporting Settings] options in [!UICONTROL Administration].

1. In [!DNL Target], fate clic su **[!UICONTROL Amministrazione]**.
1. Nell’elenco a discesa **[!UICONTROL Soluzione Experience Cloud utilizzata per i rapporti]**, fai clic su **[!UICONTROL Seleziona per attività]**.

![](assets/select-per-activity.png)

L’elenco a discesa **[!UICONTROL Origine per i rapporti]** è abilitato nella schermata **[!UICONTROL Obiettivi e impostazioni]** per la creazione e la modifica delle attività.

To always use [!DNL Analytics] as the reporting source, select **[!UICONTROL Adobe Analytics]** from the drop-down list in [!UICONTROL Administration].

## Un visitatore può passare da esperienze con targeting a esperienze controllate in visite diverse in un&#39;attività di targeting automatico che utilizza A4T?

Quanto segue è vero se l’ID visitatore non cambia per un visitatore tra una visita e l’altra.

Se la percentuale di allocazione del traffico viene modificata in base all&#39;attività media, è possibile che un visitatore si sposti tra esperienze con targeting e esperienze di controllo.

Se le percentuali non vengono modificate a livello di attività, un visitatore che inizialmente vede il controllo verrà sempre inviato a tale controllo. Un visitatore che viene inviato a esperienze con targeting sarà sempre inviato a esperienze con targeting.

* Dopo essere stato nel &quot;bucket&quot; di traffico di destinazione, il visitatore può essere inviato a un&#39;esperienza diversa da visita a visita se i modelli di machine-learning determinano che una diversa esperienza è rilevante per la nuova visita.
* Dopo essere stato assegnato al &quot;bucket&quot; di controllo del traffico, un visitatore visualizzerà sempre la stessa esperienza perché l&#39;assegnazione dell&#39;esperienza è basata su un hash pseudo-casuale deterministico del visitorId.
