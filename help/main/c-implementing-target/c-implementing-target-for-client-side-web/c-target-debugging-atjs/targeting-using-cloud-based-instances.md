---
keywords: istanze cloud;elenco suffissi pubblici;suffisso pubblico;cookie;cookie di prime parti;cookie di prime parti;azurewebsites.net;cloudapp.net;amazonaws.com;cloudfront.net;herokuapp.com;firebaseapp.com;targetGlobalSettings;cookieDomain
description: Esplorare i problemi (con le soluzioni) riscontrati dai clienti quando si utilizzano istanze basate su cloud per testare l’Adobe [!DNL Target] o a scopo di prova del concetto.
title: Posso usare [!DNL Target] con istanze basate su cloud?
feature: at.js
role: Developer
exl-id: 220371a9-ba57-4e67-b82f-8fec6f9d2833
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 67%

---

# Utilizzare istanze basate su cloud con Target

Informazioni sui problemi riscontrati dai clienti quando si utilizzano istanze basate su cloud per testare [!DNL Adobe Target].

I clienti di Target utilizzano talvolta istanze basate su cloud con [!DNL Target] per test o semplici prove di concetto. Queste istanze possono includere i seguenti domini:

`azurewebsites.net`, `cloudapp.net`, `amazonaws.com`, `cloudfront.net`, `herokuapp.com` o `firebaseapp.com`

Questi domini, e molti altri, fanno parte dell’[elenco dei suffissi pubblici](https://publicsuffix.org/list/public_suffix_list.dat).

**Problema:** se si utilizzano questi domini, i browser moderni non salvano i cookie.

La [!DNL at.js] La libreria JavaScript utilizza i cookie per tenere traccia degli utenti e garantire che [!DNL Target] presenta sempre un’esperienza coerente. Se la [!DNL Target] La libreria JavaScript non può salvare i cookie, [!DNL Target] le richieste sono disabilitate.

**Soluzione:** come best practice, se vuoi utilizzare istanze basate su cloud con domini inclusi nellʼelenco dei suffissi pubblici, personalizza lʼimpostazione `cookieDomain`. Per ulteriori informazioni, consulta [targetGlobalSettings()](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/).
