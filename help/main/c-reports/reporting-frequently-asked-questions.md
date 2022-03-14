---
keywords: risoluzione dei problemi;discrepanze metriche;FAQ;rapporti;nuovo visitatore;nuovi visitatori;visitatori di ritorno;visitatori di ritorno;visita di ritorno;nuova visita
description: Esplora un elenco delle domande frequenti e delle risposte relative all’Adobe [!DNL Target] rapporti.
title: Dove posso trovare le risposte alle domande su [!DNL Target] Segnalazione?
feature: Reports
exl-id: 1a345a67-5050-4bd3-858d-99731d2c1dd3
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '1218'
ht-degree: 33%

---

# Domande frequenti sulla generazione di rapporti

Elenco delle domande frequenti sulla generazione di rapporti in [!DNL Adobe Target].

## Come vengono conteggiate le metriche Nuovi visitatori e Visitatori di ritorno? {#methodology}

La prima visita di un nuovo visitatore dura fino a quando il visitatore è attivo sul sito.
Se l’utente è inattivo per 30 minuti o più, la sessione viene reimpostata. Reimpostando la sessione, il visitatore diventa un visitatore di ritorno alla visita successiva o diventa nuovamente attivo dopo 30 minuti di inattività.
Se il visitatore si sposta sul sito ogni 29 minuti per un’intera giornata, viene conteggiato come nuovo visitatore per l’intero giorno. La sessione non è mai stata reimpostata perché il visitatore non ha mai superato la soglia di 30 minuti.

Le informazioni seguenti spiegano più dettagliatamente come vengono conteggiati i visitatori nuovi e i visitatori di ritorno. Sono inclusi anche esempi che spiegano perché la somma di questi due segmenti non corrisponde sempre al numero di visitatori totali.

### Visitatori nuovi

Un visitatore viene incluso nel segmento Nuovi visitatori se viene soddisfatta una delle seguenti condizioni:

* È la prima volta che visita il sito.
* È la prima volta che visita il sito dopo aver cancellato i cookie.
* È la prima volta che visita il sito da quando la [Durata del profilo del visitatore](/help/main/c-target/c-visitor-profile/visitor-profile-lifetime.md) è scaduta.

### Visitatori di ritorno

Un visitatore viene incluso nel segmento Visitatore di ritorno se ha già visitato il sito, è uscito da almeno 30 minuti ed è tornato di nuovo sul sito con gli stessi cookie. Fino a quando un visitatore ritorna entro la durata del suo profilo, viene considerato un visitatore di ritorno.

Supponiamo che la durata del profilo sia impostata per 14 giorni (impostazione predefinita). Un visitatore è incluso nel segmento Visitatori di ritorno se sono soddisfatte le seguenti condizioni:

* Un visitatore visita il sito per la prima volta e viene registrato come nuovo visitatore.
* Il visitatore lascia il sito, ma ritorna sei giorni dopo.

Poiché la durata del profilo è impostata per 14 giorni, questo visitatore è incluso nel segmento Visitatori di ritorno . Se il visitatore ha eliminato dei cookie entro tale periodo di sei giorni, viene incluso nel segmento Nuovi visitatori .

### Esempi che spiegano le discrepanze tra i conteggi delle metriche

**Esempio 1**: Se questi due segmenti vengono applicati a un’attività, il segmento Nuovi visitatori e il segmento Visitatori di ritorno non sempre si sommano al numero totale di visitatori.

Prendi in considerazione l’esempio seguente, tenendo presenti le condizioni precedentemente menzionate per Nuovi visitatori e Visitatori di ritorno:

* Un visitatore visita il sito per la prima volta e viene conteggiato come nuovo visitatore.
* Il visitatore ritorna al sito dopo che le condizioni sono soddisfatte per i visitatori di ritorno e viene conteggiato come visitatore di ritorno.

Questo visitatore viene conteggiato come un singolo visitatore nel conteggio complessivo dei visitatori dell’attività, anche se viene conteggiato nei segmenti Nuovi visitatori e Visitatori di ritorno .

**Esempio 2**: Le discrepanze tra i conteggi per nuovi visitatori e visitatori di ritorno dipendono anche dalla modalità di configurazione dell’attività [metriche di successo](/help/main/c-activities/r-success-metrics/success-metrics.md).

Ad esempio:

Diversi nuovi visitatori visitano il tuo sito e sono qualificati per un’attività. Questi nuovi visitatori vengono conteggiati per il segmento Nuovi visitatori . Anche tutti questi visitatori hanno registrato una visita in quell’attività.

Alcuni visitatori hanno raggiunto la metrica di conversione, configurata come &quot;Incrementa il conteggio e mantieni l’utente in attività&quot;. Supponiamo che alcuni di questi utenti raggiungano la metrica di conversione più volte, che la metrica di conversione non aumenti. Dato che la configurazione, tuttavia, alcuni utenti potrebbero aver raggiunto la metrica di conversione e quindi tornare alla home page, qualificandosi nuovamente per l’attività per registrare una nuova visita.

## Perché i miei rapporti [!UICONTROL Targeting esperienze] (XT) contengono metriche per le esperienze di controllo?

