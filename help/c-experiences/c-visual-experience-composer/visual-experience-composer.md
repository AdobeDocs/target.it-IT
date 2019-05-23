---
description: Informazioni sull’utilizzo del Compositore esperienza visivo (VEC).
seo-description: Informazioni sull’utilizzo del Compositore esperienza visivo (VEC) in Adobe Target.
seo-title: Compositore esperienza visivo (VEC) di Adobe Target
title: Compositore esperienza visivo
uuid: f1e6f67e-1d7e-4806-8389-2ce165b534b4
translation-type: tm+mt
source-git-commit: f59e96cd5afcae9d27d730aecead9eb360f04026

---


# Compositore esperienza visivo (VEC){#visual-experience-composer-vec}

Informazioni sull’utilizzo del Compositore esperienza visivo (VEC).

Il Compositore esperienza visivo è una delle funzionalità principali di [!DNL Adobe Target]. L&#39;aula virtuale è un editor che consente ai professionisti del marketing e ai designer di creare e modificare il contenuto tramite un&#39;interfaccia visiva. che permette di operare molte scelte di progettazione senza dover intervenire direttamente sul codice. Il compositore offre anche opzioni per modificare il codice HTML e JavaScript.

Nella scheda **[!UICONTROL Configurazione]** &gt; **[!UICONTROL Preferenze]** di Target, puoi immettere l’URL predefinito del Compositore esperienza visivo.

![Impostazioni URL VEC predefinite](/help/c-experiences/c-visual-experience-composer/assets/pref-default-url-new.png)

Questo URL determina la posizione di partenza all&#39;apertura dell&#39;aula virtuale. Se non immetti un URL predefinito, viene inizialmente aperta una pagina vuota e potrai quindi specificare un URL.

>[!NOTE]
>
>Alcuni browser, come Firefox, potrebbero impedire la visualizzazione di una pagina nel VEC se la pagina contiene contenuto misto (ad esempio, una pagina non sicura in un sito protetto). Se la pagina non viene visualizzata, fate clic sull&#39;icona accanto all&#39;URL nella barra degli indirizzi del browser e fate clic **[!UICONTROL su Disattiva protezione in questa pagina]**. Questo problema non influenza la visualizzazione delle pagine da parte dei visitatori del sito.

Il contenuto all&#39;interno di un iframe sulla pagina non può essere modificato nell&#39;aula virtuale. Per modificare il contenuto all&#39;interno di un iframe, accertatevi che il documento iframe sia abilitato per Target, quindi caricate l&#39;URL iframe nell&#39;aula virtuale.

Per un’anteprima della pagina per diversi tipi di pubblico o con altre esperienze, utilizza i menu a discesa nella parte superiore della pagina. Puoi specificare un nome per ogni esperienza nel secondo elenco a discesa. Ad esempio, se stai eseguendo il test della posizione del collegamento Pagina principale nella barra di navigazione, a un’esperienza in cui compare tale collegamento puoi assegnare un nome tipo “Collegamento Pagina principale”, per individuarla più facilmente nell’elenco delle esperienze.

>[!NOTE]
>
>Le modifiche alla struttura di una pagina che influenzano le posizioni utilizzate in un’attività creata in quella pagina potrebbero causare problemi nella modifica dell’esperienza. Se una posizione è stata modificata all&#39;esterno della VEC, Target potrebbe non riuscire a trovare il percorso in cui il contenuto è stato modificato.

Mentre sposti il mouse sulla pagina, una casella sensibile al contesto segue il cursore ed evidenzia gli elementi nella pagina.

![VEC evidenziato](/help/c-experiences/c-visual-experience-composer/assets/vec-highlight-new.png)

Fate clic sull&#39;icona **[!UICONTROL Sovrapposizioni]** per modificare il modo in cui viene visualizzata l&#39;evidenziazione. Ad esempio, potete scegliere di evidenziare solo immagini, collegamenti, mbox regionali, modifiche o javascript. Potete modificare il colore dell&#39;evidenziazione. Puoi inoltre specificare il colore di evidenziazione e il tipo di riempimento da usare per diversi tipi di elementi.

