---
keywords: Targeting
description: Scopri come Adobe [!DNL Target] mostra e calcola il tasso di conversione, l'incremento, l'affidabilità e l'intervallo di affidabilità per ogni esperienza.
title: Come posso visualizzare il tasso di conversione, l’incremento e il livello di affidabilità?
feature: Reports
exl-id: b4cfe926-eb36-4ce1-b56c-7378150b0b09
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '2113'
ht-degree: 49%

---

# Tasso di conversione

Per ogni esperienza vengono riportati il tasso di conversione, l’incremento, l’affidabilità e l’intervallo di affidabilità.

La figura seguente mostra l&#39;intestazione del grafico per un&#39;attività di esempio con le intestazioni [!UICONTROL Conversion Rate], [!UICONTROL Lift] e [!UICONTROL Confidence] evidenziate.

![immagine a tasso di conversione](assets/conversion-rate.jpg)

>[!NOTE]
>
>In tutti i dati, gli ordini duplicati vengono ignorati se viene passato un `orderID`. Nel rapporto di audit vengono elencati gli ordini duplicati ignorati.

## Tasso di conversione {#section_07A36846C4E84D0881906809B9CE5A74}

Mostra il tasso di conversione mediano, l’affidabilità, l’intervallo e il numero di conversioni.

Esamina, ad esempio, la seguente colonna del rapporto sul tasso di conversione:

![immagine dei dettagli del tasso di conversione](assets/conversion-rate-detail.jpg)

La prima riga rappresenta l’esperienza di controllo. Mostra un tasso di conversione del 15%, con tre conversioni. La seconda, Esperienza B, mostra un tasso di conversione del 15%, con un intervallo di affidabilità di +/-15,65% e tre conversioni.

>[!NOTE]
>
>Attualmente, l’intervallo di affidabilità viene calcolato solo per le metriche binarie.

## Incremento {#section_0F409572C720433D9378092ABC999982}

Confronta il tasso di conversione per ogni esperienza rispetto all’esperienza di controllo.

Incremento = (TC esperienza - TC controllo) / TS controllo

Se il controllo è uguale a 0, non vi è alcuna percentuale di incremento.


## Dati retail {#section_30A674731BA6440E9BB93C421BE990EE}

I dati dei ricavi per visita, del valore medio dell&#39;ordine e delle vendite vengono visualizzati per ogni esperienza se si inserisce una mbox Inserisci ordine (`orderConfirmPage`) e la si seleziona come mbox di conversione.

## Livello di affidabilità e Intervallo di affidabilità {#concept_0D0002A1EBDF420E9C50E2A46F36629B}

Per ogni esperienza, vengono visualizzati l’intervallo di affidabilità e l’intervallo di affidabilità.

Puoi eseguire calcoli offline per for Target (A4T), ma richiede un passaggio con esportazioni di dati in [!DNL Analytics]Analytics. Per ulteriori informazioni, vedi “Esecuzione di calcoli offline per Analytics for Target (A4T)”, di seguito.

### Affidabilità {#section_26FE5E44BDD5478792A65FCFD83DCCDC}

L’affidabilità di un’esperienza o di un’offerta visualizzata rappresenta la probabilità (espressa in percentuale) di ottenere un risultato meno estremo di quello effettivamente osservato, se l’ipotesi nulla è vera (in sostanza, se non vi è alcuna differenza nei tassi di conversione tra tale esperienza o offerta e l’esperienza/offerta di controllo). In termini di valori p, l’affidabilità visualizzata è 1 - valore p. In termini più semplici, un’affidabilità maggiore indica che i dati sono meno coerenti con l’ipotesi che l’offerta/esperienza di controllo e quella di non controllo abbiano tassi di conversione uguali.

L’affidabilità raggiunge il 100,00%, quando maggiore o uguale a 99,995%.

![immagine report](assets/conf_report.png) ![immagine dettagli report](assets/conf_report_detail.png)

Prima di prendere qualsiasi decisione di business, attendi di avere un campione sufficientemente grande e che le quattro barre di affidabilità su una o più esperienze rimangano coerenti per un periodo di tempo continuativo, al fine di garantire che i risultati siano stabili.


### Intervallo di affidabilità {#section_F582738DFE1648C78B93D81EBC6CACF7}

>[!NOTE]
>
>Attualmente, l’intervallo di affidabilità viene calcolato solo per le metriche binarie.

