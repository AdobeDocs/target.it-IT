---
keywords: interfaccia utente target;interfaccia utente;ui;annunci;eventi;notifiche
description: Acquisisci familiarità con l’interfaccia utente e trova collegamenti a informazioni più approfondite per trarre il massimo da [!DNL Target].
title: Come si utilizza l’interfaccia di [!DNL Target] ?
feature: Overview
exl-id: ce4c72b2-b635-406b-9830-650816445a64
source-git-commit: be0f2289afd0c808b3ab4cb390bd28bedd8a315d
workflow-type: tm+mt
source-wordcount: '1345'
ht-degree: 46%

---

# Interfaccia utente di [!DNL Target]

L’interfaccia utente è strutturata in un formato logico e intuitivo per trarre il massimo da [!DNL Adobe Target]. La seguente breve panoramica consente di acquisire familiarità con [!DNL Target] e fornisce collegamenti per informazioni più approfondite e istruzioni dettagliate.

Intestazione nella parte superiore della [!DNL Target] L&#39;interfaccia utente contiene schede e opzioni che consentono di navigare tra le diverse funzionalità della soluzione. È inoltre possibile cambiare organizzazione e [!DNL Adobe Experience Cloud] soluzioni, ottenere aiuto e notifiche, gestire [!DNL Adobe] e disconnetti da [!DNL Target].

![Intestazione di Target](/help/main/c-intro/assets/target-header.png)

Le schede lungo il lato sinistro consentono di accedere alle varie funzionalità di [!DNL Target], di cui si discute più avanti. Cominciamo con le opzioni disponibili a destra, prima di passare alle schede.

## Organizzazioni

Un&#39;*organizzazione* è l&#39;entità che consente all&#39;amministratore di configurare gruppi e utenti e di controllare il single sign-on in [!DNL Adobe Experience Cloud]. L’organizzazione funziona come un’azienda di accesso per tutti i prodotti e le soluzioni [!DNL Experience Cloud]. Nella maggior parte dei casi, un&#39;organizzazione è il nome dell&#39;azienda. Tuttavia, un&#39;azienda può avere molte organizzazioni.

Se la tua azienda dispone di più organizzazioni, seleziona quella desiderata dall’elenco a discesa [!UICONTROL Organizzazione]:

![Elenco a discesa Organizzazione](/help/main/c-intro/assets/organizations.png)

## App

Il selettore App consente di accedere rapidamente alle soluzioni [!DNL Adobe Experience Cloud] disponibili.

![Selettore App](/help/main/c-intro/assets/apps.png)

## Aiuto

L’icona Aiuto consente di accedere a informazioni, video, blog e altro ancora per utilizzare [!DNL Target] in modo più efficace. Puoi creare un ticket di supporto, trovare i numeri di telefono dell&#39;assistenza, porre domande tramite Twitter o fornire un feedback su [!DNL Target] per farci sapere come [!DNL Target] la squadra sta facendo.

![Aiuto](/help/main/c-intro/assets/help.png)

## Notifiche e annunci {#notifications-announcements}

I pannelli [!UICONTROL Notifiche] e [!UICONTROL Annunci] consentono di essere sempre aggiornati su tutto ciò che riguarda [!DNL Adobe Target]. Le notifiche proattive ti permettono di essere sempre al corrente dello stato di [!DNL Adobe Experience Cloud] soluzioni e [!DNL Target] eventi. Le notifiche proattive ti avvisano in caso di interruzioni del servizio o interventi di manutenzione.

Fai clic sull&#39;icona della campana dall&#39;intestazione per visualizzare le notifiche:

![Icona Bell per le notifiche e gli annunci](assets/bell-icon.png)

Il pannello contiene le schede per [!UICONTROL Notifiche] e [!UICONTROL Annunci].

![Notifiche](assets/notifications.png)

Le sezioni seguenti contengono informazioni su ciascuna scheda e su come configurare notifiche e annunci:

### Notifiche

[!DNL Target] le notifiche degli eventi includono quanto segue:

* **Attività**: Notifiche per tutti i tipi di attività quando un&#39;attività viene approvata o disattivata, manualmente o quando raggiunge la data di inizio o di fine. La notifica include il nome dell’attività con un collegamento alla pagina di panoramica dell’attività.

   Le notifiche sono configurabili e vengono ricevute, per impostazione predefinita, da amministratori di prodotto, editori e approvatori nell’area di lavoro dell’attività per [!DNL Target Premium] conti. Per [!DNL Target Standard] account, notifiche vengono ricevute da tutti gli editori e approvatori.

   Le notifiche sono formattate come i seguenti esempi:

   * `Activity {target.activity.name} has been activated`

   * `Activity {target.activity.name} has been deactivated`

