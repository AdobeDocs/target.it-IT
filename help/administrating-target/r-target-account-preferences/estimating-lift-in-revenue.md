---
keywords: incremento ricavi;ricavi;stima incremento ricavi;calcolo ricavi;valore stimato
description: Utilizzate  Adobe Target per stimare l'incremento delle entrate che otterreste se tutti gli utenti visualizzassero l'esperienza vincente.
title: Estimate Lift in Revenue (Incremento stimato delle entrate)
feature: Administration & Configuration
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 90%

---


# Stimare l’Incremento dei ricavi{#estimate-lift-in-revenue}

Utilizzate [!DNL Adobe Target] per stimare l&#39;incremento delle entrate che otterreste se tutti gli utenti visualizzassero l&#39;esperienza vincente.

>[!NOTE]
>
>Al momento l&#39;incremento stimato non è disponibile per le attività [!UICONTROL Experience Targeting] (XT) di Experience Targeting.

La funzione per la stima dell’incremento è disattivata per impostazione predefinita. Può essere attivata nelle preferenze dell’account. Solo gli utenti amministratore di Experience Cloud possono abilitare o disabilitare questa funzione. Se la stima dell’incremento è disattivata, i campi corrispondenti non vengono visualizzati nell’interfaccia. La disattivazione della funzione non si traduce in una perdita di dati, compresi i dati utilizzati per le stime. Le stime si basano sui dati raccolti indipendentemente dallo stato di attivazione della funzione.

>[!IMPORTANT]
>
>L’incremento stimato è solo una stima. La sua precisione dipende da una serie di fattori, inclusi i dati previsionali basati sulla continuità delle tendenze correnti. Si tratta di stime basate sulle prestazioni passate e non devono essere utilizzate a scopo di orientamento finanziario. I risultati futuri possono variare.

La funzione di stima calcola la quantità di incremento conseguito dall’esperienza vincente e il numero totale di visitatori per tutta la durata dell’attività, e fornisce l’incremento potenzialmente realizzabile se ogni visitatore visualizza l’esperienza vincente, in caso di tendenze uguali a quelle presenti durante il test.

La stima dell’incremento dei ricavo è calcolata in base al ricavo per visitatore (Revenue per Visit, RPV) ottenuto dalla metrica dell’obiettivo primario.

La stima dell’incremento è calcolata utilizzando la seguente formula: (&lt;RPV esperienza vincente> - &lt;RPV esperienza di controllo&lt;) * &lt;numero totale di visitatori nell’attività>.

Se nella forma condensata è presente solo una cifra prima del decimale, il risultato viene arrotondato al massimo a una cifra decimale. Ad esempio: $ 1,6 M, $ 60 K, $ 900, $ 8,5 K, $ 205 K.

Ad esempio, se l’esperienza vincente mostra un incremento di $ 0,59 e quella di controllo un incremento di $ 0,15, la stima calcola un incremento di $ 0,44 per visitatore. Considerando 75.000 visitatori, se tutti visualizzano l’esperienza vincente e le tendenze correnti non subiscono modifiche, l’incremento dei ricavi sarà di $ 33.000.

Analogamente, se l’esperienza vincente mostra un incremento di $ 0,17 rispetto all’esperienza di controllo e durante il test ci sono stati 192.000 visitatori, se le tendenze attuali restano stabili puoi aspettarti un incremento dei ricavi di $ 32.640.

Il campo della stima dell’incremento dei ricavi è visualizzato come “---” nelle seguenti circostanze:

* Se il numero di visitatori non è sufficiente a calcolare una stima ragionevole.
* Se il valore stimato della metrica non è stato fornito sulla relativa pagina di configurazione.
* Se l’esperienza migliore risulta essere quella di controllo.

Quando si impostano gli obiettivi di un’attività, il campo Valore stimato fornisce un valore per l’obiettivo. Questo valore consente a Target di calcolare un incremento stimato dei ricavi. Questo campo è facoltativo; tuttavia, i ricavi incrementali per eventuali metriche non collegate ai ricavi non possono essere calcolate senza di esso. I dati sono di tipo valuta. Questo campo viene visualizzato progressivamente dopo che l’utente indica l’azione intrapresa per soddisfare l’obiettivo.

Le entrate stimate nel caso in cui il 100% dei visitatori visualizzi l’esperienza vincente, sono riportate nella parte superiore dei rapporti di Target.
