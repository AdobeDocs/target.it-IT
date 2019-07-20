---
description: Informazioni sul rapporto Attributi importanti, uno dei due rapporti specializzati disponibili per gli utenti delle attività di Personalizzazione automatizzata (AP) e Targeting automatico (AT).
keywords: Targeting;rapporto AP;rapporti di personalizzazione automatizzata;targeting automatico;auto targeting;rapporto di targeting automatico;report di targeting automatico;personalizzazione;approfondimenti;FAQ;domande frequenti;attributi importanti
seo-description: Informazioni sul rapporto Attributi importanti, uno dei due rapporti specializzati disponibili per gli utenti delle attività di Personalizzazione automatizzata (AP) e Targeting automatico (AT).
seo-title: Rapporto Attributi importanti
solution: Target
title: Rapporto Attributi importanti
title-outputclass: premium
uuid: c03bf806-0b03-4315-a176-4eaa9250a271
badge: premium
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# ![PREMIUM](/help/assets/premium.png) Rapporto Attributi importanti{#important-attributes-report}

Informazioni sul rapporto Attributi importanti, uno dei due rapporti specializzati disponibili per gli utenti delle attività di Personalizzazione automatizzata (AP) e Targeting automatico (AT).

>[!NOTE]
>Le attività di AP e AT sono disponibili come parte della soluzione Target Premium. Non sono disponibili in Target Standard senza una licenza di Target Premium.
>
>I rapporti di Approfondimenti personalizzazione sono disponibili solo per le attività di AP e AT che utilizzano un obiettivo di ottimizzazione delle conversioni. Anche le attività in cui l'obiettivo di ottimizzazione è stato modificato in conversione da ricavi dopo che l'attività era già attiva non sono supportate.|

Nelle varie attività, i vari attributi possono essere più o meno importanti per il modo in cui il modello decide di personalizzare. Questo rapporto mostra gli attributi principali che hanno influenzato il modello e la loro importanza relativa.

## Accedere al rapporto Attributi importanti {#section_8E8F997AAAF44A1B9EE06EB6FB652801}

