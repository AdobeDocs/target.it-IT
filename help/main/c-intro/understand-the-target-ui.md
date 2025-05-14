---
keywords: interfaccia utente target;interfaccia utente;ui;annunci;eventi;notifiche
description: Acquisisci familiarità con l'interfaccia utente e trova collegamenti a informazioni più approfondite per trarre il massimo da  [!DNL Target].
title: Come si utilizza l’interfaccia di [!DNL Target] ?
feature: Overview
exl-id: ce4c72b2-b635-406b-9830-650816445a64
source-git-commit: 1ab7bb6aef5982f13191ff4f0573e87aac815938
workflow-type: tm+mt
source-wordcount: '1388'
ht-degree: 28%

---

# Interfaccia utente di [!DNL Target]

L’interfaccia utente è strutturata in un formato logico e intuitivo per trarre il massimo da [!DNL Adobe Target]. La seguente breve panoramica consente di acquisire familiarità con [!DNL Target] e fornisce collegamenti per ottenere informazioni più approfondite e istruzioni dettagliate.

## Intestazione interfaccia utente [!DNL Target]

L&#39;intestazione nella parte superiore dell&#39;interfaccia utente di [!DNL Target] contiene schede e opzioni che consentono di esplorare le diverse funzionalità della soluzione. È inoltre possibile cambiare organizzazioni e soluzioni [!DNL Adobe Experience Cloud], fornire feedback se si fa parte di un programma Beta, accedere all&#39;Assistente AI, ricevere assistenza e notifiche, gestire il profilo [!DNL Adobe] e uscire da [!DNL Target].

![Intestazione di Target](/help/main/c-intro/assets/target-header.png)

Le schede a sinistra consentono di accedere alle varie funzionalità di [!DNL Target], che verranno discusse in seguito. Cominciamo con le opzioni a destra prima di esaminare le schede.

### [!UICONTROL Organization]

Un&#39;*organizzazione* è l&#39;entità che consente all&#39;amministratore di configurare gruppi e utenti e di controllare il single sign-on in [!DNL Adobe Experience Cloud]. L’organizzazione funziona come un’azienda di accesso per tutti i prodotti e le soluzioni [!DNL Experience Cloud]. Nella maggior parte dei casi, un&#39;organizzazione è il nome dell&#39;azienda. Tuttavia, un&#39;azienda può avere molte organizzazioni.

Selezionare l&#39;organizzazione desiderata nell&#39;elenco a discesa [!UICONTROL Organization] se la società dispone di più organizzazioni:

![Elenco a discesa Organizzazione](/help/main/c-intro/assets/organizations.png)

### [!UICONTROL Beta Feedback]

(Condizionale) Se fai parte di un programma Beta ufficiale di [!DNL Target], potresti visualizzare l&#39;icona [!UICONTROL Beta Feedback].

![Icona feedback Beta](/help/main/c-intro/assets/beta-feedback.png)

Fornisci una descrizione per il tuo feedback, includi i file o le schermate applicabili ed eventuali dettagli aggiuntivi, a seconda delle necessità, quindi fai clic su **[!UICONTROL Submit]**.

### [!DNL AI Assistant] (in attesa del rilascio il 20 maggio 2025)

(Condizionale) Se l’organizzazione ti ha concesso i diritti per utilizzare l’Assistente IA, fai clic sull’icona Assistente IA.

### Aiuto

L’icona Aiuto consente di accedere a informazioni, video, blog e altro ancora per utilizzare [!DNL Target] in modo più efficace. Puoi creare un ticket di supporto, trovare i numeri di telefono del supporto, porre domande tramite Twitter o fornire feedback su [!DNL Target] per farci sapere come sta andando il team di [!DNL Target].

![Aiuto](/help/main/c-intro/assets/help.png)

### Notifiche e annunci {#notifications-announcements}

I pannelli [!UICONTROL Notifications] e [!UICONTROL Announcements] consentono di essere sempre aggiornati su tutti gli elementi [!DNL Adobe Target]. Le notifiche proattive ti consentono di essere sempre al corrente dello stato di [!DNL Adobe Experience Cloud] soluzioni e [!DNL Target] eventi. Le notifiche proattive ti avvisano in caso di interruzioni del servizio o interventi di manutenzione.

Fai clic sull’icona a forma di campana nell’intestazione per visualizzare le notifiche:

![Icona Bell per notifiche e annunci](assets/bell-icon.png)

Il pannello contiene schede per [!UICONTROL Notifications] e [!UICONTROL Announcements].

![Notifiche](assets/notifications.png)

Le sezioni seguenti contengono informazioni su ciascuna scheda e su come configurare notifiche e annunci:

#### Notifiche {#notifications}

Le notifiche di [!DNL Target] eventi includono:

