---
keywords: FAQ;domande frequenti;analytics for target;a4t;configurazione delle attività
description: Risposte alle domande sulla configurazione delle attività quando si utilizza Analytics per [!DNL Target] (A4T). A4T consente di utilizzare il reporting di Analytics per [!DNL Target] attività.
title: Dove posso trovare domande frequenti sulle impostazioni delle attività con A4T?
feature: Analytics for Target (A4T)
exl-id: 8a8cdbb9-89f6-4e4a-a53e-8f33adab4d61
source-git-commit: 52dd26acfce77da0eea14be572708c069ba5e9ba
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 14%

---

# Impostazioni delle attività - Domande frequenti su A4T

Questo argomento contiene le risposte alle domande più frequenti sulla configurazione e l’utilizzo delle attività [!DNL Analytics] come origine di reporting per [!DNL Target] (A4T).

## Quali tipi di attività supportano Analytics come origine per la generazione di rapporti (A4T)? {#section_5E4F58CD25A5424E869E6FE0803968EF}

+++Risposta Per un elenco completo, vedi &quot;Tipi di attività supportati&quot; in [Adobe Analytics come origine per la generazione di rapporti per Adobe Target (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE).

+++

## Perché non posso accedere alle impostazioni avanzate durante la configurazione delle metriche obiettivo?

+++Risposta per le attività che utilizzano [!DNL Analytics] come origine per la generazione di rapporti (A4T), la metrica di obiettivo utilizza il codice &quot;[!UICONTROL Incrementa il conteggio e mantieni l&#39;utente attivo]&quot; e &quot;[!UICONTROL A ogni impression]&quot;. Queste impostazioni sono *non* configurabile.

Per ulteriori informazioni, consulta &quot;Perché non posso accedere alle opzioni Impostazioni avanzate durante la configurazione delle metriche dell’obiettivo?&quot; in [Definizioni delle metriche - Domande frequenti su A4T](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-metric-definition.md).

+++

## Ho appena creato un’attività. Perché non vedo dati in arrivo? {#section_9F8092BE4225442896F926540292F221}


+++Risposta alla creazione di un&#39;attività, [!DNL Target] invia un file di classificazione a [!DNL Analytics]. Anche se [!DNL Analytics] : durante l’acquisizione e l’elaborazione dei dati, nei rapporti non viene visualizzato questo messaggio fino a quando il file di classificazione non viene aggiornato. Questo processo può richiedere da 24 a 72 ore. Se dopo 72 ore i dati non vengono visualizzati, [contatta l’Assistenza clienti](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C). In alternativa, se sai di avviare un’attività, puoi crearla con qualche giorno di anticipo e le classificazioni vengono inviate quando l’attività viene salvata. e in questo modo al momento dell’avvio i dati potranno essere visualizzati nei rapporti. L’elaborazione dei dati in richiede 45-90 minuti [!DNL Analytics].

+++

## Perché non è possibile selezionare Analytics come origine per la generazione di rapporti quando si crea un&#39;attività? {#section_9F4F69C3085F4C2480AF439127EB27CD}

+++Risposta È possibile modificare [!UICONTROL Impostazioni di reporting] opzioni in [!UICONTROL Amministrazione].

1. In entrata [!DNL Target], fai clic su **[!UICONTROL Amministrazione]**.
1. Nell’elenco a discesa **[!UICONTROL Soluzione Experience Cloud utilizzata per i rapporti]**, fai clic su **[!UICONTROL Seleziona per attività]**.

![immagine di selezione per attività](assets/select-per-activity.png)

L’elenco a discesa **[!UICONTROL Origine per i rapporti]** è abilitato nella schermata **[!UICONTROL Obiettivi e impostazioni]** per la creazione e la modifica delle attività.

Da utilizzare sempre [!DNL Analytics] come origine per la generazione di rapporti, seleziona **[!UICONTROL Adobe Analytics]** dall’elenco a discesa in [!UICONTROL Amministrazione].

+++

## Un visitatore può passare da un’esperienza con targeting a un’esperienza controllata in visite diverse in un’attività di Targeting automatico che utilizza A4T?

+++Risposta: quanto segue è vero supponendo che l’ID visitatore non cambi per un visitatore tra una visita e l’altra.

Se la percentuale di allocazione del traffico viene regolata a metà attività, è possibile che un visitatore possa passare da un’esperienza con targeting a un’esperienza di controllo.

Se le percentuali non vengono modificate nel corso dell’attività intermedia, il visitatore che inizialmente vede il controllo viene sempre inviato al controllo. Un visitatore inviato a esperienze con targeting viene sempre inviato a esperienze con targeting.

* Dopo essere stato nel &quot;bucket&quot; di traffico mirato, il visitatore può essere inviato a un’esperienza diversa da visita a visita se i modelli di apprendimento automatico determinano che un’esperienza diversa è rilevante per la nuova visita.
* Dopo essere stato assegnato al &quot;bucket&quot; di controllo del traffico, un visitatore vedrà sempre la stessa esperienza perché l’assegnazione dell’esperienza è basata su un hash pseudo-casuale deterministico dell’ID visitatore.

+++

## Posso usare un binomio? [!DNL Analytics] metrica con un segmento applicato come obiettivo di ottimizzazione in un [!UICONTROL Allocazione automatica] attività? {#binomial}

+++Risposta Non è possibile utilizzare un [!DNL Analytics] metrica con un segmento applicato come obiettivo di ottimizzazione in un [!UICONTROL Allocazione automatica] attività. Come soluzione alternativa puoi definire un evento personalizzato che raggiunge lo stesso obiettivo e utilizzarlo come metrica di obiettivo di ottimizzazione.

+++