![Modificare le impostazioni di Sovrapposizione](/help/c-experiences/c-visual-experience-composer/assets/change-overlay.png)

Fate clic su un elemento evidenziato per un menu delle opzioni disponibili per il tipo di elemento. Ad esempio, potete fare clic su un&#39;immagine e selezionare **[!UICONTROL Modifica &gt; Testo/HTML]** per modificare il testo, oppure fare clic su un pulsante e modificare il colore dello sfondo. Con i pulsanti in alto a sinistra nella pagina puoi attivare e disattivare le sovrapposizioni.

Puoi inoltre fare clic su **[!UICONTROL Sfoglia]** e passare dalla pagina principale a una pagina disponibile, ad esempio quella di spedizione o del carrello acquisti, ed eseguire da questa il test delle modifiche. Puoi inoltre accedere agli elementi della pagina disponibili, come menu a comparsa e mini-carrelli, passando il puntatore del mouse sopra di essi. Quindi, fai clic su **[!UICONTROL Componi]** per modificare l’esperienza. Ad esempio, puoi modificare la struttura di un elenco a discesa del carrello acquisti o un carosello di immagini.

>[!NOTE]
>
>Se uno stato hover dipende da JavaScript, assicurati che **[!UICONTROL Disabilita JavaScript]** non sia selezionato. Per modificare elementi JavaScript è necessario che JavaScript sia abilitato.

Per informazioni sulle opzioni disponibili nell&#39;aula virtuale, consultate Opzioni [di Visual Experience Composer (Compositore esperienza visivo](../../c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81)).

È possibile eseguire alcune modifiche su una pagina durante il caricamento della pagina (o dopo il caricamento della pagina non riuscita), oppure è possibile annullare il caricamento della pagina nell&#39;aula virtuale. Per ulteriori informazioni, consulta:

