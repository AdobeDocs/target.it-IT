---
keywords: Obiettivo e impostazioni;obiettivo;priorità;durata
description: Scopri come utilizzare le impostazioni delle attività in Adobe [!DNL Target] per gestire l'obiettivo, la priorità e la durata delle attività.
title: Come Si Specificano Le Impostazioni Delle Attività?
feature: Activities
exl-id: 7f34080b-d2ed-4fe5-80ff-3aba16961223
TQID: https://experienceleague.adobe.com/tCKQJJOfsU1XkeHwFHNF33XP4tYvxlE0Hv01u0CBr7o
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: adee20bd-51f4-461d-b9db-d215f8756eeb
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: e0eb8757-182f-49f3-94a4-1587d16f5094id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 432
ht-degree: 77%

---

# Impostazioni delle attività

Utilizza [!UICONTROL Impostazioni attività] in [!DNL Adobe Target] per gestire la finalità, la priorità e la durata delle attività.

1. Immetti delle note sulla finalità dell&#39;attività.

   Inserisci informazioni sull’attività, utili per te o per gli altri membri del gruppo. Trascinare per ridimensionare il campo [!UICONTROL Finalità].
1. Imposta la durata dell&#39;attività.

   L’interfaccia utente e le opzioni per [!UICONTROL Priorità] variano a seconda delle impostazioni. È possibile utilizzare le impostazioni legacy Bassa, Media o Alta, oppure attivare la priorità granulare da 0 a 999.

   La priorità è utilizzata se più attività vengono assegnate alla stessa posizione con lo stesso pubblico. Se due o più attività vengono assegnate alla posizione, viene visualizzata l’attività con priorità maggiore.

   Se questa opzione non è abilitata in [!UICONTROL Amministrazione] > [!UICONTROL Generazione rapporti] (impostazione predefinita), specificare una priorità: Bassa, Medium o Alta.

   Per abilitare le priorità dettagliate, fai clic su [!UICONTROL Amministrazione] > [!UICONTROL Generazione rapporti], quindi attiva l&#39;opzione [!UICONTROL Abilita priorità precise].

   Se questa opzione è abilitata, specifica un valore compreso tra 0 e 999:

   * 0 = Bassa
   * 999 = Alta

   Per le attività create con le versioni precedenti di [!DNL Target Standard/Premium], la priorità Bassa viene convertita in 0, la priorità Media in 5 e la priorità Alta in 10. Se necessario, è possibile modificare questi valori.

   >[!NOTE]
   >
   >Prima di poter disabilitare questa opzione dopo aver utilizzato le priorità precise, tutte le priorità devono essere impostate su 0, 5 o 10.

1. Imposta la durata dell’attività.

   È possibile attivare e disattivare manualmente l&#39;attività oppure specificare la data e l&#39;ora della sua consegna. Il controllo dell&#39;ora utilizza un orologio di 24 ore, dove 00:00 corrisponde a mezzanotte. Il fuso orario è impostato sul fuso configurato nel browser. Per utilizzare un fuso orario diverso, imposta il browser su un altro fuso orario e riavvia il browser.

   >[!NOTE]
   >
   >La pianificazione di un’attività controlla l’arco temporale di consegna dell’attività; tuttavia, l’attività deve essere attivata esplicitamente prima che possa essere recapitata in base alla pianificazione specificata.

La pagina [!UICONTROL Obiettivi e impostazioni] include impostazioni aggiuntive che variano in base al tipo di attività che si sta creando. Per ulteriori informazioni su queste impostazioni, fai riferimento al tipo di attività:

* [Test A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC)
* [Personalizzazione automatizzata](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9)
* [Targeting esperienza](/help/main/c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC)
* [Test multivariato](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC)
* [Consigli](/help/main/c-recommendations/t-create-recs-activity/recs-activity-settings.md#reference_3FDA8388CEEC4159949151C1829E2FBB)

## Video di formazione: Impostazioni attività ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video include informazioni sulle impostazioni delle attività.

* Inserire una finalità per l’attività
* Impostare il livello di priorità delle attività
* Orari di inizio e fine dell’attività
* Aggiungere tipi di pubblico da usare come filtri nella generazione di rapporti
* Inserire delle note per le attività

  >[!VIDEO](https://video.tv.adobe.com/v/17381)
