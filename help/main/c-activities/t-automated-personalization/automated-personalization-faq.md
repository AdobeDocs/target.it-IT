---
keywords: risoluzione dei problemi;domande frequenti;FAQ;personalizzazione automatizzata;controllo;esperienza predefinita;best practice
description: Esplora un elenco di domande frequenti e relative risposte su [!UICONTROL Automated Personalization] Attività di (AP) in [!UICONTROL Adobe Target].
title: Come posso trovare le domande frequenti su [!UICONTROL Automated Personalization] Attività?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."
feature: Automated Personalization
exl-id: 2bf62cc1-1781-4021-a400-2884e0bae893
source-git-commit: 336da9dd876243a0eea662b4604a8fc1e6a69b1a
workflow-type: tm+mt
source-wordcount: '2054'
ht-degree: 24%

---

# Domande frequenti su Automated Personalization

Consulta le seguenti domande frequenti e risposte mentre lavori con [!UICONTROL Automated Personalization] attività in [!DNL Adobe Target].

## Posso specificare un’esperienza specifica da usare come controllo in un? [!UICONTROL Automated Personalization] attività?

+++Consulta i dettagli

Puoi selezionare un’esperienza da usare come controllo durante la creazione di un’ [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) o [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT).

Questa funzione ti permette di indirizzare tutto il traffico di controllo a una specifica esperienza, in base alla percentuale di allocazione del traffico configurata nell’attività. Puoi quindi valutare i rapporti sulle prestazioni del traffico personalizzato rispetto al traffico verso l’esperienza di controllo.

Per ulteriori informazioni, consulta [Utilizzare un’esperienza specifica come controllo](/help/main/c-activities/t-automated-personalization/experience-as-control.md).

+++

## Come posso confrontare [!UICONTROL Automated Personalization] a un’esperienza predefinita? {#section_46C1A620A2384C2C8392D6716DD18495}

+++Consulta i dettagli

Non esiste un&#39;opzione di confronto chiavi in mano [!UICONTROL Automated Personalization] a un’esperienza predefinita. Tuttavia, come soluzione alternativa, se esiste un’offerta o esperienza predefinita come parte dell’attività complessiva, per comprenderne le prestazioni di base fai clic su &quot;[!UICONTROL Controllo]&quot; nei rapporti e individuare tale offerta particolare nel rapporto a livello di offerta risultante. Il tasso di conversione registrato per questa offerta può essere utilizzato per confrontare con il tasso di conversazione dell’intero segmento &quot;Foresta casuale&quot;. Questo permette di confrontare le prestazioni della macchina rispetto all’offerta predefinita.

+++

## Quali sono le best practice per impostare un’ [!UICONTROL Automated Personalization] attività? {#section_E155B26282BE49B58EA2683413D11DE6}

+++Consulta i dettagli

* Se desideri personalizzare una pagina a traffico ridotto o apportare modifiche strutturali all’esperienza che stai personalizzando, puoi utilizzare un’ [!UICONTROL Targeting automatico] attività in sostituzione di [!UICONTROL Automated Personalization]. Consulta [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md).
* Considera il completamento di un [!UICONTROL Test A/B] attività tra le offerte e le posizioni che intendi utilizzare nel tuo [!UICONTROL Automated Personalization] per garantire che la posizione e le offerte abbiano un impatto sull’obiettivo di ottimizzazione. Se un [!UICONTROL Test A/B] l&#39;attività non dimostra una differenza significativa, [!UICONTROL Automated Personalization] probabilmente non riesce a generare l’incremento.

   * Se un test A/B...N non mostra differenze statisticamente significative tra le esperienze, una o più delle seguenti situazioni è probabilmente responsabile:

      * È probabile che le offerte non siano sufficientemente diverse tra loro.
      * Le posizioni selezionate non influiscono sulla metrica di successo.
      * L’obiettivo di ottimizzazione è troppo lontano nel funnel di conversione per essere influenzato dalle offerte scelte.