L&#39;*intervallo di attendibilità* è un intervallo di stime entro il quale è possibile trovare il valore effettivo della metrica a un determinato livello di affidabilità. Target mostra sempre intervalli di affidabilità del 95%. L’intervallo di affidabilità viene visualizzato come una percentuale +/- di colore grigio chiaro nella colonna Tasso di conversione. Nell’esempio riportato di seguito, l’intervallo di affidabilità per l’incremento di Esperienza B è +/-15,65%.

![immagine_tasso_conversione](assets/conversion_rate.png)

**Esempio:** l&#39;RPV osservato di un&#39;esperienza è di $10 e il relativo **intervallo di affidabilità** al 95% è da $5 a $15. A noi sconosciuti, il suo vero RPV è $12. Quindi, se il test viene eseguito più volte, il 95% del tempo calcolato per l&#39;intervallo di affidabilità conterrà il valore _true_ dell&#39;RPV di $12.

**Che cosa influisce sull’intervallo di affidabilità?** La formula segue metodi statistici standard per il calcolo degli intervalli di affidabilità.

* **Dimensione del campione:** al crescere del campione l’intervallo si ridurrà. Questo rapporto è quello preferenziale, perché indica che i rapporti si avvicinano al valore effettivo della metrica di successo.
* **Deviazione standard più piccola:** più risultati simili, come AOV simili o numeri simili o visitatori con conversioni ogni giorno, riducono la deviazione standard.

## Calcolo dell’affidabilità e modalità di esecuzione offline {#section_86F7C231943043A5B8B6BFE67B706E3B}

