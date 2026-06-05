---
keywords: compositore esperienza visivo;vec;url predefinito;compositore esperienza avanzato;eec;contenuto misto;istantanee esperienza;riquadro di visualizzazione mobile;css;selettori css
description: Scopri come configurare il Compositore esperienza visivo di Adobe [!DNL Target] specificandone le impostazioni generali, la configurazione del riquadro di visualizzazione mobile e i selettori CSS.
title: Come si configura il Compositore esperienza visivo?
feature: Administration & Configuration
role: Admin
exl-id: cf6c9ece-6745-477e-81ac-a3e9a9fddb09
TQID: https://experienceleague.adobe.com/E1ck4-aG4txqaFLs3t3-8bN-BQIoY8stRASTRJfhZMY
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: dfc8a233-f2b5-4811-bf63-b4262aebc5a5
subfeature_v2: id: b1d5cd6a-4ed3-43f6-9a52-2721acea1129id: c011fe9c-b94b-4a88-93d8-f2acece55112id: fc9c2184-9102-403f-bd6c-0055021e4bea
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: c1579802-ddd4-4214-8a91-97b2066abe11id: d095671a-1355-40aa-8b5f-06c33c68080bid: e0eb8757-182f-49f3-94a4-1587d16f5094id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 721
ht-degree: 47%

---

# Configura il [!UICONTROL Compositore esperienza visivo]

Configura il [!DNL Adobe Target] [!UICONTROL Compositore esperienza visivo] specificandone le impostazioni generali, la configurazione del riquadro di visualizzazione mobile e i selettori CSS.

Per accedere alla pagina di configurazione del [!UICONTROL Compositore esperienza visivo], fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Compositore esperienza visivo].**

{{permissions-update}}

>[!NOTE]
>
>Tenere presente che le impostazioni di questa pagina si applicano all&#39;intero account [!DNL Target].

## Impostazioni generali

È possibile specificare le impostazioni generali per il [!UICONTROL Compositore esperienza visivo].

![Sezione Impostazioni generali](/help/main/administrating-target/assets/general-settings.png)

Sono disponibili le seguenti impostazioni:

### URL predefinito

Imposta l&#39;URL predefinito utilizzato dal [!UICONTROL Compositore esperienza visivo]. Si tratta della pagina predefinita, ad esempio la pagina principale, utilizzata ogni volta che configuri un’esperienza per ogni nuova attività. Se non imposti un URL predefinito, dovrai immetterne uno ogni volta che crei una nuova attività.

### Abilita Compositore esperienza avanzato {#eec}

Consente la modifica sui siti non compatibili con iFrame e su siti con contenuti misti. Alcuni siti potrebbero non essere compatibili con la versione avanzata. Deseleziona questa opzione per ripristinare il [!UICONTROL Compositore esperienza visivo] originale. La distribuzione delle attività ai siti non è interessata da questa selezione.

