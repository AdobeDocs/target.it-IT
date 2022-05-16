---
keywords: privacy;indirizzo ip;geosegmentazione;opt out;opt-out;rinuncia;privacy dei dati;regolamenti governativi;regolamenti;rgpd;ccpa
description: Scopri il modo in cui Adobe  [!DNL Target]  rispetta le leggi sulla privacy dei dati applicabili, inclusa la raccolta e la gestione degli indirizzi IP e le istruzioni per la rinuncia.
title: In che modo  [!DNL Target]  gestisce le questioni relative alla privacy?
feature: Privacy & Security
role: Developer
exl-id: fb632923-fa36-4553-88a6-f27860472eb6
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: ht
source-wordcount: '738'
ht-degree: 100%

---

# Privacy

In [!DNL Adobe Target] sono stati inclusi processi e impostazioni che ti consentono di utilizzare [!DNL Target] in conformità con le leggi sulla privacy dei dati.

## Raccolta di dati sull’utilizzo delle funzioni

I dati di utilizzo delle singole funzioni vengono raccolti per uso interno di [!DNL Adobe] per stabilire se le funzioni di [!DNL Target] vengono eseguite come previsto o per identificare le funzioni utilizzate poco. Vengono raccolte varie misurazioni della latenza per contribuire a risolvere i problemi legati alle prestazioni. I dati personali non vengono raccolti.

Puoi rinunciare al reporting dei dati di utilizzo nei nostri SDK impostando `telemetryEnabled` su false nelle opzioni di inizializzazione del client. Per ulteriori informazioni, consulta [telemetryEnabled in targetGlobalSettings](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#telemetry).

## Raccolta di indirizzi IP {#section_91BDB8105EBF4B85B7B8B8A14675AC85}

L&#39;indirizzo IP di un visitatore del tuo sito Web viene trasmesso a un DPC (Adobe Data Processing Center). In base alla configurazione di rete per il visitatore, l&#39;indirizzo IP non rappresenta necessariamente l&#39;indirizzo IP del relativo computer. Potrebbe essere ad esempio l&#39;indirizzo IP esterno di un firewall con traduzione degli indirizzi di rete (Network Address Translation, NAT), di un proxy HTTP o di un gateway Internet. Target non memorizza gli indirizzi IP dell&#39;utente o dati PII (personalmente identificabili). Gli indirizzi IP vengono utilizzati solo da Target per la durata della sessione (in memoria, senza persistenza).

## Sostituzione dell’ultimo ottetto di indirizzi IP {#section_AE84EB0D7CE04E93B279B77732ADD61E}

Adobe ha sviluppato una nuova impostazione “privacy by design”, che può essere abilitata dall’Assistenza clienti di Adobe per Adobe Target. Quando questa impostazione è abilitata, l’ultimo ottetto (l’ultima parte) dell’indirizzo IP viene immediatamente oscurato quando l’indirizzo IP viene raccolto da Adobe. Questa forma di anonimizzazione viene eseguita prima di qualsiasi elaborazione dell’indirizzo IP, inclusa l’operazione di lookup geografico.

Quando questa funzione è abilitata, l’indirizzo IP è reso sufficientemente anonimo da non essere più identificabile come dato personale. Di conseguenza, è possibile utilizzare Adobe Target in conformità alle leggi sulla riservatezza dei dati nei paesi che non consentono la raccolta di informazioni personali. L’ottenimento di informazioni a livello di città sarà probabilmente influenzato in modo significativo dall’oscuramento dell’indirizzo IP. L’ottenimento di informazioni a livello di area e nazionale dovrebbe essere influenzato solo leggermente.

Sono disponibili le seguenti impostazioni:

* No obfuscation (Nessun offuscamento): Target non nasconde alcuna parte dell’indirizzo IP.
* Last octet (Ultimo ottetto): Target nasconde l’ultimo ottetto dell’indirizzo IP.
* Full IP (IP completo): Target nasconde l’intero indirizzo IP.

Target riceve l’indirizzo IP completo e lo offusca (se impostato su Last octet o Full IP) come specificato. Target tiene quindi in memoria l’indirizzo IP offuscato durante la sessione.

>[!NOTE]
>
>[Contatta l’Assistenza clienti di Adobe](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) per determinare quale impostazione stai utilizzando attualmente o per abilitare la funzione di oscuramento dell’IP.

## Geosegmentazione {#section_BB69F96559BD44BDA4177537C4A5345A}

Se attivi l’oscuramento dell’ultimo ottetto dell’indirizzo IP, i restanti valori dell’indirizzo IP possono essere analizzati utilizzando i rapporti in Adobe Target. Se l’ultimo ottetto dell’indirizzo IP non viene oscurato, l’indirizzo IP completo può essere analizzato in Adobe Target. Puoi utilizzare la funzione di geosegmentazione per mappare la posizione dei visitatori per area geografica. I dati di geosegmentazione sono granulari solo a livello di città o di codice postale, e non a livello individuale.

Se gli indirizzi IP sono completamente offuscati, GeoSegmentation e il target geografico non sono disponibili.

## Collegamento per la rinuncia {#section_E7A62B7B99C94B3A806CB262D16E27FC}

Puoi aggiungere un collegamento di rinuncia ai siti per consentire ai visitatori di rinunciare a tutte le operazioni di conteggio e di distribuzione dei contenuti.

1. Aggiungi al sito il seguente collegamento:

   `<a href="https://clientcode.tt.omtrdc.net/optout"> Your Opt Out Language Here</a>`

1. (Facoltativo) Se utilizzi CNAME, il collegamento deve contenere il parametro &quot;client=`clientcode`&quot;, ad esempio: https://my.cname.domain/optout?client=clientcode.

1. Sostituisci `clientcode` con il tuo codice cliente e aggiungi il testo o l’immagine da collegare all’URL di rinuncia.

Il visitatore che fa clic sul collegamento sarà escluso da qualsiasi richiesta mbox richiamata dalle relative sessioni di navigazione fino all’eliminazione dei cookie o per due anni (a seconda di quale dei due eventi si verifica prima). Questo funziona impostando un cookie per il visitatore denominato `disableClient` nel dominio `clientcode.tt.omtrdc.net`.

Anche se utilizzi un’implementazione di cookie di prima parte, la rinuncia viene impostata tramite un cookie di terze parti. Se il cliente utilizza solo un cookie di prima parte, Target controlla se è impostato un cookie di rinuncia.

## Normative sulla privacy e la protezione dei dati

Consulta [Privacy and data protection regulations](/help/main/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md) (Normative sulla privacy e la protezione dei dati) per informazioni sul regolamento generale sulla protezione dei dati (RGPD) dell’Unione Europea, sul California Consumer Privacy Act (CCPA) e altri requisiti internazionali sulla privacy e su come queste normative influiscono sulla tua organizzazione e su Adobe Target.
