---
keywords: regole di inclusione;criteri di inclusione;consigli;promozione;promozioni;filtro dinamico;statico;filtro statico
description: Scopri come immettere manualmente uno o più valori statici da filtrare utilizzando le regole di inclusione in Adobe [!DNL Target] Recommendations.
title: Come Posso Filtrare Per Valori Statici Nelle Attività Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."
feature: Recommendations
hide: true
hidefromtoc: true
source-git-commit: b6a55260fd49e07e2b217f6becfbc778251a5d0d
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 45%

---

# [!UICONTROL Static Filter]

Immettere manualmente uno o più valori statici da filtrare utilizzando le regole di inclusione in [!DNL Adobe Target Recommendations].

Ad esempio, per consigliare solo i contenuti con classificazione Motion Picture Association (MPA) &quot;G&quot; o &quot;PG&quot;.

È possibile creare tutte le regole di inclusione necessarie. Le regole di inclusione vengono collegate mediante un operatore E. Gli articoli verranno inclusi in un consiglio solo se vengono soddisfatte tutte le regole.

>[!NOTE]
>
>Se hai dimestichezza con la configurazione delle regole di inclusione prima della versione di Target 17.6.1 (giugno 2017), noterai che alcune delle opzioni e degli operatori sono cambiati. Vengono visualizzati solo gli operatori applicabili all’opzione selezionata; alcuni altri operatori sono stati rinominati (“corrisponde a” è ora “è uguale a”), per maggiore coerenza e intuitività. Tutte le regole di esclusione esistenti create prima di questa versione sono state automaticamente convertite nella nuova struttura. Non è necessaria alcuna modifica da parte dell’utente.

## Consiglia contenuti classificati G o PG

Per creare una regola di inclusione con valori statici per consigliare contenuti con una classificazione MPA di solo &quot;G&quot; o &quot;PG&quot; (escludendo i contenuti &quot;R&quot; e &quot;NC17&quot;), puoi creare le seguenti regole di filtro: &quot;classificazione filmato è uguale a qualsiasi di g-nominale&quot; e &quot;classificazione filmato è uguale a qualsiasi di pg-nominale&quot;.
