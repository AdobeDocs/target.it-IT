---
description: Elenco delle domande frequenti sulla Personalizzazione automatizzata.
keywords: risoluzione dei problemi;domande frequenti;FAQ;FAQs;personalizzazione automatizzata
seo-description: Elenco delle domande frequenti sulla Personalizzazione automatizzata.
seo-title: Domande frequenti sulla Personalizzazione automatizzata
solution: Target
title: Domande frequenti sulla Personalizzazione automatizzata
title-outputclass: premium
topic: Premium
uuid: 4c8aadd3-75c3-4388-b838-e62576dfb955
badge: premium
translation-type: tm+mt
source-git-commit: add895d353e7483dfcbe82f1bca55b277bc65f20

---


# ![PREMIUM](/help/assets/premium.png) Domande frequenti sulla Personalizzazione automatizzata{#automated-personalization-faq}

Elenco delle domande frequenti sulla Personalizzazione automatizzata.

## Posso specificare un'esperienza specifica da usare come controllo?

You can select an experience to be used as control while creating an [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) or [Auto-Target](/help/c-activities/auto-target-to-optimize.md) (AT) activity.

Questa funzione consente di indirizzare l'intero traffico di controllo a un'esperienza specifica, in base alla percentuale di allocazione del traffico configurata nell'attività. Potete quindi valutare i rapporti sulle prestazioni del traffico personalizzato contro il controllo del traffico verso quella singola esperienza.

For more information, see [Use a specific experience as control](/help/c-activities/t-automated-personalization/experience-as-control.md).

## Come posso confrontare la Personalizzazione automatizzata con un’esperienza predefinita? {#section_46C1A620A2384C2C8392D6716DD18495}

Non esiste un’opzione diretta per confrontare la Personalizzazione automatizzata con un’esperienza predefinita. Tuttavia, per ovviare al problema, se un’offerta o un’esperienza predefinita esiste come parte dell’attività complessiva, per comprenderne le prestazioni di base puoi fare clic sul segmento “Controllo” nei rapporti e individuare l’offerta specifica nel rapporto risultante a livello di offerta. Il tasso di conversione registrato per questa offerta può essere confrontato con il tasso di conversione dell’intero segmento “Foresta casuale”. Questo permette di confrontare le prestazioni della macchina rispetto all’offerta predefinita.

## Quali sono le best practice per impostare un’attività di Personalizzazione automatizzata? {#section_E155B26282BE49B58EA2683413D11DE6}

