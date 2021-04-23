---
keywords: privacy;indirizzo ip;geosegmentazione;opt out;opt-out;privacy dei dati;regolamenti governativi;regolamenti;rgpd;ccpa
description: Scopri in che modo Adobe [!DNL Target] rispetta le leggi sulla privacy dei dati applicabili, tra cui la raccolta e la gestione degli indirizzi IP e le istruzioni di rinuncia.
title: In che modo [!DNL Target] gestisce i problemi di privacy?
feature: Privacy e sicurezza
role: Developer
exl-id: fb632923-fa36-4553-88a6-f27860472eb6
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 70%

---

# Privacy

[!DNL Adobe Target] ha abilitato processi e impostazioni che ti consentono di utilizzare  [!DNL Target] in conformità alle leggi sulla privacy dei dati applicabili.

## Raccolta di indirizzi IP {#section_91BDB8105EBF4B85B7B8B8A14675AC85}

L&#39;indirizzo IP di un visitatore del tuo sito Web viene trasmesso a un DPC (Adobe Data Processing Center). In base alla configurazione di rete per il visitatore, l&#39;indirizzo IP non rappresenta necessariamente l&#39;indirizzo IP del relativo computer. Potrebbe essere ad esempio l&#39;indirizzo IP esterno di un firewall con traduzione degli indirizzi di rete (Network Address Translation, NAT), di un proxy HTTP o di un gateway Internet. Target non memorizza gli indirizzi IP dell&#39;utente o dati PII (personalmente identificabili). Gli indirizzi IP vengono utilizzati solo da Target per la durata della sessione (in memoria, senza persistenza).

## Sostituzione dell’ultimo ottetto degli indirizzi IP {#section_AE84EB0D7CE04E93B279B77732ADD61E}

Adobe ha sviluppato una nuova impostazione “privacy by design”, che può essere abilitata dall’Assistenza clienti di Adobe per Adobe Target. Quando questa impostazione è abilitata, l’ultimo ottetto (l’ultima parte) dell’indirizzo IP viene immediatamente oscurato quando l’indirizzo IP viene raccolto da Adobe. Questa forma di anonimizzazione viene eseguita prima di qualsiasi elaborazione dell’indirizzo IP, inclusa l’operazione di lookup geografico.

Quando questa funzione è abilitata, l’indirizzo IP è reso sufficientemente anonimo da non essere più identificabile come dato personale. Di conseguenza, è possibile utilizzare Adobe Target in conformità alle leggi sulla riservatezza dei dati nei paesi che non consentono la raccolta di informazioni personali. L’ottenimento di informazioni a livello di città sarà probabilmente influenzato in modo significativo dall’oscuramento dell’indirizzo IP. L’ottenimento di informazioni a livello di area e nazionale dovrebbe essere influenzato solo leggermente.

Sono disponibili le seguenti opzioni:

* Nessuna offuscamento: Target non nasconde alcuna parte dell’indirizzo IP.
* Ultimo ottetto: Target nasconde l’ultimo ottetto dell’indirizzo IP.
* IP completo: Target nasconde l’intero indirizzo IP.

Target riceve l’indirizzo IP completo e lo offusca (se impostato su Ultimo ottetto o IP completo) come specificato. Target conserva quindi in memoria l’indirizzo IP offuscato per tutta la durata della sessione.

>[!NOTE]
>
>[Contatta Adobe Client ](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) Carto per determinare quale impostazione stai utilizzando o per abilitare la funzione di offuscamento dell’IP.

## Geosegmentazione {#section_BB69F96559BD44BDA4177537C4A5345A}

Se attivi l’oscuramento dell’ultimo ottetto dell’indirizzo IP, i restanti valori dell’indirizzo IP possono essere analizzati utilizzando i rapporti in Adobe Target. Se l’ultimo ottetto dell’indirizzo IP non viene oscurato, l’indirizzo IP completo può essere analizzato in Adobe Target. Puoi utilizzare la funzione di geosegmentazione per mappare la posizione dei visitatori per area geografica. I dati di geosegmentazione sono granulari solo a livello di città o di codice postale, e non a livello individuale.

Se gli indirizzi IP sono completamente offuscati, GeoSegmentation e il target geografico non sono disponibili.

## Collegamento di rinuncia {#section_E7A62B7B99C94B3A806CB262D16E27FC}

Puoi aggiungere un collegamento di rinuncia ai siti per consentire ai visitatori di rinunciare a tutte le operazioni di conteggio e di distribuzione dei contenuti.

1. Aggiungi al sito il seguente collegamento:

   `<a href="https://clientcode.tt.omtrdc.net/optout"> Your Opt Out Language Here</a>`
1. Sostituisci il testo `clientcode` con il tuo codice cliente e aggiungi il testo o l’immagine da collegare all’URL di rinuncia.

Il visitatore che fa clic sul collegamento sarà escluso da qualsiasi richiesta mbox richiamata dalle relative sessioni di navigazione fino all’eliminazione dei cookie o per due anni (a seconda di quale dei due eventi si verifica prima). Questo funziona impostando un cookie per il visitatore denominato `disableClient` nel dominio `clientcode.tt.omtrdc.net`.

Anche se utilizzi un’implementazione di cookie di prima parte, la rinuncia viene impostata tramite un cookie di terze parti. Se il cliente utilizza solo un cookie di prima parte, Target controlla se è impostato un cookie di rinuncia.

## Normative sulla privacy e la protezione dei dati

Consulta [Normative sulla privacy e la protezione dei dati](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md) per informazioni sul Regolamento generale sulla protezione dei dati (RGPD) dell&#39;Unione Europea, il California Consumer Privacy Act (CCPA) e altri requisiti internazionali sulla privacy, e come questi regolamenti influiscono sulla tua organizzazione e su Adobe Target.
