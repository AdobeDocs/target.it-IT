---
keywords: Panoramica e riferimento
description: Scopri come utilizzare Adobe [!DNL Target] con Adobe Campaign per ottimizzare il contenuto delle e-mail.
title: Come posso integrare  [!DNL Target]  con Adobe Campaign?
feature: Integrations
exl-id: 605b8fe4-e32f-43bc-9131-245008b655e1
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 32%

---

# Integrare [!DNL Target] con Adobe Campaign

Utilizza [!DNL Target] con [!DNL Adobe Campaign] per ottimizzare il contenuto delle e-mail.

Per ottimizzare il contenuto delle e-mail, puoi creare un&#39;offerta di reindirizzamento in [!DNL Target], quindi utilizzare [!DNL Adobe Campaign] per gestire le offerte e-mail. Ad esempio, puoi visualizzare offerte diverse per destinatari di sesso maschile e femminile.

L’integrazione avviene all’apertura dell’e-mail. Quando il cliente apre l&#39;e-mail, viene effettuata una chiamata a [!DNL Target] e viene visualizzata una versione dinamica del contenuto. Il contenuto è costituito da un’immagine statica supportata da tutti i browser. [!DNL Target] tiene traccia della reazione all&#39;offerta a livello di pubblico o di sessione e i dati sono disponibili nei report [!DNL Target].

[!DNL Target] può tenere traccia dei seguenti dati:

* Agente utente
* Indirizzo IP
* Posizione geografica
* Segmento associato all&#39;ID del visitatore in [!DNL Target] (soggetto ad approvazione legale)
* Dati dal data mart [!DNL Campaign]

Ci sono diverse limitazioni:

* Poiché è possibile utilizzare una sola immagine, il contenuto non può essere personalizzato.
* Il tracciamento non è consolidato in [!DNL Adobe Campaign].
* Nessuna esperienza utente unificata.

Utilizzare sia [!DNL Target] che [!DNL Campaign] per impostare parti diverse dell&#39;integrazione:

* La casella raw e l&#39;esperienza in [!DNL Target]

>[!NOTE]
>
>Quando utilizzi una rawbox e [!DNL Target], consulta l’importante avviso di sicurezza in [Creare elenchi di Consentiti che specificano gli host autorizzati per l’invio di chiamate mbox a Target](/help/main/administrating-target/hosts.md#allowlist).

* La consegna in [!DNL Campaign]

## Prima di iniziare {#section_FF19BF1BCA064260930BF6C141313B0E}

Prima di utilizzare [!DNL Adobe Campaign] per configurare le offerte e-mail mirate, configura quanto segue in [!DNL Target]:

* Due o più offerte di reindirizzamento [!DNL Target]

  Vedi [Crea offerta di reindirizzamento](/help/main/c-experiences/c-manage-content/offer-redirect.md).

* Un&#39;attività [!DNL Target] con un&#39;esperienza per ogni offerta e la [metrica di successo](/help/main/c-activities/r-success-metrics/success-metrics.md) desiderata.

  Consulta [Reindirizza all’URL](/help/main/c-experiences/c-visual-experience-composer/redirect-offer.md).

Avvia l&#39;attività in [!DNL Target] prima di configurare la parte [!DNL Campaign] dell&#39;integrazione.

## Includi un&#39;offerta [!DNL Target] in un&#39;e-mail [!DNL Adobe Campaign] {#section_B201BBE27A704E18AF0D553F35695837}

1. Crea un&#39;e-mail in [!DNL Adobe Campaign].
1. Nelle proprietà e-mail, fai clic su **[!UICONTROL Include]** > **[!UICONTROL Dynamic image served by Adobe Target]**.
1. Seleziona l’immagine predefinita dalle risorse condivise.
1. Specifica la posizione (rawbox).
1. Aggiungi qualsiasi altro parametro decisionale, ad esempio il genere del destinatario.
1. Visualizza in anteprima l’e-mail, selezionando almeno un destinatario per ogni offerta (in questo caso, un uomo e una donna).
1. In [!DNL Campaign], definisci il server Edge [!DNL Target] utilizzato per controllare l&#39;attività e il nome del tenant.
1. Specificare l&#39;account esterno utilizzato per [!DNL Adobe Experience Cloud] per accedere alle risorse in [!DNL Experience Cloud].

Per ulteriori informazioni, consultare la documentazione di [!DNL Adobe Campaign].

## Video: Integrare [!DNL Target] con [!DNL Campaign]

>[!VIDEO](https://video.tv.adobe.com/v/35149)
