---
keywords: opzioni compositore esperienza visivo;opzioni compositore esperienza;opzioni esperienza;modifica testo;modifica html;modifica testo/html;modifica colore di sfondo;colore di sfondo;inserisci elemento;modifica collegamento;collegamento;collegamento compositore esperienza visivo;modifica classe css;offerta di scambio;scambio di offerte;scambio di immagini;rimozione elemento;rimozione elemento;elemento;nascondere elemento;elemento;sposta elemento;elemento;spostamento elemento;elemento;ridimensionamento elemento;ridimensionamento elemento;ridimensionamento;espandi selezione;naviga a questo collegamento;naviga collegamento;naviga;collega;naviga;collegamento;annulla;annulla;ripristina;annulla/ripristina;eventi personalizzati;componenti web
description: Esplora le opzioni disponibili nel Compositore esperienza visivo di Adobe Target. Fai clic su un elemento per vedere quali opzioni sono disponibili per tale elemento.
title: Come si utilizzano le opzioni del Compositore esperienza visivo?
feature: Visual Experience Composer (VEC)
exl-id: 50993d6c-5025-488a-8b33-9ed7c142de6e
source-git-commit: 89b995f20491fe0a51c91f8a1fe7e6b1ccc7f974
workflow-type: tm+mt
source-wordcount: '2624'
ht-degree: 71%

---

# Opzioni del Compositore esperienza visivo

Quando fai clic su un elemento di pagina nel [!DNL Adobe Target] [!UICONTROL Compositore esperienza visivo] (Compositore esperienza visivo), un menu mostra le opzioni disponibili per quel tipo di elemento. Inoltre, nella parte inferiore della pagina viene visualizzato un percorso DOM che consente di navigare facilmente nella struttura della pagina.

## Opzioni VEC

Le varie azioni del Compositore esperienza visivo sono disponibili come opzioni di menu raggruppate per rendere il processo più veloce ed efficiente:

![Menu delle opzioni del Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/vec-options.png)

>[!NOTE]
>
>Le opzioni disponibili dipendono dal tipo di attività che si sta modificando.

### [!UICONTROL Modifica]

Sono disponibili le seguenti opzioni:

#### [!UICONTROL Testo/HTML] {#edit-text-html}

Modifica il codice HTML per l&#39;elemento, ad esempio il testo per un&#39;area di testo, un pulsante o collegamento.

Oltre al codice HTML, puoi modificare e inserire codice JavaScript personalizzato.

Sono disponibili opzioni di formattazione per modificare il testo e contenuti HTML per le attività [!UICONTROL A/B] e [!UICONTROL Targeting esperienza]. Puoi scegliere font e stile, l’allineamento del testo e altre opzioni standard per la formattazione del testo. Quando modifichi l’HTML, puoi passare dalla visualizzazione del codice alla visualizzazione per modifica Rich Text dell’HTML.

I seguenti tag HTML5 possono essere nidificati:

| Tag | Tag nidificati consentiti |
| --- | --- |
| `<a>` | `<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>`, `<div>`, `<figure>`, `<figcaption>` |
| `<ins>` | `<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>` |
| `<del>` | `<ul>`, `<ol>`, `<menu>`, `<h1-h6>`, `<p>` |
| `<label>` | `<p>` |

#### [!UICONTROL Colore di sfondo]

Utilizza il settore colori per selezionare o configurare un colore di sfondo. È possibile selezionare un campione di colore e regolarlo utilizzando i valori RGB o i codici esadecimali. La x rossa nel selettore colore rende lo sfondo trasparente.

**Nota**: questa opzione non è disponibile se è impostata un’immagine di sfondo.

#### [!UICONTROL Stili] {#styles}

Il pannello [!UICONTROL Stili] consente di visualizzare o modificare il valore degli stili esistenti per l’elemento selezionato. Inoltre, è possibile aggiungere ulteriore formattazione.

Per accedere al [!UICONTROL Stili] fai clic su un elemento di pagina nel Compositore esperienza visivo, quindi fai clic su **[!UICONTROL Modifica]** > **[!UICONTROL Stili]**.

