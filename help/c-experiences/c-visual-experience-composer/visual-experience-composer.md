---
keywords: Visual Experience Composer (Compositore esperienza visivo);vec;wysiwyg
description: Scopri le basi dell'utilizzo di Visual Experience Composer (VEC) in  Adobe Target. VEC è un editor WYSIWYG che consente di creare facilmente esperienze personalizzate.
title: Come si utilizza Visual Experience Composer (VEC)?
feature: Visual Experience Composer (VEC)
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '1401'
ht-degree: 92%

---


# Compositore esperienza visivo

Informazioni sull&#39;utilizzo di [!UICONTROL Visual Experience Composer (Compositore esperienza visivo)] (VEC) in [!DNL Adobe Target].

Il VEC è un&#39;interfaccia utente WYSIWYG che consente di creare e testare facilmente esperienze e offerte personalizzate nel contesto del sito. Per creare esperienze e offerte per le attività di Target puoi trascinare, scambiare e modificare il layout e il contenuto di una pagina web (o offerta) oppure di una pagina web per dispositivi mobili.

Il Compositore esperienza visivo è una delle funzionalità principali di [!DNL Adobe Target]. Il Compositore esperienza visivo consente agli addetti al marketing e ai designer di creare e modificare i contenuti mediante un’interfaccia visiva che permette di operare molte scelte di progettazione senza dover intervenire direttamente sul codice. Il compositore offre anche opzioni per modificare il codice HTML e JavaScript.

Nella scheda Target **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** (Compositore esperienza visivo), potete immettere l&#39;URL predefinito di Visual Experience Composer (Compositore esperienza visivo).

![Impostazioni predefinite dell’URL del Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/assets/pref-default-url-new.png)

Questo URL determina la posizione di partenza all’apertura del Compositore esperienza visivo Se non immetti un URL predefinito, viene inizialmente aperta una pagina vuota e potrai quindi specificare un URL.

>[!NOTE]
>
>Alcuni browser, come Firefox, potrebbero impedire la visualizzazione di una pagina nel Compositore esperienza visivo se la pagina presenta contenuti misti (ad esempio, una pagina non protetta su un sito protetto). Se la pagina non viene visualizzata, fai clic sull’icona vicina all’URL nella barra degli indirizzi del browser, quindi fai clic su **[!UICONTROL Disattiva protezione in questa pagina]**. Questo problema non influenza la visualizzazione delle pagine da parte dei visitatori del sito.

Il contenuto all’interno di un iframe nella pagina non può essere modificato nel Compositore esperienza visivo. Per modificare il contenuto di un iframe, assicurati che il documento iframe sia abilitato per Target, quindi carica l’URL dell’iframe nel Compositore esperienza visivo.

Per un’anteprima della pagina per diversi tipi di pubblico o con altre esperienze, utilizza i menu a discesa nella parte superiore della pagina. Puoi specificare un nome per ogni esperienza nel secondo elenco a discesa. Ad esempio, se stai eseguendo il test della posizione del collegamento Pagina principale nella barra di navigazione, a un’esperienza in cui compare tale collegamento puoi assegnare un nome tipo “Collegamento Pagina principale”, per individuarla più facilmente nell’elenco delle esperienze.

>[!NOTE]
>
>Le modifiche alla struttura di una pagina che influenzano le posizioni utilizzate in un’attività creata in quella pagina potrebbero causare problemi nella modifica dell’esperienza. Se una posizione è stata modificata esternamente al Compositore esperienza visivo, Target potrebbe non individuare la posizione in cui il contenuto è stato modificato.

Mentre sposti il mouse sulla pagina, una casella sensibile al contesto segue il cursore ed evidenzia gli elementi nella pagina.

![Compositore esperienza visivo evidenziato](/help/c-experiences/c-visual-experience-composer/assets/vec-highlight-new.png)

