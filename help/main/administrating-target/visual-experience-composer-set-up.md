---
keywords: compositore esperienza visivo;vec;url predefinito;compositore esperienza avanzato;eec;contenuto misto;istantanee esperienza;riquadro di visualizzazione mobile;css;selettori css
description: Scopri come configurare il Compositore esperienza visivo di Adobe [!DNL Target] specificandone le impostazioni generali, la configurazione del riquadro di visualizzazione mobile e i selettori CSS.
title: Come si configura il Compositore esperienza visivo?
feature: Administration & Configuration
role: Admin
exl-id: cf6c9ece-6745-477e-81ac-a3e9a9fddb09
source-git-commit: fa11f93058b69e5e59e0ee20c65cffa4a1344ca0
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 48%

---

# Configurare il Compositore esperienza visivo

Configura [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) specificandone le impostazioni generali, la configurazione del riquadro di visualizzazione mobile e i selettori CSS.

Per accedere alla pagina di configurazione [!UICONTROL Visual Experience Composer], fare clic su **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer].**

>[!NOTE]
>
>Tenere presente che le impostazioni di questa pagina si applicano all&#39;intero account [!DNL Target].

![Pagina di configurazione del Compositore esperienza visivo](/help/main/administrating-target/assets/vec.png)

## Impostazioni generali

Puoi specificare le impostazioni generali per il Compositore esperienza visivo.

![Sezione Impostazioni generali](/help/main/administrating-target/assets/general-settings.png)

Sono disponibili le seguenti impostazioni:

### URL predefinito

Impostare l&#39;URL predefinito utilizzato da [!UICONTROL Visual Experience Composer]. Si tratta della pagina predefinita, ad esempio la pagina principale, utilizzata ogni volta che configuri un’esperienza per ogni nuova attività. Se non imposti un URL predefinito, dovrai immetterne uno ogni volta che crei una nuova attività.

### Abilita Compositore esperienza avanzato {#eec}

Consente la modifica sui siti non compatibili con iFrame e su siti con contenuti misti. Alcuni siti potrebbero non essere compatibili con la versione avanzata. Deselezionare questa opzione per ripristinare l&#39;originale [!UICONTROL Visual Experience Composer]. La distribuzione delle attività ai siti non è interessata da questa selezione.

Per ulteriori informazioni, vedete [Risoluzione dei problemi relativi a Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

È inoltre possibile abilitare [!UICONTROL Enhanced Experience Composer] a livello di attività.

### Caricamento contenuto misto

Abilita i contenuti misti durante l&#39;apertura di un sito Web utilizzando [!UICONTROL Enhanced Experience Composer] (Compositore esperienza avanzato). L&#39;abilitazione di questa opzione evita un carico aggiuntivo dovuto al caricamento di risorse statiche tramite i server proxy [!DNL Target].

Questa opzione è utile se, ad esempio:

* Le intestazioni Content Security Policy (CSP) consentono di caricare contenuti misti senza l’utilizzo di server proxy quando è abilitato il Compositore esperienza avanzato.
* Il sito web HTTP deve affrontare tempi di caricamento più elevati nel Compositore esperienza avanzato, con JavaScript, immagini e così via che richiedono più tempo per essere caricati tramite proxy.

### Generare istantanee delle esperienze nel diagramma del flusso di attività

L&#39;attivazione delle istantanee esperienza genera miniature per le tue esperienze nel diagramma del flusso di lavoro dell&#39;attività. La disabilitazione delle istantanee potrebbe determinare prestazioni più veloci per alcuni utenti.

## [!BADGE Premium]{type=Positive url="/help/main/c-intro/intro.md#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."}

Puoi aggiungere dispositivi da utilizzare quando visualizzi le esperienze in anteprima. A ogni dispositivo è associato un pubblico.

![Sezione configurazione riquadro di visualizzazione mobile](/help/main/administrating-target/assets/mobile-viewport-configuration.png)

Fare clic su **[!UICONTROL Add]**, specificare un nome descrittivo per il riquadro di visualizzazione mobile, specificare larghezza e altezza, selezionare il sistema operativo desiderato, quindi fare clic su [!UICONTROL Save].

Per informazioni su come aggiungere un riquadro di visualizzazione mobile, vedi [Configurazione di riquadri di visualizzazione per dispositivi mobili](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md).

## Selettori CSS {#css}

Specifica come [!DNL Target] genera selettori CSS.

![Sezione selettori CSS](/help/main/administrating-target/assets/css-selectors.png)

Queste opzioni permettono a [!DNL Target] di comprendere la struttura del sito per generare selettori CSS in modo più efficace per la distribuzione dei contenuti. Per impostazione predefinita, [!DNL Target] genera selettori in base agli ID degli elementi nella pagina. Utilizzare pochi ID, o duplicare gli ID nella stessa pagina, utilizzando poi le classi, potrebbe essere un&#39;opzione migliore per il tuo sito.

È possibile scegliere una o entrambe le opzioni seguenti:

### Usa ID elemento

Deseleziona questa opzione se lo stesso ID viene utilizzato per più elementi o se l&#39;ID elemento potrebbe cambiare in fase di caricamento della pagina.

### Utilizza classi elemento

Per impostazione predefinita, [!DNL Target] utilizza solo ID elemento. Tuttavia, se la pagina è progettata per utilizzare le classi per identificare gli elementi, ad esempio una pagina creata con [!DNL Adobe Experience Manager], è necessario selezionare anche [!UICONTROL Use element classes].

>[!NOTE]
>
>Sebbene sia stato fatto tutto il possibile per garantire la precisione, l’utilizzo delle classi può causare errori. Anche non selezionare nessuna opzione influenza la precisione. L&#39;ordine di precisione è ID > classi > nessuna opzione. Testa sempre la pagina per assicurarti che i selettori siano corretti.

È possibile sovrascrivere questa impostazione per ogni attività (fare clic sull&#39;icona a forma di ingranaggio [!UICONTROL Settings], quindi selezionare [!UICONTROL CSS Selectors]). È particolarmente utile se disponi di più siti configurati in modo diverso.

>[!NOTE]
>
>L&#39;override dell&#39;impostazione per ogni attività non è disponibile nelle attività [!UICONTROL Automated Personalization] e [!UICONTROL Multivariate Testing].  Per ulteriori informazioni sui selettori, vedi [Selettori di elementi utilizzati nel Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md).

## Video di formazione: Preferenze account (7:33) ![Icona panoramica](/help/main/assets/overview.png)

In questo video trovi informazioni sulle preferenze dell&#39;account.

* Descrizione delle impostazioni account disponibili in [!DNL Target Standard]

>[!NOTE]
>
>L&#39;interfaccia utente del menu [!DNL Target] [!UICONTROL Administration] (in precedenza [!UICONTROL Setup]) è stata riprogettata per fornire prestazioni migliori, ridurre il tempo di manutenzione necessario per il rilascio di nuove funzionalità e migliorare l&#39;esperienza utente nel prodotto. Le informazioni contenute nel video seguente sono generalmente corrette; tuttavia, le opzioni potrebbero trovarsi in punti leggermente diversi. I video aggiornati verranno pubblicati a breve.

>[!VIDEO](https://video.tv.adobe.com/v/17379)
