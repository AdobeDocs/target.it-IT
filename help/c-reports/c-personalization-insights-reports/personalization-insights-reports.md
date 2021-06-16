---
keywords: Targeting;rapporto AP;rapporti di personalizzazione automatizzata:targeting automatico;auto targeting;rapporto di targeting automatico;report di targeting automatico;personalizzazione;approfondimenti;segmenti automatizzati;FAQ;domande frequenti;attributi importanti
description: Scopri come utilizzare i rapporti specializzati per le attività di Automated Personalization (AP) e Targeting automatico (AT) - Segmenti automatizzati e Attributi importanti.
title: Come si utilizzano i rapporti Approfondimenti personalizzazione?
feature: Rapporti
exl-id: 89295d95-f179-4277-ae63-453350e1bba8
source-git-commit: c0eae79da63e2f269f603b4d9fd2a5a1170e2687
workflow-type: tm+mt
source-wordcount: '862'
ht-degree: 59%

---

# ![PREMIUM](/help/assets/premium.png) Rapporti Approfondimenti personalizzazione

Per gli utenti di attività di [!UICONTROL Personalizzazione automatizzata] (AP) e Targeting automatico (TA) sono disponibili due report specializzati: i rapporti [!UICONTROL Segmenti automatizzati] e Attributi importanti.

>[!NOTE]
>
>Quando utilizzi i rapporti Approfondimenti personalizzazione , considera quanto segue:
>
>* Le attività di AP e AT sono disponibili come parte della soluzione [!DNL Target Premium]. Non sono disponibili in [!DNL Target Standard] senza una licenza di [!DNL Target Premium].
   >
   >
* [!UICONTROL I rapporti di Approfondimenti personalizzazione sono disponibili solo per le attività di AP e AT che utilizzano un obiettivo di ottimizzazione delle conversioni. ] Anche le attività in cui l&#39;obiettivo di ottimizzazione è stato modificato in conversione da ricavi dopo che l&#39;attività era già attiva non sono supportate.
   >
   >
* [!UICONTROL I rapporti ] Approfondimenti personalizzazione sono disponibili solo se l’ [!UICONTROL obiettivo primario ] è selezionato dall’elenco a discesa  [!UICONTROL Metrica ] rapporto .
   >
   >
* I rapporti Approfondimenti personalizzati sono supportati solo nell’[ambiente predefinito](/help/administrating-target/hosts.md).
   >
   >
* [!UICONTROL I rapporti ] Approfondimenti personalizzazione sono generati solo per le attività che si trovano in   Livestatus e sono state attivate e ricevono traffico per almeno 15 giorni.


## Panoramica sui rapporti di Registri di personalizzazione {#section_B47CD4A50FEB43D587F9FACD9FFD6D9D}

L&#39;obiettivo dei rapporti [!UICONTROL Registri di personalizzazione] è fornire maggiori informazioni sulle modalità con cui i modelli di personalizzazione di Target dietro le attività di Personalizzazione automatizzata (AP) e Targeting automatico (AT) personalizzano il traffico del visitatore.  L’ [algoritmo Foresta casuale](/help/c-activities/t-automated-personalization/algo-random-forest.md) è la base dei modelli di personalizzazione [!DNL Target].

Poiché l&#39;obiettivo dei rapporti [!UICONTROL Registri di personalizzazione] è comprendere in che modo i modelli di personalizzazione [!DNL Target] hanno deciso di inviare il visitatore a quale parte di contenuto, i rapporti [!UICONTROL Registri di personalizzazione] riflettono solo un sotto-segmento di tutto il traffico gestito dall&#39;attività di PA o TA. In particolare, i due rapporti riflettono tutto il traffico che ha utilizzato il modello di personalizzazione. In altre parole, i rapporti [!UICONTROL Registri di personalizzazione] non considerano il traffico di controllo o il traffico gestito dal modello vincitore complessivo.

Sono disponibili due rapporti [!UICONTROL Registri di personalizzazione] :

| Rapporto | Dettagli |
|--- |--- |
| [!UICONTROL Segmenti automatizzati] | I vari visitatori rispondono in modo diverso alle offerte/esperienze nell&#39;attività di AP/AT. Questo rapporto mostra come i diversi segmenti automatizzati definiti dai modelli di personalizzazione [!DNL Target] rispondono alle offerte/esperienze nell’attività. |
| [!UICONTROL Attributi importanti] | Nelle varie attività, i vari attributi possono essere più o meno importanti per il modo in cui il modello decide di personalizzare. Questo rapporto mostra gli attributi principali che hanno influenzato il modello e la loro importanza relativa. |

## Interpretazione degli attributi in Approfondimenti personalizzazione {#section_B5C45E723EC941BDA2A7A642EEB30E4D}

Esistono due tipi di attributi rappresentati nei rapporti [!UICONTROL Registri di personalizzazione] e utilizzati nei modelli di Personalizzazione automatizzata (AP) e Targeting automatico (AT):

