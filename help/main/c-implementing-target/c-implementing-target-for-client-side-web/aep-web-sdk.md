---
keywords: Adobe Experience Platform Web SDK;aep web sdk;sdk Web;sdk;adobe experience cloud;piattaforma Edge network;adobe experience platform edge network;rete Edge;rete Edge;rete Edge aep edge
description: Scopri come utilizzare Adobe Experience Platform Web SDK per interagire con i vari servizi di Adobe Experience Cloud tramite AEP Edge Network.
title: Come posso implementare con Experience Platform Web SDK?
feature: AEP Web SDK
role: Developer
exl-id: afcd741f-bb7e-4bc2-b96c-ec10d5d6f4c5
source-git-commit: 719eb95049dad3bee5925dff794871cd65969f79
workflow-type: tm+mt
source-wordcount: '563'
ht-degree: 15%

---

# Adobe Experience Platform Web SDK

[!DNL Adobe Experience Platform Web SDK] (AEP Web SDK) è una libreria JavaScript lato client che consente ai clienti di [!DNL Adobe Experience Cloud] per interagire con i vari servizi dell&#39;Experience Cloud (tra cui [!DNL Target]) attraverso [!UICONTROL Adobe Experience Platform Edge Network]. Oltre alla libreria JavaScript, è presente un [!DNL Adobe Experience Platform] per informazioni sulle configurazioni dell&#39;SDK per web.

Per ulteriori informazioni, consulta i seguenti collegamenti nella sezione *Adobe Experience Platform Web SDK* aiuto:

* Per informazioni complete: [Cos’è Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=it)
* Per informazioni specifiche su [!DNL Target]: [Panoramica di Target](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/adobe-target/target-overview.html?lang=it)

## Esercitazione: Implementare Adobe Experience Cloud con Platform Web SDK

Scopri come [implementare applicazioni Experience Cloud tramite Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target=_blank}. Per informazioni specifiche su Target, consulta [Configurare Target con Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/applications-setup/setup-target.html){target=_blank} nell&#39;esercitazione.

## Documentazione consigliata

Oltre al [!DNL Platform Web SDK] documentazione di cui sopra, gli argomenti contenuti in questa guida contengono anche informazioni specifiche per [!DNL Platform Web SDK] per quanto riguarda [!DNL Target] caratteristiche e funzionalità.

| Funzione | Descrizione/Collegamento |
| --- | --- |
| [Controllo di qualità delle attività](/help/main/c-activities/c-activity-qa/activity-qa.md) | Utilizzare gli URL di controllo qualità in [!DNL Adobe Target] per eseguire attività di controllo qualità end-to-end con collegamenti di anteprima che non cambiano mai, targeting del pubblico facoltativo e reporting di controllo qualità mantenuti separati dai dati delle attività live. [!UICONTROL Controllo di qualità delle attività] consente di testare completamente il [!DNL Target] attività prima di lanciarle in diretta.<br>Vedi [Compatibilità con la modalità di controllo qualità della libreria JavaScript di Target](/help/main/c-activities/c-activity-qa/activity-qa.md#compatibility) e [URL di anteprima](/help/main/c-activities/c-activity-qa/activity-qa.md#preview). |
| [[!UICONTROL Analytics for Target] (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md) | [!DNL Adobe Analytics for Target] (A4T) è un’integrazione tra soluzioni che consente di creare attività basate su metriche di conversione e segmenti di pubblico di [!DNL Analytics]. L’integrazione di A4T consente di utilizzare i rapporti di [!DNL Analytics] per esaminare i risultati.<br>Vedi [Tipi di attività supportati](/help/main/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA) e [Passaggi per l’implementazione di un’implementazione Adobe Experience Platform Web SDK](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md#platform). |
| [Tipi di pubblico](/help/main/c-target/target.md) | Tipi di pubblico in [!DNL Adobe Target] determina chi visualizza contenuti ed esperienze in un’attività con targeting.<br>Vedi [Utilizzare l&#39;elenco Tipi di pubblico](/help/main/c-target/c-audiences/audiences.md#use-list) e [Combinare più tipi di pubblico](/help/main/c-target/combining-multiple-audiences.md). |
| [Creare tipi di pubblico](/help/main/c-target/c-audiences/audiences.md) | L’utilizzo dei tipi di pubblico creati in [!DNL Adobe Experience Platform] fornisce dati più completi sui clienti, per una personalizzazione più incisiva.<ul>Vedi [Utilizzare i tipi di pubblico da [!DNL Adobe Experience Platform]](/help/main/c-target/c-audiences/audiences.md#aep). |
| [Decisioni di offerta](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md) | Aggiungi le decisioni di offerta create in Adobe Journey Optimizer alle attività Target (test A/B manuale o targeting delle esperienze) per determinare e fornire l’offerta migliore successiva per i visitatori su web e dispositivi mobili. |
| [Offerte di reindirizzamento - Domande frequenti su A4T](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md) | Le offerte di reindirizzamento consentono ai browser dei visitatori di reindirizzare a una nuova pagina.<br>Vedi [Effettua la [!DNL Adobe Experience Platform Web SDK] supportare le offerte di reindirizzamento per A4T?](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#platform) |
| [Token di risposta](/help/main/administrating-target/response-tokens.md) | I token di risposta consentono di inviare dati di Target a Google Analytics e ad altre integrazioni di terze parti.<br>Vedi [Invio di dati a Google Analytics tramite SDK per web di Platform](/help/main/administrating-target/response-tokens.md#platform-web-sdk) per visualizzare un esempio di codice su come eseguire questa attività. |
| [Implementazione di un&#39;applicazione a pagina singola](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/adobe-target/spa-implementation.html?lang=en) in *Panoramica dell’SDK per web di Platform* guida. | [!UICONTROL Adobe Experience Platform Web SDK] offre funzioni avanzate che consentono all’azienda di eseguire personalizzazioni su tecnologie lato client di nuova generazione, come le applicazioni a pagina singola (SPA). |
| [Modifiche alla crittografia di TLS (Transport Layer Security)](https://developer.adobe.com/target/before-implement/tls-transport-layer-security-encryption/){target=_blank} | TLS (Transport Layer Security){target=_blank} ti aiuta a mantenere gli standard di sicurezza più elevati e a promuovere la sicurezza dei dati dei clienti. |