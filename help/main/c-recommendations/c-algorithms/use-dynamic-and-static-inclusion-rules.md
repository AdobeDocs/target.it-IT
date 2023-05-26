---
keywords: regole di inclusione;criteri di inclusione;consigli;creazione di nuovi criteri;promozione;promozioni;filtro dinamico;dinamico;valori vuoti;ignorare regola di filtro;filtro statico;filtro per valore;corrispondenza attributo entità;corrispondenza attributo profilo;parametro corrispondente;filtro per valore;filtro statico
description: Scopri come creare regole di inclusione in Adobe [!DNL Target] Recommendations per criteri e promozioni. Per ottenere risultati migliori, aggiungi regole di filtro più dinamiche o statiche.
title: Come si utilizzano le regole di inclusione dinamiche e statiche in Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
mini-toc-levels: 3
exl-id: 49b20e75-ee55-4239-94a0-6d175e2d4811
source-git-commit: 07062b7df75300bd7558a24da5121df454520e42
workflow-type: tm+mt
source-wordcount: '2093'
ht-degree: 16%

---

# Utilizzare regole di inclusione dinamiche e statiche

Informazioni sulla creazione di regole di inclusione per criteri e promozioni in [!DNL Adobe Target] e l’aggiunta di regole di filtro dinamiche o statiche per ottenere risultati migliori per i consigli.

Le regole di inclusione per i criteri e le promozioni possono essere create e utilizzate con processi simili, così come sono simili i rispettivi casi ed esempi di utilizzo. I criteri e le promozioni e l’uso delle regole di inclusione sono trattati in questa sezione.

## Aggiunta di regole di filtro ai criteri {#section_CD0D74B8D3BE4A75A78C36CF24A8C57F}

Durante la [creazione di criteri](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE), fai clic su **[!UICONTROL Aggiungi regola di filtro]** in **[!UICONTROL Regole di inclusione]**.

![include_options_new image](assets/inclusion_options_new.png)

Le opzioni disponibili dipendono dal settore verticale selezionato e della chiave consiglio.

## Aggiunta di regole di filtro alle promozioni {#section_D59AFB62E2EE423086281CF5D18B1076}

Durante la [creazione di una promozione](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14), seleziona **[!UICONTROL Promuovi per attributo]**, quindi fai clic su **[!UICONTROL Aggiungi regola filtro]**.

![immagine include_options](assets/inclusion_options.png)

## Tipi di filtro {#section_0125F1ED10A84C0EB45325122460EBCD}

Nelle sezioni seguenti sono elencati i tipi di opzioni di filtro per [!UICONTROL Filtro dinamico] e [!UICONTROL Filtra per valore] sia per i criteri che per le promozioni:

### Filtraggio dinamico

Le regole di inclusione dinamica sono più potenti delle regole di inclusione statiche e producono risultati e coinvolgimento migliori. Considera i seguenti aspetti:

* Le regole di inclusione dinamica forniscono consigli facendo corrispondere un attributo nel parametro di profilo di un utente o in una chiamata mbox.

   Ad esempio, puoi creare un consiglio per &quot;Criteri più popolari&quot;. Dal set di consigli restituiti, puoi filtrare tutti i consigli (in tempo reale) in base a un attributo passato quando l’utente accede a una pagina in cui vengono visualizzati i consigli.

* Utilizza regole statiche per limitare quali elementi vengono inclusi nel consiglio (anziché utilizzare le raccolte).

* Puoi creare tutte le regole di inclusione dinamica necessarie. Le regole di inclusione vengono collegate mediante un operatore E. Gli articoli verranno inclusi in un consiglio solo se vengono soddisfatte tutte le regole.

Per il filtro dinamico sono disponibili le seguenti opzioni:

