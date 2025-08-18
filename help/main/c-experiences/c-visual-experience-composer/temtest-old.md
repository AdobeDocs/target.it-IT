---
keywords: test modello;modello;stessa esperienza su pagine simili;test template
description: Scopri come utilizzare il Compositore esperienza visivo di Adobe [!DNL Target] per includere la stessa esperienza in più pagine con struttura simile o contenenti gli stessi elementi modello.
title: Posso includere la stessa esperienza in pagine simili?
feature: Experiences and Offers
exl-id: 4ea95794-496c-4eff-96ec-8a9d1f732c4a
source-git-commit: be9996c4dce0a3135a39fcbf0608b57b6e742ac3
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 33%

---

# Includere la stessa esperienza in pagine simili

Utilizzare un modello di pagina in [!DNL Adobe Target] per fornire una struttura alle pagine o, se le pagine contengono elementi simili, per testare le varianti di elementi di pagina con struttura simile o per l&#39;intero dominio.

Per funzionare correttamente, questa funzione deve essere utilizzata su pagine con una struttura simile o contenenti elementi modello strutturati allo stesso modo su tutte le pagine.

>[!IMPORTANT]
>
>L’utilizzo di questa funzione per modificare gli elementi su pagine dissimili causerà probabilmente risultati imprevisti.

Ad esempio, si può utilizzare per eseguire una delle operazioni seguenti:

* Eseguire un test di una barra di navigazione globale ridisponendo o rimuovendo elementi
* Rimuovere un elemento da tutte le pagine di prodotto che utilizzano un particolare modello di pagina
* Aggiungere un banner a tutte le pagine di prodotto
* Modificare il layout di un modello di elemento

Puoi specificare le pagine che includono gli elementi di modifica o applicare la modifica in tutto il sito o dominio.

1. Crea o modifica un&#39;attività come descritto in [Attività](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03).

1. Per specificare le pagine in cui verrà visualizzata l&#39;esperienza, nel [!UICONTROL Visual Experience Composer] (VEC) fai clic sull&#39;icona a forma di ingranaggio, quindi seleziona **[!UICONTROL Page Delivery]**.

   ![Icona ingranaggio > Consegna pagine](/help/main/c-experiences/c-visual-experience-composer/assets/icon-gear.png)

1. Fai clic su **[!UICONTROL Add Template Rule]**, quindi specifica i criteri per le pagine a cui aggiungere l&#39;esperienza.

1. Specifica l&#39;intervallo di pagine. L&#39;intervallo di pagine può essere uno tra i seguenti:

   * URL (per ulteriori informazioni su come Target valuta gli URL, consulta [Domande frequenti su destinazioni e pubblico](/help/main/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).)
   * Dominio
   * Percorso
   * Frammento hash (#) (esegue il targeting della parte di un URL che segue il simbolo #).
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

   Ad esempio, se selezioni **[!UICONTROL Domain]** e **[!UICONTROL Is (case sensitive)]**, digita il dominio in cui desideri aggiungere l&#39;esperienza in tutte le pagine.

   È possibile includere più elementi.

   >[!IMPORTANT]
   >
   >Per gli elementi multipli viene utilizzato l’operatore OR, il che significa che ogni singolo elemento nell’elenco può soddisfare la condizione.

1. Se lo si desidera, immettere criteri aggiuntivi facendo clic su **[!UICONTROL Add Template Rule]** e ripetendo la procedura descritta nei passaggi precedenti.

   I criteri multipli sono collegati mediante AND (E). [!DNL Target] aggiunge l&#39;esperienza a tutte le pagine che corrispondono ai criteri specificati.

>[!IMPORTANT]
>
> [!DNL Target] non è in grado di controllare le pagine per verificare che siano visualizzate come previsto, pertanto è sempre consigliabile utilizzare questa funzionalità per testare le pagine interessate prima di renderle pubbliche.

## Casi d’uso

Esamina i seguenti casi d’uso per scoprire come utilizzare le regole dei modelli sul sito:

### Esegui il rendering della stessa attività in tutto il dominio

Puoi considerare l’utilizzo delle regole dei modelli per eseguire il rendering della stessa attività in tutto il dominio per i seguenti casi d’uso:

* Per includere un&#39;intestazione o un piè di pagina globale
* Per includere un banner globale (ad esempio, annunci relativi alla COVID-19)
* Per includere una promozione di spedizione gratuita globale

1. Crea o modifica un&#39;attività come descritto in [Attività](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03).

1. Per specificare il dominio in cui verrà visualizzata l&#39;esperienza, nel Compositore esperienza visivo, fai clic sull&#39;icona a forma di ingranaggio, quindi seleziona **[!UICONTROL Page Delivery]**.

1. Fare clic su **[!UICONTROL Add Template Rule]** > **[!UICONTROL Domain]**.

1. Dall&#39;elenco a discesa **[!UICONTROL Choose evaluator]**, selezionare **[!UICONTROL Contains]**, quindi specificare il dominio.

   ![Il dominio contiene](/help/main/c-experiences/c-visual-experience-composer/assets/domain-template-rule.png)

## Video di formazione: Compositore esperienza visivo (2 di 2) (7:29) ![Icona esercitazione](/help/main/assets/tutorial.png)

* Rinominare e duplicare un’esperienza
* Creare un’esperienza con reindirizzamento
* Indirizzare un’attività a un singolo URL o a un gruppo di URL
* Creare un’attività multipagina
* Creare un’esperienza e visualizzarne l’anteprima per i siti web reattivi
* Evidenziare tipi di elementi con le sovrapposizioni

>[!VIDEO](https://video.tv.adobe.com/v/36327?captions=ita)
