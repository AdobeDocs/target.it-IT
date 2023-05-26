---
keywords: Panoramica e riferimento
description: Scopri come utilizzare Adobe [!DNL Target] con Adobe Campaign per ottimizzare il contenuto delle e-mail.
title: Come posso integrare [!DNL Target] con Adobe Campaign?
feature: Integrations
exl-id: 605b8fe4-e32f-43bc-9131-245008b655e1
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 41%

---

# Integrare [!DNL Target] con Adobe Campaign

Utilizzare [!DNL Target] con [!DNL Adobe Campaign] per ottimizzare il contenuto delle e-mail.

Per ottimizzare il contenuto delle e-mail, puoi creare un’offerta di reindirizzamento in [!DNL Target], quindi utilizza [!DNL Adobe Campaign] per gestire le offerte e-mail. Ad esempio, puoi visualizzare offerte diverse per destinatari di sesso maschile e femminile.

L’integrazione avviene all’apertura dell’e-mail. Quando il cliente apre l’e-mail, viene effettuata una chiamata a [!DNL Target] e viene visualizzata una versione dinamica del contenuto. Il contenuto è costituito da un’immagine statica supportata da tutti i browser. [!DNL Target] tiene traccia della reazione all’offerta, a livello di pubblico o di sessione, e tali dati sono disponibili nel rapporto di [!DNL Target]

[!DNL Target] può tenere traccia dei seguenti dati:

* Agente utente
* Indirizzo IP
* Posizione geografica
* Segmento associato all’ID del visitatore in [!DNL Target] (previa autorizzazione legale)
* Dati da [!DNL Campaign] Datamart

Ci sono diverse limitazioni:

* Poiché è possibile utilizzare una sola immagine, il contenuto non può essere personalizzato.
* Il tracciamento non è consolidato in [!DNL Adobe Campaign].
* Nessuna esperienza utente unificata.

Usa entrambi [!DNL Target] e [!DNL Campaign] per impostare parti diverse dell&#39;integrazione:

* La casella raw e l’esperienza in [!DNL Target]

>[!NOTE]
>
>Quando utilizzi una rawbox e [!DNL Target], consulta l’importante avviso di sicurezza in [Creare elenchi di Consentiti che specificano gli host autorizzati per l’invio di chiamate mbox a Target](/help/main/administrating-target/hosts.md#allowlist).

* La consegna in [!DNL Campaign]

## Prima di iniziare {#section_FF19BF1BCA064260930BF6C141313B0E}

Prima di usare [!DNL Adobe Campaign] per impostare le offerte e-mail mirate, imposta quanto segue in [!DNL Target]:

* Due o più [!DNL Target] offerte di reindirizzamento

   Consulta [Crea offerta di reindirizzamento](/help/main/c-experiences/c-manage-content/offer-redirect.md).

* A [!DNL Target] con un’esperienza per ogni offerta e il [metrica di successo](/help/main/c-activities/r-success-metrics/success-metrics.md).

   Consulta [Reindirizza all’URL](/help/main/c-experiences/c-visual-experience-composer/redirect-offer.md).

Avvia l’attività in [!DNL Target] prima di configurare [!DNL Campaign] parte dell’integrazione.

## Includi un [!DNL Target] offerta in un [!DNL Adobe Campaign] email {#section_B201BBE27A704E18AF0D553F35695837}

1. Creare un messaggio e-mail in [!DNL Adobe Campaign].
1. In proprietà e-mail, fai clic su **[!UICONTROL Includi]** > **[!UICONTROL Immagine dinamica fornita da Adobe Target]**.
1. Seleziona l’immagine predefinita dalle risorse condivise.
1. Specifica la posizione (rawbox).
1. Aggiungi qualsiasi altro parametro decisionale, ad esempio il genere del destinatario.
1. Visualizza in anteprima l’e-mail, selezionando almeno un destinatario per ogni offerta (in questo caso, un uomo e una donna).
1. In entrata [!DNL Campaign], definisci [!DNL Target] Edge Server utilizzato per controllare l’attività e il nome del tenant.
1. Specifica l’account esterno utilizzato per [!DNL Adobe Experience Cloud] per accedere alle risorse in [!DNL Experience Cloud].

Per ulteriori informazioni, consulta [!DNL Adobe Campaign] documentazione.

## Video: Integrare [!DNL Target] con [!DNL Campaign]

>[!VIDEO](https://video.tv.adobe.com/v/35149)
