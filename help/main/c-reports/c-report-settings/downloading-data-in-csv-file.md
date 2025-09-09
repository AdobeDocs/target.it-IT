---
keywords: rapporti;scaricare rapporti;CSV;metriche di successo;dettagli ordine
description: Scopri come scaricare dati da attività Adobe [!DNL Target] in formato CVS per l’importazione rapida in Excel, Access o altri programmi di analisi dei dati.
title: Come posso scaricare i dati del rapporto in un file CSV?
feature: Reports
exl-id: b4387184-8730-4367-8bc3-52d8fbe2583e
source-git-commit: e42398b8774fff57c00658636a52bd0038ad94b4
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 30%

---

# Download di dati in un file CSV

Scarica i dati in formato .csv per l&#39;importazione rapida in [!DNL Excel], [!DNL Access] o altri programmi di analisi dei dati.

Per scaricare i dati in un file CSV:

1. Fai clic su **[!UICONTROL Activities]**, quindi sull’attività desiderata tra quelle elencate.

   Se hai numerose attività, fai clic sull&#39;icona Filtro ( ![icona Filtro](/help/main/assets/icons/Filter.svg) ) per filtrare l&#39;elenco selezionando le opzioni dagli elenchi a discesa [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type] e [!UICONTROL Activity Source].

1. Fare clic sulla scheda **[!UICONTROL Reports]**.
1. Fai clic sull&#39;icona **[!UICONTROL Download]** ( ![icona Scarica](/help/main/assets/icons/Download.svg) ), quindi seleziona un tipo di rapporto da scaricare per l&#39;analisi in Excel e altri strumenti.

   * [!UICONTROL Export Reports to CSV]
   * [!UICONTROL Export Order Details to CSV]

## Formato di download CSV per popolarità e algoritmi basati su chiavi {#format}

Il file CSV scaricabile riflette in modo coerente i risultati generati dopo l’esecuzione dei criteri di back-end.

**Per gli algoritmi di popolarità (non basati su chiave), il file include:**

* Una riga di consigli di backup con prefisso *
* Una riga distinta elenca i consigli basati sulle impostazioni dell’algoritmo

**Per gli algoritmi basati su chiavi, il file include:**

* Una riga di backup simile agli algoritmi di popolarità
* Righe multiple in formato chiave-valore, dove la prima voce è l’ID prodotto della chiave, seguita da ID prodotto separati da virgole che rappresentano i candidati per i consigli

## [!UICONTROL Export Report to CSV] {#section_38BD9743EB254453B5F4A0A6F2720CD3}

Il report [!UICONTROL Success Metrics] mostra informazioni sulle metriche di successo e le metriche seguenti non disponibili nell&#39;interfaccia utente di [!DNL Target]:

* Tempo di conversione medio in ore, per vedere quanto tempo ci vuole in media affinché un visitatore raggiunga il punto di conversione
* Somma dei ricavi al quadrato, per calcoli di affidabilità statistica offline

I dati vengono salvati fino alla fine dell’attività.

>[!NOTE]
>
>Il rapporto CSV include solo dati non elaborati; non include metriche calcolate come ricavi per visitatore, incremento o affidabilità, utilizzate per i test A/B. Per calcolare queste metriche calcolate, scarica il file Excel del [!DNL Target] [calcolatore di affidabilità completo](/help/main/assets/complete_confidence_calculator.xlsx) per immettere il valore dell&#39;attività oppure controlla [i calcoli statistici nei test A/Bn](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

## [!UICONTROL Export Order Details to CSV] {#section_96B3F578F91F4CA3AFE38BACA2A0F11E}

Il report [!UICONTROL Order Details] contiene informazioni sugli ordini, tra cui:

* Data e ora dell’ordine
* Importo dell’ordine (se è stato inserito una mbox Inserisci ordine)

  Il report [!UICONTROL Order Details] funziona solo se si dispone di ordini.

