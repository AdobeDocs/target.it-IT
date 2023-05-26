---
keywords: compositore esperienza basato su moduli;compositore basato su modulo;perfezionamenti
description: Scopri come utilizzare l’Adobe [!DNL Target] Compositore esperienza basato su moduli per la creazione di esperienze non visive. Utilizza questo compositore quando il Compositore esperienza visivo non è disponibile o non è pratico.
title: Come si utilizza il Compositore esperienza basato su moduli?
feature: Form-based Experience Composer
exl-id: d06a271b-f058-4c83-af75-da2a29774967
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 46%

---

# Compositore esperienza basato su moduli

Il [!DNL Adobe Target] [!UICONTROL Compositore esperienza basato su moduli] è un’interfaccia non visiva per la creazione di esperienze, utile per creare le esperienze da utilizzare in [!UICONTROL Test A/B], [!UICONTROL Targeting esperienza], [!UICONTROL Automated Personalization], e [!UICONTROL Recommendations] attività quando [!UICONTROL Compositore esperienza visivo] (VEC) non è disponibile o non è pratico per l’uso. Ad esempio, puoi utilizzare il Compositore esperienza basato su moduli per creare esperienze e offerte da distribuire tramite e-mail, chioschi e assistenti vocali.

Se stai creando un [!UICONTROL Recommendations] attività, non ci sono esperienze. Scegli i test di verifica e progettazione. Se scegli più criteri o progettazioni, [!UICONTROL Target] genera automaticamente le esperienze.

1. Fai clic su **[!UICONTROL Crea attività]**, quindi seleziona il tipo di attività che desideri creare.

   Il [!UICONTROL Compositore esperienza basato su moduli] è disponibile per [!UICONTROL Test A/B], [!UICONTROL Targeting esperienza], [!UICONTROL Automated Personalization], e [!UICONTROL Recommendations] attività.

1. Seleziona **[!UICONTROL Modulo]** dal [!UICONTROL Crea attività] .

1. (Condizionale) Scegli un’area di lavoro e una proprietà.

1. Fai clic su **[!UICONTROL Successivo]**.

   Il [!UICONTROL Compositore esperienza basato su moduli] viene aperto.

   ![immagine location_perfezionements](assets/location_refinements.png)

   Questa schermata è diversa se stai creando un [!UICONTROL Recommendations] attività. [!UICONTROL Le attività di consigli non includono esperienze.]

1. Assegna un nome all’attività facendo clic su &quot;[!UICONTROL Attività senza titolo].&quot;
1. Seleziona una posizione.

   Quando fai clic su in [!UICONTROL Seleziona posizione] viene visualizzato un elenco delle posizioni disponibili. Seleziona una di queste posizioni.

   È inoltre possibile immettere una posizione non elencata. Tale opzione può essere utile se la mbox non è ancora stata creata o visualizzata su una pagina. Digita il nome della posizione. Presta attenzione quando inserisci una posizione che non esiste ancora. Se l&#39;ortografia o l’uso di maiuscole/minuscole non corrisponde quando viene effettuata la chiamata mbox, l’attività non verrà consegnata. Le ubicazioni immesse manualmente vengono salvate nell&#39;elenco delle ubicazioni disponibili. La prossima volta che tenti di selezionare una posizione immessa manualmente, questa sarà disponibile dal [!UICONTROL Seleziona posizione] elenco a discesa per tale attività.

   >[!NOTE]
   >
   >La creazione di una posizione inserita manualmente durante la creazione dell’attività non crea automaticamente una nuova posizione. Il nome della posizione viene salvato solo nel contesto dell’attività. La posizione viene creata quando si verifica una chiamata di consegna del contenuto. Successivamente alla posizione in fase di creazione, sarà disponibile per l’utilizzo in altre attività, per la creazione di tipi di pubblico, ecc. dall’elenco a discesa delle posizioni disponibili.