Il pannello [!UICONTROL Stili] viene visualizzato sul lato destro del Compositore esperienza visivo. Il pannello contiene un elenco di stili che consente di modificare o aggiungere formattazione all’elemento selezionato. Se hai familiarità con l’utilizzo di Cascading Style Sheet (CSS) o se ricevi del codice dallo sviluppatore, un editor CSS in tempo reale consente di visualizzare le modifiche e aggiungere stili.

![Pannello Stili](/help/c-experiences/c-visual-experience-composer/assets/styles-panel-new.png)

Quando applichi stili diversi, puoi sempre ripristinare le modifiche facendo clic sul pulsante [!UICONTROL Ripristina] che viene visualizzata nell’angolo in alto a destra del [!UICONTROL Stili] dopo aver modificato una sezione. Fai clic su [!UICONTROL Ripristina] ripristina tutte le modifiche apportate al pannello della sezione corrente.

Espandi ogni sezione per modificare o aggiungere stili, come descritto di seguito. Per salvare le modifiche, fai clic sull’icona Indietro nella parte superiore del pannello per tornare alla visualizzazione principale del pannello, quindi fai clic su **[!UICONTROL Salva]**.

I punti blu nel pannello principale e accanto a ogni opzione nei vari pannelli di sezione indicano che sono stati modificati gli stili corrispondenti. Questo indicatore visivo facilita la revisione delle modifiche prima di fare clic su [!UICONTROL Salva].

>[!NOTE]
>
>Le azioni rapide per le modifiche di layout, il colore di sfondo, il ridimensionamento e lo spostamento sono disponibili anche come azioni separate nel menu del Compositore esperienza visivo. Queste opzioni possono essere utilizzate come azioni separate oppure puoi utilizzare il menu Stili , come spiegato qui.

* **[!UICONTROL Sfondo]**

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

* **[!UICONTROL Composizione tipografica]**

   Puoi modificare la composizione tipografica di un elemento. Le modifiche tipografiche sono semplici e veloci.

   Anche se l’editor Rich Text (Modifica testo/HTML) è disponibile per la regolazione fine, questa opzione permette di intervenire rapidamente per modificare l’intero elemento. Se desideri applicare modifiche di composizione tipografica a una sola parte del testo (non al testo completo), utilizza l’[editor Rich Text](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md).

   È possibile modificare i seguenti stili di composizione tipografica:

   * [!UICONTROL Dimensione font]
   * [!UICONTROL Spessore font]
   * [!UICONTROL Stile font]
   * [!UICONTROL Colore] (specifica il codice del colore o utilizza il selettore del colore)
   * [!UICONTROL Spaziatura tra parole]
   * [!UICONTROL Altezza riga]
   * [!UICONTROL Allineamento testo]

