---
description: I filtri del pubblico (o tipi di pubblico) sono gruppi di visitatori che condividono una caratteristica specifica o un insieme di caratteristiche.
keywords: Targeting;filtro di pubblico;tipi di pubblico;filter
seo-description: I filtri dell'audience in Adobe Target (o audience) sono gruppi di visitatori che condividono una caratteristica specifica o un insieme di caratteristiche.
seo-title: Audience filters for reporting in Adobe Target
solution: Target
title: Filtri del pubblico per la generazione di rapporti
uuid: ca2632c0-87e4-4a85-95e6-e63cf800ab2f
translation-type: tm+mt
source-git-commit: 8ec84183de4c5a7c2a7a1f30e0196cd021ce937f

---


# Filtri del pubblico per i rapporti{#audience-filters-for-reporting}

I filtri del pubblico (o tipi di pubblico) sono gruppi di visitatori che condividono una caratteristica specifica o un insieme di caratteristiche.

I filtri di pubblico sono utili per specificare i tipi di pubblico utilizzati per la creazione di rapporti. È possibile selezionare un pubblico e confrontarne le prestazioni con il traffico complessivo. Si vuole capire se i vincitori sono stati diversi per le varie fonti di traffico, rispetto al traffico generale. Questo aiuta a scoprire i tipi di pubblico che a cui si dovrebbero rivolgere contenuti diversi. In molti casi, un vincitore non è adatto per tutto il traffico.

Ad esempio, i visitatori che arrivano alla tua pagina da un determinato motore di ricerca potrebbero essere un pubblico. Altri tipi di pubblico potrebbero essere basati sul genere, sull'età, sulla posizione, sullo stato di registrazione, sulla cronologia degli acquisti, o su qualsiasi altro dettaglio che si possono raccogliere sui visitatori. I filtri del pubblico permettono di dividere il traffico dei visitatori e confrontare le prestazioni dell'esperienza per ogni segmento di traffico.

Quando si pianifica di utilizzare i filtri di pubblico per un'attività, occorre prendere in considerazione le seguenti linee guida:

* **I visitatori possono trovarsi in più tipi di pubblico.** If there are two audiences set up (for example, "new visitors" and "visitors from Google"), and a person meets both criteria, then this visitor is counted and tracked in both audiences. Di conseguenza, la somma dei visitatori nei tipi di pubblico non corrisponde al numero di visitatori in un'attività.
* **Set up audiences before launching the activity.** I dati sui tipi di pubblico non possono essere recuperati retroattivamente. Se non si configurano i filtri pubblico prima di avviare l'attività, per poi decidere di utilizzarli dopo l'esecuzione dell'attività per un po' di tempo, non verranno raccolti i dati per l'ora già passata.
* **Inizia con due o quattro gruppi di destinatari.** Concentrati sulle informazioni di base, ad esempio l'origine del traffico.
* **Rinomina il pubblico come necessario.** È possibile rinominare un pubblico senza influire sui dati per rendere il nome del pubblico più significativo per i risultati raccolti, anche mentre l'attività è attiva.
* **Immetti valori precisi.** I valori dei filtri dei tipi di pubblico sono sensibili all’uso di maiuscole e minuscole. Ad esempio, se si utilizza un pubblico che filtra sulle città, è necessario utilizzare una condizione “OR” per includere possibili variazioni di ortografia e maiuscolo, ad esempio “Vienna”, “vienna”, “wien” e “Wien”.
* **I tipi di pubblico creati dall'elenco Tipi di pubblico possono essere sono riutilizzati.** I tipi di pubblico creati come parte di un'attività non possono essere riutilizzati.

Nelle sezioni seguenti vengono fornite ulteriori informazioni sull'impostazione e la creazione di rapporti sui tipi di pubblico:

| Attività | Argomento |
|--- |--- |
| Crea l'attività o il test appropriati. | [Attività e test](/help/c-intro/target-key-concepts.md) |
| Crea i tipi di pubblico, se necessario. | [Creare un pubblico](/help/c-target/c-audiences/create-audience.md) |
| Se necessario, combina più tipi di pubblico. | [Combinare più tipi di pubblico](/help/c-target/combining-multiple-audiences.md) |
| Applica i tipi di pubblico alla pagina Obiettivi e impostazioni dell'attività. | A/B Test: [Goals and Settings](/help/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md)<br>Automated Personalization:  [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md)<br>Experience Targeting: [Goals and Settings](/help/c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md)<br>Multivariate Test:  [Goals and Settings](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md)<br>Recommendations: [Recommendations activity settings](/help/c-recommendations/t-create-recs-activity/recs-activity-settings.md)<br>Activity Settings: [Activity Settings](/help/c-activities/activity-settings.md) |
| Visualizza i rapporti con informazioni sui filtri dei tipi di pubblico. | [Impostazioni dei rapporti](/help/c-reports/c-report-settings/report-settings.md) |

