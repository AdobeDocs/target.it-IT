---
keywords: Targeting;rapporto AP;rapporti di personalizzazione automatizzata;targeting automatico;targeting automatico;rapporto di targeting automatico;report di targeting automatico;personalizzazione;approfondimenti;segmenti automatizzati;FAQ;domande frequenti
description: Scopri come diversi segmenti definiti da Adobe [!DNL Target] I modelli di personalizzazione rispondono alle offerte/esperienze dell’attività visualizzando il rapporto Segmenti automatizzati.
title: Cos’è il rapporto Segmenti automatizzati?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."
feature: Reports
exl-id: d21517b7-770b-4618-9899-7ac4948c2a8b
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '2166'
ht-degree: 70%

---

# [!UICONTROL Segmenti automatizzati] rapporto

Informazioni su [!UICONTROL Segmenti automatizzati] uno dei due rapporti specializzati a disposizione degli utenti di [!UICONTROL Automated Personalization] (AP) [!UICONTROL Targeting automatico] attività (AT).

>[!NOTE]
>
>Quando si utilizzano i rapporti Approfondimenti personalizzazione, considera quanto segue:
>
>* Le attività di AP e AT sono disponibili come parte della soluzione [!DNL Target Premium]. Non sono disponibili in [!DNL Target Standard] senza una licenza di [!DNL Target Premium].
>
>* [!UICONTROL Approfondimenti personalizzazione] I rapporti sono disponibili solo per le attività di AP e AT che utilizzano un obiettivo di ottimizzazione della conversione. Anche le attività in cui l&#39;obiettivo di ottimizzazione è stato modificato in conversione da ricavi dopo che l&#39;attività era già attiva non sono supportate.
>
>* [!UICONTROL Approfondimenti personalizzazione] sono disponibili solo se il [!UICONTROL Obiettivo principale] è selezionato da [!UICONTROL Metrica rapporto] elenco a discesa.
>
>* [!UICONTROL Approfondimenti personalizzazione] i report sono supportati nella [ambiente predefinito](/help/main/administrating-target/hosts.md) solo.
>
>* [!UICONTROL Approfondimenti personalizzazione] i rapporti vengono generati solo per le attività che si trovano in [!UICONTROL Live] e sono stati attivati e hanno ricevuto traffico per almeno 15 giorni.

I vari visitatori rispondono in modo diverso alle offerte/esperienze nell&#39;attività di AP/AT. Questo rapporto mostra come i diversi segmenti automatizzati definiti dai modelli di personalizzazione di Target rispondono alle offerte/esperienze dell&#39;attività.

## Accedere al rapporto Segmenti automatizzati {#section_8E8F997AAAF44A1B9EE06EB6FB652801}

1. Clic **[!UICONTROL Attività]**, quindi fare clic sulla [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) o [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) dall&#39;elenco.

   Se hai numerose attività, puoi filtrare l’elenco selezionando le opzioni dalla [!UICONTROL Tipo], [!UICONTROL Stato], [!UICONTROL Proprietà], [!UICONTROL Origine per la generazione di rapporti], [!UICONTROL Compositore esperienza], [!UICONTROL Tipo di metrica], e [!UICONTROL Origine attività] elenchi a discesa.

1. Fai clic su **[!UICONTROL Report]**.

   Il [Riepilogo Automated Personalization](/help/main/c-reports/personalization-reports/reports-ap.md) o [Riepilogo Targeting automatico](/help/main/c-reports/personalization-reports/auto-target-summary-report.md) viene visualizzato il rapporto, che fornisce informazioni sulle prestazioni delle attività, rappresentate dall&#39;icona della prima schermata. Le altre due icone rappresentano i due rapporti di Registri di personalizzazione: Segmenti automatizzati e Attributi importanti. Il Targeting automatico ha un’icona di grafico aggiuntiva per la visualizzazione grafica del [!UICONTROL Riepilogo] rapporto.

   ![Rapporto Approfondimenti personalizzazione in Adobe Target](/help/main/c-reports/assets/personalization_insights.png)

   >[!IMPORTANT]
   >
   >Il rapporto [!UICONTROL Segmenti automatizzati] non sarà disponibile per almeno 15 giorni dopo l’attivazione dell’attività. Durante questo periodo iniziale, non potrai accedere a questo rapporto o fare clic sull’icona di [!UICONTROL Segmenti automatizzati]. Trascorsi 15 giorni, supponendo che la tua attività abbia un traffico personalizzato sufficiente, sarà disponibile il rapporto [!UICONTROL Segmenti automatizzati].

1. A 15 giorni dall&#39;attivazione dell&#39;attività, puoi fare clic sull&#39;icona **[!UICONTROL Segmenti automatizzati.]**

   ![Icona Segmenti automatizzati](/help/main/c-reports/assets/icon-automated-sements.png)

