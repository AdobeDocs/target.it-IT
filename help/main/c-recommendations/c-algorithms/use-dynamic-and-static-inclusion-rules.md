---
keywords: regole di inclusione;criteri di inclusione;consigli;creazione di nuovi criteri;promozione;promozioni;filtro dinamico;dinamico;valori vuoti;ignorare regola di filtro;filtro statico;filtro per valore;corrispondenza attributo entità;corrispondenza attributo profilo;parametro corrispondente;filtro per valore;filtro statico
description: Scopri come creare regole di inclusione in [!DNL Target] Recommendations per criteri e promozioni.
title: Come si utilizzano le regole di inclusione dinamiche e statiche nella funzione Consigli?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
mini-toc-levels: 3
exl-id: 49b20e75-ee55-4239-94a0-6d175e2d4811
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '1825'
ht-degree: 16%

---

# Utilizzare regole di inclusione dinamiche e statiche

Crea regole di inclusione per criteri e promozioni in [!DNL Adobe Target] e aggiungi regole di filtro dinamiche o statiche per ottenere risultati migliori per i consigli.

Le regole di inclusione per i criteri e le promozioni possono essere create e utilizzate con processi simili, così come sono simili i rispettivi casi ed esempi di utilizzo. I criteri e le promozioni e l’uso delle regole di inclusione sono trattati in questa sezione.

## Aggiungere regole di filtro a criteri e promozioni {#section_CD0D74B8D3BE4A75A78C36CF24A8C57F}

Le sezioni che seguono contengono le informazioni seguenti:

### Aggiungere regole di filtro ai criteri

1. Durante la [creazione dei criteri](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE) (**[!UICONTROL Recommendations]> [!UICONTROL Criteria] > [!UICONTROL Create Criteria] >[!UICONTROL Create Criteria]**), fare clic su **[!UICONTROL Add Filtering Rule]** in **[!UICONTROL Inclusion Rules]**.

   ![Aggiungi regola filtro](/help/main/c-recommendations/c-algorithms/assets/add-fitering-rule.png)

1. Fare clic sull&#39;elenco a discesa **Filtro statico** nella casella &quot;Quali altre regole devono soddisfare i consigli&quot;, quindi scegliere l&#39;opzione desiderata dall&#39;elenco a discesa [!UICONTROL Static Filter].

   ![Elenco a discesa Filtro statico](/help/main/c-recommendations/c-algorithms/assets/dynamic-and-static.png)

   Le opzioni disponibili dipendono dal settore verticale selezionato e della chiave consiglio.

### Aggiungere regole di filtro alle promozioni

1. Durante la [creazione di una promozione](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14), selezionare **[!UICONTROL Promote by Attribute]**, quindi fare clic su **[!UICONTROL Add Filtering Rule]**.

## Tipi di filtro {#section_0125F1ED10A84C0EB45325122460EBCD}

Nelle sezioni seguenti sono elencati i tipi di opzioni di filtro per [!UICONTROL Dynamic Filtering] e [!UICONTROL Filter by Value] sia per i criteri che per le promozioni:

### Filtro dinamico

Le regole di inclusione dinamica sono più potenti delle regole di inclusione statiche e producono risultati e coinvolgimento migliori. Considera i seguenti aspetti:

* Le regole di inclusione dinamica forniscono consigli facendo corrispondere un attributo nel parametro di profilo di un utente o in una chiamata mbox.

  Ad esempio, puoi creare un consiglio per &quot;Criteri più popolari&quot;. Dal set di consigli restituiti, puoi filtrare tutti i consigli (in tempo reale) in base a un attributo passato quando l’utente accede a una pagina in cui vengono visualizzati i consigli.

* Utilizza regole statiche per limitare quali elementi vengono inclusi nel consiglio (anziché utilizzare le raccolte).

* Puoi creare tutte le regole di inclusione dinamica necessarie. Le regole di inclusione vengono collegate mediante un operatore E. Gli articoli verranno inclusi in un consiglio solo se vengono soddisfatte tutte le regole.

Per il filtro dinamico sono disponibili le seguenti opzioni:

