---
keywords: target documentation change log;documentation updates;new topics;edits;updates
description: In questa pagina sono elencate le modifiche importanti apportate alla documentazione di Adobe Target, ordinate per versioni.
title: Modifiche apportate alla documentazione di Adobe Target.
topic: Standard
uuid: 6fba75e2-0a93-488d-9010-fffa423600c0
translation-type: tm+mt
source-git-commit: 9168a8f14ad45dfc48ad5c314df61ee8c02156d5

---


# Modifiche alla documentazione{#documentation-changes}

This page lists important changes made to the [!DNL Adobe Target] product documentation.

## Adobe Target Standard/Premium 20.2.1 (19 febbraio 2020)

| Data | Argomento | Modifiche |
| --- | --- | --- |
| Maggio 4 | [Domande frequenti sulla generazione di rapporti](/help/c-reports/reporting-frequently-asked-questions.md#uneven) | Sono state aggiunte nuove domande frequenti: &quot;Perché la divisione del traffico tra le mie esperienze non è uniforme nell&#39;attività A/B o MVT?&quot; |
| Aprile 29 | [Problemi noti e problemi risolti](/help/r-release-notes/known-issues-resolved-issues.md) | È stato aggiunto un problema noto per la creazione di rapporti con ordini estremi. |
| Aprile 28 | [Glossario di profili e variabili](/help/c-target/c-visitor-profile/variables-profiles-parameters-methods.md) | Sono state rimosse informazioni sull&#39;utilizzo `user.header('x-forwarded-for')` con i margini AWS più recenti per recuperare gli indirizzi IP degli utenti. Questo comando ora funziona con i bordi AWS più recenti. |
|  | [Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md) | È stata modificata la data della release di Target Standard/Premium (20.4.1) in 6 maggio. |
| Aprile 23 | [CNAME e Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) | Argomento aggiornato. |
| Aprile 22 | [Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md) | È stata aggiunta una nuova sezione: *Modifiche all&#39;API v2 di Stato batch profilo (4 maggio 2020).* |
| Aprile 20 | [Note sulla versione di Target (corrente)](/help/r-release-notes/release-notes.md) | È stata aggiunta una nuova sezione: *Adobe Target Experience Builder: Chat sviluppatore, effettua la migrazione di mbox.js di Adobe Target in at.js.* |
| Aprile 14 | [Host periferici di Whitelist Target](/help/c-implementing-target/c-considerations-before-you-implement-target/white-list-edges.md) | Nuovo argomento. |
| Aprile 10 | [Implementazione di un&#39;applicazione a pagina singola](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md#bp) | È stata aggiunta una nuova sezione: &quot;Best practice di implementazione.&quot; |
| Aprile 7 | [Incremento e affidabilità - Domande frequenti su A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-lift-and-confidence.md#lift-condidence) | Testo aggiornato per &quot;Perché non è possibile visualizzare l&#39;incremento e la confidenza sulle metriche calcolate?&quot; |
| Aprile 2 | [Glossario di profili e variabili](/help/c-target/c-visitor-profile/variables-profiles-parameters-methods.md) | Sono state aggiunte informazioni sull&#39;utilizzo `user.header('x-forwarded-for')` con i margini AWS più recenti per recuperare gli indirizzi IP degli utenti. |
|  | [Aggiornamento da at.js 1.*x* a at.js 2.*x *](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md) | È stata aggiunta la seguente nota:<ul><li>Dopo l’installazione della libreria ECID v4.3.0+ e di at.js 2.*x*, potrai creare attività che si estendono su più domini singoli e tenere traccia degli utenti. È importante notare che questa funzionalità funziona solo dopo la scadenza della sessione.</li></ul> |
| 30 marzo | [Problemi noti e problemi risolti](/help/r-release-notes/known-issues-resolved-issues.md#atjs) | Sono stati aggiunti problemi noti che interessano le versioni di at.js precedenti a at.js 2.2.0. Questo problema causava il monitoraggio dei clic per non riportare le conversioni in Analytics per Target (A4T) quando il codice Adobe Analytics non era presente sugli elementi di pagina. |
|  | [Dettagli sulle versioni di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Sono state aggiunte le seguenti informazioni ai dettagli di at.js versione 2.2.0:<ul><li>È stato risolto un problema che causava il mancato monitoraggio dei clic nel reporting delle conversioni in Analytics per Target (A4T) quando il codice Adobe Analytics non era presente negli elementi di pagina.</li></ul> |
| 25 marzo | [Dettagli sulle versioni di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Sono state aggiunte informazioni sulle seguenti nuove versioni di at.js:<ul><li>at.js versione 2.3.0</li><li>at.js versione 1.8.1</li></ul> |
|  | [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) | Sono state aggiunte le seguenti righe nella sezione &quot;Impostazioni&quot;:<ul><li>cspScriptNonce</li><li>cspStyleNonce</li></ul>È stata aggiunta la seguente sezione:<ul><li>Informativa sulla sicurezza dei contenuti</li></ul> |
| 24 marzo | [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md#impact) | Sono state aggiunte informazioni sugli impatti per i seguenti elementi:<ul><li>Script di profilo basati su 3rdPartyID</li><li>URL QA/Anteprima nei dispositivi iOS</li></ul> |
| 20 marzo | [Note sulla versione (corrente)](/help/r-release-notes/release-notes.md) | Indicato che la release di Target Standard/Premium 20.2.1 sarà il 23 marzo 2020. |
| 13 marzo | [Limiti](/help/r-troubleshooting-target/target-limits.md) | È stato aggiornato il numero di &quot;Audience, riutilizzabili per account.&quot; |
| 12 marzo | [Note sulla versione (corrente)](/help/r-release-notes/release-notes.md#summit) | Sono state aggiunte informazioni di registrazione per l&#39;accesso gratuito alla conferenza online del Summit digitale. |
| 9 marzo | [Privacy](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md) | Sono state aggiunte ulteriori informazioni nella sezione &quot;Sostituzione dell’ultimo ottetto di indirizzi IP&quot;. |
|  | [Utilizzo di attributi con più valori](/help/c-recommendations/c-algorithms/work-with-multi-value-attributes.md) | Esempio di codice aggiornato in *Passa un parametro con più valori in JavaScript*. |
|  | [Attributi di entità personalizzati](/help/c-recommendations/c-products/custom-entity-attributes.md) | È stato aggiunto un esempio di codice in *Utilizzo delle API* in *Implementazione degli attributi* multivalore. |
| 4 marzo | [Attributi del profilo](/help/c-target/c-visitor-profile/profile-parameters.md) | Aggiornato l&#39;intero argomento, con ampie revisioni alla sezione &quot;Best practice&quot;. |
| 21 febbraio | [Note sulla versione (corrente)](/help/r-release-notes/release-notes.md) | Sono state aggiunte informazioni sulla nuova navigazione in Adobe Experience Cloud. |
| 20 febbraio | [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) | Updated the description for the `enabled` setting. Sono state aggiunte informazioni per le seguenti impostazioni: `pageLoadEnabled` e `viewsEnabled`. |
| 19 febbraio | [Note sulla versione](/help/r-release-notes/release-notes.md) | Sono state aggiunte informazioni sulla prossima eliminazione della libreria mbox.js. |
|  | [Geo](/help/c-target/c-audiences/c-target-rules/geo.md) | Aggiunta nota `mboxOverride.browserIp` supportata in at.js 1.*x.* |
|  | [Dettagli sulle versioni di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Testo chiarito che spiega quali versioni di at.js supportate dal team di Target. |
|  | [Note sulla versione](/help/r-release-notes/release-notes.md): 20.2.1 | Questa versione include miglioramenti e correzioni. Consulta le Note sulla versione per saperne di più e trovare i collegamenti verso la relativa documentazione. Questa versione include anche molti aggiornamenti della documentazione. |

## Adobe Target Standard/Premium 20.1.1 (4 febbraio 2020)

| Data | Argomento | Modifiche |
| --- | --- | --- |
| 4 febbraio | [Note sulla versione](/help/r-release-notes/release-notes.md): 20.1.1 | Questa versione include miglioramenti e correzioni. Consulta le Note sulla versione per saperne di più e trovare i collegamenti verso la relativa documentazione. Questa versione include anche molti aggiornamenti della documentazione. |

## Adobe Target Standard/Premium 19.10.1 (22 ottobre 2019)

| Data | Argomento | Modifiche |
| --- | --- | --- |
| 29 gennaio 2020 | [Personalizzare una progettazione con Velocity](/help/c-recommendations/c-design-overview/customizing-a-template.md) | Testo ed esempi di codice aggiornati. I nuovi esempi di codice mostrano come utilizzare i numeri nei modelli Velocity. |
| 28 gennaio 2020 | [Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md) | È stata modificata la data di rilascio di Target Standard/Premium 20.1.1. La data di rilascio è ora il 4 febbraio 2020. |
| 27 gennaio 2020 | [Rapporti Approfondimenti personalizzazione](/help/c-reports/c-personalization-insights-reports/personalization-insights-reports.md) | È stata aggiunta una nuova sezione: &quot;Adobe Blogs.&quot; |
|  | [Limiti](/help/r-troubleshooting-target/target-limits.md) | Sono state aggiunte le seguenti informazioni: &quot;Se utilizzate l&#39;API di consegna batch, il limite è di 50 mbox per ogni richiesta batch.&quot; |
|  | [Risorse e informazioni di contatto](/help/cmp-resources-and-contact-information.md#section_354AC2658BA84A2A96E64C5B2C43B73B) | Collegamento aggiornato per aprire un ticket di supporto. |
|  | [Rapporto di riepilogo del Targeting automatico](/help/c-reports/auto-target-summary-report.md) | Aggiornati testo e immagini. |
| 23 gennaio 2020 | [Interpreta rapporti di allocazione automatica](/help/c-activities/automated-traffic-allocation/determine-winner.md) | È stata aggiunta una nota per utilizzare il calcolatore delle dimensioni del campione di Adobe Target per determinare il vincitore. |
|  | [Attributi di entità](/help/c-recommendations/c-products/entity-attributes.md) | È stata aggiunta una nota in cui si spiega che se si utilizza at.js 2.*x*, `mboxCreate` non è più supportato. Per trasmettere informazioni su prodotti o contenuti a Recommendations utilizzando at.js 2.*x*, use `targetPageParams`. |
| 22 gennaio 2020 | [Allocazione automatica](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Sono state aggiornate le seguenti domande frequenti: &quot;È possibile utilizzare il calcolatore delle dimensioni del campione quando si utilizza Auto-Allocate per stimare quanto tempo l&#39;attività impiegherà per identificare il vincitore?&quot; |
| 15 gennaio 2020 | [Abilitazione di contenuti misti nel browser](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/mixed-content.md) | È stato aggiunto un video di formazione e istruzioni per spiegare come aggiornare le impostazioni del sito per consentire contenuti misti nell&#39;ultima versione di Chrome. |
|  | [Feed](/help/c-recommendations/c-products/feeds.md) | Aggiunta nota sul caricamento e la rimozione di entità e attributi di entità. |
|  | [Domande frequenti sui consigli](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md) | Sono state aggiunte le seguenti domande frequenti: Cosa significa la risposta NO_CONTENT restituita talvolta nella traccia di contenuto di Recommendations? |
|  | [Creare una mbox di conferma d’ordine - mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/orderconfirm-create.md) | È stata aggiunta una nota che spiega come eseguire la conferma dell&#39;ordine utilizzando at.js 2.*x*. |
| 9 gennaio 2020 | [Modifiche alla crittografia di TLS (Transport Layer Security)](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md) | Testo aggiornato.<br>Dopo il 1 marzo 2020, Adobe Target non supporterà più la crittografia TLS 1.1 per Visual Experience Composer (VEC), Enhanced Experience Composer (EEC), distribuzione di attività, API e così via. Per evitare problemi, effettua l&#39;aggiornamento a TLS 1.2 prima del 1 marzo 2020. |
| 6 gennaio 2020 | [Problemi noti e problemi risolti](/help/r-release-notes/known-issues-resolved-issues.md) | È stato aggiunto un problema noto relativo allo stato del feed Criteri personalizzati. |
| 19 dicembre 2019 | [Note sulla versione - Java SDK di destinazione](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md) | Sono state aggiunte informazioni sulla versione 1.1.0. |
| 12 dicembre 2019 | [CNAME e Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) | Aggiornamento della sezione Domande frequenti. |
|  | [Interpreta rapporti di allocazione automatica](/help/c-activities/automated-traffic-allocation/determine-winner.md) | Argomento rinominato e aggiunta la sezione seguente: &quot;Comprendere i rapporti Lift and Confidence nelle attività Auto-Allocate.&quot; |
| 11 dicembre 2019 | [Domande frequenti su destinazioni e pubblico](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md) | Sono state aggiunte nuove domande frequenti: &quot;In che modo Target valuta gli URL nel targeting?&quot; |
| 10 dicembre 2019 | [Limiti di Target](/help/r-troubleshooting-target/target-limits.md) | Aggiornamento della sezione dei parametri mbox. |
|  | [Criteri](/help/c-recommendations/c-algorithms/algorithms.md) | Aggiunta nota sul supporto per la funzione Utilizzo criteri. |
| 5 dicembre 2019 | [Pagine del sito](/help/c-target/c-audiences/c-target-rules/site-pages.md) | Argomento aggiornato. |
| 2 dicembre 2019 | [Usa servizio di localizzazione](/help/c-target-mobile-app/use-location-service.md) | Nuovo argomento. |
| 26 novembre 2019 | [Gestione at.js della visualizzazione momentanea di altri contenuti](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/manage-flicker-with-atjs.md) | Testo aggiornato in &quot;Gestione dello sfarfallio quando si carica at.js in modo asincrono.&quot; |
|  | [Newsletter Target Insider](/help/r-release-notes/target-insider-newsletter.md) | Aggiunto il collegamento alla newsletter di novembre 2019. |
|  | [Utenti](/help/administrating-target/c-user-management/c-user-management/user-management.md) | Testo e immagini aggiornati in &quot;Specificare ruoli e autorizzazioni&quot;. |
| 15 novembre 2019 | [Dieci comuni insidie di test A/B e come evitarle](/help/c-activities/t-test-ab/common-ab-testing-pitfalls.md) | Aggiunto &quot;Pitfall 7: Modifica dell&#39;allocazione del traffico durante il periodo di test.&quot; |
| 11 novembre 2019 | [Note sulla versione - Java SDK di destinazione](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md) | Sono state aggiunte informazioni sulla versione 1.0.1. |
|  | [CNAME e Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) | Intero argomento aggiornato. |
|  | [Geo](/help/c-target/c-audiences/c-target-rules/geo.md#section_DD308A53AF0F48FA8C81423580561FE7) | Sono state aggiunte informazioni che spiegano che [!DNL Target] non archiviano le informazioni geografiche, come i codici ZIP. |
| 8 novembre 2019 | [Newsletter Target Insider](/help/r-release-notes/target-insider-newsletter.md) | Sono stati aggiunti collegamenti ad altri problemi passati. |
|  | [Normative sulla privacy e la protezione dei dati](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md) | Sezione CCPA aggiornata con una nuova nota.<br>Sono state aggiunte nuove domande frequenti per informare i clienti che Target non è in grado di consentire ai clienti di condividere o vendere dati direttamente da Target a terze parti, pertanto non è previsto il rifiuto di vendita per Target. |
| 7 novembre 2019 | [Attributi del profilo](/help/c-target/c-visitor-profile/profile-parameters.md#examples) | È stato aggiunto un esempio di codice per il parametro adobeQA. |
| 5 novembre 2019 | [Pagine del sito](/help/c-target/c-audiences/c-target-rules/site-pages.md#ts) | Testo aggiornato nella sezione &quot;Risoluzione dei problemi&quot;. |
| 4 novembre 2019 | [Domande frequenti su at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/target-atjs-faq.md) | Testo aggiornato con le seguenti domande frequenti: &quot;Perché viene visualizzato un messaggio di avviso, ad esempio &quot;azioni con selettori mancanti&quot;?&quot; |
| 31 ottobre 2019 | [Utilizzo di attributi con più valori](/help/c-recommendations/c-algorithms/work-with-multi-value-attributes.md) | Nuovo argomento. |
|  | [Note sulla versione - Java SDK di destinazione](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md) | Nuovo argomento. |
|  | [Aggiornamento da at.js 1.x a at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md#audience-parameters) | È stata aggiunta una nuova sezione: &quot;Che a.js 1.*I parametri x* per la creazione di audience non sono supportati in at.js 2.*x*?&quot; |
|  | [Problemi noti e problemi risolti](/help/r-release-notes/known-issues-resolved-issues.md) | È stato aggiunto un nuovo problema noto relativo agli spazi aggiuntivi da aggiungere alle regole dei modelli. |
|  | [Note sulla versione di Target (corrente)](/help/r-release-notes/release-notes.md) | Sono state aggiunte informazioni sulla versione di Target Premium 19.10.2 e sulla versione di Target Java SDK. |
| 30 ottobre 2019 | [Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md) | Sono state aggiunte informazioni sulla prossima release di Target Premium 19.10.2 (31 ottobre 2019). |
| 29 ottobre 2019 | [Similarità dei contenuti](/help/c-recommendations/c-algorithms/create-new-algorithm.md#concept_5402DAFA279C4E46A9A449526889A0CB) | Aggiunta nota. |
|  | [Visualizzare l&#39;anteprima e avviare l&#39;attività di Recommendations](/help/c-recommendations/t-create-recs-activity/previewing-and-launching-your-recommendations-activity.md) | Nuovo argomento. |
| 25 ottobre 2019 | [Parametri personalizzati](/help/c-target/c-audiences/c-target-rules/custom-parameters.md#considerations) | È stato aggiunto un nuovo elemento in &quot;Considerazioni&quot; per spiegare che il targeting non viene valutato sui parametri mbox interni. |
|  | [Utilizzare regole di inclusione dinamiche e statiche](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md) | Argomento aggiornato completamente e rimosso gli esempi obsoleti. |
|  | [adobe.target.getOffers(options) - at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) | È stata aggiunta una nota con collegamento alla documentazione API Target Delivery per aiutarti a comprendere i tipi disponibili per le richieste/risposte (array, stringa e così via). |
|  | [adobe.target.getOffers(options) - at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) | È stata aggiunta una nota con collegamento alla documentazione API Target Delivery per aiutarti a comprendere i tipi disponibili per le richieste/risposte (array, stringa e così via). |
|  | [Pagine del sito](/help/c-target/c-audiences/c-target-rules/site-pages.md#ts) | È stata aggiunta la sezione &quot;Risoluzione dei problemi&quot;. |
| 24 ottobre 2019 | [Domande frequenti sui consigli](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md#section_DB3F40673AED42228E407C05437D99E9) | Testo aggiornato nelle seguenti domande frequenti: &quot;Perché a volte Target non è in grado di mostrare le raccomandazioni?&quot; |
|  | [Problemi noti e problemi risolti](/help/r-release-notes/known-issues-resolved-issues.md#atjs) | È stata aggiunta una nota a un problema noto che interessa versioni precedenti di at.js (precedenti alla versione 2.2.0). |
|  | [Metriche di successo](/help/c-activities/r-success-metrics/success-metrics.md) | Aggiunta nota sul comportamento predefinito per le metriche di successo per le attività che utilizzano A4T. |
| 22 ottobre 2019 | [Criteri/algoritmi](/help/c-recommendations/c-algorithms/algorithms.md#criteria-algorithms) | È stata aggiunta una riga per le raccomandazioni basate sull&#39;utente. |
|  | [Criteri](/help/c-recommendations/c-algorithms/algorithms.md#custom-key) | È stata aggiunta una nuova sezione: &quot;Utilizzo di una chiave di raccomandazione personalizzata.&quot; |
|  | [Domande frequenti su Target e audience](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md) | Sono state aggiunte nuove domande frequenti: &quot;Quando si creano stringhe URL complesse, viene [!DNL Target] valutato l’intero URL?&quot; |
|  | [Note sulla versione](/help/r-release-notes/release-notes.md): 19.10.1 | Questa versione include miglioramenti e correzioni. Consulta le Note sulla versione per saperne di più e trovare i collegamenti verso la relativa documentazione. Questa versione include anche molti aggiornamenti della documentazione. |

## Adobe Target/Standard/Premium 19.9.1 (30 settembre 2019)

| Data | Argomento | Modifiche |
| --- | --- | --- |
| 17 ottobre 2019 | [Controllo di qualità delle attività](/help/c-activities/c-activity-qa/activity-qa.md) | Argomento aggiornato per spiegare in che modo il QA dell&#39;attività funziona con i cookie di terze parti. |
|  | [Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md) | Sono state aggiornate le note sulla versione per includere informazioni sulle modifiche alla Shell unificata. |
| 10 ottobre 2019 | [targetGlobalSettings](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#server-state) | È stata aggiunta una nuova sezione: &quot;serverState.&quot; |
|  | [Note sulla versione di Target (corrente)](/help/r-release-notes/release-notes.md) | Sono state aggiunte informazioni sulle versioni at.js 2.2 e at.js 1.8. |
|  | [Dettagli sulle versioni di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Sono state aggiunte informazioni sulle versioni at.js 2.2 e at.js 1.8. |
|  | [Risolvere i problemi relativi alle attività](/help/c-activities/c-troubleshooting-activities/troubleshooting-activities.md) | È stata aggiunta una nuova sezione: &quot;Ho creato un&#39;attività utilizzando l&#39;interfaccia utente di Target e non posso aggiornarla tramite API.&quot; |
| 9 ottobre 2019 | [Lato server: implementare Target](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md) | Argomento aggiornato. |
|  | [Note sulla versione - API lato server di Target](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md) | Nuovo argomento. |
|  | [Note sulla versione - SDK Node.js di destinazione](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md) | Nuovo argomento. |
|  | [Note sulla versione di Target (corrente)](/help/r-release-notes/release-notes.md) | Sono state aggiunte informazioni sulle release V1/Delivery API e Node.js SDK. |
| 8 ottobre 2019 | [Newsletter Target Insider](/help/r-release-notes/target-insider-newsletter.md) | Nuovo argomento con i collegamenti al primo batch di newsletter, con altri argomenti in arrivo. |
| 3 ottobre 2019 | [Problemi noti e problemi risolti](/help/r-release-notes/known-issues-resolved-issues.md) | È stato aggiunto quanto segue: <ul><li>Problema noto e soluzione alternativa durante la creazione di un&#39;esperienza senza modifiche con at.js 2.*x* library.</li><li>Le raccolte, le esclusioni, i criteri e le progettazioni creati mediante API non sono visibili nell’interfaccia di Target e possono essere modificati solo tramite API.</li><li>Le attività Consigli create tramite API sono visibili nell’interfaccia, ma possono essere modificate solo tramite API.</li></ul> |
|  | [Risolvere i problemi relativi alla distribuzione dei contenuti](/help/c-activities/c-troubleshooting-activities/content-trouble.md#mboxdebug) | Aggiunta nota alla sezione &quot;mboxDebug&quot;. |
| 2 ottobre 2029 | [Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md) | Sono state aggiunte informazioni sulle prossime release. |
| 1 ottobre 2019 | [Glossario di profili e variabili](/help/c-target/c-visitor-profile/variables-profiles-parameters-methods.md) | Testo aggiornato nella sezione &quot;Attributi del cliente&quot;. |
|  | [adobe.target.getOffers(options) - at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) | Esempio di codice aggiornato nella sezione &quot;Call getOffers() per tutte le viste&quot;. |
| 30 settembre 2019 | [Note sulla versione](/help/r-release-notes/release-notes.md): 19.9.1 | Questa versione include miglioramenti e correzioni. Consulta le Note sulla versione per saperne di più e trovare i collegamenti verso la relativa documentazione. Questa versione include anche molti aggiornamenti della documentazione. |

## Adobe Target Standard/Premium 19.7.1 (23 luglio 2019) {#tgt-19-7-1}

| Data | Argomento | Modifiche |
| --- | --- | --- |
| 27 settembre 2019 | [Per quanto tempo si deve eseguire un test A/B?](/help/c-activities/t-test-ab/sample-size-determination.md) | Testo aggiornato sul calcolatore delle dimensioni del campione di Target. |
|  | [Allocazione automatica](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Testo aggiornato sul calcolatore delle dimensioni del campione di Target. |
| 24 settembre 2019 | [Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md) | È stata modificata la data della release di Target/Standard 19.2.1 al 30 settembre 2019. |
|  | [Consigli come offerta](/help/c-recommendations/recommendations-as-an-offer.md) | È stato aggiunto un video di formazione. |
| 10 settembre 2019 | [Note sulla versione di Target (corrente)](/help/r-release-notes/release-notes.md) | Sono state aggiunte informazioni sulla versione di Target Standard/Premium 19.9.1. |
| 9 settembre 2019 | [Frammenti di esperienza AEM](/help/c-experiences/c-manage-content/aem-experience-fragments.md#considerations) | Aggiunta la sezione &quot;Considerazioni&quot;. |
|  | [Criteri per cookie SameSite di Google Chrome](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/google-chrome-samesite-cookie-policies.md) | Testo aggiornato per l’intero argomento. |
|  | [Informativa sulla sicurezza dei contenuti (CSP)](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/content-security-policy.md) | Nuovo argomento. |
| 6 settembre 2019 | [Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md) | Sono state aggiunte informazioni sulla versione di Target Standard/Premium 19.9.1 (10 settembre 2019). |
|  | [Domande frequenti su Target per app mobili](/help/c-target-mobile-app/target-for-mobile-apps-faq.md) | Nuovo argomento. |
| 4 settembre 2019 | [CNAME e Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) | Argomento aggiornato. |
| 23 agosto 2019 | [Anteprima mobile di Target](/help/c-target-mobile-app/target-mobile-preview.md) | Snippet di codice aggiornato in `AndroidManifest.xml`. |
|  | [Parametri personalizzati](/help/c-target/c-audiences/c-target-rules/custom-parameters.md#considerations) | È stata aggiunta la sezione: “Considerazioni”. |
|  | [Caricare criteri personalizzati](/help/c-recommendations/c-algorithms/recommendations-csv.md) | È stata aggiornata la seguente frase: “Gli aggiornamenti dei criteri personalizzati sono per impostazione predefinita “cumulativi”.” Le nuove coppie chiave-valore specificate nel file di caricamento CSV sovrascrivono le coppie chiave-valore esistenti. Le coppie chiave-valore esistenti prive di chiavi specificate nel file CSV caricato continueranno a essere disponibili per la consegna e scadranno dopo 31 giorni, a partire dal momento in cui sono state caricate con il file CSV. |
| 20 agosto 2019 | [Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md) | È stata rimandata la versione Target/Premium 19.8.1 (20 agosto 2019). Il contenuto di questa versione verrà introdotto nella versione 19.9.1 (24 settembre 2019). |
|  | [Domande frequenti sulle progettazioni](/help/c-recommendations/c-design-overview/template-faq.md) | Sono state aggiunte le seguenti domande frequenti: “Nel prezzo consigliato dell’articolo non vengono visualizzati i due valori a destra del punto decimale. Come è possibile visualizzarli?” |
| 16 agosto 2019 | [Sincronizzazione dei profili in tempo reale per mbox3rdPartyID](/help/c-target/c-visitor-profile/3rd-party-id.md) | È stata aggiunta la sezione: “Considerazioni”. |
|  | [Creare un’attività di consigli](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md) | È stato aggiunto un video di formazione. |
|  | [Feed](/help/c-recommendations/c-products/feeds.md) | Sono stati aggiunti dei video di formazione. |
|  | [Creare criteri](/help/c-recommendations/c-algorithms/create-new-algorithm.md) | È stato aggiunto un video di formazione. |
|  | [Caricare criteri personalizzati](/help/c-recommendations/c-algorithms/recommendations-csv.md) | È stato aggiunto un video di formazione. |
|  | [Creare sequenze di criteri](/help/c-recommendations/c-algorithms/create-criteria-sequence.md) | È stato aggiunto un video di formazione. |
|  | [Creare una progettazione](/help/c-recommendations/c-design-overview/create-design.md) | È stato aggiunto un video di formazione. |
|  | [Raccolte](/help/c-recommendations/c-products/collections.md) | È stato aggiunto un video di formazione. |
|  | [Esclusioni](/help/c-recommendations/c-products/exclusions.md) | È stato aggiunto un video di formazione. |
| 14 agosto 2019 | [CNAME e Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) | È stato aggiornato il testo ed è stato aggiunto un video di formazione. |
|  | [adobe.target.getOffers(options) - at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) | Sono state rese più chiare le informazioni sulla `consumerID`. |
|  | [Opzioni del Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#move) | Sono state aggiornate le informazioni riportate nella sezione “Layout > Sposta”. |
| 12 agosto 2019 | [Modificare un’attività o salvarla come bozza](/help/c-activities/edit-activity.md#classic) | È stata aggiunta la sezione: “Utilizzare le attività legacy create in Recommendations Classic”. |
| 9 agosto 2019 | [Funzionamento di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md#render) | È stata aggiunta la sezione: “Come avviene il rendering delle offerte con contenuti HTML in at.js”. |
|  | [Opzioni del Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#considerations) | È stata aggiunta la sezione: “Considerazioni”. |
| 7 agosto 2019 | [Preacquisire il contenuto dell’offerta](/help/c-target-mobile-app/prefetch-offer-content.md) | È stata aggiunta una nota sul fatto che la funzionalità di preacquisizione negli SDK non è supportata per le attività di tipo Targeting automatico, Allocazione automatica e Personalizzazione automatizzata. |
|  | [Risolvere i problemi relativi all’integrazione di Analytics e Target (A4T)](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md#unspecified) | È stata aggiunta una nota che indica il tempo necessario al completamento del processo di classificazione. |
|  | [Visualizzare i rapporti - Domande frequenti su A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md#unspecified) | È stata aggiunta una nota che indica il tempo necessario al completamento del processo di classificazione. |
|  | [Normative sulla privacy e la protezione dei dati](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md) | L’argomento è stato aggiornato per includere informazioni sul California Consumer Privacy Act (CCPA). |
|  | [Visualizzare i rapporti - Domande frequenti su A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md#metrics) | È stata aggiornata una considerazione sull’utilizzo di metriche [!UICONTROL Impression attività] e [!UICONTROL Conversioni attività] in [!DNL Analysis Workspace]. |
| 1 agosto 2019 | [Note sulla versione di Target (corrente)](/help/r-release-notes/release-notes.md) | È stato aggiunto un annuncio importante riguardo il supporto API per le autorizzazioni Enterprise. |
|  | [Consentire alle integrazioni Adobe I/O di accedere alle aree di lavoro e assegnare ruoli](/help/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md) | Nuovo argomento. |
| 31 luglio 2019 | [Introduzione alla funzione Consigli](/help/c-recommendations/introduction-to-recommendations.md) | Nuovo argomento. |
|  | [Creare criteri](/help/c-recommendations/c-algorithms/create-new-algorithm.md#recently-viewed) | È stata aggiunta una nota sugli articoli visualizzati di recente. |
|  | [Problemi noti e problemi risolti](/help/r-release-notes/known-issues-resolved-issues.md#preview) | È stato aggiunto un problema noto in merito ai collegamenti di anteprima Controllo di qualità delle attività. |
| 29 luglio 2019 | [Domande frequenti sulla generazione di rapporti](/help/c-reports/reporting-frequently-asked-questions.md) | È stata aggiunta una nuova domanda: “ Perché i miei rapporti [!UICONTROL Targeting esperienze] (XT) contengono metriche per le esperienze di controllo?” |
| 24 luglio 2019 | [Aggiornamento da at.js 1.*x* a at.js 2.*x *](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md) | È stata aggiunta la sezione: [Supporto del tracciamento tra più domini in at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md#cross-domain) |
|  | [Apple Intelligent Tracking Prevention (ITP) 2.*x *](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md) | Nuovo argomento. |
|  | [Consigli come offerta](/help/c-recommendations/recommendations-as-an-offer.md#status) | È stata aggiunta la sezione: “Visualizzazione dello stato di un’offerta Consigli”. |
|  | [Feed](/help/c-recommendations/c-products/feeds.md) | È stata aggiornata la riga “Importazione elementi” ed è stata aggiunta la riga “Feed importato correttamente alle *ora*” in [Status dei feed](/help/c-recommendations/c-products/feeds.md#status). |
|  | [Ricerca nel catalogo](/help/c-recommendations/c-products/catalog-search.md) | È stato aggiornato il testo su come si aggiorna il catalogo. |
|  | [Come funziona Adobe Target](/help/c-intro/how-target-works.md#bots) | È stata aggiunta la sezione: “Bot”. |
|  | [Attributi del profilo](/help/c-target/c-visitor-profile/profile-parameters.md#best) | Sono state aggiunte le best practice per evitare un’esecuzione lenta delle espressioni regex. |
|  | [Feed](/help/c-recommendations/c-products/feeds.md#steps) | Ai passaggi sono state aggiunte le impostazioni del server FTP supportate. |
|  | [Dettagli sulle versioni di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Nuove informazioni su at.js 2.1.1. |
|  | [Note sulla versione](/help/r-release-notes/release-notes.md): 19.7.1 | Questa versione include miglioramenti e correzioni. Consulta le Note sulla versione per saperne di più e trovare i collegamenti verso la relativa documentazione. Questa versione include anche molti aggiornamenti della documentazione. |

## Adobe Target Standard/Premium 19.6.1 (26 giugno 2019) {#tgt-19-6-1}

| Data | Argomento | Modifiche |
| --- | --- | --- |
| 10 luglio 2019 | [Limiti](/help/r-troubleshooting-target/target-limits.md) | Sono state aggiunte informazioni sui limiti per i seguenti elementi:<ul><li>Numero di esperienze per attività.</li><li>Numero di metriche di successo per attività.</li><li>Numero di tipi di pubblico/segmenti di reporting per attività.</li><li>Numero di tipi di pubblico per mbox, metrica ed esperienza.</li><li>Numero di valori univoci per regola di targeting.</li><li>Numero di tipi di pubblico univoci per regola di targeting.</li><li>Numero di regole di targeting univoche per attività.</li><li>Numero di script di profilo attivi.</li><li>Numero di script di profilo totali.</li><li>Numero di loop totali per script di profilo.</li><li>Numero di attività live.</li><li>Numero di attività salvate (e non terminate) attive.</li><li>Numero di proprietà.</li><li>Numero di offerte.</li></ul> |
|  | [Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md) | Sono state aggiunte informazioni sulla prossima versione di Target 19.7.1 (23 luglio 2019).<br>Tieni presente che queste informazioni sono soggette a modifiche. |
| 8 luglio 2019 | [CNAME e Adobe Target](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) | Sono state aggiunte informazioni che spiegano perché utilizzare CNAME. |
| 28 giugno 2019 | [Problemi noti e problemi risolti](/help/r-release-notes/known-issues-resolved-issues.md#redirect)<br>[Varianze di dati previste tra Target e Analytics durante l’utilizzo con e senza A4T](/help/c-integrating-target-with-mac/a4t/understanding-expected-data-variances.md)<br>[Offerte di reindirizzamento - Domande frequenti su A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md) | Sono state aggiunte informazioni su un problema noto a causa del quale un numero limitato di clienti con reindirizzamenti A4T ottengono una percentuale più alta di hit non uniti. |
| 26 giugno 2019 | [Opzioni del Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#styles) | Sono state aggiunte informazioni sull’opzione [!UICONTROL Sfondo] in *Stili*. |
|  | [Compositore esperienza visivo per app a pagina singola](/help/c-experiences/spa-visual-experience-composer.md) | Sono state aggiunte informazioni sull’azione [!UICONTROL Clona]. |
|  | [Tracciamento dei clic](/help/c-activities/r-success-metrics/click-tracking.md) | Sono state aggiunte informazioni sul pannello [!UICONTROL Elementi selezionati]. |
|  | [Compositore esperienza visivo per app a pagina singola](/help/c-experiences/spa-visual-experience-composer.md#page-delivery-settings) | Nuova sezione: “Impostazioni Consegna pagine per Compositore esperienza visivo per applicazioni a pagina singola” |
|  | [Selezionare il controllo per un’attività di Personalizzazione automatizzata o Targeting automatico](/help/c-activities/t-automated-personalization/experience-as-control.md) | Nuovo argomento. |
|  | [Criteri per cookie SameSite di Google Chrome](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/google-chrome-samesite-cookie-policies.md) | Nuovo argomento. |
|  | [Raccolta di dati per gli algoritmi di personalizzazione Target](/help/c-activities/t-automated-personalization/ap-data.md) | Sono state aggiunte nuove tabelle per spiegare i singoli attributi e fornire esempi. |
|  | [Domande frequenti sulla Personalizzazione automatizzata](/help/c-activities/t-automated-personalization/automated-personalization-faq.md) | È stata aggiunta una nuova domanda: “Posso specificare un’esperienza specifica da usare come controllo?”<br>È stata modificata la domanda: “Quali sono le best practice per impostare un’attività di Personalizzazione automatizzata?” |
|  | [Targeting automatico](/help/c-activities/auto-target-to-optimize.md) | Sono state aggiunte informazioni e una domanda su come specificare un’esperienza specifica da utilizzare come controllo.<br>È stata aggiornata la sezione “Determinazione dell’allocazione del traffico”. |
|  | [Creare un’attività di personalizzazione automatizzata](/help/c-activities/t-automated-personalization/create-ap-activity.md) | È stato aggiunto un passaggio con informazioni per selezionare un’esperienza specifica come predefinita. |
|  | [Problemi noti e problemi risolti](/help/r-release-notes/known-issues-resolved-issues.md) | Sono state aggiunte informazioni sui rapporti che, in alcune situazioni, non vengono generati per le attività di Targeting automatico. |
|  | [Note sulla versione](/help/r-release-notes/release-notes.md): 19.6.1 | Questa versione include miglioramenti e correzioni. Consulta le Note sulla versione per saperne di più e trovare i collegamenti verso la relativa documentazione. Questa versione include anche molti aggiornamenti della documentazione. |

## Adobe Target Standard/Premium 19.5.1 (21 maggio 2019) {#tgt-19-5-1}

| Data | Argomento | Modifiche |
| --- | --- | --- |
| 19 giugno 2019 | [Aggiungere promozioni](/help/c-recommendations/t-create-recs-activity/adding-promotions.md) | Sono state aggiunte informazioni sulla deduplicazione delle promozioni rispetto agli articoli consigliati in base ai criteri per l’attività. |
| 13 giugno 2019 | [Rapporto Attributi importanti](/help/c-reports/c-personalization-insights-reports/important-attributes-report.md) | È stata aggiunta la nuova domanda: “Perché alcune offerte/esperienze con un tasso di conversione inferiore ricevono una maggiore quantità di traffico rispetto ad altre per un determinato segmento automatizzato?” |
|  | [Come funziona Adobe Target](/help/c-intro/how-target-works.md) | È stata aggiunta una nota importante sull’utilizzo di Target in Cina. |
|  | [Browser supportati](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md) | È stato rimosso Microsoft Internet Explorer 11 (IE 11) dalla sezione “Interfaccia di Target Standard/Premium”. Target non supporta né mantiene più la compatibilità per IE 11. Questa modifica interessa solo l’interfaccia utente di Target. Non incide sulla distribuzione dei contenuti. Questa modifica segue annunci simili pubblicati per Adobe Analytics, Adobe Experience Platform e Adobe Audience Manager. Consigliamo agli utenti di passare a un browser supportato. |
| 11 giugno 2019 | [Creazione di attività](/help/c-integrating-target-with-mac/a4t/campaign-creation.md) | È stata rimossa la nota che indicava che non è necessario specificare un server di tracciamento se si utilizza A4T. |
|  | [Attività](/help/c-activities/activities.md) | È stato messo in evidenza il fatto che non è possibile ripristinare un’attività eliminata. Come best practice, invece di eliminare un’attività puoi archiviarla in modo da poter eventualmente recuperarla. |
|  | [Aggiornamento da at.js 1.x a at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md) | È stata rimossa la limitazione che indica che Experience Cloud Debugger non è del tutto supportato in at.js 2.x |
| 7 giugno 2019 | [Personalizzare una progettazione con Velocity](/help/c-recommendations/c-design-overview/customizing-a-template.md#default) | È stata aggiunta una nuova sezione: “Scenario: creare una progettazione predefinita di Recommendations 4x2 con logica di null-checking” |
|  | [Video di formazione su Adobe Target Standard e Premium](/help/c-intro/target-standard-premium-training-videos.md#tutorials) | È stato aggiornato il collegamento al nuovo sito dedicato alle esercitazioni per Adobe Target. |
| 6 giugno 2019 | [adobe.target.triggerView (viewName, options) - at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-triggerview-atjs-2.md) | È stata aggiornata la descrizione del parametro `options > page`. |
|  | [Primi passaggi per l’amministratore](/help/administrating-target/start-target.md) | È stato aggiornato l’intero articolo. |
|  | [Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md) | Sono state aggiunte note sulla versione preliminare per Target 19.6.1. |
|  | [Aggiornamento da at.js 1.x a at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md) | Sono state aggiornate le informazioni sull’implementazione di at.js con Adobe Launch, che rappresenta il metodo di implementazione preferito. |
|  | [Concetti chiave di Target](/help/c-intro/target-key-concepts.md) | Modifiche di testo minori. |
| 3 giugno 2019 | [Note sulla versione (corrente)](/help/r-release-notes/release-notes.md) | Sono state aggiunte informazioni sulla prossima versione di at.js 2.1.0. |
|  | [Dettagli sulle versioni di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Sono state aggiunte informazioni sulla prossima versione di at.js 2.1.0. |
|  | [Prima dell’implementazione](/help/c-integrating-target-with-mac/a4t/before-implement.md) | È stata aggiunta una nuova sezione: “Registrazione Analytics lato client” |
|  | [Implementazione di Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) | È stato rivisto il Passaggio 7. |
|  | [adobe.target.getOffers(options) - at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) | Sono state aggiunte delle righe alla tabella per i seguenti nomi di campo:<ul><li>Request > experienceCloud</li><li>Request > experienceCloud > analytics</li><li>Request > experienceCloud > analytics > logging</li></ul> |
|  | [Funzioni di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md) | È stata aggiunta una riga alla tabella per `adobe.target.sendNotifications(options)`. |
|  | [adobe.target.sendNotifications(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe.target.sendnotifications-atjs-21.md) | Nuovo argomento. |
|  | [Aggiornamento da at.js 1.x a at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md#integrations) | Sono state aggiunte informazioni sul supporto di Adobe Opt-in in at.js 2.1.0. |
|  | [Privacy e Regolamento generale sulla protezione dei dati (RGPD)](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md) | Sono state aggiunte informazioni sul supporto di Opt-in in at.js 2.1.0. |
| 31 maggio 2019 | [Mobile](/help/c-target/c-audiences/c-target-rules/mobile.md) | È stata aggiunta una nota relativa al targeting di dispositivi con iOS 12.2. |
|  | [Pianificare e implementare la funzione Consigli](/help/c-recommendations/plan-implement.md) | Esempio di codice aggiornato. |
| 30 maggio 2019 | [Accedere a Target da Adobe Experience Cloud](/help/c-intro/target-access-from-mac.md#doc-lang) | La documentazione è ora disponibile in cinese semplificato. |
|  | [Download di dati in un file CSV](/help/c-reports/downloading-data-in-csv-file.md) | È stata aggiunta una nuova nota nella sezione “Esportare i dettagli ordine in CSV”: “I tipi di pubblico applicati nell’interfaccia utente di Target per la generazione di rapporti non vengono trasferiti al rapporto scaricato.” |
|  | [Impostazioni dei rapporti](/help/c-reports/c-report-settings/report-settings.md) | Sono state aggiornate le videate. |
| 29 maggio 2019 | [Affinità tra categorie](/help/c-target/c-visitor-profile/category-affinity.md) | È stato aggiornato il testo per chiarire la differenza `user.categoryId` tra e `entity.categoryId`. |
|  | [Migrare da mbox.js a at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md) | La sezione è stata riposizionata in questo argomento: “Vantaggi di at.js” |
|  | [Domande frequenti su at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/target-atjs-faq.md) | La sezione è stata riposizionata in questo argomento: “Qual è l’impatto di at.js e mbox.js sui tempi di caricamento delle pagine?” |
|  | [Trasmettere i dati dinamici nelle offerte](/help/c-experiences/c-manage-content/passing-profile-attributes-to-the-html-offer.md) | È stata corretta la sintassi nella riga Comportamento passato. |
| 28 maggio 2019 | [Accedere a Target da Adobe Experience Cloud](/help/c-intro/target-access-from-mac.md#doc-lang) | È stata aggiunta una nuova sezione: “Modificare la lingua per la documentazione di Target”. |
|  | [Determinare un vincitore](/help/c-activities/automated-traffic-allocation/determine-winner.md) | Sono state aggiornate le informazioni sui valori p. |
|  | [Risoluzione dei problemi relativi al Compositore esperienza visivo e al Compositore esperienza avanzato](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md) | È stata aggiunta una sezione sulla risoluzione di problemi relativa a come Target gestisce gli iframe a più livelli. |
|  | [Domande frequenti sui consigli](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md) | È stata aggiunte una nuova domanda: “Qual è il tempo di assimilazione previsto per le operazioni di Recommendations?” |
|  | [Implementare Target con Adobe Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md) | Sono state aggiornate le informazioni nella sezione “Vantaggi dell’implementazione di at.js con Target Launch Extension”. |
|  | [Risolvere i problemi relativi alla distribuzione dei contenuti](/help/c-activities/c-troubleshooting-activities/content-trouble.md) | È stata aggiunta nuova sezione sulla risoluzione di problemi relativa alla mancata attivazione delle mbox da parte di at.js se si utilizza un doctype non valido. |
| 24 maggio 2019 | [Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md) | Nuove informazioni su at.js 2.1.0. |
| 23 maggio 2019 | [Gestire le esclusioni](/help/c-activities/t-automated-personalization/managing-exclusions.md) | Sono state aggiunte informazioni e collegamenti su come limitare quali tipi di pubblico possono vedere offerte specifiche nelle attività di Personalizzazione automatizzata mediante regole di targeting. |
|  | [Lato server: implementare Target](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md) | È stato aggiornato il testo introduttivo. |
|  | [Esperienze e offerte](/help/c-experiences/experiences.md) | È stato aggiornato il testo introduttivo. |
|  | [Tipi di pubblico](/help/c-target/target.md) | È stato aggiornato il testo introduttivo. |
|  | [Metriche di successo](/help/c-activities/r-success-metrics/success-metrics.md) | È stato aggiornato il testo introduttivo. |
|  | [Rapporti](/help/c-reports/reports.md) | È stato aggiornato il testo introduttivo. |
|  | [Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) | È stato aggiornato il testo introduttivo. |
|  | [Compositore esperienza basato su moduli](/help/c-experiences/form-experience-composer.md) | È stato aggiornato il testo introduttivo. |
|  | [autorizzazioni per gli utenti Enterprise](/help/administrating-target/c-user-management/property-channel/property-channel.md) | È stato aggiornato il testo introduttivo. |
|  | [Glossario](/help/c-intro/glossary.md) | Sono state aggiunte e aggiornate diverse voci. |
| 22 maggio 2019 | [Introduzione a Target](/help/c-intro/intro.md#kit) | È stato aggiunto un collegamento per il kit di benvenuto di Adobe Target. |
| 21 maggio 2019 | [Compositore esperienza visivo per app a pagina singola](/help/c-experiences/spa-visual-experience-composer.md) | <ul><li>Sono state aggiornate le informazioni sull’opzione “Sposta”.</li><li>È stata aggiunta una nota sulla possibilità di eseguire molte azioni prima che la pagina si carichi nel Compositore esperienza visivo, anche nel caso in cui non sia possibile caricare la pagina. </li></ul> |
|  | [Utenti](/help/administrating-target/c-user-management/c-user-management/user-management.md) | Sono stati aggiornati testo e immagini ed è stato aggiunto un video di formazione. |
|  | [Configurare le autorizzazioni Enterprise](/help/administrating-target/c-user-management/property-channel/properties-overview.md) | Sono stati aggiornati testo e immagini. |
|  | [Limiti](/help/r-troubleshooting-target/target-limits.md) | È stato aggiunto il limite di caratteri per l’ID dell’alias dell’attributo cliente. |
|  | [Note sulla versione](/help/r-release-notes/release-notes.md): 19.5.1 | Questa versione include miglioramenti e correzioni. Consulta le Note sulla versione per saperne di più e trovare i collegamenti verso la relativa documentazione. Questa versione include anche molti aggiornamenti della documentazione. |

## Adobe Target Standard/Premium 19.4.2 (30 aprile 2019) {#target-19-4-2}

**Nota**: la versione 19.4.1 di Target Standard/Premium era una versione di manutenzione per aggiornare l’interfaccia utente di Adobe Experience Cloud in modo da riflettere le modifiche di branding e prodotto.

| Data | Argomento | Modifiche |
| --- | --- | --- |
| 15 maggio 2019 | [Implementazione di un&#39;applicazione a pagina singola](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md#triggerview) | È stata aggiunta una nota sulla necessità di attivare gli eventi `at-view-start` e `at-view-end`. |
|  | [Trasmettere i dati dinamici nelle offerte](/help/c-experiences/c-manage-content/passing-profile-attributes-to-the-html-offer.md) | Testo aggiornato. |
| 13 maggio 2019 | [Controllo di qualità delle attività](/help/c-activities/c-activity-qa/activity-qa.md) | È stato aggiunta una voce all’elenco delle considerazioni sull’utilizzo della modalità di controllo qualità in un’attività multipagina. |
|  | [Includere la stessa esperienza in pagine simili](/help/c-experiences/c-visual-experience-composer/temtest.md) | Sono stati aggiornati i passaggi, in linea con l’interfaccia utente. |
|  | [Domande frequenti su at.js ](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/target-atjs-faq.md) | È stata aggiunta una nuova domanda frequente: “Quale doctype HTML richiede at.js?” |
| 10 maggio 2019 | [Preferenze](/help/administrating-target/r-target-account-preferences/target-account-preferences.md) | Aggiornati testo e immagine. |
|  | [Controllo di qualità delle attività](/help/c-activities/c-activity-qa/activity-qa.md) | Testo aggiornato. |
| 9 maggio 2019 | [Generazione di rapporti per A4T](/help/c-integrating-target-with-mac/a4t/reporting.md#reports-in-analysis-workspace) | È stata aggiunta una nuova sezione: “Rapporti in Analysis Workspace”. |
|  | [Visualizzare i rapporti - Domande frequenti su A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md) | È stata aggiunta una nuova domanda frequente: “Posso visualizzare i dati di attività Target in Adobe Analysis Workspace?” |
|  | [Autorizzazioni per gli utenti Enterprise](/help/administrating-target/c-user-management/property-channel/property-channel.md#faqs) | È stata aggiunta una nuova domanda frequente: “Se una pagina di reindirizzamento e l’URL attività appartengono a proprietà diverse, vengono registrate le conversioni con tracciamento dei clic?” |
| 8 maggio 2019 | [Video di formazione su Adobe Target Standard e Premium](/help/c-intro/target-standard-premium-training-videos.md) | Contenuto e collegamenti aggiornati. |
|  | [Attributi di entità](/help/c-recommendations/c-products/entity-attributes.md) | Testo aggiornato nella nota sotto la variabile `entity.id`. |
| 1 maggio 2019 | [Attributi di entità](/help/c-recommendations/c-products/entity-attributes.md) | Sono state corrette le maiuscole nei seguenti nomi di variabili:<br>`pageURL` è stato modificato in `pageUrl`.<br>`thumbnailURL` è stato modificato in `thumbnailUrl`. |
| 30 aprile 2019 | [Opzioni del Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/viztarget-options.md) | <ul><li>È stata aggiunta una nuova sezione: “Stili”</li><li>È stata aggiunta una tabella con l’elenco dei tag HTML5 che possono essere nidificati.</li></ul> |
|  | [Tracciamento dei clic](/help/c-activities/r-success-metrics/click-tracking.md) | Sono state aggiunte informazioni sulla funzionalità di percorso DOM alla sezione “Considerazioni”. |
|  | [Indicatori e stato di feed](/help/c-recommendations/c-products/feeds.md#section_5DDC2DECF70A42FDAFF2235E91371537) | È stata aggiornata la tabella “Stati di feed”. |
|  | [Utilizzare i contenuti della libreria](/help/c-experiences/c-manage-content/assets-working.md) | Sono state aggiunte informazioni sull’eliminazione di cartelle e immagini dalla libreria Assets. |
|  | [Note sulla versione](/help/r-release-notes/release-notes.md): 19.4.2 | Questa versione include miglioramenti e correzioni. Consulta le Note sulla versione per saperne di più e trovare i collegamenti verso la relativa documentazione. Questa versione include anche molti aggiornamenti della documentazione. |

## Adobe Target Standard/Premium 19.3.1 (29 marzo 2019) {#section-19-3-1}

| Data | Argomento | Modifiche |
| --- | --- | --- |
| 29 aprile 2019 | [Autorizzazioni per gli utenti Enterprise](/help/administrating-target/c-user-management/property-channel/property-channel.md#section_31D3450ADEAE4A29963A34F8E8C19FE0) | È stata aggiunta una nuova domanda frequente: “Perché viene visualizzato un messaggio di errore a indicare che nessuna proprietà è associata a questa attività, anche se è stata assegnata una proprietà?” |
| 24 aprile 2019 | [Aggiornamento da at.js 1.x a at.js 2.x ](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md#types) | È stata aggiunta una nota alla sezione “Tipi di attività”. |
|  | [Test AdBox di un&#39;immagine per e-mail](/help/c-implementing-target/c-non-javascript-based-implementation/testing-email-image-adbox.md) | Esempio di codice riformattato. |
|  | [Controllo di qualità delle attività](/help/c-activities/c-activity-qa/activity-qa.md) | Sono stati corretti errori minori. |
| 23 aprile 2019 | [Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md) | Sono state aggiornate le note sulla versione e la data è stata cambiata da 29 aprile a 30 aprile. |
| 22 aprile 2019 | [Accedere a Target da Adobe Experience Cloud](/help/c-intro/target-access-from-mac.md) | È stata aggiunta una nuova sezione: “Modificare la lingua predefinita per l’interfaccia utente di Target”. |
| 19 aprile 2019 | [Rapporto Segmenti automatizzati](/help/c-reports/c-personalization-insights-reports/automated-segments-report.md#section_740910A52FA646B4AC9452F98C2F5719) | È stata aggiunta una nuova domanda frequente: “Esiste una logica per l’ordine di visualizzazione degli attributi in una scheda segmenti?” |
|  | [Feed](/help/c-recommendations/c-products/feeds.md#section_5DDC2DECF70A42FDAFF2235E91371537) | È stata aggiunta una nota importante che descrive la scadenza delle entità caricate. |
| 16 aprile 2019 | [Visualizzare i rapporti - Domande frequenti su A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md) | È stata aggiunta una nuova domanda frequente: “Posso cambiare la percentuale di allocazione del traffico in un’attività che utilizza A4T dopo che l’attività è stata attivata?” |
| 15 aprile 2019 | [Provisioning iniziale - Domande frequenti su A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-initial-provisioning.md) | È stata aggiunta una nuova domanda frequente: “Come posso impostare un’attività A4T con più pagine?” |
|  | [Requisiti delle autorizzazioni utente](/help/c-integrating-target-with-mac/a4t/account-reqs.md) | Argomento aggiornato. |
|  | [Problemi noti e problemi risolti](/help/r-release-notes/known-issues-resolved-issues.md) | I problemi noti relativi ai gruppi di esclusione sono stati spostati nella tabella dei problemi risolti. |
| 11 aprile 2019 | [adobe.target.getOffers(options) - at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) | Sono stati aggiornati gli esempi di codice. |
|  | [Estensione Adobe Target VEC Helper](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) | Sono state aggiunte delle schermate. |
|  | [Allocazione automatica](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | È stata aggiunta una nuova domanda frequente: “È necessario rimuovere un’esperienza insoddisfacente da un’attività di allocazione automatica per velocizzare il processo di determinazione di un vincitore?” |
| 10 aprile 2019 | [Prima dell’implementazione](/help/c-integrating-target-with-mac/a4t/before-implement.md) | Sono stati apportati aggiornamenti minori alla sezione “Requisiti di implementazione” (i requisiti sono stati riordinati). |
|  | [adobe.target.triggerView (viewName, options) - at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-triggerview-atjs-2.md) | È stato aggiornato il testo per il parametro “options > page”. |
| 8 aprile 2019 | [Varianze di dati previste tra Target e Analytics durante l’utilizzo con e senza A4T](/help/c-integrating-target-with-mac/a4t/understanding-expected-data-variances.md) | È stata aggiornata la [Varianza dei dati prevista quando si utilizza A4T](/help/c-integrating-target-with-mac/a4t/understanding-expected-data-variances.md#expected-using-a4t). |
|  | [Minimizzare i conteggi gonfiati per visite e visitatori in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md) | Sono state aggiornate le informazioni su A4T e reindirizzamenti in [Cosa contribuisce ai dati parziali?](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#section_C9C906BEAA7D44DAB9D3C03932A2FEB8) |
|  | [Prima dell’implementazione](/help/c-integrating-target-with-mac/a4t/before-implement.md#section_A0D2EF18033D4C3997B08A6EBB34C17A) | Sono stati aggiornati i requisiti minimi per l’utilizzo di A4T con reindirizzamenti (at.js versione 1.6.2). |
|  | [Offerte di reindirizzamento - Domande frequenti su A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#section_FA9384C2AA9D41EDBCE263FFFD1D9B58) | <ul><li>Sono stati aggiornati i requisiti minimi per l’utilizzo di A4T con reindirizzamenti (at.js versione 1.6.2).</li><li>Sono state aggiunte informazioni che descrivono il modo di conteggio delle metriche dei dati quando si verifica un hit di Target, ma non si verifica alcun hit di Analytics. </li> |
|  | [Limiti](/help/r-troubleshooting-target/target-limits.md#excludedid) | Sono state aggiunte informazioni sui limiti per il parametro mbox di `excludedIDs`. |
|  | [Aggiornamento da at.js 1.x a at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md#response-tokens) | È stata aggiunta una nuova sezione: Token di risposta. |
| 5 aprile 2019 | [Webinar sulle nozioni di base di Adobe Target: introduzione alla funzione Consigli](/help/c-recommendations/recommendations.md#intro-to-recs) | È stato aggiunto un collegamento alla registrazione del webinar “Introduzione alla funzione Consigli”. |
|  | [Bookmarklet di controllo qualità delle attività](/help/c-activities/c-activity-qa/activity-qa-bookmark.md) | È stato aggiornato il codice JavaScript per il bookmarklet di controllo qualità delle attività. |
|  | [Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md) | Sono state aggiornate le note sulla versione preliminari per le versioni 19.4.1 e 19.4.2 di Target, entrambe pianificate per aprile 2019. |
| 4 aprile 2019 | [Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md) | Sono state aggiunte le note sulla versione preliminari per le versioni 19.4.1 e 19.4.2 di Target, entrambe pianificate per aprile 2019. |
| 30 marzo 2019 | [Limiti](/help/r-troubleshooting-target/target-limits.md#excludedid) | Sono state aggiunte informazioni sui limiti per il parametro mbox di `excludedID`. |
| 29 marzo 2019 | [Problemi noti e problemi risolti](/help/r-release-notes/known-issues-resolved-issues.md) | È stato aggiunto il seguente problema noto: “Per i siti Web delle applicazioni a pagina singola (SPA), l’annullamento del caricamento non consente di modificare le azioni nel pannello [!UICONTROL Modifiche]”.<br>Il seguente problema noto è stato spostato nella sezione Problemi risolti: “La versione v1 delle API per le offerte su Adobe I/O considera tutte le offerte create tramite Target come nell’area di lavoro predefinita.” |
| 28 marzo 2019 | [Compositore esperienza visivo (VEC)](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) | Sono state aggiunte le seguenti nuove sezioni:<ul><li>[Annullare il caricamento di una pagina all’interno del Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md#cancel-loading)</li><li>[Modificare una pagina durante il suo caricamento o dopo il suo mancato caricamento](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md#loading)</li></ul> |
|  | [Opzioni del Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/viztarget-options.md) | Nuova sezione: “[Navigare tra gli elementi utilizzando il percorso DOM](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path).” |
|  | [Problemi noti e problemi risolti](/help/r-release-notes/known-issues-resolved-issues.md#cancel) | È stato aggiunto un problema noto relativo all’annullamento del caricamento di una pagina nel Compositore esperienza visivo. |
|  | [Note sulla versione](/help/r-release-notes/release-notes.md): 19.3.1 | Questa versione include miglioramenti e correzioni. Consulta le Note sulla versione per saperne di più e trovare i collegamenti verso la relativa documentazione. Questa versione include anche molti aggiornamenti della documentazione. |

## Adobe Target Standard/Premium 19.2.1 (19 febbraio 2019) {#section-19-2-1}

| Data | Argomento | Modifiche |
| --- | --- | --- |
| 20 marzo 2019 | [Domande frequenti su at.js ](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/target-atjs-faq.md) | È stata aggiornata la seguente domanda frequente: “[Posso caricare la libreria Target in modo asincrono?](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/target-atjs-faq.md#section_AB9A0CA30C5440C693413F1455841470)” |
|  | [Sincronizzazione dei profili in tempo reale per mbox3rdPartyID](/help/c-target/c-visitor-profile/3rd-party-id.md) | È stata aggiunta una nota nella parte inferiore della pagina. |
|  | [Limiti](/help/r-troubleshooting-target/target-limits.md)<br>[Attributi di entità personalizzati](/help/c-recommendations/c-products/custom-entity-attributes.md#limits) | Sono state aggiunte informazioni sui limiti dell’attributo di entità personalizzato. |
|  | [Domande frequenti su destinazioni e pubblico](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md#strings-that-represent-numbers) | Testo aggiornato. |
|  | [Creare nuovi criteri](/help/c-recommendations/c-algorithms/create-new-algorithm.md#custom) | È stata aggiunta una nuova sezione che spiega come creare raggruppamenti basati su profilo per gli algoritmi di popolarità: “Utilizzare una chiave di consiglio personalizzata”. |
| 19 marzo 2019 | [Note sulla versione di Target (corrente)](/help/r-release-notes/release-notes.md) | Nuove informazioni sulle versioni 2.0.1 e 1.7.1 di at.js. |
|  | [Visualizzare i rapporti - Domande frequenti su A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md) | È stata aggiunta la seguente domanda frequente: “A4T supporta le suite di rapporti virtuali?” |
| 18 marzo 2019 | [Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md) e [dettagli sulla versione at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Nuove informazioni sulle versioni 2.0.1 e 1.7.1 di at.js. |
|  | [Metodi per immettere i dati in Target](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md#section_92AB4820A5624C669D9A1F1B6220D4FA) e [Attributi cliente](/help/c-target/c-visitor-profile/working-with-customer-attributes.md) | È stato aggiunto: non puoi inviare i seguenti caratteri in `mbox3rdPartyID`: segno più (+) e barra (/). |
| 15 marzo 2019 | [Prima dell’implementazione](/help/c-implementing-target/c-considerations-before-you-implement-target/considerations-before-you-implement-target.md) | È stata aggiunta una nota importante: “Le modifiche apportate a at.js o mbox.js non saranno supportate da Adobe Customer Care”. |
| 14 marzo 2019 | [Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md) | È stata modificata la data di rilascio di Target Standard/Premium versione 19.3.1 al 29 marzo 2019. |
| 13 marzo 2019 | [Creare un&#39;attività di personalizzazione automatizzata](/help/c-activities/t-automated-personalization/create-ap-activity.md) | È stato aggiornato il testo nella riga Metrica conversione. |
|  | [Attributi del profilo](/help/c-target/c-visitor-profile/profile-parameters.md) | È stata aggiunta una nuova sezione: “Riferimento JavaScript per parametri del profilo di script.” |
|  | [Funzioni di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md) | È stata ristrutturata la pagina e sono state create nuove pagine per ogni funzione at.js per semplificare l’accesso alle informazioni. |
|  | [Funzionamento di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) | È stato aggiunto un paragrafo introduttivo per spiegare un’implementazione lato client. |
|  | [Domande frequenti sui consigli](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md) | È stata aggiunta la seguente domanda frequente: “È possibile escludere un’entità in modo dinamico?” |
| 12 marzo 2019 | [Aggiornamento da at.js 1.x a at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md) e [Eseguire il debug di at.js utilizzando il debugger di Adobe Experience Cloud](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-debugging-atjs/target-debugging-atjs.md) | Il debugger è ora un’integrazione supportata con at.js 2.x. |
| 11 marzo 2019 | [Note sulla versione di Target (attuale)](/help/r-release-notes/release-notes.md), <br>[Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md) e <br>[Modifiche alla crittografia TLS](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md) | È stato aggiornato il testo per indicare che le modifiche TLS verranno apportate il **1 aprile 2019**. |
|  | [adobe.target.getOffers](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) | È stata aggiunta la seguente sezione: “Recupera ed esegui il rendering di dati da più mbox tramite getOffers() e applyOffers().” |
| 6 marzo 2019 | [Aggiornamento da at.js 1.x a at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md) | È stata aggiunta la riga at_property alla tabella “Parametri di at.js 1.x in corrispondenza della mappatura payload di at.js 2.x”. |
|  | [Implementazione di un&#39;applicazione a pagina singola](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md) | È stata aggiunta una nuova sezione: “Utilizza TriggerView per garantire che A4T funzioni correttamente con at.js 2.x e le applicazioni a pagina singola.” |
| 4 marzo 2019 | [Documentazione di Recommendations Classic](/help/c-recommendations/recommendations-classic-documentaton.md) | Nuovo argomento. |
|  | [Confronto tra Recommendations Classic e le attività Consigli di Target Premium](/help/c-recommendations/c-recommendations-faq/recommendations-classic-versus-recommendations-activities-target-premium.md) | Sono state aggiunte informazioni su Consigli come offerta. |
| 28 febbraio 2019 | [Attività](/help/c-activities/activities.md) | Aggiornati testo e immagini. |
|  | [Introduzione a Target](/help/c-intro/intro.md) | È stata aggiunta la sezione “Consigli come offerta” in “Target Premium”. |
|  | [Concetti chiave di Target](/help/c-intro/target-key-concepts.md) | È stata aggiornata la tabella “Tipi di attività”. |
| 26 febbraio 2019 | [Problemi noti e problemi risolti](/help/r-release-notes/known-issues-resolved-issues.md) | È stato aggiunto un problema noto sul supporto delle autorizzazioni Enterprise nelle API Target. |
| 25 febbraio 2019 | [Note sulla versione di Target (attuale)](/help/r-release-notes/release-notes.md), <br>[Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md) e <br>[Modifiche alla crittografia TLS](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md) | Sono state aggiornate le seguenti informazioni:<br>Il 20 febbraio 2019 l’infrastruttura Adobe Target è stata aggiornata nelle aree EMEA, Giappone e APAC per non raccogliere più dati dagli utenti finali con dispositivi meno recenti o browser Web che non supportano TLS 1.1 o versioni successive. Lo stesso aggiornamento è pianificato per l’area Nord America il **4 marzo 2019**. La migrazione a TLS 1.2 offre una maggiore protezione. È importante che esamini a fondo le specifiche e pianifichi le modifiche per una transizione senza problemi. |
|  | [Aggiornamento da at.js 1.x a at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md#payload-mapping) | Nuova sezione: “Parametri di at.js 1.x in corrispondenza della mappatura payload di at.js 2.x” |
|  | [Risoluzione dei problemi relativi al Compositore esperienza avanzato](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshooting-issues-related-to-the-enhanced-experience-composer-eec.md) | È stata aggiunta la colonna “Nomi host” agli indirizzi IP della whitelist. |
| 22 febbraio 2019 | [Configurare le autorizzazioni Enterprise](/help/administrating-target/c-user-management/property-channel/properties-overview.md) | È stata aggiunta la sezione “Ottieni ID Workspace”. |
| 20 febbraio 2019 | [Affinità tra categorie](/help/c-target/c-visitor-profile/category-affinity.md) | Sezione “Algoritmo di affinità tra categorie” aggiornata. |
| 19 febbraio 2019 | [Compositore esperienza visivo per app a pagina singola](/help/c-experiences/spa-visual-experience-composer.md) | Nuovo argomento e nuovi video di formazione. |
|  | [Implementazione di un&#39;applicazione a pagina singola](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md) | Nuovo argomento e nuovi video di formazione. |
|  | [Dettagli sulle versioni di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Nuove informazioni sulle versioni 1.7.0 e 2.0.0 di at.js. |
|  | [Aggiornamento da at.js 1.x a at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md) | Nuovo argomento e nuovo video di formazione. |
|  | [Funzioni di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md) | L’argomento è stato aggiornato per riflettere le modifiche introdotte con at.js 2.x.<br>Sono disponibili tre nuove funzioni per at.js 2.x.<ul><li>adobe.target.getOffers(options)</li><li>adobe.target.applyOffers(options)</li><li>adobe.target.triggerView (viewName, options)</li></ul> |
|  | [Funzionamento di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) | L’argomento è stato aggiornato per riflettere le modifiche introdotte con at.js 2.x ed è stato aggiunto un video di formazione. |
|  | [Gestione at.js della visualizzazione momentanea di altri contenuti](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/manage-flicker-with-atjs.md) | L’argomento è stato aggiornato per riflettere le modifiche introdotte con at.js 2.x. |
|  | [Domande frequenti su at.js ](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/target-atjs-faq.md) | L’argomento è stato aggiornato per riflettere le modifiche introdotte con at.js 2.x. |
|  | [Eseguire il debug di at.js utilizzando il debugger di Adobe Experience Cloud](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-debugging-atjs/target-debugging-atjs.md) | È stata aggiunta una nota per spiegare che le funzioni di richiesta rete di debug e funzionalità di tracciamento Mbox di Adobe Experience Cloud non sono ancora supportate per at.js 2.x. |
|  | [Cookie di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/atjs-cookies.md) | Nuovo argomento. |
|  | [Consigli come offerta](/help/c-recommendations/recommendations-as-an-offer.md) | Nuovo argomento. |
|  | [Opzioni del Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/viztarget-options.md) | <ul><li>Aggiunte informazioni sull’utilizzo dell’azione [!UICONTROL Inserisci prima, Inserisci dopo o Sostituisci con] per aggiungere consigli a un’esperienza in un’attività di test A/B o di targeting delle esperienze.</li><li>Aggiunte informazioni sull’utilizzo dell’azione [!UICONTROL Inserisci prima o Inserisci dopo] per aggiungere frammenti esperienza AEM a un’esperienza.</li></ul> |
|  | [Estensione Adobe Target VEC Helper](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) | Nuovo argomento. |
|  | [Privacy e Regolamento generale sulla protezione dei dati](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md) (RGPD) | Modifiche minori e informazioni relative a funzionalità Opt-in, at.js 1.7.0 e at.js 2.x. |
|  | [Problemi noti e problemi risolti](/help/r-release-notes/known-issues-resolved-issues.md) | Aggiunti problemi noti relativi alle API di Target. |
|  | [Attributi di entità](/help/c-recommendations/c-products/entity-attributes.md) | Aggiunta nota relativa alla scadenza dei valori degli attributi di entità specificati dopo 61 giorni. |
|  | [Note sulla versione](/help/r-release-notes/release-notes.md): 19.2.1 | Questa versione include miglioramenti e correzioni. Consulta le Note sulla versione per saperne di più e trovare i collegamenti verso la relativa documentazione. Questa versione include anche molti aggiornamenti della documentazione. |

## Adobe Target Standard/Premium 19.1.1 (22 gennaio 2019) {#section-19-1-1}

| Data | Argomento | Modifiche |
| --- | --- | --- |
| 2 febbraio 2019 | [Note sulla versione di Target](/help/r-release-notes/target-release-notes.md) (prerelease) | Aggiornate note sulla versione prerelease relative a [!DNL Target] 19.2.1 (19 febbraio 2019). |
| 30 gennaio 2019 | [Target e tipi di pubblico](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md) | Aggiunte nuove domande frequenti: le stringhe che rappresentano numeri (compresi i numeri a virgola mobile) sono considerate numeri. |
| 29 gennaio 2019 | [Note sulla versione di Target (corrente)](/help/r-release-notes/release-notes.md) | Data di disponibilità del supporto delle autorizzazioni Enterprise nelle API di Target aggiornata al 21 febbraio 2019. |
|  | [Aggiornamenti dello stato del sistema e notifiche proattive](/help/r-release-notes/system-status-updates.md) | Aggiunta sezione Notifiche proattive. |
| 22 gennaio 2019 | [Raccolte](/help/c-recommendations/c-products/collections.md)<br>[Esclusioni](/help/c-recommendations/c-products/exclusions.md)<br>[Ricerca nel catalogo](/help/c-recommendations/c-products/catalog-search.md)<br>[Impostazioni](/help/c-recommendations/plan-implement.md#concept_C1E1E2351413468692D6C21145EF0B84)<br>[Recommendations: filtrare raccolte ed esclusioni per ambiente (gruppo di host)](/help/administrating-target/hosts.md) | Aggiunte informazioni sul filtraggio di raccolte ed esclusioni per ambiente (gruppo host). |
|  | [Limiti](/help/r-troubleshooting-target/target-limits.md) | Aggiornate le informazioni nella riga Valore script di profilo. |
|  | [Note sulla versione](/help/r-release-notes/release-notes.md): 19.1.1 | Questa versione include miglioramenti e correzioni. Consulta le Note sulla versione per saperne di più e trovare i collegamenti verso la relativa documentazione. Questa versione include anche molti aggiornamenti della documentazione. |

## Adobe Target Standard/Premium 18.11.1 (12 novembre 2018) {#section_4AD10E8B7EB04F96807FFDB763F31703}

| Data | Argomento | Modifiche |
|--- |--- |--- |
| 16 gennaio 2019 | [Note sulla versione di Target (corrente)](/help/r-release-notes/release-notes.md)<br>[Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md)<br>[Dettagli sulla versione di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Nuove informazioni sulla versione 1.6.4 di at.js. |
| 10 gennaio 2019 | [Note sulla versione di Target (corrente)](/help/r-release-notes/release-notes.md)<br>[Note sulla versione di (prerelease)](/help/r-release-notes/target-release-notes.md)<br>[Modifiche alla crittografia di TLS (Transport Layer Security)](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md) | Aggiunta la data in cui non sarà più disponibile il supporto per la crittografia TLS 1.0: 20 febbraio 2019. |
| 9 gennaio 2019 | [Opzioni del Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/viztarget-options.md) | Aggiunte informazioni relative a Recommendations alle righe Inserisci prima, Inserisci dopo e Sostituisci con. |
|  | [Note sulla versione di Target (corrente)](/help/r-release-notes/release-notes.md)<br>[Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md)<br>[Browser supportati](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md) | Aggiunte informazioni sul supporto di Target e Adobe Experience Cloud per Microsoft Internet Explorer 11 non più disponibile a partire da marzo 2019. |
|  | [Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md) | Aggiunte informazioni per le versioni 19.1.1 di Target e 1.6.4 di at.js. |
|  | [Dettagli sulle versioni di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Aggiunte informazioni per la versione 1.6.4 di at.js. |
|  | [Minimizzare i conteggi gonfiati per visite e visitatori in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md) | Rimossa la nota relativa all’impossibilità per i clienti di creare attività A4T con offerte di reindirizzamento a partire dal 14 novembre 2016. |
|  | [Offerte di reindirizzamento - Domande frequenti su A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md) | Aggiunta nota a “Perché a volte vengono conteggiate le visualizzazioni di pagina nella pagina originale e nella pagina di reindirizzamento?” |
| 20 dicembre 2018 | [Lato server: implementare Target](../c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md) | Aggiunta nota relativa a CORS. |
| 14 dicembre 2018 | [Implementare Target con Adobe Launch](../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md) | Aggiunto collegamento a un nuovo video di formazione: Implementazione di Target con l’esercitazione di Adobe Launch. |
|  | [Rapporti Approfondimenti personalizzazione](../c-reports/c-personalization-insights-reports/personalization-insights-reports.md) | È stato aggiunto un link al video esplicativo. |
| 13 dicembre 2018 | [Compositore esperienza basato su moduli](../c-experiences/form-experience-composer.md) | Aggiornati testo e immagine. |
|  | [Problemi noti e problemi risolti](known-issues-resolved-issues.md) | Aggiunto un problema relativo all’indice del feed di Recommendations, il quale può mostrare il messaggio “In attesa dell’indice” se gli elementi nel feed sono identici a quelli della precedente esecuzione. |
|  | [Selezionare il pubblico](../c-activities/t-test-ab/t-test-create-ab/ab-audience.md) | Aggiornate le immagini. |
|  | [Aggiungi esperienza](../c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md) | Aggiornata l’immagine. |
|  | [Creare un test A/B](../c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) | Aggiornate le immagini. |
|  | [Riepilogo del test](../c-activities/c-multivariate-testing/t-create-multivariate-test/test-summary.md) | Aggiornata l’immagine. |
|  | [Visualizzare un&#39;anteprima delle esperienze per un test multivariato](../c-activities/c-multivariate-testing/t-create-multivariate-test/preview-experiences.md) | Aggiornata l’immagine. |
|  | [Creare combinazioni](../c-activities/c-multivariate-testing/t-create-multivariate-test/add-offers.md) | Aggiornati testo e immagini. |
|  | [Creazione di un test multivariato](../c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md) | Aggiornati testo e immagini. |
| 11 dicembre 2018 | [targetGlobalSettings](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) | Il valore predefinito per overrideMboxEdgeServer è “true” a partire dalla versione 1.6.2. |
| 7 dicembre 2018 | [ Problemi noti e problemi risolti ](known-issues-resolved-issues.md) | I seguenti problemi sono stati spostati dalla tabella Problemi noti alla tabella Problemi risolti: <ul><li>at.js: dopo l’aggiornamento alla versione 1.0 di at.js, le mbox non funzionano nei browser Microsoft Explorer 11 a causa dell’interazione tra at.js e Visitor API 2.2.0.0.</li><li>Geotargeting: la ricerca di una stringa contenente caratteri speciali (ad esempio uno spazio o una virgola) non è attualmente supportata durante la creazione di tipi di pubblico di geotargeting.</li></ul> |
| 5 dicembre 2018 | [ Rapporti Approfondimenti personalizzazione ](../c-reports/c-personalization-insights-reports/personalization-insights-reports.md) | Aggiunta nota relativa alla disponibilità dei rapporti Approfondimenti personalizzazione limitata all’ambiente predefinito. |
|  | [ Adobe Analytics come origine per la generazione di rapporti per Adobe Target (AT) ](../c-integrating-target-with-mac/a4t/a4t.md) | Tabella aggiornata per indicare la disponibilità del supporto di A4T per le distribuzioni lato server. |
| 29 novembre 2018 | [ Stimare il traffico necessario per il successo del test](../c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md) | Aggiornamenti minori al testo, aggiornate le immagini. |
| 27 novembre 2018 | [ Attività ](../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) | Aggiornati testo e immagini. |
|  | [ Attributi degli script di profilo ](../c-target/c-visitor-profile/profile-parameters.md#concept_8C07AEAB0A144FECA8B4FEB091AED4D2) | Aggiunta nota relativa al limite di 1.000 script di profilo per account in Target. |
| 15 novembre 2018 | [ Note sulla versione di Target (corrente) ](../r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A)<br>[ Note sulla versione di Target (prerelease) ](../r-release-notes/target-release-notes.md#reference_4A966062C61048D1A81412E2DDB16E34)<br>[ Dettagli sulla versione di at.js ](../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A) | Nuove informazioni sulla versione 1.6.3 di at.js. |
|  | [ Rapporti Approfondimenti personalizzazione ](../c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767) | Aggiunti nuovi argomenti relativi ai nuovi rapporti Approfondimenti personalizzazione: Segmenti automatizzati e Attributi importanti. |
| 14 novembre 2018 | [ Note sulla versione 18.11.1 (corrente) ](../r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A) di Target | Questa versione include miglioramenti e correzioni. Consulta le Note sulla versione per saperne di più e trovare i collegamenti verso la relativa documentazione. Questa versione include anche molti aggiornamenti della documentazione. |

## Adobe Target Standard/Premium 18.10.1 (24 ottobre 2018) {#section_F3DB9A89D944428DBEE04634EB712601}

| Data | Argomento | Modifiche |
|--- |--- |--- |
| 8 novembre 2018 | [Adobe Analytics come origine per la generazione di rapporti per Adobe Target (A4T)](../c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE) | Aggiunto l’SDK di NodeJS alla tabella di compatibilità. |
| 7 novembre 2018 | [Per quanto tempo si deve eseguire un test A/B?](../c-activities/t-test-ab/sample-size-determination.md#concept_2801F552DB874C20B8A17C1B774C0383) | Argomento modificato e ulteriori informazioni aggiunte. |
|  | [Note sulla versione di Target (prerelease)](../r-release-notes/target-release-notes.md#reference_4A966062C61048D1A81412E2DDB16E34) | Aggiunte informazioni sulle funzionalità nella versione di Target 18.11.1. |
| 5 novembre 2018 | [Integrare i Consigli con l’e-mail](../c-recommendations/c-recommendations-faq/integrating-recs-email.md#reference_256B16C894864F24AF970E43DC174420) | Il collegamento nell&#39;Opzione 3 è stato aggiornato. |
|  | [Attributi del cliente](../c-target/c-visitor-profile/working-with-customer-attributes.md#concept_16C5C434D32D4EB1AD44A71821F3DEE8). | Aggiunta la nota seguente:<br>**Importante:**il nome dell’origine dati e il nome dell’attributo non possono contenere un punto. |
| 31 ottobre 2018 | [Aggiornamenti dello stato del sistema](../r-release-notes/system-status-updates.md#concept_5CBDF506BEFA40E483CC7DE0DA915EAD) | Argomento aggiornato. |
|  | [Serie di webinar sui fondamenti di Target](../cmp-resources-and-contact-information.md#concept_11902FAC95C64479AABE020557A7EEE4) | Aggiunto un collegamento alla registrazione Best practice per la segmentazione del pubblico. |
| 29 ottobre 2018 | [Modifiche alla crittografia di TLS (Transport Layer Security)](../c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451) | È stata aggiunta una nuova sezione: Comportamento previsto con browser che supportano solo TLS 1.0. |
| 26 ottobre 2018 | [Problemi noti e problemi risolti](../r-release-notes/known-issues-resolved-issues.md#concept_625C3A16B7F24D4B82EFF130F0945541) | <ul><li>Aggiunto un problema noto sulla ricerca di stringhe contenenti caratteri speciali durante la creazione di tipi di pubblico di geotargeting.</li><li>Il problema di reindirizzamento di at.js 1.6.0 è stato spostato nella tabella Problemi risolti.</li><li>Un problema relativo alle attività nell’area di lavoro predefinita eliminate tramite API che continuavano a essere visualizzate nell’interfaccia utente di Target è stato spostato nella tabella Problemi risolti.</li></ul> |
| 24 ottobre 2018 | [Preferenze](../administrating-target/r-target-account-preferences/target-account-preferences.md#reference_0CF97B1C2214412ABBC8222EA8A36D7E) | Aggiunte delle informazioni da considerare durante la scelta dell&#39;origine per la generazione di rapporti per le attività in Configurazione > Preferenze o per attività. |
|  | [Creare un&#39;attività di personalizzazione automatizzata](../c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9) | Aggiunte delle informazioni sul filtro per le offerte non assegnate. |
|  | [Creare esperienze](../c-activities/t-experience-target/t-xt-create/xt-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00) | Aggiunte delle informazioni sulla duplicazione delle esperienze nelle attività XT. |
|  | [Aggiungi esperienza](../c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00) | Aggiunte delle informazioni sulla duplicazione delle esperienze nei Test A/B. |
|  | [Informazioni sui tipi di pubblico](../c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271) | Aggiunte informazioni sulla gestione dei tipi di pubblico eliminati in Adobe Audience Manager (AAM) a cui si fa riferimento nelle attività di Target. |
|  | [Integrazioni at.js](../c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/target-atjs-integrations.md#concept_C100BC4F073C4B57A608B309D0157B39) | Argomento aggiornato. |
|  | [Implementare Target senza un sistema per la gestione dei tag](../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#topic_397FFA3D6918456BBE02A9FBE9537894) | Tutte le sezioni sono state aggiornate.  Aggiunta una nuova sezione: Implementazione di at.js. |
|  | Versione 18.10.1 [Note sulla versione](../r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A) | Questa versione include miglioramenti e correzioni. Consulta le Note sulla versione per saperne di più e trovare i collegamenti verso la relativa documentazione. Questa versione include anche molti aggiornamenti della documentazione. |

## Adobe Target Standard/Premium 18.9.1 (26 settembre 2018) {#section_F7E74227BB9D467E9ABC0797EDC2FE0D}

<table id="table_0348AA29207D48A4BDFFA187F4F845B7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Data </th> 
   <th colname="col2" class="entry"> Argomento </th> 
   <th colname="col3" class="entry"> Modifiche </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 24 ottobre 2018 </td> 
   <td colname="col2"> <p> <a href="../r-release-notes/known-issues-resolved-issues.md#concept_625C3A16B7F24D4B82EFF130F0945541" format="dita" scope="local"> Problemi noti e problemi risolti </a> </p> </td> 
   <td colname="col3"> <p>Aggiunto un problema noto riguardante le attività eliminate tramite API nell'area di lavoro predefinita che persistono nell'interfaccia utente di Target. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-reports/c-report-settings/average-lift-bounds-and-confidence-interval.md#topic_AFFDC672A8A34D028B100EF6BE5D8129" format="dita" scope="local"> Incremento medio, limiti di incremento e intervallo di affidabilità </a> </p> </td> 
   <td colname="col3"> <p>Aggiunta una nota che spiega la presenza di lievi varianze tra i calcoli manuali utilizzando le formule elencate e i numeri visualizzati nel rapporto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 22 ottobre 2018 </td> 
   <td colname="col2"> <p> <a href="../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/cookie-behavior.md#concept_4D8107E193B64168A3C0B85B51612991" format="dita" scope="local"> Cookie di Target </a> </p> </td> 
   <td colname="col3"> <p>Aggiunta una nota importante nella parte superiore dell'argomento che consiglia ai clienti di non collegare informazioni sensibili a mboxSession e mboxPC. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 21 ottobre 2018 </td> 
   <td colname="col2"> <p> <a href="../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A" format="dita" scope="local"> Dettagli sulla versione di at.js </a> </p> </td> 
   <td colname="col3"> <p>Nuove informazioni sulla versione 1.6.2 di at.js. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md#topic_6BCC0D0984184379A2A2EA6FFC948899" format="dita" scope="local"> Privacy e Regolamento generale sulla protezione dei dati (RGPD) </a> </p> </td> 
   <td colname="col3"> <p>È stata aggiunta la sezione “Adobe Target and e la funzionalità opt-in di Adobe Launch”. </p> <p>Le seguenti domande frequenti sono state aggiornate: </p> <p> 
     <ul id="ul_BBF57B0E30A541E1BD1BCADD21A3D0F7"> 
      <li id="li_020DE613F4F340D8B68186465883A60C"> <p>Come avviene la gestione del consenso da parte di Adobe Target? </p> </li> 
      <li id="li_515B157F27B04342BB5664FD8E258FE2"> <p>Quali ID sono supportati per consentire ai clienti di completare una richiesta RGPD di accesso e cancellazione per Target? </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25" format="dita" scope="local"> Implementazione di Target con Adobe Launch </a> </p> </td> 
   <td colname="col3"> <p>Il collegamento all'estensione Adobe Target è stato aggiornato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 18 ottobre 2018 </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-recommendations-faq/ip-addresses-marketing-cloud.md#concept_216F959FF18143D6A3BA0BE937918580" format="dita" scope="local"> Indirizzi IP utilizzati dai server di elaborazione dei feed della funzionalità per i consigli (Recommendations)</a> </p> </td> 
   <td colname="col3"> <p>L’intervallo di indirizzi IP utilizzati dalle attività della funzionalità per i consigli (Recommendations) di Target è stato aggiornato. </p> <p>L’intervallo di indirizzi IP utilizzati dalle API della funzionalità per i consigli (Recommendations) di Target è stato aggiunto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 12 ottobre 2018 </td> 
   <td colname="col2"> <p> <a href="../c-activities/c-activity-qa/activity-qa.md#concept_9329EF33DE7D41CA9815C8115DBC4E40" format="dita" scope="local"> Controllo di qualità delle attività </a> </p> </td> 
   <td colname="col3"> <p>Il seguente paragrafo in <span class="wintitle">Considerazioni</span> è stato modificato: </p> <p>La funzione Controllo di qualità attività non visualizza i contenuti di attività archiviate o scadute. Se si disattiva un’attività terminata, è necessario salvare nuovamente l'attività affinché la funzione Controllo di qualità attività funzioni. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 10 ottobre 2018 </td> 
   <td colname="col2"> <p> <a href="../target-home.md#topic_74F655D8648E4586BCCFD789E60D13CE" format="dita" scope="local"> Documentazione di prodotto di Adobe Target </a> </p> </td> 
   <td colname="col3"> <p>La documentazione del prodotto di Adobe Target nelle seguenti lingue è stata aggiornata: tedesco, spagnolo, francese, italiano, giapponese e portoghese (Brasile). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 9 ottobre 2019 </td> 
   <td colname="col2"> <p> <a href="../c-target/c-visitor-profile/profile-parameters.md#concept_01A30B4762D64CD5946B3AA38DC8A201" format="dita" scope="local"> Attributi del profilo </a> </p> </td> 
   <td colname="col3"> <p>Aggiunta la sezione Domande frequenti sugli script di profilo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-recommendations-faq/ip-addresses-marketing-cloud.md#concept_216F959FF18143D6A3BA0BE937918580" format="dita" scope="local"> Indirizzi IP utilizzati dai server di elaborazione dei feed della funzionalità per i consigli (Recommendations)</a> </p> </td> 
   <td colname="col3"> <p>Testo modificato per indicare che le attività di <span class="wintitle">Consigli</span> utilizzano indirizzi IP situati nel data center dell’Oregon. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 8 ottobre 2018 </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-recommendations-faq/ip-addresses-marketing-cloud.md#concept_216F959FF18143D6A3BA0BE937918580" format="dita" scope="local"> Indirizzi IP utilizzati dai server di elaborazione dei feed della funzionalità per i consigli (Recommendations)</a> </p> </td> 
   <td colname="col3"> <p>Aggiunto un nuovo intervallo di indirizzi IP per la notazione CIDR 192.243.242.0.0/24. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 5 ottobre 2018 </td> 
   <td colname="col2"> <p> <a href="../c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-viewing-reports.md#concept_72A95F6466A04B409FCD5989A6B6A554" format="dita" scope="local"> Visualizzazione dei rapporti - Domande frequenti su A4T </a> </p> </td> 
   <td colname="col3"> <p>Rivista l’intera sezione: “È necessario utilizzare visitatori, impression di attività o visite durante la visualizzazione dei rapporti?” Riformulate le descrizioni metriche e aggiunto un elenco di considerazioni. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 4 ottobre 2018 </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE" format="dita" scope="local"> Creazione di criteri </a> </p> </td> 
   <td colname="col3"> <p>Aggiunta la sezione “Tempo di elaborazione dei criteri previsto”. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Attività </a> </p> </td> 
   <td colname="col3"> <p>Aggiunte informazioni su come disattivare il Suggerimento del giorno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 3 ottobre 2018 </td> 
   <td colname="col2"> <p> <a href="https://spark.adobe.com/page/Lo3Spm4oBOvwF/" format="https" scope="external"> Analytics &amp; Target: best practice per l'analisi </a> </p> </td> 
   <td colname="col3"> <p>Scopri la nuova esercitazione di Analytics for Target (A4t). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-intro/how-target-works.md#concept_459AB4DEE7364A9290C2FD405DC29584" format="dita" scope="local"> Come funziona Adobe Target </a> </p> </td> 
   <td colname="col3"> <p>Intero argomento aggiornato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-activities/t-test-ab/t-test-create-ab/test-create-ab.md#task_68C8079BF9FF4625A3BD6680D554BB72" format="dita" scope="local"> Creare un test A/B </a> </p> <p> <a href="../c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Creazione di un'attività di Personalizzazione automatizzata </a> </p> <p> <a href="../c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765" format="dita" scope="local"> Creare un’attività Targeting esperienze </a> </p> <p> <a href="../c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md#task_BF870FA60A8245AB8F0B775BE32EA710" format="dita" scope="local"> Creazione di un test multivariato </a> </p> <p> <a href="../c-recommendations/t-create-recs-activity/recs-activity-settings.md#reference_3FDA8388CEEC4159949151C1829E2FBB" format="dita" scope="local"> Impostazioni delle attività Consigli </a> </p> <p> <a href="../c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00" format="dita" scope="local"> Aggiungi esperienza </a> </p> <p> <a href="../c-activities/t-test-ab/t-test-create-ab/ab-set-metrics.md#task_A04AB66007C1467DA1C21A519A5C7BEB" format="dita" scope="local"> Impostare le metriche </a> </p>
   </td> 
   <td colname="col3"> <p>Aggiornata la tabella che elenca i caratteri non consentiti nei nomi di attività, esperienze o metriche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 2 ottobre 2018 </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-products/collections.md#concept_671BEFFB997D4F1282665BF3CAC00AC5" format="dita" scope="local"> Raccolte </a> </p> </td> 
   <td colname="col3"> <p>Aggiunta nota dopo il Passaggio 1. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-products/exclusions.md#task_E79DA82BA402415FB41232976EDEF1CA" format="dita" scope="local"> Esclusioni </a> </p> </td> 
   <td colname="col3"> <p>Aggiunta nota dopo il Passaggio 1. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 27 settembre 2018 </td> 
   <td colname="col2"> <p> <a href="../c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md#concept_0069C0EFB56C4700BB33F2F35C2B9B17" format="dita" scope="local">Metodi per immettere i dati in Target</a> </p> </td> 
   <td colname="col3"> <p>Aggiunte informazioni sui caratteri consentiti nelle stringhe di query. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../r-release-notes/known-issues-resolved-issues.md#concept_625C3A16B7F24D4B82EFF130F0945541" format="dita" scope="local"> Problemi noti e problemi risolti </a> </p> </td> 
   <td colname="col3"> <p>Il problema noto relativo alla generazione di rapporti a livello di offerta nelle attività di Personalizzazione automatizzata è stato spostato nella tabella Problemi risolti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 26 settembre 2018 </td> 
   <td colname="col2"> <p> <a href="../c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Opzioni del Compositore esperienza visivo </a> </p> </td> 
   <td colname="col3"> <p>Aggiunte informazioni sull'opzione <span class="wintitle">Inserisci prima</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <a href="../c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Creazione di un'attività di Personalizzazione automatizzata </a> </td> 
   <td colname="col3"> <p>Aggiunte informazioni sull'elenco Gruppo di rapporti che consentono di filtrare le offerte in base al gruppo di rapporti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-activities/t-automated-personalization/managing-exclusions.md#topic_30B4E4F89C914EB2B20B038C0299ED2E" format="dita" scope="local"> Gestire le esclusioni </a> </p> </td> 
   <td colname="col3"> <p>Aggiunte informazioni sull’utilizzo di più offerte dalla stessa posizione in un gruppo di esclusione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../cmp-resources-and-contact-information.md#concept_11902FAC95C64479AABE020557A7EEE4" format="dita" scope="local"> Serie di webinar sui fondamenti di Target </a> </p> </td> 
   <td colname="col3"> <p>Aggiunto un collegamento alla sessione Best practice per la generazione di rapporti e socializzazione dei valori. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-products/feeds.md#concept_1228B31E3D0B483B9DD42C5E2AE436E3" format="dita" scope="local"> Feed </a> </p> </td> 
   <td colname="col3"> <p>È stata aggiunta la seguente nota: </p> <p> <p>Importante: i feed caricati scadono dopo 61 giorni. Ciò significa che i consigli non verranno più restituiti se un file di feed non è stato elaborato negli ultimi 60 giorni. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../r-release-notes/known-issues-resolved-issues.md#concept_625C3A16B7F24D4B82EFF130F0945541" format="dita" scope="local"> Problemi noti e problemi risolti </a> </p> </td> 
   <td colname="col3"> <p>Aggiunto un problema noto relativo alla generazione di rapporti a livello di offerta nelle attività di Personalizzazione automatizzata. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-recommendations-faq/integrating-recs-email.md#reference_256B16C894864F24AF970E43DC174420" format="dita" scope="local"> Integrazione di Consigli con l’e-mail </a> </p> </td> 
   <td colname="col3"> <p>Nota aggiornata in “Opzione 1: utilizzare l'API di consegna”. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/recommendations.md#concept_7556C8A4543942F2A77B13A29339C0C0" format="dita" scope="local"> Consigli </a> </p> </td> 
   <td colname="col3"> <p>Argomenti riordinati in tutta la sezione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p>Versione 18.9.1 <a href="../r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A" format="dita" scope="local"> Note sulla versione </a> </p> </td> 
   <td colname="col3"> <p>Questa versione include miglioramenti e correzioni. Consulta le Note sulla versione per saperne di più e trovare i collegamenti verso la relativa documentazione. Questa versione include anche molti aggiornamenti della documentazione. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Adobe Target Standard/Premium 18.8.1 (21 agosto 2018) {#section_6A146EE91FFB49D1BA398B36817CD0A2}

<table id="table_F09AC99B587A4D6390B1F8AE54F5DC47"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Data </th> 
   <th colname="col2" class="entry"> Argomento </th> 
   <th colname="col3" class="entry"> Modifiche </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 21 settembre 2018 </td> 
   <td colname="col2"> <p> <a href="../c-implementing-target/c-implementing-target-for-client-side-web/c-target-debugging-atjs/target-debugging-atjs.md#concept_CAE591DA8C404C22917584ECD4F7494F" format="dita" scope="local"> Debugging di at.js utilizzando il debugger di Adobe Experience Cloud </a> </p> </td> 
   <td colname="col3"> <p>Rivisto l'intero argomento e aggiunti video di formazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 20 settembre 2018 </td> 
   <td colname="col2"> <p> <a href="../r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A" format="dita" scope="local"> Note sulla versione di Target </a> </p> <p> <a href="../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A" format="dita" scope="local"> Dettagli sulla versione di at.js </a> </p> </td> 
   <td colname="col3"> <p>Aggiunte informazioni sulla versione 1.6.1 di at.js. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 19 settembre 2018 </td> 
   <td colname="col2"> <p> <a href="../r-release-notes/known-issues-resolved-issues.md#concept_625C3A16B7F24D4B82EFF130F0945541" format="dita" scope="local"> Problemi noti e problemi risolti </a> </p> </td> 
   <td colname="col3"> Un problema relativo all'editor di codice è stato spostato dalla tabella Problemi noti alla tabella Problemi risolti. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 18 settembre 2018 </td> 
   <td colname="col2"> <p> <a href="../c-experiences/c-visual-experience-composer/c-vec-code-editor/experience-templates.md#concept_109BBD7EABC04DD39E6B7B1687786652" format="dita" scope="local"> Modelli di esperienza </a> </p> </td> 
   <td colname="col3"> <p>Nuovo argomento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../cmp-resources-and-contact-information.md#concept_11902FAC95C64479AABE020557A7EEE4" format="dita" scope="local"> Serie di webinar sui fondamenti di Target </a> </p> </td> 
   <td colname="col3"> <p>Le date dei prossimi webinar sono state aggiornate. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 11 settembre 2018 </td> 
   <td colname="col2"> <p> <a href="../c-activities/c-activity-qa/use-qa-mode-with-server-side-delivery.md#concept_54698C5CE8934F68B20961CD83FD6202" format="dita" scope="local"> Utilizzare il Controllo qualità delle attività con la distribuzione lato server </a> </p> </td> 
   <td colname="col3"> <p>Nuovo argomento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-target/c-audiences/c-target-rules/custom-parameters.md#concept_C4C6E00D7C5A4BE9B72D471DB2E3027B" format="dita" scope="local"> Parametri personalizzati </a> </p> </td> 
   <td colname="col3"> <p>Sono state aggiunte delle informazioni sul nuovo salvataggio di tipi di pubblico personalizzati creati prima della versione 18.5.1. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../r-release-notes/known-issues-resolved-issues.md#concept_625C3A16B7F24D4B82EFF130F0945541" format="dita" scope="local"> Problemi noti e problemi risolti </a> </p> </td> 
   <td colname="col3"> <p>Aggiunto il problema noto: Le impressioni e le conversioni delle attività di Target vengono attualmente conteggiate in modo errato in Analysis Workspace. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md#concept_41F88DE95D2943178BEC382736B5C038" format="dita" scope="local"> Domande frequenti sul Regolamento generale sulla protezione dei dati (RGPD) </a> </p> </td> 
   <td colname="col3"> <p>Esempio di codice aggiornato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-recommendations-faq/recommendations-faq.md#concept_EF272DE4AC6C47B19026BFBE816F5DB8" format="dita" scope="local"> Domande frequenti sui consigli </a> </p> </td> 
   <td colname="col3"> <p>La versione di Velocity richiesta è stata modificata a 1.7.0. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 10 settembre 2018 </td> 
   <td colname="col2"> <p> <a href="../r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A" format="dita" scope="local"> Note sulla versione di Target </a> </p> <p> <a href="../c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451" format="dita" scope="local"> Modifiche alla crittografia di TLS (Transport Layer Security) </a> </p> </td> 
   <td colname="col3"> <p>Modificata la data in cui Adobe terminerà gradualmente il supporto per TLS 1.0 dal 12 settembre 2018 a febbraio 2019. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-reports/reports.md#concept_B5077F5503AA4C98901AA99EDCE6CDE6" format="dita" scope="local"> Rapporti </a> </p> </td> 
   <td colname="col3"> <p>Aggiunte delle informazioni e un collegamento per aiutare a pianificare i test A/B. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-recommendations-faq/recommendations-faq.md#concept_EF272DE4AC6C47B19026BFBE816F5DB8" format="dita" scope="local"> Domande frequenti sui consigli </a> </p> </td> 
   <td colname="col3"> <p>Aggiunta la seguente domanda frequente: Qual è la dimensione massima di un file CSV per un caricamento del feed? </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E" format="dita" scope="local"> Profilo visitatore </a> </p> </td> 
   <td colname="col3"> <p>È stato aggiunto il seguente paragrafo: </p> <p>Un profilo visitatore viene creato nella memoria Edge locale per ogni chiamata mbox con nuovo <span class="codeph">mboxPC </span>. Dopo 30 minuti di inattività, il profilo viene salvato nel database di Target ed è accessibile da altri Edge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md#concept_D28549AAA0A14E3BB5F05F32BE8ABC90" format="dita" scope="local"> URL attività </a> </p> </td> 
   <td colname="col3"> <p>Testo modificato e illustrazione aggiornata. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 7 settembre 2018 </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-recommendations-faq/recommendations-faq.md#concept_EF272DE4AC6C47B19026BFBE816F5DB8" format="dita" scope="local"> Domande frequenti sui consigli </a> </p> </td> 
   <td colname="col3"> <p>Aggiunta una nuova domanda frequente: Perché non riesco a salvare la mia attività di consigli legacy dopo aver definito un nuovo pubblico? </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 4 settembre 2018 </td> 
   <td colname="col2"> <p> <a href="../c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md#section_42725F3C837247D58AE1831EA330E44D" format="dita" scope="local"> Fornitori di dati </a> </p> </td> 
   <td colname="col3"> <p>Esempio di codice aggiornato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md#concept_41F88DE95D2943178BEC382736B5C038" format="dita" scope="local"> Domande frequenti sul Regolamento generale sulla protezione dei dati (RGPD) </a> </p> </td> 
   <td colname="col3"> <p>Modifiche minori. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 30 agosto 2018 </td> 
   <td colname="col2"> <p> <a href="../r-release-notes/known-issues-resolved-issues.md#concept_625C3A16B7F24D4B82EFF130F0945541" format="dita" scope="local"> Problemi noti e problemi risolti </a> </p> </td> 
   <td colname="col3"> Il seguente problema noto è stato aggiunto: <p> 
     <ul id="ul_7AF527E5989D468BBC9472EA1C7F376D"> 
      <li id="li_7F53C6F01E1E471FB546AF98F1FF7F1E"> <p>Quando si utilizza la versione 1.6.0 di <span class="codeph">at.js</span> i reindirizzamenti di Analytics for Target (A4T) si verificano ma senza qualificazione dell'attività. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 28 agosto 2018 </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-products/entity-attributes.md#reference_3BCC1383FB3F44F4A2120BB36270387F" format="dita" scope="local"> Attributi di entità </a> </p> </td> 
   <td colname="col3"> <p>Aggiornata la riga ID entità. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-recommendations/c-algorithms/create-new-algorithm.md#concept_BC16005C7A1E4F1A87E33D16221F4A96" format="dita" scope="local"> Impostazioni di contenuto </a> </p> </td> 
   <td colname="col3"> <p>Le informazioni sull'opzione <span class="wintitle">Consiglia articoli acquistati in precedenza</span> sono state rese più chiare. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 21 agosto 2018 </td> 
   <td colname="col2"> <p> <a href="../c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767" format="dita" scope="local"> Rapporti Approfondimenti personalizzazione </a> </p> </td> 
   <td colname="col3"> <p>Nuovo argomento. </p> <p> <p>Nota: questa funzione sarà presto disponibile. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local"> Modifiche </a> </p> </td> 
   <td colname="col3"> <p>Aggiunte delle informazioni sull'ancoraggio del pannello Modifiche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Opzioni del Compositore esperienza visivo </a> </p> </td> 
   <td colname="col3"> <p>Tabella riorganizzata per tenere conto dei nuovi raggruppamenti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../cmp-resources-and-contact-information.md#concept_11902FAC95C64479AABE020557A7EEE4" format="dita" scope="local"> Serie di webinar sui fondamenti di Target </a> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_D5E4E05DFE7A4E45BF199395D7AC3CE1"> 
      <li id="li_7A4A621EC5C34E4AADD46AA294620D9C"> <p>Aggiunte delle informazioni sui prossimi webinar. </p> </li> 
      <li id="li_A77B214010EF45BEBD0E2CBB256AD67D"> <p>Aggiunto un collegamento alla registrazione per il secondo webinar: Passaggi per aggiungere l’automazione e altre attività più sofisticate. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Attività </a> </p> </td> 
   <td colname="col3"> <p>Aggiunta la sezione “Suggerimenti”. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../r-release-notes/known-issues-resolved-issues.md#concept_625C3A16B7F24D4B82EFF130F0945541" format="dita" scope="local"> Problemi noti e problemi risolti </a> </p> </td> 
   <td colname="col3"> <p>Riformulato un problema riguardante le attività di reindirizzamento nelle implementazioni di <span class="codeph">at.js</span> che può generare la ripetizione ciclica dell'URL di anteprima. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> <a href="../c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451" format="dita" scope="local"> Modifiche alla crittografia di TLS (Transport Layer Security) </a> </p> </td> 
   <td colname="col3"> <p>Rimossa la data precedentemente proposta in cui il supporto per TLS 1.0 sarebbe stato gradualmente eliminato (12 settembre 2018). </p> <p>La data in cui il supporto per TLS 1.0 verrà rimosso verrà annunciata in un secondo momento; tuttavia, è importante esaminare a fondo le specifiche e pianificare le modifiche per una transizione senza problemi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p>Versione 18.8.1 <a href="../r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A" format="dita" scope="local"> Note sulla versione </a> </p> </td> 
   <td colname="col3"> <p>Questa versione include miglioramenti e correzioni. Consulta le Note sulla versione per saperne di più e trovare i collegamenti verso la relativa documentazione. Questa versione include anche molti aggiornamenti della documentazione. </p> </td> 
  </tr> 
 </tbody> 
</table>

