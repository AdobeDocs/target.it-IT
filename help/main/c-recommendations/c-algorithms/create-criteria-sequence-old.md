---
keywords: sequenza criteri;criteri multipli;algoritmi;criteri;criteri consigli;sequenza;numero limite di elementi restituiti;controllo a livello di slot;slot;criteria sequence;multiple criteria;algorithms;criteria;recommendations criteria;sequence;limit number of items returned;slot level control;slot level control;slot
description: Scopri come impostare sequenze fino a cinque criteri per esercitare un maggiore controllo sugli elementi visualizzati nelle attività Adobe [!DNL Target] Recommendations.
title: Come si creano sequenze di criteri in Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: 5366c86c-7685-478b-a621-9b3f24296ab7
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 23%

---

# Creare sequenze di criteri

Utilizzare sequenze di criteri fino a cinque per esercitare un maggiore controllo sugli elementi visualizzati nelle attività di [!UICONTROL Recommendations]. È inoltre possibile limitare il numero di elementi restituiti (talvolta denominati &quot;controllo a livello di slot&quot;).

>[!NOTE]
>
>Le sequenze di criteri non possono essere utilizzate con [!UICONTROL Recommendations] attività create prima del rilascio di [!DNL Target Premium] in ottobre 2016.

Per creare una sequenza di criteri, è necessario innanzitutto creare i criteri da includere nella sequenza. Per ulteriori informazioni, vedere [Creare i criteri](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md).

Utilizzando una sequenza di criteri, è possibile fornire ulteriori consigli mirati, anziché utilizzare consigli di backup più generici, quando un criterio non fornisce abbastanza risultati per completare il progetto. In genere, una sequenza di criteri passa dal targeting più specifico, che potrebbe restituire un numero minore di risultati, al targeting più generale, che in genere restituisce più risultati.

Le sequenze di criteri possono variare in ordine a seconda del tipo di pagina, come illustrato negli esempi seguenti:

| Tipo di pagina | Possibile ordine di sequenza |
| --- | --- |
| Pagina prodotto | <ol><li>In base all&#39;articolo corrente, della stessa marca</li><li>In base all&#39;articolo corrente, di tutte le marche</li><li>In base a somiglianza del contenuto</li><li>In base agli articoli più venduti</li><li>In base agli articoli più visualizzati di tutto il sito</li></ol> |
| Home page | <ol><li>In base all’ultimo acquisto del visitatore </li><li>In base all’articolo preferito del visitatore</li><li>In base alla categoria preferita del visitatore</li><li>In base agli articoli più venduti</li><li>In base agli articoli più visualizzati di tutto il sito</li></ol> |

## Creare una sequenza di criteri

È possibile creare sequenze di criteri dalla schermata [!UICONTROL Create Criteria Sequence].

Sono disponibili diversi modi per raggiungere la schermata [!UICONTROL Create Criteria Sequence]. Alcune opzioni dipendono dal modo in cui si raggiunge la schermata.

* Nella schermata della libreria **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**, fare clic su **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]**. I criteri creati vengono automaticamente resi disponibili per tutte le attività di [!UICONTROL Recommendations].
* Quando si crea un&#39;attività [!UICONTROL Recommendations], dalla schermata Seleziona criteri fare clic su **[!UICONTROL Create New]** > **[!UICONTROL Create Criteria Sequence]**. Sarà possibile salvare la nuova sequenza di criteri da utilizzare con altre attività di [!UICONTROL Recommendations].
* Quando modifichi un&#39;attività di [!UICONTROL Recommendations], fai clic su una casella di [!UICONTROL Recommendations Location] nella pagina, quindi seleziona **[!UICONTROL Change Criteria]**. Nella schermata [!UICONTROL Select Criteria], fare clic su **[!UICONTROL Create New]** > **[!UICONTROL Create Criteria Sequence]**. Sarà possibile salvare i nuovi criteri da utilizzare per altre attività di [!UICONTROL Recommendations].

