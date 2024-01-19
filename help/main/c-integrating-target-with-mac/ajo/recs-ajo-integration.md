---
keywords: ajo;adobe percorsi optimizer;adobe percorsi optimizer integrazione target;recommendations;target recommendations;integrazione
description: Utilizzare [!DNL Adobe Target Recommendations] con [!DNL Adobe Journey Optimizer].
title: Come si utilizza [!DNL Target Recommendations] nei percorsi di clienti utilizzando [!DNL Adobe Journey Optimizer]?
feature: Integrations
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#beta newtab=true" tooltip="Cosa sono le funzioni beta in [!DNL Adobe Target]."
hide: true
hidefromtoc: true
source-git-commit: bb6c83ff393656a634e1e8ddcb02b14dc8d4c8d2
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 3%

---

# [!DNL Adobe Target Recommendations] e [!DNL Adobe Journey Optimizer] integrazione

Questo articolo spiega casi d’uso e informazioni utili per configurare l’integrazione tra [!DNL Adobe Target Recommendation] e [!DNL Adobe Journey Optimizer] per aiutarti a fornire ai tuoi clienti esperienze connesse, contestuali e personalizzate.

## Prerequisiti

Per utilizzare [!DNL Target Recommendations] e [!DNL Adobe Journey Optimizer] integrazione, è necessario disporre dei seguenti elementi:

* [[!DNL Adobe Target Premium]](/help/main/c-intro/intro.md#premium) implementato utilizzando [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=it){target=_blank}.

  La funzione non è disponibile con [!DNL Target Standard] licenza o quando si implementa [!DNL Target] con at.js o altro [!DNL Target] SDK.

* [[!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/docs/journey-optimizer/using/ajo-home.html){target=_blank}.

## Casi d’uso di esempio

Di seguito sono riportati solo due possibili casi di utilizzo per l’integrazione [!DNL Target Recommendations] con [!DNL Adobe Journey Optimizer]:

* **[!DNL Customer Journey Optimizer]invia un’e-mail personalizzata dopo l’abbandono del carrello**: questo caso d’uso si basa sulla visita di un cliente a un sito web, sul posizionamento di articoli nel carrello e sulla successiva uscita dal sito senza completare il processo di acquisto.

  Supponiamo, ad esempio, che un visitatore visiti il sito web di un’azienda di abbigliamento e metta due cappotti invernali e una felpa nel carrello. Il visitatore viene quindi distratto e lascia il sito web o non è sicuro degli acquisti e chiude il browser o l’app.

  Dopo un determinato periodo di tempo, forse alcune ore o un giorno, un’azione personalizzata in [!DNL Adobe Journey Optimizer] effettua una chiamata a [!DNL Target Recommendations] per determinare il contenuto del carrello abbandonato. [!DNL Adobe Journey Optimizer] invia quindi al visitatore un’e-mail personalizzata per ricordargli che il processo di acquisto non è stato completato, insieme a immagini e collegamenti agli elementi abbandonati.

* **[!DNL Customer Journey Optimizer]invia un’e-mail dopo la visita del sito utilizzando il profilo utente**: questo caso d’uso si basa sulla visita di un cliente a un sito web, la visualizzazione di vari elementi e l’uscita dal sito senza inserire elementi nel carrello.

  Dopo un periodo di tempo specificato, un’azione personalizzata in [!DNL Adobe Journey Optimizer] effettua una chiamata a [!DNL Target Recommendations] per determinare quali elementi ha visualizzato il visitatore utilizzando [!DNL Adobe Experience Cloud Identifier] (EDID) [!DNL Adobe Journey Optimizer] invia quindi al visitatore un’e-mail personalizzata per ricordargli che il processo di acquisto non è stato completato, insieme a immagini e collegamenti agli elementi abbandonati.

