---
keywords: advanced mbox.js settings;client;server domain;xdomain;compression level;client session id support;secureOnly;client pc id support;pass page;referring url;traffic level;traffic duration;mboxParameters() function body;mboxSupported() function body;mboxCookieDomain() function body;Extra JavaScript;SiteCatalyst plug-in;Get mbox.js as self-extracting JavaScript;flicker;body hiding;hide body
description: Informazioni utili per scegliere diverse impostazioni nella pagina Impostazioni mbox.js.
title: Configurare mbox.js
feature: at.js
translation-type: tm+mt
source-git-commit: 88f6e4c6ad168e4f9ce69aa6618d8641b466e28a
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 91%

---


# Configurare mbox.js

Informazioni utili per scegliere diverse impostazioni nella pagina Impostazioni mbox.js.

Le impostazioni predefinite della libreria di funzioni [!DNL mbox.js] rispondono alle esigenze della maggior parte degli utenti di [!DNL Target].

Se necessario, rivolgiti all’amministratore del tuo account per modificare le impostazioni di [!DNL mbox.js].

Sono disponibili le seguenti opzioni:

## Client

Il codice cliente del tuo account.

Quando si visualizza [!UICONTROL Amministrazione > Implementazione], il client nella parte superiore è il codice client per l&#39;account.

## Timeout

Timeout della richiesta di Target.

Quando si visualizza [!UICONTROL Amministrazione > Implementazione], l&#39;impostazione Timeout (secondi) corrisponde al timeout della richiesta Target. Per impostazione predefinita questo valore è impostato su 15 secondi, ma si consiglia di impostarlo su un valore compreso tra 2 e 5 secondi.

## XDomain

Determina se il browser imposta i cookie nel proprio dominio (cookie di prima parte), nel dominio di Target o entrambi.

La modifica di questa impostazione ha effetti sia su mbox.js che su at.js.

## Livello di compressione

Determina il livello di compressione del file di libreria mbox.js. Con un livello di compressione maggiore si riduce il tempo di caricamento della pagina.

## Corpo funzione mboxParameters()

Restituisce parametri aggiuntivi da passare a ogni chiamata mbox.

Ad esempio:

return &quot;test=123&quot;;

## Corpo funzione mboxSupported()

Restituisce “false” per escludere utenti specifici.

Ad esempio:

return !navigator.userAgent.indexOf(&#39;Safari&#39;) != -1;

È possibile includere o escludere i seguenti browser:

* IE 5.0 o versioni successive (Windows)
* Netscape 5.0 o versioni successive (Mac, Windows, Linux)
* Safari 1.2.4 o versioni successive (Mac)
* Mozilla Firefox 1.0 o versioni successive (Mac, Windows, Linux)

## Corpo funzione mboxCookieDomain()

Restituisce una stringa che descrive il dominio per impostare i cookie di prima parte.

Ad esempio:

return &quot;YOUR-DOMAIN&quot;;

## JavaScript aggiuntivo

Include eventuale JavaScript aggiuntivo da eseguire in ogni pagina.

## Plug-in SiteCatalyst

Abilita il plug-in Analytics Target.

Se abilitato, il plug-in Analytics genera il codice plug-in in mbox.js. Questo invia le informazioni tag di Analytics ai server di Target come richiesta mbox su ogni pagina con tag Analytics.

Tieni presente che occorre comunque fare riferimento al plug-in Analytics nella pagina.

## secureOnly

Indica se mbox.js deve utilizzare solo HTTPS o può passare da HTTP a HTTPS in base al protocollo della pagina. Si tratta di un’impostazione avanzata con impostazione predefinita False.