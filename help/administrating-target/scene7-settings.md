---
keywords: scene7;dynamic media classic;digital asset management;assets;dam;content library;swap image
description: ' Adobe Target può essere integrato con  Adobe Dynamic Media Classic (già Scene7) per fornire Digital Asset Management (DAM) nella libreria Contenuto.'
title: Integrazione con Dynamic Media Classic
feature: Administration & Configuration
translation-type: tm+mt
source-git-commit: 1c5fd1062da5f90f24720fc3deb67f7f3b05aee9
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 26%

---


# Configurazione Scene7

[!DNL Adobe Target] può essere integrato con  [!DNL Adobe Dynamic Media Classic] (già Scene7) per fornire Digital Asset Management (DAM) nella libreria  [!UICONTROL Content].

>[!NOTE]
>
>L&#39;integrazione di [!DNL Target] con [!DNL Dynamic Media Classic] consente di distribuire le risorse (come parte delle attività) caricate nella cartella [!DNL Adobe Experience Cloud] delle risorse. Questa integrazione non consente l&#39;accesso a tutte le risorse caricate in [!DNL Dynamic Media Classic] per la distribuzione in attività [!DNL Target].

Se disponete già di un account [!DNL Dynamic Media], potete fornire le credenziali esistenti. Se non disponete di un account, potete richiedere un account [!DNL Dynamic Media Classic] a uso limitato senza alcun costo aggiuntivo al vostro [!DNL Adobe] rappresentante. Questo account può essere utilizzato solo per scopi limitati per l&#39;uso in [!DNL Target]. Questo servizio viene reso disponibile ai clienti per i flussi di lavoro che necessitano di funzionalità di scambio immagini.

<!-- 
>[!NOTE]
>
>A restricted-use, free [!DNL Dynamic Media Classic] account for [!DNL Adobe Target] is no longer supported for new customers or new users. Existing sign-in credentials work as usual. 
-->

Se questa impostazione non è configurata, l&#39;opzione [!UICONTROL Swap Image offer] nel flusso di lavoro per la creazione dell&#39;attività non è disponibile. Una volta configurata, l’opzione di offerte di scambio/cambiamento immagine è disponibile sia nel [Compositore esperienza visivo che nel Compositore esperienza basato su moduli](/help/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D). Potete quindi sfruttare le offerte relative alle immagini con immagini caricate da [!DNL Adobe Experience Cloud] e utilizzarle nelle attività [!DNL Target].

Se desideri fare riferimento a un URL di immagine pubblica direttamente in un&#39;offerta o codice personalizzato durante la creazione di attività, devi distribuire l&#39;immagine ai server web e utilizzare il tuo URL nel codice. Non è possibile ottenere l&#39;URL pubblicato di un&#39;immagine caricata in [!DNL Experience Cloud] per utilizzare direttamente o all&#39;esterno dei flussi di lavoro di targeting utilizzando [!DNL Target]. Questa funzionalità non è consentita, secondo il contratto.

L&#39;URL di archiviazione e gli URL finali di pubblicazione delle immagini di [!DNL Dynamic Media] sono diversi e in questi casi non è possibile creare offerte *NOT* utilizzando il collegamento di archiviazione delle immagini. Devi usare la funzionalità delle offerte di immagini come spiegato nella nostra documentazione.

Per effettuare l&#39;integrazione con [!DNL Dynamic Media Classic] ([!DNL Scene7]), è necessario specificare le informazioni seguenti.

1. Fare clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Configurazione Scene7]**.

   ![Pagina Scene7](/help/administrating-target/assets/scene7.png)

1. Specificate le seguenti informazioni sull&#39;account [!DNL Dynamic Media Classic]:

   **Regione:** la regione per il tuo  [!DNL Dynamic Media] account: Nord America, Europa o Asia.

   **Adhoc folder** (Cartella ad hoc): posizione del contenuto che si trova al di fuori della cartella di Target e viene caricato manualmente in [!DNL Dynamic Media].

   **Indirizzo e-mail:** l&#39;indirizzo e-mail utilizzato per accedere a  [!DNL Dynamic Media Classic] ([!DNL Scene7]).

   **Password:** la password utilizzata per accedere a  [!DNL Dynamic Media Classic] ([!DNL Scene7]).

1. Fai clic su **[!UICONTROL Invia]**.
