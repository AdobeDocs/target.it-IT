---
keywords: multivariato;MVT;metriche;impostare metriche;metrica obiettivo;impostazioni attività;metrica di successo;conversione;ricavi;coinvolgimento
description: Scopri come specificare le metriche in un'attività  [!DNL Adobe Target] [!UICONTROL Test multivariato] per determinare quando una visita ha esito positivo, ad esempio [!UICONTROL Conversione], [!UICONTROL Ricavi] e [!UICONTROL Coinvolgimento].
title: Come si impostano le metriche obiettivo in un'attività [!UICONTROL Test multivariato] (MVT)?
feature: Multivariate Tests
exl-id: 8530b3f1-5daa-4a03-a482-93b10eb23208
TQID: https://experienceleague.adobe.com/iJntBcXy4QNgEq0SnzLpqMX6S5HQ6kBy4PMoQivlVxw
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 353
ht-degree: 56%

---

# Impostare le metriche per un&#39;attività [!UICONTROL Test multivariato]

Utilizzare le metriche in un [!DNL Adobe Target] [!UICONTROL Test multivariato] per determinare quando una visita ha esito positivo.

Per informazioni dettagliate sulle metriche di successo, vedi [Metriche di successo](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).

1. Specifica l’obiettivo dell’attività.
1. Seleziona una [metrica di successo](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924)

   ![Elenco per impostare le metriche](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt_metrics-list-new.png)

   Nella pagina [!UICONTROL Seleziona metriche] sono elencate le metriche di successo che è possibile scegliere per l&#39;attività. Le metriche di successo sono suddivise nelle seguenti categorie:

   * [!UICONTROL Conversione]
   * [!UICONTROL Ricavi]
   * [!UICONTROL Coinvolgimento]

   È possibile utilizzare una qualsiasi delle metriche di successo predefinite, o crearne una personalizzata. È inoltre possibile contrassegnare una metrica di successo come metrica principale. Le schede dei rapporti e di Experience Cloud per impostazione predefinita mostrano la metrica primaria, se è stata impostata.

1. Specifica le impostazioni per le metriche.

   Le impostazioni disponibili dipendono dalla metrica di successo in uso.

   Se attivato, il campo [!UICONTROL Valore stimato della conversione] (non disponibile per le metriche [!UICONTROL Punteggio di pagina]) fornisce un valore per l&#39;obiettivo. Questo valore consente a [!DNL Target] di calcolare un incremento stimato dei ricavi. Questo campo è facoltativo; tuttavia, i ricavi incrementali per eventuali metriche non collegate ai ricavi non possono essere calcolate senza di esso. Il tipo di dati è valuta. Questo campo viene visualizzato progressivamente dopo che l’utente indica l’azione intrapresa per soddisfare l’obiettivo. Consulta [Stima dell’incremento dei ricavi](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md) per maggiori informazioni.

   La corretta configurazione delle metriche di successo è fondamentale per ottenere i dati previsti.

   Per ulteriori informazioni, vedi [Metriche di successo](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924)

1. (Facoltativo) Aggiungi altre metriche.
1. Fai clic su **[!UICONTROL Salva e chiudi]** al termine dell&#39;impostazione delle metriche.

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
* Comprendere e generare le metriche [!UICONTROL Conversione], [!UICONTROL Ricavi] e [!UICONTROL Coinvolgimento]
* Creazione di una metrica di tracciamento dei clic

>[!VIDEO](https://video.tv.adobe.com/v/17380)
