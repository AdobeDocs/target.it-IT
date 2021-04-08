---
keywords: regole di inclusione;criteri di inclusione;consigli;creazione di nuovi criteri;promozione;promozioni;filtro dinamico;dinamico;valori vuoti;ignorare regola di filtro;filtro statico;filtro per valore;corrispondenza attributo entità;corrispondenza attributo profilo;parametro corrispondente;filtro per valore;filtro statico
description: Scopri come creare regole di inclusione in Adobe Target Recommendations per criteri e promozioni. Aggiungi ulteriori regole di filtro dinamiche o statiche per ottenere risultati migliori.
title: Come si utilizzano regole di inclusione dinamiche e statiche in Recommendations?
feature: Consigli
mini-toc-levels: 3
exl-id: 49b20e75-ee55-4239-94a0-6d175e2d4811
translation-type: tm+mt
source-git-commit: 6ba670ef69fa23c0023636a1920eed15dcd9dd06
workflow-type: tm+mt
source-wordcount: '1100'
ht-degree: 41%

---

# ![PREMIUM](/help/assets/premium.png) Utilizzare regole di inclusione dinamiche e statiche{#use-dynamic-and-static-inclusion-rules}

Informazioni sulla creazione di regole di inclusione per criteri e promozioni in [!DNL Adobe Target] e sull’aggiunta di regole di filtro dinamiche o statiche aggiuntive per ottenere risultati migliori per i consigli.

>[!NOTE]
>
>Le regole di inclusione per i criteri e le promozioni possono essere create e utilizzate con processi simili, così come sono simili i rispettivi casi ed esempi di utilizzo. In questa sezione sono trattati sia i criteri e le promozioni che l’uso delle regole di inclusione.

## Aggiunta di regole di filtro ai criteri {#section_CD0D74B8D3BE4A75A78C36CF24A8C57F}

Durante la [creazione di criteri](/help/c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE), fai clic su **[!UICONTROL Aggiungi regola di filtro]** in **[!UICONTROL Regole di inclusione]**.

![](assets/inclusion_options_new.png)

Le opzioni disponibili dipendono dal settore verticale selezionato e della chiave consiglio.

## Aggiunta di regole di filtro alle promozioni {#section_D59AFB62E2EE423086281CF5D18B1076}

Durante la [creazione di una promozione](/help/c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14), seleziona **[!UICONTROL Promuovi per attributo]**, quindi fai clic su **[!UICONTROL Aggiungi regola filtro]**.

![](assets/inclusion_options.png)

## Tipi di filtro {#section_0125F1ED10A84C0EB45325122460EBCD}

Nelle sezioni seguenti sono elencati i tipi di opzioni di filtro per [!UICONTROL Filtro dinamico] e [!UICONTROL Filtro per valore] per entrambi i criteri e le promozioni:

### Filtraggio dinamico

Le regole di inclusione dinamica sono più potenti delle regole di inclusione statica e producono risultati e coinvolgimento migliori. Considera i seguenti aspetti:

* Le regole di inclusione dinamiche distribuiscono i consigli confrontando un attributo nel parametro di profilo di un utente o in una chiamata mbox.

   Ad esempio, potete creare un consiglio &quot;Criteri più popolari&quot; e quindi del set di consigli restituiti, quindi filtrare eventuali consigli (in tempo reale) in base a un attributo trasmesso quando l’utente accede a una pagina in cui vengono visualizzati i consigli.

* Utilizza le regole statiche per limitare gli elementi inclusi nel consiglio (invece di utilizzare le raccolte).

* Puoi creare tutte le regole di inclusione dinamiche necessarie. Le regole di inclusione vengono collegate mediante un operatore E. Gli articoli verranno inclusi in un consiglio solo se vengono soddisfatte tutte le regole.

Per il filtro dinamico sono disponibili le seguenti opzioni:

| Opzione filtro dinamico | Dettagli |
| --- | --- |
| [Corrispondenza attributo entità](/help/c-recommendations/c-algorithms/entity-attribute-matching.md) | Filtrare dinamicamente confrontando un pool di potenziali articoli consigliati con un articolo specifico con cui gli utenti hanno interagito.<br>Utilizza  [!UICONTROL Corrispondenza attributo di entità ] quando desideri mostrare i consigli che più probabilmente interesseranno il visitatore, ad esempio il marchio preferito del visitatore. |
| [Corrispondenza attributo profilo](/help/c-recommendations/c-algorithms/profile-attribute-matching.md) | Filtrare dinamicamente confrontando gli articoli (entità) con un valore presente nel profilo dell’utente.<br>Utilizza la  [!UICONTROL corrispondenza attributo ] profilo per mostrare i consigli che corrispondono a un valore memorizzato nel profilo del visitatore, ad esempio dimensione o marchio preferito. |
| [Corrispondenza parametro](/help/c-recommendations/c-algorithms/parameter-matching.md) | Filtrare dinamicamente confrontando gli articoli (entità) con un valore nella richiesta (API o mbox).<br>Utilizza  [!UICONTROL Corrispondenza ] parametro per consigliare il contenuto che corrisponde ai parametri di pagina o ai parametri del visitatore, come le dimensioni del dispositivo o la geolocalizzazione. |

### Filtra per valore

È disponibile la seguente opzione per filtrare per valore:

| Opzione Filtraggio per valore | Dettagli |
| --- | --- |
| [Filtro statico](/help/c-recommendations/c-algorithms/static-value.md) | Immettere manualmente uno o più valori statici da filtrare. |

## Criteri dinamici ed esempi di promozione

I criteri e le promozioni dinamici sono molto più potenti dei criteri e delle promozioni statici e producono risultati e un coinvolgimento migliori.

