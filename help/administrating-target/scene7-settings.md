---
keywords: scene7;dynamic media classic;digital asset management;assets;dam;content library
description: Target Standard può essere integrato con  Adobe Dynamic Media Classic per fornire Digital Asset Management (DAM) nella libreria Contenuto.
title: Integrazione con Dynamic Media Classic
feature: administration general
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 25%

---


# Configurazione Scene7 {#scene-settings}

[!DNL Target] può essere integrato con [!DNL Adobe Dynamic Media Classic] per fornire Digital Asset Management (DAM) nella libreria [!UICONTROL Contenuto].

>[!NOTE]
>
>Integrating [!DNL Target] with [!DNL Dynamic Media Classic] enables delivery of assets (as part of activities) uploaded to the [!DNL Adobe Experience Cloud] assets folder. This integration does not enable access to all assets uploaded in [!DNL Dynamic Media Classic] for delivery in [!DNL Target] activities.

If you already have a [!DNL Dynamic Media] account, you can supply your existing credentials. If you do not have an account, you can request a restricted-use [!DNL Dynamic Media Classic] account at no additional charge from your [!DNL Adobe] representative. This account can be used for purposes restricted for use in [!DNL Target] only. Questo servizio viene reso disponibile ai clienti per i flussi di lavoro che necessitano di funzionalità di scambio immagini.

>[!NOTE]
>
>Un [!DNL Dynamic Media Classic] account gratuito a uso limitato non [!DNL Adobe Target] è più supportato per i nuovi clienti o nuovi utenti. Le credenziali di accesso esistenti funzionano normalmente.

If this setting is not configured, the [!UICONTROL Swap Image offer] option within the activity creation workflow is not available. Una volta configurata, l’opzione di offerte di scambio/cambiamento immagine è disponibile sia nel [Compositore esperienza visivo che nel Compositore esperienza basato su moduli](/help/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D). You can then leverage image offers with images that have been uploaded from the [!DNL Adobe Experience Cloud] for use in [!DNL Target] activities.

Se desideri fare riferimento a un URL di immagine pubblica direttamente in un&#39;offerta o codice personalizzato durante la creazione di attività, devi distribuire l&#39;immagine ai server web e utilizzare il tuo URL nel codice. There is no way to obtain the published URL of an image uploaded into the [!DNL Experience Cloud] to consume directly or outside of targeting workflows using [!DNL Target]. Questa funzionalità non è consentita, secondo il contratto.

Note that the storage URL and the final publish URLs of images from [!DNL Dynamic Media] are different and one must *NOT* create offers using the storage link of images as delivery will not work in such cases. Devi usare la funzionalità delle offerte di immagini come spiegato nella nostra documentazione.

To integrate with [!DNL Dynamic Media Classic] ([!DNL Scene7]), you need to specify the following information.

1. Fate clic su **[!UICONTROL Amministrazione]** > Configurazione **** Scene7.

   ![Pagina Scene7](/help/administrating-target/assets/scene7.png)

1. Specify the following [!DNL Dynamic Media Classic] account information:

   **Regione:** La regione per il tuo [!DNL Dynamic Media] account: Nord America, Europa o Asia.

   **Adhoc folder** (Cartella ad hoc): posizione del contenuto che si trova al di fuori della cartella di Target e viene caricato manualmente in [!DNL Dynamic Media].

   **Indirizzo e-mail:** L&#39;indirizzo e-mail utilizzato per accedere a [!DNL Dynamic Media Classic] ([!DNL Scene7]).

   **Password:** La password utilizzata per accedere a [!DNL Dynamic Media Classic] ([!DNL Scene7]).

1. Fai clic su **[!UICONTROL Invia]**.
