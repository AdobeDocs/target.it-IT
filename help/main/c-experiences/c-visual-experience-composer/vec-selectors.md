---
keywords: Targeting delle esperienze;test pagina di destinazione
description: Un selettore di elementi è un’espressione CSS che può identificare uno o più elementi. Scopri come utilizzare i selettori di elementi nel Compositore esperienza visivo di Adobe [!DNL Target].
title: Posso utilizzare i selettori di elementi nel Compositore esperienza visivo?
feature: Visual Experience Composer (VEC)
exl-id: f4ddb30a-f599-4fe5-861c-2deeeb9a70dd
TQID: 'https://experienceleague.adobe.com/sqvUyLFddt7HPHH62jwpOZmwTIMSg-hyLIUr8w-x7vg'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 4%
---
# Selettori di elementi utilizzati nel [!UICONTROL Compositore esperienza visivo] {#vec-selectors}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come funzionano i selettori di elementi nel [!UICONTROL Compositore esperienza visivo] (VEC), come scegliere quali selettori utilizzare e come [!DNL Target] genera un selettore per un elemento.

>[!ENDSHADEBOX]

Un selettore di elementi è un’espressione CSS che può identificare uno o più elementi. Le informazioni di base sui selettori CSS sono disponibili nel documento [Selettori](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started/Selectors) in *[!DNL Mozilla Developer Network]* (MDN).

L’utilizzo delle classi di elementi o degli ID di elementi è impostato nelle preferenze dell’account. Fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Compositore esperienza visivo]**, quindi scegli i selettori CSS preferiti:

* **[!UICONTROL Usa ID elemento]**: disabilita se lo stesso ID viene utilizzato per più elementi o se gli ID degli elementi potrebbero cambiare al caricamento della pagina.
* **[!UICONTROL Usa classi elemento]**: disabilita se le classi elemento in una pagina potrebbero cambiare.
* **[!UICONTROL Usa selettori preferiti]**: abilita l&#39;utilizzo di selettori univoci nel Compositore esperienza visivo per identificare aree chiave del sito Web.

>[!NOTE]
>
>Le classi di elementi sono disponibili come selettori nelle attività **[!UICONTROL Test A/B]**, **[!UICONTROL Automated Personalization]** e **[!UICONTROL Test multivariato]**.

Per informazioni su quando utilizzare selettori CSS e quando utilizzare ID univoci, consulta [Best practice e limitazioni del Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#vec-best-practices).

## Come [!DNL Target] genera un selettore per un elemento {#generate-selector}

[!DNL Target] utilizza un algoritmo semplice per creare un selettore. La logica di generazione è la seguente:

1. Se un elemento ha un ID, ad esempio `id="container"`, il selettore per l&#39;elemento è `#container`.

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

1. Se un elemento contiene un attributo di classe, [!DNL Target] tenta di utilizzare la prima classe di qualsiasi classe presente nell&#39;elemento.

   [!DNL Target] tenta di analizzare l&#39;elemento padre finché non trova l&#39;elemento `<HTML>` o un elemento con un ID. Ogni volta che un elemento contiene un ID e il selettore viene calcolato sul relativo figlio discendente, l’ID di questo elemento contribuisce al selettore.

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

   In questo esempio, il selettore è `#container` > `ul.navigation:eq(0)` > `li.item:eq(0)` (&quot; > &quot; indica l&#39;elemento figlio diretto).

   `eq` fornisce l&#39;indice dell&#39;elemento che ha &quot;tagName=UL&quot; e la prima classe `navigation`. Pertanto, l’`index` è 0. Per ulteriori informazioni, leggi l’articolo sui [selettori](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started/Selectors) in MDN.

1. Se un elemento non contiene una classe, [!DNL Target] utilizza `tagName` per l&#39;elemento ed analizza l&#39;elemento padre finché non viene trovato l&#39;elemento `<HTML>` o un elemento con un ID.

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

   Il selettore è `#container` > `ul.navigation:eq(0)` > `li:nth-of-type(4)`.

In questo processo:

* È possibile utilizzare qualsiasi selettore CSS, purché identifichi in modo univoco un elemento nel DOM.
* L&#39;approccio sopra riportato è quello utilizzato da [!DNL Target]. [!DNL Target] non rende obbligatorio questo approccio. È possibile aggiungere qualsiasi selettore, purché identifichi l’elemento in modo univoco.
* Qualsiasi attributo può essere utilizzato nel selettore. Questo articolo utilizza solo un nome di classe come esempio.
