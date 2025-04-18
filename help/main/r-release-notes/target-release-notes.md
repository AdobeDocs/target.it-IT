---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease;early access
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di [!DNL Adobe Target].
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione [!DNL Target] ?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 872e56662e04e3fabda7ff38233adfea32efbe48
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 47%

---

# Note sulla versione (prerelease) di [!DNL Target]

Questo articolo contiene informazioni prerelease per le prossime versioni di [!DNL Adobe Target], incluse SDK, API e librerie JavaScript.

**Ultimo aggiornamento: venerdì 17 aprile 2025**

>[!NOTE]
>
>Date di rilascio, funzioni e altre informazioni sono soggette a modifica senza preavviso.
>
>Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle release. I codici tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target Standard/Premium] 25.4.5 (24 aprile 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che causava la visualizzazione di più tipi di pubblico dell’esperienza durante la modifica o il salvataggio di un’attività. (TGT-52134)
* È stato risolto un problema che impediva la visualizzazione dei consigli sul sito Web del cliente dopo l&#39;attivazione dell&#39;attività [!DNL Recommendations]. (TGT-52164)
* `OptionLocalIDs` non incrementa più in modo errato quando l&#39;opzione rimane invariata. (TGT-52187)
* Ora i file di reporting scaricati mostrano correttamente i dati presenti nell’interfaccia utente di reporting. (TGT-52068)
* È stato risolto un problema che impediva a Target di riconoscere il carattere &quot;#&quot; nell’URL di un sito web. (TGT-52093)
* Le operazioni batch non hanno più esito negativo dopo l’aggiunta delle regole di consegna della pagina. (TGT-52097)
* È stato risolto un problema a causa del quale [!DNL Target] eliminava tutti i parametri di query dall&#39;URL del sito Web. (TGT-52100)
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
