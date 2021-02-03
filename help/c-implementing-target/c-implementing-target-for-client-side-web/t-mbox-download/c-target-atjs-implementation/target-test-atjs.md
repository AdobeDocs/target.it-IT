---
keywords: at.js;non produzione;non produzione;distribuire
description: Informazioni su come distribuire in modo sicuro at.js in un ambiente non di produzione.
title: Distribuire at.js in un ambiente non di produzione
feature: at.js
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 91%

---


# Distribuzione di at.js in un ambiente non di produzione

Informazioni sulle tecniche per distribuire in modo sicuro at.js in un ambiente non di produzione.

## Distribuzione a DTM Staging

Se utilizzi DTM, puoi facilmente salvare at.js nella configurazione di Adobe Target Tool.

Dopo aver salvato la libreria, utilizza lo strumento switch di DTM per testarlo sul codice di produzione. Questo permetterà ai tuoi consulenti Adobe di supportarti più facilmente.

Per ulteriori informazioni, vedi l&#39;[Opzione 3: Implementare la destinazione manualmente con la libreria JavaScript di Target ospitata da DTM](https://experienceleague.adobe.com/docs/dtm/implementing/target/add-target/t-implementing-target-manually-js-hosted-dtm.html) nelle *Procedure consigliate per l’implementazione di Adobe Target tramite la Dynamic Tag Management*.

## Utilizzare l&#39;estensione di Chrome Requestly per eseguire il mapping a un altro file

>[!NOTE]
>
>Oltre alle seguenti informazioni, puoi utilizzare l’estensione del browser [Adobe Target VEC Helper](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) per Google Chrome.

[Requestly](https://chrome.google.com/webstore/detail/requestly/mdnleldcmiljblolnjhpnblkcekpdkpa?hl=en) è un&#39;estensione gratuita di Chrome che consente di reindirizzare le richieste a un URL alternativo.

Si distribuisce at.js a un URL, quindi si utilizza Requestly per eseguire il mapping dell&#39;URL del file mbox.js corrente al nuovo URL at.js. A quel punto, ogni volta che il sito web prova a caricare mbox.js, carica invece at.js. Questo approccio rende anche più facile fornire supporto da parte di Adobe.

## Distribuzione in un ambiente di sviluppo, gestione temporanea o QA

Se si ospita mbox.js nel codebase e si è in grado di eseguire facilmente gli aggiornamenti agli ambienti di codice, distribuire at.js in uno dei propri ambienti più bassi.

Per un migliore supporto da parte di Adobe, distribuire il file in un ambiente a cui Adobe possa accedere.

## Utilizzare Charles o Fiddler per eseguire il mapping a un file locale

[Charles Web Debugging Proxy](https://www.charlesproxy.com/) è un&#39;applicazione disponibile per Mac e Windows la cui funzione Mappa in locale può essere utilizzata per mappare il caricamento del file di produzione mbox.js in una copia locale di at.js. Una versione di prova gratuita è disponibile per il download per Mac e Windows.

[Fiddler](https://www.telerik.com/fiddler) è uno strumento simile disponibile come download gratuito per Windows.

## Distribuire in un altro ambiente di gestione tag

Se si utilizza un altro gestore di tag, probabilmente questo può distribuire at.js in modo sicuro senza influire sul traffico di produzione.