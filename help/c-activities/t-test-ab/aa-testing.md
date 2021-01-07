---
keywords: a/b;a/a;aa;
description: Prima di eseguire un test A/A sul sito utilizzando  Adobe Target, è importante comprendere il significato di un test A/A, il motivo per cui potrebbe essere necessario eseguire un test A/A, il periodo di esecuzione del test e come interpretare i risultati.
title: Test A/A
feature: A/B Tests
translation-type: tm+mt
source-git-commit: 8110807a73e4d6d9848a52224db04faba033c98c
workflow-type: tm+mt
source-wordcount: '904'
ht-degree: 1%

---


# Test A/A

Prima di eseguire un test A/A sul sito utilizzando [!DNL Adobe Target], è importante comprendere il risultato di un test A/A, il motivo per cui potrebbe essere necessario eseguire un test A/A, il periodo di esecuzione del test e come interpretare i risultati.

## Cos&#39;è il test A/A?

Prima di spiegare i test A/A, è utile rivedere i test A/B in modo da poter discutere le differenze.

In un test A/B standard, il traffico viene allocato a due o più esperienze diverse. Un&#39;esperienza è in genere il &quot;controllo&quot; e le variazioni dell&#39;esperienza vengono testate rispetto al controllo per vedere quale esperienza crea il maggior incremento in una data metrica.

Il test A/A, tuttavia, comporta l&#39;allocazione del traffico a due esperienze identiche, in genere con una suddivisione dell&#39;allocazione del traffico pari a 50/50. Con un test A/B standard, si desidera in genere scoprire un incremento nella conversione. Ciò è diverso da un test A/A in cui l&#39;obiettivo in genere è determinare che esiste una differenza *no* nell&#39;incremento tra le esperienze identiche.

## Perché vuoi testare due esperienze identiche e cosa si ottiene?

Alcune organizzazioni eseguono test A/A durante l&#39;implementazione di un nuovo strumento di test, come [!DNL Target], per determinare se:

* L&#39;attività è stata impostata correttamente
* Il codice è stato implementato correttamente
* La segnalazione è accurata

Anche se poche organizzazioni eseguono i test A/A, in realtà è buona prassi eseguirli come esperimenti di &quot;sanità mentale&quot; per creare fiducia dopo l&#39;implementazione dello strumento o prima di eseguire test A/B che potrebbero influenzare conversione e ricavi.

## Perché potresti visualizzare un incremento per un&#39;esperienza quando le esperienze sono identiche?

Ci sono diversi motivi per cui potresti visualizzare un incremento in un&#39;esperienza rispetto a un&#39;altra (identica) esperienza:

### Impossibile eseguire il test A/A abbastanza a lungo

Un problema comune nell&#39;esecuzione di qualsiasi tipo di test, incluso un test A/A, è quello di arrestare prematuramente un test e dichiarare un&#39;esperienza vincente. Gli analisti spesso fanno ciò che viene chiamato &quot;peeking dei dati&quot;. L&#39;anteprima dei dati comporta l&#39;analisi precoce e frequente dei dati del test, cercando di determinare quale esperienza funziona meglio. Il rischio è quello di arrestare il test prematuramente, il che potrebbe invalidare i risultati.

In un test A/A, l&#39;anteprima dei dati può spesso indurre gli analisti a vedere l&#39;incremento in un&#39;unica esperienza, quando presuppongono che non ci debba essere alcuna differenza, perché le due esperienze sono identiche. Data la durata e le visite sufficienti, la differenza nell&#39;incremento dovrebbe ridursi.

Come per un normale test A/B, è quindi necessario decidere in anticipo la dimensione del campione da utilizzare, in base alla dimensione minima dell&#39;effetto, alla potenza e ai livelli di rilevanza considerati accettabili. In un test A/A, l&#39;obiettivo sarebbe quindi *not* vedere un risultato statisticamente significativo dopo che il test ha raggiunto la dimensione del campione desiderata.

[!UICONTROL  Adobe Target Sample Size Calculator] è uno strumento importante per determinare la dimensione del campione a cui si desidera mirare e per quanto tempo eseguire il test.

* [Calcolatore  dimensioni Adobe Target](/help/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6)

Inoltre, consultate i seguenti articoli per informazioni sul periodo di esecuzione di un&#39;attività, nonché altri consigli e trucchi utili:

* [Per quanto tempo si deve eseguire un test A/B?](/help/c-activities/t-test-ab/sample-size-determination.md)
* [Dieci comuni insidie A/B e come evitarle](/help/c-activities/t-test-ab/common-ab-testing-pitfalls.md)

### Il significato statistico influisce sui risultati del test

Il livello di rilevanza di un test determina la probabilità che il test indichi una differenza significativa nei tassi di conversione tra due offerte diverse quando, in realtà, non esiste alcuna differenza reale. Questo è noto come falso positivo o come errore di tipo I. Il livello di rilevanza è una soglia specificata dall&#39;utente ed esiste un compromesso tra la tolleranza per i falsi positivi e il numero di visitatori che devono essere inclusi nel test nella scelta del livello di rilevanza corretto.

Un livello di rilevanza comunemente utilizzato nei test A/A e A/B è del 5%, che corrisponde a un livello di confidenza del 95% (livello di confidenza = 100% - livello di rilevanza). Un livello di confidenza del 95% indica che ogni volta che eseguite un test, esiste una probabilità del 5% di rilevare un incremento statisticamente significativo, anche se non c&#39;è differenza tra le esperienze.

Supponete di voler raggiungere un livello di confidenza del 95% con il test A/A. Con un livello di confidenza del 95%, 1 test A/A su 20 potrebbe mostrare un incremento statisticamente significativo delle conversioni. Con un livello di confidenza del 90%, 1 test su 10 potrebbe mostrare un incremento delle conversioni quando si verificano esperienze identiche.

## Best practice

Se decidete che un test A/A è necessario nell&#39;organizzazione, tenete presente che le esperienze identiche potrebbero temporaneamente mostrare una differenza dal controllo. Questo può essere normale, a seconda dell&#39;ora in cui è consentito eseguire il test. La differenza dovrebbe ridursi, dati più tempo e visitatori.

La best practice consiste nell&#39;utilizzare una metodologia di test A/B regolare: decidete in anticipo la dimensione del campione in base alla dimensione minima dell&#39;effetto, alla potenza e al significato desiderati utilizzando il [ Adobe Target Size Calculator](/help/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6).

Quindi, concedi tempo e visitatori adeguati prima di raggiungere qualsiasi conclusione, e ricorda che a seconda del livello di rilevanza del test, esiste la possibilità che un&#39;esperienza mostrerà una differenza in incremento, e anche essere dichiarato vincitore.
