---
keywords: dati dinamici;risorse;dati;offerte;offerte personalizzate;offerte personali;sostituzione token
description: Scopri come trasmettere dati dinamici a [!DNL Adobe Target] Offerte.
title: Come faccio a trasmettere i dati dinamici alle offerte?
feature: Experiences and Offers
exl-id: b8f9c6eb-1000-41a2-aa3f-bc42c1ef5669
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 63%

---

# Trasmettere i dati dinamici nelle offerte

Puoi visualizzare in modo dinamico le informazioni sui visitatori memorizzate in [!DNL Adobe Target] profilo. Analogamente, le informazioni relative all’attività (come il nome dell’attività o dell’esperienza) possono inoltre essere utilizzate per creare una singola offerta in grado di restituire in modo dinamico contenuti personalizzati in base agli interessi del visitatore, al comportamento passato e al profilo complessivo.

## Casi aziendali

* Promuovere un’offerta scontata per un acquisto relativo all’ultimo prodotto acquistato. Invece di creare un’offerta separata per ogni elemento del catalogo, puoi creare un’offerta con testo dinamico che visualizza “l’ultimo prodotto acquistato” dal profilo insieme a un collegamento nell’offerta.
* Un visitatore arriva sulla pagina di destinazione con `keyword=world` `cup`. Mostra il termine *World cup* nell&#39;offerta.
* Personalizza un’etichetta di consigli con informazioni come (1) l’ultimo elemento aggiunto al carrello di un visitatore (Nike Air Max 1000), (2) la preferenza colore del visitatore (nero) e (3) la categoria non relativa alla scarpa preferita dal visitatore (felpe). Esempio: “Abbina a “Nike Air Max 1000” queste fantastiche “felpe” “nere””.

## Vantaggi tecnici

Poiché le preferenze, i comportamenti e lo stato specifici del visitatore possono essere memorizzati nel profilo del visitatore, puoi ripetere questo messaggio nelle visite successive. Le offerte dinamiche consentono una maggiore estensione: ti permettono infatti di configurare una singola offerta all’interno di un’attività che visualizza messaggi personalizzati per tutti i visitatori. Il contenuto del sito Web si aggiorna automaticamente per riflettere i cambiamenti nell’intento del visitatore.

## Esempio

* `mboxCreate("landingpage"`, `"profile.keyword=World Cup");`

* Codice offerta HTML: `Get your ${profile.keyword} information here!`
* Il visitatore vede: Ricevi qui le informazioni sulla Coppa del Mondo!

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

Per [!DNL Recommendations] progettazioni, vedi ulteriori esempi in [Panoramica della progettazione](/help/main/c-recommendations/c-design-overview/design-overview.md).

## Implementazione

Per i parametri di profilo trasmessi in una mbox, utilizza la sintassi:

`${profile.parameter}`

Per i parametri di profilo creati in uno script di profilo, utilizza la sintassi:

`${user.parameter}`

Quando si utilizzano attributi dinamici in un [!DNL Recommendations] per il corretto rendering del valore dinamico, è necessario inserire una barra inversa ( \ ) prima del simbolo del dollaro ( $ ):

`\${user.endpoint.lastViewedEntity}`

Queste variabili sono sostituite con il valore sul lato server, quindi nessuna virgoletta o altro JavaScript è necessario per la visualizzazione corretta.

È inoltre possibile specificare i valori predefiniti per i valori che si desidera esporre alle offerte. La sintassi è simile alla seguente:

`${user.testAttribute default="All Items!"}`

Quando `testAttribute` non esiste o è vuoto, verrà scritto è scritto. Se un valore di attributo vuoto è valido e desideri scriverlo anziché visualizzare l&#39;impostazione predefinita, puoi utilizzare:

`${user.testAttribute default="All Items!" show_blank="true"}`

Puoi inoltre usare le funzioni escape e unescape per visualizzare i valori. Se il valore ha un apostrofo, ad esempio, puoi applicare un escape al valore in modo che non interrompa il JavaScript sulla pagina. (Le offerte sono scritte in JavaScript, quindi un singolo apostrofo può essere confuso per virgolette.) Ad esempio:

`${user.encodedValue encode="unescape"}`

`${user.unencodedValue encode="escape"}`

Per i parametri di offerta (offer.name, offer.id) utilizzati nel contenuto di un’offerta:

Se l’offerta è una delle diverse offerte impostate su un’esperienza, il valore dell’ultima offerta aggiunta popola il valore del parametro. Ciò significa che questi parametri vengono valutati a livello di esperienza.