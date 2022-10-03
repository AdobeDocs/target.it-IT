---
keywords: rapporti;metodologia statistica;calcoli statistici;statistiche;media;tasso di conversione;ricavi per visitatore;rpv;intervallo di affidabilità;incremento;test t di saldatura;calcoli offline
description: Informazioni sui calcoli statistici utilizzati nel manuale [!UICONTROL Test A/B] attività [!DNL Adobe Target].
title: Come posso imparare i calcoli statistici utilizzati in [!UICONTROL Test A/B] Attività?
feature: Reports
source-git-commit: 4fc3de2a15f117a4356d67fcffd7f9b881e1179a
workflow-type: tm+mt
source-wordcount: '1078'
ht-degree: 2%

---

# Calcoli statistici nei test A/Bn

In questa pagina sono documentati i calcoli statistici dettagliati utilizzati nei test A/Bn manuali in [!DNL Adobe Target]. Sono fornite definizioni per tasso di conversione, intervallo di affidabilità del tasso di conversione, incremento, intervallo di affidabilità per incremento e affidabilità.

![Rapporto di Target che mostra il tasso di conversione, l’incremento medio e l’intervallo di affidabilità e la confidenza di un’attività di test A/B.](/help/main/c-reports/statistical-methodology/img/target_report.png)

## Prestazioni medie

La sezione seguente illustra i calcoli utilizzati nell&#39;illustrazione precedente.

### Campagne su tasso di conversione e ricavi per visitatore (RPV)

L&#39;illustrazione seguente mostra [!UICONTROL Tasso di conversione], [!UICONTROL Intervallo di affidabilità del tasso di conversione]e il numero di [!UICONTROL Conversioni] in [!DNL Target] rapporto. Ad esempio, la prima riga mostra che per l’esperienza A: la [!UICONTROL Tasso di conversione] è pari al 25,81% con un [!UICONTROL Intervallo di affidabilità] di ±7,7% e 32 conversioni. Dato che 124 visitatori hanno visto l’esperienza, questo equivale a 32/124 = 25,81%.

<p style="text-align:center;"><img width="25%" src="img/conv_rate.png"></p>

il tasso di conversione o **meschino**, *μ<sub>ν</sub>*, per ogni esperienza *ν* in un esperimento è definito come un rapporto tra la somma della metrica e il numero di unità assegnate a tale metrica, *N<sub>ν</sub>*:

<p style="text-align:center;"><img width="125px" src="img/mean_definition.png"></p>

Qui,

* *Y<sub>idroid</sub>* è il valore della metrica per ogni unità *i*, che è stato assegnato a una determinata esperienza *ν*.

* La somma su unità *i* dipende dalla scelta della metodologia di conteggio.

   * Se *Visitatori* viene utilizzata come metodologia di conteggio, ogni unità è un visitatore univoco definito come un partecipante univoco nell’attività per la vita dell’attività.
   * Se *Visite* viene utilizzato come metodologia di conteggio, ogni unità è una visita unica definita come partecipante univoco in un’esperienza durante un [!DNL Target] (con un `sessionId`). Quando il `sessionId` oppure quando il visitatore raggiunge la fase di conversione, viene conteggiata una nuova visita.
   * Se *Impression attività* viene utilizzata come metodologia di conteggio, ogni unità è un’impression univoca definita ogni volta che un visitatore carica una pagina dell’attività.

## Intervallo di affidabilità del tasso medio/di conversione

L’intervallo di affidabilità del tasso di conversione è definito in modo intuitivo come intervallo di possibili tassi di conversione coerente con i dati sottostanti.

Durante gli esperimenti, il tasso di conversione che osserviamo per una determinata esperienza è un *stima* del tasso di conversione &quot;vero&quot;. Per quantificare l&#39;incertezza in questa stima, possiamo utilizzare un intervallo di affidabilità. [!DNL Target] segnala sempre un intervallo di affidabilità del 95%, il che significa che nel lungo periodo il 95% degli intervalli di affidabilità calcolati include il tasso di conversione effettivo dell’esperienza.

Un intervallo di affidabilità del 95% del tasso di conversione *μ<sub>ν</sub>* è definito come intervallo di valori:

<p style="text-align:center;"><img width="30%" src="img/confidence_interval.png"></p>

dove l&#39;errore standard per la media è definito come

<p style="text-align:center;"><img width="75px" src="img/se_conv_continuous.png"></p>

se si utilizza una stima imparziale della deviazione standard del campione:

<p style="text-align:center;"><img width="200px" src="img/stdev_definition.png"></p>

Tieni presente che quando la campagna è una campagna a tasso di conversione (ad esempio, la metrica di conversione è binaria), l’errore standard si riduce a:

<p style="text-align:center;"><img width="150px" src="img/se_conv.png"></p>

## Incremento

La figura seguente mostra Incremento e intervallo di affidabilità in un [!DNL Target] Rapporto. Il numero rappresenta la media dell’intervallo dei limiti di incremento; la freccia indica se l’incremento è positivo o negativo. La freccia viene visualizzata in grigio finché l’affidabilità non supera il 95%. Dopo che l’affidabilità supera la soglia, la freccia è verde o rossa in base a un incremento positivo o negativo.

<p style="text-align:center;"><img width="35%" src="img/lift.png"></p>

