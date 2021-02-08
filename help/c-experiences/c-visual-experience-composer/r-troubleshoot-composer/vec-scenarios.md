---
keywords: Consigli
description: Esplora scenari comuni che mostrano come le modifiche apportate alla pagina in Visual Experience Composer (VEC) influiscono  capacità di Adobe Target di visualizzare un'esperienza.
title: Quali Sono Alcuni Scenari Di Modifica Di Pagina Comuni?
feature: Visual Experience Composer (VEC)
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 90%

---


# Scenari di modifica delle pagine

Gli scenari di questo argomento mostrano come le modifiche apportate alla pagina influiscono  capacità di Adobe Target di visualizzare un&#39;esperienza.

Il selettore di Target determina la posizione di visualizzazione di un’esperienza. Se una pagina viene modificata al di fuori di Target, le modifiche potrebbero influenzare la capacità di Target di visualizzare l’esperienza.

Quando si utilizza il selettore, la classe univoca non è equivalente all’ID. Il selettore funziona sempre con una classe univoca. Se all’elemento non è assegnata alcuna classe, il selettore calcola il numero di elementi di pari livello precedenti con lo stesso nome di tag.

>[!NOTE]
>
>Anche se questi scenari utilizzano voci di elenco come esempi, i concetti illustrati si applicano a qualsiasi elemento.

## Scenario: inserire un elemento con un nome di classe diverso prima dell’elemento selezionato {#section_298F661F72384F6AB957D5885A99D822}

In questo esempio, un nuovo elemento viene inserito come elemento di pari livello dell’elemento nel selettore di Target.

Esiste la possibilità che JavaScript aggiunga la prima classe presente nell’elemento. In tal caso, la consegna non riesce e l’azione non viene applicata.

**Elemento inserito:**

```html
<li class="kids-section">Kids</li>
```

**Selezionato:**

`<li class="women-section">Women</li>`

Selettore: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Risultato:**

Il selettore funziona come previsto perché `li.women-section:eq(0)` non è interessato.

Prima:

```html
<div id="wrap">
     <ul class="nav">
        <li class="men-section"> Men</li> <li class="women-section">Women</li>
     </ul> 
</div>
```

Dopo:

```html
<div id="wrap">
    <ul class="nav">
        <li class="kids-section">Kids</li>
        <li class="men-section"> Men</li>       <li class="women-section">Women</li>
    </ul> 
</div>
```

## Scenario: inserire un elemento con lo stesso nome di classe dell’elemento selezionato {#section_0969B88C2F154E648D9969C8C85EF55A}

In questo scenario, si tenta di inserire un elenco quando è selezionata una voce in un elenco.

**Elemento inserito:**

```html
<ul class="nav"> 
   <li class="item"> Sale </li> 
   <li> class="item"> Offers </li> 
</ul>
```

**Selezionato**

`<li class="women-section">Women</li>`

Selettore: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Risultato:**

Il selettore non funziona, perché `ul.nav:eq(0)` fornisce un elemento aggiunto in modo dinamico. L’elemento non sarà disponibile e l’azione non viene applicata. Se dopo aver creato un’attività aggiungi in modo dinamico o manuale un elemento elenco simile con la stessa classe, viene creato un nuovo elemento nella prima posizione. Questo impedisce il corretto funzionamento del selettore.

Prima:

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section"> Men</li>       <li class="women-section">Women</li>
    </ul> 
</div>
```

Dopo (tentativo):

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

## Scenario: inserire un elemento dopo l’elemento selezionato {#section_15B07B84BEE94ED39D85BBBE0733E170}

In questo scenario, una voce di elenco viene inserita dopo l’elemento selezionato.

**Elemento inserito:**

```html
<ul class="nav"> 
   <li class="men-section"> Men Clothes</li> 
   <li class="women-section"> Women Clothes</li> 
</ul>
```

**Selezionato:**

`<li class="women-section">Women Shoes</li>`

Selettore: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Risultato:**

In questo caso, l’inserimento di un elenco dopo quello che termina con la voce di elenco selezionata funziona come previsto. Il nuovo elemento viene aggiunto alla stessa posizione dell’elemento selezionato in relazione all’elemento padre.

Prima:

```html
<div id="wrap">
    <ul class="nav">
        <li class="men">Men Shoes </li>       <li class="women">Women Shoes</li>
    </ul>
</div>
```

Dopo:

```html
<div id="wrap">
    <ul class="nav">
        <li class="men">Men Shoes </li>
        <li class="women">Women Shoes</li>
    </ul>
      <ul class="nav">
        <li class="men-section">Men Clothes</li>
        <li class="women-section"> Women Clothes</li>
    </ul>
</div>
```

## Scenario: rimuovere l’elemento immediatamente precedente un altro {#section_F193674F04F84AA593EAA1137C880EBA}

In questo scenario, viene eliminata la voce di elenco che precede quella selezionata.

**Elemento rimosso:**

```html
<li class="men-section"> Men </li>
```

**Selezionato:**

`<li class="women-section">Women</li>`

Selettore: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Risultato:**

L’elemento viene rimosso correttamente perché la classe dell’elemento selezionato non viene modificata.

Prima:

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
    </ul>
</div>
```

Dopo:

```html
<div id="wrap">
    <ul class="nav">
        <li class="women-section">Women</li>
    </ul>
</div>
```

## Scenario: rimuovere l’elemento immediatamente successivo a un altro {#section_F83B51BE54924FB58679D512DAF1EBB2}

In questo scenario, viene eliminata la voce di elenco dopo l’elemento selezionato.

**Elemento rimosso:**

```html
<li class="kids-section">Kids</li>
```

**Selezionato:**

`<li class="women-section">Women</li>`

Selettore: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Risultato:**

L’elemento viene rimosso correttamente perché la classe dell’elemento selezionato non viene modificata. L’elemento rimosso include una classe univoca all’interno della relativa sottostruttura padre.

Prima:

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
        <li class="kids-section">Women</li>
    </ul>
</div>
```

Dopo:

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
    </ul>
</div>
```

## Scenario: rimuovere l’elemento selezionato {#section_1989CF1E2C344CC5963084ED83C18F9C}

In questo scenario, viene eliminata la voce di elenco selezionata.

**Elemento rimosso:**

```html
<li class="women-shoes">Women</li>
```

**Selezionato:**

`<li class="women-shoes">Women</li>`

Selettore: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Risultato:**

L’elemento viene rimosso correttamente.

Prima:

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-shoes">Women</li>
    </ul>
</div>
```

Dopo

```html
<div id="wrap">
    <ul class="nav">
       <li class="men-section">Men</li>
    </ul>
</div>
```

## Scenario: rinominare la classe dell’elemento selezionato {#section_79D244C588BA452DB8E433D82B7F63EA}

In questo scenario, viene modificata la classe della voce di elenco selezionata.

**Elemento modificato:**

```html
<li class="women-section">Women</li>
```

**Selezionato:**

`<li class="women-section">Women</li>`

Selettore: `#wrap > ul.nav:eq(0) > li.women-section:eq(0)`

**Risultato:**

La classe dell’elemento non può essere rinominata perché `class` non è stato trovato.

Prima:

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-section">Women</li>
    </ul>
</div>
```

Dopo (tentativo):

```html
<div id="wrap">
    <ul class="nav">
        <li class="men-section">Men</li>
        <li class="women-shoes">Women</li>
    </ul>
</div>
```
