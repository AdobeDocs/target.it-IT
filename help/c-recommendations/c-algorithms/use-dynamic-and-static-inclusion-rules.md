---
keywords: inclusion rules;inclusion criteria;recommendations;create new criteria;promotion;promotions;dynamic filtering;dynamic;empty values;ignore filtering rule;static filter;filter by value;entity attribute matching;profile attribute matching;parameter matching;filter by value;static filter
description: Informazioni sulla creazione di regole di inclusione in  Adobe Target Recommendations per criteri e promozioni e sull'aggiunta di ulteriori regole di filtro dinamiche o statiche per ottenere risultati migliori.
title: Utilizzare regole di inclusione dinamiche e statiche in  Adobe Target Recommendations
feature: Recommendations
mini-toc-levels: 3
translation-type: tm+mt
source-git-commit: 7b86db4b45f93a3c6169caf81c2cd52236bb5a45
workflow-type: tm+mt
source-wordcount: '1062'
ht-degree: 39%

---


# ![PREMIUM](/help/assets/premium.png) Utilizzare regole di inclusione dinamiche e statiche{#use-dynamic-and-static-inclusion-rules}

Informazioni sulla creazione di regole di inclusione per criteri e promozioni in [!DNL Adobe Target] e sull&#39;aggiunta di ulteriori regole di filtro dinamiche o statiche per ottenere risultati migliori per le raccomandazioni.

>[!NOTE]
>
>Le regole di inclusione per i criteri e le promozioni possono essere create e utilizzate con processi simili, così come sono simili i rispettivi casi ed esempi di utilizzo. Sia i criteri che le promozioni e l&#39;uso delle regole di inclusione sono trattati in questa sezione.

## Aggiunta di regole di filtro ai criteri {#section_CD0D74B8D3BE4A75A78C36CF24A8C57F}

Durante la [creazione di criteri](/help/c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE), fai clic su **[!UICONTROL Aggiungi regola di filtro]** in **[!UICONTROL Regole di inclusione]**.

![](assets/inclusion_options_new.png)

Le opzioni disponibili dipendono dal settore verticale selezionato e della chiave consiglio.

## Aggiunta di regole di filtro alle promozioni {#section_D59AFB62E2EE423086281CF5D18B1076}

Durante la [creazione di una promozione](/help/c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14), seleziona **[!UICONTROL Promuovi per attributo]**, quindi fai clic su **[!UICONTROL Aggiungi regola filtro]**.

![](assets/inclusion_options.png)

## Tipi di filtro {#section_0125F1ED10A84C0EB45325122460EBCD}

Nelle sezioni seguenti sono elencati i tipi di opzioni di filtro per [!UICONTROL Filtro dinamico] e [!UICONTROL Filtro per valore] per criteri e promozioni:

### Filtraggio dinamico

Le regole di inclusione dinamica sono più potenti delle regole di inclusione statica e producono risultati e coinvolgimento migliori. Considera i seguenti aspetti:

* Le regole di inclusione dinamica distribuiscono le raccomandazioni facendo corrispondere un attributo nel parametro di profilo di un utente o in una chiamata mbox.

   Ad esempio, potete creare una raccomandazione &quot;Most Popular Criteria&quot; (Criteri più comuni), quindi del set di raccomandazioni restituite, quindi filtrare eventuali raccomandazioni (in tempo reale) rispetto a un attributo passato quando l&#39;utente accede a una pagina in cui vengono visualizzate le raccomandazioni.

* Utilizzate le regole statiche per limitare gli elementi inclusi nella raccomandazione (invece di utilizzare le raccolte).

* Potete creare tutte le regole di inclusione dinamica necessarie. Le regole di inclusione vengono collegate mediante un operatore E. Gli articoli verranno inclusi in un consiglio solo se vengono soddisfatte tutte le regole.

Per il filtro dinamico sono disponibili le seguenti opzioni:

| Filtro dinamico, opzione | Dettagli |
| --- | --- |
| [Corrispondenza attributo entità](/help/c-recommendations/c-algorithms/entity-attribute-matching.md) | Filtrare in modo dinamico confrontando un insieme di potenziali elementi delle raccomandazioni con un elemento specifico con cui gli utenti hanno interagito.<br>Utilizzate  [!UICONTROL Entity Attribute ] Matchinging (Corrispondenza attributi entità) per mostrare le raccomandazioni più probabili per il visitatore, ad esempio il marchio preferito del visitatore. |
| [Corrispondenza attributo profilo](/help/c-recommendations/c-algorithms/profile-attribute-matching.md) | Filtrare in modo dinamico confrontando elementi (entità) con un valore nel profilo dell&#39;utente.<br>Utilizzate  [!UICONTROL Profile Attribute ] Matchinging (Corrispondenza attributi profilo) per mostrare le raccomandazioni che corrispondono a un valore memorizzato nel profilo del visitatore, ad esempio dimensione o marchio preferito. |
| [Corrispondenza parametro](/help/c-recommendations/c-algorithms/parameter-matching.md) | Filtrare in modo dinamico confrontando elementi (entità) con un valore nella richiesta (API o mbox).<br>Utilizzate  [!UICONTROL Corrispondenza ] parametri per raccomandare il contenuto che corrisponda ai parametri di pagina o ai parametri del visitatore, come le dimensioni del dispositivo o la geolocalità. |

### Filtra per valore

L&#39;opzione seguente è disponibile per filtrare in base al valore:

| Opzione Filtraggio per valore | Dettagli |
| --- | --- |
| [Filtro statico](/help/c-recommendations/c-algorithms/static-value.md) | Immettere manualmente uno o più valori statici da filtrare. |

## Criteri dinamici ed esempi di promozione

