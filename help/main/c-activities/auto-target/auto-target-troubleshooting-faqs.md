---
keywords: targeting automatico;targeting;allocazione del traffico;domande frequenti;faq;risoluzione dei problemi;risoluzione problemi;traffico
description: Esplora gli argomenti relativi alla risoluzione dei problemi e le domande frequenti sulle attività [!UICONTROL Auto-Target].
title: Come posso risolvere i problemi relativi a [!UICONTROL Auto-Target] attività?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."
feature: Auto-Target
exl-id: 934f738e-560a-4847-9608-432ecfa2afe7
source-git-commit: 3e8c2d77f300bf0e2ca83a53d30e7b9eee48894e
workflow-type: tm+mt
source-wordcount: '1850'
ht-degree: 29%

---

# Domande frequenti e risoluzione dei problemi di [!UICONTROL Auto-Target]

Risoluzione dei problemi e domande frequenti sulle attività [!UICONTROL Auto-Target] in [!DNL Adobe Target].

## [!UICONTROL Auto-Target] domande frequenti {#section_5C120A2B11D14D9BAF767BBAB50FED23}

Consulta le seguenti domande frequenti e risposte mentre lavori con [!UICONTROL Auto-Target] attività:

### Quali sono le procedure consigliate per impostare un&#39;attività [!UICONTROL Auto-Target]?

+++Risposta
* Decidere se il valore aziendale di una metrica di successo di [!UICONTROL Revenue per Visit] (RPV) vale i requisiti di traffico aggiuntivi. RPV richiede in genere almeno 1.000 conversioni per esperienza perché un&#39;attività funzioni rispetto alla conversione.
* In base ai tuoi obiettivi, decidi la ripartizione tra il controllo e le esperienze personalizzate prima di iniziare l&#39;attività.
* Determina se disponi di traffico sufficiente per la pagina in cui viene eseguita l&#39;attività [!UICONTROL Auto-Target] affinché i modelli di personalizzazione compilino in un tempo ragionevole.
* Se stai testando l&#39;algoritmo di personalizzazione, non è consigliabile modificare le esperienze o aggiungere o rimuovere attributi di profilo mentre l&#39;attività è in esecuzione.
* Prendere in considerazione il completamento di un&#39;attività A/B tra le offerte e le posizioni che si prevede di utilizzare nell&#39;attività [!UICONTROL Auto-Target] per assicurarsi che le posizioni e le offerte abbiano un impatto sull&#39;obiettivo di ottimizzazione. Se un&#39;attività A/B non riesce a dimostrare una differenza significativa, è probabile che [!UICONTROL Auto-Target] non riesca a generare incrementi.

  Se un test A/B non mostra differenze statisticamente significative tra le esperienze, probabilmente le offerte che stai prendendo in considerazione non sono sufficientemente diverse tra loro, le posizioni selezionate non incidono sulla metrica successo o l&#39;obiettivo di ottimizzazione è troppo lontano nell&#39;imbuto di conversione per essere influenzato dalle offerte scelte.

* Cerca di non apportare modifiche sostanziali alle esperienze durante l’attività.

+++

### [!UICONTROL Adobe] consiglia di utilizzare [!UICONTROL Auto Target] con una suddivisione 90(Controllo)/10(Target) fino a quando i modelli non vengono generati?

+++Risposta
La suddivisione ottimale del traffico dipende da cosa desideri eseguire.

Se l’obiettivo è quello di personalizzare il traffico il più possibile, puoi mantenere un’allocazione mirata del 90% e un controllo del 10% per la durata dell’attività. Se l’obiettivo è quello di eseguire un esperimento confrontando il comportamento degli algoritmi personalizzati rispetto al controllo, allora una suddivisione 50/50 è la migliore per la durata dell’attività.

Si consiglia di mantenere la suddivisione del traffico per la durata dell’attività in modo che i visitatori non passino da un’esperienza di targeting a una di controllo.

<!-- 
### Do the check marks indicating a model is built for that experience update if the report date range changes?

