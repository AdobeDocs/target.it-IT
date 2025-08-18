---
keywords: risoluzione dei problemi;domande frequenti;FAQ;personalizzazione automatizzata;controllo;esperienza predefinita;best practice
description: Esplora un elenco di domande frequenti e risposte sulle attività di [!UICONTROL Automated Personalization] (AP) in [!UICONTROL Adobe Target].
title: Come posso trovare le domande frequenti sulle attività [!UICONTROL Automated Personalization]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Automated Personalization
exl-id: 2bf62cc1-1781-4021-a400-2884e0bae893
source-git-commit: 336da9dd876243a0eea662b4604a8fc1e6a69b1a
workflow-type: tm+mt
source-wordcount: '1946'
ht-degree: 21%

---

# Domande frequenti su Automated Personalization

Consulta le seguenti domande frequenti e risposte mentre lavori con [!UICONTROL Automated Personalization] attività in [!DNL Adobe Target].

## È possibile specificare un&#39;esperienza specifica da utilizzare come controllo in un&#39;attività [!UICONTROL Automated Personalization]?

+++Vedi i dettagli

È possibile selezionare un&#39;esperienza da utilizzare come controllo durante la creazione di un&#39;attività [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) o [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT).

Questa funzione ti permette di indirizzare tutto il traffico di controllo a una specifica esperienza, in base alla percentuale di allocazione del traffico configurata nell’attività. Puoi quindi valutare i rapporti sulle prestazioni del traffico personalizzato rispetto al traffico verso l’esperienza di controllo.

Per ulteriori informazioni, consulta [Utilizzare un’esperienza specifica come controllo](/help/main/c-activities/t-automated-personalization/experience-as-control.md).

+++

## Come posso confrontare [!UICONTROL Automated Personalization] con un&#39;esperienza predefinita? {#section_46C1A620A2384C2C8392D6716DD18495}

+++Vedi i dettagli

Non è disponibile un&#39;opzione chiavi in mano per confrontare [!UICONTROL Automated Personalization] con un&#39;esperienza predefinita. Tuttavia, come soluzione alternativa, se esiste un&#39;offerta o un&#39;esperienza predefinita come parte dell&#39;attività complessiva, per comprenderne le prestazioni linea di base, fai clic sul segmento &quot;[!UICONTROL Control]&quot; nei rapporti e individua tale offerta nel rapporto a livello di offerta risultante. Il tasso di conversione registrato per questa offerta può essere utilizzato per confrontare con il tasso di conversazione dell’intero segmento &quot;Foresta casuale&quot;. Questo permette di confrontare le prestazioni della macchina rispetto all’offerta predefinita.

+++

## Quali sono le best practice per impostare un&#39;attività [!UICONTROL Automated Personalization]? {#section_E155B26282BE49B58EA2683413D11DE6}

+++Vedi i dettagli

* Se desideri personalizzare una pagina a traffico ridotto o apportare modifiche strutturali all&#39;esperienza che stai personalizzando, puoi utilizzare un&#39;attività [!UICONTROL Auto-Target] invece di [!UICONTROL Automated Personalization]. Vedi [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md).
* Prendere in considerazione il completamento di un&#39;attività [!UICONTROL A/B Test] tra le offerte e le posizioni che si prevede di utilizzare nell&#39;attività [!UICONTROL Automated Personalization] per assicurarsi che la posizione e le offerte abbiano un impatto sull&#39;obiettivo di ottimizzazione. Se un&#39;attività [!UICONTROL A/B Test] non riesce a dimostrare una differenza significativa, è probabile che anche [!UICONTROL Automated Personalization] non riesca a generare un incremento.

   * Se un test A/B...N non mostra differenze statisticamente significative tra le esperienze, una o più delle seguenti situazioni è probabilmente responsabile:

      * È probabile che le offerte non siano sufficientemente diverse tra loro.
      * Le posizioni selezionate non influiscono sulla metrica di successo.
      * L’obiettivo di ottimizzazione è troppo lontano nel funnel di conversione per essere influenzato dalle offerte scelte.

