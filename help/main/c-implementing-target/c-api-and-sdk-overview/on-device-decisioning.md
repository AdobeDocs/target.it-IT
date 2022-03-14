---
keywords: lato server;lato server;sdk;sdk;on-device;decisioning;sul dispositivo;ondevice;latenza zero;latenza;vicino a zero;node.js
description: Scopri come utilizzare le decisioni sul dispositivo per memorizzare in cache il tuo [!DNL Target] Attività A/B e MVT sul server per eseguire decisioni in memoria a latenza quasi zero.
title: Cos’è On-Device Decisioning?
feature: Implement Server-side
role: Developer
exl-id: ae782511-6f32-4123-be76-838584e05b39
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '693'
ht-degree: 10%

---

# Decisioning sul dispositivo

Le decisioni sul dispositivo consentono di memorizzare nella cache [!DNL Adobe Target] [!UICONTROL Test A/B] e [!UICONTROL Targeting esperienza] (XT) attività sul server ed esegui decisioni in memoria a latenza vicina a zero, senza bloccare le richieste di rete al [!DNL Adobe Target] Rete Edge.

Per ulteriori informazioni, consulta [Introduzione alle decisioni sul dispositivo](https://adobetarget-sdks.gitbook.io/docs/on-device-decisioning/introduction-to-on-device-decisioning) in *[Documentazione degli SDK per Adobe Target](https://adobetarget-sdks.gitbook.io/docs/)*.

## Webinar: personalizzare e testare a latenza zero con decisioni su dispositivi da [!DNL Adobe Target]

Più che mai, gli esperti di marketing, i proprietari dei prodotti e gli sviluppatori hanno il compito di ottimizzare l’esperienza complessiva del cliente su siti, app e ovunque si connettano con i loro clienti. Gli strumenti multipli con silos di dati e implementazioni complesse sono inadeguati.

In questo webinar registrato, [!DNL Adobe Target] gli esperti di prodotto illustrano in che modo le decisioni di ottimizzazione dell’esperienza critica sul dispositivo da eseguire localmente con latenza vicina allo zero possono aprire le porte a nuovi casi d’uso emozionanti, migliorando al contempo le prestazioni del sito per i clienti.

>[!VIDEO](https://video.tv.adobe.com/v/328148)

## Best practice

Adobe consiglia le seguenti best practice per l’utilizzo delle decisioni su dispositivi:

### Procedure consigliate quando il metodo decisionale è &quot;on-device&quot; {#best-practices-on-device}

Quando utilizzi &quot;on-device&quot; come metodo decisionale, l’artefatto viene scaricato quando il visitatore carica la pagina web per la prima volta. Qualsiasi qualificazione dell’attività che deve verificarsi al primo caricamento della pagina (nessuna cache) viene eseguita solo dopo che l’artefatto è stato completamente scaricato. Puoi seguire alcune best practice per garantire che le qualifiche di attività si verifichino rapidamente per un nuovo visitatore anonimo.

* Disattiva le attività con funzionalità &quot;On-Device&quot; che non sono progettate per essere nell’artefatto.
* Se [!DNL Target Premium], puoi utilizzare [proprietà/aree di lavoro](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) creare file di artefatti diversi per aree di lavoro diverse.
* Se i file di artefatto diventano molto grandi a causa di motivi legittimi, è possibile utilizzare il metodo di decisione &quot;ibrido&quot;. Questo metodo consente di scaricare l&#39;artefatto in parallelo e tutto [!DNL Target] Le chiamate API passano oltre il collegamento fino a quando l&#39;artefatto non viene scaricato. Leggi il meglio [sezione sulle pratiche in modalità decisionale &quot;ibrida&quot;](#best-practices-hybrid) di seguito per ulteriori informazioni su questo approccio.
* Se si dispone di un&#39;applicazione a pagina singola (SPA), [!DNL Adobe] consiglia di caricare e inizializzare at.js prima di caricare il file JavaScript principale dell&#39;applicazione durante il primo caricamento della pagina. Questo approccio avvia il download degli artefatti molto prima, fornendo un rendering più veloce dell&#39;esperienza.

### Procedure consigliate quando il metodo decisionale è &quot;ibrido&quot; {#best-practices-hybrid}

Quando si utilizza &quot;ibrido&quot; come metodo decisionale, l&#39;artefatto viene scaricato in parallelo. Fino al download dell&#39;artefatto, qualsiasi [!DNL Target] Le chiamate API passano oltre il cavo anche se le &quot;posizioni&quot; sono compatibili con il dispositivo. Questo comportamento è il predefinito per tutti `getOffers()` effettua le chiamate e fornisce le prestazioni migliori nella maggior parte delle situazioni. Se si modifica il comportamento predefinito di `getOffers()` impostando `decisioningMethod` a `on-device`, segui queste best practice per evitare errori e garantire le migliori prestazioni.

* Se decidi di chiamare `getOffers()` con `decisioningMethod` come `on-device` quando la pagina viene caricata per la prima volta, è necessario farlo all’interno del gestore eventi at.js &quot;ARTIFACT_DOWNLOAD_SUCCEEDED&quot; per evitare errori. Se l’artefatto è molto grande, tutte le &quot;posizioni&quot; che utilizzano questo approccio vengono rese solo dopo che l’artefatto è stato completamente scaricato, il che può ritardare il rendering dell’esperienza. [!DNL Adobe] consiglia di utilizzare raramente questo approccio. Segui le best practice per ridurre le dimensioni degli artefatti nella sezione [Sezione sulle best practice per dispositivi mobili](#best-practices-on-device) quando si utilizza questo approccio.

## Esercitazione: Decisioni su dispositivi

[!DNL Adobe Target] le decisioni sul dispositivo consentono la distribuzione di contenuti con latenza quasi zero.

Questo video di 7 minuti:

* Descrive le decisioni sul dispositivo, incluso il confronto con altri metodi di [!DNL Target] implementazione
* Mostra come abilitare le decisioni sul dispositivo in [!DNL Target]
* Esamina un esempio di attività del compositore basato su moduli configurata con contenuto JSON
* Mostra un esempio di codice SDK Node.JS contenente la configurazione chiave necessaria per le decisioni su dispositivi
* Mostra i risultati in un browser

>[!VIDEO](https://video.tv.adobe.com/v/329032)

Per ulteriori video ed esercitazioni, consulta la sezione [Tutorials Adobe Target](https://experienceleague.adobe.com/docs/target-learn/tutorials/overview.html?lang=it) guida.

## Adobe Tech Blog - Parte 1: Esegui [!DNL Adobe Target] SDK di NodeJS per la sperimentazione e la personalizzazione sulle piattaforme edge (Akamai Edge Workers)

[Fai clic qui per accedere al post del blog](https://medium.com/adobetech/part-1-run-adobe-target-nodejs-sdk-for-experimentation-and-personalization-on-edge-platforms-4d8660964ed9).

## Adobe Tech Blog - Parte 2: eseguire l’SDK NodeJS di [!DNL Adobe Target] a scopo di sperimentazione e personalizzazione su piattaforme edge (AWS Lambda@Edge)

[Fai clic qui per accedere al post del blog](https://medium.com/adobetech/part-2-run-adobe-target-nodejs-sdk-for-experimentation-and-personalization-on-edge-platforms-aws-4d6bdac24563).