---
keywords: Targeting esperienza;XT;metriche;impostazione metriche;metrica obiettivo;impostazioni attività;metrica di successo;conversione;entrate;ricavi;coinvolgimento
description: Scopri come specificare le metriche in un [!DNL Adobe Target] [!UICONTROL Targeting esperienza] attività per determinare quando una visita ha esito positivo, ad esempio [!UICONTROL Conversione], [!UICONTROL Ricavi], o [!UICONTROL Coinvolgimento].
title: Come si impostano le metriche dell’obiettivo in un [!UICONTROL Targeting esperienza] Attività?
feature: Experience Targeting
exl-id: 16249930-8b9c-441c-bd14-5f32332556d2
source-git-commit: d7c1bbbbc8d1dcc45ac09a09f6b3be01f7542384
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 68%

---

# Impostare le metriche in [!UICONTROL Targeting esperienza] Attività (XT)

Utilizzare le metriche in un [!DNL Adobe Target] [!UICONTROL Targeting esperienza] (XT) attività per determinare quando una visita ha esito positivo.

Per informazioni dettagliate sulle metriche di successo, consulta [Metriche di successo](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).

1. Specifica l’obiettivo dell’attività.
1. Seleziona una [metrica di successo](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924)

   ![Selezionare una metrica di successo](/help/main/c-activities/t-experience-target/t-xt-create/assets/ab_metrics-new.png)

   Il [!UICONTROL Seleziona metriche] pagina elenca le metriche di successo che puoi scegliere per l’attività. Le metriche di successo sono suddivise nelle seguenti categorie:

   * [!UICONTROL Conversione  ]
   * [!UICONTROL Ricavi]
   * [!UICONTROL Coinvolgimento]

   Puoi utilizzare una qualsiasi delle metriche di successo predefinite, oppure puoi crearne una personalizzata. È inoltre possibile contrassegnare una metrica di successo come metrica principale. Le schede dei rapporti e di Experience Cloud per impostazione predefinita mostrano la metrica primaria, se è stata impostata.
1. Specifica le impostazioni per le metriche.

   Le impostazioni disponibili dipendono dalla metrica di successo in uso.

   Se attivato, il campo [!UICONTROL Estimated Value of Conversion (Valore stimato della conversione)] (non disponibile per le metriche Page Score) fornisce un valore per l&#39;obiettivo. Questo valore consente a [!DNL Target] di calcolare un incremento stimato dei ricavi. Questo campo è facoltativo; tuttavia, i ricavi incrementali per eventuali metriche non collegate ai ricavi non possono essere calcolate senza di esso. I dati sono di tipo valuta. Questo campo viene visualizzato progressivamente dopo che l’utente indica l’azione intrapresa per soddisfare l’obiettivo. Consulta [Stima dell’incremento dei ricavi](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md) per maggiori informazioni.

   La corretta configurazione delle metriche di successo è fondamentale per ottenere i dati previsti.

   Per ulteriori informazioni, vedi [Metriche di successo](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).

1. (Facoltativo) Aggiungi altre metriche.
1. Una volta completata la configurazione delle metriche, fai clic su **[!UICONTROL Continua]**. 

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

## Video di formazione: metriche attività (7:43) ![Icona Tutorial](/help/main/assets/tutorial.png)

Questo video contiene informazioni su come utilizzare le metriche di successo.

* Le metriche per “Obiettivo”
* Comprendere e creare metriche per [!UICONTROL Conversione], [!UICONTROL Fatturato] e [!UICONTROL Coinvolgimento]
* Creazione di una metrica di tracciamento dei clic

>[!VIDEO](https://video.tv.adobe.com/v/17380)
