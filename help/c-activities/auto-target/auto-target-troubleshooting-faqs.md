---
keywords: auto-target;targeting;traffic allocation;frequently asked questions;faq;troubleshooting;trouble shooting;traffic
description: Risoluzione dei problemi e domande frequenti su Auto-Target in  Adobe Target.
title: Risoluzione dei problemi e domande frequenti su Target automatico
feature: auto-target
translation-type: tm+mt
source-git-commit: 18dbc90f52c9a23713577c4cda4ac87a5b69edd2
workflow-type: tm+mt
source-wordcount: '1830'
ht-degree: 71%

---


# ![Risoluzione dei problemi e domande frequenti su ](/help/assets/premium.png) PREMIUMAuto-Target

Risoluzione dei problemi e domande frequenti su [!UICONTROL Auto-Target] in [!DNL Adobe Target].

## Domande frequenti sul Targeting automatico {#section_5C120A2B11D14D9BAF767BBAB50FED23}

Consultate le seguenti domande frequenti e risposte durante l&#39;utilizzo delle attività di [!UICONTROL Auto-Target]:

### Quali sono le procedure consigliate per impostare un’attività di [!UICONTROL Targeting automatico]?

* Decidi se il valore aziendale di una metrica di uccesso di un Ricavo per visita (RPV) vale i requisiti di traffico aggiuntivi. RPV richiede in genere almeno 1.000 conversioni per esperienza perché un&#39;attività funzioni rispetto alla conversione.
* In base ai tuoi obiettivi, decidi la ripartizione tra il controllo e le esperienze personalizzate prima di iniziare l&#39;attività.
* Determina se disponi di traffico sufficiente per la pagina in cui l’attività di [!UICONTROL Targeting automatico] verrà eseguita affinché i modelli di personalizzazione compilino in un tempo ragionevole.
   * Se stai sopttoponendo a test l&#39;algoritmo di personalizzazione, non è consigliabile modificare le esperienze o aggiungere/rimuovere attributi di profilo mentre l&#39;attività è in esecuzione.

* È consigliabile completare un’attività A/B tra le offerte e le posizioni che prevedi di utilizzare nell’attività di [!UICONTROL Targeting automatico] per garantire che le posizioni e le offerte abbiano un impatto sull’obiettivo di ottimizzazione. Se un’attività A/B non riesce a dimostrare una differenza significativa, il [!UICONTROL Targeting automatico] probabilmente non riuscirà a generare incrementi.

   * Se un test A/B non mostra differenze statisticamente significative tra le esperienze, probabilmente le offerte che stai prendendo in considerazione non sono sufficientemente diverse tra loro, le posizioni selezionate non incidono sulla metrica successo o l&#39;obiettivo di ottimizzazione è troppo lontano nell&#39;imbuto di conversione per essere influenzato dalle offerte scelte.

* Cerca di non apportare modifiche sostanziali alle esperienze durante il corso dell&#39;attività.

### È consigliabile utilizzare Auto Target con una suddivisione 90(Control)/10(Targeting) fino alla creazione dei modelli?

La suddivisione ottimale dell&#39;allocazione del traffico dipende da cosa si desidera ottenere.

Se l&#39;obiettivo è quello di personalizzare il traffico il più possibile, potete mantenere il controllo del 90% con targeting e del 10% per la durata dell&#39;attività. Se l&#39;obiettivo è quello di eseguire un esperimento confrontando il livello di esperienza degli algoritmi personalizzati rispetto al controllo, allora una divisione 50/50 è la migliore per il ciclo di vita dell&#39;attività.

La best practice consiste nel mantenere la suddivisione dell&#39;allocazione del traffico per il ciclo di vita dell&#39;attività in modo che i visitatori non passino da un&#39;esperienza con targeting a un&#39;altra.

<!-- 
### Do the check marks indicating a model is built for that experience update if the report date range changes?

No, check marks for model generation show only the models built to date. There's no way to go back and see when a model was completed.
-->

### Se un visitatore non vede l’attività di [!UICONTROL Targeting automatico] e converte, la conversione conta nella mia attività?

No, solo i visitatori che si qualificano e visualizzano l’attività di [!UICONTROL Targeting automatico] sono conteggiati nella creazione dei rapporti.

### La mia attività di [!UICONTROL Targeting automatico] non sembra generare alcun incremento. Cosa succede? 

Ci sono quattro fattori necessari affinché un’attività di [!UICONTROL Targeting automatico] generi incremento:

* Le offerte devono essere abbastanza diverse per influenzare i visitatori.
* Le Offerte devono essere tali da poter influenzare l’obiettivo di ottimizzazione.
* Il test deve avere traffico e potenza statistica tali da consentire il rilevamento di un incremento.
* L’algoritmo di personalizzazione deve funzionare bene.

La migliore linea di azione è di assicurarsi in primo luogo che i contenuti e le posizioni, che compongono le esperienze di attività, facciano davvero una differenza per i tassi di risposta generali tramite un semplice test A/B e non personalizzato. Calcola le dimensioni del campione in tempo per assicurarti che sia possibile visualizzare un incremento ragionevole ed esegui il test A/B per una durata fissa senza interruzioni né modifiche.

