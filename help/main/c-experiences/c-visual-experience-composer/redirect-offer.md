---
keywords: reindirizza;reindirizza url;invia a pagina diversa
description: Scopri come utilizzare l'opzione Reindirizza all'URL in Adobe [!DNL Target] quando desideri inviare il visitatore a una pagina diversa anziché mostrare il contenuto nella stessa pagina.
title: Posso reindirizzare una pagina a un URL diverso?
feature: Visual Experience Composer (VEC)
exl-id: bd448482-0079-4689-aa24-65ecbb31b8ae
TQID: 'https://experienceleague.adobe.com/8Bh5z7SRWw3QqKQMHZck01GKVBtMufwLbw9JxLsSACU'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
subfeature_v2:
  - id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
    internal-label: at.js
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 2%
---
# Reindirizzamento a un URL {#redirect-to-url}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come utilizzare l&#39;opzione **[!UICONTROL Reindirizza all&#39;URL]** per inviare visitatori a una pagina diversa invece di mostrare il contenuto nella stessa pagina.

>[!ENDSHADEBOX]

L&#39;opzione **[!UICONTROL Reindirizza all&#39;URL]** in [!DNL Adobe Target] invia un visitatore a una pagina diversa invece di mostrare il contenuto nella stessa pagina. Si adatta al confronto di due pagine completamente diverse, anziché alle modifiche apportate a parti di contenuto all’interno di una pagina. Un test A/B confronta quindi la pagina A con la pagina B: un’esperienza punta alla pagina predefinita A e l’altra reindirizza alla pagina B.

Un’offerta di reindirizzamento esegue il codice JavaScript che reindirizza il browser. Il codice utilizza il metodo `window.location.replace();`, pertanto la pagina a cui il visitatore è reindirizzato non viene memorizzata nella cronologia del browser. Il visitatore può quindi continuare a utilizzare il pulsante Indietro del browser.

## Creare un’offerta di reindirizzamento {#create-redirect-offer}

L’esperienza che reindirizza definisce la pagina alla quale i visitatori vengono inviati e, facoltativamente, le condizioni del reindirizzamento.

1. Crea un&#39;esperienza.

1. Dal frame **[!UICONTROL Esperienze]**, fai clic sull&#39;icona **[!UICONTROL Altre azioni]** (![Altre azioni](/help/main/assets/icons/MoreSmallList.svg) ) per l&#39;esperienza che reindirizza.

1. Fai clic su **[!UICONTROL Reindirizza all&#39;URL]**.

   ![Icona altre azioni](assets/redirect_1.png)

1. Nella finestra di dialogo **[!UICONTROL Reindirizza all&#39;URL]** immettere l&#39;URL della pagina B.

   ![Icona altre azioni](assets/redirect_2.png)

1. (Facoltativo) Seleziona l’opzione per includere i parametri di query correnti.

   Quando questa opzione è selezionata, tutto ciò che segue `?` nell&#39;URL del visitatore viene aggiunto all&#39;URL di reindirizzamento al momento del reindirizzamento.

## Limitazioni

Le offerte di reindirizzamento presentano le seguenti limitazioni:

* **A4T:** un&#39;offerta di reindirizzamento in un&#39;attività che utilizza A4T richiede un&#39;implementazione che soddisfi determinati requisiti minimi e vengono applicate altre informazioni importanti. Vedi [Offerte di reindirizzamento - Domande frequenti su A4T](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md).
* **Compositore esperienza basato su moduli:** non utilizza un&#39;offerta di reindirizzamento nelle mbox che fanno parte della pagina. Utilizza un&#39;offerta di reindirizzamento solo da un tag script che fa parte di HTML `<head>` e utilizza sempre la creazione automatica e imposta l&#39;offerta di reindirizzamento per la mbox globale.

>[!NOTE]
>
>Per trasmettere il valore referente della pagina di destinazione, utilizza un’offerta HTML invece di un’offerta di reindirizzamento.

## Problemi noti

Le attività di reindirizzamento nelle implementazioni di at.js potrebbero generare la ripetizione ciclica dell’URL di anteprima, con l’offerta consegnata ripetutamente. Utilizza invece la modalità [Controllo qualità](/help/main/c-activities/c-activity-qa/activity-qa.md) per visualizzare in anteprima e testare l&#39;attività. Questo problema non influisce sulla consegna effettiva dell’offerta. (TGT-23019)
