---
description: Imposta le preferenze del tuo account in modo che Target Standard o Target Premium funzionino correttamente.
keywords: Preferenze account;preferenze;dettagli del sito;nome mbox personalizzato;soluzione Experience Cloud utilizzata per la creazione di rapporti;Mostra incremento stimato nei ricavi;selettori CSS;utilizza classi di elementi;URL predefinito per Compositore esperienza visivo;abilita il Compositore esperienza avanzato;Genera istantanee esperienza;configurazione di riquadri di visualizzazione mobili;Settore verticale;Filtra criteri incompatibili
seo-description: Impostate le preferenze dell'account per configurare Adobe Target Standard o Target Premium in modo che funzioni correttamente con l'account.
seo-title: Preferenze
solution: Target
subtopic: Introduzione
title: Preferenze
topic: Standard
uuid: ed3904c8-533b-4b9c-a3a1-079c61b1bf2a
translation-type: tm+mt
source-git-commit: 4631137b4464bc04008fb1d290f6872ef4144217

---


# Preferenze{#preferences}

Imposta le preferenze del tuo account in modo che [!DNL Target Standard] o [!DNL Target Premium] funzionino correttamente.

Per impostare le preferenze dell’account, fai clic su **[!UICONTROL Configurazione]** &gt; **[!UICONTROL Preferenze]**, configura le preferenze, quindi fai clic su **[!UICONTROL Invia]**.

Nell&#39;illustrazione seguente trovi le impostazioni disponibili nella pagina [!UICONTROL Preferenze account].

![Pagina Preferenze](/help/administrating-target/r-target-account-preferences/assets/target-account-preferences.png)

