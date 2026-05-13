---
keywords: scene7;dynamic media classic;gestione risorse digitali;digital asset management;risorse;assets;dam;libreria contenuti;cambiare immagine
description: Scopri come integrare Adobe  [!DNL Target]  con Adobe Dynamic Media Classic (precedentemente Scene7) per il Digital Asset Management (DAM) nella Libreria contenuti.
title: Come si configura l’integrazione Dynamic Media Classic (Scene7)?
feature: Administration & Configuration
role: Admin
exl-id: 315670ca-a4d1-4808-b3ec-f2ac195c281a
TQID: https://experienceleague.adobe.com/LKbjwlGIxrgaU-2i6Ddn1wi-VjsSmpQPAxYkFHRNOYQ
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: da3860b0-d637-47df-bef0-273751180266
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 393
ht-degree: 84%

---

# Configurazione di Dynamic Media Classic (precedentemente Scene7)

[!DNL Adobe Target] può essere integrato con [!DNL Adobe Dynamic Media Classic] (precedentemente [!DNL Scene7]) per fornire Digital Asset Management (DAM) in [!UICONTROL Content Library].

{{permissions-update}}

>[!NOTE]
>
>L’integrazione di [!DNL Target] con [!DNL Dynamic Media Classic] consente la trasmissione delle risorse (come parte delle attività) caricate nella cartella risorse di [!DNL Adobe Experience Cloud]. Tale integrazione non consente l’accesso a tutte le risorse caricate in [!DNL Dynamic Media Classic] per la trasmissione alle attività di [!DNL Target].

Se disponi già di un account [!DNL Dynamic Media], puoi fornire le tue credenziali. In caso contrario, puoi richiedere un account [!DNL Dynamic Media Classic] limitato, senza alcun costo aggiuntivo, rivolgendoti al tuo rappresentante [!DNL Adobe]. Questo account può essere utilizzato per scopi limitati solo in [!DNL Target]. Questo servizio viene reso disponibile ai clienti per i flussi di lavoro che necessitano di funzionalità di scambio immagini.

<!-- 
>[!NOTE]
>
>A restricted-use, free [!DNL Dynamic Media Classic] account for [!DNL Adobe Target] is no longer supported for new customers or new users. Existing sign-in credentials work as usual. 
-->

Se questa impostazione non è configurata, l&#39;opzione [!UICONTROL Swap Image offer] nel flusso di lavoro di creazione attività non è disponibile. Dopo aver configurato questa impostazione, l&#39;opzione per scambiare/modificare le offerte di immagini è disponibile sia nel [Compositore esperienza visivo che nel Compositore esperienza basato su moduli](/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D). Puoi quindi sfruttare le offerte di immagine con le immagini che sono state caricate da [!DNL Adobe Experience Cloud] e usarle in attività di [!DNL Target].

Se desideri fare riferimento a un URL di immagine pubblica direttamente in un&#39;offerta o codice personalizzato durante la creazione di attività, devi distribuire l&#39;immagine ai server web e utilizzare il tuo URL nel codice. Non è possibile ottenere l’URL pubblicato di un’immagine caricata su [!DNL Experience Cloud] per utilizzarlo direttamente o all’esterno dei flussi di lavoro di targeting utilizzando [!DNL Target]. Questa funzionalità non è consentita, secondo il contratto.

Tieni presente che l’URL di archiviazione e gli URL di pubblicazione finali delle immagini di [!DNL Dynamic Media] sono diversi; fai attenzione a *NON* creare offerte utilizzando il collegamento di archiviazione delle immagini, poiché in tal caso la consegna non funziona. Utilizza piuttosto la funzionalità per offerte di immagini descritta nella documentazione di supporto.

Per l’integrazione con [!DNL Dynamic Media Classic] ([!DNL Scene7]), devi specificare alcune delle seguenti informazioni.

1. Fare clic su **[!UICONTROL Administration]** > **[!UICONTROL Scene7 Configuration]**.

1. Specifica le informazioni seguenti sull’account [!DNL Dynamic Media Classic]:

   **Area geografica:** area geografica del tuo account [!DNL Dynamic Media], Nord America, Europa o Asia.

   **Adhoc folder** (Cartella ad hoc): posizione del contenuto che si trova al di fuori della cartella di Target e viene caricato manualmente in [!DNL Dynamic Media].

   **Indirizzo e-mail:** indirizzo e-mail utilizzato per accedere a [!DNL Dynamic Media Classic] ([!DNL Scene7]).

   **Password:** password utilizzata per accedere a [!DNL Dynamic Media Classic] ([!DNL Scene7]).

1. Fare clic su **[!UICONTROL Submit]**.
