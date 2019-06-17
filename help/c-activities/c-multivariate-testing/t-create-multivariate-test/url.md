---
description: L'URL attività determina la pagina utilizzata nel test multivariato (MVT), che si apre quando il test è progettato in Target.
keywords: Targeting
seo-description: L'URL attività determina la pagina utilizzata nel test multivariato (MVT), che si apre quando il test è progettato in Adobe Target.
seo-title: URL attività
solution: Target
title: URL attività
uuid: ddc7330c-199a-4e38-b3d4-6786e3997783
translation-type: tm+mt
source-git-commit: 0730d5f8f6aa2b72c2069c81d6e5a0183489e91c

---


# URL attività{#activity-url}

The activity URL determines the page that is used in the [!Multivariate Test] (MVT), and that opens when the test is designed in [!DNL Adobe Target].

Quando richiesto durante [la creazione dell&#39;attività](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md), specificate l&#39;URL attività. Digitate l&#39;URL completo (incluso `https://`), quindi fate clic su **[!UICONTROL Avanti]**.

>[!NOTE]
>
>[!DNL Target] non distingue tra protocolli URL ([!DNL https] e [!DNL http]). Di conseguenza, [!DNL `https://www.adobe.com`] e [!DNL `http://www.adobe.com`] sono entrambi validi.

Per impostazione predefinita, [!UICONTROL in Visual Experience Composer] (Compositore esperienza visivo) viene aperta la pagina specificata in [Account Preferences](/help/administrating-target/r-target-account-preferences/target-account-preferences.md)(Preferenze account). È possibile specificare una pagina diversa durante la creazione dell’attività.

Per visualizzare una pagina diversa dopo l&#39;apertura dell&#39;aula virtuale, fate clic sull&#39;icona **[!UICONTROL Configura]** , quindi selezionate **[!UICONTROL Consegna pagina]**, quindi specificate l&#39;URL.

![Consegna pagina, finestra di dialogo](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/url-config.png)

Fai clic su **[!UICONTROL Aggiungi regola modello]** per aggiungere più pagine o sezioni all’attività.

Le regole aggiuntive possono essere basate su uno dei seguenti elementi:

* URL
* Dominio
* Percorso
* Frammento hash (#)
* Query
* Parametro

È possibile aggiungere altre regole all’URL attività mediante l’operatore E oppure O. Tutte le regole aggiunte vengono valutate tra loro con E.

Al termine, fai clic su **[!UICONTROL Salva]**.

>[!NOTE]
>
>Se hai inserito un URL per un sito che non include il codice JavaScript di Target Standard, non puoi selezionare elementi di pagina.

Per impostazione predefinita, la VEC non consente modifiche agli elementi che contengono javascript, ad esempio i banner a rotazione. Puoi disattivare **[!UICONTROL Esegui rendering con JavaScript]** se desideri modificare tali elementi utilizzando il [!UICONTROL Compositore esperienza visivo].

>[!NOTE]
>
>Se modifichi l’URL dopo aver apportato modifiche a una pagina per una o più esperienze, l’esperienza viene reimpostata utilizzando la nuova pagina e le modifiche apportate andranno perse.