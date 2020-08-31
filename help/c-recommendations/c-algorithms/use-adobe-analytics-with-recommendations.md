---
keywords: behavioral data source;analytics;recommendations;criteria;product variables
description: Utilizzando  Adobe Analytics come origine dati comportamentale, i client possono utilizzare i dati comportamentali basati sulla visualizzazione e/o sull'acquisto di Analytics in  Adobe Recommendations.
title: Utilizzo di  Adobe Analytics con Target Recommendations
feature: criteria
translation-type: tm+mt
source-git-commit: f9e185ed9b8dbf2b96ac5476ba5b050725e81d4b
workflow-type: tm+mt
source-wordcount: '1024'
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

## Casi di utilizzo per i dati di Analytics in Target

L&#39;utilizzo [!DNL Analytics] come origine dati comportamentale per le raccomandazioni consente inoltre di distribuire casi d&#39;uso specifici senza il requisito di assegnare tag alle pagine di entità con tutti i parametri di [!DNL Target] entità. Anche se ciò richiede l&#39;implementazione di alcuni prerequisiti, la disponibilità di &quot;Variabili di prodotto&quot; è la cosa più importante per il funzionamento di tale funzionalità senza problemi. Le eVar e le prop regolari non sono sufficienti per consentire l&#39;applicazione automatica di questa stretta di mano tra [!DNL Analytics] e [!DNL Target].

Puoi utilizzare [!DNL Analytics] come origine dati comportamentale per:

* Mediante l&#39;utilizzo dei dati di Analytics, è possibile visualizzare raccomandazioni su un sito retail per la vendita al dettaglio agli utenti di una pagina PDP, in base agli acquisti effettuati da altri utenti della stessa categoria nell&#39;ultimo mese.
* Mediante questo componente, potete visualizzare i contenuti presenti nella schermata iniziale di un sito multimediale per i contenuti più popolari in una particolare categoria che attualmente ha un andamento, in base ai [!DNL Analytics] dati.

## Implementazione in Analytics

Le sezioni seguenti sono utili per implementare questa funzione sul [!DNL Analytics] lato.

### Prerequisiti: configurazione di variabili di prodotto in Analytics

Devi implementare le variabili di prodotto in [!DNL Analytics] con gli attributi necessari per [!DNL Target Recommendations].

Un formato di feed [!DNL Target Recommendations] di esempio fungerà da guida su cui tutti gli attributi devono essere definiti nelle variabili di prodotto. Successivamente, tali valori devono essere &quot;mappati&quot; nell&#39; [!DNL Target] interfaccia utente per i rispettivi valori di [!DNL Target] entità.

>[!NOTE]
>
>Se si tratta di un sito di contenuti, le rispettive parti di contenuto devono essere trattate come &quot;prodotti&quot; e gli attributi associati relativi a tale contenuto (ad esempio: nome autore, data di pubblicazione, titolo contenuto, mese di rilascio, ecc.) devono essere passati come attributi. La granularità del livello di categoria o dei tipi di categoria dovrebbe essere decisa dall&#39;impresa in base ai requisiti del caso d&#39;uso.

