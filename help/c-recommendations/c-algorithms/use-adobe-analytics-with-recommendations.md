---
keywords: behavioral data source;analytics;recommendations;criteria;product variables
description: Utilizzando  Adobe Analytics come origine dati comportamentale, i client possono utilizzare i dati comportamentali basati sulla visualizzazione e/o sull'acquisto di Analytics in  Adobe Recommendations.
title: Utilizzo di  Adobe Analytics con Target Recommendations
feature: criteria
translation-type: tm+mt
source-git-commit: 9bf30d6397fefdc85e51e2bd431ba163b10f6c09
workflow-type: tm+mt
source-wordcount: '761'
ht-degree: 1%

---


# Usare  Adobe Analytics con Recommendations

L&#39;utilizzo [!DNL Adobe Analytics] come origine dati comportamentale consente ai client di utilizzare i dati comportamentali basati sulla visualizzazione e/o sull&#39;acquisto provenienti da [!DNL Analytics] nelle attività delle [!DNL Adobe Target] raccomandazioni. Questa funzione è particolarmente utile nelle situazioni in cui la [!DNL Target Recommendations] configurazione è nuova e [!DNL Analytics] dispone di molti dati storici da sfruttare.

L&#39;utilizzo [!DNL Analytics] come origine dati comportamentale può fungere da ricca fonte di informazioni sul comportamento degli utenti. Ciò può includere dati provenienti da un&#39;origine di terze parti o feed condivisi solo con [!DNL Analytics].

Durante la [creazione di criteri](/help/c-recommendations/c-algorithms/create-new-algorithm.md) in Recommendations, sono disponibili due pulsanti di scelta che consentono di scegliere l&#39;origine dati da utilizzare: [!UICONTROL mbox] o [!UICONTROL Analytics].

![Pulsanti delle origini dati comportamentali](/help/c-recommendations/c-algorithms/assets/behavioral-data-source.png)

>[!NOTE]
>
>Se questi due pulsanti non vengono visualizzati nell&#39;account, rivolgiti all&#39;Assistenza [](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)clienti.

## Casi d&#39;uso

L&#39;utilizzo [!DNL Analytics] come origine dati comportamentale per le raccomandazioni consente inoltre di distribuire casi d&#39;uso specifici senza il requisito di assegnare tag alle pagine di entità con tutti i parametri di [!DNL Target] entità. Anche se ciò richiede l&#39;implementazione di alcuni prerequisiti, la disponibilità di &quot;Variabili di prodotto&quot; è la cosa più importante per il funzionamento di tale funzionalità senza problemi. Le eVar e le prop regolari non sono sufficienti per consentire l&#39;applicazione automatica di questa stretta di mano tra [!DNL Analytics] e [!DNL Target].

Puoi utilizzare [!DNL Analytics] come origine dati comportamentale per:

* Mediante l&#39;utilizzo dei dati di Analytics, è possibile visualizzare raccomandazioni su un sito retail per la vendita al dettaglio agli utenti di una pagina PDP, in base agli acquisti effettuati da altri utenti della stessa categoria nell&#39;ultimo mese.
* Mediante questo componente, potete visualizzare i contenuti presenti nella schermata iniziale di un sito multimediale per i contenuti più popolari in una particolare categoria che attualmente ha un andamento, in base ai [!DNL Analytics] dati.

## Implementazione in Analytics

Le sezioni seguenti sono utili per implementare questa funzione sul [!DNL Analytics] lato.

### Prerequisiti: variabili di prodotto in Analytics

Devi implementare le variabili di prodotto in [!DNL Analytics] con gli attributi necessari per [!DNL Target Recommendations].

Un formato di feed [!DNL Target Recommendations] di esempio fungerà da guida su cui tutti gli attributi devono essere definiti nelle variabili di prodotto. Successivamente, tali valori devono essere &quot;mappati&quot; nell&#39; [!DNL Target] interfaccia utente per i rispettivi valori di [!DNL Target] entità.

