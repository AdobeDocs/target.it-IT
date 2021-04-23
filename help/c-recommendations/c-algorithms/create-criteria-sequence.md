---
keywords: sequenza di criteri;criteri multipli;algoritmi;criteri;criteri di consigli;sequenza;numero limite di elementi restituiti;controllo a livello di slot;slot
description: Scopri come impostare sequenze di criteri fino a cinque per esercitare un maggiore controllo sugli elementi che compaiono nelle attività Adobe [!DNL Target] Recommendations.
title: Come si creano sequenze di criteri in Recommendations?
feature: Consigli
exl-id: 5366c86c-7685-478b-a621-9b3f24296ab7
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 34%

---

# ![PREMIUM](/help/assets/premium.png) Creare sequenze di criteri

Utilizza le sequenze di criteri (fino a cinque criteri per sequenza) per esercitare un maggiore controllo sugli elementi da visualizzare nelle attività [!UICONTROL Consigli. ] È inoltre possibile limitare il numero di elementi restituiti (talvolta denominati &quot;controllo a livello di slot&quot;).

>[!NOTE]
>
>Le sequenze di criteri non possono essere utilizzate con le attività [!UICONTROL Consigli] create prima del rilascio di [!DNL Target Premium] in ottobre 2016.

Per creare una sequenza di criteri, è necessario innanzitutto creare i criteri da includere nella sequenza. Consulta [Creare criteri](/help/c-recommendations/c-algorithms/create-new-algorithm.md) per ulteriori informazioni.

Utilizzando una sequenza di criteri, è possibile fornire ulteriori consigli mirati, anziché utilizzare consigli di backup più generici, quando un criterio non fornisce abbastanza risultati per completare il progetto. In genere, una sequenza di criteri procede da un targeting più specifico, che potrebbe restituire meno risultati, a un targeting più generale, che in genere restituisce più risultati.

Le sequenze di criteri possono variare in base al tipo di pagina, come illustrato negli esempi seguenti:

| Tipo di pagina | Ordine sequenziale possibile |
| --- | --- |
| Pagina di prodotto | <ol><li>In base all&#39;articolo corrente, della stessa marca</li><li>In base all&#39;articolo corrente, di tutte le marche</li><li>In base a somiglianza del contenuto</li><li>In base agli articoli più venduti</li><li>In base agli articoli più visualizzati di tutto il sito</li></ol> |
| Home page | <ol><li>In base all’ultimo acquisto del visitatore </li><li>In base all’articolo preferito del visitatore</li><li>In base alla categoria preferita del visitatore</li><li>In base agli articoli più venduti</li><li>In base agli articoli più visualizzati di tutto il sito</li></ol> |

## Creare una sequenza di criteri

Puoi creare sequenze di criteri dalla schermata [!UICONTROL Crea sequenza criteri] .

Esistono diversi modi per arrivare alla schermata [!UICONTROL Crea sequenza criteri]. Alcune opzioni dipendono dal modo in cui si raggiunge la schermata.

* Su **[!UICONTROL Consigli]** > **[!UICONTROL Criteri]**, fai clic su **[!UICONTROL Crea criterio]** > **[!UICONTROL Crea sequenza criteri]**. I criteri creati vengono automaticamente resi disponibili per tutte le attività di [!UICONTROL Consigli].
* Quando crei un&#39;attività [!UICONTROL Recommendations], dalla schermata Seleziona criteri fai clic su **[!UICONTROL Crea nuovo]** > **[!UICONTROL Crea sequenza criteri]**. Potrai salvare la nuova sequenza di criteri da utilizzare con altre attività di [!UICONTROL Consigli].
* Quando modifichi un&#39;attività [!UICONTROL Recommendations], fai clic in una casella [!UICONTROL Posizione Recommendations] sulla pagina, quindi seleziona **[!UICONTROL Cambia criteri]**. Nella schermata [!UICONTROL Seleziona criteri], fai clic su **[!UICONTROL Crea nuovo]** > **[!UICONTROL Crea sequenza criteri]**. Sarà possibile salvare i nuovi criteri da utilizzare per altre attività di [!UICONTROL Consigli].

I passaggi seguenti presuppongono l&#39;accesso alla schermata [!UICONTROL Crea sequenza criteri] utilizzando il primo metodo: la schermata della libreria **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** .

