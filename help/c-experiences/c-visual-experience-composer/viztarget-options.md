---
description: Quando fate clic su un elemento di pagina in Visual Experience Composer (Compositore esperienza visivo), un menu mostra le opzioni disponibili per tale tipo di elemento.
keywords: opzioni compositore esperienza visivo;opzioni compositore esperienza;opzioni esperienza;modifica testo;modifica HTML;modifica testo/HTML;modifica colore di sfondo;colore di sfondo;inserisci elemento;modifica collegamento;collegamento;link;collegamento al compositore esperienza visivo;modifica classe CSS;classe CSS;sostituire l’offerta;sostituisci l’offerta;scambiare immagine;scambia immagine;rimuovere elemento;rimuovi elemento;nascondere una voce;nascondi voce;riorganizzare;spostare elemento;sposta elemento;ridimensionare elemento;ridimensiona elemento;elemento;espandere la selezione;passa a questo collegamento;passare a un link;passa a un link;navigare;annullare;ripeti;annulla/ripristina
seo-description: Quando fate clic su un elemento di pagina in Adobe Target Visual Experience Composer (VEC), un menu mostra le opzioni disponibili per tale tipo di elemento.
seo-title: Opzioni di Adobe Target Visual Experience Composer (VEC)
solution: Target
title: Opzioni del Compositore esperienza visivo
topic: Standard
uuid: efd672ae-c684-455f-8ec1-0efcfe1e9534
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Opzioni del Compositore esperienza visivo{#visual-experience-composer-options}

Quando fate clic su un elemento di pagina in Visual Experience Composer (Compositore esperienza visivo), un menu mostra le opzioni disponibili per tale tipo di elemento. Inoltre, nella parte inferiore della pagina viene visualizzato un percorso DOM che consente di navigare facilmente nella struttura della pagina.

## Opzioni VEC

Le varie azioni Visual Experience Composer (Compositore esperienza visivo) raggruppate sono opzioni di menu appropriate per rendere il processo più veloce ed efficiente:

![Menu delle opzioni VEC](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/vec-options.png)

>[!NOTE]
>
>Le opzioni disponibili dipendono dal tipo di attività che si sta modificando.

### Modifica

Sono disponibili le seguenti opzioni:

#### Testo/HTML {#edit-text-html}

Modifica il codice HTML per l&#39;elemento, ad esempio il testo per un&#39;area di testo, un pulsante o collegamento.

Oltre al codice HTML, puoi modificare e inserire codice JavaScript personalizzato.

Sono disponibili opzioni di formattazione per modificare il testo e contenuti HTML per le attività [!UICONTROL A/B] e [!UICONTROL Targeting esperienza]. Puoi scegliere font e stile, l’allineamento del testo e altre opzioni standard per la formattazione del testo. Quando modifichi l’HTML, puoi passare dalla visualizzazione del codice alla visualizzazione per modifica Rich Text dell’HTML.

I seguenti tag HTML 5 possono essere nidificati:

| Tag | Tag nidificati consentiti |
| --- | --- |
| `<a>` | `<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>`, `<div>`, `<figure>`, `<figcaption>` |
| `<ins>` | `<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>` |
| `<del>` | `<ul>`, `<ol>`, `<menu>`, `<h1-h6>`, `<p>` |
| `<label>` | `<p>` |

#### Colore di sfondo

Utilizza il settore colori per selezionare o configurare un colore di sfondo. È possibile selezionare un campione di colore e regolarlo utilizzando i valori RGB o i codici esadecimali. La x rossa nel selettore colore rende lo sfondo trasparente.

**Nota**: questa opzione non è disponibile se è impostata un’immagine di sfondo.

#### Stili

Il pannello [!UICONTROL Stili] consente di visualizzare o modificare il valore degli stili esistenti per l&#39;elemento selezionato. Potete inoltre aggiungere ulteriore stile.

Per accedere al [!UICONTROL pannello Stili] , fare clic su un elemento di pagina dall&#39;interno della VEC, quindi fare clic su **[!UICONTROL Modifica]** &gt; **[!UICONTROL Stili]**.

Il [!UICONTROL pannello Stili] viene visualizzato sul lato destro della VEC. Il pannello contiene un elenco di stili che consente di modificare o aggiungere all&#39;elemento selezionato. Un editor CSS in tempo reale consente di visualizzare le modifiche e aggiungere stili se avete familiarità con Cascading Style Sheets (CSS) o se ricevete codice dallo sviluppatore.

![Pannello Stili](/help/c-experiences/c-visual-experience-composer/assets/styles-panel-new.png)

Quando si applicano stili diversi, è sempre possibile ripristinare le modifiche facendo clic sull&#39;icona [!UICONTROL Ripristina] visualizzata nell&#39;angolo in alto a destra del pannello [!UICONTROL Stili] , dopo aver apportato una modifica a qualsiasi sezione. Tenete presente che facendo clic sull&#39;icona [!UICONTROL Ripristina] , tutte le modifiche vengono ripristinate nel pannello della sezione corrente.

Espandete ogni sezione per modificare o aggiungere stili, come descritto di seguito. Per salvare le modifiche, fate clic sull&#39;icona Indietro nella parte superiore del pannello per tornare alla visualizzazione principale del pannello, quindi fate clic **[!UICONTROL su Salva]**.

Tenete presente che i punti blu nel pannello principale e accanto a ogni opzione nei vari pannelli di sezione indicano che sono state apportate modifiche agli stili corrispondenti. In questo modo è facile rivedere le modifiche prima di fare clic [!UICONTROL su Salva].

>[!NOTE]
>
>Le azioni rapide per le modifiche di layout, il colore di sfondo, il ridimensionamento e lo spostamento sono disponibili anche come azioni separate nel menu VEC. Queste opzioni possono essere utilizzate come azioni separate oppure potete usare il menu Stili, come spiegato qui.

* **Composizione tipografica**

   Modificare la composizione tipografica di un elemento. Le modifiche tipografiche sono veloci e veloci.

   Anche se l&#39;editor Rich Text (Edit Text/HTML) è disponibile per la ottimizzazione dell&#39;ottimizzazione, le azioni rapide per apportare modifiche all&#39;intero elemento sono disponibili tramite questa opzione. Se desiderate applicare modifiche tipografiche a una sola parte del testo (non al testo completo), utilizzate l&#39; [editor Rich Text](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md).

   Potete modificare i seguenti stili tipografici:

   * Dimensione font
   * Spessore font
   * Stile font
   * Colore (specificate il codice del colore o utilizzate il selettore colore)
   * Spaziatura tra parole
   * Altezza riga
   * Allineamento del testo

* **Margine**

   Modificare il margine dell&#39;elemento selezionato. Potete modificare i margini sinistro, destro, inferiore e superiore.

   Fate clic sull&#39;icona a discesa per ciascun margine per scegliere tra le opzioni seguenti:

   * Automatico
   * Valore (trascinate il cursore per impostare il margine o specificare il numero di pixel per ciascun margine)
   Il margine supporta valori positivi e negativi.

   Target supporta anche altre unità di dimensioni, come rem, pc, em ecc. Per ulteriori informazioni su queste unità, vedere [Fogli di stile Web CSS Tips and Tricks](https://www.w3.org/Style/Examples/007/units.en.html).

* **Spaziatura**

   Modificare la spaziatura per l&#39;elemento selezionato. Potete modificare la spaziatura sinistra, destra, inferiore e superiore.

   Trascinare il cursore per impostare la spaziatura o specificare il numero di pixel da applicare alla spaziatura.

   La spaziatura supporta la larghezza a partire dal 0.

   Target supporta anche [altre unità di dimensioni](https://www.w3.org/Style/Examples/007/units.en.html), come rem, pc, em ecc.

* **Bordo**

   Fate clic sulle icone dei bordi nella parte superiore del pannello per modificare il bordo dell&#39;elemento selezionato.

   È possibile modificare i seguenti stili per ciascun bordo (superiore, destro, inferiore e sinistro):

   * Stile bordo (nessuno, nascosto, punteggiato, tratteggiato, pieno o doppio)
   * Colore bordo (specificate il codice del colore o utilizzate il selettore colore)
   * Larghezza bordo (trascinate il cursore per selezionare la larghezza del bordo o specificate la larghezza in pixel)
   Il bordo supporta la larghezza a partire dal 0.

   Target supporta anche [altre unità di dimensioni](https://www.w3.org/Style/Examples/007/units.en.html), come rem, pc, em ecc.

* **Posizione**

   Sposta l&#39;elemento selezionato dalla posizione corrente. Potete modificare le posizioni di indice superiore, inferiore, sinistro, destro e [z](https://www.w3schools.com/cssref/pr_pos_z-index.asp) dell&#39;elemento.

   Click the [!UICONTROL Static] drop-down list to choose from the following position options:

   * Statiche
   * Relativo
   * Assoluto
   * Fisso
   * Problema risolto
   Fate clic sull&#39;icona a discesa per ogni posizione per scegliere tra le opzioni seguenti:

   * Automatico
   * Valore (trascinate il cursore per posizionare l&#39;elemento o specificate il numero di pixel da spostare)
   La posizione supporta valori positivi e negativi.

   Target supporta anche [altre unità di dimensioni](https://www.w3.org/Style/Examples/007/units.en.html), come rem, pc, em ecc.

* **Dimensioni**

   Modifica la larghezza e l&#39;altezza dell&#39;elemento selezionato.

   Fate clic sull&#39;icona a discesa accanto [!UICONTROL a Larghezza] e [!UICONTROL altezza] per scegliere tra le opzioni seguenti:

   * Automatico
   * Valore (trascinate il cursore per ridimensionare l&#39;elemento o specificare il numero di pixel per ciascuna dimensione)

* **Filtro**

   Trascinate il cursore per ogni opzione filtro o specificate la percentuale desiderata:

   * Seppia
   * Contrasto
   * Luminosità
   * Grayscale
   * Sfoca
   * Opacità
   * Inverti
   * Rotazione tonalità
   * Saturazione

* **Editor CSS**

   L&#39;editor CSS in tempo reale consente di visualizzare le modifiche e aggiungere stili se avete familiarità con Cascading Style Sheets (CSS) o se ricevete codice dallo sviluppatore.

   L&#39;Editor CSS visualizza le modifiche apportate nel pannello Stili. Come illustrato nell&#39;illustrazione seguente, sono state modificate le dimensioni del font, il bordo superiore e le dimensioni dell&#39;immagine:

   ![Editor CSS con modifiche](/help/c-experiences/c-visual-experience-composer/assets/css-changes.png)

   Osservate i punti blu accanto alle opzioni [!UICONTROL Composizione], [!UICONTROL Bordo e][!UICONTROL Dimensione] dell&#39;illustrazione precedente. Questi puntini indicano che sono state apportate modifiche a tali sezioni. Se aprite questi pannelli di sezione, i punti blu vengono visualizzati accanto alle opzioni specifiche modificate.

   Se lo stile desiderato non è disponibile per impostazione predefinita negli [!UICONTROL stili], è possibile digitare il codice desiderato.

   Tenete presente che l&#39;Editor CSS mostra i dettagli solo per la sessione corrente. Se salvate le modifiche e quindi riaprite l&#39;editor, i dettagli relativi alla modifica precedente non vengono visualizzati nell&#39;editor, anche se selezionate di nuovo lo stesso elemento.

   >[!Important]
   >
   >Potete applicare un&#39;immagine di sfondo utilizzando l&#39;Editor CSS, ma potrebbe causare sfarfallii. Verifica le modifiche prima della distribuzione.

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

Recommendations supporta sostituisci con i tag DIV, SECTION e ARTICOLO.

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

#### Sposta 

Consnete di spostare gli elementi nella pagina. A differenza dell’opzione [!UICONTROL Ridisponi], [!UICONTROL Sposta] non cambia la posizione degli altri elementi per lasciare spazio all’elemento spostato. Utilizza i tasti freccia per regolare meglio lo spostamento. (Miglioramento pianificato: supporto per assicurare che gli elementi spostati non risultino nascosti dietro ad altri elementi.)

In alcuni casi, ad esempio quando una limitazione CSS richiede che un elemento resti all’interno del suo elemento padre, non puoi spostare l’elemento al di fuori di quest’ultimo.

#### Nascondi

Consnete di nascondere l’elemento. Lo spazio vuoto viene conservato, ma il contenuto viene rimosso.

#### Rimuovi

Rimuovi l’elemento. Lo spazio vuoto dietro l&#39;immagine viene rimosso e lo spazio in cui l&#39;elemento si trovava viene compresso.

**Nota:** gli elementi di una mbox classica (una mbox creata in una campagna di Target Classic) non possono essere rimossi con questa opzione.

### Espandi sezione

Consente di selezionare l’elemento padre in aggiunta all’elemento selezionato originariamente. Quando selezioni un elemento padre, tutti i relativi figli vengono selezionati automaticamente. Puoi espandere la selezione più volte.

### Passa a Collegamento

Consente di aprire la destinazione del collegamento.

### Annulla/Ripristina

Annulla le modifiche apportate alle attività durante una sessione di modifica. Puoi inoltre ripristinare le modifiche precedentemente annullate.

## Navigare tra gli elementi utilizzando il percorso DOM {#dom-path}

Quando si fa clic su un elemento della pagina, viene visualizzato il menu delle opzioni VEC. Inoltre, quando fate clic su un elemento, il percorso DOM corrispondente viene visualizzato nella parte inferiore della pagina.

![Percorso DOM](/help/c-experiences/c-visual-experience-composer/assets/dom-path.png)

Potete utilizzare il percorso DOM per vedere rapidamente le informazioni sull&#39;elemento selezionato (tipo, ID e classe) e spostarsi verso l&#39;alto o il basso sul percorso DOM per selezionare l&#39;elemento desiderato.

Quando passate il mouse sul percorso DOM, una casella blu evidenzia l&#39;elemento corrispondente nell&#39;aula virtuale. Quando fate clic sull&#39;elemento, una casella arancione evidenzia l&#39;elemento e il menu delle opzioni VEC, come illustrato in precedenza.

Potete facilmente passare a qualsiasi elemento principale, di pari livello o secondario all&#39;interno della VEC utilizzando il percorso DOM.

La funzione path path (Percorso DOM) è disponibile anche quando si imposta il tracciamento [dei clic](/help/c-activities/r-success-metrics/click-tracking.md).