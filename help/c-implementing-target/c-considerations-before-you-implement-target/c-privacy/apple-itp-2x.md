---
keywords: apple;ITP;prevenzione intelligente del tracciamento;experience cloud id;ecid
description: Scopri  Adobe Target e l'impatto dell'iniziativa di Apple Intelligent Tracking Prevention (ITP) che mira a proteggere la privacy degli utenti di Safari.
title: In che modo Target gestisce il supporto di Apple ITP?
feature: Privacy & Security
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '913'
ht-degree: 51%

---


# Apple Intelligent Tracking Prevention (ITP) 2.x

Informazioni sul supporto di [!DNL Adobe Target] per l&#39;ITP 2.x di Apple tramite la libreria di ID Experience Cloud (ECID)  4.3.

Intelligent Tracking Prevention (ITP) è l’iniziativa di Apple a tutela della privacy degli utenti Safari. La prima versione di ITP, rilasciata nel 2017, interessava l’uso dei cookie di terze parti. In pratica, Apple bloccava tutti i cookie di terze parti, il che causava non poche complicazioni per aziende di tecnologie per pubblicità e marketing, perché i cookie di terze parti venivano generalmente utilizzati per tenere traccia dei visitatori e raccoglierne i dati. Ora Apple sta implementando limiti e restrizioni sul modo in cui i cookie di prima parte vengono utilizzati in Safari.

Queste versioni di ITP includono le seguenti restrizioni:

| Versione | Dettagli |
| --- | --- |
| [ITP 2.1](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/) | Ai cookie lato client inseriti nel browser utilizzando l’API `document.cookie` viene applicata una scadenza di sette giorni.<br>Data di rilascio: 21 febbraio 2019. |
| [ITP 2.2](https://webkit.org/blog/8828/intelligent-tracking-prevention-2-2/) | La scadenza di sette giorni è stata drasticamente ridotta a un giorno.<br>Data di rilascio: 24 aprile 2019. |
| [ITP 2.3](https://webkit.org/blog/9521/intelligent-tracking-prevention-2-3/) | Sono state eliminate diverse soluzioni alternative, ad esempio l&#39;impiego di localStorage o l&#39;utilizzo di JavaScript `Document.referrer property`.<br>Rilasciato il 23 settembre 2019. |

## Qual è l’impatto per i clienti di Adobe Target? {#impact}

[!DNL Target] fornisce librerie JavaScript da implementare sulle pagine in modo che [!DNL Target] possa offrire ai tuoi visitatori una personalizzazione in tempo reale. Tre librerie JavaScript di Target ([at.js 1.x, at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) e [mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md)) che posizionano cookie [!DNL Target] lato client sui browser dei visitatori tramite l&#39;API `document.cookie`. Di conseguenza, i [!DNL Target] cookie sono influenzati dall&#39;ITP 2.x di Apple e scadranno dopo sette giorni (con ITP 2.1) e dopo un giorno (con ITP 2.2 e ITP 2.3).

Apple ITP 2.x urta [!DNL Target] nelle seguenti aree:

| Impatto | Dettagli |
| --- | --- |
| Aumento potenziale dei conteggi di visitatori univoci | Poiché la finestra di scadenza è impostata su sette giorni (con ITP 2.1) e un giorno (con ITP 2.2 e ITP 2.3), è possibile che si verifichi un aumento dei visitatori unici provenienti dai browser Safari. Se i visitatori rivisitano il dominio dopo sette giorni (ITP 2.1) o un giorno (ITP 2.2 e ITP 2.3), [!DNL Target] viene costretto a inserire un nuovo cookie [!DNL Target] nel dominio al posto del cookie scaduto. Il nuovo cookie [!DNL Target] dà luogo a un nuovo visitatore univoco, nonostante si tratti sempre dello stesso visitatore. |
| Periodi di lookback ridotti per le attività [!DNL Target] | I profili dei visitatori per le attività [!DNL Target] potrebbero avere un periodo di lookback ridotto per scopi decisionali. I cookie [!DNL Target] vengono utilizzati per identificare un visitatore e archiviare gli attributi del profilo utente ai fini della personalizzazione. Poiché i cookie [!DNL Target] possono essere scaduti in Safari dopo sette giorni (ITP 2.1) o un giorno (ITP 2.2 e 2.3), i dati del profilo utente legati al cookie [!DNL Target] eliminato non possono essere utilizzati per prendere decisioni. |
| Script di profilo basati su 3rdPartyID | Poiché la finestra di scadenza è impostata su sette giorni (con ITP 2.1) e un giorno (con ITP 2.2 e ITP 2.3), gli script di profilo [](/help/c-target/c-visitor-profile/profile-parameters.md) basati sul cookie 3rdPartyID cesseranno di funzionare alla scadenza. |
| URL QA/Anteprima nei dispositivi iOS | Poiché la finestra di scadenza è impostata su sette giorni (con ITP 2.1) e un giorno (con ITP 2.2 e ITP 2.3), [QA/Preview URLs](/help/c-activities/c-activity-qa/activity-qa.md) cesserà di funzionare alla scadenza, perché gli URL sono basati sul cookie 3rdPartyID. |

## La mia attuale implementazione [!DNL Target] è interessata?

In un browser Safari, accedi al tuo sito web contenente una libreria JavaScript di [!DNL Target]. Se viene visualizzato un cookie [!DNL Target] impostato nel contesto di un CNAME, ad esempio `analytics.company.com`, ITP 2.x non viene interessato.

Se utilizzi la libreria Experience Cloud ID (ECID) oltre alla libreria JavaScript di Target, la tua implementazione sarà interessata come descritto in questo articolo: [Safari ITP 2.1 Impact on Adobe Experience Cloud and Experience Platform Customers](https://medium.com/adobetech/safari-itp-2-1-impact-on-adobe-experience-cloud-customers-9439cecb55ac) (Impatto di Safari ITP 2.1 sui clienti di Adobe Experience Cloud e Experience Platform).

## Come posso attenuare l&#39;impatto delle future release ITP 2.x su Target?

Per attenuare l&#39;impatto delle future release ITP 2.x su Target, completa le seguenti attività:

1. Implementa sulle tue pagine la libreria Experience Cloud ID (ECID).

   La libreria ECID abilita il framework di identificazione delle persone per le soluzioni Experience Cloud di base. La libreria ECID ti consente di identificare gli stessi visitatori del sito e i relativi dati in diverse soluzioni Experience Cloud, assegnando identificatori permanenti e univoci. La libreria ECID verrà aggiornata frequentemente per attenuare l’impatto di eventuali modifiche relative a ITP sulla tua implementazione.

   Per ITP 2.x, per la mitigazione è necessario utilizzare la [libreria ECID 4.3.0+](https://experienceleague.adobe.com/docs/id-service/using/release-notes/release-notes.html).

1. Utilizza il CNAME di Adobe e registrati al programma Managed Certificate di Adobe Analytics.

   Dopo aver installato la libreria ECID 4.3.0+, puoi sfruttare il CNAME e il programma Managed Certificate di Adobe Analytics. Questo consente di implementare gratuitamente un certificato di prime parti per i cookie di prime parti. Sfruttando CNAME i clienti [!DNL Target] possono ridurre l&#39;impatto di ITP 2.x.

   Se non utilizzate CNAME, potete avviare il processo parlando con il rappresentante commerciale di riferimento e iscrivervi al [ Adobe Managed Certificate Program](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-first-party.html#adobe-managed-certificate-program).

Una volta che avrai implementato una libreria JavaScript di Target in combinazione con la libreria ECID v4.3.0+ e ti sarai registrato all’Adobe Managed Certificate Program per poter utilizzare il CNAME, potrai contare su un solido piano di mitigazione a lungo termine con cui fare fronte alle modifiche relativi a ITP.

Nel settore si fanno grandi progressi nella creazione di un web più sicuro per i consumatori, e [!DNL Adobe Target] conferma il suo impegno costante nel distribuire esperienze personalizzate rispettando e superando le aspettative dei visitatori sulla privacy. [!DNL Adobe Target] ha già annunciato il supporto per i criteri Chrome di  [Google SameSite oltre al supporto per ](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/google-chrome-samesite-cookie-policies.md) i criteri di Apple ITP 2.x.

Con l’evolversi dei criteri a tutela dei consumatori, [!DNL Adobe] continuerà a supportare tali iniziative in [!DNL Target], e allo stesso tempo continuerà ad aiutare i suoi clienti a fornire le migliori esperienze personalizzate possibili.
