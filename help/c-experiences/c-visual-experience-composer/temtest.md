---
description: Se si utilizza un modello di pagina per fornire una struttura alle pagine, o se le pagine contengono elementi simili, questa funzione consente di sottoporre a test le varianti di elementi di pagina con struttura simile.
keywords: test modello;modello;stessa esperienza su pagine simili;test template
seo-description: Se si utilizza un modello di pagina per fornire una struttura alle pagine, o se le pagine contengono elementi simili, questa funzione consente di sottoporre a test le varianti di elementi di pagina con struttura simile.
seo-title: Includere la stessa esperienza in pagine simili
solution: Target
title: Includere la stessa esperienza in pagine simili
topic: Premium
uuid: 055b276e-2492-40d8-b48e-849dffa93f35
translation-type: tm+mt
source-git-commit: df79860eacc680351c6b3bdf0570b76543492570

---


# Includere la stessa esperienza su pagine simili{#include-the-same-experience-on-similar-pages}

Se si utilizza un modello di pagina per fornire una struttura alle pagine, o se le pagine contengono elementi simili, questa funzione consente di sottoporre a test le varianti di elementi di pagina con struttura simile.

Per funzionare correttamente, questa funzione deve essere utilizzata su pagine che hanno una struttura molto simile. o contengono elementi di modello strutturati allo stesso modo su tutte le pagine.

>[!IMPORTANT]
>
>L’utilizzo di questa funzione per modificare gli elementi su pagine dissimili causerà probabilmente risultati imprevisti.

Ad esempio, si può utilizzare per eseguire una delle operazioni seguenti:

* Eseguire un test di una barra di navigazione globale ridisponendo o rimuovendo elementi
* Rimuovere un elemento da tutte le pagine di prodotto che utilizzano un particolare modello di pagina
* Aggiungere un banner a tutte le pagine di prodotto
* Modificare il layout di un modello di elemento

Il video demo seguente include informazioni sull&#39;utilizzo di un modello:

Si possono specificare le pagine che contengono gli elementi di modifica, o applicare la modifica in tutto il sito.

1. Crea un’attività come descritto in [Attività](../../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03).
1. Per specificare le pagine in cui verrà visualizzata l&#39;esperienza, in Visual Experience Composer (Compositore esperienza visivo) fate clic sull&#39;icona a forma di ingranaggio, quindi selezionate **[!UICONTROL Page Delivery]**(Consegna pagina).
1. Fate clic su **[!UICONTROL Aggiungi regola modello]**, quindi specificate i criteri per le pagine a cui desiderate aggiungere l&#39;esperienza.

1. Specifica l&#39;intervallo di pagine. L&#39;intervallo di pagine può essere uno tra i seguenti:

   * URL
   * Dominio
   * Percorso
   * Hash (#) frammento (destinazione della parte di un URL che segue il simbolo #).
   * Query
   * Parametro

1. Scegli un operatore.

   L&#39;operatore specifica la correlazione tra gli elementi dopo l&#39;operatore e l&#39;intervallo di pagine. Gli operatori disponibili sono i seguenti:

   * Contiene
   * Non contiene
   * Is (con distinzione tra maiuscole e minuscole)
   * Non è
   * Inizia con
   * Termina con

1. Digita le stringhe che definiscono dove viene aggiunta l&#39;esperienza, ad esempio il dominio o le stringhe contenute nel nome della pagina.

   Ad esempio, se selezionate **[!UICONTROL Dominio]** e **[!UICONTROL Is (distinzione tra maiuscole e minuscole)]**, digitate il dominio in cui desiderate aggiungere l&#39;esperienza a tutte le pagine.

   È possibile includere più elementi.

   >[!IMPORTANT]
   >
   >Per gli elementi multipli viene utilizzato l’operatore `OR` (O), il che significa che ogni singolo elemento nell’elenco può soddisfare la condizione.

1. Se desiderato, inserite criteri aggiuntivi facendo clic **[!UICONTROL su Aggiungi regola]** modello e ripetendo la procedura nel passaggio precedente.

   I criteri multipli sono collegati mediante AND (E). Adobe Target aggiunge l&#39;esperienza a tutte le pagine che corrispondono ai criteri specificati.

>[!IMPORTANT]
>
> Target non è in grado di controllare le pagine per assicurare che siano visualizzate come previsto, quindi è sempre opportuno, quando si utilizza questa funzione, verificare le pagine interessate prima di pubblicarle.

## Video di formazione: Compositore esperienza visivo (2 di 2) (7:29)

* Rinominare e duplicare un’esperienza
* Creare un’esperienza con reindirizzamento
* Indirizzare un’attività a un singolo URL o a un gruppo di URL
* Creare un’attività multipagina
* Creare un’esperienza e visualizzarne l’anteprima per i siti web reattivi
* Evidenziare tipi di elementi con le sovrapposizioni

>[!VIDEO](https://video.tv.adobe.com/v/17401)