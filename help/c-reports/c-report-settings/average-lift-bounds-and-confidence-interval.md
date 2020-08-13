---
keywords: Target;reports;report settings;environment;lift;lift bound;variance;confidence;control
description: I rapporti includono diversi punti di dati e rappresentazioni di visualizzazione che consentono di comprendere i limiti di incremento e il livello di affidabilità associati all’attività. Ciò consente di determinare più accuratamente un vincitore.
title: Incremento medio, limiti di incremento e intervallo di affidabilità
feature: report settings
uuid: 2899503a-d81e-4dc3-b258-a5ecafd1d1a4
translation-type: tm+mt
source-git-commit: 3cf1f4fa56f86c106dccdc2c97c080c17c3982b4
workflow-type: tm+mt
source-wordcount: '845'
ht-degree: 98%

---


# Incremento medio, limiti di incremento e intervallo di affidabilità{#average-lift-lift-bounds-and-confidence-interval}

I rapporti includono diversi punti di dati e rappresentazioni di visualizzazione che consentono di comprendere i limiti di incremento e il livello di affidabilità associati all’attività. Ciò consente di determinare più accuratamente un vincitore.

## Incremento medio, limiti di incremento e intervallo di affidabilità {#topic_AFFDC672A8A34D028B100EF6BE5D8129}

I rapporti includono diversi punti di dati e rappresentazioni di visualizzazione che consentono di comprendere i limiti di incremento e il livello di affidabilità associati all’attività. Ciò consente di determinare più accuratamente un vincitore.

>[!NOTE]
>
>Questa funzionalità è disponibile solo quando i rapporti vengono visualizzati nella vista Tabella. Questa funzionalità non è disponibile per le attività che utilizzano [Analytics come origine per la generazione di rapporti (A4T)](../../c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE).

## Panoramica {#section_62C0D7E76F3D49A7B3C371C82AEF27D5}

Le informazioni sull’incremento nell’interfaccia utente di Target per la generazione di rapporti includono:

| Elemento | Dettagli |
|--- |--- |
| Incremento | Il numero elevato e la freccia riflettono il valore atteso dell’incremento. Questo numero è il punto medio nell’intervallo dei limiti di incremento. La freccia di incremento atteso è grigia fino a quando l’affidabilità non supera il 95%. Superata questa soglia, la freccia diventa rossa o verde, rispettivamente per un incremento negativo o positivo. |
| Limiti di incremento | Intervallo di affidabilità dell’incremento del 95%. Viene visualizzato come un intervallo, sotto all’incremento medio. Consulta l’esempio di calcolo di seguito per vedere come vengono calcolati questi limiti di incremento. |
| Grafico box plot | Il grafico box plot nell’interfaccia di Target rappresenta il valore atteso e l’intervallo di affidabilità del 95% della metrica di successo in questione. Immaginalo come una modalità grafica per visualizzare le informazioni sull’incremento e i suoi limiti.<br>Target consente di interpretare le informazioni sull’affidabilità in diversi modi, ad esempio tramite il colore. Nel grafico, la sovrapposizione tra l’intervallo di affidabilità di un’esperienza specifica e l’intervallo di affidabilità del controllo è indicata in grigio. L’intervallo di affidabilità di un’esperienza specifica superiore o inferiore rispetto a quello del controllo viene invece indicato rispettivamente in verde o rosso.<br>La lunghezza della barra box plot rappresenta in modo immediato la grandezza dell’intervallo di affidabilità. A seconda dei dati che vengono raccolti nell’attività, la barra si sposta e cambia. L’intervallo di affidabilità è derivato dalla varianza e dalla dimensione del campione (numero di visitatori). Minore è la varianza e maggiore è la dimensione del campione, più ridotto sarà l’intervallo di affidabilità. |
| Affidabilità | L’affidabilità di un’esperienza o di un’offerta rappresenta la probabilità che l’incremento dell’esperienza o dell’offerta a essa associata rispetto all’esperienza o all’offerta di controllo sia “reale” (non casuale). Tipicamente, 95% è il livello consigliato di affidabilità per considerare l’incremento significativo. |

