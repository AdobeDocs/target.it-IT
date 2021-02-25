---
keywords: Target Standard;Recommendations;Target Premium; Automated Personalization;auto-target;auto target;permissions;what is adobe target;
description: Apprendi le basi di Adobe Target Standard e Adobe Target Premium. Target Premium include funzionalità avanzate non disponibili nel prodotto Standard.
landing-page-description: Personalizza l’esperienza dei clienti per massimizzare le entrate tramite siti web, app mobili, social media e altri canali digitali.
title: Cos'è Target?
feature: Panoramica
translation-type: tm+mt
source-git-commit: 345b0f805ef65364b891f6754f4aaf78c163f334
workflow-type: tm+mt
source-wordcount: '947'
ht-degree: 43%

---


# Introduzione a Target

[!DNL Adobe Target] è la  [!DNL Adobe Experience Cloud] soluzione che offre tutto il necessario per adattare e personalizzare le esperienze dei clienti. [!DNL Target] consente di massimizzare le entrate sui siti Web e mobili, le app, i social media e altri canali digitali.

La soluzione [!DNL Adobe Target] può essere concessa in licenza come [!DNL Target Standard] o [!DNL Target Premium].

## Target Standard {#section_ACD5EFF17AAB4E979CBEFA0145CCD905}

[!DNL Target Standard] è il front-end  [!DNL Adobe Target] che consente di creare e gestire visivamente test A/B e attività di targeting basate su regole. [!DNL Target Standard] supporta l&#39;inserimento personalizzato del codice sia nel flusso di lavoro di  [!UICONTROL Visual Experience Composer]  (VEC) che in quello esterno. [!DNL Target Standard] offre una strategia di implementazione semplificata con le tue proprietà digitali. Una singola riga di codice su ogni pagina gestisce tutte le comunicazioni necessarie tra il sito e  [!DNL Target].

Le best practice di settore sono integrate in [!DNL Target Standard]. [!DNL Target Standard] è progettato per utenti esperti e nuovi. Puoi condividere dati e risultati e collaborare facilmente con altri membri del gruppo che utilizzano [!DNL Adobe Experience Cloud].

## Target Premium {#premium}

[!DNL Target Premium] è un&#39; [!DNL Target] offerta avanzata che richiede una licenza per aggiungere funzionalità premium a  [!DNL Target Standard].

Tutti gli articoli [!DNL Target Premium] di questa guida includono il contrassegno Premium nella parte superiore di ogni pagina:

![Badge Premium](/help/assets/premium.png)

In Target sono incluse le seguenti funzionalità Premium:

### Personalizzazione automatizzata

[ Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) (AP) fornisce algoritmi di machine learning avanzati per esperienze personalizzate e tassi di conversione migliorati per esperienze digitali.

[!UICONTROL Automated ] Personalization (Personalizzazione automatizzata) registra l&#39;attività dei visitatori sul sito, creando un profilo di visitatori in modo che il contenuto possa essere indirizzato a visitatori simili. AP tiene traccia delle risposte ai contenuti, sia per gli individui che per la popolazione nel suo insieme. AP utilizza quindi sofisticati approcci di modellazione per eseguire automaticamente il targeting di ogni singolo utente. AP considera tutto ciò che è noto su ogni visitatore.

[!UICONTROL Automated ] Personalization (Personalizzazione automatizzata) apprende da sola e richiede un&#39;analisi minima degli utenti. Completamente automatizzato, AP apprende in modo continuo. Il sistema crea modelli e impara automaticamente a quali prodotti è più probabile che un singolo visitatore sia interessato. Ogni volta che un visitatore interagisce con il sito, le informazioni vengono raccolte e memorizzate nel suo profilo. Sono disponibili vari algoritmi per fornire il modello ottimale al sistema.

### Targeting automatico

[Auto-](/help/c-activities/auto-target/auto-target-to-optimize.md) Targetutilizza l&#39;apprendimento automatico avanzato per identificare più esperienze definite dagli esperti di marketing ad alte prestazioni. [!UICONTROL Il ] targeting automatico fornisce quindi l&#39;esperienza più personalizzata a ogni visitatore. La distribuzione è basata sui profili dei singoli clienti e sul comportamento dei visitatori precedenti con profili simili. [!UICONTROL Il ] targeting automatico consente di personalizzare i contenuti e stimolare le conversioni.

### Consigli