| Opzione filtro dinamico | Dettagli |
| --- | --- |
| [[!UICONTROL Entity Attribute Matching]](/help/main/c-recommendations/c-algorithms/entity-attribute-matching.md) | Filtra dinamicamente confrontando un pool di potenziali elementi di consigli con un elemento specifico con cui gli utenti hanno interagito.<P>Utilizza [!UICONTROL Entity Attribute Matching] per mostrare consigli che hanno più probabilità di attrarre il visitatore, ad esempio il suo marchio preferito. |
| [[!UICONTROL Profile Attribute Matching]](/help/main/c-recommendations/c-algorithms/profile-attribute-matching.md) | Filtrare dinamicamente confrontando gli articoli (entità) con un valore nel profilo dell’utente.<P>Utilizza [!UICONTROL Profile Attribute Matching] per mostrare consigli che corrispondono a un valore memorizzato nel profilo del visitatore, ad esempio le dimensioni o il marchio preferito. |
| [[!UICONTROL Parameter Matching]](/help/main/c-recommendations/c-algorithms/parameter-matching.md) | Filtra dinamicamente confrontando gli elementi (entità) con un valore nella richiesta (API o mbox).<P>Utilizza [!UICONTROL Parameter Matching] per consigliare contenuti che corrispondono ai parametri della pagina o ai parametri del visitatore, come dimensioni del dispositivo o geolocalizzazione. |

### Filtra per valore

Per filtrare per valore è disponibile la seguente opzione:

| Opzione Filtro per valore | Dettagli |
| --- | --- |
| [[!UICONTROL Static Filter]](/help/main/c-recommendations/c-algorithms/static-value.md) | Immetti manualmente uno o più valori statici da filtrare. |

## Operatori disponibili {#operators}

Le promozioni e i criteri dinamici sono molto più potenti di promozioni e criteri statici e offrono risultati e coinvolgimento migliori.

Gli esempi seguenti forniscono idee generali su come utilizzare promozioni ed esclusioni dinamiche nelle attività di marketing:

| Operatore | Esempi |
| --- | --- |
| [!UICONTROL equals any of]<P>(Disponibile con [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], [!UICONTROL Parameter Matching] e [!UICONTROL Static Filter].) | Utilizzando l&#39;operatore &quot;è uguale a&quot; nelle promozioni dinamiche, quando un visitatore sta visualizzando un articolo sul tuo sito web (ad esempio un prodotto, un articolo o un filmato), puoi promuovere altri articoli appartenenti a:<ul><li>Lo stesso marchio</li><li>La stessa categoria</li><li>La stessa categoria E dal marchio della casa</li><li>Lo stesso negozio</li></ul> |
| [!UICONTROL does not equal any of]<P>(Disponibile con [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], [!UICONTROL Parameter Matching] e [!UICONTROL Static Filter].) | Utilizzando l&#39;operatore &quot;[!UICONTROL does not equal any of]&quot; nelle promozioni dinamiche, quando un visitatore sta visualizzando un articolo sul tuo sito Web (ad esempio un prodotto, un articolo o un filmato), puoi promuovere altri articoli appartenenti a:<ul><li>Un&#39;altra serie TV</li><li>Un genere diverso</li><li>Una serie di prodotti diversa</li><li>Un ID di stile diverso</li></ul> |
| [!UICONTROL is greater than or equal to any of]<P>(Disponibile con [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], [!UICONTROL Parameter Matching] e [!UICONTROL Static Filter].) | Utilizzando l&#39;operatore &quot;[!UICONTROL is greater than or equal to any of]&quot;, quando un visitatore sta visualizzando un elemento sul tuo sito Web (ad esempio un prodotto), puoi promuovere altri elementi che:<ul><li>Costano lo stesso o sono più costosi</li></ul> |
| [!UICONTROL is less than or equal to any of]<P>(Disponibile con [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], [!UICONTROL Parameter Matching] e [!UICONTROL Static Filter].) | Utilizzando l&#39;operatore &quot;[!UICONTROL is less than or equal to an of]&quot;, quando un visitatore sta visualizzando un elemento sul tuo sito Web (ad esempio un prodotto), puoi promuovere altri elementi che:<ul><li>Costo uguale o inferiore</li><li>Escludi articoli meno costosi</li></ul> |
| [!UICONTROL contains any of] (disponibile con [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], [!UICONTROL Parameter Matching] e [!UICONTROL Static Filter].) | Utilizzando l&#39;operatore &quot;[!UICONTROL contains any of]&quot;, quando un visitatore sta visualizzando un elemento sul tuo sito Web (ad esempio un prodotto), puoi promuovere altri elementi che:<ul><li>Il titolo contiene lo stesso marchio</li></ul> |
| [!UICONTROL does not contain any of]<P>(Disponibile con [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], [!UICONTROL Parameter Matching] e [!UICONTROL Static Filter].) | Utilizzando l’operatore &quot;non contiene nessuno di&quot;, quando un visitatore sta visualizzando un articolo sul tuo sito web (ad esempio un prodotto), puoi promuovere altri articoli che:<ul><li>Il titolo non contiene una parolaccia</li></ul> |
| [!UICONTROL starts with any of]<P>(Disponibile con [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], [!UICONTROL Parameter Matching] e [!UICONTROL Static Filter].) | Utilizzando l&#39;operatore &quot;[!UICONTROL starts with an of]&quot;, quando un visitatore sta visualizzando un elemento sul tuo sito Web (ad esempio un prodotto), puoi promuovere altri elementi che:<ul><li>Il nome del prodotto inizia con iPhone</li></ul> |
| [!UICONTROL ends with any of]<P>(Disponibile con [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching], [!UICONTROL Parameter Matching] e [!UICONTROL Static Filter].) | Utilizzando l&#39;operatore &quot;[!UICONTROL ends with an of]&quot;, quando un visitatore sta visualizzando un elemento sul tuo sito Web (ad esempio un prodotto), puoi promuovere altri elementi che:<ul><li>Il contenuto termina con EN, che indica la lingua inglese</li></ul> |
| [!UICONTROL is between]<P>(Disponibile con [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] e [!UICONTROL Parameter Matching].) | Utilizzando l&#39;operatore &quot;i[!UICONTROL s between]&quot; nelle promozioni dinamiche, quando un visitatore sta visualizzando un articolo sul tuo sito Web (ad esempio un prodotto, un articolo o un filmato), puoi promuovere altri articoli che sono:<ul><li>Più costoso</li><li>Meno costoso</li><li>Costo più o meno 30%</li><li>Episodi successivi nella stessa stagione</li><li>Libri precedenti in una serie</li></ul> |
| [!UICONTROL list contains an item in]<P>(Disponibile con [!UICONTROL Profile Attribute Matching] e [!UICONTROL Parameter Matching].) | Utilizzando l&#39;operatore &quot;[!UICONTROL list contains an item in]&quot; nella corrispondenza degli attributi del profilo, quando un visitatore sta visualizzando un elemento sul tuo sito Web (ad esempio un prodotto, un articolo o un filmato), puoi promuovere altri elementi che sono:<ul><li>Disponibile nella zona geografica del visitatore</li></ul>**Esempio**: vuoi consigliare gli elementi disponibili solo nell&#39;area geografica di un visitatore.<P>La regola del filtro potrebbe essere simile alla seguente:<P>`availableGeographies list contains an item in user.currentGeography`<P>**Nota**: quando si utilizza questo operatore, è previsto un elenco nel [lato destro](#caveats) della regola. |
| [!UICONTROL list does not contain an item in]<P>(Disponibile con [!UICONTROL Profile Attribute Matching] e [!UICONTROL Parameter Matching].) | Utilizzando l&#39;operatore &quot;[!UICONTROL list does not contain an item in]&quot; nella corrispondenza degli attributi del profilo, quando un visitatore sta visualizzando un elemento sul tuo sito Web (ad esempio un prodotto, un articolo o un filmato), puoi escludere altri elementi:<ul><li>Nell’elenco degli ultimi dieci elementi visualizzati dal visitatore</li></ul></ul>**Esempio**: non promuovere gli elementi visualizzati di recente dal visitatore che non ha mostrato alcun interesse.<P>La regola di filtro potrebbe avere un aspetto simile a:<P>`id is not contained in list user.lastViewedItems`<P>**Nota**: quando si utilizza questo operatore, è previsto un elenco nel [lato destro](#caveats) della regola. |
| [!UICONTROL list contains an item in]<P>(Disponibile con [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] e [!UICONTROL Parameter Matching].) | Utilizzando l&#39;operatore &quot;[!UICONTROL list contains an item in]&quot; nella corrispondenza degli attributi del profilo, quando un visitatore sta visualizzando un elemento sul tuo sito Web (ad esempio un evento sportivo o un concerto), puoi promuovere altri elementi che sono:<ul><li>Associato a uno dei team preferiti del visitatore</li></ul>**Esempio**: vuoi consigliare i giochi associati a uno dei team preferiti del visitatore.<P>La regola di filtro potrebbe avere un aspetto simile a:<P>` teamsPlaying list contains an item in user.favoriteTeams`<P>**Nota**: quando si utilizza questo operatore, è previsto un elenco in [entrambi i lati](#caveats) della regola. |
| [!UICONTROL list does not contain an item in]<P>(Disponibile con [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] e [!UICONTROL Parameter Matching].) | Utilizzando l&#39;operatore &quot;[!UICONTROL list does not contain an item in]&quot; nella corrispondenza degli attributi dei parametri, quando un visitatore sta visualizzando un elemento sul tuo sito Web (ad esempio un prodotto, un articolo o un filmato), puoi escludere altri elementi:<ul><li>Contenuto in un elenco di tipi proibiti</li></ul>**Esempio**: vuoi escludere gli articoli disponibili per i visitatori adulti, ad esempio tabacco e alcol.<P>La regola di filtro potrebbe avere un aspetto simile a:<P>`itemType is not contained in list mbox.prohibitedTypes`<P>**Nota**: quando si utilizza questo operatore, è previsto un elenco in [entrambi i lati](#caveats) della regola. |
| [!UICONTROL list contains all items in]<P>(Disponibile con [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] e [!UICONTROL Parameter Matching].) | Utilizzando l&#39;operatore &quot;[!UICONTROL list does not contain an item in]&quot; nella corrispondenza degli attributi del profilo, quando un visitatore sta visualizzando un elemento sul tuo sito Web (ad esempio un annuncio di lavoro o una ricetta), puoi promuovere altri elementi che:<ul><li>Includi un set di abilità</li><li>Includi una serie di componenti richiesti</li></ul>**Esempio 1**: supponiamo che un visitatore abbia una serie di abilità (Java, C++ e HTML). Gli elementi nel catalogo sono processi con competenze richieste (Java e HTML). Desideri accertarti che il profilo del visitatore contenga tutte le competenze richieste prima di consigliare il lavoro al visitatore.<P>La regola di filtro potrebbe avere un aspetto simile a:<P>`profile.jobSeekerSkills contains all items in entity.requiredSkills`<P>**Esempio 2**: si supponga che un utente disponga di un elenco di ingredienti della dispensa. La ricetta contiene un elenco degli ingredienti necessari. Desideri accertarti che il profilo del visitatore contenga tutti gli ingredienti necessari prima di consigliare la ricetta al visitatore.<P>La regola di filtro potrebbe avere un aspetto simile a:<P>`profile.ingredientsInPantry contains all items in recipe.ingredientsRequired`<P>**Nota**: quando si utilizza questo operatore, è previsto un elenco in [entrambi i lati](#caveats) della regola. |
| [!UICONTROL list does not contain all items in]<P>(Disponibile con [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] e [!UICONTROL Parameter Matching].) | Utilizzando l&#39;operatore &quot;[!UICONTROL list does not contain all items in]&quot; nella corrispondenza degli attributi di entità, quando un visitatore sta visualizzando un elemento sul tuo sito Web (ad esempio un evento sportivo o un concerto), puoi promuovere altri elementi che:<ul><li>Non includere un set di team</li></ul>**Esempio**: supponiamo che un evento sportivo includa due squadre. Il profilo del visitatore indica che il visitatore non desidera visualizzare i giochi per questi team. Desideri evitare di consigliare un gioco se queste squadre stanno giocando.<P>La regola di filtro potrebbe avere un aspetto simile a:<P>`profile.leastfavoriteTeams does not contain all items in entity.teamsPlaying`<P>**Nota**: quando si utilizza questo operatore, è previsto un elenco in [entrambi i lati](#caveats) della regola. |

