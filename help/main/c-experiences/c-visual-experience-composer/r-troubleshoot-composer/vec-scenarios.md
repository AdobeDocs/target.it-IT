---
keywords: Consigli
description: Esplora gli scenari comuni che mostrano come le modifiche apportate alla pagina nel Compositore esperienza visivo influiscono sulla capacità di Adobe Target di visualizzare un’esperienza.
title: Quali sono alcuni scenari comuni di modifica delle pagine?
feature: Visual Experience Composer (VEC)
exl-id: 7a05fbf9-3427-436e-a54f-4f1dd16d885a
TQID: 'https://experienceleague.adobe.com/BI2SnUU5ilCf0auld15q1rpCrnLoPEwbe1fZO6G1quc'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '626'
ht-degree: 4%
---
# Scenari di modifica delle pagine {#vec-scenarios}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri in che modo le modifiche apportate a una pagina al di fuori di [!DNL Target] influiscono sulla capacità di [!DNL Target] di visualizzare un&#39;esperienza, attraverso sette scenari con esempi.

>[!ENDSHADEBOX]

Il selettore [!DNL Target] determina dove viene visualizzata un&#39;esperienza. Quando una pagina viene modificata all&#39;esterno di [!DNL Target], le modifiche potrebbero influire sulla capacità di [!DNL Target] di trovare tale posizione e visualizzare l&#39;esperienza.

Il selettore funziona sempre con una classe univoca, che non è equivalente a un ID. Quando all&#39;elemento non viene assegnata alcuna classe, il selettore conta i pari livello precedenti che hanno lo stesso nome di tag.

>[!NOTE]
>
>Gli scenari utilizzano le voci di elenco come esempi, ma i concetti si applicano a qualsiasi elemento.

Nella tabella seguente sono riepilogati gli scenari. In ogni scenario, il selettore è `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`.

| Scenario | Azione applicata | Motivo |
|---|---|---|
| Inserisci un elemento con un nome di classe diverso prima dell’elemento selezionato | Sì | `li.women-section:eq(0)` non è interessato |
| Inserisci un elemento con lo stesso nome di classe dell’elemento selezionato | No | Un nuovo elemento prende la prima posizione, che interrompe il selettore |
| Inserisci un elemento dopo l’elemento selezionato | Sì | Il nuovo elemento viene aggiunto nella stessa posizione relativa all’elemento padre |
| Rimuovi l’elemento immediatamente precedente l’elemento selezionato | Sì | La classe dell&#39;elemento selezionato non viene modificata |
| Rimuovi l’elemento immediatamente successivo a quello selezionato | Sì | La classe dell&#39;elemento selezionato non viene modificata |
| Rimuovi l’elemento selezionato | Sì | L’elemento è stato rimosso correttamente |
| Rinomina la classe dell&#39;elemento selezionato | No | `class` non trovato |

## Inserisci un elemento con un nome di classe diverso prima dell’elemento selezionato

Un nuovo elemento viene inserito come elemento di pari livello nel selettore [!DNL Target]. Se la prima classe dell’elemento è stata aggiunta da JavaScript, la consegna non riesce e l’azione non viene applicata.

**Elemento inserito:**

```html
<li class="kids-section">Kids</li>
```

**Elemento selezionato:**

`<li class="women-section">Women</li>`

**Selettore:** `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Risultato:** Il selettore funziona come previsto, perché `li.women-section:eq(0)` non è interessato.

**Prima:**

```html
<div id="wrap">
     <ul class="nav">
        <li class="men-section"> Men</li> <li class="women-section">Women</li>
     </ul>
</div>
```

**Dopo:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="kids-section">Kids</li>
        <li class="men-section"> Men</li>       <li class="women-section">Women</li>
    </ul>
</div>
```

## Inserisci un elemento con lo stesso nome di classe dell’elemento selezionato

Quando si seleziona un elemento di un elenco, viene inserito un elenco.

**Elemento inserito:**

```html
<ul class="nav">
   <li class="item"> Sale </li>
   <li class="item"> Offers </li>
</ul>
```

**Elemento selezionato:**

`<li class="women-section">Women</li>`

