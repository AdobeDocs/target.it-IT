---
keywords: promozioni;promozioni anteriori;promozioni posteriori;tipo di promozioni;elenco di articoli;promuovere per attributo;promuovere una raccolta
description: Scopri come aggiungere elementi promossi e controllarne il posizionamento nelle progettazioni di Adobe [!DNL Target] Recommendations. Puoi aggiungere promozioni statiche e dinamiche.
title: Come si aggiungono promozioni alle progettazioni di Consigli?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: bd5e5e12-a712-4c4c-9cf8-6b0f4834067b
source-git-commit: 07062b7df75300bd7558a24da5121df454520e42
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 40%

---

# Aggiungere promozioni

Aggiungi elementi promossi e controllane il posizionamento nelle progettazioni di [!DNL Adobe Target Recommendations]. Puoi aggiungere promozioni statiche e dinamiche.

>[!IMPORTANT]
>
>Le regole di esclusione statica e dinamica sono funzioni molto efficaci che possono esserti utili nelle iniziative di marketing. Per informazioni dettagliate, esempi e scenari di utilizzo, consulta [Utilizzare regole di inclusione dinamiche e statiche](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

Quando si crea un’attività di [!DNL Recommendations], è possibile includere gli elementi promossi nel progetto di [!DNL Recommendations]. Le promozioni utilizzano gli slot disponibili in una progettazione e hanno la precedenza sui risultati dei criteri e sui consigli di backup. Ad esempio, se il progetto dispone di sei slot e ne utilizzi due per le promozioni, sono disponibili quattro slot per gli articoli consigliati in base ai criteri.

Le promozioni vengono deduplicate rispetto agli articoli consigliati dai criteri per l’attività, in modo che un dato articola non venga visualizzato due volte in una singola barra di consigli.

È possibile promuovere articoli specifici, promuovere gli articoli dinamicamente, promuoverli in base agli attributi o promuovere delle raccolte.

Opzioni ![[!UICONTROL Front Promotion] e [!UICONTROL Back Promotion] nell&#39;interfaccia utente [!DNL Target]](assets/add_promotion_toggles.png)

>[!NOTE]
>
>Utilizzando le promozioni cambiano la struttura e l’output CSV. Queste modifiche potrebbero avere un impatto su tutti i processi esterni che coinvolgono CSV, ad esempio le e-mail.

1. Nella pagina **[!UICONTROL Options]**, fare clic sull&#39;interruttore **[!UICONTROL Front Promotion]** o **[!UICONTROL Back Promotion]**.

   Nella figura seguente viene illustrato come attivare/disattivare [!UICONTROL Front Promotion].

   ![Selezionare l’opzione Promozione prima](/help/main/c-recommendations/t-create-recs-activity/assets/add_promotion_front.png)

   È possibile inserire promozioni sia prima *sia* dopo i risultati dei criteri.

1. Impostare il numero di slot di progettazione da utilizzare per gli elementi promossi.

   È possibile utilizzare fino a 20 slot, a seconda del progetto di [!DNL Recommendations]. Ogni slot utilizzato diventa non disponibile per i consigli restituiti in base ai criteri.

1. Imposta una data di inizio e una data di fine per gli articoli promossi.

   Se non si imposta una data di inizio, la promozione inizia immediatamente. Se non si imposta una data di fine la promozione viene eseguita indefinitamente.

1. Seleziona **[!UICONTROL Promotion Type]**.

   * Seleziona **[!UICONTROL List of items]** e immetti i valori `entity.id`, separati da virgole, degli elementi specifici che desideri promuovere.

   * Selezionare **[!UICONTROL Promote by attribute]** e aggiungere regole per definire gli attributi degli elementi che si desidera promuovere.

     Se si seleziona [!UICONTROL Promote by Attribute], è possibile creare corrispondenze dinamiche. Per ulteriori informazioni, vedere [Utilizzare regole di inclusione dinamiche e statiche](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

   * Selezionare **[!UICONTROL Promote a collection]** e scegliere la raccolta di elementi che si desidera promuovere.

     È possibile creare nuove raccolte da utilizzare per le promozioni. Per ulteriori informazioni, vedere [Creare una raccolta](/help/main/c-recommendations/c-products/collections.md#task_1256DFF6842141FCAADD9E1428EF7F08).

   Se si sceglie **[!UICONTROL List of Items]** come **[!UICONTROL Promotion Type]**, è possibile selezionare la casella di controllo **[!UICONTROL Randomize Item Order]**, se necessario.

   L&#39;ordinamento predefinito per [!UICONTROL List of Items] si basa sull&#39;ordine immesso nell&#39;interfaccia utente o nell&#39;API di [!DNL Target]. Se l&#39;elenco include più elementi rispetto al numero di slot impostati per le promozioni, l&#39;opzione [!UICONTROL Randomize Item Order] consente di casualizzare gli elementi promossi visualizzati nella progettazione. La scelta di questa opzione fa sì che [!DNL Target] selezioni in modo casuale gli elementi abilitati per le promozioni nel modello dall&#39;intero set di promozione su ogni hit.

   Se le entità non dispongono di un attributo `entity.value` (ad esempio, non si vendono prodotti) è possibile passare un valore numerico nell&#39;attributo `entity.value`, ad esempio la data di pubblicazione. In questo caso, gli elementi promossi possono essere promossi in base alla data di pubblicazione più recente, in ordine decrescente. L&#39;attributo `entity.value` è di tipo double e non accetta stringhe.

   Se è stata selezionata l&#39;opzione **[!UICONTROL Promote by Attribute]** o **[!UICONTROL Promote a Collection]**, l&#39;opzione per la randomizzazione dell&#39;ordine non è applicabile.

   Quando si promuovono elementi specifici utilizzando le opzioni [!UICONTROL Promote by Attribute] o [!UICONTROL Promote a Collection], l&#39;ordine predefinito in cui vengono presentati gli elementi si basa sull&#39;attributo `entity.value`, in ordine numerico decrescente.

   La tabella seguente illustra le differenze tra queste opzioni:

   | Tipo di promozione | Ordinamento predefinito | Ordine di backup | Opzione filtro dinamico |
   | --- | --- | --- | --- |
   | [!UICONTROL List of Items] | Ordine immesso nell’interfaccia utente/API di Target | Casuale (se selezionata tramite interfaccia utente/API) | No |
   | [!UICONTROL Promote by Attribute] | `entity.value` (ordine decrescente) | Nessuna randomizzazione | Sì |
   | [!UICONTROL Promote a Collection] | `entity.value` (ordine decrescente) | Nessuna randomizzazione | No |

1. Fare clic su **[!UICONTROL Save]**.

Le promozioni sono applicate a tutte le esperienze nell&#39;attività.