* Se vuoi personalizzare una pagina con traffico più basso o apportare modifiche strutturali all’esperienza che stai personalizzando, considera l’utilizzo della funzione Targeting automatico invece di Personalizzazione automatizzata. Consulta [Targeting automatico per esperienze personalizzate](../../c-activities/auto-target-to-optimize.md#concept_67779E5B7F67427A97D7EA2A6FB919B3).
* È consigliabile completare un’attività A/B tra le offerte e le posizioni che prevedi di utilizzare nell’attività di Personalizzazione automatizzata per garantire che le posizioni e le offerte abbiano un impatto sull’obiettivo di ottimizzazione. Se per un’attività A/B non è possibile dimostrare una differenza significativa, è probabile che nemmeno la Personalizzazione automatizzata riesca a generare incrementi.

   * Se un test A/B...N non mostra differenze statisticamente significative tra le esperienze, probabilmente le offerte che stai prendendo in considerazione non sono sufficientemente diverse tra loro, le posizioni selezionate non incidono sulla metrica di successo oppure l’obiettivo di ottimizzazione è troppo lontano nel funnel di conversione per essere influenzato dalle offerte scelte.

* Assicurati di utilizzare il [Calcolatore del traffico](../../c-activities/t-automated-personalization/ap-traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) per farti un’idea di quanto tempo ci vorrà per la generazione dei modelli di personalizzazione nell’attività di Personalizzazione automatizzata.
* In base ai tuoi obiettivi, decidi la ripartizione tra controllo e destinazione prima di iniziare l’attività.

   Esistono tre scenari da considerare in base all'obiettivo dell'attività e al tipo di controllo selezionato:

   * **Le Esperienze casuali come vostro controllo e l'obiettivo dell'attività consistono nel testare l'efficacia dell'algoritmo di personalizzazione**: Se l'obiettivo è quello di valutare l'algoritmo di personalizzazione, potrete avere un'immagine più precisa dell'incremento. È inoltre utile confrontare il tasso di conversione per esperienze/offerte se si esegue semplicemente un test A/B (un controllo a caso). In tal caso, si consiglia di utilizzare una allocazione del 50% per un controllo sulle esperienze fornite in modo casuale.
   * **«Esperienze casuali» come vostro controllo e l'obiettivo dell'attività consiste nel massimizzare il traffico personalizzato**: Se siete a conoscenza dell'algoritmo e desiderate avere la quantità massima di traffico personalizzata, è consigliabile effettuare un'allocazione da 10% a 30%. Il compromesso è l'accuratezza che sarà possibile visualizzare nelle informazioni dell'incremento (in quanto gli intervalli di confidenza del traffico di controllo saranno più grandi, a causa del minor traffico verso i loro movimenti).
   * **Esperienza specifica con un tipo di obiettivo**: Se desiderate confrontare un'esperienza specifica con gli esperti di marketing verso i modelli di personalizzazione, è consigliabile effettuare un'allocazione da 10% a 30% per il controllo. Quando selezionate un'unica esperienza come controllo, il traffico non viene distribuito su ogni offerta/esperienza nell'attività.

* Le regole di targeting devono essere utilizzate con la massima parsimonia possibile perché possono interferire con la capacità di ottimizzazione del modello.
* I gruppi di reporting possono limitare il successo dell’attività di Personalizzazione automatizzata. Devono quindi essere utilizzati solo in condizioni specifiche.

   * Utilizza i gruppi di reporting solo se vengono soddisfatte le seguenti condizioni: (1) prevedi di sostituire o aggiungere nuove offerte mentre l’attività è in esecuzione, (2) le offerte nel gruppo di rapporti si rivolgono agli stessi visitatori e (3) le offerte in tale gruppo hanno circa lo stesso tasso di risposta complessivo.
   * Non esiste alcuna personalizzazione tra le offerte in un gruppo di rapporti: le offerte sono tutte considerate uguali dal modello di personalizzazione.
   * Non mettere mai tutte le offerte di un’attività in un singolo gruppo di rapporti. Questa decisione farà sì che tutte le offerte siano indirizzate in modo uniforme a tutti i visitatori che accedono all’attività.

## Quali sono alcuni dei limiti della Personalizzazione automatizzata? {#section_08BA09ED51B547299963C94FE6417CFA}

Target supporta fino a 30.000 esperienze, ma funziona al meglio quando sono create meno di 10.000 esperienze.

## Come viene implementato il targeting a livello di offerta? {#section_9D7A86EA93D74E9B8C81072A681263A4}

Quando arriva un visitatore, il set di possibili offerte che il visitatore può visualizzare è determinato dalle regole di targeting a livello di offerta. Quindi, l’algoritmo sceglie l’offerta che, secondo le previsioni del modello, che avrà il miglior ricavo atteso o possibilità di conversione tra quelle offerte. Il targeting dell’offerta ha un impatto sull’efficacia degli algoritmi di apprendimento automatico di Target e, di conseguenza, dovrebbe essere utilizzato con la massima parsimonia possibile.

## La mia attività non mostra alcun incremento. Cosa succede? {#section_BFA07C8C258F45318F73A461B8F32737}

Ci sono quattro fattori necessari affinché un’attività di Personalizzazione automatizzata generi incremento:

* Le offerte in ogni posizione devono essere abbastanza diverse per influenzare i visitatori.
* Le posizioni devono essere tali da poter influenzare l’obiettivo di ottimizzazione.
* L’attività deve avere traffico e potenza statistica tali da consentire il rilevamento di un incremento.
* L’algoritmo di personalizzazione deve funzionare bene.

La migliore linea di azione è di assicurarsi in primo luogo che i contenuti e le posizioni, che compongono le esperienze di attività, facciano davvero una differenza per i tassi di risposta generali tramite un semplice test A/B e non personalizzato. Calcola le dimensioni del campione in tempo per assicurarti che sia possibile visualizzare un incremento ragionevole ed esegui il test A/B per una durata fissa senza interruzioni né modifiche. Se i risultati di un test A/B mostrano un incremento statisticamente significativo su una o più esperienze, è probabile che un’attività personalizzata funzioni. Naturalmente, la personalizzazione può funzionare anche se non ci sono differenze nei tassi di risposta complessiva delle esperienze. Il problema, solitamente, deriva dalle offerte/posizioni che non hanno un impatto sull’obiettivo di ottimizzazione tale da poter essere rilevato con rilevanza statistica.

Per ulteriori informazioni, consulta [Risoluzione dei problemi relativi alla personalizzazione automatica](../../c-activities/t-automated-personalization/ap-trouble.md#reference_281954549C3E49E2B5498009BBDC62CA).

## In che modo la Personalizzazione automatizzata alloca il traffico della mia attività? {#section_4369364F77804E0D9B78BEE551DA5659}

La personalizzazione automatizzata indirizza i visitatori all’esperienza con la metrica di successo più elevata in base ai modelli di [Foresta casuale](../../c-activities/t-automated-personalization/algo-random-forest.md#concept_48F3CDAA16A848D2A84CDCD19DAAE3AA) più recenti costruiti per ciascun modello. Questa previsione si basa sulle informazioni specifiche del visitatore e sul contesto di visita.

Ad esempio, supponi che un’attività di Personalizzazione automatizzata abbia due posizioni con due offerte ciascuna. Nella prima posizione, l’offerta A ha un tasso di conversione previsto del 3% per un visitatore specifico e l’offerta B ha un tasso di conversione previsto dell’1%. Nella seconda posizione, l’offerta C ha un tasso di conversione previsto del 2% per lo stesso visitatore e l’offerta D ha un tasso di conversione previsto del 5%. La Personalizzazione automatizzata offrirebbe quindi a questo visitatore un’esperienza con le offerte A e D.

## Quando devo interrompere l’attività di Personalizzazione automatizzata? {#section_C51F3DAB8887463BB147373F6FE06B93}

La Personalizzazione automatizzata può essere utilizzata come personalizzazione “sempre attiva” che si ottimizza costantemente. Soprattutto per i contenuti fissi, non è necessario interrompere l’attività di Personalizzazione automatizzata. Se desideri apportare modifiche sostanziali ai contenuti che non sono simili alle offerte attualmente nell’attività di Personalizzazione automatizzata, si consiglia di avviare una nuova attività. In tal modo si evita il rischio che altri utenti che esaminano i rapporti possano confondersi o utilizzare risultati precedenti con contenuti diversi.

## Quanto tempo devo aspettare per la generazione dei modelli? {#section_6F6A5A9DB3564BE6B22FFEDFA5B29619}

Il periodo di tempo necessario alla generazione dei modelli nell’attività dipende in genere dal traffico nelle posizioni delle attività selezionate e dalla metrica di successo dell’attività. Utilizza il [Calcolatore del traffico](../../c-activities/t-automated-personalization/ap-traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) per determinare il periodo di tempo previsto per la generazione dei modelli nell’attività.

## L’attività contiene un modello generato. Le visite a quell’esperienza sono personalizzate? {#section_51EA953C6D1D4A3185FC9DD290D66621}

No, per iniziare la personalizzazione occorrono almeno due modelli generati nell’attività.

## Quando posso esaminare i risultati di un’attività di Personalizzazione automatizzata? {#section_05DB5ACAE6AD429C9510766A7268EE2C}

Puoi iniziare a esaminare i risultati dell’attività di Personalizzazione automatizzata quando disponi di almeno due esperienze con modelli generati (segno di spunta verde).

## Come posso ridurre la quantità di tempo necessario alla generazione dei modelli nell’attività? {#section_CCB8CEE98DAA40BA93AADCD596C48D82}

Esamina l’impostazione dell’attività e verifica se ci sono modifiche che intendi apportare per migliorare la velocità con cui i modelli vengono generati.

* La metrica del successo è molto in basso nel funnel di vendita dalle esperienze dell’attività? Con un tasso di conversione basso, la generazione dei modelli richiederà più traffico poiché è necessario un numero minimo di conversioni.
* Se la metrica di successo è impostata su RPV, puoi modificare la conversione? Le attività di conversione tendono a richiedere meno traffico per la generazione dei modelli.
* Puoi eliminare alcune esperienze dalla tua attività? Diminuendo il numero di esperienze, diminuirà anche il tempo necessario alla generazione dei modelli.
* Esiste una pagina con traffico più alto in cui questa attività avrebbe più successo? Maggiori sono il traffico e le conversioni nelle posizioni dell’attività, più rapidamente verranno generati i modelli.

## Perché i visitatori vedono esperienze per unʼattività di personalizzazione automatizzata che non dovrebbero vedere? {#section_41CECEAE0881446A8D9F3B016857914B}

Le attività di personalizzazione automatizzata vengono valutate una volta per sessione. Se c’erano delle sessioni attive idonee per una particolare esperienza e ora sono state aggiunte nuove offerte, gli utenti vedranno il nuovo contenuto insieme alle offerte precedentemente mostrate. Poiché in precedenza sono stati considerati idonei per quelle esperienze, continueranno a vederle per tutta la durata della sessione. Per eseguire la valutazione per ogni singola visita, usa il tipo di attività Targeting esperienza (XT).
