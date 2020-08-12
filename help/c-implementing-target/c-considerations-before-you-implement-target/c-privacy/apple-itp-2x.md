---
keywords: apple;ITP;intelligent tracking prevention
description: Informazioni  supporto Adobe Target per Apple ITP 2.x tramite la libreria  ID Experience Cloud (ECID) 4.3.
title: Adobe Target e il supporto per Apple ITP
feature: null
subtopic: Getting Started
topic: Standard
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '887'
ht-degree: 54%

---


# Apple Intelligent Tracking Prevention (ITP) 2.x

Intelligent Tracking Prevention (ITP) è l’iniziativa di Apple a tutela della privacy degli utenti Safari. La prima versione di ITP, rilasciata nel 2017, interessava l’uso dei cookie di terze parti. In pratica, Apple bloccava tutti i cookie di terze parti, il che causava non poche complicazioni per aziende di tecnologie per pubblicità e marketing, perché i cookie di terze parti venivano generalmente utilizzati per tenere traccia dei visitatori e raccoglierne i dati. Ora Apple sta implementando limiti e restrizioni sul modo in cui i cookie di prima parte vengono utilizzati in Safari.

Queste versioni di ITP includono le seguenti restrizioni:

| Versione | Dettagli |
| --- | --- |
| [ITP 2.1](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/) | Ai cookie lato client inseriti nel browser utilizzando l’API `document.cookie` viene applicata una scadenza di sette giorni.<br>Data di rilascio: 21 febbraio 2019. |
| [ITP 2.2](https://webkit.org/blog/8828/intelligent-tracking-prevention-2-2/) | La scadenza di sette giorni è stata drasticamente ridotta a un giorno.<br>Data di rilascio: 24 aprile 2019. |
| [ITP 2.3](https://webkit.org/blog/9521/intelligent-tracking-prevention-2-3/) | Sono state eliminate diverse soluzioni alternative, ad esempio l&#39;impiego di localStorage o l&#39;utilizzo di JavaScript `Document.referrer property`.<br>Rilasciato il 23 settembre 2019. |

## Qual è l’impatto per i clienti di Adobe Target? {#impact}

[!DNL Target] fornisce librerie JavaScript da implementare sulle pagine in modo che [!DNL Target] possa offrire ai tuoi visitatori una personalizzazione in tempo reale. Tre librerie JavaScript di Target ([at.js 1.x, at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md), and [mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md)) that place client-side [!DNL Target] cookies on your visitors&#39; browsers via the `document.cookie` API. As a result, [!DNL Target] cookies are impacted by Apple’s ITP 2.x and will expire after seven days (with ITP 2.1) and after one day (with ITP 2.2 and ITP 2.3).

L&#39;impatto di Apple ITP 2.x [!DNL Target] nelle seguenti aree:

| Impatto | Dettagli |
| --- | --- |
| Aumento potenziale dei conteggi di visitatori univoci | Poiché la finestra di scadenza è impostata su sette giorni (con ITP 2.1) e un giorno (con ITP 2.2 e ITP 2.3), è possibile che si verifichi un aumento dei visitatori unici provenienti dai browser Safari. If your visitors revisit your domain after seven days (ITP 2.1) or one day (ITP 2.2 and ITP 2.3), [!DNL Target] is forced to place a new [!DNL Target] cookie on your domain in place of the expired cookie. Il nuovo cookie [!DNL Target] dà luogo a un nuovo visitatore univoco, nonostante si tratti sempre dello stesso visitatore. |
| Periodi di lookback ridotti per le attività [!DNL Target] | I profili dei visitatori per le attività [!DNL Target] potrebbero avere un periodo di lookback ridotto per scopi decisionali. I cookie [!DNL Target] vengono utilizzati per identificare un visitatore e archiviare gli attributi del profilo utente ai fini della personalizzazione. Given that [!DNL Target] cookies can be expired on Safari after seven days (ITP 2.1) or one day (ITP 2.2 and 2.3), the user profile data that was tied to the purged [!DNL Target] cookie cannot be used for decisioning. |
| Script di profilo basati su 3rdPartyID | Poiché la finestra di scadenza è impostata su sette giorni (con ITP 2.1) e un giorno (con ITP 2.2 e ITP 2.3), gli script [di](/help/c-target/c-visitor-profile/profile-parameters.md) profilo basati sul cookie 3rdPartyID cesseranno di funzionare alla scadenza. |
| URL QA/Anteprima nei dispositivi iOS | Poiché la finestra di scadenza è impostata su sette giorni (con ITP 2.1) e un giorno (con ITP 2.2 e ITP 2.3), gli URL [](/help/c-activities/c-activity-qa/activity-qa.md) QA/Preview cesseranno di funzionare alla scadenza, perché gli URL si basano sul cookie 3rdPartyID. |

## La mia attuale implementazione [!DNL Target] è interessata?

In un browser Safari, accedi al tuo sito web contenente una libreria JavaScript di [!DNL Target]. If you see a [!DNL Target] cookie set in the context of a CNAME, such as `analytics.company.com`, then you are not impacted by ITP 2.x.

Se utilizzi la libreria Experience Cloud ID (ECID) oltre alla libreria JavaScript di Target, la tua implementazione sarà interessata come descritto in questo articolo: [Safari ITP 2.1 Impact on Adobe Experience Cloud and Experience Platform Customers](https://medium.com/adobetech/safari-itp-2-1-impact-on-adobe-experience-cloud-customers-9439cecb55ac) (Impatto di Safari ITP 2.1 sui clienti di Adobe Experience Cloud e Experience Platform).

## Come posso attenuare l&#39;impatto delle future release ITP 2.x su Target?

Per attenuare l&#39;impatto delle future release ITP 2.x su Target, completa le seguenti attività:

1. Implementa sulle tue pagine la libreria Experience Cloud ID (ECID).

   La libreria ECID abilita il framework di identificazione delle persone per le soluzioni Experience Cloud di base. La libreria ECID ti consente di identificare gli stessi visitatori del sito e i relativi dati in diverse soluzioni Experience Cloud, assegnando identificatori permanenti e univoci. La libreria ECID verrà aggiornata frequentemente per attenuare l’impatto di eventuali modifiche relative a ITP sulla tua implementazione.

   Per ITP 2.x, [ECID library 4.3.0+](https://docs.adobe.com/content/help/en/id-service/using/release-notes/release-notes.html) deve essere utilizzato per mitigare i problemi.

1. Utilizza il CNAME di Adobe e registrati al programma Managed Certificate di Adobe Analytics.

   Dopo aver installato la libreria ECID 4.3.0+, puoi sfruttare il CNAME e il programma Managed Certificate di Adobe Analytics. Questo consente di implementare gratuitamente un certificato di prime parti per i cookie di prime parti. Leveraging CNAME will help [!DNL Target] customers mitigate the impact of ITP 2.x.

   If you are not leveraging CNAME, you can start the process by talking with your account representative and enrolling in the [Adobe Managed Certificate Program](https://docs.adobe.com/content/help/en/core-services/interface/ec-cookies/cookies-first-party.html#adobe-managed-certificate-program).

Una volta che avrai implementato una libreria JavaScript di Target in combinazione con la libreria ECID v4.3.0+ e ti sarai registrato all’Adobe Managed Certificate Program per poter utilizzare il CNAME, potrai contare su un solido piano di mitigazione a lungo termine con cui fare fronte alle modifiche relativi a ITP.

Nel settore si fanno grandi progressi nella creazione di un web più sicuro per i consumatori, e [!DNL Adobe Target] conferma il suo impegno costante nel distribuire esperienze personalizzate rispettando e superando le aspettative dei visitatori sulla privacy. [!DNL Adobe Target] ha già annunciato il supporto per le policy [Chrome di](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/google-chrome-samesite-cookie-policies.md) Google SameSite oltre al supporto per Apple ITP 2.x.

Con l’evolversi dei criteri a tutela dei consumatori, [!DNL Adobe] continuerà a supportare tali iniziative in [!DNL Target], e allo stesso tempo continuerà ad aiutare i suoi clienti a fornire le migliori esperienze personalizzate possibili.
