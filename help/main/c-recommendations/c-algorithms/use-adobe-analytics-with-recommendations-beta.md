---
keywords: origine dati comportamentali;analisi;consigli;criteri;variabili prodotto
description: Scopri come utilizzare  [!DNL Adobe Analytics] come origine dei dati comportamentali in [!DNL Target Recommendations].
title: Come si utilizza  [!DNL Adobe Analytics] con [!DNL Target Recommendations]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."
feature: Recommendations
hide: true
hidefromtoc: true
source-git-commit: 6d2a313b0e54aa5f6717eee850c79e4092309e7d
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# Usa [!DNL Adobe Analytics] con [!DNL Recommendations]

L&#39;utilizzo di [!DNL Adobe Analytics] come origine dei dati comportamentali consente ai client di utilizzare i dati comportamentali basati sulla visualizzazione e sull&#39;acquisto di [!DNL Analytics] nelle attività di [!DNL Adobe Target Recommendations]. Questa funzione è particolarmente utile nelle situazioni in cui la configurazione di [!DNL Target Recommendations] è nuova e [!DNL Analytics] contiene molti dati storici da utilizzare.

L&#39;utilizzo di [!DNL Analytics] come origine dei dati comportamentali può rappresentare una fonte completa di informazioni sul comportamento degli utenti. Queste informazioni potrebbero includere dati provenienti da un&#39;origine o un feed di terze parti condiviso solo con [!DNL Analytics].

Durante la creazione di [criteri](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md) in [!DNL Recommendations], sono disponibili due pulsanti di scelta che consentono di scegliere l&#39;origine dati da utilizzare: [!UICONTROL mboxes] o [!UICONTROL Analytics]. Per creare un criterio, fare clic su [!UICONTROL Recommendations] > [!UICONTROL Criteria] > [!UICONTROL Create Criteria] > [!UICONTROL Create Criteria]. Per ulteriori informazioni, vedere [Creare i criteri](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md).

>[!NOTE]
>
>Se questi due pulsanti non vengono visualizzati nel tuo account, contatta l&#39;[Assistenza clienti](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

## Casi d&#39;uso per i dati [!DNL Analytics] in [!DNL Target]

L&#39;utilizzo di [!DNL Analytics] come origine dei dati comportamentali per i consigli consente inoltre di distribuire casi d&#39;uso specifici senza la necessità di assegnare tag alle pagine delle entità con tutti i parametri delle entità [!DNL Target]. Anche se questo richiede l’esistenza di alcuni prerequisiti, la disponibilità di &quot;Variabili di prodotto&quot; è la cosa più importante per il corretto funzionamento di tale funzionalità. Le eVar e le proprietà regolari non sono sufficienti per consentire l&#39;esecuzione automatica di questo handshake tra [!DNL Analytics] e [!DNL Target].

È possibile utilizzare [!DNL Analytics] come origine dei dati comportamentali per:

* Visualizzare i suggerimenti su un sito di vendita al dettaglio agli utenti in una pagina dei dettagli di un prodotto, in base agli altri utenti che hanno acquistato dalla stessa categoria nell&#39;ultimo mese, utilizzando i dati di [!DNL Analytics].
* Visualizza contenuto nella schermata iniziale di un sito multimediale per i contenuti più popolari in una particolare categoria che è attualmente in tendenza, in base ai dati di [!DNL Analytics].

## Implementazione in [!DNL Analytics]

Le sezioni seguenti sono utili per implementare questa funzionalità sul lato [!DNL Analytics].

### Prerequisiti: configurare le variabili di prodotto in [!DNL Analytics]

Implementare le variabili di prodotto in [!DNL Analytics] con gli attributi necessari necessari per [!DNL Target Recommendations].

Un formato di feed di esempio [!DNL Target Recommendations] funge da guida su cui tutti gli attributi devono essere definiti nelle variabili di prodotto. Successivamente, tali valori devono essere &quot;mappati&quot; nell&#39;interfaccia utente [!DNL Target] per i rispettivi valori di entità [!DNL Target].

