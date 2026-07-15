---
title: Guida all’avvio
description: Per integrare l’applicazione con i flag, dalla richiesta di accesso alla creazione del primo flag di funzione, segui la procedura riportata di seguito.
hide: true
exl-id: 7aa09535-45fa-4ddf-9e3f-a23f8a8ee666
source-git-commit: 35fa45d2a5374dcc47a02bb737f28f24847d7fc6
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 1%

---

# Guida all’avvio {#startup-guide}

Per integrare i flag nell’applicazione, segui la procedura riportata di seguito.

## Passaggio 1: richiedere l’accesso {#step-1-access}

Richiedi l’accesso alla console Flag e unisciti al tuo team. Per istruzioni dettagliate, consulta [Richiedi accesso](../console/request-access.md).

## Passaggio 2: integrare l’applicazione {#step-2-onboard}

Dopo aver ottenuto l’accesso, accedi alla console Flag e verifica che l’applicazione sia elencata nel team. In caso contrario, chiedi all’amministratore del team di aggiungerlo. Consulta [Eseguire l&#39;onboarding dell&#39;applicazione](../applications/onboard-your-application.md).

Prima dell’onboarding, prepara quanto segue:

| Requisito | Dettagli |
|---|---|
| **ID applicazione** | Identificatore client univoco utilizzato per la chiamata delle API dei flag. Utilizza l’ID client esistente della tua applicazione, se disponibile. |
| **Client lato server** | Se esegui l’integrazione con un SDK lato server, devi disporre di un ID client amministratore con le autorizzazioni appropriate. |
| **Client desktop** | È possibile utilizzare un codice prodotto e la versione del prodotto al posto di un ID client. |

## Passaggio 3: ottieni le credenziali {#step-3-credentials}

Le credenziali necessarie dipendono dal percorso di integrazione:

* **Web e dispositivi mobili (basati su tag):** Utilizza l&#39;ID **file di ambiente** dalla proprietà tag pubblicata. Per informazioni su come ottenere questo risultato, vedere il passaggio 4a.
* **SDK lato server:** Richiedi un **ID client token di servizio** e fai in modo che i flag lo supportino, prima di poter effettuare chiamate API da SDK. Prima di eseguire chiamate API, devi inserire nell&#39;elenco Consentiti l&#39;ID client del token di servizio.
* **Desktop:** È possibile utilizzare un codice prodotto e una versione del prodotto al posto di un ID client.

## Passaggio 4: integrare utilizzando un SDK {#step-4-integrate}

Segui i [passaggi di integrazione](integration-steps.md) per il tipo di applicazione. Scegli il percorso adatto al tuo stack:

* **Servizi Web** → Java SDK o Node.js SDK
* **App Web e per dispositivi mobili** → AEP Mobile SDK. Vedere [Android](../sdk-releases/android/android-extension-integration-guide.md) e [iOS](../sdk-releases/ios/ios-extension-integration-guide.md) guide
* **App desktop** → SDK (disponibile a breve)

## Passaggio 4a: configurare la raccolta dati e pubblicare la configurazione {#step-4a-data-collection}

Se esegui l’integrazione tramite un approccio basato su tag (web o mobile), configura la proprietà tag prima di inizializzare SDK:

1. In [Raccolta dati Adobe Experience Platform](https://experience.adobe.com/#/data-collection), apri la tua proprietà mobile o web.
1. Installa l&#39;estensione **Edge Network**, quindi l&#39;estensione **Experience Rollout** (nell&#39;ordine indicato).
1. Seleziona il **flusso di dati** (deve includere il set di dati di Customer Journey Analytics) e il dominio Edge.
1. Pubblica la configurazione tramite **Dev → Staging → Produzione**.
1. Copiare l&#39;ID **file di ambiente** dalla scheda **Ambienti**. Verrà utilizzato per inizializzare SDK.

>[!IMPORTANT]
>
>Nell&#39;ambiente **staging**, aggiungere all&#39;ID del file di ambiente il prefisso `staging/`, ovvero utilizzare `staging/<environmentId>`. In **production**, utilizza direttamente l&#39;ID file dell&#39;ambiente.

## Passaggio 5: creare e verificare il primo flag di funzione {#step-5-feature-flag}

Al termine dell’integrazione, crea il primo flag di funzione nella console e verificalo:

* [Creare il primo flag di funzione](../feature-flags/create-your-first-feature-flag.md)

## Vedi anche {#see-also}

* [Integrare i flag nell’app](integrating-in-your-app.md)
* [Passaggi dell’integrazione](integration-steps.md)
* [SDK](sdks.md)

<!-- -->
