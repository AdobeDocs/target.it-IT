---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di Adobe Target.
title: Quali nuove funzioni saranno incluse nella prossima versione?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 5a5b39db9b9b4ffd95573d643dcff52fe562c0c2
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 41%

---

# Note sulla versione di Target (prerelease)

Questo articolo contiene informazioni di pre-release. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 14 settembre 2021**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle versioni. I codici tra parentesi sono per uso interno di [!DNL Adobe].

>[!IMPORTANT]
>
>**Termine del ciclo di vita di mbox.js**: a partire dal 31 marzo 2021, [!DNL Adobe Target] non supporta più la libreria mbox.js. Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto sulle pagine che hanno attività [!DNL Target] in esecuzione, che presenteranno il contenuto predefinito.
>
>Per evitare potenziali problemi con i siti, effettua la migrazione alla versione più recente del nuovo [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js. Per ulteriori informazioni, consulta [Panoramica: implementare Target per web lato client](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## [!DNL Target Standard/Premium] 21.9.1 (14 settembre 2021)

Questa versione di manutenzione include i seguenti miglioramenti, correzioni e modifiche.

* Sono stati risolti dei problemi che impedivano ai clienti di accedere al [!UICONTROL Compositore esperienza visivo] (VEC) a causa di nuovi criteri di sicurezza per i cookie di terze parti in alcuni browser web. Questo problema è stato discusso in &quot;Pagine non caricate nel Compositore esperienza visivo o Compositore esperienza avanzato (EEC) quando si utilizza Google Chrome versione 80+&quot; in [Risoluzione dei problemi relativi al Compositore esperienza visivo e al Compositore esperienza avanzato](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md).
* È stato risolto un problema a causa del quale i nomi delle offerte nel Compositore esperienza visivo visualizzavano il percorso dell’offerta invece del nome descrittivo dell’offerta. (TGT-41300)
* I nomi delle esperienze ora si riflettono in [!DNL Analysis Workspace] per le attività A4T (TGT-38674)
* È stato risolto un problema in [!DNL Recommendations] a causa del quale l’ID entità veniva erroneamente applicato a una promozione in un’attività duplicata all’attività originale. (TGT-41482)
* È stato risolto un problema che impediva la corretta visualizzazione del pulsante &quot;Modifica criteri&quot; nella pagina [!UICONTROL Esperienze] per le attività [!DNL Recommendations] nel Compositore esperienza visivo. (TGT-39512)
* È stato risolto un problema che impediva la sincronizzazione delle attività quando venivano duplicate e copiate in un’area di lavoro di test. (TGT-40686)
* È stato risolto un problema che impediva modifiche a un selettore con [frammenti esperienza](/help/c-experiences/c-manage-content/aem-experience-fragments.md) quando si utilizzava &quot;[!UICONTROL Inserisci dopo]&quot; nel Compositore esperienza visivo. (TGT-41802)
* È stato risolto un problema che impediva l’invio al backend di contenuto JSON vuoto in un’offerta. [!DNL Target] ora invia l’oggetto JSON anche se è vuoto. (TGT-41555)
* È stato risolto un problema che causava l&#39;apertura del reporting precedente [!DNL Analytics] invece di [!DNL Analysis Workspace] quando i clienti facevano clic su &quot;[!UICONTROL Visualizza in Analytics]&quot; durante la visualizzazione di un rapporto. (TGT-41867)
* Sono stati aggiunti ulteriori chiarimenti al messaggio dell’interfaccia utente visualizzato quando un cliente tenta di selezionare [!DNL Analytics] come origine per la generazione di rapporti (A4T) per un’attività [!UICONTROL Automated Personalization]. Il messaggio indica che &quot;[!DNL Target] è l&#39;unica origine supportata per le attività [!UICONTROL Automated Personalization].&quot; (TGT-41954)
* È stato aggiunto un ulteriore chiarimento al messaggio di errore quando i clienti tentano di separare gli host con &quot;nuova riga&quot; invece delle virgole. (TGT-40671)
* È stato risolto un problema che causava alcune date di &quot;[!UICONTROL Ultimo aggiornamento]&quot; delle attività diverse dall&#39;interfaccia utente inglese per i clienti spagnoli e giapponesi (quando visualizzavano l&#39;interfaccia utente in spagnolo e giapponese). (TGT-38980)

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
