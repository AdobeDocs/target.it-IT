---
keywords: Overview and Reference
description: Utilizza Target con Adobe Campaign per ottimizzare i contenuti delle e-mail.
title: Integrare Target con Adobe Campaign
feature: campaign
topic: Standard
uuid: 1a5b70e6-d501-4b52-bec8-4ae2c419d331
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 51%

---


# Integrare Target con Adobe Campaign{#integrate-target-with-adobe-campaign}

Use [!DNL Target] with [!DNL Adobe Campaign] to optimize email content.

To optimize your email content--for example, to display different offers for male and female recipients--you can create a redirect offer in [!DNL Target], then use [!DNL Adobe Campaign] to manage the email offers.

L’integrazione avviene all’apertura dell’e-mail. When the customer opens the email, a call is made to [!DNL Target] and a dynamic version of the content appears. Il contenuto è costituito da un’immagine statica supportata da tutti i browser. [!DNL Target] tiene traccia della reazione all’offerta, a livello di pubblico o di sessione, e tali dati sono disponibili nel rapporto di [!DNL Target]

Target può tenere traccia dei seguenti dati:

* Agente utente
* Indirizzo IP
* Posizione geografica
* Segmento associato all’ID del visitatore in Target (soggetto ad approvazione legale)
* Data from [!DNL Campaign] Datamart

Ci sono diverse limitazioni:

* Poiché è possibile utilizzare una sola immagine, il contenuto non può essere personalizzato.
* Tracking is not consolidated in [!DNL Adobe Campaign].
* Nessuna esperienza utente unificata.

   You must use both [!DNL Target] and [!DNL Campaign] to set up different parts of the integration:

   * La rawbox e l’esperienza in [!DNL Target]
   >[!NOTE]
   >
   >Quando utilizzate una rawbox e [!DNL Target], vedete l&#39;importante informativa sulla sicurezza nella sezione [Crea inserire nell&#39;elenco Consentiti di  che specifica gli host autorizzati a inviare chiamate mbox a Target](/help/administrating-target/hosts.md#allowlist).

   * The delivery in [!DNL Campaign]



## Prima di iniziare {#section_FF19BF1BCA064260930BF6C141313B0E}

Before you use [!DNL Adobe Campaign] to set up your targeted email offers, set up the following in [!DNL Target]:

* Two or more [!DNL Target] redirect offers

   See [Create redirect offer](/help/c-experiences/c-manage-content/offer-redirect.md).
* Un’attività di Target con un’esperienza per ogni offerta e la [metrica di successo](/help/c-activities/r-success-metrics/success-metrics.md) desiderata.

   Consulta [Reindirizza all’URL](/help/c-experiences/c-visual-experience-composer/redirect-offer.md).

Start the activity in [!DNL Target] before setting up the [!DNL Campaign] portion of the integration.

## Includere un’offerta Target in un’e-mail di Adobe Campaign {#section_B201BBE27A704E18AF0D553F35695837}

1. Create an email in [!DNL Adobe Campaign].
1. In proprietà e-mail, fai clic su **[!UICONTROL Includi]** > **[!UICONTROL Immagine dinamica fornita da Adobe Target]**.
1. Seleziona l’immagine predefinita dalle risorse condivise.
1. Specifica la posizione (rawbox).
1. Aggiungi qualsiasi altro parametro decisionale, ad esempio il genere del destinatario.
1. Visualizza in anteprima l’e-mail, selezionando almeno un destinatario per ogni offerta (in questo caso, un uomo e una donna).
1. In [!DNL Campaign], define the [!DNL Target] Edge server you are using to control the activity and the name of the tenant.
1. Specify the external account used for the [!DNL Adobe Experience Cloud] so you can access the resources in the [!DNL Experience Cloud].

For more information, refer to the [!DNL Adobe Campaign] documentation.
