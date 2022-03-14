---
keywords: implementare;implementazione;configurazione;configurazione;fornitori di dati
description: Inserire dati in [!DNL Target] utilizzo di provider di dati.
title: Come inserire i dati in [!DNL Target] Utilizzo di Fornitori di dati?
feature: Implementation
role: Developer
exl-id: 05fe9190-4d36-43e2-9fc7-c354a6821bfb
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 67%

---

# Fornitori di dati

I provider di dati sono una funzionalità che ti consente di trasmettere facilmente dati da terze parti a [!DNL Adobe Target].

Nota: I provider di dati richiedono at.js 1.3 o versione successiva.

## Formato

L&#39;impostazione `window.targetGlobalSettings.dataProviders` è un array dei fornitori di dati.

Per ulteriori informazioni sulla struttura di ciascun fornitore di dati, vedi [Fornitori di dati](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers).

## Esempi di casi d’uso

Un esempio di terza parte potrebbe essere un servizio meteo, un DMP o persino il tuo servizio web. Puoi utilizzare questi dati per generare tipi di pubblico e contenuti mirati e per arricchire il profilo del visitatore.

## Vantaggi del metodo

Questa impostazione consente ai clienti di raccogliere dati da fornitori di dati terzi, come Demandbase, BlueKai e servizi personalizzati, e di passare i dati a Target come parametri mbox nella richiesta globale di mbox.

Supporta la raccolta di dati da più provider tramite richieste sincrone e asincrone.

L&#39;utilizzo di questo approccio semplifica la gestione della visualizzazione momentanea del contenuto della pagina predefinito, inclusi i timeout indipendenti per ogni provider per limitare l&#39;impatto sulle prestazioni della pagina.

## Avvertenze

Se i fornitori di dati hanno aggiunto a `window.targetGlobalSettings.dataProviders` sono asincroni, vengono eseguiti in parallelo. La richiesta API del visitatore viene eseguita in parallelo con le funzioni aggiunte a `window.targetGlobalSettings.dataProviders` per consentire un tempo minimo di attesa.

at.js non cerca di memorizzare i dati nella cache. Se il fornitore di dati recupera i dati una sola volta, deve assicurarsi che i dati siano memorizzati nella cache e, quando viene invocata la funzione di fornitore di dati, deve servire i dati della cache per la seconda invocazione.

## Esempi di codice

Diversi esempi sono disponibili in [Fornitori di dati](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers).

## Link a informazioni rilevanti

Documentazione: [Fornitori di dati](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers)

## Video di formazione:

* [Utilizzo di Fornitori di dati in Adobe Target](https://helpx.adobe.com/it/target/kt/using/dataProviders-atjs-feature-video-use.html)
* [Implementazione di Fornitori di dati in Adobe Target](https://helpx.adobe.com/it/target/kt/using/dataProviders-atjs-technical-video-implement.html)
