---
keywords: qa;anteprima;bookmarklet;collegamenti di anteprima
description: Informazioni utili per utilizzare il bookmarklet Adobe Target per imporre a Target di rilasciarvi dalla modalità di controllo qualità.
title: bookmarklet Attività QA per Adobe Target
topic: Advanced,Standard,Classic
uuid: 2890e215-16c9-4b22-a8eb-732cd6efede3
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# Bookmarklet di controllo qualità delle attività{#activity-qa-bookmarklet}

Information to help you use the [!DNL Target] QA bookmarklet to force [!DNL Target] to release you from QA mode.

Because [QA mode](../../c-activities/c-activity-qa/activity-qa.md#concept_9329EF33DE7D41CA9815C8115DBC4E40) is sticky, after you browse a website in QA mode, your [!DNL Target] session must expire or you need to have [!DNL Target] release you from QA mode before you can view your site like a typical visitor. Use the QA [!DNL Target] bookmarklet to force yourself out of QA mode.

To use the [!DNL Target] QA bookmarklet, create a bookmarklet containing the following JavaScript code and add it to your browser's Bookmarks Toolbar:

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

You can also manually force yourself out of QA mode by loading a page on your site with the `at_preview_token` parameter with an empty value.

Ad esempio:

`https://www.mysite.com/?at_preview_token=`
