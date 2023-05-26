---
keywords: sequenza criteri;criteri multipli;algoritmi;criteri;criteri consigli;sequenza;numero limite di elementi restituiti;controllo a livello di slot;slot;criteria sequence;multiple criteria;algorithms;criteria;recommendations criteria;sequence;limit number of items returned;slot level control;slot level control;slot
description: Scopri come impostare sequenze fino a cinque criteri per esercitare un maggiore controllo sugli elementi visualizzati nell’Adobe. [!DNL Target] Attività Recommendations.
title: Come si creano sequenze di criteri in Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: 5366c86c-7685-478b-a621-9b3f24296ab7
source-git-commit: bde5506033fbca1577fad1cda1af203702fc4bb3
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 34%

---

# Creare sequenze di criteri

Utilizza le sequenze di criteri (fino a cinque criteri per sequenza) per esercitare un maggiore controllo sugli elementi da visualizzare nelle attività [!UICONTROL Consigli. ] È inoltre possibile limitare il numero di elementi restituiti (talvolta denominati &quot;controllo a livello di slot&quot;).

>[!NOTE]
>
>Le sequenze di criteri non possono essere utilizzate con le attività [!UICONTROL Consigli] create prima del rilascio di [!DNL Target Premium] in ottobre 2016.

Per creare una sequenza di criteri, è necessario innanzitutto creare i criteri da includere nella sequenza. Consulta [Creare criteri](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md) per ulteriori informazioni.

Utilizzando una sequenza di criteri, è possibile fornire ulteriori consigli mirati, anziché utilizzare consigli di backup più generici, quando un criterio non fornisce abbastanza risultati per completare il progetto. In genere, una sequenza di criteri passa dal targeting più specifico, che potrebbe restituire un numero minore di risultati, al targeting più generale, che in genere restituisce più risultati.

Le sequenze di criteri possono variare in ordine a seconda del tipo di pagina, come illustrato negli esempi seguenti:

| Tipo di pagina | Possibile ordine di sequenza |
| --- | --- |
| Pagina prodotto | <ol><li>In base all&#39;articolo corrente, della stessa marca</li><li>In base all&#39;articolo corrente, di tutte le marche</li><li>In base a somiglianza del contenuto</li><li>In base agli articoli più venduti</li><li>In base agli articoli più visualizzati di tutto il sito</li></ol> |
| Home page | <ol><li>In base all’ultimo acquisto del visitatore </li><li>In base all’articolo preferito del visitatore</li><li>In base alla categoria preferita del visitatore</li><li>In base agli articoli più venduti</li><li>In base agli articoli più visualizzati di tutto il sito</li></ol> |

## Creare una sequenza di criteri

È possibile creare sequenze di criteri da [!UICONTROL Crea sequenza criteri] schermo.

Esistono diversi modi per arrivare alla schermata [!UICONTROL Crea sequenza criteri]. Alcune opzioni dipendono dal modo in cui si raggiunge la schermata.

* Su **[!UICONTROL Consigli]** > **[!UICONTROL Criteri]**, fai clic su **[!UICONTROL Crea criterio]** > **[!UICONTROL Crea sequenza criteri]**. I criteri creati vengono automaticamente resi disponibili per tutte le attività di [!UICONTROL Consigli].
* Durante la creazione di un [!UICONTROL Recommendations] attività, nella schermata Seleziona criteri, fai clic su **[!UICONTROL Crea nuovo]** > **[!UICONTROL Crea sequenza criteri]**. Potrai salvare la nuova sequenza di criteri da utilizzare con altre attività di [!UICONTROL Consigli].
* Quando si modifica un [!UICONTROL Recommendations] attività, fai clic su [!UICONTROL Posizione Recommendations] sulla pagina, quindi seleziona **[!UICONTROL Cambia criterio]**. Nella schermata [!UICONTROL Seleziona criteri], fai clic su **[!UICONTROL Crea nuovo]** > **[!UICONTROL Crea sequenza criteri]**. Sarà possibile salvare i nuovi criteri da utilizzare per altre attività di [!UICONTROL Consigli].