* **Attività**: notifiche per tutti i tipi di attività quando un&#39;attività viene approvata o disattivata, manualmente o alla sua data di inizio o di fine. La notifica include il nome dell’attività e un collegamento alla pagina di panoramica dell’attività.

  Le notifiche sono configurabili e vengono ricevute, per impostazione predefinita, dagli amministratori di prodotto, dagli editori e dagli approvatori nell&#39;area di lavoro dell&#39;attività per gli account [!DNL Target Premium]. Per gli account [!DNL Target Standard], le notifiche vengono ricevute da tutti gli editori e gli approvatori.

  Le notifiche sono formattate come i seguenti esempi:

   * `Activity {target.activity.name} has been activated`

   * `Activity {target.activity.name} has been deactivated`

* **Script di profilo**: notifiche quando uno script di profilo viene attivato o disattivato, manualmente o da [!DNL Target].

  Le notifiche sono configurabili e vengono ricevute, per impostazione predefinita, dagli amministratori di prodotto e dagli approvatori per gli account [!DNL Target Premium] e [!DNL Target Standard].

  Le notifiche sono formattate come i seguenti esempi:

   * `Profile Script {target.profileScript.name} has been activated`
   * `Profile Script {target.profileScript.name} has been deactivated`

* **Feed consigli**: notifiche quando un feed [!DNL Recommendations] viene attivato o disattivato, manualmente o da [!DNL Target]. Le notifiche vengono inviate anche quando un feed [!DNL Recommendations] non riesce.

  Le notifiche sono configurabili e vengono ricevute, per impostazione predefinita, dagli amministratori di prodotto e dagli approvatori per gli account [!DNL Target Premium]. [!DNL Recommendations] è una funzionalità [!DNL Target Premium] e non è disponibile in [!DNL Target Standard].

  Le notifiche sono formattate come i seguenti esempi:

   * `Feed  {target.feed.name} has been activated`
   * `Feed {target.feed.name} has been deactivated`
   * `Feed {target.feed.name} has failed`
   * `Feed {target.feed.name} has failed to import from source`

Per contrassegnare le singole notifiche come lette, passa il puntatore del mouse sulla notifica desiderata e fai clic sul segno di spunta. È possibile contrassegnare tutte le notifiche come lette o visualizzare tutte le notifiche facendo clic su [!UICONTROL "Mark as Read"] o [!UICONTROL "View All"] nella parte inferiore del pannello.

È inoltre possibile impostare un promemoria per ricevere nuovamente una notifica passando il mouse su una notifica, facendo clic sull&#39;icona &quot;[!UICONTROL Remind me]&quot; e selezionando la data in cui si desidera ricevere la notifica: 5 minuti, 15 minuti, un&#39;ora o domani.

#### Annunci

Le notifiche proattive ti avvisano in caso di interruzioni del servizio o interventi di manutenzione.

