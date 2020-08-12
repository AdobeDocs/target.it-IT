---
keywords: at.js plugins;supported plugins;unsupported plugins;ttMeta;ttmeta;mboxTrack
description: Informazioni sui plug-in at.js supportati e non supportati per Adobe Target.
title: Plug-in at.js per Adobe Target
feature: null
topic: Standard
uuid: ef36b2b2-bf6d-497e-b3f5-2b572a1b8a8d
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 97%

---


# Plug-in at.js{#at-js-plug-ins}

Informazioni sui plug-in at.js supportati e non supportati in Adobe Target.

Molte persone hanno creato plug-in personalizzati e plug-in di risposta per [!DNL mbox.js]. Questi plug-in personalizzati potrebbero non essere supportati da [!DNL at.js] senzau.

Se utilizzi un plug-in che non è presente in questo elenco e desideri conoscerne lo stato, contatta il rappresentante del tuo account.

In questa pagina è indicato lo stato attuale di alcuni dei plug-in utilizzati da molti clienti insieme a [!DNL at.js]:

| Plug-in | Dettagli |
|--- |--- |
| mboxTrack | Non supportato.<br>Questo viene sostituito dalla funzione [adobe.target.trackEvent(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-trackevent.md). Aggiorna i plug-in per applicare la nuova funzione.<br>Consulta la pagina delle [integrazioni](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/target-atjs-integrations.md). |
| Plug-in di backup del profilo persistente | Non supportato.<br>Questo plug-in è stato dichiarato obsoleto quando la durata del profilo di Target è stata estesa da due settimane a 90 giorni. Controlla la data di scadenza del tuo cookie mbox per visualizzare l&#39;impostazione della durata del profilo sul tuo account.<br>Contatta il Client Care se desideri estendere la durata del profilo a 90 giorni. |
| ttMeta | I plug-in obsoleti di SiteCatalyst devono essere disattivati e sostituiti con [Adobe Analytics come origine per la generazione di rapporti per Adobe Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T). Il plug-in ttMeta deve essere disabilitato e sostituito con [Adobe Experience Cloud Debugger](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj). |