---
keywords: istanze cloud;elenco suffissi pubblici;suffisso pubblico;cookie;cookie di prime parti;cookie di prime parti;azurewebsites.net;cloudapp.net;amazonaws.com;cloudfront.net;herokuapp.com;firebaseapp.com;targetGlobalSettings;cookieDomain
description: Esplora i problemi (con le soluzioni) riscontrati dai clienti quando si utilizzano istanze basate su cloud per testare Adobe [!DNL Target] o a scopo di bozza.
title: Posso utilizzare [!DNL Target] con istanze basate su cloud?
feature: at.js
role: Developer
exl-id: 220371a9-ba57-4e67-b82f-8fec6f9d2833
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 82%

---

# Utilizzare istanze basate su cloud con Target

Informazioni sui problemi riscontrati dai clienti quando si utilizzano istanze basate su cloud per testare [!DNL Adobe Target].

I clienti di Target utilizzano talvolta istanze basate su cloud con [!DNL Target] per test o semplici prove di concetto. Queste istanze possono includere i seguenti domini:

`azurewebsites.net`, `cloudapp.net`, `amazonaws.com`, `cloudfront.net`, `herokuapp.com` o `firebaseapp.com`

Questi domini, e molti altri, fanno parte dell’[elenco dei suffissi pubblici](https://publicsuffix.org/list/public_suffix_list.dat).

**Problema:** se si utilizzano questi domini, i browser moderni non salvano i cookie.

Le librerie JavaScript [!DNL at.js] e [!DNL mbox.js] utilizzano i cookie per tracciare gli utenti in modo che [!DNL Target] possa offrire loro un’esperienza sempre coerente. Se le librerie JavaScript di [!DNL Target] non possono salvare i cookie, le richieste di [!DNL Target] sono disabilitate.

**Soluzione:** come best practice, se vuoi utilizzare istanze basate su cloud con domini inclusi nellʼelenco dei suffissi pubblici, personalizza lʼimpostazione `cookieDomain`. Per ulteriori informazioni, consulta [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md).
