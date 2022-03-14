---
keywords: targeting;dispositivi mobili;target dispositivi mobili;deviceatlas;iphone;modelli di iphone;device atlas;displaywidth;larghezza display;altezza display;tipo di dispositivo;displayheight;telefono;tablet;modello di dispositivo
description: Scopri come creare tipi di pubblico in [!DNL Adobe Target] per eseguire il targeting dei dispositivi mobili.
title: Posso indirizzare i visitatori in base alle opzioni mobile?
feature: Audiences
exl-id: 73d5c80c-bfa2-4806-8c04-652781b70bf2
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '667'
ht-degree: 40%

---

# Dispositivi mobili

Crea un pubblico in [!DNL Adobe Target] per eseguire il targeting dei dispositivi mobili in base a parametri come dispositivo mobile, tipo di dispositivo, fornitore, dimensioni dello schermo e altro ancora.

Ad esempio, potrebbe essere utile mostrare contenuti diversi agli utenti che visitano la pagina utilizzando un telefono o un computer. In tal caso, puoi selezionare la [!UICONTROL Mobile] , quindi seleziona il **[!UICONTROL È un telefono cellulare]** opzione . Puoi quindi aggiungere eventuali dettagli specifici rilevanti, ad esempio il tipo di telefono, le dimensioni dello schermo (in pixel) e così via.

Il targeting per i dispositivi mobili è fornito da [DeviceAtlas](https://deviceatlas.com/device-data/user-agent-tester), un servizio di dotMobi. DeviceAtlas è un database completo di dispositivi mobili basato su dati compilati da numerose fonti, inclusi produttori e operatori di rete. Questi dati vengono poi verificati, incrociati e convalidati per generare un database ampio e accurato dei dispositivi mobili.

Il rilevamento del dispositivo viene eseguito analizzando le stringhe Utente-Agente. Alcuni produttori di dispositivi, come ad esempio Apple, disabilitano questa funzionalità (non forniscono informazioni sufficienti nel documentazione per gli utenti).

Ad esempio, i dispositivi Apple non condividono token specifici del modello di dispositivo nell&#39;UA. Il risultato è che non è possibile rilevare i modelli iPhone (come iPhone 12 Pro, iPhone 12, iPhone 11 Pro Max e così via) utilizzando un semplice metodo basato su parole chiave.

Per risolvere questo problema, [!DNL Target] raccoglie dati aggiuntivi per rilevare con precisione iPhone e altri dispositivi Apple utilizzando i seguenti parametri:

| Parametro | Tipo | Descrizione |
|--- |--- |--- |
| devicePixelRatio | Stringa | Rapporto tra pixel fisici e pixel indipendenti dalla periferica (dips) nel browser. Ad esempio, &quot;1.5&quot; o &quot;2&quot; |
| screenOrientation | Stringa | Il motore JavaScript del dispositivo e del browser supportano l&#39;Orientamento del Dispositivo. Può essere orizzontale o verticale. |
| webGLRenderer | Stringa | Rendering del browser del driver grafico. |

>[!NOTE]
>
>I clienti che utilizzano l’SDK di Mobile non devono eseguire alcuna operazione per applicare questa funzionalità. I clienti che utilizzano at.js devono [eseguire l’aggiornamento alla versione 1.5.0 di at.js](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A) (o successiva).

È possibile scegliere più di una proprietà per i dispositivi mobili. Le selezioni multiple sono collegate tra loro con un operatore OR.

I clienti che utilizzano un&#39;integrazione personalizzata (non con at.js o l&#39;SDK mobile) possono raccogliere questi parametri e trasmetterli come parametri mbox.

1. Nell’interfaccia di [!DNL Target] fai clic su **[!UICONTROL Pubblico]** > **[!UICONTROL Crea pubblico]**.
1. Assegna un nome al pubblico e aggiungi una descrizione facoltativa.
1. Trascinamento della selezione **[!UICONTROL Mobile]** nel riquadro audience builder (generatore di pubblico).
1. Fai clic su **[!UICONTROL Seleziona]**, quindi scegli una delle seguenti opzioni:

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
1. Fai clic su **[!UICONTROL Fine]**.

L’illustrazione seguente mostra un pubblico che include i visitatori che utilizzano dispositivi mobili prodotti da Google.

![Targeting di dispositivi mobili](assets/target_mobile.png)

## Considerazioni

Quando esegui il targeting dei dispositivi mobili, considera le seguenti informazioni:

### Dispositivi di targeting con iOS 12.2 o versione successiva

A causa delle nuove modifiche introdotte in iOS 12.2, creazione di un pubblico con regole definite da [!UICONTROL Nome marketing del dispositivo] e [!UICONTROL Modello dispositivo] che specifica modelli iPhone è interessato. [!DNL Target] non può più eseguire il targeting degli utenti che hanno installato su di essi gli iPhone con iOS 12.2 (o versioni successive). Tuttavia, se tali utenti non dispongono di iOS 12.2 (o versioni successive), il targeting del modello iPhone continua a funzionare correttamente.

L’aggiornamento iOS 12.2 (o successivo) non influisce sull’identificazione dei seguenti modelli perché questi modelli non supportano l’aggiornamento ad iOS 12.2: iPhone, iPhone 3G, iPhone 3GS, iPhone 4, iPhone 4s, iPhone 5, iPhone 5c, iPad, iPad 2, display iPad / Retina, iPad Retina (4a generazione), iPod Touch 4 e iPod Touch 5.

### Dispositivi di targeting con Safari 14.0.2 (o versioni successive)

Quando si utilizzano regole mobili per indirizzare l’attività ai dispositivi che eseguono Safari versione 14.0.2 (o successiva) su macOS, a causa di un problema noto che coinvolge gli agenti utente Apple e DeviceAtlas, [!DNL Target] identifica Safari in modo non corretto sui dispositivi Mac e iPad. Questo problema verrà affrontato in futuro.

## Video di formazione: Creazione di tipi di pubblico

Questo video contiene informazioni sull&#39;utilizzo delle categorie di pubblico.

* Creazione di un pubblico
* Definizione delle categorie di pubblico

>[!VIDEO](https://video.tv.adobe.com/v/17392)
