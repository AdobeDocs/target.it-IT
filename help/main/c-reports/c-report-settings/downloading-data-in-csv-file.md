---
keywords: rapporti;scaricare rapporti;CSV;metriche di successo;dettagli ordine
description: Scopri come scaricare i dati da Adobe [!DNL Target] attività in formato CVS per l'importazione rapida in Excel, Access o altri programmi di analisi dei dati.
title: Come posso scaricare i dati del rapporto in un file CSV?
feature: Reports
exl-id: b4387184-8730-4367-8bc3-52d8fbe2583e
source-git-commit: fc1dcc2b6de1248c35191c1ecd7b36aeb891fd3f
workflow-type: tm+mt
source-wordcount: '727'
ht-degree: 54%

---

# Download di dati in un file CSV

Come scaricare i dati in un formato .csv da importare rapidamente in Excel, Access o altri programmi di analisi dei dati.

Per scaricare i dati in un file CSV:

1. Fai clic su **[!UICONTROL Attività]**, quindi sull’attività desiderata tra quelle elencate.

   Se hai numerose attività, puoi filtrare l’elenco selezionando le opzioni che ti interessano dagli elenchi a discesa [!UICONTROL Tipo], [!UICONTROL Stato], [!UICONTROL Origine per i rapporti], [!UICONTROL Compositore esperienza], [!UICONTROL Tipo di metrica] e [!UICONTROL Origine attività].

1. Fai clic sulla scheda **[!UICONTROL Rapporti]**.
1. Fai clic sull’icona **[!UICONTROL Scarica]**, quindi seleziona un tipo di rapporto da scaricare per l’analisi in Excel e altri strumenti.

   * [!UICONTROL Esportare rapporti in formato CSV]
   * [!UICONTROL Esportare i dettagli ordine in CSV]

   ![Opzioni di download](/help/main/c-reports/assets/download-options.png)

## [!UICONTROL Esportare un rapporto in formato CSV] {#section_38BD9743EB254453B5F4A0A6F2720CD3}

Il [!UICONTROL Metriche di successo] Il rapporto mostra informazioni sulle metriche di successo e le metriche seguenti che non sono disponibili in [!DNL Target] Interfaccia utente:

* Tempo di conversione medio in ore, per vedere quanto tempo ci vuole in media affinché un visitatore raggiunga il punto di conversione
* Somma dei ricavi al quadrato, per calcoli di affidabilità statistica offline

I dati vengono salvati fino alla fine dell’attività.

>[!NOTE]
>
>Il rapporto CSV include solo dati non elaborati; non include metriche calcolate come ricavi per visitatore, incremento o affidabilità, utilizzate per i test A/B. Per calcolare queste metriche calcolate, scarica la [!DNL Target] [Completa il calcolatore di affidabilità](/help/main/assets/complete_confidence_calculator.xlsx) File Excel per immettere il valore dell’attività o rivederla [Calcoli statistici nei test A/Bn](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

## [!UICONTROL Esportare i dettagli ordine in CSV] {#section_96B3F578F91F4CA3AFE38BACA2A0F11E}

Il [!UICONTROL Dettagli ordine] Il report mostra informazioni sugli ordini, tra cui:

* Data e ora dell’ordine
* Importo dell’ordine (se è stato inserito una mbox Inserisci ordine)

   Il [!UICONTROL Dettagli ordine] Il report funziona solo se si dispone di ordini.

* Flag ordine (per ordini duplicati o estremi)

   Un ordine è contrassegnato come estremo se è superiore a +/- 3 deviazioni standard dal valore medio dell’ordine. Questo calcolo utilizza l’ultimo mese di dati (fino al momento in cui è stato eseguito il calcolo). Da un’attività verranno esclusi gli ordini estremi dopo che sarà stata eseguita per un’ora o dopo 15 ordini, a seconda di quale evento si verifica per primo. Per ulteriori informazioni, consulta [Esclusione di ordini estremi](/help/main/c-reports/c-report-settings/excluding-extreme-orders.md#task_2AE7743FFCDD466DAEEB720BE5F33DAA).

* ID prodotto

   La lunghezza totale degli ID prodotto, concatenati con virgole, non deve superare i 255 caratteri o gli ID non vengono visualizzati correttamente nel rapporto. Ad esempio, se l’ordine ha prodotti con ID “aa, bb”, la lunghezza totale è “aa, bb” = 5.

* Esperienza

   Nel rapporto [!UICONTROL Dettagli ordine] per le attività [!UICONTROL Test A/B], [!UICONTROL Targeting esperienza] (XT) e [!UICONTROL Test multivariato] (MVT), la colonna [!UICONTROL Esperienza] contiene il valore `localId` dell’esperienza. Si tratta del valore restituito da `$campaign.recipe.id` nei token dell’offerta.

   Non esiste una colonna [!UICONTROL Esperienze] per le attività [!UICONTROL Personalizzazione automatica] (AP). La colonna [!UICONTROL Nome algoritmo] attuale è stata sostituita da “Controllo” rispetto a &quot;Target&quot;, come in altre aree di [!DNL Target].

   Non vi è stato alcun impatto sulle attività [!UICONTROL Consigli].

>[!NOTE]
>
>* I dati del rapporto di ordine includono quattro settimane di dati per l’ambiente predefinito (gruppo host) e due settimane per tutti gli ambienti non predefiniti.
>* Metriche dei ricavi impostate su &quot;[!UICONTROL Incrementa il conteggio e mantieni l’utente nell’attività]&quot; registra i dettagli dell’ordine solo per il primo ordine effettuato dallo stesso visitatore. Tutti gli ordini successivi aumentano il conteggio delle conversioni, ma non aggiungono ricavi a RPV/AOV/Sales e non sono inclusi nel [!UICONTROL Dettagli ordine] rapporto.


## Best practice

* Per registrare un record dell&#39;ordine, `orderTotal` Il parametro deve essere trasmesso.
* I valori trasmessi tramite il parametro mbox `ProductPurchasedId` sono elencati nel rapporto Dettagli ordine.
* Si consiglia di includere un `orderID` e un `orderTotal`. Questo consente di ignorare automaticamente eventuali ordini duplicati.

## Avvertenze  {#section_49B9590904A645B18E694B4EFFFC1DEF}

Le seguenti informazioni si applicano al [!UICONTROL Scarica] opzione:

* Puoi scaricare entrambi i rapporti per [!UICONTROL Test A/B], [!UICONTROL Automated Personalization], [!UICONTROL Targeting esperienza], e [!UICONTROL Multivariato] attività. Impossibile scaricare [!UICONTROL Metriche di successo] rapporto per [!UICONTROL Recommendations] attività.
* Il [!UICONTROL Scarica] non è disponibile per [!UICONTROL Test A/B] e [!UICONTROL Targeting esperienza] attività create prima di [!DNL Target] versione 15.7.1 (luglio 2015).
* Le esperienze a cui non sono associati dati non vengono registrate nel rapporto scaricato.
* Tipi di pubblico applicati in [!DNL Target] l’interfaccia utente di reporting non viene trasferita al rapporto scaricato.
* I rapporti generati per il download come file .csv non sono coerenti se l’attività utilizza più di una metrica. Il rapporto scaricabile viene generato solo in base alle impostazioni del rapporto e considera lo stesso valore per qualsiasi altra metrica utilizzata. L’origine di riferimento è sempre il rapporto visualizzato nell’interfaccia utente [!DNL Target].
