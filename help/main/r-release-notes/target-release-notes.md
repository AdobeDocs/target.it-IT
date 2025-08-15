---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease;early access
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di [!DNL Target].
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione [!DNL Target] ?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 1f8fa78c2b88e179f021128a8fd3dac177dfa3dd
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 37%

---

# Note sulla versione (prerelease) di [!DNL Target]

Questo articolo contiene informazioni prerelease per le prossime versioni di [!DNL Adobe Target], incluse SDK, API e librerie JavaScript.

**Ultimo aggiornamento: 15 agosto 2025**

>[!NOTE]
>
>* Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso. Le informazioni contenute in questo articolo vengono aggiornate frequentemente, soprattutto prima delle versioni di.
>
>* Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md).
>
>* I codici tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target Standard/Premium] 25.8.3 (21 agosto 2025)

Questa versione include i seguenti aggiornamenti e correzioni:

**Raccomandazioni**

+++Vedi i dettagli
* **È stato risolto un problema nell&#39;interfaccia utente di Recs a causa del quale il download del file CSV dei criteri personalizzati restituiva l&#39;errore 404**: è stato risolto un problema che impediva ai clienti di scaricare il file CSV dei criteri personalizzati nel processo di creazione delle attività.
* **È stato corretto il caricamento incoerente delle immagini in[!UICONTROL Catalog Search]**: è stato risolto un problema che impediva il caricamento coerente delle miniature e delle immagini in [!UICONTROL &#x200B; Catalog Search] nel processo di creazione attività. Le immagini non venivano visualizzate a meno che la colonna &quot;URL miniatura&quot; non fosse visibile e alcune immagini di prodotto venivano caricate parzialmente o non completamente dopo le azioni di navigazione o ricerca. (TGT-52778)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++Vedi i dettagli
* **È stato risolto un problema nel processo di creazione attività che bloccava la progressione al passaggio [!UICONTROL Targeting] nelle attività di Personalizzazione automatizzata**: è stato risolto un problema nel processo di creazione attività a causa del quale i clienti non potevano procedere al passaggio [!UICONTROL Targeting] nelle attività [!UICONTROL Automated Personalization] (Personalizzazione automatizzata) a meno che non fossero state aggiunte due posizioni. Questo comportamento era diverso dall’esperienza precedente, in cui era sufficiente una singola posizione con più offerte. Il requisito è stato corretto, consentendo ai clienti di continuare a utilizzare le impostazioni per una singola posizione come parte dei flussi di lavoro di Personalizzazione automatizzata. (TGT-53426)

+++

## Note aggiuntive e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK]&#x200B;(https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js di [!DNL Adobe Target]. |

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
