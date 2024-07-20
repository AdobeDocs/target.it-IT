---
keywords: ajo;adobe percorsi optimizer;adobe percorsi optimizer integrazione target;recommendations;target recommendations;integrazione
description: Integra [!DNL Adobe Target Recommendations] con [!DNL Adobe Journey Optimizer].
title: Come si utilizza  [!DNL Target Recommendations]  nei percorsi di clienti utilizzando  [!DNL Adobe Journey Optimizer]?
feature: Integrations
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#beta newtab=true" tooltip="Cosa sono le funzioni beta in [!DNL Adobe Target]."
hide: true
hidefromtoc: true
exl-id: 81bbbd51-47fc-4e23-a1cb-7c18fea1c159
source-git-commit: 36af6518c90ec4e055747d633b7721e5491a8d64
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 1%

---

# Integrare [!DNL Adobe Target Recommendations] e [!DNL Adobe Journey Optimizer]

In questo articolo vengono illustrati casi d&#39;uso e informazioni utili per configurare l&#39;integrazione tra [!DNL Adobe Target Recommendations] e [!DNL Adobe Journey Optimizer] e fornire ai clienti esperienze connesse, contestuali e personalizzate.

Questa integrazione ti aiuta a stimolare più conversioni e a vedere l’impatto dei messaggi e-mail contenenti consigli personalizzati.

## Prerequisiti

Per utilizzare l&#39;integrazione di [!DNL Target Recommendations] e [!DNL Adobe Journey Optimizer], è necessario quanto segue:

* [[!DNL Adobe Target Premium]](/help/main/c-intro/intro.md#premium) implementato utilizzando [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=it){target=_blank}.

  Questa funzione non è disponibile con una licenza [!DNL Target Standard] o quando si implementa [!DNL Target] con at.js o altri SDK [!DNL Target].

* [[!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/docs/journey-optimizer/using/ajo-home.html){target=_blank}.

## Casi d’uso di esempio

Questi sono solo alcuni possibili casi d&#39;uso per l&#39;integrazione di [!DNL Target Recommendations] con [!DNL Adobe Journey Optimizer]:

* **[!DNL Adobe Journey Optimizer]invia un&#39;e-mail personalizzata dopo l&#39;abbandono del carrello**: questo caso d&#39;uso è basato su un cliente che visita un sito Web, inserisce articoli nel carrello e quindi lascia il sito senza completare il processo di acquisto.

  Supponiamo, ad esempio, che un visitatore visiti il sito web di un’azienda di abbigliamento e metta due cappotti invernali e una felpa nel carrello. Il visitatore viene quindi distratto e lascia il sito web o non è sicuro degli acquisti e chiude il browser o l’app.

  Dopo un determinato periodo, forse alcune ore o un giorno, un&#39;azione personalizzata in [!DNL Adobe Journey Optimizer] effettua una chiamata a [!DNL Target Recommendations] per determinare il contenuto del carrello abbandonato utilizzando un algoritmo di [consigli basati su carrello](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md). [!DNL Adobe Journey Optimizer] invia quindi al visitatore un&#39;e-mail personalizzata per ricordare che il processo di acquisto non è stato completato, insieme a immagini e collegamenti agli elementi abbandonati.

* **[!DNL Adobe Journey Optimizer]invia un&#39;e-mail in blocco dopo le visite al sito per ricordare ai visitatori quali elementi sono stati visualizzati**: questo caso d&#39;uso si basa sui visitatori che visitano un sito Web, visualizzano vari elementi e quindi lasciano il sito o l&#39;app senza inserire elementi nel carrello.

  Dopo un periodo specificato, un&#39;azione personalizzata in [!DNL Adobe Journey Optimizer] effettua una chiamata a [!DNL Target Recommendations] per determinare gli elementi visualizzati da ogni visitatore, utilizzando il [!DNL Adobe Experience Cloud Identifier] (EDID) di ogni visitatore, il profilo [!DNL Target] del visitatore e un algoritmo [basato sull&#39;utente](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md). [!DNL Adobe Journey Optimizer] invia quindi a ogni membro del pubblico qualificato un&#39;e-mail personalizzata con immagini e collegamenti agli elementi visualizzati di ogni visitatore, in modo da invitare il visitatore a tornare e a effettuare un acquisto.

  In questo scenario, l&#39;identificatore [!UICONTROL Experience Cloud Visitor ID] (ECID) e il contenuto del profilo [!DNL Target] di ciascun visitatore vengono utilizzati per generare il consiglio in base all&#39;algoritmo visualizzato di recente.

  Supponiamo ad esempio che un visitatore visiti un sito web per la vendita al dettaglio e visualizzi diversi orologi. Il profilo [!DNL Target] del visitatore è stato aggiornato con un elenco degli orologi visualizzati. Utilizzando ECID e il profilo [!DNL Target] del visitatore, [!DNL Target] invia il consiglio a [!DNL Adobe Journey Optimizer]. [!DNL Adobe Journey Optimizer] invia quindi un messaggio e-mail contenente immagini e collegamenti agli orologi visualizzati dal visitatore, utilizzando l&#39;algoritmo visualizzato di recente. Un altro visitatore riceve un’e-mail personalizzata contenente immagini e collegamenti agli elementi visualizzati dal visitatore. Ogni messaggio e-mail è personalizzato per ogni visitatore.

* **[!DNL Adobe Journey Optimizer]invia un&#39;e-mail in blocco a visitatori qualificati dopo la visita del sito per suggerire elementi popolari**: questo caso d&#39;uso si basa sulla visita di un visitatore a un sito Web, ma non sulla visualizzazione di elementi particolari. L’e-mail viene inviata in blocco a tutti coloro che sono idonei per un particolare pubblico, ad esempio:

  Supponiamo che il visitatore non visualizzi alcun orologio particolare. Forse il visitatore ha semplicemente fatto clic intorno al sito e ha visualizzato pagine di categorie o post di blog. Di conseguenza, il profilo [!DNL Target] non contiene informazioni specifiche sugli elementi visualizzati di recente. In questa situazione, [!DNL Target Recommendations] utilizza un [consiglio di backup](/help/main/c-recommendations/c-algorithms/backup-recs.md) in modo che [!DNL Adobe Journey Optimizer] possa inviare un&#39;e-mail con immagini e collegamenti agli elementi più popolari sul sito Web per richiedere al visitatore di tornare e di effettuare eventualmente un acquisto.
