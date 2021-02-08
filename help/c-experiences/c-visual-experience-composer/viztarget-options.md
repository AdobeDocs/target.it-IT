---
keywords: opzioni compositore esperienza visivo;opzioni compositore esperienza;opzioni esperienza;modifica testo;modifica HTML;modifica testo/HTML;modifica colore di sfondo;colore di sfondo;inserisci elemento;modifica collegamento;collegamento;link;collegamento al compositore esperienza visivo;modifica classe CSS;classe CSS;sostituire l’offerta;sostituisci l’offerta;scambiare immagine;scambia immagine;rimuovere elemento;rimuovi elemento;nascondere una voce;nascondi voce;riorganizzare;spostare elemento;sposta elemento;ridimensionare elemento;ridimensiona elemento;elemento;espandere la selezione;passa a questo collegamento;passare a un link;passa a un link;navigare;annullare;ripeti;annulla/ripristina
description: Esplorate le opzioni disponibili in  Adobe Target Visual Experience Composer (VEC). È sufficiente fare clic su un elemento per vedere quali opzioni sono disponibili per tale elemento.
title: Come si utilizzano le opzioni di Visual Experience Composer (VEC)?
feature: Visual Experience Composer (VEC)
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '2480'
ht-degree: 93%

---


# Opzioni del Compositore esperienza visivo

Quando fate clic su un elemento di pagina in [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC), un menu mostra le opzioni disponibili per quel tipo di elemento. Inoltre, nella parte inferiore della pagina viene visualizzato un percorso DOM che consente di navigare facilmente nella struttura della pagina.

## Opzioni del Compositore esperienza visivo

Le varie azioni del Compositore esperienza visivo sono disponibili come opzioni di menu raggruppate per rendere il processo più veloce ed efficiente:

![Menu delle opzioni del Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/vec-options.png)

>[!NOTE]
>
>Le opzioni disponibili dipendono dal tipo di attività che si sta modificando.

### Modifica

Sono disponibili le seguenti opzioni:

#### Testo/HTML {#edit-text-html}

Modifica il codice HTML per l&#39;elemento, ad esempio il testo per un&#39;area di testo, un pulsante o collegamento.

Oltre al codice HTML, puoi modificare e inserire codice JavaScript personalizzato.

Sono disponibili opzioni di formattazione per modificare il testo e contenuti HTML per le attività [!UICONTROL A/B] e [!UICONTROL Targeting esperienza]. Puoi scegliere font e stile, l’allineamento del testo e altre opzioni standard per la formattazione del testo. Quando modifichi l’HTML, puoi passare dalla visualizzazione del codice alla visualizzazione per modifica Rich Text dell’HTML.

I seguenti tag HTML5 possono essere nidificati:

| Tag | Tag nidificati consentiti |
| --- | --- |
| `<a>` | `<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>`, `<div>`, `<figure>`, `<figcaption>` |
| `<ins>` | `<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>` |
| `<del>` | `<ul>`,  `<ol>`,  `<menu>`,  `<h1-h6>`,  `<p>` |
| `<label>` | `<p>` |

#### Colore di sfondo

Utilizza il settore colori per selezionare o configurare un colore di sfondo. È possibile selezionare un campione di colore e regolarlo utilizzando i valori RGB o i codici esadecimali. La x rossa nel selettore colore rende lo sfondo trasparente.

**Nota**: questa opzione non è disponibile se è impostata un’immagine di sfondo.

#### Stili {#styles}

Il pannello [!UICONTROL Stili] consente di visualizzare o modificare il valore degli stili esistenti per l’elemento selezionato. Inoltre, è possibile aggiungere ulteriore formattazione.

Per accedere al pannello [!UICONTROL Stili], fare clic su un elemento di pagina all&#39;interno del VEC, quindi fare clic su **[!UICONTROL Modifica]** > **[!UICONTROL Stili]**.

Il pannello [!UICONTROL Stili] viene visualizzato sul lato destro del Compositore esperienza visivo. Il pannello contiene un elenco di stili che consente di modificare o aggiungere formattazione all’elemento selezionato. Se hai familiarità con l’utilizzo di Cascading Style Sheet (CSS) o se ricevi del codice dallo sviluppatore, un editor CSS in tempo reale consente di visualizzare le modifiche e aggiungere stili.

![Pannello Stili](/help/c-experiences/c-visual-experience-composer/assets/styles-panel-new.png)