La figura seguente illustra i limiti di incremento e le informazioni sul livello di affidabilità:

![Rapporto di incremento medio e livello di affidabilità](/help/c-reports/c-report-settings/assets/lift-screenshot-new.png)

## Calcolo dei limiti di incremento {#section_1D360781D972483693680BE0F07AEAD1}

I limiti di incremento rappresentano gli intervalli di affidabilità al 95% dell’incremento per l’esperienza o l’offerta specifica rispetto all’esperienza o all’offerta di controllo. In altre parole, significa che l’incremento reale ha circa il 95% di probabilità di essere compreso tra questi limiti.

I limiti di incremento vengono calcolati con la seguente formula:

![](assets/lift_diagram.png)

Vi sono dei calcoli aggiuntivi per ottenere l’input per i limiti di incremento:

* **Valore-t:** il dato statistico cruciale per il livello di affidabilità al 95% è di 1,96. Ulteriori informazioni sul [valore-t](https://en.wikipedia.org/wiki/T-statistic).
* **Varianza dell’incremento:** l’errore standard della metrica di successo dell’esperienza N e l’errore standard della metrica di successo dell’esperienza di controllo sono necessari per determinare la varianza dell’incremento, la quale è calcolata con la seguente formula (illustrata per un caso in cui la metrica di successo è la conversione).

   ![](assets/lift_variance.png)

* **Errore standard per tasso di conversione/metrica di successo:** l’errore standard viene calcolato nello stesso modo per l’esperienza N e per il controllo, con la seguente formula (illustrata per un caso in cui la metrica di successo è la conversione). Ulteriori informazioni su [Errore standard](https://en.wikipedia.org/wiki/Standard_error).

   ![](assets/standard_error.png)

   >[!NOTE]
   >
   >L’errore standard per le attività con metriche di successo sul ricavo si basa sulla varianza dei ricavi del campione.

## Esempio di calcolo {#section_35BD6FB7AFD346E28BA093147C248471}

Consideriamo un’attività di esempio con due esperienze e i seguenti risultati:

| Esperienza | Visitatori | Conversioni | Tasso di conversione |
|--- |--- |--- |--- |
| Esperienza A (controllo) | 219, 328 | 2.466 | 1,12% |
| Esperienza B | 218, 362 | 3.040 | 1,39% |

Basandoci sulle formule, possiamo calcolare gli input necessari per i limiti di incremento.

**Errore standard per l’esperienza A (controllo)**

![](assets/standard_error_A.png)

**Errore standard per l’esperienza B**

![](assets/standard_error_B.png)

**Varianza di incremento per l’esperienza B**

![](assets/lift_variance_B.png)

**Limiti di incremento per l’esperienza B**

Incremento atteso per l’esperienza B:

![](assets/lift_bounds_B.png)

Pertanto, i limiti di incremento per l’esperienza B saranno:

![](assets/lift_bounds_B2.png)

>[!NOTE]
>
>Potrebbero esserci lievi varianze tra i calcoli manuali svolti utilizzando le formule di cui sopra e i numeri visualizzati nel rapporto. La differenza può essere attribuita al fatto che i numeri delle visualizzazioni di pagina utilizzati nei calcoli manuali sono arrotondati. L&#39;incremento mostrato nel rapporto di Target è basato sui numeri esatti ottenuti dal coinvolgimento totale e dal conteggio del coinvolgimento. I numeri di coinvolgimento possono essere ottenuti tramite l&#39;API di rapporto sulle prestazioni.

## Casi in cui i limiti di incremento non vengono visualizzati{#section_C5622E1E94684DAD937249B51A9E42CC}

In alcuni casi, Target non mostra i limiti di incremento:

* Per qualsiasi attività, quando il numero totale di visite o visitatori è inferiore a 30.
* Per attività di allocazione automatica, nessun limite di incremento viene visualizzato fino a quando un’esperienza non raggiungi il 60% di affidabilità.