I seguenti passaggi presuppongono l’accesso a [!UICONTROL Crea sequenza criteri] utilizzando il primo metodo: **[!UICONTROL Recommendations]** > **[!UICONTROL Criteri]** schermata della libreria.

1. Clic **[!UICONTROL Recommendations]** > **[!UICONTROL Criteri]**.

1. Clic **[!UICONTROL Crea criterio]** > **[!UICONTROL Crea sequenza criteri]**.

   ![Immagine CreateCriteriaSequence](assets/CreateCriteriaSequence.png)

1. Compila le informazioni nel [Informazioni di base](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info) sezione.

1. In **[!UICONTROL Sequenza criteri]** , fare clic su **[!UICONTROL Aggiungi criterio]**.

   L&#39;ordine sequenziale definisce l&#39;ordine di riempimento di una progettazione. Se il criterio 1 non ha abbastanza consigli per riempire la progettazione, gli slot rimanenti verranno riempiti con il criterio 2 e così via.

   ![Aggiungi criterio](/help/main/c-recommendations/c-algorithms/assets/add-criteria.png)

1. Il giorno [!UICONTROL Seleziona criterio] , seleziona un criterio, quindi fai clic su **[!UICONTROL Aggiungi]**.

   Puoi utilizzare la casella di ricerca e i menu a discesa dei filtri per trovare i criteri desiderati.

   ![Selezionare criteri](/help/main/c-recommendations/c-algorithms/assets/select-criteria.png)

1. (Facoltativo) Fai scorrere il **[!UICONTROL Limita il numero di elementi restituiti]** attiva, quindi specifica il numero di elementi (tra 1 e 50).

   ![Limita il numero di elementi restituiti](/help/main/c-recommendations/c-algorithms/assets/limit-number.png)

   Per aiutarti a comprendere il valore della [!UICONTROL Limita il numero di elementi restituiti] (talvolta denominato &quot;controllo a livello di slot&quot;), prendere in considerazione i seguenti casi d&#39;uso:

   * **Caso d’uso 1**: desideri disporre di una combinazione di diversi tipi di elementi in un’unica barra dei consigli. Ad esempio, vuoi mostrare un mix di outerwear (giacche) e top (camicie, T-shirt). A questo scopo, utilizza una raccolta per l’attività che include tutti i potenziali tipi di prodotto desiderati negli slot della progettazione. Quindi, imposta il primo criterio con un filtro statico che limita i criteri in modo da includere solo l’outerwear, e imposta il secondo criterio con un filtro statico che limita i criteri in modo da includere solo i top. Infine, aggiungi entrambi i criteri a una sequenza di criteri e limita il primo criterio a 2 slot.

      L’area dei consigli potrebbe presentarsi così sul sito:

      ![Vassoio consigli prodotti in primo piano](/help/main/c-recommendations/c-algorithms/assets/featured-products.png)

   * **Caso d’uso 2**: desideri una combinazione di articoli alternativi e complementari. Imposta un criterio per utilizzare un algoritmo visualizzato/visualizzato e un filtro dinamico che limiti gli elementi consigliati alla categoria dell’elemento corrente. Imposta il secondo criterio per utilizzare un algoritmo visualizzato/acquistato e un filtro dinamico che includa solo gli articoli consigliati che non corrispondono alla categoria dell’articolo corrente. Infine, aggiungi entrambi i criteri a una sequenza e limita il primo criterio a 2 slot.

1. Continua ad aggiungere altri criteri alla sequenza. È possibile aggiungere fino a cinque criteri a una sequenza.

1. Abilita [Opzioni di contenuto di backup](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content).

1. Fai clic su **[!UICONTROL Salva]**.

   La sequenza di criteri verrà visualizzata nell&#39;elenco criteri.

   Per ulteriori informazioni sulle opzioni di logica per i consigli, consulta [Criteri](/help/main/c-recommendations/c-algorithms/algorithms.md).

## Video di formazione: Creare i criteri in Recommendations (12:33) ![Icona Tutorial](/help/main/assets/tutorial.png)

Questo video contiene le seguenti informazioni:

* Creare criteri
* Creare sequenze di criteri
* Caricare criteri personalizzati

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)
