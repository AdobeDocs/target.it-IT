---
keywords: Targeting;filtro pubblico;tipi di pubblico;filtro
description: Scopri come utilizzare i filtri del pubblico in [!DNL Adobe Target] per visualizzare i dati dei visitatori che condividono le stesse caratteristiche.
title: Posso usare i filtri pubblico per i rapporti?
feature: Audiences
exl-id: af8dae97-4b10-4edb-a0e6-0d8daf2f0d22
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 72%

---

# Filtri del pubblico per la generazione di rapporti

I filtri (o tipi di pubblico) di [!DNL Adobe Target] sono gruppi di visitatori che condividono una caratteristica specifica o un insieme di caratteristiche.

I filtri di pubblico sono utili per specificare i tipi di pubblico utilizzati per la creazione di rapporti. È possibile selezionare un pubblico e confrontarne le prestazioni con il traffico complessivo. Si vuole capire se i vincitori sono stati diversi per le varie fonti di traffico, rispetto al traffico generale. I filtri del pubblico consentono di individuare i tipi di pubblico che potrebbero essere indirizzati a contenuti diversi. In molti casi, un vincitore non è adatto per tutto il traffico.

Ad esempio, i visitatori che arrivano alla tua pagina da un determinato motore di ricerca potrebbero essere un pubblico. Altri tipi di pubblico potrebbero essere basati sul genere, sull&#39;età, sulla posizione, sullo stato di registrazione, sulla cronologia degli acquisti, o su qualsiasi altro dettaglio che si possono raccogliere sui visitatori. I filtri del pubblico permettono di dividere il traffico dei visitatori e confrontare le prestazioni dell&#39;esperienza per ogni segmento di traffico.

Quando si pianifica di utilizzare i filtri di pubblico per un&#39;attività, occorre prendere in considerazione le seguenti linee guida:

* **I visitatori possono trovarsi in più tipi di pubblico.** Se sono impostati due tipi di pubblico (ad esempio, &quot;nuovi visitatori&quot; e &quot;visitatori da Google&quot;) e una persona soddisfa entrambi i criteri, il visitatore viene conteggiato e tracciato in entrambi i tipi di pubblico. Di conseguenza, la somma dei visitatori nei tipi di pubblico non corrisponde al numero di visitatori in un&#39;attività.
* **Imposta i tipi di pubblico prima di avviare l&#39;attività.** I dati sui tipi di pubblico non possono essere recuperati retroattivamente. Se non si configurano i filtri pubblico prima di avviare l&#39;attività, per poi decidere di utilizzarli dopo l&#39;esecuzione dell&#39;attività per un po&#39; di tempo, non verranno raccolti i dati per l&#39;ora già passata.
* **Inizia con due o quattro gruppi di destinatari.** Concentrati sulle informazioni di base, ad esempio l&#39;origine del traffico.
* **Rinomina il pubblico come necessario.** È possibile rinominare un pubblico senza influire sui dati per rendere il nome del pubblico più significativo per i risultati raccolti, anche mentre l&#39;attività è attiva.
* **Immetti valori precisi.** I valori dei filtri dei tipi di pubblico sono sensibili all’uso di maiuscole e minuscole. Ad esempio, se si utilizza un pubblico che filtra sulle città, è necessario utilizzare una condizione “OR” per includere possibili variazioni di ortografia e maiuscolo, ad esempio “Vienna”, “vienna”, “wien” e “Wien”.
* **I tipi di pubblico creati dall&#39;elenco [!UICONTROL Audiences] possono essere riutilizzati.** I tipi di pubblico creati come parte di un&#39;attività non possono essere riutilizzati.

Nelle sezioni seguenti vengono fornite ulteriori informazioni sull&#39;impostazione e la creazione di rapporti sui tipi di pubblico:

| Attività | Argomento |
|--- |--- |
| Crea l&#39;attività o il test appropriati. | [Attività e test](/help/main/c-intro/target-key-concepts.md) |
| Crea i tipi di pubblico, se necessario. | [Creare un pubblico](/help/main/c-target/c-audiences/create-audience.md) |
| Se necessario, combina più tipi di pubblico. | [Combinare più tipi di pubblico](/help/main/c-target/combining-multiple-audiences.md) |
| Applica i tipi di pubblico alla pagina Obiettivi e impostazioni dell&#39;attività. | Test A/B: [Obiettivi e impostazioni](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md)<br>Automated Personalization: [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md)<br>Targeting esperienza: [Obiettivi e impostazioni](/help/main/c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md)<br>Test multivariato: [Obiettivi e impostazioni](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md)<br>Recommendations: [Impostazioni attività di Recommendations](/help/main/c-recommendations/t-create-recs-activity/recs-activity-settings.md)<br>Impostazioni attività: [Impostazioni attività](/help/main/c-activities/activity-settings.md) |
| Visualizza i rapporti con informazioni sui filtri dei tipi di pubblico. | [Impostazioni dei rapporti](/help/main/c-reports/c-report-settings/report-settings.md) |
