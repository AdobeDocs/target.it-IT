---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella prossima versione di Adobe Target, inclusi SDK, API e librerie JavaScript.
title: Quali nuove funzioni saranno incluse nella prossima versione?
feature: Note sulla versione
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
translation-type: tm+mt
source-git-commit: 2e678fa8a4826f6bfdaef1a04b89b8da7de48d12
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 22%

---

# Note sulla versione di Target (prerelease)

Questo articolo contiene informazioni prerelease. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 16 aprile 2021**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere le stesse, a seconda della data di rilascio delle versioni. I codici tra parentesi sono per uso interno di [!DNL Adobe].

>[!IMPORTANT]
>
>**Terminazione di mbox.js**: A partire dal 31 marzo 2021,  [!DNL Adobe Target] non supporta più la libreria mbox.js . Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js hanno esito negativo e hanno un impatto positivo sulle pagine che hanno [!DNL Target] attività in esecuzione servendo il contenuto predefinito.
>
>Per evitare potenziali problemi con i siti, effettua la migrazione alla versione più recente della nuova [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js. Per ulteriori informazioni, consulta [Panoramica: implementare Target per web lato client](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## Target Standard/Premium 21.4.1 (19 aprile 2021)

Questa versione contiene le seguenti nuove funzioni. I codici tra parentesi sono per uso interno di [!DNL Adobe].

| Funzione | Dettagli |
| --- | --- |
| Supporto delle decisioni su dispositivi per at.js | Le decisioni sul dispositivo consentono agli addetti al marketing e agli sviluppatori di distribuire esperimenti e personalizzazioni sul browser di un utente con latenza vicina allo zero. |

Questa versione contiene i miglioramenti, le correzioni e le modifiche seguenti.

* È stato risolto un problema che impediva la sincronizzazione di un&#39;attività dopo la modifica del pubblico in [!UICONTROL Tutti i visitatori]. (TGT-40259)
* È stato risolto un problema che impediva la duplicazione delle offerte quando vengono utilizzate in posizioni diverse nelle attività [!UICONTROL Automated Personalization] anche se l&#39;opzione [!UICONTROL Non consentire duplicati] è abilitata. (TGT-39567)
* È stato risolto un problema che impediva il caricamento corretto della pagina [!UICONTROL Amministrazione] > [!UICONTROL Configurazione Scene7] . (TGT-39918)
* È stato risolto un problema che causava il mapping delle proprietà all&#39;area di lavoro errata. (TGT-39869)
* [!DNL Target Recommendations] supporta nuovi operatori basati su elenco per le regole di filtro entità. (TGT-39234)

   Gli operatori appena aggiunti includono:

   * È Contenuto Nell’Elenco
   * Non è contenuto nell’elenco
   * Elenco Contiene Un Elemento In
   * L&#39;Elenco Non Contiene Un Elemento In
   * Elenco Contiene Tutti Gli Elementi In
   * Elenco Non Contiene Tutti Gli Elementi

* È stato risolto un problema che causava un caricamento infinito se la richiesta non riusciva dopo la modifica dell’ambiente durante la creazione di un’esclusione consigli. (TGT-39948)

## at.js versione 2.5.0 (19 aprile 2021)

Questa versione di at.js include i seguenti miglioramenti:

* Supporto delle decisioni su dispositivi per at.js
* Supporto dei collegamenti di anteprima per le attività di Automated Personalization

Questa versione rimuove anche il supporto per Microsoft Internet Explorer 10 e versioni successive.

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
