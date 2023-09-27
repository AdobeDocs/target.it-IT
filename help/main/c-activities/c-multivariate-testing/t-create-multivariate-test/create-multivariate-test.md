---
keywords: MVT;test multivariato;creare test multivariato;creazione test multivariato;creare MVT;creazione MVT;come MVT;come test multivariato
description: Scopri come utilizzare il [!UICONTROL Compositore esperienza visivo] (VEC) in [!DNL Adobe Target] per creare un [!UICONTROL Test multivariato] (MVT)
title: Come si crea un [!UICONTROL Test multivariato]?
feature: Multivariate Tests
exl-id: 7712b747-543a-4e19-b689-bea36c44805c
source-git-commit: 7853d8c5934e40d1026e067dfa413f520ecba931
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 63%

---

# Creazione di un test multivariato

Il [!UICONTROL Compositore esperienza visivo] (VEC) in [!DNL Adobe Target] semplifica la creazione di un [!UICONTROL Test multivariato] e per modificare parti della pagina in [!DNL Target].

Il [!DNL Target] l’editor rapido consente di scegliere qualsiasi posizione e di aggiungere più offerte.

Il [!UICONTROL test multivariato] richiede un rapporto di tipo “page-first”. In altre parole, il test viene eseguito su un URL specifico, con l’esperienza progettata per tale pagina.

1. Fate clic su **[!UICONTROL Crea attività]** > **[!UICONTROL Test multivariato]**.

   ![Creare un test multivariato](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/create-multivariate.png)

   >[!NOTE]
   >
   >Per ulteriori informazioni sui vari tipi di attività disponibili in [!DNL Target] e sulle loro differenze, consulta [Attività](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). Consulta [Tipi di attività di Target](/help/main/c-activities/target-activities-guide.md) per aiutarti a stabilire il tipo di attività più adatto per le tue esigenze.

1. (Condizionale) Scegli il tipo di consegna: [!UICONTROL Web], [!UICONTROL Dispositivi mobili], [!UICONTROL E-mail], o [!UICONTROL Altro/API].

1. (Condizionale) Se sei un [Target Premium](/help/main/c-intro/intro.md#premium) cliente, [scegli un’area di lavoro](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. [Specifica l’URL](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/url.md#concept_C12E4A85FF3B4E518E3110F6CF1AF9C0) per la pagina da testare, quindi fai clic su **[!UICONTROL Successivo]**.

   >[!NOTE]
   >
   >Utilizza un URL completo, incluso HTTP o HTTPS all’inizio.

   Se viene visualizzato un messaggio che richiede di abilitare i contenuti misti nel browser, segui le istruzioni incluse nel messaggio. Dopo aver abilitato i contenuti misti nel browser, riparti dal passaggio 1.

   Il [!UICONTROL Compositore esperienza visivo] viene aperto.

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

1. Fai clic su **[!UICONTROL Anteprima]** per [visualizzare l’anteprima delle esperienze](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/preview-experiences.md).

   ![Anteprima esperienze](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/preview-mvt.png)

   Puoi visualizzare ogni esperienza, escludendo quelle da non includere nel test. Per escludere una o più esperienze, seleziona le relative caselle di controllo e fai clic su **[!UICONTROL Escludi]**.

   ![Escludere le esperienze](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/preview-mvt-exclude.png)

1. [Utilizza Il Calcolatore del traffico](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) per verificare la fattibilità del piano di test.

   ![Indicatore del traffico](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt-traffic-indicator.png)

   L’illustrazione seguente indica che l’attività non dispone di traffico sufficiente.

   ![immagine stimatore](assets/estimator.png)

   L’illustrazione seguente indica che l’attività non dispone di traffico sufficiente.

   ![immagine estimator2](assets/estimator2.png)

1. Fai clic su **[!UICONTROL Successivo]** per passare alla pagina [!UICONTROL Targeting.]

1. Scegli il pubblico e la percentuale di visitatori validi che dovranno accedere all’attività.

   ![Pagina Targeting nell’attività MVT](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/mvt_audperc.png)

   Ad esempio, puoi limitare l’accesso al 50% di tutti i visitatori o 45% del pubblico “Californians”.

   >[!NOTE]
   >
   >Oltre a selezionare un pubblico esistente, puoi combinare più tipi di pubblico per creare un pubblico combinato ad hoc anziché crearne uno nuovo. Per ulteriori informazioni, consulta [Combinazione di più tipi di pubblico](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. [Rivedi il riepilogo del test](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/test-summary.md#reference_971AB225963A4DC18EEB5B0E20F0A4A7) e apporta eventuali modifiche, quindi fai clic su **[!UICONTROL Successivo]**.

1. [Specifica obiettivi e impostazioni](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) per il test.

1. Fai clic su **[!UICONTROL Salva e chiudi]** per creare l’attività.

## Video di formazione: Creazione di test multivariati (09:25) ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video illustra come pianificare e creare un test multivariato utilizzando [!DNL Target] flusso di lavoro guidato in tre passaggi.

* Definizione e progettazione di un test multivariato
* Creazione di un test multivariato

>[!VIDEO](https://video.tv.adobe.com/v/17395)
