---
keywords: ajo;adobe percorsi optimizer;adobe percorsi optimizer integrazione target;recommendations;target recommendations;integrazione
description: Integrare [!DNL Adobe Target Recommendations] con [!DNL Adobe Journey Optimizer].
title: Come si utilizza [!DNL Target Recommendations] nei percorsi di clienti utilizzando [!DNL Adobe Journey Optimizer]?
feature: Integrations
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#beta newtab=true" tooltip="Cosa sono le funzioni beta in [!DNL Adobe Target]."
hide: true
hidefromtoc: true
source-git-commit: ce74c85380333476b97f47fab4d2659a3c9c86e1
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 1%

---

# Integrare [!DNL Adobe Target Recommendations] e [!DNL Adobe Journey Optimizer]

Questo articolo spiega casi d’uso e informazioni utili per configurare l’integrazione tra [!DNL Adobe Target Recommendations] e [!DNL Adobe Journey Optimizer] per aiutarti a fornire ai tuoi clienti esperienze connesse, contestuali e personalizzate.

Questa integrazione ti aiuta a stimolare più conversioni e a vedere l’impatto dei messaggi e-mail contenenti consigli personalizzati.

## Prerequisiti

Per utilizzare [!DNL Target Recommendations] e [!DNL Adobe Journey Optimizer] integrazione, è necessario disporre dei seguenti elementi:

* [[!DNL Adobe Target Premium]](/help/main/c-intro/intro.md#premium) implementato utilizzando [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=it){target=_blank}.

  Questa funzione non è disponibile con [!DNL Target Standard] licenza o quando si implementa [!DNL Target] con at.js o altro [!DNL Target] SDK.

* [[!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/docs/journey-optimizer/using/ajo-home.html){target=_blank}.

## Casi d’uso di esempio

Questi sono solo alcuni possibili casi d&#39;uso per l&#39;integrazione [!DNL Target Recommendations] con [!DNL Adobe Journey Optimizer]:

* **[!DNL Adobe Journey Optimizer]invia un’e-mail personalizzata dopo l’abbandono del carrello**: questo caso d’uso si basa sulla visita di un cliente a un sito web, sul posizionamento di articoli nel carrello e sulla successiva uscita dal sito senza completare il processo di acquisto.

  Supponiamo, ad esempio, che un visitatore visiti il sito web di un’azienda di abbigliamento e metta due cappotti invernali e una felpa nel carrello. Il visitatore viene quindi distratto e lascia il sito web o non è sicuro degli acquisti e chiude il browser o l’app.

  Dopo un determinato periodo, forse alcune ore o un giorno, un’azione personalizzata in [!DNL Adobe Journey Optimizer] effettua una chiamata a [!DNL Target Recommendations] per determinare il contenuto del carrello abbandonato utilizzando un [consigli basati su carrello](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md) algoritmo. [!DNL Adobe Journey Optimizer] invia quindi al visitatore un’e-mail personalizzata per ricordargli che il processo di acquisto non è stato completato, insieme a immagini e collegamenti agli elementi abbandonati.

* **[!DNL Adobe Journey Optimizer]invia un messaggio e-mail in blocco dopo le visite al sito per ricordare ai visitatori quali elementi sono stati visualizzati**: questo caso d’uso si basa sui visitatori che visitano un sito web, visualizzano vari elementi e poi abbandonano il sito o l’app senza inserire elementi nel carrello.

  Dopo un periodo specificato, un’azione personalizzata in [!DNL Adobe Journey Optimizer] effettua una chiamata a [!DNL Target Recommendations] per determinare gli elementi visualizzati da ogni visitatore, utilizzando [!DNL Adobe Experience Cloud Identifier] (EDID), del [!DNL Target] e un [basato su utente](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md) algoritmo. [!DNL Adobe Journey Optimizer] invia quindi a ogni membro del pubblico qualificato un’e-mail personalizzata con immagini e collegamenti agli elementi visualizzati di ogni visitatore, per invitarlo a tornare indietro e a effettuare un acquisto.

  In questo scenario, il [!UICONTROL ID visitatore Experience Cloud] (ECID) e il contenuto di ogni [!DNL Target] Il profilo viene utilizzato per generare il consiglio in base all’algoritmo visualizzato di recente.

  Supponiamo ad esempio che un visitatore visiti un sito web per la vendita al dettaglio e visualizzi diversi orologi. Di questo visitatore [!DNL Target] Il profilo viene aggiornato con un elenco degli orologi visualizzati. Utilizzo dell’ECID e del [!DNL Target] profilo, [!DNL Target] invia il consiglio a [!DNL Adobe Journey Optimizer]. [!DNL Adobe Journey Optimizer] invia quindi un messaggio e-mail contenente immagini e collegamenti agli orologi visualizzati dal visitatore, utilizzando l’algoritmo visualizzato di recente. Un altro visitatore riceve un’e-mail personalizzata contenente immagini e collegamenti agli elementi visualizzati dal visitatore. Ogni messaggio e-mail è personalizzato per ogni visitatore.

* **[!DNL Adobe Journey Optimizer]invia un’e-mail in blocco ai visitatori qualificati dopo la visita del sito per suggerire gli elementi più popolari**: questo caso d’uso si basa sulla visita di un visitatore a un sito web, ma non sulla visualizzazione di alcun elemento particolare. L’e-mail viene inviata in blocco a tutti coloro che sono idonei per un particolare pubblico, ad esempio:

  Supponiamo che il visitatore non visualizzi alcun orologio particolare. Forse il visitatore ha semplicemente fatto clic intorno al sito e ha visualizzato pagine di categorie o post di blog. Di conseguenza, il [!DNL Target] Il profilo non contiene informazioni specifiche sugli elementi visualizzati di recente. In questa situazione, [!DNL Target Recommendations] utilizza un [consiglio di backup](/help/main/c-recommendations/c-algorithms/backup-recs.md) in modo che [!DNL Adobe Journey Optimizer] può inviare un’e-mail con immagini e collegamenti agli articoli più popolari sul sito web per invitare il visitatore a tornare ed eventualmente effettuare un acquisto.


