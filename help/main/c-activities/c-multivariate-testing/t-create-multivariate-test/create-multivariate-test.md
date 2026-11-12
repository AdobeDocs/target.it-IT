---
keywords: MVT;test multivariato;creare test multivariato;creazione test multivariato;creare MVT;creazione MVT;come MVT;come test multivariato
description: Scopri come utilizzare il [!UICONTROL Compositore esperienza visivo] (VEC) in [!DNL Adobe Target] per creare un [!UICONTROL test multivariato] (MVT).
title: Come si crea un [!UICONTROL test multivariato]?
feature: Multivariate Tests
exl-id: 7712b747-543a-4e19-b689-bea36c44805c
TQID: 'https://experienceleague.adobe.com/gxrnY43A7OWsiW48Rlq1Orp7ZxBswdAPZEAbRQrCDZA'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: b934e7cf-c07f-5a64-924b-3c9da8413e3d
    internal-label: Multivariate Tests
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: aad553690f1f399177214c94a2276d038f46d9cb
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 16%
---
# Creazione di un test multivariato {#create-mvt}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come creare un **[!UICONTROL Test multivariato]** (MVT) nel **[!UICONTROL Compositore esperienza visivo]** (VEC). Puoi creare l’attività, generare e rivedere le esperienze, impostare il targeting, quindi configurare obiettivi e impostazioni.

>[!ENDSHADEBOX]

Il **[!UICONTROL Compositore esperienza visivo]** (VEC) in [!DNL Adobe Target] semplifica la creazione di un **[!UICONTROL test multivariato]** e la modifica di parti della pagina in [!DNL Target].

L&#39;editor point-and-click di [!DNL Target] consente di scegliere qualsiasi posizione e di aggiungere più offerte.

Il **[!UICONTROL test multivariato]** (MVT) accetta un report di tipo &quot;page-first&quot;. In altre parole, il test viene eseguito su un URL specifico, con l’esperienza progettata per tale pagina.

Segui i passaggi seguenti per creare un **[!UICONTROL Test multivariato]** (MVT):