| Opzione filtro dinamico | Dettagli |
| --- | --- |
| [Corrispondenza attributo entità](/help/main/c-recommendations/c-algorithms/entity-attribute-matching.md) | Filtra dinamicamente confrontando un pool di potenziali elementi di consigli con un elemento specifico con cui gli utenti hanno interagito.<br>Utilizzare [!UICONTROL Corrispondenza attributo entità] quando desideri mostrare consigli che hanno più probabilità di attrarre il visitatore, ad esempio il suo marchio preferito. |
| [Corrispondenza attributo profilo](/help/main/c-recommendations/c-algorithms/profile-attribute-matching.md) | Filtrare dinamicamente confrontando gli articoli (entità) con un valore nel profilo dell’utente.<br>Utilizzare [!UICONTROL Corrispondenza attributo profilo] quando desideri mostrare consigli che corrispondono a un valore memorizzato nel profilo del visitatore, ad esempio dimensioni o marchio preferito. |
| [Corrispondenza parametro](/help/main/c-recommendations/c-algorithms/parameter-matching.md) | Filtra dinamicamente confrontando gli elementi (entità) con un valore nella richiesta (API o mbox).<br>Utilizzare [!UICONTROL Corrispondenza parametro] per consigliare contenuti che corrispondono ai parametri di pagina o ai parametri del visitatore, ad esempio le dimensioni del dispositivo o la geolocalizzazione. |

### Filtra per valore

Per filtrare per valore è disponibile la seguente opzione:

| Opzione Filtro per valore | Dettagli |
| --- | --- |
| [Filtro statico](/help/main/c-recommendations/c-algorithms/static-value.md) | Immetti manualmente uno o più valori statici da filtrare. |

## Operatori disponibili {#operators}

Le promozioni e i criteri dinamici sono molto più potenti di promozioni e criteri statici e offrono risultati e coinvolgimento migliori.

Gli esempi seguenti forniscono idee generali su come utilizzare promozioni ed esclusioni dinamiche nelle attività di marketing:

| Operatore | Esempi |
| --- | --- |
| Uguale a<br>(disponibile con Corrispondenza attributo entità, Corrispondenza attributo profilo, Corrispondenza parametro e Filtro statico). | Utilizzando l&#39;operatore &quot;è uguale a&quot; nelle promozioni dinamiche, quando un visitatore sta visualizzando un articolo sul tuo sito web (ad esempio un prodotto, un articolo o un filmato), puoi promuovere altri articoli appartenenti a:<ul><li>Lo stesso marchio</li><li>La stessa categoria</li><li>La stessa categoria E dal marchio della casa</li><li>Lo stesso negozio</li></ul> |
| Does Not Equal<br>(disponibile con Corrispondenza attributo entità, Corrispondenza attributo profilo, Corrispondenza parametro e Filtro statico). | Utilizzando l&#39;operatore &quot;è diverso da&quot; nelle promozioni dinamiche, quando un visitatore sta visualizzando un articolo sul tuo sito Web (ad esempio un prodotto, un articolo o un filmato), puoi promuovere altri articoli appartenenti a:<ul><li>Un&#39;altra serie TV</li><li>Un genere diverso</li><li>Una serie di prodotti diversa</li><li>Un ID di stile diverso</li></ul> |
| Non contiene sottostringa<br>(disponibile con Corrispondenza attributo entità, Corrispondenza attributo profilo, Corrispondenza parametro e Filtro statico). | Utilizzando l’operatore &quot;non contiene sottostringhe&quot;, quando un visitatore sta visualizzando un articolo sul tuo sito web (ad esempio un prodotto), puoi promuovere altri articoli che:<ul><li>Il titolo non contiene una parolaccia</li></ul> |
| Inizia con<br>(disponibile con Corrispondenza attributo entità, Corrispondenza attributo profilo, Corrispondenza parametro e Filtro statico). | Utilizzando l’operatore &quot;inizia con&quot;, quando un visitatore visualizza un articolo sul tuo sito web (ad esempio un prodotto), puoi promuovere altri articoli che:<ul><li>Il nome del prodotto inizia con iPhone</li></ul> |
| Termina con<br>(disponibile con Corrispondenza attributo entità, Corrispondenza attributo profilo, Corrispondenza parametro e Filtro statico). | Utilizzando l’operatore &quot;termina con&quot;, quando un visitatore visualizza un articolo sul tuo sito web (ad esempio un prodotto), puoi promuovere altri articoli che:<ul><li>Il contenuto termina con EN, che indica la lingua inglese</li></ul> |
| È maggiore di o uguale a<br>(disponibile con Corrispondenza attributo entità, Corrispondenza attributo profilo, Corrispondenza parametro e Filtro statico). | Utilizzando l’operatore &quot;è maggiore di o uguale a&quot;, quando un visitatore sta visualizzando un articolo sul tuo sito web (ad esempio un prodotto), puoi promuovere altri articoli che:<ul><li>Costano lo stesso o sono più costosi</li></ul> |
| È minore di o uguale a<br>(disponibile con Corrispondenza attributo entità, Corrispondenza attributo profilo, Corrispondenza parametro e Filtro statico). | Utilizzando l’operatore &quot;è minore di o uguale a&quot;, quando un visitatore sta visualizzando un articolo sul tuo sito web (ad esempio un prodotto), puoi promuovere altri articoli che:<ul><li>Costo uguale o inferiore</li><li>Escludi articoli meno costosi</li></ul> |
| È tra<br>(disponibile con Corrispondenza attributo entità, Corrispondenza attributo profilo e Corrispondenza parametro). | Utilizzando l&#39;operatore &quot;è tra&quot; nelle promozioni dinamiche, quando un visitatore sta visualizzando un articolo sul tuo sito web (ad esempio un prodotto, un articolo o un filmato), puoi promuovere altri articoli che sono:<ul><li>Più costoso</li><li>Meno costoso</li><li>Costo più o meno 30%</li><li>Episodi successivi nella stessa stagione</li><li>Libri precedenti in una serie</li></ul> |
| È contenuto nell’elenco<br>(disponibile con Corrispondenza attributo profilo e Corrispondenza parametro). | Utilizzando l’operatore &quot;è contenuto nell’elenco&quot; nella corrispondenza degli attributi del profilo, quando un visitatore sta visualizzando un elemento sul tuo sito web (ad esempio un prodotto, un articolo o un filmato), puoi promuovere altri elementi che sono:<ul><li>Disponibile nella zona geografica del visitatore</li></ul>**Esempio**: vuoi consigliare solo gli elementi disponibili nell’area geografica di un visitatore.<br>La regola del filtro potrebbe essere simile alla seguente:<br>`availableGeographies list contains an item in user.currentGeography`<br>**Nota**: quando si utilizza questo operatore, è previsto un elenco in [lato destro](#caveats) della regola. |
| Non è contenuto nell’elenco<br>(disponibile con Corrispondenza attributo profilo e Corrispondenza parametro). | Utilizzando l’operatore &quot;non contenuto nell’elenco&quot; nella corrispondenza degli attributi del profilo, quando un visitatore sta visualizzando un elemento sul tuo sito web (ad esempio un prodotto, un articolo o un filmato), puoi escludere altri elementi:<ul><li>Nell’elenco degli ultimi dieci elementi visualizzati dal visitatore</li></ul></ul>**Esempio**: non desideri promuovere articoli che il visitatore ha visualizzato di recente e per i quali non ha mostrato alcun interesse.<br>La regola di filtro potrebbe avere un aspetto simile a:<br>`id is not contained in list user.lastViewedItems`<br>**Nota**: quando si utilizza questo operatore, è previsto un elenco in [lato destro](#caveats) della regola. |
| L’elenco contiene un elemento in<br>(disponibile con Corrispondenza attributo entità, Corrispondenza attributo profilo e Corrispondenza parametro). | Utilizzando l’operatore &quot;list contains an item in&quot; nella corrispondenza degli attributi del profilo, quando un visitatore sta visualizzando un articolo sul tuo sito web (ad esempio un evento sportivo o un concerto), puoi promuovere altri articoli che sono:<ul><li>Associato a uno dei team preferiti del visitatore</li></ul>**Esempio**: vuoi consigliare i giochi associati a uno dei team preferiti del visitatore.<br>La regola di filtro potrebbe avere un aspetto simile a:<br>` teamsPlaying list contains an item in user.favoriteTeams`<br>**Nota**: quando si utilizza questo operatore, è previsto un elenco in [entrambi i lati](#caveats) della regola. |
| L’elenco non contiene un elemento in<br>(disponibile con Corrispondenza attributo entità, Corrispondenza attributo profilo e Corrispondenza parametro). | Utilizzando l’operatore &quot;list does not contain an item in&quot; nella corrispondenza degli attributi dei parametri, quando un visitatore sta visualizzando un elemento sul tuo sito web (ad esempio un prodotto, un articolo o un filmato), puoi escludere altri elementi che sono:<ul><li>Contenuto in un elenco di tipi proibiti</li></ul>**Esempio**: vuoi escludere gli articoli disponibili per i visitatori adulti, ad esempio tabacco e alcol.<br>La regola di filtro potrebbe avere un aspetto simile a:<br>`itemType is not contained in list mbox.prohibitedTypes`<br>**Nota**: quando si utilizza questo operatore, è previsto un elenco in [entrambi i lati](#caveats) della regola. |
| L’elenco contiene tutti gli elementi in<br>(disponibile con Corrispondenza attributo entità, Corrispondenza attributo profilo e Corrispondenza parametro). | Utilizzando l’operatore &quot;list contains all items in&quot; nella corrispondenza degli attributi del profilo, quando un visitatore sta visualizzando un articolo sul tuo sito web (ad esempio un annuncio di lavoro o una ricetta), puoi promuovere altri articoli che:<ul><li>Includi un set di abilità</li><li>Includi una serie di componenti richiesti</li></ul>**Esempio 1**: supponiamo che un visitatore abbia una serie di abilità (Java, C++ e HTML). Gli elementi nel catalogo sono processi con competenze richieste (Java e HTML). Desideri accertarti che il profilo del visitatore contenga tutte le competenze richieste prima di consigliare il lavoro al visitatore.<br>La regola di filtro potrebbe avere un aspetto simile a:<br>`profile.jobSeekerSkills contains all items in entity.requiredSkills`<br>**Esempio 2**: supponiamo che un utente abbia un elenco di ingredienti della dispensa. La ricetta contiene un elenco degli ingredienti necessari. Desideri accertarti che il profilo del visitatore contenga tutti gli ingredienti necessari prima di consigliare la ricetta al visitatore.<br>La regola di filtro potrebbe avere un aspetto simile a:<br>`profile.ingredientsInPantry contains all items in recipe.ingredientsRequired`<br>**Nota**: quando si utilizza questo operatore, è previsto un elenco in [entrambi i lati](#caveats) della regola. |
| L’elenco non contiene tutti gli elementi in<br>(disponibile con Corrispondenza attributo entità, Corrispondenza attributo profilo e Corrispondenza parametro). | L’utilizzo dell’operatore &quot;list does not contain all items in&quot; nella corrispondenza degli attributi dell’entità, quando un visitatore sta visualizzando un articolo sul tuo sito web (ad esempio un evento sportivo o un concerto), puoi promuovere altri articoli che:<ul><li>Non includere un set di team</li></ul>**Esempio**: supponiamo che un evento sportivo includa due squadre. Il profilo del visitatore indica che il visitatore non desidera visualizzare i giochi per questi team. Desideri evitare di consigliare un gioco se queste squadre stanno giocando.<br>La regola di filtro potrebbe avere un aspetto simile a:<br>`profile.leastfavoriteTeams does not contain all items in entity.teamsPlaying`<br>**Nota**: quando si utilizza questo operatore, è previsto un elenco in [entrambi i lati](#caveats) della regola. |

## Gestione dei valori vuoti durante l’applicazione di filtri per corrispondenza attributo entità, attributo profilo e parametro {#section_7D30E04116DB47BEA6FF840A3424A4C8}

Puoi scegliere diverse opzioni per gestire i valori vuoti quando filtri per [!UICONTROL Corrispondenza attributo entità], [!UICONTROL Corrispondenza attributo profilo], e [!UICONTROL Corrispondenza parametro] per i criteri di uscita e le promozioni.

In precedenza, non veniva restituito alcun risultato se un valore era vuoto. L&#39;elenco a discesa “Se *x* è vuoto” consente di scegliere l&#39;azione da eseguire se i criteri hanno valori vuoti, come illustrato di seguito:

![immagine empty_value](assets/empty_value.png)

Per selezionare l’azione desiderata, passa il puntatore sull’icona a forma di ingranaggio (![icon_gear image](assets/icon_gear.png)), quindi scegli l’azione desiderata:

| Azione | Disponibile per | Dettagli |
|--- |--- |--- |
| [!UICONTROL Ignora questa regola di filtro] | [!UICONTROL Corrispondenza attributo profilo] e [!UICONTROL Corrispondenza parametro] | Questa è l&#39;azione predefinita per [!UICONTROL Corrispondenza attributo profilo] e [!UICONTROL Corrispondenza parametro].<br>Questa opzione specifica che la regola viene ignorata. Ad esempio, se sono presenti tre regole di filtro e la terza regola non passa alcun valore, invece di non restituire alcun risultato si può semplicemente ignorare la terza regola con valori vuoti. |
| [!UICONTROL Non mostrare alcun risultato per questo criterio]<br>(Solo criteri) | [!UICONTROL Corrispondenza attributo entità], [!UICONTROL Corrispondenza attributo profilo], e [!UICONTROL Corrispondenza parametro] | Questa è l&#39;azione predefinita per [!UICONTROL Corrispondenza attributo entità].<br>Questa azione è come [!DNL Target] ha gestito i valori vuoti prima dell’aggiunta di questa opzione: per questo criterio non viene visualizzato alcun risultato. |
| [!UICONTROL Non promuovere nessun elemento<br>(Solo promozioni)] | [!UICONTROL Corrispondenza attributo entità], [!UICONTROL Corrispondenza attributo profilo], e [!UICONTROL Corrispondenza parametro] | Questa è l&#39;azione predefinita per [!UICONTROL Corrispondenza attributo entità].<br>Questa azione è come [!DNL Target] ha gestito i valori vuoti prima dell’aggiunta di questa opzione: per questo criterio non viene visualizzato alcun risultato. |
| [!UICONTROL Usa un valore statico] | [!UICONTROL Corrispondenza attributo entità], [!UICONTROL Corrispondenza attributo profilo], e [!UICONTROL Corrispondenza parametro] | Se un valore è vuoto, è possibile scegliere di utilizzare un valore statico. |

## Avvertenze {#caveats}

>[!IMPORTANT]
>
>Gli attributi di tipi di dati diversi potrebbero non essere compatibili nelle promozioni o nei criteri dinamici in fase di esecuzione con gli operatori “è uguale a” e “è diverso da”. Utilizzare [!UICONTROL Valore], [!UICONTROL Margine], [!UICONTROL Inventario], e [!UICONTROL Ambiente] valori correttamente sul lato destro se il lato sinistro dispone di attributi predefiniti o personalizzati.

![immagine left_right](assets/left_right.png)

Nella tabella seguente vengono mostrate regole efficaci e regole che potrebbero invece non essere compatibili in fase di esecuzione:

| Regole compatibili | Regole potenzialmente incompatibili |
|--- |--- |
| value - è tra - 90% e 110% dell’articolo corrente - salesValue | salesValue - è tra - 90% e 110% dell’articolo corrente - value |
| value - è tra - 90% e 110% dell’articolo corrente - value | clearancePrice - è tra - 90% e 110% dell’articolo corrente - margin |
| margin - è tra - 90% e 110% dell’articolo corrente - margin | storeInventory - è uguale a - dell’articolo corrente - inventory |
| inventory - è uguale a - dell’articolo corrente - inventory |  |
