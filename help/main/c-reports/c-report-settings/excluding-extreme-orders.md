---
keywords: Target;rapporti;impostazioni rapporti;ordini estremi;valori estremi
description: Scopri come escludere i valori estremi dai rapporti in Adobe [!DNL Target] in modo che alcuni ordini insoliti non influiscano sui risultati dell'attività.
title: Come posso escludere i valori estremi nei rapporti?
feature: Reports
exl-id: fd2d0c18-62c0-41e0-800c-b2ae123f0e74
TQID: https://experienceleague.adobe.com/yQtG4u-sLVJ66PezWW9ZgmY8ZuK177m-hLdQq-zlmfI
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 332
ht-degree: 62%

---

# Escludere i valori estremi

È possibile escludere i valori estremi dai rapporti in [!DNL Adobe Target] in modo che alcuni ordini insoliti non influiscano sui risultati dell&#39;attività. Un esempio di un ordine insolito potrebbe essere un allenatore che acquista le maglie per tutta la squadra, rispetto a singoli acquirenti che acquistano una sola maglia ciascuno.

>[!NOTE]
>
>Il flag [!UICONTROL Escludi valori estremi] si applica solo alle attività con [!UICONTROL Ricavi] e [!UICONTROL Coinvolgimento] tipi di metrica.

I valori estremi vengono contrassegnati automaticamente in base alle regole descritte di seguito. Puoi alternare la visualizzazione e l&#39;esclusione dei valori estremi dai rapporti. I estremi di un&#39;attività verranno esclusi, dopo per un&#39;ora di operatività o dopo 15 ordini, se tale condizione si verifica prima.

Un valore è considerato estremo se è superiore a +/-3 deviazioni standard dal valore medio dell&#39;ordine in base all&#39;ultimo mese di dati (fino al momento in cui è stato effettuato il calcolo).

Ad esempio, il filtro di valore estremo è spesso utile quando si utilizza RPV. RPV combina il tasso di conversione e il valore medio dell&#39;ordine e spesso espone la volatilità di tali metriche. Se utilizzi RPV e stabilisci che gli ordini non sembrano essere distribuiti normalmente, potresti osservare risultati più normali applicando il filtro di ordine estremo.

Quando un valore è contrassegnato come estremo, il valore dell&#39;ordine viene sostituito con il valore medio dell&#39;ordine dell&#39;esperienza per l&#39;ultimo mese, esclusi gli estremi. L&#39;ordine è inoltre contrassegnato come estremo nel rapporto [!UICONTROL Dettagli ordine] e nel file CSV scaricabile per i risultati giornalieri.

**Per escludere i valori estremi dai rapporti:**

1. Apri un&#39;attività che include i tipi di metrica [!UICONTROL Ricavi] o [!UICONTROL Coinvolgimento], quindi fai clic sulla scheda **[!UICONTROL Rapporti]**.
1. Fare clic sull&#39;icona Impostazioni report ( ![icona Impostazioni report](/help/main/assets/icons/Setting.svg) ) per visualizzare la finestra di dialogo **[!UICONTROL Impostazioni]**.

1. Far scorrere l&#39;opzione **[!UICONTROL Escludi valori estremi]** fino a quando non è attivata o disattivata, come desiderato.
1. Fai clic su **[!UICONTROL Salva]**.
