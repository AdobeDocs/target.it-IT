---
keywords: Targeting delle esperienze;test pagina di destinazione
description: Un selettore di elementi è un’espressione CSS che può identificare uno o più elementi. Scopri come utilizzare i selettori di elementi nel Compositore esperienza visivo di Adobe [!DNL Target] .
title: Posso utilizzare i selettori di elementi nel Compositore esperienza visivo?
feature: Visual Experience Composer (VEC)
exl-id: f4ddb30a-f599-4fe5-861c-2deeeb9a70dd
source-git-commit: 52f11998149cddeb4245a0f07280562d79332a04
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 85%

---

# Selettori di elementi utilizzati nel Compositore esperienza visivo

Un selettore di elementi è un’espressione CSS che può identificare uno o più elementi.

Puoi trovare informazioni di base sui selettori CSS nel documento sui [selettori](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started/Selectors) in Mozilla Developer Network (MDN).

Puoi specificare se utilizzare l’ID o la classe degli elementi nelle preferenze dell’account. Fai clic su **[!UICONTROL Administration > Visual Experience Composer]**, quindi scegli i selettori CSS preferiti.

![immagine css_selectors](assets/css_selectors.png)

>[!NOTE]
>
>Le classi di elementi sono disponibili come selettori nelle attività per test A/B, Personalizzazione automatizzata e test multivariati.

Per informazioni su quando utilizzare selettori CSS e quando utilizzare ID univoci, consulta [Best practice e limitazioni del Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#concept_E284B3F704C04406B174D9050A2528A6).

## Come Adobe [!DNL Target] genera un selettore per un elemento {#section_D89D954BCBFB486CA081BE183776A475}

Target utilizza un semplice algoritmo per creare un selettore. Ecco una brevissima spiegazione della logica di generazione:

1. Se un elemento ha un ID, ad esempio `id="container"`, allora il selettore per l’elemento è `#container`.

   Ad esempio:

   ```html
   <div class="wrapper">
     <div id="container"> <!-- Selector is computed for this element -->
       <ul class="navigation">
         <li class="item active"> Home </li>
         <li class="item"> Men </li>
         <li class="item"> Women </li>
         <li class="item"> Kids </li>
       </ul>
     </div>
   </div>
   ```

1. Se un elemento contiene un attributo di classe, Target tenta di sfruttare la prima classe di qualsiasi classe presente nell’elemento.

   Target tenta di analizzare l’elemento padre fino a quando non trova l’elemento `<HTML>` o un elemento con un ID. Ogni volta che un elemento contiene un ID e il selettore viene calcolato sul suo discendente, l’ID di questo elemento contribuisce al selettore.

   Ad esempio:

   ```html
   <div class="wrapper">
     <div id="container"> <!-- id is present here. It contributes to selector -->
       <ul class="navigation">
         <li class="item active"> Home </li> <!-- Selector is computed for this element -->
         <li class="item"> Men </li>
         <li class="item"> Women </li>
         <li class="item"> Kids </li>
       </ul>
     </div>
   </div>
   ```

   In questo esempio:

   Selettore: `#container` > `ul.navigation:eq(0)` > `li.item:eq(0)` (“ > ” indica l’elemento figlio diretto).

   `eq` comunica all’indice che c’è un elemento con &quot;tagName=UL&quot; e che la prima classe è `navigation`. Pertanto, l’`index` è 0. Per ulteriori informazioni, leggi l’articolo sui [selettori](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started/Selectors) in MDN.

1. Se un elemento non contiene una classe, Target utilizza `tagName` per l’elemento ed analizza l’elemento padre fino a quando non viene trovato l’elemento `<HTML>` o un elemento con un ID.

   Ad esempio:

   ```html
   <div class="wrapper">
     <div id="container"> <!-- id is present here. It contributes to selector -->
       <ul class="navigation">
         <li> Home </li>
         <li> Men </li>
         <li class="active"> Women </li>
         <li> Kids </li><!-- Selector is computed for this element -->
       </ul>
     </div>
   </div>
   ```

   Selettore: `#container` > `ul.navigation(0)` > `li:nth-of-type(4)`

Nel processo sopra indicato:

* È possibile utilizzare qualsiasi selettore CSS purché identifichi in modo univoco un elemento nel DOM.
* L’approccio sopra indicato è quello utilizzato da Target. Target non impone di utilizzare questo approccio. È possibile aggiungere qualsiasi selettore purché il punto #1 sia rispettato.
* È possibile utilizzare qualsiasi attributo nel selettore. Questo documento utilizza solo il nome della classe come esempio.
