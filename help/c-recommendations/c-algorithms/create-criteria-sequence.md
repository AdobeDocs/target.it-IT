---
keywords: criteria sequence;multiple criteria;algorithms;criteria;recommendations criteria;sequence;
description: Utilizzate sequenze con un massimo di cinque criteri per esercitare un maggiore controllo sugli elementi visualizzati nelle attività di Adobe Target Recommendations .
title: Creare sequenze di criteri
feature: criteria
uuid: 9a5ca86b-fc79-4c24-b86f-e333b0c63088
translation-type: tm+mt
source-git-commit: 638d70f44a479f67cfe40854bc26b6180d33f935
workflow-type: tm+mt
source-wordcount: '1106'
ht-degree: 43%

---


# ![PREMIUM](/help/assets/premium.png) Creare sequenze di criteri

Utilizza le sequenze di criteri (fino a cinque criteri per sequenza) per esercitare un maggiore controllo sugli elementi da visualizzare nelle attività [!UICONTROL Consigli].

>[!NOTE]
>
>Le sequenze di criteri non possono essere utilizzate con le attività [!UICONTROL Consigli] create prima del rilascio di [!DNL Target Premium] in ottobre 2016.

Per creare una sequenza di criteri, è necessario innanzitutto creare i criteri da includere nella sequenza. Consulta [Creare criteri](/help/c-recommendations/c-algorithms/create-new-algorithm.md) per ulteriori informazioni.

Utilizzando una sequenza di criteri, è possibile fornire ulteriori consigli mirati, anziché utilizzare consigli di backup più generici, quando un criterio non fornisce abbastanza risultati per completare il progetto. In genere, una sequenza di criteri passa da un targeting più specifico, che potrebbe restituire meno risultati, a un targeting più generale, che in genere restituisce più risultati.

Le sequenze di criteri possono variare in base al tipo di pagina, come illustrato negli esempi seguenti:

| Tipo pagina | Possibile ordine di sequenza |
| --- | --- |
| Pagina prodotto | <ol><li>In base all&#39;articolo corrente, della stessa marca</li><li>In base all&#39;articolo corrente, di tutte le marche</li><li>In base a somiglianza del contenuto</li><li>In base agli articoli più venduti</li><li>In base agli articoli più visualizzati di tutto il sito</li></ol> |
| Home page | <ol><li>In base all’ultimo acquisto del visitatore </li><li>In base all’articolo preferito del visitatore</li><li>In base alla categoria preferita del visitatore</li><li>In base agli articoli più venduti</li><li>In base agli articoli più visualizzati di tutto il sito</li></ol> |

## Accedere alla schermata Crea sequenza criteri

Esistono diversi modi per arrivare alla schermata [!UICONTROL Crea sequenza criteri]. Alcune opzioni dipendono dal modo in cui si raggiunge la schermata.

* Su **[!UICONTROL Consigli]** > **[!UICONTROL Criteri]**, fai clic su **[!UICONTROL Crea criterio]** > **[!UICONTROL Crea sequenza criteri]**. I criteri creati vengono automaticamente resi disponibili per tutte le attività di [!UICONTROL Consigli].
* Quando create un&#39;attività [!UICONTROL Recommendations] , nella schermata Seleziona criteri fate clic su **[!UICONTROL Crea nuovo]** > **[!UICONTROL Crea sequenza]** criteri. Potrai salvare la nuova sequenza di criteri da utilizzare con altre attività di [!UICONTROL Consigli].
* When you are editing a [!UICONTROL Recommendations] activity, click in a [!UICONTROL Recommendations Location] box on your page, then select **[!UICONTROL Change Criteria]**. Nella schermata [!UICONTROL Seleziona criteri], fai clic su **[!UICONTROL Crea nuovo]** > **[!UICONTROL Crea sequenza criteri]**. Sarà possibile salvare i nuovi criteri da utilizzare per altre attività di [!UICONTROL Consigli].

Nella procedura seguente si presuppone che sia possibile accedere alla schermata [!UICONTROL Crea sequenza] criteri utilizzando il primo metodo: nella schermata Libreria **[!UICONTROL Recommendations]** > **[!UICONTROL Criteri]** .

1. Fate clic su **[!UICONTROL Recommendations]** > **[!UICONTROL Criteri]**.

1. Fate clic su **[!UICONTROL Crea criteri]** > **[!UICONTROL Crea sequenza]** criteri.

   ![](assets/CreateCriteriaSequence.png)

## Compila la sezione Informazioni

1. Digita un **[!UICONTROL Nome]** per la sequenza.

   Si tratta del nome “interno” usato per descrivere la sequenza di criteri. I visitatori del sito non vedranno questo nome.

   ![Sezione Informazioni sulla sequenza di criteri](/help/c-recommendations/c-algorithms/assets/criteria-sequence-info.png)

1. Digita un **[!UICONTROL Titolo di visualizzazione generico rivolto al pubblico]** in modo che sia visualizzato nella pagina nel caso in cui vengano utilizzati più criteri nella sequenza per riempire la progettazione dei [!UICONTROL Consigli].

   Ad esempio, si potrebbe desiderare di sostituire “I clienti che hanno visualizzato questo hanno visto anche...” con “Consigliato per te”, nel caso in cui la progettazione possa includere elementi in base a più di un codice [!UICONTROL Consigli].

1. Digita una breve **[!UICONTROL Descrizione]** della sequenza di criteri.

   La descrizione dovrebbe facilitare l&#39;identificazione della sequenza di criteri e potrebbe includere informazioni sulla sua funzione.