**Selettore:** `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Risultato:** Il selettore non funziona. `ul.nav:eq(0)` ora fa riferimento a un elemento aggiunto in modo dinamico, che non è disponibile, pertanto l&#39;azione non viene applicata. L’aggiunta di una voce di elenco simile con la stessa classe, in modo dinamico o manuale, dopo la creazione dell’attività mette un nuovo elemento nella prima posizione, interrompendo il selettore.

**Prima:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section"> Men</li>       <li class="women-section">Women</li>
    </ul>
</div>
```

**Dopo (tentativo):**

```html
<div id="wrap">
     <ul class="nav">
        <li class="item"> Sale</li>
        <li> class="item"> Offers</li>
     </ul>
     <ul class="nav">
       <li class="men-section"> Men</li>
       <li class="women-section">Women</li>
    </ul>
</div>
```

## Inserisci un elemento dopo l’elemento selezionato

Dopo la voce di elenco selezionata viene inserito un elenco.

**Elemento inserito:**

```html
<ul class="nav">
   <li class="men-section"> Men Clothes</li>
   <li class="women-section"> Women Clothes</li>
</ul>
```

**Elemento selezionato:**

`<li class="women-section">Women Shoes</li>`

**Selettore:** `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Risultato:** l&#39;inserimento di un elenco dopo l&#39;elenco che termina con l&#39;elemento selezionato funziona come previsto. Il nuovo elemento viene aggiunto nella stessa posizione dell’elemento selezionato rispetto all’elemento padre.

**Prima:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men Shoes </li>       <li class="women-section">Women Shoes</li>
    </ul>
</div>
```

**Dopo:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men Shoes </li>
        <li class="women-section">Women Shoes</li>
    </ul>
      <ul class="nav">
        <li class="men-section">Men Clothes</li>
        <li class="women-section"> Women Clothes</li>
    </ul>
</div>
```

## Rimuovi l’elemento immediatamente precedente l’elemento selezionato

La voce di elenco prima dell’elemento selezionato viene eliminata.

**Elemento rimosso:**

```html
<li class="men-section"> Men </li>
```

**Elemento selezionato:**

`<li class="women-section">Women</li>`

**Selettore:** `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Risultato:** l&#39;elemento è stato rimosso correttamente perché la classe dell&#39;elemento selezionato non è stata modificata.

**Prima:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
    </ul>
</div>
```

**Dopo:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="women-section">Women</li>
    </ul>
</div>
```

## Rimuovi l’elemento immediatamente successivo a quello selezionato

La voce di elenco dopo l’eliminazione dell’elemento selezionato.

**Elemento rimosso:**

```html
<li class="kids-section">Kids</li>
```

**Elemento selezionato:**

`<li class="women-section">Women</li>`

**Selettore:** `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Risultato:** l&#39;elemento è stato rimosso correttamente perché la classe dell&#39;elemento selezionato non è stata modificata e l&#39;elemento rimosso ha una classe univoca all&#39;interno della relativa sottostruttura padre.

**Prima:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
        <li class="kids-section">Kids</li>
    </ul>
</div>
```

**Dopo:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
    </ul>
</div>
```

## Rimuovi l’elemento selezionato

La voce di elenco selezionata viene eliminata.

**Elemento rimosso:**

```html
<li class="women-section">Women</li>
```

**Elemento selezionato:**

`<li class="women-section">Women</li>`

**Selettore:** `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Risultato:** Rimozione dell&#39;elemento completata.

**Prima:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
    </ul>
</div>
```

**Dopo:**

```html
<div id="wrap">
    <ul class="nav">
       <li class="men-section">Men</li>
    </ul>
</div>
```

## Rinomina la classe dell&#39;elemento selezionato

La classe della voce di elenco selezionata viene modificata.

**Elemento modificato:**

```html
<li class="women-section">Women</li>
```

**Elemento selezionato:**

`<li class="women-section">Women</li>`

**Selettore:** `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Risultato:** Impossibile rinominare la classe perché `class` non è stato trovato.

**Prima:**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
    </ul>
</div>
```

**Dopo (tentativo):**

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-shoes">Women</li>
    </ul>
</div> 
```
