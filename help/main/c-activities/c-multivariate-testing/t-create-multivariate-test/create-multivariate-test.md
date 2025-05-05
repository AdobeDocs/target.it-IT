---
keywords: MVT;test multivariato;creare test multivariato;creazione test multivariato;creare MVT;creazione MVT;come MVT;come test multivariato
description: Scopri come utilizzare il [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] per creare un [!UICONTROL Multivariate Test] (MVT).
title: Come si crea [!UICONTROL Multivariate Test]?
feature: Multivariate Tests
exl-id: 7712b747-543a-4e19-b689-bea36c44805c
source-git-commit: be118753eed999ce24d547c90ac9d195cce7e9e9
workflow-type: tm+mt
source-wordcount: '724'
ht-degree: 26%

---

# Creazione di un test multivariato

Il [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] semplifica la creazione di un [!UICONTROL Multivariate Test] e la modifica di parti della pagina in [!DNL Target].

L&#39;editor point-and-click di [!DNL Target] consente di scegliere qualsiasi posizione e di aggiungere più offerte.

[!UICONTROL Multivariate Test] (MVT) accetta un rapporto di tipo &quot;page-first&quot;. In altre parole, il test viene eseguito su un URL specifico, con l’esperienza progettata per tale pagina.

1. Fare clic su **[!UICONTROL Create Activity]** > **[!UICONTROL Multivariate Test]**.

   >[!NOTE]
   >
   >Per ulteriori informazioni sui vari tipi di attività disponibili in [!DNL Target] e sulle loro differenze, consulta [Attività](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). Consulta [Tipi di attività di Target](/help/main/c-activities/target-activities-guide.md) per aiutarti a stabilire il tipo di attività più adatto per le tue esigenze.

1. (Condizionale) Scegliere il tipo di consegna: [!UICONTROL Web], [!UICONTROL Mobile], [!UICONTROL Email] o [!UICONTROL Other/API].