* [Modifica di una pagina durante il caricamento della pagina o dopo il caricamento della pagina](#loading)
* [Annullamento del caricamento di una pagina all&#39;interno della VEC](#cancel-loading)

## Modifica di una pagina durante il caricamento della pagina o dopo il caricamento della pagina {#loading}

Potrai eseguire molte azioni prima che la pagina si carichi nel VEC, anche nel caso in cui la pagina non riesca a caricarsi completamente (per esempio, il codice personalizzato non è più operativo).

Alcuni motivi per cui è possibile accedere o apportare modifiche a una pagina durante il caricamento all&#39;interno dell&#39;aula virtuale o dopo il caricamento:

* Desiderate apportare una semplice modifica a una pagina, ad esempio per aggiungere codice personalizzato o modificare il nome di un&#39;esperienza
* Desiderate copiare il codice personalizzato esistente da una pagina non più accessibile
* Una pagina non viene caricata all&#39;interno della VEC, ma si desidera comunque apportare semplici modifiche

Mentre la pagina viene caricata (o dopo il caricamento), il [!UICONTROL pannello Esperienze] , [!UICONTROL le modifiche] e le impostazioni nella parte superiore dell&#39;esperienza (Sovrapposizioni, Modifiche, Configura e così via) sono accessibili.

L&#39;illustrazione seguente mostra che è possibile inserire codice personalizzato o eseguire altre azioni mentre la pagina continua a caricarsi:

![Caricamento della pagina](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/loading-page.png)

## Annullamento del caricamento di una pagina all&#39;interno della VEC {#cancel-loading}

Potete annullare il caricamento di una pagina all&#39;interno della VEC per sbloccare la modifica dell&#39;attività senza attendere che la pagina venga caricata. Questa funzione consente di risparmiare tempo e di apportare semplici modifiche o di inserire codice personalizzato in modo più efficace, senza attendere che la pagina venga caricata all&#39;interno della VEC.

Alcuni motivi per cui potrebbe essere utile annullare il caricamento della pagina all&#39;interno dell&#39;aula virtuale:

* Apportare modifiche minori alle modifiche esistenti
* Eliminare una o più modifiche esistenti
* Desiderate inserire o modificare il codice personalizzato
* Hai immesso erroneamente l&#39;URL errato per la pagina
* Per abilitare o disabilitare javascript prima di caricare la pagina in Aula virtuale
* Desiderate aggiungere ulteriori regole di test dei modelli ai criteri di consegna delle pagine
* Si desidera ignorare l&#39;attivazione (Modifica avanzata) globale di Experience Composer (Compositore esperienza avanzata) quando si carica una pagina tramite l&#39;iframe o solo l&#39;iframe potrebbe variare a seconda della pagina

Dopo aver annullato il caricamento della pagina nella VEC, potete passare alle diverse esperienze nell&#39;attività senza attendere che la pagina venga caricata. Per visualizzare nuovamente la pagina all&#39;interno della VEC, fare clic sul **[!UICONTOL pulsante Ricarica]** .

>[!IMPORTANT]
>
>Tenete presente che quando effettuate il codice personalizzato o eventuali modifiche, scegliendo di annullare il caricamento all&#39;interno della VEC, dovete verificare che la codifica o le modifiche vengano eseguite correttamente. Assicurati di eseguire una QA appropriata per assicurare che il codice personalizzato e qualsiasi altra modifica vengano consegnati come previsto.

Per annullare il caricamento di una pagina all&#39;interno della VEC, fate clic sul pulsante **[!UICONTROL Annulla caricamento]** durante il caricamento della pagina. La pagina non viene caricata nell&#39;aula virtuale per questa attività durante la sessione di modifica corrente.

![Pulsante Annulla caricamento](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/cancel-loading.png)

Per continuare a gestire le esperienze nell&#39;attività corrente o per aggiungere nuove modifiche, fate clic sul **[!UICONTROL pulsante Ricarica]** .

![Pulsante Ricarica](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/reload-in-vec.png)

>[!NOTE]
>
>Esiste un problema noto corrente con questa funzione che verrà risolta nella prossima release. Per ulteriori informazioni, consultate &quot;Annulla caricamento di una pagina all&#39;interno della VEC&quot; sui problemi [noti e sulla pagina dei problemi](/help/r-release-notes/known-issues-resolved-issues.md#cancel) risolti.

## Video di formazione

I video seguenti contengono ulteriori informazioni sui concetti descritti in questo articolo.

### Compositore esperienza visivo (07:17)

Questo video fornisce informazioni sull’utilizzo delle opzioni del Compositore esperienza visivo.

* Modificare il contenuto di una pagina
* Modificare il layout di una pagina

>[!VIDEO](https://video.tv.adobe.com/v/17399)

### Compositore esperienza visivo (1 di 2) (7:17)

* Modificare il contenuto di una pagina
* Modificare il layout di una pagina

>[!VIDEO](https://video.tv.adobe.com/v/17399)

### Compositore esperienza visivo (2 di 2) (7:29)

* Rinominare e duplicare un’esperienza
* Creare un’esperienza con reindirizzamento
* Indirizzare un’attività a un singolo URL o a un gruppo di URL
* Creare un’attività multipagina
* Creare un’esperienza e visualizzarne l’anteprima per i siti web reattivi
* Evidenziare tipi di elementi con le sovrapposizioni

>[!VIDEO](https://video.tv.adobe.com/v/17401)

### Office Hours: Compositore esperienza visivo

Questo video è una registrazione di “ [Office Hours](../../cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7)”, un’iniziativa condotta dal team di assistenza clienti Adobe.

* Funzionamento del Compositore esperienza visivo
* Come evitare i problemi più comuni con Compositore esperienza visivo
* Procedure utili che puoi utilizzare con Compositore esperienza visivo

>[!VIDEO](https://video.tv.adobe.com/v/20784/)