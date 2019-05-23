---
description: In Adobe Target sono stati inclusi processi e impostazioni che ne consentono l’utilizzo in conformità con le leggi sulla riservatezza dei dati.
keywords: Panoramica e riferimento
seo-description: In Adobe Target sono stati inclusi processi e impostazioni che ne consentono l’utilizzo in conformità con le leggi sulla riservatezza dei dati.
seo-title: Privacy
solution: Target
subtopic: Introduzione
title: Privacy
topic: Standard
uuid: aaeda1e6-7b2c-4a00-b65d-bfc95ea796b5
translation-type: tm+mt
source-git-commit: 19a73ca8d1f165a5279b2b76f5f22057a070f0a9

---


# Privacy{#privacy}

In Adobe Target sono stati inclusi processi e impostazioni che ne consentono l’utilizzo in conformità con le leggi sulla riservatezza dei dati.

## Raccolta di indirizzi IP  {#section_91BDB8105EBF4B85B7B8B8A14675AC85}

L&#39;indirizzo IP di un visitatore del tuo sito Web viene trasmesso a un DPC (Adobe Data Processing Center). In base alla configurazione di rete per il visitatore, l&#39;indirizzo IP non rappresenta necessariamente l&#39;indirizzo IP del relativo computer. Potrebbe essere ad esempio l&#39;indirizzo IP esterno di un firewall con traduzione degli indirizzi di rete (Network Address Translation, NAT), di un proxy HTTP o di un gateway Internet. Target non memorizza gli indirizzi IP dell&#39;utente o dati PII (personalmente identificabili). Gli indirizzi IP vengono utilizzati solo da Target per la durata della sessione (in memoria, senza persistenza).

## Oscuramento dell’ultimo ottetto dell’indirizzo IP {#section_AE84EB0D7CE04E93B279B77732ADD61E}

Adobe ha sviluppato una nuova impostazione “privacy by design”, che può essere abilitata dall’Assistenza clienti di Adobe per Adobe Target. Quando questa impostazione è abilitata, l’ultimo ottetto (l’ultima parte) dell’indirizzo IP viene immediatamente oscurato quando l’indirizzo IP viene raccolto da Adobe. Questa forma di anonimizzazione viene eseguita prima di qualsiasi elaborazione dell’indirizzo IP, inclusa l’operazione di lookup geografico.

Quando questa funzione è abilitata, l’indirizzo IP è reso sufficientemente anonimo da non essere più identificabile come dato personale. Di conseguenza, è possibile utilizzare Adobe Target in conformità alle leggi sulla riservatezza dei dati nei paesi che non consentono la raccolta di informazioni personali. L’ottenimento di informazioni a livello di città sarà probabilmente influenzato in modo significativo dall’oscuramento dell’indirizzo IP. L’ottenimento di informazioni a livello di area e nazionale dovrebbe essere influenzato solo leggermente.

È disponibile anche un&#39;impostazione per offuscare l&#39;intero indirizzo IP.

Per abilitare la funzione di oscuramento dell’IP, contatta l’Assistenza clienti di Adobe.

## Geosegmentazione  {#section_BB69F96559BD44BDA4177537C4A5345A}

Se attivi l’oscuramento dell’ultimo ottetto dell’indirizzo IP, i restanti valori dell’indirizzo IP possono essere analizzati utilizzando i rapporti in Adobe Target. Se l’ultimo ottetto dell’indirizzo IP non viene oscurato, l’indirizzo IP completo può essere analizzato in Adobe Target. Puoi utilizzare la funzione di geosegmentazione per mappare la posizione dei visitatori per area geografica. I dati di geosegmentazione sono granulari solo a livello di città o di codice postale, e non a livello individuale.

Se gli indirizzi IP sono completamente offuscati, GeoSegmentation e il target geografico non sono disponibili.

## Collegamento per la rinuncia {#section_E7A62B7B99C94B3A806CB262D16E27FC}

Puoi aggiungere un collegamento di rinuncia ai siti per consentire ai visitatori di rinunciare a tutte le operazioni di conteggio e di distribuzione dei contenuti.

1. Aggiungi al sito il seguente collegamento:

   `<a href="https://clientcode.tt.omtrdc.net/optout"> Your Opt Out Language Here</a>`
1. Sostituisci il testo `clientcode` con il tuo codice cliente e aggiungi il testo o l’immagine da collegare all’URL di rinuncia.

Il visitatore che fa clic sul collegamento sarà escluso da qualsiasi richiesta mbox richiamata dalle relative sessioni di navigazione fino all’eliminazione dei cookie o per due anni (a seconda di quale dei due eventi si verifica prima). Questo funziona impostando un cookie per il visitatore denominato `disableClient` nel dominio `clientcode.tt.omtrdc.net`.

Anche se utilizzi un’implementazione di cookie di prima parte, la rinuncia viene impostata tramite un cookie di terze parti. Se il cliente utilizza solo un cookie di prima parte, Target controlla se è impostato un cookie di rinuncia.
