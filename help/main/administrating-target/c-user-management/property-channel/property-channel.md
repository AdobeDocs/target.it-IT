---
keywords: aree di lavoro;gestire proprietà;autorizzazioni;configurazione prodotto;profilo prodotto;ruoli;progetto;osservatore;editor;approvatore;publisher
description: Scopri come creare aree di lavoro separate (profili di prodotto) e quindi assegnare agli utenti ruoli e autorizzazioni diversi per singole pagine, proprietà o siti web.
title: Quali sono le autorizzazioni per gli utenti Enterprise e come si utilizzano?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Administration & Configuration
role: Admin
exl-id: 838abe87-dba7-4274-97b4-31a7905846dc
source-git-commit: 12831d6584acc482db415629d7e70a18e39c47c2
workflow-type: tm+mt
source-wordcount: '3165'
ht-degree: 48%

---

# Autorizzazioni per gli utenti Enterprise

Le autorizzazioni per gli utenti Enterprise rappresentano un mezzo per amministrare formalmente l&#39;accesso degli utenti a [!DNL Adobe Target] a livello aziendale. Aggiungere utenti a [!DNL Target], assegnare le autorizzazioni in base ai ruoli e creare aree di lavoro per i team in base a reparti, posizioni globali, canali e altri raggruppamenti logici. È possibile assegnare agli utenti i ruoli di [!UICONTROL Observer], [!UICONTROL Editor], [!UICONTROL Approver] o [!UICONTROL Publisher].

{{permissions-update}}

## Determinare se si dispone dell&#39;accesso alle autorizzazioni per gli utenti aziendali

>[!NOTE]
>
>La funzionalità [!UICONTROL Properties and Permissions] è disponibile come parte della soluzione [!DNL Target] Premium. Non sono disponibili in [!DNL Target] Standard senza una licenza [!DNL Target] Premium.
>
>L&#39;implementazione di [!DNL Target] può utilizzare qualsiasi versione di at.js o [!DNL Adobe Experience Platform Web SDK].

Per verificare se la tua organizzazione dispone di una licenza Standard o Premium, fai clic sul collegamento [!UICONTROL Administration] nella parte superiore dell&#39;interfaccia utente di [!DNL Target].

* Clienti **[!DNL Target Standard]**: se è presente la scheda [!UICONTROL Users] ([!UICONTROL Administration > Users]) (e non la scheda [!UICONTROL Properties]), la tua organizzazione dispone di una licenza [!DNL Target Standard]. I clienti [!DNL Target Standard] devono seguire le istruzioni in [Utenti](/help/main/administrating-target/c-user-management/c-user-management/user-management.md) per aggiungere utenti e assegnare autorizzazioni in [!DNL Adobe Admin Console].

* Clienti **[!DNL Target Premium]**: se sono presenti la scheda [!UICONTROL Properties] ([!UICONTROL Administration > Properties]) e la scheda [!UICONTROL Users], la tua organizzazione dispone di una licenza [!DNL Target Premium]. I clienti [!DNL Target Premium] devono seguire le istruzioni contenute in questo articolo e in [Configurare le autorizzazioni Enterprise](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md).

## Prima di iniziare a utilizzare le autorizzazioni Enterprise