Per modificare l’evidenziazione, fai clic sull’icona **[!UICONTROL Sovrapposizioni]**. Ad esempio, puoi scegliere di evidenziare solo immagini, collegamenti, mbox regionali, modifiche o JavaScript. Puoi modificare il colore dell’evidenziazione. Puoi inoltre specificare il colore di evidenziazione e il tipo di riempimento da usare per diversi tipi di elementi.

![Modifica le impostazioni di Sovrapposizione](/help/c-experiences/c-visual-experience-composer/assets/change-overlay.png)

Per visualizzare il menu delle opzioni disponibili per un certo tipo di elemento evidenziato, fai clic su quell’elemento. Ad esempio, per modificare un testo fai clic su un’immagine e seleziona **[!UICONTROL Modifica > Testo/HTML]**, oppure fai clic su un pulsante e modifica il colore dello sfondo. Con i pulsanti in alto a sinistra nella pagina puoi attivare e disattivare le sovrapposizioni.

Puoi inoltre fare clic su **[!UICONTROL Sfoglia]** e passare dalla pagina principale a una pagina disponibile, ad esempio quella di spedizione o del carrello acquisti, ed eseguire da questa il test delle modifiche. Puoi inoltre accedere agli elementi della pagina disponibili, come menu a comparsa e mini-carrelli, passando il puntatore del mouse sopra di essi. Quindi, fai clic su **[!UICONTROL Componi]** per modificare l’esperienza. Ad esempio, puoi modificare la struttura di un elenco a discesa del carrello acquisti o un carosello di immagini.

>[!NOTE]
>
>Se uno stato hover dipende da JavaScript, assicurati che **[!UICONTROL Disabilita JavaScript]** non sia selezionato. Per modificare elementi JavaScript è necessario che JavaScript sia abilitato.

Per informazioni sulle opzioni disponibili nel Compositore esperienza visivo, vedi [Opzioni del Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81).

È possibile eseguire alcune modifiche su una pagina mentre questa è in fase di caricamento (o dopo il suo mancato caricamento), oppure è possibile annullarne nel Compositore esperienza visivo. Per ulteriori informazioni, consulta:

