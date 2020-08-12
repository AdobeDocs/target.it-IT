---
keywords: Target;reports;report settings;extreme orders;extreme values
description: Potete escludere valori estremi dall'influenza dei rapporti in  Adobe Target, in modo che alcuni ordini insoliti non influenzino i risultati dell'attività. Un esempio di un ordine insolito potrebbe essere un allenatore che acquista le maglie per tutta la squadra, rispetto a singoli acquirenti che acquistano una sola maglia ciascuno.
title: Escludere valori estremi nei report  Adobe Target
feature: null
uuid: bb151b54-09ef-40b5-bc04-95c61b761f5a
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 88%

---


# Escludere i valori estremi{#exclude-extreme-values}

Puoi escludere i valori estremi dai rapporti in modo che pochi ordini insoliti non influiscano sui risultati dell’attività. Un esempio di un ordine insolito potrebbe essere un allenatore che acquista le maglie per tutta la squadra, rispetto a singoli acquirenti che acquistano una sola maglia ciascuno.

>[!NOTE]
>
>Il flag [!UICONTROL Escludi valori estremi] si applica solo alle attività con tipi di metrica di ricavi e coinvolgimento.

I valori estremi vengono contrassegnati automaticamente in base alle regole descritte di seguito. Puoi alternare la visualizzazione e l&#39;esclusione dei valori estremi dai rapporti. I estremi di un&#39;attività verranno esclusi, dopo per un&#39;ora di operatività o dopo 15 ordini, se tale condizione si verifica prima.

Un valore è considerato estremo se è superiore a +/-3 deviazioni standard dal valore medio dell&#39;ordine in base all&#39;ultimo mese di dati (fino al momento in cui è stato effettuato il calcolo).

Ad esempio, il filtro di valore estremo è spesso utile quando si utilizza RPV. RPV combina il tasso di conversione e il valore medio dell&#39;ordine e spesso espone la volatilità di tali metriche. Se utilizzi RPV e stabilisci che gli ordini non sembrano essere distribuiti normalmente, potresti osservare risultati più normali applicando il filtro di ordine estremo.

Quando un valore è contrassegnato come estremo, il valore dell&#39;ordine viene sostituito con il valore medio dell&#39;ordine dell&#39;esperienza per l&#39;ultimo mese, esclusi gli estremi. L&#39;ordine è inoltre contrassegnato come estremo nel rapporto dettagli ordine e nel file CSV scaricabile per i risultati giornalieri.

**Per escludere i valori estremi dai rapporti:**

1. Apri un’attività che include i tipi di metrica di ricavi o coinvolgimento, quindi fai clic sulla scheda **[!UICONTROL Rapporti]**.
1. Fate clic sull’icona dell’ingranaggio.

   ![Impostazioni dei rapporti](/help/c-reports/c-report-settings/assets/report-settings-gear-icon.png)

   Viene visualizzata la finestra di dialogo Impostazioni  rapporto.

   ![Risultato passaggio](assets/exclude_extreme_values.png)

1. Attiva o disattiva l’opzione **[!UICONTROL Escludi valori estremi]** a tuo piacimento.
1. Fai clic su **[!UICONTROL Salva]**.
