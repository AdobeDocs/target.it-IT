---
keywords: Targeting;rapporto AP;rapporti di personalizzazione automatizzata:targeting automatico;auto targeting;rapporto di targeting automatico;report di targeting automatico;personalizzazione;approfondimenti;segmenti automatizzati;FAQ;domande frequenti;attributi importanti
description: 'Scopri come utilizzare i rapporti specializzati per le attività di Automated Personalization (AP) e Targeting automatico (AT): Segmenti automatizzati e Attributi importanti.'
title: Come si utilizzano i rapporti Approfondimenti Personalization?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Reports
exl-id: 89295d95-f179-4277-ae63-453350e1bba8
TQID: https://experienceleague.adobe.com/qDaIhyfV-m3oHJArqg8TKMAe-k5QwjEUjGzhZrPSTEI
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
subfeature_v2:
  - id: fff07a91-d479-45f4-ae95-9762e79b1b7c
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 1023
ht-degree: 29%

---

# [!UICONTROL Rapporti di Personalization Insights]

Sono disponibili due report specializzati per gli utenti di [!UICONTROL attività di Automated Personalization] (AP) e [!UICONTROL Targeting automatico] (AT): i report [!UICONTROL Segmenti automatizzati] e [!UICONTROL Attributi importanti].

## Considerazioni

Quando si utilizzano i report [!UICONTROL Personalization Insights], considera quanto segue:

* Le attività di AP e AT sono disponibili come parte della [[!DNL Target Premium] soluzione](/help/main/c-intro/intro.md#premium). Non sono disponibili in [!DNL Target Standard] senza una licenza di [!DNL Target Premium].

* I report [!UICONTROL Personalization Insights] sono disponibili solo per le attività di Personalizzazione automatizzata e Targeting automatico configurate come segue:

   * [!DNL Target] generazione rapporti > [!UICONTROL Conversione]

     Ad esempio:

     ![Generazione rapporti di Target > Conversione](/help/main/c-reports/assets/conversion.png)

   * [!DNL Analytics] generazione rapporti > [!DNL Conversion]

     Ad esempio:

     ![Reporting analitico > Conversione](/help/main/c-reports/assets/analytics-reporting-conversion.png)

   * [!DNL Analytics] creazione di rapporti > [!UICONTROL Usa una metrica di Analytics] > [!UICONTROL Massimizza tasso di conversione visita]

     Ad esempio:

     ![Usa una metrica di Analytics > Massimizza tasso di conversione visita](/help/main/c-reports/assets/maximize-visit-conversion-rate.png)

* Anche le attività in cui l&#39;obiettivo di ottimizzazione è stato modificato in conversione da ricavi dopo che l&#39;attività era già attiva non sono supportate.

* I report [!UICONTROL Personalization Insights] sono disponibili solo se l&#39;obiettivo principale  è selezionato dall&#39;elenco a discesa [!UICONTROL Metrica report].

* I rapporti di [!UICONTROL Personalization Insights] sono supportati solo nell&#39;[ambiente predefinito](/help/main/administrating-target/hosts.md).

* I report [!UICONTROL Personalization Insights] vengono generati solo per le attività che si trovano nello stato [!UICONTROL Live] e che sono state attivate e ricevono traffico per almeno 15 giorni.

## Panoramica sulla generazione rapporti di Personalization Insights {#section_B47CD4A50FEB43D587F9FACD9FFD6D9D}

L&#39;obiettivo dei report [!UICONTROL Personalization Insights] è quello di fornire ulteriori informazioni su come i modelli di personalizzazione [!UICONTROL Target] dietro le attività di Personalizzazione automatizzata e Targeting automatico personalizzano il traffico del visitatore. L&#39;[algoritmo Foresta casuale](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) è la base per i modelli di personalizzazione [!DNL Target].

Poiché l&#39;obiettivo dei report [!UICONTROL Personalization Insights] è comprendere in che modo i modelli di personalizzazione [!DNL Target] hanno deciso di inviare un visitatore a quali parti di contenuto, i report [!UICONTROL Personalization Insights] riflettono solo un sottosegmento di tutto il traffico gestito dall&#39;attività di AP o AT. In particolare, i due rapporti riflettono tutto il traffico che ha utilizzato il modello di personalizzazione. In altre parole, i rapporti [!UICONTROL Registri di personalizzazione] non considerano il traffico di controllo o il traffico gestito dal modello vincitore complessivo.

Sono disponibili due rapporti di [!UICONTROL Personalization Insights]:

| Rapporto | Dettagli |
|--- |--- |
| [!UICONTROL Segmenti automatizzati] | I vari visitatori rispondono in modo diverso alle offerte/esperienze nell&#39;attività di AP/AT. Questo report mostra come diversi segmenti automatizzati definiti dai modelli di personalizzazione [!DNL Target] hanno risposto alle offerte/esperienze nell&#39;attività. |
| [!UICONTROL Attributi importanti] | Nelle varie attività, i vari attributi possono essere più o meno importanti per il modo in cui il modello decide di personalizzare. Questo rapporto mostra gli attributi principali che hanno influenzato il modello e la loro importanza relativa. |

## Interpretazione degli attributi in Personalization Insights {#section_B5C45E723EC941BDA2A7A642EEB30E4D}

Esistono due tipi di attributi rappresentati nei rapporti [!UICONTROL Registri di personalizzazione] e utilizzati nei modelli di PA e Targeting automatico:

* **Attributi raccolti automaticamente da Target:** [!DNL Target] utilizza un set di dati base per creare gli algoritmi di personalizzazione nelle attività di AP e AT che si riflettono in Personalization Insights. Consulta [Raccolta dati per gli algoritmi Personalization](/help/main/c-activities/t-automated-personalization/ap-data.md) di Target per i tipi di dati, gli attributi di esempio e la relativa convenzione di denominazione [!UICONTROL Personalization Insights]. Tieni presente che anche se questi attributi vengono considerati, i modelli di una singola attività potrebbero non utilizzare tutti questi attributi nel modello finale.
* **Attributi passati a Target:** Consulta [Caricamento dei dati per gli algoritmi di Personalization di Target](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md).

[!DNL Target] consente di passare dati aggiuntivi a [!DNL Target] per arricchire il set di dati base utilizzato per creare gli algoritmi di personalizzazione nelle attività di AP e AT in diversi modi:

| Tipo di dati | Descrizione | Convenzione sulla denominazione del tipo di dati |
|--- |--- |--- |
| Attributi profilo, inclusi gli script del profilo, API di aggiornamento profilo e attributi del profilo in-page | Tutte le informazioni da includere nel profilo utente di Target.<br>Queste informazioni possono provenire da script di profilo, informazioni caricate utilizzando l’API di aggiornamento del profilo o parametri di profilo nella mbox con il prefisso “profile”. | `Custom - Profile - [parameter name]` |
| Parametri di pagina (detti anche &quot;parametri mbox&quot;) | Coppie di nome/valore trasmesse direttamente attraverso il codice di pagina che non sono memorizzate nel profilo del visitatore per un utilizzo futuro. | `Custom - Mbox Parameter - [parameter name]` |
| Attributi del cliente | Gli attributi dei clienti consentono di caricare i dati del profilo visitatori tramite FTP nell&#39;Experience Cloud. Una volta effettuato l&#39;aggiornamento, sfrutta i dati in Adobe Analytics e Adobe Target. | `Custom - Customer Attributes - [parameter name]` |
| Destinatari condivisi (Adobe Audience Manager o Adobe Analytics) | Destinatari creati tramite Adobe Audience Manager o Adobe Analytics e condivisi con Target. | `Custom - Experience Cloud Segment - [segment name]` |
| Pubblico condiviso (Adobe Experience Platform/Real-time CDP) | Tipi di pubblico creati tramite Adobe Experience Platform/Real-time CDP e condivisi con Target tramite Destinations. | `Custom - Adobe Experience Platform Segment - [segment name]` |
| Attributi condivisi (Adobe Experience Platform/Real-time CDP) | Attributi creati tramite Adobe Experience Platform/Real-time CDP e condivisi con Target tramite Destinations. Questa funzione è attualmente in Beta. | `Custom - Adobe Experience Platform Attribute - [attribute name]]` |
| Destinatari di reporting nell&#39;attività - Segmenti | I tipi di pubblico definiti nell&#39;attività di Personalizzazione automatizzata e Targeting automatico durante l&#39;impostazione in &quot;Obiettivi e metriche&quot;. | `Custom - Reporting Segment - [segment name]` |

## Domande frequenti

Elenco delle domande frequenti sui report [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Targeting automatico] [!UICONTROL Insights].

### Per quanto tempo persistono i dati per i modelli [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Targeting automatico]?

I modelli [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Targeting automatico] sono stati addestrati negli ultimi 45 giorni di comportamento dell&#39;utente (profili utente, eventi di impression ed eventi di conversione) per l&#39;attività.

I modelli [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Targeting automatico] conservano il comportamento dell&#39;utente, i record di formazione e i dati di decisione del modello per 90 giorni per produrre [!UICONTROL report Approfondimenti]. Dopo 90 giorni, i documenti relativi alla formazione e i modelli decisi vengono eliminati. Anche i modelli [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Targeting automatico] conservano dati di conversione e impression a livello di esperienza/offerta aggregati a scopo di reporting per due anni. Questi dati sono solo dati a livello aggregato e non contengono dati di profilo a livello individuale.

## Video di formazione: Utilizzo dei rapporti Approfondimenti Personalization ![Icona esercitazione](/help/main/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/25601/)

Per ulteriori informazioni, vedere [Utilizzo dei rapporti Approfondimenti Personalization in Adobe Target](https://helpx.adobe.com/target/kt/using/personalization-insights-report-feature-video-use.html).

## Blog di Adobe

* Parte 1: [Estrarre il mistero dalla magia del Personalization basato sull&#39;intelligenza artificiale](https://theblog.adobe.com/taking-mystery-magic-ai-driven-personalization-part-1/)
* Parte 2: [Uno sguardo dietro la cortina dell&#39;intelligenza artificiale per Personalization in Adobe Target](https://theblog.adobe.com/a-peek-behind-the-curtain-of-ai-for-personalization-in-adobe-target/)
* Parte 3: [MAGIX — la soluzione al problema Black Box di Personalization basato sull&#39;intelligenza artificiale](https://theblog.adobe.com/magix-the-solution-to-the-black-box-issue-of-ai-driven-personalization/)