* Assicurati di utilizzare il [Calcolatore del traffico](/help/main/c-activities/t-automated-personalization/ap-traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) puoi capire quanto tempo ci vuole affinché i modelli di personalizzazione vengano generati nel tuo [!UICONTROL Automated Personalization] attività.
* Decidi l’allocazione tra il controllo e il targeting prima di iniziare l’attività, in base ai tuoi obiettivi.

  Esistono tre scenari da considerare in base all’obiettivo dell’attività e al tipo di controllo selezionato:

   * **Controllo: esperienze casuali; obiettivo dell’attività: testare l’efficacia dell’algoritmo di personalizzazione**: se il tuo obiettivo è quello di valutare l’algoritmo di personalizzazione, vuoi ottenere un’immagine più precisa dell’incremento. Inoltre, molto probabilmente vorrai confrontare il tasso di conversione per le esperienze o le offerte nel caso in cui ti sia limitato a [!UICONTROL Test A/B] (controllo casuale). In tal caso, si consiglia di utilizzare un’allocazione del 50% a un controllo composto da esperienze distribuite in modo casuale.
   * **Controllo: esperienze casuali; obiettivo dell’attività: massimizzare il traffico personalizzato**: se l’algoritmo va bene e desideri che la quantità massima di traffico sia personalizzata, si consiglia di allocare al controllo dal 10% al 30% del traffico. Il compromesso qui è la precisione che vedete nelle informazioni sull&#39;incremento. Gli intervalli di affidabilità del traffico di controllo sono più ampi perché il traffico verso di essi scorre meno.
   * **Controllo: esperienza specifica; entrambi i tipi di obiettivo**: se desideri confrontare con i modelli di personalizzazione un’esperienza specifica definita dagli esperti di marketing, si consiglia di allocare al controllo dal 10% al 30% del traffico. Quando selezioni una sola esperienza come controllo, tale traffico non viene distribuito su ogni offerta o esperienza nell’attività.

* Le regole di targeting devono essere utilizzate con la massima parsimonia possibile perché possono interferire con la capacità di ottimizzazione del modello.
* I gruppi di reporting possono limitare il successo della [!UICONTROL Automated Personalization] attività. Utilizza i gruppi di reporting solo in determinate condizioni:

   * Utilizza i gruppi di reporting solo se sono soddisfatte le seguenti condizioni:

      * Pianifica la sostituzione o l’aggiunta di nuove offerte mentre l’attività è in esecuzione.
      * Le offerte nel gruppo di reporting si rivolgono agli stessi visitatori.
      * Le offerte in quel gruppo di reporting hanno circa lo stesso tasso di risposta complessivo.

   * Non esiste alcuna personalizzazione tra le offerte di un gruppo di reporting. Le offerte vengono tutte trattate come tali dal modello di personalizzazione.
   * Non mettere mai tutte le offerte di un’attività in un singolo gruppo di rapporti. In questo modo tutte le offerte vengono distribuite in modo casuale e uniforme a tutti i visitatori nell’attività.

+++

## Quali sono alcuni limiti in [!UICONTROL Automated Personalization]? {#section_08BA09ED51B547299963C94FE6417CFA}

+++Consulta i dettagli

[!DNL Target] supporta fino a 30.000 esperienze, ma funziona al meglio quando sono create meno di 10.000 esperienze.

Lo stesso limite viene applicato anche quando l’attività ha abilitato [!UICONTROL Disabilita duplicati] opzione.

Per ulteriori informazioni sui limiti dei caratteri e altri limiti (dimensioni dell’offerta, pubblico, profili, valori, parametri e così via) che influenzano le attività e altri elementi in [!DNL Target], vedi [Limiti](/help/main/r-troubleshooting-target/target-limits.md).

+++

## Come viene implementato il targeting a livello di offerta? {#section_9D7A86EA93D74E9B8C81072A681263A4}

+++Consulta i dettagli

Quando arriva un visitatore, il set di possibili offerte che il visitatore può visualizzare è determinato dalle regole di targeting a livello di offerta. Quindi, l’algoritmo sceglie l’offerta che il modello prevede produca il miglior ricavo atteso o la migliore possibilità di conversione da tali offerte. Il targeting delle offerte influisce sull’efficacia di [!DNL Target] gli algoritmi di apprendimento automatico e, di conseguenza, dovrebbero essere utilizzati con la massima moderazione possibile.

+++

## Perché il mio [!UICONTROL Automated Personalization] l&#39;attività non mostra l&#39;incremento? {#section_BFA07C8C258F45318F73A461B8F32737}

+++Consulta i dettagli

Ci sono quattro fattori necessari per [!UICONTROL Automated Personalization] attività per generare l’incremento:

* Le offerte in ogni posizione devono essere sufficientemente diverse da influenzare i visitatori.
* Le posizioni devono essere qualcosa che faccia la differenza per l’obiettivo di ottimizzazione.
* L’attività deve avere traffico e potenza statistica tali da consentire il rilevamento di un incremento.
* L’algoritmo di personalizzazione deve funzionare bene.

