---
keywords: Tracciamento clic;tracciamento dei clic;clic;AppMeasurement
description: Scopri come  [!DNL Adobe Target]  consente di tenere traccia dei clic su qualsiasi elemento come metrica di successo.
title: Cos’è il tracciamento dei clic?
feature: Success Metrics
exl-id: 9181424b-179e-49fc-b760-b764a0c3458a
source-git-commit: 43d2484e57b1e2d292cf65c041fb9f5f49b2084c
workflow-type: tm+mt
source-wordcount: '858'
ht-degree: 75%

---

# Tracciamento dei clic

[!DNL Adobe Target] consente di tenere traccia dei clic su qualsiasi elemento come metrica di successo. Il tracciamento dei clic si riferisce al processo di monitoraggio e registrazione delle interazioni dell’utente, in particolare dei clic, sugli elementi all’interno di una pagina web o esperienza. Si tratta di un elemento chiave per misurare il coinvolgimento e le prestazioni in test A/B, test multivariati e attività di personalizzazione.

>[!NOTE]
>
>Il tracciamento dei clic non è supportato nella richiesta globale di [!DNL Target] se questa viene utilizzata come posizione in un’attività basata su modulo.

## Configurare il tracciamento dei clic {#section_5540C5A533114E57BAE022A600B02E72}

1. Quando imposterai gli obiettivi dell&#39;attività nella pagina [!UICONTROL Goals & Settings], seleziona la metrica di successo **[!UICONTROL Conversion]**.
1. Per eseguire l&#39;azione, selezionare **[!UICONTROL Clicked an element]**, quindi fare clic su **[!UICONTROL Select elements]**.

   La pagina verrà aperta in [!UICONTROL Visual Experience Composer] (VEC).

1. Seleziona gli elementi di cui desideri tenere traccia.

   Per suggerimenti sulla selezione degli elementi, consulta la sezione *Considerazioni* di seguito.

1. Fai clic su **[!UICONTROL Done]** nella parte superiore della schermata per salvare le selezioni.

Quando un partecipante all’attività fa clic su un elemento selezionato, tale clic viene conteggiato come conversione.

## Pannello Elementi selezionati {#selected-elements}

Per le attività [!UICONTROL A/B Test], [!UICONTROL Experience Targeting] (XT), [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Multivariate Test] (MVT), un pannello [!UICONTROL Selected Elements] elenca gli elementi selezionati per il tracciamento dei clic sul lato sinistro.

![Pannello Elementi selezionati](/help/main/c-activities/r-success-metrics/assets/selected-elements.png)

Quando si fa clic su un elemento nel pannello [!UICONTROL Tracked Components] è possibile applicare diverse azioni. La tabella seguente descrive ogni azione che è possibile eseguire su un elemento:

| Azione | Descrizione |
| --- | --- |
| [!UICONTROL Tracked actions] | Visualizza l&#39;azione elemento. |
| [!UICONTROL CSS selector] | Consente di modificare il selettore CSS. |
| [!DNL Delete] | Elimina l’elemento. |

### Aggiungi elemento

Se conosci già il percorso DOM del selettore, puoi aggiungerlo manualmente facendo clic sull&#39;icona [!UICONTROL Add Component] nella parte superiore del pannello.

## Considerazioni {#considerations}

Ci sono diversi fattori da considerare quando si selezionano gli elementi:

* La funzione percorso DOM è disponibile quando si imposta il tracciamento dei clic. Facendo clic su un elemento della pagina, viene visualizzato il menu delle opzioni del Compositore esperienza visivo. Inoltre, il percorso DOM corrispondente viene visualizzato nella parte inferiore della pagina. Puoi utilizzare il percorso DOM per vedere rapidamente le informazioni sull’elemento selezionato (tipo, ID e classe) e spostarti verso l’alto o il basso nel percorso DOM per selezionare l’elemento desiderato.

  Come per la creazione di esperienze, al passaggio 1 nel flusso di lavoro di creazione attività, puoi scegliere un elemento con il selettore del percorso DOM nella parte inferiore della pagina. Quando selezioni un elemento dal percorso DOM, nel Compositore esperienza visivo l’elemento corrispondente è visualizzato come Selezionato. Per deselezionare un elemento selezionato, puoi fare clic di nuovo su di esso nel selettore del percorso DOM o sulla casella “Selezionato” nel Compositore esperienza visivo.

  Per ulteriori informazioni, consulta [Navigare tra gli elementi utilizzando il percorso DOM](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path) in *Opzioni del Compositore esperienza visivo*.

