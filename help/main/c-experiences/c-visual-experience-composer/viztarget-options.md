---
keywords: opzioni compositore esperienza visivo;opzioni compositore esperienza;opzioni esperienza;modifica testo;modifica html;modifica testo/html;modifica colore di sfondo;colore di sfondo;inserire elemento;modifica collegamento;collegamento;collegamento;collegamento compositore esperienza visivo;modifica classe css;classe css;sostituire offerta;scambiare immagine;scambiare immagine;rimuovere elemento;rimuovere elemento;elemento rimuovere;nascondere elemento;nascondere elemento;ridisporre;spostare elemento;spostare elemento;ridimensionare elemento;ridimensionare elemento;elemento;espandere la selezione;passare a questo collegamento;passare al collegamento;passare al collegamento;navigare;passare;collegamento;annullare;ripetere;annullare/ripetere;eventi personalizzati;componenti web;decisione offerta;offer decisioning
description: Esplora le opzioni disponibili nel  [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC).
title: Come si utilizzano le opzioni [!UICONTROL Visual Experience Composer] (VEC)?
feature: Visual Experience Composer (VEC)
exl-id: 50993d6c-5025-488a-8b33-9ed7c142de6e
source-git-commit: 2fc704a1779414a370ffd00ef5442fce36e7a5dd
workflow-type: tm+mt
source-wordcount: '2667'
ht-degree: 55%

---

# Opzioni del Compositore esperienza visivo

Quando si fa clic su un elemento di pagina nel [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC), un menu mostra le opzioni disponibili per tale tipo di elemento. Inoltre, nella parte inferiore della pagina viene visualizzato un percorso DOM che consente di navigare facilmente nella struttura della pagina.

Le varie azioni di [!UICONTROL Visual Experience Composer] (VEC) sono raggruppate nelle opzioni di menu appropriate per rendere il processo più veloce ed efficiente:

![Menu delle opzioni del Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/vec-options.png)

>[!NOTE]
>
>Le opzioni disponibili dipendono dal tipo di attività che si sta creando o modificando.

## [!UICONTROL Edit]

Sono disponibili le seguenti opzioni:

### [!UICONTROL Text/HTML] {#edit-text-html}

Modifica il codice HTML per l&#39;elemento, ad esempio il testo per un&#39;area di testo, un pulsante o collegamento.

Oltre al codice HTML, puoi modificare e inserire codice JavaScript personalizzato.

Sono disponibili diverse opzioni di formattazione per modificare testo e HTML per le attività [!UICONTROL A/B] e [!UICONTROL Experience Targeting]. Puoi scegliere font e stile, l’allineamento del testo e altre opzioni standard per la formattazione del testo. Quando modifichi l’HTML, puoi passare dalla visualizzazione del codice alla visualizzazione per modifica Rich Text dell’HTML.

I seguenti tag HTML5 possono essere nidificati:

| Tag | Tag nidificati consentiti |
| --- | --- |
| `<a>` | `<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>`, `<div>`, `<figure>`, `<figcaption>` |
| `<ins>` | `<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>` |
| `<del>` | `<ul>`, `<ol>`, `<menu>`, `<h1-h6>`, `<p>` |
| `<label>` | `<p>` |

### [!UICONTROL Background Color]

Utilizza il settore colori per selezionare o configurare un colore di sfondo. È possibile selezionare un campione di colore e regolarlo utilizzando i valori RGB o i codici esadecimali. La x rossa nel selettore colore rende lo sfondo trasparente.

**Nota**: questa opzione non è disponibile se è impostata un’immagine di sfondo.

### [!UICONTROL Styles] {#styles}

Utilizzare il pannello [!UICONTROL Styles] per visualizzare o modificare il valore degli stili esistenti per l&#39;elemento selezionato. Inoltre, è possibile aggiungere ulteriore formattazione.

Per accedere al pannello [!UICONTROL Styles], fai clic su un elemento di pagina nel Compositore esperienza visivo, quindi su **[!UICONTROL Edit]** > **[!UICONTROL Styles]**.

