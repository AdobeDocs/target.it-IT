---
keywords: informativa sulla sicurezza dei contenuti;csp;at.js;whitelist;inserire nell'elenco Consentiti;visualizzazione momentanea di altri contenuti;pre-nascondere;pre-nascondere;pre-nascondere
description: Scopri le direttive Content Security Policy (CSP) da aggiungere quando utilizzi Adobe Target.
title: Come funziona [!DNL Target] Gestire i criteri sulla sicurezza dei contenuti (CSP)?
feature: Privacy & Security
role: Developer
exl-id: 31457b16-ed21-4540-8d0c-abfb49d1fbe9
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 5%

---

# Direttive Content Security Policy (CSP)

Se utilizzi [Informativa sulla sicurezza dei contenuti](https://en.wikipedia.org/wiki/Content_Security_Policy) (CSP) per [!DNL Adobe Target] Implementazione, aggiungi le seguenti direttive CSP quando utilizzi [at.js 2.1 o successivo](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md):

* `connect-src` con `*.tt.omtrdc.net` inserito nell&#39;elenco Consentiti. Necessario per consentire la richiesta di rete al [!DNL Target] bordo.
* `style-src unsafe-inline`. Necessario per il controllo pre-hiding e visualizzazione momentanea di altro contenuto.
* `script-src unsafe-inline`.  Obbligatorio per consentire l’esecuzione JavaScript che potrebbe far parte di un’offerta HTML.
