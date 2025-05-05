---
keywords: Targeting;rapporto AP;rapporti di personalizzazione automatizzata;targeting automatico;targeting automatico;rapporto di targeting automatico;report di targeting automatico;personalizzazione;approfondimenti;segmenti automatizzati;FAQ;domande frequenti
description: Scopri in che modo i diversi segmenti definiti dai modelli di personalizzazione Adobe [!DNL Target] rispondono alle offerte o esperienze dell'attività visualizzando il rapporto Segmenti automatizzati.
title: Cos’è il rapporto Segmenti automatizzati?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Reports
exl-id: d21517b7-770b-4618-9899-7ac4948c2a8b
source-git-commit: c1a71d1fb6fa9b5c14e22fa3199358a4594bb4a1
workflow-type: tm+mt
source-wordcount: '2066'
ht-degree: 59%

---

# Report [!UICONTROL Automated Segments]

Informazioni sul report [!UICONTROL Automated Segments], uno dei due report specializzati disponibili per gli utenti di [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Auto-Target] (AT) attività.

>[!NOTE]
>
>Quando si utilizzano i report [!UICONTROL Personalization Insights], tenere presente quanto segue:
>
>* Le attività di AP e AT sono disponibili come parte della soluzione [!DNL Target Premium]. Non sono disponibili in [!DNL Target Standard] senza una licenza di [!DNL Target Premium].
>
>* I report [!UICONTROL Personalization Insights] sono disponibili solo per le attività di AP e AT che utilizzano un obiettivo di ottimizzazione della conversione. Anche le attività in cui l&#39;obiettivo di ottimizzazione è stato modificato in conversione da ricavi dopo che l&#39;attività era già attiva non sono supportate.
>
>* I report [!UICONTROL Personalization Insights] sono disponibili solo se [!UICONTROL Primary Goal] è selezionato dall&#39;elenco a discesa [!UICONTROL Report Metric].
>
>* [!UICONTROL Personalization Insights] report sono supportati solo nell&#39;[ambiente predefinito](/help/main/administrating-target/hosts.md).
>
>* I report [!UICONTROL Personalization Insights] vengono generati solo per le attività che si trovano nello stato [!UICONTROL Live] e che sono state attivate e ricevono traffico per almeno 15 giorni.

I vari visitatori rispondono in modo diverso alle offerte/esperienze nell&#39;attività di AP/AT. Questo rapporto mostra come i diversi segmenti automatizzati definiti dai modelli di personalizzazione di Target rispondono alle offerte/esperienze dell&#39;attività.

## Accedere al rapporto Segmenti automatizzati {#section_8E8F997AAAF44A1B9EE06EB6FB652801}

1. Fai clic su **[!UICONTROL Activities]**, quindi sull&#39;attività [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) o [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) desiderata tra quelle elencate.

   Se hai numerose attività, fai clic sull&#39;icona Filtro ( ![icona Filtro](/help/main/assets/icons/Filter.svg) ) per filtrare l&#39;elenco selezionando le opzioni dagli elenchi a discesa [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type] e [!UICONTROL Activity Source].

1. Fare clic su **[!UICONTROL Reports]**.

   Viene visualizzato il report [Riepilogo Automated Personalization](/help/main/c-reports/personalization-reports/reports-ap.md) o [Riepilogo Targeting automatico](/help/main/c-reports/personalization-reports/auto-target-summary-report.md), che fornisce informazioni sulle prestazioni delle attività, rappresentate dall&#39;icona della prima schermata. Le due icone aggiuntive rappresentano i due rapporti [!UICONTROL Personalization Insights]: **[!UICONTROL Automated Segments]** ( ![Rapporto Segmenti automatizzati](/help/main/assets/icons/AutomatedSegment.svg) ) e **[!UICONTROL Important Attributes]** ( ![Icona Attributi importanti](/help/main/assets/icons/ViewList.svg) ). Il Targeting automatico ha un&#39;icona di grafico aggiuntiva per la visualizzazione grafica del report [!UICONTROL Summary].

   >[!IMPORTANT]
   >
   >Il report [!UICONTROL Automated Segments] non sarà disponibile per almeno 15 giorni dopo l&#39;attivazione dell&#39;attività. Durante questo periodo iniziale, non potrai accedere a questo report o fare clic sull&#39;icona [!UICONTROL Automated Segments]. Trascorsi 15 giorni, supponendo che la tua attività abbia un traffico personalizzato sufficiente, il rapporto [!UICONTROL Automated Segments] sarà disponibile.