1. Seleziona l&#39;intervallo di date desiderato.

   A differenza della [!UICONTROL Riepilogo] rapporto (rapporto sulle prestazioni), [!UICONTROL Approfondimenti personalizzazione], tra cui [!UICONTROL Segmenti automatizzati], è disponibile solo per intervalli di date fissi: 15 giorni, 30 giorni e 60 giorni. Questi intervalli di date fissi consentono a [!UICONTROL Registri di personalizzazione] di utilizzare una gamma di dati abbastanza ampia da ridurre la probabilità di trarre informazioni da un modello di breve durata all&#39;interno dell&#39;attività. Le due decisioni che puoi prendere per l&#39;intervallo di date sono “Data di fine” e “Durata”. Noterai che &quot;Start&quot; è inattivo. La data di inizio cambia automaticamente in base alla data di fine e alla durata selezionate.

   ![Calendario nel rapporto di Adobe Target](/help/main/c-reports/assets/personalization_insights_calendar_1.png)

   Puoi accedere agli intervalli di date fissi disponibili dall&#39;elenco a discesa [!UICONTROL Scegli la durata].

   ![Elenco a discesa Durata in Adobe Target](/help/main/c-reports/assets/personalization_insights_calendar_2.png)

1. Esamina i dati del rapporto [!UICONTROL Segmenti automatizzati].

   ![Rapporto Segmenti automatizzati](/help/main/c-reports/assets/automated_segments_report.png)

