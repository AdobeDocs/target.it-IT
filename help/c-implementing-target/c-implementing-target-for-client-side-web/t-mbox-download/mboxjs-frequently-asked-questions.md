---
keywords: faq mbox.js;domande frequenti mbox.js;document.write;tt.omtrdc.net;blocco del parser
description: Scopri l’implementazione legacy di mbox.js di Adobe Target. Esegui la migrazione a Adobe Experience Platform Web SDK (AEP Web SDK) o all’ultima versione di at.js.
title: Quali sono alcune domande frequenti su [!DNL Target] mbox.js?
feature: at.js
role: Developer
exl-id: 0e207896-d45b-45f9-8556-6532fda72a45
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 71%

---

# Domande frequenti su mbox.js

Risposte alle domande più frequenti su mbox.js.

>[!IMPORTANT]
>
>**Terminazione di mbox.js**: A partire dal 31 marzo 2021,  [!DNL Adobe Target] non supporta più la libreria mbox.js . Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto positivo sulle pagine che hanno [!DNL Target] attività in esecuzione servendo il contenuto predefinito.
>
>È consigliabile che tutti i clienti effettuino la migrazione alla versione più recente della nuova [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js prima di tale data, per evitare potenziali problemi con i siti. Per ulteriori informazioni, consulta [Panoramica: implementare Target per web lato client](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## Qual è l’impatto di mbox.js sui tempi di caricamento pagina? {#section_90B3B94FE0BF4B369577FCB97B67F089}

Per ulteriori informazioni, consulta [Vantaggi di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#benefits).

## Perché compaiono messaggi di avviso “blocco del parser” in Google Chrome quando si utilizzano mbox.js e document.write? {#section_355A3A5BF02F42EEB8271C96EF41590A}

Questo messaggio della console viene visualizzato quando si utilizza Chrome in molti scenari in cui la funzione `document.write` viene utilizzata all’interno del file mbox.js. Questo è un messaggio di avviso e non dovrebbe influenzare il processo di configurazione dell’attività.

Il modo migliore per prevenire questa situazione consiste nella [migrazione dell’implementazione di Target alla libreria JavaScript at. js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA), che non utilizza la funzione `document.write`. L’utilizzo di at.js fornisce molti vantaggi rispetto a mbox.js. Per ulteriori informazioni, consulta [Domande frequenti su at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/target-atjs-faq.md#concept_D6EFE8D84A06476DB5ABD494D7E8C769).

## Perché le mie mbox non vengono lanciate sulle mie pagine web? {#section_4BA5DA424B734324AAB51E4588FA50F5}

I clienti di Target utilizzano talvolta istanze basate su cloud con [!DNL Target] per test o semplici prove di concetto. Questi domini, e molti altri, fanno parte dell’[elenco dei suffissi pubblici](https://publicsuffix.org/list/public_suffix_list.dat).

I browser moderni non salvano i cookie se si utilizzano questi domini, a meno che non si personalizzi l’impostazione `cookieDomain` utilizzando targetGlobalSettings(). Per ulteriori informazioni, consulta [Utilizzo di istanze basate su Cloud con Target](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-debugging-atjs/targeting-using-cloud-based-instances.md#concept_A2077766948F4EA081CE592D8998F566).

## Le chiamate server [!DNL Target] sono indirizzate al dominio tt.omtrdc.net: di che si tratta? {#section_999C29940E8B4CAD8A957A6B1D440317}

[!DNL tt.omtrdc.net] è il nome di dominio della rete EDGE di Adobe, utilizzato per ricevere tutte le chiamate server per Target.

## Perché at.js e mbox.js non utilizzano i flag HttpOnly e Secure? {#section_74527E3B41B54B0A83F217C3E664ED1F}

HttpOnly può essere impostato solo tramite codice basato su server. I cookie Target, come mbox, vengono creati e salvati tramite il codice JavaScript, quindi Target non può utilizzare il flag di cookie HttpOnly.

È possibile impostare il flag Secure tramite JavaScript solo se la pagina è stata caricata tramite HTTPS. Se la pagina viene inizialmente caricata tramite HTTP, JavaScript non può impostare questo flag. Inoltre, se viene utilizzato il flag Secure, il cookie sarà disponibile solo nelle pagine HTTPS.

Per garantire che Target possa correttamente tenere traccia degli utenti e per far sì che i cookie vengano generati dal lato del cliente, Target non utilizza nessuno di questi flag.
