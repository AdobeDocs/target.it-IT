---
keywords: punteggio di acquisizione;punteggio
description: Scopri la metrica di coinvolgimento Punteggio di acquisizione in Adobe [!DNL Target] che calcola un punteggio aggregato in base al valore assegnato alle pagine visitate sul sito.
title: Cos’è la metrica Punteggio di acquisizione?
feature: Success Metrics
exl-id: 3446cdef-7ee0-40dd-bf17-27def56668d4
TQID: 'https://experienceleague.adobe.com/iqCPEY9x7Lg9TlAhxn8e-B1XOnUfNgUWFdOf8Bw2F3w'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: dfc8a233-f2b5-4811-bf63-b4262aebc5a5
    internal-label: Administration and configuration
subfeature_v2:
  - id: eb2bfbe8-b0f3-4cc3-ae8d-af79179585eb
    internal-label: Success metrics
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 8c6f23b495228ab930e6649aa2f9e6dae506cae2
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 13%
---
# Acquisire il punteggio {#capture-score}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come la metrica di coinvolgimento Punteggio di acquisizione calcola il punteggio di una visita e come assegnare un punteggio a una pagina.

>[!ENDSHADEBOX]

La metrica di coinvolgimento Punteggio di acquisizione in [!DNL Adobe Target] calcola un punteggio aggregato in base al valore assegnato alle pagine visualizzate da un visitatore sul sito. Il punteggio inizia nel punto in cui il visitatore vede per la prima volta la prima richiesta di visualizzazione [!DNL Target] dell&#39;attività.

L’esempio seguente mostra come viene calcolato il punteggio in un’attività che testa due esperienze, una con un’immagine di gatto e una con un’immagine di cane.

![Flusso di pagina della visita esperienza del gatto, con un punteggio per ogni pagina](assets/example_score.png)

In questo esempio, il primo visitatore vede l’esperienza del gatto. Si supponga che una richiesta [!DNL Target] globale passi in un punteggio di pagina basato sul valore della pagina. Se l&#39;addetto al marketing ha raccolto il coinvolgimento del conteggio delle pagine su una metrica di successo associata a **qualsiasi richiesta Target**, il punteggio di visita si accumula per qualsiasi richiesta visualizzata dopo la richiesta di visualizzazione attorno all&#39;immagine del gatto.

La prima pagina aggiunge 1 al punteggio, la seconda pagina 0,25, la terza 0,10 e la quarta 0,10, per un totale di 1,45. Questo totale può essere interpretato come valuta o punti. In una visita separata, un visitatore vede l’esperienza del cane. Anche se questo visitatore visualizza meno pagine, il punteggio è 2,10, che è maggiore rispetto all’altra visita, perché ha visualizzato pagine di maggior valore.

Prendi in considerazione i costi di acquisizione e i ricavi del collegamento di affiliazione passando adbox e reindirizzamenti, come descritto nel seguente flusso di pagina. In questo esempio, entrambe le richieste [!DNL Target] nella pagina dell&#39;articolo superano un punteggio, probabilmente rappresentando un CPM noto.

![Flusso di pagine con costi di acquisizione e ricavi da collegamenti affiliati passati come punteggi](assets/example_score2.png)

## Assegnazione di un punteggio di pagina

Puoi assegnare un valore a qualsiasi pagina del tuo sito in base a ciò al valore della pagina. Ad esempio, un sito di cucina potrebbe essere in grado di vendere annunci pubblicitari per più soldi sulle sue pagine di articoli di funzioni rispetto alla sezione esperienza. Gli articoli sulle funzioni sono quindi più importanti della sezione esperienza. Un punteggio di pagina consente di sviluppare un &quot;valore&quot; complessivo di una visita, in modo che una persona che legge più articoli di funzionalità ottenga più &quot;punti&quot; rispetto a una persona che naviga solo nelle esperienze.

Esistono due metodi per assegnare un punteggio a una pagina:

* Nella richiesta [!DNL Target], creare un parametro denominato `mboxPageValue`.

  Esempio: `('global_mbox', 'mboxPageValue=10');`

  Il valore specificato viene aggiunto al punteggio ogni volta che viene visualizzata la pagina con quella richiesta [!DNL Target]. Se più richieste nella pagina includono valori di punteggio, il punteggio per la pagina è il totale di tutti i valori di richiesta. `mboxPageValue` è un parametro riservato utilizzato per la trasmissione dei valori in una richiesta [!DNL Target] per acquisire un punteggio di coinvolgimento. Possono essere trasmessi valori positivi e negativi. La somma viene calcolata alla fine di ogni visita per determinare il punteggio totale della visita.

* Passa il parametro `?mboxPageValue=n` nell&#39;URL della pagina.

  Esempio: `https://www.mydomain.com?mboxPageValue=5`

  Il valore specificato viene aggiunto al punteggio per ogni richiesta [!DNL Target] nella pagina. Ad esempio, se passi il parametro `?mboxPageValue=10` e ci sono tre [!DNL Target] richieste nella pagina, il punteggio per la pagina è di 30.

>[!NOTE]
>
>Il contatore inizia con la prima richiesta di visualizzazione dell&#39;attività, non con la richiesta di immissione, e [!DNL Target] richieste che si trovano sopra la richiesta non sono incluse nel punteggio. Ad esempio, se si immette l&#39;attività nella home page, che non dispone di una richiesta di visualizzazione, e quindi si collega a una pagina di catalogo che contiene una richiesta di visualizzazione, il contatore inizia quando si passa alla pagina di catalogo.

La best practice prevede l&#39;assegnazione di valori nella richiesta [!DNL Target]. Questo metodo ti consente di essere preciso riguardo ai valori misurati, a seconda del contenuto di ogni richiesta.

>[!NOTE]
>
>Per semplificare la manutenzione, è possibile configurare le assegnazioni di valore del punteggio di pagina del sito nel file [!DNL at.js] con una logica condizionale di JavaScript. Questo approccio elimina la necessità di aggiungere altro codice alle pagine. Contatta il tuo consulente dell&#39;account per l&#39;assistenza.

È possibile combinare i due metodi, ma questo potrebbe causare un punteggio più alto del previsto. Ad esempio, si assegna un valore di 10 a ciascuna delle tre richieste [!DNL Target] e nessun punteggio a una quarta richiesta, quindi si passa il parametro URL `?mboxPageValue=5`. Il punteggio di pagina è 50: 30 per le tre richieste con valori assegnati, più 20 per il parametro URL (5 per ciascuna delle quattro richieste sulla pagina).

Inoltre puoi passare in valori negativi su alcune pagine che costano o non è opportuno che un visitatore le veda. Anche i valori negativi influiscono sul punteggio complessivo. Questa tecnica può essere utilizzata in una pagina che i visitatori raggiungono da un annuncio pubblicitario, in modo da sapere quanto è stato il CPC. Può essere utilizzato anche su una pagina di supporto o di contatto, in cui i visitatori possono chiamare o richiedere assistenza.
