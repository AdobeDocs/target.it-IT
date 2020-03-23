---
keywords: apple;ITP;intelligent tracking prevention
description: Informazioni sul Supporto di Adobe Target per Apple ITP 2.1 e ITP 2.2 tramite la libreria Experience Cloud ID (ECID) 4.3.
title: Adobe Target e il supporto per Apple ITP
subtopic: Getting Started
topic: Standard
translation-type: tm+mt
source-git-commit: 0fad08727233566dae6e948e53cda4f7acb64f6f

---


# Apple Intelligent Tracking Prevention (ITP) 2.x

Intelligent Tracking Prevention (ITP) è l’iniziativa di Apple a tutela della privacy degli utenti Safari. La prima versione di ITP, rilasciata nel 2017, interessava l’uso dei cookie di terze parti. In pratica, Apple bloccava tutti i cookie di terze parti, il che causava non poche complicazioni per aziende di tecnologie per pubblicità e marketing, perché i cookie di terze parti venivano generalmente utilizzati per tenere traccia dei visitatori e raccoglierne i dati. Ora Apple sta implementando limiti e restrizioni sul modo in cui i cookie di prima parte vengono utilizzati in Safari.

Queste versioni di ITP includono le seguenti restrizioni:

| Versione | Dettagli |
| --- | --- |
| [ITP 2.1](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/) | Ai cookie lato client inseriti nel browser utilizzando l’API `document.cookie` viene applicata una scadenza di sette giorni.<br>Data di rilascio: 21 febbraio 2019. |
| [ITP 2.2](https://webkit.org/blog/8828/intelligent-tracking-prevention-2-2/) | La scadenza di sette giorni è stata drasticamente ridotta a un giorno.<br>Data di rilascio: 24 aprile 2019. |

## Qual è l’impatto per i clienti di Adobe Target? {#impact}

[!DNL Target] fornisce librerie JavaScript da implementare sulle pagine in modo che [!DNL Target] possa offrire ai tuoi visitatori una personalizzazione in tempo reale. Tre librerie JavaScript di Target ([at.js 1.x and at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md), and [mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md)) that place client-side [!DNL Target] cookies on your visitors&#39; browsers via the `document.cookie` API. Di conseguenza, i cookie di [!DNL Target] sono interessati da Apple ITP 2.1 e 2.2 e scadranno rispettivamente dopo sette giorni e dopo un giorno.

Apple ITP 2.1 e 2.2 hanno un impatto su [!DNL Target] nelle seguenti aree:

| Impatto | Dettagli |
| --- | --- |
| Aumento potenziale dei conteggi di visitatori univoci | Poiché la finestra di scadenza è impostata su sette giorni (ITP 2.1) e un giorno (ITP 2.2), vi può verificare un incremento nel numero di visitatori univoci provenienti dai browser Safari. Se lo stesso visitatore ritorna sul tuo dominio dopo sette giorni (ITP 2.1) o un giorno (ITP 2.2), [!DNL Target] deve inserire nel dominio un nuovo cookie [!DNL Target] in sostituzione di quello scaduto. Il nuovo cookie [!DNL Target] dà luogo a un nuovo visitatore univoco, nonostante si tratti sempre dello stesso visitatore. |
| Periodi di lookback ridotti per le attività [!DNL Target] | I profili dei visitatori per le attività [!DNL Target] potrebbero avere un periodo di lookback ridotto per scopi decisionali. I cookie [!DNL Target] vengono utilizzati per identificare un visitatore e archiviare gli attributi del profilo utente ai fini della personalizzazione. Dato che i cookie [!DNL Target] possono scadere su Safari dopo sette giorni (ITP 2.1) o un giorno (ITP 2.2), i dati del profilo utente associati al cookie [!DNL Target] eliminato non possono essere più utilizzati a fini decisionali. |
| Script di profilo basati su 3rdPartyID | Poiché la finestra di scadenza è impostata su sette giorni (con ITP 2.1) e un giorno (con ITP 2.2), gli script [di](/help/c-target/c-visitor-profile/profile-parameters.md) profilo basati sul cookie 3rdPartyID cesseranno di funzionare alla scadenza. |
| URL QA/Anteprima nei dispositivi iOS | Poiché la finestra di scadenza è impostata su sette giorni (con ITP 2.1) e un giorno (con ITP 2.2), gli URL [](/help/c-activities/c-activity-qa/activity-qa.md) QA/Anteprima non funzioneranno più alla scadenza, perché gli URL sono basati sul cookie 3rdPartyID. |

## La mia attuale implementazione [!DNL Target] è interessata?

In un browser Safari, accedi al tuo sito web contenente una libreria JavaScript di [!DNL Target]. Se trovi un cookie [!DNL Target] impostato nel contesto di un CNAME, ad esempio `analytics.company.com`, non sei interessato da ITP 2.1 o 2.2.

Se utilizzi la libreria Experience Cloud ID (ECID) oltre alla libreria JavaScript di Target, la tua implementazione sarà interessata come descritto in questo articolo: [Safari ITP 2.1 Impact on Adobe Experience Cloud and Experience Platform Customers](https://medium.com/adobetech/safari-itp-2-1-impact-on-adobe-experience-cloud-customers-9439cecb55ac) (Impatto di Safari ITP 2.1 sui clienti di Adobe Experience Cloud e Experience Platform).

## Come posso attenuare l’impatto su [!DNL Target] di ITP 2.1, ITP 2.2 e future versioni di ITP?

Per attenuare l’impatto su [!DNL Target] di ITP 2.1, ITP 2.2 e future versioni ITP, completa le seguenti attività:

1. Implementa sulle tue pagine la libreria Experience Cloud ID (ECID).

   La libreria ECID abilita il framework di identificazione delle persone per le soluzioni Experience Cloud di base. La libreria ECID ti consente di identificare gli stessi visitatori del sito e i relativi dati in diverse soluzioni Experience Cloud, assegnando identificatori permanenti e univoci. La libreria ECID verrà aggiornata frequentemente per attenuare l’impatto di eventuali modifiche relative a ITP sulla tua implementazione.

   Per ITP 2.1 e ITP 2.2, [ECID library 4.3.0+](https://docs.adobe.com/content/help/en/id-service/using/release-notes/release-notes.html) deve essere utilizzato per mitigare i problemi.

1. Utilizza il CNAME di Adobe e registrati al programma Managed Certificate di Adobe Analytics.

   Dopo aver installato la libreria ECID 4.3.0+, puoi sfruttare il CNAME e il programma Managed Certificate di Adobe Analytics. Questo consente di implementare gratuitamente un certificato di prime parti per i cookie di prime parti. Con l’utilizzo del CNAME i clienti [!DNL Target] potranno mitigare con più facilità l’impatto di ITP 2.1 e ITP 2.2.

   If you are not leveraging CNAME, you can start the process by talking with your account representative and enrolling in the [Adobe Managed Certificate Program](https://docs.adobe.com/content/help/en/core-services/interface/ec-cookies/cookies-first-party.html#adobe-managed-certificate-program).

Una volta che avrai implementato una libreria JavaScript di Target in combinazione con la libreria ECID v4.3.0+ e ti sarai registrato all’Adobe Managed Certificate Program per poter utilizzare il CNAME, potrai contare su un solido piano di mitigazione a lungo termine con cui fare fronte alle modifiche relativi a ITP.

Nel settore si fanno grandi progressi nella creazione di un web più sicuro per i consumatori, e [!DNL Adobe Target] conferma il suo impegno costante nel distribuire esperienze personalizzate rispettando e superando le aspettative dei visitatori sulla privacy. È già stato annunciato che [!DNL Adobe Target] supporterà i [criteri di Chrome per i cookie SameSite di Google](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/google-chrome-samesite-cookie-policies.md), oltre a Apple ITP 2.1 e ITP 2.2.

Con l’evolversi dei criteri a tutela dei consumatori, [!DNL Adobe] continuerà a supportare tali iniziative in [!DNL Target], e allo stesso tempo continuerà ad aiutare i suoi clienti a fornire le migliori esperienze personalizzate possibili.
