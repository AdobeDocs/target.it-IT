---
keywords: plug-in at.js;plug-in supportati;plug-in non supportati;ttMeta;ttmeta;mboxTrack
description: Scopri l’implementazione legacy di mbox.js di Adobe Target. Esegui la migrazione a Adobe Experience Platform Web SDK (AEP Web SDK) o all’ultima versione di at.js.
title: Quali plug-in legacy non sono supportati in [!DNL Target] at.js?
feature: at.js
role: Developer
exl-id: 1d858f5b-58dc-4181-9cb5-aa6b22011abc
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 82%

---

# Plug-in at.js

Informazioni sui plug-in at.js supportati e non supportati in Adobe Target.

Molte persone hanno creato plug-in personalizzati e plug-in di risposta per [!DNL mbox.js]. Questi plug-in personalizzati potrebbero non essere supportati da [!DNL at.js] senzau.

Se utilizzi un plug-in che non è presente in questo elenco e desideri conoscerne lo stato, contatta il rappresentante del tuo account.

In questa pagina è indicato lo stato attuale di alcuni dei plug-in utilizzati da molti clienti insieme a [!DNL at.js]:

| Plug-in | Dettagli |
|--- |--- |
| mboxTrack | Non supportato.<br>Questo viene sostituito dalla funzione [adobe.target.trackEvent(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-trackevent.md). Aggiorna i plug-in per applicare la nuova funzione.<br>Consulta la pagina delle [integrazioni](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/target-atjs-integrations.md). |
| Plug-in di backup del profilo persistente | Non supportato.<br>Questo plug-in è stato dichiarato obsoleto quando la durata del profilo di Target è stata estesa da due settimane a 90 giorni. Controlla la data di scadenza del tuo cookie mbox per visualizzare l&#39;impostazione della durata del profilo sul tuo account.<br>Contatta il Client Care se desideri estendere la durata del profilo a 90 giorni. |
| ttMeta | I plug-in obsoleti di SiteCatalyst devono essere disattivati e sostituiti con [Adobe Analytics come origine per la generazione di rapporti per Adobe Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T). Il plug-in ttMeta deve essere disabilitato e sostituito con [Adobe Experience Cloud Debugger](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj). |
