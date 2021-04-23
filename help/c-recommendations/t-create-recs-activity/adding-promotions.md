---
keywords: promozioni;promozioni anteriori;promozioni posteriori;tipo di promozioni;elenco di articoli;promuovere per attributo;promuovere una raccolta
description: Scopri come aggiungere elementi promossi e controllarne il posizionamento nelle progettazioni Adobe [!DNL Target] Recommendations. Puoi aggiungere promozioni statiche e dinamiche.
title: Come si aggiungono le promozioni nei progetti Recommendations?
feature: Consigli
exl-id: bd5e5e12-a712-4c4c-9cf8-6b0f4834067b
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 56%

---

# ![PREMIUM](/help/assets/premium.png) Aggiungere promozioni

Aggiungi articoli in promozione e controllane il posizionamento nelle progettazioni di Adobe Target Recommendations. Puoi aggiungere promozioni statiche e dinamiche.

>[!IMPORTANT]
>
>Le regole di esclusione statica e dinamica sono funzioni molto efficaci che possono esserti utili nelle iniziative di marketing. Per informazioni dettagliate, esempi e scenari di utilizzo, consulta [Utilizzare regole di inclusione dinamiche e statiche](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

Quando si crea un’attività di [!DNL Recommendations], è possibile includere gli elementi promossi nel progetto di [!DNL Recommendations]. Le promozioni utilizzano gli slot disponibili in una progettazione e hanno la precedenza sui risultati dei criteri e sui consigli di backup. Ad esempio, se il progetto dispone di sei slot e ne utilizzi due per le promozioni, sono disponibili quattro slot per gli articoli consigliati in base ai criteri.

Le promozioni vengono deduplicate rispetto agli articoli consigliati dai criteri per l’attività, in modo che un dato articola non venga visualizzato due volte in una singola barra di consigli.

È possibile promuovere articoli specifici, promuovere gli articoli dinamicamente, promuoverli in base agli attributi o promuovere delle raccolte.

![](assets/add_promotion_toggles.png)

>[!NOTE]
>
>Utilizzando le promozioni cambiano la struttura e l’output CSV. Queste modifiche potrebbero avere un impatto su tutti i processi esterni che coinvolgono CSV, ad esempio le e-mail.

1. Nella pagina **[!UICONTROL Opzioni]**, scegli tra le opzioni **[!UICONTROL Promozione prima]** o **[!UICONTROL Promozione dopo]**.

   L’illustrazione seguente mostra l’opzione [!UICONTROL Promozione prima] attivata.

   ![Selezionare l’opzione Promozione prima](/help/c-recommendations/t-create-recs-activity/assets/add_promotion_front.png)

   È possibile inserire promozioni sia prima *sia* dopo i risultati dei criteri.
1. Impostare il numero di slot di progettazione da utilizzare per gli elementi promossi.

   È possibile utilizzare fino a 20 slot, a seconda del progetto di [!DNL Recommendations]. Ogni slot utilizzato diventa non disponibile per i consigli restituiti in base ai criteri.

1. Imposta una data di inizio e una data di fine per gli articoli promossi.

   Se non si imposta una data di inizio, la promozione inizia immediatamente. Se non si imposta una data di fine la promozione viene eseguita indefinitamente.

1. Seleziona un **[!UICONTROL Tipo di promozione]**.

   * Seleziona **[!UICONTROL Elenco di voci]** e immetti i valori `entity.id`, separati da virgole, degli articoli specifici che desideri promuovere.

   * Seleziona **[!UICONTROL Promuovi per attributo]** e aggiungi regole per definire gli attributi degli elementi che desideri promuovere.

      Se si seleziona Promuovi per attributo, è possibile creare corrispondenze dinamiche. Per ulteriori informazioni, consulta [Utilizzare regole di inclusione dinamiche e statiche](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

   * Seleziona **[!UICONTROL Promuovi una raccolta]** e scegli la raccolta di elementi che desideri promuovere.

      È possibile creare nuove raccolte da utilizzare per le promozioni. Consulta [Creare una raccolta](/help/c-recommendations/c-products/collections.md#task_1256DFF6842141FCAADD9E1428EF7F08) per ulteriori informazioni.
   Se si sceglie **[!UICONTROL Elenco di elementi]** come **[!UICONTROL Tipo di promozione]**, è possibile selezionare la casella di controllo **[!UICONTROL Ordine casuale degli elementi]**, se necessario.

   L’ordinamento predefinito per [!UICONTROL Elenco di elementi] si basa sull’ordine immesso nell’interfaccia utente o nell’API di Target. Se l&#39;elenco include più elementi rispetto al numero di slot impostati per le promozioni, l&#39;opzione [!UICONTROL Ordine articoli casuale] randomizza gli elementi promossi visualizzati nella progettazione. Scegliendo questa opzione [!DNL Target] si selezionano in modo casuale gli elementi abilitati per le promozioni nel modello dall’intero set di promozione su ogni hit.

   Se le entità non dispongono di un attributo `entity.value` (ad esempio, non vendi prodotti) puoi passare un valore numerico all’attributo `entity.value` , ad esempio la data di pubblicazione. In questo caso, gli elementi promossi possono essere promossi in base alla data di pubblicazione più recente, in ordine decrescente. L&#39;attributo `entity.value` è di tipo doppio; non accetta stringhe.

   Se hai selezionato l&#39;opzione **[!UICONTROL Promuovi per attributo]** o **[!UICONTROL Promuovi una raccolta]**, l&#39;opzione per randomizzare l&#39;ordine non è applicabile.

   Quando promuovi elementi specifici utilizzando le opzioni [!UICONTROL Promuovi per attributo] o [!UICONTROL Promuovi una raccolta] , l&#39;ordine predefinito in cui vengono presentati gli elementi si basa sull&#39;attributo `entity.value`, in ordine numerico decrescente.

   La tabella seguente illustra le differenze tra queste opzioni:

   | Tipo di promozione | Ordinamento predefinito | Ordinamento backup | Opzione filtro dinamico |
   | --- | --- | --- | --- |
   | Elenco elementi | Ordine immesso nell’interfaccia utente/API di Target | Casuale (se selezionato tramite interfaccia utente/API) | No |
   | Promuovi per attributo | `entity.value` (ordine decrescente) | Randomized su ogni richiesta (quando non è presente alcun attributo `entity.value`) | Sì |
   | Promuovere una raccolta | `entity.value` (ordine decrescente) | Randomized su ogni richiesta (quando non è presente alcun attributo `entity.value`) | No |

1. Fai clic su **[!UICONTROL Salva]**.

Le promozioni sono applicate a tutte le esperienze nell&#39;attività.
