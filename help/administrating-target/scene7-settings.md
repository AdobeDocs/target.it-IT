---
keywords: scene7;dynamic media classic;gestione risorse digitali;risorse;dam;libreria contenuti;immagine di scambio
description: Scopri come integrare Adobe [!DNL Target] con Adobe Dynamic Media Classic (già Scene7) per fornire Digital Asset Management (DAM) nella libreria dei contenuti.
title: Come si configura l’integrazione Dynamic Media Classic (Scene7)?
feature: Amministrazione e configurazione
role: Administrator
exl-id: 315670ca-a4d1-4808-b3ec-f2ac195c281a
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 25%

---

# Configurazione di Dynamic Media Classic (precedentemente Scene7)

[!DNL Adobe Target] può essere integrato con  [!DNL Adobe Dynamic Media Classic] (precedentemente  [!DNL Scene7]) per fornire Digital Asset Management (DAM) nella libreria dei  [!UICONTROL contenuti].

>[!NOTE]
>
>L’integrazione di [!DNL Target] con [!DNL Dynamic Media Classic] consente la distribuzione delle risorse (come parte delle attività) caricate nella cartella delle risorse [!DNL Adobe Experience Cloud]. Questa integrazione non consente l’accesso a tutte le risorse caricate in [!DNL Dynamic Media Classic] per la distribuzione nelle attività [!DNL Target].

Se disponi già di un account [!DNL Dynamic Media], puoi fornire le tue credenziali esistenti. Se non disponi di un account, puoi richiedere un account per uso limitato [!DNL Dynamic Media Classic] senza alcun costo aggiuntivo dal tuo [!DNL Adobe] rappresentante. Questo account può essere utilizzato solo per scopi limitati all&#39;utilizzo in [!DNL Target]. Questo servizio viene reso disponibile ai clienti per i flussi di lavoro che necessitano di funzionalità di scambio immagini.

<!-- 
>[!NOTE]
>
>A restricted-use, free [!DNL Dynamic Media Classic] account for [!DNL Adobe Target] is no longer supported for new customers or new users. Existing sign-in credentials work as usual. 
-->

Se questa impostazione non è configurata, l&#39;opzione [!UICONTROL Scambia immagine] all&#39;interno del flusso di lavoro di creazione dell&#39;attività non è disponibile. Una volta configurata, l’opzione di offerte di scambio/cambiamento immagine è disponibile sia nel [Compositore esperienza visivo che nel Compositore esperienza basato su moduli](/help/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D). Puoi quindi sfruttare le offerte di immagini con immagini caricate da [!DNL Adobe Experience Cloud] per utilizzarle nelle attività [!DNL Target].

Se desideri fare riferimento a un URL di immagine pubblica direttamente in un&#39;offerta o codice personalizzato durante la creazione di attività, devi distribuire l&#39;immagine ai server web e utilizzare il tuo URL nel codice. Non è possibile ottenere l&#39;URL pubblicato di un&#39;immagine caricata in [!DNL Experience Cloud] per utilizzare direttamente o all&#39;esterno dei flussi di lavoro di targeting utilizzando [!DNL Target]. Questa funzionalità non è consentita, secondo il contratto.

Tieni presente che l’URL di archiviazione e gli URL di pubblicazione finali delle immagini di [!DNL Dynamic Media] sono diversi e che è necessario *NOT* creare offerte utilizzando il collegamento di archiviazione delle immagini, in quanto la consegna non funzionerà in tali casi. Devi utilizzare la funzionalità delle offerte di immagini come spiegato nella nostra documentazione di aiuto.

Per eseguire l&#39;integrazione con [!DNL Dynamic Media Classic] ([!DNL Scene7]), è necessario specificare le informazioni seguenti.

1. Fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Configurazione Scene7]**.

   ![Pagina Scene7](/help/administrating-target/assets/scene7.png)

1. Specifica le seguenti informazioni sull&#39;account [!DNL Dynamic Media Classic]:

   **Regione:** la regione del tuo  [!DNL Dynamic Media] account: Nord America, Europa o Asia.

   **Adhoc folder** (Cartella ad hoc): posizione del contenuto che si trova al di fuori della cartella di Target e viene caricato manualmente in [!DNL Dynamic Media].

   **Indirizzo e-mail:** l’indirizzo e-mail utilizzato per accedere a  [!DNL Dynamic Media Classic] ([!DNL Scene7]).

   **Password:** password utilizzata per accedere a  [!DNL Dynamic Media Classic] ([!DNL Scene7]).

1. Fai clic su **[!UICONTROL Invia]**.
