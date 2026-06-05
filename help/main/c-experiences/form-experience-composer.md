---
keywords: compositore esperienza basato su moduli;compositore basato su modulo;perfezionamenti
description: Scopri come utilizzare il Compositore esperienza basato su moduli di Adobe [!DNL Target] per la creazione di esperienze non visive. Utilizza questo compositore quando il Compositore esperienza visivo non è disponibile o non è pratico.
title: Come si utilizza il Compositore esperienza basato su moduli?
feature: Form-based Experience Composer
exl-id: d06a271b-f058-4c83-af75-da2a29774967
TQID: https://experienceleague.adobe.com/X67IwQIWaOUNZECFjyXCAFsxEr3-FunVIhlRugKsWm8
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: adee20bd-51f4-461d-b9db-d215f8756eeb
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 988
ht-degree: 35%

---

# Compositore esperienza basato su moduli

Il [!DNL Adobe Target] [!UICONTROL Compositore esperienza basato su moduli] è un&#39;interfaccia non visiva per la creazione di esperienze, utile per creare le esperienze da utilizzare nelle attività [!UICONTROL Test A/B], [!UICONTROL Targeting esperienza], [!UICONTROL Automated Personalization] e [!UICONTROL Consigli] quando il [!UICONTROL Compositore esperienza visivo] non è disponibile o se non risulta pratico. Ad esempio, puoi utilizzare il Compositore esperienza basato su moduli per creare esperienze e offerte da distribuire tramite e-mail, chioschi e assistenti vocali.

Se stai creando un&#39;attività [!UICONTROL Consigli], non ci sono esperienze. Scegli i test di verifica e progettazione. Se scegli più criteri o progettazioni, [!UICONTROL Target] genera automaticamente le esperienze.

1. Fai clic su **[!UICONTROL Crea attività]**, quindi seleziona il tipo di attività che desideri creare.

   Il [!UICONTROL Compositore esperienza basato su moduli] è disponibile per le attività [!UICONTROL Test A/B], [!UICONTROL Targeting esperienza], [!UICONTROL Automated Personalization] e [!UICONTROL Consigli].

1. Seleziona **[!UICONTROL Modulo]** dalla finestra di dialogo [!UICONTROL Crea attività].

