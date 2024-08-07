---
keywords: risoluzione dei problemi;discrepanze metriche;FAQ;rapporti;nuovo visitatore;nuovi visitatori;visitatore di ritorno;visitatori di ritorno;visita di ritorno;nuova visita
description: Esplora un elenco delle domande e risposte più frequenti sul reporting Adobe [!DNL Target] .
title: Dove posso trovare le risposte alle domande sul reporting di  [!DNL Target] ?
feature: Reports
exl-id: 1a345a67-5050-4bd3-858d-99731d2c1dd3
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '1367'
ht-degree: 20%

---

# Domande frequenti sulla generazione di rapporti

Elenco delle domande frequenti sulla generazione di rapporti in [!DNL Adobe Target].

## Come vengono conteggiate le metriche Nuovi visitatori e Visitatori di ritorno? {#methodology}

La prima visita di un nuovo visitatore dura finché il visitatore è attivo sul sito.
Se l’utente è inattivo per 30 minuti o più, la sessione viene reimpostata. Reimpostando la sessione, il visitatore diventa un visitatore di ritorno alla visita successiva o ridiventa attivo dopo 30 minuti di inattività.
Se il visitatore si sposta all’interno del sito ogni 29 minuti per un giorno intero, viene conteggiato come nuovo visitatore per l’intero giorno. La sessione non è mai stata reimpostata perché il visitatore non ha mai superato la soglia dei 30 minuti.

Le seguenti informazioni spiegano più dettagliatamente come vengono conteggiati i nuovi visitatori e i visitatori di ritorno. Sono inclusi anche esempi che spiegano perché la somma di questi due segmenti non sempre corrisponde al numero di visitatori totali.

### Visitatori nuovi

Un visitatore viene incluso nel segmento Nuovi visitatori se viene soddisfatta una delle seguenti condizioni:

* È la prima volta che visita il sito.
* È la prima volta che visita il sito dopo aver cancellato i cookie.
* È la prima volta che visita il sito da quando la [durata del profilo del visitatore](/help/main/c-target/c-visitor-profile/visitor-profile-lifetime.md) è scaduta.

### Visitatori di ritorno

Un visitatore viene incluso nel segmento Visitatore di ritorno se ha già visitato il sito, è uscito da almeno 30 minuti ed è tornato di nuovo sul sito con gli stessi cookie. Fino a quando un visitatore ritorna entro la durata del suo profilo, viene considerato un visitatore di ritorno.

Supponiamo che la durata del profilo sia impostata su 14 giorni (impostazione predefinita). Un visitatore viene incluso nel segmento Visitatori di ritorno se sono soddisfatte le seguenti condizioni:

* Un visitatore visita il sito per la prima volta e viene registrato come nuovo visitatore.
* Il visitatore lascia il sito, ma ritorna dopo sei giorni.

Poiché la durata del profilo è impostata su 14 giorni, il visitatore viene incluso nel segmento Visitatori di ritorno. Se il visitatore ha eliminato dei cookie entro tale periodo di sei giorni, viene incluso nel segmento Nuovi visitatori.

### Esempi che spiegano le discrepanze tra i conteggi delle metriche

**Esempio 1**: se questi due segmenti sono applicati a un&#39;attività, la somma dei segmenti Nuovi visitatori e Visitatori di ritorno non corrisponde sempre al numero totale di visitatori.

Prendi in considerazione l’esempio seguente, prendendo in considerazione le condizioni precedentemente menzionate per Nuovi visitatori e Visitatori di ritorno:

* Un visitatore visita il sito per la prima volta e viene conteggiato come nuovo visitatore.
* Il visitatore ritorna al sito dopo che sono state soddisfatte le condizioni per Visitatori di ritorno e viene conteggiato come Visitatore di ritorno.

Questo visitatore viene conteggiato come un singolo visitatore nel conteggio complessivo dei visitatori dell’attività, anche se viene conteggiato sia nel segmento Nuovi visitatori che nel segmento Visitatori di ritorno.

