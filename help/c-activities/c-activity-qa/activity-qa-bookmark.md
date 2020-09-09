---
keywords: qa;preview;bookmarklet;preview links
description: Informazioni utili per utilizzare il bookmarklet  Adobe Target QA per forzare Target a rilasciarvi dalla modalità QA.
title: bookmarklet QA attività per  Adobe Target
feature: qa
topic: Advanced,Standard,Classic
uuid: 2890e215-16c9-4b22-a8eb-732cd6efede3
translation-type: tm+mt
source-git-commit: 620bb6dfbe160cf27ef5de9199c3d91fb806f316
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 11%

---


# Bookmarklet di controllo qualità delle attività{#activity-qa-bookmarklet}

Information to help you use the [!DNL Target] QA bookmarklet to force [!DNL Target] to release you from QA mode.

>[!NOTE]
>
>La procedura per creare un bookmarklet varia in base al tipo e alla versione del browser. Consulta la guida del browser o cerca su internet indicazioni specifiche.

## bookmarklet QA attività per at.js 1.*x*

Because [QA mode](../../c-activities/c-activity-qa/activity-qa.md#concept_9329EF33DE7D41CA9815C8115DBC4E40) is sticky, after you browse a website in QA mode, your [!DNL Target] session must expire or you need to have [!DNL Target] release you from QA mode before you can view your site like a typical visitor. Use the QA [!DNL Target] bookmarklet to force yourself out of QA mode.

To use the [!DNL Target] QA bookmarklet, create a bookmarklet containing the following JavaScript code and add it to your browser&#39;s Bookmarks Toolbar:

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

## bookmarklet QA attività per at.js 2.*x*

Contrariamente a at.js 1.*x*, at.js 2.*x* non supporta i cookie di terze parti e la modalità QA è fissa solo per il dominio di prime parti (tramite un cookie di prime parti impostato da at.js). Così, in at.js 2.*x*, la sessione in modalità QA viene gestita solo sul lato client e non vengono inviati cookie in modalità QA a Target.

To use the [!DNL Target] QA bookmarklet, create a bookmarklet containing the following JavaScript code and add it to your browser&#39;s Bookmarks Toolbar:

```
javascript:(
    function () {
        var AT_QA_MODE = 'at_qa_mode=';
        var isSet = document.cookie.split(';').some(function (cookie) {
            return cookie.trim().startsWith(AT_QA_MODE);
        });
        if (isSet) {
            document.cookie = AT_QA_MODE + '; Max-Age=-99999999;';
            var url = window.location.href.split('at_preview_token',2)[0];
            window.location.href = url.substring(0, url.length - 1);
        }
    })();
```

## Utilizzare il bookmarklet QA dell&#39;attività

Fare clic sul bookmarklet sulla barra degli strumenti del browser.

You can also manually force yourself out of QA mode by loading a page on your site with the `at_preview_token` parameter with an empty value.

Ad esempio:

`https://www.mysite.com/?at_preview_token=`
