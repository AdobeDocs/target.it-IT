---
description: Utilizza Target con Adobe Campaign per ottimizzare i contenuti delle e-mail.
keywords: Panoramica e riferimento
seo-description: Utilizza Target con Adobe Campaign per ottimizzare i contenuti delle e-mail.
seo-title: Integrare Target con Adobe Campaign
solution: Target
title: Integrare Target con Adobe Campaign
topic: Standard
uuid: 1a5b70e6-d501-4b52-bec8-4ae2c419d331
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Integrare Target con Adobe Campaign{#integrate-target-with-adobe-campaign}

Utilizza Target con Adobe Campaign per ottimizzare i contenuti delle e-mail.

Per ottimizzare il contenuto della posta elettronica, ad esempio per presentare offerte diverse a destinatari di genere diverso, è possibile creare un’offerta di reindirizzamento in Target, quindi gestire le offerte di posta elettronica tramite Adobe Campaign.

L’integrazione avviene all’apertura dell’e-mail. Quando il cliente apre l’e-mail, viene effettuata una chiamata a Target e viene visualizzata una versione dinamica del contenuto. Il contenuto è costituito da un’immagine statica supportata da tutti i browser. Target tiene traccia della reazione all’offerta, a livello di pubblico o di sessione, e tali dati sono disponibili nel rapporto di Target.

Target può tenere traccia dei seguenti dati:

* Agente utente
* Indirizzo IP
* Posizione geografica
* Segmento associato all’ID del visitatore in Target (soggetto ad approvazione legale)
* Dati da Campaign Datamart

Ci sono diverse limitazioni:

* Poiché è possibile utilizzare una sola immagine, il contenuto non può essere personalizzato.
* Il tracciamento non è consolidato in Adobe Campaign.
* Nessuna esperienza utente unificata.

   È necessario utilizzare sia Target sia Campaign per impostare parti diverse dell’integrazione:

   * La rawbox e l’esperienza in Target
   * La consegna in Campaign

## Prima di iniziare {#section_FF19BF1BCA064260930BF6C141313B0E}

Prima di utilizzare Adobe Campaign per impostare le offerte e-mail mirate, imposta quanto segue in Target:

* Due o più offerte Target di reindirizzamento

   Consulta [Crea un’offerta di reindirizzamento](https://marketing.adobe.com/resources/help/en_US/target/target/t_offer_redirect.html).
* Un’attività di Target con un’esperienza per ogni offerta e la [metrica di successo](https://marketing.adobe.com/resources/help/en_US/target/target/r_success_metrics.html) desiderata.

   Consulta [Reindirizza all’URL](https://marketing.adobe.com/resources/help/en_US/target/target/t_redirect_offer.html).

Avvia l’attività in Target prima di impostare la parte dell’integrazione in Campaign.

## Includere un’offerta Target in un’e-mail di Adobe Campaign {#section_B201BBE27A704E18AF0D553F35695837}

1. Crea un’e-mail in Adobe Campaign.
1. In proprietà e-mail, fai clic su **[!UICONTROL Includi]** &gt; **[!UICONTROL Immagine dinamica fornita da Adobe Target]**.
1. Seleziona l’immagine predefinita dalle risorse condivise.
1. Specifica la posizione (rawbox).
1. Aggiungi qualsiasi altro parametro decisionale, ad esempio il genere del destinatario.
1. Visualizza in anteprima l’e-mail, selezionando almeno un destinatario per ogni offerta (in questo caso, un uomo e una donna).
1. In Campaign, definisci il server Edge di Target utilizzato per controllare l’attività e il nome del proprietario.
1. Specifica l’account esterno utilizzato per Experience Cloud in modo da poter accedere alle risorse in Experience Cloud.

Per ulteriori informazioni, consulta la documentazione di Adobe Campaign.
