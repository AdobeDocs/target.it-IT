---
keywords: origine dati comportamentali;analytics;consigli;criteri;variabili prodotto
description: Scopri come utilizzare Adobe Analytics come origine di dati comportamentali per utilizzare i dati comportamentali basati sulla visualizzazione e/o sugli acquisti di Analytics in [!DNL Target] Recommendations.
title: Come si utilizza Adobe Analytics con [!DNL Target] Recommendations?
feature: Recommendations
exl-id: d2b7e840-9546-4a8e-bec4-1ebea5a79672
source-git-commit: 2a4cae206bf634bf3fbec65c5c4b289aadefede1
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 1%

---

# Utilizza Adobe Analytics con Recommendations

Utilizzo [!DNL Adobe Analytics] come origine di dati comportamentali consente ai client di utilizzare i dati comportamentali basati sulla visualizzazione e/o sull’acquisto da [!DNL Analytics] in [!DNL Adobe Target] attività di consigli. Questa funzione è particolarmente utile nelle situazioni in cui [!DNL Target Recommendations] la configurazione è nuova e [!DNL Analytics] ha molti dati storici da sfruttare.

Utilizzo [!DNL Analytics] come l’origine dei dati comportamentali può fungere da ricca fonte di informazioni sul comportamento degli utenti. Ciò potrebbe includere dati provenienti da un’origine o un feed di terze parti condivisi solo con [!DNL Analytics].

Quando [creazione di criteri](/help/c-recommendations/c-algorithms/create-new-algorithm.md) in Recommendations sono disponibili due pulsanti di scelta che consentono di scegliere l’origine dati da utilizzare: [!UICONTROL mbox] o [!UICONTROL Analytics].

![Pulsanti dell’origine dei dati comportamentali](assets/behavioral-data-source.png)

>[!NOTE]
>
>Se questi due pulsanti non vengono visualizzati nel tuo account, contatta [Assistenza clienti](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

## Casi d’uso per i dati di Analytics in Target

Utilizzo [!DNL Analytics] come origine di dati comportamentali per i consigli fornisce anche la possibilità di distribuire casi d’uso specifici senza il requisito di assegnare tag alle pagine di entità con tutti i [!DNL Target] parametri di entità. Anche se ciò richiede l&#39;implementazione di alcuni prerequisiti, la disponibilità di &quot;Variabili di prodotto&quot; è la cosa più importante per il corretto funzionamento di tale funzionalità. Le eVar e le proprietà regolari non sono sufficienti per far sì che questo handshake si verifichi automaticamente tra [!DNL Analytics] e [!DNL Target].

È possibile utilizzare [!DNL Analytics] come origine dei dati comportamentali per:

* In una pagina PDP puoi visualizzare raccomandazioni su un sito di vendita al dettaglio per gli utenti, in base a ciò che altri utenti hanno acquistato dalla stessa categoria nell’ultimo mese, utilizzando i dati di Analytics.
* Visualizza i contenuti nella schermata iniziale di un sito multimediale per i contenuti più popolari in una particolare categoria attualmente in tendenza, in base a [!DNL Analytics] dati.

## Implementazione in Analytics

Le sezioni seguenti ti aiuteranno a implementare questa funzione nel [!DNL Analytics] lato.

### Prerequisiti: configurare le variabili di prodotto in Analytics

Devi implementare le variabili di prodotto in [!DNL Analytics] con gli attributi necessari per [!DNL Target Recommendations].

A [!DNL Target Recommendations] il formato di feed di esempio fungerà da guida su cui tutti gli attributi devono essere definiti nelle variabili di prodotto. Successivamente, tali valori devono essere &quot;mappati&quot; all&#39;interno della [!DNL Target] Interfaccia per i rispettivi [!DNL Target] valori di entità.

>[!NOTE]
>
>Se si tratta di un sito di contenuto, le rispettive parti di contenuto devono essere trattate come &quot;prodotti&quot; e gli attributi associati relativi a tale contenuto (ad esempio: nome dell’autore, data di pubblicazione, titolo del contenuto, mese di rilascio, ecc.) devono essere passati come attributi. La granularità del livello di categoria, o dei tipi di categoria, deve essere decisa dall&#39;impresa in base ai requisiti del caso d&#39;uso.

Per maggiori dettagli su come impostare le variabili di prodotto, vedi [products](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/products.html) in *Guida all’implementazione di Analytics*. Alcune delle note presenti in tale documentazione richiedono discrezione al team che le sta distribuendo (esempio: Categoria). È sempre consigliabile consultare l’Adobe prima di eseguire questa attività.

### Considerazioni

[!DNL Analytics] i dati vengono inviati tramite un feed giornaliero. I risultati comportamentali richiederanno fino a 24 ore per essere rispecchiati nei risultati dei consigli sul sito. Come per tutti [!DNL Recommendations] impostazioni dei criteri, questa origine dati può e deve essere testata.

Per un processo decisionale rapido sull&#39;origine di dati da utilizzare, se gli utenti generano molti dati organici quotidianamente e non richiedono molta dipendenza dai dati storici, utilizzano un [!DNL Target] mbox come origine di dati comportamentali può essere una buona misura. In caso di minore disponibilità di dati biologici generati di recente, se si desidera effettuare un&#39;analisi [!DNL Analytics] i dati, quindi l&#39;utilizzo [!DNL Analytics] poiché l’origine dei dati comportamentali è una buona soluzione.

Ora è il momento di mappare queste variabili su [!DNL Target] per la fornitura continua di dati comportamentali.

## Implementare in Target

1. In Target, fai clic su **[!UICONTROL Recommendations]**, quindi fai clic su **[!UICONTROL Feed]** scheda .

   ![Feed](/help/c-recommendations/c-algorithms/assets/feeds-tab.png)

1. Fai clic su **[!UICONTROL Creazione di un feed]**.

1. Seleziona **[!UICONTROL Classificazioni di Analytics]**, quindi specifica la suite di rapporti.

   ![Opzione Classificazioni di Analytics](/help/c-recommendations/c-algorithms/assets/analytics-classifications.png)

1. Fai clic su **[!UICONTROL Mappatura]**, quindi mappa le intestazioni della colonna del campo nel modo appropriato [!UICONTROL Recommendations] nomi di campo.

   ![Sezione mappatura](/help/c-recommendations/c-algorithms/assets/mapping.png)

1. Fai clic su **[!UICONTROL Salva]**.

## Domande frequenti 

Considera le seguenti domande frequenti mentre utilizzi [!DNL Analytics] con [!DNL Target]:

### Sono `entity.id` e `entity.categoryId` valori che devono essere trasmessi all&#39;interno del [!DNL Target] Chiamata mbox?

Sì, questi due valori sono ancora obbligatori. Il resto degli attributi può essere trasmesso tramite un [!DNL Analytics] feed, come descritto in questo documento.

### Posso utilizzare regole di inclusione dinamiche, ad esempio il parametro di entità corrisponde agli attributi di profilo utilizzando [!DNL Analytics] approccio ai mangimi?

Sì, puoi. Il metodo è simile quando si utilizza [!DNL Target] stand-alone. In questo caso, tuttavia, è necessario tenere presente il fattore di temporizzazione. Le variabili di entità che si suppone corrispondano alle variabili di profilo dipendono dal livello di dati che potrebbe apparire molto più tardi sulla pagina.
