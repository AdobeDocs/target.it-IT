---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;static;static filter
description: Immettete manualmente uno o più valori statici per filtrare utilizzando le regole di inclusione in  Adobe Target Recommendations.
title: Filtrare per valori statici nelle regole di inclusione in  Adobe Target Recommendations
feature: criteria
translation-type: tm+mt
source-git-commit: b51c980d8e7db3ee574350a04f9056fe5b00a703
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 75%

---


# ![Filtro statico PREMIUM](/help/assets/premium.png)

Immettete manualmente uno o più valori statici per filtrare utilizzando le regole di inclusione in  Adobe Target Recommendations.

Ad esempio, per consigliare solo i contenuti con una classificazione MPAA di “G” o “PG”.

Operatori disponibili:

* è uguale a
* è diverso da
* contiene
* non contiene
* inizia con
* termina con
* è presente un valore
* il valore non è presente
* è maggiore o uguale a
* è minore o uguale a

>[!NOTE]
>
>Se hai dimestichezza con la configurazione delle regole di inclusione prima della versione di Target 17.6.1 (giugno 2017), noterai che alcune delle opzioni e degli operatori sono cambiati. Vengono visualizzati solo gli operatori applicabili all’opzione selezionata; alcuni altri operatori sono stati rinominati (“corrisponde a” è ora “è uguale a”), per maggiore coerenza e intuitività. Tutte le regole di esclusione esistenti create prima di questa versione sono state automaticamente convertite nella nuova struttura. Non è necessaria alcuna modifica da parte dell’utente.

È possibile creare tutte le regole di inclusione necessarie. Le regole di inclusione vengono collegate mediante un operatore E. Gli articoli verranno inclusi in un consiglio solo se vengono soddisfatte tutte le regole.