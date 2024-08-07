---
keywords: targeting;dispositivi mobili;target dispositivi mobili;deviceatlas;iphone;modelli di iphone;device atlas;displaywidth;larghezza display;altezza display;tipo di dispositivo;displayheight;telefono;tablet;modello di dispositivo
description: Scopri come creare tipi di pubblico in [!DNL Adobe Target] per eseguire il targeting di dispositivi mobili.
title: Posso indirizzare i visitatori in base alle opzioni mobile?
feature: Audiences
exl-id: 73d5c80c-bfa2-4806-8c04-652781b70bf2
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 33%

---

# Dispositivi mobili

Crea tipi di pubblico in [!DNL Adobe Target] per indirizzare l&#39;attività a dispositivi mobili in base a parametri quali dispositivo mobile, tipo di dispositivo, fornitore, dimensioni dello schermo e altro ancora.

Ad esempio, potrebbe essere utile mostrare contenuti diversi agli utenti che visitano la pagina utilizzando un telefono rispetto a quelli che visualizzano utilizzando un computer. In tal caso, è possibile selezionare il pubblico [!UICONTROL Mobile], quindi selezionare l&#39;opzione **[!UICONTROL Is Mobile Phone]**. Puoi quindi aggiungere qualsiasi dettaglio specifico che ti interessi, ad esempio il tipo di telefono, le dimensioni dello schermo (in pixel) e così via.

Il targeting per i dispositivi mobili è fornito da [DeviceAtlas](https://deviceatlas.com/device-data/user-agent-tester), un servizio di dotMobi. DeviceAtlas è un database completo di dispositivi mobili basato su dati compilati da numerose fonti, inclusi produttori e operatori di rete. Questi dati vengono poi verificati, incrociati e convalidati per generare un database ampio e accurato dei dispositivi mobili.

Il rilevamento del dispositivo viene eseguito analizzando le stringhe Utente-Agente. Alcuni produttori di dispositivi, come ad esempio Apple, disabilitano questa funzionalità (non forniscono informazioni sufficienti nel documentazione per gli utenti).

Ad esempio, i dispositivi Apple non condividono token specifici del modello di dispositivo nell&#39;UA. Il risultato è che non è possibile rilevare i modelli di iPhone (come iPhone 12 Pro, iPhone 12, iPhone 11 Pro Max e così via) utilizzando un semplice metodo basato su parole chiave.

Per risolvere questo problema, [!DNL Target] raccoglie dati aggiuntivi per rilevare con precisione iPhone e altri dispositivi Apple utilizzando i seguenti parametri:

| Parametro | Tipo | Descrizione |
|--- |--- |--- |
| devicePixelRatio | Stringa | Rapporto tra pixel fisici e pixel indipendenti dalla periferica (dips) nel browser. Ad esempio, &quot;1,5&quot; o &quot;2&quot; |
| screenOrientation | Stringa | Il motore JavaScript del dispositivo e del browser supportano l&#39;Orientamento del Dispositivo. Può essere orizzontale o verticale. |
| webGLRenderer | Stringa | Rendering del browser del driver grafico. |

>[!NOTE]
>
>I clienti che utilizzano l’SDK di Mobile non devono eseguire alcuna operazione per applicare questa funzionalità. I clienti che utilizzano at.js devono [eseguire l&#39;aggiornamento alla versione 1.5.0](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} di at.js (o successiva).

È possibile scegliere più di una proprietà per i dispositivi mobili. Le selezioni multiple sono collegate da un operatore OR.

I clienti che utilizzano un&#39;integrazione personalizzata (non con at.js o l&#39;SDK mobile) possono raccogliere questi parametri e trasmetterli come parametri mbox.

1. Nell&#39;interfaccia [!DNL Target], fare clic su **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**.
1. Assegna un nome al pubblico e aggiungi una descrizione facoltativa.
1. Trascina **[!UICONTROL Mobile]** nel riquadro Generatore di pubblico.
1. Fare clic su **[!UICONTROL Select]**, quindi selezionare una delle opzioni seguenti:

   * Nome marketing del dispositivo
   * Modello dispositivo
   * Produttore dispositivo
   * È un dispositivo mobile
   * È un telefono cellulare
   * È un tablet
   * Sistema operativo
   * Altezza schermo (px)
   * Larghezza schermo (px)

   >[!NOTE]
   >
   >Puoi eseguire il targeting per gestore di telefonia mobile utilizzando le [impostazioni Geo](/help/main/c-target/c-audiences/c-target-rules/geo.md#concept_5B4D99DE685348FB877929EE0F942670).

1. (Facoltativo) Imposta regole aggiuntive per il pubblico.
1. Fare clic su **[!UICONTROL Done]**.

L’illustrazione seguente mostra un pubblico che include i visitatori che utilizzano dispositivi mobili prodotti da Google.

![Targeting di dispositivi mobili](assets/target_mobile.png)

## Considerazioni

Quando esegui il targeting di dispositivi mobili, considera le seguenti informazioni:

### Targeting di dispositivi con iOS 12.2 o versione successiva

A causa delle nuove modifiche introdotte in iOS 12.2, la creazione di un pubblico con regole definite da [!UICONTROL Device Marketing Name] e [!UICONTROL Device Model] che specificano modelli iPhone è interessata. [!DNL Target] non può più eseguire il targeting di utenti che dispongono di iPhone con iOS 12.2 (o versione successiva) installato su di essi. Tuttavia, se tali utenti non dispongono di iOS 12.2 (o versioni successive), il targeting del modello iPhone continua a funzionare correttamente.

L’aggiornamento iOS 12.2 (o versioni successive) non influisce sull’identificazione dei seguenti modelli, poiché questi non supportano l’aggiornamento a iOS 12.2: iPhone, iPhone 3G, iPhone 3GS, iPhone 4, iPhone 4s, iPhone 5, iPhone 5c, iPad, iPad 2, display iPad/Retina, iPad Retina (4a generazione), iPod Touch 4 e iPod Touch 5.

### Targeting di dispositivi con Safari 14.0.2 (o versione successiva)

Quando si utilizzano le regole per dispositivi mobili per eseguire il targeting di dispositivi che eseguono Safari versione 14.0.2 (o successiva) su macOS, a causa di un problema noto che coinvolge gli agenti utente e DeviceAtlas di Apple, [!DNL Target] identifica in modo errato Safari sui dispositivi Mac e iPad. Questo problema sarà affrontato in futuro.

## Video di formazione: Creazione di tipi di pubblico

Questo video contiene informazioni sull&#39;utilizzo delle categorie di pubblico.

* Creazione di un pubblico
* Definizione delle categorie di pubblico

>[!VIDEO](https://video.tv.adobe.com/v/17392)
