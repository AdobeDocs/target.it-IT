---
keywords: targeting automatico;targeting;allocazione del traffico;domande frequenti;faq;risoluzione dei problemi;risoluzione problemi;traffico
description: Esplora gli argomenti relativi alla risoluzione dei problemi e le domande frequenti sulle attività di Targeting automatico in Adobe Target.
title: Come posso risolvere i problemi relativi alle attività di Targeting automatico?
feature: Auto-Target
exl-id: 934f738e-560a-4847-9608-432ecfa2afe7
source-git-commit: d35ca5955b42772387c08a36e5b9e4ac207718a0
workflow-type: tm+mt
source-wordcount: '1921'
ht-degree: 58%

---

# ![PREMIUM](/help/main/assets/premium.png) Domande frequenti sul Targeting automatico e risoluzione dei problemi

Risoluzione dei problemi e domande frequenti su [!UICONTROL Targeting automatico] attività [!DNL Adobe Target].

## [!UICONTROL Domande frequenti sul Targeting automatico] {#section_5C120A2B11D14D9BAF767BBAB50FED23}

Consulta le seguenti domande frequenti e risposte mentre lavori con le attività di [!UICONTROL Targeting automatico]:

### Quali sono le procedure consigliate per impostare un’attività di [!UICONTROL Targeting automatico]?

+++Risposta
* Decidere se il valore aziendale di un [!UICONTROL Ricavo per visita] La metrica di successo (RPV) vale i requisiti di traffico aggiuntivi. RPV richiede in genere almeno 1.000 conversioni per esperienza perché un&#39;attività funzioni rispetto alla conversione.
* In base ai tuoi obiettivi, decidi la ripartizione tra il controllo e le esperienze personalizzate prima di iniziare l&#39;attività.
* Determina se disponi di traffico sufficiente per la pagina in cui l’attività di [!UICONTROL Targeting automatico] verrà eseguita affinché i modelli di personalizzazione compilino in un tempo ragionevole.
   * Se stai testando l’algoritmo di personalizzazione, non devi modificare le esperienze o aggiungere o rimuovere attributi di profilo mentre l’attività è in esecuzione.

* È consigliabile completare un’attività A/B tra le offerte e le posizioni che intendi utilizzare nel [!UICONTROL Targeting automatico] per garantire che le posizioni e le offerte abbiano un impatto sull’obiettivo di ottimizzazione. Se un’attività A/B non riesce a dimostrare una differenza significativa, il [!UICONTROL Targeting automatico] probabilmente non riuscirà a generare incrementi.

   * Se un test A/B non mostra differenze statisticamente significative tra le esperienze, probabilmente le offerte che stai prendendo in considerazione non sono sufficientemente diverse tra loro, le posizioni selezionate non incidono sulla metrica successo o l&#39;obiettivo di ottimizzazione è troppo lontano nell&#39;imbuto di conversione per essere influenzato dalle offerte scelte.

* Cerca di non apportare modifiche sostanziali alle esperienze durante il corso dell&#39;attività.

+++

### Adobe consigliato con [!UICONTROL Targeting automatico] con una divisione 90(Control)/10(Target) fino a quando i modelli non vengono generati?

+++Risposta La suddivisione ottimale dell’allocazione del traffico dipende da cosa si desidera eseguire.

Se l’obiettivo è quello di personalizzare il traffico il più possibile, puoi mantenere un’allocazione mirata del 90% e un controllo del 10% per la durata dell’attività. Se l’obiettivo è quello di eseguire un esperimento confrontando il livello di efficacia degli algoritmi personalizzati rispetto al controllo, allora una suddivisione 50/50 è la migliore per la durata dell&#39;attività.

Si consiglia di mantenere la suddivisione del traffico per la durata dell’attività in modo che i visitatori non passino da un’esperienza di targeting a una di controllo.

<!-- 
### Do the check marks indicating a model is built for that experience update if the report date range changes?

No, check marks for model generation show only the models built to date. There's no way to go back and see when a model was completed.
-->

+++