## Gestione dei valori vuoti durante il filtraggio per [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] e [!UICONTROL Parameter Matching] {#section_7D30E04116DB47BEA6FF840A3424A4C8}

Puoi scegliere diverse opzioni per gestire i valori vuoti quando filtri per [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] e [!UICONTROL Parameter Matching] per i criteri di uscita e le promozioni.

In precedenza, non veniva restituito alcun risultato se un valore era vuoto. L&#39;elenco a discesa “Se *x* è vuoto” consente di scegliere l&#39;azione da eseguire se i criteri hanno valori vuoti, come illustrato di seguito:

![immagine valore_vuoto](assets/empty_value.png)

Per selezionare l&#39;azione desiderata, passa il puntatore sull&#39;icona ingranaggio (![icon_gear image](assets/icon_gear.png)), quindi scegli l&#39;azione desiderata:

| Azione | Disponibile per | Dettagli |
|--- |--- |--- |
| [!UICONTROL Ignore this filtering rule] | [!UICONTROL Profile Attribute Matching] e [!UICONTROL Parameter Matching] | Questa azione è predefinita per [!UICONTROL Profile Attribute Matching] e [!UICONTROL Parameter Matching].<P>Questa opzione specifica che la regola viene ignorata. Ad esempio, se sono presenti tre regole di filtro e la terza regola non passa alcun valore, invece di non restituire alcun risultato si può semplicemente ignorare la terza regola con valori vuoti. |
| [!UICONTROL Do not show any results for this criteria]<P>(Solo criteri) | [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] e [!UICONTROL Parameter Matching] | Questa è l&#39;azione predefinita per [!UICONTROL Entity Attribute Matching].<P>Questa azione indica il modo in cui [!DNL Target] ha gestito i valori vuoti prima dell&#39;aggiunta di questa opzione: non vengono visualizzati risultati per questo criterio. |
| [!UICONTROL Non promuovere alcun elemento<P>(Solo promozioni)] | [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] e [!UICONTROL Parameter Matching] | Questa è l&#39;azione predefinita per [!UICONTROL Entity Attribute Matching].<P>Questa azione indica il modo in cui [!DNL Target] ha gestito i valori vuoti prima dell&#39;aggiunta di questa opzione: non vengono visualizzati risultati per questo criterio. |
| [!UICONTROL Use a static value] | [!UICONTROL Entity Attribute Matching], [!UICONTROL Profile Attribute Matching] e [!UICONTROL Parameter Matching] | Se un valore è vuoto, è possibile scegliere di utilizzare un valore statico. |

