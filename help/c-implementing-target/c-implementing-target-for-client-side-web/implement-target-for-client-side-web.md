---
description: Informazioni sull’implementazione di Adobe Target per web lato client.
title: Implementare Adobe Target per web lato client
feature: client-side
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 100%

---


# Panoramica: Implementare Target per web lato client

In un’implementazione lato client di [!DNL Adobe Target], [!DNL Target] distribuisce le esperienze associate a un’attività direttamente al browser client. Il browser determina quale esperienza visualizzare e la visualizza. Con un’implementazione lato client, puoi utilizzare un editor WYSIWYG, il [Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) o un’interfaccia non visiva, il [Compositore esperienza basato su moduli](/help/c-experiences/form-experience-composer.md), per creare esperienze di attività e personalizzazione.

Per implementare [!DNL Adobe Target] lato client, è necessario utilizzare la libreria [at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) o mbox.js.

>[!NOTE]
>
>La libreria mbox.js non verrà più sviluppata. Tutti i clienti devono [implementare at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/how-to-deployatjs.md) o [migrare da mbox.js a at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md).
