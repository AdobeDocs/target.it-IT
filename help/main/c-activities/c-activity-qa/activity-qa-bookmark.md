---
keywords: qa;anteprima;bookmarklet;collegamenti di anteprima
description: Scopri come utilizzare il bookmarklet di controllo qualità di Adobe [!DNL Target] per forzare il rilascio di [!DNL Target] dalla modalità di controllo qualità.
title: Come si utilizza il Bookmarklet di controllo qualità delle attività?
feature: Activities
exl-id: dbfe59eb-6853-4909-abf1-e5630e979a98
TQID: 'https://experienceleague.adobe.com/kOQcdF2WgiAGkOS3rrLWfDSFTvRJX8jb-IeaahWnM0c'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: 6efa6b7a-8062-5c41-aef4-b4853cc306ae
    internal-label: Activities
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 0a683f6e68bb7481b9e45c91a275a46b84a1ffd8
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 6%
---
# Bookmarklet di controllo qualità delle attività {#activity-qa-bookmarklet}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come utilizzare il bookmarklet di controllo qualità di [!DNL Target] per uscire dalla modalità **[!UICONTROL Controllo qualità attività]** e visualizzare il tuo sito come un normale visitatore.

>[!ENDSHADEBOX]

Dopo aver navigato in un sito Web in [modalità Controllo qualità](/help/main/c-activities/c-activity-qa/activity-qa.md), la modalità Controllo qualità persiste tra le pagine fino alla scadenza della sessione [!DNL Target]. Un bookmarklet è un segnalibro del browser che esegue JavaScript. Il bookmarklet di controllo qualità [!DNL Target] forza [!DNL Target] a rilasciare l&#39;utente dalla modalità di controllo qualità, quindi non è necessario attendere la scadenza della sessione. Utilizza la versione che corrisponde alla versione at.js distribuita sul tuo sito.

>[!NOTE]
>
>La procedura per creare un bookmarklet varia in base al tipo e alla versione del browser. Consulta l’aiuto del browser o cerca su Internet indicazioni specifiche.

## Bookmarklet di controllo qualità attività per at.js 1.*x*

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

Puoi anche forzare manualmente l&#39;uscita dalla modalità di controllo qualità caricando una pagina del sito con il parametro `at_preview_token` impostato su un valore vuoto. Ad esempio:

`https://www.mysite.com/?at_preview_token=`

## Bookmarklet di controllo qualità attività per at.js 2.*x*

A differenza di at.js 1.*x*, at.js 2.*x* non supporta i cookie di terze parti. La modalità di controllo qualità persiste solo per il dominio di prima parte, per mezzo di un cookie di prima parte impostato da at.js. Di conseguenza, la sessione in modalità di controllo qualità viene gestita solo sul lato client e nessun cookie in modalità di controllo qualità viene inviato a [!DNL Target].

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

Dopo aver aggiunto al browser il bookmarklet che corrisponde alla versione at.js in uso, utilizzalo ogni volta che vuoi uscire dalla modalità di controllo qualità:

1. Apri qualsiasi pagina del sito mentre sei in modalità di controllo qualità.
1. Fare clic sul bookmarklet nella barra degli strumenti Segnalibri del browser.
1. Carica una pagina del sito. [!DNL Target] rilascia la sessione dalla modalità di controllo qualità e il sito viene visualizzato come per un normale visitatore.