>[!NOTE]
>
>Alcune di queste preferenze sono disponibili solo se si dispone [di Target Premium](/help/c-intro/intro.md#premium).

## Dettagli sito {#section_04A3340FC29B46978DB77058259F4EE0}

Specificate la modalità di configurazione del sito.

### Mbox globale personalizzata

Seleziona il nome mbox personalizzato facoltativo utilizzato per distribuire le attività [!DNL Target]. Questa mbox globale deve essere vuota, ovvero priva di contenuto predefinito. Salvate questa impostazione solo dopo l&#39;installazione del file o [!DNL at.js][!DNL mbox.js] del file sul sito.

>[!CAUTION]
>
>La configurazione errata di questa impostazione potrebbe causare un’interruzione delle attività esistenti.

## Risultati e reporting {#section_47C887AABD704A96BCD1C00BEABF4BCE}

Imposta le opzioni che determinano quali dati vengono utilizzati per i risultati e i rapporti.

| Opzione | Descrizione |
|--- |--- |
| Soluzione Experience Cloud utilizzata per la creazione di rapporti | Seleziona l&#39;origine di creazione di rapporti per le attività, sia in [!DNL Target] sia in Adobe Analytics. È inoltre possibile selezionare l&#39;origine per la generazione di rapporti per ogni attività. Considera le seguenti informazioni nella scelta dell&#39;origine per la generazione di rapporti:<ul><li>La creazione, l’attivazione e la disattivazione delle attività di [!UICONTROL Allocazione automatica], [!UICONTROL Targeting automatico] e [!UICONTROL Personalizzazione automatizzata] (AP) sono consentite indipendentemente dall’origine per la generazione di rapporti selezionata. Questi tipi di attività non sono supportati quando si sceglie [Adobe Analytics come origine per la generazione di rapporti per Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md). Anche se si specifica Analytics come origine per la generazione di rapporti, [!DNL Target] viene utilizzato come origine per la generazione di rapporti per questi tipi di attività.</li><li>Se l’origine per la generazione di rapporti è impostata su Analytics qui, non è consentito attivare un’attività che utilizza [!DNL Target] come origine per la generazione di rapporti (l’origine per la generazione di rapporti è specificata come Target per attività). È necessario modificare l&#39;origine per la generazione di rapporti in Analytics nell’attività o modificare il motore di generazione di rapporti in Seleziona per attività in Configurazione &gt; Preferenze.</li><li>Se l&#39;origine per la generazione di rapporti è impostata su [!DNL Target] qui, non è consentito attivare un&#39;attività che utilizza Analytics come origine per la generazione di rapporti. È necessario modificare l&#39;origine per la generazione di rapporti in [!DNL Target] nell’attività o modificare l’origine per la generazione di rapporti in Seleziona per attività in Configurazione &gt; Preferenze.</li><li>Se l&#39;origine per la generazione di rapporti è impostata su Seleziona per attività qui, è possibile creare, attivare e disattivare attività supportate dall&#39;origine per la generazione di rapporti selezionata. Per una matrice delle attività supportate, vedi [Adobe Analytics come origine per la generazione di rapporti per Adobe Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T).</li><li>Quando si passa da Manuale A/B ad [!UICONTROL Allocazione automatica] o [!UICONTROL Targeting automatico] tutte le metriche e i pubblici di reportistica vengono persi se l’origine per la generazione di rapporti dell’attività Manuale A/B non è supportata nelle attività di [!UICONTROL Allocazione automatica] o [!UICONTROL Targeting automatico].</li></ul> |
| Mostra incremento stimato nei ricavi | Inoltre, puoi scegliere di mostrare l&#39;incremento stimato nei ricavi immettendo un valore monetario per il tuo obiettivo. Con [!DNL Target] puoi stimare l’incremento dei ricavi potenziali se tutti gli utenti visualizzano l’esperienza vincente. La funzione di stima dell&#39;incremento è disabilitata per impostazione predefinita.<br>Solo gli utenti amministratore di Experience Cloud possono abilitare o disabilitare questa funzione. Se la stima dell’incremento è disattivata, i campi corrispondenti non vengono visualizzati nell’interfaccia. La disattivazione della funzione non si traduce in una perdita di dati, compresi i dati utilizzati per le stime. Le stime si basano sui dati raccolti indipendentemente dallo stato di attivazione della funzione.<br>Per informazioni dettagliate, vedi [Stima dell’incremento dei ricavi](/help/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md). |
| Abilitare le priorità precise | Consente di specificare voci numeriche con priorità da 0-999.<br>L’interfaccia utente e le opzioni per Priorità variano a seconda delle impostazioni. È possibile utilizzare le impostazioni legacy Bassa, Media o Alta, oppure attivare la priorità granulare da 0 a 999.<br>La priorità è utilizzata se più attività vengono assegnate alla stessa posizione con lo stesso pubblico. Se due o più attività vengono assegnate alla posizione, viene visualizzata l’attività con priorità maggiore. |

## Selettori CSS {#section_8155EDBF449E4198863235F94D1EA872}

Specifica come [!DNL Target] genera selettori CSS.

Queste opzioni permettono a [!DNL Target] di comprendere la struttura del sito per generare selettori CSS in modo più efficace per la distribuzione dei contenuti. Per impostazione predefinita, [!DNL Target] genera selettori in base agli ID degli elementi nella pagina. Utilizzare pochi ID, o duplicare gli ID nella stessa pagina, utilizzando poi le classi, potrebbe essere un&#39;opzione migliore per il tuo sito.

È possibile scegliere una o entrambe le opzioni seguenti:

| Opzione | Descrizione |
|--- |--- |
| Usa ID elemento | Deseleziona questa opzione se lo stesso ID viene utilizzato per più elementi o se l&#39;ID elemento potrebbe cambiare in fase di caricamento della pagina. |
| Utilizza classi elemento | Per impostazione predefinita, [!DNL Target] utilizza solo ID elemento. Tuttavia, se la tua pagina è progettata per utilizzare le classi per identificare gli elementi, ad esempio una pagina creata con [!DNL Adobe Experience Manager], dovrai selezionare anche [!UICONTROL Usa classi elemento].<br>**Nota**: anche se abbiamo fatto tutto il possibile per assicurare precisione, usare le classi può provocare errori. Anche non selezionare nessuna opzione influenza la precisione. L&#39;ordine di precisione è ID &gt; classi &gt; nessuna opzione. Testa sempre la pagina per assicurarti che i selettori siano corretti.<br>Puoi eseguire l&#39;override di questa [!UICONTROL impostazione] per ogni attività (fai clic sull&#39;icona Impostazioni, quindi seleziona [!UICONTROL Selettori CSS]). È particolarmente utile se disponi di più siti configurati in modo diverso.<br>**Nota**: la possibilità di bypassare l’impostazione per ogni attività non è disponibile nella [!UICONTROL Personalizzazione automatizzata] e nelle attività di [!UICONROL Test multivariato].  Per ulteriori informazioni sui selettori, vedi [Selettori di elementi utilizzati nel Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/vec-selectors.md). |

## Compositore esperienza visivo  {#section_CD9BDD372CF54E678F88E8BA95757A5A}

| Opzione | Descrizione |
|--- |--- |
| URL Compositore esperienza visivo predefinito  | Imposta l&#39;URL predefinito utilizzato dal [!UICONTROL Compositore esperienza visivo]. Si tratta della pagina predefinita, ad esempio la pagina principale, utilizzata ogni volta che configuri un’esperienza per ogni nuova attività. Se non imposti un URL predefinito, dovrai immetterne uno ogni volta che crei una nuova attività. |
| Abilita Compositore esperienza avanzato | Consente la modifica sui siti non compatibili con iFrame e su siti con contenuti misti. Alcuni siti potrebbero non essere compatibili con la versione avanzata. Deseleziona questa opzione per ripristinare il Compositore esperienza originale. La distribuzione delle attività ai siti non è interessata da questa selezione.<br>Per ulteriori informazioni, consulta [Risoluzione dei problemi relativi a Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).<br>**Nota**: puoi anche abilitare il Compositore esperienza avanzato a livello di attività. |
| Carica contenuto misto | Abilitare il contenuto misto durante l&#39;apertura di un sito Web mediante Enhanced Experience Composer (EEC). L&#39;abilitazione di questa opzione evita il sovraccarico aggiuntivo del caricamento di risorse statiche tramite server proxy di Target.<br>Questa opzione è utile, ad esempio, se le intestazioni dell&#39;Informativa sulla sicurezza dei contenuti (CSP) consentono di caricare contenuto misto senza l&#39;utilizzo di server proxy con la versione EEC attivata.<br>Questa opzione è utile anche se il sito Web HTTP contiene un tempo di caricamento maggiore nella EEC, in cui javascript, immagini e così via richiedono più tempo per il caricamento tramite proxy. |
| Genera istantanee esperienza | L&#39;attivazione delle istantanee esperienza genera miniature per le tue esperienze nel diagramma del flusso di lavoro dell&#39;attività. La disabilitazione delle istantanee potrebbe determinare prestazioni più veloci per alcuni utenti. |

## Configurazione di riquadri di visualizzazione per dispositivi mobili {#section_42176D062BCE4A28ADBB784CC4BEF84D}

Puoi aggiungere dispositivi da utilizzare quando visualizzi le esperienze in anteprima. A ogni dispositivo è associato un pubblico.

| Opzione | Descrizione |
|--- |--- |
| ![Badge Premium](/help/assets/premium.png) Aggiungi nuovo | Fai clic su [!UICONTROL Aggiungi nuovo], assegna un nome descrittivo al riquadro di visualizzazione mobile, specifica la larghezza e l&#39;altezza, seleziona il sistema operativo desiderato, quindi fai clic su [!UICONTROL Salva].  Per informazioni su come aggiungere un riquadro di visualizzazione mobile, vedi [Configurazione di riquadri di visualizzazione per dispositivi mobili](/help/c-experiences/c-visual-experience-composer/mobile-viewports.md). |

## Video di formazione: Preferenze dell’account (7:33)

In questo video trovi informazioni sulle preferenze dell&#39;account.

* Descrizione delle impostazioni account disponibili in [!DNL Target Standard]

>[!VIDEO](https://video.tv.adobe.com/v/17379)