1. Fai clic su **[!UICONTROL Attività]**, quindi sull’attività di [AP](../../c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) o [AT](../../c-activities/auto-target-to-optimize.md#concept_67779E5B7F67427A97D7EA2A6FB919B3) desiderata tra quelle elencate.

   Se hai numerose attività, puoi filtrare l’elenco selezionando le opzioni che ti interessano dagli elenchi a discesa [!UICONTROL Tipo], [!UICONTROL Stato], [!UICONTROL Origine per i rapporti], [!UICONTROL Compositore esperienza], [!UICONTROL Tipo di metrica] e [!UICONTROL Origine attività].

1. Fai clic su **[!UICONTROL Rapporto]**.

   Viene visualizzato il rapporto di [!UICONTROL Riepilogo], che fornisce informazioni sulle prestazioni delle attività, rappresentate dall'icona della prima schermata. Le altre due icone rappresentano i due rapporti di Registri di personalizzazione: Segmenti automatizzati e Attributi importanti. Tieni presente che Targeting automatico ha un'ulteriore icona di grafico per la visualizzazione grafica del rapporto di [!UICONTROL Riepilogo].

   ![](assets/personalization_insights.png)

   >[!IMPORTANT]
   >
   >Il rapporto [!UICONTROL Attributi importanti] non sarà disponibile per almeno 15 giorni dopo l’attivazione dell’attività. Durante questo periodo iniziale, non potrai accedere a questo rapporto o fare clic sull’icona di [!UICONTROL Attributi importanti]. Trascorsi 15 giorni, supponendo che la tua attività abbia un traffico personalizzato sufficiente, sarà disponibile il rapporto [!UICONTROL Attributi importanti].

1. A 15 giorni dall'attivazione dell'attività, puoi fare clic sull'icona **[!UICONTROL Attributi importanti]**.

   ![](assets/model_attribute_ranking.png)

1. Seleziona l'intervallo di date desiderato.

   A differenza del rapporto di [!UICONTROL Riepilogo] (rapporto sulle prestazioni), [!UICONTROL Registri di personalizzazione], incluso [!UICONTROL Attributi importanti], è disponibile solo per intervalli di date fissi: 15 giorni, 30 giorni, 45 giorni, 60 giorni e 90 giorni. Questi intervalli di date fissi consentono a [!UICONTROL Registri di personalizzazione] di utilizzare una gamma di dati abbastanza ampia da ridurre la probabilità di trarre informazioni da un modello di breve durata all'interno dell'attività. Le due decisioni che puoi prendere per l'intervallo di date sono “Data di fine” e “Durata”. Noterai che “Start” è inattivo. La data di inizio cambia automaticamente in base alla data di fine e alla durata selezionate.

   ![](assets/personalization_insights_calendar_1.png)

   Puoi accedere agli intervalli di date fissi disponibili dall'elenco a discesa [!UICONTROL Scegli la durata].

   ![](assets/personalization_insights_calendar_2.png)

1. Esamina i dati del rapporto [!UICONTROL Attributi importanti].

   ![](assets/model_attribute_ranking_report.png)


1. (Facoltativo) [Scarica il rapporto in formato CSV](../../c-reports/c-report-settings/report-settings.md#section_77E65C50BAAF4AB79242DB3A8778ADEF) per l'analisi in Excel e altri programmi.

   >[!NOTE]
   >
   >Il rapporto dell’interfaccia utente di Registri di personalizzazione contiene informazioni selezionate. Il CSV scaricabile per il rapporto Attributi importanti contiene ulteriori dettagli. Il download del rapporto Attributi importanti include l'elenco completo dei 100 attributi principali, mentre il rapporto dell'interfaccia utente include soltanto i primi 10. Se non trovi un attributo specifico nel rapporto, ciò non significa che questo non sta influenzando l'attività, ma semplicemente che non è rientrato nella lista dei primi 100.

## Interpretare il rapporto Attributi importanti

La tabella seguente spiega come interpretare il rapporto e ne descrive gli elementi:

| Elemento | Dettagli |
|--- |--- |
| Grafico a barre | Il grafico a barre multicolore nella parte superiore dello schermo consente di visualizzare questi punteggi e mappe di importanza relativa con il colore del punto accanto a ciascun attributo nella tabella. Puoi anche posizionare il cursore su un colore specifico nel grafico a barre per visualizzare l'attributo che rappresenta.  I punteggi di importanza dei 100 attributi principali totalizzano il 100%. Per ulteriori informazioni sull’aggiunta di altri attributi utilizzabili dai modelli di personalizzazione di Target, consulta [Caricamento di dati per gli algoritmi di personalizzazione di Target](/help/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md). |
| Grafico di Classifica Attributi del Modello | Il grafico di Classifica Attributi del Modello include i 10 attributi principali, ovvero i più importanti nel criterio con cui il modello di personalizzazione di Target ha fatto visualizzare un determinato contenuto a ciascun visitatore. Il punteggio di importanza mostra, relativamente ai 100 attributi principali, quanto è stato importante un determinato attributo per i modelli di personalizzazione di Target in questa attività. |

## Domande frequenti sugli attributi importanti {#section_740910A52FA646B4AC9452F98C2F5719}

**I rapporti Registri di personalizzazione non sono ancora disponibili per la mia attività. Perché?**

Ci sono vari motivi per cui i rapporti [!UICONTROL Approfondimenti personalizzazione] potrebbero non essere ancora disponibili per la tua attività:

* non sono trascorsi 15 giorni dall'attivazione dell'attività. I rapporti di Segmenti automatizzati e Attributi importanti non saranno disponibili per almeno 15 giorni dopo l'attivazione dell'attività. Durante questo periodo iniziale, non potrai accedere a questi rapporti o fare clic sulle icone di Segmenti automatizzati e Attributi importanti.
* L'attività non ha avuto traffico a sufficienza durante il periodo di tempo specificato. Trascorsi 15 giorni, supponendo che la tua attività abbia un [traffico personalizzato sufficiente](/help/c-activities/auto-target-to-optimize.md#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB), saranno disponibili i rapporti Segmenti automatizzati e Attributi importanti.
* L'attività ha un obiettivo di ottimizzazione dei profitti. Attualmente, [!UICONTROL Registri di personalizzazione] è disponibile solo per le attività con obiettivo di ottimizzazione della conversione. Il supporto per le attività di ottimizzazione dei profitti verrà aggiunto in una versione futura.

**Cos'è un attributo?**

Un attributo è un'informazione su un visitatore o sulla sua visita specifica che gli algoritmi di personalizzazione utilizzano per imparare a personalizzare il traffico. Gli attributi possono essere, ad esempio, il tipo di browser, la posizione, l'orario della visita e così via.

Per ulteriori informazioni sugli attributi utilizzati da [!DNL Target] nei modelli di personalizzazione, consulta [Raccolta di dati per gli algoritmi di personalizzazione di Target](../../c-activities/t-automated-personalization/ap-data.md#reference_255BD3DE7AD04DC9B766E0BC78961058). Per ulteriori informazioni su come caricare in Target nuovi attributi da utilizzare nei modelli di personalizzazione di Target, vedi [Metodi per immettere i dati in Target](../../c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md#concept_0069C0EFB56C4700BB33F2F35C2B9B17).

**Le informazioni nei rapporti di[!UICONTROL Segmenti automatizzati]e[!UICONTROL Attributi importanti]sono le stesse del file CSV scaricabile?**

No, il rapporto dell'interfaccia utente contiene specifiche informazioni. Il file CSV scaricabile contiene ulteriori dettagli. Il download del rapporto di Registri di segmento automatizzato comprende altri Segmenti automatizzati oltre ai segmenti principali inclusi nell'interfaccia utente, così come le prestazioni di quei segmenti rispetto alle offerte o esperienze. Il rapporto di Attributi importanti include i principali 100 attributi dei visitatori e l'importanza relativa, mentre l'interfaccia utente include solo i 10 attributi principali.

**Posso visualizzare Registri di personalizzazione per un intervallo di date personalizzato?**

Il rapporto di Registri di personalizzazione (sia per [!UICONTROL Segmenti automatizzati] sia per [!UICONTROL Attributi importanti]) è disponibile solo per intervalli di date fissi: 15 giorni, 30 giorni, 45 giorni, 60 giorni e 90 giorni. Questi intervalli di date fissi consentono a [!UICONTROL Registri di personalizzazione] di utilizzare una gamma di dati abbastanza ampia da ridurre la probabilità di trarre informazioni da un modello di breve durata all'interno dell'attività. Puoi selezionare queste durate per qualsiasi data di fine (laddove vi siano dati a sufficienza per soddisfare la durata).

**Come viene creato[!UICONTROL Registri di personalizzazione]?**

[!UICONTROL Registri di personalizzazione] viene creato tramite una tecnica di Adobe in attesa di licenza denominata MAGIX (Model Agnostic Globally Interpretable Explanations). Per ulteriori informazioni su MAGIX, consulta il documento pubblicato del team di ricerca Adobe sul sito [arXiv.org](https://arxiv.org/abs/1706.07160).

**[!UICONTROL Registri di personalizzazione]è disponibile per obiettivi di modeling/obiettivi primari basati sui profitti?**

Attualmente, [!UICONTROL Registri di personalizzazione] è disponibile solo per le attività con obiettivo di ottimizzazione della conversione. Il supporto per le attività di ottimizzazione dei profitti verrà aggiunto in una versione futura.

**Qual è il punteggio di importanza dell'attributo nel rapporto relativo agli Attributi importanti?**

Il punteggio di importanza nella sezione “Classifica di Importanza degli Attributi” del rapporto fornisce input sulle variabili, utilizzate dall'algoritmo per apprendere, che sono state più importanti nel determinare la suddivisione di tutti i visitatori nei segmenti che identificava. Ha assegnato un punteggio percentuale ai 100 attributi principali utilizzati dal modello.

**Perché alcune offerte/esperienze con un tasso di conversione inferiore ricevono una maggiore quantità di traffico rispetto ad altre per un determinato segmento automatizzato?**

Esistono diversi motivi potenziali per vedere più visite a un'offerta/esperienza di conversione inferiore all'interno di un segmento automatizzato, inclusi:

* Un basso numero di visite ad alcune o tutte le offerte/esperienze per un determinato segmento automatizzato.
* Attività più basse in cui determinate offerte o esperienze non sono dotati di modelli.
* Attività più basse in cui i modelli venivano creati prima per alcune offerte/esperienze rispetto ad altri. Ad esempio, supponiamo che un modello aggiuntivo sia stato creato il giorno 22 e che i dati vengano visti dai giorni 10-24.
* Regole di targeting su un'offerta specifica che limita i visitatori in grado di vedere quali offerte o esperienze sono disponibili.
* Non ci sono intervalli di confidenza nella generazione dei rapporti. Tuttavia, se i tassi di conversione sono sufficientemente vicini, il modello potrebbe distribuire il traffico in modo che sia più elevato nell'importo in punti, ma non i numeri statisticamente diversi.

È utile sapere come funziona il modello per distribuire il traffico. Ogni individuo viene distribuito in base al suo profilo totale. Tuttavia, i report Approfondimenti generalizzano questo comportamento per renderlo più interpretografabile da un uomo. Di conseguenza, i segmenti non si escludono a vicenda. Questo può portare a singoli segmenti che mostrano questo tipo di comportamento, perché la stessa persona può essere visualizzata in più segmenti.

**Come posso sfruttare le informazioni in Registri di personalizzazione?**

* Scopri un nuovo gruppo di destinatari: se vedi un segmento automatizzato dalle prestazioni particolarmente buone, puoi creare un gruppo di destinatari per riutilizzare il segmento in altri rapporti.
* Verifica le tue ipotesi sui tipi di visitatori che risponderanno a determinate esperienze.
* Scopri i contenuti che hanno funzionato per determinati tipi di visitatori: le offerte che hanno avuto maggiore riscontro.
* Individua il contenuto con le prestazioni più basse.
* Scopri gli attributi cruciali per l'apprendimento del modello.
* Scopri gli attributi utilizzati nei modelli di personalizzazione e la loro importanza.
* Individua le opportunità per ulteriori punti di dati da trasmettere a Target per informare ulteriormente la tua personalizzazione.