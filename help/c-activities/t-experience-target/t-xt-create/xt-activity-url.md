---
description: L'URL attività determina la pagina utilizzata nell'attività Experience Targeting (Targeting esperienza) e che viene aperta in Visual Experience Composer (Compositore esperienza visivo) o in Experience Composer (Compositore esperienza basato su modulo) quando l'attività è stata progettata.
keywords: Targeting
seo-description: L'URL attività determina la pagina utilizzata nell'attività Experience Targeting (Targeting esperienza) e che viene aperta in Adobe Target Visual Experience Composer (VEC) o Experience Composer (Compositore esperienza basato su modulo) quando l'attività è stata progettata.
seo-title: URL attività
solution: Target
title: URL attività
uuid: 970de8ba-ab60-4339-866b-27889bec67f9
translation-type: tm+mt
source-git-commit: ca9639ccca286dac182728f7bbd43fac78217209

---


# URL attività{#activity-url}

L&#39;URL attività determina la pagina utilizzata nell&#39;attività Experience Targeting (XT), che viene aperta in Visual Experience Composer (Compositore esperienza visivo) o in Experience Experience Composer (Compositore esperienza basato su modulo) quando l&#39;attività è stata progettata.

1. Quando viene richiesto durante [la creazione di un&#39;attività XT](/help/c-activities/t-experience-target/t-xt-create/xt-create.md), specificate l&#39;URL attività. Digita l’URL completo (comprensivo di `https://`), quindi fai clic su **[!UICONTROL Crea attività]**.

   >[!NOTE]
   >
   >[!DNL Target] non distingue tra protocolli URL ([!DNL https] e [!DNL http]). Di conseguenza, [!DNL `https://www.adobe.com`] e [!DNL `http://www.adobe.com`] sono entrambi validi.
   >
   >Per impostazione predefinita, il composer di esperienze VEC o Basato su modulo apre la pagina specificata in Preferenze [account](/help/administrating-target/r-target-account-preferences/target-account-preferences.md). È possibile specificare una pagina diversa durante la creazione dell’attività.
   >
   >Se specificate un URL per un sito che non include il codice javascript di Target Standard, non potete selezionare elementi di pagina.

1. (Condizionale) Per visualizzare una pagina diversa dopo l&#39;apertura dell&#39;aula virtuale, fate clic su **[!UICONTROL Configura]**, selezionate **[!UICONTROL Consegna]** pagina e specificate l&#39;URL nel campo [!UICONTROL URL] .

   ![Consegna pagina, finestra di dialogo](/help/c-activities/t-experience-target/t-xt-create/assets/url-config-new.png)

   >[!NOTE]
   >
   >Se modifichi l’URL dopo aver apportato modifiche a una pagina per una o più esperienze, l’esperienza viene reimpostata utilizzando la nuova pagina e le modifiche apportate andranno perse.

1. (Condizionale) Fate clic su **[!UICONTROL Aggiungi regola]** modello per aggiungere altre pagine o sezioni all&#39;attività.

   Le regole aggiuntive possono essere basate su uno dei seguenti elementi:

   * URL
   * Dominio
   * Percorso
   * Frammento hash (#)
   * Query
   * Parametro mbox
   È possibile aggiungere altre regole all’URL attività mediante l’operatore E oppure O. Tutte le regole aggiunte vengono valutate tra loro con E.

1. Al termine, fai clic su **[!UICONTROL Salva]**.