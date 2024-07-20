---
kewords: Automated Personalization;ap;troublshoot;troubleshooting;model;lift
description: Esplora le potenziali sfide che potresti affrontare durante l'utilizzo delle attività di [!UICONTROL Automated Personalization] (AP) in Adobe Target, insieme alle soluzioni suggerite.
title: Come posso risolvere i problemi relativi a [!UICONTROL Automated Personalization] attività?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."
feature: Automated Personalization
exl-id: bc23e5db-5b65-44be-be45-c972287a64e7
source-git-commit: 2cb2c2b68f6487d1af41ecc7e73750afa1ad85f9
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 32%

---

# Risoluzione dei problemi di [!UICONTROL Automated Personalization]

A volte le attività non vanno come previsto. Di seguito sono riportate alcune potenziali sfide che potresti affrontare durante l&#39;utilizzo di [!UICONTROL Automated Personalization] (AP) e alcune soluzioni suggerite.

## La mia attività [!UICONTROL Automated Personalization] sta impiegando troppo tempo per generare i modelli. {#section_20028B204DBB4D77A324BA193434AEE2}

+++Consulta i dettagli

Sono disponibili diverse modifiche dell&#39;impostazione dell&#39;attività che possono ridurre il tempo previsto per la generazione di modelli, tra cui il numero di esperienze nell&#39;attività [!UICONTROL Automated Personalization], il traffico verso il sito e la metrica di successo selezionata.

**Soluzione:** controlla la configurazione dell&#39;attività e verifica se sono state apportate modifiche per migliorare la velocità di generazione dei modelli.

* Se la metrica di successo è impostata su RPV, è possibile modificare la conversione? Le attività di conversione tendono a richiedere meno traffico per la generazione dei modelli. I dati dell’attività non vengono persi se modifichi la metrica di successo da RPV alla conversione.
* La metrica del successo è molto in basso nel funnel di vendita dalle esperienze dell’attività? Con un tasso di conversione basso, la generazione dei modelli richiederà più traffico poiché è necessario un numero minimo di conversioni.
* Puoi eliminare alcune offerte i esperienze dalla tua attività? La riduzione del numero di esperienze in un’attività velocizza il tempo necessario per creare modelli.
* Esiste una pagina con traffico più elevato in cui questa attività avrebbe più successo? Maggiore è il traffico e le conversioni nelle posizioni di attività, più rapidi saranno i modelli generati.

+++

## La mia attività [!UICONTROL Automated Personalization] non ha generato l&#39;incremento. {#section_8900BC8968474438B8092F7A94C0C6CF}

+++Consulta i dettagli

Ci sono diversi fattori necessari affinché un&#39;attività [!UICONTROL Automated Personalization] generi incremento:

* Le offerte devono essere sufficientemente diverse da influenzare i visitatori.
* Le offerte devono essere posizionate in un punto che faccia la differenza per l’obiettivo di ottimizzazione.
* Il test deve avere traffico e potenza statistica tali da consentire il rilevamento di un incremento.
* L’algoritmo di personalizzazione deve funzionare bene.

**Soluzione:** la migliore linea di azione è di assicurarsi in primo luogo che i contenuti e le posizioni, che compongono le esperienze di attività, facciano davvero una differenza per i tassi di risposta generali tramite un semplice test A/B e non personalizzato. Calcola le dimensioni del campione in anticipo. Calcolare le dimensioni dei campioni in anticipo consente di garantire una potenza sufficiente per visualizzare un incremento ragionevole. Puoi quindi eseguire il test A/B per una durata fissa senza interromperlo o apportare modifiche. Se il risultato di un test A/B mostra un incremento statisticamente significativo su una o più esperienze, è probabile che un’attività personalizzata abbia esito positivo. Personalization può funzionare anche se non ci sono differenze nei tassi di risposta generali delle esperienze. In genere, il problema deriva dal fatto che le offerte o le posizioni non hanno un impatto sufficiente sull’obiettivo di ottimizzazione da rilevare con significatività statistica.

+++

## L&#39;URL della mia attività [!UICONTROL Automated Personalization] mostra il contenuto delle offerte su pagine errate. {#section_82A224406DBF4107B05204BEFBBE458C}

+++Consulta i dettagli

In [!UICONTROL Automated Personalization], le regole di test di URL e modelli vengono aggiunte al vincolo di immissione della richiesta [!DNL Target] (ad esempio, target-global-mbox), dove vengono valutate una sola volta. Quando un utente si qualifica per un’attività, le regole di targeting a livello di richiesta di Target non vengono rivalutate. Tuttavia, il pubblico di destinazione viene aggiunto alle regole di targeting per la posizione.

**Soluzione:** Aggiungi le regole del modello necessarie come pubblico-input dell&#39;attività. La valutazione del pubblico avviene su ogni richiesta/chiamata.

+++

## Qualsiasi metrica dipendente da una metrica di conversione non consegue mai la conversione. {#section_076D1F44298C4E4A849AC52F5A33214D}

+++Consulta i dettagli

Si tratta di un comportamento previsto.

In un&#39;attività [!UICONTROL Automated Personalization], una volta convertita una metrica di conversione (che si tratti di obiettivo di ottimizzazione o di corrispondenza), il visitatore viene rilasciato dall&#39;esperienza e l&#39;attività viene riavviata.

Prendiamo ad esempio un’attività con una metrica di conversione (C1) e una metrica aggiuntiva (A1). A1 dipende da C1. Quando un visitatore accede all’attività per la prima volta e i criteri di conversione per A1 e C1 non vengono soddisfatti, la metrica A1 non consegue la conversione a causa della dipendenza dalla metrica di successo. Se il visitatore converte C1 e poi A1, A1 non viene ancora convertito perché quando C1 viene convertito, il visitatore viene rilasciato.

+++

## I miei URL di esperienza non funzionano come previsto. {#section_7B08DA1F30AA483E9406336DAF361BA4}

+++Consulta i dettagli

* Se non riesci a visualizzare l’anteprima nella nuova scheda (a causa della cache del browser), prova ad aggiornare due o tre volte. Puoi anche copiare il collegamento e aprirlo in un nuovo browser o in una nuova sessione.
* Rigenera i collegamenti degli URL di esperienza se hai modificato qualsiasi contenuto e condividi i nuovi collegamenti con i tuoi compagni di team.

+++
