---
description: Informazioni sul supporto di Target per i sistemi ITP 2.1 e ITP 2.2 di Apple tramite la libreria Experience Cloud ID (ECID) 4.3.
keywords: apple;ITP;Intelligent Tracking Prevention
seo-description: Informazioni sul supporto di Adobe Target per Apple ITP 2.1 e ITP 2.2 tramite la libreria Experience Cloud ID (ECID) 4.3.
seo-title: Supporto per Adobe Target e Apple ITP
solution: Target
subtopic: Introduzione
title: Apple ITP 2.x
topic: Standard
translation-type: tm+mt
source-git-commit: 8dc94ca1ed48366e6b3ac7a75b03c214f1db71d9

---


# Apple Intelligent Tracking Prevention (ITP) 2.x

Intelligent Tracking Prevention (ITP) è un’iniziativa di Apple volta a proteggere la privacy degli utenti di Safari. La prima release di ITP, risalente al 2017, riguardava l'utilizzo di cookie di terze parti. In realtà, Apple ha bloccato tutti i cookie di terze parti, che a loro volta, hanno causato un forte mal di testa per le aziende di tecnologie per annunci e mar, perché i cookie di terze parti sono generalmente utilizzati per monitorare i visitatori e raccogliere i dati dei visitatori. Ora Apple sta per introdurre limitazioni e restrizioni sull'utilizzo dei cookie di prime parti in Safari.

Queste versioni di ITP includono le seguenti limitazioni:

| Versione | Dettagli |
| --- | --- |
| [ITP 2.1](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/) | Cookie lato client sottoposti a maschiatura che vengono inseriti nel browser utilizzando l' `document.cookie` API per una scadenza di sette giorni.<br>Rilasciato il 21 febbraio 2019. |
| [ITP 2.2](https://webkit.org/blog/8828/intelligent-tracking-prevention-2-2/) | Drasticamente ridotto il limite di scadenza di sette giorni a un giorno.<br>Rilasciato il 24 aprile 2019. |

## Qual è l'impatto per me come cliente Adobe Target?

[!DNL Target] fornisce librerie JavaScript da distribuire sulle pagine in modo da [!DNL Target] poter fornire ai visitatori la personalizzazione in tempo reale. Esistono tre librerie JavaScript Target ([at.js 1.*x* e at.js 2.*x*](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md)e [mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md)) che posizionano [!DNL Target] cookie lato client sui browser dei visitatori tramite l' `document.cookie` API. Di conseguenza, [!DNL Target] i cookie sono influenzati dall’ITP 2.1 e 2.2 di Apple e scadranno dopo sette giorni (con ITP 2.1) e dopo un giorno (con ITP 2.2).

Apple ITP 2.1 e 2.1 [!DNL Target] nelle seguenti aree:

| Impatto | Dettagli |
| --- | --- |
| Potenziale aumento dei conteggi dei visitatori unici | Poiché la finestra di scadenza è impostata su sette giorni (con ITP 2.1) e un giorno (con ITP 2.2), è possibile che si verifichi un aumento dei visitatori unici provenienti dai browser Safari. Se i visitatori rivisitano il dominio dopo sette giorni (ITP 2.1) o un giorno (ITP 2.2), [!DNL Target] viene imposto di inserire un nuovo [!DNL Target] cookie nel dominio al posto del cookie scaduto. Il nuovo [!DNL Target] cookie si traduce in un nuovo visitatore univoco anche se l’utente è lo stesso. |
| Periodi di lookback ridotti per [!DNL Target] le attività | I profili dei visitatori per [!DNL Target] le attività potrebbero avere un periodo di lookback inferiore per le decisioni. [!DNL Target] i cookie vengono utilizzati per identificare un visitatore e archiviare gli attributi del profilo utente per la personalizzazione. Poiché [!DNL Target] i cookie possono essere scaduti in Safari dopo sette giorni (ITP 2.1) o un giorno (ITP 2.2), i dati del profilo utente legati al [!DNL Target] cookie eliminato non possono essere utilizzati per le decisioni. |

## La mia attuale implementazione è [!DNL Target] influenzata?

In un browser Safari, accedete al sito Web in cui è presente una libreria [!DNL Target] JavaScript. Se viene visualizzato un [!DNL Target] cookie impostato nel contesto di un CNAME, ad esempio `analytics.company.com`, non viene influenzato da ITP 2.1 o 2.2.

Se utilizzi la libreria Experience Cloud ID (ECID) oltre alla libreria JavaScript di Target, l’implementazione avrà un impatto sui modi elencati in questo articolo: Impatto [Safari ITP 2.1 sui clienti](https://medium.com/adobetech/safari-itp-2-1-impact-on-adobe-experience-cloud-customers-9439cecb55ac)di Adobe Experience Cloud e della piattaforma Experience.

## Come posso attenuare l'impatto delle release ITP 2.1, ITP 2.2 e ITP future su [!DNL Target]?

Per attenuare l'impatto dei rilasci ITP 2.1, ITP 2.2 e di ITP futuri, [!DNL Target]completare le seguenti attività:

1. Distribuisci la libreria Experience Cloud ID (ECID) nelle tue pagine.

   La libreria ECID abilita il framework di identificazione delle persone per le soluzioni Experience Cloud Core. La libreria ECID consente di identificare gli stessi visitatori del sito e i loro dati in diverse soluzioni Experience Cloud assegnando identificatori univoci e persistenti. La libreria ECID verrà aggiornata di frequente per attenuare eventuali modifiche relative all'ITP che influiscono sull'implementazione.

   Per ITP 2.1 e ITP 2.2, [ECID library 4.3.0+](https://docs.adobe.com/content/help/en/id-service/using/release-notes/release-notes.html) deve essere utilizzato per mitigare i problemi.

1. Utilizza il CNAME di Adobe e iscriviti al programma di certificazione gestito di Adobe Analytics.

   Dopo aver installato la libreria ECID 4.3.0+, potete sfruttare il CNAME di Adobe Analytics e il programma di certificazione gestito. Questo programma consente di implementare gratuitamente un certificato di prima parte per i cookie di prime parti. Sfruttando CNAME [!DNL Target] i clienti potranno ridurre l'impatto di ITP 2.1 e ITP 2.2.

   Se non utilizzate CNAME, potete avviare il processo parlando con il rappresentante commerciale di riferimento e iscrivervi ad [Adobe Managed Certificate Program](https://docs.adobe.com/content/help/en/core-services/interface/ec-cookies/cookies-first-party.html#adobe-managed-certificate-program).

Dopo aver distribuito una libreria JavaScript di Target insieme alla libreria ECID v4.3.0+ e aver effettuato l’iscrizione al programma di certificazione gestito Adobe per sfruttare il CNAME, avrete a disposizione un piano di mitigazione affidabile e a lungo termine per le modifiche relative a ITP.

As the industry makes strides to create a more secure web for consumers, [!DNL Adobe Target] is absolutely committed to delivering personalized experiences while meeting and exceeding the privacy expectations of visitors. [!DNL Adobe Target] ha già annunciato il supporto per le policy [Chrome di](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/google-chrome-samesite-cookie-policies.md) Google SameSite oltre al supporto per i sistemi ITP 2.1 e ITP 2.2 di Apple.

Con l'evoluzione delle politiche volte a proteggere i nostri consumatori, [!DNL Adobe] continuerà anche a supportare queste iniziative in [!DNL Target], aiutando i nostri clienti a fornire le migliori esperienze personalizzate.