1. Seleziona un **[!UICONTROL Settore verticale]**.

   Your default [industry vertical](/help/c-recommendations/c-algorithms/algorithms.md#section_936BCFCF234C49A2BEC1C38AAC2D71AF) appears automatically.

1. Seleziona un **[!UICONTROL tipo di pagina]**.

   Puoi selezionare più tipi di pagina.

   Insieme, i tipi di pagina e i settori verticali vengono utilizzati per categorizzare la sequenza di criteri salvati, semplificando il riutilizzo delle sequenze per altre attività di [!UICONTROL Consigli].

## Crea sequenza {#sequence}

L’ordine di sequenza definisce l’ordine in cui la progettazione viene riempita. Se i criteri 1 non dispongono di un numero sufficiente di raccomandazioni per completare la progettazione, gli slot rimanenti verranno compilati con i criteri 2 e così via.

1. Nella sezione Sequenza **** criteri, fare clic su **[!UICONTROL Aggiungi criteri]**.

   ![Aggiungi criteri](/help/c-recommendations/c-algorithms/assets/add-criteria.png)

1. On the [!UICONTROL Select Criteria] screen, select a criteria.

   Potete usare la casella di ricerca e i menu a discesa dei filtri per individuare i criteri desiderati.

   ![Selezionare criteri](/help/c-recommendations/c-algorithms/assets/select-criteria.png)

1. Fai clic su **[!UICONTROL Aggiungi]**.

1. (Facoltativo) Fate scorrere il **[!UICONTROL limite del numero di elementi restituiti]** per passare alla posizione &quot;on&quot;, quindi specificate il numero di elementi (tra 1 e 50).

   ![Limita il numero di elementi restituiti](/help/c-recommendations/c-algorithms/assets/limit-number.png)

   Per comprendere meglio il valore dell&#39;opzione [!UICONTROL Limita il numero di elementi restituiti] , prendere in considerazione i seguenti casi di utilizzo:

   * **Caso d’uso 1**: Desiderate disporre di diversi tipi di elementi in un unico vassoio delle raccomandazioni. Ad esempio, si desidera mostrare un mix di abbigliamento (giacca) e top (camicie, T-shirt). A tal fine, utilizzate una raccolta per l&#39;attività che include tutti i potenziali tipi di prodotti che desiderate in qualsiasi slot del vostro progetto. Quindi, impostate il primo criterio con un filtro statico che limiti i criteri in modo che includano solo l&#39;uso esterno e il secondo criterio con un filtro statico che limiti i criteri in modo da includere solo i piani. Infine, aggiungete entrambi i criteri a una sequenza di criteri e limitate i primi criteri a 2 slot.

      Il vassoio delle raccomandazioni potrebbe essere simile al seguente sul sito:

      ![Vassoio delle raccomandazioni per i prodotti](/help/c-recommendations/c-algorithms/assets/featured-products.png)

   * **Caso d’uso 2**: Desiderate un mix di articoli alternativi e complementari. Impostate un criterio per utilizzare un algoritmo visualizzato/visualizzato e utilizzate un filtro dinamico che limiti gli elementi raccomandati alla categoria dell&#39;elemento corrente. Impostate il secondo criterio per utilizzare un algoritmo visualizzato/acquistato e utilizzate un filtro dinamico che includa solo gli elementi consigliati che non corrispondono alla categoria dell&#39;elemento corrente. Infine, aggiungete entrambi i criteri a una sequenza e limitate i primi criteri a 2 slot.

1. Continuate ad aggiungere altri criteri alla sequenza. È possibile aggiungere fino a cinque criteri a una sequenza.

## Specificare il contenuto di backup

Scegliete quale contenuto viene restituito quando non sono disponibili abbastanza raccomandazioni per compilare il modello di progettazione.

Quando si crea una sequenza di criteri, le impostazioni di backup e di rendering parziale della progettazione vengono ignorate per i singoli criteri che costituiscono la sequenza. Per utilizzare i consigli di backup e il rendering parziale della progettazione, è necessario abilitarli per la sequenza. Seleziona i pulsanti appropriati. Se si sceglie di consentire i consigli di backup, è altresì possibile scegliere se applicare le regole di inclusione ai backup.

![Impostazioni di backup del contenuto](/help/c-recommendations/c-algorithms/assets/backup-content-settings.png)

1. (Facoltativo) Fate scorrere l&#39;interruttore di rendering **[!UICONTROL della struttura]** parziale nella posizione &quot;attivato&quot;.

   Verranno compilati tutti gli slot possibili, ma il modello di progettazione potrebbe includere spazio vuoto per gli slot rimanenti.

1. (Facoltativo) Fate scorrere l’interruttore **[!UICONTROL Backup Recommendations]** nella posizione &quot;attivato&quot;.

   Riempite tutti gli slot vuoti rimanenti nel progetto con una selezione casuale di prodotti più visualizzati da tutto il sito.

   Per ulteriori informazioni, consultate [Utilizzare una raccomandazione](/help/c-recommendations/c-algorithms/backup-recs.md)di backup.

1. (Condizionale) Se avete selezionato **[!UICONTROL Backup Recommendations]** nel passaggio precedente, potete selezionare **[!UICONTROL Applica regole di inclusione alle raccomandazioni]** di backup.

   For more information see [Use dynamic and static inclusion rules](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md).

1. Fai clic su **[!UICONTROL Salva]**.

   La sequenza di criteri verrà visualizzata nell&#39;elenco criteri.

   Per ulteriori informazioni sulle opzioni di logica per i consigli, consulta [Criteri](../../c-recommendations/c-algorithms/algorithms.md#concept_4BD01DC437F543C0A13621C93A302750).

## Video di formazione: Creare i criteri in Recommendations (12:33) ![Badge di esercitazione](/help/assets/tutorial.png)

Questo video contiene le seguenti informazioni:

* Creare criteri
* Creare sequenze di criteri
* Caricare criteri personalizzati

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)
