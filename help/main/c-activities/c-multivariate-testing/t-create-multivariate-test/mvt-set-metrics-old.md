---
keywords: multivariato;MVT;metriche;impostare metriche;metrica obiettivo;impostazioni attività;metrica di successo;conversione;ricavi;impegno
description: Scopri come specificare le metriche in un'attività  [!DNL Adobe Target] [!UICONTROL Multivariate Test] per determinare quando una visita ha esito positivo, ad esempio [!UICONTROL Conversion], [!UICONTROL Revenue] e [!UICONTROL Engagement].
title: Come si impostano le metriche obiettivo in un'attività [!UICONTROL Multivariate Test] (MVT)?
feature: Multivariate Tests
exl-id: 8530b3f1-5daa-4a03-a482-93b10eb23208
source-git-commit: 8f9c0ea65197fd639d463628e54db79db993c2da
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 60%

---

# Impostare le metriche per un&#39;attività [!UICONTROL Multivariate Test]

Utilizzare le metriche in un [!DNL Adobe Target] [!UICONTROL Multivariate Test] per determinare quando una visita ha esito positivo.

Per informazioni dettagliate sulle metriche di successo, vedi [Metriche di successo](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).

1. Specifica l’obiettivo dell’attività.
1. Seleziona una [metrica di successo](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924)

   ![Elenco per impostare le metriche](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt_metrics-list.png)

   Nella pagina [!UICONTROL Select Metrics] sono elencate le metriche di successo che è possibile scegliere per l&#39;attività. Le metriche di successo sono suddivise nelle seguenti categorie:

   * [!UICONTROL Conversion]
   * [!UICONTROL Revenue]
   * [!UICONTROL Engagement]

   È possibile utilizzare una qualsiasi delle metriche di successo predefinite, o crearne una personalizzata. È inoltre possibile contrassegnare una metrica di successo come metrica principale. Le schede dei rapporti e di Experience Cloud per impostazione predefinita mostrano la metrica primaria, se è stata impostata.

1. Specifica le impostazioni per le metriche.

   Le impostazioni disponibili dipendono dalla metrica di successo in uso.

   Se attivato, il campo [!UICONTROL Estimated Value of the Conversion] (non disponibile per le metriche [!UICONTROL Page Score]) fornisce un valore per l&#39;obiettivo. Questo valore consente a [!DNL Target] di calcolare un incremento stimato dei ricavi. Questo campo è facoltativo; tuttavia, i ricavi incrementali per eventuali metriche non collegate ai ricavi non possono essere calcolate senza di esso. I dati sono di tipo valuta. Questo campo viene visualizzato progressivamente dopo che l’utente indica l’azione intrapresa per soddisfare l’obiettivo. Consulta [Stima dell’incremento dei ricavi](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md) per maggiori informazioni.

   La corretta configurazione delle metriche di successo è fondamentale per ottenere i dati previsti.

   Per ulteriori informazioni, vedi [Metriche di successo](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924)

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
