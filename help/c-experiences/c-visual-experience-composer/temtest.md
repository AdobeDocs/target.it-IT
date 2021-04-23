---
keywords: test modello;modello;stessa esperienza su pagine simili;test template
description: Scopri come utilizzare l’Adobe  [!DNL Target] Compositore esperienza visivo (VEC) per includere la stessa esperienza in più pagine con struttura simile o contenenti gli stessi elementi modello.
title: Posso includere la stessa esperienza in pagine simili?
feature: Esperienze e offerte
exl-id: 4ea95794-496c-4eff-96ec-8a9d1f732c4a
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 46%

---

# Includere la stessa esperienza in pagine simili

Utilizza un modello di pagina in [!DNL Adobe Target] per fornire una struttura alle pagine o, se le pagine contengono elementi simili, per testare le varianti di elementi di pagina strutturati in modo simile o nell’intero dominio.

Per funzionare correttamente, questa funzione deve essere utilizzata su pagine con una struttura simile o contenenti elementi modello strutturati allo stesso modo su tutte le pagine.

>[!IMPORTANT]
>
>L’utilizzo di questa funzione per modificare gli elementi su pagine dissimili causerà probabilmente risultati imprevisti.

Ad esempio, si può utilizzare per eseguire una delle operazioni seguenti:

* Eseguire un test di una barra di navigazione globale ridisponendo o rimuovendo elementi
* Rimuovere un elemento da tutte le pagine di prodotto che utilizzano un particolare modello di pagina
* Aggiungere un banner a tutte le pagine di prodotto
* Modificare il layout di un modello di elemento

È possibile specificare le pagine che includono gli elementi di modifica o applicare la modifica al sito o al dominio.

1. Crea o modifica un&#39;attività come descritto in [Attività](/help/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03).

1. Per specificare le pagine in cui verrà visualizzata l&#39;esperienza, nel [!UICONTROL Compositore esperienza visivo] (VEC) fai clic sull&#39;icona a forma di ingranaggio, quindi seleziona **[!UICONTROL Consegna pagine]**.

   ![Icona a forma di ingranaggio > Consegna pagine](/help/c-experiences/c-visual-experience-composer/assets/icon-gear.png)

1. Fai clic su **[!UICONTROL Aggiungi regola modello]**, quindi specifica i criteri per le pagine a cui aggiungere l’esperienza.

1. Specifica l&#39;intervallo di pagine. L&#39;intervallo di pagine può essere uno tra i seguenti:

   * URL (Per ulteriori informazioni su come Target valuta gli URL, consulta [Domande frequenti su destinazioni e pubblico](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).)
   * Dominio
   * Percorso
   * Frammento hash (#) (esegui il targeting della parte di un URL che segue il simbolo #.)
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
   >Per gli elementi multipli viene utilizzato l’operatore logico OR, il che significa che ogni singolo elemento dell’elenco può soddisfare la condizione.

1. Se lo desideri, inserisci criteri aggiuntivi facendo clic su **[!UICONTROL Aggiungi regola modello]** e ripetendo la procedura descritta nei passaggi precedenti.

   I criteri multipli sono collegati mediante AND (E). [!DNL Target] aggiunge l&#39;esperienza a tutte le pagine che corrispondono ai criteri specificati.

>[!IMPORTANT]
>
> [!DNL Target] non è in grado di controllare le pagine per assicurare che siano visualizzate come previsto, quindi è sempre opportuno, quando si utilizza questa funzione, verificare le pagine interessate prima di pubblicarle.

## Casi di utilizzo

Consulta i seguenti casi d’uso per scoprire come utilizzare le regole dei modelli sul tuo sito:

### Esegui il rendering della stessa attività in tutto il dominio

Puoi considerare l’utilizzo di regole modello per eseguire il rendering della stessa attività in tutto il dominio per i seguenti casi d’uso:

* Per includere un’intestazione o un piè di pagina globale
* Per includere un banner globale (ad esempio, annunci COVID-19)
* Per includere una promozione globale sulla spedizione gratuita

1. Crea o modifica un&#39;attività come descritto in [Attività](/help/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03).

1. Per specificare il dominio in cui verrà visualizzata l&#39;esperienza, nel Compositore esperienza visivo fai clic sull&#39;icona a forma di ingranaggio, quindi seleziona **[!UICONTROL Consegna pagine]**.

1. Fai clic su **[!UICONTROL Aggiungi regola modello]** > **[!UICONTROL Dominio]**.

1. Dal menu a discesa **[!UICONTROL Scegli valutatore]**, seleziona **[!UICONTROL Contiene]**, quindi specifica il dominio.

   ![Il dominio contiene](/help/c-experiences/c-visual-experience-composer/assets/domain-template-rule.png)

## Video di formazione: Compositore esperienza visivo (2 di 2) (7:29) ![Badge tutorial](/help/assets/tutorial.png)

* Rinominare e duplicare un’esperienza
* Creare un’esperienza con reindirizzamento
* Indirizzare un’attività a un singolo URL o a un gruppo di URL
* Creare un’attività multipagina
* Creare un’esperienza e visualizzarne l’anteprima per i siti web reattivi
* Evidenziare tipi di elementi con le sovrapposizioni

>[!VIDEO](https://video.tv.adobe.com/v/17401)