Gli esempi seguenti forniscono idee generali su come utilizzare le promozioni dinamiche nelle attività di marketing:

| Operatore | Esempi |
| --- | --- |
| È uguale a | Utilizzando l’operatore &quot;è uguale a&quot; nelle promozioni dinamiche, quando un visitatore sta visualizzando un articolo sul tuo sito web (ad esempio un prodotto, un articolo o un filmato), puoi promuovere altri articoli appartenenti a:<ul><li>lo stesso marchio</li><li>la stessa categoria</li><li>la stessa categoria E lo stesso marchio</li><li>lo stesso store</li></ul> |
| Does Not Equal | Utilizzando l’operatore &quot;è diverso da&quot; nelle promozioni dinamiche, quando un visitatore sta visualizzando un articolo sul tuo sito web (ad esempio un prodotto, un articolo o un filmato), puoi promuovere altri articoli appartenenti a:<ul><li>una serie TV diversa</li><li>un genere diverso</li><li>una serie di prodotti diversi</li><li>un ID di stile diverso</li></ul> |
| È tra | Utilizzando l&#39;operatore &quot;è tra&quot; nelle promozioni dinamiche, quando un visitatore sta visualizzando un articolo sul tuo sito web (ad esempio un prodotto, un articolo o un filmato), puoi promuovere altri articoli che sono:<ul><li>più costosi</li><li>meno costosi</li><li>più o meno costosi del 30%</li><li>episodi successivi nella stessa stagione</li><li>libri precedenti in una collana</li></ul> |

## Gestione dei valori vuoti durante l&#39;applicazione di filtri per Corrispondenza attributo entità, Corrispondenza attributo profilo e Corrispondenza parametro {#section_7D30E04116DB47BEA6FF840A3424A4C8}

Puoi scegliere diverse opzioni per gestire i valori vuoti quando filtri per [!UICONTROL Corrispondenza attributo entità], [!UICONTROL Corrispondenza attributo profilo] e [!UICONTROL Corrispondenza parametro] per i criteri e le promozioni di uscita.

In precedenza, non veniva restituito alcun risultato se un valore era vuoto. L&#39;elenco a discesa “Se *x* è vuoto” consente di scegliere l&#39;azione da eseguire se i criteri hanno valori vuoti, come illustrato di seguito:

![](assets/empty_value.png)

Per selezionare l’azione desiderata, passa il puntatore sull’icona ingranaggio (![](assets/icon_gear.png)), quindi scegli l’azione desiderata:

| Azione | Disponibile per | Dettagli |
|--- |--- |--- |
| [!UICONTROL Ignora questa regola di filtro] | [!UICONTROL Corrispondenza attributo profilo ] e corrispondenza  [!UICONTROL parametro] | Questa è l&#39;azione predefinita per [!UICONTROL Corrispondenza attributo profilo] e [!UICONTROL Corrispondenza parametro].<br>Questa opzione specifica che la regola viene ignorata. Ad esempio, se sono presenti tre regole di filtro e la terza regola non passa alcun valore, invece di non restituire alcun risultato si può semplicemente ignorare la terza regola con valori vuoti. |
| [!UICONTROL Non mostrare alcun risultato per questo criterio]<br> (solo criteri) | [!UICONTROL Corrispondenza attributo entità], Corrispondenza attributo  [!UICONTROL profilo] e Corrispondenza  [!UICONTROL parametro] | Questa è l&#39;azione predefinita per [!UICONTROL Corrispondenza attributo entità].<br>[!DNL Target]Corrisponde al modo in cui gestiva i valori vuoti prima dell’aggiunta di questa opzione, ossia non verrà visualizzato alcun risultato per questo criterio. |
| [!UICONTROL Non promuovere alcun elemento<br> (solo promozioni)] | [!UICONTROL Corrispondenza attributo entità], Corrispondenza attributo  [!UICONTROL profilo] e Corrispondenza  [!UICONTROL parametro] | Questa è l&#39;azione predefinita per [!UICONTROL Corrispondenza attributo entità].<br>[!DNL Target]Corrisponde al modo in cui gestiva i valori vuoti prima dell’aggiunta di questa opzione, ossia non verrà visualizzato alcun risultato per questo criterio. |
| [!UICONTROL Usa un valore statico] | [!UICONTROL Corrispondenza attributo entità], Corrispondenza attributo  [!UICONTROL profilo] e Corrispondenza  [!UICONTROL parametro] | Se un valore è vuoto, è possibile scegliere di utilizzare un valore statico. |

## Avvertenze {#section_A889FAF794B7458CA074DEE06DD0E345}

>[!IMPORTANT]
>
>Gli attributi di tipi di dati diversi potrebbero non essere compatibili nelle promozioni o nei criteri dinamici in fase di esecuzione con gli operatori “è uguale a” e “è diverso da”. Utilizza i valori [!UICONTROL Valore], [!UICONTROL Margine], [!UICONTROL Inventario] e [!UICONTROL Ambiente] con saggezza sul lato destro se sul lato sinistro sono presenti attributi predefiniti o attributi personalizzati.

![](assets/left_right.png)

Nella tabella seguente vengono mostrate regole efficaci e regole che potrebbero invece non essere compatibili in fase di esecuzione:

| Regole compatibili | Regole potenzialmente incompatibili |
|--- |--- |
| value - è tra - 90% e 110% dell’articolo corrente - salesValue | salesValue - è tra - 90% e 110% dell’articolo corrente - value |
| value - è tra - 90% e 110% dell’articolo corrente - value | clearancePrice - è tra - 90% e 110% dell’articolo corrente - margin |
| margin - è tra - 90% e 110% dell’articolo corrente - margin | storeInventory - è uguale a - dell’articolo corrente - inventory |
| inventory - è uguale a - dell’articolo corrente - inventory |  |
