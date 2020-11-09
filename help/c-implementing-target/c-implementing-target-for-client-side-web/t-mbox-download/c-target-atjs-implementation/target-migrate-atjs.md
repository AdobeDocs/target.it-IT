---
keywords: Target;at.js;migrate to at.js;readiness;audit at.js;integrate at.js
description: La migrazione da mbox.js a at.js è un processo semplice.
title: Come migrare a at.js da mbox.js
feature: null
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '826'
ht-degree: 99%

---


# Come migrare a at.js da mbox.js{#how-to-migrate-to-at-js-from-mbox-js}

La migrazione da mbox.js a at.js in [!DNL Adobe Target] è un processo semplice.

Attieniti alla procedura seguente per eseguire e controllare la migrazione da [!DNL mbox.js] a [!DNL at.js]:

1. Determina i requisiti aziendali di [supporto del browser](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md#reference_01B4BF99E7D545A7998773202A2F6100).
1. Controlla l&#39;attuale implementazione [!DNL mbox.js] del tuo sito web per le funzionalità che non sono supportate da [!DNL at.js].

   Quando controlli l&#39;implementazione, cerca i seguenti elementi:

   **Quali tipi di mbox utilizzi attualmente?**

   | Tipo | Dettagli |
   |--- |--- |
   | Mbox globale creata automaticamente | La mbox globale creata automaticamente viene creata quando l&#39;unica linea di codice di Target sul tuo sito è il file mbox.js. Tale file genera automaticamente una chiamata mbox. |
   | mboxCreate globale vuota | Si consiglia di passare alla mbox globale creata automaticamente. |
   | mboxCreate con wrapping | La migrazione dovrebbe essere semplice, purché `mboxCreate()` sia preceduto da `<div class="mboxDefault"></div>`. |
   | mboxUpdate | La migrazione dovrebbe essere semplice quando `mboxUpdate()` viene utilizzato in combinazione con `mboxDefine()` o `mboxCreate()`. `mboxUpdate()` non aggiorna la mbox globale creata automaticamente o una mbox originariamente creata da `getOffer()`. In queste circostanze, utilizza una combinazione di `getOffer()` e `applyOffer()` per sostituire `mboxUpdate()` durante la migrazione a at.js. |
   | mbox di monitoraggio clic personalizzati, tra cui mboxTrack | Si consiglia di aggiornare il codice per utilizzare `trackEvent()`. |

   >[!NOTE]
   >
   >Per ulteriori informazioni sulle varie funzioni menzionate nella tabella precedente, consulta [Funzioni di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md).

   **Hai delle personalizzazioni per il tuo file [!DNL mbox.js]?**

   * mboxParameters()
   * mboxSupported()
   * mboxCookieDomain()
   * JavaScript aggiuntivo
   * Altre posizioni

   La maggior parte degli [oggetti e dei metodi mbox.js](/help/c-target/c-visitor-profile/variables-profiles-parameters-methods.md#section_8C78059D15D9452F95636A5640188537) (ad esempio `mbox`, `mboxCurrent`, `mboxFactoryDefault`, `mboxFactories` e altri) non sono supportati. Per realizzare il tuo progetto, potresti avere a disposizione approcci alternativi.

   **Hai [!DNL mbox.js] su una qualsiasi delle tue pagine web?**

   Non puoi utilizzare sia [!DNL at.js] che [!DNL mbox.js] sulla stessa pagina web. Tuttavia, puoi utilizzare le due librerie JavaScript su due pagine diverse dello stesso sito web.

   Il cookie mbox è il modo principale di Adobe di collegare il visitatore da una pagina all&#39;altra. Per realizzare il controllo qualità, devi confermare che il cookie sia conservato e letto correttamente mentre il visitatore si muove avanti e indietro fra le pagine con [!DNL at.js] e quelle con [!DNL mbox.js]. Assicurati che gli stessi valori `mboxPC` e `mboxSession` siano trasmessi nelle chiamate mbox, indipendentemente dalla sezione del sito ([!DNL at.js] o [!DNL mbox.js]) a cui il visitatore sia approdato prima e che originariamente imposta il cookie. Se utilizzi i cookie di terze parti nell&#39;implementazione, assicurati che tali valori rimangano invariati quando esplori il sito.

   **Utilizzi integrazioni di [!DNL Target] con altre soluzioni Adobe?**

   * Analytics (A4T)
   * Analytics (integrazione legacy)
   * AAM (modulo)
   * AAM (interfaccia legacy)
   * AEM
   * Data Workbench

   Alcune delle integrazioni legacy non sono supportate da [!DNL at.js]. Per ulteriori informazioni, consulta la pagina [Integrazioni](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/target-atjs-integrations.md#concept_C100BC4F073C4B57A608B309D0157B39).

   **Utilizzi integrazioni di [!DNL Target] con uno strumento di terze parti?**

   * Altri strumenti di analisi
   * Altri sistemi DMP
   * Demandbase
   * Click-tale
   * Altro

   Potrebbe essere necessario adattare queste integrazioni affinché funzionino con [!DNL at.js]. Per ulteriori informazioni, consulta la pagina [Integrazioni](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/target-atjs-integrations.md#concept_C100BC4F073C4B57A608B309D0157B39).

   **Utilizzi un gestore di tag?**

   * Dynamic Tag Management
   * Ensighten
   * Tealium
   * Signal/BrightTag

   Per ulteriori informazioni, consulta [Integrazioni at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/target-atjs-integrations.md#concept_C100BC4F073C4B57A608B309D0157B39).

   >[!NOTE]
   >
   >Se attualmente non stai utilizzando un gestore di tag per distribuire [!DNL Target], ora potrebbe essere un buon momento per prendere in considerazione questa possibilità. [Dynamic Tag Management](https://dtm.adobe.com) di Adobe è gratuita per i clienti [!DNL Target] ed è il metodo consigliato per distribuire [!DNL Target]. Per ulteriori informazioni, vedi [Procedure consigliate per l’implementazione di Adobe Target tramite la Dynamic Tag Management](https://experienceleague.adobe.com/docs/dtm/implementing/overview.html).

1. Verifica che tutte le attività e le integrazioni correnti funzionino come previsto.

   Ecco alcune operazioni che poi eseguire durante il test per verificare che [!DNL at.js] funziona come previsto:

   * Assicurati che tutte le attività correnti funzionino con la nuova libreria JavaScript.
   * Verifica che tutte le [integrazioni](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/target-atjs-integrations.md#concept_C100BC4F073C4B57A608B309D0157B39) e i [plug-in](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-plugins.md#concept_F5D4C0A4DACF41409CC42FDD93B13FAF) funzionino come previsto.
   * Assicurati di avere familiarità con il [debugging](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-debugging-atjs/target-debugging-atjs.md#concept_CAE591DA8C404C22917584ECD4F7494F) con gli approcci disponibili con [!DNL at.js].

**Possibili problemi durante la migrazione a at.js** Alcuni clienti hanno segnalato i seguenti problemi dopo l’esecuzione della migrazione a at.js:

* Per alcune attività del Compositore esperienza visivo che sono state create in una pagina con [!DNL mbox.js] potrebbe essere necessario eseguire l&#39;aggiornamento prima di lavorare con [!DNL at.js].

   Questo problema si verifica più di frequente su siti web che non utilizzano molti attributi ID o attributi classe in elementi HTML. Puoi controllare se si verifica questo problema e capire se l’esperienza viene consegnata come previsto caricando la pagina con `?mboxDebug=true` e rivedendo le istruzioni della console.

   ![](assets/mboxdebug.png)In questi casi, i selettori di elementi potrebbero iniziare con qualcosa di simile,

   ```
   HTML > BODY > DIV:nth-of-type(2)
   ```

   sono stati costruiti tenendo in considerazione che [!DNL mbox.js] debba aggiungere un elemento extra `<div>` all’inizio della pagina. Poiché [!DNL at.js] non aggiunge un elemento `<div>` all’inizio della pagina, questo selettore non funzionerebbe più con [!DNL at.js].

   Puoi risolvere questo problema ricreando l&#39;attività nel Compositore esperienza visivo sull&#39;URL utilizzando [!DNL at.js] o aggiornando manualmente il selettore con l&#39;opzione **[!UICONTROL &lt;/> Codice]** > **[!UICONTROL Modifiche]** nel Compositore esperienza visivo.

   Per ovviare a questo problema, devi sottrarre 1 dal numero nth-of-type nel primo elemento DIV dopo BODY. Nell&#39;esempio precedente il codice modificato sarebbe:

   ```
   HTML > BODY > DIV:nth-of-type(1)
   ```

   Per ulteriori informazioni su come utilizzare l’editor di codice per eseguire questa procedura, vedi [Editor di codice](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5).

* Poiché tutte le mbox sono ora asincrone, non bloccano il rendering della pagina né tornano nell&#39;ordine in cui sono state attivate. Per ulteriori informazioni, vedi “Considerazioni asincrone” in [Limitazioni di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-limitations.md#concept_FA99E4D6EC274552BF45E01AFB76CCAE).
