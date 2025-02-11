---
keywords: compositore esperienza visivo;vec;wysiwyg
description: Scopri le nozioni di base sull’utilizzo del Compositore esperienza visivo in Adobe Target. Il Compositore esperienza visivo è un editor di WYSIWYG che consente di creare facilmente esperienze personalizzate.
title: Come si utilizza il Compositore esperienza visivo?
feature: Visual Experience Composer (VEC)
exl-id: 51650f2a-1f24-40c7-8692-77f55656b4f6
source-git-commit: 457b02cb3cbaeee8ad9b56844891dd7e9f6f2d86
workflow-type: tm+mt
source-wordcount: '1130'
ht-degree: 57%

---

# Compositore esperienza visivo

Informazioni sull&#39;utilizzo di [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target].

>[!NOTE]
>
>La versione di [!DNL Target Standard/Premium] 25.2.1 (11 febbraio 2025) includeva una versione aggiornata del Compositore esperienza visivo. Per informazioni sulle differenze tra il Compositore esperienza visivo aggiornato e la versione precedente, vedi [Modifiche al Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md).

Il Compositore esperienza visivo è un’interfaccia utente di WYSIWYG che consente di creare e testare offerte ed esperienze personalizzate nel contesto del sito. È possibile creare esperienze e offerte per le attività [!DNL Target] trascinando, scambiando e modificando il layout e il contenuto di una pagina Web (o offerta) o di una pagina Web per dispositivi mobili.

Il Compositore esperienza visivo è una delle funzionalità principali di [!DNL Adobe Target]. Il Compositore esperienza visivo consente agli addetti al marketing e ai designer di creare e modificare i contenuti mediante un’interfaccia visiva che permette di operare molte scelte di progettazione senza dover intervenire direttamente sul codice. Il compositore offre anche opzioni per modificare il codice HTML e JavaScript.

Nella scheda Target **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]**, è possibile immettere l&#39;URL predefinito [!UICONTROL Visual Experience Composer].

![Compositore esperienza visivo evidenziato](/help/main/c-experiences/c-visual-experience-composer/assets/vec-highlight-refresh.png)

Questo URL determina la posizione di partenza all’apertura del Compositore esperienza visivo Se non immetti un URL predefinito, viene inizialmente aperta una pagina vuota e potrai quindi specificare un URL.

>[!NOTE]
>
>Alcuni browser, come [!DNL Firefox], potrebbero impedire la visualizzazione di una pagina nel Compositore esperienza visivo se la pagina contiene contenuti misti (ad esempio, una pagina non protetta su un sito protetto). Se la pagina non viene visualizzata, fare clic sull&#39;icona accanto all&#39;URL nella barra degli indirizzi del browser, quindi fare clic su **[!UICONTROL Disable protection on this page]**. Questo problema non influenza la visualizzazione delle pagine da parte dei visitatori del sito.

Il contenuto all’interno di un iframe nella pagina non può essere modificato nel Compositore esperienza visivo. Per modificare il contenuto di un iframe, accertati che il documento iframe sia abilitato per [!DNL Target], quindi carica l’URL dell’iframe nel Compositore esperienza visivo.

È possibile utilizzare le schede nel frame [!UICONTROL Experiences] per visualizzare la pagina così come apparirebbe a tipi di pubblico diversi o con esperienze diverse. Puoi fornire un nome per ogni esperienza. Ad esempio, se stai eseguendo il test della posizione del collegamento Pagina principale nella barra di navigazione, a un’esperienza in cui compare tale collegamento puoi assegnare un nome tipo “Collegamento Pagina principale”, per individuarla più facilmente nell’elenco delle esperienze.

>[!NOTE]
>
>Le modifiche alla struttura di una pagina che influenzano le posizioni utilizzate in un’attività creata in quella pagina potrebbero causare problemi nella modifica dell’esperienza. Se una posizione è stata modificata all&#39;esterno del Compositore esperienza visivo, [!DNL Target] potrebbe non essere in grado di trovare la posizione in cui è stato modificato il contenuto.

Mentre sposti il mouse sulla pagina, una casella sensibile al contesto segue il cursore ed evidenzia gli elementi nella pagina.

<!--Click the **[!UICONTROL Overlays]** icon to change the way the highlight displays. For example, you can choose to highlight only images, links, regional mboxes, modifications, or JavaScript. You can change the color of the highlight. You can also specify a highlight color and type of fill used to highlight different element types.

![Change Overlay settings](/help/main/c-experiences/c-visual-experience-composer/assets/change-overlay.png)-->

Fare clic su un elemento evidenziato per visualizzare il menu delle opzioni disponibili per il tipo di elemento. Ad esempio, è possibile fare clic su un&#39;immagine e selezionare **[!UICONTROL Change Image]** per modificare l&#39;immagine in un&#39;altra immagine. In alternativa, fare clic su un pulsante e modificare il colore del testo.