Il pannello [!UICONTROL Styles] viene visualizzato sul lato destro del Compositore esperienza visivo. Il pannello contiene un elenco di stili che consente di modificare o aggiungere formattazione all’elemento selezionato. Se hai familiarità con l’utilizzo di Cascading Style Sheet (CSS) o se ricevi del codice dallo sviluppatore, un editor CSS in tempo reale consente di visualizzare le modifiche e aggiungere stili.

![Pannello Stili](/help/main/c-experiences/c-visual-experience-composer/assets/styles-panel-new.png)

Quando si applicano stili diversi, è sempre possibile ripristinare le modifiche facendo clic sull&#39;icona [!UICONTROL Revert] visualizzata nell&#39;angolo in alto a destra del pannello [!UICONTROL Styles] dopo aver modificato una sezione. Facendo clic sull&#39;icona [!UICONTROL Revert] vengono ripristinate tutte le modifiche nel pannello della sezione corrente.

Espandi ogni sezione per modificare o aggiungere stili, come descritto di seguito. Per salvare le modifiche, fai clic sull&#39;icona [!UICONTROL Back] nella parte superiore del pannello per tornare alla visualizzazione principale del pannello, quindi fai clic su **[!UICONTROL Save]**.

I punti blu nel pannello principale e accanto a ogni opzione nei vari pannelli di sezione indicano che sono stati modificati gli stili corrispondenti. Questo indicatore visivo semplifica la revisione delle modifiche prima di fare clic su [!UICONTROL Save].

>[!NOTE]
>
>Le azioni rapide per le modifiche di layout, il colore di sfondo, il ridimensionamento e lo spostamento sono disponibili anche come azioni separate nel menu del Compositore esperienza visivo. Queste opzioni possono essere utilizzate come azioni separate oppure puoi utilizzare il menu Stili, come spiegato qui.

* **[!UICONTROL Background]**

  Cambia il colore e l’immagine di sfondo.

   * Colore (specifica il codice del colore o utilizza il selettore del colore)
   * Immagine (seleziona un’immagine dal selettore immagini)
   * Origine immagine (specifica un URL esterno)
   * Allegato
      * Fai clic sull’elenco a discesa in alto per selezionare scroll, fixed o local (Scorrimento, Fisso o Locale).
      * Fai clic sull’elenco a discesa in alto per selezionare repeat, repeat-x, repeat-y, no-repeat, space o round (Ripeti, Ripeti x, Ripeti y, Non ripetere, Spazio, Arrotonda).
   * Clip
      * Fai clic sull’elenco a discesa in alto per selezionare border-box, padding-box, content-box o text (Casella bordo, Casella margine, Casella contenuto, Testo).
      * Fai clic sull’elenco a discesa in alto per selezionare auto audio o audio (Audio automatico, Audio).

* **[!UICONTROL Typography]**

  Puoi modificare la composizione tipografica di un elemento. Le modifiche tipografiche sono semplici e veloci.

  Anche se l’editor Rich Text (Modifica testo/HTML) è disponibile per eseguire regolazioni precise, questa opzione consente di accedere ad azioni rapide per modificare l’intero elemento. Se desideri applicare modifiche di composizione tipografica a una sola parte del testo (non al testo completo), utilizza l’[editor Rich Text](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md).

  È possibile modificare i seguenti stili di composizione tipografica:

   * [!UICONTROL Font size]
   * [!UICONTROL Font weight]
   * [!UICONTROL Font style]
   * [!UICONTROL Color] (specificare il codice colore o utilizzare il selettore colore)
   * [!UICONTROL Word spacing]
   * [!UICONTROL Line height]
   * [!UICONTROL Text alignment]

