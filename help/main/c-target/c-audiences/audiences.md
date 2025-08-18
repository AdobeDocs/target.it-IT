---
keywords: pubblico;regole del pubblico;creare un pubblico;creazione di pubblico;pubblico di destinazione;rapporti sul pubblico;report sul pubblico;segmento;parametri di profilo personalizzati;definizione del pubblico;elenco di tipi di pubblico;audience
description: Scopri come utilizzare i tipi di pubblico in [!DNL Adobe Target].
title: Come si utilizza l’elenco del pubblico?
feature: Audiences
exl-id: 7af7f101-f550-4fdc-bcd9-90e4107b0415
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 22%

---

# Creazione di un pubblico

I tipi di pubblico in [!DNL Adobe Target] determinano chi visualizzerà il contenuto e le esperienze in un&#39;attività di destinazione.

I tipi di pubblico sono utilizzati in tutte le situazioni in cui è disponibile il targeting. Quando esegui il targeting di un’attività, disponi delle seguenti opzioni:

* Selezionare un pubblico riutilizzabile dall&#39;elenco [!UICONTROL Audiences]
* [Crea un pubblico specifico per l&#39;attività](/help/main/c-target/creating-activity-only-audience.md) e impostalo come destinazione
* [Combina più tipi di pubblico](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) per creare un pubblico ad hoc

È inoltre possibile utilizzare i dati del pubblico raccolti da [!DNL Adobe Analytics] per il targeting e la personalizzazione in tempo reale in [!DNL Target] e in altre applicazioni [!DNL Adobe Experience Cloud]. Consulta [Tipi di pubblico di Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html?lang=it) nella *Guida ai componenti dell&#39;interfaccia centrale di Experience Cloud*.

Esistono due tipi di pubblico in [!DNL Target]:

* **Tipi di pubblico di destinazione:** utilizzato per fornire contenuti diversi a diversi tipi di visitatori.
* **Tipi di pubblico per reportistica:** per determinare in che modo diversi tipi di visitatori rispondono allo stesso contenuto e analizzare i risultati dei test.

  In [!DNL Target], è possibile configurare i tipi di pubblico per reportistica solo se [!DNL Target] è utilizzato come origine per la generazione di rapporti. Se utilizzi [Adobe Analytics come origine per la generazione di rapporti](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T), devi configurare i tipi di pubblico per la generazione di rapporti in [!DNL Analytics].

## Utilizza l&#39;elenco [!UICONTROL Audiences] {#use-list}

Per accedere all&#39;elenco [!UICONTROL Audiences], fare clic su **[!UICONTROL Audiences]** nella barra dei menu superiore:

![[!UICONTROL Audiences] elenco](assets/audiences_list.png)

L&#39;elenco [!UICONTROL Audiences] contiene i tipi di pubblico che è possibile utilizzare nelle attività. Utilizza l&#39;elenco [!UICONTROL Audiences] per creare, modificare, duplicare, copiare o combinare i tipi di pubblico. L’elenco mostra anche l’origine in cui è stato creato il pubblico:

* [!DNL Adobe Target]
* [!DNL Adobe Target Classic]
* [!DNL Experience Cloud]
* [!DNL Adobe Experience Platform]

  >[!NOTE]
  >
  >L&#39;origine [!DNL Adobe Experience Platform] è disponibile per tutti i clienti [!DNL Target] che utilizzano [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=it){target=_blank}. I tipi di pubblico disponibili da [!DNL Adobe Experience Platform] possono essere utilizzati così come sono o [combinati con tipi di pubblico esistenti](/help/main/c-target/combining-multiple-audiences.md).
  >
  >Gli utenti devono avere lo stato [!UICONTROL Approver] o superiore in [!DNL Target] per configurare le schede [!DNL Target] [!UICONTROL Destinations] in AEP/RTCDP ([!DNL Real-time Customer Data Platform]).
  >
  >Per ulteriori informazioni, vedere [Utilizzare i tipi di pubblico di Adobe Experience Platform](#aep).

Impossibile rinominare i tipi di pubblico predefiniti, ad esempio &quot;[!UICONTROL New Visitors]&quot; e &quot;[!UICONTROL Returning Visitors]&quot;.

Quando si lavora con tipi di pubblico creati originariamente in [!DNL Experience Cloud] o [!DNL Adobe Experience Platform], [!DNL Target] ti avvisa se si fa riferimento a un pubblico in [!DNL Target] attività che sono state successivamente eliminate in [!DNL Experience Cloud] o [!DNL Adobe Experience Platform].

* Se un pubblico è stato eliminato in [!DNL Experience Cloud] o [!DNL Adobe Experience Platform], viene visualizzata un&#39;icona di avviso sia nell&#39;elenco [!UICONTROL Audience] che nel selettore del pubblico. Una descrizione comandi nell&#39;interfaccia utente di [!DNL Target] indica inoltre che il pubblico è stato eliminato in [!DNL Experience Cloud] o [!DNL Adobe Experience Platform].
* Se si tenta di combinare più tipi di pubblico con un pubblico eliminato o se si tenta di salvare un&#39;attività che fa riferimento a un pubblico eliminato, viene visualizzato un messaggio di avviso.

Puoi inoltre eseguire il targeting di parametri di profilo personalizzati e parametri `user.`. Durante la creazione di un pubblico, trascina gli attributi che desideri utilizzare per eseguire il targeting dell’attività nella finestra di audience builder. Se l&#39;attributo desiderato non viene visualizzato, significa che non è stato attivato da una mbox. Altri parametri mbox personalizzati sono disponibili nell&#39;elenco a discesa [!UICONTROL Custom Parameters].

Utilizzare il pulsante [!UICONTROL Filters] per filtrare l&#39;elenco [!UICONTROL Audiences] per origine: [!DNL Adobe Target], [!DNL Adobe Target Classic], [!DNL Experience Cloud] e [!DNL Adobe Experience Platform].

Opzione ![Filtri nell&#39;elenco [!UICONTROL Audiences]](assets/filters.png)

Utilizzare la casella [!UICONTROL Search audiences] per eseguire ricerche nell&#39;elenco [!UICONTROL Audiences]. Puoi cercare qualsiasi parte del nome di un pubblico, oppure racchiudere tra virgolette una stringa specifica.

È possibile ordinare l&#39;elenco [!UICONTROL Audiences] in base al nome del pubblico o alla data dell&#39;ultima modifica. Per ordinare in base al nome o alla data, fai clic sull’intestazione di colonna, quindi seleziona la visualizzazione dei tipi di pubblico in ordine crescente o decrescente.

## Visualizzare le definizioni del pubblico {#section_11B9C4A777E14D36BA1E925021945780}

Puoi visualizzare i dettagli della definizione del pubblico in una scheda a comparsa in varie posizioni nell&#39;interfaccia utente di [!DNL Target] senza aprire il pubblico. Questa funzionalità si applica ai tipi di pubblico creati in [!DNL Target Standard/Premium] e ai tipi di pubblico importati da [!DNL Target Classic] o creati tramite API.

Ad esempio, per accedere alla scheda di definizione del pubblico seguente fai clic sull&#39;icona [!UICONTROL View Details] per il pubblico desiderato:

![Attività > Definizione pubblico](assets/audience_definition_list.png)

È possibile accedere alla scheda di definizione del pubblico seguente facendo clic sull&#39;icona [!UICONTROL View Details] nella pagina [!UICONTROL Overview] di un&#39;attività:

![Attività > Definizione pubblico](assets/view-details-activity-overview.png)

La scheda di definizione del pubblico mostra il tipo, l’origine e gli attributi del pubblico. Fai clic su **[!UICONTROL View full details]** per visualizzare altre attività che fanno riferimento a tale pubblico, se applicabile. Se visualizzi una scheda di definizione del pubblico dalla pagina [!UICONTROL Overview] di un&#39;attività, fai clic su **[!UICONTROL Audience Usage]**.

Le informazioni sull’utilizzo del pubblico possono aiutarti a evitare un impatto accidentale su altre attività mentre modifichi i tipi di pubblico. Le informazioni includono [!UICONTROL Live Activities], [!UICONTROL Inactive Activities], [!UICONTROL Archived Activities] e [!UICONTROL Syncing Activities]. Questa funzione è disponibile per tutti i tipi di pubblico (pubblico della libreria e [pubblico per sola attività](/help/main/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483)).

Se un pubblico è [combinato con un altro pubblico](/help/main/c-target/combining-multiple-audiences.md) e il pubblico combinato viene utilizzato per creare un&#39;attività, le informazioni di utilizzo per entrambi i tipi di pubblico elencano l&#39;attività appena creata.

![immagine audience_definition_list_usage](assets/audience_definition_list_usage.png)

<!--The following audience definition card is for an audience imported from the Adobe Experience Cloud. In this instance, the audience was imported from Adobe Audience Manager (AAM).

![Usage tab on Audience Definition card](assets/audience_definition_mc.png)

The following details are available for these imported audience types:

| Audience Type | Details |
|--- |--- |
|Mobile audience|Marketing Name, Vendor, and Model.<br>The `matches | does not match` operator displays instead of `equals | does not equal`<br>![Imported Mobile Audience](/help/main/c-target/c-audiences/assets/imported_mobile_audience.png).|
|Visitor-behavior audience|**user.categoryAffinity:** `categoryAffinity` with `FAVORITE` parameter.<br>![Imported Category Affinity](/help/main/c-target/c-audiences/assets/imported_category_affinity.png)<br>**Monitoring:** Monitoring service equals true.<br>**No Monitoring Service:** Monitoring service equals false.<br>![Imported Monitoring](/help/main/c-target/c-audiences/assets/imported_monitoring.png)|
|Audiences using the NOT operator|**Single Rule:** Target displays the audience in the format `[All Visitor AND [NOT [rule]`. Single NOT rule displays with AND with `AllVisitor` audience.<br>![Imported Not Audience](/help/main/c-target/c-audiences/assets/imported_not_audience.png)|

Keep the following points in mind as you work with imported audiences:

* Expression target audiences are no longer supported in Target Standard/Premium. 
* Target Standard/Premium does not support some deprecated audiences or has improved operators for ease of use. Because of this, the definition of an imported audience, although working as per definition, does not mean that same is now available for creation in the Standard/Premium interface. For example, Social Audiences are visible with their rules but Target Standard/Premium does not allow social audiences to be created.-->

## Utilizzo dei tipi di pubblico da [!DNL Adobe Experience Platform] {#aep}

L&#39;utilizzo dei tipi di pubblico creati in [!DNL Adobe Experience Platform] fornisce dati più completi sui clienti per una personalizzazione di maggiore impatto.

Per ulteriori informazioni, vedere [Utilizzare i tipi di pubblico di [!DNL Adobe Experience Platform]](/help/main/c-integrating-target-with-mac/integrating-with-rtcdp.md#aep).

## Video di formazione: Utilizzo dei tipi di pubblico ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video include informazioni sull&#39;utilizzo dei tipi di pubblico.

* Spiegazione del termine “pubblico”
* Spiegazione dei due modi in cui il pubblico viene utilizzato per lʼottimizzazione
* Trovare un pubblico nellʼelenco Tipi di pubblico
* Indirizzare unʼattività a un pubblico
* Utilizzare i tipi di pubblico per la reportistica passiva in un’attività

>[!VIDEO](https://video.tv.adobe.com/v/17398)