* Assicurati di utilizzare il [Calcolatore del traffico](/help/main/c-activities/t-automated-personalization/ap-traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) per capire quanto tempo ci vuole per la generazione dei modelli di personalizzazione nell&#39;attività [!UICONTROL Automated Personalization].
* Decidi l’allocazione tra il controllo e il targeting prima di iniziare l’attività, in base ai tuoi obiettivi.

  Esistono tre scenari da considerare in base all’obiettivo dell’attività e al tipo di controllo selezionato:

   * **Controllo: esperienze casuali; obiettivo dell&#39;attività: testare l&#39;efficacia dell&#39;algoritmo di personalizzazione**: se l&#39;obiettivo è quello di valutare l&#39;algoritmo di personalizzazione, è necessario avere un&#39;immagine più precisa dell&#39;incremento. Inoltre, è molto probabile che si voglia confrontare il tasso di conversione per le esperienze o le offerte se si è semplicemente fatto un [!UICONTROL A/B Test] (un controllo fornito in modo casuale). In tal caso, si consiglia di utilizzare un’allocazione del 50% a un controllo composto da esperienze distribuite in modo casuale.
   * **&quot;Esperienze casuali&quot; come controllo e l&#39;obiettivo dell&#39;attività è quello di massimizzare il traffico personalizzato**: se l&#39;algoritmo va bene e desideri che la quantità massima di traffico sia personalizzata, si consiglia di allocare al controllo dal 10% al 30% del traffico. Il compromesso qui è la precisione che vedete nelle informazioni sull&#39;incremento. Gli intervalli di affidabilità del traffico di controllo sono più ampi perché il traffico verso di essi scorre meno.
   * **Controllo: esperienza specifica; entrambi i tipi di obiettivo**: se desideri confrontare con i modelli di personalizzazione un’esperienza specifica definita dagli esperti di marketing, si consiglia di allocare al controllo dal 10% al 30% del traffico. Quando selezioni una sola esperienza come controllo, tale traffico non viene distribuito su ogni offerta o esperienza nell’attività.

* Le regole di targeting devono essere utilizzate con la massima parsimonia possibile perché possono interferire con la capacità di ottimizzazione del modello.
* I gruppi di reporting possono limitare il successo dell&#39;attività [!UICONTROL Automated Personalization]. Utilizza i gruppi di reporting solo in determinate condizioni:

   * Utilizza i gruppi di reporting solo se sono soddisfatte le seguenti condizioni:

      * Pianifica la sostituzione o l’aggiunta di nuove offerte mentre l’attività è in esecuzione.
      * Le offerte nel gruppo di reporting si rivolgono agli stessi visitatori.
      * Le offerte in quel gruppo di reporting hanno circa lo stesso tasso di risposta complessivo.

   * Non esiste alcuna personalizzazione tra le offerte di un gruppo di reporting. Le offerte vengono tutte trattate come tali dal modello di personalizzazione.
   * Non mettere mai tutte le offerte di un’attività in un singolo gruppo di rapporti. In questo modo tutte le offerte vengono distribuite in modo casuale e uniforme a tutti i visitatori nell’attività.

+++

## Quali sono alcuni limiti in [!UICONTROL Automated Personalization]? {#section_08BA09ED51B547299963C94FE6417CFA}

+++Vedi i dettagli

[!DNL Target] ha un limite massimo di 30.000 esperienze, ma funziona al meglio quando vengono create meno di 10.000 esperienze.

Lo stesso limite viene applicato anche quando l&#39;attività ha abilitato l&#39;opzione [!UICONTROL Disalow Duplicates].

