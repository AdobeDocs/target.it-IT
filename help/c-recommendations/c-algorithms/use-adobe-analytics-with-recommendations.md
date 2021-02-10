---
keywords: origine dati comportamentale;analisi;raccomandazioni;criteri;variabili prodotto
description: Scopri come utilizzare  Adobe Analytics come origine dati comportamentale per utilizzare i dati comportamentali basati sulla visualizzazione e/o sull'acquisto da Analytics in Target Recommendations.
title: Come si utilizza  Adobe Analytics con Target Recommendations?
feature: Recommendations
translation-type: tm+mt
source-git-commit: 87877502d25fe8da830f70126820d1ca825ebc9d
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 0%

---


# Usare  Adobe Analytics con Recommendations

L&#39;utilizzo di [!DNL Adobe Analytics] come origine dati comportamentale consente ai client di utilizzare i dati comportamentali basati sulla vista e/o sull&#39;acquisto di [!DNL Analytics] nelle attività di [!DNL Adobe Target] Recommendations. Questa funzione è particolarmente utile nelle situazioni in cui la configurazione [!DNL Target Recommendations] è nuova e [!DNL Analytics] contiene molti dati storici da sfruttare.

L&#39;utilizzo di [!DNL Analytics] come origine dati comportamentale può fungere da ricca fonte di informazioni sul comportamento degli utenti. Ciò può includere dati da un&#39;origine o feed di terze parti condivisi solo con [!DNL Analytics].

Durante la creazione di [criteri](/help/c-recommendations/c-algorithms/create-new-algorithm.md) in Recommendations, sono disponibili due pulsanti di scelta che consentono di scegliere l&#39;origine dati da utilizzare: [!UICONTROL mbox] o [!UICONTROL Analytics].

![Pulsanti delle origini dati comportamentali](/help/c-recommendations/c-algorithms/assets/behavioral-data-source.png)

>[!NOTE]
>
>Se questi due pulsanti non vengono visualizzati nell&#39;account, contattare l&#39; [Assistenza clienti](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

## Casi di utilizzo per i dati di Analytics in Target

L&#39;utilizzo di [!DNL Analytics] come origine dati comportamentale per le raccomandazioni consente inoltre di distribuire casi d&#39;uso specifici senza il requisito di assegnare tag alle pagine di entità con tutti i parametri di entità [!DNL Target]. Anche se ciò richiede l&#39;implementazione di alcuni prerequisiti, la disponibilità di &quot;Variabili di prodotto&quot; è la cosa più importante per il funzionamento di tale funzionalità senza problemi. Le eVar e le prop regolari non sono sufficienti per consentire l&#39;applicazione automatica di questo handshake tra [!DNL Analytics] e [!DNL Target].

È possibile utilizzare [!DNL Analytics] come origine dati comportamentale per:

* Mediante l&#39;utilizzo dei dati di Analytics, è possibile visualizzare raccomandazioni su un sito retail per la vendita al dettaglio agli utenti di una pagina PDP, in base agli acquisti effettuati da altri utenti della stessa categoria nell&#39;ultimo mese.
* Mediante questo componente, potete visualizzare il contenuto presente nella schermata iniziale di un sito multimediale per individuare il contenuto più popolare in una particolare categoria attualmente in tendenza, in base ai dati [!DNL Analytics].

## Implementazione in Analytics

Le sezioni seguenti sono utili per implementare questa funzionalità sul lato [!DNL Analytics].

### Prerequisiti: configurazione di variabili di prodotto in Analytics

È necessario implementare le variabili di prodotto in [!DNL Analytics] con gli attributi necessari per [!DNL Target Recommendations].

Un formato di feed di esempio [!DNL Target Recommendations] fungerà da guida su cui tutti gli attributi devono essere definiti nelle variabili di prodotto. Successivamente, tali valori devono essere &quot;mappati&quot; nell&#39;interfaccia [!DNL Target] per i rispettivi valori di entità [!DNL Target].

>[!NOTE]
>
>Se si tratta di un sito di contenuti, le rispettive parti di contenuto devono essere trattate come &quot;prodotti&quot; e gli attributi associati relativi a tale contenuto (ad esempio: nome autore, data di pubblicazione, titolo contenuto, mese di rilascio, ecc.) devono essere passati come attributi. La granularità del livello di categoria o dei tipi di categoria dovrebbe essere decisa dall&#39;impresa in base ai requisiti del caso d&#39;uso.

Per ulteriori dettagli su come impostare le variabili di prodotto, vedere [products](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/products.html) nella *Guida all&#39;implementazione di Analytics*. Alcune delle note contenute in tale documentazione richiedono discrezione da parte del team che la sta distribuendo (ad esempio: Categoria). È sempre consigliabile consultare  Adobe prima di eseguire questa attività.

### Considerazioni

[!DNL Analytics] i dati vengono inviati tramite un feed giornaliero. I risultati comportamentali richiederanno fino a 24 ore per essere visualizzati nei risultati delle raccomandazioni sul sito. Come per tutte le impostazioni di criteri [!DNL Recommendations], questa origine dati può e deve essere testata.

Per un rapido processo decisionale sull&#39;origine dati da utilizzare, se ci sono molti dati organici generati ogni giorno dagli utenti, e non molta dipendenza richiesta dai dati storici, allora utilizzare una [!DNL Target] mbox come origine dati comportamentale può essere una buona misura. In caso di minore disponibilità di dati organici generati di recente, se si desidera eseguire il bank su [!DNL Analytics] dati, l&#39;utilizzo di [!DNL Analytics] come origine dati comportamentale è una buona misura.

Ora è il momento di mappare queste variabili sul lato [!DNL Target] per la fornitura continua di dati comportamentali.

## Implementazione in Target

1. In Target, fare clic su **[!UICONTROL Recommendations]**, quindi fare clic sulla scheda **[!UICONTROL Feed]**.

   ![Feed](/help/c-recommendations/c-algorithms/assets/feeds-tab.png)

1. Fare clic su **[!UICONTROL Crea feed]**.

1. Seleziona **[!UICONTROL Analytics Classifications]**, quindi specifica la suite di rapporti.

   ![Classificazioni di Analytics, opzione](/help/c-recommendations/c-algorithms/assets/analytics-classifications.png)

1. Fare clic su **[!UICONTROL Mapping]**, quindi mappare le intestazioni delle colonne dei campi ai nomi dei campi [!UICONTROL Recommendations] appropriati.

   ![Sezione mapping](/help/c-recommendations/c-algorithms/assets/mapping.png)

1. Fai clic su **[!UICONTROL Salva]**.

## Domande frequenti 

Considerate le seguenti domande frequenti durante l&#39;utilizzo di [!DNL Analytics] con [!DNL Target]:

### È necessario trasmettere i valori `entity.id` e `entity.categoryId` all&#39;interno della chiamata mbox [!DNL Target]?

Sì, questi due valori sono ancora obbligatori. Gli altri attributi possono essere passati tramite un feed [!DNL Analytics], come descritto in questo documento.

### Posso utilizzare le regole di inclusione dinamica, come il parametro di entità corrisponde agli attributi di profilo utilizzando l&#39;approccio di feed [!DNL Analytics]?

Sì, puoi. Il metodo è simile se si utilizza [!DNL Target] autonoma. In questo caso, tuttavia, dovete essere attenti al fattore di temporizzazione. Le variabili di entità che dovrebbero corrispondere alle variabili di profilo dipendono dal livello dati che potrebbe essere visualizzato molto più tardi sulla pagina.