* È possibile passare a una pagina diversa per monitorare i clic su una pagina in cui non è possibile modificare il contenuto. Questa pagina diversa deve essere inclusa nell&#39;attività utilizzando la [funzionalità multipagina](/help/main/c-experiences/c-visual-experience-composer/multipage-activity.md#concept_277E096063E14813AC5D8EDFA1D2ED48) e [!DNL at.js] deve essere implementato su di essa.
* Se selezioni più di un elemento, quando un partecipante fa clic su uno qualsiasi degli elementi scelti, il clic viene conteggiato. Per contare ogni elemento separatamente, imposta le metriche di successo individuali per ogni elemento. Per contare un elemento facendo clic su più elementi in una pagina, modifica il selettore degli elementi CSS in modo che corrisponda a più elementi.
* Assicurati di selezionare il livello di elemento di cui desideri tenere traccia. Ad esempio, quando definisci un pulsante, assicurati di selezionare il collegamento e non il testo del pulsante.
* Gli eventi clic vengono inviati a [!DNL Target] nella stessa pagina del clic.
* Se la metrica di tracciamento dei clic è la metrica obiettivo di un&#39;attività [!UICONTROL Analytics for Target] (A4T), affinché possa essere tracciata il visitatore deve fare clic su tale elemento entro 60 secondi dal caricamento della pagina.
* Il tracciamento dei clic non funziona su elementi che includono caratteri di escape nei rispettivi selettori, inclusi i seguenti:

  | Carattere | Descrizione |
  |---|---|
  | N. | Cancelletto o hash |
  | : | Due punti |
  | . | Punto |
  | $ | Simbolo del dollaro |
  | `[ ]` | Parentesi quadre |

* Se si utilizza il tracciamento dei clic [!DNL at.js] e si utilizza anche [!DNL Analytics] AppMeasurement, il tracciamento dei clic [!DNL at.js] annulla tutti gli altri gestori eventi di clic. Di conseguenza, il gestore di clic AppMeasurement non viene mai eseguito.

  [!DNL at.js] gestisce in modo particolare il tracciamento dei clic quando l’elemento sottostante è un tag `A` (collegamento) o un tag `FORM`.

  I seguenti passaggi vengono eseguiti da [!DNL at.js] quando l’evento di tracciamento dei clic è associato un tag `A` (collegamento) o a un tag `FORM`:

   1. Invocare `event.preventDefault()`.

   1. Attivare la richiesta di [!DNL Target].

   1. Quando la richiesta di [!DNL Target] genera un callback di esito positivo o errore, eseguire il comportamento predefinito:

      * Tag (collegamento)`A`: il comportamento predefinito consiste nel passare all&#39;URL definito dall&#39;attributo href.
      * Tag `FORM`: il comportamento predefinito consiste nell’inviare il modulo.

  Questo comportamento predefinito potrebbe interferire con il tracciamento dei clic di [!DNL Analytics]. Se si utilizza [!DNL Analytics], per il tracciamento dei clic è necessario appoggiarsi ad [!DNL Analytics] anziché a [!DNL Target].

* Il tracciamento dei clic non viene registrato nelle pagine in cui la pagina e l’URL attività appartengono a proprietà diverse. Le autorizzazioni per utenti Enterprise sono una funzione di [!DNL Target Premium]. Per ulteriori informazioni, consulta [Autorizzazioni per gli utenti Enterprise](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

* Le metriche di tracciamento dei clic non sono collegate ad alcuna esperienza specifica in un’attività.

* Utilizza i tipi di pubblico se è necessario limitare l’ambito delle metriche di tracciamento dei clic.

* Più attività possono definire una metrica di tracciamento dei clic per lo stesso selettore. In tal caso, quando un visitatore è idoneo a una di queste attività e fa clic sul selettore, la metrica di tracciamento dei clic aumenta per tutte le attività associate per le quali il visitatore è qualificato.

## Video di formazione {#section_36607204DAE146E3B8E2C609D244EDB1}

Questo video include informazioni sulla creazione di metriche di successo per il tracciamento dei clic.

* Le metriche per “Obiettivo”
* Comprendere e generare metriche [!UICONTROL Conversion], [!UICONTROL Revenue] e [!UICONTROL Engagement]
* Creazione di una metrica di tracciamento dei clic

>[!VIDEO](https://video.tv.adobe.com/v/17380)
