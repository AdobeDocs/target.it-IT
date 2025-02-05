---
keywords: Targeting esperienza;xt;creare
description: Scopri come utilizzare il [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] per creare un'attività [!UICONTROL Experience Targeting] (XT).
title: Come si crea un'attività [!UICONTROL Experience Targeting]?
feature: Experience Targeting
exl-id: fc7fc37f-40bf-4947-a4d0-e51fa09b6c56
source-git-commit: 3a44c05bea24c622292dd0b774f88f0c93be1d88
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 33%

---

# Crea un&#39;attività [!UICONTROL Experience Targeting] (XT)

Utilizzare il Compositore esperienza visivo [!UICONTROL Visual Experience Composer] per creare un&#39;attività [!UICONTROL Experience Targeting] (XT) in una pagina abilitata per [!DNL Target] e modificare parti della pagina in [!DNL Adobe Target].

[!UICONTROL Experience Targeting] (XT) fornisce contenuti a un pubblico specifico in base a una serie di regole e criteri definiti dall&#39;addetto al marketing.

[!UICONTROL Experience Targeting], incluso [il geotargeting](/help/main/c-target/c-audiences/c-target-rules/geo.md), è utile per definire regole che rivolgono un&#39;esperienza o un contenuto specifico a un determinato pubblico. È possibile definire diverse regole in un’attività per fornire diverse varianti di contenuto a tipi di pubblico diversi.

Per ulteriori informazioni su [!UICONTROL Experience Targeting], uno scenario di utilizzo e video di formazione, vedere [Targeting esperienza](/help/main/c-activities/t-experience-target/experience-target.md).

**Per creare un&#39;attività [!UICONTROL Experience Targeting]:**

1. Dall&#39;elenco [!UICONTROL Activities], fare clic su **[!UICONTROL Create Activity]** > **[!UICONTROL Experience Targeting]**.

   >[!NOTE]
   >
   >I tipi di attività disponibili dipendono dall’account [!DNL Target]. Alcuni tipi di attività potrebbero non essere visualizzati nell’elenco. [!UICONTROL Automated Personalization] è una [funzionalità di Target Premium](/help/main/c-intro/intro.md#premium).
   >
   >Per ulteriori informazioni sui vari tipi di attività disponibili in [!DNL Target] e sulle loro differenze, consulta [Attività](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). Consulta [Tipi di attività di Target](/help/main/c-activities/target-activities-guide.md) per aiutarti a stabilire il tipo di attività più adatto per le tue esigenze.

1. Selezionare **[!UICONTROL Visual]**, se necessario.

   Se preferisci utilizzare il [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md), seleziona [!UICONTROL Form].

   >[!NOTE]
   >
   >Oltre al Compositore esperienza visivo e a [!UICONTROL Form-Based Experience Composer], [!DNL Target] offre anche il Compositore esperienza visivo per applicazione a pagina singola. Per ulteriori informazioni sui vari moduli di composizione, consulta [Esperienze e offerte](/help/main/c-experiences/experiences.md).
   >
   >Per informazioni sulla risoluzione dei problemi relativi al Compositore esperienza visivo, vedere [Risoluzione dei problemi relativi al Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Condizionale) Se sei un cliente di [!DNL Target Premium], [scegli un&#39;area di lavoro](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

   L&#39;opzione [!UICONTROL Choose Workplace] è una funzionalità di [Target Premium](/help/main/c-intro/intro.md). Se la tua organizzazione dispone di una licenza di [!DNL Target Standard], questa opzione non è disponibile.

1. Specifica l&#39;[URL attività](/help/main/c-activities/t-experience-target/t-xt-create/xt-activity-url.md#concept_D28549AAA0A14E3BB5F05F32BE8ABC90), quindi fai clic su **[!UICONTROL Create]**.

   Se l’account è [configurato con un URL predefinito](/help/main/administrating-target/visual-experience-composer-set-up.md), questo verrà visualizzato come impostazione predefinita. Se necessario, è possibile passare dall’URL predefinito a un altro.

   Viene aperto il Compositore esperienza visivo, con la pagina specificata nell’URL.

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

1. Crea nuove esperienze indirizzate a tipi di pubblico diversi.

   Per istruzioni dettagliate, consulta [Aggiungere un’esperienza](/help/main/c-activities/t-experience-target/t-xt-create/xt-add-experience.md).

1. Specifica [obiettivi e impostazioni](/help/main/c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) per l’attività.
