---
keywords: pubblico;regole pubblico;creare pubblico;creazione di pubblico;solo attività;per una sola attività;ad hoc
description: Scopri come creare tipi di pubblico per sola attività in Adobe [!DNL Target] per un utilizzo una tantum.
title: Posso creare un pubblico da utilizzare una sola volta?
feature: Audiences
exl-id: 5fe0507a-75d1-47bc-a941-8c8eeeaf3b75
source-git-commit: 974b2093bc9ebc81acb64aa5df0c4c345e52383c
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 55%

---

# Creare un pubblico per sola attività

Creazione di tipi di pubblico per sola attività dall’interno di [!DNL Adobe Target] flusso di lavoro guidato in tre passaggi durante la creazione di un’attività. Questi tipi di pubblico specifici possono essere utilizzati in altre aree della stessa attività, ma non vengono memorizzati nella [!UICONTROL Libreria tipi di pubblico] e non possono quindi essere utilizzati in altre attività.

I tipi di pubblico per sola attività forniscono i seguenti vantaggi:

* È possibile utilizzare i tipi di pubblico per sola attività per creare un pubblico da utilizzare una sola volta, senza archiviarlo nella [!UICONTROL Libreria tipi di pubblico]. I tipi di pubblico per sola attività impediscono la [!UICONTROL Libreria Pubblico] da essere riempiti di tipi di pubblico che non desideri utilizzare mai più.
* I tipi di pubblico per sola attività non sono visibili nella [!UICONTROL Libreria tipi di pubblico]. Poiché questi tipi di pubblico non sono visibili nella libreria, vengono protetti da modifiche indesiderate apportate da altri utenti della tua organizzazione.

1. Durante la creazione di un’ [attività](/help/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03), sul **[!UICONTROL Targeting]** fare clic sui tre puntini di sospensione verticali, quindi fare clic su **[!UICONTROL Sostituisci pubblico]**.

   ![Risultato passaggio](assets/edit_audience.png)

1. Fai clic su **[!UICONTROL Crea pubblico]**.

1. Fai clic su **[!UICONTROL Solo questa attività]**.

   ![](assets/activity-only-aud.png)

1. Inserisci un nome descrittivo per il pubblico.
1. Trascina e rilascia gli attributi desiderati nel generatore di pubblico.

   Le regole consentono di limitare il pubblico a un sottoinsieme di visitatori del sito. Ogni tipo di regola ha i propri parametri. Consulta [Categorie di pubblico](/help/c-target/c-audiences/c-target-rules/target-rules.md#concept_E3A77E42F1644503A829B5107B20880D) per ulteriori informazioni su come configurare ogni tipo di regola per la definizione del pubblico.

1. Fai clic su **[!UICONTROL Fine]**.

## Considerazioni

Quando lavori con tipi di pubblico per sola attività, considera quanto segue:

* Puoi creare tipi di pubblico per sola attività nella [!UICONTROL Compositore esperienza visivo] (Compositore esperienza visivo) o [!UICONTROL Compositore esperienza basato su moduli]. Questa funzionalità sostituisce le regole di perfezionamento delle versioni precedenti di [!DNL Target].
* Puoi creare un pubblico da archiviare nella [!UICONTROL Libreria tipi di pubblico] per riutilizzarlo in altre attività, oppure un pubblico per una sola attività. Dopo aver salvato il pubblico, non puoi cambiare tipo di pubblico.
* I perfezionamenti per le attività esistenti vengono trasferiti ai tipi di pubblico per sola attività.
* I tipi di pubblico per sola attività hanno lo stato [!UICONTROL Utilizzato] o [!UICONTROL Non utilizzato]. I tipi di pubblico per sola attività non utilizzati vengono visualizzate finché l’attività non viene salvata. Se restano inutilizzati e tenti di salvare l’attività, un messaggio di avvertenza ti informa che i tipi di pubblico per sola attività inutilizzati verranno eliminati.
* Puoi visualizzare i dettagli della definizione del pubblico in una scheda a comparsa dal selettore del pubblico, senza aprire il pubblico.
* È possibile [combinare più tipi di pubblico](/help/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) per creare un pubblico per sola attività.
* I tipi di pubblico per sola attività non supportano le regole di esclusione.

   Puoi utilizzare le seguenti alternative per utilizzare le regole di esclusione:

   * [Creare e utilizzare un pubblico della libreria](/help/c-target/c-audiences/create-audience.md) invece di un pubblico per sola attività.
   * [Combinare più](/help/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) (fino a 20) tipi di pubblico della libreria in un pubblico per sola attività. Quando si combinano i tipi di pubblico, è possibile utilizzare regole di inclusione ed esclusione nei singoli tipi di pubblico della libreria anche quando il pubblico combinato viene salvato come pubblico per una sola attività.
