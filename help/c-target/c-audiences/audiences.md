---
keywords: audience;audience rules;create audience;creating audience;targeting audience;reporting audience;report audience;segment;custom profile parameters;audience definition;audiences list
description: I tipi di pubblico (o audience) in Adobe Target determinano le fasce di visitatori a cui verranno presentati i contenuti e le esperienze di un’attività di destinazione.
title: Utilizzo del pubblico in Adobe Target
feature: audiences
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '879'
ht-degree: 95%

---


# Creazione di un pubblico{#create-audiences}

I tipi di pubblico (o audience) in Adobe Target determinano le fasce di visitatori a cui verranno presentati i contenuti e le esperienze di un’attività di destinazione.

I tipi di pubblico sono utilizzati in tutte le situazioni in cui è disponibile il targeting. Quando esegui il targeting di un’attività, per indirizzarla a un determinato pubblico, puoi selezionare un pubblico riutilizzabile dall’elenco [!UICONTROL Tipi di pubblico], [creare un pubblico specifico per l’attività](/help/c-target/creating-activity-only-audience.md) e impostarlo come destinazione, oppure [combinare più tipi di pubblico](/help/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) per creare un pubblico ad hoc.

Inoltre, puoi utilizzare dati sul pubblico raccolti da [!DNL Analytics] per il targeting in tempo reale e la personalizzazione in [!DNL Adobe Target] e altre soluzioni [!DNL Experience Cloud]. Consulta [Audiences](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html) (Audience) nella Guida *utente dei servizi* di base.

[!DNL Target] definisce due tipi di pubblico:

* **Tipi di pubblico di targeting:** per fornire contenuti diversi a diversi tipi di visitatori.
* **Tipi di pubblico per reportistica:** per determinare come diversi tipi di visitatori rispondono allo stesso contenuto e analizzare i risultati dei test.

   In [!DNL Target], è possibile configurare i tipi di pubblico per reportistica solo se [!DNL Target] è utilizzato come origine per la generazione di rapporti. Se utilizzi [ Adobe Analytics come origine per la generazione di rapporti](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T), devi configurare i tipi di pubblico per la generazione di rapporti in [!DNL Analytics].

## Utilizzo dell’elenco Tipi di pubblico

Per accedere all’elenco [!UICONTROL Tipi di pubblico], fai clic su **[!UICONTROL Tipi di pubblico]** nella barra dei menu superiore:

![Elenco Tipi di pubblico](assets/audiences_list.png)

Nell&#39;elenco [!UICONTROL Tipi di pubblico] sono inclusi tutti i gruppi di destinazione che puoi utilizzare nelle attività. Puoi usare l&#39;elenco [!UICONTROL Tipi di pubblico] per creare, modificare, eliminare, copiare o combinare i tipi di pubblico. L’elenco mostra anche l’origina in cui è stato creato il pubblico ([!DNL Target], [!DNL Target Classic], [!DNL Adobe Audience Manager (AAM),] [!DNL Experience Cloud] e così via). I tipi di pubblico predefiniti, ad esempio “Nuovi visitatori” e “Visitatori di ritorno”, non possono essere rinominati.

Quando si lavora con tipi di pubblico originariamente creati in AAM, Target avvisa se si fa riferimento a un pubblico in attività di Target che sono state successivamente eliminate in AAM.

* Se un pubblico è stato eliminato in AAM, viene visualizzata un&#39;icona di avviso sia nell&#39;elenco [!UICONTROL Tipi di pubblico] sia nel selettore dei tipi di pubblico. Un suggerimento nell&#39;interfaccia utente indica inoltre che il pubblico è stato eliminato in AAM.
* Se si tenta di combinare più tipi di pubblico con un pubblico eliminato o se si tenta di salvare un&#39;attività che fa riferimento a un pubblico eliminato, viene visualizzato un messaggio di avviso.

Puoi inoltre eseguire il targeting di parametri di profilo personalizzati e parametri `user.`. When adding an audience, click **[!UICONTROL Add Rule]** > **[!UICONTROL Visitor Profile]**, then choose the parameter you want to use to target your activity. Se il parametro desiderato non viene visualizzato, significa che non è stato attivato da una mbox. Sono disponibili altri parametri mbox personalizzati nellʼelenco a discesa [!UICONTROL Parametri personalizzati].

Utilizza la casella di ricerca per cercare nellʼelenco [!UICONTROL Tipi di pubblico]. Puoi cercare qualsiasi parte del nome di un pubblico, oppure racchiudere tra virgolette una stringa specifica.

