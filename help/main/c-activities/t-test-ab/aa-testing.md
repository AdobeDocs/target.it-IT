---
keywords: a/b;a/a;aa;
description: Scopri cos’è un test A/A, perché potresti voler eseguire un test A/A, per quanto tempo dovresti eseguire il test e come interpretare i risultati.
title: Cos’è il test A/A?
feature: A/B Tests
exl-id: 7489f4f5-3655-45f9-a743-651ba1c23c53
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 1%

---

# Test A/A

Prima di eseguire un test A/A sul sito utilizzando [!DNL Adobe Target], è importante comprendere cos’è un test A/A, il motivo per cui potrebbe essere utile eseguire un test A/A, la durata di esecuzione del test e come interpretare i risultati.

## Cos’è il test A/A?

Prima di spiegare il test A/A, è opportuno rivedere il test A/B in modo da poter discutere le differenze.

In un test A/B standard, il traffico viene allocato a due o più esperienze diverse. Un’esperienza è in genere il &quot;controllo&quot; e le varianti dell’esperienza vengono testate rispetto al controllo per vedere quale esperienza crea il maggior incremento in una data metrica.

Il test A/A, tuttavia, comporta l’allocazione del traffico a due esperienze identiche, di solito con una suddivisione del traffico 50/50. Con un test A/B standard, in genere desideri scoprire un incremento nella conversione. Questo è diverso da un test A/A in cui l&#39;obiettivo è solitamente quello di determinare che c&#39;è *no* differenza di incremento tra le esperienze identiche.

## Perché vorresti testare due esperienze identiche e quali risultati si ottengono?

Alcune organizzazioni eseguono test A/A quando implementano un nuovo strumento di test, ad esempio [!DNL Target], per determinare se:

* L’attività è stata impostata correttamente
* Il codice è stato implementato correttamente
* Il reporting è accurato

Anche se poche organizzazioni eseguono test A/A, in realtà è buona prassi eseguirli come esperimenti di &quot;sanità&quot; per creare fiducia dopo l’implementazione dello strumento o prima di eseguire test A/B che potrebbero influire sulla conversione e sui ricavi.

## Perché potresti visualizzare l’incremento per un’esperienza quando le esperienze sono identiche?

Ci sono diversi motivi per cui potresti vedere l’incremento in un’esperienza rispetto all’altra esperienza (identica):

### Il test A/A è stato monitorato continuamente

Un problema comune nell’esecuzione di qualsiasi tipo di test, incluso un test A/A, consiste nell’esaminare i risultati in modo continuo, interrompere anticipatamente un test non appena viene rilevata una rilevanza statistica e dichiarare un’esperienza vincente. Gli analisti fanno spesso ciò che viene chiamato &quot;sbirciamento dei dati&quot;. Il peking dei dati comporta l’esame dei dati del test in anticipo e con frequenza, cercando di determinare quale esperienza funziona meglio. Il rischio è quello di interrompere prematuramente il test, il che potrebbe invalidare i risultati.

In un test A/A, il data peking può spesso causare la visualizzazione dell’incremento da parte degli analisti in un’esperienza, quando in realtà non dovrebbe esserci alcuna differenza, perché le due esperienze sono identiche. Infatti, con il peking continuo, i test A/A sono in realtà _garantito_ mostrare &quot;significatività statistica&quot; (vale a dire, un’affidabilità al di sopra di una certa soglia, come il 95%) ad un certo punto durante il test.

Per evitare questo problema, e come con un normale test A/B, è necessario quindi decidere in anticipo quale dimensione campione utilizzare, in base alla dimensione minima dell’effetto (l’incremento minimo al di sotto del quale un effetto non è importante per la tua azienda), alla potenza e ai livelli di significatività che ritieni accettabili.

In un test A/A, l’obiettivo sarebbe quindi quello di *non* vedi un risultato statisticamente significativo dopo che il test ha raggiunto la dimensione di campione desiderata.

Il [!UICONTROL Calcolatore dimensioni campione Adobe Target] è uno strumento importante per determinare la dimensione del campione da prendere in considerazione e per quanto tempo si deve eseguire il test.

* [Calcolatore dimensioni Adobe Target](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6)

Inoltre, consulta i seguenti articoli per informazioni sulla durata di un’attività, nonché altri suggerimenti e trucchi utili:

* [Per quanto tempo si deve eseguire un test A/B?](/help/main/c-activities/t-test-ab/sample-size-determination.md)
* [Dieci insidie A/B comuni e come evitarle](/help/main/c-activities/t-test-ab/common-ab-testing-pitfalls.md)

### La rilevanza statistica influisce sui risultati dei test

Il livello di significatività di un test determina la probabilità che il test riporti una differenza significativa nei tassi di conversione tra due offerte diverse, quando in realtà non c’è alcuna differenza reale. Questo è noto come falso positivo o errore di tipo I. Il livello di significatività è una soglia specificata dall’utente ed esiste un compromesso tra la tolleranza per i falsi positivi e il numero di visitatori che devono essere inclusi nel test per scegliere il livello di significatività corretto.

Un livello di significatività comunemente utilizzato nei test A/A e A/B è 5%, che corrisponde a un livello di affidabilità del 95% (livello di affidabilità = 100% - livello di significatività). Un livello di affidabilità del 95% significa che ogni volta che esegui un test, esiste una probabilità del 5% di rilevare un incremento statisticamente significativo anche se non vi è alcuna differenza tra le esperienze.

Supponi di voler raggiungere un livello di affidabilità del 95% con il test A/A. Con un livello di affidabilità del 95%, 1 test A/A su 20 potrebbe mostrare un incremento statisticamente significativo nelle conversioni. Con un livello di affidabilità del 90%, 1 test su 10 potrebbe mostrare un incremento delle conversioni durante il test di esperienze identiche.

## Best practice

Se ritieni necessario un test A/A nell’organizzazione, tieni presente che le esperienze identiche potrebbero mostrare temporaneamente una differenza rispetto al controllo. Questo può essere normale, a seconda del tempo in cui il test può essere eseguito. La differenza dovrebbe ridursi con l’aumentare del tempo e dei visitatori.

Si consiglia di utilizzare una metodologia di test A/B regolare: decidere la dimensione del campione in anticipo in base a una dimensione minima dell’effetto rilevante, alla potenza desiderata e alla significatività utilizzando [Calcolatore dimensioni Adobe Target](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6).

Quindi, lascia un tempo adeguato e i visitatori prima di raggiungere qualsiasi conclusione, e ricorda che a seconda del livello di significatività del test, c&#39;è la possibilità che un&#39;esperienza mostri una differenza nell&#39;incremento, e possa anche essere dichiarata vincitrice.
