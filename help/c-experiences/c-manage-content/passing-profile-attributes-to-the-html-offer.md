---
description: Potete visualizzare i valori di profilo e le informazioni sull'attività direttamente in un'offerta HTML o JSON.
keywords: dati dinamici; risorse; dati; offerte; offerte personalizzate; offerte personali; sostituzione token
seo-description: Potete visualizzare i valori di profilo e le informazioni sull'attività direttamente in un'offerta HTML o JSON.
seo-title: Trasmettere i dati dinamici nelle offerte
solution: Target
title: Trasmettere i dati dinamici nelle offerte
topic: Premium
uuid: 1910a7f5-e4bd-413a-9875-e0b005407f50
translation-type: tm+mt
source-git-commit: bdbdc98949b4b678b04d1dd2b772e8ffd5975e4b

---


# Trasmettere i dati dinamici nelle offerte{#pass-dynamic-data-into-offers}

Potete visualizzare in modo dinamico le informazioni dei visitatori memorizzate nel profilo di Target. Analogamente, anche le informazioni relative all&#39;attività (come il nome dell&#39;attività o il nome dell&#39;esperienza) possono essere utilizzate anche per creare una singola offerta in grado di restituire dinamicamente contenuti personalizzati in base agli interessi del visitatore, al comportamento passato e al profilo complessivo.

**Casi di business**

* Promuovere un&#39;offerta scontata per «ridisporre» o «ricostituire» l&#39;ultimo prodotto acquistato. Invece di creare un&#39;offerta separata per ogni elemento del catalogo, potete creare un&#39;offerta con testo dinamico che legge l &#39;«ultimo prodotto acquistato» dal profilo e visualizza un collegamento nell&#39;offerta.
* Un visitatore arriva sulla pagina di destinazione con `keyword=world` `cup`. Mostra il termine *World cup* nell&#39;offerta.
* Personalizzate un&#39;etichetta di Recommendations con informazioni come (1) l&#39;ultimo elemento aggiunto al carrello di un visitatore (Nike Air Max 1000 s), (2) la preferenza colore del visitatore (nero) e (3) la categoria non stampabile preferita dal visitatore (hoodies). Esempio: &quot; Accedete a «Nike Air Max 1000 s» con questi cool&#39;black &#39;&#39;hoodies &#39;!»


**Vantaggi tecnici**

Dato che preferenze, comportamenti, stato e così via specifici per l&#39;utente possono essere memorizzati nel profilo dell&#39;utente, è possibile ripetere questo messaggio nelle visite successive. Le offerte dinamiche consentono una maggiore scala consentendo di configurare una singola offerta all&#39;interno di un&#39;attività che visualizza messaggi personalizzati per tutti i visitatori. Quando l&#39;intento del visitatore cambia, il contenuto del sito Web riflette automaticamente tali modifiche.

**Esempio**

* `mboxCreate("landingpage"`, `"profile.keyword=World Cup");`

* Codice offerta HTML: `Get your ${profile.keyword} information here!`
* L&#39;utente vede: Get your World Cup information here!

I seguenti valori possono essere “sostituiti tramite token”:

| Valori | Esempi |
|--- |--- |
| Parametri di profilo in-mbox | `${profile.age}` |
| Parametri di profilo script | `${user.lifetimeSpend}` |
| Parametri mbox | `${mbox.favoriteColor}` |
| Informazioni sulla campagna | `${campaign.name}`, `${campaign.recipe.name}`, `${campaign.id}`, `${campaign.recipe.id}`, e `${campaign.recipe.trafficType}` |
| ID visitatore univoco | `${user.pcId}` |
| ID di sessione univoco | `${user.sessionId}` |
| Prima sessione del visitatore (vero o falso) | `${user.isFirstSession}` |
| Comportamento passato | `${user.endpoint.lastPurchasedEntity}`, `${user.endpoint.lastViewedEntity}`, `${user.endpoint.mostViewedEntity}`, `${user.endpoint.categoryAffinity}` |

Log information in the console for debugging purposes, such as `${campaign.name}`, `${campaign.id}`, `${campaign.recipe.name}`, `${campaign.recipe.id}`, `${offer.name}`, `${offer.id}`, `${campaign.name}`

Per le progettazioni di Recommendations, consultate Altri esempi in [Panoramica progettazione](/help/c-recommendations/c-design-overview/design-overview.md).

**Implementazione**

Per i parametri di profilo passati in una mbox, utilizzate la sintassi: `${profile.parameter}` Per i parametri di profilo creati in uno script di profilo, utilizzate la sintassi:

`${user.parameter}`

Quando utilizzate gli attributi dinamici in una progettazione di Recommendations, dovete inserire una barra rovesciata (&#39;\&#39;) prima del simbolo del dollaro (&#39;$&#39;) per rendere il valore dinamico corretto: `\${user.endpoint.lastViewedEntity}`

Queste variabili sono sostituite con il valore sul lato server, quindi nessuna virgoletta o altro JavaScript è necessario per la visualizzazione corretta.

Puoi inoltre specificare i valori predefiniti se desideri esporli alle offerte. La sintassi è simile alla seguente:

`${user.testAttribute default="All Items!"}`

Quando `testAttribute` non esiste o è vuoto, verrà scritto “All Items!” Se un valore di attributo vuoto è valido e desideri scriverlo anziché visualizzare l&#39;impostazione predefinita, puoi utilizzare:

`${user.testAttribute default="All Items!" show_blank="true"}`

Puoi inoltre usare le funzioni escape e unescape per visualizzare i valori. Se il valore ha un apostrofo, ad esempio, potrai applicare ad esso la funzione escape in modo da non rompere JavaScript sulla pagina. (Le offerte sono scritte in JavaScript, quindi un singolo apostrofo può essere confuso per virgolette.) Ad esempio:

`${user.encodedValue encode="unescape"}`

`${user.unencodedValue encode="escape"}`