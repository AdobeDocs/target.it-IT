---
keywords: Target;rapporti;impostazioni dei rapporti;ambiente;incremento;limiti di incremento;varianza;affidabilità;controllo
description: Scopri come interpretare i rapporti di Adobe [!DNL Target] che includono punti di dati e rappresentazioni di visualizzazione per aiutarti a comprendere i limiti di incremento e il livello di affidabilità delle tue attività.
title: Come si visualizza l'incremento medio, i limiti di incremento e l'intervallo di affidabilità?
feature: Rapporti
exl-id: 0453aec1-cca5-462c-8eed-0d40bb4cf323
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 73%

---

# Incremento medio, limiti di incremento e intervallo di affidabilità

I rapporti includono diversi punti di dati e rappresentazioni di visualizzazione che consentono di comprendere i limiti di incremento e il livello di affidabilità associati all’attività [!DNL Adobe Target] per determinare più accuratamente un vincitore.

>[!NOTE]
>
>Questa funzione è disponibile solo quando i rapporti vengono visualizzati nella vista [!UICONTROL Tabella] . Questa funzionalità non è disponibile per le attività che utilizzano [Analytics come origine per la generazione di rapporti (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE).

## Interpreta i dati {#section_62C0D7E76F3D49A7B3C371C82AEF27D5}

L&#39;illustrazione seguente mostra le informazioni [!UICONTROL Limiti di incremento e Livello di affidabilità] :

![Rapporto di incremento medio e livello di affidabilità](/help/c-reports/c-report-settings/assets/lift-screenshot-new.png)

Le informazioni sull’incremento e sull’affidabilità nell’ interfaccia utente per la generazione di rapporti [!DNL Target] includono:

### Incremento

Il numero elevato e la freccia riflettono il valore atteso dell’incremento. Questo numero è il punto medio nell’intervallo dei limiti di incremento. La freccia di incremento atteso è grigia fino a quando l’affidabilità non supera il 95%. Superata questa soglia, la freccia diventa rossa o verde, rispettivamente per un incremento negativo o positivo.

### Limiti di incremento

Intervallo di affidabilità dell’incremento del 95%. Viene visualizzato come un intervallo, sotto all’incremento medio. Consulta [Esempio di calcolo](#example) di seguito per un esempio di come vengono calcolati questi limiti di incremento.

### Grafico a trama

Il grafico a box plot nell’ interfaccia [!DNL Target] rappresenta il valore previsto e l’intervallo di affidabilità del 95% della metrica di successo in questione. Immaginalo come una modalità grafica per visualizzare le informazioni sull’incremento e i suoi limiti.

Esistono alcuni modi principali [!DNL Target] per interpretare le informazioni sull’affidabilità, uno dei quali è il colore. Nel grafico, la sovrapposizione tra l’intervallo di affidabilità di un’esperienza specifica e l’intervallo di affidabilità del controllo è indicata in grigio. L’intervallo di affidabilità di un’esperienza specifica superiore o inferiore rispetto a quello del controllo viene invece indicato rispettivamente in verde o rosso.

La lunghezza della barra box plot rappresenta in modo immediato la grandezza dell’intervallo di affidabilità. A seconda dei dati che vengono raccolti nell’attività, la barra si sposta e cambia. L’intervallo di affidabilità è derivato dalla varianza e dalla dimensione del campione (numero di visitatori). Minore è la varianza e maggiore è la dimensione del campione, più ridotto sarà l’intervallo di affidabilità.

### Affidabilità

L’affidabilità di un’esperienza o di un’offerta rappresenta la probabilità che l’incremento dell’esperienza o dell’offerta a essa associata rispetto all’esperienza o all’offerta di controllo sia “reale” (non casuale). Tipicamente, 95% è il livello consigliato di affidabilità per considerare l’incremento significativo.

## Come vengono calcolati i limiti di incremento? {#section_1D360781D972483693680BE0F07AEAD1}

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

## Esempio di calcolo {#example}

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
>Potrebbero esserci lievi varianze tra i calcoli manuali svolti utilizzando le formule di cui sopra e i numeri visualizzati nel rapporto. La differenza può essere attribuita al fatto che i numeri delle visualizzazioni di pagina utilizzati nei calcoli manuali sono arrotondati. L’incremento mostrato nel rapporto [!DNL Target] si basa sui numeri esatti ottenuti dal coinvolgimento totale e dal conteggio del coinvolgimento. I numeri di coinvolgimento possono essere ottenuti tramite l&#39;API di rapporto sulle prestazioni.

## Quando i limiti di incremento non vengono visualizzati? {#section_C5622E1E94684DAD937249B51A9E42CC}

In alcuni casi, [!DNL Target] non visualizza i limiti di incremento:

* Per qualsiasi attività, quando il numero totale di visite o visitatori è inferiore a 30.
* Per le attività [!UICONTROL Allocazione automatica] , non vengono visualizzati limiti di incremento finché un’esperienza non raggiunge un livello di affidabilità del 60%.