Nelle attività Targeting esperienze (XT) deve essere sempre presente un’esperienza di controllo. Se utilizzi un’attività XT in modo simile a un’[!UICONTROL attività Test A/B], come spesso avviene, i dati sull’esperienza di controllo sono utili. Se ritieni che non siano utili nei tuoi rapporti, puoi semplicemente ignorarli.

## Perché il numero di visite in [!DNL Target] è inferiore rispetto ad altre soluzioni [!DNL Adobe Experience Cloud]? {#section_7E626FDB417E41B8B58BBF30FB207409}

Numeri delle metriche, ad esempio visite, segnalati da [!DNL Target] sono sempre inferiori ai numeri riportati in altri [!DNL Experience Cloud] soluzioni per diversi motivi:

* [!DNL Target] conta le visite solo per i visitatori che si qualificano per l’attività. Altre soluzioni contano le visite per i visitatori che visualizzano la pagina, indipendentemente dall’attività che li ha portati alla pagina.
* In alcune situazioni, attività differenti competono per la stessa posizione (reciprocamente esclusive). Di conseguenza, i visitatori visualizzano contenuti diversi in una pagina web, che influiscono sui numeri della metrica riportati da [!DNL Target].

## Perché non sono disponibili dati per il rapporto della mia attività? {#section_E4722F6445884130951DF79981C8289B}

Se il contenuto di un’attività è stato recapitato correttamente agli utenti ma il relativo rapporto non contiene dati, assicurati di aver selezionato l’ambiente corretto ([gruppo host](/help/main/administrating-target/hosts.md)) nelle impostazioni del rapporto.

Se hai selezionato un ambiente di sviluppo, potresti visualizzare il seguente messaggio di errore: “Non sono disponibili dati per le impostazioni di rapporto selezionate.”.

Per modificare l’ambiente per il rapporto di un’attività:

1. Fai clic su **[!UICONTROL Attività]**, scegli l’attività desiderata dall’elenco, quindi fai clic sulla scheda **[!UICONTROL Rapporti]**.
1. Fai clic sull’icona a forma di ruota dentata per configurare le impostazioni dei rapporti.

   ![Finestra di dialogo Impostazioni A/B](/help/main/c-reports/c-report-settings/assets/ab_settings_dialog.png)

   >[!NOTE]
   >
   >L’icona a forma di ingranaggio non è disponibile per i rapporti di [!UICONTROL Personalizzazione automatizzata].

1. Dall’elenco a discesa **[!UICONTROL Ambiente]**, seleziona **[!UICONTROL Produzione]**.

   I dati del rapporto potrebbero non essere disponibili se hai selezionato un ambiente di sviluppo.

1. Fai clic su **[!UICONTROL Salva]**.

Per ulteriori informazioni sugli ambienti, vedi [Host](/help/main/administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E).

## Perché il traffico è suddiviso tra le mie esperienze in modo non uniforme nella mia attività A/B o MVT? {#uneven}

Ad esempio, ho impostato la suddivisione del traffico su 50/50 o 25/25/25/25/25, ma vedo una distribuzione molto diversa tra le esperienze nel reporting. Ci sono diverse ragioni spiegabili per conteggi irregolari dei visitatori in [!DNL Target] reporting:

* Quando un [!DNL Target] l’attività viene avviata per la prima volta, la distribuzione del traffico può essere irregolare a causa dell’architettura dei nodi perimetrali che [!DNL Target] utilizza per ottimizzare la distribuzione delle esperienze. La best practice prevede di dare a un’attività un po’ di tempo per raccogliere più dati e la distribuzione si normalizzerà. Per ulteriori informazioni su [!DNL Adobe Target] l&#39;architettura e i nodi di Edge, vedi [Come funziona Adobe Target](/help/main/c-intro/how-target-works.md).
* Se sei in [!DNL Target] o [!DNL Analytics] e si utilizza il **[!UICONTROL Visite]** metrica, ricorda che [!DNL Target] è un sistema basato su visitatore e la distribuzione del traffico per un test A/B o MVT è assegnata a livello di visitatore. Pertanto, se esamini i risultati dell’attività utilizzando **[!UICONTROL Visite]** , la distribuzione del traffico potrebbe apparire irregolare perché alcuni visitatori potrebbero avere più visite. I visitatori sono la metrica standard di normalizzazione durante la valutazione delle prestazioni dell’attività.
* La best practice per i test A/B e MVT consiste nel mantenere uniformi le suddivisioni del traffico. La modifica della distribuzione del traffico tra le esperienze (ad esempio dal 10/90 al 50/50) durante un test può portare a visitatori irregolari tra le diverse esperienze. L&#39;esperienza di traffico inferiore potrebbe non &quot;recuperare&quot;.
* Se segui le best practice di cui sopra e la suddivisione del traffico non si normalizza nel tempo, controlla quanto segue:

   * Utilizzi la libreria at.js più recente? Per ulteriori informazioni sulla versione corrente e sulle relative note sulla versione, consulta [Dettagli sulle versioni di at.js](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

   * È un test di reindirizzamento? La corretta tempistica dei tag attivati sulla pagina può causare suddivisioni del traffico non uniformi, soprattutto quando si utilizza [!DNL Analytics] come origine dati per un [!DNL Target] attività. Per informazioni dettagliate su come correggere la distribuzione non uniforme del traffico su un’attività di reindirizzamento con Analytics for Target (A4T), consulta [Offerte di reindirizzamento - Domande frequenti su A4T](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md).
