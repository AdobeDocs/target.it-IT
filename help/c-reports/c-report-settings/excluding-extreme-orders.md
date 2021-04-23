---
keywords: Target;rapporti;impostazioni rapporti;ordini estremi;valori estremi
description: Scopri come escludere i valori estremi dall’influenzare i rapporti in Adobe [!DNL Target] in modo che alcuni ordini insoliti non influiscano sui risultati dell’attività.
title: Come si escludono i valori estremi nei rapporti?
feature: Rapporti
exl-id: fd2d0c18-62c0-41e0-800c-b2ae123f0e74
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 72%

---

# Escludere i valori estremi

È possibile escludere valori estremi dall’influenzare i rapporti in [!DNL Adobe Target] in modo che alcuni ordini insoliti non influiscano sui risultati dell’attività. Un esempio di un ordine insolito potrebbe essere un allenatore che acquista le maglie per tutta la squadra, rispetto a singoli acquirenti che acquistano una sola maglia ciascuno.

>[!NOTE]
>
>Il flag [!UICONTROL Escludi valori estremi] si applica solo alle attività con tipi di metrica di ricavi e coinvolgimento.

I valori estremi vengono contrassegnati automaticamente in base alle regole descritte di seguito. Puoi alternare la visualizzazione e l&#39;esclusione dei valori estremi dai rapporti. I estremi di un&#39;attività verranno esclusi, dopo per un&#39;ora di operatività o dopo 15 ordini, se tale condizione si verifica prima.

Un valore è considerato estremo se è superiore a +/-3 deviazioni standard dal valore medio dell&#39;ordine in base all&#39;ultimo mese di dati (fino al momento in cui è stato effettuato il calcolo).

Ad esempio, il filtro di valore estremo è spesso utile quando si utilizza RPV. RPV combina il tasso di conversione e il valore medio dell&#39;ordine e spesso espone la volatilità di tali metriche. Se utilizzi RPV e stabilisci che gli ordini non sembrano essere distribuiti normalmente, potresti osservare risultati più normali applicando il filtro di ordine estremo.

Quando un valore è contrassegnato come estremo, il valore dell&#39;ordine viene sostituito con il valore medio dell&#39;ordine dell&#39;esperienza per l&#39;ultimo mese, esclusi gli estremi. L’ordine è inoltre contrassegnato come estremo nel rapporto [!UICONTROL Dettagli ordine] e nel download CSV per i risultati giornalieri.

**Per escludere i valori estremi dai rapporti:**

1. Apri un’attività che include i tipi di metrica di ricavi o coinvolgimento, quindi fai clic sulla scheda **[!UICONTROL Rapporti]**.
1. Fai clic sull&#39;icona a forma di ingranaggio per visualizzare la finestra di dialogo **[!UICONTROL Impostazioni]** .

   ![Risultato passaggio](assets/exclude_extreme_values.png)

1. Fai scorrere l&#39;interruttore **[!UICONTROL Escludi valori estremi]** nella posizione &quot;on&quot; o &quot;off&quot;, come desiderato.
1. Fai clic su **[!UICONTROL Salva]**.
