---
description: Per gli utenti di Personalizzazione automatizzata sono disponibili rapporti specializzati.
keywords: Targeting;rapporti AP;rapporti di personalizzazione automatizzata;rapporto livello attività;rapporto livello offerta;rapporto dettagli offerta
seo-description: Per gli utenti di Personalizzazione automatizzata sono disponibili rapporti specializzati.
seo-title: Rapporto di riepilogo per Personalizzazione automatizzata
solution: Target
title: Rapporto di riepilogo per Personalizzazione automatizzata
title-outputclass: premium
uuid: 959b6814-9686-4741-8a79-5957e64f6209
badge: premium
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# ![PREMIUM](/help/assets/premium.png) Rapporti di riepilogo per Personalizzazione automatizzata{#automated-personalization-summary-reports}

Per gli utenti di Personalizzazione automatizzata sono disponibili rapporti specializzati.

>[!NOTE]
>
>La personalizzazione automatizzata è disponibile come parte della soluzione [!DNL Target Premium]. Non è disponibile in [!DNL Target Standard] senza una licenza [!DNL Target Premium].

1. Fai clic su **[!UICONTROL Attività]**, fai clic sull’attività di [!UICONTROL Personalizzazione automatica] desiderata dall’elenco, quindi fai clic sulla scheda **[!UICONTROL Rapporti]**.

   Se hai numerose attività, puoi filtrare l’elenco selezionando [!UICONTROL Personalizzazione automatizzata] dall’elenco a discesa [!UICONTROL Tipo].

1. (Facoltativo) Fai clic sull&#39;icona [!UICONTROL Scarica] per scaricare il riepilogo (ad esempio, il confronto tra il Controllo e il Traffico mirato) con suddivisione in base a tutte le metriche di successo disponibili.

>[!NOTE]
>
>L’icona [!UICONTROL Impostazioni] non è disponibile per i rapporti di [!UICONTROL Personalizzazione automatizzata].

La funzione [!UICONTROL Personalizzazione automatizzata] fornisce i seguenti rapporti:

## Rapporto a livello di attività {#section_6F72FC5C790B4492B3DCECBFFA971337}

Il rapporto a [!UICONTROL livello di attività] consente di confrontare le prestazioni di aggregazione dell&#39;utilizzo di un algoritmo di [!UICONTROL Personalizzazione automatizzata] per il contenuto fornito in modo casuale (controllo).

![](assets/box_plot_ap.jpg)

Si applicano comunque le regole standard di interpretazione dei risultati per il test A/B, tra cui incremento, affidabilità, trend, durata e così via. Per ulteriori informazioni sull’interpretazione dei risultati, vedi  [Tasso di conversione](../c-reports/conversion-rate.md#concept_2D9FEDE8F94A485DAC86D611BFBDC844).

## Rapporto a livello di offerta {#section_CAA6409879E349C6906E2BE8156D87A1}

Il rapporto a [!UICONTROL livello di offerta] per l’esperienza Foresta casuale confronta le prestazioni di ogni offerta applicata dall’algoritmo alla stessa offerta fornita casualmente (controllo). Pertanto, non devi confrontare le offerte tra loro in questa visualizzazione. Nell&#39;esempio che segue, si può affermare che l&#39;offerta D mostra un incremento del 12,43% quando viene fornita in base alla logica dell’algoritmo (Foresta casuale) invece che casualmente (controllo).

Fai clic sull’algoritmo dell&#39;esperienza (Foresta casuale o Controllo) per visualizzare il rapporto a livello di offerta.

![](assets/ap_OfferLevelRpt.png)

Le offerte possono essere visualizzate all’interno di gruppi di rapporti, che possono essere compressi e espansi. Seleziona [!UICONTROL Gruppo di rapporti] nell’elenco a discesa per visualizzare le informazioni aggregate da gruppi di rapporti, anziché da offerte.

>[!NOTE]
>
>L’icona dell’orologio indica che il modello dell’algoritmo è ancora in corso. L’icona di spunta indica che l’algoritmo di base è stato determinato.

