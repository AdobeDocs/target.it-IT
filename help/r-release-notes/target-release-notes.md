---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella prossima versione di Adobe Target, inclusi SDK, API e librerie JavaScript.
title: Quali nuove funzioni saranno incluse nella prossima versione?
feature: Note sulla versione
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
translation-type: tm+mt
source-git-commit: dba3044c94502ea9e25b21a3034dc581de10f431
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 20%

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

Questa versione contiene le nuove funzioni e i miglioramenti seguenti. I codici tra parentesi sono per uso interno di [!DNL Adobe].

| Funzione | Dettagli |
| --- | --- |
| Supporto delle decisioni su dispositivi per at.js | Le decisioni sul dispositivo consentono agli addetti al marketing e agli sviluppatori di distribuire esperimenti e personalizzazioni sul browser di un utente con latenza vicina allo zero.<br>Per ulteriori informazioni, consulta Decisioni  [sul dispositivo per at.js.](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md)<br>(Data da comunicare) |
| ![Operatori basati su ](/help/assets/premium.png) PremiumList per le regole di filtro entità | [!DNL Target Recommendations] supporta nuovi operatori basati su elenco per le regole di filtro entità. (TGT-39234)<br>Gli operatori appena aggiunti includono:<br><ul><li>È Contenuto Nell’Elenco</li><li>Non è contenuto nell’elenco</li><li>Elenco Contiene Un Elemento In</li><li>L&#39;Elenco Non Contiene Un Elemento In</li><li>Elenco Contiene Tutti Gli Elementi In</li><li>Elenco Non Contiene Tutti Gli Elementi</li></ul>Per ulteriori informazioni, consulta &quot;Operatori disponibili&quot; in [Utilizzare regole di inclusione dinamiche e statiche](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#operators). |

Questa versione contiene le seguenti correzioni.

* È stato risolto un problema che impediva la sincronizzazione di un&#39;attività dopo la modifica del pubblico in [!UICONTROL Tutti i visitatori]. (TGT-40259)
* È stato risolto un problema che impediva la duplicazione delle offerte quando vengono utilizzate in posizioni diverse nelle attività [!UICONTROL Automated Personalization] anche se l&#39;opzione [!UICONTROL Non consentire duplicati] è abilitata. (TGT-39567)
* È stato risolto un problema che impediva il caricamento corretto della pagina [!UICONTROL Amministrazione] > [!UICONTROL Configurazione Scene7] . (TGT-39918)
* È stato risolto un problema che causava il mapping delle proprietà all&#39;area di lavoro errata. (TGT-39869)
* È stato risolto un problema che causava un caricamento infinito se la richiesta non riusciva dopo la modifica dell’ambiente durante la creazione di un’esclusione consigli. (TGT-39948)

## at.js versione 2.5.0 (data da annunciare)

Questa versione di at.js include i miglioramenti e le modifiche seguenti:

* [Supporto ](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md) decisionale su dispositivo per at.js.
* [Supporto dei ](/help/c-activities/c-activity-qa/activity-qa.md) collegamenti di anteprima per le attività di Automated Personalization

Questa versione rimuove anche il supporto per Microsoft Internet Explorer 10 e versioni successive.

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
