---
keywords: apple;ITP;prevenzione del tracciamento intelligente;experience cloud id;ecid
description: Scopri Adobe [!DNL Target] e l'impatto dell'iniziativa ITP (Intelligent Tracking Prevention) di Apple che cerca di proteggere la privacy degli utenti di Safari.
title: In che modo [!DNL Target] gestisce il supporto Apple ITP?
feature: Privacy e sicurezza
role: Developer
exl-id: 05a62be5-ccfb-4d5c-b511-35023b95e567
source-git-commit: dd20791535e47c83d0f0ac60addfe0888748f86a
workflow-type: tm+mt
source-wordcount: '910'
ht-degree: 52%

---

# Apple Intelligent Tracking Prevention (ITP) 2.x

Informazioni sul supporto [!DNL Adobe Target] per Apple ITP 2.x tramite la libreria Experience Cloud ID (ECID) 4.3.

Intelligent Tracking Prevention (ITP) è l’iniziativa di Apple a tutela della privacy degli utenti Safari. La prima versione di ITP, rilasciata nel 2017, interessava l’uso dei cookie di terze parti. In pratica, Apple bloccava tutti i cookie di terze parti, il che causava non poche complicazioni per aziende di tecnologie per pubblicità e marketing, perché i cookie di terze parti venivano generalmente utilizzati per tenere traccia dei visitatori e raccoglierne i dati. Ora Apple sta implementando limiti e restrizioni sul modo in cui i cookie di prima parte vengono utilizzati in Safari.

Queste versioni di ITP includono le seguenti restrizioni:

