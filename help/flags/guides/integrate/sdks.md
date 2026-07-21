---
title: SDK
description: Scopri l’architettura di SDK in Flags e le estensioni disponibili per AEP Web SDK e AEP Mobile SDK.
hide: true
exl-id: 110a440d-b52a-4e1e-a94f-86f9741a223a
source-git-commit: eeba7af62ab101e687852ce993a001832ce4a83b
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 1%

---

# SDK {#sdks}

Flag fornisce SDK per l’integrazione di flag di funzione nelle applicazioni. I flag vengono distribuiti tramite AEP Web SDK e AEP Mobile SDK.

## Architettura SDK {#architecture}

Tutti gli SDK dei flag condividono la stessa architettura di base:

* **Inizializzazione** - SDK è configurato all&#39;avvio e si registra con il servizio Flags.
* **Recupero funzionalità**: SDK recupera i dati dei flag di funzionalità e valuta i flag localmente.
* **Memorizzazione in cache**: SDK memorizza nella cache i dati dei flag di funzionalità e li aggiorna in base a un intervallo di polling configurabile.
* **Gestione errori** - Se il servizio non è disponibile, SDK continua a fornire valutazioni dei flag di funzionalità dalla cache locale.

## SDK disponibili {#available-sdks}

### AEP Web SDK {#web-sdk}

L’estensione Flags per web si integra con Adobe Experience Platform Web SDK.

>[!NOTE]
>
>Il supporto per Web SDK sarà presto disponibile. Contatta il tuo rappresentante Adobe per ricevere assistenza all’accesso anticipato.

### Estensione Android {#android-extension}

L&#39;estensione Flags per Android si integra con Adobe Experience Platform Mobile SDK.

Per istruzioni sulla configurazione, consulta la [Guida all&#39;integrazione dell&#39;estensione Android](../sdk-releases/android/android-extension-integration-guide.md).

### Estensione iOS {#ios-extension}

L&#39;estensione Flags per iOS si integra con Adobe Experience Platform Mobile SDK.

Per istruzioni sulla configurazione, consulta la [Guida all&#39;integrazione dell&#39;estensione iOS](../sdk-releases/ios/ios-extension-integration-guide.md).

## Vedi anche {#see-also}

* [guida all’integrazione delle estensioni Android](../sdk-releases/android/android-extension-integration-guide.md)
* [guida all’integrazione delle estensioni iOS](../sdk-releases/ios/ios-extension-integration-guide.md)
* [Guida all’integrazione delle estensioni web](../sdk-releases/web/web-extension-integration-guide.md)

<!-- -->
