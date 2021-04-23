---
keywords: origine dati comportamentali;analytics;consigli;criteri;variabili prodotto
description: Scopri come utilizzare Adobe Analytics come origine di dati comportamentali per utilizzare i dati comportamentali basati sulla visualizzazione e/o sull’acquisto da Analytics in [!DNL Target] Recommendations.
title: Come si utilizza Adobe Analytics con [!DNL Target] Recommendations?
feature: Consigli
exl-id: d2b7e840-9546-4a8e-bec4-1ebea5a79672
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 1%

---

# Utilizzare Adobe Analytics con Recommendations

L’utilizzo di [!DNL Adobe Analytics] come origine di dati comportamentali consente ai clienti di utilizzare dati comportamentali basati sulla visualizzazione e/o sull’acquisto da [!DNL Analytics] nelle attività di consigli di [!DNL Adobe Target]. Questa funzione è particolarmente utile nelle situazioni in cui la configurazione [!DNL Target Recommendations] è nuova e [!DNL Analytics] contiene molti dati storici da sfruttare.

L’utilizzo di [!DNL Analytics] come origine di dati comportamentali può fungere da ricca fonte di informazioni sul comportamento degli utenti. Ciò potrebbe includere dati provenienti da un’origine o un feed di terze parti condivisi solo con [!DNL Analytics].

Durante la [creazione di criteri](/help/c-recommendations/c-algorithms/create-new-algorithm.md) in Recommendations, sono disponibili due pulsanti di scelta che consentono di scegliere l&#39;origine dati da utilizzare: [!UICONTROL mbox] o [!UICONTROL Analytics].

![Pulsanti dell’origine dei dati comportamentali](/help/c-recommendations/c-algorithms/assets/behavioral-data-source.png)

>[!NOTE]
>
>Se questi due pulsanti non vengono visualizzati nel tuo account, contatta l’ [Assistenza clienti](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

## Casi d’uso per i dati di Analytics in Target

L’utilizzo di [!DNL Analytics] come origine dei dati comportamentali per i consigli consente inoltre di distribuire casi d’uso specifici senza il requisito di assegnare tag alle pagine di entità con tutti i parametri di entità [!DNL Target]. Anche se ciò richiede l&#39;implementazione di alcuni prerequisiti, la disponibilità di &quot;Variabili di prodotto&quot; è la cosa più importante per il corretto funzionamento di tale funzionalità. Le eVar e le proprietà regolari non sono sufficienti per far sì che questo handshake si verifichi automaticamente tra [!DNL Analytics] e [!DNL Target].

Puoi utilizzare [!DNL Analytics] come origine dei dati comportamentali per:

* In una pagina PDP puoi visualizzare raccomandazioni su un sito di vendita al dettaglio per gli utenti, in base a ciò che altri utenti hanno acquistato dalla stessa categoria nell’ultimo mese, utilizzando i dati di Analytics.
* Visualizza il contenuto nella schermata iniziale di un sito multimediale per i contenuti più popolari in una particolare categoria attualmente in tendenza, in base ai dati [!DNL Analytics].

## Implementazione in Analytics

Le sezioni seguenti sono utili per implementare questa funzione sul lato [!DNL Analytics].

### Prerequisiti: configurare le variabili di prodotto in Analytics

È necessario implementare le variabili di prodotto in [!DNL Analytics] con gli attributi necessari richiesti per [!DNL Target Recommendations].

Un formato di feed di esempio [!DNL Target Recommendations] fungerà da guida in cui tutti gli attributi devono essere definiti nelle variabili di prodotto. Successivamente, tali valori devono essere &quot;mappati&quot; nell’interfaccia utente [!DNL Target] per i rispettivi valori di entità [!DNL Target].

>[!NOTE]
>
>Se si tratta di un sito di contenuto, le rispettive parti di contenuto devono essere trattate come &quot;prodotti&quot; e gli attributi associati relativi a tale contenuto (ad esempio: nome dell’autore, data di pubblicazione, titolo del contenuto, mese di rilascio, ecc.) devono essere passati come attributi. La granularità del livello di categoria, o dei tipi di categoria, deve essere decisa dall&#39;impresa in base ai requisiti del caso d&#39;uso.

Per ulteriori dettagli su come impostare le variabili di prodotto, consulta [products](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/products.html) nella *Guida all’implementazione di Analytics*. Alcune delle note presenti in tale documentazione richiedono discrezione al team che le sta distribuendo (esempio: Categoria). È sempre consigliabile consultare l’Adobe prima di eseguire questa attività.

### Considerazioni

[!DNL Analytics] i dati vengono inviati tramite un feed giornaliero. I risultati comportamentali richiederanno fino a 24 ore per essere rispecchiati nei risultati dei consigli sul sito. Come per tutte le impostazioni dei criteri [!DNL Recommendations], questa origine dati può e deve essere testata.

Per un processo decisionale rapido su quale origine di dati deve essere utilizzata, se gli utenti generano molti dati biologici al giorno e non sono molto dipendenti dai dati storici, l’utilizzo di una [!DNL Target] mbox come origine di dati comportamentali può essere una buona soluzione. In casi di minore disponibilità di dati biologici generati di recente, se desideri effettuare il banking con dati [!DNL Analytics], l’utilizzo di [!DNL Analytics] come origine di dati comportamentali è una buona soluzione.

Ora è il momento di mappare queste variabili sul lato [!DNL Target] per una fornitura continua di dati comportamentali.

## Implementare in Target

1. In Target, fai clic su **[!UICONTROL Recommendations]**, quindi fai clic sulla scheda **[!UICONTROL Feed]** .

   ![Feed](/help/c-recommendations/c-algorithms/assets/feeds-tab.png)

1. Fai clic su **[!UICONTROL Crea feed]**.

1. Seleziona **[!UICONTROL Classificazioni Analytics]**, quindi specifica la suite di rapporti.

   ![Opzione Classificazioni di Analytics](/help/c-recommendations/c-algorithms/assets/analytics-classifications.png)

1. Fai clic su **[!UICONTROL Mappatura]**, quindi mappare le intestazioni delle colonne dei campi sui nomi di campo [!UICONTROL Recommendations] appropriati.

   ![Sezione mappatura](/help/c-recommendations/c-algorithms/assets/mapping.png)

1. Fai clic su **[!UICONTROL Salva]**.

## Domande frequenti 

Quando utilizzi [!DNL Analytics] con [!DNL Target] , considera le seguenti domande frequenti:

### I valori `entity.id` e `entity.categoryId` devono essere trasmessi all&#39;interno della chiamata mbox [!DNL Target]?

Sì, questi due valori sono ancora obbligatori. Gli altri attributi possono essere passati tramite un feed [!DNL Analytics], come descritto in questo documento.

### Posso usare le regole di inclusione dinamica, ad esempio il parametro di entità corrisponde agli attributi di profilo utilizzando l’approccio dei feed [!DNL Analytics]?

Sì, puoi. Il metodo è simile quando si utilizza [!DNL Target] stand-alone. In questo caso, tuttavia, è necessario tenere presente il fattore di temporizzazione. Le variabili di entità che si suppone corrispondano alle variabili di profilo dipendono dal livello di dati che potrebbe apparire molto più tardi sulla pagina.
