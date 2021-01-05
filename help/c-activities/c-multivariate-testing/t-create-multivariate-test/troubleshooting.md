---
keywords: Multivariate Tests;troubleshoot;troubleshooting;mvt
description: Questo argomento contiene suggerimenti per la risoluzione di alcuni problemi che potrebbero verificarsi durante la progettazione di un test MVT in  Adobe Target.
title: Risolvere i problemi relativi ai test multivariati
feature: Multivariate Tests
translation-type: tm+mt
source-git-commit: 4adade56529fb95e4400e06d04d3c6c69e120edc
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 45%

---


# Risolvere i problemi relativi ai test multivariati

Questo argomento contiene suggerimenti per la risoluzione di alcuni problemi che possono verificarsi durante la progettazione di un test [!UICONTROL multivariato] (MVT) in [!DNL Adobe Target].

* Quando modificate un&#39;attività, se avete utilizzato metriche basate su [!DNL Analytics] e la suite di rapporti non viene caricata (viene visualizzato lo spinner), passate alle metriche [!DNL Target] e quindi tornate alla metrica basata su [!DNL Analytics]. In questo modo sarà possibile caricare la suite di rapporti.
* Se apportate modifiche a un test già in esecuzione, potreste ripristinare il test e i relativi dati.

   [!DNL Target] consente di modificare un&#39;attività live. È importante considerare che la modifica di un’attività in corso potrebbe ripristinare il test, quindi i rapporti potrebbero non riconoscere alcune delle modifiche.

   Puoi apportare piccoli cambiamenti, ad esempio modificare le offerte di testo o HTML esistenti.

   Le azioni specifiche che ripristinano i nomi e i rapporti relativi alle esperienze sono:

   * Aggiunta di una nuova posizione
   * Eliminazione di una posizione
   * Aggiunta di nuove offerte o eliminazione di offerte da una posizione esistente

