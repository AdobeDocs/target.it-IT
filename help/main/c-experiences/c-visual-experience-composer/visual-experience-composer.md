---
keywords: compositore esperienza visivo;vec;wysiwyg
description: Scopri le nozioni di base sull’utilizzo del Compositore esperienza visivo in Adobe Target. Il Compositore esperienza visivo è un editor di WYSIWYG che consente di creare facilmente esperienze personalizzate.
title: Come si utilizza il Compositore esperienza visivo?
feature: Visual Experience Composer (VEC)
exl-id: 51650f2a-1f24-40c7-8692-77f55656b4f6
TQID: 'https://experienceleague.adobe.com/X4nfYuOtD3TVusnVIIEZhXwUdCZ-dMvbZeJlrkmI9Hs'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 140a7287246905d47bf02a84348627017a619386
workflow-type: tm+mt
source-wordcount: '889'
ht-degree: 0%
---
# [!UICONTROL Compositore esperienza visivo] (VEC)

Il [!UICONTROL Compositore esperienza visivo] (VEC) in [!DNL Adobe Target] è un editor WYSIWYG per la creazione e il testing di esperienze personalizzate direttamente su siti Web e pagine Web mobili senza modificare il codice.

Creare esperienze e offerte per le attività [!DNL Target] trascinando e rilasciando elementi, scambiando contenuti e modificando i layout di pagina. Il compositore fornisce anche opzioni per la modifica di HTML e JavaScript.

## Requisiti del browser {#browser-requirements}

[!DNL Safari] è supportato per l&#39;interfaccia [!DNL Adobe Target]. È possibile creare attività basate su moduli in [!DNL Safari] e utilizzare tutte le funzionalità, ad eccezione del Compositore esperienza visivo e del [!UICONTROL Compositore esperienza avanzato] (EEC). Se si apre Compositore esperienza visivo in [!DNL Safari], viene richiesto di passare a [!DNL Google Chrome] per modificare le esperienze.

I browser come [!DNL Firefox] potrebbero bloccare la visualizzazione nel Compositore esperienza visivo delle pagine che contengono contenuti misti, ad esempio una pagina non protetta all&#39;interno di un sito protetto. Se una pagina non viene visualizzata, fare clic sull&#39;icona accanto all&#39;URL nella barra degli indirizzi del browser, quindi fare clic su **[!UICONTROL Disattiva protezione in questa pagina]**. Questo problema non influisce sulla modalità di visualizzazione delle pagine per i visitatori del sito.

## Aprire il Compositore esperienza visivo {#open-the-vec}

Per impostare la pagina che si apre per impostazione predefinita nel Compositore esperienza visivo, immetti un URL predefinito di [!UICONTROL Compositore esperienza visivo] nella scheda [!DNL Target] **[!UICONTROL Amministrazione]** > **[!UICONTROL Compositore esperienza visivo]**.

Se non imposti un URL predefinito, il Compositore esperienza visivo si apre con una pagina vuota in cui puoi specificare un URL.

![Compositore esperienza visivo evidenziato](/help/main/c-experiences/c-visual-experience-composer/assets/vec-highlight-refresh.png)

## Modificare le esperienze {#edit-experiences}

### Visualizzare e denominare le esperienze {#view-and-name-experiences}

Utilizza le schede nella barra [!UICONTROL Esperienze] per visualizzare in che modo la pagina viene visualizzata da tipi di pubblico diversi o con esperienze diverse. Assegna un nome descrittivo a ogni esperienza per facilitarne l’identificazione nell’elenco.

Ad esempio, quando verifichi la posizione del collegamento Home nella barra di navigazione, denomina l’esperienza in cui appare prima &quot;Collegamento Home&quot;.

