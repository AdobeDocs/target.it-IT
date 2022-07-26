---
keywords: FAQ;domande frequenti;analytics for target;a4t;configurazione delle attività
description: Trova le risposte alle domande sulla configurazione dell’attività durante l’utilizzo di Analytics per [!DNL Target] (A4T). A4T consente di utilizzare i rapporti di Analytics per [!DNL Target] attività.
title: Dove posso trovare le domande frequenti sulle impostazioni delle attività con A4T?
feature: Analytics for Target (A4T)
exl-id: 8a8cdbb9-89f6-4e4a-a53e-8f33adab4d61
source-git-commit: ed4fadc338bf5a1afad87e2b245a9b00e225b92c
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 16%

---

# Impostazioni delle attività - Domande frequenti su A4T

Questo argomento contiene le risposte alle domande più frequenti sulla configurazione delle attività e sull’utilizzo [!DNL Analytics] come origine per la generazione di rapporti per [!DNL Target] (A4T).

## Quali tipi di attività supportano Analytics come origine per la generazione di rapporti (A4T)? {#section_5E4F58CD25A5424E869E6FE0803968EF}

+++Risposta Per un elenco completo, consulta &quot;Tipi di attività supportati&quot; in [Adobe Analytics come origine per la generazione di rapporti per Adobe Target (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE).

+++

## Durante la configurazione delle metriche obiettivo, perché non posso accedere alle impostazioni avanzate?

+++Risposta per le attività che utilizzano [!DNL Analytics] come origine per la generazione di rapporti (A4T), la metrica di obiettivo utilizza il valore &quot;[!UICONTROL Incrementa il conteggio e mantieni l’utente nell’attività]&quot; e &quot;[!UICONTROL A ogni impression]&quot; impostazioni. Queste impostazioni sono *not* configurabile.

Per ulteriori informazioni, consulta &quot;Durante la configurazione delle metriche dell’obiettivo, perché non posso accedere alle opzioni Impostazioni avanzate?&quot; in [Definizioni delle metriche - Domande frequenti su A4T](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-metric-definition.md).

+++

## Ho appena creato un’attività. Perché non vedo dati in arrivo? {#section_9F8092BE4225442896F926540292F221}


+++Risposta Quando viene creata un’attività, [!DNL Target] invia un file di classificazione a [!DNL Analytics]. Nonostante [!DNL Analytics] acquisisce ed elabora i dati, non li mostra nei rapporti fino a quando il file di classificazione non è stato aggiornato. Questo processo può richiedere fino a 24 ore. Se dopo 48 ore non vedi i tuoi dati, [contatta l’assistenza clienti](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C). In alternativa, se sai di avviare un’attività, puoi crearla con qualche giorno di anticipo e le classificazioni vengono inviate quando l’attività viene salvata. e in questo modo al momento dell’avvio i dati potranno essere visualizzati nei rapporti. Si prega di notare che ci vogliono 45-90 minuti perché i dati vengano elaborati in [!DNL Analytics].

+++

## Perché non è possibile selezionare Analytics come origine per la generazione di rapporti quando si crea un’attività? {#section_9F4F69C3085F4C2480AF439127EB27CD}

+++Risposta È possibile modificare la [!UICONTROL Impostazioni reporting] opzioni in [!UICONTROL Amministrazione].

1. In [!DNL Target], fai clic su **[!UICONTROL Amministrazione]**.
1. Nell’elenco a discesa **[!UICONTROL Soluzione Experience Cloud utilizzata per i rapporti]**, fai clic su **[!UICONTROL Seleziona per attività]**.

![immagine select-per-activity](assets/select-per-activity.png)

L’elenco a discesa **[!UICONTROL Origine per i rapporti]** è abilitato nella schermata **[!UICONTROL Obiettivi e impostazioni]** per la creazione e la modifica delle attività.

Per utilizzare sempre [!DNL Analytics] come origine per la generazione di rapporti, seleziona **[!UICONTROL Adobe Analytics]** dall’elenco a discesa in [!UICONTROL Amministrazione].

+++

## Un visitatore può passare da un’esperienza con targeting a un’esperienza controllata in visite diverse in un’attività di Targeting automatico che utilizza A4T?

+++Risposta È vero quanto segue supponendo che l&#39;ID visitatore non cambi per un visitatore tra una visita e l&#39;altra.

Se la percentuale di allocazione del traffico viene regolata a metà attività, è possibile che un visitatore possa spostarsi tra le esperienze di targeting e di controllo.

Se le percentuali non vengono corrette a metà attività, un visitatore che inizialmente vede il controllo viene sempre inviato al controllo. Un visitatore inviato a esperienze con targeting viene sempre inviato a esperienze con targeting.

* Dopo essere stato nel &quot;bucket&quot; di traffico mirato, il visitatore può essere inviato a un’esperienza diversa da quella da visita per visitare se i modelli di apprendimento automatico determinano che una diversa esperienza è rilevante per la nuova visita.
* Dopo essere stato assegnato al &quot;bucket&quot; di traffico di controllo, un visitatore visualizzerà sempre la stessa esperienza perché l’assegnazione dell’esperienza è basata su un hash pseudo-casuale deterministico del visitorId del visitatore.

+++

## Posso usare un binomio? [!DNL Analytics] con un segmento applicato come obiettivo di ottimizzazione in un [!UICONTROL Allocazione automatica] attività? {#binomial}

+++Risposta Non è possibile utilizzare un [!DNL Analytics] con un segmento applicato come obiettivo di ottimizzazione in un [!UICONTROL Allocazione automatica] attività. Come soluzione alternativa è possibile definire un evento personalizzato che raggiunga lo stesso obiettivo e utilizzarlo come metrica di obiettivo di ottimizzazione.

+++