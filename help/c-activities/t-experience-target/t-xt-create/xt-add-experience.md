---
description: Il Compositore esperienza offre un’interfaccia visiva per la modifica delle esperienze sulla pagina.
keywords: creare un’esperienza;creazione di esperienza;priorità;pubblico;esperienza;compositore esperienza visivo
seo-description: Il Compositore esperienza offre un’interfaccia visiva per la modifica delle esperienze sulla pagina.
seo-title: Creare esperienze
solution: Target
title: Creare esperienze
topic: Advanced,Standard,Classic
uuid: ce559c3c-5a16-46b8-b2a7-df696626c7c0
translation-type: tm+mt
source-git-commit: b1dd50db873cb9a7cdca976366171ddf0c02d156

---


# Creare esperienze{#create-experience}

Il Compositore esperienza offre un’interfaccia visiva per la modifica delle esperienze sulla pagina.

Per ulteriori dettagli sulle esperienze, vedi [Esperienze](../../../c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D).

1. Fai clic su **[!UICONTROL Aggiungi esperienza]**.

   >[!NOTE]
   >
   >Se stai eseguendo il targeting di un&#39;esperienza per un pubblico, è necessario selezionare il pubblico prima di poter aggiungere un’esperienza. Viene visualizzato un messaggio per ricordarti di scegliere il pubblico.

1. Quando richiesto, immetti l&#39;URL attività. Digita l’URL completo (comprensivo di `https://`), quindi fai clic su **[!UICONTROL Continua]**.

   Nel Compositore esperienza (vedi [Esperienze](../../../c-experiences/experiences.md#concept_1D011219034B492BB03C08B3BB80E3F0)) viene aperta la pagina specificata in Preferenze account. Per visualizzare una pagina diversa fai clic sull’icona del globo e immetti l’URL nella casella Seleziona URL nel Compositore esperienza, quindi fai clic su **[!UICONTROL Continua]**. Se hai inserito un URL per un sito che non include il codice JavaScript di Target Standard, non puoi selezionare elementi di pagina.

   Per impostazione predefinita, il Compositore esperienza visivo non consente di modificare gli elementi contenenti JavaScript, ad esempio i banner rotanti. È possibile disattivare JavaScript per poter modificare tali elementi utilizzando il Compositore esperienza visivo.

   >[!NOTE]
   >
   >Se modifichi l’URL dopo aver apportato modifiche a una pagina per una o più esperienze, l’esperienza viene reimpostata utilizzando la nuova pagina e le modifiche apportate andranno perse.

1. Seleziona gli elementi da modificare e apporta le modifiche desiderate.

   Quando passi il puntatore del mouse sopra gli elementi della pagina, gli elementi vengono evidenziati. Qualsiasi elemento evidenziato può essere modificato utilizzando il Compositore esperienza.

   Se hai creato una mbox sulla pagina utilizzando Target Classic (in precedenza Test&amp;Target), questa viene visualizzata come un elemento che mostra il nome della mbox, e può essere modificata come qualsiasi altro elemento.

   Per un elenco delle azioni che possono essere eseguite su un elemento nella pagina visualizzata per modificare l&#39;esperienza, consulta [Opzioni del Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/viztarget-options.md).

   >[!NOTE]
   >
   >Se distribuisci un’immagine da un’origine diversa dalla pagina principale (ad esempio un’immagine in hosting su akamai.net e distribuita a dell.com), l’immagine non viene visualizzata nella miniatura della pagina mostrata nel diagramma di flusso.

1. Fai clic sul pulsante con il segno di spunta una volta terminata la progettazione dell&#39;esperienza.

   Il diagramma dell&#39;attività mostra quanto segue:

   ![](assets/xt_diagram.png)

   Se un’esperienza include contenuto di diversi domini, la miniatura potrebbe non essere visualizzata correttamente ed essere sostituita da un’icona.
1. Se necessario, crea ulteriori esperienze.

   >[!NOTE]
   >
   >È possibile trascinare e rilasciare le coppie Pubblico/Esperienza durante la creazione o la modifica di attività di Targeting esperienze per disporre le coppie nell’ordine desiderato. I visitatori saranno valutati per le esperienze, nell&#39;ordine dall&#39;alto verso il basso.

   ![](assets/move_experiences.jpg)

   Il targeting delle esperienze presuppone che l&#39;ordine sia importante. Se un visitatore rientra nella prima coppia Pubblico/Esperienza, viene consegnata la prima esperienza.

   Supponi, ad esempio, di non sapere che l’ordine è importante durante la creazione di un’attività di targeting esperienze. Successivamente, ti rendi conto durante i test che i visitatori che ritenevi più idonei per le esperienze B o C sono invece qualificati per l&#39;esperienza A. Questo potrebbe essere perché i tipi di pubblico non si escludono a vicenda e non sono nell&#39;ordine corretto (per esempio, esperienza A = Stati Uniti, esperienza B = San Francisco ed esperienza C = California). In questo scenario, tutti gli utenti degli Stati Uniti si qualificano per l&#39;esperienza A, sia che si trovino a San Francisco o altrove in California. È possibile riordinare le coppie Pubblico/Esperienza da più restrittive a meno restrittive (San Francisco &gt; California &gt; Stati Uniti) senza ricreare l&#39;intera attività.

## Rinominare, modificare o eliminare un’esperienza

Fai clic sull’icona Modifica (tre puntini di sospensione verticali) in un’esperienza in un’attività di un test A/B o targeting di esperienza (XT) e scegli tra le seguenti opzioni, a seconda delle necessità:

* Rinomina
* Modifica
* Elimina

![](assets/experience_edit.png)

Fai clic su **[!UICONTROL Successivo]** dopo aver completato il passaggio.

## Duplicare un’esperienza

È possibile copiare un’esperienza in un’attività di Targeting esperienza (XT) così da poter apportare modifiche minori senza dover ricreare l’esperienza da zero.

Nella pagina **[!UICONTROL Esperienze]** (il primo passaggio del flusso di lavoro guidato in tre passaggi), fai clic sui tre puntini di sospensione verticali &gt; **[!UICONTROL Duplica]**.

![](assets/duplicate_experience.png)

## Video di formazione: Utilizzo del Compositore esperienza visivo

Questo video fornisce informazioni sull’utilizzo delle opzioni del Compositore esperienza visivo.

* Modificare il contenuto di una pagina
* Modificare il layout di una pagina

>[!VIDEO](https://video.tv.adobe.com/v/17399)