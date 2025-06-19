---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease;early access
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di [!DNL Adobe Target].
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione [!DNL Target] ?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: b1bde455f686c34e7a5184868ce63db0b74e2af7
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 29%

---

# Note sulla versione (prerelease) di [!DNL Target]

Questo articolo contiene informazioni prerelease per le prossime versioni di [!DNL Adobe Target], incluse SDK, API e librerie JavaScript.

**Ultimo aggiornamento: 19 giugno 2025**

>[!NOTE]
>
>* Date di rilascio, funzioni e altre informazioni sono soggette a modifica senza preavviso.
>
>* Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md).
>
>* I codici tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target Standard/Premium] 25.6.3 (sabato 20 giugno 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* Opzione [!UICONTROL Rearrange] aggiunta all&#39;interfaccia utente [!UICONTROL Visual Experience Composer] (VEC) aggiornata per allinearla alle funzionalità disponibili nel Compositore esperienza visivo legacy. (TGT-46957)
* È stato risolto un problema a causa del quale la copia di un’attività da un’area di lavoro a un’altra causava errori quali &quot;non deve essere null&quot; o &quot;Si è verificato un errore&quot;. (TGT-52474)
* È stato risolto un problema che impediva la generazione di rapporti [!UICONTROL Automated Segments] e [!UICONTROL Important Attributes] per alcune attività. (TNT-52904)
* È stato risolto un problema nel Compositore esperienza visivo aggiornato a causa del quale la gestione del contenuto predefinito nelle attività di [!UICONTROL Automated Personalization] (AP) non corrispondeva all&#39;interfaccia utente legacy. Il sistema ora aggiunge automaticamente un `optionGroup` predefinito denominato &quot;Contenuto predefinito&quot; con `optionGroupLocalId = 0` quando nessun gruppo viene aggiunto in modo esplicito. Questo gruppo include l&#39;opzione predefinita, ad esempio `optionLocalId: 0`. Se il contenuto predefinito viene rimosso, viene rimosso anche il gruppo di opzioni corrispondente. (TGT-52651)
* È stato risolto un problema nelle attività [!UICONTROL Multivariate Test] (MVT) a causa del quale il riutilizzo di un `experienceLocalId` da esperienze precedentemente rimosse non era consentito correttamente. (TNT-52672)
* È stato risolto un problema che impediva agli URL nei percorsi di attività di visualizzare i parametri di query a causa di caratteri non validi, ad esempio barre (/). (TNT52845)
* È stato migliorato il messaggio di errore di convalida per gli aggiornamenti dell&#39;attività [!DNL A/B Test] tramite l&#39;API di back-end. Quando sono presenti nomi di posizione duplicati, il messaggio ora indica chiaramente: &quot;I nomi duplicati non sono consentiti&quot; per `locations.selectors`. (TGT-52589)
* È stato corretto un errore che si verificava durante l&#39;aggiornamento di un&#39;attività live [!UICONTROL Recommendations] a causa di una proprietà non riconosciuta nel payload della richiesta. Il sistema ora gestisce correttamente il codice JSON &quot;Non valido&quot;. Errore &quot;Nome proprietà non riconosciuto&quot;. (TNT52723)
* È stato corretto un errore di convalida del back-end che causava un errore &quot;400 Bad Request&quot; durante il salvataggio di un&#39;attività [!UICONTROL Recommendations]. (TNT-52716)
* È stato risolto un problema in [!UICONTROL Form-Based Experience Composer] a causa del quale il passaggio del mouse su una mbox con caratteri speciali nel menu a discesa [!UICONTROL Location] causava la visualizzazione di un valore vuoto dell&#39;editor e causava l&#39;attivazione di un messaggio di tipo &quot;Impossibile eseguire &#39;querySelector&#39; su &#39;Element&#39;.&quot; errore. (TGT-52717)
* È stata migliorata la precisione dello stato di avanzamento con un nuovo indicatore &quot;PARTIALLY_IMPORTED&quot;. In precedenza, i feed venivano contrassegnati come &quot;riusciti&quot; anche quando non venivano importate tutte le righe di un file, il che era fuorviante.
* È stato corretto un errore a causa del quale, dopo la migrazione ad AP V2, alcune chiamate API a `/admin/rest/ui/v1/campaigns` restituivano errori lato client (HTTP 4xx). (TGT-52721)

## Note aggiuntive e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK]&#x200B;(https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js di [!DNL Adobe Target]. |

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