L’incremento tra un’esperienza  *ν* e l&#39;esperienza di controllo *ν<sub>0</sub>* è il relativo &quot;delta&quot; nei tassi di conversione, definito come

<p style="text-align:center;"><img width="15%" src="img/lift_definition.png"></p>

dove i singoli tassi di conversione sono definiti sopra. Più semplicemente,

```
Lift(Experience N) = (Performance_Experience_N - Performance_Control)/ Performance_Control
```

Se il tasso di conversione dell’esperienza di controllo *ν<sub>0</sub>* è 0, non c&#39;è alcun incremento.

## Intervallo di affidabilità dell’incremento

Il grafico a boxplot nel [!UICONTROL Incremento medio e intervallo di affidabilità] rappresenta il valore medio e l’intervallo di affidabilità del 95% dell’incremento. Il grafico a discesa è grigio quando esiste una sovrapposizione nell’intervallo di affidabilità di una determinata esperienza senza controllo con l’intervallo di affidabilità dell’esperienza di controllo ed è verde o rosso quando l’intervallo di affidabilità di una determinata esperienza è superiore o inferiore all’intervallo di affidabilità dell’esperienza di controllo.

Errore standard dell’incremento tra un’esperienza  *ν* e l&#39;esperienza di controllo  *ν<sub>0</sub>* è definito come:

<p style="text-align:center;"><img width="35%" src="img/se_lift.png" alt="media"></p>

Quindi l’intervallo di affidabilità del 95% dell’incremento è:

<p style="text-align:center;"><img width="40%" src="img/lift_CI.png"></p>

Questo calcolo utilizza il metodo &quot;Delta&quot; e viene descritto [più dettagliatamente in questo documento](/help/main/assets/confidence_interval_lift.pdf)

## Affidabilità

L’ultima colonna mostra l’affidabilità in un [!DNL Target] rapporto. L&#39;affidabilità di un&#39;esperienza è una probabilità (indicata come percentuale) di ottenere un risultato meno estremo di quello effettivamente osservato dato che l&#39;ipotesi null è vera. In termini di valori p, l’affidabilità visualizzata è *1 - p-value*. Intuitivamente, una maggiore affidabilità significa che è meno probabile che l’esperienza di controllo e non di controllo abbia tassi di conversione uguali.

In [!DNL Target], a due code **Test t di Welch** viene eseguita tra l’esperienza di test e l’esperienza di controllo per verificare se i mezzi di prova e di controllo sono gli stessi. Perché di solito non sappiamo se le dimensioni del campione e le varianze di due gruppi sono le stesse prima di eseguire l&#39;esperimento, e [!DNL Target] consente anche di inviare percentuali di traffico diverse a ogni esperienza, non si presuppone che la varianza per ogni esperienza sia uguale. Così, il test t di Welch è scelto invece del test t di Student.

Per eseguire il test t di Welch, iniziamo prima a calcolare il valore t-statistic e i gradi di libertà, quindi eseguiamo un test t a due code per generare il valore p. Infine, calcoliamo l’affidabilità in base al valore p.

La *t*-statistica è definita come la differenza dei mezzi di qualsiasi due variabili casuali indipendenti, *ν* e *ν<sub>0</sub>*, diviso per l’errore standard della differenza:

<p style="text-align:center;"><img width="100px" src="img/t_value.png"></p>

dove *μ<sub>v</sub>* e *μ<sub>v0</sub>* sono i mezzi *ν*  e *ν<sub>0</sub>* e l&#39;errore standard della differenza tra *μ<sub>v</sub>* e *μ<sub>v0</sub>* sono forniti da:

<p style="text-align:center;"><img width="150px" src="img/standard_error_diff.png"></p>

dove *Þ<sup>2</sup><sub>v</sub>* e *Þ<sup>2</sup><sub>v<sub>0</sub></sub>* sono le varianze di due esperienze *ν*  e *ν<sub>0</sub>* rispettivamente *N<sub>v</sub>* e *N<sub>v<sub>0</sub></sub>* sono dimensioni del campione per *ν* e *ν<sub>0</sub>* rispettivamente.

Per il test t di Welch, il grado di libertà è calcolato come segue:

<p style="text-align:center;"><img width="180px" src="img/degree_of_freedom.png"></p>

e il grado di libertà per *ν*  e *ν<sub>0</sub>* sono definiti come:

<p style="text-align:center;"><img width="100px" src="img/df_v.png"></p>

<p style="text-align:center;"><img width="100px" src="img/df_v0.png"></p>

Quindi il valore p può essere calcolato dall&#39;area nelle code del *t*-distribuzione:

<p style="text-align:center;"><img width="20%" src="img/p_value.png"></p>

Infine, la Confidence riportata in [!DNL Target] è definito come:

<p style="text-align:center;"><img width="20%" src="img/confidence.png"></p>

## Esecuzione dei calcoli offline

Il [rapporto CSV scaricato](/help/main/c-reports/downloading-data-in-csv-file.md#concept_3F276FF2BBB2499388F97451D6DE2E75) include solo dati non elaborati; non include metriche calcolate come ricavi per visitatore, incremento o affidabilità, utilizzate per i test A/B.

Per calcolare queste quantità statistiche, scarica il [Calcolatore di affidabilità completo](/help/main/assets/complete_confidence_calculator.xlsx) File Excel per inserire il valore dell&#39;attività.