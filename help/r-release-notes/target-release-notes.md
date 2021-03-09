---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella prossima versione di Adobe Target, inclusi SDK, API e librerie JavaScript.
title: Quali nuove funzioni saranno incluse nella prossima versione?
feature: Note sulla versione
translation-type: tm+mt
source-git-commit: 801a2717615a1f0ff2ce306cda59f68cc5c4a8f8
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 21%

---


# Note sulla versione di Target (prerelease)

Questo articolo contiene informazioni prerelease. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 1 marzo 2021**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere le stesse, a seconda della data di rilascio delle versioni. I codici tra parentesi sono per uso interno di [!DNL Adobe].

>[!IMPORTANT]
>
>**Terminazione di mbox.js**: Il 31 marzo 2021 non  [!DNL Adobe Target] supporterà più la libreria mbox.js . Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto positivo sulle pagine che hanno [!DNL Target] attività in esecuzione servendo il contenuto predefinito.
>
>L’Adobe consiglia a tutti i clienti di eseguire la migrazione alla versione più recente della nuova [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js prima di tale data, per evitare potenziali problemi con i siti. Per ulteriori informazioni, consulta [Panoramica: implementare Target per web lato client](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## Target Standard/Premium 21.2.1 (9 marzo 2021)

Questa versione di manutenzione contiene i miglioramenti, le correzioni e le modifiche seguenti.

I codici tra parentesi sono per uso interno di [!DNL Adobe].

* È stata aumentata la dimensione dell’offerta consentita (TGT-38304):

   | Tipo | Limite precedente | Nuovo limite |
   | --- | --- | --- |
   | HTML | 256 KB | 1024 KB |
   | Offerte visive dall’interfaccia utente di Target | 64 KB | 1024 KB per ogni esperienza |
   | Tramite API | 512 KB | 1024 KB |

* [!UICONTROL I rapporti ] Approfondimenti personalizzazione per le attività di  [!UICONTROL Targeting automatico]  (AT) e  [!UICONTROL Automated Personalization]  (AP) ora vengono prodotti su base giornaliera. Puoi scegliere un rapporto che fornisce [!UICONTROL Segmenti automatizzati] o [!UICONTROL Attributi importanti] per gli ultimi 15, 30 e 60 giorni. Le opzioni di 45 e 90 giorni sono state rimosse per consentire l’esecuzione giornaliera delle altre impostazioni dell’intervallo di lookback. (TGT-39472)
* È stato risolto un problema che impediva la visualizzazione della dipendenza corrente quando i clienti fanno clic su [!UICONTROL Modifica dipendenza] nella pagina [!UICONTROL Obiettivi e impostazioni] di un&#39;attività. (TGT-39340)
* È stato risolto un problema che si verificava durante l&#39;aggiornamento della [!UICONTROL Libreria pubblico] di un&#39;area di lavoro. Prima dell’aggiornamento, vengono visualizzati i tipi di pubblico per l’area di lavoro attualmente selezionata. Dopo l&#39;aggiornamento, vengono visualizzati il [!UICONTROL Area di lavoro predefinita] e i relativi tipi di pubblico. L’area di lavoro corrente e i relativi tipi di pubblico ora persistono dopo l’aggiornamento. (TGT-38871)
* È stato risolto un problema che si verificava durante la copia di un&#39;attività [!UICONTROL Recommendations] e in seguito durante la modifica dell&#39;attività originale modificando la sequenza di criteri. La modifica nella sequenza di criteri nell’attività originale è stata applicata in modo errato anche all’attività copiata. (TGT-39155)
* È stato risolto un problema che causava la visualizzazione di un numero errato di prodotti per le esclusioni [!UICONTROL Recommendations]. (TGT-39599)

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
