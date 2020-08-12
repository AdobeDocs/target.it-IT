---
keywords: faq;frequently asked questions;analytics for target;a4T;activity setup
description: Questo argomento contiene le risposte alle domande più frequenti sulla configurazione delle attività e sull’utilizzo di Analytics come origine per la generazione di rapporti per Target (A4T).
title: Impostazioni delle attività - Domande frequenti su A4T
feature: null
topic: Standard
uuid: 3472ab3c-908b-40f8-81a6-512dccde64a6
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 89%

---


# Impostazioni delle attività - Domande frequenti su A4T{#activity-settings-a-t-faq}

Questo argomento contiene le risposte alle domande più frequenti sulla configurazione delle attività e sull’utilizzo di Analytics come origine per la generazione di rapporti per Target (A4T).

## Quali tipi di attività supportano Analytics come origine per la generazione di rapporti (A4T)? {#section_5E4F58CD25A5424E869E6FE0803968EF}

Per un elenco completo, consulta “Tipi di attività supportati” in [Adobe Analytics come origine per la generazione di rapporti per Adobe Target (A4T)](../../../c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE).

## Ho appena creato un’attività. Perché non vedo dati in arrivo? {#section_9F8092BE4225442896F926540292F221}

Quando viene creata un’attività, Target invia un file di classificazione ad Analytics. Sebbene Analytics acquisisca ed elabori i dati, questi non vengono visualizzati nei rapporti fino a quando il file di classificazione non sarà stato aggiornato. Questa operazione può richiedere fino a 24 ore. Se dopo 48 ore non vedi i tuoi dati, [contatta l’assistenza clienti](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C). In alternativa, se sai che lancerai un’attività, puoi crearla con qualche giorno di anticipo: le classificazioni vengono infatti inviate quando l’attività viene salvata. e in questo modo al momento dell’avvio i dati potranno essere visualizzati nei rapporti. Tieni presente che l’elaborazione dei dati da parte di Analytics richiede 45-90 minuti.

## Perché non è possibile selezionare Analytics come origine per la generazione di rapporti quando si crea una nuova attività? {#section_9F4F69C3085F4C2480AF439127EB27CD}

Puoi modificare le opzioni delle impostazioni di reporting in Amministrazione.

1. In Adobe Target, click **[!UICONTROL Administration]**.
1. Nell’elenco a discesa **[!UICONTROL Soluzione Experience Cloud utilizzata per i rapporti]**, fai clic su **[!UICONTROL Seleziona per attività]**.

![](assets/select-per-activity.png)

L’elenco a discesa **[!UICONTROL Origine per i rapporti]** è abilitato nella schermata **[!UICONTROL Obiettivi e impostazioni]** per la creazione e la modifica delle attività.

To always use Analytics as the reporting source, select **[!UICONTROL Adobe Analytics]** from the drop-down list in Administration.