No, check marks for model generation show only the models built to date. There's no way to go back and see when a model was completed.
-->

+++

### Se un visitatore **non** vede l&#39;attività [!UICONTROL Auto-Target] e converte, la conversione conta nella mia attività?

+++Risposta
No, solo i visitatori che si qualificano e visualizzano l&#39;attività [!UICONTROL Auto-Target] sono conteggiati nel reporting.

+++

### Perché la mia attività [!UICONTROL Auto-Target] non sembra generare alcun incremento.

+++Risposta
Sono necessari quattro fattori affinché un&#39;attività [!UICONTROL Auto-Target] generi incremento:

* Le offerte devono essere sufficientemente diverse da influenzare i visitatori.
* Le offerte devono essere posizionate in un punto che faccia la differenza per l’obiettivo di ottimizzazione.
* Il test deve avere traffico e potenza statistica tali da consentire il rilevamento di un incremento.
* L’algoritmo di personalizzazione deve funzionare bene.

La migliore linea di azione è di assicurarsi in primo luogo che i contenuti e le posizioni, che compongono le esperienze di attività, facciano davvero una differenza per i tassi di risposta generali tramite un semplice test A/B e non personalizzato. Calcola le dimensioni del campione in tempo per assicurarti che sia possibile visualizzare un incremento ragionevole ed esegui il test A/B per una durata fissa senza interruzioni né modifiche.

Se i risultati di test A/B mostrano un incremento statisticamente significativo su una o più esperienze, può funzionare un&#39;attività personalizzata. Naturalmente, la personalizzazione può funzionare anche se non ci sono differenze nei tassi di risposta complessiva delle esperienze. In genere, il problema deriva dal fatto che le offerte e le posizioni non hanno un impatto sufficiente sull’obiettivo di ottimizzazione da rilevare con significatività statistica.

+++

### Quando devo interrompere l&#39;attività [!UICONTROL Auto-Target]?

+++Risposta
[!UICONTROL Auto-Target] può essere utilizzato come personalizzazione &quot;sempre attiva&quot; che si ottimizza costantemente. Soprattutto per i contenuti fissi, non è necessario interrompere l&#39;attività [!UICONTROL Auto-Target].

Se si desidera apportare modifiche sostanziali al contenuto dell&#39;attività [!UICONTROL Auto-Target], la procedura consigliata consiste nell&#39;avviare una nuova attività in modo che gli altri utenti che revisionano i report non confondano o riferiscano i risultati passati con contenuti diversi.

+++

### Quanto tempo devo aspettare per la generazione dei modelli? {#how-long}

+++Risposta
Il tempo necessario alla generazione dei modelli nell&#39;attività [!UICONTROL Auto-Target] dipende in genere dal traffico delle posizioni dell&#39;attività selezionate e dai tassi di conversione associati alla metrica di successo dell&#39;attività.

