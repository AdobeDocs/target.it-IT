---
keywords: rapporti;scaricare rapporti;CSV;metriche di successo;dettagli ordine
description: Scopri come scaricare dati da attività Adobe [!DNL Target] in formato CVS per l’importazione rapida in Excel, Access o altri programmi di analisi dei dati.
title: Come posso scaricare i dati del rapporto in un file CSV?
feature: Reports
exl-id: b4387184-8730-4367-8bc3-52d8fbe2583e
TQID: https://experienceleague.adobe.com/-1FEosKnw-h8hRoK-VTO9VZsi5vIghnMnZp-fUUXo2U
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 737
ht-degree: 35%

---

# Download di dati in un file CSV

Scarica i dati in formato .csv per l&#39;importazione rapida in [!DNL Excel], [!DNL Access] o altri programmi di analisi dei dati.

Per scaricare i dati in un file CSV:

1. Fai clic su **[!UICONTROL Attività]**, quindi sull’attività desiderata tra quelle elencate.

   Se hai numerose attività, fai clic sull&#39;icona Filtro ( ![icona Filtro](/help/main/assets/icons/Filter.svg) ) per filtrare l&#39;elenco selezionando le opzioni dagli elenchi a discesa [!UICONTROL Tipo], [!UICONTROL Stato], [!UICONTROL Source per la generazione di rapporti], [!UICONTROL Compositore esperienza], [!UICONTROL Tipo di metrica] e [!UICONTROL Source attività].

1. Fai clic sulla scheda **[!UICONTROL Rapporti]**.
1. Fai clic sull&#39;icona **[!UICONTROL Scarica]** ( ![Icona Scarica](/help/main/assets/icons/Download.svg) ), quindi seleziona un tipo di rapporto da scaricare per l&#39;analisi in Excel e altri strumenti.

   * [!UICONTROL Esporta rapporti in CSV]
   * [!UICONTROL Esportare i dettagli ordine in CSV]

## [!UICONTROL Esportare un rapporto in formato CSV] {#section_38BD9743EB254453B5F4A0A6F2720CD3}

Il report [!UICONTROL Metriche di successo] mostra informazioni sulle metriche di successo e le metriche seguenti non disponibili nell&#39;interfaccia utente di [!DNL Target]:

* Tempo di conversione medio in ore, per vedere quanto tempo ci vuole in media affinché un visitatore raggiunga il punto di conversione
* Somma dei ricavi al quadrato, per calcoli di affidabilità statistica offline

I dati vengono salvati fino alla fine dell’attività.

>[!NOTE]
>
>Il rapporto CSV include solo dati non elaborati; non include metriche calcolate come ricavi per visitatore, incremento o affidabilità, utilizzate per i test A/B. Per calcolare queste metriche calcolate, scarica il file Excel del [!DNL Target] [calcolatore di affidabilità completo](/help/main/assets/complete_confidence_calculator.xlsx) per immettere il valore dell&#39;attività oppure controlla [i calcoli statistici nei test A/Bn](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

## [!UICONTROL Esportare i dettagli ordine in CSV] {#section_96B3F578F91F4CA3AFE38BACA2A0F11E}

Il report [!UICONTROL Dettagli ordine] mostra informazioni sugli ordini, tra cui:

* Data e ora dell’ordine
* Importo dell’ordine (se è stato inserito una mbox Inserisci ordine)

  Il report [!UICONTROL Dettagli ordine] funziona solo se sono presenti ordini.

* Flag ordine (per ordini duplicati o estremi)

  Un ordine è contrassegnato come estremo se è superiore a +/- 3 deviazioni standard dal valore medio dell’ordine. Questo calcolo utilizza l’ultimo mese di dati (fino al momento in cui è stato eseguito il calcolo). Da un’attività verranno esclusi gli ordini estremi dopo che sarà stata eseguita per un’ora o dopo 15 ordini, a seconda di quale evento si verifica per primo. Per ulteriori informazioni, consulta [Esclusione di ordini estremi](/help/main/c-reports/c-report-settings/excluding-extreme-orders.md#task_2AE7743FFCDD466DAEEB720BE5F33DAA).

* ID prodotto

  La lunghezza totale degli ID prodotto, concatenati con virgole, non deve superare i 255 caratteri o gli ID non vengono visualizzati correttamente nel rapporto. Ad esempio, se l’ordine ha prodotti con ID “aa, bb”, la lunghezza totale è “aa, bb” = 5.

* Esperienza

  Nel report [!UICONTROL Dettagli ordine] per le attività [!UICONTROL Test A/B], [!UICONTROL Targeting esperienza] (XT) e [!UICONTROL Test multivariato] (MVT), la colonna [!UICONTROL Esperienza] contiene l&#39;esperienza `localId`. Si tratta del valore restituito da `$campaign.recipe.id` nei token dell’offerta.

  Non esiste una colonna [!UICONTROL Esperienze] per le attività [!UICONTROL Personalizzazione automatica] (AP). La colonna [!UICONTROL Nome algoritmo] corrente è stata sostituita da &quot;Controllo&quot; rispetto a &quot;Destinato&quot;, come mostrato altrove in [!DNL Target].

  Non vi è stato alcun impatto sulle attività [!UICONTROL Consigli].

>[!NOTE]
>
>* I dati del rapporto di ordine includono quattro settimane di dati per l’ambiente predefinito (gruppo host) e due settimane per tutti gli ambienti non predefiniti.
>* Le metriche dei ricavi impostate su &quot;[!UICONTROL Incrementa il conteggio e mantieni l&#39;utente nell&#39;attività]&quot; registrano i dettagli solo per il primo ordine effettuato dallo stesso visitatore. Tutti gli ordini successivi aumentano il conteggio delle conversioni, ma non aggiungono ricavi a RPV/AOV/Sales e non sono inclusi nel rapporto [!UICONTROL Dettagli ordine].

## Best practice

* Per registrare un record dell&#39;ordine, è necessario passare il parametro `orderTotal`.
* I valori passati tramite il parametro mbox `ProductPurchasedId` sono elencati nel report [!UICONTROL Dettagli ordine].
* Si consiglia di includere `orderID` e `orderTotal`. Questo consente di ignorare automaticamente eventuali ordini duplicati.

## Avvertenze {#section_49B9590904A645B18E694B4EFFFC1DEF}

Le informazioni seguenti si applicano all&#39;opzione [!UICONTROL Scarica]:

* È possibile scaricare entrambi i rapporti per [!UICONTROL attività Test A/B], [!UICONTROL Automated Personalization], [!UICONTROL Targeting esperienza] e [!UICONTROL attività multivariate]. Impossibile scaricare il report [!UICONTROL Metriche di successo] per le attività [!UICONTROL Consigli].
* L&#39;opzione [!UICONTROL Scarica] non è disponibile per le attività [!UICONTROL Test A/B] e [!UICONTROL Targeting esperienza] create prima della versione [!DNL Target] 15.7.1 (luglio 2015).
* Le esperienze a cui non sono associati dati non vengono registrate nel rapporto scaricato.
* I tipi di pubblico applicati nell&#39;interfaccia utente di reporting di [!DNL Target] non vengono trasferiti al report di download.
* I rapporti generati per il download come file .csv non sono coerenti se l’attività utilizza più di una metrica. Il rapporto scaricabile viene generato solo in base alle impostazioni del rapporto e considera lo stesso valore per tutte le altre metriche utilizzate. L’origine di riferimento è sempre il rapporto visualizzato nell’interfaccia utente [!DNL Target].
