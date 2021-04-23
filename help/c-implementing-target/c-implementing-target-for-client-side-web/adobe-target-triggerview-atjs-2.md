---
keywords: adobe.target.triggerView;triggerView;triggerview;attiva visualizzazione;at.js;funzioni;funzione;viewName;viewname;nome visualizzazione
description: Utilizza la funzione adobe.target.triggerView() per la libreria JavaScript Adobe [!DNL Target] at.js da utilizzare nelle applicazioni a pagina singola (SPA). (at.js 2.x)
title: Come si utilizza la funzione adobe.target.triggerView()?
feature: at.js
role: Developer
exl-id: 619d5166-d1d9-49a6-9807-338544782e66
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 84%

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
| options > page | Booleano | No | **TRUE:** il valore predefinito della pagina è vero. Con page=true, si inviano notifiche al backend [!DNL Target] per incrementare il conteggio delle impression.<br>Una notifica viene sempre inviata per impostazione predefinita quando  `triggerView` viene chiamata una, a meno che non quando options > page sia impostato su false.<br>**FALSE:** con page=false, non si inviano le notifiche per incrementare il conteggio delle impression. Da utilizzare solo per eseguire nuovamente il rendering di un componente su una pagina con un’offerta. |

## Esempio: True

Chiamata `triggerView()` per inviare una notifica al backend Target per incrementare le impression dell’attività e altre metriche.

```javascript
adobe.target.triggerView("homeView")
```

## Esempio: False

Chiamata `triggerView()` per non inviare notifiche al backend Target per il conteggio delle impression.

```javascript
adobe.target.triggerView("homeView", {page: false})
```
