---
description: Il compositore esperienza basato su moduli permette di creare esperienze in modo non visivo.
keywords: compositore esperienza basato su moduli;compositore basato su modulo;perfezionamenti
seo-description: Il compositore esperienza basato su moduli permette di creare esperienze in modo non visivo.
seo-title: Compositore esperienza basato su moduli
solution: Target
title: Compositore esperienza basato su moduli
topic: Standard
uuid: 6791ed6f-69d0-4ec4-9ea4-47aa92b2a4c9
translation-type: tm+mt
source-git-commit: b1dd50db873cb9a7cdca976366171ddf0c02d156

---


# Compositore esperienza basato su moduli{#form-based-experience-composer}

Il compositore esperienza basato su moduli permette di creare esperienze in modo non visivo.

Questa funzione consente a Target Standard di consegnare attività di test A/B, targeting delle esperienze, personalizzazione automatizzata e consigli in e-mail, app per dispositivi mobili, kiosk e altre destinazioni che non consentono l’utilizzo del Compositore esperienza visivo.

Se stai creando un’attività di consigli, non ci sono esperienze. Scegli i test di verifica e progettazione. Se scegli più criteri o progettazioni, Target genera automaticamente le esperienze.

1. Fai clic su **[!UICONTROL Crea attività]**, quindi seleziona il tipo di attività che desideri creare.

   Il Compositore esperienza basato su moduli è disponibile per test A/B, targeting di esperienza, personalizzazione automatizzata e attività di consigli.
1. Seleziona **[!UICONTROL Compositore esperienza basato su moduli]** nella finestra di dialogo [!UICONTROL Nuova attività].

   Si apre il Compositore esperienza basato su moduli.

   ![](assets/location_refinements.png)

   La schermata è diversa se si sta creando un’attività di consigli. Le attività di consigli non includono esperienze.
1. Assegna un nome all’attività.
1. Seleziona una posizione.

   Quando fai clic nella casella Seleziona posizione, viene visualizzato un elenco di posizioni disponibili. Seleziona una di queste posizioni. Per scegliere la posizione globale fornita tramite target.js, seleziona “target-global-mbox”.

   È inoltre possibile immettere una posizione non elencata. Tale opzione può essere utile se la mbox non è ancora stata creata o visualizzata su una pagina. Digita il nome della posizione. Presta attenzione quando inserisci una posizione che non esiste ancora. Se l&#39;ortografia o l’uso di maiuscole/minuscole non corrisponde quando viene effettuata la chiamata mbox, l’attività non verrà consegnata. Le posizioni inserite manualmente vengono salvate nell’elenco.
1. Fai clic su **[!UICONTROL Aggiungi perfezionamenti pubblico]**, quindi scegli uno o più tipi di [pubblico](../c-target/target.md#concept_A782F8481A5041EBA75103CB26376522) per questa attività.

   ![](assets/location_refinements_2.png)

   Nel Compositore esperienza basato su moduli, i Perfezionamenti sono stati sostituiti da funzionalità di pubblico complete. I perfezionamenti per le attività esistenti sono stati trasferiti ai tipi di  [pubblico per sola attività](../c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483).
1. Seleziona il tipo di contenuto da visualizzare in tale posizione.

   ![](assets/form_content.png)

1. Specifica il contenuto per il tipo selezionato.

   **Modifica offerta HTML:** scegli un’offerta HTML.

   **Modifica Offerte immagine:** scegli un’immagine salvata nella libreria di contenuti di Target.

   È inoltre possibile aggiungere un collegamento a un&#39;immagine (click-through, destinazione e così via.)

   1. Fai clic su [!UICONTROL Cambia offerta immagine].
   1. Seleziona l&#39;immagine desiderata, quindi fai clic su [!UICONTROL Modifica collegamenti].
   1. Specifica l&#39;URL o la pagina desiderata nel sito, quindi fai clic su [!UICONTROL Aggiorna].
   **Modifica offerta JSON:** scegli un’offerta JSON.

   **Modifica frammento esperienza:** scegli un frammento esperienza.

   **Modifica offerta di reindirizzamento:** scegli un’offerta di reindirizzamento.

   **Modifica offerta remota:** scegli un’offerta remota.

   **Crea offerta HTML:**

   1. Fai clic su [!UICONTROL Offerte], quindi seleziona la scheda [!UICONTROL Offerte di codice].
   1. Fai clic su [!UICONTROL Crea] &gt; [!UICONTROL Offerta HTML].
   1. Digita un nome per l’offerta.
   1. Digita o incolla il codice HTML nella casella Codice.
   1. Fai clic su [!UICONTROL Salva].
   **Crea offerta JSON:**

   1. Fai clic su [!UICONTROL Offerte], quindi seleziona la scheda [!UICONTROL Offerte di codice].
   1. Fai clic su [!UICONTROL Crea] &gt; [!UICONTROL Offerta JSON].
   1. Digita un nome per l’offerta.
   1. Digita o incolla il codice JSON nella casella Codice.
   1. Fai clic su [!UICONTROL Salva].
   Per un&#39;attività Consigli, l&#39;elenco a discesa del contenuto fornisce l&#39;opzione Aggiungi consiglio. Fai clic su **[!UICONTROL Aggiungi consiglio]**, quindi seleziona il tipo di pagina. Quindi segui i passi consueti descritti per [creare un’attività di consigli](https://marketing.adobe.com/resources/help/en_US/target/recs/t_create_recs_activity.html).

   Durante la selezione dei criteri di Consigli nel compositore esperienza basato su moduli, è ora disponibile un collegamento diretto alla scheda dei criteri selezionati per poter modificare in modo semplice e veloce i criteri.

   ![](assets/change_criteria.png)

   Dalla pagina di targeting del workflow guidato in tre fasi di Target:

   ![](assets/change_criteria_2.png)

1. (Facoltativo, per attività AB, Personalizzazione automatizzata e Targeting delle esperienze) Per ripetere il processo per posizioni aggiuntive, fai clic su `Add Location` e configura la posizione e il contenuto.
1. Fai clic su **[!UICONTROL Continua]**, quindi completa i passaggi di creazione dell’attività come di consueto secondo il tipo di attività.

* [Creare un test A/B](../c-activities/t-test-ab/t-test-create-ab/test-create-ab.md#task_68C8079BF9FF4625A3BD6680D554BB72)
* [Creare un’attività Targeting delle esperienze](../c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765)
* [Creare un’attività Consigli](../c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F)

## Video di formazione: Compositore basato su modulo

Questo video fornisce una demo del Compositore esperienza basato su moduli.

* Creare un’attività utilizzando il Compositore esperienza basato su moduli
* Quando utilizzare il Compositore esperienza basato su moduli o il Compositore esperienza visivo
* Indirizzare una posizione con i perfezionamenti

>[!VIDEO](https://video.tv.adobe.com/v/17390)