1. [Creare l’attività](#create-activity)
1. [Creare e rivedere le esperienze](#build-experiences)
1. [Imposta targeting](#set-targeting)
1. [Configurare obiettivi e impostazioni](#configure-goals-and-settings)

## Creare l’attività {#create-activity}

Scegli il tipo di attività e di consegna, specifica la pagina da testare e assegna un nome all’attività.

1. Fai clic su **[!UICONTROL Crea attività]** > **[!UICONTROL Test multivariato]**.

   Per ulteriori informazioni sui vari tipi di attività disponibili in [!DNL Target] e sulle loro differenze, consulta [Attività](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). Consulta [Tipi di attività di Target](/help/main/c-activities/target-activities-guide.md) per aiutarti a stabilire il tipo di attività più adatto per le tue esigenze.

   ![](../../assets/create-mvt-1.png)

1. Scegli il tipo di consegna: **[!UICONTROL Web]**, **[!UICONTROL Mobile]**, **[!UICONTROL E-mail]** o **[!UICONTROL Altro/API]**.

1. (Condizionale) Se sei un cliente di [Target Premium](/help/main/c-intro/intro.md#premium), [scegli un&#39;area di lavoro](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. [Specificare l&#39;URL](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md#ab-activity-url) per la pagina da verificare. Utilizza un URL completo, incluso HTTP o HTTPS all’inizio.

1. Quindi fare clic su **[!UICONTROL Crea]**. Verrà aperto il **[!UICONTROL Compositore esperienza visivo]**.

1. Per assegnare un nome all&#39;attività, fare clic sull&#39;icona **[!UICONTROL Modifica]** ( ![Modifica icona](/help/main/assets/icons/Edit.svg) ) e specificare un nome descrittivo per l&#39;attività, quindi fare clic su **[!UICONTROL Salva]**.

   {{activity-name-rules}}

   ![](../../assets/create-mvt-2.png)

## Creare e rivedere le esperienze {#build-experiences}

Aggiungi offerte a ciascuna posizione, visualizza in anteprima le esperienze risultanti e verifica che il piano di test sia fattibile.

1. [Crea le offerte in ogni posizione](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/add-offers.md#concept_DCE6B45C30F7419B8EC17AFDEE8D8AA6).

   Puoi aggiungere i seguenti tipi di offerte:

   * HTML
   * Immagine
   * Testo

1. Fai clic su **[!UICONTROL Anteprima]** per [visualizzare l&#39;anteprima delle esperienze](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/preview-experiences.md).

1. Fai clic sull&#39;icona **[!UICONTROL Mostra esperienze]** ( ![Mostra esperienze](/help/main/assets/icons/WebPages.svg) ) per visualizzare l&#39;elenco di tutte le esperienze nel frame a sinistra, quindi fai clic su un&#39;esperienza specifica nell&#39;elenco per visualizzarla.

1. [Utilizza Il Calcolatore del traffico](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) per verificare la fattibilità del piano di test.

### Escludi esperienze (facoltativo) {#exclude-experiences}

Puoi scegliere di escludere un’esperienza che mostra varianti in conflitto tra loro o una esteticamente non equilibrata.

1. Fai clic sull&#39;icona **[!UICONTROL Gestisci contenuto]** ( ![icona Gestisci esperienze](/help/main/assets/icons/Experience.svg) ) per visualizzare la finestra di dialogo **[!UICONTROL Gestisci esperienze]**.

1. Per escludere un&#39;esperienza, fai clic sull&#39;icona **[!UICONTROL Altre azioni]** ( ![Altre azioni](/help/main/assets/icons/MoreSmallList.svg) ) accanto a tale esperienza, quindi fai clic su **[!UICONTROL Escludi]**.

1. Per escludere più esperienze, seleziona le relative caselle di controllo e fai clic su **[!UICONTROL Escludi]**.

## Imposta targeting {#set-targeting}

Scegli quali visitatori inserire nel test e rivedi il riepilogo del test.

1. Fai clic su **[!UICONTROL Avanti]** per accedere alla pagina **[!UICONTROL Targeting]**.

   Il diagramma di flusso ti guida attraverso i passaggi per assegnare un pubblico e la relativa percentuale di traffico, selezionare il metodo di allocazione del traffico e specificare l’allocazione del traffico per ogni esperienza nell’attività.

1. (Condizionale) Fai clic sul controllo **[!UICONTROL Tutti i visitatori]** per selezionare un altro pubblico per l&#39;attività.

   Il pubblico **[!UICONTROL Tutti i visitatori]** è impostato come predefinito. Se selezioni un altro pubblico, il suo nome viene visualizzato nel controllo più a sinistra. Ad esempio, puoi limitare l’accesso al 50% di tutti i visitatori o 45% del pubblico “Californians”.

   +++ Passaggi per selezionare un pubblico diverso

   Viene visualizzato il frame a destra, che consente di aggiungere o eliminare un pubblico e di assegnare la percentuale di visitatori per l’attività.

   1. Per cambiare il pubblico, fai clic sull&#39;icona **[!UICONTROL Sostituisci]** ( ![Sostituisci](/help/main/assets/icons/Retweet.svg) ) nel riquadro a destra.
   1. Nella finestra di dialogo **[!UICONTROL Aggiungi pubblico]**, [seleziona il pubblico desiderato](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md), quindi fai clic su **[!UICONTROL Assegna pubblico]**.

      Per creare un pubblico che combina più tipi di pubblico, fare clic su **[!UICONTROL Combina tipi di pubblico]**. Per ulteriori dettagli, vedere [Combinare più tipi di pubblico](/help/main/c-target/combining-multiple-audiences.md).

      Per creare un nuovo pubblico che non sia già presente nella **[!UICONTROL Libreria pubblico]**, fai clic su **[!UICONTROL Crea pubblico]**. Nel flusso di lavoro [create-audience](/help/main/c-target/c-audiences/audiences.md), scegli una delle seguenti opzioni:

      * **[!UICONTROL Libreria tipi di pubblico]**: crea un pubblico on-demand salvato nella **[!UICONTROL Libreria tipi di pubblico]** e riutilizzabile in altre attività.
      * **[!UICONTROL Solo per questa attività]**: crea un [pubblico specifico per l&#39;attività](/help/main/c-target/creating-activity-only-audience.md) che non viene salvato nella **[!UICONTROL Libreria tipi di pubblico]** e che può essere utilizzato solo nell&#39;attività corrente.

   1. Fai clic su **[!UICONTROL Percentuale visitatori]** nel frame a destra, quindi scegli la percentuale di visitatori idonei che desideri inserire nell&#39;attività.

   +++

1. [Rivedi il riepilogo del test](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/test-summary.md#reference_971AB225963A4DC18EEB5B0E20F0A4A7) e apporta le modifiche desiderate, quindi fai clic su **[!UICONTROL Avanti]**.

## Configurare obiettivi e impostazioni {#configure-goals-and-settings}

Nella pagina **[!UICONTROL Obiettivi e impostazioni]**, indica a [!DNL Target] come misurare il test. Le impostazioni disponibili dipendono dall&#39;utilizzo di [!DNL Target] o [!DNL Analytics] come origine per la generazione di rapporti.

1. Rivedi le sezioni della pagina e imposta ciò che ti serve. Vedi [Impostazioni impostate nella pagina Obiettivi e impostazioni](#goals-settings-overview).


   | Sezione | Impostazioni |
   |---|---|
   | **[!UICONTROL Impostazioni attività]** | Obiettivo facoltativo: **[!UICONTROL Priorità]** (utilizzata quando più attività condividono una posizione e un pubblico) e **[!UICONTROL Durata]** (date di inizio e fine). |
   | **[!UICONTROL Impostazioni reporting]** | L&#39;origine per la generazione di rapporti, la metrica di obiettivo (ad esempio, una metrica di **[!UICONTROL conversione]**), metriche aggiuntive e tipi di pubblico per la generazione dei rapporti. Le impostazioni avanzate per la metrica dell’obiettivo sono disponibili anche qui. |
   | **[!UICONTROL Altri metadati]** | Note sull’attività utili per te o per altri membri del gruppo. |

1. Fai clic su **[!UICONTROL Salva e chiudi]** per creare l&#39;attività.

Per informazioni dettagliate su ogni opzione, vedere [Obiettivi e impostazioni](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#ab-goals-and-settings).

## Video di formazione: Creazione di test multivariati (9:25) ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video illustra come pianificare e creare un test multivariato utilizzando il flusso di lavoro guidato in tre passaggi di [!DNL Target].

* Definizione e progettazione di un test multivariato
* Creazione di un test multivariato

>[!VIDEO](https://video.tv.adobe.com/v/36329?captions=ita)
