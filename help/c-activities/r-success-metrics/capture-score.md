---
keywords: capture score;score
description: La metrica di coinvolgimento Capture Score calcola un punteggio aggregato basato sul valore assegnato alle pagine visitate sul sito, dal momento in cui il visitatore vede per la prima volta la prima richiesta Target di visualizzazione della campagna.
title: Punteggio di acquisizione
feature: success metrics
subtopic: Getting Started
topic: Standard
uuid: 977454ad-da32-449a-a8c9-1f3c75220be6
translation-type: tm+mt
source-git-commit: b2f80c89ecceb6f88a176db7a90e71a162a24641
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 51%

---


# Punteggio di acquisizione{#capture-score}

The Capture Score engagement metric calculates an aggregated score based on the value assigned to pages visited on the site, from the point the visitor first sees the campaign&#39;s first display [!DNL Target] request.

Nell&#39;esempio seguente viene illustrato come viene calcolato il coinvolgimento del punteggio in una campagna che verifica due esperienze, una con l&#39;immagine di un gatto e l&#39;altra con l&#39;immagine di un cane.

![](assets/example_score.png)

In questo esempio, il primo visitatore sperimenta l&#39;esperienza del gatto. Assume that a global [!DNL Target] request passes in a page score based on the value of the page. If the marketer has captured page count engagement on a success metric associated with `**any Target request**`, the visit score accumulates for any request seen after the display request around the cat image.

La prima pagina aggiunge 1 al punteggio, la seconda pagina 0,25, la terza 0,10 e la quarta 0,10 per un totale di 1,45. Questo potrebbe essere interpretato come valuta o punti. In una visita diversa, un visitatore sperimenta l&#39;esperienza del cane e anche se il visitatore vede meno pagine, il punteggio è 2,10, quindi maggiore di altre visite, perché il visitatore ha visualizzato pagine con maggiore valore.

Prendi in considerazione i costi di acquisizione e i ricavi del collegamento di affiliazione passando adbox e reindirizzamenti, come descritto nel seguente flusso di pagina. Notice that, in this example, both [!DNL Target] requests on the article page pass a score, possibly representing a known CPM.

![](assets/example_score2.png)

**Assegnazione di un punteggio di pagina**

Puoi assegnare un valore a qualsiasi pagina del tuo sito in base a ciò al valore della pagina. Ad esempio, un sito di cucina potrebbe essere in grado di vendere annunci pubblicitari per più soldi sulle pagine di articoli caratteristiche rispetto alla sezione esperienza. Gli articoli caratteristici sono più importanti della sezione esperienza. Il Punteggio di pagina consente di sviluppare un “valore” complessivo di una visita, in modo che la persona che legge più articoli caratteristici ottenga più “punti” di qualcuno che sfoglia solo le esperienze.

Esistono due metodi per assegnare un punteggio a una pagina:

* Nella [!DNL Target] richiesta, create un parametro denominato `mboxPageValue`.

   Esempio: `('global_mbox', 'mboxPageValue=10');`

   The specified value is added to the score every time the page with that [!DNL Target] request is viewed. Se più richieste sulla pagina includono dei valori di punteggio, la valutazione della pagina corrisponde al totale di tutti i valori di richiesta. `mboxPageValue` è un parametro riservato utilizzato per trasmettere valori in una richiesta Target per acquisire un punteggio di coinvolgimento. Possono essere trasmessi valori positivi e negativi. La somma è calcolata alla fine della visita di ogni visitatore per calcolare il punteggio totale per la visita.

* Passa il parametro `?mboxPageValue=n` nell’URL della pagina.

   Esempio: `https://www.mydomain.com?mboxPageValue=5`

   Using this method, the specified value is added to the score for each [!DNL Target] request on the page. For example, if you pass the parameter `?mboxPageValue=10`and there are three [!DNL Target] requests on the page, the score for the page is 30.

>[!NOTE]
>
>Le richieste di destinazione che si trovano al di sopra della prima richiesta di visualizzazione [!DNL Target] dell&#39;attività non saranno incluse nella valutazione.

Best practice is to assign values in the [!DNL Target] request. Questo consente di essere precisi nei valori misurati, a seconda del contenuto di ogni richiesta.

>[!NOTE]
>
>Per semplificare la manutenzione, è possibile configurare le assegnazioni di valore del Punteggio di pagina del sito nel file [!DNL at.js] o [!DNL mbox.js] con una logica condizionale JavaScript. Questo elimina la necessità di aggiungere altro codice alle tue pagine. Contatta il tuo consulente dell&#39;account per l&#39;assistenza.

È possibile combinare i due metodi, ma questo potrebbe causare un punteggio più alto del previsto. For example, if you assign a value of 10 to each of three [!DNL Target] requests and no score to a fourth request, then pass the URL parameter `?mboxPageValue=5`, your page score will be 50, 30 for the three requests with assigned values, and then 5 for each of the four requests on the page.

Il contatore inizia con la prima richiesta di visualizzazione, non con la richiesta di ingresso. Ad esempio, se immettete l&#39;attività nella home page che non dispone di una richiesta di visualizzazione, e quindi il collegamento alla pagina del catalogo contenente una richiesta di visualizzazione, il contatore inizia quando passate alla pagina del catalogo.

Inoltre puoi passare in valori negativi su alcune pagine che costano o non è opportuno che un visitatore le veda. Anche i valori negativi influiscono sul punteggio complessivo. Questa tecnica può essere utilizzata su una pagina che i visitatori raggiungono da un annuncio, in modo da sapere quanto è stato il CPC. Oppure, per esempio, può essere utilizzata per una pagina di supporto o di contatto, dalla quale sai che i visitatori potrebbero chiamare o richiedere assistenza.
