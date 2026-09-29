---
keywords: Targeting esperienza;XT;metriche;impostazione metriche;metrica obiettivo;impostazioni attività;metrica di successo;conversione;entrate;ricavi;coinvolgimento
description: Scopri come specificare le metriche in un'attività [!DNL Adobe Target] [!UICONTROL Targeting esperienza] per determinare quando una visita ha esito positivo, ad esempio [!UICONTROL Conversione], [!UICONTROL Ricavi] o [!UICONTROL Coinvolgimento].
title: Come si impostano le metriche obiettivo in un'attività [!UICONTROL Targeting esperienza]?
feature: Experience Targeting
exl-id: 16249930-8b9c-441c-bd14-5f32332556d2
TQID: 'https://experienceleague.adobe.com/DRFhQ7plSdYqXdzodxFe8h22fSz9xZs9ATt5Ri2s6AA'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: b6f5758b-84f7-4943-8b05-1297a046943c
    internal-label: Experience target
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: ed3d4b67c78791454c55a2cad4908a37a4d60e26
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 52%
---
# Impostare le metriche nelle attività [!UICONTROL Targeting esperienza] (XT)

Utilizza le metriche in un&#39;attività [!DNL Adobe Target] [!UICONTROL Targeting esperienza] (XT) per determinare quando una visita ha esito positivo.

Per informazioni dettagliate sulle metriche di successo, vedi [Metriche di successo](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).

1. Specifica l’obiettivo dell’attività.
1. Seleziona una [metrica di successo](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924)

   ![Selezionare una metrica di successo](/help/main/c-activities/t-experience-target/t-xt-create/assets/ab_metrics-new.png)

   Nella pagina [!UICONTROL Seleziona metriche] sono elencate le metriche di successo che è possibile scegliere per l&#39;attività. Le metriche di successo sono suddivise nelle seguenti categorie:

   * [!UICONTROL Conversione]
   * [!UICONTROL Ricavi]
   * [!UICONTROL Coinvolgimento]

   Puoi utilizzare una qualsiasi delle metriche di successo predefinite, oppure puoi crearne una personalizzata. È inoltre possibile contrassegnare una metrica di successo come metrica principale. Le schede dei rapporti e di Experience Cloud per impostazione predefinita mostrano la metrica primaria, se è stata impostata.
1. Specifica le impostazioni per le metriche.

   Le impostazioni disponibili dipendono dalla metrica di successo in uso.

   Se attivato, il campo [!UICONTROL Valore stimato della conversione] (non disponibile per le metriche [!UICONTROL Punteggio di pagina]) fornisce un valore per l&#39;obiettivo. Questo valore consente a [!DNL Target] di calcolare un incremento stimato dei ricavi. Questo campo è facoltativo; tuttavia, i ricavi incrementali per eventuali metriche non collegate ai ricavi non possono essere calcolate senza di esso. Il tipo di dati è valuta. Questo campo viene visualizzato progressivamente dopo che l’utente indica l’azione intrapresa per soddisfare l’obiettivo. Consulta [Stima dell’incremento dei ricavi](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md) per maggiori informazioni.

   La corretta configurazione delle metriche di successo è fondamentale per ottenere i dati previsti.

   Per ulteriori informazioni, vedi [Metriche di successo](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).

1. (Facoltativo) Aggiungi altre metriche.
1. Fai clic su **[!UICONTROL Continua]** una volta completata l&#39;impostazione delle metriche.

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
