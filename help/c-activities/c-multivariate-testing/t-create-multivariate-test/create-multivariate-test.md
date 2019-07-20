---
description: In Visual Experience Composer (Compositore esperienza visivo) in Target è facile creare un test multivariato (MVT) su una pagina compatibile con Target e modificarne una o più parti all'interno di Target.
keywords: MVT;test multivariato;creare test multivariato;creazione test multivariato;creare MVT;creazione MVT;come MVT;come test multivariato
seo-description: In Visual Experience Composer (Compositore esperienza visivo) in Adobe Target è facile creare un test multivariato (MVT) su una pagina compatibile con Target e modificarne una o più parti all'interno di Target.
seo-title: Creazione di un test multivariato
solution: Target
title: Creazione di un test multivariato
uuid: 876441bd-d841-4974-b1ec-3ad7cb6ef3ee
translation-type: tm+mt
source-git-commit: 5dd87afce38e7ff9c763aa65031ec837689d4ae8

---


# Creazione di un test multivariato{#create-a-multivariate-test}

The [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Target] makes it easy to create your test right on a Target-enabled page and to modify portions of the page within [!DNL Target].

L'editor rapido di Target consente di scegliere qualsiasi posizione e di aggiungere offerte multiple.

The [!UICONTROL Multivariate Test] (MVT) takes a page-first report. In altre parole, il test viene eseguito su un URL specifico, con l'esperienza progettata per tale pagina.

1. Fai clic su **[!UICONTROL Crea attività]** &gt; **[!UICONTROL Test multivariato]**.

   ![Crea test multivariato](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/create-multivariate.png)

   >[!NOTE]
   >
   >I tipi di attività disponibili dipendono dall’account Target. Alcuni tipi di attività potrebbero non essere visualizzati nell'elenco. For example, [!UICONTROL Automated Personalization] is a [Target Premium feature](/help/c-intro/intro.md#premium).
   >
   >For more information about the various activity types available in [!DNL Target] and their differences, see [Activities](../../../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). See [Target Activity types](/help/c-activities/target-activities-guide.md) to help you decide which activity type best suites your needs.

1. Select **[!UICONTROL Visual (Default)]**, if necessary.

   ![Crea attività test multivariato, finestra di dialogo](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/create-mvt-dialog.png)

   >[!NOTE]
   >
   >Per informazioni sulla risoluzione dei problemi relativi al Compositore esperienza visivo, consulta [Risoluzione dei problemi relativi al Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).
   >
   >The [!UICONTROL Choose Workplace] option in the preceding illustration is a [Target Premium](/help/c-intro/intro.md) feature. Se l'opzione non è visualizzata, l'organizzazione dispone di una licenza di Target Standard.]

1. (Conditional) If you are a Target Premium customer, [choose a workspace](/help/administrating-target/c-user-management/property-channel/property-channel.md).

1. [Specificate l'URL](../../../c-activities/c-multivariate-testing/t-create-multivariate-test/url.md#concept_C12E4A85FF3B4E518E3110F6CF1AF9C0) della pagina da sottoporre a test, quindi fate clic su **[!UICONTROL Avanti]**.

   >[!NOTE]
   >
   >Utilizza un URL completo, incluso il prefisso HTTP o HTTPS.

   Se viene visualizzato un messaggio che richiede di abilitare i contenuti misti nel browser, segui le istruzioni incluse nel messaggio. Dopo aver abilitato i contenuti misti nel browser, riparti dal passaggio 1.

   Viene visualizzato il Compositore esperienza visivo.

1. Digita un nome per l'attività.

   ![Campo Nome attività](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/activityname.png)

   I seguenti caratteri non sono consentiti nel nome di un’attività:

   | Carattere | Descrizione |
   |--- |--- |
   | / | Barra |
   | ? | Punto interrogativo |
   | # | Cancelletto |
   | : | Due punti |
   | = | Uguale |
   | + | Più |
   | - | Meno |
   | @ | Chiocciola |

1. [Crea le offerte in ogni posizione](../../../c-activities/c-multivariate-testing/t-create-multivariate-test/add-offers.md#concept_DCE6B45C30F7419B8EC17AFDEE8D8AA6).

   ![Modifica testo/HTML, finestra di dialogo](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/editoffers.png)

   Puoi aggiungere i seguenti tipi di offerte:

   * HTML
   * Immagine
   * Testo

1. Click **[!UICONTROL Preview]** to [preview your experiences](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/preview-experiences.md).

   ![Anteprima esperienze](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/preview-mvt.png)

   Puoi visualizzare ogni esperienza, escludendo quelle da non includere nel test. To exclude one or more experiences, select the desired checkboxes, then click **[!UICONTROL Exclude]** .

   ![Escludi esperienze](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/preview-mvt-exclude.png)

1. [Utilizza Il Calcolatore del traffico](../../../c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) per verificare la fattibilità del piano di test.

   ![Indicatore traffico](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt-traffic-indicator.png)

   L'illustrazione seguente indica che l'attività ha traffico insufficiente.

   ![](assets/estimator.png)

   L'illustrazione seguente indica che l'attività ha traffico insufficiente.

   ![](assets/estimator2.png)

1. Click **[!UICONTROL Next]** to advance to the [!UICONTROL Targeting] page.]

1. Scegli il pubblico e la percentuale di visitatori validi che dovranno accedere all’attività.

   ![Pagina Targeting nell'attività MVT](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt_audperc.png)

   Ad esempio, puoi limitare l’accesso al 50% di tutti i visitatori o 45% del pubblico “Californians”.

   >[!NOTE]
   >
   >Oltre a selezionare un pubblico esistente, puoi combinare più tipi di pubblico per creare un pubblico combinato ad hoc anziché crearne uno nuovo. Per ulteriori informazioni, consulta [Combinazione di più tipi di pubblico](../../../c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. [Rivedete il riepilogo del test](../../../c-activities/c-multivariate-testing/t-create-multivariate-test/test-summary.md#reference_971AB225963A4DC18EEB5B0E20F0A4A7) e apportate eventuali modifiche, quindi fate clic su **[!UICONTROL Avanti]**.

1. [Specifica obiettivi e impostazioni](../../../c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) per il test.

1. Fai clic su **[!UICONTROL Salva e chiudi]** per creare l’attività.

## Video di formazione: Creazione di test multivariati (09:25)

In questo video viene illustrato come pianificare e creare un test multivariato utilizzando il flusso di lavoro guidato a tre passaggi di Target.

* Definizione e progettazione di un test multivariato
* Creazione di un test multivariato

>[!VIDEO](https://video.tv.adobe.com/v/17395?captions=ita)
