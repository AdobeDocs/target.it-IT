---
description: Elenco di funzioni mbox.js da utilizzare per l'implementazione con mbox.js.
keywords: Funzioni mbox
seo-description: Elenco di funzioni mbox.js da utilizzare per l'implementazione con mbox.js.
seo-title: Funzioni di mbox.js
solution: Target
title: Funzioni di mbox.js
uuid: f503bc44-a664-4d09-82dc-80a1198ad9d0
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Funzioni di mbox.js{#mbox-js-functions}

Elenco di funzioni mbox.js da utilizzare per l&#39;implementazione con mbox.js.

>[!NOTE]
>
>Se si utilizza [!DNL at.js], questi metodi non sono applicabili.

| Metodo | Note |
|--- |--- |
| `mbox.getName()` |  |
| `mbox.getURL()` |  |
| `mbox.getDiv()` | Restituisce il div associato alla mbox (con il contenuto predefinito o un&#39;offerta) |
| `mbox.getParameters()` | Matrice di parametri con due campi, nome e valore |
| `mbox.setOnError()` | Esempio:<br>`mbox.setOnError(function() { alert(this.getName() +" had error"});` |
| `mbox.setMessage(message)` | È possibile visualizzare il messaggio nella finestra di debug. |
| `mboxCurrent.activate()` |  |
| `mboxCurrent.cancelTimeout()` |  |
| `mboxCurrent.finalize()` |  |
| `mboxCurrent.getDefaultDiv()` |  |
| `mboxCurrent.getDiv()` | Restituisce il div associato alla mbox (con il contenuto predefinito o un&#39;offerta) |
| `mboxCurrent.getEventTimes()` |  |
| `mboxCurrent.getFetcher()` |  |
| `mboxCurrent.getId()` |  |
| `mboxCurrent.getImportName()` |  |
| `mboxCurrent.getName()` |  |
| `mboxCurrent.getOffer()` |  |
| `mboxCurrent.getParameters()` | Matrice di parametri con due campi, nome e valore. |
| `mboxCurrent.getURL()` |  |
| `mboxCurrent.getURLBuilder()` |  |
| `mboxCurrent.hide()` |  |
| `mboxCurrent.isActivated`() |  |
| `mboxCurrent.load()` |  |
| `mboxCurrent.loaded()` |  |
| `mboxCurrent.setEventTime()` |  |
| `mboxCurrent.setFetcher()` |  |
| `mboxCurrent.setMessage()` |  |
| `mboxCurrent.setMessage(message)` | Visualizza il messaggio nella finestra di debug. |
| `mboxCurrent.setOffer()` |  |
| `mboxCurrent.setOnError()` | Esempio:<br>`mboxCurrent.setOnError(function(){ alert(this.getName() +" had error"});` |
| `mboxCurrent.setOnLoad()` | Esempio:<br>`mboxCurrent.setOnLoad(function(){alert(this.getName()+" loaded")});` |
| `mboxCurrent.show()` |  |
| `mboxCurrent.showContent()` |  |
| `mboxFactoryDefault.addOnLoad(action)` | L&#39;azione viene chiamata quando la pagina viene caricata. |
| `mboxFactoryDefault.getMboxes().each()` | Esempio:<br>`mboxFactoryDefault.getMboxes().each(function() { alert(mbox.getName()) };` |
| `mboxFactoryDefault.getMboxes().length()` |  |
| `mboxFactoryDefault.getPageId()` |  |
| `mboxFactoryDefault.getPCId().getId()` |  |
| `mboxFactoryDefault.getSessionId().getId()` |  |
| `mboxFactories.get('default').getSessionId()​.forceId("1276011116668");` |  |
| `mboxFactories.get('default').getPCId()​.forceId("1276011116668");` |  |
| `mboxFactoryDefault.create()` |  |
| `mboxFactoryDefault.disable()` |  |
| `mboxFactoryDefault.enable()` |  |
| `mboxFactoryDefault.get()` |  |
| `mboxFactoryDefault.getCookieManager()` |  |
| `mboxFactoryDefault.getDisableReason()` |  |
| `mboxFactoryDefault.getEllapsedTime()` |  |
| `mboxFactoryDefault.getEllapsedTimeUntil()` |  |
| `mboxFactoryDefault.getMboxes()` | Restituisce un valore `mboxList`. |
| `mboxFactoryDefault.getSignaler()` |  |
| `mboxFactoryDefault.getURLBuilder()` |  |
| `mboxFactoryDefault.isAdmin()` |  |
| `mboxFactoryDefault.isDomLoaded()` |  |
| `mboxFactoryDefault.isEnabled()` |  |
| `mboxFactoryDefault.isSupported()` |  |
| `mboxFactoryDefault.limitTraffic()` |  |
| `mboxFactoryDefault.update()` |  |
| `mboxFactoryDefault.getCookieManager()​.getCookie("name")//!= null) {` |  |
| `mboxFactoryDefault.getCookieManager()​.setCookie(_name,_value, _duration);` |  |