---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease;early access
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di [!DNL Target].
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione [!DNL Target] ?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 65bc050a189b65af57b1258afeff497a0dafcfb5
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 44%

---

# Note sulla versione (prerelease) di [!DNL Target]

Questo articolo contiene informazioni prerelease per le prossime versioni di [!DNL Adobe Target], incluse SDK, API e librerie JavaScript.

**Ultimo aggiornamento: 21 agosto 2025**

>[!NOTE]
>
>* Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso. Le informazioni contenute in questo articolo vengono aggiornate frequentemente, soprattutto prima delle versioni di.
>
>* Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md).
>
>* I codici tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target Standard/Premium] 25.8.4 (28 agosto 2025)

Questa versione include i seguenti aggiornamenti e correzioni:

**[!DNL Recommendations]**

+++Vedi i dettagli
**L&#39;interfaccia utente è stata aggiornata in modo che il filtro di ricerca avanzato in [!UICONTROL Product Catalog Search] non distingua tra maiuscole e minuscole**: l&#39;interfaccia utente [!UICONTROL Advanced Search] nella pagina [!UICONTROL Product Catalog Search] ha eseguito in precedenza la corrispondenza esatta tra maiuscole e minuscole sui valori restituiti, anche se sia la query di back-end che la query GraphQL non distinguevano tra maiuscole e minuscole. Questa incoerenza ha causato confusione e ridotto l’accuratezza della ricerca. Il filtro [!UICONTROL Advanced Search] non distingue tra maiuscole e minuscole, in quanto si allinea al comportamento del back-end e migliora l&#39;usabilità.

+++

**[!UICONTROL Visual Experience Composer (VEC)]**

+++Vedi i dettagli
* **È stato risolto un problema che impediva la persistenza della ridenominazione di una posizione in un&#39;attività [!UICONTROL Automated Personalization] (AP) o [!UICONTROL Multivariate Test] (MVT) dopo essere passati al passaggio [!UICONTROL Targeting] e aver restituito.** I clienti ora possono modificare e salvare correttamente i nomi delle posizioni e le modifiche rimangono visibili durante il processo di creazione attività. (TGT-52367)

+++

## Note aggiuntive e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK]&#x200B;(https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js di [!DNL Adobe Target]. |

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
