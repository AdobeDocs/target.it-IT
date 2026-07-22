---
title: Guida all’avvio
description: Per integrare l’applicazione con i flag, dalla richiesta di accesso alla creazione del primo flag di funzione, segui la procedura riportata di seguito.
badge: label="Beta" type="Informative"
hide: true
exl-id: 7aa09535-45fa-4ddf-9e3f-a23f8a8ee666
source-git-commit: 339de89fff7bb14eb8146d42482b30c86feeedef
workflow-type: tm+mt
source-wordcount: '397'
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

## Passaggio 3: ottieni l’ID del file di ambiente {#step-3-credentials}

L’ID file di ambiente necessario dipende dal percorso di integrazione:

* **Web e dispositivi mobili (basati su tag):** Utilizza l&#39;ID **file di ambiente** dalla proprietà tag pubblicata. Per informazioni su come ottenere questo risultato, vedere il passaggio 4a.

## Passaggio 4: integrare utilizzando un SDK {#step-4-integrate}

Segui la guida all’integrazione per il tipo di applicazione. Scegli il percorso adatto al tuo stack:

* **App Web e per dispositivi mobili**. Vedere le [guide di Android](../sdk-releases/android/android-extension-integration-guide.md), [iOS](../sdk-releases/ios/ios-extension-integration-guide.md) e [Web](../sdk-releases/web/web-extension-integration-guide.md) nella sezione della guida all&#39;integrazione

## Passaggio 4a: configurare la raccolta dati e pubblicare la configurazione {#step-4a-data-collection}

Se esegui l’integrazione tramite un approccio basato su tag (web o mobile), configura la proprietà tag prima di inizializzare SDK:

1. In [Raccolta dati Adobe Experience Platform](https://experience.adobe.com/#/data-collection), creare una [proprietà tag](https://experienceleague.adobe.com/it/docs/experience-platform/tags/get-started/quick-start) se non ne è già disponibile una, oppure utilizzare una proprietà tag esistente.
1. Apri la proprietà del tag per dispositivi mobili o web e passa a [Estensioni](https://experienceleague.adobe.com/it/docs/experience-platform/tags/ui/extensions/overview).
1. Installa e configura l&#39;estensione **Edge Network**. Quindi installa l&#39;estensione **Flags**.
1. Seleziona lo **stream di dati** (deve includere il set di dati di Customer Journey Analytics) e configura il dominio Edge.
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
* [SDK](sdks.md)

<!-- -->
