---
keywords: qa;anteprima;bookmarklet;collegamenti di anteprima
description: Informazioni utili per utilizzare il bookmarklet  Adobe Target QA per forzare Target a rilasciarvi dalla modalità QA.
title: Bookmarklet di controllo qualità delle attività
feature: Activities
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 14%

---


# Bookmarklet di controllo qualità delle attività

Informazioni utili per utilizzare il bookmarklet [!DNL Target] QA per forzare [!DNL Target] il rilascio dalla modalità QA.

>[!NOTE]
>
>La procedura per creare un bookmarklet varia in base al tipo e alla versione del browser. Consulta la guida del browser o cerca su internet indicazioni specifiche.

## bookmarklet QA attività per at.js 1.*x*

Poiché la [modalità QA](/help/c-activities/c-activity-qa/activity-qa.md) è fissa, dopo aver navigato in un sito Web in modalità QA, la sessione [!DNL Target] deve scadere oppure è necessario che [!DNL Target] rilasci dalla modalità QA prima di poter visualizzare il sito come un visitatore tipico. Utilizzate il bookmarklet QA [!DNL Target] per uscire dalla modalità QA.

Per utilizzare il bookmarklet [!DNL Target] QA, creare un bookmarklet contenente il codice JavaScript seguente e aggiungerlo alla barra degli strumenti Segnalibri del browser in uso:

```javascript
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

Potete anche uscire manualmente dalla modalità di controllo qualità caricando una pagina sul sito con il parametro `at_preview_token` con un valore vuoto.

Ad esempio:

`https://www.mysite.com/?at_preview_token=`

## bookmarklet QA attività per at.js 2.*x*

Contrariamente a at.js 1.*x*, at.js 2.*xnon* supporta i cookie di terze parti, e la modalità QA è fissa solo per il dominio di prime parti (tramite un cookie di prime parti impostato da at.js). Così, in at.js 2.*x*, la sessione in modalità QA viene gestita solo sul lato client e non vengono inviati cookie in modalità QA a Target.

Per utilizzare il bookmarklet [!DNL Target] QA, creare un bookmarklet contenente il codice JavaScript seguente e aggiungerlo alla barra degli strumenti Segnalibri del browser in uso:

```javascript
javascript:(
    function () {
        var AT_QA_MODE = 'at_qa_mode=';
        var isSet = document.cookie.split(';').some(function (cookie) {
            return cookie.trim().startsWith(AT_QA_MODE);
        });
        if (isSet) {
            document.cookie = AT_QA_MODE + '; Path=/; Max-Age=-0;';
            var url = window.location.href.split('at_preview_token',2)[0];
            window.open(url.substring(0, url.length - 1), '_self', 'noreferrer');
        }
    })();
```

## Utilizzare il bookmarklet QA dell&#39;attività

Fare clic sul bookmarklet sulla barra degli strumenti del browser.