>[!IMPORTANT]
>
>Assicurati di aver letto la sezione [Avvertenze](/help/main/administrating-target/c-user-management/property-channel/property-channel.md#section_9714311B1CD9497A86F4910F8AE635E2) di seguito prima di procedere con le autorizzazioni Enterprise.

## Termini e definizioni utilizzati in questa sezione {#section_F8D229544FEA41C3BC2EFD1F95AA0116}

I termini seguenti vengono utilizzati in questa sezione e potrebbero essere nuovi per gli utenti che desiderano utilizzare la funzionalità Proprietà e autorizzazioni in [!DNL Target] Premium.

### Proprietà

Le proprietà sono simili per natura alle proprietà all&#39;interno di [!DNL Adobe Experience Platform] in quanto utilizzano uno snippet di codice univoco per differenziarle.

Una proprietà web è una libreria di regole e un codice incorporato. Una proprietà web può essere un raggruppamento di uno o più domini e sottodomini.

Le proprietà vengono abilitate aggiungendo una coppia nome/valore specifica come parametro con qualsiasi chiamata (chiamata Target, chiamata API e così via) a [!DNL Target].

Le proprietà appartengono a canali specifici (web, mobile, email o API/altro).

### Area di lavoro (profilo prodotto) {#workspace}

Un’area di lavoro consente a un’azienda di assegnare un gruppo specifico di utenti a un insieme specifico di proprietà. Un’area di lavoro è simile per vari aspetti a una suite di rapporti di [!DNL Adobe Analytics].

Nota: le aree di lavoro sono note come [!UICONTROL Product Profiles] in [!DNL Adobe Admin Console for Enterprise].

Se fai parte di un’azienda multinazionale, potresti avere un’area di lavoro per le pagine web, le proprietà o i siti europei e un’altra per le pagine web, le proprietà o i siti americani. Se fai parte di un’azienda multi-brand, potresti avere un’area di lavoro diversa per ciascuno dei marchi.

Gli utenti possono fare parte di più aree di lavoro e possono anche avere ruoli diversi all’interno di ogni area di lavoro.

Gli utenti possono avere visualizzazioni diverse di [!DNL Adobe Target] spostandosi tra le aree di lavoro, in modo analogo a come [!DNL Analytics] utenti hanno visualizzazioni diverse di [!DNL Analytics] spostandosi tra le suite di rapporti.

Le aree di lavoro possono includere tipi di pubblico, offerte di codice e attività completamente diversi.

Tutti i tipi di pubblico e le attività creati prima della migrazione del nuovo modello di autorizzazioni Enterprise sono raggruppati nel &quot;Workspace predefinito&quot; discusso di seguito.

Tutte le attività create tramite [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] e [!DNL Adobe Target Classic] fanno parte del &quot;Workspace predefinito&quot;.

### Area di lavoro predefinita

Tutte le aree di lavoro esistenti (profili prodotto) in [!DNL Admin Console] vengono unite in un&#39;unica area di lavoro denominata &quot;Default Workspace&quot; durante la migrazione dell&#39;organizzazione al nuovo modello di autorizzazioni Enterprise.

>[!IMPORTANT]
>
>Non eliminare l’area di lavoro predefinita.

Tutti i ruoli utente e l&#39;accesso a tutte le funzionalità di [!DNL Target] rimangono invariati rispetto a prima della migrazione al nuovo modello di autorizzazioni Enterprise.

### Gruppi di utenti

Puoi creare gruppi di utenti, ad esempio sviluppatori, analisti, addetti al marketing e dirigenti. Puoi quindi assegnare privilegi a più prodotti Adobe e aree di lavoro. Per assegnare a un nuovo membro del team tutti i privilegi appropriati per i diversi prodotti Adobe, sarà sufficiente aggiungerlo a un gruppo di utenti specifico.

### Ruoli e autorizzazioni {#roles-permissions}

I ruoli e le autorizzazioni determinano i livelli di accesso che gli utenti devono creare e gestire le attività nell&#39;implementazione di [!DNL Target]. In [!DNL Target] i ruoli includono:

| Ruolo | Descrizione |
|--- |--- |
| [!UICONTROL Approver] | Può creare, modificare, attivare o interrompere le attività. |
| [!UICONTROL Editor] | Può creare e modificare le attività prima che siano in diretta, ma non può approvare l’avvio di un’attività. |
| [!UICONTROL Observer] | Può visualizzare le attività, ma non può crearle o modificarle. |
| [!UICONTROL Publisher] | Simile al ruolo [!UICONTROL Observer] (può visualizzare le attività, ma non può crearle o modificarle). Tuttavia, il ruolo [!UICONTROL Publisher] dispone dell&#39;autorizzazione aggiuntiva per attivare le attività. |

### Canale

Il canale si riferisce al tipo di contenuto in cui vengono consegnate le attività [!DNL Target]: pagine Web, app mobili, messaggi e-mail e così via.

Quando crei un’attività, questa viene creata nell’area di lavoro attualmente selezionata. Nella prima finestra di dialogo sono visualizzate le opzioni di selezione del canale che consentono di scegliere il canale desiderato per l’attività: Web, App mobile, E-mail o Altro/API.

## Panoramica sulle autorizzazioni {#section_DC2172520DA84605B218A5E9FB6D187A}

Le informazioni seguenti spiegano il modo in cui le autorizzazioni sono state applicate in precedenza in [!DNL Target] e come vengono applicate utilizzando le funzionalità [!UICONTROL Properties] e [!UICONTROL Permissions].

La nuova funzionalità [!UICONTROL Permissions] consente di creare progetti diversi (denominati &quot;profili prodotto&quot; in [!DNL Adobe Admin Console for Enterprise]). I progetti ti consentono di assegnare a un singolo utente diverse autorizzazioni che ne determinano i diritti di accesso per ciascun progetto. Questi progetti distinti possono essere paragonati al modo in cui le suite di rapporti funzionano in [!DNL Adobe Analytics]. In ogni progetto possono essere inclusi utenti specifici con ruoli specifici applicabili a un insieme di proprietà. Di conseguenza, i clienti possono limitare l’accesso alla visualizzazione, alla modifica e all’approvazione ai propri utenti in base all’area geografica, all’ambiente (dev/stage/prod), al canale o ad altri criteri personalizzati, come illustrato di seguito:

![immagine autorizzazioni](assets/permissions.png)

Ad esempio, un utente specifico potrebbe avere accesso “approvato” ai siti Web americani, ma solo un accesso di “visualizzazione” sull&#39;applicazione mobile europea. Lo stesso utente potrebbe non avere alcun accesso neppure per visualizzare le attività offerte sulle proprietà Web e mobile nella regione APAC.

Il modello [!DNL Target] [!UICONTROL Permissions] dispone dei seguenti ruoli di autorizzazione (osservatore, editor, approvatore e osservatore). Il ruolo Osservatore non viene mostrato nelle illustrazioni di questo articolo.

![autorizzazioni_1 immagine](assets/permissions_1.png)

Ogni ruolo dispone di diversi livelli di autorizzazioni:

| Ruolo | Descrizione |
|--- |--- |
| Responsabile approvazione | Può creare, modificare, attivare o interrompere le attività. |
| Editor | Può creare e modificare le attività prima che siano in diretta, ma non può approvare l’avvio di un’attività. |
| Osservatore | Può visualizzare le attività, ma non può crearle o modificarle. |
| Editore | Simile al ruolo Osservatore (può visualizzare le attività, ma non può crearle o modificarle). Tuttavia, il ruolo Editore è anche autorizzato ad attivare le attività. |

È importante notare che il ruolo di ogni utente si applica a ogni pagina, proprietà o sito dell&#39;account che include i tag di [!DNL Target], come illustrato di seguito:

![autorizzazioni_2 immagine](assets/permissions_2.png)

Il nuovo modello [!DNL Target] [!UICONTROL Permissions] dispone degli stessi tre ruoli di autorizzazione (osservatore, editor e approvatore). È tuttavia possibile assegnare separatamente i ruoli delle autorizzazioni di un utente per singole pagine, proprietà o siti, come illustrato di seguito:

![autorizzazioni_3 immagine](assets/permissions_3.png)

In questo esempio, Jan dispone delle autorizzazioni da approvatore per la Homepage e il sito internet degli Stati Uniti e le autorizzazioni da osservatore per il sito francese.

Inoltre Jan non può visualizzare pagine, proprietà o siti di [!DNL Target] per i quali non dispone dell&#39;autorizzazione di visualizzazione, come illustrato di seguito:

![autorizzazioni_4 immagine](assets/permissions_4.png)

In questo esempio Jan non può visualizzare le pagine dei prodotti, il sito russo e il sito carriere.

## Scenari di utilizzo {#section_F3CE8576959E4F4CB13BEEED38311DD8}

I seguenti casi di utilizzo possono essere utili per comprendere come le proprietà, i progetti, i ruoli e le autorizzazioni consentono di raggiungere gli obiettivi di marketing con [!DNL Target]:

### Organizzazione multinazionale

Se fai parte di un’azienda multinazionale, potresti avere un’area di lavoro per le pagine web, le proprietà o i siti europei e un’altra per le pagine web, le proprietà o i siti americani. Dopo una riorganizzazione, utilizzando gli utenti tipo nelle illustrazioni di cui sopra, è possibile impostare le aree di lavoro e le autorizzazioni simili alle seguenti:

* **Jan**: Jan è il capo dell’ottimizzazione nel centro di eccellenza per le pagine Web degli Stati Uniti, le proprietà e i siti della sua organizzazione. Molto probabilmente dispone dei diritti di amministratore di sistema nel cloud Adobe Experience Cloud.

  Nel suo ruolo, ha le autorizzazioni di approvatore per la homepage degli Stati Uniti e il sito statunitense. Con l&#39;autorizzazione dell&#39;approvatore, può creare, modificare, attivare o interrompere le attività.

  Jan si consulta anche con il team di ottimizzazione in Francia e, pertanto, dispone delle autorizzazioni di osservatore per il sito Francia che le danno un accesso in sola lettura alle attività. Jan può visualizzare le attività, ma non può crearle o modificarle.

  Siccome Jan non ha un ruolo che richiede la sua visualizzazione delle pagine dei prodotti, del sito Russia, o del sito carriere, lei non può vedere le attività per quei siti.

* **Ernie**: Ernie è un Marketing Manager per l’organizzazione ed è responsabile del marketing negli Stati Uniti.

  Siccome Ernie è entrato di recente nell&#39;organizzazione e non ha esperienza con Target, dispone dei permessi editor per la homepage degli Stati Uniti, il sito degli Stati Uniti e le pagine dei prodotti. Con le autorizzazioni dell’editor, Ernie può creare e modificare le attività prima che siano live. Non può approvare l’avvio di un’attività: un utente con autorizzazione di approvazione, come Jan, deve approvare l’attività prima che possa essere messa in produzione.

  Siccome Ernie non ha un ruolo che richiede la sua visualizzazione del sito Russia, del sito Francia, o del sito carriere, non può vedere le attività per quei siti.

* **Diana**: Diana è ora un’analista per l’organizzazione e le sono stati concessi i permessi di osservatore per la homepage degli Stati Uniti, il sito degli Stati Uniti, le pagine dei prodotti, il sito Russia e il sito di Francia, che le consentono un accesso in sola lettura alle attività. Diana può visualizzare le attività, ma non può crearle o modificarle.

  Siccome Diana non ha alcun ruolo che richiede la sua visualizzazione del sito carriere, lei non può vedere le attività per quei siti.

### Organizzazione multi-brand

Se fai parte di un&#39;azienda multi-brand, potresti avere un&#39;area di lavoro separata per le pagine Web, le proprietà o i siti di ogni marca.

Dopo una riorganizzazione, utilizzando gli utenti tipo nelle illustrazioni di cui sopra, è possibile impostare i progetti e le autorizzazioni come di seguito:

* **Jan**: Jan è il capo dell’ottimizzazione nel centro di eccellenza di un’organizzazione sanitaria che opera nell’ambito dei prodotti ospedalieri e dei prodotti di consumo. Molto probabilmente dispone dei diritti di amministratore di sistema nel cloud Adobe Experience Cloud.

  Nel suo ruolo dispone delle autorizzazioni di approvatore per il sito ospedaliero. Con l&#39;autorizzazione dell&#39;approvatore, può creare, modificare, attivare o interrompere le attività.

  Jan si consulta inoltre con il team di ottimizzazione nell&#39;ambito dei prodotti di consumo e, pertanto, dispone delle autorizzazioni di osservatore per quel sito, che le consentono l&#39;accesso in sola lettura alle attività. Jan può visualizzare le attività, ma non può crearle o modificarle.

* **Ernie:** Ernie è un Marketing Manager per l’organizzazione ed è responsabile del marketing nell’ambito dei prodotti di consumo.

  Siccome Ernie è entrato di recente nell&#39;organizzazione e non ha esperienza con Target, dispone dell&#39;autorizzazione Editor per il sito consumatore. Con le autorizzazioni dell’editor, Ernie può creare e modificare le attività prima che siano live. Non può approvare l’avvio di un’attività: un utente con autorizzazioni di approvazione per il sito consumatore, ma non Jan in questo scenario, deve approvare l’attività prima che possa essere messa in produzione.

  Siccome Ernie non ha un ruolo che richiede la sua visualizzazione del sito dell&#39;ospedale, non può vedere le attività per quel sito.

* **Diana**: Diana è ora un’analista per l’organizzazione e le sono stati concessi i permessi di osservatore per il sito dell’ospedale e il sito consumatore, che le consentono un accesso in sola lettura alle attività. Diana può visualizzare le attività, ma non può crearle o modificarle.

## Punti di contatto per proprietà e autorizzazioni dell’interfaccia utente di Target {#section_3414371393BB42999A268628B5456EC9}

La nuova funzionalità delle autorizzazioni può essere vista in varie posizioni nell&#39;interfaccia utente di [!DNL Target].

* **Elenco a discesa Workspace (profilo prodotto):** L&#39;elenco a discesa Workspace viene visualizzato nella parte superiore delle pagine [!UICONTROL Activities], [!UICONTROL Audiences] e [!UICONTROL Offers]. Seleziona l&#39;area di lavoro desiderata per filtrare l&#39;elenco e visualizzare solo gli elementi nell&#39;area di lavoro selezionata.

* **Creazione attività:** Quando si crea un&#39;attività, questa viene creata nell&#39;area di lavoro attualmente selezionata. Nella prima finestra di dialogo sono visualizzate le opzioni di selezione del canale che consentono di scegliere il canale desiderato per l’attività: Web, App mobile, E-mail o Altro/API.

* **Creazione pubblico:** Quando si crea un pubblico, questo viene creato nell&#39;area di lavoro attualmente selezionata.
* **Elenco tipi di pubblico:** È possibile spostare i tipi di pubblico tra aree di lavoro utilizzando l&#39;opzione [!UICONTROL More Actions] > [!DNL Move] nella pagina [!UICONTROL Audiences].
* **Creazione offerta:** Quando si crea un&#39;offerta, questa viene creata nell&#39;area di lavoro attualmente selezionata.
* **Pagina delle proprietà (Amministrazione > Proprietà):** È possibile utilizzare la casella [!UICONTROL Search] per eseguire ricerche nell&#39;elenco [!UICONTROL Property].

## Avvertenze {#section_9714311B1CD9497A86F4910F8AE635E2}

Quando si utilizzano o si configurano proprietà e autorizzazioni in [!DNL Target] Premium, tenere presente quanto segue:

* **Importante**: non eliminare le aree di lavoro con le attività. Se elimini un’area di lavoro con attività, contatta l’Assistenza clienti per ripristinarle.
* Quando usi la vista Tutte le aree di lavoro:

   * Puoi visualizzare le attività, i destinatari e le offerte per tutti gli spazi di lavoro e le autorizzazioni per accedere.
   * Quando si seleziona la visualizzazione [!UICONTROL All My Workspaces], viene aggiunta una nuova colonna alla pagina Attività, Tipi di pubblico e Offerte. In questa colonna sono elencate l&#39;area di lavoro e l&#39;autorizzazione utente associate all&#39;elemento (osservatore, editor o approvatore).
   * Quando crei un&#39;attività, un pubblico o un&#39;offerta nella vista Tutte le aree di lavoro, devi selezionare l&#39;area di lavoro in cui deve essere creato l&#39;elemento. Possono essere selezionate solamente le aree di lavoro per cui si possiedono le autorizzazioni dell&#39;editor o dell&#39;approvatore.
   * Quando copi un&#39;attività, un pubblico o un&#39;offerta nella vista Tutte le aree di lavoro, devi selezionare l&#39;area di lavoro in cui copiare l&#39;elemento. Possono essere selezionate solamente le aree di lavoro per cui si possiedono le autorizzazioni dell&#39;editor o dell&#39;approvatore.

* Qualsiasi impostazione nelle pagine [!UICONTROL Administration] seguenti può essere controllata da qualsiasi [!UICONTROL Approver] in qualsiasi area di lavoro:

   * Compositore esperienza visivo
   * Generazione di rapporti
   * Configurazione Scene7
   * Implementazione
   * Proprietà
   * Host
   * Ambienti
   * Token di risposta
   * Utenti

* Gli utenti non possono spostare le risorse da un&#39;area di lavoro (profilo prodotto) a un&#39;altra. Copy, tuttavia, è supportato.
* Quando si visualizzano i tipi di pubblico dalla pagina [!DNL Audiences], questa viene caricata più lentamente del previsto. Se interagite in qualsiasi modo con la barra di ricerca, la pagina dei tipi di pubblico si visualizzerà più velocemente. Questo problema è noto e verrà risolto in un prossimo aggiornamento. Questo problema non influisce sulla selezione dei destinatari durante il flusso di lavoro della creazione di attività.
* Le risorse seguenti fanno parte del nuovo modello di autorizzazioni Enterprise:

   * Attività, tipi di pubblico e offerte di codice creati in [!DNL Target Standard/Premium] sono disponibili per l&#39;utilizzo dopo l&#39;abilitazione del cliente per le autorizzazioni. (Nota: i clienti devono avere diritto a [!DNL Target Premium].)
   * Le proprietà possono essere aggiunte alle attività esistenti nel Workspace predefinito; tuttavia, questo approccio è soggetto a modifiche.
   * Solo le nuove risorse (ad esempio attività, offerte di codice e tipi di pubblico) create all’interno di Target Premium (dopo l’abilitazione delle autorizzazioni Enterprise) sono disponibili per limitare le autorizzazioni.
   * Le risorse esterne sono disponibili solo per gli utenti nell&#39;area di lavoro predefinita. Il ruolo di un utente nell&#39;area di lavoro predefinita si applica globalmente (a tutte le richieste Target e a tutte le risorse Target).

* Le risorse seguenti *non* fanno parte del nuovo modello di autorizzazioni Enterprise:

   * Offerte immagine
   * Tutte le risorse di Recommendations, inclusi Libreria criteri, Libreria progettazioni, Catalogo, Configurazione Recommendations.
   * Le risorse esistenti (ad esempio attività, offerte di codice e tipi di pubblico) create all’interno di Target Premium prima di abilitare le autorizzazioni Enterprise possono essere copiate ma non possono essere spostate in altre aree di lavoro.
   * Le attività, i tipi di pubblico, le offerte basate su codice, le offerte immagini o qualsiasi altra risorsa creata utilizzando le soluzioni o i metodi seguenti non possono essere controllate dal modello di autorizzazioni Enterprise, ma fanno parte di Workspace predefinito: Target Classic, Adobe Experience Manager (AEM), Adobe Mobile Services e le risorse create tramite API. Le risorse create tramite API includono le attività, i tipi di pubblico, le offerte basate su codice e le offerte di immagini.
   * Le offerte di immagini (le risorse archiviate in `https://[tenantName].marketing.adobe.com/content/mac/[tenantName]/target/offers.html#image-library` non possono essere attualmente controllate dal modello di autorizzazioni Enterprise.
   * clickTracking e reindirizzamenti funzionano quando il collegamento di destinazione o la pagina di destinazione fanno parte di una proprietà inclusa nell’attività. Inoltre, clickTracking potrebbe non funzionare quando si utilizza la funzione `targetPageParams()`. La funzione suggerita è `targetPageParamsAll()`.

  [!DNL Target] attualmente richiede un token `at_property` per essere presente in qualsiasi pagina in cui si verifica il tracciamento. Se il token è (1) non presente, (2) non rilevato al momento della configurazione dell’attività (all’interno del Compositore esperienza visivo), o (3) non passato alla chiamata di destinazione clickTracking tramite la funzione `targetPageParamsAll()`, la metrica non viene incrementata e viene visualizzata come &quot;0&quot;.

  Lo stesso vale per le attività che utilizzano i reindirizzamenti. La pagina di destinazione deve avere un token `at_property` ed essere riconosciuta al momento della configurazione all&#39;interno di Compositore esperienza visivo.

  In una versione futura, Target lavorerà su pagine in cui non è presente alcun token `at_property` o su pagine in cui è presente un token `at_property` diverso.

* La funzionalità Autorizzazioni Enterprise non è supportata nelle chiamate API di Adobe Developer.

## Domande frequenti {#faqs}

Le domande frequenti sulle autorizzazioni Enterprise includono:

### Cosa succede se un utente dispone di più ruoli e autorizzazioni? {#multiple-roles}

Se un utente dispone di più ruoli e autorizzazioni, viene applicato il ruolo con le autorizzazioni dell’utente che assume. Ad esempio, se un utente ha [!UICONTROL Observer] e [!UICONTROL Approver] ruoli, viene applicato il ruolo [!UICONTROL Approver].

### Posso spostare un&#39;attività da un&#39;area di lavoro a un&#39;altra?

Sfortunatamente non è possibile spostare le attività da un&#39;area di lavoro a un&#39;altra. Tuttavia, puoi copiare un’attività in qualsiasi area di lavoro sapendo che i dati di reporting non vengono trasferiti. Per ulteriori informazioni, vedere “Copia/modifica di un&#39;attività quando si utilizzano aree di lavoro” in [Copia/modifica di un&#39;attività quando si utilizzano aree di lavoro](/help/main/c-activities/edit-activity.md#section_45A92E1DD3934523B07E71EF90C4F8B6).

Le attività create prima della migrazione continuano a essere eseguite nello stesso modo nell&#39;area di lavoro predefinita, a meno che non siano proprietà modificate e assegnate. Le attività in un’area di lavoro specifica rispettano la proprietà assegnata a tale area di lavoro e, pertanto, il comportamento potrebbe non rimanere invariato rispetto a prima della migrazione.

### È possibile spostare un pubblico da un’area di lavoro a un’altra? {#move-audience}

Sì, è possibile spostare i tipi di pubblico tra aree di lavoro utilizzando l&#39;opzione [!UICONTROL More Actions] nella pagina [!UICONTROL Audiences].

1. Fare clic sul pulsante **[!UICONTROL More Actions]** (i tre puntini di sospensione), quindi fare clic su **[!UICONTROL Move]**.

   ![Altre azioni > Sposta](/help/main/administrating-target/c-user-management/property-channel/assets/move-audience.png)

1. Selezionare l&#39;area di lavoro desiderata dall&#39;elenco a discesa **[!UICONTROL Workspace]**, quindi fare clic su **[!UICONTROL Move]**.

   ![Selezionare il pubblico desiderato per passare alla nuova area di lavoro](/help/main/administrating-target/c-user-management/property-channel/assets/workspace-move.png)

>[!NOTE]
>
>Devi disporre dei diritti appropriati per modificare un pubblico. Inoltre, il pubblico non deve essere utilizzato in altre attività. Se il pubblico è utilizzato in altre attività e desideri comunque spostarlo in un’altra area di lavoro, rimuovilo dalle altre attività in cui viene utilizzato.

### Perché viene visualizzato un messaggio di errore a indicare che nessuna proprietà è associata a questa attività, anche se è stata assegnata una proprietà?

Se si implementa [!DNL Target] con i tag in [!DNL Adobe Experience Platform] e si riceve un messaggio di errore che indica che non vi è alcuna proprietà associata all&#39;attività, passare il parametro `at_property` con la funzione `targetPageParams`.

### Se una pagina reindirizzata e l’URL attività appartengono a proprietà diverse, vengono registrate le conversioni con tracciamento dei clic?

Il tracciamento dei clic non viene registrato nelle pagine in cui la pagina e l’URL attività appartengono a proprietà diverse.

Considera lo scenario seguente:

* Pagina1 appartiene a Proprietà1.
* Pagina2 appartiene a Proprietà2.
* Nell’attività, la Pagina 1 reindirizzerà a Pagina 2, contenente le tracce di clic.

Quando un visitatore apre Pagina1 in un browser, viene reindirizzato a Pagina2. Poiché la Pagina2 non è qualificata per consegnare l’attività, la chiamata di Target non contiene le tracce di clic nella risposta.

Se la pagina di reindirizzamento e l’URL attività appartengono alla stessa proprietà, le tracce di clic funzionano come previsto. Per ulteriori informazioni, consulta [Tracciamento dei clic](/help/main/c-activities/r-success-metrics/click-tracking.md).

## Video di formazione

I video seguenti contengono ulteriori informazioni sui concetti descritti in questo articolo.

### Video di formazione: Video di formazione sulle autorizzazioni Enterprise ![Icona panoramica](/help/main/assets/overview.png)

Finalità di apprendimento:

* I tre livelli di ruolo disponibili per gli utenti di Adobe Target
* I concetti di Proprietà e Aree di lavoro e come funzionano questi limiti e raggruppamenti per consentire il controllo sui livelli di accesso degli utenti
* Diversi esempi di Proprietà da considerare per la tua organizzazione

>[!VIDEO](https://video.tv.adobe.com/v/19042/)

### Orario ufficio: [!DNL Target] aree di lavoro Premium

Questo video è una registrazione di “Office Hours”, un’iniziativa condotta dal team di assistenza clienti di Adobe.

* Creare un’area di lavoro (profilo prodotto)
* Creazione delle proprietà
* Aggiunta di utenti
* Aggiornamento dell’implementazione

>[!NOTE]
>
>L&#39;interfaccia utente del menu [!DNL Target] [!UICONTROL Administration] (in precedenza [!UICONTROL Setup]) è stata riprogettata per fornire prestazioni migliori, ridurre il tempo di manutenzione necessario per il rilascio di nuove funzionalità e migliorare l&#39;esperienza utente nel prodotto. Le informazioni contenute nel video seguente sono corrette; tuttavia, le opzioni potrebbero trovarsi in posizioni leggermente diverse.

>[!VIDEO](https://video.tv.adobe.com/v/23643/)