| Versione | Dettagli |
| --- | --- |
| [ITP 2.1](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/) | Ai cookie lato client inseriti nel browser utilizzando l’API `document.cookie` viene applicata una scadenza di sette giorni.<br>Data di rilascio: 21 febbraio 2019. |
| [ITP 2.2](https://webkit.org/blog/8828/intelligent-tracking-prevention-2-2/) | La scadenza di sette giorni è stata drasticamente ridotta a un giorno.<br>Data di rilascio: 24 aprile 2019. |
| [ITP 2.3](https://webkit.org/blog/9521/intelligent-tracking-prevention-2-3/) | Sono state eliminate diverse soluzioni alternative, ad esempio l&#39;utilizzo di localStorage o l&#39;utilizzo di JavaScript `Document.referrer property`.<br>Data di rilascio: 23 settembre 2019. |

## Qual è l&#39;impatto per un cliente di Adobe [!DNL Target]? {#impact}

[!DNL Target] fornisce librerie JavaScript da implementare sulle pagine in modo che [!DNL Target] possa offrire ai tuoi visitatori una personalizzazione in tempo reale. Sono disponibili tre librerie JavaScript di Target at.js 1.x, at.js 2.x che inseriscono cookie lato client [!DNL Target] sui browser dei visitatori tramite l’ API `document.cookie` . Di conseguenza, i cookie [!DNL Target] sono interessati da Apple ITP 2.x e scadranno dopo sette giorni (con ITP 2.1) e dopo un giorno (con ITP 2.2 e ITP 2.3).

Apple ITP 2.x ha un impatto [!DNL Target] nelle seguenti aree:

| Impatto | Dettagli |
| --- | --- |
| Aumento potenziale dei conteggi di visitatori univoci | Poiché la finestra di scadenza è impostata su sette giorni (con ITP 2.1) e un giorno (con ITP 2.2 e ITP 2.3), si potrebbe notare un aumento dei visitatori unici provenienti dai browser Safari. Se i visitatori rivisitano il dominio dopo sette giorni (ITP 2.1) o un giorno (ITP 2.2 e ITP 2.3), [!DNL Target] viene costretto a inserire un nuovo cookie [!DNL Target] sul dominio al posto del cookie scaduto. Il nuovo cookie [!DNL Target] dà luogo a un nuovo visitatore univoco, nonostante si tratti sempre dello stesso visitatore. |
| Periodi di lookback ridotti per le attività [!DNL Target] | I profili dei visitatori per le attività [!DNL Target] potrebbero avere un periodo di lookback ridotto per scopi decisionali. I cookie [!DNL Target] vengono utilizzati per identificare un visitatore e archiviare gli attributi del profilo utente ai fini della personalizzazione. Dato che i cookie [!DNL Target] possono scadere su Safari dopo sette giorni (ITP 2.1) o un giorno (ITP 2.2 e 2.3), i dati del profilo utente associati al cookie [!DNL Target] eliminato non possono essere utilizzati a fini decisionali. |
| Script di profilo basati su 3rdPartyID | Poiché la finestra di scadenza è impostata su sette giorni (con ITP 2.1) e un giorno (con ITP 2.2 e ITP 2.3), [gli script di profilo](/help/c-target/c-visitor-profile/profile-parameters.md) basati sul cookie 3rdPartyID cesseranno di funzionare alla scadenza. |
| URL di controllo qualità/anteprima nei dispositivi iOS | Poiché la finestra di scadenza è impostata su sette giorni (con ITP 2.1) e un giorno (con ITP 2.2 e ITP 2.3), [QA/Preview URL](/help/c-activities/c-activity-qa/activity-qa.md) smetterà di funzionare alla scadenza perché gli URL sono basati sul cookie 3rdPartyID. |

## La mia attuale implementazione [!DNL Target] è interessata?

In un browser Safari, accedi al tuo sito web contenente una libreria JavaScript di [!DNL Target]. Se trovi un cookie [!DNL Target] impostato nel contesto di un CNAME, ad esempio `analytics.company.com`, non sei interessato da ITP 2.x.

Se utilizzi la libreria Experience Cloud ID (ECID) oltre alla libreria JavaScript di Target, la tua implementazione sarà interessata come descritto in questo articolo: [Safari ITP 2.1 Impact on Adobe Experience Cloud and Experience Platform Customers](https://medium.com/adobetech/safari-itp-2-1-impact-on-adobe-experience-cloud-customers-9439cecb55ac) (Impatto di Safari ITP 2.1 sui clienti di Adobe Experience Cloud e Experience Platform).

## Come posso attenuare l’impatto di future versioni ITP 2.x su Target?

Per attenuare l’impatto di future versioni di ITP 2.x su Target, completa le seguenti attività:

1. Implementa sulle tue pagine la libreria Experience Cloud ID (ECID).

   La libreria ECID abilita il framework di identificazione delle persone per le soluzioni Experience Cloud di base. La libreria ECID ti consente di identificare gli stessi visitatori del sito e i relativi dati in diverse soluzioni Experience Cloud, assegnando identificatori permanenti e univoci. La libreria ECID verrà aggiornata frequentemente per attenuare l’impatto di eventuali modifiche relative a ITP sulla tua implementazione.

   Per ITP 2.x, [la libreria ECID 4.3.0+](https://experienceleague.adobe.com/docs/id-service/using/release-notes/release-notes.html?lang=it) deve essere utilizzata per la mitigazione.

1. Utilizza il CNAME di Adobe e registrati al programma Managed Certificate di Adobe Analytics.

   Dopo aver installato la libreria ECID 4.3.0+, puoi sfruttare il CNAME e il programma Managed Certificate di Adobe Analytics. Questo consente di implementare gratuitamente un certificato di prime parti per i cookie di prime parti. L’utilizzo del CNAME aiuterà i clienti [!DNL Target] a mitigare l’impatto di ITP 2.x.

   Se non utilizzi CNAME, puoi avviare il processo parlando con il rappresentante del tuo account e iscriverti al [Adobe Managed Certificate Program](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-first-party.html#adobe-managed-certificate-program).

Una volta che avrai implementato una libreria JavaScript di Target in combinazione con la libreria ECID v4.3.0+ e ti sarai registrato all’Adobe Managed Certificate Program per poter utilizzare il CNAME, potrai contare su un solido piano di mitigazione a lungo termine con cui fare fronte alle modifiche relativi a ITP.

Nel settore si fanno grandi progressi nella creazione di un web più sicuro per i consumatori, e [!DNL Adobe Target] conferma il suo impegno costante nel distribuire esperienze personalizzate rispettando e superando le aspettative dei visitatori sulla privacy. [!DNL Adobe Target] ha già annunciato il supporto per i criteri Chrome SameSite di  [ ](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/google-chrome-samesite-cookie-policies.md) Google, oltre al supporto per Apple ITP 2.x.

Con l’evolversi dei criteri a tutela dei consumatori, [!DNL Adobe] continuerà a supportare tali iniziative in [!DNL Target], e allo stesso tempo continuerà ad aiutare i suoi clienti a fornire le migliori esperienze personalizzate possibili.
