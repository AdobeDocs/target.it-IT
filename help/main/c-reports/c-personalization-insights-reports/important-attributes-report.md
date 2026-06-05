---
keywords: Targeting;rapporto AP;rapporti di personalizzazione automatizzata;targeting automatico;auto targeting;rapporto di targeting automatico;report di targeting automatico;personalizzazione;approfondimenti;FAQ;domande frequenti;attributi importanti
description: Scopri come utilizzare il rapporto [!UICONTROL Attributi importanti] che mostra gli attributi principali che hanno influenzato il modello di personalizzazione e la loro importanza relativa.
title: Cos’è il rapporto Attributi importanti?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Reports
exl-id: c1069ca7-e221-4865-a82e-6cff5b4c0055
TQID: https://experienceleague.adobe.com/4G8mYap2O5RW5wr9YvXEaHm2k-oNQVVCHyKv4ltaNHo
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 1937
ht-degree: 61%

---

# Rapporto Attributi importanti

Informazioni sul report [!UICONTROL Attributi importanti], uno dei due report specializzati disponibili per gli utenti di [!UICONTROL attività di Automated Personalization] (AP) e [!UICONTROL Targeting automatico] (AT).

>[!NOTE]
>
>Quando si utilizzano i report [!UICONTROL Personalization Insights], considera quanto segue:
>
>* Le attività di AP e AT sono disponibili come parte della soluzione [!DNL Target Premium]. Non sono disponibili in [!DNL Target Standard] senza una licenza di [!DNL Target Premium].
>
>* I report [!UICONTROL Personalization Insights] sono disponibili solo per le attività di AP e AT che utilizzano un obiettivo di ottimizzazione della conversione. Anche le attività in cui l&#39;obiettivo di ottimizzazione è stato modificato in conversione da ricavi dopo che l&#39;attività era già attiva non sono supportate.
>
>* I report [!UICONTROL Personalization Insights] sono disponibili solo se l&#39;obiettivo principale  è selezionato dall&#39;elenco a discesa [!UICONTROL Metrica report].
>
>* I rapporti di [!UICONTROL Personalization Insights] sono supportati solo nell&#39;[ambiente predefinito](/help/main/administrating-target/hosts.md).
>
>* I report [!UICONTROL Personalization Insights] vengono generati solo per le attività che si trovano nello stato [!UICONTROL Live] e che sono state attivate e ricevono traffico per almeno 15 giorni.

Nelle varie attività, i vari attributi possono essere più o meno importanti per il modo in cui il modello decide di personalizzare. Questo rapporto mostra gli attributi principali che hanno influenzato il modello e la loro importanza relativa.

## Accedi al report [!UICONTROL Attributi importanti] {#section_8E8F997AAAF44A1B9EE06EB6FB652801}

1. Fai clic su **[!UICONTROL Attività]**, quindi sull&#39;attività [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) o [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) desiderata tra quelle elencate.

   Se hai numerose attività, fai clic sull&#39;icona Filtro ( ![icona Filtro](/help/main/assets/icons/Filter.svg) ) per filtrare l&#39;elenco selezionando le opzioni dagli elenchi a discesa [!UICONTROL Tipo], [!UICONTROL Stato], [!UICONTROL Source per la generazione di rapporti], [!UICONTROL Compositore esperienza], [!UICONTROL Tipo di metrica] e [!UICONTROL Source attività].

1. Fai clic su **[!UICONTROL Report]**.

   Viene visualizzato il report [Riepilogo Automated Personalization](/help/main/c-reports/personalization-reports/reports-ap.md) o [Riepilogo Targeting automatico](/help/main/c-reports/personalization-reports/auto-target-summary-report.md), che fornisce informazioni sulle prestazioni delle attività, rappresentate dall&#39;icona della prima schermata. Le due icone aggiuntive rappresentano i due rapporti [!UICONTROL Personalization Insights]: **[!UICONTROL Segmenti automatizzati]** ( ![Rapporto Segmenti automatizzati](/help/main/assets/icons/AutomatedSegment.svg) ) e **[!UICONTROL Attributi importanti]** ( ![Icona Attributi importanti](/help/main/assets/icons/ViewList.svg) ).


   [!UICONTROL Targeting automatico] ha un&#39;ulteriore icona di grafico per la visualizzazione grafica del report [!UICONTROL Riepilogo].

   >[!IMPORTANT]
   >
   >Il report [!UICONTROL Attributi importanti] non sarà disponibile per almeno 15 giorni dopo l&#39;attivazione dell&#39;attività. Durante questo periodo iniziale, non potrai accedere a questo report o fare clic sull’icona di [!UICONTROL Attributi importanti]. Trascorsi 15 giorni, supponendo che la tua attività abbia un traffico personalizzato sufficiente, il rapporto [!UICONTROL Attributi importanti] è disponibile.

