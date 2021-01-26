---
keywords: Overview and Reference
description: Utilizza Target con Adobe Campaign per ottimizzare i contenuti delle e-mail.
title: Integrare Target con Adobe Campaign
feature: Integrations
translation-type: tm+mt
source-git-commit: cf47b7f3625bb1c3430b9fba00c573f489efc448
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 51%

---


# Integrare Target con Adobe Campaign{#integrate-target-with-adobe-campaign}

Utilizzate [!DNL Target] con [!DNL Adobe Campaign] per ottimizzare il contenuto delle e-mail.

Per ottimizzare il contenuto delle e-mail, ad esempio per visualizzare offerte diverse per i destinatari maschi e femmine, potete creare un&#39;offerta di reindirizzamento in [!DNL Target], quindi utilizzare [!DNL Adobe Campaign] per gestire le offerte e-mail.

L’integrazione avviene all’apertura dell’e-mail. Quando il cliente apre l&#39;e-mail, viene effettuata una chiamata a [!DNL Target] e viene visualizzata una versione dinamica del contenuto. Il contenuto è costituito da un’immagine statica supportata da tutti i browser. [!DNL Target] tiene traccia della reazione all’offerta, a livello di pubblico o di sessione, e tali dati sono disponibili nel rapporto di [!DNL Target]

Target può tenere traccia dei seguenti dati:

* Agente utente
* Indirizzo IP
* Posizione geografica
* Segmento associato all’ID del visitatore in Target (soggetto ad approvazione legale)
* Dati da [!DNL Campaign] Datamart

Ci sono diverse limitazioni:

* Poiché è possibile utilizzare una sola immagine, il contenuto non può essere personalizzato.
* Il tracciamento non è consolidato in [!DNL Adobe Campaign].
* Nessuna esperienza utente unificata.

   È necessario utilizzare [!DNL Target] e [!DNL Campaign] per impostare diverse parti dell&#39;integrazione:

   * La rawbox e l’esperienza in [!DNL Target]
   >[!NOTE]
   >
   >Quando utilizzate una rawbox e [!DNL Target], vedete l&#39;importante avviso di sicurezza in [Creare inserire nell&#39;elenco Consentiti  che specificano gli host autorizzati a inviare chiamate mbox a Target](/help/administrating-target/hosts.md#allowlist).

   * La consegna in [!DNL Campaign]



## Prima di iniziare {#section_FF19BF1BCA064260930BF6C141313B0E}

Prima di utilizzare [!DNL Adobe Campaign] per impostare le offerte e-mail di destinazione, impostate quanto segue in [!DNL Target]:

* Due o più offerte di reindirizzamento [!DNL Target]

   Consultate [Creare un&#39;offerta di reindirizzamento](/help/c-experiences/c-manage-content/offer-redirect.md).
* Un’attività di Target con un’esperienza per ogni offerta e la [metrica di successo](/help/c-activities/r-success-metrics/success-metrics.md) desiderata.

   Consulta [Reindirizza all’URL](/help/c-experiences/c-visual-experience-composer/redirect-offer.md).

Avviate l&#39;attività in [!DNL Target] prima di impostare la parte [!DNL Campaign] dell&#39;integrazione.

## Includere un’offerta Target in un’e-mail di Adobe Campaign  {#section_B201BBE27A704E18AF0D553F35695837}

1. Create un&#39;e-mail in [!DNL Adobe Campaign].
1. In proprietà e-mail, fai clic su **[!UICONTROL Includi]** > **[!UICONTROL Immagine dinamica fornita da Adobe Target]**.
1. Seleziona l’immagine predefinita dalle risorse condivise.
1. Specifica la posizione (rawbox).
1. Aggiungi qualsiasi altro parametro decisionale, ad esempio il genere del destinatario.
1. Visualizza in anteprima l’e-mail, selezionando almeno un destinatario per ogni offerta (in questo caso, un uomo e una donna).
1. In [!DNL Campaign], definire il [!DNL Target] server periferico che si sta utilizzando per controllare l&#39;attività e il nome del tenant.
1. Specificate l&#39;account esterno utilizzato per [!DNL Adobe Experience Cloud] in modo da poter accedere alle risorse in [!DNL Experience Cloud].

Per ulteriori informazioni, consultare la documentazione di [!DNL Adobe Campaign].
