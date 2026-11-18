---
keywords: risoluzione dei problemi;domande frequenti;FAQ;personalizzazione automatizzata;controllo;esperienza predefinita;best practice
description: Esplora un elenco di domande frequenti e risposte sulle attività di [!UICONTROL Automated Personalization] (AP) in [!UICONTROL Adobe Target].
title: Come posso trovare le domande frequenti sulle [!UICONTROL attività Automated Personalization]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Automated Personalization
exl-id: 2bf62cc1-1781-4021-a400-2884e0bae893
TQID: 'https://experienceleague.adobe.com/cYdFwvkJDlfGYdcxql9iWGwNiTed4Lb2kC7JdN7xgdo'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
    internal-label: Automated personalization
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
    internal-label: Machine learning
source-git-commit: 44c6bdd4ab818226e76477782d7e4238b49d5cdc
workflow-type: tm+mt
source-wordcount: '2088'
ht-degree: 6%
---
# Domande frequenti su Automated Personalization {#ap-faq}

>[!BEGINSHADEBOX]

**In questa pagina:** Trova le risposte alle domande frequenti sulle **[!UICONTROL attività Automated Personalization]**.

>[!ENDSHADEBOX]

Nelle domande e risposte seguenti viene illustrato come impostare le attività di **[!UICONTROL Automated Personalization]** in [!DNL Adobe Target], come vengono generati i modelli di personalizzazione, come viene allocato il traffico e come leggere i risultati.

## Configurare un’attività {#set-up-an-activity}

+++ Quali sono le best practice per impostare un&#39;attività [!UICONTROL Automated Personalization]?

* Presta particolare attenzione alla *forma attività* (numero di posizioni × numero di offerte), non solo al conteggio totale delle esperienze. Le combinazioni cartesiane di posizioni e offerte influiscono sulle prestazioni in fase di authoring più del numero non elaborato di esperienze. Per prestazioni e gestibilità ottimali, limita le attività **[!UICONTROL Automated Personalization]** e **[!UICONTROL Targeting automatico]** a 4-6 posizioni con 4-6 offerte per posizione, come descritto nella domanda &quot;Quali sono alcuni limiti in Automated Personalization?&quot; in questa sezione. Configurazioni più grandi non sono consigliate e possono rallentare il caricamento o la modifica nel **[!UICONTROL Compositore esperienza visivo]**.
* Per personalizzare una pagina a traffico ridotto o per apportare modifiche strutturali all&#39;esperienza che stai personalizzando, prova a utilizzare un&#39;attività [**[!UICONTROL Targeting automatico ]**](/help/main/c-activities/auto-target/auto-target-to-optimize.md) invece di**[!UICONTROL  Automated Personalization ]**.
* Valuta l&#39;esecuzione di un&#39;attività **[!UICONTROL A/B Test]** tra le offerte e le posizioni che intendi utilizzare nell&#39;attività **[!UICONTROL Automated Personalization]**, per verificare che le posizioni e le offerte abbiano un impatto sull&#39;obiettivo di ottimizzazione. Se l&#39;attività **[!UICONTROL Test A/B]** non riesce a dimostrare una differenza significativa, è probabile che anche **[!UICONTROL Automated Personalization]** non riesca a generare un incremento.

  Se un test A/B...N non mostra differenze statisticamente significative tra le esperienze, una o più delle seguenti situazioni è probabilmente responsabile:

  * È probabile che le offerte non siano sufficientemente diverse tra loro.
  * Le posizioni selezionate non influiscono sulla metrica di successo.
  * L’obiettivo di ottimizzazione è troppo lontano nel funnel di conversione per essere influenzato dalle offerte scelte.