1. Fai clic su **[!UICONTROL Recommendations]** > **[!UICONTROL Criteri]**.

1. Fai clic su **[!UICONTROL Crea criteri]** > **[!UICONTROL Crea sequenza criteri]**.

   ![](assets/CreateCriteriaSequence.png)

1. Compila le informazioni nella sezione [Informazioni di base](/help/c-recommendations/c-algorithms/create-new-algorithm.md#info) .

1. Nella sezione **[!UICONTROL Sequenza criteri]**, fai clic su **[!UICONTROL Aggiungi criteri]**.

   L&#39;ordine di sequenza definisce l&#39;ordine in cui una progettazione viene riempita. Se i consigli per i criteri 1 non sono sufficienti per completare la progettazione, gli slot rimanenti verranno riempiti con i criteri 2 e così via.

   ![Aggiungi criteri](/help/c-recommendations/c-algorithms/assets/add-criteria.png)

1. Nella schermata [!UICONTROL Seleziona criteri], seleziona un criterio, quindi fai clic su **[!UICONTROL Aggiungi]**.

   Puoi utilizzare la casella Ricerca e i menu a discesa del filtro per trovare i criteri desiderati.

   ![Selezionare criteri](/help/c-recommendations/c-algorithms/assets/select-criteria.png)

1. (Facoltativo) Fare scorrere il percorso **[!UICONTROL Limita il numero di elementi restituiti]** in posizione &quot;on&quot;, quindi specificare il numero di elementi (tra 1 e 50).

   ![Limita il numero di elementi restituiti](/help/c-recommendations/c-algorithms/assets/limit-number.png)

   Per comprendere meglio il valore dell&#39;opzione [!UICONTROL Limita il numero di elementi restituiti] (talvolta denominata &quot;controllo del livello di slot&quot;), considera i seguenti casi d&#39;uso:

   * **Caso d&#39;uso 1**: Desideri disporre di un insieme di diversi tipi di elementi in un&#39;unica barra delle raccomandazioni. Ad esempio, si desidera mostrare un mix di abbigliamento (giacche) e top (camicie, T-shirt). A questo scopo, utilizza una raccolta per l’attività che include tutti i potenziali tipi di prodotto desiderati in qualsiasi slot del progetto. Quindi, imposta il tuo primo criterio con un filtro statico che limita i criteri per includere solo l&#39;usura esterna e imposta il tuo secondo criterio con un filtro statico che limita i criteri a includere solo i piani. Infine, aggiungi entrambi i criteri a una sequenza di criteri e limita i primi criteri a 2 slot.

      L&#39;area delle raccomandazioni potrebbe avere l&#39;aspetto seguente sul sito:

      ![Vassoio delle raccomandazioni per i prodotti](/help/c-recommendations/c-algorithms/assets/featured-products.png)

   * **Caso d&#39;uso 2**: Vuoi un mix di articoli alternativi e complementari. Imposta un criterio per utilizzare un algoritmo visualizzato/visualizzato e utilizza un filtro dinamico che limiti gli elementi consigliati alla categoria dell’elemento corrente. Imposta il secondo criterio per utilizzare un algoritmo visualizzato/acquistato e utilizza un filtro dinamico che include solo gli elementi consigliati che non corrispondono alla categoria dell’elemento corrente. Infine, aggiungi entrambi i criteri a una sequenza e limita i primi criteri a 2 slot.

1. Continua ad aggiungere altri criteri alla sequenza. È possibile aggiungere fino a cinque criteri a una sequenza.

1. Abilita le opzioni [Contenuto di backup](/help/c-recommendations/c-algorithms/create-new-algorithm.md#content).

1. Fai clic su **[!UICONTROL Salva]**.

   La sequenza di criteri verrà visualizzata nell&#39;elenco criteri.

   Per ulteriori informazioni sulle opzioni di logica per i consigli, consulta [Criteri](/help/c-recommendations/c-algorithms/algorithms.md).

## Video di formazione: Creare i criteri in Recommendations (12:33)  ![Badge tutorial](/help/assets/tutorial.png)

Questo video contiene le seguenti informazioni:

* Creare criteri
* Creare sequenze di criteri
* Caricare criteri personalizzati

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)