1. Clic **[!UICONTROL Aggiungi perfezionamenti pubblico]**, scegli uno o più [pubblico](/help/main/c-target/target.md#concept_A782F8481A5041EBA75103CB26376522) per questa attività, quindi fai clic su **[!UICONTROL Fine]**.

   ![immagine location_perfezionements_2](assets/location_refinements_2.png)

   In [!UICONTROL Compositore esperienza basato su moduli], i miglioramenti sono stati sostituiti da funzionalità di pubblico complete. I perfezionamenti per le attività esistenti sono stati trasferiti ai tipi di [pubblico per sola attività](/help/main/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483).

1. Seleziona il tipo di contenuto da visualizzare in tale posizione.

   ![immagine form_content](assets/form_content.png)

1. Specifica il contenuto per il tipo selezionato.

   **Modifica offerta HTML:** scegli un’offerta HTML.

   **Modifica Offerte immagine:** scegli un’immagine salvata nella libreria di contenuti di Target.

   È inoltre possibile aggiungere un collegamento a un&#39;immagine (click-through, destinazione e così via.)

   1. Fai clic su [!UICONTROL Cambia offerta immagine].
   1. Seleziona l&#39;immagine desiderata, quindi fai clic su [!UICONTROL Modifica collegamenti].
   1. Specifica l&#39;URL o la pagina desiderata nel sito, quindi fai clic su [!UICONTROL Aggiorna].

   **Modifica offerta JSON:** scegli un’offerta JSON.

   **Modifica frammento esperienza:** scegli un frammento esperienza. Per ulteriori informazioni, consulta [Frammento esperienza](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md).

   **Modifica offerta di reindirizzamento:** scegli un’offerta di reindirizzamento. Per ulteriori informazioni, consulta [Creare offerte di reindirizzamento](/help/main/c-experiences/c-manage-content/offer-redirect.md).

   **Modifica offerta remota:** scegli un’offerta remota. Per ulteriori informazioni, consulta [Creare offerte remote](/help/main/c-experiences/c-manage-content/about-remote-offers.md).

   **Crea offerta HTML:**

   1. Fai clic su [!UICONTROL Offerte], quindi seleziona la scheda [!UICONTROL Offerte di codice].
   1. Fai clic su [!UICONTROL Crea] > [!UICONTROL Offerta HTML].
   1. Digita un nome per l’offerta.
   1. Digita o incolla il codice HTML nella casella Codice.
   1. Fai clic su [!UICONTROL Salva].

   **Crea offerta JSON:**

   1. Fai clic su [!UICONTROL Offerte], quindi seleziona la scheda [!UICONTROL Offerte di codice].
   1. Fai clic su [!UICONTROL Crea] > [!UICONTROL Offerta JSON].
   1. Digita un nome per l’offerta.
   1. Digita o incolla il codice JSON nella casella Codice.
   1. Fai clic su [!UICONTROL Salva].

   **Aggiungi consiglio:**

   Per un’attività di Recommendations, il menu a discesa Content (Contenuto) offre [!UICONTROL Aggiungi consiglio] opzione. Fai clic su **[!UICONTROL Aggiungi consiglio]**, quindi seleziona il tipo di pagina. Quindi segui i passi consueti descritti per [creare un’attività di consigli](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md).

   Durante la selezione dei criteri di consigli nel compositore esperienza basato su moduli, è ora disponibile un collegamento diretto alla scheda dei criteri selezionati per poter modificare in modo semplice e veloce i criteri.

   ![immagine change_criteria](assets/change_criteria.png)

   Dalla pagina di targeting del workflow guidato in tre fasi di Target:

   ![immagine change_criteria_2](assets/change_criteria_2.png)

   **Aggiungi decisione di offerta:**

   Aggiungere un’offerta creata in [!DNL Adobe Journey Optimizer] (AJO) a un [!DNL Adobe Target] attività per presentare l’offerta e l’esperienza dinamica migliore ai visitatori sul sito web o sul sito mobile utilizzando offer decisioning. Questa opzione è disponibile per le operazioni manuali [!UICONTROL Test A/B] e [!UICONTROL Targeting esperienza] (XT) solo attività.

   Per ulteriori informazioni, consulta [Utilizzare le decisioni sulle offerte](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md).

1. (Facoltativo, per [!UICONTROL Test A/B], [!UICONTROL Automated Personalization], e [!UICONTROL Targeting esperienza] attività) Per ripetere il processo per altre posizioni, fai clic su **[!UICONTROL Aggiungi posizione]** e configurare la posizione e il contenuto.
1. Clic **[!UICONTROL Successivo]**, quindi completa i passaggi di creazione dell’attività come di consueto secondo il tipo di attività.

* [Creare un test A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)
* [Creare un’attività Targeting delle esperienze](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765)
* [Creare un’attività Consigli](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F)

## Video di formazione: Compositore basato su moduli ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video fornisce una demo del Compositore esperienza basato su moduli.

* Creare un’attività utilizzando il Compositore esperienza basato su moduli
* Quando utilizzare il Compositore esperienza basato su moduli o il Compositore esperienza visivo
* Indirizzare una posizione con i perfezionamenti

>[!VIDEO](https://video.tv.adobe.com/v/17390)