* **[!UICONTROL Margine]**

   Modifica il margine dell’elemento selezionato. È possibile modificare il margine sinistro, destro, inferiore e superiore.

   Fai clic sull’icona a discesa di ciascun margine per scegliere tra le opzioni seguenti:

   * [!UICONTROL Automatico]
   * [!UICONTROL Valore] (trascina il cursore per impostare il margine o specifica il numero di pixel per ciascun margine)

   Il margine supporta valori positivi e negativi.

   Target supporta anche altre unità di misura, come rem, pc, em. Per ulteriori informazioni su queste unità, vedi [Suggerimenti e trucchi per i fogli di stile web CSS](https://www.w3.org/Style/Examples/007/units.en.html).

* **[!UICONTROL Spaziatura]**

   Modifica la spaziatura per l’elemento selezionato. È possibile modificare la spaziatura sinistra, destra, inferiore e superiore.

   Trascina il cursore per impostare la spaziatura o specifica il numero di pixel da applicare alla spaziatura.

   La spaziatura supporta valori di larghezza a partire da 0.

   Target supporta anche [altre unità](https://www.w3.org/Style/Examples/007/units.en.html), come rem, pc, em.

* **[!UICONTROL Bordo]**

   Fai clic sulle icone dei bordi nella parte superiore del pannello per modificare il bordo dell’elemento selezionato.

   È possibile modificare i seguenti stili per ciascun bordo (superiore, destro, inferiore e sinistro):

   * [!UICONTROL Stile bordo] (Nessuno, nascosto, punteggiato, tratteggiato, pieno o doppio)
   * [!UICONTROL Colore bordo] (specifica il codice del colore o utilizza il selettore del colore)
   * [!UICONTROL Larghezza bordo] (trascina il cursore per selezionare la larghezza di un bordo o specifica la larghezza in pixel)

   Il bordo supporta valori di spessore a partire da 0.

   Target supporta anche [altre unità](https://www.w3.org/Style/Examples/007/units.en.html), come rem, pc, em.

* **[!UICONTROL Posizione]**

   Sposta l’elemento selezionato dalla posizione corrente. È possibile modificare i valori superiore, inferiore, sinistro, destro e [Indice Z](https://www.w3schools.com/cssref/pr_pos_z-index.asp) posizione.

   Fai clic sull’elenco a discesa [!UICONTROL Statico] per scegliere tra le seguenti opzioni di posizione:

   * [!UICONTROL Statiche]
   * [!UICONTROL Relativo]
   * [!UICONTROL Assoluto]
   * [!UICONTROL In rilievo]
   * [!UICONTROL Fisso]

   Fai clic sull’icona a discesa per ciascuna posizione per scegliere tra le seguenti opzioni:

   * [!UICONTROL Automatico]
   * [!UICONTROL Valore] (trascinate il cursore per posizionare l’elemento o specificate il numero di pixel da spostare)

   La posizione supporta valori positivi e negativi.

   Target supporta anche [altre unità](https://www.w3.org/Style/Examples/007/units.en.html), come rem, pc, em.

* **[!UICONTROL Dimensioni]**

   Modifica la larghezza e l’altezza dell’elemento selezionato.

   Fai clic sull’icona a discesa accanto a [!UICONTROL Larghezza] e [!UICONTROL Altezza] per scegliere tra le seguenti opzioni:

   * [!UICONTROL Automatico]
   * [!UICONTROL Valore] (trascina il cursore per ridimensionare l’elemento o specifica il numero di pixel per ciascuna dimensione)

* **[!UICONTROL Filtro]**

   Trascina il cursore per ogni opzione filtro o specifica la percentuale desiderata:

   * [!UICONTROL Seppia]
   * [!UICONTROL Contrasto]
   * [!UICONTROL Luminosità]
   * [!UICONTROL Scala di grigi]
   * [!UICONTROL Sfocatura]
   * [!UICONTROL Opacità]
   * [!UICONTROL Inverti]
*
[!UICONTROL  Hue-rotate]
   * [!UICONTROL Saturazione]

* **[!UICONTROL Editor CSS]**

   Se hai familiarità con l’utilizzo di Cascading Style Sheet (CSS) o se ricevi del codice dallo sviluppatore, l’editor CSS in tempo reale consente di visualizzare le modifiche e aggiungere stili.

   L’Editor CSS visualizza le modifiche apportate nel pannello Stili. Come mostrato nell’illustrazione seguente, sono state modificate le dimensioni del font, il bordo superiore e le dimensioni dell’immagine:

   ![Editor CSS con modifiche](/help/c-experiences/c-visual-experience-composer/assets/css-changes.png)

   Osserva i punti blu accanto alle opzioni [!UICONTROL Composizione tipografica], [!UICONTROL Bordo] e [!UICONTROL Dimensione] dell’illustrazione precedente. Questi punti indicano che queste sezioni sono state modificate. Se apri questi pannelli di sezione, i punti blu vengono visualizzati accanto alle opzioni modificate.

   Se per impostazione predefinita lo stile desiderato non è disponibile negli [!UICONTROL Stili], è possibile digitare il codice desiderato.

   L’Editor CSS mostra i dettagli solo per la sessione corrente. Se salvi le modifiche e quindi riapri l’editor, i dettagli relativi alla modifica precedente non vengono visualizzati nell’editor, anche se selezioni di nuovo lo stesso elemento.

   >[!IMPORTANT]
   >
   >È possibile applicare un’immagine di sfondo utilizzando l’Editor CSS, ma potrebbe causare sfarfallii. Verifica le modifiche prima di implementarle.

#### [!UICONTROL Classe CSS]

Specifica la classe CSS predefinita utilizzata per l’elemento. Se vengono selezionati più elementi, separa le classi CSS con uno spazio.

Disponibile per attività di [!UICONTROL A/B], [!UICONTROL personalizzazione automatizzata] e [!UICONTROL test multivariato].

#### [!UICONTROL Collegamento]

Modifica l’URL nel collegamento.

Utilizza Modifica collegamento per aggiornare il selettore in modo che indirizzi allo stesso elemento immagine. Tuttavia, il collegamento a un elemento immagine diverso non è supportato. Per eseguire il collegamento a un elemento immagine diverso, elimina l’azione originale dall’editor di codice e utilizza il [!UICONTROL Compositore esperienza visivo] per applicare l’azione all’altro elemento immagine.

### [!UICONTROL Inserisci prima]

Sono disponibili le seguenti opzioni:

#### [!UICONTROL Immagine], [!UICONTROL HTML]e [!UICONTROL Testo]

Consente di aggiungere qualsiasi tipo di elemento alla pagina, e di modificare il contenuto esistente. Puoi aggiungere testo, codice, elenchi e così via per creare esperienze diverse da testare.

Seleziona un elemento nella pagina, quindi fai clic su [!UICONTROL Inserisci prima] e scegli se desideri inserire un’immagine, un HTML o un testo. L’elemento inserito viene visualizzato prima dell’elemento selezionato.

Il comportamento dell’elemento inserito dipende dalla struttura della pagina, dal CSS e da altre opzioni di configurazione della pagina. Per la corretta visualizzazione della pagina è necessario un codice HTML valido. Verifica sempre la pagina dopo l’inserimento di un elemento per essere certo che venga visualizzata come previsto.

[!UICONTROL Recommendations] supporta la funzione [!UICONTROL Inserisci prima] per i contenuti dei tag DIV, SECTION e ARTICLE.

**Nota:** l’inserimento di un’immagine richiede che [!DNL Adobe Scene7 Publishing System] sia attivato, in modo da avere accesso alla libreria delle immagini.

#### Consiglio

Includi consigli all’interno di attività di test A/B (tra cui Allocazione automatica e Targeting automatico) e targeting delle esperienze (XT). Per ulteriori informazioni, consulta [Consigli come offerta](/help/c-recommendations/recommendations-as-an-offer.md).

#### [!UICONTROL Frammento esperienza]

Inserisci frammenti esperienza creati in [!DNL Adobe Experience Manager] (AEM) nelle attività di [!DNL Target] per aiutare l’ottimizzazione o la personalizzazione. Per ulteriori informazioni, consulta [Frammenti esperienza AEM](/help/c-experiences/c-manage-content/aem-experience-fragments.md).

### [!UICONTROL Inserisci dopo]

Sono disponibili le seguenti opzioni:

#### [!UICONTROL Immagine], [!UICONTROL HTML]e [!UICONTROL Testo]

Consente di aggiungere qualsiasi tipo di elemento alla pagina, e di modificare il contenuto esistente. Puoi aggiungere testo, codice, elenchi e così via per creare esperienze diverse da testare.

Seleziona un elemento nella pagina, quindi fai clic su [!UICONTROL Inserisci dopo] e scegli se desideri inserire un’immagine, un HTML o un testo. L’elemento inserito viene visualizzato dopo l’elemento selezionato.

Il comportamento dell’elemento inserito dipende dalla struttura della pagina, dal CSS e da altre opzioni di configurazione della pagina. Per la corretta visualizzazione della pagina è necessario un codice HTML valido. Verifica sempre la pagina dopo l’inserimento di un elemento per essere certo che venga visualizzata come previsto.

[!UICONTROL Recommendations] supporta la funzione [!UICONTROL Inserisci dopo] per i contenuti dei tag DIV, SECTION e ARTICLE.

**Nota:** l’inserimento di un’immagine richiede che [!DNL Adobe Scene7 Publishing System] sia attivato, in modo da avere accesso alla libreria delle immagini.

#### Consiglio

Includi consigli all’interno di attività di test A/B (tra cui Allocazione automatica e Targeting automatico) e targeting delle esperienze (XT). Per ulteriori informazioni, consulta [Consigli come offerta](/help/c-recommendations/recommendations-as-an-offer.md).

#### [!UICONTROL Frammento esperienza]

Inserisci frammenti esperienza creati in [!DNL Adobe Experience Manager] (AEM) nelle attività di [!DNL Target] per aiutare l’ottimizzazione o la personalizzazione. Per ulteriori informazioni, consulta [Frammenti esperienza AEM](/help/c-experiences/c-manage-content/aem-experience-fragments.md).

### [!UICONTROL Sostituisci con]

Sono disponibili le seguenti opzioni:

#### [!UICONTROL Immagine]

Consente di selezionare una diversa immagine dalla libreria Contenuto. Le immagini disponibili per la sostituzione includono le immagini caricate nella cartella delle risorse di Experience Cloud o nella libreria di contenuti in Target.

Durante la creazione dell’attività iniziale, l’URL visualizzato non è l’URL utilizzato per la consegna. Dopo l’attività di sincronizzazione, tale URL viene aggiornato a un URL Scene7 di produzione.

Ad esempio, l’URL iniziale potrebbe essere simile all’esempio seguente:

`https://test.marketing.adobe.com/content/dam/mac/scholasticinc/Aug_MBM.jpeg?ch_ck=1470774943867`

Dopo la sincronizzazione dell’attività, l’URL di consegna potrebbe essere simile al seguente:

`http://s7d2.scene7.com/is/image/TargetTest/Aug_MBM?tm=1470768352933&fit=constrain&hei=173&wid=300`

La funzione Consigli supporta la funzione Sostituisci con nei tag DIV, SECTION e ARTICLE.

**Nota:** lo scambio delle immagini richiede un account Adobe Scene7 Publishing System.

#### [!UICONTROL Offerta HTML]

Seleziona un’offerta diversa dalla [!UICONTROL libreria dei contenuti].

**Nota:**[!DNL Target] le offerte HTML sono memorizzate sui server di

Un’offerta HTML può contenere fino a 256 KB.

#### Consiglio

Includi consigli all’interno di attività di test A/B (tra cui Allocazione automatica e Targeting automatico) e targeting delle esperienze (XT). Per ulteriori informazioni, consulta [Consigli come offerta](/help/c-recommendations/recommendations-as-an-offer.md).

#### [!UICONTROL Frammento esperienza]

Inserisci frammenti esperienza creati in [!DNL Adobe Experience Manager] (AEM) nelle attività di [!DNL Target] per aiutare l’ottimizzazione o la personalizzazione. Per ulteriori informazioni, consulta [Frammenti esperienza AEM](/help/c-experiences/c-manage-content/aem-experience-fragments.md).

### [!UICONTROL Layout]

Sono disponibili le seguenti opzioni:

#### [!UICONTROL Ridisponi]

Trascina l’elemento in un’altra posizione nello stesso elemento padre o DIV. Gli altri elementi vengono spostati per fare spazio all’elemento ridisposto.

**Nota:** il tracciamento dei clic non funziona sugli elementi ridisposti.

#### [!UICONTROL Ridimensiona]

Consente di ridimensionare un elemento nella pagina. Quando selezioni [!UICONTROL Ridimensiona], nell’angolo in basso a destra dell’elemento viene visualizzata una maniglia che consente di trascinare tale angolo per ridimensionare. Tieni premuto il tasto Maiusc per mantenere le stesse proporzioni.

**Nota:** gli elementi in linea non possono essere ridimensionati.

#### [!UICONTROL Sposta] {#move}

Consnete di spostare gli elementi nella pagina. A differenza dell’opzione [!UICONTROL Ridisponi], [!UICONTROL Sposta] non cambia la posizione degli altri elementi per lasciare spazio all’elemento spostato. Utilizza i tasti freccia per regolare meglio lo spostamento. (Miglioramento pianificato: per garantire che gli elementi spostati non siano nascosti dietro ad altri elementi.)

In alcune situazioni, ad esempio quando una limitazione CSS richiede che un elemento resti all’interno del suo elemento padre, non puoi spostare l’elemento al di fuori di quest’ultimo. Un elemento non può essere spostato all’esterno di un contenitore seguito dalla proprietà CSS `overflow: hidden`.

#### [!UICONTROL Nascondi]

Consnete di nascondere l’elemento. Lo spazio vuoto viene conservato, ma il contenuto viene rimosso.

#### [!UICONTROL Rimuovi]

Rimuovi l’elemento. Lo spazio vuoto dietro l&#39;immagine viene rimosso e lo spazio in cui l&#39;elemento si trovava viene compresso.

**Nota:** gli elementi di una mbox classica (una mbox creata in una campagna di Target Classic) non possono essere rimossi con questa opzione.

### [!UICONTROL Espandi sezione]

Consente di selezionare l’elemento padre in aggiunta all’elemento selezionato originariamente. Quando selezioni un elemento padre, tutti i relativi figli vengono selezionati automaticamente. Puoi espandere la selezione più volte.

### [!UICONTROL Vai al link]

Consente di aprire la destinazione del collegamento.

### [!UICONTROL Annulla]/[!UICONTROL Ripeti]

Annulla le modifiche apportate alle attività durante una sessione di modifica. Puoi inoltre ripristinare le modifiche precedentemente annullate.

## Considerazioni {#considerations}

* Se un’offerta contiene contenuti HTML, consulta la sezione su come avviene il rendering di contenuti HTML in at.js, in [Funzionamento di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md#render).

## Supporto di elementi personalizzati {#custom}

Il Compositore esperienza visivo supporta [Componenti web](https://developer.mozilla.org/en-US/docs/Web/Web_Components) per creare e testare esperienze e offerte personalizzate su elementi personalizzati e su elementi all’interno di elementi personalizzati. Questa funzionalità è disponibile nel Compositore esperienza visivo per tutti [!DNL Target] tipi di attività.

>[!NOTE]
>
>Il supporto del Compositore esperienza visivo per gli elementi personalizzati è supportato in [versione at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) 2.7.0 (o successiva). Assicurati che il tuo sito web disponga della versione richiesta distribuita. Se utilizzi [Estensione helper del Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md), deve anche avere la versione richiesta di at.js distribuita. Le opzioni del Compositore esperienza visivo descritte sopra non sono visibili e sono disponibili per l’uso con le versioni non supportate di at.js.
>
>Il supporto del Compositore esperienza visivo per gli elementi personalizzati non è attualmente supportato con [Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md).

La maggior parte delle azioni del Compositore esperienza visivo è supportata su eventi personalizzati e all’interno di eventi personalizzati, con le seguenti eccezioni:

Le azioni seguenti non sono disponibili sugli elementi personalizzati:

* [!UICONTROL Modifica]
   * [!UICONTROL Testo/HTML]
   * [!UICONTROL Collegamento]
   * [!UICONTROL Modifica origine]

* [!UICONTROL Sostituisci contenuto]

L’azione seguente non è disponibile all’interno di elementi personalizzati:

* [!UICONTROL Layout]
   * [!UICONTROL Ridisponi]

## Navigare tra gli elementi utilizzando il percorso DOM {#dom-path}

Facendo clic su un elemento della pagina, viene visualizzato il menu delle opzioni del Compositore esperienza visivo. Inoltre, quando fai clic su un elemento, il percorso DOM corrispondente viene visualizzato nella parte inferiore della pagina.

![Percorso DOM](/help/c-experiences/c-visual-experience-composer/assets/dom-path.png)

Puoi utilizzare il percorso DOM per vedere rapidamente le informazioni sull’elemento selezionato (tipo, ID e classe) e spostarti verso l’alto o il basso nel percorso DOM per selezionare l’elemento desiderato.

Quando passi il cursore del mouse sul percorso DOM, una casella blu evidenzia l’elemento corrispondente nel Compositore esperienza visivo. Se fai clic sull’elemento, una casella arancione evidenzia l’elemento e viene visualizzato il menu delle opzioni del Compositore esperienza visivo, come illustrato in precedenza.

Utilizzando il percorso DOM, è possibile passare facilmente a qualsiasi elemento principale, di pari livello o secondario all’interno del Compositore esperienza visivo.

La funzione Percorso DOM è disponibile anche quando si imposta il [tracciamento dei clic](/help/c-activities/r-success-metrics/click-tracking.md).
