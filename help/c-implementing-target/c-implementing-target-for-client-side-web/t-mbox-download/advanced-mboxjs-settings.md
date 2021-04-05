---
keywords: impostazioni avanzate di mbox.js;client;dominio server;xdomain;livello di compressione;supporto id sessione client;secureOnly;supporto id pc client;passare una pagina;URL di riferimento;livello di traffico;durata del traffico;funzione mboxParameters();funzione mboxSupported();funzione mboxCookieDomain();JavaScript extra;plug-in SiteCatalyst;mbox.js come JavaScript autoestraente;visualizzazione momentanea di altri contenuti;nascondere il corpo;corpo nascosto
description: Scopri l’implementazione legacy di mbox.js di Adobe Target. Esegui la migrazione a Adobe Experience Platform Web SDK (AEP Web SDK) o all’ultima versione di at.js.
title: Come si configura la libreria mbox.js di Target?
feature: at.js
role: Sviluppatori
exl-id: 17821e60-2692-49af-a225-764bd1b6aec1
translation-type: tm+mt
source-git-commit: 0a685427a047bfc0a2f5e81525b32df70af6d69f
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 71%

---

# Configurare mbox.js

Informazioni utili per scegliere diverse impostazioni nella pagina Impostazioni mbox.js.

>[!IMPORTANT]
>
>**Terminazione di mbox.js**: A partire dal 31 marzo 2021,  [!DNL Adobe Target] non supporta più la libreria mbox.js . Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto positivo sulle pagine che hanno [!DNL Target] attività in esecuzione servendo il contenuto predefinito.
>
>È consigliabile che tutti i clienti effettuino la migrazione alla versione più recente della nuova [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js prima di tale data, per evitare potenziali problemi con i siti. Per ulteriori informazioni, consulta [Panoramica: implementare Target per web lato client](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

Le impostazioni predefinite della libreria di funzioni [!DNL mbox.js] rispondono alle esigenze della maggior parte degli utenti di [!DNL Target].

Se necessario, rivolgiti all’amministratore del tuo account per modificare le impostazioni di [!DNL mbox.js].

Sono disponibili le seguenti opzioni:

## Client

Il codice cliente del tuo account.

In [!UICONTROL Amministrazione > Implementazione], il codice cliente del tuo account è riportato in alto.

## Timeout

Timeout della richiesta di Target.

Quando visualizzi [!UICONTROL Amministrazione > Implementazione], l&#39;impostazione Timeout (secondi) corrisponde al timeout della richiesta di Target. Per impostazione predefinita questo valore è impostato su 15 secondi, ma si consiglia di impostarlo su un valore compreso tra 2 e 5 secondi.

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
