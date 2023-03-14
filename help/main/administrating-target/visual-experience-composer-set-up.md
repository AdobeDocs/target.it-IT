---
keywords: compositore esperienza visivo;vec;url predefinito;compositore esperienza avanzato;eec;contenuto misto;istantanee esperienza;riquadro di visualizzazione mobile;css;selettori css
description: Scopri come configurare l’Adobe [!DNL Target] Compositore esperienza visivo specificando le impostazioni generali, la configurazione del riquadro di visualizzazione mobile e i selettori CSS.
title: Come si configura il Compositore esperienza visivo?
feature: Administration & Configuration
role: Admin
exl-id: cf6c9ece-6745-477e-81ac-a3e9a9fddb09
source-git-commit: fa11f93058b69e5e59e0ee20c65cffa4a1344ca0
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 57%

---

# Configurare il Compositore esperienza visivo

Configura le [!DNL Adobe Target] [!UICONTROL Compositore esperienza visivo] (VEC) specificando le impostazioni generali, la configurazione del riquadro di visualizzazione mobile e i selettori CSS.

Per accedere al [!UICONTROL Compositore esperienza visivo] pagina di configurazione, fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Compositore esperienza visivo].**

>[!NOTE]
>
>Tieni presente che le impostazioni in questa pagina si applicano all’intero [!DNL Target] conto.

![Pagina di configurazione del Compositore esperienza visivo](/help/main/administrating-target/assets/vec.png)

## Impostazioni generali

Puoi specificare le impostazioni generali del Compositore esperienza visivo.

![Sezione Impostazioni generali](/help/main/administrating-target/assets/general-settings.png)

Sono disponibili le seguenti impostazioni:

### URL predefinito

Imposta l&#39;URL predefinito utilizzato dal [!UICONTROL Compositore esperienza visivo]. Si tratta della pagina predefinita, ad esempio la pagina principale, utilizzata ogni volta che configuri un’esperienza per ogni nuova attività. Se non imposti un URL predefinito, dovrai immetterne uno ogni volta che crei una nuova attività.

### Abilita Compositore esperienza avanzato {#eec}

Consente la modifica sui siti non compatibili con iFrame e su siti con contenuti misti. Alcuni siti potrebbero non essere compatibili con la versione avanzata. Deseleziona questa opzione per ripristinare l’originale [!UICONTROL Compositore esperienza visivo]. La distribuzione delle attività ai siti non è interessata da questa selezione.

Per ulteriori informazioni, consulta [Risoluzione dei problemi relativi a Compositore esperienza visivo.](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md)

È inoltre possibile abilitare [!UICONTROL Compositore esperienza avanzato] a livello di attività.

### Caricamento contenuto misto

Abilitare i contenuti misti durante l’apertura di un sito web utilizzando [!UICONTROL Compositore esperienza avanzato] (CEE) n. L’abilitazione di questa opzione evita il sovraccarico aggiuntivo derivante dal caricamento di risorse statiche tramite [!DNL Target] server proxy.

Questa opzione è utile se, ad esempio:

* Le intestazioni Content Security Policy (CSP) consentono di caricare contenuti misti senza l’utilizzo di server proxy con il Compositore esperienza avanzato abilitato.
* Nel sito web HTTP si verificano tempi di caricamento più elevati nel Compositore esperienza avanzato, con JavaScript, immagini e così via che richiedono più tempo per essere caricati tramite proxy.

### Genera istantanee esperienza nel diagramma di flusso dell&#39;attività

L&#39;attivazione delle istantanee esperienza genera miniature per le tue esperienze nel diagramma del flusso di lavoro dell&#39;attività. La disabilitazione delle istantanee potrebbe determinare prestazioni più veloci per alcuni utenti.

## [!BADGE Premium]{type=Positive url="/help/main/c-intro/intro.md#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."}

Puoi aggiungere dispositivi da utilizzare quando visualizzi le esperienze in anteprima. A ogni dispositivo è associato un pubblico.

![Sezione Configurazione di riquadri di visualizzazione per dispositivi mobili](/help/main/administrating-target/assets/mobile-viewport-configuration.png)

Fai clic su **[!UICONTROL Aggiungi]**, specifica un nome descrittivo per il riquadro di visualizzazione mobile, specifica la larghezza e l&#39;altezza, seleziona il sistema operativo desiderato, quindi fai clic su [!UICONTROL Salva].

Per informazioni su come aggiungere un riquadro di visualizzazione mobile, vedi [Configurazione di riquadri di visualizzazione per dispositivi mobili](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md).

## Selettori CSS {#css}

Specifica come [!DNL Target] genera selettori CSS.

![Sezione Selettori CSS](/help/main/administrating-target/assets/css-selectors.png)

Queste opzioni permettono a [!DNL Target] di comprendere la struttura del sito per generare selettori CSS in modo più efficace per la distribuzione dei contenuti. Per impostazione predefinita, [!DNL Target] genera selettori in base agli ID degli elementi nella pagina. Utilizzare pochi ID, o duplicare gli ID nella stessa pagina, utilizzando poi le classi, potrebbe essere un&#39;opzione migliore per il tuo sito.

È possibile scegliere una o entrambe le opzioni seguenti:

### Usa ID elemento

Deseleziona questa opzione se lo stesso ID viene utilizzato per più elementi o se l&#39;ID elemento potrebbe cambiare in fase di caricamento della pagina.

### Utilizza classi elemento

Per impostazione predefinita, [!DNL Target] utilizza solo ID elemento. Tuttavia, se la tua pagina è progettata per utilizzare le classi per identificare gli elementi, ad esempio una pagina creata con [!DNL Adobe Experience Manager], dovrai selezionare anche [!UICONTROL Usa classi elemento].

>[!NOTE]
>
>Anche se è stato fatto tutto il possibile per garantire precisione, è importante tenere presente che l’utilizzo delle classi può causare errori. Anche non selezionare nessuna opzione influenza la precisione. L&#39;ordine di precisione è ID > classi > nessuna opzione. Testa sempre la pagina per assicurarti che i selettori siano corretti.

Puoi eseguire l&#39;override di questa [!UICONTROL impostazione] per ogni attività (fai clic sull&#39;icona Impostazioni, quindi seleziona [!UICONTROL Selettori CSS]). È particolarmente utile se disponi di più siti configurati in modo diverso.

>[!NOTE]
>
>L’override dell’impostazione per ogni attività non è disponibile in [!UICONTROL Automated Personalization] e [!UICONTROL Multivariate Testing] attività.  Per ulteriori informazioni sui selettori, vedi [Selettori di elementi utilizzati nel Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md).

## Video di formazione: Preferenze account (7:33) ![Badge panoramica](/help/main/assets/overview.png)

In questo video trovi informazioni sulle preferenze dell&#39;account.

* Descrizione delle impostazioni account disponibili in [!DNL Target Standard]

>[!NOTE]
>
>L’interfaccia utente di [!DNL Target] del menu [!UICONTROL Amministrazione] (precedentemente [!UICONTROL Configurazione]) è stato riprogettato per fornire prestazioni migliori, ridurre il tempo di manutenzione necessario durante il rilascio di nuove funzioni e migliorare l’esperienza utente nel prodotto. Le informazioni contenute nel video seguente sono generalmente corrette; tuttavia, le opzioni potrebbero trovarsi in punti leggermente diversi. I video aggiornati verranno pubblicati a breve.

>[!VIDEO](https://video.tv.adobe.com/v/17379)
