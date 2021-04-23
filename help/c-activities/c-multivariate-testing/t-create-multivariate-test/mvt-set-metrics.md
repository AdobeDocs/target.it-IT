---
keywords: multivariato;MVT;metriche;impostare metriche;metrica obiettivo;impostazioni attività;metrica di successo;conversione;ricavi;impegno
description: Scopri come specificare le metriche in un’attività Test multivariato di Adobe [!DNL Target] per determinare quando una visita ha esito positivo, ad esempio Conversione, Entrate e Coinvolgimento.
title: Come si impostano le metriche degli obiettivi in un’attività Test multivariato (MVT)?
feature: Test multivariati
exl-id: 8530b3f1-5daa-4a03-a482-93b10eb23208
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 82%

---

# Impostare le metriche per i test multivariati

Utilizza le metriche in un test multivariato di Adobe Target per determinare quando una visita ha esito positivo.

Per informazioni dettagliate sulle metriche di successo, consulta [Metriche di successo](/help/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924).

1. Specifica l’obiettivo dell’attività.
1. Seleziona una [metrica di successo](/help/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924)

   ![Elenco per impostare le metriche](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt_metrics-list.png)

   Nella pagina [!UICONTROL Seleziona metriche] sono incluse le metriche di successo che si possono scegliere per l’attività. Le metriche di successo sono suddivise nelle seguenti categorie:

   * Conversione
   * Ricavi
   * Coinvolgimento

   È possibile utilizzare una qualsiasi delle metriche di successo predefinite, o crearne una personalizzata. È inoltre possibile contrassegnare una metrica di successo come metrica principale. Le schede dei rapporti e di Experience Cloud per impostazione predefinita mostrano la metrica primaria, se è stata impostata.
1. Specifica le impostazioni per le metriche.

   Le impostazioni disponibili dipendono dalla metrica di successo in uso.

   Se attivato, il campo del [!UICONTROL valore stimato della conversione] (non disponibile per le metriche Punteggio di pagina) fornisce un valore per l’obiettivo. Questo valore consente a Target di calcolare un incremento stimato dei ricavi. Questo campo è facoltativo; tuttavia, i ricavi incrementali per eventuali metriche non collegate ai ricavi non possono essere calcolate senza di esso. I dati sono di tipo valuta. Questo campo viene visualizzato progressivamente dopo che l’utente indica l’azione intrapresa per soddisfare l’obiettivo. Consulta [Stima dell’incremento dei ricavi](/help/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md) per maggiori informazioni.

   La corretta configurazione delle metriche di successo è fondamentale per ottenere i dati previsti.

   Per ulteriori informazioni, vedi [Metriche di successo](/help/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924)
1. (Facoltativo) Aggiungi altre metriche.
1. Una volta completata la configurazione delle metriche, fai clic su **[!UICONTROL Continua]**. Nota che quando denomini o rinomini una metrica, i seguenti caratteri non sono consentiti:

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

## Video di formazione: metriche attività (7:43)  ![Badge tutorial](/help/assets/tutorial.png)

Questo video contiene informazioni su come utilizzare le metriche di successo.

* Le metriche per “Obiettivo”
* Concetti e creazione di metriche per conversione, ricavi e coinvolgimento
* Creazione di una metrica di tracciamento dei clic

>[!VIDEO](https://video.tv.adobe.com/v/17380)
