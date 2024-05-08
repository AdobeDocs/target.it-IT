---
keywords: aree di lavoro;gestire proprietà;autorizzazioni;configurazione prodotto;profilo prodotto;ruoli;progetto;osservatore;editor;approvatore;publisher
description: Scopri come creare aree di lavoro separate (profili di prodotto) e quindi assegnare agli utenti ruoli e autorizzazioni diversi per singole pagine, proprietà o siti web.
title: Quali sono le autorizzazioni per gli utenti Enterprise e come si utilizzano?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."
feature: Administration & Configuration
role: Admin
exl-id: 838abe87-dba7-4274-97b4-31a7905846dc
source-git-commit: 5e86d3a95dad291f6c876f126568ba685ff32670
workflow-type: tm+mt
source-wordcount: '3171'
ht-degree: 48%

---

# Autorizzazioni per gli utenti Enterprise

Le autorizzazioni per gli utenti Enterprise rappresentano un mezzo per amministrare formalmente l’accesso degli utenti a livello aziendale a [!DNL Adobe Target]. Aggiungi utenti a [!DNL Target], assegna le autorizzazioni in base ai loro ruoli e crea aree di lavoro per i team in base a reparto, posizione globale, canali e altri raggruppamenti logici. Puoi assegnare agli utenti i ruoli di [!UICONTROL Observer], [!UICONTROL Editor], [!UICONTROL Approver], o [!UICONTROL Publisher].

## Determinare se si dispone dell&#39;accesso alle autorizzazioni per gli utenti aziendali

>[!NOTE]
>
>[!UICONTROL Properties and Permissions] funzionalità è disponibile come parte del [!DNL Target] Soluzione Premium. Non sono disponibili in [!DNL Target] Standard senza una licenza [!DNL Target] Premium.
>
>Il tuo [!DNL Target] L&#39;implementazione può utilizzare qualsiasi versione di at.js oppure [!DNL Adobe Experience Platform Web SDK].

Per verificare se la tua organizzazione dispone di una licenza Standard o Premium, fai clic sul pulsante [!UICONTROL Administration] collegamento nella parte superiore della sezione [!DNL Target] UI.

* **[!DNL Target Standard]Clienti**: se trovi il [!UICONTROL Users] scheda ([!UICONTROL Administration > Users]) (e non il [!UICONTROL Properties] ), la tua organizzazione dispone di un [!DNL Target Standard] licenza. [!DNL Target Standard] I clienti devono seguire le istruzioni riportate in [Utenti](/help/main/administrating-target/c-user-management/c-user-management/user-management.md) per aggiungere utenti e assegnare autorizzazioni in [!DNL Adobe Admin Console].

* **[!DNL Target Premium]Clienti**: se trovi il [!UICONTROL Properties] scheda ([!UICONTROL Administration > Properties]) e [!UICONTROL Users] , la tua organizzazione dispone di un [!DNL Target Premium] licenza. I clienti [!DNL Target Premium] devono seguire le istruzioni contenute in questo articolo e in [Configurare le autorizzazioni Enterprise](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md).

## Prima di iniziare a utilizzare le autorizzazioni Enterprise