### Se un visitatore lo fa **not** vedi [!UICONTROL Targeting automatico] attività e conversioni, la conversione conta nella mia attività?

+++Risposta No, solo i visitatori che si qualificano e visualizzano il [!UICONTROL Targeting automatico] l’attività viene conteggiata nel reporting.

+++

### Perché il mio [!UICONTROL Targeting automatico] l’attività sembra generare un incremento.

+++Risposta Ci sono quattro fattori necessari per un [!UICONTROL Targeting automatico] attività per generare incremento:

* Le offerte devono essere abbastanza diverse per influenzare i visitatori.
* Le Offerte devono essere tali da poter influenzare l’obiettivo di ottimizzazione.
* Il test deve avere traffico e potenza statistica tali da consentire il rilevamento di un incremento.
* L’algoritmo di personalizzazione deve funzionare bene.

La migliore linea di azione è di assicurarsi in primo luogo che i contenuti e le posizioni, che compongono le esperienze di attività, facciano davvero una differenza per i tassi di risposta generali tramite un semplice test A/B e non personalizzato. Calcola le dimensioni del campione in tempo per assicurarti che sia possibile visualizzare un incremento ragionevole ed esegui il test A/B per una durata fissa senza interruzioni né modifiche.

Se i risultati di test A/B mostrano un incremento statisticamente significativo su una o più esperienze, può funzionare un&#39;attività personalizzata. Naturalmente, la personalizzazione può funzionare anche se non ci sono differenze nei tassi di risposta complessiva delle esperienze. Il problema, solitamente, deriva dalle offerte/posizioni che non hanno un impatto sull’obiettivo di ottimizzazione tale da poter essere rilevato con rilevanza statistica.

+++

### Quando devo interrompere l’attività di [!UICONTROL Targeting automatico]?

+++Risposta
[!UICONTROL Targeting automatico] può essere utilizzato come personalizzazione &quot;sempre attiva&quot; che si ottimizza costantemente. Soprattutto per i contenuti fissi, non è necessario arrestare l’attività di [!UICONTROL Targeting automatico].

Se desideri apportare modifiche sostanziali al contenuto nel tuo [!UICONTROL Targeting automatico] attività , la best practice consiste nell’avviare una nuova attività in modo che gli altri utenti che revisionano i rapporti non confondano o riferiscano i risultati passati con contenuti diversi.

+++

### Quanto tempo devo aspettare per la generazione dei modelli? {#how-long}

+++Risposta Il tempo necessario alla generazione dei modelli nel [!UICONTROL Targeting automatico] in genere l’attività dipende dal traffico delle posizioni dell’attività selezionate e dai tassi di conversione associati alla metrica di successo dell’attività.