* **Attributi raccolti automaticamente da :**[!DNL Target] Target utilizza un set di dati base per la creazione degli algoritmi di personalizzazione nelle attività di AP e AT che si riflettono in Registri di personalizzazione. Consulta [Raccolta di dati per gli algoritmi di personalizzazione di Target](/help/c-activities/t-automated-personalization/ap-data.md) per i tipi di dati, gli attributi di esempio e la relativa convenzione di denominazione per [!UICONTROL Registri di personalizzazione]. Tieni presente che nonostante questi attributi vengano considerati, i modelli di una singola attività potrebbero non utilizzare tutti gli attributi nel modello finale.
* **Attributi trasmessi a Target:** vedi [Caricamento dei dati per gli algoritmi di personalizzazione Target](/help/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md).

[!DNL Target] offre diverse opzioni per la trasmissione di dati a al fine di aumentare il set di dati base utilizzati per la creazione di algoritmi di personalizzazione nelle attività di AP e AT:[!DNL Target]

| Tipo di dati | Descrizione | Convenzione sulla denominazione del tipo di dati |
|--- |--- |--- |
| Attributi profilo, inclusi gli script del profilo, API di aggiornamento profilo e attributi del profilo in-page | Tutte le informazioni da includere nel profilo utente di Target.<br>Queste informazioni possono provenire da script di profilo, informazioni caricate utilizzando l’API di aggiornamento del profilo o parametri di profilo nella mbox con il prefisso “profile”. | `Custom - Profile - [parameter name]` |
| Parametri di pagina (detti anche “parametri mbox”) | Coppie di nome/valore trasmesse direttamente attraverso il codice di pagina che non sono memorizzate nel profilo del visitatore per un utilizzo futuro. | `Custom - Mbox Parameter - [parameter name]` |
| Attributi del cliente | Gli attributi dei clienti consentono di caricare i dati del profilo visitatori tramite FTP nell&#39;Experience Cloud. Una volta effettuato l&#39;aggiornamento, sfrutta i dati in Adobe Analytics e Adobe Target. | `Custom - Customer Attributes - [parameter name]` |
| Destinatari condivisi (Adobe Audience Manager o Adobe Analytics) | Destinatari creati tramite Adobe Audience Manager o Adobe Analytics e condivisi con Target. | `Custom - Experience Cloud Segment - [segment name]` |
| Destinatari di reporting nell&#39;attività - Segmenti | I destinatari definiti nell&#39;attività di Personalizzazione automatizzata o Targeting automatico durante l&#39;impostazione in “Obiettivi e Metrica”. | `Custom - Reporting Segment - [segment name]` |

## Domande frequenti 

Elenco delle domande frequenti sui rapporti [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Targeting automatico] [!UICONTROL Approfondimenti].

### Per quanto tempo persistono i dati per i modelli [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Targeting automatico]?

[!UICONTROL I modelli di Automated Personalization]  (AP) e  [!UICONTROL Auto-] Targeting vengono addestrati negli ultimi 45 giorni del comportamento degli utenti (profili utente, eventi di impression ed eventi di conversione) per l’attività.

[!UICONTROL I modelli Automated Personalization]  (AP) e  [!UICONTROL Auto-] Targeting conservano il comportamento degli utenti, i record di formazione e i dati decisionali del modello per 90 giorni per produrre rapporti   Approfondimenti. Dopo 90 giorni, i record di formazione e le decisioni relative ai modelli vengono scartati. [!UICONTROL Anche i modelli Automated Personalization]  (AP) e  [!UICONTROL Auto-] Targeting conservano per due anni i dati aggregati di impression/offerta a livello di offerta e conversione a scopo di reporting. Questi dati sono solo dati a livello aggregato e non contengono dati di profilo a livello individuale.

## Video di formazione: Utilizzo dei rapporti Approfondimenti personalizzazione ![Badge tutorial](/help/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/25601/)

Per ulteriori informazioni, consulta [Utilizzo dei rapporti Approfondimenti personalizzazione in Adobe Target](https://helpx.adobe.com/target/kt/using/personalization-insights-report-feature-video-use.html).

## Blog di Adobe

* Parte 1: [Estrarre il mistero dalla magia della personalizzazione guidata dall&#39;intelligenza artificiale](https://theblog.adobe.com/taking-mystery-magic-ai-driven-personalization-part-1/)
* Parte 2: [Un&#39;occhiata dietro la tenda dell&#39;intelligenza artificiale per la personalizzazione in Adobe Target](https://theblog.adobe.com/a-peek-behind-the-curtain-of-ai-for-personalization-in-adobe-target/)
* Parte 3: [MAGIX — la soluzione al problema del Black Box della personalizzazione guidata dall&#39;intelligenza artificiale](https://theblog.adobe.com/magix-the-solution-to-the-black-box-issue-of-ai-driven-personalization/)
