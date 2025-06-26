---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease;early access
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di [!DNL Adobe Target].
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione [!DNL Target] ?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 926a045e5bcebc8d094ea41a6c1b7c59568a35ab
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 27%

---

# Note sulla versione (prerelease) di [!DNL Target]

Questo articolo contiene informazioni prerelease per le prossime versioni di [!DNL Adobe Target], incluse SDK, API e librerie JavaScript.

**Ultimo aggiornamento: 26 giugno 2025**

>[!NOTE]
>
>* Date di rilascio, funzioni e altre informazioni sono soggette a modifica senza preavviso.
>
>* Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md).
>
>* I codici tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target Standard/Premium] 25.6.4 (venerdì 26 giugno 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* Opzione [!UICONTROL Rearrange] aggiunta all&#39;interfaccia utente [!UICONTROL Visual Experience Composer] (VEC) aggiornata per allinearla alle funzionalità disponibili nel Compositore esperienza visivo legacy. (TGT-46957 e TGT-52876)
* È stato risolto un problema che impediva il mantenimento delle modifiche apportate alle esperienze di varianti (ad esempio, Esperienza B) in un&#39;attività [!UICONTROL A/B Test]. Dopo il passaggio da un’esperienza all’altra, le modifiche apportate alla variante scompaiono. Questo problema non ha influito sull’esperienza di controllo. (TGT-52664)
* È stato risolto un problema che impediva ad alcuni clienti di creare o salvare attività, mentre altri potevano eseguire le stesse azioni senza alcun problema. Il problema era incoerente tra gli account.(TGT-52842)
* È stato risolto un problema che impediva agli utenti del Compositore esperienza visivo aggiornato di spostare le modifiche a [!UICONTROL Page Load event], una funzionalità già presente nell&#39;interfaccia utente legacy. (TGT-52617)
* È stato risolto un problema che impediva la corretta visualizzazione di alcune modifiche dell’attività nel Compositore esperienza visivo aggiornato. (TGT-52818)
* È stata corretta un&#39;eccezione Null Pointer che si verificava durante il recupero dei dati di reporting per le attività di [!UICONTROL Automated Personalization] (AP). (TGT-52362)
* È stato risolto un problema che impediva la visualizzazione dei dettagli a livello di offerta nel file .CSV per le attività [!UICONTROL Automated Personalization] (AP). (TGT-52675)
* È stato risolto un problema che si verificava durante l’applicazione di modifiche nel Compositore esperienza visivo aggiornato, a causa del quale le modifiche inizialmente venivano visualizzate correttamente, incluso il [!UICONTROL Experience Fragment] previsto. Tuttavia, quando si passa da un’esperienza all’altra o si apportano ulteriori modifiche, alcune modifiche non vengono applicate a causa di problemi del selettore. (TGT-52679)
* È stato risolto un problema a causa del quale, quando veniva creata una nuova attività clonandone una esistente, i collegamenti di controllo qualità nell’attività clonata mantenevano erroneamente gli URL della pagina dall’attività originale. (TGT-52775)
* È stato risolto un problema che impediva involontariamente a [!UICONTROL On-device Decisioning] di essere disponibile nel Compositore esperienza visivo aggiornato. (TGT-52371)
* È stato risolto un problema che impediva la modifica di un&#39;attività di prodotto [!DNL Recommendations]. Quando si tenta di accedere al Compositore esperienza visivo tramite l’interfaccia utente di Target, nella pagina [!UICONTROL Overview] viene visualizzato un errore che impedisce eventuali modifiche. (TGT-52823)
* È stato risolto un problema che impediva il salvataggio di un&#39;attività [!DNL Recommendations] quando i nomi delle esperienze superavano i 50 caratteri. (TGT-52619)
* È stato risolto un problema che impediva ai clienti di salvare un’attività Consigli dopo la modifica dei criteri nella nuova interfaccia utente. Il problema sembra essere relativo alle autorizzazioni e non influisce su tutti gli utenti con ruoli simili. (TGT-52816)
* È stato risolto un problema che impediva agli utenti con la mansione [!UICONTROL Editor] di modificare un&#39;attività [!DNL Recommendations]. Il tentativo di modificare la progettazione e salvare l&#39;attività ha restituito un errore 403 Forbidden, che indica che il privilegio &quot;[editor]&quot; era obbligatorio, anche se l&#39;utente aveva già quel ruolo nell&#39;area di lavoro pertinente. (TGT-52836)

## Note aggiuntive e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK]&#x200B;(https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js di [!DNL Adobe Target]. |

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