1. A 15 giorni dall&#39;attivazione dell&#39;attività, fai clic sull&#39;icona **[!UICONTROL Attributi importanti]** ( ![Icona Attributi importanti](/help/main/assets/icons/ViewList.svg) ).

1. Seleziona l&#39;intervallo di date desiderato.

   A differenza del rapporto [!UICONTROL Riepilogo] (rapporto sulle prestazioni), [!UICONTROL Personalization Insights], incluso [!UICONTROL Attributi importanti], è disponibile solo per intervalli di date fissi: 15 giorni, 30 giorni e 60 giorni.

   Questi intervalli di date fissi consentono a [!UICONTROL Registri di personalizzazione] di utilizzare una gamma di dati abbastanza ampia da ridurre la probabilità di trarre informazioni da un modello di breve durata all&#39;interno dell&#39;attività. Le due decisioni che puoi prendere per l&#39;intervallo di date sono “Data di fine” e “Durata”. Noterai che “Start” è inattivo. La data di inizio cambia automaticamente in base alla data di fine e alla durata selezionate.

   Puoi accedere agli intervalli di date fissi disponibili dall&#39;elenco a discesa [!UICONTROL Intervallo date predefinito].

1. Esamina i dati del rapporto [!UICONTROL Attributi importanti].

1. (Facoltativo) Fai clic sull&#39;icona Scarica ( ![icona Scarica](/help/main/assets/icons/Download.svg) ) per [scaricare il rapporto in formato CSV](/help/main/c-reports/c-report-settings/report-settings.md#section_77E65C50BAAF4AB79242DB3A8778ADEF) per l&#39;analisi in Excel e altri strumenti.

   >[!NOTE]
   >
   >Il rapporto dell’interfaccia utente di Registri di personalizzazione contiene informazioni selezionate. Il CSV scaricabile per il rapporto Attributi importanti contiene ulteriori dettagli. Il download del rapporto Attributi importanti include l&#39;elenco completo dei 100 attributi principali, mentre il rapporto dell&#39;interfaccia utente include soltanto i primi 10. Se non trovi un attributo specifico nel rapporto, ciò non significa che questo non sta influenzando l&#39;attività, ma semplicemente che non è rientrato nella lista dei primi 100.

## Interpretare il rapporto Attributi importanti

La tabella seguente spiega come interpretare il rapporto e ne descrive gli elementi:

| Elemento | Dettagli |
|--- |--- |
| Grafico a barre | Il grafico a barre multicolore nella parte superiore dello schermo consente di visualizzare questi punteggi e mappe di importanza relativa con il colore del punto accanto a ciascun attributo nella tabella. Puoi anche passare il puntatore su un colore specifico nel grafico a barre per visualizzare l’attributo che rappresenta.  I punteggi di importanza dei 100 attributi principali totalizzano il 100%. Per ulteriori informazioni su come aggiungere altri attributi utilizzabili dai modelli di personalizzazione di Target, vedere [Caricamento di dati per gli algoritmi di Personalization di Target](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md). |
| Grafico di Classifica Attributi del Modello | Il grafico di Classifica Attributi del Modello include i 10 attributi principali, ovvero i più importanti nel criterio con cui il modello di personalizzazione di Target ha fatto visualizzare un determinato contenuto a ciascun visitatore. Il punteggio di importanza mostra, relativamente ai 100 attributi principali, quanto è stato importante un determinato attributo per i modelli di personalizzazione di Target in questa attività. |

## Domande frequenti sugli attributi importanti {#section_740910A52FA646B4AC9452F98C2F5719}

Consulta le seguenti domande frequenti per le risposte alle domande più frequenti sull&#39;utilizzo del report [!UICONTROL Attributi importanti].

### I rapporti Approfondimenti Personalization non sono ancora disponibili per la mia attività. Perché?

