---
keywords: compositore esperienza visivo;vec;url predefinito;compositore esperienza avanzato;eec;contenuto misto;istantanee esperienza;riquadro di visualizzazione mobile;css;selettori css
description: Scopri come configurare il Compositore esperienza visivo di Adobe [!DNL Target] specificandone le impostazioni generali, la configurazione del riquadro di visualizzazione mobile e i selettori CSS.
title: Come si configura il Compositore esperienza visivo?
feature: Administration & Configuration
role: Admin
exl-id: cf6c9ece-6745-477e-81ac-a3e9a9fddb09
TQID: https://experienceleague.adobe.com/E1ck4-aG4txqaFLs3t3-8bN-BQIoY8stRASTRJfhZMY
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: dfc8a233-f2b5-4811-bf63-b4262aebc5a5
    internal-label: Administration and configuration
subfeature_v2:
  - id: b1d5cd6a-4ed3-43f6-9a52-2721acea1129
    internal-label: Troubleshooting
  - id: c011fe9c-b94b-4a88-93d8-f2acece55112
    internal-label: Administration
  - id: fc9c2184-9102-403f-bd6c-0055021e4bea
    internal-label: Overview
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 553aa8fb523a62f72f0e2be7d7fd1b4eb663da6b
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 32%
---
# Configurare il Compositore esperienza visivo

Utilizza la scheda **[!UICONTROL Compositore esperienza visivo]** in **[!UICONTROL Amministrazione]** per impostare le impostazioni predefinite a livello di account per il [!DNL Adobe Target] [!UICONTROL Compositore esperienza visivo]. Queste impostazioni si applicano ogni volta che gli autori creano o visualizzano in anteprima le esperienze nel Compositore esperienza visivo.

**Panoramica sulla configurazione**