Quando si applicano stili diversi, è sempre possibile ripristinare le modifiche facendo clic sull’icona [!UICONTROL Ripristina] in alto a destra nel pannello [!UICONTROL Stili], dopo aver apportato una modifica a una sezione. Considera che facendo clic sull’icona [!UICONTROL Ripristina], vengono ripristinate tutte le modifiche nel pannello della sezione corrente.

Espandi ogni sezione per modificare o aggiungere stili, come descritto di seguito. Per salvare le modifiche, fai clic sull’icona Indietro nella parte superiore del pannello per tornare alla visualizzazione principale del pannello, quindi fai clic su **[!UICONTROL Salva]**.

I punti blu nel pannello principale e accanto a ogni opzione nei vari pannelli di sezione indicano che sono state apportate modifiche agli stili corrispondenti. In questo modo è facile rivedere le modifiche prima di fare clic su [!UICONTROL Salva].

>[!NOTE]
>
>Le azioni rapide per le modifiche di layout, il colore di sfondo, il ridimensionamento e lo spostamento sono disponibili anche come azioni separate nel menu del Compositore esperienza visivo. Queste opzioni possono essere utilizzate come azioni separate oppure puoi usare il menu Stili, come spiegato qui.

* **Sfondo**

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

* **Composizione tipografica**

   Puoi modificare la composizione tipografica di un elemento. Le modifiche tipografiche sono semplici e veloci.

   Anche se l’editor Rich Text (Modifica testo/HTML) è disponibile per eseguire regolazioni precise, questa opzione permette di usare azioni rapide per apportare modifiche all’intero elemento. Se desideri applicare modifiche di composizione tipografica a una sola parte del testo (non al testo completo), utilizza l’[editor Rich Text](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md).

   È possibile modificare i seguenti stili di composizione tipografica:

   * Dimensione font
   * Spessore font
   * Stile font
   * Colore (specifica il codice del colore o utilizza il selettore del colore)
   * Spaziatura tra parole
   * Altezza riga
   * Allineamento testo

