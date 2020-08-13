---
keywords: dynamic data;assets;data;offers;personalized offers;personal offers;token replace
description: Puoi visualizzare i valori dei profili e le informazioni sull’attività direttamente in un’offerta HTML o JSON.
title: Trasmettere i dati dinamici nelle offerte
feature: offers
uuid: 1910a7f5-e4bd-413a-9875-e0b005407f50
translation-type: tm+mt
source-git-commit: 3cf1f4fa56f86c106dccdc2c97c080c17c3982b4
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 100%

---


# Trasmettere i dati dinamici nelle offerte{#pass-dynamic-data-into-offers}

Puoi visualizzare in modo dinamico le informazioni dei visitatori memorizzate nel profilo Target. Analogamente, le informazioni relative all’attività (come il nome dell’attività o dell’esperienza) possono inoltre essere utilizzate per creare una singola offerta in grado di restituire in modo dinamico contenuti personalizzati in base agli interessi del visitatore, al comportamento passato e al profilo complessivo.

**Casi aziendali**

* Promuovere un’offerta scontata per un acquisto relativo all’ultimo prodotto acquistato. Invece di creare un’offerta separata per ogni elemento del catalogo, puoi creare un’offerta con testo dinamico che visualizza “l’ultimo prodotto acquistato” dal profilo insieme a un collegamento nell’offerta.
* Un visitatore arriva sulla pagina di destinazione con `keyword=world` `cup`. Mostra il termine *World cup* nell&#39;offerta.
* Personalizza un’etichetta di consigli con informazioni come (1) l’ultimo elemento aggiunto al carrello di un visitatore (Nike Air Max 1000), (2) la preferenza colore del visitatore (nero) e (3) la categoria non relativa alla scarpa preferita dal visitatore (felpe). Esempio: “Abbina a “Nike Air Max 1000” queste fantastiche “felpe” “nere””.


**Vantaggi tecnici**

Poiché le preferenze, i comportamenti, gli stati specifici dell’utente possono essere memorizzati nel profilo utente, puoi ripetere questo messaggio nelle visite successive. Le offerte dinamiche consentono una maggiore estensione: ti permettono infatti di configurare una singola offerta all’interno di un’attività che visualizza messaggi personalizzati per tutti i visitatori. Il contenuto del sito Web si aggiorna automaticamente per riflettere i cambiamenti nell’intento del visitatore.

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

Registra le informazioni nella console per scopi di debug, come `${campaign.name}`, `${campaign.id}`, `${campaign.recipe.name}`, `${campaign.recipe.id}`, `${offer.name}`, `${offer.id}`, `${campaign.name}`

Consulta ulteriori esempi in [Panoramica della progettazione](/help/c-recommendations/c-design-overview/design-overview.md) per progetti Consigli.

**Implementazione**

Per i parametri di profilo trasmessi in una mbox, utilizza la sintassi: `${profile.parameter}`; per i parametri di profilo creati in uno script di profilo, utilizza la sintassi:

`${user.parameter}`

Durante l’utilizzo degli attributi dinamici nei progetti Consigli, devi inserire una barra inversa (\) prima del simbolo del dollaro ($) affinché il valore dinamico possa essere visualizzato correttamente: `\${user.endpoint.lastViewedEntity}`

Queste variabili sono sostituite con il valore sul lato server, quindi nessuna virgoletta o altro JavaScript è necessario per la visualizzazione corretta.

Puoi inoltre specificare i valori predefiniti se desideri esporli alle offerte. La sintassi è simile alla seguente:

`${user.testAttribute default="All Items!"}`

Quando `testAttribute` non esiste o è vuoto, verrà scritto “All Items!” Se un valore di attributo vuoto è valido e desideri scriverlo anziché visualizzare l&#39;impostazione predefinita, puoi utilizzare:

`${user.testAttribute default="All Items!" show_blank="true"}`

Puoi inoltre usare le funzioni escape e unescape per visualizzare i valori. Se il valore ha un apostrofo, ad esempio, potrai applicare ad esso la funzione escape in modo da non rompere JavaScript sulla pagina. (Le offerte sono scritte in JavaScript, quindi un singolo apostrofo può essere confuso per virgolette.) Ad esempio:

`${user.encodedValue encode="unescape"}`

`${user.unencodedValue encode="escape"}`