>[!IMPORTANT]
>
>Assicurati di aver letto [Avvertenze](/help/main/administrating-target/c-user-management/property-channel/property-channel.md#section_9714311B1CD9497A86F4910F8AE635E2) prima di procedere con le autorizzazioni Enterprise.

## Termini e definizioni utilizzati in questa sezione {#section_F8D229544FEA41C3BC2EFD1F95AA0116}

I termini seguenti vengono utilizzati in questa sezione e potrebbero essere nuovi per gli utenti che desiderano utilizzare la funzionalità Proprietà e Autorizzazioni in [!DNL Target] Premium.

### Proprietà

Le proprietà sono simili per natura alle proprietà all’interno di [!DNL Adobe Experience Platform] in quanto utilizzano uno snippet di codice univoco per differenziarli.

Una proprietà web è una libreria di regole e un codice incorporato. Una proprietà web può essere un raggruppamento di uno o più domini e sottodomini.

Le proprietà vengono abilitate aggiungendo una coppia nome/valore specifica come parametro con qualsiasi chiamata (chiamata Target, chiamata API e così via) a [!DNL Target].

Le proprietà appartengono a canali specifici (web, mobile, email o API/altro).

### Area di lavoro (profilo prodotto) {#workspace}

Un’area di lavoro consente a un’azienda di assegnare un gruppo specifico di utenti a un insieme specifico di proprietà. Un’area di lavoro è simile per vari aspetti a una suite di rapporti di [!DNL Adobe Analytics].

Nota: le aree di lavoro sono note come [!UICONTROL Product Profiles] nel [!DNL Adobe Admin Console for Enterprise].

Se fai parte di un’azienda multinazionale, potresti avere un’area di lavoro per le pagine web, le proprietà o i siti europei e un’altra per le pagine web, le proprietà o i siti americani. Se fai parte di un’azienda multi-brand, potresti avere un’area di lavoro diversa per ciascuno dei marchi.

Gli utenti possono fare parte di più aree di lavoro e possono anche avere ruoli diversi all’interno di ogni area di lavoro.

Gli utenti possono avere diverse visualizzazioni di [!DNL Adobe Target] spostandosi tra le aree di lavoro, in modo simile a come [!DNL Analytics] gli utenti hanno visualizzazioni diverse di [!DNL Analytics] spostandosi tra le diverse suite di rapporti.

Le aree di lavoro possono includere tipi di pubblico, offerte di codice e attività completamente diversi.

Tutti i tipi di pubblico e le attività creati prima della migrazione del nuovo modello di autorizzazioni Enterprise sono raggruppati nell’&quot;Area di lavoro predefinita&quot;, discussa di seguito.

Tutte le attività create tramite [!DNL Adobe Experience Manager] (AEM) [!DNL Adobe Mobile Services], e [!DNL Adobe Target Classic] fanno parte di &quot;Default Workspace&quot; (Area di lavoro predefinita).

### Area di lavoro predefinita

Tutte le aree di lavoro esistenti (profili prodotto) in [!DNL Admin Console] vengono uniti in un’unica area di lavoro denominata &quot;Area di lavoro predefinita&quot; durante la migrazione dell’organizzazione al nuovo modello di autorizzazioni Enterprise.

>[!IMPORTANT]
>
>Non eliminare l’area di lavoro predefinita.

Tutti i ruoli utente e accesso a tutti [!DNL Target] Le funzionalità rimanevano invariate rispetto al periodo precedente la migrazione al nuovo modello di autorizzazioni Enterprise.

### Gruppi di utenti

Puoi creare gruppi di utenti, ad esempio sviluppatori, analisti, addetti al marketing e dirigenti. È quindi possibile assegnare privilegi a più prodotti di Adobe e aree di lavoro. Per assegnare a un nuovo membro del team tutti i privilegi appropriati per i diversi prodotti Adobe, sarà sufficiente aggiungerlo a un gruppo di utenti specifico.

### Ruoli e autorizzazioni {#roles-permissions}

I ruoli e le autorizzazioni determinano i livelli di accesso che gli utenti devono creare e gestire le attività nel [!DNL Target] implementazione. In entrata [!DNL Target], i ruoli includono quanto segue:

| Ruolo | Descrizione |
|--- |--- |
| [!UICONTROL Approver] | Può creare, modificare, attivare o interrompere le attività. |
| [!UICONTROL Editor] | Può creare e modificare le attività prima che siano in diretta, ma non può approvare l’avvio di un’attività. |
| [!UICONTROL Observer] | Può visualizzare le attività, ma non può crearle o modificarle. |
| [!UICONTROL Publisher] | Simile a [!UICONTROL Observer] ruolo (può visualizzare le attività, ma non può crearle o modificarle). Tuttavia, il [!UICONTROL Publisher] Il ruolo dispone dell&#39;autorizzazione aggiuntiva per attivare le attività. |

### Canale

Il canale si riferisce al tipo di contenuto in cui il [!DNL Target] Le attività vengono distribuite: pagine Web, app mobili, messaggi e-mail e così via.

Quando crei un’attività, questa viene creata nell’area di lavoro attualmente selezionata. Nella prima finestra di dialogo sono visualizzate le opzioni di selezione del canale che consentono di scegliere il canale desiderato per l’attività: Web, App mobile, E-mail o Altro/API.

## Panoramica sulle autorizzazioni {#section_DC2172520DA84605B218A5E9FB6D187A}

Le informazioni seguenti spiegano il modo in cui le autorizzazioni sono state applicate in precedenza in [!DNL Target] e come vengono applicati utilizzando [!UICONTROL Properties] e [!UICONTROL Permissions] funzionalità.

Il nuovo [!UICONTROL Permissions] Questa funzionalità consente di creare progetti diversi (denominati &quot;profili di prodotto&quot; nel [!DNL Adobe Admin Console for Enterprise]). I progetti ti consentono di assegnare a un singolo utente diverse autorizzazioni che ne determinano i diritti di accesso per ciascun progetto. Questi progetti distinti possono essere paragonati al modo in cui le suite di rapporti funzionano in [!DNL Adobe Analytics]. In ogni progetto possono essere inclusi utenti specifici con ruoli specifici applicabili a un insieme di proprietà. Di conseguenza, i clienti possono limitare l’accesso alla visualizzazione, alla modifica e all’approvazione ai propri utenti in base all’area geografica, all’ambiente (dev/stage/prod), al canale o ad altri criteri personalizzati, come illustrato di seguito:

![immagine autorizzazioni](assets/permissions.png)

Ad esempio, un utente specifico potrebbe avere accesso “approvato” ai siti Web americani, ma solo un accesso di “visualizzazione” sull&#39;applicazione mobile europea. Lo stesso utente potrebbe non avere alcun accesso neppure per visualizzare le attività offerte sulle proprietà Web e mobile nella regione APAC.

Il [!DNL Target] [!UICONTROL Permissions] Il modello dispone dei seguenti ruoli di autorizzazione (osservatore, editor, approvatore e osservatore). Il ruolo Osservatore non viene mostrato nelle illustrazioni di questo articolo.

![immagine permissions_1](assets/permissions_1.png)

Ogni ruolo dispone di diversi livelli di autorizzazioni:

| Ruolo | Descrizione |
|--- |--- |
| Responsabile approvazione | Può creare, modificare, attivare o interrompere le attività. |
| Editor | Può creare e modificare le attività prima che siano in diretta, ma non può approvare l’avvio di un’attività. |
| Osservatore | Può visualizzare le attività, ma non può crearle o modificarle. |
| Editore | Simile al ruolo Osservatore (può visualizzare le attività, ma non può crearle o modificarle). Tuttavia, il ruolo Editore è anche autorizzato ad attivare le attività. |

È importante notare che il ruolo di ogni utente si applica a ogni pagina, proprietà o sito dell&#39;account che include i tag di [!DNL Target], come illustrato di seguito:

![immagine permissions_2](assets/permissions_2.png)

Il nuovo [!DNL Target] [!UICONTROL Permissions] Il modello dispone degli stessi tre ruoli di autorizzazione (osservatore, editor e approvatore); è tuttavia possibile assegnare separatamente i ruoli delle autorizzazioni di un utente per singole pagine, proprietà o siti, come illustrato di seguito:

![immagine permissions_3](assets/permissions_3.png)

In questo esempio, Jan dispone delle autorizzazioni da approvatore per la Homepage e il sito internet degli Stati Uniti e le autorizzazioni da osservatore per il sito francese.

Inoltre, Jan non può visualizzare pagine, proprietà o siti in [!DNL Target] che non è autorizzata a visualizzare, come illustrato di seguito:

![immagine permissions_4](assets/permissions_4.png)

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

* **Elenco a discesa Area di lavoro (profilo prodotto):** L’elenco a discesa Workspace viene visualizzato nella parte superiore della sezione [!UICONTROL Activities], [!UICONTROL Audiences], e [!UICONTROL Offers] pagine. Seleziona l&#39;area di lavoro desiderata per filtrare l&#39;elenco e visualizzare solo gli elementi nell&#39;area di lavoro selezionata.

  ![immagine a discesa workspace](assets/workspace_drop-down.png)

* **Creazione attività:** Quando crei un’attività, questa viene creata nell’area di lavoro attualmente selezionata. Nella prima finestra di dialogo sono visualizzate le opzioni di selezione del canale che consentono di scegliere il canale desiderato per l’attività: Web, App mobile, E-mail o Altro/API.

  ![immagine channel_options](assets/channel_options.png)

* **Creazione di pubblico:** Quando crei un pubblico, questo viene creato nell’area di lavoro attualmente selezionata.
* **Elenco pubblico:** È possibile spostare i tipi di pubblico tra aree di lavoro utilizzando [!UICONTROL More Actions] > [!DNL Move] opzione sul [!UICONTROL Audiences] pagina.
* **Creazione di offerte:** Quando crei un’offerta, questa viene creata nell’area di lavoro attualmente selezionata.
* **Pagina Proprietà (Amministrazione > Proprietà):** È possibile utilizzare [!UICONTROL Search] casella per eseguire la ricerca [!UICONTROL Property] elenco.

  ![immagine properties_list](assets/properties_list.png)

## Avvertenze {#section_9714311B1CD9497A86F4910F8AE635E2}

Quando utilizzi o configuri proprietà e autorizzazioni in, tieni presente quanto segue: [!DNL Target] Premium:

* **Importante**: non eliminare le aree di lavoro con le attività. Se elimini un’area di lavoro con attività, contatta l’Assistenza clienti per ripristinarle.
* Quando usi la vista Tutte le aree di lavoro:

   * Puoi visualizzare le attività, i destinatari e le offerte per tutti gli spazi di lavoro e le autorizzazioni per accedere.
   * Quando selezioni il [!UICONTROL All My Workspaces] viene aggiunta una nuova colonna alla pagina Attività, Tipi di pubblico e Offerte. In questa colonna sono elencate l&#39;area di lavoro e l&#39;autorizzazione utente associate all&#39;elemento (osservatore, editor o approvatore).
   * Quando crei un&#39;attività, un pubblico o un&#39;offerta nella vista Tutte le aree di lavoro, devi selezionare l&#39;area di lavoro in cui deve essere creato l&#39;elemento. Possono essere selezionate solamente le aree di lavoro per cui si possiedono le autorizzazioni dell&#39;editor o dell&#39;approvatore.
   * Quando copi un&#39;attività, un pubblico o un&#39;offerta nella vista Tutte le aree di lavoro, devi selezionare l&#39;area di lavoro in cui copiare l&#39;elemento. Possono essere selezionate solamente le aree di lavoro per cui si possiedono le autorizzazioni dell&#39;editor o dell&#39;approvatore.

* Qualsiasi impostazione sui seguenti [!UICONTROL Administration] Le pagine possono essere controllate da qualsiasi [!UICONTROL Approver] in qualsiasi area di lavoro:

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

   * Attività, tipi di pubblico e offerta di codice creati in [!DNL Target Standard/Premium] sono disponibili per l’uso dopo che il cliente è stato abilitato per le autorizzazioni. (Nota: i clienti devono avere il diritto di [!DNL Target Premium].)
   * È possibile aggiungere proprietà alle attività esistenti nell’area di lavoro predefinita; tuttavia, questo approccio è soggetto a modifiche.
   * Solo le nuove risorse (come attività, offerte di codice e tipi di pubblico) create all&#39;interno di Target Premium (dopo l&#39;abilitazione delle autorizzazioni Enterprise) sono disponibili per limitare le autorizzazioni.
   * Le risorse esterne sono disponibili solo per gli utenti nell&#39;area di lavoro predefinita. Il ruolo di un utente nell&#39;area di lavoro predefinita si applica globalmente (a tutte le richieste Target e a tutte le risorse Target).

* Le risorse seguenti *non* fanno parte del nuovo modello di autorizzazioni Enterprise:

   * Offerte immagine
   * Tutte le risorse di Recommendations, inclusi Libreria criteri, Libreria progettazioni, Catalogo, Configurazione Recommendations.
   * Le risorse esistenti (ad esempio attività, offerte di codice e tipi di pubblico) create in Target Premium prima di abilitare le autorizzazioni Enterprise possono essere copiate ma non possono essere spostate in altre aree di lavoro.
   * Le attività, i tipi di pubblico, le offerte basate su codice, le offerte immagini o qualsiasi altra risorsa creata utilizzando le soluzioni o i metodi seguenti non possono essere controllate dal modello di autorizzazioni Enterprise, ma fanno parte dell’Area di lavoro predefinita: Target Classic, Adobe Experience Manager (AEM), Adobe Mobile Services e le risorse create tramite API. Le risorse create tramite API includono le attività, i tipi di pubblico, le offerte basate su codice e le offerte di immagini.
   * Offerte di immagini (risorse memorizzate in `https://[tenantName].marketing.adobe.com/content/mac/[tenantName]/target/offers.html#image-library` non può essere attualmente controllato dal modello di autorizzazioni Enterprise.
   * clickTracking e reindirizzamenti funzionano quando il collegamento di destinazione o la pagina di destinazione fanno parte di una proprietà inclusa nell’attività. Inoltre, clickTracking potrebbe non funzionare quando si utilizza `targetPageParams()` funzione. La funzione suggerita è `targetPageParamsAll()`.

  [!DNL Target] attualmente richiede un `at_property` deve essere presente in qualsiasi pagina in cui si verifica il tracciamento. Se il token è (1) non presente, (2) non rilevato al momento della configurazione dell’attività (all’interno del Compositore esperienza visivo), o (3) non passato alla chiamata di destinazione clickTracking tramite il `targetPageParamsAll()` , la metrica non viene incrementata e viene visualizzata come &quot;0&quot;.

  Lo stesso vale per le attività che utilizzano i reindirizzamenti. La pagina di destinazione deve avere un token `at_property` ed essere riconosciuta al momento della configurazione all&#39;interno di Compositore esperienza visivo.

  In una versione futura, Target lavorerà su pagine in cui non è presente alcun token `at_property` o su pagine in cui è presente un token `at_property` diverso.

* La funzionalità Autorizzazioni Enterprise non è supportata nelle chiamate API di Adobe Developer.

## Domande frequenti {#faqs}

Le domande frequenti sulle autorizzazioni Enterprise includono:

### Cosa succede se un utente dispone di più ruoli e autorizzazioni? {#multiple-roles}

Se un utente dispone di più ruoli e autorizzazioni, viene applicato il ruolo con le autorizzazioni dell’utente che assume. Ad esempio, se un utente ha [!UICONTROL Observer] e [!UICONTROL Approver] ruoli, il [!UICONTROL Approver] ruolo applicato.

### Posso spostare un&#39;attività da un&#39;area di lavoro a un&#39;altra?

Sfortunatamente non è possibile spostare le attività da un&#39;area di lavoro a un&#39;altra. Tuttavia, puoi copiare un’attività in qualsiasi area di lavoro sapendo che i dati di reporting non vengono trasferiti. Per ulteriori informazioni, vedere “Copia/modifica di un&#39;attività quando si utilizzano aree di lavoro” in [Copia/modifica di un&#39;attività quando si utilizzano aree di lavoro](/help/main/c-activities/edit-activity.md#section_45A92E1DD3934523B07E71EF90C4F8B6).

Le attività create prima della migrazione continuano a essere eseguite nello stesso modo nell&#39;area di lavoro predefinita, a meno che non siano proprietà modificate e assegnate. Le attività in un’area di lavoro specifica rispettano la proprietà assegnata a tale area di lavoro e, pertanto, il comportamento potrebbe non rimanere invariato rispetto a prima della migrazione.

### È possibile spostare un pubblico da un’area di lavoro a un’altra? {#move-audience}

Sì, puoi spostare i tipi di pubblico tra aree di lavoro utilizzando [!UICONTROL More Actions] opzione sul [!UICONTROL Audiences] pagina.

1. Fai clic su **[!UICONTROL More Actions]** (i tre puntini di sospensione), quindi fare clic su **[!UICONTROL Move]**.

   ![Altre azioni > Sposta](/help/main/administrating-target/c-user-management/property-channel/assets/move-audience.png)

1. Seleziona l’area di lavoro desiderata da **[!UICONTROL Workspace]** , quindi fai clic su **[!UICONTROL Move]**.

   ![Seleziona il pubblico desiderato per passare alla nuova area di lavoro](/help/main/administrating-target/c-user-management/property-channel/assets/workspace-move.png)

>[!NOTE]
>
>Devi disporre dei diritti appropriati per modificare un pubblico. Inoltre, il pubblico non deve essere utilizzato in altre attività. Se il pubblico è utilizzato in altre attività e desideri comunque spostarlo in un’altra area di lavoro, rimuovilo dalle altre attività in cui viene utilizzato.

### Perché viene visualizzato un messaggio di errore a indicare che nessuna proprietà è associata a questa attività, anche se è stata assegnata una proprietà?

Se hai implementato [!DNL Target] con tag in [!DNL Adobe Experience Platform] e riceve un messaggio di errore che indica che non è associata alcuna proprietà all’attività, passa il comando `at_property` parametro con `targetPageParams` funzione.

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

### Video di formazione: Video sulla formazione sulle autorizzazioni Enterprise ![Badge panoramica](/help/main/assets/overview.png)

Finalità di apprendimento:

* I tre livelli di ruolo disponibili per gli utenti di Adobe Target
* I concetti di Proprietà e Aree di lavoro e come funzionano questi limiti e raggruppamenti per consentire il controllo sui livelli di accesso degli utenti
* Diversi esempi di Proprietà da considerare per la tua organizzazione

>[!VIDEO](https://video.tv.adobe.com/v/19042/)

### Orario ufficio: [!DNL Target] Aree di lavoro Premium

Questo video è una registrazione di “Office Hours”, un’iniziativa condotta dal team di assistenza clienti di Adobe.

* Creare un’area di lavoro (profilo prodotto)
* Creazione delle proprietà
* Aggiunta di utenti
* Aggiornamento dell’implementazione

>[!NOTE]
>
>Il [!DNL Target] [!UICONTROL Administration] interfaccia utente del menu (in precedenza [!UICONTROL Setup]) è stato riprogettato per fornire prestazioni migliori, ridurre il tempo di manutenzione necessario durante il rilascio di nuove funzioni e migliorare l&#39;esperienza utente nel prodotto. Le informazioni contenute nel video seguente sono corrette; tuttavia, le opzioni potrebbero trovarsi in posizioni leggermente diverse.

>[!VIDEO](https://video.tv.adobe.com/v/23643/)