* **Margine**

   Modifica il margine dell’elemento selezionato. È possibile modificare il margine sinistro, destro, inferiore e superiore.

   Fai clic sull’icona a discesa di ciascun margine per scegliere tra le opzioni seguenti:

   * Automatico
   * Valore (trascina il cursore per impostare il margine o specifica il numero di pixel per ciascun margine)

   Il margine supporta valori positivi e negativi.

   Target supporta anche altre unità di misura, come rem, pc, em ecc. Per ulteriori informazioni su queste unità, vedere [Suggerimenti e trucchi CSS per i fogli di stile Web](https://www.w3.org/Style/Examples/007/units.en.html).

* **Spaziatura**

   Modifica la spaziatura per l’elemento selezionato. È possibile modificare la spaziatura sinistra, destra, inferiore e superiore.

   Trascina il cursore per impostare la spaziatura o specifica il numero di pixel da applicare alla spaziatura.

   La spaziatura supporta valori di larghezza a partire da 0.

   Target supporta anche [altre unità di dimensione](https://www.w3.org/Style/Examples/007/units.en.html), come rem, pc, em, ecc.

* **Bordo**

   Fai clic sulle icone dei bordi nella parte superiore del pannello per modificare il bordo dell’elemento selezionato.

   È possibile modificare i seguenti stili per ciascun bordo (superiore, destro, inferiore e sinistro):

   * Stile del bordo (nessuno, nascosto, punteggiato, tratteggiato, linea continua o linea doppia)
   * Colore del bordo (specifica il codice del colore o utilizza il selettore colore)
   * Spessore del bordo (trascina il cursore per selezionare lo spessore del bordo o specifica lo spessore in pixel)

   Il bordo supporta valori di spessore a partire da 0.

   Target supporta anche [altre unità di dimensione](https://www.w3.org/Style/Examples/007/units.en.html), come rem, pc, em, ecc.

* **Posizione**

   Sposta l’elemento selezionato dalla posizione corrente. È possibile modificare la posizione superiore, inferiore, sinistra, destra e [Z-index](https://www.w3schools.com/cssref/pr_pos_z-index.asp) dell&#39;elemento.

   Fai clic sull’elenco a discesa [!UICONTROL Statico] per scegliere tra le seguenti opzioni di posizione:

   * Statiche
   * Relativo
   * Assoluto
   * In rilievo
   * Fisso

   Fai clic sull’icona a discesa per ciascuna posizione per scegliere tra le seguenti opzioni:

   * Automatico
   * Valore (trascina il cursore per posizionare l’elemento o specifica il numero di pixel a cui spostare l’elemento)

   La posizione supporta valori positivi e negativi.

   Target supporta anche [altre unità di dimensione](https://www.w3.org/Style/Examples/007/units.en.html), come rem, pc, em, ecc.

* **Dimensioni**

   Modifica la larghezza e l’altezza dell’elemento selezionato.

   Fai clic sull’icona a discesa accanto a [!UICONTROL Larghezza] e [!UICONTROL Altezza] per scegliere tra le seguenti opzioni:

   * Automatico
   * Valore (trascina il cursore per ridimensionare l’elemento o specifica il numero di pixel per ciascuna dimensione)

* **Filtro**

   Trascina il cursore per ogni opzione filtro o specifica la percentuale desiderata:

   * Seppia
   * Contrasto
   * Luminosità
   * Scala di grigi
   * Sfocatura
   * Opacità
   * Inverti
   * Hue-rotate
   * Saturazione

* **Editor CSS**

   Se hai familiarità con l’utilizzo di Cascading Style Sheet (CSS) o se ricevi del codice dallo sviluppatore, l’editor CSS in tempo reale consente di visualizzare le modifiche e aggiungere stili.

   L’Editor CSS visualizza le modifiche apportate nel pannello Stili. Come mostrato nell’illustrazione seguente, sono state modificate le dimensioni del font, il bordo superiore e le dimensioni dell’immagine:

   ![Editor CSS con modifiche](/help/c-experiences/c-visual-experience-composer/assets/css-changes.png)

   Osserva i punti blu accanto alle opzioni [!UICONTROL Composizione tipografica], [!UICONTROL Bordo] e [!UICONTROL Dimensione] dell’illustrazione precedente. Questi punti indicano che sono state apportate modifiche a tali sezioni. Se apri questi pannelli di sezione, i punti blu vengono visualizzati accanto alle opzioni modificate.

   Se per impostazione predefinita lo stile desiderato non è disponibile negli [!UICONTROL Stili], è possibile digitare il codice desiderato.

   Considera che l’Editor CSS mostra i dettagli solo per la sessione in corso. Se salvi le modifiche e quindi riapri l’editor, i dettagli relativi alla modifica precedente non vengono visualizzati nell’editor, anche se selezioni di nuovo lo stesso elemento.

   >[!IMPORTANT]
   >
   >È possibile applicare un’immagine di sfondo utilizzando l’Editor CSS, ma potrebbe causare sfarfallii. Verifica le modifiche prima di implementarle.

#### Classe CSS

Specifica la classe CSS predefinita utilizzata per l’elemento. Se vengono selezionati più elementi, separa le classi CSS con uno spazio.

Disponibile per attività di [!UICONTROL A/B], [!UICONTROL personalizzazione automatizzata] e [!UICONTROL test multivariato].

#### Collegamento

Modifica l’URL nel collegamento.

Utilizza Modifica collegamento per aggiornare il selettore in modo che indirizzi allo stesso elemento immagine. Tuttavia, il collegamento a un elemento immagine diverso non è supportato. Per eseguire il collegamento a un elemento immagine diverso, elimina l’azione originale dall’editor di codice e utilizza il [!UICONTROL Compositore esperienza visivo] per applicare l’azione all’altro elemento immagine.

### Inserisci prima

Sono disponibili le seguenti opzioni:

#### Immagine, HTML e testo

Consente di aggiungere qualsiasi tipo di elemento alla pagina, e di modificare il contenuto esistente. Puoi aggiungere testo, codice, elenchi e così via per creare esperienze diverse da testare.

Seleziona un elemento nella pagina, quindi fai clic su [!UICONTROL Inserisci prima] e scegli se desideri inserire un’immagine, un HTML o un testo. L’elemento inserito viene visualizzato prima dell’elemento selezionato.

Il comportamento dell’elemento inserito dipende dalla struttura della pagina, dal CSS e da altre opzioni di configurazione della pagina. Per la corretta visualizzazione della pagina è necessario un codice HTML valido. Verifica sempre la pagina dopo l’inserimento di un elemento per essere certo che venga visualizzata come previsto.

[!UICONTROL Recommendations] supporta la funzione [!UICONTROL Inserisci prima] per i contenuti dei tag DIV, SECTION e ARTICLE.

**Nota:** l’inserimento di un’immagine richiede che [!DNL Adobe Scene7 Publishing System] sia attivato, in modo da avere accesso alla libreria delle immagini.

#### Consiglio

Includi consigli all’interno di attività di test A/B (tra cui Allocazione automatica e Targeting automatico) e targeting delle esperienze (XT). Per ulteriori informazioni, consulta [Consigli come offerta](/help/c-recommendations/recommendations-as-an-offer.md).

#### Frammento esperienza

Inserisci frammenti esperienza creati in [!DNL Adobe Experience Manager] (AEM) nelle attività di [!DNL Target] per aiutare l’ottimizzazione o la personalizzazione. Per ulteriori informazioni, consulta [Frammenti esperienza AEM](/help/c-experiences/c-manage-content/aem-experience-fragments.md).

### Inserisci dopo

Sono disponibili le seguenti opzioni:

#### Immagine, HTML e testo

Consente di aggiungere qualsiasi tipo di elemento alla pagina, e di modificare il contenuto esistente. Puoi aggiungere testo, codice, elenchi e così via per creare esperienze diverse da testare.

Seleziona un elemento nella pagina, quindi fai clic su [!UICONTROL Inserisci dopo] e scegli se desideri inserire un’immagine, un HTML o un testo. L’elemento inserito viene visualizzato dopo l’elemento selezionato.

Il comportamento dell’elemento inserito dipende dalla struttura della pagina, dal CSS e da altre opzioni di configurazione della pagina. Per la corretta visualizzazione della pagina è necessario un codice HTML valido. Verifica sempre la pagina dopo l’inserimento di un elemento per essere certo che venga visualizzata come previsto.

[!UICONTROL Recommendations] supporta la funzione [!UICONTROL Inserisci dopo] per i contenuti dei tag DIV, SECTION e ARTICLE.

**Nota:** l’inserimento di un’immagine richiede che [!DNL Adobe Scene7 Publishing System] sia attivato, in modo da avere accesso alla libreria delle immagini.

#### Consiglio

Includi consigli all’interno di attività di test A/B (tra cui Allocazione automatica e Targeting automatico) e targeting delle esperienze (XT). Per ulteriori informazioni, consulta [Consigli come offerta](/help/c-recommendations/recommendations-as-an-offer.md).

#### Frammento esperienza

Inserisci frammenti esperienza creati in [!DNL Adobe Experience Manager] (AEM) nelle attività di [!DNL Target] per aiutare l’ottimizzazione o la personalizzazione. Per ulteriori informazioni, consulta [Frammenti esperienza AEM](/help/c-experiences/c-manage-content/aem-experience-fragments.md).

### Sostituisci con

Sono disponibili le seguenti opzioni:

#### Immagine

Consente di selezionare una diversa immagine dalla libreria Contenuto. Le immagini disponibili per la sostituzione includono le immagini caricate nella cartella delle risorse di Experience Cloud o nella libreria di contenuti in Target.

Durante la creazione dell’attività iniziale, l’URL visualizzato non è l’URL utilizzato per la consegna. Dopo l’attività di sincronizzazione, tale URL viene aggiornato a un URL Scene7 di produzione.

Ad esempio, l’URL iniziale potrebbe essere simile all’esempio seguente:

`https://test.marketing.adobe.com/content/dam/mac/scholasticinc/Aug_MBM.jpeg?ch_ck=1470774943867`

Dopo la sincronizzazione dell’attività, l’URL di consegna potrebbe essere simile al seguente:

`http://s7d2.scene7.com/is/image/TargetTest/Aug_MBM?tm=1470768352933&fit=constrain&hei=173&wid=300`

La funzione Consigli supporta la funzione Sostituisci con nei tag DIV, SECTION e ARTICLE.

**Nota:** lo scambio delle immagini richiede un account Adobe Scene7 Publishing System.

#### Offerta HTML

Seleziona un’offerta diversa dalla [!UICONTROL libreria dei contenuti].

**Nota:**[!DNL Target] le offerte HTML sono memorizzate sui server di

Le dimensioni di un&#39;offerta HTML non possono superare i 256 KB.

#### Consiglio

Includi consigli all’interno di attività di test A/B (tra cui Allocazione automatica e Targeting automatico) e targeting delle esperienze (XT). Per ulteriori informazioni, consulta [Consigli come offerta](/help/c-recommendations/recommendations-as-an-offer.md).

#### Frammento esperienza

Inserisci frammenti esperienza creati in [!DNL Adobe Experience Manager] (AEM) nelle attività di [!DNL Target] per aiutare l’ottimizzazione o la personalizzazione. Per ulteriori informazioni, consulta [Frammenti esperienza AEM](/help/c-experiences/c-manage-content/aem-experience-fragments.md).

### Layout

Sono disponibili le seguenti opzioni:

#### Ridisponi

Trascina l’elemento in un’altra posizione nello stesso elemento padre o DIV. Gli altri elementi vengono spostati per fare spazio all’elemento ridisposto.

**Nota:** il tracciamento dei clic non funziona sugli elementi ridisposti.

#### Ridimensiona

Consente di ridimensionare un elemento nella pagina. Quando selezioni [!UICONTROL Ridimensiona], una maniglia compare nell’angolo in basso a destra dell’elemento e consente di trascinarlo per ridimensionare. Tieni premuto il tasto Maiusc per mantenere le stesse proporzioni.

**Nota:** gli elementi in linea non possono essere ridimensionati.

#### Sposta  {#move}

Consnete di spostare gli elementi nella pagina. A differenza dell’opzione [!UICONTROL Ridisponi], [!UICONTROL Sposta] non cambia la posizione degli altri elementi per lasciare spazio all’elemento spostato. Utilizza i tasti freccia per regolare meglio lo spostamento. (Miglioramento pianificato: supporto per assicurare che gli elementi spostati non risultino nascosti dietro ad altri elementi.)

In alcuni casi, ad esempio quando una limitazione CSS richiede che un elemento resti all’interno del suo elemento padre, non puoi spostare l’elemento al di fuori di quest’ultimo. Un elemento non può essere spostato all’esterno di un contenitore seguito dalla proprietà CSS `overflow: hidden`.

#### Nascondi

Consnete di nascondere l’elemento. Lo spazio vuoto viene conservato, ma il contenuto viene rimosso.

#### Rimuovi

Rimuovi l’elemento. Lo spazio vuoto dietro l&#39;immagine viene rimosso e lo spazio in cui l&#39;elemento si trovava viene compresso.

**Nota:** gli elementi di una mbox classica (una mbox creata in una campagna di Target Classic) non possono essere rimossi con questa opzione.

### Espandi sezione

Consente di selezionare l’elemento padre in aggiunta all’elemento selezionato originariamente. Quando selezioni un elemento padre, tutti i relativi figli vengono selezionati automaticamente. Puoi espandere la selezione più volte.

### Vai al link

Consente di aprire la destinazione del collegamento.

### Annulla/Ripristina

Annulla le modifiche apportate alle attività durante una sessione di modifica. Puoi inoltre ripristinare le modifiche precedentemente annullate.

## Considerazioni {#considerations}

* Se un’offerta contiene contenuti HTML, consulta la sezione su come avviene il rendering di contenuti HTML in at.js, in [Funzionamento di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md#render).

## Navigare tra gli elementi utilizzando il percorso DOM {#dom-path}

Facendo clic su un elemento della pagina, viene visualizzato il menu delle opzioni del Compositore esperienza visivo. Inoltre, quando fai clic su un elemento, il percorso DOM corrispondente viene visualizzato nella parte inferiore della pagina.

![Percorso DOM](/help/c-experiences/c-visual-experience-composer/assets/dom-path.png)

Puoi utilizzare il percorso DOM per vedere rapidamente le informazioni sull’elemento selezionato (tipo, ID e classe) e spostarti verso l’alto o il basso nel percorso DOM per selezionare l’elemento desiderato.

Quando passi il cursore del mouse sul percorso DOM, una casella blu evidenzia l’elemento corrispondente nel Compositore esperienza visivo. Se fai clic sull’elemento, una casella arancione evidenzia l’elemento e viene visualizzato il menu delle opzioni del Compositore esperienza visivo, come illustrato in precedenza.

Utilizzando il percorso DOM, è possibile passare facilmente a qualsiasi elemento principale, di pari livello o secondario all’interno del Compositore esperienza visivo.

La funzione Percorso DOM è disponibile anche quando si imposta il [tracciamento dei clic](/help/c-activities/r-success-metrics/click-tracking.md).