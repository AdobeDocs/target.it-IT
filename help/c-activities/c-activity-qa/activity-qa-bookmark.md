---
description: Informazioni su come utilizzare il bookmarklet di controllo qualità di Target per forzare l’uscita dalla modalità di controllo qualità.
keywords: qa;anteprima;bookmarklet;collegamenti di anteprima
seo-description: Informazioni su come utilizzare il bookmarklet di controllo qualità di Target per forzare l’uscita dalla modalità di controllo qualità.
seo-title: Bookmarklet di controllo qualità delle attività
solution: Target
title: Bookmarklet di controllo qualità delle attività
topic: Advanced,Standard,Classic
uuid: 2890e215-16c9-4b22-a8eb-732cd6efede3
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Bookmarklet di controllo qualità delle attività{#activity-qa-bookmarklet}

Informazioni su come utilizzare il bookmarklet di controllo qualità di Target per forzare l’uscita dalla modalità di controllo qualità.

Siccome il [Controllo di qualità attività](../../c-activities/c-activity-qa/activity-qa.md#concept_9329EF33DE7D41CA9815C8115DBC4E40) è persistente, dopo aver navigato su un sito web in modalità di controllo qualità sarà possibile visualizzare il sito come un normale visitatore solo dopo che sessione di Target sarà scaduta o dopo che l’uscita forzata dalla modalità di controllo qualità. Utilizza il bookmarklet Controllo di qualità di Target per forzare l'uscita dalla modalità Controllo di qualità.

Per utilizzare il bookmarklet di controllo di qualità di Target, crea un bookmarklet contenente il seguente codice JavaScript e aggiungilo alla barra dei segnalibri del browser:

```
javascript:(
    function () {
        if (window.location.href.indexOf('?') != -1) {
            var parts = window.location.href.split('at_preview_token',2);
            if (parts.length > 1) {
                window.location.href = parts[0].concat('at_preview_token=');
            } else {
                window.location.href = window.location.href.concat("&at_preview_token=")
            }
        } else {
            window.location.href = window.location.href.concat("?at_preview_token=")
        }
    }
)();
```

Il bookmarklet dovrebbe quindi apparire sulla barra degli strumenti, pronto per essere riutilizzato.

>[!NOTE]
>
>La procedura per creare un bookmarklet varia in base al tipo e alla versione del browser. Consulta la guida del browser o cerca su internet indicazioni specifiche.

Puoi anche forzare manualmente l’uscita dalla modalità di controllo qualità caricando una pagina del sito con il parametro `at_preview_token` con un valore vuoto (ad esempio, `https://www.mysite.com/?at_preview_token=`).
