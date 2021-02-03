---
keywords: regole di inclusione;criteri di inclusione;raccomandazioni;promozione;promozioni;filtro dinamico;statico;filtro statico
description: Immettete manualmente uno o più valori statici per filtrare utilizzando le regole di inclusione in  Adobe Target Recommendations.
title: Filtrare Per Valori Statici Nelle Regole Di Inclusione In  Adobe Target Recommendations
feature: Recommendations
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 46%

---


# ![Filtro ](/help/assets/premium.png) PREMIUMStatic

Immettere manualmente uno o più valori statici da filtrare utilizzando le regole di inclusione in [!DNL Adobe Target] [!DNL Recommendations].

Ad esempio, si consiglia solo il contenuto con una valutazione MPA (Motion Picture Association) pari a &quot;G&quot; o &quot;PG&quot;.

È possibile creare tutte le regole di inclusione necessarie. Le regole di inclusione vengono collegate mediante un operatore E. Gli articoli verranno inclusi in un consiglio solo se vengono soddisfatte tutte le regole.

>[!NOTE]
>
>Se hai dimestichezza con la configurazione delle regole di inclusione prima della versione di Target 17.6.1 (giugno 2017), noterai che alcune delle opzioni e degli operatori sono cambiati. Vengono visualizzati solo gli operatori applicabili all’opzione selezionata; alcuni altri operatori sono stati rinominati (“corrisponde a” è ora “è uguale a”), per maggiore coerenza e intuitività. Tutte le regole di esclusione esistenti create prima di questa versione sono state automaticamente convertite nella nuova struttura. Non è necessaria alcuna modifica da parte dell’utente.

## Consiglia contenuto classificato G o PG

Per creare una regola di inclusione con valori statici per raccomandare il contenuto con una valutazione MPA di &quot;G&quot; o &quot;PG&quot; solo (escludendo il contenuto &quot;R&quot; e &quot;NC17&quot;), potete creare le seguenti regole di filtro &quot;movie-rating equals g-rating&quot; e &quot;movie-rating uguale pg-rating&quot;, come mostrato di seguito.

![esempio di valutazione dei filmati](/help/c-recommendations/c-algorithms/assets/movies.png)