La migliore linea di azione è di assicurarsi in primo luogo che i contenuti e le posizioni, che compongono le esperienze di attività, facciano davvero una differenza per i tassi di risposta generali utilizzando un [!UICONTROL Test A/B] attività. Calcola le dimensioni del campione in tempo per assicurarti che sia possibile visualizzare un incremento ragionevole ed esegui il test A/B per una durata fissa senza interruzioni né modifiche. Se i risultati del test A/B mostrano un incremento statisticamente significativo su una o più esperienze, è probabile che un’attività personalizzata abbia esito positivo. La personalizzazione può funzionare anche se non ci sono differenze nei tassi di risposta generali delle esperienze. In genere, il problema deriva dal fatto che le offerte o le posizioni non hanno un impatto sufficiente sull’obiettivo di ottimizzazione da rilevare con significatività statistica.

Per ulteriori informazioni, consulta [Risoluzione dei problemi relativi alla personalizzazione automatica](/help/main/c-activities/t-automated-personalization/ap-trouble.md#reference_281954549C3E49E2B5498009BBDC62CA).

+++

## Com’è [!UICONTROL Automated Personalization] allocare il traffico della mia attività? {#section_4369364F77804E0D9B78BEE551DA5659}

+++Consulta i dettagli

La personalizzazione automatizzata indirizza i visitatori all’esperienza con la metrica di successo più elevata in base ai modelli di [Foresta casuale](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) più recenti costruiti per ciascun modello. Questa previsione si basa sulle informazioni specifiche del visitatore e sul contesto di visita.

Ad esempio, si supponga che un [!UICONTROL Automated Personalization] l’attività aveva due posizioni con due offerte ciascuna. Nella prima posizione, l’offerta A ha un tasso di conversione previsto del 3% per un visitatore specifico e l’offerta B ha un tasso di conversione previsto dell’1%. Nella seconda posizione, l’offerta C ha un tasso di conversione previsto del 2% per lo stesso visitatore e l’offerta D ha un tasso di conversione previsto del 5%. Pertanto, [!UICONTROL Automated Personalization] offre al visitatore un’esperienza con l’Offerta A e l’Offerta D.

+++

## Quando devo interrompere il mio [!UICONTROL Automated Personalization] attività? {#section_C51F3DAB8887463BB147373F6FE06B93}

+++Consulta i dettagli

[!UICONTROL Automated Personalization] può essere utilizzata come personalizzazione &quot;sempre attiva&quot; che si ottimizza costantemente. Soprattutto per i contenuti fissi, non è necessario arrestare [!UICONTROL Automated Personalization] attività. Se desideri apportare modifiche sostanziali al contenuto che non sono simili alle offerte attualmente nel tuo [!UICONTROL Automated Personalization] attività, la best practice consiste nell’avviare una nuova attività. L’avvio di una nuova attività consente ad altri utenti che revisionano i rapporti di non confondere o correlare i risultati passati con contenuti diversi.

+++

## Quanto tempo devo aspettare per la generazione dei modelli? {#section_6F6A5A9DB3564BE6B22FFEDFA5B29619}

+++Consulta i dettagli

Il tempo necessario alla generazione dei modelli nell’attività dipende in genere dal traffico delle posizioni dell’attività selezionate e dalla metrica di successo dell’attività. Utilizza il [Calcolatore del traffico](/help/main/c-activities/t-automated-personalization/ap-traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) per determinare il periodo di tempo previsto per la generazione dei modelli nell’attività.

+++

## Un modello è generato nel mio [!UICONTROL Automated Personalization] attività. Le visite a quell’esperienza sono personalizzate? {#section_51EA953C6D1D4A3185FC9DD290D66621}

+++Consulta i dettagli

No, per iniziare la personalizzazione occorrono almeno due modelli generati nell’attività.

+++

## Quando posso esaminare i risultati [!UICONTROL Automated Personalization] attività? {#section_05DB5ACAE6AD429C9510766A7268EE2C}

+++Consulta i dettagli

Puoi iniziare a esaminare i risultati dei [!UICONTROL Automated Personalization] attività dopo aver creato almeno due esperienze con modelli (segno di spunta verde) per l’esperienza con modelli generati.

+++

## Come posso ridurre il tempo necessario alla generazione dei modelli nel mio [!UICONTROL Automated Personalization] attività? {#section_CCB8CEE98DAA40BA93AADCD596C48D82}

+++Consulta i dettagli

Esamina la configurazione dell’attività e osserva se sei disposto a apportare modifiche per migliorare la velocità di generazione dei modelli.

* La metrica del successo è molto in basso nel funnel di vendita dalle esperienze dell’attività? Con un tasso di conversione basso, la generazione dei modelli richiederà più traffico poiché è necessario un numero minimo di conversioni.
* Se la metrica di successo è impostata su RPV, è possibile modificare la conversione? Le attività di conversione tendono a richiedere meno traffico per la generazione dei modelli.
* Puoi eliminare alcune esperienze dalla tua attività? La riduzione del numero di esperienze in un’attività velocizza il tempo necessario per creare modelli.
* Esiste una pagina con traffico più elevato in cui questa attività avrebbe più successo? Maggiore è il traffico e le conversioni nelle posizioni di attività, più rapidi saranno i modelli generati.

+++

## Perché i visitatori visualizzano esperienze per un [!UICONTROL Automated Personalization] attività che non dovrebbero vedere? {#section_41CECEAE0881446A8D9F3B016857914B}

+++Consulta i dettagli

[!UICONTROL Le attività di personalizzazione automatizzata vengono valutate una volta per sessione. ] Se ci sono sessioni attive idonee per una particolare esperienza e ora sono state aggiunte nuove offerte, i visitatori vedranno il nuovo contenuto insieme alle offerte precedentemente mostrate. Poiché questi visitatori in precedenza erano qualificati per tali esperienze, le visualizzano ancora durante la sessione. Per valutare questo aspetto a ogni visita della pagina, devi modificare il [!UICONTROL Targeting esperienza] (XT) tipo di attività.

+++

## Posso cambiare la metrica di obiettivo a metà strada attraverso un [!UICONTROL Automated Personalization] attività? {#change-metric}

+++Consulta i dettagli

[!DNL Adobe] sconsiglia di modificare la metrica obiettivo a metà strada attraverso un’attività. Anche se è possibile modificare la metrica dell’obiettivo durante un’attività utilizzando l’interfaccia utente [!DNL Target], è sempre necessario avviare una nuova attività. [!DNL Adobe] non fornire alcuna garanzia su ciò che accade se modifichi la metrica obiettivo in un’attività dopo l’esecuzione.

Questo consiglio si applica alle attività [!UICONTROL Allocazione automatica], [!UICONTROL Targeting automatico] e [!UICONTROL Automated Personalization] che utilizzano [!DNL Target] o [!DNL Analytics] (A4T) come origine per la generazione di rapporti.

+++

## Posso utilizzare il [!UICONTROL Ripristina dati rapporto] durante l&#39;esecuzione di un [!UICONTROL Automated Personalization] attività?

+++Consulta i dettagli

[!DNL Adobe] non consiglia di utilizzare il [!UICONTROL Ripristina dati rapporto] opzione per [!UICONTROL Automated Personalization] attività. Anche se rimuove i dati di reporting visibili, questa opzione non rimuove tutti i record di formazione dal [!UICONTROL Automated Personalization] modello. Invece di utilizzare [!UICONTROL Ripristina dati rapporto] opzione per [!UICONTROL Automated Personalization] , crea una nuova attività e disattiva l&#39;attività originale. Questa guida si applica anche a [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico] attività.

+++

## In che modo [!UICONTROL Automated Personalization] creare modelli per quanto riguarda gli ambienti?

+++Consulta i dettagli

Un modello è progettato per identificare le prestazioni della strategia personalizzata rispetto al traffico servito in modo casuale rispetto all’invio di tutto il traffico all’esperienza vincente complessiva. Questo modello considera gli hit e le conversioni solo nell’ambiente predefinito.

Il traffico proveniente da un secondo set di modelli viene generato per ciascun gruppo di modellazione ([!UICONTROL Automated Personalization]) o esperienza ([!UICONTROL Targeting automatico]). Per ciascuno di questi modelli, vengono considerati gli hit e le conversioni in tutti gli ambienti.

Le richieste vengono quindi gestite con lo stesso modello, indipendentemente dall’ambiente. Tuttavia, la pluralità di traffico deve provenire dall’ambiente predefinito per garantire che l’esperienza vincente complessiva identificata sia coerente con il comportamento reale.

+++