I criteri e le promozioni dinamici sono molto più potenti dei criteri e delle promozioni statici e offrono risultati e coinvolgimento migliori.

Gli esempi seguenti forniscono idee generali su come utilizzare le promozioni dinamiche nelle attività di marketing:

| Operatore | Esempi |
| --- | --- |
| È uguale a | Utilizzando l&#39;operatore &quot;uguale&quot; nelle promozioni dinamiche, quando un visitatore visualizza un elemento sul sito Web (ad esempio un prodotto, un articolo o un filmato) potete promuovere altri elementi da:<ul><li>lo stesso marchio</li><li>la stessa categoria</li><li>la stessa categoria E lo stesso marchio</li><li>lo stesso store</li></ul> |
| Non uguale | Utilizzando l&#39;operatore &quot;non uguale&quot; nelle promozioni dinamiche, quando un visitatore visualizza un elemento sul sito Web (ad esempio un prodotto, un articolo o un filmato) potete promuovere altri elementi da:<ul><li>una serie TV diversa</li><li>un genere diverso</li><li>una serie di prodotti diversi</li><li>un ID di stile diverso</li></ul> |
| È tra | Utilizzando l&#39;operatore &quot;è compreso&quot; nelle promozioni dinamiche, quando un visitatore visualizza un elemento sul sito Web (ad esempio un prodotto, un articolo o un filmato) potete promuovere altri elementi:<ul><li>più costosi</li><li>meno costosi</li><li>più o meno costosi del 30%</li><li>episodi successivi nella stessa stagione</li><li>libri precedenti in una collana</li></ul> |

## Gestione dei valori vuoti durante il filtraggio per corrispondenza attributi entità, corrispondenza attributi profilo e corrispondenza parametri {#section_7D30E04116DB47BEA6FF840A3424A4C8}

Potete scegliere diverse opzioni per gestire i valori vuoti durante il filtraggio per [!UICONTROL Corrispondenza attributi entità], [!UICONTROL Corrispondenza attributi profilo] e per [!UICONTROL Corrispondenza parametri] per criteri e promozioni di uscita.

In precedenza, non veniva restituito alcun risultato se un valore era vuoto. L&#39;elenco a discesa “Se *x* è vuoto” consente di scegliere l&#39;azione da eseguire se i criteri hanno valori vuoti, come illustrato di seguito:

![](assets/empty_value.png)

Per selezionare l’azione desiderata, passa il puntatore sull’icona ingranaggio (![](assets/icon_gear.png)), quindi scegli l’azione desiderata:

| Azione | Disponibile per | Dettagli |
|--- |--- |--- |
| [!UICONTROL Ignora questa regola di filtro] | [!UICONTROL Corrispondenza attributi profilo ] [!UICONTROL e corrispondenza parametri] | Questa è l&#39;azione predefinita per [!UICONTROL Corrispondenza attributi profilo] e [!UICONTROL Corrispondenza parametri].<br>Questa opzione specifica che la regola viene ignorata. Ad esempio, se sono presenti tre regole di filtro e la terza regola non passa alcun valore, invece di non restituire alcun risultato si può semplicemente ignorare la terza regola con valori vuoti. |
| [!UICONTROL Non mostrare risultati per questo criterio]<br> (solo criteri) | [!UICONTROL Corrispondenza] attributi entità, corrispondenza attributi  [!UICONTROL profilo] e corrispondenza  [!UICONTROL parametri] | Questa è l&#39;azione predefinita per [!UICONTROL Corrispondenza attributo entità].<br>[!DNL Target]Corrisponde al modo in cui gestiva i valori vuoti prima dell’aggiunta di questa opzione, ossia non verrà visualizzato alcun risultato per questo criterio. |
| [!UICONTROL Non promuovere elementi<br> (solo Promozioni)] | [!UICONTROL Corrispondenza] attributi entità, corrispondenza attributi  [!UICONTROL profilo] e corrispondenza  [!UICONTROL parametri] | Questa è l&#39;azione predefinita per [!UICONTROL Corrispondenza attributo entità].<br>[!DNL Target]Corrisponde al modo in cui gestiva i valori vuoti prima dell’aggiunta di questa opzione, ossia non verrà visualizzato alcun risultato per questo criterio. |
| [!UICONTROL Usa un valore statico] | [!UICONTROL Corrispondenza] attributi entità, corrispondenza attributi  [!UICONTROL profilo] e corrispondenza  [!UICONTROL parametri] | Se un valore è vuoto, è possibile scegliere di utilizzare un valore statico. |

## Avvertenze {#section_A889FAF794B7458CA074DEE06DD0E345}

>[!IMPORTANT]
>
>Gli attributi di tipi di dati diversi potrebbero non essere compatibili nelle promozioni o nei criteri dinamici in fase di esecuzione con gli operatori “è uguale a” e “è diverso da”. È consigliabile utilizzare i valori [!UICONTROL Value], [!UICONTROL Margin], [!UICONTROL Inventory] e [!UICONTROL Environment] saggiamente sul lato destro se il lato sinistro dispone di attributi predefiniti o personalizzati.

![](assets/left_right.png)

Nella tabella seguente vengono mostrate regole efficaci e regole che potrebbero invece non essere compatibili in fase di esecuzione:

| Regole compatibili | Regole potenzialmente non compatibili |
|--- |--- |
| value - è tra - 90% e 110% dell’articolo corrente - salesValue | salesValue - è tra - 90% e 110% dell’articolo corrente - value |
| value - è tra - 90% e 110% dell’articolo corrente - value | clearancePrice - è tra - 90% e 110% dell’articolo corrente - margin |
| margin - è tra - 90% e 110% dell’articolo corrente - margin | storeInventory - è uguale a - dell’articolo corrente - inventory |
| inventory - è uguale a - dell’articolo corrente - inventory |  |
