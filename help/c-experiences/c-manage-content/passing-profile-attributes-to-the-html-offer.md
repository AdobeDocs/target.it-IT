---
keywords: dati dinamici;risorse;dati;offerte;offerte personalizzate;offerte personali;sostituzione token
description: Scopri come passare dati dinamici in [!DNL Adobe Target] Offerte. Esplora i casi aziendali che mostrano perché utilizzare offerte dinamiche e visualizza esempi e informazioni sull’implementazione.
title: Come faccio a trasmettere i dati dinamici alle offerte?
feature: Esperienze e offerte
exl-id: b8f9c6eb-1000-41a2-aa3f-bc42c1ef5669
translation-type: tm+mt
source-git-commit: 5055efce2069d3aca7008b1d78b84c131f05faf3
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 78%

---

# Trasmettere i dati dinamici nelle offerte

Puoi visualizzare in modo dinamico le informazioni sui visitatori memorizzate nel profilo [!DNL Adobe Target]. Analogamente, le informazioni relative all’attività (come il nome dell’attività o dell’esperienza) possono inoltre essere utilizzate per creare una singola offerta in grado di restituire in modo dinamico contenuti personalizzati in base agli interessi del visitatore, al comportamento passato e al profilo complessivo.

## Casi aziendali

* Promuovere un’offerta scontata per un acquisto relativo all’ultimo prodotto acquistato. Invece di creare un’offerta separata per ogni elemento del catalogo, puoi creare un’offerta con testo dinamico che visualizza “l’ultimo prodotto acquistato” dal profilo insieme a un collegamento nell’offerta.
* Un visitatore arriva sulla pagina di destinazione con `keyword=world` `cup`. Mostra il termine *World cup* nell&#39;offerta.
* Personalizza un’etichetta di consigli con informazioni come (1) l’ultimo elemento aggiunto al carrello di un visitatore (Nike Air Max 1000), (2) la preferenza colore del visitatore (nero) e (3) la categoria non relativa alla scarpa preferita dal visitatore (felpe). Esempio: “Abbina a “Nike Air Max 1000” queste fantastiche “felpe” “nere””.

## Vantaggi tecnici

Poiché le preferenze, i comportamenti, gli stati specifici dell’utente possono essere memorizzati nel profilo utente, puoi ripetere questo messaggio nelle visite successive. Le offerte dinamiche consentono una maggiore estensione: ti permettono infatti di configurare una singola offerta all’interno di un’attività che visualizza messaggi personalizzati per tutti i visitatori. Il contenuto del sito Web si aggiorna automaticamente per riflettere i cambiamenti nell’intento del visitatore.

## Esempio

* `mboxCreate("landingpage"`, `"profile.keyword=World Cup");`

* Codice offerta HTML: `Get your ${profile.keyword} information here!`
* L&#39;utente vede: Get your World Cup information here!

I seguenti valori possono essere “sostituiti tramite token”:

| Valore | Esempi |
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

## Implementazione

Per i parametri di profilo trasmessi in una mbox, utilizza la sintassi:

`${profile.parameter}`

Per i parametri di profilo creati in uno script di profilo, utilizza la sintassi:

`${user.parameter}`

Quando utilizzi gli attributi dinamici in un progetto [!DNL Recommendations], devi inserire una barra inversa ( \ ) prima del simbolo del dollaro ( $ ) affinché il valore dinamico possa essere visualizzato correttamente:

`\${user.endpoint.lastViewedEntity}`

Queste variabili sono sostituite con il valore sul lato server, quindi nessuna virgoletta o altro JavaScript è necessario per la visualizzazione corretta.

È inoltre possibile specificare i valori predefiniti per i valori che si desidera esporre alle offerte. La sintassi è simile alla seguente:

`${user.testAttribute default="All Items!"}`

Quando `testAttribute` non esiste o è vuoto, verrà scritto “All Items!” Se un valore di attributo vuoto è valido e desideri scriverlo anziché visualizzare l&#39;impostazione predefinita, puoi utilizzare:

`${user.testAttribute default="All Items!" show_blank="true"}`

Puoi inoltre usare le funzioni escape e unescape per visualizzare i valori. Se il valore ha un apostrofo, ad esempio, potrai applicare ad esso la funzione escape in modo da non rompere JavaScript sulla pagina. (Le offerte sono scritte in JavaScript, quindi un singolo apostrofo può essere confuso per virgolette.) Ad esempio:

`${user.encodedValue encode="unescape"}`

`${user.unencodedValue encode="escape"}`