**Esempio 2**: le discrepanze tra i conteggi per Nuovi visitatori e Visitatori di ritorno dipendono anche da come configuri le [metriche di successo](/help/main/c-activities/r-success-metrics/success-metrics.md) dell&#39;attività.

Ad esempio:

Diversi nuovi visitatori visitano il tuo sito e sono qualificati per un’attività. Questi nuovi visitatori vengono conteggiati nel segmento Nuovi visitatori. Tutti questi visitatori hanno anche registrato una visita a quell’attività.

Alcuni visitatori hanno raggiunto la metrica di conversione, configurata come &quot;Incrementa il conteggio e mantieni l’utente in attività&quot;. Supponiamo che alcuni di questi utenti raggiungano più volte la metrica di conversione, la metrica di conversione non aumenta. Dato che la configurazione, tuttavia, alcuni utenti potrebbero raggiungere la metrica di conversione e quindi tornare alla home page, qualificandosi di nuovo nell’attività per registrare una nuova visita.

## Perché i miei report [!UICONTROL Experience Targeting] (XT) contengono metriche per le esperienze di controllo?

Nelle attività Targeting esperienze (XT) deve essere sempre presente un’esperienza di controllo. Se si utilizza un&#39;attività XT in modo simile a un&#39;attività [!UICONTROL A/B Test], come spesso avviene, i dati sull&#39;esperienza di controllo sono utili. Se ritieni che non siano utili nei tuoi rapporti, puoi semplicemente ignorarli.

## Perché il numero di visite in [!DNL Target] è inferiore rispetto ad altre soluzioni [!DNL Adobe Experience Cloud]? {#section_7E626FDB417E41B8B58BBF30FB207409}

I numeri delle metriche, ad esempio le visite, segnalati da [!DNL Target] sono sempre inferiori ai numeri riportati in altre soluzioni [!DNL Experience Cloud] per diversi motivi:

* [!DNL Target] conta le visite solo per i visitatori che si qualificano per l’attività. Altre soluzioni contano le visite per i visitatori che visualizzano la pagina, indipendentemente dall’attività che li ha portati alla pagina.
* In alcune situazioni, attività differenti competono per la stessa posizione (reciprocamente esclusive). Di conseguenza, i visitatori visualizzano contenuti diversi in una pagina web, che influiscono sui numeri della metrica riportati da [!DNL Target].

## Perché non sono disponibili dati per il rapporto della mia attività? {#section_E4722F6445884130951DF79981C8289B}

Se il contenuto di un’attività è stato recapitato correttamente ai visitatori ma il relativo rapporto non contiene dati, potrebbe venire visualizzato il seguente messaggio di errore: &quot;Non sono disponibili dati per le impostazioni di rapporto selezionate&quot;.

Ci sono alcuni possibili motivi per cui i dati mancano dai rapporti di attività:

* Non hai selezionato l’ambiente corretto nelle impostazioni del rapporto
* Non è stato allocato traffico all&#39;esperienza di controllo

### Nelle impostazioni del rapporto non è stato selezionato l’ambiente corretto:

Se il contenuto di un’attività è stato recapitato correttamente agli utenti ma il relativo rapporto non contiene dati, assicurati di aver selezionato l’ambiente corretto ([gruppo host](/help/main/administrating-target/hosts.md)) nelle impostazioni del rapporto.

Per modificare l’ambiente per il rapporto di un’attività:

1. Fare clic su **[!UICONTROL Activities]**, selezionare l&#39;attività desiderata dall&#39;elenco, quindi fare clic sulla scheda **[!UICONTROL Reports]**.
1. Fai clic sull’icona a forma di ruota dentata per configurare le impostazioni dei rapporti.

   ![Finestra di dialogo Impostazioni A/B](/help/main/c-reports/c-report-settings/assets/ab_settings_dialog.png)

1. Dall&#39;elenco a discesa **[!UICONTROL Environment]**, selezionare **[!UICONTROL Production]**.

   I dati del rapporto potrebbero non essere disponibili se hai selezionato un ambiente di sviluppo.