1. [Impostazioni generali](#general-settings): URL predefinito, Compositore esperienza avanzato, contenuti misti e istantanee delle esperienze.
1. [Configurazione riquadro di visualizzazione mobile](#mobile-viewport-configuration): dispositivi di anteprima per esperienze reattive ([Target Premium](/help/main/c-intro/intro.md#premium)).
1. [Selettori CSS](#css): come Target genera i selettori per la distribuzione dei contenuti.

Per aprire la pagina di configurazione, fare clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Compositore esperienza visivo]**.

>[!NOTE]
>
>Le impostazioni di questa pagina vengono applicate all&#39;intero account [!DNL Target].

## Impostazioni generali {#general-settings}

Nella sezione **[!UICONTROL Impostazioni generali]**, configura le impostazioni predefinite utilizzate all&#39;apertura del Compositore esperienza visivo.

![Sezione Impostazioni generali](/help/main/administrating-target/assets/general-settings.png)

Sono disponibili le seguenti impostazioni:

* **URL predefinito**

  Imposta l&#39;URL predefinito utilizzato dal [!UICONTROL Compositore esperienza visivo]. Si tratta della pagina predefinita, ad esempio la pagina principale, utilizzata ogni volta che configuri un’esperienza per ogni nuova attività. Se non imposti un URL predefinito, dovrai immetterne uno ogni volta che crei una nuova attività.

* **Abilita Compositore esperienza avanzato**

  Consente la modifica sui siti non compatibili con iFrame e su siti con contenuti misti. Alcuni siti potrebbero non essere compatibili con la versione avanzata. Deseleziona questa opzione per ripristinare il [!UICONTROL Compositore esperienza visivo] originale. La distribuzione delle attività ai siti non è interessata da questa selezione.

  Il [!UICONTROL Compositore esperienza avanzato] non è supportato in [!DNL Safari].

  Per ulteriori informazioni, vedete [Risoluzione dei problemi relativi a Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

  Puoi anche abilitare il [!UICONTROL Compositore esperienza avanzato] a livello di attività. Consulta [Scopri come abilitare il Compositore esperienza avanzato a livello di attività](/help/main/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md).

* **Carica contenuto misto**

  Abilita i contenuti misti durante l&#39;apertura di un sito Web utilizzando [!UICONTROL Compositore esperienza avanzato] (EEC). L&#39;abilitazione di questa opzione evita un carico aggiuntivo dovuto al caricamento di risorse statiche tramite i server proxy [!DNL Target].

  Questa opzione è utile se, ad esempio:

  * Le intestazioni Content Security Policy (CSP) consentono di caricare contenuti misti senza l’utilizzo di server proxy quando è abilitato il Compositore esperienza avanzato.
  * Il sito web HTTP deve affrontare tempi di caricamento più elevati nel Compositore esperienza avanzato, con JavaScript, immagini e così via che richiedono più tempo per essere caricati tramite proxy.

* **Genera istantanee esperienza nel diagramma del flusso di attività**

  Abilitando le istantanee delle esperienze, vengono generate miniature per le tue esperienze nel diagramma del flusso di lavoro delle attività. La disabilitazione delle istantanee potrebbe determinare prestazioni più veloci per alcuni utenti.

## Configurazione di riquadri di visualizzazione mobili {#mobile-viewport-configuration}

>[!NOTE]
>
>Le impostazioni della **[!UICONTROL configurazione riquadro di visualizzazione mobile]** sono una funzionalità di [Target Premium](/help/main/c-intro/intro.md#premium).

Aggiungi dispositivi da utilizzare per l&#39;anteprima delle esperienze. A ogni dispositivo è associato un pubblico.

![Sezione configurazione riquadro di visualizzazione mobile](/help/main/administrating-target/assets/mobile-viewport-configuration.png)

Per aggiungere un riquadro di visualizzazione mobile, procedi come segue:

1. Fai clic su **[!UICONTROL Aggiungi]**.
1. Specifica un nome descrittivo per il riquadro di visualizzazione mobile, specifica la larghezza e l’altezza, quindi seleziona il sistema operativo desiderato.
1. Fai clic su **[!UICONTROL Salva]**.

Per informazioni dettagliate sull&#39;anteprima e sul pubblico, consulta [Scopri come utilizzare i riquadri di visualizzazione mobili per esperienze dinamiche](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md).

## Selettori CSS {#css}

Specifica come [!DNL Target] genera selettori CSS.

![Sezione selettori CSS](/help/main/administrating-target/assets/css-selectors.png)

Queste opzioni permettono a [!DNL Target] di comprendere la struttura del sito per generare selettori CSS in modo più efficace per la distribuzione dei contenuti. Per impostazione predefinita, [!DNL Target] genera selettori in base agli ID degli elementi nella pagina. Utilizzare pochi ID, o duplicare gli ID nella stessa pagina, utilizzando poi le classi, potrebbe essere un&#39;opzione migliore per il tuo sito.

È possibile scegliere una o entrambe le opzioni seguenti:

* **Usa ID elemento**

  Deseleziona questa opzione se lo stesso ID viene utilizzato per più elementi o se l&#39;ID elemento potrebbe cambiare in fase di caricamento della pagina.

* **Usa classi elemento**

  Per impostazione predefinita, [!DNL Target] utilizza solo ID elemento. Tuttavia, se la pagina è progettata per utilizzare classi per identificare elementi, ad esempio una pagina creata con [!DNL Adobe Experience Manager], è necessario selezionare anche **[!UICONTROL Usa classi elemento]**. La precisione del selettore è generalmente massima quando si utilizzano gli ID, inferiore quando si utilizzano le classi e inferiore quando non è selezionata alcuna opzione. Verifica la pagina nel Compositore esperienza visivo per verificare che i selettori siano corretti.

  Puoi sovrascrivere questa impostazione per ogni attività facendo clic sull&#39;icona a forma di ingranaggio **[!UICONTROL Impostazioni]** e selezionando **[!UICONTROL Selettori CSS]**, utile quando i siti nello stesso account sono configurati in modo diverso. Le sostituzioni per attività non sono disponibili nelle **[!UICONTROL attività Automated Personalization]** o **[!UICONTROL Multivariate Testing]**. Per informazioni sul comportamento del selettore e sulla risoluzione dei problemi, vedere [Selettori di elementi utilizzati nel Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md).

## Video di formazione: Preferenze account (7:33) ![Icona panoramica](/help/main/assets/overview.png)

>[!BEGINSHADEBOX]

L&#39;interfaccia utente del menu [!DNL Target] **[!UICONTROL Amministrazione]** (in precedenza **[!UICONTROL Configurazione]**) è stata riprogettata per fornire prestazioni migliori, ridurre il tempo di manutenzione necessario per il rilascio di nuove funzionalità e migliorare l&#39;esperienza utente nel prodotto. Le informazioni contenute nel video seguente sono generalmente corrette; tuttavia, le opzioni potrebbero trovarsi in punti leggermente diversi. I video aggiornati verranno pubblicati a breve.

>[!ENDSHADEBOX]

In questo video trovi informazioni sulle preferenze dell&#39;account.

* Descrizione delle impostazioni account disponibili in [!DNL Target Standard]

>[!VIDEO](https://video.tv.adobe.com/v/17379)
