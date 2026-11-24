---
keywords: origine dati comportamentali;analisi;consigli;criteri;variabili prodotto
description: Scopri come utilizzare [!DNL Adobe Analytics] come origine dei dati comportamentali in [!DNL Target Recommendations].
title: Utilizza Adobe Analytics con la funzione Consigli
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: d2b7e840-9546-4a8e-bec4-1ebea5a79672
TQID: 'https://experienceleague.adobe.com/2ryixOT-YoKjDlMbqs8g2DJElNVmlCUFhbdZzpfSnNs'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c4147b6e-073b-4d3c-9ab1-d60f2f4434ef
    internal-label: Behavioral data
source-git-commit: 374d176c5c40826d958a8b87d220422466433690
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 1%
---
# Usa [!DNL Adobe Analytics] con [!DNL Recommendations] {#use-analytics-with-recommendations}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come utilizzare [!DNL Adobe Analytics] come origine dei dati comportamentali nelle attività di [!DNL Adobe Target Recommendations].

>[!ENDSHADEBOX]

L&#39;utilizzo di [!DNL Adobe Analytics] come origine dei dati comportamentali consente alle attività di [!DNL Adobe Target Recommendations] di utilizzare i dati comportamentali basati su visualizzazione e su acquisto di [!DNL Analytics]. Questa funzione è utile quando la configurazione di [!DNL Target Recommendations] è nuova e [!DNL Analytics] ha molti dati storici da utilizzare. I dati potrebbero inoltre includere informazioni provenienti da un&#39;origine o un feed di terze parti condiviso solo con [!DNL Analytics].

L&#39;origine dati è selezionata con l&#39;opzione **[!UICONTROL Behavioral Data Source]** durante la [creazione dei criteri](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#data-source) in [!DNL Recommendations]: **[!UICONTROL Adobe Target]** o **[!UICONTROL Analytics]**.

>[!NOTE]
>
>Se queste due opzioni non vengono visualizzate nell&#39;account, contatta l&#39;[Assistenza clienti](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

## Casi d&#39;uso per i dati [!DNL Analytics] in [!DNL Target] {#use-cases}

L&#39;utilizzo di [!DNL Analytics] come origine dei dati comportamentali consente inoltre di distribuire casi d&#39;uso specifici senza assegnare tag alle pagine delle entità con tutti i parametri delle entità [!DNL Target]. Questo richiede alcuni prerequisiti e la disponibilità di &quot;Variabili di prodotto&quot; è quella più importante. Le eVar e le proprietà regolari non sono sufficienti per consentire a [!DNL Analytics] e [!DNL Target] di scambiare automaticamente questi dati.

[!DNL Analytics] può essere utilizzato come origine dei dati comportamentali per:

* Visualizzare i suggerimenti su un sito di vendita al dettaglio agli utenti in una pagina dei dettagli di un prodotto, in base agli altri utenti che hanno acquistato dalla stessa categoria nell&#39;ultimo mese, utilizzando i dati di [!DNL Analytics].
* Visualizza contenuto nella schermata iniziale di un sito multimediale per i contenuti più popolari in una particolare categoria che è attualmente in tendenza, in base ai dati di [!DNL Analytics].

## Implementazione in [!DNL Analytics]

### Prerequisiti: configurare le variabili di prodotto in [!DNL Analytics] {#prerequisites}

Implementare le variabili di prodotto in [!DNL Analytics] con gli attributi richiesti per [!DNL Target Recommendations]. Un esempio di formato di feed [!DNL Target Recommendations] guida gli attributi che devono essere definiti nelle variabili di prodotto. Questi valori devono essere successivamente &quot;mappati&quot; nell&#39;interfaccia utente [!DNL Target] ai rispettivi valori dell&#39;entità [!DNL Target].

>[!NOTE]
>
>Se si tratta di un sito di contenuti, le rispettive parti di contenuto devono essere trattate come &quot;prodotti&quot; e gli attributi associati di tale contenuto devono essere passati come attributi. Tali attributi possono includere il nome dell’autore, la data di pubblicazione, il titolo del contenuto, il mese di rilascio e così via. L’azienda deve decidere la granularità del livello di categoria, o dei tipi di categoria, in base ai requisiti del caso d’uso.

Per ulteriori dettagli sulla configurazione delle variabili di prodotto, vedi [products](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/products.html) nella *Guida all&#39;implementazione di Adobe Analytics*. Alcune delle note in tale documentazione, ad esempio quelle relative alla categoria, richiedono il giudizio del team che le distribuisce. Consulta [!DNL Adobe] prima che questa attività sia consigliata.

### Considerazioni {#considerations}

I dati di [!DNL Analytics] vengono inviati tramite un feed giornaliero. I risultati comportamentali possono richiedere fino a 24 ore per essere riflessi nei risultati delle raccomandazioni sul sito. Come per tutte le impostazioni dei criteri [!DNL Recommendations], questa origine dati deve essere testata.

Per scegliere un&#39;origine dati:

* Una mbox [!DNL Target] è adatta quando molti dati organici vengono generati ogni giorno dagli utenti ed è necessaria una piccola dipendenza dai dati storici.
* [!DNL Analytics] è adatto quando di recente sono stati generati meno dati organici e devono essere utilizzati i dati [!DNL Analytics].

I valori `entity.id` e `entity.categoryId` devono ancora essere trasmessi nella chiamata mbox [!DNL Target]. Gli altri attributi possono essere trasmessi tramite un feed [!DNL Analytics], come descritto in questa pagina.

Le regole di inclusione dinamica, ad esempio la corrispondenza di un parametro di entità a un attributo di profilo, possono essere utilizzate con l&#39;approccio feed [!DNL Analytics]. Il metodo è simile all&#39;utilizzo di [!DNL Target] in modo autonomo, ma è necessario considerare la tempistica: le variabili di entità che devono corrispondere alle variabili di profilo dipendono dal livello dati, che potrebbe apparire molto più tardi sulla pagina.

## Implementare in [!DNL Target] {#implement-target}

Le variabili di prodotto sono mappate in [!DNL Target] per fornire una fornitura continua di dati comportamentali.

1. In [!DNL Target], fai clic su **[!UICONTROL Consigli]**, quindi fai clic sulla scheda **[!UICONTROL Feed]**.

1. Fare clic su **[!UICONTROL Crea feed]**.

   ![Pagina Feed con il pulsante Crea feed evidenziato](../assets/feeds_1.png)

1. Seleziona **[!UICONTROL Classificazioni Analytics]**, quindi specifica la suite di rapporti.

1. Fai clic su **[!UICONTROL Avanti]** per passare alle impostazioni **[!UICONTROL Pianifica]**, quindi seleziona una frequenza per il feed: **[!UICONTROL Giornaliero]**, **[!UICONTROL Settimanale]**, **[!UICONTROL Ogni 2 settimane]** o **[!UICONTROL Mai]**. È inoltre possibile selezionare l’ora del giorno in cui elaborare il feed.

   ![Passaggio pianificato della finestra di dialogo Crea feed con le opzioni di frequenza Giornaliero, Settimanale, Ogni 2 settimane e Mai e il campo Ora del giorno](../assets/feeds_3.png)

1. Fai clic su **[!UICONTROL Avanti]** per passare alle impostazioni di **[!UICONTROL Mappatura]**, quindi mappa le intestazioni delle colonne di campo ai nomi di campo **[!UICONTROL Consigli]** appropriati.

1. Fai clic su **[!UICONTROL Salva]**.

Per ulteriori informazioni sulla creazione di un feed, vedere [Creare un feed](/help/main/c-recommendations/c-products/feeds.md#steps).