Puoi ordinare lʼelenco [!UICONTROL Tipi di pubblico] in base al nome o alla data dellʼultima modifica. Per ordinare in base al nome o alla data, fai clic sull’intestazione di colonna, quindi seleziona la visualizzazione dei tipi di pubblico in ordine crescente o decrescente.

## Visualizzare le definizioni dei tipi di pubblico {#section_11B9C4A777E14D36BA1E925021945780}

Puoi visualizzare i dettagli della definizione del pubblico in una scheda a comparsa in diverse aree nell&#39;interfaccia utente di Target, senza aprire il pubblico. Questa funzionalità è applicabile ai tipi di pubblico creati in Target Standard/Premium e importati da Target Classic oppure creati tramite API.

Ad esempio, se passi il mouse su un pubblico nell&#39;elenco Tipi di pubblico e fai clic sull&#39;icona Visualizza, puoi accedere alla scheda di definizione del pubblico seguente:

![Attività > Definizione pubblico](assets/audience_definition_list.png)

Fai clic sull’icona Visualizza nella pagina Panoramica di un’attività per accedere alla scheda di definizione del pubblico seguente:

![Attività > Definizione pubblico](assets/audience_definition_list.png)

Fai clic sulla scheda [!UICONTROL Utilizzo tipo di pubblico] per visualizzare altre attività che fanno riferimento a tale pubblico, se applicabile. In questo modo puoi evitare un impatto accidentale su altre attività mentre modifichi i tipi di pubblico. Le informazioni includono attività live, inattive, archiviate e di sincronizzazione. Questa funzione è disponibile per tutti i tipi di pubblico (pubblico della libreria e [pubblico per sola attività](/help/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483)).

Se un pubblico viene combinato con un altro e il pubblico combinato viene utilizzato per creare un&#39;attività, nelle informazioni di utilizzo per entrambi i tipi di pubblico verrà riportata l&#39;attività appena creata.

![](assets/audience_definition_list_usage.png)

La scheda di definizione seguente è per un pubblico importato da Adobe Experience Cloud. In questo caso, il pubblico è stato importato da Adobe Audience Manager (AAM).

![Scheda Utilizzo nella scheda Definizione pubblico](assets/audience_definition_mc.png)

Per questi tipi di pubblico importati sono disponibili i seguenti dettagli:

| Tipo di pubblico | Dettagli |
|--- |--- |
| Pubblico mobile | Nome marketing, produttore e modello.<br>L’operatore `matches | does not match` viene visualizzato invece del `equals | does not equal`<br>![Pubblico mobile importato](/help/c-target/c-audiences/assets/imported_mobile_audience.png). |
| Pubblico con comportamento del visitatore | **user.categoryAffinity:** `categoryAffinity` con parametro `FAVORITE`.<br>![Affinità tra categorie importata ](/help/c-target/c-audiences/assets/imported_category_affinity.png)<br>**Monitoraggio:** il servizio di monitoraggio è uguale a vero.<br>**Nessun servizio di monitoraggio:** il servizio di monitoraggio è uguale a falso.<br>![Monitoraggio importato](/help/c-target/c-audiences/assets/imported_monitoring.png) |
| Tipi di pubblico con operatore NOT | **Regola singola:** Target mostra il pubblico nel formato `[All Visitor AND [NOT [rule]`. Viene visualizzata una singola regola NOT con AND con pubblico `AllVisitor`.<br>![Pubblico NOT importato](/help/c-target/c-audiences/assets/imported_not_audience.png) |

Quando lavori con tipi di pubblico importati, considera i seguenti punti:

* Il pubblico di destinazione con espressioni non è più supportato in Target Standard/Premium.
* In Target Standard/Premium non sono supportati alcuni tipi di pubblico obsoleti o sono stati migliorati alcuni operatori per facilitarne l&#39;uso. Per questo motivo, anche se un pubblico importato funziona in base alla sua definizione, potrebbe non essere disponibile per la creazione di un pubblico nell&#39;interfaccia Standard/Premium. Ad esempio, i tipi di pubblico Social sono visibili con le loro regole, ma Target Standard/Premium non consente di creare un pubblico Social.

## Video di formazione: Utilizzo dei tipi di pubblico ![Badge di esercitazione](/help/assets/tutorial.png)

Questo video include informazioni sull&#39;utilizzo dei tipi di pubblico.

* Spiegazione del termine “pubblico”
* Spiegazione dei due modi in cui il pubblico viene utilizzato per lʼottimizzazione
* Trovare un pubblico nellʼelenco Tipi di pubblico
* Indirizzare unʼattività a un pubblico
* Utilizzare i tipi di pubblico per la reportistica passiva in un’attività

>[!VIDEO](https://video.tv.adobe.com/v/17398)
