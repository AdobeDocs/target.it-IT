---
description: Il Compositore esperienza visivo in Target è utile per creare i test direttamente su una pagina abilitata per Target e modificare parti della pagina in Target.
keywords: MVT;test multivariato;creare test multivariato;creazione test multivariato;creare MVT;creazione MVT;come MVT;come test multivariato
seo-description: Il Compositore esperienza visivo in Target è utile per creare i test direttamente su una pagina abilitata per Target e modificare parti della pagina in Target.
seo-title: Creazione di un test multivariato
solution: Target
title: Creazione di un test multivariato
uuid: 876441bd-d841-4974-b1ec-3ad7cb6ef3ee
translation-type: tm+mt
source-git-commit: f689812658d45342f958629d02b74c252c7f0369

---


# Creazione di un test multivariato{#create-a-multivariate-test}

In [!UICONTROL Visual Experience Composer] (Compositore esperienza visivo) in è [!DNL Target] facile creare il test su una pagina compatibile con Target e modificarne una o [!DNL Target]più parti.

L&#39;editor rapido di Target consente di scegliere qualsiasi posizione e di aggiungere offerte multiple.

Il [!UICONTROL test multivariato (MVT)] prende un report sulla pagina. In altre parole, il test viene eseguito su un URL specifico, con l&#39;esperienza progettata per tale pagina.

1. Fai clic su **[!UICONTROL Crea attività]** &gt; **[!UICONTROL Test multivariato]**.

   ![Crea test multivariato](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/create-multivariate.png)

   >[!NOTE]
   >
   >I tipi di attività disponibili dipendono dall’account Target. Alcuni tipi di attività potrebbero non essere visualizzati nell&#39;elenco. Ad esempio [!UICONTROL , Automated Personalization] (Personalizzazione automatizzata) è una [funzione Target Premium](/help/c-intro/intro.md#premium).
   >
   >Per ulteriori informazioni sui vari tipi di attività disponibili [!DNL Target] e sulle relative differenze, vedi [Attività](../../../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). Vedi [Tipi di attività Target](/help/c-activities/target-activities-guide.md) per aiutarti a stabilire quale tipo di attività più suite deve soddisfare le tue esigenze.

1. Selezionate **[!UICONTROL Visual (Elemento visivo) (Predefinito)]**, se necessario.

   ![Finestra di dialogo Crea attività targeting esperienza](/help/c-activities/t-experience-target/t-xt-create/assets/form_url-new.png)

   Se preferisci utilizzare il Compositore esperienza basato su moduli, seleziona [!UICONTROL Modulo]. Per [ulteriori informazioni, consultate Composer](/help/c-experiences/form-experience-composer.md) esperienza basato su modulo.

   >[!NOTE]
   >
   >Oltre a VEC e Experience Composer basato su modulo, Target offre il VEC applicazione singola e il VEC per le app mobili. Per ulteriori informazioni sui vari moduli di composizione, vedi [Esperienze e offerte](/help/c-experiences/experiences.md).
   >
   >Per informazioni sulla risoluzione dei problemi relativi al Compositore esperienza visivo, consulta [Risoluzione dei problemi relativi al Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).
   >
   >L&#39;opzione [!UICONTROL Scegli processo di lavoro] nell&#39;illustrazione precedente è una [funzione Target Premium](/help/c-intro/intro.md) . Se l&#39;opzione non è visualizzata, l&#39;organizzazione dispone di una licenza di Target Standard.]

1. (Condizionale) Se siete clienti Target Premium, [scegliete un&#39;area di lavoro](/help/administrating-target/c-user-management/property-channel/property-channel.md).

1. [Specificate l&#39;URL](../../../c-activities/c-multivariate-testing/t-create-multivariate-test/url.md#concept_C12E4A85FF3B4E518E3110F6CF1AF9C0) della pagina da sottoporre a test, quindi fate clic su **[!UICONTROL Avanti]**.

   >[!NOTE]
   >
   >Utilizza un URL completo, incluso il prefisso HTTP o HTTPS.

   Se viene visualizzato un messaggio che richiede di abilitare i contenuti misti nel browser, segui le istruzioni incluse nel messaggio. Dopo aver abilitato i contenuti misti nel browser, riparti dal passaggio 1.

   Viene visualizzato il Compositore esperienza visivo.

1. Digita un nome per l&#39;attività.

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

1. Fate clic **[!UICONTROL su Anteprima]** per [visualizzare l&#39;anteprima delle esperienze](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/preview-experiences.md).

   ![Anteprima esperienze](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/preview-mvt.png)

   Puoi visualizzare ogni esperienza, escludendo quelle da non includere nel test. Per escludere una o più esperienze, selezionate le caselle di controllo desiderate, quindi fate clic **[!UICONTROL su Exclude]** (Escludi).

   ![Escludi esperienze](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/preview-mvt-exclude.png)

1. [Utilizza Il Calcolatore del traffico](../../../c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) per verificare la fattibilità del piano di test.

   ![Indicatore traffico](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt-traffic-indicator.png)

   L&#39;illustrazione seguente indica che l&#39;attività ha traffico insufficiente.

   ![](assets/estimator.png)

   L&#39;illustrazione seguente indica che l&#39;attività ha traffico insufficiente.

   ![](assets/estimator2.png)

1. Fate clic **[!UICONTROL su Avanti]** per passare alla [!UICONTROL pagina Targeting] .]

1. Scegli il pubblico e la percentuale di visitatori validi che dovranno accedere all’attività.

   ![Pagina Targeting nell&#39;attività MVT](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt_audperc.png)

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
