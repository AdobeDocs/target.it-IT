---
keywords: Targeting esperienza;xt;creare
description: Scopri come utilizzare il [!UICONTROL Compositore esperienza visivo] (VEC) in [!DNL Adobe Target] per creare un [!UICONTROL Targeting esperienza] (XT) attività.
title: Come si crea un [!UICONTROL Targeting esperienza] Attività?
feature: Experience Targeting
exl-id: fc7fc37f-40bf-4947-a4d0-e51fa09b6c56
source-git-commit: 4faafcef38d02674072d8b20ae03d3e2ef2115d6
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 51%

---

# Creare un [!UICONTROL Targeting esperienza] Attività (XT)

Utilizza il [!UICONTROL Compositore esperienza visivo] (VEC) per creare un’ [!UICONTROL Targeting esperienza] (XT) attività su un [!DNL Target]e per modificare parti della pagina in [!DNL Adobe Target].

La funzione [!UICONTROL Targeting dell’esperienza] (XT) fornisce contenuti a un pubblico specifico in base a una serie di regole e criteri definiti dall’esperto marketing.

La funzione Targeting esperienza, che comprende il [geotargeting](/help/main/c-target/c-audiences/c-target-rules/geo.md), è utile per definire regole che rivolgono un’esperienza o un contenuto specifico a un determinato pubblico. È possibile definire diverse regole in un’attività per fornire diverse varianti di contenuto a tipi di pubblico diversi.

Per ulteriori informazioni su [!UICONTROL Targeting esperienza], uno scenario di utilizzo e video di formazione, consulta [Targeting esperienza](/help/main/c-activities/t-experience-target/experience-target.md).

**Per creare un [!UICONTROL Targeting esperienza] attività:**

1. Nell&#39;elenco [!UICONTROL Attività] fai clic su **[!UICONTROL Crea attività]** > **[!UICONTROL Targeting dell&#39;esperienza]**.

   ![Crea attività > Targeting esperienza](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_select-1.png)

   >[!NOTE]
   >
   >I tipi di attività disponibili dipendono dall’account [!DNL Target]. Alcuni tipi di attività potrebbero non essere visualizzati nell’elenco. Ad esempio, [!UICONTROL Personalizzazione automatizzata] è una [funzione disponibile in Target Premium](/help/main/c-intro/intro.md#premium).
   >
   >Per ulteriori informazioni sui vari tipi di attività disponibili in [!DNL Target] e sulle loro differenze, consulta [Attività](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). Consulta [Tipi di attività di Target](/help/main/c-activities/target-activities-guide.md) per aiutarti a stabilire il tipo di attività più adatto per le tue esigenze.

1. Se necessario, seleziona **[!UICONTROL Visivo (impostazione predefinita)]**.

   Se preferisce utilizzare il [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md), seleziona [!UICONTROL Modulo].

   >[!NOTE]
   >
   >Oltre al Compositore esperienza visivo e [!UICONTROL Compositore esperienza basato su moduli], [!DNL Target] offre il Compositore esperienza visivo per applicazione a pagina singola. Per ulteriori informazioni sui vari moduli di composizione, consulta [Esperienze e offerte](/help/main/c-experiences/experiences.md).
   >
   >Per informazioni sulla risoluzione dei problemi relativi al Compositore esperienza visivo, consulta [Risoluzione dei problemi relativi al Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Condizionale) Se sei un [!DNL Target Premium] cliente, [scegli un’area di lavoro](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

   Il [!UICONTROL Scegli area di lavoro] l&#39;opzione è [Target Premium](/help/main/c-intro/intro.md) funzionalità. Se la tua organizzazione dispone di [!DNL Target Standard] se questa opzione non è disponibile.

1. Specifica l’[URL di attività](/help/main/c-activities/t-experience-target/t-xt-create/xt-activity-url.md#concept_D28549AAA0A14E3BB5F05F32BE8ABC90), quindi fai clic su **[!UICONTROL Crea]**.

   Se l’account è [configurato con un URL predefinito](/help/main/administrating-target/visual-experience-composer-set-up.md), questo verrà visualizzato come impostazione predefinita. Se necessario, è possibile passare dall’URL predefinito a un altro.

   Viene aperto il Compositore esperienza visivo, con la pagina specificata nell’URL.

   ![Attività Targeting esperienza nel Compositore esperienza visivo](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt-in-vec.png)

1. Digita un nome per l’attività nello spazio fornito.

   ![Campo Nome](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_name-new.png)

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