1. A 15 giorni dall&#39;attivazione dell&#39;attività, puoi fare clic sull&#39;icona **[!UICONTROL Automated Segments]**.

1. Seleziona l&#39;intervallo di date desiderato.

   A differenza del rapporto [!UICONTROL Summary] (rapporto sulle prestazioni), [!UICONTROL Personalization Insights], incluso [!UICONTROL Automated Segments], è disponibile solo per intervalli di date fissi: 15 giorni, 30 giorni e 60 giorni. Questi intervalli di date fissi consentono a [!UICONTROL Personalization Insights] di utilizzare un intervallo di dati sufficientemente ampio per ridurre la probabilità che si ottengano informazioni da un pattern di breve durata nell&#39;attività. Le due decisioni che puoi prendere per l&#39;intervallo di date sono “Data di fine” e “Durata”. Noterai che &quot;Start&quot; è inattivo. La data di inizio cambia automaticamente in base alla data di fine e alla durata selezionate.

   È possibile accedere agli intervalli di date fissi disponibili dall&#39;elenco a discesa [!UICONTROL Preset Date Range].

1. Esaminare i dati del report [!UICONTROL Automated Segments].

1. (Facoltativo) Fai clic sull&#39;icona **[!UICONTROL Download]** ( ![Icona Scarica](/help/main/assets/icons/Download.svg) ) per [scaricare il rapporto in formato CSV](/help/main/c-reports/c-report-settings/report-settings.md#section_77E65C50BAAF4AB79242DB3A8778ADEF) per l&#39;analisi in Excel e altri strumenti.

   >[!NOTE]
   >
   >Il rapporto dell’interfaccia utente di Registri di personalizzazione contiene informazioni selezionate. Il file CSV scaricabile per il rapporto Segmenti automatizzati contiene ulteriori dettagli. Il file scaricabile del rapporto di Segmenti automatizzati comprende altri Segmenti automatizzati oltre ai segmenti principali inclusi nell&#39;interfaccia utente, così come le prestazioni di quei segmenti rispetto alle offerte o esperienze.

## Interpretare il rapporto Segmenti automatizzati

La tabella seguente spiega come interpretare il rapporto e ne descrive gli elementi:

| Elemento | Dettagli |
|--- |--- |
| Pannello laterale sinistro | Nel pannello laterale sinistro sono elencati i 20 “segmenti automatizzati” più grandi identificati dai modelli di personalizzazione di Target per questa attività. Un “segmento automatizzato” è una sorta di pubblico, che però è definito dai modelli di personalizzazione di Target anziché dall’addetto al marketing. Ciascun segmento automatizzato è composto da valori specifici (o intervalli di valore) di attributi specifici.<br>I segmenti automatizzati possono sovrapporsi. I segmenti automatizzati possono essere definiti da uno, due, tre o quattro attributi. Per ulteriori informazioni, consulta gli esempi seguenti.<br>Per ulteriori informazioni sui modelli di personalizzazione di Target, consulta [Algoritmo Foresta casuale](/help/main/c-activities/t-automated-personalization/algo-random-forest.md). Per ulteriori informazioni sugli attributi utilizzati dai modelli di personalizzazione di Target per creare i segmenti automatizzati, consulta [Raccolta di dati per gli algoritmi di personalizzazione di Target](/help/main/c-activities/t-automated-personalization/ap-data.md). |
| Grafico centrale | I grafici centrali mostrano le prestazioni del contenuto dell’attività per il segmento automatico evidenziato. Quando fai clic sui vari segmenti nel pannello a sinistra, si aggiornano i grafici centrali. |
| Grafici a torta | I grafici a torta nella parte superiore del pannello centrale mostrano le dimensioni del segmento automatizzato e il numero totale di visite personalizzate nell&#39;attività (ad esempio, il traffico verso l&#39;attività gestito dal modello di personalizzazione. Non include il traffico di controllo o il traffico gestito dal modello vincitore complessivo). La dimensione del segmento si basa solo su visite personalizzate.<br>![Grafico a torta](/help/main/c-reports/assets/pie.png) |
| Istogramma a doppio asse | L&#39;istogramma a doppio asse include le informazioni sulle visite e sulle conversioni dell&#39;offerta o esperienza per quel segmento automatizzato specifico. |
| Barra rosa | La barra rosa rappresenta il tasso di conversione e utilizza l&#39;asse inferiore del grafico. Posiziona il puntatore sulla barra per ulteriori informazioni |
| Barra blu | La barra blu rappresenta il numero di visite e utilizza l&#39;asse superiore del grafico. Posiziona il puntatore sulla barra per ulteriori informazioni. |
| Linea punteggiata grigia | La linea punteggiata grigia rappresenta il tasso di conversione per tutte le visite personalizzate nell&#39;attività, in tutte le offerte/esperienze e nei segmenti automatizzati. |

**Segmento automatizzato, esempio 1**

Questo segmento automatizzato viene definito in base a un solo attributo. I visitatori inclusi nel segmento automatizzato hanno visualizzato questa attività di Personalizzazione automatizzata in un giorno feriale al di fuori del normale orario lavorativo o in un weekend.

![Esempio di rapporto Segmenti automatizzati 1](/help/main/c-reports/assets/automated_segment_example_1.png)

**Segmento automatizzato, esempio 2**