![Rinominare un&#39;esperienza nella barra Esperienze](/help/main/c-experiences/c-visual-experience-composer/assets/rename_exp.png)

### Selezionare e modificare gli elementi {#select-and-modify-elements}

Sposta il cursore sulla pagina per evidenziare singoli elementi con una casella sensibile al contesto.

Fai clic su un elemento evidenziato per visualizzare le opzioni di modifica per tale tipo di elemento. Ad esempio, selezionare un&#39;immagine e fare clic su **[!UICONTROL Cambia origine immagine]** per sostituirla oppure selezionare un pulsante per modificarne il colore del testo.

![Modifica delle opzioni per un elemento selezionato](/help/main/c-experiences/c-visual-experience-composer/assets/properties-exp.png)

Non è possibile modificare il contenuto all’interno di un iframe incorporato nella pagina. Per modificare tale contenuto, accertati che il documento iframe sia abilitato per [!DNL Target], quindi carica l’URL iframe direttamente nel Compositore esperienza visivo.

Le modifiche alla struttura della pagina all’esterno del Compositore esperienza visivo possono influenzare le posizioni utilizzate da un’attività. Se tali percorsi cambiano, [!DNL Target] potrebbe non essere in grado di trovare gli elementi modificati, il che potrebbe causare problemi durante la modifica delle esperienze.

### Sfoglia e progetta {#browse-and-design}

Fai clic su **[!UICONTROL Sfoglia]** per passare a una pagina accessibile dalla pagina corrente, ad esempio una pagina di spedizione o un carrello acquisti, ed esegui il test delle modifiche.

![Modalità Sfoglia nel Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/assets/browse_exp.png)

In modalità Sfoglia è inoltre possibile accedere agli elementi visualizzati al passaggio del mouse, ad esempio menu a comparsa e mini-carrelli. Quando si raggiunge la pagina o l&#39;elemento che si desidera modificare, fare clic su **[!UICONTROL Progettazione]** per modificare l&#39;esperienza.

Se uno stato al passaggio del mouse dipende da JavaScript, assicurarsi che **[!UICONTROL Disabilita JavaScript]** non sia selezionato. Per modificare gli elementi che dipendono da JavaScript, è necessario abilitarlo.

Per informazioni dettagliate sulle opzioni di modifica disponibili, vedere [Opzioni del Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81).

## Gestire il caricamento delle pagine {#manage-page-loading}

Alcune opzioni di modifica rimangono disponibili durante il caricamento di una pagina o dopo il suo mancato caricamento. Puoi anche annullare il caricamento della pagina per accedere a queste opzioni senza attendere.

### Modificare una pagina durante il suo caricamento o dopo il suo mancato caricamento {#loading}

Puoi apportare alcune modifiche prima che una pagina finisca di essere caricata nel Compositore esperienza visivo o dopo il suo mancato caricamento, ad esempio, perché il codice personalizzato non funziona più.

Utilizza le opzioni di modifica disponibili per:

* Apportare semplici modifiche, ad esempio aggiungere codice personalizzato o rinominare un’esperienza
* Copia il codice personalizzato esistente da una pagina non più accessibile
* Apportare semplici modifiche a una pagina che non può essere caricata nel Compositore esperienza visivo

La barra [!UICONTROL Esperienze], la barra [!UICONTROL Componenti] e le opzioni [!UICONTROL Configura] rimangono accessibili durante il caricamento della pagina o dopo il suo mancato caricamento.

### Annullare il caricamento di una pagina all’interno del Compositore esperienza visivo {#cancel-loading}

Annulla il caricamento della pagina nel Compositore esperienza visivo per modificare l’attività senza attendere il completamento del caricamento della pagina.

L’annullamento del caricamento della pagina è utile quando è necessario:

* Apportare modifiche minori alle modifiche esistenti
* Elimina una o più modifiche esistenti
* Inserisci o modifica codice personalizzato
* Correggere un URL di pagina immesso in modo errato
* Attivare o disattivare JavaScript prima di caricare la pagina nel Compositore esperienza visivo
* Aggiungi regole di test dei modelli ai criteri [!UICONTROL Consegna pagine]
* Ignora l&#39;interruttore globale [!UICONTROL Compositore esperienza avanzato] durante il caricamento di una pagina tramite il Compositore esperienza avanzato o in modalità solo iframe

Dopo aver annullato il caricamento della pagina, puoi passare da un’esperienza all’altra nell’attività senza attendere che la pagina venga caricata. Fai clic su **[!UICONTROL Ricarica]** per visualizzare nuovamente la pagina nel Compositore esperienza visivo.

>[!IMPORTANT]
>
>Se modifichi il codice personalizzato o apporti altre modifiche dopo aver annullato il caricamento della pagina, esegui un test di controllo qualità per verificare che le modifiche vengano consegnate come previsto.

Per interrompere il caricamento della pagina, fare clic su **[!UICONTROL Annulla caricamento]** durante il caricamento della pagina. La pagina rimane scaricata per questa attività durante la sessione di modifica corrente a meno che non venga ricaricata.

Fai clic su **[!UICONTROL Ricarica]** per riprendere a gestire le esperienze nell&#39;attività corrente o aggiungere nuove modifiche.