[!UICONTROL Targeting automatico] non tenta di creare un modello personalizzato per una determinata esperienza fino a quando non vi sono almeno 50 conversioni per tale esperienza. Inoltre, se il modello costruito è di qualità insufficiente (come determinato dalla valutazione offline sui dati &quot;di prova&quot; di stallo, utilizzando [una metrica nota come AUC](https://it.wikipedia.org/wiki/Receiver_operating_characteristic#Area_under_the_curve)), il modello non viene utilizzato per distribuire il traffico in modo personalizzato.

Altri punti da tenere a mente sulla creazione di modelli di [!UICONTROL Targeting automatico]:

* Dopo che un’attività è attiva, [!UICONTROL Targeting automatico] considera fino agli ultimi 45 giorni di dati forniti in modo casuale durante la generazione di modelli (ad esempio, il traffico di controllo, più alcuni dati forniti in modo casuale dall’algoritmo).
* Quando [!UICONTROL Ricavo per visita] è la metrica di successo, in genere queste attività richiedono più dati per generare modelli a causa della varianza di dati più elevata che esiste in genere nei ricavi da visita rispetto al tasso di conversione.
* Poiché i modelli sono generati in base all’esperienza, sostituire un’esperienza con un’altra implica la necessità di raccogliere per la nuova esperienza un traffico sufficiente (almeno 50 conversioni) prima di poter ricostruire i modelli personalizzati.

+++

### L’attività contiene un modello generato. Le visite a quell’esperienza sono personalizzate?

+++Risposta No, per iniziare la personalizzazione devono essere presenti almeno due modelli generati all’interno dell’attività.

+++

### Quando posso iniziare a esaminare i risultati della mia [!UICONTROL Targeting automatico] attività?

+++Risposta Puoi iniziare a esaminare i risultati del tuo [!UICONTROL Targeting automatico] effettua il test dopo aver creato almeno due esperienze con modelli generati (segno di spunta verde) per l’esperienza che ha generato modelli.

+++

### Posso specificare un’esperienza particolare da usare come controllo?

+++Risposta Puoi selezionare un’esperienza da usare come controllo durante la creazione di un [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) o [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT).

Questa funzione ti consente di indirizzare l’intero traffico di controllo a una specifica esperienza, in base alla percentuale di allocazione del traffico configurata nell’attività. Puoi quindi valutare i rapporti sulle prestazioni del traffico personalizzato rispetto al traffico verso l’esperienza di controllo.

Per ulteriori informazioni, consulta [Utilizzare un’esperienza specifica come controllo](/help/main/c-activities/t-automated-personalization/experience-as-control.md).

+++

### Posso cambiare la metrica dell’obiettivo a metà strada attraverso un [!UICONTROL Targeting automatico] attività? {#change-metric}

L’Adobe +++Risposta non consiglia di modificare la metrica obiettivo a metà strada all’interno di un’attività. Anche se è possibile modificare la metrica dell’obiettivo durante un’attività utilizzando l’interfaccia utente [!DNL Target], è sempre necessario avviare una nuova attività. Non forniamo alcuna garanzia su ciò che accade se modifichi la metrica dell’obiettivo in un’attività dopo l’esecuzione.

Questo consiglio si applica alle attività [!UICONTROL Allocazione automatica], [!UICONTROL Targeting automatico] e [!UICONTROL Automated Personalization] che utilizzano [!DNL Target] o [!DNL Analytics] (A4T) come origine per la generazione di rapporti.

+++

### Posso utilizzare il [!UICONTROL Ripristina dati dei rapporti] durante l&#39;esecuzione di un [!UICONTROL Targeting automatico] attività?

+++Risposta utilizzando la [!UICONTROL Ripristina dati dei rapporti] opzione per [!UICONTROL Targeting automatico] le attività non sono suggerite. Anche se rimuove i dati di reporting visibili, questa opzione non rimuove tutti i record di formazione dal modello [!UICONTROL Targeting automatico]. Invece di utilizzare l’opzione [!UICONTROL Ripristina dati rapporto] per le attività di [!UICONTROL Targeting automatico], crea una nuova attività e disattiva l’attività originale.

La presente guida si applica anche [!UICONTROL Allocazione automatica] e [!UICONTROL Automated Personalization] attività.

+++

### Cosa succede se rimuovo una singola esperienza da una [!UICONTROL Targeting automatico] attività?

+++Risposta
[!DNL Target] crea un modello per esperienza, quindi rimuovere un’esperienza significa [!DNL Target] crea un modello in meno e non influisce sui modelli per le altre esperienze.

Ad esempio, supponi di avere un’attività [!UICONTROL Targeting automatico] con otto esperienze e di non apprezzare le prestazioni di un’esperienza. È possibile rimuovere tale esperienza e non influisce sui modelli per le sette esperienze rimanenti.

+++

## Risoluzione dei problemi di [!UICONTROL Targeting automatico] {#section_23995AB813F24525AF294D20A20875C8}

A volte le attività non vanno come previsto. Di seguito sono riportate alcune potenziali sfide che potresti affrontare durante l&#39;utilizzo di [!UICONTROL Targeting automatico] e alcune soluzioni suggerite.

### La mia attività di [!UICONTROL Targeting automatico] sta impiegando troppo tempo per generare i modelli.

+++Suggerimenti per la risoluzione dei problemi Ci sono diverse modifiche alla configurazione dell&#39;attività che possono ridurre il tempo previsto per la generazione dei modelli, incluso il numero di esperienze nel [!UICONTROL Targeting automatico] attività , il traffico verso il sito e la metrica di successo selezionata.

**Soluzione:** esamina l’impostazione dell’attività e verifica se ci sono modifiche che intendi apportare per migliorare la velocità con cui i modelli vengono generati.

* Se la metrica di successo è impostata su [!UICONTROL RPV], puoi passare alla conversione? Le attività di conversione tendono a richiedere meno traffico per la generazione dei modelli. Non perderai i dati di attività se modifichi la metrica di successo da RPV a conversione.
* La metrica del successo è molto in basso nel funnel di vendita dalle esperienze dell’attività? Un tasso di conversione di attività inferiore aumenta i requisiti di traffico necessari per la generazione dei modelli, perché è necessario un numero minimo di conversioni.
* È possibile eliminare alcune esperienze dall’attività? La riduzione del numero di esperienze in un’attività riduce il tempo necessario alla generazione dei modelli.
* Esiste una pagina con traffico più alto in cui questa attività avrebbe più successo? Maggiori sono il traffico e le conversioni nelle posizioni dell’attività, più rapidamente verranno generati i modelli.

+++

### La mia attività di [!UICONTROL Targeting automatico] non genera alcun incremento.

+++Suggerimenti per la risoluzione dei problemi Ci sono quattro fattori necessari affinché un&#39;attività AT generi incremento:

* Le offerte devono essere abbastanza diverse per influenzare i visitatori.
* Le offerte devono essere posizionate in un punto che faccia la differenza con l’obiettivo di ottimizzazione.
* Il test deve avere traffico e potenza statistica tali da consentire il rilevamento di un incremento.
* L’algoritmo di personalizzazione deve funzionare bene.

**Soluzione:** in primo luogo, assicurati che l&#39;attività personalizzi il traffico. Se i modelli non sono generati per tutte le esperienze, l’attività di [!UICONTROL Targeting automatico] fornisce ancora in modo casuale una parte significativa di visite per tentare di generare tutti i modelli il più rapidamente possibile. Se i modelli non sono generati, il [!UICONTROL Targeting automatico] non personalizza il traffico.

Quindi, assicurati che le offerte e le posizioni di attività facciano realmente la differenza nei tassi di risposta complessiva tramite un semplice test A/B non personalizzato. Calcola le dimensioni del campione in tempo per assicurarti che sia possibile visualizzare un incremento ragionevole ed esegui il test A/B per una durata fissa senza interruzioni né modifiche. Se i risultati di un test A/B mostrano un incremento statisticamente significativo su una o più esperienze, è probabile che un’attività personalizzata funzioni. Naturalmente, la personalizzazione può funzionare anche se non ci sono differenze nei tassi di risposta complessiva delle esperienze. In genere, il problema deriva dalle offerte e posizioni che non hanno un impatto sufficiente sull’obiettivo di ottimizzazione da rilevare con rilevanza statistica.

+++

### Qualsiasi metrica dipendente da una metrica di conversione non consegue mai la conversione.

+++Suggerimenti per la risoluzione dei problemi Questo è previsto.

In un’attività di [!UICONTROL Targeting automatico], una volta conseguita la conversione per una metrica di conversione (che si tratti di obiettivo di ottimizzazione o di corrispondenza), l’utente viene rilasciato dall’esperienza e l’attività viene riavviata.

Prendiamo ad esempio un’attività con una metrica di conversione (C1) e una metrica aggiuntiva (A1). A1 dipende da C1. Quando un visitatore accede all’attività per la prima volta e i criteri di conversione per A1 e C1 non vengono soddisfatti, la metrica A1 non consegue la conversione a causa della dipendenza dalla metrica di successo. Se il visitatore consegue la conversione per C1 e poi per A1, la conversione A1 non risulta perché, non appena ottenuta la conversione per C1, il visitatore viene rilasciato.

+++
