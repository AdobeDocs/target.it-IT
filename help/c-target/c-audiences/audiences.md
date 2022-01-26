---
keywords: pubblico;regole del pubblico;creare un pubblico;creazione di pubblico;pubblico di destinazione;rapporti sul pubblico;report sul pubblico;segmento;parametri di profilo personalizzati;definizione del pubblico;elenco di tipi di pubblico;audience
description: Scopri come utilizzare i tipi di pubblico in [!DNL Adobe Target].
title: Come si utilizza l'elenco dei tipi di pubblico?
feature: Audiences
exl-id: 7af7f101-f550-4fdc-bcd9-90e4107b0415
source-git-commit: 54d68bd528bac2ef3867943c670445c7c9e147e0
workflow-type: tm+mt
source-wordcount: '1044'
ht-degree: 26%

---

# Creazione di un pubblico

Tipi di pubblico in [!DNL Adobe Target] determina chi visualizza contenuti ed esperienze in un’attività con targeting.

I tipi di pubblico sono utilizzati in tutte le situazioni in cui è disponibile il targeting. Quando esegui il targeting di un’attività, hai le seguenti opzioni:

* Selezionare un pubblico riutilizzabile dalla [!UICONTROL Tipi di pubblico] elenco
* [Creare un pubblico specifico per l’attività](/help/c-target/creating-activity-only-audience.md) e mirarlo
* [Combinare più tipi di pubblico](/help/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) per creare un pubblico ad hoc

Puoi inoltre utilizzare i dati del pubblico raccolti da [!DNL Adobe Analytics] per il targeting in tempo reale e la personalizzazione in [!DNL Target] e altri [!DNL Adobe Experience Cloud] applicazioni. Vedi [Tipi di pubblico di Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html?lang=it) in *Componenti dell’interfaccia centrale di Experience Cloud* guida.

Esistono due tipi di pubblico in [!DNL Target]:

* **Tipi di pubblico di targeting:** Utilizzato per fornire contenuti diversi a diversi tipi di visitatori.
* **Tipi di pubblico per reportistica:** Utilizzato per determinare come diversi tipi di visitatori rispondono allo stesso contenuto e analizzare i risultati del test.

   In [!DNL Target], è possibile configurare i tipi di pubblico per reportistica solo se [!DNL Target] è utilizzato come origine per la generazione di rapporti. Se utilizzi [ Adobe Analytics come origine per la generazione di rapporti](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T), devi configurare i tipi di pubblico per la generazione di rapporti in [!DNL Analytics].

## Utilizza la [!UICONTROL Tipi di pubblico] elenco {#use-list}

Per accedere all’elenco [!UICONTROL Tipi di pubblico], fai clic su **[!UICONTROL Tipi di pubblico]** nella barra dei menu superiore:

![Elenco Tipi di pubblico](assets/audiences_list.png)

La [!UICONTROL Tipi di pubblico] contiene i tipi di pubblico che puoi utilizzare nelle attività. Utilizza la [!UICONTROL Tipi di pubblico] crea, modifica, duplica, copia o combina tipi di pubblico. L’elenco mostra anche l’origine in cui è stato creato il pubblico:

* [!DNL Adobe Target]
* [!DNL Adobe Target Classic]
* [!DNL Experience Cloud]
* [!DNL Adobe Experience Platform]

   >[!NOTE]
   >
   >La [!DNL Adobe Experience Platform] l&#39;origine è disponibile per tutti [!DNL Target] i clienti che utilizzano [Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md). Tipi di pubblico disponibili dal [!DNL Adobe Experience Platform] può essere utilizzato così come è o [combinato con tipi di pubblico esistenti](/help/c-target/combining-multiple-audiences.md).
   >
   >Gli utenti devono avere [!UICONTROL Approvatore] o lo stato precedente in [!DNL Target] per configurare [!DNL Target] [!UICONTROL Destinazioni] schede in AEP/RTCDP ([!DNL Real-time Customer Data Platform]).
   >
   >Per ulteriori informazioni consulta [Utilizzare i tipi di pubblico da Adobe Experience Platform](#aep).

Tipi di pubblico predefiniti, ad esempio &quot;[!UICONTROL Nuovi visitatori]&quot; e &quot;[!UICONTROL Visitatori di ritorno],&quot; non può essere rinominato.

Quando si lavora con tipi di pubblico originariamente creati in [!DNL Experience Cloud] o [!DNL Adobe Experience Platform], [!DNL Target] ti avvisa se fai riferimento a un pubblico in [!DNL Target] attività successivamente eliminate in [!DNL Experience Cloud] o [!DNL Adobe Experience Platform].

* Se un pubblico è stato eliminato in [!DNL Experience Cloud] o [!DNL Adobe Experience Platform], un’icona di avviso sia nel [!UICONTROL Pubblico] vengono visualizzati l’elenco e il selettore del pubblico. Una descrizione comandi nel [!DNL Target] L’interfaccia utente indica anche che il pubblico è stato eliminato in [!DNL Experience Cloud] o [!DNL Adobe Experience Platform].
* Se si tenta di combinare più tipi di pubblico con un pubblico eliminato o se si tenta di salvare un&#39;attività che fa riferimento a un pubblico eliminato, viene visualizzato un messaggio di avviso.

Puoi inoltre eseguire il targeting di parametri di profilo personalizzati e parametri `user.`. Quando crei un pubblico, trascina gli attributi che desideri utilizzare per eseguire il targeting dell’attività nella finestra di audience builder. Se l&#39;attributo desiderato non viene visualizzato, non è stato attivato da una mbox. Sono disponibili altri parametri mbox personalizzati nellʼelenco a discesa [!UICONTROL Parametri personalizzati].

Utilizza la [!UICONTROL Filtri] per filtrare [!UICONTROL Tipi di pubblico] elenco per origine: [!DNL Adobe Target], [!DNL Adobe Target Classic], [!DNL Experience Cloud]e [!DNL Adobe Experience Platform].

![Opzione Filtri in [!UICONTROL Tipi di pubblico] elenco](assets/filters.png)

Utilizza la [!UICONTROL Ricerca di tipi di pubblico] casella per cercare [!UICONTROL Tipi di pubblico] elenco. Puoi cercare qualsiasi parte del nome di un pubblico, oppure racchiudere tra virgolette una stringa specifica.

Puoi ordinare lʼelenco [!UICONTROL Tipi di pubblico] in base al nome o alla data dellʼultima modifica. Per ordinare in base al nome o alla data, fai clic sull’intestazione di colonna, quindi seleziona la visualizzazione dei tipi di pubblico in ordine crescente o decrescente.

## Visualizzare le definizioni dei tipi di pubblico {#section_11B9C4A777E14D36BA1E925021945780}

Puoi visualizzare i dettagli della definizione del pubblico in una scheda a comparsa in varie posizioni nella [!DNL Target] Interfaccia utente senza aprire il pubblico. Questa funzionalità si applica ai tipi di pubblico creati in [!DNL Target Standard/Premium] e i tipi di pubblico importati da [!DNL Target Classic] o creato tramite API.

Ad esempio, fai clic sul pulsante [!UICONTROL Visualizza dettagli] per il pubblico desiderato:

![Attività > Definizione pubblico](assets/audience_definition_list.png)

Fai clic sulla scheda di definizione del pubblico seguente per accedervi [!UICONTROL Visualizza dettagli] icona di un’attività [!UICONTROL Panoramica] pagina:

![Attività > Definizione pubblico](assets/view-details-activity-overview.png)

La scheda di definizione del pubblico mostra il tipo, la sorgente e gli attributi del pubblico. Fai clic su **[!UICONTROL Visualizza dettagli completi]** per visualizzare altre attività che fanno riferimento a tale pubblico, se applicabile. Se visualizzi una scheda di definizione del pubblico da un’attività [!UICONTROL Panoramica] pagina, fai clic su **[!UICONTROL Utilizzo del pubblico]**.

Le informazioni sull’utilizzo del pubblico possono aiutarti a evitare un impatto accidentale su altre attività durante la modifica dei tipi di pubblico. Informazioni [!UICONTROL Attività live], [!UICONTROL Attività inattive], [!UICONTROL Attività archiviate]e [!UICONTROL Sincronizzazione delle attività]. Questa funzione è disponibile per tutti i tipi di pubblico (pubblico della libreria e [pubblico per sola attività](/help/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483)).

Se un pubblico è [combinato con un altro pubblico](/help/c-target/combining-multiple-audiences.md) e il pubblico combinato viene utilizzato per creare un&#39;attività, le informazioni di utilizzo per entrambi i tipi di pubblico elencano la nuova attività creata.

![](assets/audience_definition_list_usage.png)

<!--The following audience definition card is for an audience imported from the Adobe Experience Cloud. In this instance, the audience was imported from Adobe Audience Manager (AAM).

![Usage tab on Audience Definition card](assets/audience_definition_mc.png)

The following details are available for these imported audience types:

| Audience Type | Details |
|--- |--- |
|Mobile audience|Marketing Name, Vendor, and Model.<br>The `matches | does not match` operator displays instead of `equals | does not equal`<br>![Imported Mobile Audience](/help/c-target/c-audiences/assets/imported_mobile_audience.png).|
|Visitor-behavior audience|**user.categoryAffinity:** `categoryAffinity` with `FAVORITE` parameter.<br>![Imported Category Affinity](/help/c-target/c-audiences/assets/imported_category_affinity.png)<br>**Monitoring:** Monitoring service equals true.<br>**No Monitoring Service:** Monitoring service equals false.<br>![Imported Monitoring](/help/c-target/c-audiences/assets/imported_monitoring.png)|
|Audiences using the NOT operator|**Single Rule:** Target displays the audience in the format `[All Visitor AND [NOT [rule]`. Single NOT rule displays with AND with `AllVisitor` audience.<br>![Imported Not Audience](/help/c-target/c-audiences/assets/imported_not_audience.png)|

Keep the following points in mind as you work with imported audiences:

* Expression target audiences are no longer supported in Target Standard/Premium. 
* Target Standard/Premium does not support some deprecated audiences or has improved operators for ease of use. Because of this, the definition of an imported audience, although working as per definition, does not mean that same is now available for creation in the Standard/Premium interface. For example, Social Audiences are visible with their rules but Target Standard/Premium does not allow social audiences to be created.-->

## Utilizzare i tipi di pubblico da [!DNL Adobe Experience Platform] {#aep}

Utilizzo dei tipi di pubblico creati in [!DNL Adobe Experience Platform] forniscono dati più ricchi sui clienti che consentono una personalizzazione più incisiva. La [Real-time Customer Data Platform](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html){target=_blank} (RTCP), integrato in [!DNL Adobe Experience Platform], consente alle aziende di unire dati noti e anonimi provenienti da più origini aziendali. Questo processo ti consente di creare profili cliente da utilizzare in tempo reale per fornire esperienze cliente personalizzate su tutti i canali e dispositivi.

Collegamento [!DNL Target] al [!DNL Real-time Customer Data Platform], i clienti possono arricchire la personalizzazione web sbloccando nuovi segmenti che in precedenza potevano essere inaccessibili a [!DNL Target] per abilitare la personalizzazione in tempo reale di millisecondi nella prima pagina della visita web di un cliente. Utilizzo dei tipi di pubblico creati in [!DNL Adobe Experience Platform] ti consente di espandere i punti dati disponibili per una personalizzazione più ricca.

Per maggiori informazioni, vedi i seguenti argomenti:

* [Note sulla versione delle destinazioni](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=en#destinations){target=_blank}
* [Connessione di personalizzazione personalizzata](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/custom-personalization.html){target=_blank} nel *Panoramica sulle destinazioni* guida
* [Connessione Adobe Target](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-target-connection.html){target=_blank} nel *Panoramica sulle destinazioni* guida
* [Configurare le destinazioni di personalizzazione per la stessa pagina e i casi d’uso di personalizzazione della pagina successivi](https://www.adobe.com/go/destinations-edge-personalization-en){target=_blank}

La tabella seguente mostra il tempo di valutazione dei segmenti per gli eventi provenienti da diversi scenari di implementazione:

| Scenario | Segmento perimetrale (valutazione in millisecondi) | Segmento in streaming (valutazione dei minuti) | Valutazione dei segmenti in batch |
| --- | --- | --- | --- |
| Eventi/dati dagli SDK Adobe Experience Platform | Sì | Sì | N/D |
| Eventi da at.js | No | Sì | N/D |
| Eventi dagli SDK di Target Mobile | No | Sì | N/D |
| Eventi da caricamento batch | No | No | Sì |
| Eventi da dati offline (streaming) | No | Sì | Sì |

## Video di formazione: Utilizzo del pubblico ![Badge tutorial](/help/assets/tutorial.png)

Questo video include informazioni sull&#39;utilizzo dei tipi di pubblico.

* Spiegazione del termine “pubblico”
* Spiegazione dei due modi in cui il pubblico viene utilizzato per lʼottimizzazione
* Trovare un pubblico nellʼelenco Tipi di pubblico
* Indirizzare unʼattività a un pubblico
* Utilizzare i tipi di pubblico per la reportistica passiva in un’attività

>[!VIDEO](https://video.tv.adobe.com/v/17398)