* Utilizza [Calcolatore traffico](/help/main/c-activities/t-automated-personalization/ap-traffic-estimator.md#use-traffic-estimator) per capire quanto tempo ci vuole per la generazione dei modelli di personalizzazione nell&#39;attività **[!UICONTROL Automated Personalization]**.
* Decidi l’allocazione tra il controllo e il traffico di destinazione prima di iniziare l’attività, in base ai tuoi obiettivi. Nella tabella seguente sono elencati i tre scenari da considerare, in base all’obiettivo dell’attività e al tipo di controllo selezionato.

  | Obiettivo di controllo e attività | Allocazione consigliata al controllo | Dettagli |
  | --- | --- | --- |
  | **[!UICONTROL Esperienze casuali]** come controllo e l&#39;obiettivo è quello di testare l&#39;efficacia dell&#39;algoritmo di personalizzazione | 50% | Questo obiettivo richiede un&#39;immagine più precisa dell&#39;incremento. Inoltre, è molto probabile che tu voglia confrontare il tasso di conversione delle tue esperienze o offerte con il tasso che un semplice **[!UICONTROL Test A/B]** (un controllo fornito in modo casuale) darebbe. |
  | **[!UICONTROL Esperienze casuali]** come controllo e l&#39;obiettivo è quello di massimizzare il traffico personalizzato | Da 10% a 30% | Utilizza questa opzione se hai familiarità con l’algoritmo e desideri personalizzare la quantità massima di traffico. Il compromesso è la precisione delle informazioni sull’incremento: gli intervalli di affidabilità del traffico di controllo sono più ampi, in quanto a essi viene indirizzato meno traffico. |
  | **[!UICONTROL Esperienza specifica]** come controllo, con uno degli obiettivi | Da 10% a 30% | Utilizza questa opzione per confrontare con i modelli di personalizzazione un’esperienza specifica definita dagli esperti di marketing. Quando selezioni una sola esperienza come controllo, tale traffico non viene distribuito su ogni offerta o esperienza nell’attività. |

* Utilizza le regole di targeting con la massima moderazione possibile, in quanto possono interferire con la capacità del modello di ottimizzare. Per ulteriori informazioni, consulta [Targeting delle offerte di Personalizzazione automatizzata](/help/main/c-activities/t-automated-personalization/ap-target-offers.md).
* I gruppi di reporting possono limitare il successo dell&#39;attività **[!UICONTROL Automated Personalization]**, quindi utilizzarli solo in condizioni specifiche. Per ulteriori informazioni, consulta [Gruppi di reporting di offerte in Automated Personalization](/help/main/c-activities/t-automated-personalization/offer-reporting-groups-in-automated-personalization.md).

  * Utilizzare i gruppi di reporting solo se sono soddisfatte tutte le seguenti condizioni:

    * Intendi sostituire o aggiungere offerte mentre l’attività è in esecuzione.
    * Le offerte nel gruppo di reporting si rivolgono agli stessi visitatori.
    * Le offerte nel gruppo di reporting hanno circa lo stesso tasso di risposta complessivo.

  * Non esiste alcuna personalizzazione tra le offerte di un gruppo di reporting. Il modello di personalizzazione tratta tutte le offerte come se fossero uguali.
  * Non mettere mai tutte le offerte di un’attività in un singolo gruppo di rapporti. In questo modo tutte le offerte vengono distribuite in modo casuale e uniforme a tutti i visitatori nell’attività.

+++

+++ Quali sono alcuni limiti in [!UICONTROL Automated Personalization]?

[!DNL Target] ha un limite massimo di 30.000 esperienze, ma funziona al meglio quando vengono create meno di 10.000 esperienze. Lo stesso limite si applica quando per l&#39;attività è abilitata l&#39;opzione **[!UICONTROL Non consentire duplicati]**.

Anche se le attività **[!UICONTROL Automated Personalization]** e **[!UICONTROL Targeting automatico]** possono supportare un numero elevato di esperienze, le prestazioni di authoring dipendono in larga misura dalla *forma attività* (numero di posizioni × numero di offerte). Alcune configurazioni creano grandi combinazioni cartesiane che possono avere un impatto significativo sul carico e sulle prestazioni di modifica, anche al di sotto dei limiti di esperienza documentati.

Per prestazioni e gestibilità ottimali, limita le attività **[!UICONTROL Automated Personalization]** e **[!UICONTROL Targeting automatico]** a 4-6 posizioni con 4-6 offerte per posizione. Configurazioni più grandi non sono consigliate e potrebbero essere soggette a restrizioni nell&#39;interfaccia utente [!DNL Target].

Nell&#39;interfaccia utente [!DNL Target] corrente, le attività **[!UICONTROL Automated Personalization]** e **[!UICONTROL Targeting automatico]** sono configurate direttamente nel passaggio **[!UICONTROL Esperienze]**. [!DNL Target] potrebbe visualizzare avvisi in linea o impedire il salvataggio di un&#39;attività quando la configurazione supera le soglie supportate e riconvalida la forma attività in **[!UICONTROL Avanti]**, **[!UICONTROL Salva]** e **[!UICONTROL Pubblica]**.

Per ulteriori informazioni sui limiti dei caratteri e altri limiti (dimensioni dell&#39;offerta, pubblico, profili, valori, parametri e così via) che influiscono sulle attività e su altri elementi in [!DNL Target], vedere [Limiti](/help/main/r-troubleshooting-target/target-limits.md).

+++

+++ È possibile specificare un&#39;esperienza specifica da utilizzare come controllo in un&#39;attività [!UICONTROL Automated Personalization]?

Puoi selezionare un&#39;esperienza specifica da usare come controllo durante la creazione di un&#39;attività [**[!UICONTROL Automated Personalization]**](/help/main/c-activities/t-automated-personalization/automated-personalization.md#automated-personalization-overview) (AP) o [**[!UICONTROL Targeting automatico]**](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT).

Questa funzione ti consente di indirizzare l’intero traffico di controllo a tale esperienza, in base alla percentuale di allocazione del traffico configurata nell’attività. Puoi quindi valutare i rapporti sulle prestazioni del traffico personalizzato rispetto al traffico verso l’esperienza di controllo.

Per ulteriori informazioni, vedere [Selezionare l&#39;esperienza di controllo](/help/main/c-activities/t-automated-personalization/experience-as-control.md).

+++

+++ Come viene implementato il targeting a livello di offerta?

Quando ogni visitatore arriva, le regole di targeting a livello di offerta determinano il set di offerte che il visitatore può vedere. L’algoritmo sceglie quindi tra queste offerte l’offerta che il modello prevede abbia il miglior ricavo atteso o la migliore possibilità di conversione. Il targeting delle offerte influisce sull&#39;efficacia degli algoritmi di apprendimento automatico [!DNL Target], pertanto utilizzali con la massima moderazione possibile. Per ulteriori informazioni, consulta [Targeting delle offerte di Personalizzazione automatizzata](/help/main/c-activities/t-automated-personalization/ap-target-offers.md).

+++

## Creazione di modelli e allocazione del traffico {#models-and-traffic}

+++ In che modo [!UICONTROL Automated Personalization] alloca il traffico della mia attività?

**[!UICONTROL Automated Personalization]** indirizza i visitatori all&#39;esperienza con la metrica di successo più elevata in base ai modelli di [Foresta casuale](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) più recenti. Questa previsione si basa sulle informazioni specifiche e sul contesto della visita del visitatore.

Si supponga, ad esempio, che un&#39;attività **[!UICONTROL Automated Personalization]** abbia due posizioni con due offerte ciascuna. Nella prima posizione, l’offerta A ha un tasso di conversione previsto del 3% per un visitatore specifico e l’offerta B ha un tasso di conversione previsto dell’1%. Nella seconda posizione, l’offerta C ha un tasso di conversione previsto del 2% per lo stesso visitatore e l’offerta D ha un tasso di conversione previsto del 5%. Pertanto, **[!UICONTROL Automated Personalization]** offre al visitatore un&#39;esperienza con l&#39;offerta A e l&#39;offerta D.

+++

+++ In che modo [!UICONTROL Automated Personalization] genera modelli in relazione agli ambienti?

Un modello è progettato per identificare le prestazioni della strategia personalizzata rispetto al traffico servito in modo casuale rispetto all’invio di tutto il traffico all’esperienza vincente complessiva. Questo modello considera gli hit e le conversioni solo nell’ambiente predefinito.

Viene creato un secondo set di modelli per ogni gruppo di reporting (**[!UICONTROL Automated Personalization]**) o esperienza (**[!UICONTROL Targeting automatico]**). Per ciascuno di questi modelli, vengono considerati gli hit e le conversioni in tutti gli ambienti.

Le richieste vengono quindi gestite con lo stesso modello, indipendentemente dall’ambiente. Tuttavia, la pluralità di traffico deve provenire dall’ambiente predefinito per garantire che l’esperienza vincente complessiva identificata sia coerente con il comportamento reale.

+++

+++ Quanto tempo devo aspettare per la generazione dei modelli?

Il tempo necessario alla generazione dei modelli nell’attività dipende in genere dal traffico delle posizioni dell’attività selezionate e dalla metrica di successo dell’attività. Utilizza [Calcolatore del traffico](/help/main/c-activities/t-automated-personalization/ap-traffic-estimator.md#use-traffic-estimator) per determinare il periodo di tempo previsto per la generazione dei modelli nell&#39;attività.

+++

+++ Come posso ridurre il tempo necessario alla generazione dei modelli nella mia attività [!UICONTROL Automated Personalization]?

Esamina l’impostazione dell’attività per individuare eventuali modifiche che migliorano la velocità di generazione dei modelli. Ad esempio, modifica una metrica di successo RPV in conversione, scegli una metrica di successo più vicina alle esperienze dell’attività nel funnel di vendita, elimina alcune esperienze dall’attività o utilizza una pagina con traffico più elevato. Per ulteriori informazioni, vedere [Risoluzione dei problemi di Automated Personalization](/help/main/c-activities/t-automated-personalization/ap-trouble.md).

+++

+++ Un modello è stato creato nell&#39;attività [!UICONTROL Automated Personalization]. Le visite a quell’esperienza sono personalizzate?

No. Per iniziare la personalizzazione, è necessario creare almeno due modelli nell’attività.

+++

## Risultati e incremento {#results-and-lift}

+++ Quando posso esaminare i risultati della mia attività [!UICONTROL Automated Personalization]?

Puoi iniziare a esaminare i risultati dell&#39;attività **[!UICONTROL Automated Personalization]** dopo che almeno due esperienze hanno generato modelli (indicati da un segno di spunta verde).

+++

+++ Perché la mia attività [!UICONTROL Automated Personalization] non mostra l&#39;incremento?

Sono necessari quattro fattori affinché un&#39;attività **[!UICONTROL Automated Personalization]** generi incremento:

* Le offerte in ogni posizione devono essere sufficientemente diverse da influenzare i visitatori.
* Le posizioni devono essere qualcosa che faccia la differenza per l’obiettivo di ottimizzazione.
* L’attività deve avere traffico e potenza statistica tali da consentire il rilevamento di un incremento.
* L’algoritmo di personalizzazione deve funzionare bene.

La migliore linea di azione è di assicurarsi in primo luogo, utilizzando una semplice attività di **[!UICONTROL Test A/B]** non personalizzata, che i contenuti e le posizioni che compongono le esperienze di attività facciano davvero una differenza per i tassi di risposta generali. Per la procedura completa, vedere [Risoluzione dei problemi di Automated Personalization](/help/main/c-activities/t-automated-personalization/ap-trouble.md).

+++

+++ Come posso confrontare [!UICONTROL Automated Personalization] con un&#39;esperienza predefinita?

Nessuna opzione chiavi in mano per confrontare **[!UICONTROL Automated Personalization]** con un&#39;esperienza predefinita. Come soluzione alternativa, se come parte dell&#39;attività esiste un&#39;offerta o un&#39;esperienza predefinita, fai clic sul segmento **[!UICONTROL Controllo]** nei report e individua tale offerta nel report a livello di offerta risultante. Il tasso di conversione registrato per questa offerta può essere confrontato con il tasso di conversione dell’intero segmento &quot;Foresta casuale&quot;. Questo confronto mostra le prestazioni del modello rispetto all’offerta predefinita.

+++

## Gestire un’attività live {#manage-live-activity}

+++ Quando devo interrompere l&#39;attività [!UICONTROL Automated Personalization]?

**[!UICONTROL Automated Personalization]** può essere utilizzato come personalizzazione &quot;sempre attiva&quot; che si ottimizza costantemente. Soprattutto per i contenuti fissi, non è necessario arrestare l&#39;attività **[!UICONTROL Automated Personalization]**. Se desideri apportare modifiche sostanziali al contenuto che non sono simili alle offerte attualmente nell’attività, la best practice consiste nell’avviare una nuova attività. L’avvio di una nuova attività aiuta gli altri utenti che esaminano i rapporti a evitare di confondere o correlare i risultati passati con contenuti diversi.

+++

+++ Posso cambiare la metrica obiettivo a metà strada attraverso un&#39;attività [!UICONTROL Automated Personalization]?

[!DNL Adobe] non consiglia di modificare la metrica obiettivo a metà strada in un&#39;attività. Anche se è possibile modificare la metrica dell&#39;obiettivo durante un&#39;attività utilizzando l&#39;interfaccia utente [!DNL Target], avviare sempre una nuova attività. [!DNL Adobe] non garantisce ciò che accade se si modifica la metrica obiettivo in un&#39;attività dopo che è in esecuzione.

Questo consiglio si applica alle attività **[!UICONTROL Allocazione automatica]**, **[!UICONTROL Targeting automatico]** e **[!UICONTROL Automated Personalization]** che utilizzano [!DNL Target] o [!DNL Analytics] (A4T) come origine per la generazione di rapporti.

+++

+++ È possibile utilizzare l&#39;opzione [!UICONTROL Ripristina dati report] durante l&#39;esecuzione di un&#39;attività [!UICONTROL Automated Personalization]?

[!DNL Adobe] sconsiglia di utilizzare l&#39;opzione **[!UICONTROL Ripristina dati report]** per **[!UICONTROL attività Automated Personalization]**. Anche se rimuove i dati di reporting visibili, questa opzione non rimuove tutti i record di formazione dal modello **[!UICONTROL Automated Personalization]**. Invece di utilizzare l&#39;opzione **[!UICONTROL Ripristina dati report]**, crea una nuova attività e disattiva l&#39;attività originale. Questa guida si applica anche alle attività **[!UICONTROL Allocazione automatica]** e **[!UICONTROL Targeting automatico]**.

+++

+++ Perché i visitatori visualizzano esperienze per un&#39;attività [!UICONTROL Automated Personalization] che non dovrebbero visualizzare?

**[!UICONTROL Le attività Automated Personalization]** vengono valutate una volta per sessione. Se ci sono sessioni attive idonee per una particolare esperienza e da allora sono state aggiunte nuove offerte, i visitatori visualizzano il nuovo contenuto insieme alle offerte precedentemente mostrate. Questi visitatori in precedenza si qualificavano per tali esperienze, che potranno quindi vedere ancora durante la sessione. Per valutare l&#39;attività a ogni visita di pagina, passa al tipo di attività **[!UICONTROL Targeting esperienza]** (XT).

+++
