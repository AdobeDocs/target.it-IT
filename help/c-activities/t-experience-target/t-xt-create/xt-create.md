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
source-git-commit: c6085fae6428cb837eed6eadd778140687348817

---


# Creare un’attività Targeting esperienze{#create-an-experience-targeting-activity}

Utilizzate [!UICONTROL Visual Experience Composer] (Compositore esperienza visivo) per creare un [!UICONTROL &#39;attività Experience Targeting] (XT) su una pagina compatibile con Target e per modificarne una o [!DNL Adobe Target]più parti.

La funzione Targeting esperienza (XT) fornisce contenuti a un pubblico specifico basato su una serie di regole e criteri definiti dagli addetti al marketing.

Il targeting delle esperienze, incluso [il geotargeting](/help/c-target/c-audiences/c-target-rules/geo.md), è utile per definire regole che indirizzano un&#39;esperienza o un contenuto specifico a un particolare pubblico. È possibile definire diverse regole in un&#39;attività per fornire diverse varianti di contenuto a tipi di pubblico diversi.

Per ulteriori informazioni sul targeting delle esperienze, su uno scenario di utilizzo e sui video di formazione, consulta [Targeting delle esperienze](/help/c-activities/t-experience-target/experience-target.md).

**Per creare un&#39;attività XT:**

1. Dall’elenco [!UICONTROL Attività], fai clic su **[!UICONTROL Crea attività]** &gt; **[!UICONTROL Targeting delle esperienze]**.

   ![Creare attività &gt; Targeting delle esperienze](/help/c-activities/t-experience-target/t-xt-create/assets/xt_select-1.png)

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

1. Specificate l&#39;URL [attività](../../../c-activities/t-experience-target/t-xt-create/xt-activity-url.md#concept_D28549AAA0A14E3BB5F05F32BE8ABC90), quindi fate clic su **[!UICONTROL Avanti]**.

   Se l&#39;account è [configurato con un URL predefinito](/help/administrating-target/r-target-account-preferences/target-account-preferences.md), per impostazione predefinita viene visualizzato l&#39;URL. Se necessario, potete passare da un URL predefinito a un altro.

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

   Per istruzioni dettagliate, consultate [Aggiunta di un&#39;esperienza](/help/c-activities/t-experience-target/t-xt-create/xt-add-experience.md).

1. Specifica [obiettivi e impostazioni](../../../c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) per l&#39;attività.