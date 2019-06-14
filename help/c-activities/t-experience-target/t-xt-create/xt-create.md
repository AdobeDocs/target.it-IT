---
description: Utilizza il Compositore esperienza visivo per creare un’attività Targeting esperienze su una pagina abilitata per Target e modificarne alcune parti della pagina in Target.
seo-description: Utilizzate Visual Experience Composer (Compositore esperienza visivo) per creare un'attività di targeting delle esperienze su una pagina compatibile con Target e per modificarne una o più parti all'interno di Adobe Target.
seo-title: Creare un’attività Targeting esperienze
solution: Target
subtopic: Test multivariato
title: Creare un’attività Targeting esperienze
topic: Standard
uuid: 6299982b-b1ba-4dd0-9c69-36a76680a3e1
translation-type: tm+mt
source-git-commit: 5eb79fcd0407e0da841048bcd0a1b64393490fcf

---


# Creare un’attività Targeting esperienze{#create-an-experience-targeting-activity}

Utilizzate [!UICONTROL Visual Experience Composer] (Compositore esperienza visivo) per creare un [!UICONTROL &#39;attività Experience Targeting] (XT) su una pagina compatibile con Target e per modificarne una o [!DNL Adobe Target]più parti.

1. Dall’elenco [!UICONTROL Attività], fai clic su **[!UICONTROL Crea attività]** &gt; **[!UICONTROL Targeting delle esperienze]**.

   ![Creare attività &gt; Targeting delle esperienze](/help/c-activities/t-experience-target/t-xt-create/assets/xt_select-1.png)

   >[!NOTE]
   >
   >I tipi di attività disponibili dipendono dall’account Target. Alcuni tipi di attività potrebbero non essere visualizzati nell&#39;elenco. Ad esempio, Automated Personalization (Personalizzazione automatizzata) è una [funzione Target Premium](/help/c-intro/intro.md#premium).

   Per informazioni sui tipi di attività, consultate [Attività](../../../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) e [tipi di attività Target](/help/c-activities/target-activities-guide.md).

1. Selezionate **[!UICONTROL Visual (Elemento visivo) (Predefinito)]**, se necessario.

   ![Finestra di dialogo Crea attività targeting esperienza](/help/c-activities/t-experience-target/t-xt-create/assets/form_url-new.png)

   Se preferisci utilizzare il Compositore esperienza basato su moduli, seleziona tale opzione. Vedi [Compositore esperienza basato su moduli](https://marketing.adobe.com/resources/help/en_US/target/target/t_form_experience_composer.html).

   >[!NOTE]
   >
   >Oltre a VEC e Experience Composer basato su modulo, Target offre il VEC applicazione singola e il VEC per le app mobili. Per ulteriori informazioni sui vari moduli di composizione, vedi [Esperienze e offerte](/help/c-experiences/experiences.md).

   Per informazioni sulla risoluzione dei problemi relativi al Compositore esperienza visivo, consulta [Risoluzione dei problemi relativi al Compositore esperienza visivo](../../../c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md#reference_77743144F10143A3A89D56E116D296E4).

1. Specificate l&#39;URL [attività](../../../c-activities/t-experience-target/t-xt-create/xt-activity-url.md#concept_D28549AAA0A14E3BB5F05F32BE8ABC90), quindi fate clic su **[!UICONTROL Avanti]**.

   Se l&#39;account è configurato con un URL predefinito, tale URL verrà visualizzato come impostazione predefinita. È possibile passare dall’URL predefinito a un altro.

   Verrà aperto il Compositore esperienza visivo, con la pagina specificata nell&#39;URL.

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

1. Crea nuove esperienze modificando gli elementi nella pagina.

   Per istruzioni dettagliate, consultate [Aggiunta di un&#39;esperienza](/help/c-activities/t-experience-target/t-xt-create/xt-add-experience.md).

   Per impostazione predefinita, il Compositore esperienza visivo non consente di modificare gli elementi contenenti JavaScript, ad esempio i banner rotanti. È possibile disattivare JavaScript per poter modificare tali elementi utilizzando il Compositore esperienza visivo.

   Quando passi il puntatore del mouse sopra gli elementi della pagina, gli elementi vengono evidenziati. Qualsiasi elemento evidenziato può essere modificato utilizzando la VEC. Per un elenco delle azioni che possono essere eseguite su un elemento per modificare l&#39;esperienza, consultate Opzioni [di Visual Experience Composer (Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/viztarget-options.md)).

   Se hai creato una mbox sulla pagina utilizzando Target Classic (in precedenza Test&amp;Target), questa viene visualizzata come un elemento che mostra il nome della mbox, e può essere modificata come qualsiasi altro elemento.

1. Specifica [obiettivi e impostazioni](../../../c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) per l&#39;attività.