1. (Condizionale) Se sei un cliente di [Target Premium](/help/main/c-intro/intro.md#premium), [scegli un&#39;area di lavoro](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. [Specificare l&#39;URL](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/url.md#concept_C12E4A85FF3B4E518E3110F6CF1AF9C0) per la pagina da verificare, quindi fare clic su **[!UICONTROL Create]**.

   >[!NOTE]
   >
   >Utilizza un URL completo, incluso HTTP o HTTPS all’inizio.

   Se viene visualizzato un messaggio che richiede di abilitare i contenuti misti nel browser, segui le istruzioni incluse nel messaggio. Dopo aver abilitato i contenuti misti nel browser, riparti dal passaggio 1.

   Verrà aperto [!UICONTROL Visual Experience Composer].

1. &#x200B;
   1. Fare clic sull&#39;icona **[!UICONTROL Rename]** ( ![icona Rinomina](/help/main/assets/icons/MoreSmallListVert.svg) ), fare clic su **[!UICONTROL Rename]**, specificare un nome per l&#39;attività, quindi fare clic su **[!UICONTROL Save]**.

   Il nome dell’attività non può iniziare con uno dei seguenti caratteri:

   | Carattere | Descrizione |
   |--- |--- |
   | `=` | Uguale |
   | `+` | Più |
   | `-` | Meno |
   | `@` | Chiocciola |

   Il nome dell’attività non può contenere nessuna delle seguenti sequenze di caratteri:

   | Sequenza di caratteri | Descrizione |
   |--- |--- |
   | ;= | Punto e virgola, uguale a |
   | ;+ | Punto e virgola, segno più |
   | ;- | Punto e virgola, meno |
   | ;@ | Punto e virgola, segno A |
   | ,= | Virgola, uguale a |
   | ,+ | Virgola più |
   | ,- | Virgola meno |
   | ,@ | Virgola, segno A |
   | `[`&quot; | Parentesi quadra aperta, virgolette doppie |
   | &quot;`]` | Virgolette doppie, parentesi quadra chiusa |

1. [Crea le offerte in ogni posizione](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/add-offers.md#concept_DCE6B45C30F7419B8EC17AFDEE8D8AA6).

   Puoi aggiungere i seguenti tipi di offerte:

   * HTML
   * Immagine
   * Testo

1. Fai clic su **[!UICONTROL Preview]** per [visualizzare l&#39;anteprima delle esperienze](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/preview-experiences.md).

1. Fai clic sull&#39;icona **[!UICONTROL Show Experiences]** ( ![icona Mostra esperienze](/help/main/assets/icons/WebPages.svg) ) per visualizzare l&#39;elenco di tutte le esperienze nel frame a sinistra.

1. Fai clic su un’esperienza specifica nell’elenco per visualizzarla.

1. (Condizionale) Per escludere una o più esperienze dall&#39;attività, fare clic sull&#39;icona **[!UICONTROL Manage Content]** ( ![icona Gestisci esperienze](/help/main/assets/icons/Experience.svg) ) per visualizzare la finestra di dialogo [!UICONTROL Manage Experiences].

1. (Condizionale) Nella finestra di dialogo [!UICONTROL Manage Experiences], fai clic sull&#39;icona **[!UICONTROL More Actions]** ( ![Icona Altre azioni](/help/main/assets/icons/MoreSmallList.svg) ) accanto all&#39;esperienza da escludere, quindi fai clic su **[!UICONTROL Exclude]**.

   Puoi scegliere di escludere un’esperienza che mostra varianti in conflitto tra loro o una esteticamente non equilibrata.

1. (Condizionale) Per escludere più esperienze, seleziona le caselle di controllo per le esperienze desiderate, quindi fai clic su **[!UICONTROL Exclude]**.

1. [Utilizza Il Calcolatore del traffico](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) per verificare la fattibilità del piano di test.

1. Fare clic su **[!UICONTROL Next]** per passare alla pagina [!UICONTROL Targeting].

   Il passaggio **Targeting** ha un aspetto familiare se sono stati utilizzati altri tipi di attività [!DNL Target]. Qui puoi selezionare un pubblico e specificare la percentuale di visitatori che visualizzano ogni esperienza.

   Il diagramma di flusso ti guida attraverso i passaggi per assegnare un pubblico e la relativa percentuale di traffico, selezionare il metodo di allocazione del traffico e specificare l’allocazione del traffico per ogni esperienza nell’attività.

1. (Condizionale) Fare clic sul controllo **[!UICONTROL All Visitors]** per selezionare un altro pubblico per l&#39;attività.

   Il pubblico [!UICONTROL All Visitors] è impostato come predefinito. Se selezioni un altro pubblico, il suo nome viene visualizzato nel controllo più a sinistra.

   Viene visualizzato il frame a destra, che consente di aggiungere o eliminare un pubblico e di assegnare la percentuale di visitatori per l’attività.

   1. Per cambiare il pubblico, fai clic sull&#39;icona **[!UICONTROL Replace]** ( ![Icona Sostituisci](/help/main/assets/icons/Retweet.svg) ) nel frame a destra.
   1. Nella finestra di dialogo [!UICONTROL Add Audience], [seleziona il pubblico desiderato](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md), quindi fai clic su **[!UICONTROL Assign Audience]**.

      Puoi fare clic su **Combina tipi di pubblico** per [creare un pubblico che combini più tipi di pubblico](/help/main/c-target/combining-multiple-audiences.md).

      Se devi creare un nuovo pubblico che non sia già presente in [!UICONTROL Audience Library], fai clic su **Crea pubblico**. Durante il flusso di lavoro [create-audience](/help/main/c-target/c-audiences/audiences.md) puoi scegliere tra le seguenti opzioni:

      * **[!UICONTROL Audience Library]**: crea un pubblico su richiesta salvato in [!UICONTROL Audience Library] che può essere riutilizzato in altre attività.
      * **[!UICONTROL This activity only]**: crea un [pubblico specifico per l&#39;attività](/help/main/c-target/creating-activity-only-audience.md) che non è salvato in [!UICONTROL Audience Library] e può essere utilizzato solo nell&#39;attività corrente.

   1. Fai clic su **[!UICONTROL Visitor Percentage]** nel frame a destra, quindi scegli la percentuale di visitatori idonei che dovranno accedere all&#39;attività.

   Ad esempio, puoi limitare l’accesso al 50% di tutti i visitatori o 45% del pubblico “Californians”.

1. [Rivedere il riepilogo del test](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/test-summary.md#reference_971AB225963A4DC18EEB5B0E20F0A4A7) e apportare le modifiche desiderate, quindi fare clic su **[!UICONTROL Next]**.

1. [Specifica obiettivi e impostazioni](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) per il test.

1. Fare clic su **[!UICONTROL Save and Close]** per creare l&#39;attività.

## Video di formazione: Creazione di test multivariati (9:25) ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video illustra come pianificare e creare un test multivariato utilizzando il flusso di lavoro guidato in tre passaggi di [!DNL Target].

* Definizione e progettazione di un test multivariato
* Creazione di un test multivariato

>[!VIDEO](https://video.tv.adobe.com/v/36329?captions=ita)
