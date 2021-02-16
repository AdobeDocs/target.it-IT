---
keywords: note sulla versione;rilasci;aggiornamenti;release futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella prossima release di  Adobe Target, inclusi SDK, API e librerie JavaScript.
title: Quali nuove funzioni sono incluse nella prossima release?
feature: Release Notes
translation-type: tm+mt
source-git-commit: 2d610a91118b2e1c69e23faed2f8b7c411c5b7ea
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 25%

---


# Note sulla versione di Target (prerelease)

Questo articolo contiene informazioni prerelease. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 16 febbraio 2021**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni presenti in queste pagine potrebbero essere le stesse, a seconda della data di rilascio. I codici tra parentesi sono per uso interno di [!DNL Adobe].

>[!IMPORTANT]
>
>**fine ciclo di vita** di mbox.js: Il 31 marzo 2021 non  [!DNL Adobe Target] supporterà più la libreria mbox.js. Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto positivo sulle pagine che hanno attività [!DNL Target] in esecuzione distribuendo contenuti predefiniti.
>
>È consigliabile che tutti i clienti effettuino la migrazione alla versione più recente della nuova [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js prima di tale data, per evitare potenziali problemi con i siti. Per ulteriori informazioni, vedere [Panoramica: implementate Target per Web lato client](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## Target Standard/Premium 21.2.1 (2 marzo 2021)

Questa versione di manutenzione contiene i seguenti miglioramenti, correzioni e modifiche.

I codici tra parentesi sono per uso interno di [!DNL Adobe].

* È stata aumentata la dimensione dell&#39;offerta consentita:

   | Tipo | Limite precedente | Nuovo limite |
   | --- | --- | --- |
   | HTML | 256 KB | 1024 KB |
   | Offerte visive dall&#39;interfaccia utente di Target | 64 KB | 1024 KB per ogni esperienza |
   | Tramite API | 512 KB | 1024 KB |

* È stato risolto un problema che impediva la visualizzazione della dipendenza corrente quando i clienti facevano clic su [!UICONTROL Edit Dependency] nella pagina [!UICONTROL Goals &amp; Settings] di un&#39;attività. (TGT-39340)
* È stato risolto un problema durante l&#39;aggiornamento della [!UICONTROL Libreria Pubblico di un&#39;area di lavoro]. Prima dell&#39;aggiornamento, venivano visualizzati i tipi di pubblico dell&#39;area di lavoro correntemente selezionata. Dopo l&#39;aggiornamento, viene visualizzato l&#39; [!UICONTROL Area di lavoro predefinita] e i relativi tipi di pubblico. L&#39;area di lavoro corrente e i relativi tipi di pubblico ora persistono dopo l&#39;aggiornamento. (TGT-38871)
* È stato risolto un problema che si verificava durante la copia di un&#39;attività [!UICONTROL Recommendations] e successivamente durante la modifica dell&#39;attività originale, modificando la sequenza dei criteri. La modifica nella sequenza di criteri nell&#39;attività originale è stata applicata erroneamente anche all&#39;attività copiata. (TGT-39155)

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
