---
keywords: registro modifiche attività;registro modifiche
description: Accedere al registro delle modifiche di un'attività in Adobe [!DNL Target] per visualizzare un record di chi ha modificato le attività e quando si sono verificate le modifiche.
title: Come posso visualizzare un registro delle modifiche delle attività?
feature: Activities
exl-id: 72a901c1-4fba-4044-b72b-393cab56b936
TQID: 'https://experienceleague.adobe.com/YmadzVwbj4Hy1bk3Q7a0hp9oZ7-lSgl12ImQaEsiDwU'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: 6efa6b7a-8062-5c41-aef4-b4853cc306ae
    internal-label: Activities
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 8c6f23b495228ab930e6649aa2f9e6dae506cae2
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 10%
---
# Registro delle modifiche apportate alle attività {#change-log}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come visualizzare le azioni eseguite su un&#39;attività, chi le ha eseguite e quando.

>[!ENDSHADEBOX]

Il [!DNL Adobe Target] **[!UICONTROL Registro modifiche]** registra le azioni eseguite su un&#39;attività, inclusi gli elementi modificati, gli autori delle modifiche e il momento in cui si sono verificati. Fornisce una chiara cronologia dell&#39;attività e la pagina **[!UICONTROL Registro modifiche]** viene compilata per ottenere informazioni in tempo reale.

Per accedere alla pagina **[!UICONTROL Registro modifiche]**:

1. Fai clic su **[!UICONTROL Attività]**, quindi sull&#39;attività nell&#39;elenco.
1. Fai clic su **[!UICONTROL Registro modifiche]** nella barra a sinistra.

   Nella pagina sono elencate l’azione eseguita, la data dell’azione e l’utente che l’ha eseguita ogni volta che un’attività viene creata, aggiornata, attivata o disattivata. Vengono inoltre elencate le modifiche apportate alle destinazioni e alle offerte personalizzate utilizzate nell&#39;attività.

   ![Modifica menu registro](assets/change_logs.png)

1. Per elencare le azioni in ordine crescente o decrescente, fare clic sull&#39;intestazione di colonna **[!UICONTROL Data]**.

1. Aggiorna la pagina per visualizzare le modifiche dello stato.

## API del registro di controllo di Target

* [Revisioni: ottiene il registro di controllo in base al nome dell’ultimo autore e a un timestamp dopo modificato](https://developer.adobe.com/target/administer/admin-api/#tag/Revisions){target=_blank}
* [Registro modifiche attività elenco](https://developer.adobe.com/target/administer/admin-api/#tag/Activities/operation/getChangelog){target=_blank}
