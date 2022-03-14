---
keywords: implementazione;libreria javascript;js;atjs;decisioni su dispositivi;decisioni su dispositivi;at.js;on-device;su dispositivo;risoluzione dei problemi;risoluzione dei problemi;risoluzione dei problemi
description: Scopri come risolvere i problemi relativi alle decisioni sul dispositivo con la libreria at.js .
title: Come posso risolvere i problemi di On-Device Decisioning con la libreria JavaScript at.js?
feature: at.js
role: Developer
exl-id: 76bb9393-1560-455b-9d95-91576faee1f2
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 1%

---

# Risoluzione dei problemi relativi al decisioning sul dispositivo per at.js

Completa i seguenti passaggi per risolvere i problemi relativi alle decisioni sul dispositivo in [!DNL Adobe Target] con la libreria JavaScript at.js:

## Passaggio 1: Abilita il registro della console per at.js

Aggiunta del parametro URL `mboxDebug=1` consente ad at.js di stampare i messaggi nella console del browser.

Tutti i messaggi contengono il prefisso &quot;AT:&quot; per una comoda panoramica. Per verificare che un artefatto sia stato caricato correttamente, il registro della console deve contenere messaggi simili ai seguenti:

```
AT: LD.ArtifactProvider fetching artifact - https://assets.adobetarget.com/your-client-cide/production/v1/rules.json
AT: LD.ArtifactProvider artifact received - status=200
```

La figura seguente mostra questi messaggi nel registro della console:

![Registro della console con messaggi di artefatto](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/browser-console.png)

## Passaggio 2: Verifica il download dell’artefatto della regola nella scheda Rete del browser

Apri la scheda Rete del browser.

Ad esempio, per aprire DevTools in Google Chrome:

1. Premere Ctrl+Maiusc+J (Windows) o Comando+Opzione+J (Mac).
1. Passa alla scheda Rete .
1. Filtra le chiamate per parola chiave &quot;rules.json&quot; per assicurarti che venga visualizzato solo il file delle regole di artefatto.

   Inoltre, puoi filtrare per &quot;/delivery|rules.json/&quot; per visualizzare tutti [!DNL Target] chiamate e regole di artefatto.json.

   ![Scheda Rete in Google Chrome](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/rule-json.png)

## Passaggio 3: Verifica il download dell’artefatto della regola utilizzando gli eventi personalizzati at.js

La libreria at.js invia due nuovi eventi personalizzati per supportare le decisioni sui dispositivi.

* `adobe.target.event.ARTIFACT_DOWNLOAD_SUCCEEDED`
* `adobe.target.event.ARTIFACT_DOWNLOAD_FAILED`

Puoi abbonarti per ascoltare questi eventi personalizzati nella tua applicazione e intervenire in caso di successo o guasto del download del file delle regole di artefatto.

L’esempio seguente mostra un esempio di codice che ascolta gli eventi di successo e di errore del download degli artefatti:

```javascript
document.addEventListener(adobe.target.event.ARTIFACT_DOWNLOAD_SUCCEEDED, function(e) { 
  console.log("Artifact successfully downloaded", e.detail);
}, false);

document.addEventListener(adobe.target.event.ARTIFACT_DOWNLOAD_FAILED, function(e) { 
  console.log("Artifact failed to download", e.detail);
}, false);
```
