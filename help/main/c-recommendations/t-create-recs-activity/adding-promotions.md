---
keywords: promozioni;promozioni anteriori;promozioni posteriori;tipo di promozioni;elenco di articoli;promuovere per attributo;promuovere una raccolta
description: Scopri come aggiungere elementi promossi e controllarne il posizionamento nelle progettazioni di Adobe [!DNL Target] Recommendations. Puoi aggiungere promozioni statiche e dinamiche.
title: Come si aggiungono promozioni alle progettazioni di Consigli?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: bd5e5e12-a712-4c4c-9cf8-6b0f4834067b
TQID: https://experienceleague.adobe.com/tAfKOzwjnUJgypDh-4LdVukNlTVwMS4UkvcNmCaCV0E
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 709
ht-degree: 41%

---

# Aggiungere promozioni

Aggiungi elementi promossi e controllane il posizionamento nelle progettazioni di [!DNL Adobe Target Recommendations]. Puoi aggiungere promozioni statiche e dinamiche.

>[!IMPORTANT]
>
>Le regole di esclusione statica e dinamica sono funzioni molto efficaci che possono esserti utili nelle iniziative di marketing. Per informazioni dettagliate, esempi e scenari di utilizzo, consulta [Utilizzare regole di inclusione dinamiche e statiche](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

Quando si crea un’attività di [!DNL Recommendations], è possibile includere gli elementi promossi nel progetto di [!DNL Recommendations]. Le promozioni utilizzano gli slot disponibili in una progettazione e hanno la precedenza sui risultati dei criteri e sui consigli di backup. Ad esempio, se il progetto dispone di sei slot e ne utilizzi due per le promozioni, sono disponibili quattro slot per gli articoli consigliati in base ai criteri.

Le promozioni vengono deduplicate rispetto agli articoli consigliati dai criteri per l’attività, in modo che un dato articola non venga visualizzato due volte in una singola barra di consigli.

È possibile promuovere articoli specifici, promuovere gli articoli dinamicamente, promuoverli in base agli attributi o promuovere delle raccolte.

![[!UICONTROL Promozione prima] e [!UICONTROL Promozione dopo] opzioni nell&#39;interfaccia utente [!DNL Target]](assets/add_promotion_toggles.png)

>[!NOTE]
>
>Utilizzando le promozioni cambiano la struttura e l’output CSV. Queste modifiche potrebbero avere un impatto su tutti i processi esterni che coinvolgono CSV, ad esempio le e-mail.

1. Nella pagina **[!UICONTROL Opzioni]**, fai clic sull&#39;interruttore **[!UICONTROL Promozione prima]** o **[!UICONTROL Promozione dopo]**.

   La figura seguente mostra l&#39;opzione [!UICONTROL Promozione prima] attivata.

   ![Selezionare l’opzione Promozione prima](/help/main/c-recommendations/t-create-recs-activity/assets/add_promotion_front.png)

   È possibile inserire promozioni sia prima *sia* dopo i risultati dei criteri.

1. Impostare il numero di slot di progettazione da utilizzare per gli elementi promossi.

   È possibile utilizzare fino a 20 slot, a seconda del progetto di [!DNL Recommendations]. Ogni slot utilizzato diventa non disponibile per i consigli restituiti in base ai criteri.

1. Imposta una data di inizio e una data di fine per gli articoli promossi.

   Se non si imposta una data di inizio, la promozione inizia immediatamente. Se non si imposta una data di fine la promozione viene eseguita indefinitamente.

1. Seleziona un **[!UICONTROL Tipo di promozione]**.

   * Seleziona **[!UICONTROL Elenco di elementi]** e immetti i valori `entity.id`, separati da virgole, degli elementi specifici che desideri promuovere.

   * Seleziona **[!UICONTROL Promuovi per attributo]** e aggiungi regole per definire gli attributi degli elementi che desideri promuovere.

     Se si seleziona [!UICONTROL Promuovi per attributo], è possibile creare corrispondenze dinamiche. Per ulteriori informazioni, vedere [Utilizzare regole di inclusione dinamiche e statiche](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

   * Seleziona **[!UICONTROL Promuovi una raccolta]** e scegli la raccolta di elementi che desideri promuovere.

     È possibile creare nuove raccolte da utilizzare per le promozioni. Per ulteriori informazioni, vedere [Creare una raccolta](/help/main/c-recommendations/c-products/collections.md#task_1256DFF6842141FCAADD9E1428EF7F08).

   Se si sceglie **[!UICONTROL Elenco di elementi]** come **[!UICONTROL Tipo promozione]**, è possibile selezionare la casella di controllo **[!UICONTROL Ordine elementi casuale]**, se necessario.

   L&#39;ordinamento predefinito per [!UICONTROL Elenco di elementi] si basa sull&#39;ordine immesso nell&#39;interfaccia utente o nell&#39;API [!DNL Target]. Se l&#39;elenco include più elementi rispetto al numero di slot impostati per le promozioni, l&#39;opzione [!UICONTROL Ordine elementi casuale] consente di randomizzare gli elementi promossi visualizzati nella progettazione. La scelta di questa opzione fa sì che [!DNL Target] selezioni in modo casuale gli elementi abilitati per le promozioni nel modello dall&#39;intero set di promozione su ogni hit.

   Se le entità non dispongono di un attributo `entity.value` (ad esempio, non si vendono prodotti) è possibile passare un valore numerico nell&#39;attributo `entity.value`, ad esempio la data di pubblicazione. In questo caso, gli elementi promossi possono essere promossi in base alla data di pubblicazione più recente, in ordine decrescente. L&#39;attributo `entity.value` è di tipo double e non accetta stringhe.

   Se hai selezionato l&#39;opzione **[!UICONTROL Promuovi per attributo]** o **[!UICONTROL Promuovi una raccolta]**, l&#39;opzione per la randomizzazione dell&#39;ordine non è applicabile.

   Quando si promuovono elementi specifici utilizzando le opzioni [!UICONTROL Promuovi per attributo] o [!UICONTROL Promuovi una raccolta], l&#39;ordine predefinito in cui vengono presentati gli elementi è basato sull&#39;attributo `entity.value`, in ordine numerico decrescente.

   La tabella seguente illustra le differenze tra queste opzioni:

   | Tipo di promozione | Ordinamento predefinito | Ordine di backup | Opzione filtro dinamico |
   | --- | --- | --- | --- |
   | [!UICONTROL Elenco di elementi] | Ordine immesso nell’interfaccia utente/API di Target | Casuale (se selezionata tramite interfaccia utente/API) | No |
   | [!UICONTROL Promuovi per attributo] | `entity.value` (ordine decrescente) | Nessuna randomizzazione | Sì |
   | [!UICONTROL Promuovi una raccolta] | `entity.value` (ordine decrescente) | Nessuna randomizzazione | No |

1. Fai clic su **[!UICONTROL Salva]**.

Le promozioni sono applicate a tutte le esperienze nell&#39;attività.
