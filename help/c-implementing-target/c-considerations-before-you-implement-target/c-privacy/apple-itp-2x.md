---
description: Informazioni sul supporto di Target per ITP 2.1 di Apple e ITP 2.2 tramite la libreria Experience Cloud ID (ECID) 4.3.
keywords: apple; ITP; protezione intelligente del tracciamento
seo-description: Informazioni sul supporto di Adobe Target per ITP 2.1 di Apple e ITP 2.2 tramite la libreria Experience Cloud ID (ECID) 4.3.
seo-title: Supporto per Adobe Target e Apple ITP
solution: Target
subtopic: Introduzione
title: Apple ITP 2. x
topic: Standard
translation-type: tm+mt
source-git-commit: 71419ee6053eeb86ab6595cfba2f05d8506e05b3

---


# Apple Intelligent Tracking Prevention (ITP) 2. x

Intelligent Tracking Prevention (ITP) è l'iniziativa di Apple per proteggere la privacy degli utenti Safari. La prima release di ITP, che era in 2017, indicava l'uso dei cookie di terze parti. In realtà Apple ha bloccato tutti i cookie di terze parti, che a loro volta causava un forte header per aziende tecniche e tecnologie tecniche, perché i cookie di terze parti venivano generalmente utilizzati per tenere traccia dei visitatori e raccogliere i dati dei visitatori. Ora Apple si trova sul passaggio per inserire limiti e limitazioni per il modo in cui i cookie di prime parti vengono utilizzati in Safari.

Queste versioni di ITP includono le seguenti restrizioni:

| Versione | Dettagli |
| --- | --- |
| [ITP 2.1](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/) | Capped client-side cookies that are placed on the browser using the `document.cookie` API to a seven-day expiry.<br>Data di rilascio: 21 febbraio 2019. |
| [ITP 2.2](https://webkit.org/blog/8828/intelligent-tracking-prevention-2-2/) | Ridotto drasticamente il CAP di sette giorni a un giorno.<br>Data di rilascio: 24 aprile 2019. |

## Qual è l'impatto su me stesso di Adobe Target?

[!DNL Target] fornisce librerie javascript da distribuire sulle pagine in modo da [!DNL Target] offrire la personalizzazione in tempo reale ai visitatori. There are three Target JavaScript libraries ([at.js 1.*x* e at. js 2.*x*](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md)e [mbox. js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md)) che posizionano i cookie lato client [!DNL Target] sui browser dei visitatori tramite l' `document.cookie` API. As a result, [!DNL Target] cookies are impacted by Apple’s ITP 2.1 and 2.2 and will expire after seven days (with ITP 2.1) and after one day (with ITP 2.2).

Apple ITP 2.1 and 2.1 impact [!DNL Target] in the following areas:

| Impatto | Dettagli |
| --- | --- |
| Aumento potenziale dei conteggi dei visitatori unici | Poiché la finestra di scadenza è impostata su sette giorni (con ITP 2.1) e un giorno (con ITP 2.2), potrebbe essere visualizzato un aumento dei visitatori univoci provenienti dai browser Safari. If your visitors revisit your domain after seven days (ITP 2.1) or one day (ITP 2.2), [!DNL Target] is forced to place a new [!DNL Target] cookie on your domain in place of the expired cookie. The new [!DNL Target] cookie translates to a new unique visitor even though the user is the same. |
| Decreased lookback periods for [!DNL Target] activities | Visitor profiles for [!DNL Target] activities might have a decreased lookback period for decisioning. [!DNL Target] si sfruttano per identificare un visitatore e archiviare gli attributi del profilo utente per la personalizzazione. Given that [!DNL Target] cookies can be expired on Safari after seven days (ITP 2.1) or one day (ITP 2.2), the user profile data that was tied to the purged [!DNL Target] cookie cannot be used for decisioning. |

## Is my current implementation of [!DNL Target] impacted?

In a Safari browser, navigate to your website on which you have a [!DNL Target] JavaScript library. If you see a [!DNL Target] cookie set in the context of a CNAME, such as `analytics.company.com`, then you are not impacted by ITP 2.1 or 2.2.

If you are using the Experience Cloud ID (ECID) library in addition to the Target JavaScript library, your implementation will be impacted in the ways listed in this article: [Safari ITP 2.1 Impact on Adobe Experience Cloud and Experience Platform Customers](https://medium.com/adobetech/safari-itp-2-1-impact-on-adobe-experience-cloud-customers-9439cecb55ac).

## How can I mitigate the impact of ITP 2.1, ITP 2.2, and future ITP releases to [!DNL Target]?

To mitigate the impact of ITP 2.1, ITP 2.2, and future ITP releases to [!DNL Target], complete the following tasks:

1. Distribuisci la libreria Experience Cloud ID (ECID) sulle tue pagine.

   La libreria ECID abilita il framework di identificazione delle persone per le soluzioni di base di Experience Cloud. La libreria ECID consente di identificare gli stessi visitatori del sito e i relativi dati in diverse soluzioni Experience Cloud assegnando identificatori permanenti e univoci. La libreria ECID verrà aggiornata frequentemente per attenuare eventuali modifiche ITP che influiscono sulla tua implementazione.

   For ITP 2.1 and ITP 2.2, [ECID library 4.3.0+](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-release-notes.html) must be utilized for mitigation.

1. Utilizza il CNAME e l'iscrizione di Adobe per il programma di certificazione gestito di Adobe Analytics.

   Dopo aver installato la libreria ECID 4.3.0 +, potete sfruttare il CNAME di Adobe Analytics e il programma di certificazione gestito. Questo programma consente di implementare gratuitamente un certificato di prime parti per i cookie di prime parti. Leveraging CNAME will help [!DNL Target] customers mitigate the impact of ITP 2.1 and ITP 2.2.

   If you are not leveraging CNAME, you can start the process by talking with your account representative and enrolling in the [Adobe Managed Certificate Program](https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/adobe_managed_cert_pgm.html).

Dopo aver distribuito una libreria javascript Target in combinazione con la libreria ECID v 4.3.0 + e registrato nel programma di certificazione gestito di Adobe per sfruttare il CNAME, avrai un piano di attenuazione potente e a lungo termine per le modifiche a ITP.

As the industry makes strides to create a more secure web for consumers, [!DNL Adobe Target] is absolutely committed to delivering personalized experiences while meeting and exceeding the privacy expectations of visitors. [!DNL Adobe Target] ha già annunciato il supporto per i criteri samesite Chrome di [Google](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/google-chrome-samesite-cookie-policies.md) in aggiunta al supporto per ITP 2.1 e ITP 2.2 di Apple.

As policies continue to evolve to protect our consumers, [!DNL Adobe] will also continue to support these initiatives in [!DNL Target], while helping our customers provide the best-in-class personalized experiences.
