---
keywords: Test multivariati;risoluzione dei problemi;risoluzione dei problemi;mvt
description: Esplora le potenziali sfide che potresti affrontare durante l’utilizzo di [!UICONTROL Test multivariato] (MVT) attività in [!DNL Adobe Target], insieme alle soluzioni suggerite.
title: Come posso risolvere i problemi di un [!UICONTROL Test multivariato]?
feature: Multivariate Tests
exl-id: 93bb8446-06af-4466-9824-7099c1080059
source-git-commit: 6c00224e814abb33cdf968a249bd36fb2e5ed2ed
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 21%

---

# Risoluzione dei problemi [!UICONTROL Test multivariato] attività

Questo articolo contiene suggerimenti per la risoluzione di alcuni problemi che potrebbero verificarsi durante la progettazione di un [!UICONTROL Test multivariato] (MVT) in [!DNL Adobe Target].

* Quando modifichi un’attività, se utilizzi [!DNL Analytics]basate su metriche e la suite di rapporti non si carica (viene visualizzato il numero di rotazioni), imposta le metriche su [!DNL Target] e quindi passare di nuovo a [!DNL Analytics]metrica basata su. In questo modo sarà possibile caricare la suite di rapporti.
* Se apporti modifiche a un test già in esecuzione, puoi reimpostare il test e i relativi dati.

  [!DNL Target] consente di modificare un’attività live. La modifica di un’attività in corso potrebbe reimpostare il test, pertanto i rapporti potrebbero non riconoscere alcune delle modifiche.

  Puoi apportare piccoli cambiamenti, ad esempio modificare le offerte di testo o HTML esistenti.

  Le azioni specifiche che reimpostano i nomi delle esperienze e i rapporti includono:

   * Aggiunta di una nuova posizione
   * Eliminazione di una posizione
   * Aggiunta di nuove offerte o eliminazione di offerte da una posizione esistente
