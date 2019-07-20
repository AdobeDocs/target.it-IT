---
description: La metrica di coinvolgimento “Punteggio di acquisizione” calcola un punteggio aggregato in base al valore assegnato alle pagine visitate sul sito, dal momento in cui il visitatore vede per la prima volta la prima mbox di visualizzazione della campagna.
keywords: punteggio di acquisizione;punteggio
seo-description: La metrica di coinvolgimento “Punteggio di acquisizione” calcola un punteggio aggregato in base al valore assegnato alle pagine visitate sul sito, dal momento in cui il visitatore vede per la prima volta la prima mbox di visualizzazione della campagna.
seo-title: Punteggio di acquisizione
solution: Target
subtopic: Introduzione
title: Punteggio di acquisizione
topic: Standard
uuid: 977454ad-da32-449a-a8c9-1f3c75220be6
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Punteggio di acquisizione{#capture-score}

La metrica di coinvolgimento “Punteggio di acquisizione” calcola un punteggio aggregato in base al valore assegnato alle pagine visitate sul sito, dal momento in cui il visitatore vede per la prima volta la prima mbox di visualizzazione della campagna.

Nell'esempio seguente viene illustrato come viene calcolato il coinvolgimento del punteggio in una campagna che verifica due esperienze, una con l'immagine di un gatto e l'altra con l'immagine di un cane.

![](assets/example_score.png)

In questo esempio, il primo visitatore sperimenta l'esperienza del gatto. Supponiamo che una mbox globale passi in un punteggio di pagina in base al valore della pagina. Se l’esperto di marketing ha raccolto il coinvolgimento del conteggio delle pagine su una metrica di successo associata a `**any mbox**`, il punteggio di visita si accumula per qualsiasi mbox di richiesta visto dopo la mbox di visualizzazione intorno all’immagine del gatto.

La prima pagina aggiunge 1 al punteggio, la seconda pagina 0,25, la terza 0,10 e la quarta 0,10 per un totale di 1,45. Questo potrebbe essere interpretato come valuta o punti. In una visita diversa, un visitatore sperimenta l'esperienza del cane e anche se il visitatore vede meno pagine, il punteggio è 2,10, quindi maggiore di altre visite, perché il visitatore ha visualizzato pagine con maggiore valore.

Prendi in considerazione i costi di acquisizione e i ricavi del collegamento di affiliazione passando adbox e reindirizzamenti, come descritto nel seguente flusso di pagina. Nota che, in questo esempio, entrambe le mbox nella pagina dell'articolo passano un punteggio, possibilmente rappresentando un CPM noto.

![](assets/example_score2.png)

**Assegnazione di un punteggio di pagina**

Puoi assegnare un valore a qualsiasi pagina del tuo sito in base a ciò al valore della pagina. Ad esempio, un sito di cucina potrebbe essere in grado di vendere annunci pubblicitari per più soldi sulle pagine di articoli caratteristiche rispetto alla sezione esperienza. Gli articoli caratteristici sono più importanti della sezione esperienza. Il Punteggio di pagina consente di sviluppare un “valore” complessivo di una visita, in modo che la persona che legge più articoli caratteristici ottenga più “punti” di qualcuno che sfoglia solo le esperienze.

Esistono due metodi per assegnare un punteggio a una pagina:

* Nel codice mbox, crea un parametro mbox chiamato `mboxPageValue`.

   Esempio: `('global_mbox', 'mboxPageValue=10');`

   Il valore specificato viene aggiunto al punteggio ogni volta che viene visualizzata la pagina con tale mbox. Se più mbox nella pagina includono valori di punteggio, il punteggio per la pagina è il totale di tutti i valori mbox. `mboxPageValue` è un parametro riservato usato per la trasmissione dei valori in una mbox per acquisire un punteggio di coinvolgimento. Possono essere trasmessi valori positivi e negativi. La somma è calcolata alla fine della visita di ogni visitatore per calcolare il punteggio totale per la visita.

* Passa il parametro `?mboxPageValue=n` nell’URL della pagina.

   Esempio: `https://www.mydomain.com?mboxPageValue=5`

   Utilizzando questo metodo, il valore specificato viene aggiunto al punteggio per ogni mbox nella pagina. Ad esempio, se passi il parametro `?mboxPageValue=10` e ci sono tre mbox sulla pagina, il punteggio per la pagina è di 30.

>[!NOTE] {class=“- topic/note ”}
>
>Le mbox situate sopra la prima mbox visualizzata della campagna non saranno incluse nel punteggio.

La procedura consigliata consiste nell'assegnare valori nel codice mbox. Questo permette di essere precisi nei valori che misuri, a seconda del contenuto di ogni mbox.

>[!NOTE] {class=“- topic/note ”}
>
>Per semplificare la manutenzione, è possibile configurare le assegnazioni di valore del Punteggio di pagina del sito nel file [!DNL at.js] o [!DNL mbox.js] con una logica condizionale JavaScript. Questo elimina la necessità di aggiungere altro codice alle tue pagine. Contatta il tuo consulente dell'account per l'assistenza.

È possibile combinare i due metodi, ma questo potrebbe causare un punteggio più alto del previsto. Ad esempio, se assegni un valore di 10 a ciascuna delle tre mbox e nessun punteggio a una quarta mbox, passando infine il parametro URL `?mboxPageValue=5`, il tuo punteggio di pagina sarà 50, di cui 30 per le tre mbox con i valori assegnati e 5 per ciascuna delle quattro mbox sulla pagina.

Il contatore inizia con la prima mbox visualizzata, non la mbox di ingresso. Ad esempio, se immetti la campagna sulla pagina principale che non ha una mbox visualizzata, poi colleghi alla pagina del catalogo contenente una mbox visualizzata, il contatore inizia quando si passa alla pagina del catalogo.

Inoltre puoi passare in valori negativi su alcune pagine che costano o non è opportuno che un visitatore le veda. Anche i valori negativi influiscono sul punteggio complessivo. Questa tecnica può essere utilizzata su una pagina che i visitatori raggiungono da un annuncio, in modo da sapere quanto è stato il CPC. Oppure, per esempio, può essere utilizzata per una pagina di supporto o di contatto, dalla quale sai che i visitatori potrebbero chiamare o richiedere assistenza.
