---
keywords: A/B;metriche di attività;metriche;configurare metriche;metriche obiettivo;impostazioni attività;metrica successo;conversione;ricavi;coinvolgimento
description: Scopri come impostare le metriche in un’attività A/B, Targeting esperienza o Test multivariato per determinare il successo della visita, tra cui [!UICONTROL Conversione], [!UICONTROL Ricavi] e [!UICONTROL Coinvolgimento].
title: Come si impostano le metriche dell’obiettivo in un’attività A/B?
feature: A/B Tests
exl-id: 9e9e8787-c0cd-4aab-bd2d-0e9591e0a07d
TQID: 'https://experienceleague.adobe.com/WE27AidwrwYLn-ZlnpxKNfOG2jT07iPYztdrovRl0Qk'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ab2570eb-4844-49aa-8334-e91a345525e5
    internal-label: A/B Tests
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: c87804d95464cc31658be23bc7de051c6e1bc12e
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 24%
---
# Impostare le metriche {#ab-set-metrics}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come impostare la metrica obiettivo e le metriche aggiuntive di un&#39;attività A/B, Targeting esperienza (XT) o Test multivariato (MVT) e quali caratteri non sono consentiti nei nomi delle metriche.

>[!ENDSHADEBOX]

Utilizza le metriche in un&#39;attività A/B [!DNL Adobe Target], [!UICONTROL Targeting esperienza] (XT) o [!UICONTROL Test multivariato] (MVT) per determinare quando una visita ha esito positivo. Per informazioni dettagliate sulle metriche di successo, vedi [Metriche di successo](/help/main/c-activities/r-success-metrics/success-metrics.md#overview).

>[!NOTE]
>
>Questa pagina si applica quando [!DNL Adobe Target] è l&#39;origine per la generazione di rapporti. Per le altre origini per la generazione di rapporti, vedere [[!DNL Adobe Analytics] come origine per la generazione di rapporti di [!DNL Target]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) and [[!DNL Target] in [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md).

## Impostare una metrica {#set-a-metric}

1. Nella sezione **[!UICONTROL Impostazioni reporting]** della pagina **[!UICONTROL Obiettivi e impostazioni]**, seleziona una [metrica di successo](/help/main/c-activities/r-success-metrics/success-metrics.md#overview).

   L&#39;opzione **[!UICONTROL Seleziona metriche]** elenca le metriche di successo che è possibile scegliere per l&#39;attività. Le metriche di successo sono suddivise nelle seguenti categorie:

   * **[!UICONTROL Conversione]**
   * **[!UICONTROL Ricavi]**
   * **[!UICONTROL Coinvolgimento]**

   È possibile utilizzare una qualsiasi delle metriche di successo predefinite, o crearne una personalizzata. È inoltre possibile contrassegnare una metrica di successo come metrica principale. Le schede dei rapporti e di Experience Cloud per impostazione predefinita mostrano la metrica primaria, se è stata impostata.

   ![](../../assets/metric-1.png)

1. Specifica le impostazioni per le metriche. Le impostazioni disponibili dipendono dalla metrica di successo in uso.

1. Se attivato, il campo **[!UICONTROL Valore stimato della conversione]** fornisce un valore per l&#39;obiettivo:

   * Il valore consente a [!DNL Target] di calcolare un incremento stimato dei ricavi.
   * Il campo è facoltativo; tuttavia, i ricavi incrementali per qualsiasi metrica non relativa ai ricavi non possono essere calcolati senza di esso.
   * Il campo non è disponibile per le metriche **[!UICONTROL Punteggio di pagina]**.
   * Il tipo di dati è valuta.
   * Il campo viene visualizzato progressivamente dopo che l’utente indica l’azione intrapresa per soddisfare l’obiettivo.

   Consulta [Stima dell’incremento dei ricavi](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md) per maggiori informazioni. La corretta configurazione delle metriche di successo è fondamentale per ottenere i dati previsti.

   ![](../../assets/metric-2.png)

1. (Facoltativo) Per tenere traccia di più metriche dell&#39;obiettivo, fare clic su **[!UICONTROL Aggiungi una nuova metrica]**, quindi selezionare e configurare ogni metrica aggiuntiva come descritto nei passaggi precedenti.

1. Al termine dell&#39;impostazione delle metriche, fare clic su **[!UICONTROL Continua]** in un&#39;attività XT o su **[!UICONTROL Salva e chiudi]** in un&#39;attività MVT.

## Caratteri non consentiti nei nomi delle metriche {#metric-name-rules}

![](../../assets/metric-3.png)

Quando denomini o rinomini una metrica, i seguenti caratteri non sono consentiti:


| Carattere | Descrizione |
|--- |--- |
| `/` | Barra |
| `?` | Punto interrogativo |
| `#` | Cancelletto |
| `:` | Due punti |
| `=` | Uguale |
| `+` | Più |
| `-` | Meno |
| `@` | Chiocciola |
