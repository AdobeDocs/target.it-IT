---
description: Schema del sistema Target che mostra il flusso di chiamate e informazioni inviate o raccolte per una mbox globale creata automaticamente utilizzando at.js.
keywords: schema di sistema;visualizzazione momentanea;Target Standard;at. js;implementazione
seo-description: Schema del sistema Adobe Target che mostra il flusso di chiamate e informazioni inviate o raccolte per una mbox globale creata automaticamente utilizzando at.js.
seo-title: Come funziona at.js
solution: Target
title: Funzionamento di at.js
topic: Standard
uuid: 8ed04881-3dd9-496f-9c9c-feb9c740ed80
translation-type: tm+mt
source-git-commit: 2e2b7d8ccd8efa29c5734e22d53acedf6635e9e2

---


# Funzionamento di at.js{#how-at-js-works}

Devi utilizzare la libreria at.js per implementare [!DNL Adobe Target] sul lato client.

In un’implementazione lato client di [!DNL Adobe Target], [!DNL Target] consegna le esperienze associate a un’attività direttamente al browser client. Il browser determina quale esperienza visualizzare e la visualizza. Con un’implementazione lato client, puoi utilizzare un editor WYSIWYG (il [Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md)) o un’interfaccia non visiva (il [Compositore esperienza basato su moduli](/help/c-experiences/form-experience-composer.md)) per creare esperienze di test e personalizzazione.

## Che cos’è at.js?

la [libreria at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17) è la nuova libreria di implementazione per Target. La libreria at.js migliora i tempi di caricamento delle pagine per le implementazioni Web e fornisce migliori opzioni di implementazione per le applicazioni a pagina singola. at.js è la libreria di implementazione consigliata e viene aggiornata frequentemente con nuove funzionalità. Si consiglia a tutti i clienti di implementare o eseguire la migrazione alla [versione più recente di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A).

