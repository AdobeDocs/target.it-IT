---
keywords: più tipi di pubblico;versioni esperienza;versioni esperienza target
description: Scopri come eseguire il targeting di diversi segmenti di pubblico con versioni della stessa esperienza nelle attività A/B.
title: Posso utilizzare più versioni di esperienza in un'attività A/B?
feature: A/B Tests
exl-id: 7afe36f0-ec46-4d63-bfff-45d2c8923a04
TQID: 'https://experienceleague.adobe.com/FleyH-u5cWI5vku9E4-RMWeIc95WgPy-VQ-eytxka18'
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
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 4876228feee28031373f7e0abe62a66b05b15274
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 8%
---
# Esperienza con più tipi di pubblico un testo A/B {#multiple-experience-audiences}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come eseguire il targeting di tipi di pubblico diversi con versioni della stessa esperienza in un&#39;attività A/B, come illustrato da un caso d&#39;uso con i passaggi da seguire e le best practice.

>[!ENDSHADEBOX]

Nelle attività A/B di [!DNL Adobe Target], è possibile indirizzare le versioni della stessa esperienza a tipi di pubblico diversi. È possibile impostare più tipi di pubblico per un&#39;esperienza nel **[!UICONTROL Compositore esperienza visivo]** o nel Compositore esperienza basato su moduli.

I dati vengono raccolti per l&#39;esperienza indipendentemente dalla versione, pertanto il rapporto mostra le prestazioni dell&#39;esperienza e non di ogni versione. I visitatori possono anche passare da un pubblico all’altro con la modifica del loro profilo. Non sono bloccati nella stessa esperienza per tutta la durata dell’attività.

## Caso d’uso {#use-case}

Stai testando due esperienze:

* un banner con targeting geografico

* un banner generico.

Il banner per ogni area geografica deve essere diverso, ma l’obiettivo del test è determinare se il geotargeting funziona meglio dei contenuti generici.

Se imposti un’esperienza separata per ogni posizione, puoi misurare le prestazioni di ogni area geografica rispetto alle altre. Non puoi misurare se il geotargeting aiuta a raggiungere gli obiettivi di successo rispetto al banner generico.

In questo caso, sono necessarie versioni specifiche per l’area geografica dell’esperienza, in modo da poter testare l’esperienza con targeting geografico rispetto a un controllo non con targeting geografico.

Per impostare le versioni specifiche per le aree geografiche:

1. [Crea un&#39;attività A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) come si farebbe normalmente.

   Quando configuri l’esperienza con più versioni, seleziona il pubblico per ciascuna versione, come descritto nei passaggi seguenti.

1. Seleziona l&#39;esperienza, quindi fai clic su **[!UICONTROL Configura]** > **[!UICONTROL Più tipi di pubblico]**.

1. Nel riquadro **[!UICONTROL Tipi di pubblico per l&#39;esperienza]**, fai clic sull&#39;icona **[!UICONTROL Aggiungi pubblico]** ( ![Icona Aggiungi](/help/main/assets/icons/Add.svg) ), quindi seleziona il primo pubblico a cui desideri rivolgerti. Ripeti per ogni pubblico.

   Se il pubblico non esiste ancora, [crea il pubblico](/help/main/c-target/c-audiences/create-audience.md) e configuralo.

1. Continua a configurare l’attività.

## Best practice {#best-practices}

* Scegli tipi di pubblico reciprocamente esclusivi. Se un visitatore è idoneo per più di un pubblico, viene restituito il contenuto di tutti questi tipi di pubblico e nella pagina viene visualizzato l’ultimo contenuto del pubblico elencato. Questo vale per le attività create nel Compositore esperienza visivo.
* I tipi di pubblico per l’immissione di attività definiti nel diagramma vengono combinati con i tipi di pubblico dell’esperienza utilizzando una condizione AND. Per accedere all’attività, un visitatore deve qualificarsi per il pubblico dell’attività e per uno dei tipi di pubblico dell’esperienza.
* Aggiungi gli stessi tipi di pubblico come segmenti per i rapporti. Questo consente di esaminare i risultati del test al livello elevato dell’esperienza A rispetto a B e al livello inferiore dell’esperienza A rispetto a B solo per &quot;browser lang ja_JP&quot;. Funziona solo per i report basati su [!DNL Target], non per i report basati su [!DNL Analytics].