>[!NOTE]
>
>Se si tratta di un sito di contenuti, le rispettive parti di contenuto devono essere trattate come &quot;prodotti&quot; e gli attributi associati relativi a tale contenuto (ad esempio: nome autore, data di pubblicazione, titolo contenuto, mese di rilascio, ecc.) devono essere passati come attributi. La granularità del livello di categoria o dei tipi di categoria dovrebbe essere decisa dall&#39;impresa in base ai requisiti del caso d&#39;uso.

Per ulteriori dettagli su come impostare le variabili di prodotto, vedi [prodotti](https://docs.adobe.com/content/help/en/analytics/implementation/vars/page-vars/products.html) nella Guida all&#39;implementazione di *Analytics*. Alcune delle note contenute in tale documentazione richiedono discrezione da parte del team che la sta distribuendo (ad esempio: Categoria). È sempre consigliabile consultare  Adobe prima di eseguire questa attività.

### Considerazioni

[!DNL Analytics] i dati vengono inviati tramite un feed giornaliero. I risultati comportamentali richiederanno fino a 24 ore per essere visualizzati nei risultati delle raccomandazioni sul sito. Come per tutte le impostazioni dei [!DNL Recommendations] criteri, questa origine dati può e deve essere testata.

Per un rapido processo decisionale sull&#39;origine dati da utilizzare, se ci sono molti dati organici generati ogni giorno dagli utenti, e non molta dipendenza richiesta dai dati storici, allora utilizzare una [!DNL Target] mbox come l&#39;origine dati comportamentale può essere una buona misura. In caso di minore disponibilità di dati organici generati di recente, se si desidera eseguire il bank sui [!DNL Analytics] dati, l&#39;utilizzo [!DNL Analytics] come origine dati comportamentale è una buona misura.

### Contatta l’Assistenza clienti per creare un feed di dati

Presupponendo che tutti i prerequisiti siano stati predisposti, contatta l’Assistenza [](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) clienti per richiedere la creazione di un feed di dati.

## Implementazione in Target

1. In Target, fate clic su **[!UICONTROL Recommendations]**, quindi fate clic sulla scheda **[!UICONTROL Feed]** .

   ![Feed](/help/c-recommendations/c-algorithms/assets/feeds-tab.png)

1. Fate clic su **[!UICONTROL Crea feed]**.

1. Seleziona Classificazioni **** Analytics, quindi specifica la suite di rapporti.

   ![Classificazioni di Analytics, opzione](/help/c-recommendations/c-algorithms/assets/analytics-classifications.png)

1. Fate clic su **[!UICONTROL Mapping]**, quindi mappate le intestazioni delle colonne dei campi ai nomi dei campi [!UICONTROL Recommendations] appropriati.

   ![Sezione mapping](/help/c-recommendations/c-algorithms/assets/mapping.png)

1. Fai clic su **[!UICONTROL Salva]**.

## Domande frequenti 

Considerate le seguenti domande frequenti utilizzate [!DNL Analytics] con [!DNL Target]:

### I valori `entity.id` e `entity.categoryId` devono essere passati all&#39;interno della chiamata [!DNL Target] mbox?

Sì, questi due valori sono ancora obbligatori. Gli altri attributi possono essere passati tramite un [!DNL Analytics] feed, come descritto in questo documento.

### Posso utilizzare le regole di inclusione dinamica, ad esempio il parametro di entità corrisponde agli attributi di profilo utilizzando l&#39;approccio [!DNL Analytics] feed?

Sì, puoi. Il metodo è simile quando si utilizza il metodo [!DNL Target] standalone. In questo caso, tuttavia, dovete essere attenti al fattore di temporizzazione. Le variabili di entità che dovrebbero corrispondere alle variabili di profilo dipendono dal livello dati che potrebbe essere visualizzato molto più tardi sulla pagina.