## Avvertenze {#caveats}

>[!IMPORTANT]
>
>Gli attributi di tipi di dati diversi potrebbero non essere compatibili nelle promozioni o nei criteri dinamici in fase di esecuzione con gli operatori “è uguale a” e “non è uguale a”. Utilizzare i valori [!UICONTROL Value], [!UICONTROL Margin], [!UICONTROL Inventory] e [!UICONTROL Environment] in modo appropriato sul lato destro se sul lato sinistro sono presenti attributi predefiniti o attributi personalizzati.

![immagine sinistra_destra](assets/left_right.png)

Nella tabella seguente vengono mostrate regole efficaci e regole che potrebbero invece non essere compatibili in fase di esecuzione:

| Regole compatibili | Regole potenzialmente incompatibili |
|--- |--- |
| value - è tra - 90% e 110% dell’articolo corrente - salesValue | salesValue - è tra - 90% e 110% dell’articolo corrente - value |
| value - è tra - 90% e 110% dell’articolo corrente - value | clearancePrice - è tra - 90% e 110% dell’articolo corrente - margin |
| margin - è tra - 90% e 110% dell’articolo corrente - margin | storeInventory - è uguale a - dell’articolo corrente - inventory |
| inventory - è uguale a - dell’articolo corrente - inventory |  |