1. (Facoltativo) [Scarica il rapporto in formato CSV](/help/main/c-reports/c-report-settings/report-settings.md#section_77E65C50BAAF4AB79242DB3A8778ADEF) per l&#39;analisi in Excel e altri programmi.

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

![Esempio di rapporto Segmenti automatizzati 2](/help/main/c-reports/assets/automated_segment_example_2.png)

## Domande frequenti sui Segmenti automatizzati {#section_740910A52FA646B4AC9452F98C2F5719}

**I rapporti Registri di personalizzazione non sono ancora disponibili per la mia attività. Perché?**

Ci sono vari motivi per cui i rapporti di [!UICONTROL Registri di personalizzazione] non sono ancora disponibili per la tua attività:

* Non sono trascorsi 15 giorni dall’attivazione dell’attività. I rapporti di Segmenti automatizzati e Attributi importanti non saranno disponibili per almeno 15 giorni dopo l&#39;attivazione dell&#39;attività. Durante questo periodo iniziale, non potrai accedere a questi rapporti o fare clic sulle icone di Segmenti automatizzati e Attributi importanti.
* L&#39;attività non ha avuto traffico a sufficienza durante l’arco temporale specificato. Trascorsi 15 giorni, supponendo che la tua attività abbia un traffico personalizzato sufficiente, saranno disponibili i rapporti Segmenti automatizzati e Attributi importanti.
* L&#39;attività ha un obiettivo di ottimizzazione dei profitti. Attualmente, [!UICONTROL Approfondimenti personalizzazione] è disponibile solo per le attività con obiettivo di ottimizzazione della conversione. Ad Adobe, in una versione futura verrà aggiunto il supporto per le attività con obiettivo di ottimizzazione dei ricavi.

**Cos&#39;è un attributo?**

Un attributo è un&#39;informazione su un visitatore o sulla sua visita specifica che gli algoritmi di personalizzazione utilizzano per imparare a personalizzare il traffico. Gli attributi possono essere, ad esempio, il tipo di browser, la posizione, l&#39;orario della visita e così via.

Per ulteriori informazioni sugli attributi utilizzati da [!DNL Target] nei modelli di personalizzazione, consulta [Raccolta di dati per gli algoritmi di personalizzazione di Target](/help/main/c-activities/t-automated-personalization/ap-data.md). Per ulteriori informazioni su come caricare in Target nuovi attributi da utilizzare nei modelli di personalizzazione di Target, consulta [Metodi per immettere i dati in Target](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html){target=_blank}.

**Cos&#39;è un segmento automatizzato?**

Un “segmento automatizzato” è una sorta di pubblico, che però è definito dai modelli di personalizzazione di Target anziché dall’addetto al marketing.

Un segmento automatizzato è composto da valori specifici (o intervalli di valore) di attributi specifici. Consulta il passaggio 5 sopra per esempi di segmenti automatizzati. I segmenti possono sovrapporsi.

Per ulteriori informazioni sull’algoritmo di personalizzazione della foresta casuale, ovvero la base dei modelli di personalizzazione di Target, consulta [Algoritmo Foresta casuale](/help/main/c-activities/t-automated-personalization/algo-random-forest.md).

**Cosa determina l’ordine dei segmenti automatizzati?**

Per ogni segmento viene calcolato un punteggio in base alle sue dimensioni e prestazioni nel contenuto dell&#39;attività. La combinazione di questi input determina l&#39;ordine dei segmenti automatizzati, in modo tale che i segmenti più grandi e con maggiori differenze di prestazione in rapporto ai vari contenuti appaiano in cima all&#39;elenco.

**Perché nel rapporto di Segmenti automatizzati non sono visibili tutte le offerte/esperienze?**

Le attività di Personalizzazione automatizzata (AP) e Targeting automatico (AT) creano un modello per ogni offerta (nel caso di AP) e un modello per esperienze (nel caso di AT). Queste attività iniziano a gestire il traffico personalizzato e a creare [!UICONTROL Registri di personalizzazione] a partire da due modelli. Se non trovi tutte le offerte/esperienze in [!UICONTROL Approfondimenti personalizzazione]Tuttavia, è probabile che non siano presenti modelli generati per tali offerte/esperienze specifiche. Puoi controllare i [!UICONTROL Riepilogo] genera un rapporto e controlla se accanto quell’offerta o esperienza è presente l’icona dell’orologio. Questa icona indica che i modelli non sono ancora stati generati per quell’offerta o esperienza.

**Perché alcune offerte/esperienze con un tasso di conversione inferiore ricevono una maggiore quantità di traffico rispetto ad altre per un determinato segmento automatizzato?**

Vi sono vari motivi per cui potresti vedere più visite a un&#39;offerta o esperienza a basso tasso di conversione in un segmento automatizzato, tra cui:

* Un basso numero di visualizzazioni per alcune o tutte le offerte/esperienze per un determinato segmento automatizzato.
* Le attività a volume ridotto in cui alcune offerte/esperienze non dispongono di modelli o in cui i modelli sono stati creati prima per certe offerte/esperienze rispetto ad altre.
* Le regole di Targeting su un&#39;offerta specifica che selezionano i visitatori che possono visualizzare una determinata offerta/esperienza.

**Le informazioni nei rapporti di [!UICONTROL Segmenti automatizzati] e [!UICONTROL Attributi importanti] sono le stesse del file CSV scaricabile?**

No, il rapporto dell&#39;interfaccia utente contiene specifiche informazioni. Il file CSV scaricabile contiene ulteriori dettagli. Il download del rapporto di Registri di segmento automatizzato comprende altri Segmenti automatizzati oltre ai segmenti principali inclusi nell&#39;interfaccia utente, così come le prestazioni di quei segmenti rispetto alle offerte o esperienze. Il rapporto di Attributi importanti include i principali 100 attributi dei visitatori e l&#39;importanza relativa, mentre l&#39;interfaccia utente include solo i 10 attributi principali.

**Posso visualizzare [!UICONTROL Registri di personalizzazione] per un intervallo di date personalizzato?**

Rapporti Approfondimenti personalizzazione (entrambi [!UICONTROL Segmenti automatizzati] e [!UICONTROL Attributi importanti]) è disponibile solo per intervalli di date fissi: 15, 30 e 60 giorni. Questi intervalli di date fissi consentono a [!UICONTROL Registri di personalizzazione] di utilizzare una gamma di dati abbastanza ampia da ridurre la probabilità di trarre informazioni da un modello di breve durata all&#39;interno dell&#39;attività. Puoi selezionare queste durate per qualsiasi data di fine (laddove vi siano dati a sufficienza per soddisfare la durata).

**Come viene creato [!UICONTROL Registri di personalizzazione]?**

[!UICONTROL Registri di personalizzazione] viene creato tramite una tecnica di Adobe in attesa di licenza denominata MAGIX (Model Agnostic Globally Interpretable Explanations). Per ulteriori informazioni su MAGIX, consulta il documento pubblicato del team di ricerca Adobe sul [sito Web arXiv.org](https://arxiv.org/abs/1706.07160).

**Perché i dati sul traffico totale dei visitatori nel rapporto [!UICONTROL Segmenti automatizzati] non corrispondono al rapporto di riepilogo/prestazioni di Personalizzazione automatizzata (AP) o Targeting automatico (AT)?**

Il [!UICONTROL Approfondimenti personalizzazione] i rapporti includono solo i visitatori che hanno visto un contenuto selezionato dai modelli di personalizzazione di Target (ovvero non considera il traffico di controllo o il traffico gestito dal modello vincitore complessivo). Questo tipo di traffico è denominato traffico &quot;personalizzato&quot;. Il rapporto sulle prestazioni di riepilogo in AP/AT include il controllo rispetto al traffico &quot;mirato&quot;. Il traffico mirato include il traffico personalizzato, nonché quello gestito tramite il modello vincitore complessivo e quello gestito in modo casuale utilizzato per continuare l&#39;apprendimento.

**I segmenti automatizzati si escludono a vicenda?**

No, c&#39;è una sovrapposizione tra i segmenti automatizzati.

**[!UICONTROL Registri di personalizzazione] è disponibile per obiettivi di modeling/obiettivi primari basati sui profitti?**

Attualmente, [!UICONTROL Registri di personalizzazione] è disponibile solo per le attività con obiettivo di ottimizzazione della conversione. Ad Adobe, in una versione futura verrà aggiunto il supporto per le attività con obiettivo di ottimizzazione dei ricavi.

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
