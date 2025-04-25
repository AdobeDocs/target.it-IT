---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease;early access
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di [!DNL Adobe Target].
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione [!DNL Target] ?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 24cbccca7ac76dd77668abf0b4498ab4fd374893
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 29%

---

# Note sulla versione (prerelease) di [!DNL Target]

Questo articolo contiene informazioni prerelease per le prossime versioni di [!DNL Adobe Target], incluse SDK, API e librerie JavaScript.

**Ultimo aggiornamento: venerdì 24 aprile 2025**

>[!NOTE]
>
>Date di rilascio, funzioni e altre informazioni sono soggette a modifica senza preavviso.
>
>Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle release. I codici tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target Standard/Premium] 25.4.5 (25 aprile 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che causava discrepanze nelle inserzioni del pubblico tra la pagina delle impostazioni [!UICONTROL Activity] e la pagina della panoramica [!UICONTROL Reporting]. (TGT-52203)
* È stato risolto un problema che impediva l’aggiunta di una nuova pagina a un’attività a causa di un errore di input dell’utente non valido. (TGT-52263)
* È stato risolto un problema che impediva la visualizzazione dei consigli sul sito Web del cliente dopo l&#39;attivazione dell&#39;attività [!DNL Recommendations]. (TGT-52164)
* È stato risolto un problema che causava l&#39;incremento errato di `OptionLocalIDs` quando l&#39;opzione rimaneva invariata. (TGT-52187)
* È stato risolto un problema a causa del quale i file di reporting scaricati mostravano correttamente i dati presenti nell’interfaccia utente di reporting. (TGT-52068)
* È stato risolto un problema che impediva il corretto funzionamento delle operazioni batch dopo l’aggiunta delle regole di consegna della pagina. (TGT-52097)
* È stato risolto un problema a causa del quale [!DNL Target] eliminava tutti i parametri di query dall&#39;URL del sito Web. (TGT-52100)
* È stato risolto un errore della console che impediva ai clienti di creare attività sia nell’interfaccia utente di Target legacy che aggiornata. (TGT-52181)
* È stato risolto un problema che impediva ai clienti di aggiungere nuove pagine, causando un errore di input dell’utente non valido. (TGT-52258)
* È stato risolto un problema che causava la scomparsa delle modifiche dopo l&#39;aggiunta di ulteriori pagine e il ritorno alla scheda [!UICONTROL Experiences]. (TGT-52264)
* È stato risolto un problema che impediva ai clienti di modificare il pubblico in un&#39;attività [!UICONTROL Experience Targeting] (XT). (TGT-52191)
* È stato corretto un errore che impediva la modifica di un’attività XT a causa di una regola dell’interfaccia utente non supportata. (TGT-52273)
* È stato risolto un problema che impediva la visualizzazione delle modifiche delle attività nell&#39;interfaccia utente [!DNL Target], nonostante il corretto recapito alla pagina Web. (TGT-52192)
* È stato risolto un problema nel [!UICONTROL Visual Experience Composer] (VEC) aggiornato a causa del quale le breadcrumb non venivano sempre visualizzate nella parte inferiore dell’editor, causando difficoltà nella selezione precisa degli elementi. (TGT-51169)
* È stato risolto un problema che impediva all&#39;elenco a discesa [!UICONTROL Audience] di visualizzare tutti i tipi di pubblico a causa dell&#39;impaginazione. (TGT-52204)
* È stato risolto un problema che causava un messaggio di input utente non valido durante l&#39;aggiunta di nuove offerte nelle attività [!UICONTROL Automated Personalization] (AP). (TGT-52210)
* È stato risolto un problema a causa del quale [!UICONTROL Analytics for Target] (A4T) veniva erroneamente selezionato come origine per la generazione di rapporti, anche se il cliente non aveva accesso ad A4T. (TGT-52226)
* È stato risolto un problema che impediva il salvataggio di un&#39;attività con la metrica URL [!UICONTROL View a Page]. (TGT-52260)
* È stato risolto un problema che impediva ai clienti di selezionare aree di lavoro durante la creazione di offerte all’interno di un’attività. (TGT-52289)
* È stato risolto un problema che causava la visualizzazione errata delle modifiche da un’esperienza quando si passava a un’altra. (TGT-52184)
* È stato risolto un problema che impediva la corretta visualizzazione dell&#39;offerta predefinita nell&#39;interfaccia utente [!DNL Target] all&#39;apertura dell&#39;attività. (TGT-52198)

## [!DNL Target Standard/Premium] 25.4.5 (25 aprile 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che impediva a [!DNL Target] di riconoscere il carattere &quot;#&quot; nell&#39;URL di un sito Web. (TGT-52093)
* È stato risolto un problema che impediva la cancellazione dei tipi di pubblico e la modifica dei tipi di pubblico combinati nell&#39;interfaccia utente aggiornata per le attività [!UICONTROL Automated Personalization] (AP). (TGT-52149)
* È stato risolto un problema che causava l’inversione dei perfezionamenti del pubblico e dei tipi di pubblico dell’attività nell’interfaccia utente aggiornata. (TGT-52158)

## Aggiornamento delle autorizzazioni di Target (22 aprile 2025)

Questo aggiornamento futuro migliora il controllo dell&#39;organizzazione sulle configurazioni delle istanze [!DNL Target], impedendo aggiornamenti accidentali che potrebbero influire sulla distribuzione delle attività tra i vari team di test e personalizzazione.

A decorrere dal 22 aprile 2025, solo gli amministratori [!UICONTROL Product] e [!UICONTROL Solutions] potranno aggiornare le impostazioni nelle sezioni [!UICONTROL Administration], indipendentemente dai loro ruoli nelle aree di lavoro [!DNL Target]. Gli utenti senza questa autorizzazione avranno accesso in sola lettura alle sezioni [!UICONTROL Administration].

Per ulteriori informazioni, vedere [Amministrare Target](/help/main/administrating-target/start-target.md).

## Note aggiuntive e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js di [!DNL Adobe Target]. |

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
