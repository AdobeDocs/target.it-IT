---
keywords: A/B;metriche di attività;metriche;configurare metriche;metriche obiettivo;impostazioni attività;metrica successo;conversione;ricavi;impegno
description: Scopri come specificare le metriche in un [!DNL Adobe Target] Attività A/B per determinare quando una visita ha esito positivo, ad esempio [!UICONTROL Conversione], [!UICONTROL Ricavi], e [!UICONTROL Coinvolgimento].
title: Come si impostano le metriche dell’obiettivo in un’attività A/B?
feature: A/B Tests
exl-id: 9e9e8787-c0cd-4aab-bd2d-0e9591e0a07d
source-git-commit: 2d5272a852dc879e7307695744b70afe7fee9a38
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 68%

---

# Impostare le metriche

Utilizzare le metriche in un [!DNL Adobe Target] Attività A/B per determinare quando una visita ha esito positivo.

Per informazioni dettagliate sulle metriche di successo, consulta [Metriche di successo](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).

1. In **[!UICONTROL Impostazioni di reporting]** sezione del **[!UICONTROL Obiettivi e impostazioni]** , seleziona una [metrica di successo](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924)

   ![Selezionare una metrica di successo](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_metrics-new.png)

   Il [!UICONTROL Seleziona metriche] opzione elenca le metriche di successo che puoi scegliere per l’attività. Le metriche di successo sono suddivise nelle seguenti categorie:

   * [!UICONTROL Conversione  ]
   * [!UICONTROL Ricavi]
   * [!UICONTROL Coinvolgimento]

   È possibile utilizzare una qualsiasi delle metriche di successo predefinite, o crearne una personalizzata. È inoltre possibile contrassegnare una metrica di successo come metrica principale. Le schede dei rapporti e di Experience Cloud per impostazione predefinita mostrano la metrica primaria, se è stata impostata.

1. Specifica le impostazioni per le metriche.

   Le impostazioni disponibili dipendono dalla metrica di successo in uso.

   Se attivato, il campo del [!UICONTROL valore stimato della conversione] (non disponibile per le metriche Punteggio di pagina) fornisce un valore per l’obiettivo.  Questo valore consente a [!DNL Target] di calcolare un incremento stimato dei ricavi. Questo campo è facoltativo; tuttavia, i ricavi incrementali per eventuali metriche non collegate ai ricavi non possono essere calcolate senza di esso. I dati sono di tipo valuta. Questo campo viene visualizzato progressivamente dopo che l’utente indica l’azione intrapresa per soddisfare l’obiettivo. Consulta [Stima dell’incremento dei ricavi](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md) per maggiori informazioni.

   La corretta configurazione delle metriche di successo è fondamentale per ottenere i dati previsti.

   Per ulteriori informazioni, vedi [Metriche di successo](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).

1. (Facoltativo) Aggiungi altre metriche.

Quando denomini o rinomini una metrica, i seguenti caratteri non sono consentiti:

| Carattere | Descrizione |
|--- |--- |
| / | Barra |
| ? | Punto interrogativo |
| # | Cancelletto |
| : | Due punti |
| = | Uguale |
| + | Più |
| - | Meno |
| @ | Chiocciola |

## Video di formazione: metriche attività (7:43) ![Icona Tutorial](/help/main/assets/tutorial.png)

Questo video contiene informazioni su come utilizzare le metriche di successo.

* Le metriche per “Obiettivo”
* Comprendere e creare metriche per Conversione, Fatturato e Coinvolgimento
* Creazione di una metrica di tracciamento dei clic

>[!VIDEO](https://video.tv.adobe.com/v/17380)