Ulteriori informazioni sono disponibili nella pagina [Stato Adobe](https://status.adobe.com/it).

### Configurare notifiche e annunci

Per modificare le preferenze per le notifiche:

1. Fare clic sull&#39;icona, quindi fare clic su **[!UICONTROL Notifications]**.
1. In **[!UICONTROL Target]**, fare clic su **[!UICONTROL Customize]**.
1. Seleziona o deseleziona le categorie per le quali desideri ricevere le notifiche:

   * Richieste: quando qualcuno ti invia una richiesta per approvare un oggetto o concederne l’accesso. Non puoi annullare l’abbonamento a questa categoria.
   * Assegnato a me: quando qualcuno ti assegna un oggetto.
   * Riferimenti: quando qualcuno ti menziona in un commento.
   * Nuove versioni: quando è disponibile una nuova versione di un prodotto o di un servizio a cui hai accesso.
   * Condiviso con me: quando qualcuno condivide un oggetto con te.
   * Aggiornamenti sul contenuto: quando qualcuno modifica, elimina o aggiunge commenti a un oggetto che hai creato o che segui.
   * Altro:

   >[!NOTE]
   >
   >&quot;Nuove versioni&quot; e &quot;Aggiornamenti sul contenuto&quot; sono le uniche categorie di notifica applicabili a [!DNL Target]. Le altre categorie si applicano ad altre soluzioni Adobe.

1. Seleziona le categorie che desideri siano considerate ad alta priorità.
1. Seleziona le notifiche per le quali desideri visualizzare gli avvisi nel browser.

   Questi avvisi vengono visualizzati nell’angolo in alto a destra del browser per alcuni secondi. Puoi scegliere di visualizzare le categorie ad alta priorità, tutte le categorie o nascondere tutti i popup di notifica. Puoi anche configurare se desideri che le notifiche rimangano visibili fino a quando non le ignori oppure puoi configurare la durata della notifica.

1. Seleziona la frequenza con cui desideri ricevere le e-mail di notifica:

   * Non inviare e-mail
   * Notifiche immediate
   * Riepilogo giornaliero
   * Riepilogo settimanale

### Commutatore app

Il selettore App consente di accedere rapidamente alle soluzioni [!DNL Adobe Experience Cloud] disponibili.

![Selettore App](/help/main/c-intro/assets/apps.png)

### Profilo

Fai clic sull’avatar del tuo profilo per modificare le preferenze di [!DNL Adobe Experience Cloud] o per uscire da [!DNL Target]. Puoi anche accedere al tuo profilo [!DNL Adobe] o modificarlo.

![Avatar del profilo](/help/main/c-intro/assets/change-language.png)

Ora parliamo delle schede che si trovano lungo il lato sinistro dell’intestazione di [!DNL Target].

## Attività

L&#39;elenco **[!UICONTROL Activities]** è la visualizzazione predefinita all&#39;apertura di [!DNL Target]. Puoi creare attività da questa pagina e gestire quelle esistenti.

![Attività, elenco](/help/main/c-intro/assets/activities-list.png)

Per informazioni approfondite sui tipi di attività disponibili in [!DNL Target] e per ulteriori informazioni sull&#39;interfaccia utente dell&#39;elenco [!UICONTROL Activity], vedere [Attività](/help/main/c-activities/activities.md).

## Tipi di pubblico

Fai clic sulla scheda **[!UICONTROL Audiences]** per visualizzare l&#39;elenco [!UICONTROL Audiences] in cui puoi creare tipi di pubblico e gestire quelli esistenti.

![Elenco dei tipi di pubblico](/help/main/c-intro/assets/audience-list.png)

Un pubblico è un gruppo di partecipanti a un’attività simili che visualizzano un’attività con targeting. Un pubblico è un gruppo di persone con le stesse caratteristiche, ad esempio nuovi visitatori, visitatori di ritorno o visitatori provenienti da una specifica area geografica. La funzione [!UICONTROL Audience] consente di indirizzare contenuti ed esperienze diversi a tipi di pubblico specifici per ottimizzare le attività di marketing digitale, presentando al momento giusto i messaggi più appropriati ai vari visitatori. Se un visitatore viene identificato come parte di un pubblico, [!DNL Target] determina quale esperienza mostrare, in base ai criteri stabiliti durante la creazione dell’attività.

Consulta [Crea tipi di pubblico](/help/main/c-target/c-audiences/create-audience.md) per informazioni approfondite sui tipi di pubblico in [!DNL Target] e per ulteriori informazioni sull&#39;interfaccia utente dell&#39;elenco [!UICONTROL Audience].

## Offerte

Fai clic sulla scheda **[!UICONTROL Offers]** per visualizzare l&#39;elenco [!UICONTROL Offers] in cui puoi creare esperienze e offerte e gestire quelle esistenti.

![Elenco Offerte](/help/main/c-intro/assets/offers.png)

Un’esperienza può essere un’offerta, un’immagine, un testo, un pulsante, un video, una combinazione di questi vari elementi su una pagina, un’intera pagina web o un set di pagine, ad esempio un percorso di acquisto o altra sequenza logica di pagine. Può essere anche la risposta di un assistente vocale o di uno script di servizio clienti, o addirittura un gusto personalizzato da un distributore di bevande. Puoi testare o personalizzare le esperienze nelle attività di [!DNL Target].

Per informazioni approfondite sui tipi di offerta in [!DNL Target] e per ulteriori informazioni sull&#39;interfaccia utente dell&#39;elenco [!UICONTROL Offer], vedere [Offerte](/help/main/c-experiences/c-manage-content/manage-content.md).

## Recommendations

Fare clic sulla scheda **[!UICONTROL Recommendations]** per accedere a [!DNL Target Recommendations].

>[!NOTE]
>
>Le attività Consigli sono disponibili come parte della soluzione [!DNL Target Premium]. Non sono disponibili in [!DNL Target Standard] senza una licenza [!DNL Target Premium]. Per ulteriori informazioni, consulta [Target Premium](/help/main/c-intro/intro.md#premium) in *Introduzione a Target*.

![Recommendations](/help/main/c-intro/assets/recommendations.png)

Le attività di [!UICONTROL Recommendations] visualizzano automaticamente prodotti o contenuti che potrebbero interessare i clienti in base alle loro attività precedenti o ad altri algoritmi. Le raccomandazioni aiutano a indirizzare i clienti verso elementi rilevanti di cui potrebbero non essere a conoscenza.

Consulta [Recommendations](/help/main/c-recommendations/recommendations.md) per informazioni approfondite su [!UICONTROL Recommendations] in [!DNL Target] e per ulteriori informazioni sull&#39;interfaccia utente di [!UICONTROL Recommendations].

## Amministrazione

Fare clic sulla scheda **[!UICONTROL Administration]** per accedere alle pagine [!UICONTROL Administration].

![Pagine amministrazione](/help/main/c-intro/assets/administration.png)

Le pagine [!UICONTROL Administration] consentono di amministrare [!DNL Target], incluse le impostazioni di configurazione per [!UICONTROL Visual Experience Composer] (VEC), il reporting, la configurazione di [!DNL Scene7], l&#39;implementazione, gli host, gli ambienti, i token di risposta e gli utenti.

Per ulteriori informazioni dettagliate sull’interfaccia utente, consulta [Panoramica sull’amministrazione di Target](/help/main/administrating-target/administrating-target.md).