Ci sono diversi motivi per cui i rapporti di [!UICONTROL Personalization Insights] potrebbero non essere ancora disponibili per la tua attività:

* non sono trascorsi 15 giorni dall&#39;attivazione dell&#39;attività. I rapporti di Segmenti automatizzati e Attributi importanti non saranno disponibili per almeno 15 giorni dopo l&#39;attivazione dell&#39;attività. Durante questo periodo iniziale, non potrai accedere a questi rapporti o fare clic sulle icone di Segmenti automatizzati e Attributi importanti.
* L&#39;attività non ha avuto traffico a sufficienza durante l’arco temporale specificato. Trascorsi 15 giorni, supponendo che la tua attività abbia un [traffico personalizzato sufficiente](/help/main/c-activities/auto-target/auto-target-to-optimize.md#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB), saranno disponibili i rapporti Segmenti automatizzati e Attributi importanti.
* L&#39;attività ha un obiettivo di ottimizzazione dei profitti. Attualmente, [!UICONTROL Registri di personalizzazione] è disponibile solo per le attività con obiettivo di ottimizzazione della conversione. Il supporto per le attività di ottimizzazione dei profitti verrà aggiunto in una versione futura.

### Che cos’è un attributo?

Un attributo è un&#39;informazione su un visitatore o sulla sua visita specifica che gli algoritmi di personalizzazione utilizzano per imparare a personalizzare il traffico. Gli attributi possono essere, ad esempio, il tipo di browser, la posizione, l&#39;orario della visita e così via.

Per ulteriori informazioni sugli attributi utilizzati da [!DNL Target] nei modelli di personalizzazione, consulta [Raccolta di dati per gli algoritmi di personalizzazione di Target](/help/main/c-activities/t-automated-personalization/ap-data.md). Per ulteriori informazioni su come caricare in Target nuovi attributi da utilizzare nei modelli di personalizzazione di Target, vedi [Metodi per immettere i dati in Target](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=it){target=_blank}.

### Visualizzo uno o più attributi che non desidero che il modello utilizzi per la formazione. Posso rimuovere questi attributi dal modello di formazione? {#models-api}

L&#39;API [!UICONTROL Models], denominata anche API di Inserisce nell&#39;elenco Bloccati di Automated Personalization, consente agli utenti di visualizzare e gestire l&#39;elenco di attributi (o funzionalità) utilizzati nei modelli di apprendimento automatico per le attività  (AP) e [!UICONTROL Targeting automatico] (AT). Se vuoi escludere uno o più attributi dall&#39;utilizzo da parte dei modelli per attività di AP o AT, puoi utilizzare l&#39;API dei modelli per aggiungere tali attributi al &quot;inserisco nell&#39;elenco Bloccati di&quot;.

