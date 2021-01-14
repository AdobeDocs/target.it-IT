---
keywords: troubleshooting;metric discrepancies;FAQ;reports;new visitor;new visitors;returning visitor;returning visitors;return visit;new visit
description: Elenco delle domande frequenti sulla generazione di rapporti in Adobe Target.
title: Domande frequenti sulla generazione di rapporti in Adobe Target
feature: Reports
translation-type: tm+mt
source-git-commit: 7b86db4b45f93a3c6169caf81c2cd52236bb5a45
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 31%

---


# Domande frequenti sulla generazione di rapporti{#reporting-faq}

Elenco delle domande frequenti sulla generazione di rapporti in [!DNL Target].

## Come vengono contate le metriche Nuovi visitatori e Visitatori di ritorno?

Le informazioni seguenti spiegano come vengono conteggiati i nuovi visitatori e visitatori di ritorno e forniscono esempi del motivo per cui la somma di questi due segmenti non corrisponde sempre al numero totale di visitatori.

### Visitatori nuovi

Un visitatore è incluso nel segmento Nuovi visitatori se è soddisfatta una delle seguenti condizioni:

* È la prima volta che il visitatore visita il sito.
* È la prima volta che il visitatore visita il sito dopo aver cancellato i cookie.
* È la prima volta che il visitatore visita il sito da quando la [Durata del profilo del visitatore](/help/c-target/c-visitor-profile/visitor-profile-lifetime.md) è scaduta.

### Visitatori di ritorno

Il visitatore viene incluso nel segmento Visitatori di ritorno se l’utente ha visitato in precedenza il sito, se ne è andato per almeno 30 minuti e ha nuovamente effettuato la restituzione al sito con gli stessi cookie. Fino a quando un visitatore ritorna entro la durata del suo profilo, viene considerato un visitatore di ritorno.

Supponiamo che la durata del profilo sia impostata per 14 giorni (impostazione predefinita). Un visitatore è incluso nel segmento Visitatori di ritorno se sono soddisfatte le seguenti condizioni:

* Un visitatore visita il sito per la prima volta e viene registrato come Nuovo visitatore.
* Il visitatore esce dal sito, ma ritorna sei giorni dopo.

Poiché la durata del profilo è impostata per 14 giorni, il visitatore viene incluso nel segmento Visitatori di ritorno. Tieni presente che se il visitatore ha eliminato dei cookie entro tale periodo di sei giorni, quel visitatore verrà incluso nel segmento Nuovi visitatori.

### Esempi che spiegano le discrepanze tra i conteggi delle metriche

**Esempio 1**: Se questi due segmenti sono applicati a un&#39;attività, il segmento Nuovi visitatori e il segmento Visitatori di ritorno non sempre si sommano al numero totale di visitatori.

Considerate l&#39;esempio seguente, tenendo conto delle condizioni sopra indicate per i nuovi visitatori e i visitatori di ritorno:

* Un visitatore visita il sito per la prima volta e viene conteggiato come Nuovo visitatore.
* Il visitatore ritorna al sito dopo che sono state soddisfatte le condizioni per i visitatori di ritorno e viene conteggiato come Visitatore di ritorno.

Questo visitatore viene conteggiato come singolo visitatore nel conteggio complessivo dei visitatori dell&#39;attività anche se viene conteggiato nei segmenti Nuovi visitatori e Visitatori di ritorno.

**Esempio 2**: Le discrepanze tra i conteggi per i nuovi visitatori e i visitatori di ritorno dipendono anche da come configurate le metriche [ di ](/help/c-activities/r-success-metrics/success-metrics.md)successo dell&#39;attività.

Ad esempio:

Diversi nuovi visitatori visitano il sito e sono qualificati per un&#39;attività. Questi nuovi visitatori vengono conteggiati nel segmento Nuovi visitatori. Tutti questi visitatori hanno anche registrato una visita in quell&#39;attività.

Alcuni visitatori hanno raggiunto la metrica di conversione, che era configurata come &quot;Incremento conteggio e Mantieni utente in attività&quot;. Se alcuni di questi utenti raggiungono la metrica di conversione più volte, la metrica di conversione non aumenterà. Dato che l&#39;impostazione, tuttavia, alcuni utenti potrebbero aver raggiunto la metrica di conversione e quindi tornare alla home page, abilitando nuovamente l&#39;attività per registrare una nuova visita.

## Perché i miei rapporti [!UICONTROL Targeting esperienze] (XT) contengono metriche per le esperienze di controllo?

Nelle attività Targeting esperienze (XT) deve essere sempre presente un’esperienza di controllo. Se utilizzi un’attività XT in modo simile a un’[!UICONTROL attività Test A/B], come spesso avviene, i dati sull’esperienza di controllo sono utili. Se ritieni che non siano utili nei tuoi rapporti, puoi semplicemente ignorarli.

## Perché il numero di visite in [!DNL Target] è inferiore rispetto ad altre soluzioni [!DNL Adobe Experience Cloud]?{#section_7E626FDB417E41B8B58BBF30FB207409}