* **Script di profilo**: Notifiche quando uno script di profilo viene attivato o disattivato, manualmente o da [!DNL Target].

   Le notifiche sono configurabili e vengono ricevute, per impostazione predefinita, da amministratori di prodotto e approvatori per entrambi [!DNL Target Premium] e [!DNL Target Standard] conti.

   Le notifiche sono formattate come i seguenti esempi:

   * `Profile Script {target.profileScript.name} has been activated`
   * `Profile Script {target.profileScript.name} has been deactivated`

* **Feed Recommendations**: Notifiche quando un [!DNL Recommendations] il feed è attivato o disattivato, manualmente o tramite [!DNL Target]. Le notifiche vengono inviate anche quando un [!DNL Recommendations] il feed non riesce.

   Le notifiche sono configurabili e vengono ricevute, per impostazione predefinita, da amministratori di prodotto e approvatori per [!DNL Target Premium] conti. [!DNL Recommendations] è un [!DNL Target Premium] e non è disponibile in [!DNL Target Standard].

   Le notifiche sono formattate come i seguenti esempi:

   * `Feed  {target.feed.name} has been activated`
   * `Feed {target.feed.name} has been deactivated`
   * `Feed {target.feed.name} has failed to import from source`

Puoi contrassegnare le singole notifiche come lette passando il mouse sulla notifica desiderata e facendo clic sul segno di spunta. Puoi contrassegnare tutte le notifiche come di lettura o visualizzare tutte le notifiche facendo clic su [!UICONTROL &quot;Segna come letto&quot;] o [!UICONTROL &quot;Visualizza tutto&quot;] nella parte inferiore del pannello.

Puoi anche impostare un promemoria per ricevere nuovamente una notifica passando il mouse su una notifica e facendo clic su &quot;[!UICONTROL Ricordami]&quot;, quindi seleziona quando desideri ricevere una notifica: 5 minuti, 15 minuti, un&#39;ora o domani.

### Annunci

Le notifiche proattive ti avvisano in caso di interruzioni del servizio o interventi di manutenzione.

