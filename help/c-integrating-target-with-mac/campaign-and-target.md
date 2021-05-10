---
keywords: Panoramica e riferimento
description: Scopri come utilizzare Adobe [!DNL Target] con Adobe Campaign per ottimizzare il contenuto delle e-mail.
title: Come posso integrare [!DNL Target] con Adobe Campaign?
feature: Integrazioni
exl-id: 605b8fe4-e32f-43bc-9131-245008b655e1
translation-type: tm+mt
source-git-commit: f3a9ee9827d635d335cb9707d3d92d0de1bd0304
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 37%

---

# Integrare [!DNL Target] con Adobe Campaign

Utilizza [!DNL Target] con [!DNL Adobe Campaign] per ottimizzare il contenuto delle e-mail.

Per ottimizzare il contenuto delle e-mail, puoi creare un’offerta di reindirizzamento in [!DNL Target], quindi utilizzare [!DNL Adobe Campaign] per gestire le offerte e-mail. Ad esempio, puoi visualizzare offerte diverse per i destinatari di sesso maschile e femminile.

L’integrazione avviene all’apertura dell’e-mail. Quando il cliente apre l’e-mail, viene effettuata una chiamata a [!DNL Target] e viene visualizzata una versione dinamica del contenuto. Il contenuto è costituito da un’immagine statica supportata da tutti i browser. [!DNL Target] tiene traccia della reazione all’offerta, a livello di pubblico o di sessione, e tali dati sono disponibili nel rapporto di [!DNL Target]

[!DNL Target] può tenere traccia dei seguenti dati:

* Agente utente
* Indirizzo IP
* Posizione geografica
* Segmento associato all’ID del visitatore in [!DNL Target] (soggetto ad approvazione legale)
* Dati da [!DNL Campaign] Datamart

Ci sono diverse limitazioni:

* Poiché è possibile utilizzare una sola immagine, il contenuto non può essere personalizzato.
* Il tracciamento non è consolidato in [!DNL Adobe Campaign].
* Nessuna esperienza utente unificata.

Utilizza sia [!DNL Target] che [!DNL Campaign] per configurare diverse parti dell&#39;integrazione:

    * La casella non elaborata e l’esperienza in [!DNL Target]
    
    >[!NOTE]
     > 
    >Quando si utilizza una rawbox e [!DNL Target], see the important security notice under [Create allowlists that specify hosts that are authorized to send mbox calls to Target] (/help/administrating-target/hosts.md#inserire nell&#39;elenco Consentiti).
    
    * Consegna in [!DNL Campaign]

## Prima di iniziare {#section_FF19BF1BCA064260930BF6C141313B0E}

Prima di utilizzare [!DNL Adobe Campaign] per impostare le offerte e-mail con targeting, imposta quanto segue in [!DNL Target]:

* Due o più offerte di reindirizzamento [!DNL Target]

   Consulta [Creare un&#39;offerta di reindirizzamento](/help/c-experiences/c-manage-content/offer-redirect.md).

* Un&#39;attività [!DNL Target] con un&#39;esperienza per ogni offerta e la [metrica di successo](/help/c-activities/r-success-metrics/success-metrics.md) desiderata.

   Consulta [Reindirizza all’URL](/help/c-experiences/c-visual-experience-composer/redirect-offer.md).

Avvia l&#39;attività in [!DNL Target] prima di impostare la parte [!DNL Campaign] dell&#39;integrazione.

## Includi un&#39;offerta [!DNL Target] in un messaggio e-mail [!DNL Adobe Campaign] {#section_B201BBE27A704E18AF0D553F35695837}

1. Crea un messaggio e-mail in [!DNL Adobe Campaign].
1. In proprietà e-mail, fai clic su **[!UICONTROL Includi]** > **[!UICONTROL Immagine dinamica fornita da Adobe Target]**.
1. Seleziona l’immagine predefinita dalle risorse condivise.
1. Specifica la posizione (rawbox).
1. Aggiungi qualsiasi altro parametro decisionale, ad esempio il genere del destinatario.
1. Visualizza in anteprima l’e-mail, selezionando almeno un destinatario per ogni offerta (in questo caso, un uomo e una donna).
1. In [!DNL Campaign], definisci il [!DNL Target] server Edge utilizzato per controllare l’attività e il nome del tenant.
1. Specifica l&#39;account esterno utilizzato per [!DNL Adobe Experience Cloud] in modo da poter accedere alle risorse in [!DNL Experience Cloud].

Per ulteriori informazioni, consulta la documentazione [!DNL Adobe Campaign] .

## Video: Integrare [!DNL Target] con [!DNL Campaign]

>[!VIDEO](https://video.tv.adobe.com/v/35149)