Per ulteriori informazioni, consulta [Librerie JavaScript di Target](/help/c-intro/how-target-works.md#libraries).

Nell’implementazione di [!DNL Target] illustrata di seguito sono implementate le seguenti soluzioni di [!DNL Adobe Experience Cloud]: Analytics, Target e Audience Manager. Inoltre, sono implementati i seguenti servizi principali di Experience Cloud: Adobe Launch, Audiences e Servizio ID visitatore.

## Qual è la differenza tra i flussi di lavoro di at.js 1.*x* e di at.js 2.x?

Consulta [Aggiornamento da at.js 1.x a at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md) per informazioni sulle differenze tra 2.0 e 1.*x*.

Da un punto di vista avanzato, esistono alcune differenze tra le due versioni:

* at.js 2.x non ha un concetto di richiesta mbox globale, ma una richiesta al caricamento della pagina. Una richiesta di caricamento della pagina si può intendere come una richiesta per recuperare il contenuto da applicare al caricamento iniziale della pagina del sito web.
* at.js 2.x gestisce il concetto di Viste utilizzate per le applicazione a pagina singola. In at.js 1.*x* questo concetto non è disponibile.

## Diagrammi at.js 2.x

I seguenti diagrammi ti aiutano a comprendere il flusso di lavoro di at.js 2.x tramite Visualizzazioni e come questo migliori l’integrazione con le applicazioni a pagina singola. Per una migliore introduzione dei concetti utilizzati in at.js 2.x, consulta [Implementazione di un’applicazione a pagina singola](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md).

![Flusso di Target con at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/system-diagram-atjs-20.png)

| Passaggio | Dettagli |
| --- | --- |
| 1 | La chiamata restituisce l&#39;[!DNL Experience Cloud ID] se l’utente è autenticato; un’altra chiamata sincronizza l’ID cliente. |
| 2 | La libreria at.js viene caricata in modo sincrono e nasconde il corpo del documento.<br>at. js possono anche essere caricati in modo asincrono con un snippet facoltativo implementato sulla pagina. |
| 3 | Si effettua una richiesta di caricamento della pagina, con tutti i parametri configurati (MCID, SDID e ID cliente). |
| 4 | Gli script di profilo vengono eseguiti e quindi inseriti nell’archivio profili. L’archivio richiede un pubblico idoneo dalla libreria Pubblico (ad esempio, pubblico condiviso da Adobe Analytics, Audience Manager, ecc.).<br>Gli attributi del cliente vengono inviati all’archivio profili in un processo batch. |
| 5 | In base ai parametri di richiesta dell’URL e ai dati di profilo, [!DNL Target] determina le attività ed esperienze da restituire al visitatore per la pagina corrente e le visualizzazioni future. |
| 6 | Il contenuto di destinazione viene rinviato alla pagina, includendo facoltativamente i valori di profilo per ulteriore personalizzazione.<br>Il contenuto mirato sulla pagina corrente viene mostrato il più rapidamente possibile senza che venga visualizzato momentaneamente il contenuto predefinito.<br>Contenuto mirato per le viste mostrate come risultato delle azioni dell&#39;utente in un’applicazione a pagina singola memorizzata nella cache del browser, in modo da applicarla immediatamente senza una chiamata al server aggiuntiva quando si attivano le viste tramite `triggerView()`. |
| 7 | I dati Analytics vengono inviati ai server di raccolta dati. |
| 8 | I dati di Target vengono confrontati con i dati di Analytics tramite SDID ed elaborati nell’archivio dei rapporti di Analytics.<br>I dati di Analytics possono quindi essere visualizzati sia in Analytics che in Target tramite i rapporti Analytics for Target (A4T). |

Ora, ovunque si implementi `triggerView()` nell’applicazione a pagina singola, le visualizzazioni e le azioni vengono recuperate dalla cache e mostrate all’utente senza una chiamata al server. `triggerView()` invia anche una richiesta di notifica al backend [!DNL Target] per incrementare e registrare i conteggi delle impression. Per ulteriori informazioni su at.js per applicazioni a pagina singola con viste, consulta [Implementazione di un’applicazione a pagina singola](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md).

![Flusso di Target triggerView at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/atjs-20-triggerview.png)

| Passaggio | Dettagli |
| --- | --- |
| 1 | Si richiama `triggerView()` nell’applicazione a pagina singola per eseguire il rendering della visualizzazione e applicare azioni per modificare gli elementi visuali. |
| 2 | Il contenuto mirato per la visualizzazione viene letto dalla cache. |
| 3 | Il contenuto mirato viene mostrato il più rapidamente possibile senza che venga visualizzato momentaneamente il contenuto predefinito. |
| 4 | Si invia la richiesta di notifica all&#39;archivio profili di [!DNL Target] per conteggiare il visitatore nell&#39;attività e nelle metriche incrementali. |
| 5 | Dati di Analytics inviati ai server di raccolta dati. |
| 6 | I dati di Target vengono confrontati con i dati di Analytics tramite SDID e vengono elaborati nell’archivio dei rapporti di Analytics. È quindi possibile visualizzare i dati di Analytics sia in Analytics che in Target tramite i rapporti A4T. |

## Diagramma di at.js 1.x

![](assets/target-flow.png)

| Passaggio | Descrizione | Chiamata | Descrizione |
|--- |--- |--- |--- |
| 1 | La chiamata restituisce l’[!DNL Experience Cloud ID] (MCID) se l’utente è autenticato; un’altra chiamata sincronizza l’ID cliente. | 2 | La libreria at.js viene caricata in modo sincrono e nasconde il corpo del documento. |
| 3 | Viene effettuata una richiesta mbox globale, con tutti i parametri configurati, MCID, SDID e ID cliente (facoltativo). | 4 | Gli script di profilo vengono eseguiti e quindi inseriti nell’archivio profili. L’archivio richiede tipi di pubblico idonei dalla [!UICONTROL libreria Pubblico] (ad esempio, audience condivisi da [!DNL Adobe Analytics], [!DNL Audience Manager], ecc.).<br>Gli attributi del cliente vengono inviati al [!DNL Profile Store] in un processo batch. |
| 5 | In base all’URL, ai parametri mbox e ai dati di profilo, [!DNL Target] decide quali attività ed esperienze restituire al visitatore. | 6 | Il contenuto di destinazione viene rinviato alla pagina, includendo facoltativamente i valori di profilo per ulteriore personalizzazione.<br>L’esperienza viene mostrata il più rapidamente possibile senza che venga visualizzato momentaneamente il contenuto predefinito. |
| 7 | I dati [!DNL Analytics] vengono inviati ai server di raccolta dati. | 8 | I dati di [!DNL Target] vengono confrontati con i dati di [!DNL Analytics] tramite SDID e vengono elaborati nell’archivio dei rapporti di [!DNL Analytics].<br>I dati di [!DNL Analytics] possono quindi essere visualizzati sia in [!DNL Analytics] che in [!DNL Target] tramite i rapporti [!DNL Analytics for Target] (A4T). |

## Video di formazione: diagramma architetturale di at.js 2.x

at.js 2.x migliora il supporto di Adobe Target per le applicazioni a pagina singola e consente l’integrazione con altre soluzioni Experience Cloud. Questo video spiega come sono stati uniti questi elementi.

>[!VIDEO](https://video.tv.adobe.com/v/26250?captions=ita)

See [Understanding how at.js 2.x works](https://helpx.adobe.com/target/kt/using/atjs20-diagram-technical-video-understand.html) for more information.