---
description: Informazioni sulle integrazioni più comuni con Target e il loro stato di supporto con at.js.
keywords: integrazioni at.js;integrazioni supportate;integrazioni non supportate;integrazioni di terze parti
seo-description: Informazioni sulle integrazioni più comuni con Target e il loro stato di supporto con at.js.
seo-title: Integrazioni at.js
solution: Target
title: Integrazioni at.js
topic: Standard
uuid: 19036a1d-941c-4d31-8c7b-f50c86996b1c
translation-type: tm+mt
source-git-commit: ffa6585834b271838629d65ceb00d1770b37e80c

---


# Integrazioni at.js{#at-js-integrations}

Informazioni sulle integrazioni più comuni con [!DNL Target] e il loro stato di supporto con at.js.

Se hai bisogno di un&#39;integrazione non supportata o menzionata qui, contatta il rappresentante del tuo account o il tuo consulente.

## Integrazioni supportate {#section_3B44A970D3FB42D1973701452C868B55}

| Integrazione | Dettagli |
|--- |--- |
| Analytics for Target (A4T) | Consulta [Adobe Analytics come origine per la generazione di rapporti per Adobe Target (A4T)](../../../c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE). |
| Profili e Tipi di pubblico (P&amp;A) | Vedi [Tipi di pubblico](https://marketing.adobe.com/resources/help/en_US/mcloud/audience_library.html) nella Guida di Adobe Experience Cloud e servizi di base. |
| Servizio Experience Cloud ID | Vedi la [documentazione del Servizio Adobe Experience Cloud ID](https://marketing.adobe.com/resources/help/en_US/mcvid/). |
| Adobe Launch | Launch è la piattaforma di gestione dei tag di nuova generazione di Adobe ed è il metodo preferito per implementare Adobe Target. Launch offre ai clienti un modo semplice di implementare e gestire tutti i tag di analisi, marketing e annunci pubblicitari necessari per fornire ai clienti esperienze personalizzate.  Consulta [Implementazione di Target con Adobe Launch](../../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25). |
| Dynamic Tag Management (DTM) | Vedi la [guida all’implementazione di Target con Dynamic Tag Management](https://marketing.adobe.com/resources/help/en_US/target/ov2/implementing-target-using-dynamic-tag-management.html).   Importante: [Adobe Launch](../../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) è il metodo preferito e aggiornato per l’implementazione di Target e della libreria at.js. Per le nuove implementazioni di Target, utilizza Launch. La guida riportata di seguito è rivolta ai clienti esistenti che utilizzano un’implementazione DTM.   Quando si utilizza un’integrazione DTM, considera quanto segue: <ul><li>Gestione libreria: utilizza l&#39;opzione di hosting “Personalizza” per utilizzare at.js. La gestione “automatica” non è attualmente supportata. </li></ul> |
| Servizio Cloud di Adobe Experience Manager (AEM) | Il servizio Cloud di AEM consente la creazione di test A/B e attività di Targeting esperienza all&#39;interno del flusso di lavoro di AEM. Supporta at.js con Adobe Experience Manager 6.2 con FP-11577 (o versioni successive). Per ulteriori informazioni, vedi [Integrazione con Adobe Target](https://helpx.adobe.com/experience-manager/6-2/sites/administering/using/target.html) e seleziona la versione di AEM. |
| Frammenti esperienza AEM | I frammenti di esperienza creati in AEM nelle attività di Target consentono di combinare la facilità d&#39;uso e la potenza di AEM con le potenti capacità di intelligenza automatizzata (AI) ed apprendimento automatico (ML) di Target per testare e personalizzare le esperienze su grande scala.  AEM riunisce tutti i contenuti e le risorse in una posizione centrale per alimentare la tua strategia di personalizzazione. AEM consente di creare facilmente contenuti per desktop, tablet e dispositivi mobili in un&#39;unica posizione senza scrivere codice. Non è necessario creare pagine per ogni dispositivo: AEM regola automaticamente ogni esperienza utilizzando il contenuto.  Consulta [Frammenti di esperienza AEM](../../../c-experiences/c-manage-content/aem-experience-fragments.md#topic_1E1E4EA01F074349B2CF8785387B5FE8). |

## Integrazioni non supportate {#section_8EFCAED418DC42E0B07F95924819EAC2}

| Integrazione | Dettagli |
|--- |--- |
| [!DNL Legacy Target to SiteCatalyst Integration] | Questa era l’integrazione che inviava gli ID di campagne e ricette a [!DNL SiteCatalyst] tramite la richiesta di pagina in modo da poter usare le funzioni di reporting nell’interfaccia di [!DNL SiteCatalyst]. A4T sostituisce questa funzionalità. |
| [!DNL Legacy Target to SiteCatalyst Integration] | Questa era l’integrazione che effettuava le chiamate mbox `"SiteCatalyst: Event"` e `"SiteCatalyst: Purchase"` che consentivano di generare metriche di successo e profili utente basati su eVar e Prop. A4T e P&amp;A sostituiscono questa funzionalità. |
| [!DNL Legacy Audience Manager (AAM) to Target Integration] | Questa era l’integrazione che effettuava una chiamata API front-end per recuperare i segmenti AAM e inviarli come parametri mbox per ogni chiamata mbox sulla pagina. |

## Integrazioni di terze parti {#section_EE599839CCAD49DD97640E5EDAD9082E}

| Integrazione | Dettagli |
|--- |--- |
| Altri gestori di tag | at. js dovrebbe funzionare con piattaforme di gestione dei tag non-Adobe, ma presta attenzione quando utilizzi funzionalità di integrazione personalizzate sviluppate da altri fornitori. Le loro integrazioni potrebbero dipendere da funzioni interne di mbox.js che non esistono più in at.js. |
| Provider di dati di terze parti (ad esempio Demandbase, BlueKai, API meteo) | Molti fornitori di dati di terze parti utilizzati per integrare la profilazione utente di Target possono essere integrati utilizzando la funzionalità [Fornitori di dati](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers) di at.js. |