---
keywords: promozioni;promozioni anteriori;promozioni posteriori;tipo di promozioni;elenco di articoli;promuovere per attributo;promuovere una raccolta
description: Scopri come aggiungere articoli in promozione e controllarne il posizionamento nell’Adobe [!DNL Target] Progetti Recommendations. Puoi aggiungere promozioni statiche e dinamiche.
title: Come si aggiungono promozioni ai progetti Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: bd5e5e12-a712-4c4c-9cf8-6b0f4834067b
source-git-commit: 07062b7df75300bd7558a24da5121df454520e42
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 49%

---

# Aggiungere promozioni

Aggiungi articoli in promozione e controllane il posizionamento nel tuo [!DNL Adobe Target Recommendations] progetti. Puoi aggiungere promozioni statiche e dinamiche.

>[!IMPORTANT]
>
>Le regole di esclusione statica e dinamica sono funzioni molto efficaci che possono esserti utili nelle iniziative di marketing. Per informazioni dettagliate, esempi e scenari di utilizzo, consulta [Utilizzare regole di inclusione dinamiche e statiche](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

Quando si crea un’attività di [!DNL Recommendations], è possibile includere gli elementi promossi nel progetto di [!DNL Recommendations]. Le promozioni utilizzano gli slot disponibili in una progettazione e hanno la precedenza sui risultati dei criteri e sui consigli di backup. Ad esempio, se il progetto dispone di sei slot e ne utilizzi due per le promozioni, sono disponibili quattro slot per gli articoli consigliati in base ai criteri.

Le promozioni vengono deduplicate rispetto agli articoli consigliati dai criteri per l’attività, in modo che un dato articola non venga visualizzato due volte in una singola barra di consigli.

È possibile promuovere articoli specifici, promuovere gli articoli dinamicamente, promuoverli in base agli attributi o promuovere delle raccolte.

![[!UICONTROL Promozione prima] e [!UICONTROL Promozione dopo] opzioni in [!DNL Target] UI](assets/add_promotion_toggles.png)

>[!NOTE]
>
>Utilizzando le promozioni cambiano la struttura e l’output CSV. Queste modifiche potrebbero avere un impatto su tutti i processi esterni che coinvolgono CSV, ad esempio le e-mail.

1. Nella pagina **[!UICONTROL Opzioni]**, scegli tra le opzioni **[!UICONTROL Promozione prima]** o **[!UICONTROL Promozione dopo]**.

   L’illustrazione seguente mostra l’opzione [!UICONTROL Promozione prima] attivata.

   ![Selezionare l’opzione Promozione prima](/help/main/c-recommendations/t-create-recs-activity/assets/add_promotion_front.png)

   È possibile inserire promozioni sia prima *sia* dopo i risultati dei criteri.

1. Impostare il numero di slot di progettazione da utilizzare per gli elementi promossi.

   È possibile utilizzare fino a 20 slot, a seconda del progetto di [!DNL Recommendations]. Ogni slot utilizzato diventa non disponibile per i consigli restituiti in base ai criteri.

1. Imposta una data di inizio e una data di fine per gli articoli promossi.

   Se non si imposta una data di inizio, la promozione inizia immediatamente. Se non si imposta una data di fine la promozione viene eseguita indefinitamente.

1. Seleziona un **[!UICONTROL Tipo di promozione]**.

   * Seleziona **[!UICONTROL Elenco di voci]** e immetti i valori `entity.id`, separati da virgole, degli articoli specifici che desideri promuovere.

   * Seleziona **[!UICONTROL Promuovi per attributo]** e aggiungi regole per definire gli attributi degli elementi che desideri promuovere.

      Se si seleziona [!UICONTROL Promuovi per attributo], puoi creare corrispondenze dinamiche. Per ulteriori informazioni, consulta [Utilizzare regole di inclusione dinamiche e statiche](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

   * Seleziona **[!UICONTROL Promuovi una raccolta]** e scegli la raccolta di elementi che desideri promuovere.

      È possibile creare nuove raccolte da utilizzare per le promozioni. Consulta [Creare una raccolta](/help/main/c-recommendations/c-products/collections.md#task_1256DFF6842141FCAADD9E1428EF7F08) per ulteriori informazioni.
   Se si sceglie **[!UICONTROL Elenco di voci]** come **[!UICONTROL Tipo di promozione]**, è possibile selezionare **[!UICONTROL Ordine elementi casuale]** , se necessario.

   Ordinamento predefinito per [!UICONTROL Elenco di voci] si basa sull&#39;ordine immesso in [!DNL Target] Interfaccia utente o API. Se l’elenco include più elementi rispetto al numero di slot impostati per le promozioni, il [!UICONTROL Ordine elementi casuale] L’opzione consente di casualizzare gli elementi promossi visualizzati nel progetto. La scelta di questa opzione comporta [!DNL Target] selezionando in modo casuale gli elementi abilitati per le promozioni nel modello dall&#39;intero set di promozione su ogni hit.

   Se le entità non dispongono di un `entity.value` (ad esempio, non si vendono prodotti) è possibile trasmettere un valore numerico nel campo `entity.value` ad esempio la data di pubblicazione. In questo caso, gli elementi promossi possono essere promossi in base alla data di pubblicazione più recente, in ordine decrescente. Il `entity.value` l&#39;attributo è di tipo double e non accetta stringhe.

   Se hai selezionato **[!UICONTROL Promuovi per attributo]** o **[!UICONTROL Promuovi una raccolta]** , l’opzione per randomizzare l’ordine non è applicabile.

   Quando si promuovono elementi specifici utilizzando [!UICONTROL Promuovi per attributo] o [!UICONTROL Promuovi una raccolta] opzioni, l&#39;ordine predefinito in cui vengono presentati gli elementi è basato su `entity.value` decrescente.

   La tabella seguente illustra le differenze tra queste opzioni:

   | Tipo di promozione | Ordinamento predefinito | Ordine di backup | Opzione filtro dinamico |
   | --- | --- | --- | --- |
   | [!UICONTROL Elenco di voci] | Ordine immesso nell’interfaccia utente/API di Target | Casuale (se selezionata tramite interfaccia utente/API) | No |
   | [!UICONTROL Promuovi per attributo] | `entity.value` (ordine decrescente) | Nessuna randomizzazione | Sì |
   | [!UICONTROL Promuovi una raccolta] | `entity.value` (ordine decrescente) | Nessuna randomizzazione | No |

1. Fai clic su **[!UICONTROL Salva]**.

Le promozioni sono applicate a tutte le esperienze nell&#39;attività.