Per ulteriori informazioni sui limiti dei caratteri e altri limiti (dimensioni dell&#39;offerta, pubblico, profili, valori, parametri e così via) che influiscono sulle attività e su altri elementi in [!DNL Target], vedere [Limiti](/help/main/r-troubleshooting-target/target-limits.md).

+++

## Come viene implementato il targeting a livello di offerta? {#section_9D7A86EA93D74E9B8C81072A681263A4}

+++Vedi i dettagli

Quando arriva un visitatore, il set di possibili offerte che il visitatore può visualizzare è determinato dalle regole di targeting a livello di offerta. Quindi, l’algoritmo sceglie l’offerta che il modello prevede produca il miglior ricavo atteso o la migliore possibilità di conversione da tali offerte. Il targeting delle offerte influisce sull&#39;efficacia di [!DNL Target] algoritmi di apprendimento automatico e, di conseguenza, deve essere utilizzato con la massima moderazione possibile.

+++

## Perché la mia attività [!UICONTROL Automated Personalization] non viene visualizzata? {#section_BFA07C8C258F45318F73A461B8F32737}

+++Vedi i dettagli

Sono necessari quattro fattori affinché un&#39;attività [!UICONTROL Automated Personalization] generi incremento:

* Le offerte in ogni posizione devono essere sufficientemente diverse da influenzare i visitatori.
* Le posizioni devono essere qualcosa che faccia la differenza per l’obiettivo di ottimizzazione.
* L’attività deve avere traffico e potenza statistica tali da consentire il rilevamento di un incremento.
* L’algoritmo di personalizzazione deve funzionare bene.

La migliore linea di azione è di assicurarsi in primo luogo che i contenuti e le posizioni che compongono le esperienze di attività facciano davvero una differenza per i tassi di risposta generali utilizzando una semplice attività [!UICONTROL A/B Test] non personalizzata. Calcola le dimensioni del campione in tempo per assicurarti che sia possibile visualizzare un incremento ragionevole ed esegui il test A/B per una durata fissa senza interruzioni né modifiche. Se i risultati del test A/B mostrano un incremento statisticamente significativo su una o più esperienze, è probabile che un’attività personalizzata abbia esito positivo. Personalization può funzionare anche se non ci sono differenze nei tassi di risposta generali delle esperienze. In genere, il problema deriva dal fatto che le offerte o le posizioni non hanno un impatto sufficiente sull’obiettivo di ottimizzazione da rilevare con significatività statistica.

Per ulteriori informazioni, consulta [Risoluzione dei problemi relativi alla personalizzazione automatica](/help/main/c-activities/t-automated-personalization/ap-trouble.md#reference_281954549C3E49E2B5498009BBDC62CA).

+++

## Come sta [!UICONTROL Automated Personalization] allocando il traffico della mia attività? {#section_4369364F77804E0D9B78BEE551DA5659}

+++Vedi i dettagli

[!UICONTROL Automated Personalization] indirizza i visitatori all&#39;esperienza con la metrica di successo più elevata in base ai modelli di [Foresta casuale](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) più recenti generati per ciascun modello. Questa previsione si basa sulle informazioni specifiche del visitatore e sul contesto di visita.

Si supponga, ad esempio, che un&#39;attività [!UICONTROL Automated Personalization] abbia due posizioni con due offerte ciascuna. Nella prima posizione, l’offerta A ha un tasso di conversione previsto del 3% per un visitatore specifico e l’offerta B ha un tasso di conversione previsto dell’1%. Nella seconda posizione, l’offerta C ha un tasso di conversione previsto del 2% per lo stesso visitatore e l’offerta D ha un tasso di conversione previsto del 5%. Pertanto, [!UICONTROL Automated Personalization] offre al visitatore un&#39;esperienza con l&#39;offerta A e l&#39;offerta D.

+++

## Quando devo interrompere l&#39;attività [!UICONTROL Automated Personalization]? {#section_C51F3DAB8887463BB147373F6FE06B93}

+++Vedi i dettagli

[!UICONTROL Automated Personalization] può essere utilizzato come personalizzazione &quot;sempre attiva&quot; che si ottimizza costantemente. Soprattutto per i contenuti fissi, non è necessario interrompere l&#39;attività [!UICONTROL Automated Personalization]. Se si desidera apportare modifiche sostanziali al contenuto che non sono simili alle offerte attualmente presenti nell&#39;attività [!UICONTROL Automated Personalization], la procedura consigliata consiste nell&#39;avviare una nuova attività. L’avvio di una nuova attività consente ad altri utenti che revisionano i rapporti di non confondere o correlare i risultati passati con contenuti diversi.

+++

## Quanto tempo devo aspettare per la generazione dei modelli? {#section_6F6A5A9DB3564BE6B22FFEDFA5B29619}

+++Vedi i dettagli

Il tempo necessario alla generazione dei modelli nell’attività dipende in genere dal traffico delle posizioni dell’attività selezionate e dalla metrica di successo dell’attività. Utilizza [Calcolatore del traffico](/help/main/c-activities/t-automated-personalization/ap-traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) per determinare il periodo di tempo previsto per la generazione dei modelli nell&#39;attività.

+++

## Un modello è generato nella mia attività [!UICONTROL Automated Personalization]. Le visite a quell’esperienza sono personalizzate? {#section_51EA953C6D1D4A3185FC9DD290D66621}

+++Vedi i dettagli

No, per iniziare la personalizzazione occorrono almeno due modelli generati nell’attività.

+++

## Quando posso esaminare i risultati della mia attività [!UICONTROL Automated Personalization]? {#section_05DB5ACAE6AD429C9510766A7268EE2C}

+++Vedi i dettagli

È possibile iniziare a esaminare i risultati dell&#39;attività [!UICONTROL Automated Personalization] dopo aver creato almeno due esperienze con modelli (segno di spunta verde) per l&#39;esperienza con modelli generati.

+++

## Come posso ridurre il tempo necessario alla generazione dei modelli nella mia attività [!UICONTROL Automated Personalization]? {#section_CCB8CEE98DAA40BA93AADCD596C48D82}

+++Vedi i dettagli

Esamina la configurazione dell’attività e osserva se sei disposto a apportare modifiche per migliorare la velocità di generazione dei modelli.

* La metrica del successo è molto in basso nel funnel di vendita dalle esperienze dell’attività? Con un tasso di conversione basso, la generazione dei modelli richiederà più traffico poiché è necessario un numero minimo di conversioni.
* Se la metrica di successo è impostata su RPV, è possibile modificare la conversione? Le attività di conversione tendono a richiedere meno traffico per la generazione dei modelli.
* Puoi eliminare alcune esperienze dalla tua attività? La riduzione del numero di esperienze in un’attività velocizza il tempo necessario per creare modelli.
* Esiste una pagina con traffico più elevato in cui questa attività avrebbe più successo? Maggiore è il traffico e le conversioni nelle posizioni di attività, più rapidi saranno i modelli generati.

+++

## Perché i visitatori visualizzano esperienze per un&#39;attività [!UICONTROL Automated Personalization] che non dovrebbero visualizzare? {#section_41CECEAE0881446A8D9F3B016857914B}

+++Vedi i dettagli

[!UICONTROL Automated Personalization] attività vengono valutate una volta per sessione. Se ci sono sessioni attive idonee per una particolare esperienza e ora sono state aggiunte nuove offerte, i visitatori vedranno il nuovo contenuto insieme alle offerte precedentemente mostrate. Poiché questi visitatori in precedenza erano qualificati per tali esperienze, le visualizzano ancora durante la sessione. Per valutare questa situazione a ogni visita di pagina, devi passare al tipo di attività [!UICONTROL Experience Targeting] (XT).

+++

## Posso cambiare la metrica obiettivo a metà strada attraverso un&#39;attività [!UICONTROL Automated Personalization]? {#change-metric}

+++Vedi i dettagli

[!DNL Adobe] non consiglia di modificare la metrica obiettivo a metà strada in un&#39;attività. Anche se è possibile modificare la metrica dell’obiettivo durante un’attività utilizzando l’interfaccia utente [!DNL Target], è sempre necessario avviare una nuova attività. [!DNL Adobe] non forniscono alcuna garanzia su ciò che accade se si modifica la metrica obiettivo in un&#39;attività dopo l&#39;esecuzione.

Questo consiglio si applica alle attività [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target] e [!UICONTROL Automated Personalization] che utilizzano [!DNL Target] o [!DNL Analytics] (A4T) come origine per la generazione di rapporti.

+++

## È possibile utilizzare l&#39;opzione [!UICONTROL Reset Report Data] durante l&#39;esecuzione di un&#39;attività [!UICONTROL Automated Personalization]?

+++Vedi i dettagli

[!DNL Adobe] sconsiglia di utilizzare l&#39;opzione [!UICONTROL Reset Report Data] per le attività [!UICONTROL Automated Personalization]. Anche se rimuove i dati di reporting visibili, questa opzione non rimuove tutti i record di formazione dal modello [!UICONTROL Automated Personalization]. Invece di utilizzare l&#39;opzione [!UICONTROL Reset Report Data] per le attività [!UICONTROL Automated Personalization], crea una nuova attività e disattiva l&#39;attività originale. Questa guida si applica anche alle attività [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target].

+++

## In che modo [!UICONTROL Automated Personalization] genera i modelli rispetto agli ambienti?

+++Vedi i dettagli

Un modello è progettato per identificare le prestazioni della strategia personalizzata rispetto al traffico servito in modo casuale rispetto all’invio di tutto il traffico all’esperienza vincente complessiva. Questo modello considera gli hit e le conversioni solo nell’ambiente predefinito.

Il traffico proveniente da un secondo set di modelli viene generato per ogni gruppo di modeling ([!UICONTROL Automated Personalization]) o esperienza ([!UICONTROL Auto-Target]). Per ciascuno di questi modelli, vengono considerati gli hit e le conversioni in tutti gli ambienti.

Le richieste vengono quindi gestite con lo stesso modello, indipendentemente dall’ambiente. Tuttavia, la pluralità di traffico deve provenire dall’ambiente predefinito per garantire che l’esperienza vincente complessiva identificata sia coerente con il comportamento reale.

+++
