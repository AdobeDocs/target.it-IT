---
kewords: Automated Personalization;ap;troublshoot;troubleshooting;model;lift
description: A volte le attività non vanno come previsto. Questo articolo elenca alcuni potenziali problemi che si possono presentare durante l’utilizzo della Personalizzazione automatizzata, con possibili soluzioni.
title: Risolvere i problemi relativi alla personalizzazione automatica
feature: Automated Personalization
translation-type: tm+mt
source-git-commit: 4adade56529fb95e4400e06d04d3c6c69e120edc
workflow-type: tm+mt
source-wordcount: '725'
ht-degree: 94%

---


# ![PREMIUM](/help/assets/premium.png) Risoluzione dei problemi di Personalizzazione automatizzata{#troubleshoot-automated-personalization}

A volte le attività non vanno come previsto. Questo articolo elenca alcuni potenziali problemi che si possono presentare durante l’utilizzo della Personalizzazione automatizzata, con possibili soluzioni.

## La mia attività di Personalizzazione automatizzata sta impiegando troppo tempo per generare i modelli. {#section_20028B204DBB4D77A324BA193434AEE2}

Sono disponibili diverse modifiche dell&#39;impostazione dell&#39;attività che possono ridurre il tempo previsto per la generazione di modelli, tra cui il numero di esperienze nell&#39;attività di Personalizzazione automatizzata, il traffico verso il sito e la metrica di successo selezionata.

**Soluzione:** esamina l’impostazione dell’attività e verifica se ci sono modifiche che intendi apportare per migliorare la velocità con cui i modelli vengono generati.

* Se la metrica di successo è impostata su RPV, è possibile modificare la conversione? Le attività di conversione tendono a richiedere meno traffico per la generazione dei modelli. Non perderai i dati di attività se modifichi la metrica di successo da RPV a conversione.
* La metrica del successo è molto in basso nel funnel di vendita dalle esperienze dell’attività? Con un tasso di conversione basso, la generazione dei modelli richiederà più traffico poiché è necessario un numero minimo di conversioni.
* Puoi eliminare alcune offerte i esperienze dalla tua attività? Diminuendo il numero di esperienze, diminuirà anche il tempo necessario alla generazione dei modelli.
* Esiste una pagina con traffico più alto in cui questa attività avrebbe più successo? Maggiori sono il traffico e le conversioni nelle posizioni dell’attività, più rapidamente verranno generati i modelli.

## La mia attività di Personalizzazione automatizzata non ha generato alcun incremento. {#section_8900BC8968474438B8092F7A94C0C6CF}

Ci sono diversi fattori necessari affinché un’attività di Personalizzazione automatizzata generi incremento:

* Le offerte devono essere abbastanza diverse per influenzare i visitatori.
* Le Offerte devono essere tali da poter influenzare l’obiettivo di ottimizzazione.
* Il test deve avere traffico e potenza statistica tali da consentire il rilevamento di un incremento.
* L’algoritmo di personalizzazione deve funzionare bene.

**Soluzione:** la migliore linea di azione è di assicurarsi in primo luogo che i contenuti e le posizioni, che compongono le esperienze di attività, facciano davvero una differenza per i tassi di risposta generali tramite un semplice test A/B e non personalizzato. Calcola le dimensioni del campione in tempo per assicurarti che sia possibile visualizzare un incremento ragionevole ed esegui il test A/B per una durata fissa senza interruzioni né modifiche. Se i risultati di un test A/B mostrano un incremento statisticamente significativo su una o più esperienze, è probabile che un’attività personalizzata funzioni. Naturalmente, la personalizzazione può funzionare anche se non ci sono differenze nei tassi di risposta complessiva delle esperienze. Il problema, solitamente, deriva dalle offerte/posizioni che non hanno un impatto sull’obiettivo di ottimizzazione tale da poter essere rilevato con rilevanza statistica.

## L’URL della mia attività Personalizzazione automatizzata mostra il contenuto delle offerte su pagine errate.  {#section_82A224406DBF4107B05204BEFBBE458C}

In AP, le regole di verifica degli URL e dei modelli vengono aggiunte al vincolo di immissione della richiesta [!DNL Target] (ad esempio, target-global-mbox), in cui vengono valutate solo una volta. Quando un utente si qualifica per un&#39;attività, le regole di targeting a livello di richiesta di Target non vengono rivalutate. Tuttavia, il pubblico di destinazione viene aggiunto alle regole di targeting per la posizione.

**Soluzione:** aggiungi le regole di modello necessarie come pubblico di input della campagna. La valutazione del pubblico avviene su ogni richiesta/chiamata.

Questo problema verrà risolto in una delle prossime versioni.

## Le metriche dipendenti dalla metrica di conversione non conseguono mai la conversione.  {#section_076D1F44298C4E4A849AC52F5A33214D}

Si tratta di un comportamento previsto.

In un&#39;attività di Personalizzazione automatizzata, una volta convertita una metrica di conversione (che si tratti di obiettivo di ottimizzazione o di corrispondenza), l&#39;utente viene rilasciato dall&#39;esperienza e l&#39;attività viene riavviata.

Prendiamo ad esempio un’attività con una metrica di conversione (C1) e una metrica aggiuntiva (A1). A1 dipende da C1. Quando un visitatore accede all’attività per la prima volta e i criteri di conversione per A1 e C1 non vengono soddisfatti, la metrica A1 non consegue la conversione a causa della dipendenza dalla metrica di successo. Se il visitatore consegue la conversione per C1 e poi per A1, la conversione A1 non risulta perché, non appena ottenuta la conversione per C1, il visitatore viene rilasciato.

## I miei URL di esperienza non funzionano come previsto.  {#section_7B08DA1F30AA483E9406336DAF361BA4}

* Se non puoi visualizzare l&#39;anteprima nella nuova scheda (a causa della cache del browser), prova ad aggiornare due o tre volte o a copiare il collegamento e aprirlo in un nuovo browser o una nuova sessione.
* Rigenera i collegamenti degli URL di esperienza se hai modificato qualsiasi contenuto e condividi i nuovi collegamenti con i tuoi compagni di team.

