---
keywords: pubblico;regole pubblico;creare pubblico;creazione di pubblico;solo attività;per una sola attività;ad hoc
description: Scopri come creare tipi di pubblico per sola attività in Adobe [!DNL Target] utilizzabili una tantum.
title: Posso creare un pubblico da utilizzare una sola volta?
feature: Audiences
exl-id: 5fe0507a-75d1-47bc-a941-8c8eeeaf3b75
TQID: https://experienceleague.adobe.com/IWQT8Lw7uXxY8znUlzOIB-92M2sdjvMj91Ut-gAvZVU
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: adee20bd-51f4-461d-b9db-d215f8756eeb
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 477
ht-degree: 27%

---

# Creare un pubblico per sola attività

Durante la creazione di un&#39;attività puoi creare tipi di pubblico per sola attività dal flusso di lavoro guidato in tre passaggi di [!DNL Adobe Target]. Questi tipi di pubblico specifici possono essere utilizzati in altre aree della stessa attività, ma non vengono memorizzati nella [!UICONTROL Libreria tipi di pubblico] per l&#39;utilizzo in altre attività.

I tipi di pubblico per sola attività forniscono i seguenti vantaggi:

* È possibile utilizzare i tipi di pubblico per sola attività per creare un pubblico da utilizzare una sola volta, senza archiviarlo nella [!UICONTROL Libreria tipi di pubblico]. I tipi di pubblico per sola attività consentono di evitare che la [!UICONTROL Libreria tipi di pubblico] si riempia di tipi di pubblico che non verranno più utilizzati.
* Il pubblico per sola attività non è visibile nella [!UICONTROL Libreria tipi di pubblico]. Poiché questi tipi di pubblico non sono visibili nella libreria, sono protetti da modifiche indesiderate da parte di altri utenti dell’organizzazione.

1. Durante la creazione di un&#39;[attività](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03), nella pagina **[!UICONTROL Targeting]**, fai clic sui tre puntini di sospensione verticali e quindi su **[!UICONTROL Sostituisci pubblico]**.

   ![Risultato passaggio](assets/edit_audience.png)

1. Fai clic su **[!UICONTROL Crea pubblico]**.

1. Fare clic su **[!UICONTROL Solo questa attività]**.

   ![immagine in modalità solo attività](assets/activity-only-aud.png)

1. Inserisci un nome descrittivo per il pubblico.
1. Trascina e rilascia gli attributi desiderati nel generatore di pubblico.

   Le regole consentono di limitare il pubblico a un sottoinsieme di visitatori del sito. Ogni tipo di regola ha i propri parametri. Consulta [Categorie di pubblico](/help/main/c-target/c-audiences/c-target-rules/target-rules.md#concept_E3A77E42F1644503A829B5107B20880D) per ulteriori informazioni sulla configurazione di ogni tipo di regola per i tipi di pubblico.

1. Fai clic su **[!UICONTROL Fine]**.

## Considerazioni

Quando lavori con tipi di pubblico per sola attività, considera quanto segue:

* È possibile creare tipi di pubblico per sola attività nel [!UICONTROL Compositore esperienza visivo] o nel [!UICONTROL Compositore esperienza basato su moduli]. Questa funzionalità sostituisce le regole di ottimizzazione delle versioni precedenti di [!DNL Target].
* È possibile creare un&#39;attività da archiviare nella [!UICONTROL Libreria tipi di pubblico] per riutilizzarla in altre attività oppure creare un pubblico per sola attività. Dopo aver salvato il pubblico, non puoi cambiare tipo di pubblico.
* I perfezionamenti per le attività esistenti vengono trasferiti ai tipi di pubblico per sola attività.
* I tipi di pubblico per sola attività hanno lo stato [!UICONTROL Usato] o [!UICONTROL Non utilizzato]. I tipi di pubblico per sola attività non utilizzati vengono visualizzate finché l’attività non viene salvata. Se restano inutilizzati e tenti di salvare l’attività, un messaggio di avvertenza ti informa che i tipi di pubblico per sola attività inutilizzati verranno eliminati.
* Puoi visualizzare i dettagli della definizione del pubblico in una scheda a comparsa dal selettore del pubblico, senza aprire il pubblico.
* È possibile [combinare più tipi di pubblico](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) per creare un pubblico per sola attività.
* I tipi di pubblico per sola attività non supportano le regole di esclusione.

  Per utilizzare le regole di esclusione, puoi utilizzare le seguenti alternative:

   * [Crea e utilizza un pubblico della libreria](/help/main/c-target/c-audiences/create-audience.md) invece di un pubblico per sola attività.
   * [Combina più](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) (fino a 20) tipi di pubblico della libreria in un pubblico per sola attività. Quando si combinano tipi di pubblico, è possibile utilizzare le regole di inclusione ed esclusione nei singoli tipi di pubblico della libreria anche quando il pubblico combinato viene salvato come pubblico per sola attività.
