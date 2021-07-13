---
keywords: istanze cloud;elenco suffissi pubblici;suffisso pubblico;cookie;cookie di prime parti;cookie di prime parti;azurewebsites.net;cloudapp.net;amazonaws.com;cloudfront.net;herokuapp.com;firebaseapp.com;targetGlobalSettings;cookieDomain
description: Esplora i problemi (con le soluzioni) riscontrati dai clienti quando si utilizzano istanze basate su cloud per testare Adobe [!DNL Target] o a scopo di bozza.
title: Posso utilizzare [!DNL Target] con istanze basate su cloud?
feature: at.js
role: Developer
exl-id: 220371a9-ba57-4e67-b82f-8fec6f9d2833
source-git-commit: 3c79b2ce70e456275ddf6774a35ae5c36f0ae99d
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 67%

---

# Utilizzare istanze basate su cloud con Target

Informazioni sui problemi riscontrati dai clienti quando si utilizzano istanze basate su cloud per testare [!DNL Adobe Target].

I clienti di Target utilizzano talvolta istanze basate su cloud con [!DNL Target] per test o semplici prove di concetto. Queste istanze possono includere i seguenti domini:

`azurewebsites.net`, `cloudapp.net`, `amazonaws.com`, `cloudfront.net`, `herokuapp.com` o `firebaseapp.com`

Questi domini, e molti altri, fanno parte dell’[elenco dei suffissi pubblici](https://publicsuffix.org/list/public_suffix_list.dat).

**Problema:** se si utilizzano questi domini, i browser moderni non salvano i cookie.

La libreria JavaScript [!DNL at.js] utilizza i cookie per tenere traccia degli utenti e assicurarsi che [!DNL Target] presenti sempre un’esperienza coerente. Se la libreria JavaScript [!DNL Target] non può salvare i cookie, le richieste [!DNL Target] sono disabilitate.

**Soluzione:** come best practice, se vuoi utilizzare istanze basate su cloud con domini inclusi nellʼelenco dei suffissi pubblici, personalizza lʼimpostazione `cookieDomain`. Per ulteriori informazioni, consulta [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md).
