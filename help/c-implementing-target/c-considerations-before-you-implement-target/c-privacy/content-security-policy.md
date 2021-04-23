---
keywords: informativa sulla sicurezza dei contenuti;csp;at.js;whitelist;inserire nell'elenco Consentiti;visualizzazione momentanea di altri contenuti;pre-nascondere;pre-nascondere;pre-nascondere
description: Scopri le direttive Content Security Policy (CSP) da aggiungere quando utilizzi Adobe Target.
title: In che modo [!DNL Target] gestisce i criteri sulla sicurezza dei contenuti (CSP)?
feature: Privacy e sicurezza
role: Developer
exl-id: 31457b16-ed21-4540-8d0c-abfb49d1fbe9
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 5%

---

# Direttive Content Security Policy (CSP)

Se utilizzi [Criteri sulla sicurezza dei contenuti](https://en.wikipedia.org/wiki/Content_Security_Policy) (CSP) per l&#39;implementazione [!DNL Adobe Target], quando utilizzi [at.js 2.1 o versioni successive](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) aggiungi le seguenti direttive CSP:

* `connect-src` con  `*.tt.omtrdc.net` inserito nell&#39;elenco Consentiti. Necessario per consentire la richiesta di rete al server Edge [!DNL Target] .
* `style-src unsafe-inline`. Necessario per il controllo pre-hiding e visualizzazione momentanea di altro contenuto.
* `script-src unsafe-inline`.  Obbligatorio per consentire l&#39;esecuzione JavaScript che potrebbe far parte di un&#39;offerta HTML.