Se i risultati di test A/B mostrano un incremento statisticamente significativo su una o più esperienze, può funzionare un&#39;attività personalizzata. Naturalmente, la personalizzazione può funzionare anche se non ci sono differenze nei tassi di risposta complessiva delle esperienze. Il problema, solitamente, deriva dalle offerte/posizioni che non hanno un impatto sull’obiettivo di ottimizzazione tale da poter essere rilevato con rilevanza statistica.

### Quando devo interrompere l’attività di [!UICONTROL Targeting automatico]?

Il [!UICONTROL Targeting automatico] può essere utilizzato come personalizzazione “sempre attiva” che si ottimizza costantemente. Soprattutto per i contenuti fissi, non è necessario arrestare l’attività di [!UICONTROL Targeting automatico].

Se desideri apportare modifiche sostanziali al contenuto nell’attività di [!UICONTROL Targeting automatico], la procedura consigliata consiste nell’avviare una nuova attività in modo che gli altri utenti che revisionano i rapporti non confondano o riferiscano i risultati passati con contenuti diversi.

### Quanto tempo devo aspettare per la generazione dei modelli? {#how-long}

Il tempo necessario per la creazione dei modelli nell&#39;attività [!UICONTROL Auto-Target] dipende in genere dal traffico nelle posizioni dell&#39;attività selezionate e dai tassi di conversione associati alla metrica di successo dell&#39;attività.