Per informazioni dettagliate, consulta [Panoramica di Models API](https://experienceleague.adobe.com/docs/target-dev/developer/api/models-api/models-api.html){target=_blank} nella *Guida per gli sviluppatori di Adobe Target*. Per utilizzare l&#39;API per bloccare gli attributi, vedere [Models API](https://experienceleague.adobe.com/docs/target-dev/developer/api/models-api/models-api-overview.html){target=_blank}.

### Le informazioni nei rapporti [!UICONTROL Segmenti automatizzati] e [!UICONTROL Attributi importanti] sono le stesse del file CSV scaricabile?

No, il rapporto dell&#39;interfaccia utente contiene specifiche informazioni. Il file CSV scaricabile contiene ulteriori dettagli. Il download del rapporto di Registri di segmento automatizzato comprende altri Segmenti automatizzati oltre ai segmenti principali inclusi nell&#39;interfaccia utente, così come le prestazioni di quei segmenti rispetto alle offerte o esperienze. Il rapporto di Attributi importanti include i principali 100 attributi dei visitatori e l&#39;importanza relativa, mentre l&#39;interfaccia utente include solo i 10 attributi principali.

### Posso visualizzare Personalization Insights per un intervallo di date personalizzato?

Il report di Registri di personalizzazione (sia per [!UICONTROL Segmenti automatizzati] sia per [!UICONTROL Attributi importanti]) è disponibile solo per intervalli di date fissi: 15 giorni, 30 giorni, 45 giorni, 60 giorni e 90 giorni. Questi intervalli di date fissi consentono a [!UICONTROL Registri di personalizzazione] di utilizzare una gamma di dati abbastanza ampia da ridurre la probabilità di trarre informazioni da un modello di breve durata all&#39;interno dell&#39;attività. Puoi selezionare queste durate per qualsiasi data di fine (laddove vi siano dati a sufficienza per soddisfare la durata).

### Come viene creato [!UICONTROL Personalization Insights]?

[!UICONTROL Registri di personalizzazione viene creato tramite una tecnica di Adobe in attesa di licenza denominata MAGIX (Model Agnostic Globally Interpretable Explanations).] Per ulteriori informazioni su MAGIX, consulta il documento pubblicato del team di ricerca Adobe sul [arXiv.org sito Web](https://arxiv.org/abs/1706.07160).

### Sono disponibili [!UICONTROL Personalization Insights] per obiettivi di modeling/obiettivi primari basati sui ricavi?

Attualmente, [!UICONTROL Registri di personalizzazione] è disponibile solo per le attività con obiettivo di ottimizzazione della conversione. Il supporto per le attività di ottimizzazione dei profitti verrà aggiunto in una versione futura.

### Qual è il punteggio di importanza dell&#39;attributo nel rapporto Attributi importanti?

Il punteggio di importanza nella sezione “Classifica di Importanza degli Attributi” del rapporto fornisce input sulle variabili, utilizzate dall&#39;algoritmo per apprendere, che sono state più importanti nel determinare la suddivisione di tutti i visitatori nei segmenti che identificava. Ha assegnato un punteggio percentuale ai 100 attributi principali utilizzati dal modello.

### Perché alcune offerte/esperienze con un tasso di conversione inferiore ricevono una maggiore quantità di traffico rispetto ad altre per un determinato segmento automatizzato?

Vi sono vari motivi per cui potresti vedere più visite per un’offerta o esperienza a basso tasso di conversione in un segmento automatizzato, tra cui:

* Un basso numero di visualizzazioni per alcune o tutte le offerte/esperienze per un determinato segmento automatizzato.
* Attività dal volume ridotto con alcune offerte o esperienze prive di modelli.
* Attività dal volume ridotto in cui i modelli sono stati creati prima per alcune offerte o esperienze rispetto ad altre. Questo si verifica, ad esempio, se un modello aggiuntivo è stato creato il giorno 22 e si esaminano i dati relativi ai giorni 10-24.
* Regole di targeting di una particolare offerta in base alle quali alcuni visitatori non possono visualizzare una determinata offerta o esperienza.
* Assenza di intervalli di affidabilità nella generazione dei rapporti Approfondimenti. Tuttavia, se i tassi di conversione sono abbastanza vicini, il modello potrebbe distribuire il traffico in modo che sia più alto nella quantità di punti, ma non sono numeri &quot;statisticamente diversi&quot;.

È utile sapere come funziona il modello in base al quale viene distribuito il traffico. Ogni persona riceve i contenuti in base al suo profilo totale. Tuttavia, i rapporti Approfondimenti generalizzano questo comportamento per facilitarne l’interpretazione. Di conseguenza, i segmenti non si escludono a vicenda. Di conseguenza questo tipo di comportamento può interessare singoli segmenti perché una stessa persona può essere inclusa in più segmenti.

### Quali sono i diversi modi in cui posso sfruttare le informazioni in Personalization Insights?

* Scopri nuovi tipi di pubblico: se vedi un segmento automatizzato dalle prestazioni particolarmente buone, puoi creare un pubblico per riutilizzare tale segmento in altri rapporti.
* Verifica le tue ipotesi sui tipi di visitatori che risponderanno a determinate esperienze.
* Scopri i contenuti che hanno funzionato per determinati tipi di visitatori: le offerte che hanno avuto maggiore riscontro.
* Individua il contenuto con le prestazioni più basse.
* Scopri gli attributi cruciali per l&#39;apprendimento del modello.
* Scopri gli attributi utilizzati nei modelli di personalizzazione e la loro importanza.
* Individua le opportunità per ulteriori punti di dati da trasmettere a Target per informare ulteriormente la tua personalizzazione.

## Problemi noti

Il seguente problema è attualmente in fase di analisi da parte del team di progettazione [!DNL Target].

* I nomi dei segmenti [!DNL Adobe Experience Platform] non vengono visualizzati nel report [!UICONTROL Attributi importanti] per le attività [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Targeting automatico] (AT). (TOP-3813)