* [Modificare una pagina durante il suo caricamento o dopo il suo mancato caricamento](#loading)
* [Annullare il caricamento di una pagina all’interno del Compositore esperienza visivo](#cancel-loading)

## Modificare una pagina durante il suo caricamento o dopo il suo mancato caricamento{#loading}

Potrai eseguire molte azioni prima che la pagina si carichi nel Compositore esperienza visivo, anche qualora non possa essere caricata completamente (ad esempio, se il codice personalizzato non è più operativo).

Alcuni motivi per cui potresti voler accedere o apportare modifiche a una pagina mentre è in fase di caricamento all’interno del Compositore esperienza visivo o dopo il suo mancato caricamento:

* Desideri apportare una semplice modifica a una pagina, ad esempio per aggiungere codice personalizzato o modificare il nome di un’esperienza
* Desideri copiare il codice personalizzato esistente da una pagina non più accessibile
* Sai che una pagina non può essere caricata nel Compositore esperienza visivo, ma desideri comunque apportare semplici modifiche

Mentre la pagina viene caricata (o dopo il suo mancato caricamento), il pannello [!UICONTROL Esperienze], il pannello [!UICONTROL Modifiche] e le impostazioni nella parte superiore dell’esperienza (Sovrapposizioni, Modifiche, Configura e così via) sono tutti accessibili.

L’illustrazione seguente mostra che è possibile inserire codice personalizzato o eseguire altre azioni mentre è ancora in corso il caricamento della pagina:

![Caricamento della pagina](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/loading-page.png)

## Annullare il caricamento di una pagina all’interno del Compositore esperienza visivo{#cancel-loading}

Puoi annullare il caricamento di una pagina all’interno del Compositore esperienza visivo per poter procedere con la modifica dell’attività senza attendere che venga completato il caricamento della pagina. Questa funzione consente di risparmiare tempo e di apportare semplici modifiche o di inserire codice personalizzato in modo più efficace, senza attendere che la pagina venga caricata all’interno del Compositore esperienza visivo.

Alcuni motivi per cui potrebbe essere utile annullare il caricamento della pagina all’interno del Compositore esperienza visivo:

* Desideri apportare modifiche minori alle modifiche esistenti
* Desideri eliminare una o più modifiche esistenti
* Desideri inserire o modificare del codice personalizzato
* Hai immesso erroneamente l’URL errato per la pagina
* Desideri abilitare o disabilitare JavaScript prima di caricare la pagina nel Compositore esperienza visivo
* Desideri aggiungere ulteriori regole di test dei modelli ai criteri di consegna delle pagine
* Desideri ignorare l’attivazione globale del Compositore esperienza avanzato quando si carica una pagina tramite il Compositore esperienza avanzato oppure soltanto l’iframe, pagina per pagina

Dopo aver annullato il caricamento della pagina nel Compositore esperienza visivo, puoi passare alle diverse esperienze nell’attività senza attendere che la pagina venga caricata. Per visualizzare nuovamente la pagina nel Compositore esperienza visivo, fai clic sul pulsante **[!UICONTROL Ricarica]**.

>[!IMPORTANT]
>
>Tieni presente che quando effettui un codice personalizzato o eventuali modifiche, scegliendo di annullare il caricamento nel Compositore esperienza visivo, devi verificare che la codifica o le modifiche vengano eseguite correttamente. Assicurati di eseguire un controllo qualità appropriato per verificare che il codice personalizzato ed altre modifiche vengano consegnati come previsto.

Per annullare il caricamento di una pagina nel Compositore esperienza visivo, fai clic sul pulsante **[!UICONTROL Annulla caricamento]** durante il caricamento della pagina. La pagina non viene caricata nel Compositore esperienza visivo per questa attività durante la sessione di modifica corrente.

![Pulsante Annulla caricamento](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/cancel-loading.png)

Per continuare a gestire le esperienze nell’attività corrente o per aggiungere nuove modifiche, fai clic sul pulsante **[!UICONTROL Ricarica]**.

![Pulsante Ricarica](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/reload-in-vec.png)

>[!NOTE]
>
>Esiste attualmente un problema noto con questa funzione che verrà risolto nella prossima versione. Per ulteriori informazioni, consulta “Annullare il caricamento di una pagina all’interno del Compositore esperienza visivo” nella pagina [Problemi noti e problemi risolti](/help/r-release-notes/known-issues-resolved-issues.md#cancel).

## Video di formazione

I video seguenti contengono ulteriori informazioni sui concetti descritti in questo articolo.

### Visual Experience Composer (1 di 2) (7:17) ![Logo di esercitazione](/help/assets/tutorial.png)

* Modificare il contenuto di una pagina
* Modificare il layout di una pagina

>[!VIDEO](https://video.tv.adobe.com/v/17399)

### Visual Experience Composer (2 di 2) (7:29) ![Logo di esercitazione](/help/assets/tutorial.png)

* Rinominare e duplicare un’esperienza
* Creare un’esperienza con reindirizzamento
* Indirizzare un’attività a un singolo URL o a un gruppo di URL
* Creare un’attività multipagina
* Creare un’esperienza e visualizzarne l’anteprima per i siti web reattivi
* Evidenziare tipi di elementi con le sovrapposizioni

>[!VIDEO](https://video.tv.adobe.com/v/17401)

### Orario ufficio: Visual Experience Composer (Compositore esperienza visivo) ![Logo di esercitazione](/help/assets/tutorial.png)

Questo video è una registrazione di “ [Office Hours](/help/cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7)”, un’iniziativa condotta dal team di assistenza clienti Adobe.

* Funzionamento del Compositore esperienza visivo
* Come evitare i problemi più comuni con Compositore esperienza visivo
* Procedure utili che puoi utilizzare con Compositore esperienza visivo

>[!VIDEO](https://video.tv.adobe.com/v/20784/)