1. Fare clic su **[!UICONTROL Save]**.

Per ulteriori informazioni sugli ambienti, vedi [Host](/help/main/administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E).

### Non è stato allocato traffico all&#39;esperienza di controllo

Se il contenuto di un’attività è stato recapitato correttamente agli utenti ma il relativo rapporto non contiene dati, assicurati di utilizzare un’esperienza con il traffico come esperienza di controllo.

1. Fare clic su **[!UICONTROL Activities]**, selezionare l&#39;attività desiderata dall&#39;elenco, quindi fare clic sulla scheda **[!UICONTROL Reports]**.
1. Fai clic sull’icona a forma di ruota dentata per configurare le impostazioni dei rapporti.

1. Dall&#39;elenco a discesa **[!UICONTROL Control]**, seleziona un&#39;esperienza che riceve traffico.

1. Fare clic su **[!UICONTROL Save]**.

>[!NOTE]
>
>Per ulteriori informazioni su come aggiornare un&#39;attività di [!UICONTROL Automated Personalization] (AP) e modificare l&#39;esperienza di controllo in un&#39;esperienza che riceve il traffico, vedere [Selezionare il controllo per l&#39;attività di Automated Personalization o Targeting automatico](/help/main/c-activities/t-automated-personalization/experience-as-control.md).


## Perché la suddivisione del traffico tra le mie esperienze è irregolare nella mia attività A/B o MVT? {#uneven}

Ad esempio, ho impostato la suddivisione del traffico su 50/50 o 25/25/25/25 ma vedo una distribuzione molto diversa tra le esperienze nel reporting. Ci sono diversi motivi spiegabili per i conteggi irregolari dei visitatori nel reporting di [!DNL Target]:

* Quando viene avviata un&#39;attività [!DNL Target], la distribuzione del traffico può essere irregolare a causa dell&#39;architettura dei nodi perimetrali utilizzata da [!DNL Target] per ottimizzare la distribuzione delle esperienze. La best practice prevede che un’attività disponga di un certo tempo per raccogliere più dati, in modo che la distribuzione si normalizzi. Per ulteriori informazioni sull&#39;architettura di [!DNL Adobe Target] e sui nodi di Edge, vedere [Come funziona Adobe Target](/help/main/c-intro/how-target-works.md).
* Se ti trovi in [!DNL Target] o [!DNL Analytics] e utilizzi la metrica **[!UICONTROL Visits]**, ricorda che [!DNL Target] è un sistema basato su visitatore e che la distribuzione del traffico per un test A/B o MVT è assegnata a livello di visitatore. Pertanto, se esamini i risultati dell&#39;attività utilizzando la metrica **[!UICONTROL Visits]**, la distribuzione del traffico potrebbe apparire irregolare perché alcuni visitatori potrebbero avere più visite. Visitatori è la metrica di normalizzazione standard durante la valutazione delle prestazioni dell’attività.
* La best practice per i test A/B e MVT consiste nel mantenere uniformi le suddivisioni del traffico. Cambiare la distribuzione del traffico tra le esperienze (ad esempio da 90/10 a 50/50) durante un test può portare a visitatori irregolari tra le esperienze. L’esperienza con traffico ridotto potrebbe non &quot;recuperare&quot; mai.
* Se segui le best practice di cui sopra e la suddivisione del traffico non si normalizza nel tempo, controlla quanto segue:

   * Stai utilizzando la libreria at.js più recente? Per ulteriori informazioni sulla versione corrente e sulle relative note sulla versione, consulta [Dettagli sulla versione di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank}.

   * È un test di reindirizzamento? L&#39;attivazione errata dei tag sulla pagina può causare divisioni del traffico irregolari, soprattutto quando si utilizza [!DNL Analytics] come origine dati per un&#39;attività [!DNL Target]. Per informazioni su come risolvere il problema della distribuzione irregolare del traffico in un&#39;attività di reindirizzamento con Analytics for Target (A4T), consulta [Offerte di reindirizzamento - Domande frequenti su A4T](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md).
