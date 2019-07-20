---
description: Informazioni utili per scegliere diverse impostazioni nella pagina Impostazioni mbox.js.
keywords: impostazioni avanzate di mbox.js;client;dominio server;xdomain;livello di compressione;supporto id sessione client;secureOnly;supporto id pc client;passare una pagina;URL di riferimento;livello di traffico;durata del traffico;funzione mboxParameters();funzione mboxSupported();funzione mboxCookieDomain();JavaScript extra;plug-in SiteCatalyst;mbox.js come JavaScript autoestraente;visualizzazione momentanea di altri contenuti;nascondere il corpo;corpo nascosto
seo-description: Informazioni utili per scegliere diverse impostazioni nella pagina Impostazioni mbox.js.
seo-title: Configurare mbox.js
solution: Target
title: Configurare mbox.js
uuid: e79c7af7-f8bd-4e2b-8e67-b04eddf0c65d
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Configurare mbox.js{#configure-mbox-js}

Informazioni utili per scegliere diverse impostazioni nella pagina Impostazioni mbox.js.

Le impostazioni predefinite della libreria di funzioni [!DNL mbox.js] rispondono alle esigenze della maggior parte degli utenti di [!DNL Target].

Se necessario, rivolgiti all’amministratore del tuo account per modificare le impostazioni di [!DNL mbox.js].

Sono disponibili le seguenti opzioni:

## Client

Il codice cliente del tuo account.

In [!UICONTROL Configurazione &gt; Implementazione &gt; Modifica impostazioni mbox.js], il codice cliente del tuo account è riportato in alto.

## Timeout

Timeout della richiesta di Target.

In [!UICONTROL Configurazione &gt; Implementazione &gt; Modifica impostazioni mbox.js], il valore Timeout dopo Livello di compressione riporta il timeout della richiesta di Target. Per impostazione predefinita questo valore è impostato su 15 secondi, ma si consiglia di impostarlo su un valore compreso tra 2 e 5 secondi.

## XDomain

Determina se il browser imposta i cookie nel proprio dominio (cookie di prima parte), nel dominio di Target o entrambi.

La modifica di questa impostazione ha effetti sia su mbox.js che su at.js.

## Livello di compressione

Determina il livello di compressione del file di libreria mbox.js. Con un livello di compressione maggiore si riduce il tempo di caricamento della pagina.

## Corpo funzione mboxParameters()

Restituisce parametri aggiuntivi da passare a ogni chiamata mbox.

Ad esempio:

return "test=123";

## Corpo funzione mboxSupported()

Restituisce “false” per escludere utenti specifici.

Ad esempio:

return !navigator.userAgent.indexOf('Safari') != -1;

È possibile includere o escludere i seguenti browser:

* IE 5.0 o versioni successive (Windows)
* Netscape 5.0 o versioni successive (Mac, Windows, Linux)
* Safari 1.2.4 o versioni successive (Mac)
* Mozilla Firefox 1.0 o versioni successive (Mac, Windows, Linux)

## Corpo funzione mboxCookieDomain()

Restituisce una stringa che descrive il dominio per impostare i cookie di prima parte.

Ad esempio:

return "YOUR-DOMAIN";

## JavaScript aggiuntivo

Include eventuale JavaScript aggiuntivo da eseguire in ogni pagina.

## Plug-in SiteCatalyst

Abilita il plug-in Analytics Target.

Se abilitato, il plug-in Analytics genera il codice plug-in in mbox.js. Questo invia le informazioni tag di Analytics ai server di Target come richiesta mbox su ogni pagina con tag Analytics.

Tieni presente che occorre comunque fare riferimento al plug-in Analytics nella pagina.

## secureOnly

Indica se mbox.js deve utilizzare solo HTTPS o può passare da HTTP a HTTPS in base al protocollo della pagina. Si tratta di un’impostazione avanzata con impostazione predefinita False.