---
keywords: MVT;test multivariato;creare test multivariato;creazione test multivariato;creare MVT;creazione MVT;come MVT;come test multivariato
description: Scopri come utilizzare il [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] per creare un [!UICONTROL Multivariate Test] (MVT).
title: Come si crea [!UICONTROL Multivariate Test]?
feature: Multivariate Tests
exl-id: 7712b747-543a-4e19-b689-bea36c44805c
source-git-commit: 8f9c0ea65197fd639d463628e54db79db993c2da
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 56%

---

# Creazione di un test multivariato

Il [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] semplifica la creazione di un [!UICONTROL Multivariate Test] e la modifica di parti della pagina in [!DNL Target].

L&#39;editor point-and-click di [!DNL Target] consente di scegliere qualsiasi posizione e di aggiungere più offerte.

[!UICONTROL Multivariate Test] (MVT) accetta un rapporto di tipo &quot;page-first&quot;. In altre parole, il test viene eseguito su un URL specifico, con l’esperienza progettata per tale pagina.

1. Fare clic su **[!UICONTROL Create Activity]** > **[!UICONTROL Multivariate Test]**.

   ![Creare un test multivariato](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/create-multivariate.png)

   >[!NOTE]
   >
   >Per ulteriori informazioni sui vari tipi di attività disponibili in [!DNL Target] e sulle loro differenze, consulta [Attività](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). Consulta [Tipi di attività di Target](/help/main/c-activities/target-activities-guide.md) per aiutarti a stabilire il tipo di attività più adatto per le tue esigenze.

1. (Condizionale) Scegliere il tipo di consegna: [!UICONTROL Web], [!UICONTROL Mobile], [!UICONTROL Email] o [!UICONTROL Other/API].

1. (Condizionale) Se sei un cliente di [Target Premium](/help/main/c-intro/intro.md#premium), [scegli un&#39;area di lavoro](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. [Specificare l&#39;URL](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/url.md#concept_C12E4A85FF3B4E518E3110F6CF1AF9C0) per la pagina da verificare, quindi fare clic su **[!UICONTROL Next]**.

   >[!NOTE]
   >
   >Utilizza un URL completo, incluso HTTP o HTTPS all’inizio.

   Se viene visualizzato un messaggio che richiede di abilitare i contenuti misti nel browser, segui le istruzioni incluse nel messaggio. Dopo aver abilitato i contenuti misti nel browser, riparti dal passaggio 1.

   Verrà aperto [!UICONTROL Visual Experience Composer].

1. Digita un nome per l’attività.

   ![Campo Nome attività](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/activityname.png)

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

   ![Finestra di dialogo Modifica testo/HTML](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/editoffers.png)

   Puoi aggiungere i seguenti tipi di offerte:

   * HTML
   * Immagine
   * Testo

1. Fai clic su **[!UICONTROL Preview]** per [visualizzare l&#39;anteprima delle esperienze](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/preview-experiences.md).

   ![Anteprima esperienze](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/preview-mvt.png)

   Puoi visualizzare ogni esperienza, escludendo quelle da non includere nel test. Per escludere una o più esperienze, selezionare le caselle di controllo desiderate, quindi fare clic su **[!UICONTROL Exclude]**.

   ![Escludere le esperienze](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/preview-mvt-exclude.png)

1. [Utilizza Il Calcolatore del traffico](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) per verificare la fattibilità del piano di test.

   ![Indicatore del traffico](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt-traffic-indicator.png)

   L’illustrazione seguente indica che l’attività non dispone di traffico sufficiente.

   ![immagine stimatore](assets/estimator.png)

   L’illustrazione seguente indica che l’attività non dispone di traffico sufficiente.

   ![immagine stimator2](assets/estimator2.png)

1. Fare clic su **[!UICONTROL Next]** per passare alla pagina [!UICONTROL Targeting].

1. Scegli il pubblico e la percentuale di visitatori validi che dovranno accedere all’attività.

   ![Pagina Targeting nell’attività MVT](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt_audperc.png)

   Ad esempio, puoi limitare l’accesso al 50% di tutti i visitatori o 45% del pubblico “Californians”.

   >[!NOTE]
   >
   >Oltre a selezionare un pubblico esistente, puoi combinare più tipi di pubblico per creare un pubblico combinato ad hoc anziché crearne uno nuovo. Per ulteriori informazioni, consulta [Combinazione di più tipi di pubblico](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. [Rivedere il riepilogo del test](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/test-summary.md#reference_971AB225963A4DC18EEB5B0E20F0A4A7) e apportare le modifiche desiderate, quindi fare clic su **[!UICONTROL Next]**.

1. [Specifica obiettivi e impostazioni](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) per il test.

1. Fare clic su **[!UICONTROL Save and Close]** per creare l&#39;attività.

## Video di formazione: Creazione di test multivariati (9:25) ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video illustra come pianificare e creare un test multivariato utilizzando il flusso di lavoro guidato in tre passaggi di [!DNL Target].

* Definizione e progettazione di un test multivariato
* Creazione di un test multivariato

>[!VIDEO](https://video.tv.adobe.com/v/36329?captions=ita)
