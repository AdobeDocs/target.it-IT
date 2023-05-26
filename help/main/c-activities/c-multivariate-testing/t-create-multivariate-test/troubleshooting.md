---
keywords: Test multivariati;risoluzione dei problemi;risoluzione dei problemi;mvt
description: Esplora le potenziali sfide che potresti affrontare durante l’utilizzo delle attività di Test multivariato (MVT) in Adobe Target, insieme alle soluzioni suggerite.
title: Come posso risolvere i problemi relativi ai test multivariati?
feature: Multivariate Tests
exl-id: 93bb8446-06af-4466-9824-7099c1080059
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 42%

---

# Risolvere i problemi relativi ai test multivariati

Questo argomento contiene suggerimenti per la risoluzione di alcuni problemi che potrebbero verificarsi durante la progettazione di un [!UICONTROL Multivariato] (MVT) test in [!DNL Adobe Target].

* Quando modifichi un’attività, se utilizzi [!DNL Analytics]basate su metriche e la suite di rapporti non si carica (viene visualizzato il numero di rotazioni), imposta le metriche su [!DNL Target] e quindi passare di nuovo a [!DNL Analytics]metrica basata su. In questo modo sarà possibile caricare la suite di rapporti.
* Se apporti modifiche a un test già in esecuzione, puoi reimpostare il test e i relativi dati.

   [!DNL Target] consente di modificare un’attività live. È importante considerare che la modifica di un’attività in corso potrebbe ripristinare il test, quindi i rapporti potrebbero non riconoscere alcune delle modifiche.

   Puoi apportare piccoli cambiamenti, ad esempio modificare le offerte di testo o HTML esistenti.

   Le azioni specifiche che ripristinano i nomi e i rapporti relativi alle esperienze sono:

   * Aggiunta di una nuova posizione
   * Eliminazione di una posizione
   * Aggiunta di nuove offerte o eliminazione di offerte da una posizione esistente
