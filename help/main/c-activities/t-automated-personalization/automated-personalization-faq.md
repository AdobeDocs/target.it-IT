---
keywords: risoluzione dei problemi;domande frequenti;FAQ;FAQ;personalizzazione automatizzata;controllo;esperienza predefinita;best practice
description: Esplora un elenco delle domande frequenti e delle risposte sulle attività di Automated Personalization (AP) in Adobe Target.
title: Come posso trovare le domande frequenti sulle attività di Automated Personalization?
feature: Automated Personalization
exl-id: 2bf62cc1-1781-4021-a400-2884e0bae893
source-git-commit: 6857ba1a6410d3140a83a052efc50e9dd1776fd9
workflow-type: tm+mt
source-wordcount: '2004'
ht-degree: 76%

---

# ![PREMIUM](/help/main/assets/premium.png) Domande frequenti su Automated Personalization

Elenco delle domande frequenti sulla Personalizzazione automatizzata.

## Posso specificare un’esperienza particolare da usare come controllo?

Puoi selezionare un’esperienza da usare come controllo durante la creazione di un’attività [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) oppure [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md).

Questa funzione ti permette di indirizzare tutto il traffico di controllo a una specifica esperienza, in base alla percentuale di allocazione del traffico configurata nell’attività. Puoi quindi valutare i rapporti sulle prestazioni del traffico personalizzato rispetto al traffico verso l’esperienza di controllo.

Per ulteriori informazioni, consulta [Utilizzare un’esperienza specifica come controllo](/help/main/c-activities/t-automated-personalization/experience-as-control.md).

## Come posso confrontare la Personalizzazione automatizzata con un’esperienza predefinita? {#section_46C1A620A2384C2C8392D6716DD18495}

Non esiste un’opzione diretta per confrontare la Personalizzazione automatizzata con un’esperienza predefinita. Tuttavia, come soluzione alternativa, se un’offerta o un’esperienza predefinita esiste come parte dell’attività complessiva, per comprenderne le prestazioni di base puoi fare clic sul segmento &quot;Controllo&quot; nei rapporti e individuare tale offerta particolare nel rapporto risultante a livello di offerta. Il tasso di conversione registrato per questa offerta può essere utilizzato per confrontare con il tasso di conversazione dell’intero segmento &quot;Foresta casuale&quot;. Questo permette di confrontare le prestazioni della macchina rispetto all’offerta predefinita.

## Quali sono le best practice per impostare un’attività di Personalizzazione automatizzata? {#section_E155B26282BE49B58EA2683413D11DE6}

* Se vuoi personalizzare una pagina con traffico più basso o apportare modifiche strutturali all’esperienza che stai personalizzando, considera l’utilizzo della funzione Targeting automatico invece di Personalizzazione automatizzata. Consulta [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md).
* È consigliabile completare un’attività A/B tra le offerte e le posizioni che prevedi di utilizzare nell’attività di Personalizzazione automatizzata per garantire che le posizioni e le offerte abbiano un impatto sull’obiettivo di ottimizzazione. Se per un’attività A/B non è possibile dimostrare una differenza significativa, è probabile che nemmeno la Personalizzazione automatizzata riesca a generare incrementi.

   * Se un test A/B...N non mostra differenze statisticamente significative tra le esperienze, probabilmente le offerte che stai prendendo in considerazione non sono sufficientemente diverse tra loro, le posizioni selezionate non incidono sulla metrica di successo oppure l’obiettivo di ottimizzazione è troppo lontano nel funnel di conversione per essere influenzato dalle offerte scelte.

