---
keywords: lato server;lato server;sdk;sdk;on-device;decisioning;sul dispositivo;ondevice;latenza zero;latenza;vicino a zero;node.js
description: 'Scopri come utilizzare le decisioni sui dispositivi per memorizzare nella cache le attività A/B e MVT sul server in modo da eseguire le decisioni in memoria a latenza vicina allo zero. [!DNL Target] '
title: Cos’è On-Device Decisioning?
feature: Implementare lato server
role: Developer
exl-id: ae782511-6f32-4123-be76-838584e05b39
source-git-commit: fe70f357e2298f1656d713aae5fae800e6775d64
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 10%

---

# Decisioning sul dispositivo

Le decisioni sul dispositivo consentono di memorizzare nella cache le attività [!DNL Adobe Target] [!UICONTROL A/B Test] e [!UICONTROL Experience Targeting] (XT) sul server ed eseguire le decisioni in memoria a latenza vicina a zero, senza bloccare le richieste di rete sulla rete [!DNL Adobe Target] Edge Network.

Per ulteriori informazioni, consulta [Introduzione alle decisioni sul dispositivo](https://adobetarget-sdks.gitbook.io/docs/on-device-decisioning/introduction-to-on-device-decisioning) nella documentazione *[SDK per Adobe Target](https://adobetarget-sdks.gitbook.io/docs/)*.

## Webinar: Personalizzare e testare a latenza zero con decisioni su dispositivi da [!DNL Adobe Target]

Più che mai, gli esperti di marketing, i proprietari dei prodotti e gli sviluppatori hanno il compito di ottimizzare l’esperienza complessiva del cliente su siti, app e ovunque si connettano con i loro clienti. Gli strumenti multipli con silos di dati e implementazioni complesse sono inadeguati.

In questo webinar registrato, [!DNL Adobe Target] gli esperti di prodotto discutono di come lo spostamento delle decisioni di ottimizzazione dell&#39;esperienza critica sul dispositivo da eseguire localmente con latenza vicina allo zero può aprire le porte a nuovi casi d&#39;uso emozionanti e al contempo migliorare le prestazioni del sito per i clienti.

>[!VIDEO](https://video.tv.adobe.com/v/328148)

## Best practice

Adobe consiglia le seguenti best practice per l’utilizzo delle decisioni su dispositivi:

### Procedure consigliate quando il metodo decisionale è &quot;on-device&quot; {#best-practices-on-device}

Quando utilizzi &quot;on-device&quot; come metodo decisionale, l’artefatto viene scaricato quando il visitatore carica la pagina web per la prima volta. Qualsiasi qualificazione dell’attività che deve verificarsi al primo caricamento della pagina (nessuna cache) viene eseguita solo dopo che l’artefatto è stato completamente scaricato. Puoi seguire alcune best practice per garantire che le qualifiche di attività si verifichino rapidamente per un nuovo visitatore anonimo.

* Disattiva le attività con funzionalità &quot;On-Device&quot; che non sono progettate per essere nell’artefatto.
* Se si dispone di [!DNL Target Premium], è possibile utilizzare [proprietà/aree di lavoro](/help/administrating-target/c-user-management/property-channel/property-channel.md) per creare file di artefatti diversi per diverse aree di lavoro.
* Se i file di artefatto diventano molto grandi a causa di motivi legittimi, è possibile utilizzare il metodo di decisione &quot;ibrido&quot;. Questo metodo ti consente di scaricare l’artefatto in parallelo e tutte le chiamate [!DNL Target] API passano sul filo fino a quando l’artefatto non viene scaricato. Per ulteriori informazioni su questo approccio, leggi la sezione sulle best practice [relative alla modalità decisionale &quot;ibrida&quot;](#best-practices-hybrid) di seguito.
* Se disponi di un’applicazione a pagina singola (SPA), [!DNL Adobe] consiglia di caricare e inizializzare at.js prima di caricare il file JavaScript principale dell’applicazione durante il primo caricamento della pagina. Questo approccio avvia il download degli artefatti molto prima, fornendo un rendering più veloce dell&#39;esperienza.

### Procedure consigliate quando il metodo decisionale è &quot;ibrido&quot; {#best-practices-hybrid}

Quando si utilizza &quot;ibrido&quot; come metodo decisionale, l&#39;artefatto viene scaricato in parallelo. Fino a quando l&#39;artefatto non viene scaricato, tutte le chiamate API [!DNL Target] passano oltre il cavo anche se le &quot;posizioni&quot; sono compatibili con il dispositivo. Questo è il comportamento predefinito per tutte le chiamate `getOffers()` e fornisce le prestazioni migliori nella maggior parte delle situazioni. Se modifichi il comportamento predefinito di `getOffers()` impostando `decisioningMethod` su `on-device`, segui queste best practice per evitare errori e garantire le migliori prestazioni.

* Se decidi di chiamare `getOffers()` con `decisioningMethod` come `on-device` al primo caricamento della pagina, devi farlo all&#39;interno del gestore eventi at.js &quot;ARTIFACT_DOWNLOAD_SUCCEEDED&quot; per evitare errori. Se l’artefatto è molto grande, tutte le &quot;posizioni&quot; che utilizzano questo approccio vengono rese solo dopo che l’artefatto è stato completamente scaricato, il che può ritardare il rendering dell’esperienza. [!DNL Adobe] consiglia di utilizzare raramente questo approccio. Segui le best practice per ridurre la dimensione degli artefatti nella sezione [&quot;On Device&quot; (Sul dispositivo)](#best-practices-on-device) precedente quando utilizzi questo approccio.

## Esercitazione: Decisioni su dispositivi

[!DNL Adobe Target] le decisioni sul dispositivo consentono la distribuzione di contenuti con latenza quasi zero.

Questo video di 7 minuti:

* Descrive le decisioni sul dispositivo, incluso il confronto con altri metodi di implementazione [!DNL Target]
* Mostra come abilitare le decisioni sul dispositivo in [!DNL Target]
* Esamina un esempio di attività del compositore basato su moduli configurata con contenuto JSON
* Mostra un esempio di codice SDK Node.JS contenente la configurazione chiave necessaria per le decisioni su dispositivi
* Mostra i risultati in un browser

>[!VIDEO](https://video.tv.adobe.com/v/329032)

Per ulteriori video ed esercitazioni, consulta la guida [Tutorials Adobe Target](https://experienceleague.adobe.com/docs/target-learn/tutorials/overview.html?lang=it) .

## Adobe Tech Blog - Parte 1: Esegui [!DNL Adobe Target] SDK di NodeJS per la sperimentazione e la personalizzazione sulle piattaforme edge (Akamai Edge Workers)

[Fai clic qui per accedere al post](https://medium.com/adobetech/part-1-run-adobe-target-nodejs-sdk-for-experimentation-and-personalization-on-edge-platforms-4d8660964ed9) del blog.

## Adobe Tech Blog - Parte 2: eseguire l’SDK NodeJS di [!DNL Adobe Target] a scopo di sperimentazione e personalizzazione su piattaforme edge (AWS Lambda@Edge)

[Fai clic qui per accedere al post](https://medium.com/adobetech/part-2-run-adobe-target-nodejs-sdk-for-experimentation-and-personalization-on-edge-platforms-aws-4d6bdac24563) del blog.