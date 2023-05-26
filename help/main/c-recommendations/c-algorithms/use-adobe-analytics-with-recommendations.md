---
keywords: origine dati comportamentali;analisi;consigli;criteri;variabili prodotto
description: Scopri come utilizzare [!DNL Adobe Analytics] come origine di dati comportamentali per utilizzare i dati comportamentali basati sulla visualizzazione e/o sull’acquisto di [!DNL Analytics] in [!DNL Target Recommendations].
title: Come si utilizza [!DNL Adobe Analytics] con [!DNL Target Recommendations]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: d2b7e840-9546-4a8e-bec4-1ebea5a79672
source-git-commit: bde5506033fbca1577fad1cda1af203702fc4bb3
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 2%

---

# Utilizzare [!DNL Adobe Analytics] con [!DNL Recommendations]

Utilizzo di [!DNL Adobe Analytics] come origine dei dati comportamentali consente ai clienti di utilizzare i dati comportamentali basati sulla visualizzazione e/o sull’acquisto provenienti da [!DNL Analytics] in [!DNL Adobe Target] [!DNL Recommendations] attività. Questa funzione è particolarmente utile quando [!DNL Target Recommendations] la configurazione è nuova e [!DNL Analytics] dispone di molti dati storici da utilizzare.

Utilizzo di [!DNL Analytics] in quanto l’origine dei dati comportamentali può fungere da ricca fonte di informazioni sul comportamento degli utenti. Queste informazioni possono includere dati provenienti da un’origine o un feed di terze parti condivisi solo con [!DNL Analytics].

Mentre [creazione di criteri](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md) in [!DNL Recommendations], sono disponibili due pulsanti di scelta che consentono di scegliere l’origine dati da utilizzare: [!UICONTROL mbox] o [!UICONTROL Analytics]. Per creare un criterio, fai clic su [!UICONTROL Recommendations] > [!UICONTROL Criteri] > [!UICONTROL Crea criterio] > [!UICONTROL Crea criterio]. Per ulteriori informazioni, consulta [Creare i criteri](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md).

![Pulsanti origine dati comportamentali](assets/behavioral-data-source.png)