>[!NOTE]
>
>Se si tratta di un sito di contenuti, le rispettive parti di contenuto devono essere trattate come &quot;prodotti&quot; e gli attributi associati a tale contenuto devono essere passati come attributi. Tali attributi possono includere il nome dell’autore, la data di pubblicazione, il titolo del contenuto, il mese di rilascio e così via. La granularità del livello di categoria, o dei tipi di categoria, deve essere decisa dall’azienda in base ai requisiti del caso d’uso.

Per ulteriori dettagli sulla configurazione delle variabili di prodotto, vedi [products](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/products.html) nella *Guida all&#39;implementazione di Adobe Analytics*. Alcune delle note in tale documentazione richiedono discrezione da parte del team che la sta distribuendo (ad esempio: Categoria). È sempre consigliabile consultare [!DNL Adobe] prima di eseguire questa attività.

### Considerazioni

I dati di [!DNL Analytics] vengono inviati tramite un feed giornaliero. I risultati comportamentali possono richiedere fino a 24 ore per essere rispecchiati nei risultati dei consigli sul sito. Come per tutte le impostazioni dei criteri [!DNL Recommendations], questa origine dati può e deve essere testata.

Per un processo decisionale rapido su quale origine dati deve essere utilizzata, se ogni giorno gli utenti generano molti dati organici e non è necessaria una grande dipendenza dai dati storici, l&#39;utilizzo di una mbox [!DNL Target] come origine dati comportamentali può essere una buona soluzione. Nei casi di minore disponibilità di dati organici generati di recente, se desideri basarti sui dati [!DNL Analytics], l&#39;utilizzo di [!DNL Analytics] come origine di dati comportamentali è una buona soluzione.

Ora è il momento di mappare queste variabili sul lato [!DNL Target] per la fornitura continua di dati comportamentali.

## Implementare in [!DNL Target]

1. In [!DNL Target], fare clic su **[!UICONTROL Recommendations]**, quindi sulla scheda **[!UICONTROL Feeds]**.

1. Fare clic su **[!UICONTROL Create Feed]**.

1. Seleziona **[!UICONTROL Analytics Classifications]**, quindi specifica la suite di rapporti.

1. Fare clic su **[!UICONTROL Next]** per passare alle impostazioni di **[!UICONTROL Schedule]** e selezionare un periodo di frequenza per il feed:

   * [!UICONTROL Daily]
   * [!UICONTROL Weekly]
   * [!UICONTROL Every 2 weeks]
   * [!UICONTROL Never]

   Puoi anche selezionare l’ora del giorno in cui il feed deve essere elaborato.

1. Fai clic su **[!UICONTROL Next]** per passare alle impostazioni di **[!UICONTROL Mapping]**, quindi mappa le intestazioni delle colonne di campo ai nomi di campo [!UICONTROL Recommendations] appropriati.

1. Fare clic su **[!UICONTROL Save]**.

## Domande frequenti

Considera le seguenti domande frequenti mentre utilizzi [!DNL Analytics] con [!DNL Target]:

### I valori `entity.id` e `entity.categoryId` devono essere trasmessi entro la chiamata mbox [!DNL Target]?

Sì, questi due valori sono ancora obbligatori. Gli altri attributi possono essere trasmessi tramite un feed [!DNL Analytics], come descritto in questo documento.

### È possibile utilizzare le regole di inclusione dinamica, ad esempio il parametro di entità corrisponde agli attributi del profilo utilizzando l&#39;approccio feed [!DNL Analytics]?

Sì, puoi. Il metodo è simile quando si utilizza [!DNL Target] in modalità autonoma. In questo caso, tuttavia, devi prestare attenzione al fattore temporale. Le variabili di entità che devono corrispondere alle variabili di profilo dipendono dal livello dati che potrebbe apparire molto più tardi sulla pagina.