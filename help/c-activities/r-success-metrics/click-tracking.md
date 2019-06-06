---
description: Target ti consente di tenere traccia dei clic su qualsiasi elemento come metrica di successo.
keywords: Tracciamento clic;tracciamento dei clic;clic; AppMeasurement
seo-description: Target ti consente di tenere traccia dei clic su qualsiasi elemento come metrica di successo.
seo-title: Tracciamento dei clic
solution: Target
subtopic: Introduzione
title: Tracciamento dei clic
topic: Standard
uuid: 4a8fbb23-93d8-49f3-aca3-dbbdd6da0178
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Tracciamento dei clic{#click-tracking}

Target ti consente di tenere traccia dei clic su qualsiasi elemento come metrica di successo.

>[!NOTE]
>
>Il tracciamento dei clic non è supportato nella mbox globale di destinazione quando viene utilizzata come posizione in un’attività basata su modulo.

## Impostazione del tracciamento dei clic {#section_5540C5A533114E57BAE022A600B02E72}

1. Quando imposterai gli obiettivi dell&#39;attività nella pagina [!UICONTROL Obiettivi e impostazioni], seleziona la metrica di successo **[!UICONTROL Conversione]**.
1. Per eseguire tale azione, seleziona **[!UICONTROL Scegli un elemento]**, quindi fai clic su **[!UICONTROL Seleziona elementi]**.

   La pagina viene visualizzata nel [!UICONTROL Compositore esperienza visivo].

1. Seleziona gli elementi di cui desideri tenere traccia.

   Per suggerimenti sulla selezione degli elementi, consulta la sezione Considerazioni, di seguito.

1. Fai clic sul segno di spunta nella parte superiore dello schermo per salvare le selezioni.

Quando un partecipante all&#39;attività fa clic su un elemento selezionato, tale clic viene conteggiato come conversione.

## Considerazioni {#considerations}

Ci sono diversi fattori da considerare quando si selezionano gli elementi:

* La funzione percorso DOM è disponibile quando si imposta il tracciamento dei clic. Facendo clic su un elemento della pagina, viene visualizzato il menu delle opzioni del Compositore esperienza visivo. Inoltre, il percorso DOM corrispondente viene visualizzato nella parte inferiore della pagina. Puoi utilizzare il percorso DOM per vedere rapidamente le informazioni sull’elemento selezionato (tipo, ID e classe) e spostarti verso l’alto o il basso nel percorso DOM per selezionare l’elemento desiderato.

   ![Illustrazione del percorso DOM](/help/c-activities/r-success-metrics/assets/click-tracking-dom.png)

   Come per la creazione di esperienze, al passaggio 1 nel flusso di lavoro di creazione attività, puoi scegliere un elemento con il selettore del percorso DOM nella parte inferiore della pagina. Quando selezioni un elemento dal percorso DOM, nel Compositore esperienza visivo l’elemento corrispondente è visualizzato come Selezionato. Per deselezionare un elemento selezionato, puoi fare clic di nuovo su di esso nel selettore del percorso DOM o sulla casella Selezionato nel Compositore esperienza visivo.

   Per ulteriori informazioni, consulta [Navigare tra gli elementi utilizzando il percorso DOM](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path) in *Opzioni del Compositore esperienza visivo*.

* È possibile passare a una pagina diversa per monitorare i clic su una pagina in cui non è possibile modificare il contenuto. Questa pagina diversa deve essere inclusa nell’attività utilizzando [la funzione multipagina](../../c-experiences/c-visual-experience-composer/multipage-activity.md#concept_277E096063E14813AC5D8EDFA1D2ED48) e [!DNL at.js] o [!DNL mbox.js] deve essere implementato su di essa.
* Se selezioni più di un elemento, quando un partecipante fa clic su uno qualsiasi degli elementi scelti, il clic viene conteggiato. Per contare ogni elemento separatamente, imposta le metriche di successo individuali per ogni elemento.
* Assicurati di selezionare il livello di elemento di cui desideri tenere traccia. Ad esempio, quando definisci un pulsante, assicurati di selezionare il collegamento e non il testo del pulsante.
* Gli eventi clic vengono inviati a [!DNL Target] nella stessa pagina del clic.
* Se la metrica di tracciamento dei clic è la metrica di obiettivo di un&#39;attività A4T, il visitatore deve fare clic su tale elemento entro 60 secondi dal caricamento della pagina in modo da tenere traccia della metrica.
* Il tracciamento dei clic non funziona su elementi che includono caratteri di escape nei rispettivi selettori, inclusi i seguenti:

   | Carattere | Descrizione |
   |---|---|
   | # | Cancelletto o hash |
   | : | Due punti |
   | . | Punto |
   | $ | Simbolo del dollaro |
   | [ ] | Parentesi quadre |

* Se si utilizza il tracciamento dei clic [!DNL at.js] e si utilizza anche Analytics AppMeasurement, il tracciamento dei clic [!DNL at.js] annulla tutti gli altri gestori eventi di clic. Di conseguenza, il gestore di clic AppMeasurement non viene mai eseguito.

   [!DNL at.js] gestisce in modo particolare il tracciamento dei clic quando l’elemento sottostante è un tag `A` (collegamento) o un tag `FORM`.

   I seguenti passaggi vengono eseguiti da [!DNL at.js] quando l’evento di tracciamento dei clic è associato un tag `A` (collegamento) o a un tag `FORM`:

   1. Invocare `event.preventDefault()`.

   1. Attivare la richiesta di Target.

   1. In base al successo della richiesta di Target o all&#39;errore di callback, eseguire il comportamento predefinito:

      * Tag (collegamento)`A`: il comportamento predefinito consiste nel passare all&#39;URL definito dall&#39;attributo href.
      * Tag `FORM`: il comportamento predefinito consiste nell’inviare il modulo.
   Questo comportamento predefinito potrebbe interferire con il tracciamento dei clic di Analytics. Se si utilizza Analytics, per il tracciamento dei clic è necessario fare affidamento su Analytics anziché su Target.

* Il tracciamento dei clic non viene registrato nelle pagine in cui la pagina e l’URL attività appartengono a proprietà diverse. Le autorizzazioni per utenti Enterprise sono una funzione di Target Premium. Per ulteriori informazioni, consulta [Autorizzazioni per gli utenti Enterprise](/help/administrating-target/c-user-management/property-channel/property-channel.md).

## Video di formazione {#section_36607204DAE146E3B8E2C609D244EDB1}

Questo video include informazioni sulla creazione di metriche di successo per il tracciamento dei clic.

* Le metriche per “Obiettivo”
* Concetti e creazione di metriche per conversione, ricavi e coinvolgimento
* Creazione di una metrica di tracciamento dei clic

>[!VIDEO](https://video.tv.adobe.com/v/17380)