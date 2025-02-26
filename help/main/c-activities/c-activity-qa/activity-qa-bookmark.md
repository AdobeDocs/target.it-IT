---
keywords: qa;anteprima;bookmarklet;collegamenti di anteprima
description: Scopri come utilizzare il bookmarklet Adobe [!DNL Target] QA per forzare [!DNL Target] l'uscita dalla modalità di controllo qualità.
title: Come si utilizza il Bookmarklet di controllo qualità delle attività?
feature: Activities
exl-id: dbfe59eb-6853-4909-abf1-e5630e979a98
source-git-commit: 4b5111c00384fdc73eaadbf0eec22ac6c2784a22
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 13%

---

# Bookmarklet di controllo qualità delle attività

Informazioni sull&#39;utilizzo del bookmarklet di controllo qualità [!DNL Target] per forzare il rilascio di [!DNL Target] dalla modalità di controllo qualità.

>[!NOTE]
>
>La procedura per creare un bookmarklet varia in base al tipo e alla versione del browser. Consulta la guida del browser o cerca su internet indicazioni specifiche.

## Bookmarklet di controllo qualità delle attività per at.js 1.*x*

Poiché la modalità [Controllo qualità](/help/main/c-activities/c-activity-qa/activity-qa.md) è persistente, dopo aver navigato in un sito Web in modalità di controllo qualità è necessario che la sessione di [!DNL Target] scada o che [!DNL Target] sia rilasciato dalla modalità di controllo qualità prima di poter visualizzare il sito come un normale visitatore. Utilizza il bookmarklet di controllo qualità [!DNL Target] per uscire dalla modalità di controllo qualità.

Per utilizzare il bookmarklet di controllo qualità [!DNL Target], creare un bookmarklet contenente il codice JavaScript seguente e aggiungerlo alla barra dei segnalibri del browser:

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

Puoi anche forzare manualmente l&#39;uscita dalla modalità di controllo qualità caricando una pagina del sito con il parametro `at_preview_token` con un valore vuoto.

Ad esempio:

`https://www.mysite.com/?at_preview_token=`

## Bookmarklet di controllo qualità delle attività per at.js 2.*x*

A differenza di at.js 1.*x*, at.js 2.*x* non supporta i cookie di terze parti e la modalità di controllo qualità è definitiva solo per il dominio di prima parte (tramite un cookie di prima parte impostato da at.js). Pertanto, in at.js 2.*x*, la sessione in modalità di controllo qualità è gestita solo sul lato client e non vengono inviati cookie in modalità di controllo qualità a Target.

Per utilizzare il bookmarklet di controllo qualità [!DNL Target], creare un bookmarklet contenente il codice JavaScript seguente e aggiungerlo alla barra dei segnalibri del browser:

```javascript
javascript:(
    function () {
        var AT_QA_MODE = 'at_qa_mode=';
        var isSet = document.cookie.split(';').some(function (cookie) {
            return cookie.trim().startsWith(AT_QA_MODE);
        });
        if (isSet) {            
            document.cookie = AT_QA_MODE + ';domain='+window.location.hostname+";Path=/; Max-Age=-0;";
            var token = window.location.href.indexOf("?at_preview_token")<0? "&at_preview_token" : "?at_preview_token";
            var url = window.location.href.split(token,2)[0];
            window.open(url, '_self', 'noreferrer');
        }
    })(); 
```

## Utilizzare il bookmarklet di controllo qualità delle attività

Fare clic sul bookmarklet sulla barra degli strumenti del browser.
