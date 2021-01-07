---
keywords: at.js integration;supported integrations;unsupported integrations;third party integrations
description: Informazioni sulle integrazioni più comuni con Target e il loro stato di supporto con at.js.
title: Integrazioni at.js
feature: at.js
translation-type: tm+mt
source-git-commit: 6bb75e3b818a71af323614d9150e50e3e9f611b7
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 91%

---


# Integrazioni at.js{#at-js-integrations}

Informazioni sulle integrazioni più comuni con [!DNL Target] e il loro stato di supporto con at.js.

Se hai bisogno di un&#39;integrazione non supportata o menzionata qui, contatta il rappresentante del tuo account o il tuo consulente.

## Integrazioni supportate {#section_3B44A970D3FB42D1973701452C868B55}

| Integrazione | Dettagli |
|--- |--- |
| Analytics for Target (A4T) | Consulta [Adobe Analytics come origine per la generazione di rapporti per Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE). |
| Profili e Tipi di pubblico (P&amp;A) | Vedere [Audiences](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html) nella *Guida utente dei servizi di base*. |
| Servizio Experience Cloud ID | Vedi la [documentazione del Servizio Adobe Experience Cloud ID](https://experienceleague.adobe.com/docs/id-service/using/home.html). |
| Adobe Launch | Launch è la piattaforma di gestione dei tag di nuova generazione di Adobe ed è il metodo preferito per implementare Adobe Target. Launch offre ai clienti un modo semplice di implementare e gestire tutti i tag di analisi, marketing e annunci pubblicitari necessari per fornire ai clienti esperienze personalizzate.  Consulta [Implementazione di Target con Adobe Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25). |
| Dynamic Tag Management (DTM) | Consulta la guida [Best Practices for Implementation Target Using Dynamic Tag Management Guide](https://experienceleague.adobe.com/docs/dtm/implementing/overview.html) (Tecniche consigliate per l&#39;implementazione di Target con Gestione tag dinamica).   Importante: [Adobe Launch](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) è il metodo preferito e aggiornato per l’implementazione di Target e della libreria at.js. Per le nuove implementazioni di Target, utilizza Launch. La guida riportata di seguito è rivolta ai clienti esistenti che utilizzano un’implementazione DTM.   Quando si utilizza un’integrazione DTM, considera quanto segue: <ul><li>Gestione libreria: utilizza l&#39;opzione di hosting “Personalizza” per utilizzare at.js. La gestione “automatica” non è attualmente supportata. </li></ul> |
| Servizio Cloud di Adobe Experience Manager (AEM) | Il servizio Cloud di AEM consente la creazione di test A/B e attività di Targeting esperienza all&#39;interno del flusso di lavoro di AEM. Supporta at.js con Adobe Experience Manager 6.2 con FP-11577 (o versioni successive). Per ulteriori informazioni, vedi [Integrazione con Adobe Target](https://helpx.adobe.com/experience-manager/6-2/sites/administering/using/target.html) e seleziona la versione di AEM. |
| Frammenti esperienza AEM | I frammenti di esperienza creati in AEM nelle attività di Target consentono di combinare la facilità d&#39;uso e la potenza di AEM con le potenti capacità di intelligenza automatizzata (AI) ed apprendimento automatico (ML) di Target per testare e personalizzare le esperienze su grande scala.  AEM riunisce tutti i contenuti e le risorse in una posizione centrale per alimentare la tua strategia di personalizzazione. AEM consente di creare facilmente contenuti per desktop, tablet e dispositivi mobili in un&#39;unica posizione senza scrivere codice. Non è necessario creare pagine per ogni dispositivo: AEM regola automaticamente ogni esperienza utilizzando il contenuto.  Consulta [Frammenti di esperienza AEM](/help/c-experiences/c-manage-content/aem-experience-fragments.md#topic_1E1E4EA01F074349B2CF8785387B5FE8). |

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