Per ulteriori dettagli su come impostare le variabili di prodotto, vedi [prodotti](https://docs.adobe.com/content/help/en/analytics/implementation/vars/page-vars/products.html) nella Guida all&#39;implementazione di *Analytics*. Alcune delle note contenute in tale documentazione richiedono discrezione da parte del team che la sta distribuendo (ad esempio: Categoria). È sempre consigliabile consultare  Adobe prima di eseguire questa attività.

### Considerazioni

[!DNL Analytics] i dati vengono inviati tramite un feed giornaliero. I risultati comportamentali richiederanno fino a 24 ore per essere visualizzati nei risultati delle raccomandazioni sul sito. Come per tutte le impostazioni dei [!DNL Recommendations] criteri, questa origine dati può e deve essere testata.

Per un rapido processo decisionale sull&#39;origine dati da utilizzare, se ci sono molti dati organici generati ogni giorno dagli utenti, e non molta dipendenza richiesta dai dati storici, allora utilizzare una [!DNL Target] mbox come l&#39;origine dati comportamentale può essere una buona misura. In caso di minore disponibilità di dati organici generati di recente, se si desidera eseguire il bank sui [!DNL Analytics] dati, l&#39;utilizzo [!DNL Analytics] come origine dati comportamentale è una buona misura.

### Passaggi per la distribuzione

Presupponendo che tutti i prerequisiti siano stati predisposti, il [!DNL Adobe Target Recommendations] team deve eseguire le seguenti attività:

>[!IMPORTANT]
>
>I passaggi indicati di seguito sono solo a scopo illustrativo. Un membro del [!DNL Recommendations] team deve attualmente eseguire questi passaggi. [Contatta l&#39;Assistenza clienti per ulteriori informazioni.](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)

1. In [!DNL Target], fate clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]** per acquisire il codice [!DNL Target] client.

   ![Codice cliente](/help/c-recommendations/c-algorithms/assets/client-code.png)

1. Acquisisci la tua suite di [!DNL Analytics] rapporti.

   Utilizzate la suite di rapporti del sito [!DNL Analytics] di produzione. Questa è la suite di rapporti che tiene traccia del sito in cui hai [!DNL Recommendations] distribuito.

1. In [!DNL Analytics], fai clic su **[!UICONTROL Admin]** > **[!UICONTROL Data Feeds (Feed di dati)]**.

   ![Configurazione > Feed dati](/help/c-recommendations/c-algorithms/assets/data-feed.png)

1. Click **[!UICONTROL Add]** to create a new feed.

   ![Aggiungi feed](/help/c-recommendations/c-algorithms/assets/add-feed.png)

1. Compila le informazioni sui feed:

   * **Nome**: Feed Recs Prod
   * **Suite** di rapporti: Suite di rapporti predeterminata
   * **E-mail**: Specifica l&#39;indirizzo appropriato per un utente Amministratore
   * **Intervallo** feed: Selezionare l&#39;intervallo desiderato
   * **Elaborazione** ritardata: Nessun ritardo.
   * **Date** di inizio e fine: Alimentazione continua

   ![Sezione Informazioni sui feed](/help/c-recommendations/c-algorithms/assets/feed-information.png)

1. Fill in the details in the **[!UICONTROL Destination]** section:

   >[!NOTE]
   > 
   >Consultate il [!DNL Adobe Analytics] team prima di eseguire questo passaggio.

   * **Tipo**: FTP
   * **Host**: `xxx.yyy.com`
   * **Percorso**: Codice [!DNL Target] client
   * **Nome utente**: Specificare il nome utente
   * **Password**: Specificare la password

   Lo screenshot è solo a scopo di riferimento. La distribuzione avrà credenziali diverse. Consulta il team [!DNL Adobe Analytics] o l&#39;Assistenza clienti durante questo passaggio.

   ![Sezione di destinazione](/help/c-recommendations/c-algorithms/assets/destination.png)

1. Compila le definizioni delle colonne **[!UICONTROL di]** dati:

   * **Formato** di compressione: Gzip
   * **Tipo** di pacchetto:  File singolo
   * **Manifesto:** Fine file

      ![Impostazioni Formato compressione, Tipo di pacchetto e Manifest](/help/c-recommendations/c-algorithms/assets/compression.png)

   * **Colonne** incluse:

      >[!IMPORTANT]
      >
      >Le colonne devono essere aggiunte nello stesso ordine indicato qui. Selezionate le colonne nel seguente ordine e fate clic su **[!UICONTROL Aggiungi]** per ciascuna colonna.

      * hit_time_gmt
      * visid_high
      * visid_low
      * event_list
      * product_list
      * visit_num

1. Fai clic su **[!UICONTROL Salva]**.

   ![Sezione definizioni colonna dati](/help/c-recommendations/c-algorithms/assets/data-column-definitions.png)

Con questo, la configurazione da [!DNL Analytics] lato è completa. Ora è il momento di mappare queste variabili [!DNL Target] sul lato opposto per la fornitura continua di dati comportamentali.

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