[!UICONTROL Auto-Target] non tenta di creare un modello personalizzato per una determinata esperienza finché non ci sono almeno 50 conversioni per tale esperienza. Inoltre, se il modello generato è di qualità insufficiente (come determinato dalla valutazione offline sui dati &quot;test&quot; di sospensione, utilizzando [una metrica nota come AUC](https://it.wikipedia.org/wiki/Receiver_operating_characteristic#Area_under_the_curve)), il modello non viene utilizzato per gestire il traffico in modo personalizzato.

Altri punti da tenere a mente sulla creazione di modelli di [!UICONTROL Auto-Target]:

* Dopo che un&#39;attività è attiva, [!UICONTROL Auto-Target] considera fino agli ultimi 45 giorni di dati serviti in modo casuale durante il tentativo di generare modelli. Ad esempio, controlla il traffico, più alcuni dati forniti in modo casuale dall’algoritmo.
* Quando [!UICONTROL Revenue per Visit] è la metrica di successo, in genere queste attività richiedono più dati per generare modelli a causa della varianza di dati più elevata che esiste in genere nei ricavi da visita rispetto al tasso di conversione.
* Poiché i modelli sono generati in base all’esperienza, sostituire un’esperienza con un’altra significa che è necessario raccogliere per la nuova esperienza un traffico sufficiente (almeno 50 conversioni) prima di poter ricostruire i modelli personalizzati.

+++

### L’attività contiene un modello generato. Le visite a quell’esperienza sono personalizzate?

+++Risposta
No, per iniziare la personalizzazione devono essere presenti almeno due modelli generati nell’attività.

+++

### Quando posso iniziare a esaminare i risultati della mia attività [!UICONTROL Auto-Target]?

+++Risposta
È possibile iniziare a esaminare i risultati del test [!UICONTROL Auto-Target] quando si dispone di almeno due esperienze con modelli generati (segno di spunta verde) per l&#39;esperienza con modelli generati.

+++

### Posso specificare un’esperienza particolare da usare come controllo?

+++Risposta
Puoi selezionare un&#39;esperienza da usare come controllo durante la creazione di un&#39;attività [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) o [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT).

Questa funzione ti consente di indirizzare l’intero traffico di controllo a un’esperienza specifica, in base alla percentuale di allocazione del traffico configurata nell’attività. Puoi quindi valutare i rapporti sulle prestazioni del traffico personalizzato rispetto al traffico verso l’esperienza di controllo.

Per ulteriori informazioni, consulta [Utilizzare un’esperienza specifica come controllo](/help/main/c-activities/t-automated-personalization/experience-as-control.md).

+++

### Posso cambiare la metrica obiettivo a metà strada attraverso un&#39;attività [!UICONTROL Auto-Target]? {#change-metric}

+++Risposta
L’Adobe non consiglia di modificare la metrica obiettivo a metà strada attraverso un’attività. Anche se è possibile modificare la metrica dell’obiettivo durante un’attività utilizzando l’interfaccia utente [!DNL Target], è sempre necessario avviare una nuova attività. Adobe non fornisce alcuna garanzia su ciò che accade se modifichi la metrica obiettivo in un’attività dopo l’esecuzione.

Questo consiglio si applica alle attività [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target] e [!UICONTROL Automated Personalization] che utilizzano [!DNL Target] o [!DNL Analytics] (A4T) come origine per la generazione di rapporti.

+++

### È possibile utilizzare l&#39;opzione [!UICONTROL Reset Report Data] durante l&#39;esecuzione di un&#39;attività [!UICONTROL Auto-Target]?

+++Risposta
L&#39;utilizzo dell&#39;opzione [!UICONTROL Reset Report Data] per le attività [!UICONTROL Auto-Target] non è consigliato. Anche se rimuove i dati di reporting visibili, questa opzione non rimuove tutti i record di formazione dal modello [!UICONTROL Auto-Target]. Invece di utilizzare l&#39;opzione [!UICONTROL Reset Report Data] per le attività [!UICONTROL Auto-Target], crea una nuova attività e disattiva l&#39;attività originale.

Questa guida si applica anche alle attività [!UICONTROL Auto-Allocate] e [!UICONTROL Automated Personalization].

+++

### Cosa succede se rimuovo una singola esperienza da un&#39;attività [!UICONTROL Auto-Target]?

+++Risposta
[!DNL Target] crea un modello per esperienza, pertanto rimuovendo un&#39;esperienza [!DNL Target] crea un modello in meno e non influisce sui modelli per le altre esperienze.

Si supponga, ad esempio, di disporre di un&#39;attività [!UICONTROL Auto-Target] con otto esperienze e di non apprezzare le prestazioni di un&#39;esperienza. Puoi rimuovere tale esperienza e non influisce sui modelli per le sette esperienze rimanenti.

+++

## Risoluzione dei problemi [!UICONTROL Auto-Target] {#section_23995AB813F24525AF294D20A20875C8}

A volte le attività non vanno come previsto. Di seguito sono riportate alcune potenziali sfide che potresti affrontare durante l&#39;utilizzo di [!UICONTROL Auto-Target] e alcune soluzioni suggerite.

### La mia attività [!UICONTROL Auto-Target] sta impiegando troppo tempo per generare i modelli.

+++Suggerimenti per la risoluzione dei problemi
Sono disponibili diverse modifiche dell&#39;impostazione dell&#39;attività che possono ridurre il tempo previsto per la generazione di modelli, tra cui il numero di esperienze nell&#39;attività [!UICONTROL Auto-Target], il traffico verso il sito e la metrica di successo selezionata.

**Soluzione:** controlla la configurazione dell&#39;attività e verifica se sono state apportate modifiche per migliorare la velocità di generazione dei modelli.

* Se la metrica di successo è impostata su [!UICONTROL RPV], è possibile modificare la conversione? Le attività di conversione tendono a richiedere meno traffico per la generazione dei modelli. Non perderai i dati di attività se modifichi la metrica di successo da RPV a conversione.
* La metrica del successo è molto in basso nel funnel di vendita dalle esperienze dell’attività? Un tasso di conversione dell’attività più basso aumenta i requisiti di traffico necessari per la generazione dei modelli, perché è necessario un numero minimo di conversioni.
* È possibile eliminare alcune esperienze dall’attività? La riduzione del numero di esperienze in un’attività riduce il tempo necessario per generare i modelli.
* Esiste una pagina con traffico più alto in cui questa attività avrebbe più successo? Maggiore è il traffico e le conversioni nelle posizioni di attività, più rapidi saranno i modelli generati.

+++

### La mia attività [!UICONTROL Auto-Target] non genera alcun incremento.

+++Suggerimenti per la risoluzione dei problemi
Sono necessari quattro fattori affinché un&#39;attività [!UICONTROL Auto-Target] generi incremento:

* Le offerte devono essere sufficientemente diverse da influenzare i visitatori.
* Le offerte devono essere posizionate in un punto che faccia la differenza per l’obiettivo di ottimizzazione.
* Il test deve avere traffico e potenza statistica tali da consentire il rilevamento di un incremento.
* L’algoritmo di personalizzazione deve funzionare bene.

**Soluzione:** in primo luogo, assicurati che l&#39;attività personalizzi il traffico. Se i modelli non sono generati per tutte le esperienze, l&#39;attività [!UICONTROL Auto-Target] fornisce ancora in modo casuale una parte significativa di visite per tentare di generare tutti i modelli il più rapidamente possibile. Se i modelli non sono generati, [!UICONTROL Auto-Target] non personalizza il traffico.

Quindi, assicurati che le offerte e le posizioni di attività facciano davvero la differenza nei tassi di risposta generali utilizzando un semplice test A/B non personalizzato. Calcola le dimensioni del campione in tempo per assicurarti che sia possibile visualizzare un incremento ragionevole ed esegui il test A/B per una durata fissa senza interruzioni né modifiche. Se i risultati di un test A/B mostrano un incremento statisticamente significativo su una o più esperienze, è probabile che un’attività personalizzata funzioni. Personalization può funzionare anche se non ci sono differenze nei tassi di risposta generali delle esperienze. In genere, il problema deriva dal fatto che le offerte e le posizioni non hanno un impatto sufficiente sull’obiettivo di ottimizzazione da rilevare con significatività statistica.

+++

### Qualsiasi metrica dipendente da una metrica di conversione non consegue mai la conversione.

+++Suggerimenti per la risoluzione dei problemi
Questo è previsto.

In un&#39;attività [!UICONTROL Auto-Target], una volta convertita una metrica di conversione (che si tratti di obiettivo di ottimizzazione o di corrispondenza), l&#39;utente viene rilasciato dall&#39;esperienza e l&#39;attività viene riavviata.

Prendiamo ad esempio un’attività con una metrica di conversione (C1) e una metrica aggiuntiva (A1). A1 dipende da C1. Quando un visitatore accede all’attività per la prima volta e i criteri di conversione per A1 e C1 non vengono soddisfatti, la metrica A1 non consegue la conversione a causa della dipendenza dalla metrica di successo. Se il visitatore converte C1 e poi A1, A1 non viene ancora convertito perché quando C1 viene convertito, il visitatore viene rilasciato.

+++
