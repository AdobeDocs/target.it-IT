---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease;early access
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di [!DNL Adobe Target].
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione [!DNL Target] ?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 7e23eea48abdebd60f37ad1bf453813a63779d33
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 28%

---

# Note sulla versione (prerelease) di [!DNL Target]

Questo articolo contiene informazioni prerelease per le prossime versioni di [!DNL Adobe Target], incluse SDK, API e librerie JavaScript.

**Ultimo aggiornamento: venerdì 10 aprile 2025**

>[!NOTE]
>
>Date di rilascio, funzioni e altre informazioni sono soggette a modifica senza preavviso.
>
>Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle release. I codici tra parentesi sono per uso interno di [!DNL Adobe].

## Aggiornamento delle autorizzazioni di Target (22 aprile 2025)

Questo aggiornamento futuro migliora il controllo dell&#39;organizzazione sulle configurazioni delle istanze [!DNL Target], impedendo aggiornamenti accidentali che potrebbero influire sulla distribuzione delle attività tra i vari team di test e personalizzazione.

A decorrere dal 22 aprile 2025, solo gli amministratori [!UICONTROL Product] e [!UICONTROL Solutions] potranno aggiornare le impostazioni nelle sezioni [!UICONTROL Administration], indipendentemente dai loro ruoli nelle aree di lavoro [!DNL Target]. Gli utenti senza questa autorizzazione avranno accesso in sola lettura alle sezioni [!UICONTROL Administration].

Per ulteriori informazioni, vedere [Amministrare Target](/help/main/administrating-target/start-target.md).

## [!DNL Target Standard/Premium] 25.4.4 (15 aprile 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato aggiunto un messaggio di errore per guidare gli utenti nella risoluzione delle opzioni duplicate in un’attività. (TGT-51927)
* È stato risolto un problema che impediva la rimozione dei selettori ClickTrack durante l&#39;eliminazione di pagine o esperienze con offerte di reindirizzamento. (TGT-51952)
* È stato risolto un problema che impediva a [!DNL Target] di rilevare correttamente un carattere &quot;#&quot; nell&#39;URL attività. (TGT-52093)
* È stato risolto un problema a causa del quale le definizioni dei tipi di pubblico non erano visibili durante la modifica del targeting a livello di offerta nelle attività [!UICONTROL Automated Personalization] (AP). (TGT-52148)
* È stato risolto un problema a causa del quale i perfezionamenti del pubblico e i tipi di pubblico di targeting delle attività venivano invertiti nell’interfaccia utente. (TGT-52158)

## [!DNL Target Standard/Premium] 25.4.3 (10 aprile 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato corretto un errore che impediva ai clienti di aprire il pop-up di informazioni sul pubblico per alcune attività [!UICONTROL Experience Targeting] (XT). (TGT-52049)
* È stato risolto un problema che impediva ai clienti di inserire un [!UICONTROL Experience Fragment] nell&#39;area di lavoro predefinita. (TGT-52073)
* È stato risolto un problema che causava la visualizzazione di un&#39;offerta come &quot;Contenuto non trovato&quot; e non sulla pagina [!UICONTROL Offers] per un&#39;attività [!UICONTROL Automated Personalization] (AP). (TGT-52150)
* È stata aggiunta la possibilità di consentire la duplicazione dei tipi di pubblico all’interno di un’attività. (TGT-51200)
* È stato risolto un problema che causava la visualizzazione del nome mbox errato nella pagina [!UICONTROL Goals & Settings] per un&#39;attività XT dopo la modifica. (TGT-52026)
* È stato risolto un problema che causava la visualizzazione di `defaultContent` nelle opzioni nonostante non fosse in `experiences/optionLocations`. (TGT-52036)
* È stato risolto un problema per garantire che le stringhe vuote non vengano convertite in valori Null. (TGT-52037)
* È stato risolto un problema che richiedeva ai clienti di riconfigurare [!UICONTROL Optimization Goal] in [!UICONTROL Reporting Settings] nella pagina [!UICONTROL Goals & Settings] dopo le modifiche. (TGT-52071)
* È stato risolto un problema a causa del quale un&#39;attività senza regole di consegna pagina visualizzava più regole sulla pagina [!UICONTROL Overview]. (TGT-52084)
* È stato aggiunto un messaggio di errore per gli utenti che tentano di salvare un’offerta con caratteri al di fuori del piano multilingue di base, ad esempio emoji. (TGT-52105)
* È stato risolto un problema a causa del quale l’apertura di un’attività attivava il messaggio di errore: &quot;Questa attività utilizza uno o più tipi di pubblico eliminati alla sorgente&quot;. (TGT-52120)
* È stato risolto un problema che impediva la visualizzazione delle metriche ClickTrack nel Compositore esperienza visivo [!UICONTROL Visual Experience Composer] aggiornato durante la modifica. (TGT-52152)
* È stato risolto un problema a causa del quale un URL con un parametro di query come posizione dell&#39;attività non visualizzava il parametro di query nella pagina [!UICONTROL Overview] dell&#39;attività. (TGT-51635)
* È stato risolto un problema che impediva la visualizzazione dell&#39;intero URL dell&#39;esperienza in [!UICONTROL Browse mode] all&#39;interno del [!UICONTROL Visual Experience Composer] (VEC). (TGT-52101)
* È stato risolto un problema a causa del quale la modifica di un’attività causava l’aggiunta di &quot;/&quot; alla fine dell’URL da parte della consegna della pagina, che ne causava l’invalidità. (TGT-52114)
* È stato risolto un problema che causava il reindirizzamento errato del collegamento [!UICONTROL Activity QA] nella home page di [!UICONTROL Form-Based Experience Composer] alla home page di [!DNL Adobe Experience Cloud]. (TGT-52055)
* È stato risolto un problema che impediva il mantenimento delle pagine aggiuntive aggiunte all&#39;attività [!UICONTROL A/B Test] dopo il salvataggio e la riapertura. (TGT-51994)
* È stato risolto un problema che impediva ai clienti di eliminare gli stili nella sezione stile in linea. (TGT-52070)
* È stato ripristinato l&#39;accesso alle [schede di definizione del pubblico](/help/main/c-target/c-audiences/audiences.md#section_11B9C4A777E14D36BA1E925021945780) nella finestra di dialogo [!UICONTROL Activity QA], in modo simile all&#39;interfaccia utente legacy. (TGT-52056)
* L’interfaccia utente aggiornata non salvava pagine o tipi di pubblico senza modifiche. Se i clienti hanno aggiunto nuove pagine o tipi di pubblico a un&#39;attività ma non vi apportano modifiche, [!DNL Target] ha eliminato i tipi di pubblico non modificati al momento del salvataggio. Le notifiche sono state aggiunte in posizioni rilevanti per informare gli utenti di questo comportamento. (TGT-52104)

## Note aggiuntive e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js di [!DNL Adobe Target]. |

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