* **[!UICONTROL Margin]**

  Modifica il margine dell’elemento selezionato. È possibile modificare il margine sinistro, destro, inferiore e superiore.

  Fai clic sull’icona a discesa di ciascun margine per scegliere tra le opzioni seguenti:

   * [!UICONTROL Auto]
   * [!UICONTROL Value] (trascina il cursore per impostare il margine o specifica il numero di pixel per ciascun margine)

  Il margine supporta valori positivi e negativi.

  Target supporta anche altre unità di misura, come rem, pc, em. Per ulteriori informazioni su queste unità, vedere [Suggerimenti e trucchi per i fogli di stile Web CSS](https://www.w3.org/Style/Examples/007/units.en.html).

* **[!UICONTROL Padding]**

  Modifica la spaziatura per l’elemento selezionato. È possibile modificare la spaziatura sinistra, destra, inferiore e superiore.

  Trascina il cursore per impostare la spaziatura o specifica il numero di pixel da applicare alla spaziatura.

  La spaziatura supporta valori di larghezza a partire da 0.

  Target supporta anche [altre unità di misura](https://www.w3.org/Style/Examples/007/units.en.html), ad esempio rem, pc, em.

* **[!UICONTROL Border]**

  Fai clic sulle icone dei bordi nella parte superiore del pannello per modificare il bordo dell’elemento selezionato.

  È possibile modificare i seguenti stili per ciascun bordo (superiore, destro, inferiore e sinistro):

   * [!UICONTROL Border style] (nessuno, nascosto, punteggiato, tratteggiato, pieno o doppio)
   * [!UICONTROL Border color] (specificare il codice colore o utilizzare il selettore colore)
   * [!UICONTROL Border width] (trascina il cursore per selezionare lo spessore di un bordo o specifica lo spessore in pixel)

  Il bordo supporta valori di spessore a partire da 0.

  Target supporta anche [altre unità di misura](https://www.w3.org/Style/Examples/007/units.en.html), ad esempio rem, pc, em.

* **[!UICONTROL Position]**

  Sposta l’elemento selezionato dalla posizione corrente. È possibile modificare la posizione superiore, inferiore, sinistra, destra e [indice Z](https://www.w3schools.com/cssref/pr_pos_z-index.asp) dell&#39;elemento.

  Fare clic sull&#39;elenco a discesa [!UICONTROL Static] per scegliere tra le seguenti opzioni di posizione:

   * [!UICONTROL Static]
   * [!UICONTROL Relative]
   * [!UICONTROL Absolute]
   * [!UICONTROL Sticky]
   * [!UICONTROL Fixed]

  Fai clic sull’icona a discesa per ciascuna posizione per scegliere tra le seguenti opzioni:

   * [!UICONTROL Auto]
   * [!UICONTROL Value] (trascina il cursore per posizionare l&#39;elemento o specifica il numero di pixel da spostare)

  La posizione supporta valori positivi e negativi.

  Target supporta anche [altre unità di misura](https://www.w3.org/Style/Examples/007/units.en.html), ad esempio rem, pc, em.

* **[!UICONTROL Size]**

  Modifica la larghezza e l’altezza dell’elemento selezionato.

  Fai clic sull&#39;icona a discesa accanto a [!UICONTROL Width] e [!UICONTROL Height] per scegliere tra le seguenti opzioni:

   * [!UICONTROL Auto]
   * [!UICONTROL Value] (trascina il cursore per ridimensionare l&#39;elemento o specifica il numero di pixel per ogni dimensione)

* **[!UICONTROL Filter]**

  Trascina il cursore per ogni opzione filtro o specifica la percentuale desiderata:

   * [!UICONTROL Sepia]
   * [!UICONTROL Contrast]
   * [!UICONTROL Brightness]
   * [!UICONTROL GrayScale]
   * [!UICONTROL Blur]
   * [!UICONTROL Opacity]
   * [!UICONTROL Invert]
*[!UICONTROL  Hue-rotate]
   * [!UICONTROL Saturate]

* **[!UICONTROL CSS Editor]**

  Se hai familiarità con l’utilizzo di Cascading Style Sheet (CSS) o se ricevi del codice dallo sviluppatore, l’editor CSS in tempo reale consente di visualizzare le modifiche e aggiungere stili.

  L’Editor CSS visualizza le modifiche apportate nel pannello Stili. Come mostrato nell’illustrazione seguente, sono state modificate le dimensioni del font, il bordo superiore e le dimensioni dell’immagine:

  ![Editor CSS con modifiche](/help/main/c-experiences/c-visual-experience-composer/assets/css-changes.png)

  Osserva i punti blu accanto alle opzioni [!UICONTROL Typography], [!UICONTROL Border] e [!UICONTROL Size] nell&#39;illustrazione precedente. Questi punti indicano che le sezioni sono state modificate. Se apri questi pannelli di sezione, i punti blu vengono visualizzati accanto alle opzioni modificate.

  Se lo stile desiderato non è disponibile per impostazione predefinita in [!UICONTROL Styles], è possibile digitare il codice desiderato.

  L’editor CSS mostra i dettagli solo per la sessione corrente. Se salvi le modifiche e quindi riapri l’editor, i dettagli relativi alla modifica precedente non vengono visualizzati nell’editor, anche se selezioni di nuovo lo stesso elemento.

  >[!IMPORTANT]
  >
  >È possibile applicare un’immagine di sfondo utilizzando l’Editor CSS, ma potrebbe causare sfarfallii. Verifica le modifiche prima di implementarle.

### [!UICONTROL CSS Class]

Specifica la classe CSS predefinita utilizzata per l’elemento. Se vengono selezionati più elementi, separa le classi CSS con uno spazio.

Disponibile per [!UICONTROL A/B], [!UICONTROL Automated Personalization] e [!UICONTROL Multivariate Test] attività.

### [!UICONTROL Link]

Modifica l’URL nel collegamento.

Utilizza Modifica collegamento per aggiornare il selettore in modo che indirizzi allo stesso elemento immagine. Tuttavia, il collegamento a un elemento immagine diverso non è supportato. Per collegare un elemento immagine diverso, eliminare l&#39;azione originale dall&#39;editor di codice e utilizzare [!UICONTROL Visual Experience Composer] per applicare l&#39;azione all&#39;altro elemento immagine.

## [!UICONTROL Insert Before]

Sono disponibili le seguenti opzioni:

### [!UICONTROL Offer Decision]

Aggiungi un&#39;offerta [creata in [!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioniong/get-started/starting-offer-decisioning.html){target=_blank} per presentare ai clienti l&#39;offerta e l&#39;esperienza migliore utilizzando offer decisioning.

**Nota:** questa opzione è disponibile solo per la modifica o la creazione di [attività manuali [!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md#types) o [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md) (XT). Questa opzione non è disponibile per altri tipi di attività.

Per ulteriori informazioni, consulta [Utilizzare le decisioni sulle offerte](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md).

### [!UICONTROL Image], [!UICONTROL HTML] e [!UICONTROL Text]

Consente di aggiungere qualsiasi tipo di elemento alla pagina, e di modificare il contenuto esistente. Puoi aggiungere testo, codice, elenchi e così via per creare esperienze diverse da testare.

Selezionare un elemento nella pagina, quindi fare clic su [!UICONTROL Insert Before] e scegliere se si desidera inserire un&#39;immagine, un HTML o un testo. L’elemento inserito viene visualizzato prima dell’elemento selezionato.

Il comportamento dell’elemento inserito dipende dalla struttura della pagina, dal CSS e da altre opzioni di configurazione della pagina. Per la corretta visualizzazione della pagina è necessario un codice HTML valido. Verifica sempre la pagina dopo l’inserimento di un elemento per essere certo che venga visualizzata come previsto.

[!UICONTROL Recommendations] supporta [!UICONTROL Insert Before] il contenuto dei tag DIV, SECTION e ARTICLE.

**Nota:** l’inserimento di un’immagine richiede che [!DNL Adobe Scene7 Publishing System] sia attivato, in modo da avere accesso alla libreria delle immagini.

### Consiglio

Includi consigli all’interno di attività di test A/B (tra cui Allocazione automatica e Targeting automatico) e targeting delle esperienze (XT). Per ulteriori informazioni, consulta [Consigli come offerta](/help/main/c-recommendations/recommendations-as-an-offer.md).

### [!UICONTROL Experience Fragment]

Inserisci frammenti esperienza creati in [!DNL Adobe Experience Manager] (AEM) nelle attività di [!DNL Target] per aiutare l’ottimizzazione o la personalizzazione. Per ulteriori informazioni, consulta [Frammenti esperienza AEM](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md).

## [!UICONTROL Insert After]

Sono disponibili le seguenti opzioni:

### [!UICONTROL Offer Decision]

Aggiungi un&#39;offerta [creata in [!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioniong/get-started/starting-offer-decisioning.html){target=_blank} per presentare ai clienti l&#39;offerta e l&#39;esperienza migliore utilizzando offer decisioning.

**Nota:** questa opzione è disponibile solo per la modifica o la creazione di [attività manuali [!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md#types) o [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md) (XT). Questa opzione non è disponibile per altri tipi di attività.

Per ulteriori informazioni, consulta [Utilizzare le decisioni sulle offerte](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md).

### [!UICONTROL Image], [!UICONTROL HTML] e [!UICONTROL Text]

Consente di aggiungere qualsiasi tipo di elemento alla pagina, e di modificare il contenuto esistente. Puoi aggiungere testo, codice, elenchi e così via per creare esperienze diverse da testare.

Selezionare un elemento nella pagina, quindi fare clic su [!UICONTROL Insert After] e scegliere se si desidera inserire un&#39;immagine, un HTML o un testo. L’elemento inserito viene visualizzato dopo l’elemento selezionato.

Il comportamento dell’elemento inserito dipende dalla struttura della pagina, dal CSS e da altre opzioni di configurazione della pagina. Per la corretta visualizzazione della pagina è necessario un codice HTML valido. Verifica sempre la pagina dopo l’inserimento di un elemento per essere certo che venga visualizzata come previsto.

[!UICONTROL Recommendations] supporta [!UICONTROL Insert After] il contenuto dei tag DIV, SECTION e ARTICLE.

**Nota:** l’inserimento di un’immagine richiede che [!DNL Adobe Scene7 Publishing System] sia attivato, in modo da avere accesso alla libreria delle immagini.

### Consiglio

Includi consigli all’interno di attività di test A/B (tra cui Allocazione automatica e Targeting automatico) e targeting delle esperienze (XT). Per ulteriori informazioni, consulta [Consigli come offerta](/help/main/c-recommendations/recommendations-as-an-offer.md).

### [!UICONTROL Experience Fragment]

Inserisci frammenti esperienza creati in [!DNL Adobe Experience Manager] (AEM) nelle attività di [!DNL Target] per aiutare l’ottimizzazione o la personalizzazione. Per ulteriori informazioni, consulta [Frammenti esperienza AEM](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md).

## [!UICONTROL Replace Content]

Sono disponibili le seguenti opzioni:

### [!UICONTROL Offer Decision]

Aggiungi un&#39;offerta [creata in [!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioniong/get-started/starting-offer-decisioning.html){target=_blank} per presentare ai clienti l&#39;offerta e l&#39;esperienza migliore utilizzando offer decisioning.

**Nota:** questa opzione è disponibile solo per la modifica o la creazione di [attività manuali [!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md#types) o [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md) (XT). Questa opzione non è disponibile per altri tipi di attività.

Per ulteriori informazioni, consulta [Utilizzare le decisioni sulle offerte](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md).

### [!UICONTROL Image]

Consente di selezionare una diversa immagine dalla libreria Contenuto. Le immagini disponibili per la sostituzione includono le immagini caricate nella cartella delle risorse di Experience Cloud o nella libreria di contenuti in Target.

Durante la creazione dell’attività iniziale, l’URL visualizzato non è l’URL utilizzato per la consegna. Dopo l’attività di sincronizzazione, tale URL viene aggiornato a un URL Scene7 di produzione.

Ad esempio, l’URL iniziale potrebbe essere simile all’esempio seguente:

`https://test.marketing.adobe.com/content/dam/mac/scholasticinc/Aug_MBM.jpeg?ch_ck=1470774943867`

Dopo la sincronizzazione dell’attività, l’URL di consegna potrebbe essere simile al seguente:

`http://s7d2.scene7.com/is/image/TargetTest/Aug_MBM?tm=1470768352933&fit=constrain&hei=173&wid=300`

La funzione Consigli supporta la funzione Sostituisci con nei tag DIV, SECTION e ARTICLE.

**Nota:** lo scambio delle immagini richiede un account Adobe Scene7 Publishing System.

### [!UICONTROL HTML Offer]

Selezionare un&#39;offerta diversa da [!UICONTROL Content Library].

**Nota:**[!DNL Target] le offerte HTML sono memorizzate sui server di

Un’offerta HTML può avere una dimensione massima di 256 KB.

### Consiglio

Includi consigli all’interno di attività di test A/B (tra cui Allocazione automatica e Targeting automatico) e targeting delle esperienze (XT). Per ulteriori informazioni, consulta [Consigli come offerta](/help/main/c-recommendations/recommendations-as-an-offer.md).

### [!UICONTROL Experience Fragment]

Inserisci frammenti esperienza creati in [!DNL Adobe Experience Manager] (AEM) nelle attività di [!DNL Target] per aiutare l’ottimizzazione o la personalizzazione. Per ulteriori informazioni, consulta [Frammenti esperienza AEM](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md).

## [!UICONTROL Layout]

Sono disponibili le seguenti opzioni:

### [!UICONTROL Rearrange]

Trascina l’elemento in un’altra posizione nello stesso elemento padre o DIV. Gli altri elementi vengono spostati per fare spazio all’elemento ridisposto.

**Nota**: il tracciamento dei clic non funziona sugli elementi ridisposti.

Attualmente, alcune azioni del Compositore esperienza visivo, come [!UICONTROL Rearrange] e [!UICONTROL Move], presuppongono che gli elementi di pari livello degli elementi padre di origine e di destinazione siano completamente caricati. Se si verifica un caricamento lento sotto gli elementi DOM principali (sorgente o destinazione), queste azioni del Compositore esperienza visivo possono causare un comportamento incoerente. Stiamo lavorando a un approccio più affidabile per far funzionare le azioni del Compositore esperienza visivo in elementi DOM caricati lentamente. Come soluzione alternativa temporanea, puoi utilizzare [!UICONTROL Custom Code] in questi scenari per eseguire il rendering delle esperienze.

### [!UICONTROL Resize]

Consente di ridimensionare un elemento nella pagina. Quando si seleziona [!UICONTROL Resize], nell&#39;angolo inferiore destro dell&#39;elemento viene visualizzato un quadratino che consente di trascinare l&#39;angolo per ridimensionarlo. Tieni premuto il tasto Maiusc per mantenere le stesse proporzioni.

**Nota:** gli elementi in linea non possono essere ridimensionati.

### [!UICONTROL Move] {#move}

Consnete di spostare gli elementi nella pagina. A differenza dell&#39;opzione [!UICONTROL Rearrange], [!UICONTROL Move] non sposta altri elementi per lasciare spazio all&#39;elemento da spostare. Utilizza i tasti freccia per regolare meglio lo spostamento. (Miglioramento pianificato: supporto per garantire che gli elementi spostati non siano nascosti dietro altri elementi.)

In alcune situazioni, ad esempio quando una limitazione CSS richiede che un elemento resti all’interno del suo elemento padre, non puoi spostare l’elemento al di fuori di quest’ultimo. Un elemento non può essere spostato all’esterno di un contenitore seguito dalla proprietà CSS `overflow: hidden`.

Vedere [!UICONTROL Rearrange] sopra per ulteriori informazioni sul comportamento incoerente con le azioni [!UICONTROL Move] e [!UICONTROL Rearrange] a causa del caricamento lento degli elementi DOM.

### [!UICONTROL Hide]

Consnete di nascondere l’elemento. Lo spazio vuoto viene conservato, ma il contenuto viene rimosso.

### [!UICONTROL Remove]

Rimuovi l’elemento. Lo spazio vuoto dietro l&#39;immagine viene rimosso e lo spazio in cui l&#39;elemento si trovava viene compresso.

**Nota:** gli elementi di una mbox classica (una mbox creata in una campagna di Target Classic) non possono essere rimossi con questa opzione.

## [!UICONTROL Expand Section]

Consente di selezionare l’elemento padre in aggiunta all’elemento selezionato originariamente. Quando selezioni un elemento padre, tutti i relativi figli vengono selezionati automaticamente. Puoi espandere la selezione più volte.

## [!UICONTROL Navigate to Link]

Consente di aprire la destinazione del collegamento.

## [!UICONTROL Undo]/[!UICONTROL Redo]

Annulla le modifiche apportate alle attività durante una sessione di modifica. Puoi inoltre ripristinare le modifiche precedentemente annullate.

## Considerazioni {#considerations}

* Se un&#39;offerta contiene contenuti HTML, consulta la sezione su come avviene il rendering delle offerte con contenuti HTML in [Funzionamento di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/at-js/how-atjs-works.html){target=_blank} per ulteriori informazioni.

## Supporto per elementi personalizzati {#custom}

Il Compositore esperienza visivo supporta [Componenti Web](https://developer.mozilla.org/en-US/docs/Web/Web_Components) per consentire di creare e testare offerte ed esperienze personalizzate su elementi personalizzati e su elementi al loro interno. Questa funzionalità è disponibile nel Compositore esperienza visivo per tutti i tipi di attività [!DNL Target].

>[!NOTE]
>
>Il supporto VEC per gli elementi personalizzati è supportato in [at.js versione](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} 2.7.0 (o successiva){target=_blank}. Verifica che sul tuo sito web sia installata la versione richiesta. Se utilizzi l&#39;estensione helper [Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md), è necessario distribuire anche la versione richiesta di at.js. Le opzioni del Compositore esperienza visivo descritte in precedenza non sono visibili e sono disponibili per l’utilizzo con le versioni non supportate di at.js.
>
>Il supporto VEC per gli elementi personalizzati non è attualmente supportato con [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=it){target=_blank}.

La maggior parte delle azioni del Compositore esperienza visivo è supportata su eventi personalizzati e all’interno di eventi personalizzati, con le seguenti eccezioni:

Le seguenti azioni non sono disponibili sugli elementi personalizzati:

* [!UICONTROL Edit]
   * [!UICONTROL Text/HTML]
   * [!UICONTROL Link]
   * [!UICONTROL Edit Source]

* [!UICONTROL Replace Content]

La seguente azione non è disponibile all’interno di elementi personalizzati:

* [!UICONTROL Layout]
   * [!UICONTROL Rearrange]

## Navigare tra gli elementi utilizzando il percorso DOM {#dom-path}

Facendo clic su un elemento della pagina, viene visualizzato il menu delle opzioni del Compositore esperienza visivo. Inoltre, quando fai clic su un elemento, il percorso DOM corrispondente viene visualizzato nella parte inferiore della pagina.

![Percorso DOM](/help/main/c-experiences/c-visual-experience-composer/assets/dom-path.png)

Puoi utilizzare il percorso DOM per vedere rapidamente le informazioni sull’elemento selezionato (tipo, ID e classe) e spostarti verso l’alto o il basso nel percorso DOM per selezionare l’elemento desiderato.

Quando passi il cursore del mouse sul percorso DOM, una casella blu evidenzia l’elemento corrispondente nel Compositore esperienza visivo. Se fai clic sull’elemento, una casella arancione evidenzia l’elemento e viene visualizzato il menu delle opzioni del Compositore esperienza visivo, come illustrato in precedenza.

Utilizzando il percorso DOM, è possibile passare facilmente a qualsiasi elemento principale, di pari livello o secondario all’interno del Compositore esperienza visivo.

La funzione Percorso DOM è disponibile anche quando si imposta il [tracciamento dei clic](/help/main/c-activities/r-success-metrics/click-tracking.md).
