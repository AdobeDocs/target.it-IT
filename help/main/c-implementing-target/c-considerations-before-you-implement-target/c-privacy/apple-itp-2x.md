---
keywords: apple;ITP;prevenzione del tracciamento intelligente;experience cloud id;ecid;itp
description: Scopri l’Adobe [!DNL Target] e l’impatto dell’iniziativa ITP (Intelligent Tracking Prevention) di Apple che cerca di proteggere la privacy degli utenti di Safari.
title: Come funziona [!DNL Target] Gestire il supporto Apple ITP?
feature: Privacy & Security
role: Developer
exl-id: 05a62be5-ccfb-4d5c-b511-35023b95e567
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '589'
ht-degree: 36%

---

# Apple Intelligent Tracking Prevention (ITP) 2.x

Intelligent Tracking Prevention (ITP) è l’iniziativa di Apple a tutela della privacy degli utenti Safari. La prima versione di ITP, rilasciata nel 2017, interessava l’uso dei cookie di terze parti. In pratica, Apple bloccava tutti i cookie di terze parti, il che causava non poche complicazioni per aziende di tecnologie per pubblicità e marketing, perché i cookie di terze parti venivano generalmente utilizzati per tenere traccia dei visitatori e raccoglierne i dati. Ora Apple sta implementando limiti e restrizioni sul modo in cui i cookie di prima parte vengono utilizzati in Safari.

Queste versioni di ITP includono le seguenti restrizioni:

| Versione | Dettagli |
| --- | --- |
| [ITP 2.1](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/) | Ai cookie lato client inseriti nel browser utilizzando l’API `document.cookie` viene applicata una scadenza di sette giorni.<br>Data di rilascio: 21 febbraio 2019. |
| [ITP 2.2](https://webkit.org/blog/8828/intelligent-tracking-prevention-2-2/) | La scadenza di sette giorni è stata drasticamente ridotta a un giorno.<br>Data di rilascio: 24 aprile 2019. |
| [ITP 2.3](https://webkit.org/blog/9521/intelligent-tracking-prevention-2-3/) | Sono state eliminate diverse soluzioni alternative, ad esempio l&#39;utilizzo di localStorage o JavaScript `Document.referrer property`.<br>Data di rilascio: 23 settembre 2019.<br>Funzione di difesa CNAME-cloaking per ITP rilasciata in Safari 14, macOS Big Sur, Catalina, Mojave, iOS 14 e iPadOS 14. Tutti i cookie creati da una risposta HTTP di terze parti mascherata da CNAME scadranno in sette giorni.<br>Annunciato il 12 novembre 2020. |

## Qual è l&#39;impatto per me come Adobe [!DNL Target] cliente? {#impact}

[!DNL Target] fornisce librerie JavaScript da implementare sulle pagine in modo che [!DNL Target] possa offrire ai tuoi visitatori una personalizzazione in tempo reale. Esistono tre librerie JavaScript di Target at.js 1.x, at.js 2.x che inseriscono lato client [!DNL Target] cookie sui browser dei visitatori tramite `document.cookie` API. Di conseguenza, [!DNL Target] I cookie sono interessati da ITP 2.1, 2.2 e 2.3 di Apple e scadranno dopo sette giorni (con ITP 2.1) e dopo un giorno (con ITP 2.2 e ITP 2.3).

Effetti di Apple ITP 2.x [!DNL Target] nei seguenti settori:

| Impatto | Dettagli |
| --- | --- |
| Aumento potenziale dei conteggi di visitatori univoci | Poiché la finestra di scadenza è impostata su sette giorni (con ITP 2.1) e un giorno (con ITP 2.2 e ITP 2.3), si potrebbe notare un aumento dei visitatori unici provenienti dai browser Safari. Se i visitatori rivisitano il tuo dominio dopo sette giorni (ITP 2.1) o un giorno (ITP 2.2 e ITP 2.3), [!DNL Target] è costretto a mettere un nuovo [!DNL Target] cookie sul dominio al posto del cookie scaduto. Il nuovo cookie [!DNL Target] dà luogo a un nuovo visitatore univoco, nonostante si tratti sempre dello stesso visitatore. |
| Periodi di lookback ridotti per le attività [!DNL Target] | I profili dei visitatori per le attività [!DNL Target] potrebbero avere un periodo di lookback ridotto per scopi decisionali. I cookie [!DNL Target] vengono utilizzati per identificare un visitatore e archiviare gli attributi del profilo utente ai fini della personalizzazione. Dato che [!DNL Target] I cookie possono scadere su Safari dopo sette giorni (ITP 2.1) o un giorno (ITP 2.2 e 2.3), i dati del profilo utente associati all’eliminazione [!DNL Target] cookie non può essere utilizzato per le decisioni. |
| Script di profilo basati su 3rdPartyID | Poiché la finestra di scadenza è impostata su sette giorni (con ITP 2.1) e un giorno (con ITP 2.2 e ITP 2.3), [script di profilo](/help/main/c-target/c-visitor-profile/profile-parameters.md) in base al cookie 3rdPartyID non funziona più alla scadenza. |
| URL di controllo qualità/anteprima nei dispositivi iOS | Poiché la finestra di scadenza è impostata su sette giorni (con ITP 2.1) e un giorno (con ITP 2.2 e ITP 2.3), [URL di QA/anteprima](/help/main/c-activities/c-activity-qa/activity-qa.md) smetterà di funzionare alla scadenza perché gli URL sono basati sul cookie 3rdPartyID. |

## La mia attuale implementazione [!DNL Target] è interessata?

Se utilizzi la libreria Experience Cloud ID (ECID) oltre alla libreria [!DNL Target] Libreria JavaScript, l’implementazione sarà interessata nei modi elencati in questo articolo: [Impatto di Safari ITP 2.1 sui clienti Adobe Experience Cloud e Experience Platform](https://medium.com/adobetech/safari-itp-2-1-impact-on-adobe-experience-cloud-customers-9439cecb55ac).