È inoltre possibile fare clic su **[!UICONTROL Browse]**, quindi passare a una pagina disponibile dalla pagina principale, ad esempio una pagina di spedizione o un carrello acquisti, ed eseguire il test delle modifiche su tale pagina. Puoi inoltre accedere agli elementi della pagina disponibili, come menu a comparsa e mini-carrelli, passando il puntatore del mouse sopra di essi. Al termine della navigazione alla pagina, fare clic su **[!UICONTROL Design]** per modificare l&#39;esperienza. Ad esempio, puoi modificare la struttura di un elenco a discesa del carrello acquisti o un carosello di immagini.

>[!NOTE]
>
>Se uno stato hover dipende da JavaScript, assicurarsi che **[!UICONTROL Disable JavaScript]** non sia selezionato. Per modificare elementi JavaScript è necessario che JavaScript sia abilitato.

Per informazioni sulle opzioni disponibili nel Compositore esperienza visivo, vedi [Opzioni del Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81).

È possibile eseguire alcune modifiche su una pagina mentre questa è in fase di caricamento (o dopo il suo mancato caricamento), oppure è possibile annullarne nel Compositore esperienza visivo. Per ulteriori informazioni, consulta:

* [Modificare una pagina durante il suo caricamento o dopo il suo mancato caricamento](#loading)
* [Annullare il caricamento di una pagina all’interno del Compositore esperienza visivo](#cancel-loading)

## Modificare una pagina durante il suo caricamento o dopo il suo mancato caricamento {#loading}

Potrai eseguire molte azioni prima che la pagina si carichi nel Compositore esperienza visivo, anche qualora non possa essere caricata completamente (ad esempio, se il codice personalizzato non è più operativo).

Alcuni motivi per cui potresti voler accedere o apportare modifiche a una pagina mentre è in fase di caricamento all’interno del Compositore esperienza visivo o dopo il suo mancato caricamento:

* Desideri apportare una semplice modifica a una pagina, ad esempio per aggiungere codice personalizzato o modificare il nome di un’esperienza
* Desideri copiare il codice personalizzato esistente da una pagina non più accessibile
* Sai che una pagina non può essere caricata nel Compositore esperienza visivo, ma desideri comunque apportare semplici modifiche

Mentre la pagina viene caricata (o dopo il suo mancato caricamento), il pannello [!UICONTROL Experiences], il pannello [!UICONTROL Modifications] e le impostazioni nella parte superiore dell&#39;esperienza (Sovrapposizioni, Modifiche, Configura e così via) sono tutti accessibili.

## Annullare il caricamento di una pagina all’interno del Compositore esperienza visivo {#cancel-loading}

Puoi annullare il caricamento di una pagina all’interno del Compositore esperienza visivo per poter procedere con la modifica dell’attività senza attendere che venga completato il caricamento della pagina. Questa funzione consente di risparmiare tempo e di apportare semplici modifiche o di inserire codice personalizzato in modo più efficace, senza attendere che la pagina venga caricata all’interno del Compositore esperienza visivo.

Alcuni motivi per cui potrebbe essere utile annullare il caricamento della pagina all’interno del Compositore esperienza visivo:

* Desideri apportare modifiche minori alle modifiche esistenti
* Desideri eliminare una o più modifiche esistenti
* Desideri inserire o modificare del codice personalizzato
* Hai immesso erroneamente l’URL errato per la pagina
* Desideri abilitare o disabilitare JavaScript prima di caricare la pagina nel Compositore esperienza visivo
* Desideri aggiungere ulteriori regole di test dei modelli ai criteri di consegna delle pagine
* Desideri ignorare l’attivazione globale del Compositore esperienza avanzato quando si carica una pagina tramite il Compositore esperienza avanzato oppure soltanto l’iframe, pagina per pagina

Dopo aver annullato il caricamento della pagina nel Compositore esperienza visivo, puoi passare alle diverse esperienze nell’attività senza attendere che la pagina venga caricata. Per visualizzare di nuovo la pagina nel Compositore esperienza visivo, fai clic sul pulsante **[!UICONTROL Reload]**.

>[!IMPORTANT]
>
>Tieni presente che quando effettui un codice personalizzato o eventuali modifiche, scegliendo di annullare il caricamento nel Compositore esperienza visivo, devi verificare che la codifica o le modifiche vengano eseguite correttamente. Assicurati di eseguire un controllo qualità appropriato per verificare che il codice personalizzato ed altre modifiche vengano consegnati come previsto.

Per annullare il caricamento di una pagina nel Compositore esperienza visivo, fai clic sul pulsante **[!UICONTROL Cancel Loading]** durante il caricamento della pagina. La pagina non viene caricata nel Compositore esperienza visivo per questa attività durante la sessione di modifica corrente.

Per continuare a gestire le esperienze nell&#39;attività corrente o per aggiungere nuove modifiche, fare clic sul pulsante **[!UICONTROL Reload]**.