* Flag ordine (per ordini duplicati o estremi)

  Un ordine è contrassegnato come estremo se è superiore a +/- 3 deviazioni standard dal valore medio dell’ordine. Questo calcolo utilizza l’ultimo mese di dati (fino al momento in cui è stato eseguito il calcolo). Da un’attività verranno esclusi gli ordini estremi dopo che sarà stata eseguita per un’ora o dopo 15 ordini, a seconda di quale evento si verifica per primo. Per ulteriori informazioni, consulta [Esclusione di ordini estremi](/help/main/c-reports/c-report-settings/excluding-extreme-orders.md#task_2AE7743FFCDD466DAEEB720BE5F33DAA).

* ID prodotto

  La lunghezza totale degli ID prodotto, concatenati con virgole, non deve superare i 255 caratteri o gli ID non vengono visualizzati correttamente nel rapporto. Ad esempio, se l’ordine ha prodotti con ID “aa, bb”, la lunghezza totale è “aa, bb” = 5.

* Esperienza

  Nel report [!UICONTROL Order Details] per le attività [!UICONTROL A/B Test], [!UICONTROL Experience Targeting] (XT) e [!UICONTROL Multivariate Test] (MVT), la colonna [!UICONTROL Experience] contiene l&#39;esperienza `localId`. Si tratta del valore restituito da `$campaign.recipe.id` nei token dell’offerta.

  Non esiste una colonna [!UICONTROL Experience] per le attività [!UICONTROL Automated Personalization] (AP). La colonna [!UICONTROL Algorithm Name] corrente è stata sostituita da &quot;Controllo&quot; rispetto a &quot;Destinato&quot;, come mostrato altrove in [!DNL Target].

  Nessun impatto sulle attività [!UICONTROL Recommendations].

>[!NOTE]
>
>* I dati del rapporto di ordine includono quattro settimane di dati per l’ambiente predefinito (gruppo host) e due settimane per tutti gli ambienti non predefiniti.
>* Le metriche dei ricavi impostate su &quot;[!UICONTROL Increment count and keep the user in the activity]&quot; registrano i dettagli solo per il primo ordine effettuato dallo stesso visitatore. Tutti gli ordini successivi aumentano il conteggio delle conversioni, ma non aggiungono ricavi a RPV/AOV/Sales e non sono inclusi nel report [!UICONTROL Order Details].

## Best practice

* Per registrare un record dell&#39;ordine, è necessario passare il parametro `orderTotal`.
* I valori passati tramite il parametro mbox `ProductPurchasedId` sono elencati nel report [!UICONTROL Order Details].
* Si consiglia di includere `orderID` e `orderTotal`. Questo consente di ignorare automaticamente eventuali ordini duplicati.

## Avvertenze  {#section_49B9590904A645B18E694B4EFFFC1DEF}

Le informazioni seguenti si applicano all&#39;opzione [!UICONTROL Download]:

* È possibile scaricare entrambi i rapporti per le attività [!UICONTROL A/B Test], [!UICONTROL Automated Personalization], [!UICONTROL Experience Targeting] e [!UICONTROL Multivariate]. Impossibile scaricare il report [!UICONTROL Success Metrics] per le attività [!UICONTROL Recommendations].
* L&#39;opzione [!UICONTROL Download] non è disponibile per le attività [!UICONTROL A/B Test] e [!UICONTROL Experience Targeting] create prima della versione 15.7.1 di [!DNL Target] (luglio 2015).
* Le esperienze a cui non sono associati dati non vengono registrate nel rapporto scaricato.
* I tipi di pubblico applicati nell&#39;interfaccia utente di reporting di [!DNL Target] non vengono trasferiti al report di download.
* I rapporti generati per il download come file .csv non sono coerenti se l’attività utilizza più di una metrica. Il rapporto scaricabile viene generato solo in base alle impostazioni del rapporto e considera lo stesso valore per tutte le altre metriche utilizzate. L’origine di riferimento è sempre il rapporto visualizzato nell’interfaccia utente [!DNL Target].
