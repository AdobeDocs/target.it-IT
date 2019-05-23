---
description: 'Per gli utenti di attività di Personalizzazione automatizzata (AP) e Targeting automatico (AT) sono disponibili due rapporti specializzati: Segmenti automatizzati e Attributi importanti.'
keywords: Targeting;rapporto AP;rapporti di personalizzazione automatizzata:targeting automatico;auto targeting;rapporto di targeting automatico;report di targeting automatico;personalizzazione;approfondimenti;segmenti automatizzati;FAQ;domande frequenti;attributi importanti
seo-description: 'Per gli utenti di attività di Personalizzazione automatizzata (AP) e Targeting automatico (AT) sono disponibili due rapporti specializzati: Segmenti automatizzati e Attributi importanti.'
seo-title: Rapporti Approfondimenti personalizzazione
solution: Target
title: Rapporti Approfondimenti personalizzazione
title-outputclass: premium
uuid: 2507a7a6-d229-412a-a992-5777b45c80e7
badge: premium
translation-type: tm+mt
source-git-commit: 6cd0179b3fc1df8ec9ae1cbecd10749f751d9cd8

---


# ![PREMIUM](/help/assets/premium.png) Rapporti Approfondimenti personalizzazione{#personalization-insights-reports}

Per gli utenti di attività di Personalizzazione automatizzata (AP) e Targeting automatico (AT) sono disponibili due rapporti specializzati: i rapporti Segmenti automatizzati e Attributi importanti.

>[!NOTE]
>
>Le attività di AP e AT sono disponibili come parte della soluzione [!DNL Target Premium]. Non sono disponibili in [!DNL Target Standard] senza una licenza di [!DNL Target Premium].
>
>I rapporti di Approfondimenti personalizzazione sono disponibili solo per le attività di AP e AT che utilizzano un obiettivo di ottimizzazione delle conversioni. Anche le attività in cui l&#39;obiettivo di ottimizzazione è stato modificato in conversione da ricavi dopo che l&#39;attività era già attiva non sono supportate.
>
>I rapporti Approfondimenti personalizzati sono supportati solo nell’[ambiente predefinito](../../administrating-target/hosts.md).

## Panoramica sui rapporti di Registri di personalizzazione {#section_B47CD4A50FEB43D587F9FACD9FFD6D9D}

L&#39;obiettivo dei rapporti [!UICONTROL Registri di personalizzazione] è fornire maggiori informazioni sulle modalità con cui i modelli di personalizzazione di Target dietro le attività di Personalizzazione automatizzata (AP) e Targeting automatico (AT) personalizzano il traffico del visitatore. L’[algoritmo Foresta casuale](/help/c-activities/t-automated-personalization/algo-random-forest.md) è la base dei modelli di personalizzazione di Target.

Poiché l’obiettivo dei rapporti Registri di personalizzazione è comprendere il criterio con cui i modelli di personalizzazione di Target assegnano a ciascun contenuto un visitatore, i rapporti Registri di personalizzazione riflettono solo un sotto-segmento di tutto il traffico gestito dall&#39;attività di AP o AT. In particolare, i due rapporti riflettono tutto il traffico che ha utilizzato il modello di personalizzazione. In altre parole, i rapporti Registri di personalizzazione non considerano il traffico di controllo o il traffico gestito dal modello vincitore complessivo.

Sono disponibili due rapporti:

| Rapporto | Dettagli |
|--- |--- |
| Segmenti automatizzati | I vari visitatori rispondono in modo diverso alle offerte/esperienze nell&#39;attività di AP/AT. Questo rapporto mostra come i diversi segmenti automatizzati definiti dai modelli di personalizzazione di Target rispondono alle offerte/esperienze dell&#39;attività. |
| Attributi importanti | Nelle varie attività, i vari attributi possono essere più o meno importanti per il modo in cui il modello decide di personalizzare. Questo rapporto mostra gli attributi principali che hanno influenzato il modello e la loro importanza relativa. |

## Interpretazione degli attributi in Approfondimenti personalizzazione {#section_B5C45E723EC941BDA2A7A642EEB30E4D}

Esistono·due·tipi·di·attributi·rappresentati·nei·rapporti·[!UICONTROL Registri·di·personalizzazione]·e·utilizzati·nei·modelli·di·Personalizzazione automatizzata (AP) e Targeting automatico (AT):

* **Attributi raccolti automaticamente da Target:** Target utilizza un set di dati base per la creazione degli algoritmi di personalizzazione nelle attività di AP e AT che si riflettono in Registri di personalizzazione. Consulta [Raccolta di dati per gli algoritmi di personalizzazione di Target](../../c-activities/t-automated-personalization/ap-data.md#reference_255BD3DE7AD04DC9B766E0BC78961058) per i tipi di dati, gli attributi di esempio e la relativa convenzione di denominazione per [!UICONTROL Registri di personalizzazione]. Tieni presente che nonostante questi attributi vengano considerati, i modelli di una singola attività potrebbero non utilizzare tutti gli attributi nel modello finale.
* **Attributi passati a Target:** vedi  [Caricamento dei dati per gli algoritmi di personalizzazione Target](../../c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md#concept_85EA505B37E54514A1C8AB91553FEED6).

Target offre diverse opzioni per la trasmissione di dati a Target al fine di aumentare il set di dati base utilizzati per la creazione di algoritmi di personalizzazione nelle attività di AP e AT:

| Tipo di dati | Descrizione | Convenzione sulla denominazione del tipo di dati |
|--- |--- |--- |
| Attributi profilo, inclusi gli script del profilo, API di aggiornamento profilo e attributi del profilo in-page | Tutte le informazioni da includere nel profilo utente di Target.<br>Queste informazioni possono provenire da script di profilo, informazioni caricate utilizzando l’API di aggiornamento del profilo o parametri di profilo nella mbox con il prefisso “profile”. | `Custom - Profile - [parameter name]` |
| Parametri di pagina (detti anche “parametri mbox”) | Coppie di nome/valore trasmesse direttamente attraverso il codice di pagina che non sono memorizzate nel profilo del visitatore per un utilizzo futuro. | `Custom - Mbox Parameter - [parameter name]` |
| Attributi del cliente | Gli attributi dei clienti consentono di caricare i dati del profilo visitatori tramite FTP nell&#39;Experience Cloud. Una volta effettuato l&#39;aggiornamento, sfrutta i dati in Adobe Analytics e Adobe Target. | `Custom - Customer Attributes - [parameter name]` |
| Destinatari condivisi (Adobe Audience Manager o Adobe Analytics) | Destinatari creati tramite Adobe Audience Manager o Adobe Analytics e condivisi con Target. | `Custom - Experience Cloud Segment - [segment name]` |
| Destinatari di reporting nell&#39;attività - Segmenti | I destinatari definiti nell&#39;attività di Personalizzazione automatizzata o Targeting automatico durante l&#39;impostazione in “Obiettivi e Metrica”. | `Custom - Reporting Segment - [segment name]` |

## Video di formazione: Utilizzo dei rapporti Approfondimenti personalizzazione

>[!VIDEO](https://video.tv.adobe.com/v/25601/)

Per ulteriori informazioni, consulta [Utilizzo dei report personalizzazione di Adobe Target](https://helpx.adobe.com/target/kt/using/personalization-insights-report-feature-video-use.html).