Il [rapporto CSV scaricato](/help/main/c-reports/downloading-data-in-csv-file.md#concept_3F276FF2BBB2499388F97451D6DE2E75) include solo dati non elaborati; non include metriche calcolate come ricavi per visitatore, incremento o affidabilità, utilizzate per i test A/B.

Per calcolare queste metriche calcolate, scarica il file Excel del [calcolatore di affidabilità completo](/help/main/assets/complete_confidence_calculator.xlsx) di Target per immettere il valore dell&#39;attività oppure controlla [i calcoli statistici nei test A/Bn](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

>[!NOTE]
>
>Questo calcolatore è per i rapporti basati su Target e non per la creazioni di rapporti per A4T.

## Esecuzione di calcoli offline per Analytics for Adobe Target (A4T) {#section_B34BD016C8274C97AC9564F426B9607E}

Puoi eseguire calcoli offline per A4T, ma è necessario un ulteriore passaggio di esportazione dei dati di [!DNL Analytics].

Per A4T viene utilizzato un calcolo del test t [Welch](https://en.wikipedia.org/wiki/Welch%27s_t-test){target=_blank} per variabili continue (anziché metriche binarie). In Analytics, un visitatore viene sempre tracciato e ogni azione intrapresa viene conteggiata. Pertanto, se il visitatore effettua più acquisti o visita una metrica di successo più volte, tali hit aggiuntivi vengono conteggiati. Questo rende la metrica una variabile continua. Per eseguire il calcolo del test t di Welch, è necessaria la &quot;somma dei quadrati&quot; per calcolare la varianza, che viene utilizzata nel denominatore della statistica t. [I calcoli statistici nei test A/Bn](/help/main/c-reports/statistical-methodology/statistical-calculations.md) spiegano i dettagli delle formule matematiche utilizzate. La somma dei quadrati può essere recuperata da [!DNL Analytics]. Per ottenere la somma dei quadrati è necessario eseguire un’esportazione a livello del visitatore per la metrica che desideri ottimizzare, per un periodo di tempo campione.

Ad esempio, se stai ottimizzando le visualizzazioni di pagina per visitatore, puoi esportare un campione del numero totale di visualizzazioni di pagina per visitatore per un intervallo di tempo specificato, forse un paio di giorni (sono sufficienti poche migliaia di punti dati). Dovresti poi quadrare ogni valore e sommare i totali (è importante eseguire le operazioni in questo ordine). Questo valore di “somma dei quadrati” viene quindi utilizzato nel Calcolatore di affidabilità completo. Per questi valori consulta la sezione “ricavi” del foglio di calcolo.

**Per eseguire la funzione di esportazione dei dati di [!DNL Analytics]:**

1. Accedi a [!DNL Adobe Analytics].
1. Fare clic su **[!UICONTROL Tools]** > **[!UICONTROL Data Warehouse]**.
1. Nella scheda **[!UICONTROL Data Warehouse Request]**, compila i campi.

   Per ulteriori informazioni su ogni campo, consulta “Descrizioni di Data Warehouse” in [Data Warehouse](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse.html).

   | Campo | Istruzioni |
   |--- |--- |
   | Request Name (Nome richiesta) | Specifica un nome per la richiesta. |
   | Reporting Date (Data rapporto) | Specifica un periodo di tempo e una granularità.<br>Per la prima richiesta si consiglia di scegliere non più di un’ora o un giorno di dati.  L’elaborazione dei file di Data Warehouse richiede più tempo per periodo di tempo più lunghi, pertanto è sempre consigliabile richiedere prima dati per un periodo di tempo breve, per assicurarsi che il file restituisca il risultato atteso. Quindi, passa a Request Manager (Gestione richieste), duplica la richiesta e richiedi più dati la seconda volta. Inoltre, se si imposta la granularità su un valore diverso da &quot;None&quot;, la dimensione del file aumenterà drasticamente.<br>![Data Warehouse](/help/main/c-reports/assets/datawarehouse.png) |
   | Available Segments (Segmenti disponibili) | Applica un segmento, se necessario. |
   | Breakdowns (Suddivisioni) | Seleziona le dimensioni desiderate: Standard è pronto all’uso (OOTB), mentre Personalizzato include eVar e proprietà. Se sono necessarie informazioni a livello di ID visitatore, è consigliabile utilizzare &quot;ID visitatore&quot; anziché &quot;ID visitatore Experience Cloud&quot;.<ul><li>ID visitatore è l’ID finale utilizzato da Analytics. Si tratterà di AID (se il cliente è un’azienda) o MID (se il cliente è nuovo o se ha cancellato i cookie da quando è stato avviato il servizio ID visitatore di MC).</li><li>L’ID visitatore di Experience Cloud sarà impostato solo per i clienti che sono nuovi o che hanno cancellato i cookie da quando è stato avviato il servizio ID visitatore di MC.</li></ul> |
   | Metrics (Metriche) | Seleziona la metrica desiderata. La metrica standard è OOTB, mentre quella personalizzata include eventi personalizzati. |
   | Report Preview (Anteprima rapporto) | Rivedi le impostazioni prima di pianificare il rapporto.<br>![Data Warehouse 2](/help/main/c-reports/assets/datawarehouse2.png) |
   | Schedule Delivery (Pianifica consegna) | Immettere un indirizzo di posta elettronica a cui recapitare il file, assegnare un nome al file, quindi selezionare [!UICONTROL Send Immediately].<br>Nota: il file può essere consegnato tramite FTP in [!UICONTROL Advanced Delivery Options]<br>![Pianifica consegna](/help/main/c-reports/assets/datawarehouse3.png). |

1. Fare clic su **[!UICONTROL Request this Report]**.

   La consegna dei file può richiedere fino a 72 ore, a seconda della quantità di dati richiesti. Puoi controllare l&#39;avanzamento della tua richiesta in qualsiasi momento facendo clic su [!UICONTROL Tools] > [!UICONTROL Data Warehouse] > [!UICONTROL Request Manager].

   Se desideri richiedere nuovamente i dati richiesti in passato, puoi duplicare una vecchia richiesta da [!UICONTROL Request Manager] in base alle esigenze.

Per ulteriori informazioni su [!DNL Data Warehouse], consulta i seguenti collegamenti nella documentazione di [!DNL Analytics]:

* [Crea una richiesta Data Warehouse](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/t-dw-create-request.html)
* [Data Warehouse best practice](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse-bp.html)

## Metodologia di conteggio {#concept_EC19BC897D66411BABAF2FA27BCE89AA}

È possibile scegliere di visualizzare i rapporti in base a diverse metodologie di conteggio per capire come le attività create influiscono sugli utenti, durante l’intero ciclo di vita o in una singola sessione.

La metodologia di conteggio è supportata per i seguenti tipi di attività:

* Test A/B

  Come eccezione, le attività A/B di targeting automatica supportano solo la metodologia di conteggio predefinita “Visite”.

* Targeting esperienza (XT)
* Test multivariato (MVT)

  Per il rapporto sul contributo degli elementi MVT, Target non supporta l’attività Impression per i tipi di metrica Ricavi.

* Consigli

Per le attività Personalizzazione automatica (AP) al momento è supportata solo la metodologia di conteggio predefinita (Visite).

È possibile visualizzare i rapporti tramite le seguenti metodologie di conteggio:

* **Visitatore:** un partecipante univoco nell’attività, per tutta la durata dell’attività.

  Una persona viene conteggiata come nuovo partecipante se visita il sito da un nuovo computer o un nuovo browser; se elimina il cookie; o se viene convertito e torna all’attività con lo stesso cookie. Un partecipante è identificato dal PCID nel cookie mbox del visitatore. Se il PCID cambia, la persona viene considerata come un nuovo visitatore.

* **Visita:** un partecipante univoco in un’esperienza durante una singola sessione del browser di 30 minuti.

  Se viene realizzata una conversione o se il visitatore ritorna al sito dopo un’assenza di almeno 30 minuti, il visitatore di ritorno viene conteggiato come una nuova visita. Una visita è identificata da `sessionID` nel cookie mbox del visitatore. Quando `sessionID` cambia, la visita viene considerata nuova.

* **Impression/Visualizzazione pagina:** conteggiata ogni volta che un visitatore carica una pagina dell’attività.

  Una singola visita potrebbe includere diverse impression, ad esempio, della home page.

>[!NOTE]
>
>Di solito, questi conteggi sono determinati dai cookie e dalle attività di sessione. Tuttavia, se il visitatore raggiunge il punto di conversione finale di un’attività e quindi accede nuovamente all’attività, viene considerato come un nuovo partecipante e una nuova visita all’attività. Questo vale anche se i valori PCID e `sessionID` non cambiano.

## Perché [!DNL Target] consiglia di utilizzare i test t di Welch? {#t-test}

I test A/B sono esperimenti per confrontare il valore medio di alcune metriche di business in una variante di controllo (nota anche come esperienza) con il valore medio della stessa metrica in una o più esperienze alternative.

[!DNL Target] consiglia di utilizzare il test t di [Welch](https://en.wikipedia.org/wiki/Welch%27s_t-test), in quanto questi presupposti richiedono meno presupposti rispetto ad alternative come i test z e rappresentano il test statistico appropriato per eseguire confronti a coppie di metriche aziendali (quantitative) tra esperienze di controllo ed esperienze alternative.

### Più in dettaglio

Quando si eseguono test A/B online, ogni utente/visitatore viene assegnato in modo casuale a una singola variante. Successivamente, effettuiamo misurazioni delle metriche aziendali di interesse (ad esempio conversioni, ordini, ricavi, ecc.) per i visitatori in ogni variante. Il test statistico utilizzato verifica quindi l’ipotesi che la metrica di business media (ad esempio tasso di conversione, ordini per utente, ricavi per utente, ecc.) è uguale per il controllo e per una determinata variante alternativa.

Anche se la metrica aziendale stessa potrebbe essere distribuita in base a una distribuzione arbitraria, la distribuzione della media di questa metrica (all&#39;interno di ogni variante) dovrebbe convergere in una distribuzione normale tramite il [Teorema del limite centrale](https://en.wikipedia.org/wiki/Central_limit_theorem). Tieni presente che, anche se non vi è alcuna garanzia sulla velocità con cui questa distribuzione di campionamento della media convergerà verso la normale, questa condizione viene in genere raggiunta data la scala dei visitatori nei test online.

Data questa normalità della media, si può dimostrare che la statistica di prova da utilizzare segue una distribuzione t, perché è il rapporto tra un valore distribuito normalmente (la differenza nella media della metrica di business) e un termine di scala basato su una stima dei dati (l’errore standard della differenza nelle medie). Il **t-test** è quindi il test di ipotesi appropriato, dato che la statistica del test segue una distribuzione t.

### Perché non vengono utilizzati altri test

Un **z-test** è tecnicamente inappropriato perché nel tipico scenario di test A/B, il denominatore della statistica del test non è derivato da una varianza nota, ma deve essere stimato dai dati. Tuttavia, per campioni di dimensioni sufficientemente grandi, il test z e il test t sono identici.

**I test del chi-quadrato** non vengono utilizzati perché sono appropriati per determinare se esiste una relazione qualitativa tra due varianti (ovvero un&#39;ipotesi nulla che non vi sia alcuna differenza tra le varianti). I test T sono più appropriati per lo scenario di _quantitativamente_ metriche di confronto.

Il test U **Mann-Whitney** è un test non parametrico appropriato quando la distribuzione di campionamento della metrica di business media (per ogni variante) non è distribuita normalmente. Tuttavia, come discusso in precedenza, date le dimensioni del traffico coinvolto nei test online, il Teorema del limite centrale si applica in genere, e quindi il test t può essere applicato in modo sicuro.

Metodi più complessi come **ANOVA** (che generalizzano test t in più di due varianti) possono essere applicati quando un test ha più di due esperienze (&quot;test A/Bn&quot;). Tuttavia, ANOVA risponde alla domanda &quot;se tutte le varianti hanno lo stesso mezzo&quot;, mentre nel tipico test A/Bn siamo più interessati a _quale variante specifica_ è migliore. In [!DNL Target] vengono quindi applicati test t regolari che confrontano ogni variante con un controllo, con una correzione Bonferroni per tenere conto di confronti multipli.