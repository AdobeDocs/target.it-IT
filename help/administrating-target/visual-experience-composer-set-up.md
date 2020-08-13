---
keywords: visual experience composer;vec;default url;enhanced experience composer;eec;mixed content;experience snapshots;mobile viewport;css;css selectors
description: Configurate  Adobe Target Visual Experience Composer (VEC) specificandone le impostazioni generali, la configurazione del viewport mobile e i selettori CSS.
title: Configurare  Adobe Target Visual Experience Composer
feature: administration general
topic: Standard
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 52%

---


# Configurare il Compositore esperienza visivo

Configurate [!DNL Adobe Target] Visual Experience Composer (VEC) (Compositore esperienza [!UICONTROL visivo] visivo) specificandone le impostazioni generali, la configurazione del viewport mobile e i selettori CSS.

Per accedere alla pagina di configurazione di [!UICONTROL Visual Experience Composer (Compositore esperienza visivo)] , fate clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Visual Experience Composer (Compositore esperienza visivo)].**

>[!NOTE]
>
>Tenete presente che le impostazioni in questa pagina si applicano all’intero [!DNL Target] account.

![Pagina di configurazione di Visual Experience Composer (Compositore esperienza visivo)](/help/administrating-target/assets/vec.png)

## Impostazioni generali

Potete specificare le impostazioni generali di Visual Experience Composer (Compositore esperienza visivo).

![Sezione Impostazioni generali](/help/administrating-target/assets/general-settings.png)

Sono disponibili le seguenti opzioni:

### URL predefinito

Imposta l&#39;URL predefinito utilizzato dal [!UICONTROL Compositore esperienza visivo]. Si tratta della pagina predefinita, ad esempio la pagina principale, utilizzata ogni volta che configuri un’esperienza per ogni nuova attività. Se non imposti un URL predefinito, dovrai immetterne uno ogni volta che crei una nuova attività.

### Abilita Compositore esperienza avanzato

Consente la modifica sui siti non compatibili con iFrame e su siti con contenuti misti. Alcuni siti potrebbero non essere compatibili con la versione avanzata. Deselect this option to revert to the original [!UICONTROL Visual Experience Composer]. La distribuzione delle attività ai siti non è interessata da questa selezione.

Per ulteriori informazioni, consulta [Risoluzione dei problemi relativi a Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

You can also enable the [!UICONTROL Enhanced Experience Composer] at the activity level.

### Caricamento contenuto misto

Enable mixed content while opening a website using the [!UICONTROL Enhanced Experience Composer] (EEC). Enabling this option avoids the extra overhead of loading static resources via [!DNL Target] proxy servers.

Questa opzione è utile se, ad esempio:

* Le intestazioni di Content Security Policy (CSP) consentono il caricamento di contenuti misti senza l&#39;uso di server proxy con la tecnologia EEC abilitata.
* Il sito Web HTTP deve affrontare un tempo di caricamento maggiore in CEE, dove JavaScript, immagini e così via richiedono più tempo per il caricamento tramite proxy.

### Generazione di snapshot dell&#39;esperienza nel diagramma del flusso di attività

L&#39;attivazione delle istantanee esperienza genera miniature per le tue esperienze nel diagramma del flusso di lavoro dell&#39;attività. La disabilitazione delle istantanee potrebbe determinare prestazioni più veloci per alcuni utenti.

## ![Configurazione vista](/help/assets/premium.png) mobile badge Premium

Puoi aggiungere dispositivi da utilizzare quando visualizzi le esperienze in anteprima. A ogni dispositivo è associato un pubblico.

![Sezione Configurazione di Mobile Viewer](/help/administrating-target/assets/mobile-viewport-configuration.png)

Click **[!UICONTROL Add]**, specify a descriptive name for the mobile viewport, specify the width and height, select the desired operating system, then click [!UICONTROL Save].

Per informazioni su come aggiungere un riquadro di visualizzazione mobile, vedi [Configurazione di riquadri di visualizzazione per dispositivi mobili](/help/c-experiences/c-visual-experience-composer/mobile-viewports.md).

## Selettori CSS {#css}

Specifica come [!DNL Target] genera selettori CSS.

![Sezione Selettori CSS](/help/administrating-target/assets/css-selectors.png)

Queste opzioni permettono a [!DNL Target] di comprendere la struttura del sito per generare selettori CSS in modo più efficace per la distribuzione dei contenuti. Per impostazione predefinita, [!DNL Target] genera selettori in base agli ID degli elementi nella pagina. Utilizzare pochi ID, o duplicare gli ID nella stessa pagina, utilizzando poi le classi, potrebbe essere un&#39;opzione migliore per il tuo sito.

È possibile scegliere una o entrambe le opzioni seguenti:

### Usa ID elemento

Deseleziona questa opzione se lo stesso ID viene utilizzato per più elementi o se l&#39;ID elemento potrebbe cambiare in fase di caricamento della pagina.

### Utilizza classi elemento

Per impostazione predefinita, [!DNL Target] utilizza solo ID elemento. Tuttavia, se la tua pagina è progettata per utilizzare le classi per identificare gli elementi, ad esempio una pagina creata con [!DNL Adobe Experience Manager], dovrai selezionare anche [!UICONTROL Usa classi elemento].

>[!NOTE]
>
>Anche se è stato fatto tutto per garantire la precisione, è importante tenere presente che l&#39;uso delle classi può causare errori. Anche non selezionare nessuna opzione influenza la precisione. L&#39;ordine di precisione è ID > classi > nessuna opzione. Testa sempre la pagina per assicurarti che i selettori siano corretti.

Puoi eseguire l&#39;override di questa [!UICONTROL impostazione] per ogni attività (fai clic sull&#39;icona Impostazioni, quindi seleziona [!UICONTROL Selettori CSS]). È particolarmente utile se disponi di più siti configurati in modo diverso.

>[!NOTE]
>
>Overriding the setting per activity is not available in [!UICONTROL Automated Personalization] and [!UICONTROL Multivariate Testing] activities.  Per ulteriori informazioni sui selettori, vedi [Selettori di elementi utilizzati nel Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/vec-selectors.md).

## Video di formazione: Preferenze account (7:33) ![badge Panoramica](/help/assets/overview.png)

In questo video trovi informazioni sulle preferenze dell&#39;account.

* Descrizione delle impostazioni account disponibili in [!DNL Target Standard]

>[!NOTE]
>
>L’interfaccia utente del menu [!DNL Target] Amministrazione [!UICONTROL (precedentemente] Configurazione ) è stata riprogettata per fornire prestazioni migliori, ridurre il tempo di manutenzione necessario per rilasciare nuove funzioni e migliorare l’esperienza dell’utente nel prodotto. Le informazioni riportate nel seguente video sono generalmente corrette; tuttavia, le opzioni potrebbero trovarsi in posizioni leggermente diverse. I video aggiornati verranno pubblicati a breve.

>[!VIDEO](https://video.tv.adobe.com/v/17379)
