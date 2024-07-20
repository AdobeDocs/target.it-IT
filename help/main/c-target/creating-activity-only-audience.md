---
keywords: pubblico;regole pubblico;creare pubblico;creazione di pubblico;solo attività;per una sola attività;ad hoc
description: Scopri come creare tipi di pubblico per sola attività in Adobe [!DNL Target] utilizzabili una tantum.
title: Posso creare un pubblico da utilizzare una sola volta?
feature: Audiences
exl-id: 5fe0507a-75d1-47bc-a941-8c8eeeaf3b75
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 27%

---

# Creare un pubblico per sola attività

Durante la creazione di un&#39;attività puoi creare tipi di pubblico per sola attività dal flusso di lavoro guidato in tre passaggi di [!DNL Adobe Target]. Questi tipi di pubblico specifici possono essere utilizzati in altre aree della stessa attività, ma non vengono memorizzati in [!UICONTROL Audiences Library] per l&#39;utilizzo in altre attività.

I tipi di pubblico per sola attività forniscono i seguenti vantaggi:

* È possibile utilizzare i tipi di pubblico per sola attività per creare un pubblico che si desidera utilizzare una sola volta e non archiviarlo in [!UICONTROL Audiences Library]. I tipi di pubblico per sola attività consentono di evitare che [!UICONTROL Audiences Library] si riempia di tipi di pubblico che non verranno più utilizzati.
* Il pubblico per sola attività non è visibile in [!UICONTROL Audiences Library]. Poiché questi tipi di pubblico non sono visibili nella libreria, sono protetti da modifiche indesiderate da parte di altri utenti dell’organizzazione.

1. Durante la creazione di un&#39;[attività](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03), nella pagina **[!UICONTROL Targeting]** fare clic sui tre puntini di sospensione verticali e quindi su **[!UICONTROL Replace Audience]**.

   ![Risultato passaggio](assets/edit_audience.png)

1. Fare clic su **[!UICONTROL Create Audience]**.

1. Fare clic su **[!UICONTROL This activity only]**.

   ![immagine in modalità solo attività](assets/activity-only-aud.png)

1. Inserisci un nome descrittivo per il pubblico.
1. Trascina e rilascia gli attributi desiderati nel generatore di pubblico.

   Le regole consentono di limitare il pubblico a un sottoinsieme di visitatori del sito. Ogni tipo di regola ha i propri parametri. Consulta [Categorie di pubblico](/help/main/c-target/c-audiences/c-target-rules/target-rules.md#concept_E3A77E42F1644503A829B5107B20880D) per ulteriori informazioni sulla configurazione di ogni tipo di regola per i tipi di pubblico.

1. Fare clic su **[!UICONTROL Done]**.

## Considerazioni

Quando lavori con tipi di pubblico per sola attività, considera quanto segue:

* È possibile creare tipi di pubblico per sola attività nel [!UICONTROL Visual Experience Composer] (VEC) o nel [!UICONTROL Form-Based Experience Composer]. Questa funzionalità sostituisce le regole di ottimizzazione delle versioni precedenti di [!DNL Target].
* È possibile creare un&#39;attività da archiviare in [!UICONTROL Audience Library] per riutilizzarla in altre attività oppure creare un pubblico per sola attività. Dopo aver salvato il pubblico, non puoi cambiare tipo di pubblico.
* I perfezionamenti per le attività esistenti vengono trasferiti ai tipi di pubblico per sola attività.
* I tipi di pubblico per sola attività hanno lo stato [!UICONTROL Used] o [!UICONTROL Unused]. I tipi di pubblico per sola attività non utilizzati vengono visualizzate finché l’attività non viene salvata. Se restano inutilizzati e tenti di salvare l’attività, un messaggio di avvertenza ti informa che i tipi di pubblico per sola attività inutilizzati verranno eliminati.
* Puoi visualizzare i dettagli della definizione del pubblico in una scheda a comparsa dal selettore del pubblico, senza aprire il pubblico.
* È possibile [combinare più tipi di pubblico](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) per creare un pubblico per sola attività.
* I tipi di pubblico per sola attività non supportano le regole di esclusione.

  Per utilizzare le regole di esclusione, puoi utilizzare le seguenti alternative:

   * [Crea e utilizza un pubblico della libreria](/help/main/c-target/c-audiences/create-audience.md) invece di un pubblico per sola attività.
   * [Combina più](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) (fino a 20) tipi di pubblico della libreria in un pubblico per sola attività. Quando si combinano tipi di pubblico, è possibile utilizzare le regole di inclusione ed esclusione nei singoli tipi di pubblico della libreria anche quando il pubblico combinato viene salvato come pubblico per sola attività.
