---
description: Aggiungi articoli in promozione e controllane il posizionamento nelle progettazioni dei consigli. Puoi aggiungere promozioni statiche e dinamiche.
keywords: Promozioni;promozioni prima;promozioni dopo;tipo di promozioni
seo-description: Aggiungete elementi promossi e controllatene il posizionamento nelle progettazioni di Adobe Target Recommendations. Puoi aggiungere promozioni statiche e dinamiche.
seo-title: Aggiungete promozioni nelle progettazioni di Adobe Target.
solution: Target
title: Aggiungere promozioni
title-outputclass: premium
topic: Premium
uuid: 732bf2c2-0cc7-4d5d-9919-9fe668344d39
badge: premium
translation-type: tm+mt
source-git-commit: e8e6dcadf307209abcc712798b714af0a5be2e7e

---


# ![PREMIUM](/help/assets/premium.png) Aggiungere promozioni{#add-promotions}

Aggiungi articoli in promozione e controllane il posizionamento nelle progettazioni dei consigli. Puoi aggiungere promozioni statiche e dinamiche.

>[!IMPORTANT]
>
>Le regole di esclusione statica e dinamica sono funzioni molto efficaci che possono esserti utili nelle iniziative di marketing. Per informazioni dettagliate, esempi e scenari di utilizzo, consulta [Utilizzare regole di inclusione dinamiche e statiche](../../c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

Quando si crea un’attività di [!DNL Recommendations], è possibile includere gli elementi promossi nel progetto di [!DNL Recommendations]. Le promozioni utilizzano gli slot disponibili in una progettazione e hanno la precedenza sui risultati dei criteri e sui consigli di backup. Ad esempio, se il progetto dispone di sei slot e ne utilizzi due per le promozioni, sono disponibili quattro slot per gli articoli consigliati in base ai criteri.

Le promozioni vengono deduplicate rispetto agli elementi consigliati dai criteri per l'attività, pertanto un dato elemento non verrà visualizzato due volte in una singola vassoio delle raccomandazioni.

È possibile promuovere elementi specifici, promuovere dinamicamente gli elementi, promuovere gli elementi in base agli attributi o promuoverne gli insiemi.

![](assets/add_promotion_toggles.png)

>[!NOTE]
>
>Utilizzando le promozioni cambiano la struttura e l’output CSV. Queste modifiche potrebbero avere un impatto su tutti i processi esterni che coinvolgono CSV, ad esempio le e-mail.

1. On the **[!UICONTROL Options]** page, click the **[!UICONTROL Front Promotion]** or **[!UICONTROL Back Promotion]** toggle.

   The following illustration shows the [!UICONTROL Front Promotion] toggle in the "On" position.

   ![Opzioni di promozione Aggiungi](/help/c-recommendations/t-create-recs-activity/assets/add_promotion_front.png)

   È possibile inserire promozioni sia prima *sia* dopo i risultati dei criteri.
1. Impostare il numero di slot di progettazione da utilizzare per gli elementi promossi.

   È possibile utilizzare fino a 20 slot, a seconda del progetto di [!DNL Recommendations]. Ogni slot utilizzato diventa non disponibile per i consigli restituiti in base ai criteri.

1. Imposta una data di inizio e una data di fine per gli elementi promossi.

   Se non impostate una data di inizio, la promozione inizia immediatamente. Se non impostate una data di fine, la promozione viene eseguita indefinitamente.

1. Seleziona un **[!UICONTROL Tipo di promozione]**.

   * Seleziona **[!UICONTROL Elenco di voci]** e immetti i valori `entity.id`, separati da virgole, degli elementi specifici che desideri promuovere.

      Se l'elenco include più elementi rispetto al numero di slot impostati per le promozioni, è possibile selezionare la casella **[!UICONTROL Ordine casuale degli articoli]per variare gli elementi promossi visualizzati nella progettazione.** Quando si sceglie questa opzione, Target seleziona in modo casuale il numero di elementi abilitati per le promozioni nel modello dall'intero set di promozioni per ogni visita.

   * Seleziona **[!UICONTROL Promuovi per attributo]** e aggiungi regole per definire gli attributi degli elementi che desideri promuovere.

      Se si seleziona Promuovi per attributo, è possibile creare corrispondenze dinamiche. Per ulteriori informazioni, consulta [Utilizzare regole di inclusione dinamiche e statiche](../../c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

   * Seleziona **[!UICONTROL Promuovi una raccolta]** e scegli la raccolta di elementi che desideri promuovere. È possibile creare nuove raccolte da utilizzare per le promozioni. Consulta [Creare una raccolta](../../c-recommendations/c-products/collections.md#task_1256DFF6842141FCAADD9E1428EF7F08) per ulteriori informazioni.

1. Fai clic su **[!UICONTROL Salva]**.

Le promozioni sono applicate a tutte le esperienze nell'attività.
