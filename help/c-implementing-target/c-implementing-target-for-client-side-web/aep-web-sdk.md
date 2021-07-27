---
keywords: Adobe Experience Platform Web SDK;aep web sdk;sdk Web;sdk;adobe experience cloud;piattaforma Edge network;adobe experience platform edge network;rete Edge;rete Edge;rete Edge aep edge
description: Scopri come utilizzare Adobe Experience Platform Web SDK per interagire con i vari servizi di Adobe Experience Cloud tramite AEP Edge Network.
title: Come posso implementare con Experience Platform Web SDK?
feature: AEP Web SDK
role: Developer
exl-id: afcd741f-bb7e-4bc2-b96c-ec10d5d6f4c5
source-git-commit: 28be06a329d017fd25d069986a0b7b047ddda206
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 6%

---

# Tutorial per Adobe Experience Platform Web SDK

[!DNL Adobe Experience Platform Web SDK] (AEP Web SDK) è una libreria JavaScript lato client che consente ai clienti di  [!DNL Adobe Experience Cloud] interagire con i vari servizi dell’Experience Cloud (incluso  [!DNL Target]) tramite  [!UICONTROL Adobe Experience Platform Edge Network]. Oltre alla libreria JavaScript, esiste un&#39;estensione [!DNL Experience Platform Launch] per facilitare le configurazioni dell&#39;SDK per web.

Per ulteriori informazioni, consulta i seguenti collegamenti nella guida *Adobe Experience Platform Web SDK* :

* Per informazioni complete: [Cos&#39;è Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html)
* Per informazioni specifiche su [!DNL Target]: [Panoramica di Target](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/adobe-target/target-overview.html)

## Documentazione consigliata

Oltre alla documentazione [!DNL Platform Web SDK] di cui sopra, gli argomenti di questa guida contengono anche informazioni specifiche sulle [!DNL Platform Web SDK] relative alle funzioni e alle funzionalità [!DNL Target].

| Funzione | Descrizione/Collegamento |
| --- | --- |
| [Controllo di qualità delle attività](/help/c-activities/c-activity-qa/activity-qa.md) | Gli URL di controllo qualità in [!DNL Adobe Target] consentono di verificare in modo semplice e completo la qualità delle attività tramite collegamenti di anteprima che restano invariati, l’eventuale definizione di un pubblico di destinazione e rapporti di controllo qualità mantenuti separati dai dati delle attività live. [!UICONTROL Il ] controllo qualità delle attività ti consente di testare completamente  [!DNL Target] le attività prima di avviarle in diretta.<br>Consulta  [Compatibilità della modalità di controllo qualità della libreria JavaScript di Target ](/help/c-activities/c-activity-qa/activity-qa.md#compatibility) e  [URL di anteprima](/help/c-activities/c-activity-qa/activity-qa.md#preview). |
| [[!UICONTROL Analytics for Target] (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md) | [!DNL Adobe Analytics for Target] (A4T) è un’integrazione tra più soluzioni che consente di creare attività basate su metriche di  [!DNL Analytics] conversione e segmenti di pubblico. L’integrazione A4T consente di utilizzare i rapporti [!DNL Analytics] per esaminare i risultati.<br>Consulta  [Tipi di attività ](/help/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA) supportati e Passaggi  [di implementazione per un’implementazione Adobe Experience Platform Web SDK](/help/c-integrating-target-with-mac/a4t/a4timplementation.md#platform). |
| [Tipi di pubblico](/help/c-target/target.md) | I tipi di pubblico in [!DNL Adobe Target] determinano chi visualizza contenuti ed esperienze in un’attività con targeting.<br>Consulta  [Utilizzare l&#39;](/help/c-target/c-audiences/audiences.md#use-list) elenco Tipi di pubblico e  [Combinare più tipi di pubblico](/help/c-target/combining-multiple-audiences.md). |
| [Offerte di reindirizzamento - Domande frequenti su A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md) | Le offerte di reindirizzamento consentono ai browser dei visitatori di reindirizzare a una nuova pagina.<br>Consulta  [Supporta  [!DNL Adobe Experience Platform Web SDK] le offerte di reindirizzamento per A4T?](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#platform) |
| [Token di risposta](/help/administrating-target/response-tokens.md) | I token di risposta consentono di inviare dati di Target a Google Analytics e ad altre integrazioni di terze parti.<br>Per un esempio di codice per eseguire questa attività, consulta  [Invio di dati a Google Analytics tramite ](/help/administrating-target/response-tokens.md#platform-web-sdk) SDK per web di Platform. |
| [Implementazione di applicazioni a pagina singola ](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/adobe-target/spa-implementation.html?lang=en) nella guida  *panoramica* Platform Web SDK. | [!UICONTROL Adobe Experience Platform Web ] SDKfornisce funzioni avanzate che consentono all’azienda di eseguire personalizzazioni su tecnologie lato client di nuova generazione, come le applicazioni a pagina singola (SPA). |
| [Modifiche alla crittografia di TLS (Transport Layer Security)](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md) | TLS (Transport Layer Security) ti aiuta a mantenere gli standard di sicurezza più elevati e a promuovere la sicurezza dei dati dei clienti. |