I numeri delle metriche, ad esempio le visite, segnalati da [!DNL Target] saranno sempre inferiori ai numeri riportati in altre soluzioni di [!DNL Experience Cloud] per una serie di motivi:

* [!DNL Target] conta le visite solo per i visitatori che si qualificano per l’attività. Altre soluzioni contano le visite per i visitatori che visualizzano la pagina, indipendentemente dall’attività che li ha portati alla pagina.
* In alcune situazioni, attività differenti competono per la stessa posizione (reciprocamente esclusive). Di conseguenza, i visitatori visualizzano contenuti diversi in una pagina web, che influiscono sui numeri della metrica riportati da [!DNL Target].

## Perché non sono disponibili dati per il rapporto della mia attività? {#section_E4722F6445884130951DF79981C8289B}

Se il contenuto di un’attività è stato recapitato correttamente agli utenti ma il relativo rapporto non contiene dati, assicurati di aver selezionato l’ambiente corretto ([gruppo host](/help/administrating-target/hosts.md)) nelle impostazioni del rapporto.

Se hai selezionato un ambiente di sviluppo, potresti visualizzare il seguente messaggio di errore: “Non sono disponibili dati per le impostazioni di rapporto selezionate.”.

Per modificare l’ambiente per il rapporto di un’attività:

1. Fai clic su **[!UICONTROL Attività]**, scegli l’attività desiderata dall’elenco, quindi fai clic sulla scheda **[!UICONTROL Rapporti]**.
1. Fai clic sull’icona a forma di ruota dentata per configurare le impostazioni dei rapporti.

   ![Finestra di dialogo Impostazioni A/B](/help/c-reports/c-report-settings/assets/ab_settings_dialog.png)

   >[!NOTE]
   >
   >L’icona a forma di ingranaggio non è disponibile per i rapporti di [!UICONTROL Personalizzazione automatizzata].

1. Dall’elenco a discesa **[!UICONTROL Ambiente]**, seleziona **[!UICONTROL Produzione]**.

   I dati del rapporto potrebbero non essere disponibili se hai selezionato un ambiente di sviluppo.

1. Fai clic su **[!UICONTROL Salva]**.

Per ulteriori informazioni sugli ambienti, vedi [Host](/help/administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E).

## Perché la divisione del traffico tra le mie esperienze non è uniforme nell&#39;attività A/B o MVT? {#uneven}

Ad esempio, ho impostato la suddivisione del traffico su 50/50 o 25/25/25/25, ma vedo una distribuzione molto diversa tra le esperienze nel reporting. Esistono diversi motivi spiegabili per i conteggi irregolari dei visitatori nei report [!DNL Target]:

* Quando viene avviata per la prima volta un&#39;attività [!DNL Target], la distribuzione del traffico potrebbe non essere uniforme a causa dell&#39;architettura dei nodi periferici che [!DNL Target] utilizza per ottimizzare la distribuzione dell&#39;esperienza. La procedura ottimale consiste nel concedere a un&#39;attività un certo tempo per la raccolta di dati aggiuntivi e la distribuzione si normalizzerà. Per ulteriori informazioni sull&#39;architettura [!DNL Adobe Target] e sui nodi Edge, vedere [Come  Adobe Target](/help/c-intro/how-target-works.md).
* Se siete in [!DNL Target] o [!DNL Analytics] e state utilizzando la metrica **[!UICONTROL Visits]**, ricordate che [!DNL Target] è un sistema basato sui visitatori e che la distribuzione del traffico per un test A/B o MVT è assegnata a livello di visitatore. Pertanto, se si esaminano i risultati dell&#39;attività utilizzando la metrica **[!UICONTROL Visits]**, la distribuzione del traffico potrebbe apparire diseguale perché alcuni visitatori potrebbero avere più visite. I visitatori sono la metrica standard di normalizzazione per la valutazione delle prestazioni dell&#39;attività.
* La procedura ottimale per i test A/B e MVT consiste nel mantenere uniformi le suddivisioni del traffico. La modifica della distribuzione del traffico tra le esperienze (ad esempio da 90/10 a 50/50) durante un test può portare a visitatori irregolari tra le esperienze. L&#39;esperienza di traffico inferiore potrebbe non &quot;raggiungere&quot;.
* Se state seguendo le best practice indicate sopra e la suddivisione del traffico non si normalizza nel tempo, è necessario verificare quanto segue:

   * Utilizzi la libreria at.js più recente? Per ulteriori informazioni sulla versione corrente e sulle relative note sulla versione, consultate [at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

   * È un test di reindirizzamento? I tempi errati per l&#39;attivazione dei tag sulla pagina possono causare interruzioni del traffico, soprattutto se si utilizza [!DNL Analytics] come origine dati per un&#39;attività [!DNL Target]. Per informazioni dettagliate per correggere la distribuzione del traffico diseguale in un&#39;attività di reindirizzamento con Analytics for Target (A4T), consultate [Offerte di reindirizzamento - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md).
