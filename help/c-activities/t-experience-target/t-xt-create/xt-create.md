---
description: Utilizza il Compositore esperienza visivo per creare un’attività Targeting esperienze su una pagina abilitata per Target e modificarne alcune parti della pagina in Target.
seo-description: Utilizzate Visual Experience Composer (Compositore esperienza visivo) per creare un'attività Experience Targeting (XT) su una pagina compatibile con Target e per modificare una parte della pagina all'interno di Adobe Target.
seo-title: Creare un’attività Targeting esperienze
solution: Target
subtopic: Test multivariato
title: Creare un’attività Targeting esperienze
topic: Standard
uuid: 6299982b-b1ba-4dd0-9c69-36a76680a3e1
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Creare un’attività Targeting esperienze{#create-an-experience-targeting-activity}

Use the [!UICONTROL Visual Experience Composer] (VEC) to create an [!UICONTROL Experience Targeting] (XT) activity on a Target-enabled page and to modify portions of the page within [!DNL Adobe Target].

La funzione Targeting esperienza (XT) fornisce contenuti a un pubblico specifico basato su una serie di regole e criteri definiti dagli addetti al marketing.

Experience Targeting, including [geo-targeting](/help/c-target/c-audiences/c-target-rules/geo.md), is valuable for defining rules that target a specific experience or content to a particular audience. È possibile definire diverse regole in un&#39;attività per fornire diverse varianti di contenuto a tipi di pubblico diversi.

For more information about Experience Targeting, a use-case scenario, and training videos, see [Experience Targeting](/help/c-activities/t-experience-target/experience-target.md).

**Per creare un&#39;attività XT:**

1. Dall’elenco [!UICONTROL Attività], fai clic su **[!UICONTROL Crea attività]** &gt; **[!UICONTROL Targeting delle esperienze]**.

   ![Creare attività &gt; Targeting delle esperienze](/help/c-activities/t-experience-target/t-xt-create/assets/xt_select-1.png)

   >[!NOTE]
   >
   >I tipi di attività disponibili dipendono dall’account Target. Alcuni tipi di attività potrebbero non essere visualizzati nell&#39;elenco. For example, [!UICONTROL Automated Personalization] is a [Target Premium feature](/help/c-intro/intro.md#premium).
   >
   >For more information about the various activity types available in [!DNL Target] and their differences, see [Activities](../../../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). See [Target Activity types](/help/c-activities/target-activities-guide.md) to help you decide which activity type best suites your needs.

1. Select **[!UICONTROL Visual (Default)]**, if necessary.

   ![Finestra di dialogo Crea attività targeting esperienza](/help/c-activities/t-experience-target/t-xt-create/assets/form_url-new.png)

   Se preferisci utilizzare il Compositore esperienza basato su moduli, seleziona [!UICONTROL Modulo]. See [Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md) for more information.

   >[!NOTE]
   >
   >Oltre a VEC e Experience Composer basato su modulo, Target offre il VEC applicazione singola e il VEC per le app mobili. For more information about the various composers, see [Experiences and Offers](/help/c-experiences/experiences.md).
   >
   >Per informazioni sulla risoluzione dei problemi relativi al Compositore esperienza visivo, consulta [Risoluzione dei problemi relativi al Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).
   >
   >The [!UICONTROL Choose Workplace] option in the preceding illustration is a [Target Premium](/help/c-intro/intro.md) feature. Se l&#39;opzione non è visualizzata, l&#39;organizzazione dispone di una licenza di Target Standard.]

1. (Conditional) If you are a Target Premium customer, [choose a workspace](/help/administrating-target/c-user-management/property-channel/property-channel.md).

1. Specify your [activity URL](../../../c-activities/t-experience-target/t-xt-create/xt-activity-url.md#concept_D28549AAA0A14E3BB5F05F32BE8ABC90), then click **[!UICONTROL Next]**.

   If your account is [configured with a default URL](/help/administrating-target/r-target-account-preferences/target-account-preferences.md), that URL appears by default. Se necessario, potete passare da un URL predefinito a un altro.

   Viene aperto il VEC, che mostra la pagina specificata nell&#39;URL.

   ![Attività Targeting delle esperienze all&#39;interno della VEC](/help/c-activities/t-experience-target/t-xt-create/assets/xt-in-vec.png)

1. Digita un nome per l&#39;attività nello spazio fornito.

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

1. Crea nuove esperienze mirate per le audience delle differenze.

   For step-by-step instructions, see [Add experience](/help/c-activities/t-experience-target/t-xt-create/xt-add-experience.md).

1. Specifica [obiettivi e impostazioni](../../../c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) per l&#39;attività.