---
description: Durante la creazione di un’attività puoi creare tipi di pubblico per sole attività dal flusso di lavoro guidato in tre passaggi. Questi tipi di pubblico specifici possono essere utilizzati in altre aree della stessa attività, ma non vengono memorizzati nella Libreria pubblico e non possono quindi essere utilizzati in altre attività.
keywords: pubblico;regole pubblico;creare pubblico;creazione di pubblico;solo attività;per una sola attività;ad hoc
seo-description: Create audience di solo attività dall'interno del flusso di lavoro guidato in tre fasi di Adobe Target durante la creazione di un'attività. Questi tipi di pubblico specifici possono essere utilizzati in altre aree della stessa attività, ma non vengono memorizzati nella Libreria pubblico e non possono quindi essere utilizzati in altre attività.
seo-title: Creare un pubblico per sola attività in Adobe Target
solution: Target
title: Creare un pubblico per sola attività
topic: Advanced,Standard,Classic
uuid: 3d0898d0-96e8-4bc9-86bd-3ae39db0e74d
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Creare un pubblico per sola attività{#create-an-activity-only-audience}

Durante la creazione di un’attività puoi creare tipi di pubblico per sole attività dal flusso di lavoro guidato in tre passaggi. These ad hoc audiences can be used in other places within the same activity, but are not stored in the [!UICONTROL Audiences Library] for use in other activities.

I tipi di pubblico per sola attività forniscono i seguenti vantaggi:

* You can use activity-only audiences to create an audience that you want to use only once and you do not want to store it in the [!UICONTROL Audiences Library]. This prevents the [!UICONTROL Audiences Library] from being cluttered with audiences that you never want to use again.
* Activity-only audiences are not visible in the [!UICONTROL Audiences Library]. In tal modo si evita il rischio che possano essere modificate da parte di altri membri della tua organizzazione.

1. While creating an [activity](../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03), on the **[!UICONTROL Target]** page, click the three vertical ellipses, then click **[!UICONTROL Replace Audience]**.

   ![Risultato passaggio](assets/edit_audience.png)

1. On the [!UICONTROL Choose Audience] page, click **[!UICONTROL Activity Only Audience]**.

   ![](assets/activity-only-aud.png)

1. Fai clic su **[!UICONTROL Crea pubblico]**.
1. Inserisci un nome descrittivo per il pubblico.
1. Fai clic su **[!UICONTROL + Aggiungi regola]**.

   Le regole consentono di limitare il pubblico a un sottoinsieme di visitatori del sito.

1. Seleziona un tipo di regola.

   Ogni tipo di regola ha i propri parametri. Consulta [Categorie di pubblico](../c-target/c-audiences/c-target-rules/target-rules.md#concept_E3A77E42F1644503A829B5107B20880D) per ulteriori informazioni su come configurare ogni tipo di regola per la definizione del pubblico.

1. Definisci i parametri della regola.
1. Fai clic su **[!UICONTROL Salva]**.

## Considerazioni

Quando lavori con tipi di pubblico per sola attività, considera quanto segue:

* È possibile creare tipi di pubblico per sola attività nel Compositore esperienza visivo o nel Compositore esperienza basato su moduli. Questa funzionalità sostituisce le regole di perfezionamento delle versioni precedenti di Target.
* You can create an activity to store in the [!UICONTROL Audience Library] for reuse in other activities or you create an activity-only audience. Dopo aver salvato il pubblico, non puoi cambiare tipo di pubblico.
* I perfezionamenti per le attività esistenti vengono trasferiti ai tipi di pubblico per sola attività.
* Activity-only audiences have a status of [!UICONTROL Used] or [!UICONTROL Unused]. I tipi di pubblico per sola attività non utilizzati vengono visualizzate finché l’attività non viene salvata. Se restano inutilizzati e tenti di salvare l’attività, un messaggio di avvertenza ti informa che i tipi di pubblico per sola attività inutilizzati verranno eliminati.
* Puoi visualizzare i dettagli della definizione del pubblico in una scheda a comparsa dal selettore del pubblico, senza aprire il pubblico.
* È possibile [combinare più tipi di pubblico](../c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) per creare un pubblico per sola attività.

