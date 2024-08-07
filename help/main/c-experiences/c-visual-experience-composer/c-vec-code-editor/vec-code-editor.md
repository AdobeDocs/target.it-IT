---
keywords: selettore css;codice personalizzato;editor di codice;Mobile Web Experience Editor
description: Scopri come utilizzare il pannello Modifiche nell’Adobe  [!DNL Target]  per visualizzare le modifiche apportate alla pagina e aggiungere ulteriori modifiche (selettore CSS, Mbox e codice personalizzato).
title: Quali modifiche è possibile apportare alla pagina?
feature: Visual Experience Composer (VEC)
exl-id: 23456a4b-9457-4f05-989e-a7c39ce17cc2
source-git-commit: e458793e4d0110d97f3f5124cbe6e54520d3f0e9
workflow-type: tm+mt
source-wordcount: '2207'
ht-degree: 72%

---

# Modifiche

Informazioni sulla pagina [!UICONTROL Modifications] in [!DNL Adobe Target] che consente di visualizzare le modifiche apportate alla pagina e di aggiungere ulteriori modifiche (selettore CSS, Mbox e codice personalizzato).

La pagina [!UICONTROL Modifications] mostra tutte le modifiche apportate alla pagina nel Compositore esperienza visivo e consente di apportare ulteriori modifiche facendo clic su ogni elemento della pagina e [selezionando un&#39;azione](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81). Ogni modifica apportata viene visualizzata come un&#39;azione o un elemento separato nell&#39;elenco [!UICONTROL Modifications]. Puoi anche aggiungere modifiche, compresi i seguenti tipi di modifica: Selettore CSS, Mbox. e Codice personalizzato.

## Panoramica sulle modifiche {#section_EE27E7572AA74397BBDED563B2B3D509}

La pagina [!UICONTROL Modifications] mostra tutte le modifiche apportate alla pagina nel Compositore esperienza visivo. Ogni modifica apportata viene visualizzata come un&#39;azione o un elemento separato nell&#39;elenco [!UICONTROL Modifications].

![immagine codeeditor_page_mods](assets/codeeditor_page_mods.png)

Utilizza la pagina Modifiche per apportare piccole modifiche al selettore scelto da Target quando utilizzi il Compositore esperienza visivo per configurare il modo in cui viene distribuito il contenuto. È possibile modificare sia il contenuto che un attributo HTML. È inoltre possibile modificare il codice per creare l&#39;equivalente di un&#39;offerta HTML all&#39;interno di una mbox.

Utilizza la pagina Modifiche per:

* Visualizzare un&#39;azione intrapresa nel compositore visivo.

  ![immagine codeeditor_viewchange](assets/codeeditor_viewchange.png)

* Modificare un&#39;azione esistente. Passa il puntatore del mouse sulla modifica desiderata, quindi fai clic sull&#39;icona **[!UICONTROL Edit]**.

  ![immagine codeeditor_edit](assets/codeeditor_edit.png)

  Apporta le modifiche.

  ![immagine codeeditor_changechange1](assets/codeeditor_changechange1.png)

* Elimina un&#39;azione esistente. Passa il puntatore del mouse sulla modifica desiderata, quindi fai clic sull&#39;icona **[!UICONTROL Delete]**.

  ![immagine codeditor_delete](assets/codeditor_delete.png)

* Aggiungi una nuova modifica. Fai clic su **[!UICONTROL Add Modification]** o sull&#39;icona +, quindi specifica le modifiche come descritto di seguito.

  ![codeeditor_nuova immagine](assets/codeeditor_new.png)

  Dopo la creazione di una modifica, Target visualizza un&#39;icona + nella parte superiore del pannello Modifiche, invece che nel pulsante Aggiungi modifica nella parte inferiore del pannello.

* Ancora il pannello Modifiche in verticale lungo il lato dell’interfaccia di Target oppure in orizzontale lungo il bordo inferiore. Fai clic sull&#39;icona [!UICONTROL Dock] per passare da una impostazione all&#39;altra.

  ![immagine codeditor_dock](assets/codeditor_dock.png)

  Nella figura seguente viene illustrato il pannello Modifiche ancorato nella parte inferiore dello schermo:

  ![immagine codeeditor_dock_bottom](assets/codeeditor_dock_bottom.png)

## Aggiungere modifiche {#section_C7ABCD5731A048CB8F90EDC31A32EDF9}

1. Per visualizzare la pagina [!UICONTROL Modifications] per un&#39;esperienza selezionata, nel Compositore esperienza visivo fai clic sull&#39;icona **[!UICONTROL Modifications]** &lt;/>.

   ![immagine codeeditor_icon_big](assets/codeeditor_icon_big.png)

   >[!NOTE]
   >
   >Per aprire il pannello Modifiche nel Compositore esperienza basato su modulo, crea o modifica un’offerta HTML. Per ulteriori informazioni, consulta [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E).

   Viene visualizzata la pagina [!UICONTROL Modifications], che suddivide lo schermo tra la modalità visiva a sinistra e il pannello Modifiche a destra. Fai clic sull&#39;icona [!UICONTROL Dock] per ancorare il pannello Modifiche in verticale lungo il lato dell&#39;interfaccia utente di Target o in orizzontale nella parte inferiore. Nota che l&#39;esperienza A nella figura seguente non ha modifiche precedenti.

   ![immagine codeeditor_page](assets/codeeditor_page.png)

   L&#39;esperienza B mostra le modifiche precedenti nel pannello [!UICONTROL Modifications] a destra.

   ![immagine codeeditor_page_mods](assets/codeeditor_page_mods.png)

1. Per aggiungere una modifica:

   * Se non è stata apportata alcuna modifica precedente, fare clic sul pulsante **[!UICONTROL Add Modification]** nella parte inferiore del pannello [!UICONTROL Modifications] sul lato destro.
   * Se sono presenti modifiche precedenti per l&#39;esperienza, fai clic sull&#39;icona + nella parte superiore del pannello [!UICONTROL Modifications] a destra.

   Il pannello Modifiche visualizza:

   ![codeeditor_page_mods_add immagine](assets/codeeditor_page_mods_add.png)

1. Dall&#39;elenco a discesa **[!UICONTROL Modifications Type]**, scegliere il tipo desiderato:

   | Tipo di modifica | Dettagli |
   |--- |--- |
   | Selettore CSS | Nella casella Selettore elemento CSS, specifica l&#39;elemento CSS che desideri modificare, seleziona un tipo di azione (Imposta contenuto o Imposta attributo), quindi compila le informazioni richieste e il contenuto desiderato. |
   | Mbox | Specifica il nome mbox e il contenuto desiderato.<p>**Nota**: le mbox non sono più supportate nel Compositore esperienza visivo nelle pagine che utilizzano at.js 2.*x*.<p>Come soluzioni alternative:<ul><li>Se utilizzi at.js 2.*x*, aggiungi una modifica al selettore CSS invece di una modifica Mbox e aggiungi il contenuto al selettore che la mbox stava utilizzando. </li><li>Utilizzare attività basate su moduli (funziona con mbox e at.js 1.*x* che in at.js 2.*x*).</li><li>Utilizzare at.js 1.*x* nel Compositore esperienza visivo.</li></ul> |
   | Codice personalizzato | Specificare un nome facoltativo, selezionare o deselezionare la casella di controllo [!UICONTROL Add Code in the `<HEAD>` sezione], quindi aggiungere il codice personalizzato.<p>Se si seleziona [!UICONTROL Add Code in the `<HEAD>` sezione], il codice personalizzato viene aggiunto alla sezione `<head>` e l&#39;esecuzione non attende il corpo o eventi di caricamento della pagina. Aggiungi solo gli elementi `<script>` e `<style>`. L’aggiunta di tag `<div>` e di altri elementi potrebbe causare la comparsa di elementi `<head>` rimanenti nel `<body>`. Se utilizzi at.js, tutte le offerte verranno consegnate in modo asincrono.<p> Se si deseleziona la sezione [!UICONTROL Add Code in the `<HEAD>`], il codice personalizzato viene eseguito subito dopo il tag `<body>`. Racchiudi tutto il codice in un unico `<div>` per conservare la struttura DOM. Se utilizzi at.js, tutte le offerte verranno consegnate in modo asincrono.<p>Se HTML per `<BODY>` contiene `<SCRIPT>` e `<DIV>`, `<DIV>` viene aggiunto a `<BODY>` e `<SCRIPT>` viene eseguito in `<HEAD>`. Inoltre, `<SCRIPT>` che carica un file esterno viene aggiunto a `<HEAD>`.<p>**Nota**: gli script vengono eseguiti in modo asincrono. Ciò significa che non è possibile, ad esempio, utilizzare `document.write` o metodi di scripting simili.<p>Il codice personalizzato fornisce un&#39;interfaccia non visiva per visualizzare, modificare e aggiungere nuove azioni nel Compositore esperienza visivo, nel Compositore esperienza basato su moduli e nell&#39;editor di offerte HTML. Il pannello fornisce una visualizzazione del codice di un&#39;esperienza e facilita la creazione di esperienze più complesse, l&#39;ottimizzazione di quelle esistenti e la risoluzione di problemi.<p>Il codice personalizzato è destinato agli utenti avanzati che hanno dimestichezza con HTML, JavaScript e CSS. La visualizzazione codice consente di modificare o perfezionare le modifiche o correggere i problemi del selettore. Può inoltre essere utilizzato per aggiungere nuove azioni e un codice personalizzato. È possibile aggiungere più di un codice personalizzato e facoltativamente assegnare un nome a ciascuno di essi.<p>**Nota**: il codice personalizzato è attualmente disponibile solo per attività A/B e per l&#39;esperienza di targeting (XT). Il codice personalizzato è disabilitato in caso di sovrapposizione e se viene applicata un&#39;offerta di reindirizzamento.<p>Il codice personalizzato supporta i seguenti casi di utilizzo:<ul><li>Aggiunta di JavaScript, HTML o CSS personalizzati da eseguire nella parte superiore della pagina</li><li>Visualizzazione o modifica del codice generato dal Compositore esperienza visivo dopo aver apportato modifiche</li><li>Impostazione del contenuto HTML per un selettore (solo selettore CSS)</li><li>Impostazione di un attributo su un elemento HTML</li><li>Aggiunta di contenuto dell&#39;offerta da consegnare in una mbox regionale</li><li>Scambio su DOM-ready, utilizzando jQuery</li><li>Scambio su DOM-ready, non jQuery (non supporta Internet Explorer 8)</li><li>Scambio con meccanismo DOM tramite plug-in “elementOnLoad”</li><li>Reindirizzamento personalizzato</li></ul>Il codice personalizzato fornisce:<ul><li>Numeri di linea per un migliore uso.</li><li>Colorazione della sintassi che consente di evitare errori di sintassi nelle offerte HTML.</li><li>La possibilità di creare più codici personalizzati e fornire un nome facoltativo per ciascuno di essi. La creazione di più codici personalizzati semplifica il debug futuro. Invece di creare un codice personalizzato per eseguire diverse modifiche, puoi creare un codice personalizzato distinto per ogni modifica con un nome descrittivo. L&#39;uso di codici personalizzati separati rende le modifiche più modulari e gestibili. Tieni presente che l&#39;esecuzione di più codici personalizzati in un&#39;attività non è garantita nella sequenza in cui sono stati creati.</li></ul>Il pannello Modifiche suddivide lo schermo tra la modalità visiva e la modalità codice. Entrambe le modalità rimangono sincronizzate. Ogni modifica apportata visivamente ha una riga corrispondente nella vista Codice. Allo stesso modo, ogni modifica inserita nella vista Codice viene visualizzata nell&#39;esperienza visiva. Facendo clic su una qualsiasi riga della vista Codice, viene selezionato l&#39;elemento corrispondente nella pagina visiva.<p>Il codice personalizzato supporta HTML, script e stili. Qualsiasi codice HTML o script valido può essere aggiunto o modificato. |

1. Aggiungi ulteriori modifiche in base alle esigenze.

## Casi di utilizzo del codice personalizzato {#section_26CB3360097D400FB02E20AE5FDBA352}

Il pannello **[!UICONTROL Custom Code]** contiene codice eseguito all&#39;inizio del caricamento della pagina.

Puoi eseguire il codice JavaScript nel tag `<head>`. L’esecuzione del codice non attende che il tag `<body>` sia presente nel DOM.

I selettori per le azioni visive successive dipendono dagli elementi HTML aggiunti in questa scheda.

Il pannello Codice personalizzato viene comunemente utilizzato per aggiungere JavaScript o CSS all&#39;inizio della pagina.

![immagine codeeditor_custom](assets/codeeditor_custom.png)

Utilizzare la scheda **[!UICONTROL Custom Code]** per:

* Utilizzare JavaScript in linea o per un collegamento a un file JavaScript esterno

  Ad esempio, per modificare il colore di un elemento:

  ```javascript
  <script type="text/javascript"> 
  document.getElementById("element_id").style.color = "blue"; 
  </script> 
  ```

* Configurare uno stile in linea o un collegamento a un foglio di stile esterno

  Ad esempio, per definire una classe per un elemento sovrapposto:

  ```html
  <style> 
  .overlay 
  { position: absolute; top:0; left: 0; right: 0; bottom: 0; background: red; } 
  </style> 
  ```

* Aggiungere frammenti HTML per definire nuovi elementi

  Ad esempio, utilizza il seguente frammento HTML per creare una sovrapposizione `<div>` utilizzando la classe CSS definita sopra:

  ```html
  <div class="overlay"></div>
  ```

* Scambio su DOM-ready, utilizzando jQuery

  L&#39;esempio seguente, che utilizza JQuery, presuppone che il sito Web del cliente abbia jQuery disponibile sulla pagina quando [!DNL Target] esegue le offerte.

  ```javascript
  <style>#default_content {visibility:hidden;}</style> 
  <script> 
  jQuery( document ).ready(function() { 
      jQuery("#default_content").html( "<span style='color:red'>Hello <strong>Again</strong></span>" ); 
      jQuery("#default_content").css("visibility","visible"); 
  }); 
  </script> 
  ```

* Scambio su DOM-ready, non jQuery (non supporta Internet Explorer 8)

  ```javascript
  <style>#default_content {visibility:hidden;}</style> 
  <script> 
  document.addEventListener("DOMContentLoaded", function(event) {  
      document.getElementById("default_content").innerHTML = "<span style='color:red'>Hello <strong>Again</strong></span>"; 
      document.getElementById("default_content").style.visibility="visible"; 
  }); 
  </script> 
  ```

* Reindirizzamento personalizzato passando parametri esistenti, parametro `s_tnt` (per l&#39;integrazione legacy di Analytics), parametri di riferimento e sessione mbox

  ```javascript
  <style type="text/css">body{display:none!important;}</style> 
  <script type="text/javascript"> 
   var qs='';window.location.search?qs=window.location.search+'&':qs='?'; 
   window.location.replace('//www.mywebsite.com/'+qs+'s_tnt=${campaign.id}:${campaign.recipe.id}:${campaign.recipe.trafficType}&s_tntref='+encodeURIComponent(document.referrer)+'&mboxSession='+mboxFactoryDefault.getSessionId().getId()+''+window.location.hash+''); 
  </script> 
  ```

* Aggiungi i modelli Adobe Target Experience per il codice personalizzato. I modelli di esperienza di Target sono esempi precodificati con input configurabili da utilizzare per casi di utilizzo ricorrenti per gli addetti al marketing. Questi modelli di esperienza sono disponibili gratuitamente per gli sviluppatori e i rivenditori come punto di partenza per eseguire alcuni casi comuni di utilizzo esterno in Adobe Target (tramite il Compositore esperienza visivo o il Compositore esperienza basato su modulo). I casi di utilizzo includono lightbox, giostre, countdown e altro ancora.

  Per ulteriori informazioni, vedere [Modelli di esperienza](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/experience-templates.md#concept_109BBD7EABC04DD39E6B7B1687786652).

## Tecniche consigliate per il codice personalizzato {#section_10DFFD9FB92A43C1BB444A45E0272B28}

**Racchiudi sempre il codice personalizzato in un elemento.**

Ad esempio:

```html
<div id="custom-code"> 
// My Code goes here 
</div>
```

Nel caso in cui siano necessarie modifiche, apporta modifiche all&#39;interno di questo contenitore.

Se non è più necessario il codice personalizzato, è sufficiente lasciare vuoto questo contenitore, ma non rimuoverlo. Ciò assicura che altre modifiche di esperienza non siano influenzate.

**Non utilizzare l&#39;ID elemento “CDQID” per apportare modifiche alla pagina eseguita nell&#39;editor di codice.**

Target applica un nuovo ID elemento con il valore “CDQID” a qualsiasi elemento della pagina modificato da Target. Poiché questo ID viene applicato da Target, non deve essere utilizzato per ulteriori modifiche o regolazioni nell&#39;editor di codice.

**Non eseguire azioni document.write negli script di codice personalizzati.**

Gli script vengono eseguiti in modo asincrono. Questo causa spesso la comparsa delle azioni `document.write` nel punto sbagliato della pagina. L&#39;utilizzo di `document.write` negli script creati nel codice personalizzato non è consigliato.

**Se crei un elemento e quindi lo modifichi, non eliminare l&#39;elemento originale.**

Ogni modifica crea un nuovo elemento nel pannello Modifiche. La seconda azione modifica l&#39;elemento 1: se lo elimini, questa azione non avrà più niente da modificare, risultando nella mancata applicazione della modifica. Per ulteriori informazioni, consulta “Risoluzione dei problemi”.

**Presta attenzione se utilizzi la funzionalità di codice personalizzato per due attività con targeting allo stesso URL.**

Se utilizzi la funzione codice personalizzato per due attività con targeting allo stesso URL, JavaScript viene integrato nella pagina da entrambe le attività. Target determina automaticamente l&#39;ordine del contenuto recapitato. Assicurati che il codice non dipenda dal posizionamento. Spetta a te verificare che non vi siano conflitti nel codice.

## Risoluzione dei problemi del codice personalizzato {#section_6C965CBC31C348D7AA5B57B63DAB9E7F}

**Il codice personalizzato non viene eseguito quando si utilizza `triggerView`.**

Le offerte di codice personalizzato nel Compositore esperienza visivo non vengono sottoposte nuovamente a rendering quando `triggerView()` viene chiamato con `{page: false}` come opzione.

**Ho ricevuto un avviso rispetto al fatto che un&#39;azione non può essere applicata a causa di modifiche strutturali a una pagina. Cosa significa?**

Questo messaggio indica che la struttura della pagina è cambiata dall&#39;ultimo salvataggio dell&#39;attività.

I selettori mancanti potrebbero essere raggiunti utilizzando la modalità Sfoglia. È consigliabile eliminare e quindi ricreare ogni esperienza per assicurarsi che il contenuto venga visualizzato come previsto, come indicato nel messaggio di avviso.

![immagine code_editor_2](assets/code_editor_2.png)

***Quando elimino un elemento, viene visualizzato un avviso che indica che &quot;L&#39;eliminazione di questa azione può influire sulle azioni successive.&quot; Cosa significa?***

Ad esempio, supponiamo che tu abbia eseguito due azioni:

* Aggiunta di una classe all&#39;elemento 1
* Modifica del codice HTML dell&#39;elemento 1

Ogni modifica crea un nuovo elemento nel pannello Modifiche. La seconda azione modifica l&#39;elemento 1: se lo elimini, la seconda azione non avrà più niente da modificare, risultando nella mancata applicazione della modifica.

In altre parole, se aggiungi un elemento con testo e modifichi tale elemento con un testo diverso in un&#39;azione separata, il pannello Modifiche mostrerà entrambe le azioni come elementi distinti. Durante la modifica dell&#39;elemento è stato creato un nuovo elemento, contenente il testo modificato, che modifica l&#39;elemento originale creato. Se elimini l&#39;elemento originale, il testo modificato non sarà in grado di trovare l&#39;elemento modificato e non verrà visualizzato. Il secondo elemento rimarrà nell&#39;elenco senza tuttavia influire sulla pagina, poiché l&#39;elemento da modificare non esiste più.

***Un elemento creato utilizzando `document.write` in uno script non viene visualizzato dove previsto.***

Gli script vengono eseguiti in modo asincrono. Questo causa spesso la comparsa delle azioni `document.write` nel punto sbagliato della pagina. Adobe consiglia di non utilizzare `document.write` negli script creati nel codice personalizzato.

***Il mio JavaScript visualizza gli errori nel codice personalizzato.***

Qualsiasi JavaScript in linea che non è un JavaScript valido mostra gli errori nel codice personalizzato.

***Impossibile annullare una modifica nel codice personalizzato.***

Attualmente, l&#39;annullamento non è supportato per le azioni di modifica ed eliminazione dal pannello Modifiche e nel codice personalizzato. L&#39;annullamento di una di queste operazioni potrebbe comportare l&#39;incoerenza dell&#39;esperienza con le azioni effettive visibili nel codice personalizzato all&#39;interno del Compositore esperienza visivo. Tuttavia, le azioni nel codice personalizzato sono nello stato corretto e non vi è alcuna conseguenza sulla consegna. Questo è un problema di interfaccia utente. Per aggiornare l&#39;esperienza, salvarla e riaprirla, oppure andare al passaggio successivo e tornare indietro. Una di queste azioni ricarica l&#39;esperienza e quindi viene visualizzata come previsto ed è coerente con le azioni nel pannello Modifiche.

**Il codice personalizzato non produce i risultati previsti in Internet Explorer 8.**

Target non supporta più IE8.
