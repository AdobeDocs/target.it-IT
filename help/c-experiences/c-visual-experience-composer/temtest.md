---
keywords: template testing;template;same experience on similar pages;template test
description: Utilizzate un modello di pagina in  Adobe Target per fornire struttura alle pagine, o se le pagine contengono elementi simili, per testare le varianti di elementi di pagina con struttura simile.
title: Includere la stessa esperienza in pagine simili utilizzando  Adobe Target
feature: experiences
uuid: 055b276e-2492-40d8-b48e-849dffa93f35
translation-type: tm+mt
source-git-commit: bd13fee3a0a2ef675d121a9832583c3aa125865d
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 45%

---


# Includere la stessa esperienza in pagine simili

Utilizzate un modello di pagina in [!DNL Adobe Target] per fornire struttura alle pagine, o se le pagine contengono elementi simili, per testare le varianti di elementi di pagina con struttura simile o nell&#39;intero dominio.

Per funzionare correttamente, questa funzione deve essere utilizzata su pagine con una struttura simile o contenenti elementi di modello strutturati allo stesso modo su tutte le pagine.

>[!IMPORTANT]
>
>L’utilizzo di questa funzione per modificare gli elementi su pagine dissimili causerà probabilmente risultati imprevisti.

Ad esempio, si può utilizzare per eseguire una delle operazioni seguenti:

* Eseguire un test di una barra di navigazione globale ridisponendo o rimuovendo elementi
* Rimuovere un elemento da tutte le pagine di prodotto che utilizzano un particolare modello di pagina
* Aggiungere un banner a tutte le pagine di prodotto
* Modificare il layout di un modello di elemento

Potete specificare le pagine che contengono gli elementi di modifica o applicare la modifica al sito o al dominio.

1. Create  or edit an activity as described in [Activities](../../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03).

1. To specify the pages where the experience will appear, in the [!UICONTROL Visual Experience Composer] (VEC) click the gear icon, then select **[!UICONTROL Page Delivery]**.

   ![Icona ingranaggio > Consegna pagina](/help/c-experiences/c-visual-experience-composer/assets/icon-gear.png)

1. Fai clic su **[!UICONTROL Aggiungi regola modello]**, quindi specifica i criteri per le pagine a cui aggiungere l’esperienza.

1. Specifica l&#39;intervallo di pagine. L&#39;intervallo di pagine può essere uno tra i seguenti:

   * URL Per ulteriori informazioni sul modo in cui Target valuta gli URL, consulta [Domande frequenti](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md)su Target e audience.
   * Dominio
   * Percorso
   * Frammento hash (#) (eseguite il targeting della parte di un URL che segue il simbolo #.)
   * Query
   * Parametro

1. Scegli un operatore.

   L&#39;operatore specifica la correlazione tra gli elementi dopo l&#39;operatore e l&#39;intervallo di pagine. Gli operatori disponibili includono:

   * Contiene
   * Non contiene
   * è (distinzione maiuscole/minuscole)
   * Non è
   * Inizia con
   * Termina con

1. Digita le stringhe che definiscono dove viene aggiunta l&#39;esperienza, ad esempio il dominio o le stringhe contenute nel nome della pagina.

   Ad esempio, se selezioni **[!UICONTROL Dominio]** e **[!UICONTROL è (distinzione maiuscole/minuscole)]**, digita il dominio in cui desideri aggiungere l’esperienza in tutte le pagine.

   È possibile includere più elementi.

   >[!IMPORTANT]
   >
   >Più elementi utilizzano la logica OR, il che significa che qualsiasi elemento nell&#39;elenco rende vera la condizione.

1. If desired, enter additional criteria by clicking **[!UICONTROL Add Template Rule]** and repeating the procedure in the previous steps.

   I criteri multipli sono collegati mediante AND (E). [!DNL Target] aggiunge l&#39;esperienza a tutte le pagine che corrispondono ai criteri specificati.

>[!IMPORTANT]
>
> [!DNL Target] non è in grado di controllare le pagine per assicurare che siano visualizzate come previsto, quindi è sempre opportuno, quando si utilizza questa funzione, verificare le pagine interessate prima di pubblicarle.

## Casi di utilizzo

Consultate i seguenti casi di utilizzo per trovare i modi per utilizzare le regole dei modelli sul sito:

### Eseguire il rendering della stessa attività nell&#39;intero dominio

Potete prendere in considerazione l&#39;uso delle regole del modello per eseguire il rendering della stessa attività in tutto il dominio per i seguenti casi di utilizzo:

* Per includere un&#39;intestazione o un piè di pagina globale
* Per includere un banner globale (ad esempio, annunci COVID-19)
* Per includere una promozione globale sulla spedizione gratuita

1. Create or edit an activity as described in [Activities](../../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03).

1. To specify the domain where the experience will appear, in the Visual Experience Composer click the gear icon, then select **[!UICONTROL Page Delivery]**.

1. Fate clic su **[!UICONTROL Aggiungi regola]** modello > **[!UICONTROL Dominio]**.

1. Dal menu a discesa **[!UICONTROL Scegli valutatore]** , selezionate **[!UICONTROL Contiene]**, quindi specificate il dominio.

   ![Il dominio contiene](/help/c-experiences/c-visual-experience-composer/assets/domain-template-rule.png)

## Training video: Visual Experience Composer (2 of 2) (7:29) ![Tutorial badge](/help/assets/tutorial.png)

* Rinominare e duplicare un’esperienza
* Creare un’esperienza con reindirizzamento
* Indirizzare un’attività a un singolo URL o a un gruppo di URL
* Creare un’attività multipagina
* Creare un’esperienza e visualizzarne l’anteprima per i siti web reattivi
* Evidenziare tipi di elementi con le sovrapposizioni

>[!VIDEO](https://video.tv.adobe.com/v/17401)