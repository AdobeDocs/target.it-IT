---
keywords: Automated Personalization;ap;risoluzione dei problemi;risoluzione dei problemi;modello;incremento
description: Esplora le potenziali sfide che potresti affrontare durante l'utilizzo di [!UICONTROL attività Automated Personalization] (AP) in Adobe Target, insieme alle soluzioni suggerite.
title: Come posso risolvere i problemi relativi alle [!UICONTROL attività Automated Personalization]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Automated Personalization
exl-id: bc23e5db-5b65-44be-be45-c972287a64e7
TQID: 'https://experienceleague.adobe.com/1Qevyq-TiutN1dEZnfC1DDmUgXoHIxtBl-3RMPq-m-0'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
    internal-label: Automated personalization
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 44c6bdd4ab818226e76477782d7e4238b49d5cdc
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 7%
---
# Risoluzione dei problemi di [!UICONTROL Automated Personalization] {#ap-troubleshooting}

>[!BEGINSHADEBOX]

**In questa pagina:** Trova soluzioni ai problemi comuni con **[!UICONTROL attività Automated Personalization]**.

>[!ENDSHADEBOX]

Le attività non vanno sempre come previsto. Utilizzare il seguente elenco per identificare la causa dei problemi comuni nelle attività di [!UICONTROL Automated Personalization] (AP) e per applicare la soluzione suggerita.

## Modelli e sollevamento {#models-and-lift}

+++ La mia attività [!UICONTROL Automated Personalization] sta impiegando troppo tempo per generare i modelli

Diverse scelte di configurazione dell&#39;attività influiscono sul tempo che i modelli devono generare, tra cui il numero di esperienze nell&#39;attività **[!UICONTROL Automated Personalization]**, il traffico verso il sito e la metrica di successo selezionata.

**Soluzione:** verifica la configurazione dell&#39;attività e verifica se è possibile apportare modifiche che migliorano la velocità di generazione dei modelli.

* Se la metrica di successo è impostata su RPV, è possibile modificare la conversione? Le attività di conversione tendono a richiedere meno traffico per la generazione dei modelli. I dati dell’attività non vengono persi se modifichi la metrica di successo da RPV alla conversione.
* La metrica del successo è molto in basso nel funnel di vendita dalle esperienze dell’attività? Un tasso di conversione dell’attività inferiore aumenta i requisiti di traffico per i modelli da generare, in quanto è richiesto un numero minimo di conversioni.
* Puoi escludere alcune offerte o esperienze dalla tua attività? La riduzione del numero di esperienze in un’attività velocizza il tempo necessario per creare modelli.
* Esiste una pagina con traffico più elevato in cui questa attività avrebbe più successo? Maggiore è il traffico e le conversioni nelle posizioni di attività, più rapidi saranno i modelli generati.

+++

+++ La mia attività [!UICONTROL Automated Personalization] non ha generato l&#39;incremento

Sono necessari diversi fattori affinché un&#39;attività **[!UICONTROL Automated Personalization]** generi incremento:

* Le offerte devono essere sufficientemente diverse da influenzare i visitatori.
* Le offerte devono essere posizionate in un punto che faccia la differenza per l’obiettivo di ottimizzazione.
* Il test deve avere traffico e potenza statistica tali da consentire il rilevamento di un incremento.
* L’algoritmo di personalizzazione deve funzionare bene.

**Soluzione:** La migliore linea di azione è di assicurarsi in primo luogo che i contenuti e le posizioni, che compongono le esperienze di attività, facciano davvero una differenza per i tassi di risposta generali, utilizzando un semplice test A/B e non personalizzato. Calcola le dimensioni del campione in anticipo per assicurarti che sia disponibile energia sufficiente per visualizzare un incremento ragionevole, quindi esegui il test A/B per una durata fissa senza interromperlo o apportare modifiche. Se i risultati del test A/B mostrano un incremento statisticamente significativo su una o più esperienze, è probabile che un’attività personalizzata abbia successo. Personalization può funzionare anche se non ci sono differenze nei tassi di risposta generali delle esperienze. In genere, il problema deriva dal fatto che le offerte o le posizioni non hanno un impatto sufficiente sull’obiettivo di ottimizzazione da rilevare con significatività statistica.

+++

## Configurazione delle attività e reporting {#setup-and-reporting}

+++ L&#39;URL della mia attività [!UICONTROL Automated Personalization] mostra il contenuto delle offerte su pagine errate

**Causa:** In **[!UICONTROL Automated Personalization]**, le regole di test di URL e modelli vengono aggiunte al vincolo di immissione della richiesta [!DNL Target] (ad esempio, target-global-mbox), dove vengono valutate una sola volta. Quando un visitatore diventa idoneo per un&#39;attività, le regole di targeting a livello di richiesta [!DNL Target] non vengono rivalutate, mentre il pubblico di targeting viene aggiunto alle regole di targeting della posizione.

**Soluzione:** Aggiungi le regole del modello necessarie come pubblico di input dell&#39;attività. La valutazione del pubblico avviene a ogni richiesta (chiamata).

+++

+++ Qualsiasi metrica dipendente da una metrica di conversione non converte mai

Questo comportamento è previsto.

In un&#39;attività **[!UICONTROL Automated Personalization]**, una volta convertita una metrica di conversione (che si tratti di un obiettivo di ottimizzazione o di un obiettivo post), il visitatore viene rilasciato dall&#39;esperienza e l&#39;attività viene riavviata.

Ad esempio, un’attività ha una metrica di conversione (C1) e una metrica aggiuntiva (A1) che dipende da C1. Quando un visitatore accede all’attività per la prima volta e non ha convertito né C1 né A1, A1 non viene convertito a causa della dipendenza dalla metrica di successo. Se il visitatore converte C1 e poi A1, A1 non viene ancora convertito, in quanto il visitatore viene rilasciato quando C1 viene convertito.

+++

+++ I miei URL di esperienza non funzionano come previsto

**Soluzione:** Utilizzare le azioni seguenti:

* Se non riesci a visualizzare l’anteprima nella nuova scheda (a causa della cache del browser), prova ad aggiornare due o tre volte. Puoi anche copiare il collegamento e aprirlo in un nuovo browser o in una nuova sessione.
* Se hai modificato un contenuto, rigenera i collegamenti URL esperienza e condividi i nuovi collegamenti con i tuoi colleghi di team.

+++
