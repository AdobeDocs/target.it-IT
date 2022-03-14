---
keywords: a/b;a/a;aa;
description: Scopri cos’è un test A/A, perché eseguire un test A/A, per quanto tempo eseguire il test e come interpretare i risultati.
title: Cos’è il test A/A?
feature: A/B Tests
exl-id: 7489f4f5-3655-45f9-a743-651ba1c23c53
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 1%

---

# Test A/A

Prima di eseguire un test A/A sul sito utilizzando [!DNL Adobe Target], è importante comprendere cos’è un test A/A, perché eseguire un test A/A, per quanto tempo eseguire il test e come interpretare i risultati.

## Cos’è un test A/A?

Prima di spiegare il test A/A, è utile rivedere il test A/B in modo da poter discutere delle differenze.

In un test A/B standard, il traffico viene allocato a due o più esperienze diverse. Un’esperienza è tipicamente il &quot;controllo&quot; e le varianti dell’esperienza vengono testate rispetto al controllo per vedere quale esperienza crea l’incremento più elevato in una determinata metrica.

Il test A/A, tuttavia, comporta l’allocazione del traffico a due esperienze identiche, di norma con un’allocazione del traffico suddivisa in 50/50. Con un test A/B standard, in genere desideri scoprire un incremento nella conversione. Questo differisce da un test A/A in cui l&#39;obiettivo di solito è determinare che ci sono *no* differenza di incremento tra le esperienze identiche.

## Perché vuoi testare due esperienze identiche e cosa si ottiene?

Alcune organizzazioni eseguono un test A/A durante l&#39;implementazione di un nuovo strumento di test, ad esempio [!DNL Target], per determinare se:

* L’attività è stata configurata correttamente
* Il codice è stato implementato correttamente
* La segnalazione è accurata

Sebbene poche organizzazioni eseguano test A/A, è in realtà buona prassi eseguirli come esperimenti di &quot;sanità pubblica&quot; per creare fiducia dopo l’implementazione dello strumento o prima di eseguire test A/B che potrebbero influenzare la conversione e i ricavi.

## Perché potresti visualizzare un incremento per un’esperienza quando le esperienze sono identiche?

Ci sono numerose ragioni per cui potresti vedere un incremento in un’esperienza rispetto a un’altra (identica) esperienza:

### Il test A/A è stato monitorato continuamente

Un problema comune nell’esecuzione di qualsiasi tipo di test, incluso un test A/A, è quello di esaminare continuamente i risultati e arrestare prematuramente un test non appena vedi la rilevanza statistica e dichiarare un’esperienza vincente. Gli analisti spesso fanno ciò che viene chiamato &quot;sbirciando dati&quot;. Il peking dei dati comporta l’analisi dei dati del test in modo rapido e frequente, mentre si cerca di determinare quale esperienza funziona meglio. Il rischio è quello di arrestare il test prematuramente, il che potrebbe invalidare i risultati.

In un test A/A, il peking dei dati può spesso causare agli analisti un incremento in un’esperienza, quando in realtà non dovrebbe esserci alcuna differenza, perché le due esperienze sono identiche. Infatti, con un&#39;sbirciata continua, i test A/A sono in realtà _garantito_ mostrare &quot;rilevanza statistica&quot; (vale a dire, un’affidabilità al di sopra di una certa soglia, ad esempio il 95%) ad un certo punto durante il test.

Per evitare questo problema, e come con un normale test A/B, è quindi necessario decidere in anticipo quale dimensione del campione utilizzare, in base alla dimensione minima dell’effetto (l’incremento minimo al di sotto del quale un effetto non è importante per la propria attività), potenza e livelli di significatività ritenuti accettabili.

In un test A/A, l’obiettivo sarebbe quindi quello di *not* dopo aver raggiunto la dimensione desiderata del campione, puoi vedere un risultato statisticamente significativo.

La [!UICONTROL Calcolatore delle dimensioni del campione di Adobe Target] è uno strumento importante per determinare la dimensione del campione a cui si desidera indirizzare e per quanto tempo eseguire il test.

* [Calcolatore delle dimensioni di Adobe Target](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6)

Inoltre, consulta i seguenti articoli per informazioni su per quanto tempo eseguire un’attività, nonché altri suggerimenti e trucchi utili:

* [Per quanto tempo si deve eseguire un test A/B?](/help/main/c-activities/t-test-ab/sample-size-determination.md)
* [Dieci insidie A/B comuni e come evitarle](/help/main/c-activities/t-test-ab/common-ab-testing-pitfalls.md)

### L’importanza statistica influisce sui risultati dei test

Il livello di significatività di un test determina la probabilità che il test riporti una differenza significativa nei tassi di conversione tra due offerte diverse, quando, in realtà, non vi è alcuna differenza reale. Questo è noto come falso positivo o errore di tipo I. Il livello di significatività è una soglia specificata dall’utente ed esiste un compromesso tra la tolleranza per i falsi positivi e il numero di visitatori che devono essere inclusi nel test nella scelta del livello di significatività corretto.

Un livello di significatività comunemente utilizzato nei test A/A e A/B è del 5%, che corrisponde a un livello di affidabilità del 95% (livello di affidabilità = 100% - livello di significatività). Un livello di affidabilità del 95% indica che ogni volta che esegui un test, esiste una probabilità del 5% di rilevare un incremento statisticamente significativo, anche se non c’è differenza tra le esperienze.

Supponiamo di voler raggiungere un livello di affidabilità del 95% con il test A/A. Con un livello di affidabilità del 95%, 1 test A/A su 20 potrebbe mostrare un incremento statisticamente significativo nelle conversioni. Con un livello di affidabilità del 90%, 1 test su 10 potrebbe mostrare un incremento nelle conversioni quando si testano esperienze identiche.

## Best practice

Se decidi che nell’organizzazione è necessario un test A/A, tieni presente che le esperienze identiche potrebbero temporaneamente mostrare una differenza rispetto al controllo. Ciò può essere normale, a seconda del momento in cui il test può essere eseguito. La differenza dovrebbe ridursi a causa di più tempo e visitatori.

Si consiglia di utilizzare una metodologia di test A/B regolare: decide in anticipo la dimensione del campione in base a una dimensione minima dell&#39;effetto, alla potenza desiderata e alla significatività utilizzando [Calcolatore delle dimensioni di Adobe Target](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6).

Quindi, concedi tempo adeguato e ai visitatori prima di raggiungere qualsiasi conclusione e ricorda che a seconda del livello di significatività del test, esiste la possibilità che un’esperienza mostri una differenza di incremento, e anche che venga dichiarata l’esperienza vincente.
