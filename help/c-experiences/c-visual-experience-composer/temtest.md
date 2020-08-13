---
keywords: template testing;template;same experience on similar pages;template test
description: Se si utilizza un modello di pagina per fornire una struttura alle pagine, o se le pagine contengono elementi simili, questa funzione consente di sottoporre a test le varianti di elementi di pagina con struttura simile.
title: Includere la stessa esperienza in pagine simili
feature: experiences
uuid: 055b276e-2492-40d8-b48e-849dffa93f35
translation-type: tm+mt
source-git-commit: 3cf1f4fa56f86c106dccdc2c97c080c17c3982b4
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 96%

---


# Includere la stessa esperienza in pagine simili{#include-the-same-experience-on-similar-pages}

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
1. Per specificare le pagine in cui verrà visualizzata l’esperienza, nel Compositore esperienza visivo, fai clic sull’icona a forma di ingranaggio, quindi seleziona **[!UICONTROL Consegna pagina]**.
1. Fai clic su **[!UICONTROL Aggiungi regola modello]**, quindi specifica i criteri per le pagine a cui aggiungere l’esperienza.

1. Specifica l&#39;intervallo di pagine. L&#39;intervallo di pagine può essere uno tra i seguenti:

   * URL Per ulteriori informazioni sul modo in cui Target valuta gli URL, consulta [Domande frequenti](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md)su Target e audience.
   * Dominio
   * Percorso
   * Hash (#) frammento (destinazione della parte di un URL che segue il simbolo #).
   * Query
   * Parametro

1. Scegli un operatore.

   L&#39;operatore specifica la correlazione tra gli elementi dopo l&#39;operatore e l&#39;intervallo di pagine. Gli operatori disponibili sono i seguenti:

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
   >Per gli elementi multipli viene utilizzato l’operatore `OR` (O), il che significa che ogni singolo elemento nell’elenco può soddisfare la condizione.

1. Se lo desideri, inserisci criteri aggiuntivi facendo clic su **[!UICONTROL Aggiungi regola modello]** e ripetendo la procedura di cui al passaggio precedente.

   I criteri multipli sono collegati mediante AND (E). Adobe Target aggiunge l&#39;esperienza a tutte le pagine che corrispondono ai criteri specificati.

>[!IMPORTANT]
>
> Target non è in grado di controllare le pagine per assicurare che siano visualizzate come previsto, quindi è sempre opportuno, quando si utilizza questa funzione, verificare le pagine interessate prima di pubblicarle.

## Video di formazione: Compositore esperienza visivo (2 di 2) (7:29) ![Badge di esercitazione](/help/assets/tutorial.png)

* Rinominare e duplicare un’esperienza
* Creare un’esperienza con reindirizzamento
* Indirizzare un’attività a un singolo URL o a un gruppo di URL
* Creare un’attività multipagina
* Creare un’esperienza e visualizzarne l’anteprima per i siti web reattivi
* Evidenziare tipi di elementi con le sovrapposizioni

>[!VIDEO](https://video.tv.adobe.com/v/17401)