Questo segmento automatizzato viene definito in base a due attributi. I visitatori inclusi in questo segmento automatizzato che hanno visualizzato questa attività di Personalizzazione automatizzata hanno effettuato meno di tre visualizzazioni nella visita in questione ed erano geograficamente localizzati a una latitudine tra 42.57 e 47.29 (all&#39;incirca tra New Hampshire/Oregon e Washington/Maine per una società con sede negli Stati Uniti).

![Rapporto Segmenti automatizzati, esempio 2](/help/main/c-reports/assets/automated_segment_example_2.png)

## Domande frequenti sui Segmenti automatizzati {#section_740910A52FA646B4AC9452F98C2F5719}

**I rapporti Registri di personalizzazione non sono ancora disponibili per la mia attività. Perché?**

Ci sono diversi motivi per cui i report [!UICONTROL Personalization Insights] non sono ancora disponibili per l&#39;attività:

* Non sono trascorsi 15 giorni dall’attivazione dell’attività. I rapporti di Segmenti automatizzati e Attributi importanti non saranno disponibili per almeno 15 giorni dopo l&#39;attivazione dell&#39;attività. Durante questo periodo iniziale, non potrai accedere a questi rapporti o fare clic sulle icone di Segmenti automatizzati e Attributi importanti.
* L&#39;attività non ha avuto traffico a sufficienza durante l’arco temporale specificato. Trascorsi 15 giorni, supponendo che la tua attività abbia un traffico personalizzato sufficiente, saranno disponibili i rapporti Segmenti automatizzati e Attributi importanti.
* L&#39;attività ha un obiettivo di ottimizzazione dei profitti. Attualmente, [!UICONTROL Personalization Insights] è disponibile solo per le attività con obiettivo di ottimizzazione della conversione. In una versione futura, Adobe aggiungerà il supporto per le attività con obiettivo di ottimizzazione dei ricavi.

**Cos&#39;è un attributo?**

Un attributo è un&#39;informazione su un visitatore o sulla sua visita specifica che gli algoritmi di personalizzazione utilizzano per imparare a personalizzare il traffico. Gli attributi possono essere, ad esempio, il tipo di browser, la posizione, l&#39;orario della visita e così via.

Per ulteriori informazioni sugli attributi utilizzati da [!DNL Target] nei modelli di personalizzazione, consulta [Raccolta di dati per gli algoritmi di personalizzazione di Target](/help/main/c-activities/t-automated-personalization/ap-data.md). Per ulteriori informazioni su come caricare in Target nuovi attributi da utilizzare nei modelli di personalizzazione di Target, vedi [Metodi per immettere i dati in Target](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=it){target=_blank}.

**Cos&#39;è un segmento automatizzato?**

Un “segmento automatizzato” è una sorta di pubblico, che però è definito dai modelli di personalizzazione di Target anziché dall’addetto al marketing.

Un segmento automatizzato è composto da valori specifici (o intervalli di valore) di attributi specifici. Consulta il passaggio 5 sopra per esempi di segmenti automatizzati. I segmenti possono sovrapporsi.

Per ulteriori informazioni sull&#39;algoritmo di personalizzazione della foresta casuale, ovvero la base dei modelli di personalizzazione di Target, vedere [Algoritmo Foresta casuale](/help/main/c-activities/t-automated-personalization/algo-random-forest.md).

**Che cosa determina l&#39;ordine dei segmenti automatizzati?**

Per ogni segmento viene calcolato un punteggio in base alle sue dimensioni e prestazioni nel contenuto dell&#39;attività. La combinazione di questi input determina l&#39;ordine dei segmenti automatizzati, in modo tale che i segmenti più grandi e con maggiori differenze di prestazione in rapporto ai vari contenuti appaiano in cima all&#39;elenco.

**Perché nel rapporto di Segmenti automatizzati non sono visibili tutte le offerte/esperienze?**

Le attività di Personalizzazione automatizzata (AP) e Targeting automatico (AT) creano un modello per ogni offerta (nel caso di AP) e un modello per esperienze (nel caso di AT). Queste attività iniziano a fornire traffico personalizzato e creano [!UICONTROL Personalization Insights] con appena due modelli generati. Se non trovi tutte le offerte/esperienze in [!UICONTROL Personalization Insights], probabilmente non disponi di modelli generati per tali offerte/esperienze specifiche. Controlla il rapporto [!UICONTROL Summary] della tua attività e verifica se accanto quell&#39;offerta o esperienza è presente l&#39;icona dell&#39;orologio. Questa icona indica che i modelli non sono ancora stati generati per quell’offerta o esperienza.

**Perché alcune offerte/esperienze con un tasso di conversione inferiore ricevono una maggiore quantità di traffico rispetto ad altre per un determinato segmento automatizzato?**

Vi sono vari motivi per cui potresti vedere più visite a un&#39;offerta o esperienza a basso tasso di conversione in un segmento automatizzato, tra cui:

* Un basso numero di visualizzazioni per alcune o tutte le offerte/esperienze per un determinato segmento automatizzato.
* Le attività a volume ridotto in cui alcune offerte/esperienze non dispongono di modelli o in cui i modelli sono stati creati prima per certe offerte/esperienze rispetto ad altre.
* Le regole di Targeting su un&#39;offerta specifica che selezionano i visitatori che possono visualizzare una determinata offerta/esperienza.

**Le informazioni nei report [!UICONTROL Automated Segments] e [!UICONTROL Important Attributes] sono le stesse del file CSV scaricabile?**

No, il rapporto dell&#39;interfaccia utente contiene specifiche informazioni. Il file CSV scaricabile contiene ulteriori dettagli. Il download del rapporto di Registri di segmento automatizzato comprende altri Segmenti automatizzati oltre ai segmenti principali inclusi nell&#39;interfaccia utente, così come le prestazioni di quei segmenti rispetto alle offerte o esperienze. Il rapporto di Attributi importanti include i principali 100 attributi dei visitatori e l&#39;importanza relativa, mentre l&#39;interfaccia utente include solo i 10 attributi principali.

**Posso visualizzare [!UICONTROL Personalization Insights] per un intervallo di date personalizzato?**

Il rapporto di Personalization Insights (sia [!UICONTROL Automated Segments] che [!UICONTROL Important Attributes]) è disponibile solo per intervalli di date fissi: 15 giorni, 30 giorni e 60 giorni. Questi intervalli di date fissi consentono a [!UICONTROL Personalization Insights] di utilizzare un intervallo di dati sufficientemente ampio per ridurre la probabilità che si ottengano informazioni da un pattern di breve durata nell&#39;attività. Puoi selezionare queste durate per qualsiasi data di fine (laddove vi siano dati a sufficienza per soddisfare la durata).

**Come viene creato [!UICONTROL Personalization Insights]?**

[!UICONTROL Personalization Insights] viene creato utilizzando una tecnica in attesa di brevetto Adobe denominata MAGIX (Model Agnostic Globally Interpretable Explanations). Per ulteriori informazioni su MAGIX, consulta il documento pubblicato del team di ricerca Adobe sul sito Web [arXiv.org](https://arxiv.org/abs/1706.07160).

**Perché i dati sul traffico totale dei visitatori nel report [!UICONTROL Automated Segments] non corrispondono al report di riepilogo/prestazioni di Personalizzazione automatizzata (AP) o Targeting automatico (AT)?**

I report [!UICONTROL Personalization Insights] includono solo i visitatori che hanno visto un contenuto selezionato dai modelli di personalizzazione di Target (ovvero non considera il traffico di controllo o il traffico gestito dal modello vincitore complessivo). Questo tipo di traffico è denominato traffico &quot;personalizzato&quot;. Il rapporto sulle prestazioni di riepilogo in AP/AT include il controllo rispetto al traffico &quot;mirato&quot;. Il traffico mirato include il traffico personalizzato, nonché quello gestito tramite il modello vincitore complessivo e quello gestito in modo casuale utilizzato per continuare l&#39;apprendimento.

**I segmenti automatizzati si escludono a vicenda?**

No, c&#39;è una sovrapposizione tra i segmenti automatizzati.

**[!UICONTROL Personalization Insights] è disponibile per obiettivi di modeling/obiettivi primari basati sui ricavi?**

Al momento, [!UICONTROL Personalization Insights] è disponibile solo per le attività con obiettivo di ottimizzazione della conversione. In una versione futura, Adobe aggiungerà il supporto per le attività con obiettivo di ottimizzazione dei ricavi.

**Come posso sfruttare le informazioni in Registri di personalizzazione?**

* Scopri nuovi tipi di pubblico per il targeting: se vedi un particolare segmento automatizzato con prestazioni ottimali, puoi creare un pubblico per riutilizzare tale segmento in altri rapporti.
* Prova le tue ipotesi sul tipo di visitatori che rispondono a quale delle tue esperienze.
* Scopri i contenuti che hanno funzionato per determinati tipi di visitatori: le offerte che hanno avuto maggiore riscontro.
* Individua il contenuto con le prestazioni più basse.
* Scopri gli attributi cruciali per l&#39;apprendimento del modello.
* Scopri gli attributi utilizzati nei modelli di personalizzazione e la loro importanza.
* Individua le opportunità per ulteriori punti di dati da trasmettere a Target per informare ulteriormente la tua personalizzazione.

**Esiste una logica per l’ordine di visualizzazione degli attributi in una scheda segmenti?**

No, l’ordine delle schede è basato solo su una classificazione, come precedentemente descritto. L’ordine degli attributi all’interno di una scheda non è basato su alcuna logica.