Per ulteriori informazioni, vedete [Risoluzione dei problemi relativi a Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

Puoi anche abilitare il [!UICONTROL Compositore esperienza avanzato] a livello di attività.

### Caricamento contenuto misto

Abilita i contenuti misti durante l&#39;apertura di un sito Web utilizzando [!UICONTROL Compositore esperienza avanzato] (EEC). L&#39;abilitazione di questa opzione evita un carico aggiuntivo dovuto al caricamento di risorse statiche tramite i server proxy [!DNL Target].

Questa opzione è utile se, ad esempio:

* Le intestazioni Content Security Policy (CSP) consentono di caricare contenuti misti senza l’utilizzo di server proxy quando è abilitato il Compositore esperienza avanzato.
* Il sito web HTTP deve affrontare tempi di caricamento più elevati nel Compositore esperienza avanzato, con JavaScript, immagini e così via che richiedono più tempo per essere caricati tramite proxy.

### Generare istantanee delle esperienze nel diagramma del flusso di attività

Abilitando le istantanee delle esperienze, vengono generate miniature per le tue esperienze nel diagramma del flusso di lavoro delle attività. La disabilitazione delle istantanee potrebbe determinare prestazioni più veloci per alcuni utenti.

## Configurazione di riquadri di visualizzazione per dispositivi mobili

>[!NOTE]
>
>Le impostazioni della [!UICONTROL configurazione riquadro di visualizzazione mobile] sono una funzionalità di [Target Premium](/help/main/c-intro/intro.md#premium).


Puoi aggiungere dispositivi da utilizzare quando visualizzi le esperienze in anteprima. A ogni dispositivo è associato un pubblico.

![Sezione configurazione riquadro di visualizzazione mobile](/help/main/administrating-target/assets/mobile-viewport-configuration.png)

Fai clic su **[!UICONTROL Aggiungi]**, specifica un nome descrittivo per il riquadro di visualizzazione mobile, specifica la larghezza e l&#39;altezza, seleziona il sistema operativo desiderato, quindi fai clic su [!UICONTROL Salva].

Per informazioni su come aggiungere un riquadro di visualizzazione mobile, vedi [Configurazione di riquadri di visualizzazione per dispositivi mobili](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md).

## Selettori CSS {#css}

Specifica come [!DNL Target] genera selettori CSS.

![Sezione selettori CSS](/help/main/administrating-target/assets/css-selectors.png)

Queste opzioni permettono a [!DNL Target] di comprendere la struttura del sito per generare selettori CSS in modo più efficace per la distribuzione dei contenuti. Per impostazione predefinita, [!DNL Target] genera selettori in base agli ID degli elementi nella pagina. Utilizzare pochi ID, o duplicare gli ID nella stessa pagina, utilizzando poi le classi, potrebbe essere un&#39;opzione migliore per il tuo sito.

È possibile scegliere una o entrambe le opzioni seguenti:

### Usa ID elemento

Deseleziona questa opzione se lo stesso ID viene utilizzato per più elementi o se l&#39;ID elemento potrebbe cambiare in fase di caricamento della pagina.

### Utilizza classi elemento

Per impostazione predefinita, [!DNL Target] utilizza solo ID elemento. Tuttavia, se la pagina è progettata per utilizzare classi per identificare elementi, ad esempio una pagina creata con [!DNL Adobe Experience Manager], è necessario selezionare anche [!UICONTROL Usa classi elemento].

>[!NOTE]
>
>Sebbene sia stato fatto tutto il possibile per garantire la precisione, l’utilizzo delle classi può causare errori. Anche non selezionare nessuna opzione influenza la precisione. L&#39;ordine di precisione è ID > classi > nessuna opzione. Testa sempre la pagina per assicurarti che i selettori siano corretti.

Puoi sovrascrivere questa impostazione per ogni attività (fai clic sull&#39;icona a forma di ingranaggio [!UICONTROL Impostazioni], quindi seleziona [!UICONTROL Selettori CSS]). È particolarmente utile se disponi di più siti configurati in modo diverso.

>[!NOTE]
>
>L&#39;override dell&#39;impostazione per ogni attività non è disponibile nelle attività [!UICONTROL Automated Personalization] e [!UICONTROL Multivariate Testing].  Per ulteriori informazioni sui selettori, vedi [Selettori di elementi utilizzati nel Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md).

## Video di formazione: Preferenze account (7:33) ![Icona panoramica](/help/main/assets/overview.png)

In questo video trovi informazioni sulle preferenze dell&#39;account.

* Descrizione delle impostazioni account disponibili in [!DNL Target Standard]

>[!NOTE]
>
>L&#39;interfaccia utente del menu [!DNL Target] [!UICONTROL Amministrazione] (in precedenza [!UICONTROL Configurazione]) è stata riprogettata per fornire prestazioni migliori, ridurre il tempo di manutenzione necessario per il rilascio di nuove funzionalità e migliorare l&#39;esperienza utente nel prodotto. Le informazioni contenute nel video seguente sono generalmente corrette; tuttavia, le opzioni potrebbero trovarsi in punti leggermente diversi. I video aggiornati verranno pubblicati a breve.

>[!VIDEO](https://video.tv.adobe.com/v/17379)