Mediante le attività [Consigli](/help/c-recommendations/recommendations.md#concept_7556C8A4543942F2A77B13A29339C0C0) vengono visualizzati automaticamente prodotti o contenuti che potrebbero interessare ai clienti sulla base delle loro precedenti attività. [!UICONTROL I consigli aiutano a indirizzare i clienti verso elementi rilevanti di cui potrebbero non essere a conoscenza.]

Un consiglio determina in che modo un prodotto viene suggerito a un cliente, in base alle sue attività sul sito. Ad esempio:

* Incoraggiare chi acquista uno zaino a considerare l’acquisto di scarpe e bastoncini da trekking.

   Creare un consiglio che mostra gli elementi acquistati spesso insieme, utilizzando i criteri “Chi ha acquistato questo ha acquistato anche”.

* Aumentare il tempo di permanenza dei visitatori sul sito multimediale consigliando contenuti video simili a quelli che stanno visualizzando al momento.

   Creare un consiglio che suggerisce altri video, utilizzando i criteri “Chi ha visualizzato questo ha visualizzato anche”.

* Suggerire ai clienti che hanno visualizzato informazioni su piani di risparmio di una banca di consultare anche le informazioni sui conti IRA.

   Mostrare altri elementi acquistati dai visitatori dopo aver visualizzato un prodotto, senza mostrare il primo prodotto nei consigli, utilizzando i criterio “Chi ha visualizzato questo ha acquistato anche”.

### Consigli come offerta

[Recommendations come ](/help/c-recommendations/recommendations-as-an-offer.md) offerta consente di includere raccomandazioni all&#39;interno delle attività Test A/B,  [!UICONTROL Auto-Allocate],  [!UICONTROL Auto-Target] e  [!UICONTROL Experience Targeting]  (XT).

Questo apre a funzionalità tutte nuove, ad esempio:

* Contenuto relativo e non relativo a consigli di test e targeting all’interno della stessa attività.
* Facile sperimentazione con il posizionamento di consigli sulla pagina, tra cui l’ordine di più consigli.
* Invio automatico di traffico all&#39;esperienza di consigli con le prestazioni migliori tramite [!UICONTROL Allocazione automatica].
* Assegnare dinamicamente i visitatori alle esperienze di raccomandazioni personalizzate in base ai singoli profili utilizzando [!UICONTROL Auto-Target].

### Autorizzazioni per gli utenti Enterprise

[La funzionalità ](/help/administrating-target/c-user-management/property-channel/property-channel.md#concept_E396B16FA2024ADBA27BC056138F9838) Autorizzazioni utente Enterprise consente di creare diversi progetti (denominati &quot;Profili di prodotto&quot; in  [!DNL Adobe Admin Console for Enterprise]). [!UICONTROL Le ] autorizzazioni utente Enterprise consentono di assegnare autorizzazioni diverse a un singolo utente che stabilisce i diritti di accesso dell&#39;utente per ciascun progetto. Questi progetti distinti possono essere paragonati al modo in cui le suite di rapporti funzionano in [!DNL Adobe Analytics]. In ogni progetto possono essere inclusi utenti specifici con ruoli specifici applicabili a un insieme di proprietà. Il risultato è che i clienti possono limitare la visualizzazione, la modifica, l’approvazione e l’accesso alla pubblicazione ai propri utenti. Puoi limitare gli utenti in base a regione, ambiente (dev/stage/prod), canale o altri criteri personalizzati.

## Recommendations Classic {#section_9554068100054D2DBDB298CBE5A0E413}

>[!IMPORTANT]
>
>[!DNL Recommendations Classic] è un prodotto legacy e non dispone più della licenza per i nuovi clienti. Per una migliore esperienza [!DNL Recommendations], eseguire l&#39;aggiornamento alle attività [!DNL Recommendations] disponibili in [!DNL Adobe Target Premium], come descritto in precedenza.

Con [!DNL Recommendations Classic] vengono visualizzati automaticamente prodotti o contenuti di potenziale interesse per i clienti sulla base della precedente attività dell&#39;utente sul sito web. Con la funzionalità Consigli è possibile indirizzare i clienti verso articoli di cui potrebbero ignorare l’esistenza, incrementando le vendite generate sul sito.

Per ulteriori informazioni, consulta la [documentazione di Recommendations Classic](/help/assets/adobe-recommendations-classic.pdf).

## Experience League: kit di benvenuto per Adobe Target {#kit}

Crea il tuo programma di ottimizzazione e personalizzazione su [!DNL Adobe Target] con questo kit di benvenuto. Il kit di benvenuto include informazioni chiave, strumenti e risorse utili per preparare e avviare la prima [!DNL Target] attività. Il kit include idee per ottenere risultati rapidi a breve termine e strategie di ottimizzazione a lungo termine.

[ Adobe Target Welcome Kit](https://expleague.azureedge.net/pdf/Adobe-Target-Welcome-Kit.pdf)

## Video di formazione: Tipi di attività (9:03) ![Logo Panoramica](/help/assets/overview.png)

Il seguente video illustra i tipi di attività disponibili in [!DNL Target Standard/Premium] e come il [!DNL Target] flusso di lavoro guidato in tre fasi può aiutarti a raggiungere gli obiettivi del tuo sito.

* Descrizione dei tipi di attività inclusi in [!DNL Adobe Target]
* Selezionare il tipo di attività appropriato per i tuoi obiettivi
* Descrizione del flusso di lavoro guidato in tre passaggi da applicare a tutti i tipi di attività

>[!VIDEO](https://video.tv.adobe.com/v/17386)
