---
keywords: Targeting esperienza;XT;metriche;impostazione metriche;metrica obiettivo;impostazioni attività;metrica di successo;conversione;entrate;ricavi;coinvolgimento
description: Scopri come specificare le metriche in un'attività  [!DNL Adobe Target] [!UICONTROL Experience Targeting] per determinare quando una visita ha esito positivo, ad esempio [!UICONTROL Conversion], [!UICONTROL Revenue] o [!UICONTROL Engagement].
title: Come si impostano le metriche obiettivo in un'attività [!UICONTROL Experience Targeting]?
feature: Experience Targeting
exl-id: 16249930-8b9c-441c-bd14-5f32332556d2
source-git-commit: d7c1bbbbc8d1dcc45ac09a09f6b3be01f7542384
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 56%

---

# Impostare le metriche nelle attività [!UICONTROL Experience Targeting] (XT)

Utilizzare le metriche in un&#39;attività [!DNL Adobe Target] [!UICONTROL Experience Targeting] (XT) per determinare quando una visita ha esito positivo.

Per informazioni dettagliate sulle metriche di successo, vedi [Metriche di successo](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).

1. Specifica l’obiettivo dell’attività.
1. Seleziona una [metrica di successo](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924)

   ![Selezionare una metrica di successo](/help/main/c-activities/t-experience-target/t-xt-create/assets/ab_metrics-new.png)

   Nella pagina [!UICONTROL Select Metrics] sono elencate le metriche di successo che è possibile scegliere per l&#39;attività. Le metriche di successo sono suddivise nelle seguenti categorie:

   * [!UICONTROL Conversion]
   * [!UICONTROL Revenue]
   * [!UICONTROL Engagement]

   Puoi utilizzare una qualsiasi delle metriche di successo predefinite, oppure puoi crearne una personalizzata. È inoltre possibile contrassegnare una metrica di successo come metrica principale. Le schede dei rapporti e di Experience Cloud per impostazione predefinita mostrano la metrica primaria, se è stata impostata.
1. Specifica le impostazioni per le metriche.

   Le impostazioni disponibili dipendono dalla metrica di successo in uso.

   Se attivato, il campo [!UICONTROL Estimated Value of the Conversion] (non disponibile per le metriche [!UICONTROL Page Score]) fornisce un valore per l&#39;obiettivo. Questo valore consente a [!DNL Target] di calcolare un incremento stimato dei ricavi. Questo campo è facoltativo; tuttavia, i ricavi incrementali per eventuali metriche non collegate ai ricavi non possono essere calcolate senza di esso. I dati sono di tipo valuta. Questo campo viene visualizzato progressivamente dopo che l’utente indica l’azione intrapresa per soddisfare l’obiettivo. Consulta [Stima dell’incremento dei ricavi](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md) per maggiori informazioni.

   La corretta configurazione delle metriche di successo è fondamentale per ottenere i dati previsti.

   Per ulteriori informazioni, vedi [Metriche di successo](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).

1. (Facoltativo) Aggiungi altre metriche.
1. Fare clic su **[!UICONTROL Continue]** al termine dell&#39;impostazione delle metriche.

Quando denomini o rinomini una metrica, i seguenti caratteri non sono consentiti:

| Carattere | Descrizione |
|--- |--- |
| `/` | Barra |
| `?` | Punto interrogativo |
| `#` | Cancelletto |
| `:` | Due punti |
| `=` | Uguale |
| `+` | Più |
| `-` | Meno |
| `@` | Chiocciola |

## Video di formazione: Metriche attività (7:43) ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video contiene informazioni su come utilizzare le metriche di successo.

* Le metriche per “Obiettivo”
* Comprendere e generare metriche [!UICONTROL Conversion], [!UICONTROL Revenue] e [!UICONTROL Engagement]
* Creazione di una metrica di tracciamento dei clic

>[!VIDEO](https://video.tv.adobe.com/v/17380)
