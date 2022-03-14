---
keywords: qa;anteprima;bookmarklet;collegamenti di anteprima
description: Scopri come utilizzare l’Adobe [!DNL Target] Bookmarklet di controllo qualità per forzare [!DNL Target] per uscire dalla modalità di controllo qualità.
title: Come si utilizza il Bookmarklet di controllo qualità delle attività?
feature: Activities
exl-id: dbfe59eb-6853-4909-abf1-e5630e979a98
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 13%

---

# Bookmarklet di controllo qualità delle attività

Informazioni utili per l’utilizzo del [!DNL Target] Bookmarklet di controllo qualità per forzare [!DNL Target] per uscire dalla modalità di controllo qualità.

>[!NOTE]
>
>La procedura per creare un bookmarklet varia in base al tipo e alla versione del browser. Consulta la guida del browser o cerca su internet indicazioni specifiche.

## Bookmarklet di controllo qualità delle attività per at.js 1.*x*

Perché [Modalità QA](/help/main/c-activities/c-activity-qa/activity-qa.md) è persistente, dopo aver navigato su un sito web in modalità di controllo qualità, il tuo [!DNL Target] la sessione deve scadere o è necessario [!DNL Target] rilascia l’utente dalla modalità di controllo qualità prima di poter visualizzare il sito come un normale visitatore. Utilizzare il Controllo qualità [!DNL Target] bookmarklet per uscire dalla modalità di controllo qualità.

Per utilizzare [!DNL Target] Bookmarklet di controllo qualità, crea un bookmarklet contenente il seguente codice JavaScript e aggiungilo alla barra dei segnalibri del browser:

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

Puoi anche forzare manualmente l’uscita dalla modalità di controllo qualità caricando una pagina del sito con `at_preview_token` con un valore vuoto.

Ad esempio:

`https://www.mysite.com/?at_preview_token=`

## Bookmarklet di controllo qualità delle attività per at.js 2.*x*

A differenza di at.js 1.*x*, at.js 2.*x* non supporta i cookie di terze parti e la modalità di controllo qualità è persistente solo per il dominio di prima parte (tramite un cookie di prima parte impostato da at.js). Pertanto, in at.js 2.*x*, la sessione in modalità di controllo qualità viene gestita solo sul lato client e non vengono inviati cookie in modalità di controllo qualità a Target.

Per utilizzare [!DNL Target] Bookmarklet di controllo qualità, crea un bookmarklet contenente il seguente codice JavaScript e aggiungilo alla barra dei segnalibri del browser:

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

## Utilizzare il bookmarklet Controllo di qualità delle attività

Fai clic sul bookmarklet sulla barra degli strumenti del browser.
