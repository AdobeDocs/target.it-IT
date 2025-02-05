---
keywords: Target;rapporti;impostazioni rapporti;ordini estremi;valori estremi
description: Scopri come escludere i valori estremi dai rapporti in Adobe [!DNL Target] in modo che alcuni ordini insoliti non influiscano sui risultati dell'attività.
title: Come posso escludere i valori estremi nei rapporti?
feature: Reports
exl-id: fd2d0c18-62c0-41e0-800c-b2ae123f0e74
source-git-commit: c1a71d1fb6fa9b5c14e22fa3199358a4594bb4a1
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 64%

---

# Escludere i valori estremi

È possibile escludere i valori estremi dai rapporti in [!DNL Adobe Target] in modo che alcuni ordini insoliti non influiscano sui risultati dell&#39;attività. Un esempio di un ordine insolito potrebbe essere un allenatore che acquista le maglie per tutta la squadra, rispetto a singoli acquirenti che acquistano una sola maglia ciascuno.

>[!NOTE]
>
>Il flag [!UICONTROL Exclude Extreme Values] si applica solo alle attività con [!UICONTROL Revenue] e [!UICONTROL Engagement] tipi di metrica.

I valori estremi vengono contrassegnati automaticamente in base alle regole descritte di seguito. Puoi alternare la visualizzazione e l&#39;esclusione dei valori estremi dai rapporti. I estremi di un&#39;attività verranno esclusi, dopo per un&#39;ora di operatività o dopo 15 ordini, se tale condizione si verifica prima.

Un valore è considerato estremo se è superiore a +/-3 deviazioni standard dal valore medio dell&#39;ordine in base all&#39;ultimo mese di dati (fino al momento in cui è stato effettuato il calcolo).

Ad esempio, il filtro di valore estremo è spesso utile quando si utilizza RPV. RPV combina il tasso di conversione e il valore medio dell&#39;ordine e spesso espone la volatilità di tali metriche. Se utilizzi RPV e stabilisci che gli ordini non sembrano essere distribuiti normalmente, potresti osservare risultati più normali applicando il filtro di ordine estremo.

Quando un valore è contrassegnato come estremo, il valore dell&#39;ordine viene sostituito con il valore medio dell&#39;ordine dell&#39;esperienza per l&#39;ultimo mese, esclusi gli estremi. L&#39;ordine è inoltre contrassegnato come estremo nel rapporto [!UICONTROL Order Details] e nel file CSV scaricabile per i risultati giornalieri.

**Per escludere i valori estremi dai rapporti:**

1. Apri un&#39;attività che include [!UICONTROL Revenue] o [!UICONTROL Engagement] tipi di metrica, quindi fai clic sulla scheda **[!UICONTROL Reports]**.
1. Fare clic sull&#39;icona Impostazioni report ( ![icona Impostazioni report](/help/main/assets/icons/Setting.svg) ) per visualizzare la finestra di dialogo **[!UICONTROL Settings]**.

1. Far scorrere l&#39;interruttore **[!UICONTROL Exclude Extreme Values]** in posizione &quot;on&quot; o &quot;off&quot;, come desiderato.
1. Fare clic su **[!UICONTROL Save]**.