* Assicurati di utilizzare il [Calcolatore del traffico](/help/main/c-activities/t-automated-personalization/ap-traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) per farti un’idea di quanto tempo ci vorrà per la generazione dei modelli di personalizzazione nell’attività di Personalizzazione automatizzata.
* In base ai tuoi obiettivi, decidi la ripartizione tra controllo e destinazione prima di iniziare l’attività.

   Esistono tre scenari da considerare in base all’obiettivo dell’attività e al tipo di controllo selezionato:

   * **Controllo: esperienze casuali; obiettivo dell’attività: testare l’efficacia dell’algoritmo di personalizzazione**: Se l’obiettivo è quello di valutare l’algoritmo di personalizzazione, allora avrai bisogno di avere un’immagine più precisa dell’incremento. Inoltre, vorrai probabilmente un confronto con il tasso di conversione per esperienze/offerte rispetto a un semplice test A/B (controllo casuale). In tal caso, si consiglia di utilizzare un’allocazione del 50% a un controllo composto da esperienze distribuite in modo casuale.
   * **Controllo: esperienze casuali e obiettivo dell’attività: massimizzare il traffico personalizzato**: Se l’algoritmo è a tuo agio e desideri che la quantità massima di traffico sia personalizzata, si consiglia di allocare al controllo dal 10% al 30% del traffico. Il compromesso è la precisione che sarà possibile vedere nelle informazioni sull’incremento (in quanto gli intervalli di affidabilità del traffico di controllo saranno più ampi perché vi è meno traffico verso di loro).
   * **Controllo: esperienza specifica; entrambi i tipi di obiettivo**: se desideri confrontare con i modelli di personalizzazione un’esperienza specifica definita dagli esperti di marketing, si consiglia di allocare al controllo dal 10% al 30% del traffico. Quando selezioni una sola esperienza come controllo, tale traffico non viene distribuito su ogni offerta/esperienza nell’attività.

* Le regole di targeting devono essere utilizzate con la massima parsimonia possibile perché possono interferire con la capacità di ottimizzazione del modello.
* I gruppi di reporting possono limitare il successo dell’attività di Personalizzazione automatizzata. Devono quindi essere utilizzati solo in condizioni specifiche.

   * Utilizza i gruppi di reporting solo se vengono soddisfatte le seguenti condizioni: (1) prevedi di sostituire o aggiungere nuove offerte mentre l’attività è in esecuzione, (2) le offerte nel gruppo di rapporti si rivolgono agli stessi visitatori e (3) le offerte in tale gruppo hanno circa lo stesso tasso di risposta complessivo.
   * Non esiste alcuna personalizzazione tra le offerte in un gruppo di rapporti: le offerte sono tutte considerate uguali dal modello di personalizzazione.
   * Non mettere mai tutte le offerte di un’attività in un singolo gruppo di rapporti. Questa decisione farà sì che tutte le offerte siano indirizzate in modo uniforme a tutti i visitatori che accedono all’attività.

## Domande frequenti 

Consulta le seguenti domande frequenti e risposte mentre lavori con [!UICONTROL Automated Personalization] attività:

### Quali sono alcuni dei limiti della Personalizzazione automatizzata? {#section_08BA09ED51B547299963C94FE6417CFA}

[!DNL Target] supporta fino a 30.000 esperienze, ma funziona al meglio quando sono create meno di 10.000 esperienze.

Lo stesso limite viene applicato anche quando l’attività ha abilitato il [!UICONTROL Duplicati di visualizzazione] opzione .

### Come viene implementato il targeting a livello di offerta? {#section_9D7A86EA93D74E9B8C81072A681263A4}

Quando arriva un visitatore, il set di possibili offerte che il visitatore può visualizzare è determinato dalle regole di targeting a livello di offerta. Quindi, l’algoritmo sceglie l’offerta che, secondo le previsioni del modello, che avrà il miglior ricavo atteso o possibilità di conversione tra quelle offerte. Il targeting dell’offerta ha un impatto sull’efficacia degli algoritmi di apprendimento automatico di Target e, di conseguenza, dovrebbe essere utilizzato con la massima parsimonia possibile.

### La mia attività non mostra alcun incremento. Cosa succede?  {#section_BFA07C8C258F45318F73A461B8F32737}

Ci sono quattro fattori necessari affinché un’attività di Personalizzazione automatizzata generi incremento:

* Le offerte in ogni posizione devono essere abbastanza diverse per influenzare i visitatori.
* Le posizioni devono essere tali da poter influenzare l’obiettivo di ottimizzazione.
* L’attività deve avere traffico e potenza statistica tali da consentire il rilevamento di un incremento.
* L’algoritmo di personalizzazione deve funzionare bene.

La migliore linea di azione è di assicurarsi in primo luogo che i contenuti e le posizioni, che compongono le esperienze di attività, facciano davvero una differenza per i tassi di risposta generali tramite un semplice test A/B e non personalizzato. Calcola le dimensioni del campione in tempo per assicurarti che sia possibile visualizzare un incremento ragionevole ed esegui il test A/B per una durata fissa senza interruzioni né modifiche. Se i risultati di un test A/B mostrano un incremento statisticamente significativo su una o più esperienze, è probabile che un’attività personalizzata funzioni. Naturalmente, la personalizzazione può funzionare anche se non ci sono differenze nei tassi di risposta complessiva delle esperienze. Il problema, solitamente, deriva dalle offerte/posizioni che non hanno un impatto sull’obiettivo di ottimizzazione tale da poter essere rilevato con rilevanza statistica.

Per ulteriori informazioni, consulta [Risoluzione dei problemi relativi alla personalizzazione automatica](/help/main/c-activities/t-automated-personalization/ap-trouble.md#reference_281954549C3E49E2B5498009BBDC62CA).

### In che modo la Personalizzazione automatizzata alloca il traffico della mia attività? {#section_4369364F77804E0D9B78BEE551DA5659}

La personalizzazione automatizzata indirizza i visitatori all’esperienza con la metrica di successo più elevata in base ai modelli di [Foresta casuale](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) più recenti costruiti per ciascun modello. Questa previsione si basa sulle informazioni specifiche del visitatore e sul contesto di visita.

Ad esempio, supponi che un’attività di Personalizzazione automatizzata abbia due posizioni con due offerte ciascuna. Nella prima posizione, l’offerta A ha un tasso di conversione previsto del 3% per un visitatore specifico e l’offerta B ha un tasso di conversione previsto dell’1%. Nella seconda posizione, l’offerta C ha un tasso di conversione previsto del 2% per lo stesso visitatore e l’offerta D ha un tasso di conversione previsto del 5%. La Personalizzazione automatizzata offrirebbe quindi a questo visitatore un’esperienza con le offerte A e D.

### Quando devo interrompere l’attività di Personalizzazione automatizzata? {#section_C51F3DAB8887463BB147373F6FE06B93}

La Personalizzazione automatizzata può essere utilizzata come personalizzazione “sempre attiva” che si ottimizza costantemente. Soprattutto per i contenuti fissi, non è necessario interrompere l’attività di Personalizzazione automatizzata. Se desideri apportare modifiche sostanziali ai contenuti che non sono simili alle offerte attualmente nell’attività di Personalizzazione automatizzata, si consiglia di avviare una nuova attività. In tal modo si evita il rischio che altri utenti che esaminano i rapporti possano confondersi o utilizzare risultati precedenti con contenuti diversi.

### Quanto tempo devo aspettare per la generazione dei modelli? {#section_6F6A5A9DB3564BE6B22FFEDFA5B29619}

Il periodo di tempo necessario alla generazione dei modelli nell’attività dipende in genere dal traffico nelle posizioni delle attività selezionate e dalla metrica di successo dell’attività. Utilizza il [Calcolatore del traffico](/help/main/c-activities/t-automated-personalization/ap-traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) per determinare il periodo di tempo previsto per la generazione dei modelli nell’attività.

### L’attività contiene un modello generato. Le visite a quell’esperienza sono personalizzate? {#section_51EA953C6D1D4A3185FC9DD290D66621}

No, per iniziare la personalizzazione occorrono almeno due modelli generati nell’attività.

### Quando posso esaminare i risultati di un’attività di Personalizzazione automatizzata? {#section_05DB5ACAE6AD429C9510766A7268EE2C}

Puoi iniziare a esaminare i risultati dell’attività di Personalizzazione automatizzata quando disponi di almeno due esperienze con modelli generati (segno di spunta verde).

### Come posso ridurre la quantità di tempo necessario alla generazione dei modelli nell’attività? {#section_CCB8CEE98DAA40BA93AADCD596C48D82}

Esamina l’impostazione dell’attività e verifica se ci sono modifiche che intendi apportare per migliorare la velocità con cui i modelli vengono generati.

* La metrica del successo è molto in basso nel funnel di vendita dalle esperienze dell’attività? Con un tasso di conversione basso, la generazione dei modelli richiederà più traffico poiché è necessario un numero minimo di conversioni.
* Se la metrica di successo è impostata su RPV, è possibile modificare la conversione? Le attività di conversione tendono a richiedere meno traffico per la generazione dei modelli.
* È possibile eliminare alcune esperienze dall’attività? Diminuendo il numero di esperienze, diminuirà anche il tempo necessario alla generazione dei modelli.
* Esiste una pagina con traffico più alto in cui questa attività avrebbe più successo? Maggiori sono il traffico e le conversioni nelle posizioni dell’attività, più rapidamente verranno generati i modelli.

### Perché i visitatori vedono esperienze per unʼattività di personalizzazione automatizzata che non dovrebbero vedere? {#section_41CECEAE0881446A8D9F3B016857914B}

Le attività di personalizzazione automatizzata vengono valutate una volta per sessione. Se c’erano delle sessioni attive idonee per una particolare esperienza e ora sono state aggiunte nuove offerte, gli utenti vedranno il nuovo contenuto insieme alle offerte precedentemente mostrate. Poiché in precedenza sono stati considerati idonei per quelle esperienze, continueranno a vederle per tutta la durata della sessione. Per eseguire la valutazione per ogni singola visita, usa il tipo di attività Targeting esperienza (XT).

### Posso cambiare la metrica dell’obiettivo a metà strada attraverso un’attività Automated Personalization? {#change-metric}

Non è consigliabile modificare la metrica obiettivo a metà strada all’interno di un’attività. Anche se è possibile modificare la metrica dell’obiettivo durante un’attività utilizzando l’interfaccia utente [!DNL Target], è sempre necessario avviare una nuova attività. Non forniamo alcuna garanzia su ciò che accade se modifichi la metrica dell’obiettivo in un’attività dopo l’esecuzione.

Questo consiglio si applica alle attività [!UICONTROL Allocazione automatica], [!UICONTROL Targeting automatico] e [!UICONTROL Automated Personalization] che utilizzano [!DNL Target] o [!DNL Analytics] (A4T) come origine per la generazione di rapporti.

### Posso utilizzare l’opzione Reimposta dati dei rapporti durante l’esecuzione di un’attività Automated Personalization?

Utilizzo della [!UICONTROL Ripristina dati dei rapporti] opzione per [!UICONTROL Automated Personalization] le attività non sono suggerite. Anche se rimuove i dati di reporting visibili, questa opzione non rimuove tutti i record di formazione dal [!UICONTROL Automated Personalization] modello. Invece di utilizzare il [!UICONTROL Ripristina dati dei rapporti] opzione per [!UICONTROL Automated Personalization] , crea una nuova attività e disattiva l’attività originale. (Nota: La presente guida si applica anche [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico] attività).

### In che modo Automated Personalization genera i modelli rispetto agli ambienti?

Un modello è costruito per identificare le prestazioni della strategia personalizzata rispetto al traffico distribuito in modo casuale rispetto all’invio di tutto il traffico all’esperienza vincente complessiva. Questo modello considera gli hit e le conversioni solo nell’ambiente predefinito.

Il traffico proveniente da un secondo set di modelli viene generato per ciascun gruppo di modeling (AP) o per esperienza (AT). Per ciascuno di questi modelli, vengono considerati hit e conversioni in tutti gli ambienti.

Le richieste verranno quindi servite con lo stesso modello, indipendentemente dall’ambiente, ma la pluralità di traffico dovrebbe provenire dall’ambiente predefinito per garantire che l’esperienza vincente complessiva identificata sia coerente con il comportamento del mondo reale.
