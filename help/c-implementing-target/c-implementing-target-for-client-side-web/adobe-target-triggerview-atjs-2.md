---
description: 'Informazioni sulla funzione adobe.target.triggerView (viewName, options) per at.js. '
keywords: adobe.target.notification;element;selector;notification;extension
seo-description: Informazioni sulla funzione adobe.target.triggerView (viewName, options) per la libreria at.js JavaScript di Adobe Target.
seo-title: Informazioni sulla funzione adobe.target.triggerView (viewName, options) per la libreria at.js JavaScript di Adobe Target.
solution: Target
subtopic: Introduzione
title: adobe.target.triggerView (viewName, options)
topic: Standard
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

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
| options &gt; page | Booleano | No | **TRUE:** il valore predefinito della pagina è vero. Con page=true, si inviano notifiche al backend [!DNL Target] per incrementare il conteggio delle impression.<br>Se non viene associata alcuna esperienza di attività o metrica di attività alla visualizzazione, non viene inviata alcuna notifica.<br>**FALSE:** con page=false, non si inviano le notifiche per incrementare il conteggio delle impression. Da utilizzare solo per eseguire nuovamente il rendering di un componente su una pagina con un’offerta. |

## Esempio: True

`triggerView()` per inviare una notifica al backend Target per incrementare le impression dell'attività e altre metriche.

```
adobe.target.triggerView("homeView")
```

## Esempio: False

`triggerView()` per evitare che vengano inviate notifiche al back-backend Target per il conteggio delle impression.

```
adobe.target.triggerView("homeView", {page: false})
```
