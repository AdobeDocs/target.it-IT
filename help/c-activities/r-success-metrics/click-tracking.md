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
translation-type: tm+mt
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

* La funzione path path (Percorso DOM) è disponibile quando si imposta il tracciamento dei clic. Quando si fa clic su un elemento della pagina, viene visualizzato il menu delle opzioni VEC. Inoltre, il percorso DOM corrispondente viene visualizzato nella parte inferiore della pagina. Potete utilizzare il percorso DOM per vedere rapidamente le informazioni sull&#39;elemento selezionato (tipo, ID e classe) e spostarsi verso l&#39;alto o il basso sul percorso DOM per selezionare l&#39;elemento desiderato.

   ![Illustrazione percorso DOM](/help/c-activities/r-success-metrics/assets/click-tracking-dom.png)

   Esattamente come durante la creazione di esperienze nel passaggio 1 nel flusso di lavoro di creazione attività, il selettore percorso DOM nella parte inferiore della pagina consente di scegliere un elemento. Quando si seleziona un elemento dal percorso DOM, l&#39;elemento corrispondente nell&#39;aula virtuale viene visualizzato come &quot;Selezionato&quot;. Per deselezionare un elemento selezionato, potete di nuovo fare clic sull&#39;elemento nel selettore del percorso DOM o fare clic sulla casella «Selezionato» all&#39;interno della VEC.

   Per ulteriori informazioni, consultate [Navigare tra gli elementi mediante il percorso DOM](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path) in *Visual Experience Composer Options*(Opzioni di Visual Experience Composer (Compositore esperienza visivo).

* È possibile passare a una pagina diversa per monitorare i clic su una pagina in cui non è possibile modificare il contenuto. Questa pagina diversa deve essere inclusa nell&#39;attività utilizzando  [la funzione multipagina](../../c-experiences/c-visual-experience-composer/multipage-activity.md#concept_277E096063E14813AC5D8EDFA1D2ED48) e [!DNL at.js] o [!DNL mbox.js] deve essere implementato su di essa.
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

* Il monitoraggio dei clic non viene registrato nelle pagine in cui la pagina e l&#39;URL attività appartengono a proprietà diverse. Le autorizzazioni dell&#39;utente Enterprise sono una funzione Target Premium. Per ulteriori informazioni, consultate [Autorizzazioni utente Enterprise](/help/administrating-target/c-user-management/property-channel/property-channel.md).

## Video di formazione {#section_36607204DAE146E3B8E2C609D244EDB1}

Questo video include informazioni sulla creazione di metriche di successo per il tracciamento dei clic.

* Le metriche per “Obiettivo”
* Concetti e creazione di metriche per conversione, ricavi e coinvolgimento
* Creazione di una metrica di tracciamento dei clic

>[!VIDEO](https://video.tv.adobe.com/v/17380)