[!UICONTROL Il ] targeting automatico non tenterà di creare un modello personalizzato per una determinata esperienza fino a quando non ci saranno almeno 50 conversioni per tale esperienza. Inoltre, se il modello costruito è di qualità insufficiente (come determinato dalla valutazione offline sui dati &quot;test&quot; del blocco, utilizzando [una metrica nota come AUC](https://en.wikipedia.org/wiki/Receiver_operating_characteristic#Area_under_the_curve)), il modello non sarà utilizzato per servire il traffico in modo personalizzato.

Altri punti da tenere a mente sulla creazione di modelli di [!UICONTROL Auto-Target]:

* Una volta che un&#39;attività è live, [!UICONTROL Auto-Target] considera fino agli ultimi 45 giorni di dati serviti in modo casuale quando si tenta di creare modelli (ad esempio, controllare il traffico, più alcuni dati serviti in modo casuale aggiuntivi conservati dal nostro algoritmo).
* Quando [!UICONTROL Revenue per Visit] è la metrica di successo, queste attività in genere richiedono più dati per creare modelli a causa della maggiore varianza di dati che generalmente esiste nelle entrate da visita rispetto al tasso di conversione.
* Poiché i modelli sono basati su un&#39;esperienza specifica, sostituire un&#39;esperienza con un&#39;altra significa che è necessario raccogliere il traffico sufficiente (ovvero almeno 50 conversioni) per la nuova esperienza prima di poter ricostruire i modelli personalizzati.

### L’attività contiene un modello generato. Le visite a quell’esperienza sono personalizzate? 

No, per iniziare la personalizzazione occorrono almeno due modelli generati nell’attività.

### Quando posso iniziare a esaminare i risultati della mia attività di [!UICONTROL Targeting automatico]?

Puoi iniziare a esaminare i risultati dei test di [!UICONTROL Targeting automatico] quando disponi di almeno due esperienze con modelli generati (segno di spunta verde) nell’attività che presenta modelli generati.

### Posso specificare un’esperienza particolare da usare come controllo?

Puoi selezionare un’esperienza da usare come controllo durante la creazione di un’attività [Personalizzazione automatizzata](/help/c-activities/t-automated-personalization/automated-personalization.md) oppure [Targeting automatico](/help/c-activities/auto-target/auto-target-to-optimize.md).

Questa funzione ti permette di indirizzare tutto il traffico di controllo a una specifica esperienza, in base alla percentuale di allocazione del traffico configurata nell’attività. Puoi quindi valutare i rapporti sulle prestazioni del traffico personalizzato rispetto al traffico verso l’esperienza di controllo.

Per ulteriori informazioni, consulta [Utilizzare un’esperienza specifica come controllo](/help/c-activities/t-automated-personalization/experience-as-control.md).

### Posso cambiare la metrica obiettivo a metà strada attraverso un&#39;attività di targeting automatico? {#change-metric}

Non è consigliabile modificare la metrica obiettivo a metà di un&#39;attività. Sebbene sia possibile modificare la metrica di obiettivo durante un&#39;attività utilizzando l&#39;interfaccia utente [!DNL Target], è comunque necessario avviare sempre una nuova attività. Non garantiamo cosa accade se si modifica la metrica di obiettivo in un&#39;attività dopo che è in esecuzione.

Questa raccomandazione si applica alle attività [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target] e [!UICONTROL  Automated Personalization] che utilizzano [!DNL Target] o [!DNL Analytics] (A4T) come origine di reporting.

### Posso utilizzare l&#39;opzione Reimposta dati rapporto durante l&#39;esecuzione di un&#39;attività di targeting automatico?

Non è consigliabile utilizzare l&#39;opzione [!UICONTROL Reimposta dati rapporto] per le attività [!UICONTROL Auto-Target]. Anche se rimuove i dati di reporting visibili, questa opzione non rimuove tutti i record di formazione dal modello [!UICONTROL Auto-Target]. Invece di utilizzare l&#39;opzione [!UICONTROL Reimposta dati rapporto] per le attività [!UICONTROL Auto-Target], create una nuova attività e disattivate l&#39;attività originale. (Nota: Questa guida si applica anche alle attività [!UICONTROL Auto-Allocate] e [!UICONTROL  Automated Personalization].

## Risoluzione dei problemi di [!UICONTROL Targeting automatico] {#section_23995AB813F24525AF294D20A20875C8}

A volte le attività non vanno come previsto. Di seguito sono elencate alcune potenziali sfide che potresti affrontare durante l’utilizzo del [!UICONTROL Targeting automatico] e alcune soluzioni suggerite.

### La mia attività di [!UICONTROL Targeting automatico] sta impiegando troppo tempo per generare i modelli.

Sono disponibili diverse modifiche dell’impostazione dell’attività che possono ridurre il tempo previsto per la generazione di modelli, tra cui il numero di esperienze nell’attività di [!UICONTROL Targeting automatico], il traffico verso il sito e la metrica di successo selezionata.

**Soluzione:** esamina l’impostazione dell’attività e verifica se ci sono modifiche che intendi apportare per migliorare la velocità con cui i modelli vengono generati.

* Se la metrica di successo è impostata su RPV, è possibile modificare la conversione? Le attività di conversione tendono a richiedere meno traffico per la generazione dei modelli. Non perderai i dati di attività se modifichi la metrica di successo da RPV a conversione.
* La metrica del successo è molto in basso nel funnel di vendita dalle esperienze dell’attività? Con un tasso di conversione basso, la generazione dei modelli richiederà più traffico poiché è necessario un numero minimo di conversioni.
* È possibile eliminare alcune esperienze dall’attività? Diminuendo il numero di esperienze, diminuirà anche il tempo necessario alla generazione dei modelli.
* Esiste una pagina con traffico più alto in cui questa attività avrebbe più successo? Maggiori sono il traffico e le conversioni nelle posizioni dell’attività, più rapidamente verranno generati i modelli.

### La mia attività di [!UICONTROL Targeting automatico] non genera alcun incremento.

Ci sono quattro fattori necessari affinché un’attività di Personalizzazione automatizzata generi incremento:

* Le offerte devono essere abbastanza diverse per influenzare i visitatori.
* Le Offerte devono essere tali da poter influenzare l’obiettivo di ottimizzazione.
* Il test deve avere traffico e potenza statistica tali da consentire il rilevamento di un incremento.
* L’algoritmo di personalizzazione deve funzionare bene.

**Soluzione:** in primo luogo, assicurati che l&#39;attività personalizzi il traffico. Se i modelli non sono generati per tutte le esperienze, l’attività di [!UICONTROL Targeting automatico] fornisce ancora in modo casuale una parte significativa di visite per tentare di generare tutti i modelli il più rapidamente possibile. Se i modelli non sono generati, il [!UICONTROL Targeting automatico] non personalizza il traffico.

Quindi, assicurati che le offerte e le posizioni di attività facciano realmente la differenza nei tassi di risposta complessiva tramite un semplice test A/B non personalizzato. Calcola le dimensioni del campione in tempo per assicurarti che sia possibile visualizzare un incremento ragionevole ed esegui il test A/B per una durata fissa senza interruzioni né modifiche. Se i risultati di un test A/B mostrano un incremento statisticamente significativo su una o più esperienze, è probabile che un’attività personalizzata funzioni. Naturalmente, la personalizzazione può funzionare anche se non ci sono differenze nei tassi di risposta complessiva delle esperienze. Il problema, solitamente, deriva dalle offerte/posizioni che non hanno un impatto sull’obiettivo di ottimizzazione tale da poter essere rilevato con rilevanza statistica.

### Le metriche dipendenti dalla metrica di conversione non conseguono mai la conversione.

Si tratta di un comportamento previsto.

In un’attività di [!UICONTROL Targeting automatico], una volta conseguita la conversione per una metrica di conversione (che si tratti di obiettivo di ottimizzazione o di corrispondenza), l’utente viene rilasciato dall’esperienza e l’attività viene riavviata.

Prendiamo ad esempio un’attività con una metrica di conversione (C1) e una metrica aggiuntiva (A1). A1 dipende da C1. Quando un visitatore accede all’attività per la prima volta e i criteri di conversione per A1 e C1 non vengono soddisfatti, la metrica A1 non consegue la conversione a causa della dipendenza dalla metrica di successo. Se il visitatore consegue la conversione per C1 e poi per A1, la conversione A1 non risulta perché, non appena ottenuta la conversione per C1, il visitatore viene rilasciato.
