---
keywords: Experience Targeting;xt;create
description: Utilizza il Compositore esperienza visivo per creare un’attività Targeting esperienza su una pagina abilitata per Target e modificare alcune parti della pagina in Adobe Target.
title: Creare un’attività Targeting esperienze
feature: Experience Targeting
translation-type: tm+mt
source-git-commit: 4adade56529fb95e4400e06d04d3c6c69e120edc
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 100%

---


# Creare un’attività Targeting esperienze{#create-an-experience-targeting-activity}

Utilizza il [!UICONTROL Compositore esperienza visivo] per creare un’attività [!UICONTROL Targeting esperienza] su una pagina abilitata per Target e modificare alcune parti della pagina in [!DNL Adobe Target].

La funzione Targeting esperienza (XT) fornisce contenuti a un pubblico specifico basato su una serie di regole e criteri definiti dagli addetti al marketing.

La funzione Targeting esperienza, che comprende il [geotargeting](/help/c-target/c-audiences/c-target-rules/geo.md), è utile per definire regole che rivolgono un’esperienza o un contenuto specifico a un determinato pubblico. È possibile definire diverse regole in un’attività per fornire diverse varianti di contenuto a tipi di pubblico diversi.

Per ulteriori informazioni su Targeting esperienza, un esempio di utilizzo e video di formazione, consulta [Targeting esperienza](/help/c-activities/t-experience-target/experience-target.md).

**Per creare un’attività Targeting esperienza:**

1. Nell&#39;elenco [!UICONTROL Attività] fai clic su **[!UICONTROL Crea attività]** > **[!UICONTROL Targeting dell&#39;esperienza]**.

   ![Crea attività > Targeting esperienza](/help/c-activities/t-experience-target/t-xt-create/assets/xt_select-1.png)

   >[!NOTE]
   >
   >I tipi di attività disponibili dipendono dall’account Target. Alcuni tipi di attività potrebbero non essere visualizzati nell’elenco. Ad esempio, [!UICONTROL Personalizzazione automatizzata] è una [funzione disponibile in Target Premium](/help/c-intro/intro.md#premium).
   >
   >Per ulteriori informazioni sui vari tipi di attività disponibili in [!DNL Target] e sulle loro differenze, consulta [Attività](/help/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). Consulta [Tipi di attività di Target](/help/c-activities/target-activities-guide.md) per aiutarti a stabilire il tipo di attività più adatto per le tue esigenze.

1. Se necessario, seleziona **[!UICONTROL Visivo (impostazione predefinita)]**.

   ![Finestra di dialogo Crea attività di targeting esperienza](/help/c-activities/t-experience-target/t-xt-create/assets/form_url-new.png)

   Se preferisci utilizzare il Compositore esperienza basato su moduli, seleziona [!UICONTROL Modulo]. Per ulteriori informazioni, consulta [Compositore esperienza basato su moduli](/help/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Oltre al Compositore esperienza visivo e al Compositore esperienza basato su moduli, Target offre anche il Compositore esperienza visivo per applicazione a pagina singola e quello per app mobili. Per ulteriori informazioni sui vari moduli di composizione, consulta [Esperienze e offerte](/help/c-experiences/experiences.md).
   >
   >Per informazioni sulla risoluzione dei problemi relativi al Compositore esperienza visivo, consulta [Risoluzione dei problemi relativi al Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).
   >
   >L’opzione [!UICONTROL Choose Workplace] (Scegli luogo di lavoro) nell’illustrazione precedente è una funzione di [Target Premium](/help/c-intro/intro.md). Se la tua organizzazione dispone di una licenza di Target Standard, questa opzione non è disponibile.

1. (Condizionale) Se sei un cliente Target Premium, [scegli un’area di lavoro](/help/administrating-target/c-user-management/property-channel/property-channel.md).

1. Specifica l’[URL di attività](/help/c-activities/t-experience-target/t-xt-create/xt-activity-url.md#concept_D28549AAA0A14E3BB5F05F32BE8ABC90), quindi fai clic su **[!UICONTROL Successivo]**.

   Se l’account è [configurato con un URL predefinito](/help/administrating-target/visual-experience-composer-set-up.md), questo verrà visualizzato come impostazione predefinita. Se necessario, è possibile passare dall’URL predefinito a un altro.

   Viene aperto il Compositore esperienza visivo, con la pagina specificata nell’URL.

   ![Attività Targeting esperienza nel Compositore esperienza visivo](/help/c-activities/t-experience-target/t-xt-create/assets/xt-in-vec.png)

1. Digita un nome per l’attività nello spazio fornito.

   ![Campo Nome](/help/c-activities/t-experience-target/t-xt-create/assets/xt_name-new.png)

   I seguenti caratteri non sono consentiti nel nome di un’attività:

   | Carattere | Descrizione |
   |--- |--- |
   | `/` | Barra |
   | `?` | Punto interrogativo |
   | `#` | Cancelletto |
   | `:` | Due punti |
   | `=` | Uguale |
   | `+` | Più |
   | `-` | Meno |
   | `@` | Chiocciola |

1. Crea nuove esperienze indirizzate a tipi di pubblico diversi.

   Per istruzioni dettagliate, consulta [Aggiungere un’esperienza](/help/c-activities/t-experience-target/t-xt-create/xt-add-experience.md).

1. Specifica [obiettivi e impostazioni](/help/c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) per l’attività.