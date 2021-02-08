---
keywords: criterio di protezione del contenuto;csp;at.js;whitelist; inserire nell'elenco Consentiti;flicker;pre-hide;pre-hide;pre-hide;prenascondere
description: Informazioni sulle direttive di Content Security Policy (CSP) da aggiungere quando si utilizza  Adobe Target.
title: In che modo Target gestisce i criteri per la sicurezza dei contenuti (CSP)?
feature: Privacy & Security
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 5%

---


# Direttive Content Security Policy (CSP)

Se si utilizza [Content Security Policy](https://en.wikipedia.org/wiki/Content_Security_Policy) (CSP) per l&#39;implementazione [!DNL Adobe Target], è necessario aggiungere le seguenti direttive CSP quando si utilizza [at.js 2.1 o successivo](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md):

* `connect-src` con  `*.tt.omtrdc.net` inserito nell&#39;elenco Consentiti. Necessario per consentire la richiesta di rete al [!DNL Target] edge.
* `style-src unsafe-inline`. Necessario per il controllo pre-occultamento e sfarfallio.
* `script-src unsafe-inline`.  Obbligatorio per consentire l&#39;esecuzione JavaScript che potrebbe far parte di un&#39;offerta HTML.
