---
keywords: regole di inclusione;criteri di inclusione;consigli;promozione;promozioni;filtro dinamico;statico;filtro statico
description: Scopri come immettere manualmente uno o più valori statici per filtrare utilizzando le regole di inclusione in Adobe [!DNL Target] Recommendations.
title: Come Posso Filtrare Per Valori Statici Nelle Attività Di Recommendations?
feature: Consigli
exl-id: 217e19bf-521f-4913-9b41-099c9af8b393
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 46%

---

# ![](/help/assets/premium.png) PREMIUMStatic Filter

Immetti manualmente uno o più valori statici da filtrare utilizzando le regole di inclusione in [!DNL Adobe Target] [!DNL Recommendations].

Ad esempio, per consigliare solo i contenuti con una classificazione Motion Picture Association (MPA) di &quot;G&quot; o &quot;PG&quot;.

È possibile creare tutte le regole di inclusione necessarie. Le regole di inclusione vengono collegate mediante un operatore E. Gli articoli verranno inclusi in un consiglio solo se vengono soddisfatte tutte le regole.

>[!NOTE]
>
>Se hai dimestichezza con la configurazione delle regole di inclusione prima della versione di Target 17.6.1 (giugno 2017), noterai che alcune delle opzioni e degli operatori sono cambiati. Vengono visualizzati solo gli operatori applicabili all’opzione selezionata; alcuni altri operatori sono stati rinominati (“corrisponde a” è ora “è uguale a”), per maggiore coerenza e intuitività. Tutte le regole di esclusione esistenti create prima di questa versione sono state automaticamente convertite nella nuova struttura. Non è necessaria alcuna modifica da parte dell’utente.

## Consiglia contenuto classificato G o PG

Per creare una regola di inclusione con valori statici per consigliare i contenuti con una classificazione MPA di solo &quot;G&quot; o &quot;PG&quot; (escludere i contenuti &quot;R&quot; e &quot;NC17&quot;), puoi creare le seguenti regole di filtro &quot;la classificazione dei film è uguale a g&quot; e &quot;la classificazione dei film è uguale a pg&quot;, come mostrato di seguito.

![esempio di valutazione dei film](/help/c-recommendations/c-algorithms/assets/movies.png)
