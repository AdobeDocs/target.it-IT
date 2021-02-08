---
keywords: Obiettivi e impostazioni;obiettivo;priorità;durata
description: Scoprite come utilizzare le impostazioni dell'attività in  Adobe Target per gestire l'obiettivo, la priorità e la durata delle attività.
title: Come Si Specificano Le Impostazioni Dell'Attività?
feature: Activities
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 80%

---


# Impostazioni delle attività

Utilizzate [!UICONTROL Activity Settings] in [!DNL Adobe Target] per gestire l&#39;obiettivo, la priorità e la durata delle attività.

1. Immetti delle note sulla finalità dell&#39;attività.

   Inserisci informazioni sull’attività, utili per te o per gli altri membri del gruppo. Trascina per ridimensionare il campo [!UICONTROL Finalità].
1. Imposta la durata dell&#39;attività.

   L’interfaccia utente e le opzioni per [!UICONTROL Priorità] variano a seconda delle impostazioni. È possibile utilizzare le impostazioni legacy Bassa, Media o Alta, oppure attivare la priorità precisa da 0 a 999.

   La priorità è utilizzata se più attività vengono assegnate alla stessa posizione con lo stesso pubblico. Se due o più attività vengono assegnate alla posizione, viene visualizzata l’attività con priorità maggiore.

   Se questa opzione non è abilitata in [!UICONTROL Amministrazione] > [!UICONTROL Reporting] (impostazione predefinita), specificate una priorità: Bassa, Media o Alta.

   Per abilitare le priorità con granulosità fine, fare clic su [!UICONTROL Amministrazione] > [!UICONTROL Reporting], quindi attivare l&#39;opzione [!UICONTROL Abilita priorità con granulosità fine] nella posizione &quot;Attivato&quot;.

   Se questa opzione è abilitata, specifica un valore compreso tra 0 e 999:

   * 0 = Bassa
   * 999 = Alta

   Per le attività create con le versioni precedenti di [!DNL Target Standard/Premium], la priorità Bassa viene convertita in 0, la priorità Media in 5 e la priorità Alta in 10. Se necessario, è possibile modificare questi valori.

   >[!NOTE]
   >
   >Prima di poter disabilitare questa opzione dopo aver utilizzato le priorità precise, tutte le priorità devono essere impostate su 0, 5 o 10.

1. Imposta la durata dell’attività.

   È possibile attivare e disattivare manualmente l&#39;attività oppure specificare la data e l&#39;ora della sua consegna. Il controllo del tempo usa un orologio di 24 ore, dove 00:00 indica la mezzanotte. Il fuso orario è impostato sul fuso configurato nel browser. Per utilizzare un fuso orario diverso, imposta il browser su un altro fuso orario e riavvia il browser.

   >[!NOTE]
   >
   >La pianificazione di un’attività controlla l’intervallo di tempo di consegna dell’attività; tuttavia, l’attività deve essere attivata esplicitamente prima che possa essere recapitata in base alla pianificazione specificata.

La pagina [!UICONTROL Obiettivi e impostazioni] include impostazioni aggiuntive che variano in base al tipo di attività che si sta creando. Per ulteriori informazioni su queste impostazioni, fai riferimento al tipo di attività:

* [Test A/B](/help/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC)
* [Personalizzazione automatizzata](/help/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9)
* [Targeting esperienza](/help/c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC)
* [Test multivariato](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC)
* [Consigli](/help/c-recommendations/t-create-recs-activity/recs-activity-settings.md#reference_3FDA8388CEEC4159949151C1829E2FBB)

## Video di formazione: Impostazioni attività  ![Badge di esercitazione](/help/assets/tutorial.png)

Questo video include informazioni sulle impostazioni delle attività.

* Inserire una finalità per l’attività
* Impostare il livello di priorità delle attività
* Orari di inizio e fine dell’attività
* Aggiungere tipi di pubblico da usare come filtri nella generazione di rapporti
* Inserire delle note per le attività

   >[!VIDEO](https://video.tv.adobe.com/v/17381)
