---
keywords: test modello;modello;stessa esperienza su pagine simili;test template
description: Scopri come utilizzare il Compositore esperienza visivo di Adobe [!DNL Target] per includere la stessa esperienza in più pagine con struttura simile o contenenti gli stessi elementi modello.
title: Posso includere la stessa esperienza in pagine simili?
feature: Experiences and Offers
exl-id: 4ea95794-496c-4eff-96ec-8a9d1f732c4a
TQID: 'https://experienceleague.adobe.com/zk7U6g7gk7XkpWsEFQbwuCm7xbpIb1lCaZefxjn-39g'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: dfc8a233-f2b5-4811-bf63-b4262aebc5a5
    internal-label: Administration and configuration
subfeature_v2:
  - id: ef98a6e0-f26c-4870-9bd4-e6b72e9cc699
    internal-label: Experiences and offers
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 17%
---
# Includere la stessa esperienza in pagine simili {#similar-pages}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come utilizzare le regole di consegna pagine nel [!UICONTROL Compositore esperienza visivo] per includere la stessa esperienza in pagine con una struttura simile.

>[!ENDSHADEBOX]

Un modello di pagina in [!DNL Adobe Target] fornisce una struttura alle pagine. Quando le pagine contengono elementi simili, le varianti in tali elementi di pagina con struttura simile possono essere testate su più pagine o su un intero dominio.

Per funzionare correttamente, questa funzione deve essere utilizzata su pagine con una struttura simile o contenenti elementi modello strutturati allo stesso modo su tutte le pagine.

>[!IMPORTANT]
>
>L’utilizzo di questa funzione per modificare gli elementi su pagine dissimili può causare risultati imprevisti.

Questa funzione può essere utilizzata, ad esempio, per eseguire una delle operazioni seguenti:

* Eseguire un test di una barra di navigazione globale ridisponendo o rimuovendo elementi
* Rimuovere un elemento da tutte le pagine di prodotto che utilizzano un particolare modello di pagina
* Aggiungere un banner a tutte le pagine di prodotto
* Modificare il layout del modello di articolo

## Specificare le pagine per un&#39;esperienza {#specify-pages}

Le pagine in cui viene visualizzata un’esperienza vengono specificate con le regole di consegna pagina. Le regole possono includere pagine specifiche o applicare la modifica in tutto il sito o dominio.

1. Crea o modifica un&#39;attività come descritto in [Attività](/help/main/c-activities/activities.md).

1. Nel [!UICONTROL Compositore esperienza visivo] (VEC), fai clic sull&#39;icona **[!UICONTROL Configura]** ( ![icona Configura](/help/main/assets/icons/Setting.svg) ), quindi seleziona **[!UICONTROL Consegna pagine]**.

   ![Attività](assets/vec_edit_1.png)

1. Fai clic su **[!UICONTROL Aggiungi regola]**, quindi specifica i criteri per le pagine a cui aggiungere l&#39;esperienza.

1. Specifica l&#39;intervallo di pagine: **[!UICONTROL URL]**, **[!UICONTROL Dominio]**, **[!UICONTROL Percorso]**, **[!UICONTROL Frammento hash (#)]** (la parte di un URL che segue il simbolo #), **[!UICONTROL Query]** o **[!UICONTROL Personalizzato]**.

   Per ulteriori informazioni sulla valutazione degli URL da parte di [!DNL Target], vedere [Domande frequenti su destinazioni e pubblico](/help/main/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).

   ![Attività](assets/vec_edit_2.png)

1. Scegli un operatore. L&#39;operatore specifica la correlazione tra gli elementi dopo l&#39;operatore e l&#39;intervallo di pagine.

1. Digita le stringhe che definiscono dove viene aggiunta l&#39;esperienza, ad esempio il dominio o le stringhe contenute nel nome della pagina.

   Ad esempio, se sono selezionati **[!UICONTROL Dominio]** e **[!UICONTROL È (distinzione maiuscole/minuscole)]**, digita il dominio in cui l&#39;esperienza viene aggiunta a tutte le pagine.

   È possibile includere più elementi. Per gli elementi multipli viene utilizzato l’operatore OR, il che significa che ogni singolo elemento nell’elenco può soddisfare la condizione.

1. (Facoltativo) Fai clic su **[!UICONTROL Aggiungi regola]** e ripeti i passaggi da 3 a 6 per inserire criteri aggiuntivi.

   I criteri multipli sono collegati mediante AND (E). [!DNL Target] aggiunge l&#39;esperienza a tutte le pagine che corrispondono ai criteri specificati.

>[!IMPORTANT]
>
>[!DNL Target] non è in grado di controllare le pagine per verificare che siano visualizzate come previsto, pertanto è sempre consigliabile utilizzare questa funzionalità per verificare le pagine interessate prima di renderle pubbliche.

## Casi d’uso {#use-cases}

Le regole del modello possono essere utilizzate in un sito in diversi modi, come mostra il seguente caso d’uso.

### Esegui il rendering della stessa attività in tutto il dominio {#entire-domain}

Le regole di modello possono eseguire il rendering della stessa attività in tutto il dominio, ad esempio:

* Per includere un&#39;intestazione o un piè di pagina globale
* Per includere un banner globale (ad esempio, annunci relativi alla COVID-19)
* Per includere una promozione di spedizione gratuita globale

1. Crea o modifica un&#39;attività come descritto in [Attività](/help/main/c-activities/activities.md).

1. Per specificare il dominio in cui viene visualizzata l&#39;esperienza, nel [!UICONTROL Compositore esperienza visivo] fai clic sull&#39;icona **[!UICONTROL Configura]** ( ![icona Configura](/help/main/assets/icons/Setting.svg) ), quindi seleziona **[!UICONTROL Consegna pagine]**.

1. Fai clic su **[!UICONTROL Aggiungi regola]** > **[!UICONTROL Dominio]**.

1. Dall&#39;elenco a discesa **[!UICONTROL Scegli valutatore]**, seleziona **[!UICONTROL Contiene]**, quindi specifica il dominio.

   ![Attività](assets/vec_edit_3.png)
