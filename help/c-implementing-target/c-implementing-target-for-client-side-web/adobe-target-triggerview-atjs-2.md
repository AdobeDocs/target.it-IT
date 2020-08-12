---
keywords: adobe.target.triggerView;triggerView;triggerview;trigger view;at.js;functions;function;viewName;viewname;view name
description: Informazioni sulla funzione adobe.target.triggerView (viewName, options) per la libreria at.js JavaScript di Adobe Target.
title: Informazioni sulla funzione adobe.target.triggerView (viewName, options) per la libreria at.js JavaScript di Adobe Target.
feature: null
subtopic: Getting Started
topic: Standard
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 100%

---


# adobe.target.triggerView (viewName, options) - at.js 2.x

È possibile chiamare questa funzione a ogni caricamento di una nuova pagina o quando si esegue di nuovo il rendering di un componente di una pagina. Implementare `adobe.target.triggerView()` per le applicazioni a pagina singola per utilizzare il Compositore esperienza visiva per creare test A/B e attività di Targeting di esperienza (XT). Se non si implementa `adobe.target.triggerView()` sul sito, non sarà possibile usare il Compositore esperienza visiva per l’applicazione a pagina singola. Per ulteriori informazioni, consulta [Implementazione di un’applicazione a pagina singola](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md).

>[!NOTE]
>
>Questa funzione è stata introdotta con at.js 2.x e non è disponibile per at.js versione 1.*x*.

| Parametro | Tipo | Obbligatorio | Descrizione |
| --- | --- | --- | --- |
| viewName | Stringa | Sì | Passa un nome qualsiasi come tipo di stringa che desideri rappresenti la tua visualizzazione. Questo nome della visualizzazione appare nel pannello [!UICONTROL Modifiche] del Compositore esperienza visivo per consentire agli addetti al marketing di creare azioni ed eseguire le attività A/B e XT. |
| options | Oggetto | No |  |
| options > page | Booleano | No | **TRUE:** il valore predefinito della pagina è vero. Con page=true, si inviano notifiche al backend [!DNL Target] per incrementare il conteggio delle impression.<br>Se alla visualizzazione non è associata alcuna esperienza o metrica di attività, non viene inviata alcuna notifica.<br>**FALSE:**con page=false, non si inviano le notifiche per incrementare il conteggio delle impression. Da utilizzare solo per eseguire nuovamente il rendering di un componente su una pagina con un’offerta. |

## Esempio: True

Chiamata `triggerView()` per inviare una notifica al backend Target per incrementare le impression dell’attività e altre metriche.

```
adobe.target.triggerView("homeView")
```

## Esempio: False

Chiamata `triggerView()` per non inviare notifiche al backend Target per il conteggio delle impression.

```
adobe.target.triggerView("homeView", {page: false})
```