Ulteriori informazioni sono disponibili nella pagina [Stato dei sistemi Adobe.](https://status.adobe.com/)

### Configurare notifiche e annunci

Per modificare le preferenze per le notifiche:

1. Fai clic sull’icona a forma di ingranaggio, quindi fai clic su **[!UICONTROL Notifiche]**.
1. Sotto **[!UICONTROL Target]**, fai clic su **[!UICONTROL Personalizza]**.
1. Seleziona o deseleziona le categorie per le quali desideri ricevere le notifiche:

   * Richieste: Quando un utente invia una richiesta per approvare un oggetto o concedere l&#39;accesso a un oggetto. Non puoi annullare l’iscrizione a questa categoria.
   * Assegnato a me: Quando un utente assegna un oggetto all&#39;utente.
   * Riferimenti: Quando qualcuno ti parla in un commento.
   * Nuove versioni: Quando è disponibile una nuova versione per un prodotto o un servizio a cui hai accesso.
   * Condiviso con me: Quando qualcuno condivide con te un oggetto.
   * Aggiornamenti sul contenuto: Quando un utente modifica, elimina o commenta un oggetto creato o seguito.
   * Altri:

   >[!NOTE]
   >
   >Le uniche categorie di notifica applicabili a &quot;Nuove versioni&quot; e &quot;Aggiornamenti sul contenuto&quot; [!DNL Target]. Le altre categorie si applicano ad altre soluzioni di Adobe.


1. Seleziona le categorie a cui vuoi assegnare la priorità alta.
1. Seleziona le notifiche per le quali desideri visualizzare gli avvisi nel browser.

   Questi avvisi vengono visualizzati nell’angolo in alto a destra del browser per alcuni secondi. Puoi scegliere di visualizzare le categorie ad alta priorità, tutte le categorie o di nascondere tutti i pop-up di notifiche. Puoi anche configurare se vuoi che le notifiche rimangano visibili finché non le ignora o se puoi configurare la durata della notifica.

1. Seleziona la frequenza con cui desideri ricevere le e-mail di notifica:

   * Non inviare e-mail
   * Notifiche istantanee
   * Riepilogo giornaliero
   * Digest settimanale

## Profilo

Fai clic sull’avatar del tuo profilo per modificare le preferenze di [!DNL Adobe Experience Cloud] o per uscire da [!DNL Target]. Puoi anche accedere al tuo profilo [!DNL Adobe] o modificarlo.

![Avatar del profilo](/help/main/c-intro/assets/change-language.png)

Ora parliamo delle schede che si trovano lungo il lato sinistro dell’intestazione di [!DNL Target].

## Attività

L’elenco **[!UICONTROL Attività]** è la vista predefinita all’apertura di [!DNL Target]. Puoi creare attività da questa pagina e gestire le attività esistenti.

![Attività, elenco](/help/main/c-intro/assets/activities-list.png)

Consulta [Attività](/help/main/c-activities/activities.md) per informazioni approfondite sui tipi di attività disponibili in [!DNL Target] e per ulteriori informazioni sull’interfaccia utente dell’elenco [!UICONTROL Attività].

## Tipi di pubblico

Fai clic sul pulsante **[!UICONTROL Tipi di pubblico]** per visualizzare la scheda [!UICONTROL Tipi di pubblico] in cui puoi creare tipi di pubblico e gestire quelli esistenti.

![Elenco dei tipi di pubblico](/help/main/c-intro/assets/audience-list.png)

Un pubblico è un gruppo di partecipanti a un’attività simile che visualizzano un’attività con targeting. Un pubblico è un gruppo di persone con le stesse caratteristiche, ad esempio nuovi visitatori, visitatori di ritorno o visitatori provenienti da una specifica area geografica. La funzione [!UICONTROL Pubblico] consente di indirizzare contenuti ed esperienze diversi a tipi di pubblico specifici per ottimizzare le attività di marketing digitale, presentando al momento giusto i messaggi più appropriati ai vari visitatori. Se un visitatore viene identificato come parte di un pubblico, [!DNL Target] determina quale esperienza mostrare, in base ai criteri stabiliti durante la creazione dell’attività.

Consulta [Creare tipi di pubblico](/help/main/c-target/c-audiences/create-audience.md) per informazioni approfondite sui tipi di pubblico in [!DNL Target] e per ulteriori informazioni sull’interfaccia utente dell’elenco [!UICONTROL Tipi di pubblico].

## Offerte

Fai clic sul pulsante **[!UICONTROL Offerte]** per visualizzare la scheda [!UICONTROL Offerte] in cui puoi creare esperienze e offerte e gestire esperienze e offerte esistenti.

![Elenco Offerte](/help/main/c-intro/assets/offers.png)

Un’esperienza può essere un’offerta, un’immagine, un testo, un pulsante, un video, una combinazione di questi vari elementi su una pagina, un’intera pagina web o un set di pagine, ad esempio un percorso di acquisto o altra sequenza logica di pagine. Può essere anche la risposta di un assistente vocale o di uno script di servizio clienti, o addirittura un gusto personalizzato da un distributore di bevande. Puoi testare o personalizzare le esperienze nelle attività di [!DNL Target].

Consulta [Offerte](/help/main/c-experiences/c-manage-content/manage-content.md) per informazioni approfondite sui tipi di offerta disponibili in [!DNL Target] e per ulteriori informazioni sull’interfaccia utente dell’elenco [!UICONTROL Offerte].

## Recommendations

Fai clic sulla scheda **[!UICONTROL Recommendations]** (Consigli) per accedere a [!DNL Target Recommendations].

>[!NOTE]
>
>Le attività Consigli sono disponibili come parte della soluzione [!DNL Target Premium]. Non sono disponibili in [!DNL Target Standard] senza una licenza [!DNL Target Premium]. Per ulteriori informazioni, consulta [Target Premium](/help/main/c-intro/intro.md#premium) in *Introduzione a Target*.

![Recommendations](/help/main/c-intro/assets/recommendations.png)

Le attività di generazione dei [!UICONTROL consigli] visualizzano automaticamente prodotti o contenuti che potrebbero interessare i clienti in base alle loro attività precedenti o ad altri algoritmi. Recommendations aiuta a indirizzare i clienti verso articoli rilevanti di cui potrebbero ignorare l’esistenza.

Consulta [Recommendations](/help/main/c-recommendations/recommendations.md) (Consigli) per informazioni dettagliate su [!UICONTROL Recommendations] in [!DNL Target] e per ulteriori informazioni sull’interfaccia utente di [!UICONTROL Recommendations].

## Amministrazione

Fai clic sulla scheda **[!UICONTROL Amministrazione]** per accedere alle pagine [!UICONTROL Amministrazione].

![Pagine amministrazione](/help/main/c-intro/assets/administration.png)

Le pagine [!UICONTROL Amministrazione] consentono di amministrare [!DNL Target], incluse le impostazioni di configurazione per il [!UICONTROL Compositore esperienza visivo], la generazione di rapporti, la configurazione di [!DNL Scene7], l’implementazione, gli host, gli ambienti, i token di risposta e gli utenti.

Per ulteriori informazioni dettagliate sull’interfaccia utente, consulta [Panoramica sull’amministrazione di Target](/help/main/administrating-target/administrating-target.md).
