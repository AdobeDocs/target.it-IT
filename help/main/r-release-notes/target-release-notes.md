---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di [!DNL Adobe Target].
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione [!DNL Target] ?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: f326a689420e4d351aba20eec665fdd8cd721139
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 68%

---

# Note sulla versione (prerelease) di [!DNL Target]

Questo articolo contiene informazioni prerelease per le prossime versioni di [!DNL Adobe Target], incluse SDK, API e librerie JavaScript.

**Ultimo aggiornamento: 19 maggio 2023**

>[!NOTE]
>
>Date di rilascio, funzioni e altre informazioni sono soggette a modifica senza preavviso.
>
>Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle release. I codici tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target] Standard/Premium 23.5.1 (23-25 maggio 2023)

Questa versione sarà disponibile in base al seguente programma scaglionato:

23 maggio: area geografica Europa, Medio Oriente e Africa (EMEA) 24 maggio: area geografica Asia-Pacifico (APAC) 25 maggio: area geografica delle Americhe

Questa versione include le nuove funzioni, i miglioramenti e le correzioni seguenti:

| Funzione | Dettagli |
|--- |--- |
| Attributi di profilo Real-Time CDP condivisi con [!DNL Target] | Gli [!UICONTROL attributi di profilo Real-Time CDP] possono essere condivisi con [!DNL Target] per l’utilizzo nelle offerte HTML e JSON.<P>Per ulteriori informazioni, consulta [Condividere gli attributi di profilo Real-Time CDP con [!DNL Target]](/help/main/c-integrating-target-with-mac/integrating-with-rtcdp.md#rtcdp-profile-attributes). |

* È stato risolto un problema che impediva ad alcuni clienti di creare tipi di pubblico con profili di visitatori utilizzando operatori &quot;maggiore di&quot; o &quot;minore di&quot;. (TGT-45271)

## [!DNL Target] Standard/Premium 23.5.2 (31 maggio 2023)

Questa versione include i miglioramenti e le correzioni seguenti:

* È stato risolto un problema che causava la visualizzazione di una pagina vuota durante la generazione di un token di autorizzazione API profilo. (TGT-45387)
* È stato risolto un problema che impediva la visualizzazione di un’immagine in [!UICONTROL Crea design] se il nome dell’immagine contiene GB 18030 caratteri. (TGT-44614)
* È stato risolto un problema che causava la generazione di rapporti per [!UICONTROL Personalizzazione automatica] attività da congelare durante l’analisi. (TGT-44820)

## [!DNL Target] Standard/Premium 23.5.3 (data da definire)

Questo rilascio contiene i seguenti miglioramenti:

| Funzione | Dettagli |
|--- |--- |
| [!UICONTROL Modalità di controllo qualità] per [!UICONTROL Automated Personalization] attività | [!DNL Adobe Target] [!UICONTROL Modalità di controllo qualità] è ora disponibile per [!UICONTROL Automated Personalization] attività, sostituzione [!UICONTROL Collegamenti di anteprima] funzionalità.<P>Per ulteriori informazioni, consulta [Controllo qualità delle attività](/help/main/c-activities/c-activity-qa/activity-qa.md). |

* Miglioramenti delle prestazioni per non consentire la duplicazione delle funzionalità (inclusa la riduzione del tempo di caricamento) durante [gestione delle esclusioni](/help/main/c-activities/t-automated-personalization/managing-exclusions.md#concept_4EF78013F80E48EFA024AE0274C9F037) in [!UICONTROL Automated Personalization] attività.

## Note aggiuntive e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js di [!DNL Adobe Target]. |

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