Nei passaggi seguenti si presuppone che si acceda alla schermata [!UICONTROL Create Criteria Sequence] utilizzando il primo metodo: la schermata della libreria **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**.

1. Fare clic su **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**.

1. Fare clic su **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]**.

   ![Immagine CreateCriteriaSequence](assets/CreateCriteriaSequence.png)

1. Immettere le informazioni nella sezione [Informazioni di base](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info).

1. Nella sezione **[!UICONTROL Criteria Sequence]**, fare clic su **[!UICONTROL Add Criteria]**.

   L&#39;ordine sequenziale definisce l&#39;ordine di riempimento di una progettazione. Se il criterio 1 non ha abbastanza consigli per riempire la progettazione, gli slot rimanenti verranno riempiti con il criterio 2 e così via.

   ![Aggiungi criterio](/help/main/c-recommendations/c-algorithms/assets/add-criteria.png)

1. Nella schermata [!UICONTROL Select Criteria], selezionare un criterio, quindi fare clic su **[!UICONTROL Add]**.

   Puoi utilizzare la casella di ricerca e i menu a discesa dei filtri per trovare i criteri desiderati.

   ![Selezionare criteri](/help/main/c-recommendations/c-algorithms/assets/select-criteria.png)

1. (Facoltativo) Far scorrere l&#39;interruttore **[!UICONTROL Limit the number of items returned]** in posizione &quot;on&quot;, quindi specificare il numero di elementi (tra 1 e 50).

   ![Limita/disattiva il numero di elementi restituiti](/help/main/c-recommendations/c-algorithms/assets/limit-number.png)

   Per comprendere meglio il valore dell&#39;opzione [!UICONTROL Limit the number of items returned] (talvolta denominata &quot;controllo a livello di slot&quot;), considerare i seguenti casi d&#39;uso:

   * **Caso d&#39;uso 1**: si desidera disporre di un insieme di diversi tipi di elementi in un&#39;unica barra dei consigli. Ad esempio, vuoi mostrare un mix di outerwear (giacche) e top (camicie, T-shirt). A questo scopo, utilizza una raccolta per l’attività che include tutti i potenziali tipi di prodotto desiderati negli slot della progettazione. Quindi, imposta il primo criterio con un filtro statico che limita i criteri in modo da includere solo l’outerwear, e imposta il secondo criterio con un filtro statico che limita i criteri in modo da includere solo i top. Infine, aggiungi entrambi i criteri a una sequenza di criteri e limita il primo criterio a 2 slot.

     L’area dei consigli potrebbe presentarsi così sul sito:

     ![Vassoio consigli prodotti in primo piano](/help/main/c-recommendations/c-algorithms/assets/featured-products.png)

   * **Caso d&#39;uso 2**: si desidera una combinazione di elementi alternativi e complementari. Imposta un criterio per utilizzare un algoritmo visualizzato/visualizzato e un filtro dinamico che limiti gli elementi consigliati alla categoria dell’elemento corrente. Imposta il secondo criterio per utilizzare un algoritmo visualizzato/acquistato e un filtro dinamico che includa solo gli articoli consigliati che non corrispondono alla categoria dell’articolo corrente. Infine, aggiungi entrambi i criteri a una sequenza e limita il primo criterio a 2 slot.

1. Continua ad aggiungere altri criteri alla sequenza. È possibile aggiungere fino a cinque criteri a una sequenza.

1. Abilita [Opzioni di contenuto di backup](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content).

1. Fare clic su **[!UICONTROL Save]**.

   La sequenza di criteri verrà visualizzata nell&#39;elenco criteri.

   Per ulteriori informazioni sulle opzioni di logica per i consigli, consulta [Criteri](/help/main/c-recommendations/c-algorithms/algorithms.md).

## Video di formazione: Crea criteri in Recommendations (12:33) ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video contiene le seguenti informazioni:

* Creare criteri
* Creare sequenze di criteri
* Caricare criteri personalizzati

>[!VIDEO](https://video.tv.adobe.com/v/328806?quality=12&captions=ita)