1. (Condizionale) Se sei un [cliente Target Premium](/help/main/c-intro/intro.md#premium), dall&#39;elenco a discesa **[!UICONTROL Scegli Workspace]** scegli un [area di lavoro](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

   L&#39;opzione [[!UICONTROL Scegli area di lavoro]](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) è una funzionalità di [Target Premium](/help/main/c-intro/intro.md) e potrebbe non essere visualizzata se la tua organizzazione dispone di una licenza di [!UICONTROL Target Standard].

1. Scegli una proprietà.

1. Fai clic su **[!UICONTROL Crea]**.

   Verrà aperto [!UICONTROL Compositore esperienza basato su moduli].

   Questa schermata è diversa se stai creando un&#39;attività [!UICONTROL Consigli]. Le attività [!UICONTROL Consigli] non includono esperienze.

1. 
   1. Fai clic sull&#39;icona **[!UICONTROL Rinomina]** ( ![Rinomina icona](/help/main/assets/icons/MoreSmallListVert.svg) ), fai clic su **[!UICONTROL Rinomina]**, specifica un nome per l&#39;attività, quindi fai clic su **[!UICONTROL Salva]**.

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

1. Seleziona una posizione.

   Quando si fa clic nella casella [!UICONTROL Seleziona percorso], viene visualizzato un elenco dei percorsi disponibili. Seleziona una di queste posizioni.

   È inoltre possibile immettere una posizione non elencata. Tale opzione può essere utile se la mbox non è ancora stata creata o visualizzata su una pagina. Digita il nome della posizione. Presta attenzione quando inserisci una posizione che non esiste ancora. Se l&#39;ortografia o l’uso di maiuscole/minuscole non corrisponde quando viene effettuata la chiamata mbox, l’attività non verrà consegnata. Le ubicazioni immesse manualmente vengono salvate nell&#39;elenco delle ubicazioni disponibili. La prossima volta che tenti di selezionare una posizione immessa manualmente, questa sarà disponibile nell&#39;elenco a discesa [!UICONTROL Seleziona posizione] per tale attività.

   >[!NOTE]
   >
   >La creazione di una posizione inserita manualmente durante la creazione dell’attività non crea automaticamente una nuova posizione. Il nome della posizione viene salvato solo nel contesto dell’attività. La posizione viene creata quando si verifica una chiamata di consegna del contenuto. Successivamente alla posizione in fase di creazione, sarà disponibile per l’utilizzo in altre attività, per la creazione di tipi di pubblico, ecc., dall’elenco a discesa delle posizioni disponibili.

1. Fai clic su **[!UICONTROL Aggiungi perfezionamenti pubblico]**, scegli uno o più [tipi di pubblico](/help/main/c-target/target.md#concept_A782F8481A5041EBA75103CB26376522) per questa attività, quindi fai clic su **[!UICONTROL Fine]**.

   In [!UICONTROL Compositore esperienza basato su moduli], i miglioramenti sono stati sostituiti da funzionalità di pubblico complete. I perfezionamenti per le attività esistenti sono stati migrati a [tipi di pubblico per sola attività](/help/main/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483).

1. Seleziona il tipo di contenuto da visualizzare in tale posizione.

1. Specifica il contenuto per il tipo selezionato.

   **Modifica offerta HTML:** scegli un’offerta HTML.

   **Modifica Offerte immagine:** scegli un’immagine salvata nella libreria di contenuti di Target.

   È inoltre possibile aggiungere un collegamento a un&#39;immagine (click-through, destinazione e così via.)

   1. Fai clic su [!UICONTROL Cambia offerta immagine].
   1. Seleziona l&#39;immagine desiderata, quindi fai clic su [!UICONTROL Modifica collegamenti].
   1. Specifica l&#39;URL o la pagina desiderata nel sito, quindi fai clic su [!UICONTROL Aggiorna].

   **Modifica offerta JSON:** scegli un’offerta JSON.

   **Modifica frammento esperienza:** Scegli un frammento esperienza. Per ulteriori informazioni, vedere [Frammento esperienza](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md).

   **Modifica offerta di reindirizzamento:** Scegli un&#39;offerta di reindirizzamento. Per ulteriori informazioni, vedere [Creare offerte di reindirizzamento](/help/main/c-experiences/c-manage-content/offer-redirect.md).

   **Modifica offerta remota:** Scegli un&#39;offerta remota. Per ulteriori informazioni, vedere [Creare offerte remote](/help/main/c-experiences/c-manage-content/about-remote-offers.md).

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

   Per un&#39;attività Consigli, l&#39;elenco a discesa Contenuto fornisce l&#39;opzione [!UICONTROL Aggiungi consiglio]. Fai clic su **[!UICONTROL Aggiungi consiglio]**, quindi seleziona il tipo di pagina. Quindi segui i passi consueti descritti per [creare un’attività di consigli](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md).

   Durante la selezione dei criteri di consigli nel compositore esperienza basato su moduli, è ora disponibile un collegamento diretto alla scheda dei criteri selezionati per poter modificare in modo semplice e veloce i criteri.

   Dalla pagina [!UICONTROL Targeting] del flusso di lavoro guidato in tre passaggi di [!DNL Target]:

   **Aggiungi decisione di offerta:**

   Aggiungi un&#39;offerta creata in [!DNL Adobe Journey Optimizer] (AJO) a un&#39;attività di [!DNL Adobe Target] per presentare l&#39;offerta e l&#39;esperienza dinamica migliore ai visitatori sul tuo sito Web o sito mobile tramite Offer Decisioning. Questa opzione è disponibile solo per le attività manuali [!UICONTROL Test A/B] e [!UICONTROL Targeting esperienza] (XT).

   Per ulteriori informazioni, consulta [Utilizzare le decisioni sulle offerte](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md).

1. (Facoltativo, per [!UICONTROL Attività Test A/B], [!UICONTROL Automated Personalization] e [!UICONTROL Targeting esperienza]) Per ripetere il processo per altre posizioni, fai clic su **[!UICONTROL Aggiungi posizione]** e configura la posizione e il contenuto.
1. Fai clic su **[!UICONTROL Avanti]**, quindi completa i passaggi di creazione dell&#39;attività come di consueto secondo il tipo di attività.

* [Creare un test A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)
* [Creare un’attività Targeting delle esperienze](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765)
* [Creare un’attività Consigli](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F)

## Video di formazione: Compositore basato su moduli ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video fornisce una demo del Compositore esperienza basato su moduli.

* Creare un’attività utilizzando il Compositore esperienza basato su moduli
* Quando utilizzare il Compositore esperienza basato su moduli o il Compositore esperienza visivo
* Indirizzare una posizione con i perfezionamenti

>[!VIDEO](https://video.tv.adobe.com/v/17390)