>[!NOTE]
>
>Se questi due pulsanti non vengono visualizzati nel tuo account, contatta [Assistenza clienti](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

## Casi d’uso per i dati di Analytics in Target

Utilizzo di [!DNL Analytics] come origine di dati comportamentali per i consigli, consente di distribuire casi d’uso specifici senza la necessità di assegnare tag alle pagine delle entità con tutte le [!DNL Target] parametri di entità. Anche se questo richiede l’esistenza di alcuni prerequisiti, la disponibilità di &quot;Variabili di prodotto&quot; è la cosa più importante per il corretto funzionamento di tale funzionalità. Le eVar e le proprietà regolari non sono sufficienti per consentire l’esecuzione automatica di questo handshake tra [!DNL Analytics] e [!DNL Target].

È possibile utilizzare [!DNL Analytics] come origine dei dati comportamentali per:

* Visualizza i consigli agli utenti su un sito di vendita al dettaglio in una pagina di dettagli del prodotto, in base agli acquisti effettuati da altri utenti nella stessa categoria nell’ultimo mese, utilizzando [!DNL Analytics] dati.
* Visualizza contenuto nella schermata iniziale di un sito multimediale per i contenuti più popolari in una particolare categoria attualmente in tendenza, in base a [!DNL Analytics] dati.

## Implementazione in [!DNL Analytics]

Le sezioni seguenti sono utili per implementare questa funzione nel [!DNL Analytics] lato.

### Prerequisiti: configurare le variabili di prodotto in [!DNL Analytics]

Implementare le variabili di prodotto in [!DNL Analytics] con gli attributi necessari richiesti per [!DNL Target Recommendations].

A [!DNL Target Recommendations] il formato feed di esempio funge da guida in cui tutti gli attributi devono essere definiti nelle variabili di prodotto. In seguito, tali valori devono essere &quot;mappati&quot; all’interno del [!DNL Target] Interfaccia utente per il rispettivo [!DNL Target] valori di entità.

>[!NOTE]
>
>Se si tratta di un sito di contenuti, le rispettive parti di contenuto devono essere trattate come &quot;prodotti&quot; e gli attributi associati a tale contenuto devono essere passati come attributi. Tali attributi possono includere il nome dell’autore, la data di pubblicazione, il titolo del contenuto, il mese di rilascio e così via. La granularità del livello di categoria, o dei tipi di categoria, deve essere decisa dall’azienda in base ai requisiti del caso d’uso.

Per ulteriori dettagli su come impostare le variabili di prodotto, consulta [products](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/products.html) nel *Implementare Adobe Analytics* guida. Alcune delle note in tale documentazione richiedono discrezione da parte del team che la sta distribuendo (ad esempio: Categoria). È sempre consigliabile consultare [!DNL Adobe] prima di eseguire questa attività.

### Considerazioni

[!DNL Analytics] I dati vengono inviati tramite un feed giornaliero. I risultati comportamentali possono richiedere fino a 24 ore per essere rispecchiati nei risultati dei consigli sul sito. Come per tutti [!DNL Recommendations] impostazioni dei criteri, questa origine dati può e deve essere testata.

Per un processo decisionale rapido su quale sorgente di dati deve essere utilizzata, se sono presenti molti dati organici generati ogni giorno dagli utenti e non è necessaria una grande dipendenza dai dati storici, utilizzando un’ [!DNL Target] mbox come origine dei dati comportamentali può essere una buona soluzione. Nei casi di minore disponibilità di dati organici generati di recente, se desideri utilizzare [!DNL Analytics] dati, quindi l’ [!DNL Analytics] in quanto l’origine dei dati comportamentali è una buona combinazione.

È ora di mappare queste variabili su [!DNL Target] per la fornitura continua di dati comportamentali.

## Implementare in [!DNL Target]

1. In entrata [!DNL Target], fai clic su **[!UICONTROL Recommendations]**, quindi fare clic su **[!UICONTROL Feed]** scheda.

   ![Feed](/help/main/c-recommendations/c-algorithms/assets/feeds-tab.png)

1. Clic **[!UICONTROL Crea feed]**.

1. Seleziona **[!UICONTROL Classificazioni di Analytics]**, quindi specifica la suite di rapporti.

   ![Opzione Classificazioni di Analytics](/help/main/c-recommendations/c-algorithms/assets/analytics-classifications.png)

1. Clic **[!UICONTROL Successivo]** per passare al **[!UICONTROL Pianificazione]** , seleziona un periodo di frequenza per il feed:

   * [!UICONTROL Giornaliero]
   * [!UICONTROL Settimanale]
   * [!UICONTROL Ogni 2 settimane]
   * [!UICONTROL Mai]

   Puoi anche selezionare l’ora del giorno in cui il feed deve essere elaborato.

1. Clic **[!UICONTROL Successivo]** per passare al  **[!UICONTROL Mappatura]** , quindi mappare le intestazioni di colonna dei campi sulle [!UICONTROL Recommendations] nomi dei campi.

   ![Sezione mappatura](/help/main/c-recommendations/c-algorithms/assets/mapping.png)

1. Fai clic su **[!UICONTROL Salva]**.

## Domande frequenti

Considera le seguenti domande frequenti mentre utilizzi [!DNL Analytics] con [!DNL Target]:

### Sono `entity.id` e `entity.categoryId` valori da trasmettere all&#39;interno del [!DNL Target] Chiamata mbox?

Sì, questi due valori sono ancora obbligatori. Gli altri attributi possono essere trasmessi tramite un [!DNL Analytics] feed, come descritto in questo documento.

### Posso utilizzare regole di inclusione dinamica, come il parametro di entità corrisponde agli attributi di profilo utilizzando [!DNL Analytics] approccio feed?

Sì, puoi. Il metodo è simile quando si utilizza [!DNL Target] autonomo. In questo caso, tuttavia, devi prestare attenzione al fattore temporale. Le variabili di entità che devono corrispondere alle variabili di profilo dipendono dal livello dati che potrebbe apparire molto più tardi sulla pagina.
