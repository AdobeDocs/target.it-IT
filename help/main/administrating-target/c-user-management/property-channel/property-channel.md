---
keywords: aree di lavoro;gestisci proprietà;autorizzazioni;configurazione prodotto;profilo prodotto;ruoli;progetto
description: Scopri come creare aree di lavoro separate (profili di prodotto) e quindi assegnare agli utenti ruoli e autorizzazioni diversi per singole pagine, proprietà o siti web.
title: Cosa sono le autorizzazioni utente Enterprise e come le utilizzo?
feature: Administration & Configuration
role: Admin
exl-id: 838abe87-dba7-4274-97b4-31a7905846dc
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '3171'
ht-degree: 59%

---

# ![PREMIUM](/help/main/assets/premium.png) Autorizzazioni per utenti Enterprise

Le autorizzazioni per gli utenti aziendali sono un mezzo per amministrare formalmente l&#39;accesso degli utenti a livello aziendale a [!DNL Adobe Target]. Aggiungi utenti a [!DNL Target], assegna le autorizzazioni in base ai loro ruoli e crea aree di lavoro per i team in base a reparti, posizioni globali, canali e altri raggruppamenti logici diversi. Puoi assegnare agli utenti i ruoli di [!UICONTROL Osservatore], [!UICONTROL Editor]oppure [!UICONTROL Approvatore].

## Determinare se si dispone dell&#39;accesso alle autorizzazioni per gli utenti aziendali

>[!NOTE]
>
>Le funzionalità Proprietà e Autorizzazioni sono disponibili come parte della soluzione [!DNL Target] Premium. Non sono disponibili in [!DNL Target] Standard senza una licenza [!DNL Target] Premium.
>
>Le [!DNL Target] l’implementazione può utilizzare qualsiasi versione di at.js.

Per verificare se la tua organizzazione dispone di una licenza Standard o Premium, fai clic sul collegamento [!UICONTROL Amministrazione] in alto nell’interfaccia utente di [!DNL Target].

* Clienti **[!DNL Target Standard]**: se è presente la scheda [!UICONTROL Utenti] ([!UICONTROL Amministrazione > Utenti]) (e non la scheda [!UICONTROL Proprietà]), la tua organizzazione dispone di una licenza [!DNL Target Standard]  I clienti [!DNL Target Standard] possono seguire le istruzioni riportate in [Utenti](/help/main/administrating-target/c-user-management/c-user-management/user-management.md) per aggiungere utenti e assegnare autorizzazioni in [!DNL Adobe Admin Console].

* **[!DNL Target Premium]Clienti**: Se vedi la [!UICONTROL Proprietà] scheda ([!UICONTROL Amministrazione > Proprietà]) e [!UICONTROL Utenti] la tua organizzazione dispone di un [!DNL Target Premium] licenza. I clienti [!DNL Target Premium] devono seguire le istruzioni contenute in questo articolo e in [Configurare le autorizzazioni Enterprise](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md).

## Prima di iniziare con le autorizzazioni Enterprise

>[!IMPORTANT]
>
>Assicurati di aver letto il [Avvertenze](/help/main/administrating-target/c-user-management/property-channel/property-channel.md#section_9714311B1CD9497A86F4910F8AE635E2) sezione seguente prima di procedere con le autorizzazioni Enterprise.

## Termini e definizioni utilizzati in questa sezione {#section_F8D229544FEA41C3BC2EFD1F95AA0116}

I termini seguenti vengono utilizzati in questa sezione e potrebbero essere nuovi per gli utenti che desiderano utilizzare la funzionalità Proprietà e Autorizzazioni in [!DNL Target] Premium.

### Proprietà

Le proprietà sono simili in natura alle proprietà all&#39;interno di [!DNL Adobe Experience Platform] in quanto utilizzano uno snippet univoco di codice per differenziarli.

Una proprietà web è una libreria di regole e un codice incorporato. Una proprietà web può essere un raggruppamento di uno o più domini e sottodomini.

Le proprietà vengono abilitate aggiungendo una coppia nome/valore specifica come parametro con qualsiasi chiamata (chiamata Target, chiamata API e così via) a [!DNL Target].

Le proprietà appartengono a canali specifici (web, mobile, email o API/altro).

### Area di lavoro (profilo prodotto)

Un’area di lavoro consente a un’azienda di assegnare un gruppo specifico di utenti a un insieme specifico di proprietà. Un’area di lavoro è simile per vari aspetti a una suite di rapporti di [!DNL Adobe Analytics].

Nota: Le aree di lavoro sono note come [!UICONTROL Profili di prodotto] in [!DNL Adobe Admin Console for Enterprise].

Se fai parte di un’azienda multinazionale, potresti avere un’area di lavoro per le pagine web, le proprietà o i siti europei e un’altra per le pagine web, le proprietà o i siti americani. Se fai parte di un’azienda multi-brand, potresti avere un’area di lavoro diversa per ciascuno dei marchi.

Gli utenti possono fare parte di più aree di lavoro e possono anche avere ruoli diversi all’interno di ogni area di lavoro.

Gli utenti possono avere diverse visualizzazioni di [!DNL Adobe Target] spostandosi tra le diverse aree di lavoro, in modo simile a [!DNL Analytics] gli utenti hanno visualizzazioni diverse di [!DNL Analytics] spostandosi tra le suite di rapporti.

Le aree di lavoro possono includere tipi di pubblico, offerte di codice e attività differenti.

Tutti i tipi di pubblico e le attività create prima della migrazione al nuovo modello di autorizzazioni Enterprise sono raggruppati in &quot;Area di lavoro predefinita&quot;, come illustrato di seguito.

Tutte le attività create tramite [!DNL Adobe Experience Manager] AEM, [!DNL Adobe Mobile Services]e [!DNL Adobe Target Classic] fanno parte di &quot;Area di lavoro predefinita&quot;.

### Area di lavoro predefinita

Tutte le aree di lavoro esistenti (profili prodotto) all’interno di [!DNL Admin Console] sono unite in una singola area di lavoro denominata &quot;Area di lavoro predefinita&quot; durante la migrazione dell’organizzazione al nuovo modello di autorizzazioni Enterprise.

>[!IMPORTANT]
>
>Non eliminare l’area di lavoro predefinita.

Tutti i ruoli utente e accesso a tutti [!DNL Target] La funzionalità rimane la stessa di prima della migrazione al nuovo modello di autorizzazioni Enterprise.

### Gruppi di utenti

Puoi creare gruppi di utenti, ad esempio sviluppatori, analisti, addetti al marketing, dirigenti e così via. Puoi quindi assegnare privilegi a più prodotti Adobe e aree di lavoro. Per assegnare a un nuovo membro del team tutti i privilegi appropriati per i diversi prodotti Adobe, sarà sufficiente aggiungerlo a un gruppo di utenti specifico.

### Ruoli e autorizzazioni

I ruoli e le autorizzazioni determinano i livelli di accesso che gli utenti devono creare e gestiscono le attività nell&#39;implementazione del tuo [!DNL Target]. In [!DNL Target] i ruoli includono quanto segue:

| Ruolo | Descrizione |
|--- |--- |
| Responsabile approvazione | Può creare, modificare, attivare o interrompere le attività. |
| Editor | Può creare e modificare le attività prima che siano in diretta, ma non può approvare l’avvio di un’attività. |
| Osservatore | Può visualizzare le attività, ma non può crearle o modificarle. |
| Editore | Simile al ruolo Osservatore (può visualizzare le attività, ma non può crearle o modificarle). Tuttavia, il ruolo Editore è anche autorizzato ad attivare le attività. |

### Canale

Il canale si riferisce al tipo di contenuto in cui vengono recapitate le attività di [!DNL Target]: pagine Web, applicazioni mobili, messaggi e-mail e così via.

Quando crei un’attività, questa viene creata nell’area di lavoro attualmente selezionata. Nella prima finestra di dialogo sono visualizzate le opzioni di selezione del canale che consentono di scegliere il canale desiderato per l’attività: Web, app mobile, e-mail o altro/API.

## Panoramica sulle autorizzazioni {#section_DC2172520DA84605B218A5E9FB6D187A}

Le informazioni seguenti spiegano il modo in cui le autorizzazioni sono state applicate in precedenza in [!DNL Target] e come vengono applicate utilizzando la funzionalità [!UICONTROL Proprietà] e [!UICONTROL Autorizzazioni].

Il nuovo [!UICONTROL Autorizzazioni] consente di creare progetti diversi (denominati &quot;profili di prodotto&quot; nella sezione [!DNL Adobe Admin Console for Enterprise]). I progetti ti consentono di assegnare autorizzazioni diverse a un singolo utente che ne determinano i diritti di accesso per ciascun progetto. Questi progetti distinti possono essere paragonati al modo in cui le suite di rapporti funzionano in [!DNL Adobe Analytics]. In ogni progetto possono essere inclusi utenti specifici con ruoli specifici applicabili a un insieme di proprietà. Il risultato è che i clienti possono limitare l’accesso a visualizzazione, modifica e approvazione dei propri utenti in base all’area geografica, all’ambiente (sviluppo/fase/prod), al canale o ad altri criteri personalizzati, come illustrato di seguito:

![immagine delle autorizzazioni](assets/permissions.png)

Ad esempio, un utente specifico potrebbe avere accesso “approvato” ai siti Web americani, ma solo un accesso di “visualizzazione” sull&#39;applicazione mobile europea. Lo stesso utente potrebbe non avere alcun accesso neppure per visualizzare le attività offerte sulle proprietà Web e mobile nella regione APAC.

Il modello di [!DNL Target] [!UICONTROL Autorizzazioni] corrente dispone di tre ruoli di autorizzazione (osservatore, editor e approvatore), come illustrato nella figura seguente:

![permissions_1 immagine](assets/permissions_1.png)

Ogni ruolo dispone di diversi livelli di autorizzazioni:

| Ruolo | Descrizione |
|--- |--- |
| Responsabile approvazione | Può creare, modificare, attivare o interrompere le attività. |
| Editor | Può creare e modificare le attività prima che siano in diretta, ma non può approvare l’avvio di un’attività. |
| Osservatore | Può visualizzare le attività, ma non può crearle o modificarle. |
| Editore | Simile al ruolo Osservatore (può visualizzare le attività, ma non può crearle o modificarle). Tuttavia, il ruolo Editore è anche autorizzato ad attivare le attività. |

È importante notare che il ruolo di ogni utente si applica a ogni pagina, proprietà o sito dell&#39;account che include i tag di [!DNL Target], come illustrato di seguito:

![permissions_2 immagine](assets/permissions_2.png)

Il nuovo modello di [!DNL Target] [!UICONTROL Autorizzazioni] presenta gli stessi tre ruoli di autorizzazione (osservatore, editor e approvatore); è tuttavia possibile assegnare separatamente i ruoli delle autorizzazioni di un utente per singole pagine, proprietà o siti, come illustrato di seguito:

![permissions_3 immagine](assets/permissions_3.png)

In questo esempio, Jan dispone delle autorizzazioni da approvatore per la Homepage e il sito internet degli Stati Uniti e le autorizzazioni da osservatore per il sito francese.

Inoltre Jan non può visualizzare pagine, proprietà o siti in [!DNL Target] che non dispone delle autorizzazioni di visualizzazione, come illustrato di seguito:

![permissions_4 immagine](assets/permissions_4.png)

In questo esempio Jan non può visualizzare le pagine dei prodotti, il sito russo e il sito carriere.

## Scenari di casi d’uso {#section_F3CE8576959E4F4CB13BEEED38311DD8}

I seguenti casi di utilizzo possono essere utili per comprendere come le proprietà, i progetti, i ruoli e le autorizzazioni consentono di raggiungere gli obiettivi di marketing con [!DNL Target]:

### Organizzazione multinazionale

Se fai parte di un’azienda multinazionale, potresti avere un’area di lavoro per le pagine web, le proprietà o i siti europei e un’altra per le pagine web, le proprietà o i siti americani. Dopo una riorganizzazione, utilizzando gli utenti tipo nelle illustrazioni di cui sopra, è possibile impostare le aree di lavoro e le autorizzazioni simili alle seguenti:

* **Jan**: Jan è il capo dell’ottimizzazione nel centro di eccellenza per le pagine Web degli Stati Uniti, le proprietà e i siti della sua organizzazione. Molto probabilmente dispone dei diritti di amministratore di sistema nel cloud Adobe Experience Cloud.

   Nel suo ruolo, ha le autorizzazioni di approvatore per la homepage degli Stati Uniti e il sito statunitense. grazie alle autorizzazioni di approvatore può creare, modificare e attivare o arrestare le attività.

   Jan si consulta anche con il team di ottimizzazione in Francia e, pertanto, dispone delle autorizzazioni di osservatore per il sito Francia che le danno un accesso in sola lettura alle attività. Jan può visualizzare le attività, ma non può crearle o modificarle.

   Siccome Jan non ha un ruolo che richiede la sua visualizzazione delle pagine dei prodotti, del sito Russia, o del sito carriere, lei non può vedere le attività per quei siti.

* **Ernie**: Ernie è un Marketing Manager per l’organizzazione ed è responsabile del marketing negli Stati Uniti.

   Siccome Ernie è entrato di recente nell&#39;organizzazione e ha poca esperienza con Target, dispone dei permessi editor per la homepage degli Stati Uniti, il sito degli Stati Uniti e le pagine dei prodotti. Con le autorizzazioni dell’editor, Ernie può creare e modificare le attività prima che siano live. Non può approvare l’avvio di un’attività, perché un utente con autorizzazioni di approvazione, come Jan, deve approvare l’attività prima che possa essere messa in produzione.

   Siccome Ernie non ha un ruolo che richiede la sua visualizzazione del sito Russia, del sito Francia, o del sito carriere, non può vedere le attività per quei siti.

* **Diana**: Diana è ora un’analista per l’organizzazione e le sono stati concessi i permessi di osservatore per la homepage degli Stati Uniti, il sito degli Stati Uniti, le pagine dei prodotti, il sito Russia e il sito di Francia, che le consentono un accesso in sola lettura alle attività. Diana può visualizzare le attività, ma non può crearle o modificarle.

   Siccome Diana non ha alcun ruolo che richiede la sua visualizzazione del sito carriere, lei non può vedere le attività per quei siti.

### Organizzazione multi-brand

Se fai parte di un&#39;azienda multi-brand, potresti avere un&#39;area di lavoro separata per le pagine Web, le proprietà o i siti di ogni marca.

Dopo una riorganizzazione, utilizzando gli utenti tipo nelle illustrazioni di cui sopra, è possibile impostare i progetti e le autorizzazioni come di seguito:

* **Jan**: Jan è il capo dell’ottimizzazione nel centro di eccellenza di un’organizzazione sanitaria che opera nell’ambito dei prodotti ospedalieri e dei prodotti di consumo. Molto probabilmente dispone dei diritti di amministratore di sistema nel cloud Adobe Experience Cloud.

   Nel suo ruolo dispone delle autorizzazioni di approvatore per il sito ospedaliero. grazie alle autorizzazioni di approvatore può creare, modificare e attivare o arrestare le attività.

   Jan si consulta inoltre con il team di ottimizzazione nell&#39;ambito dei prodotti di consumo e, pertanto, dispone delle autorizzazioni di osservatore per quel sito, che le consentono l&#39;accesso in sola lettura alle attività. Jan può visualizzare le attività, ma non può crearle o modificarle.

* **Ernie:** Ernie è un Marketing Manager per l’organizzazione ed è responsabile del marketing nell’ambito dei prodotti di consumo.

   Siccome Ernie è entrato di recente nell&#39;organizzazione e ha poca esperienza con Target, dispone dei permessi editor per il sito consumatore. Con le autorizzazioni dell’editor, Ernie può creare e modificare le attività prima che siano live. Non può approvare l&#39;avvio di un&#39;attività: un utente con autorizzazioni di approvazione per il sito consumatore, ma non Jan in questo scenario, deve approvare l&#39;attività prima che possa essere messa in produzione.

   Siccome Ernie non ha un ruolo che richiede la sua visualizzazione del sito dell&#39;ospedale, non può vedere le attività per quel sito.

* **Diana**: Diana è ora un’analista per l’organizzazione e le sono stati concessi i permessi di osservatore per il sito dell’ospedale e il sito consumatore, che le consentono un accesso in sola lettura alle attività. Diana può visualizzare le attività, ma non può crearle o modificarle.

## Punti di contatto nell’interfaccia utente di Target per proprietà e autorizzazioni {#section_3414371393BB42999A268628B5456EC9}

La nuova funzionalità delle autorizzazioni può essere vista in varie posizioni nell&#39;interfaccia utente di [!DNL Target].

* **Elenco a discesa nell&#39;area di lavoro (profilo prodotto):** l&#39;elenco a discesa nell&#39;area di lavoro viene visualizzato nella parte superiore delle pagine [!UICONTROL Attività], [!UICONTROL Tipi di pubblico] e [!UICONTROL Offerte]. Seleziona l&#39;area di lavoro desiderata per filtrare l&#39;elenco e visualizzare solo gli elementi nell&#39;area di lavoro selezionata.

   ![workspace_immagine a discesa](assets/workspace_drop-down.png)

* **Creazione di attività:** Quando crei un’attività, questa viene creata nell’area di lavoro attualmente selezionata. Nella prima finestra di dialogo sono visualizzate le opzioni di selezione del canale che consentono di scegliere il canale desiderato per l’attività: Web, app mobile, e-mail o altro/API.

   ![immagine channel_options](assets/channel_options.png)

* **Creazione di pubblico:** Quando crei un pubblico, questo viene creato nell&#39;area di lavoro attualmente selezionata.
* **Elenco pubblico:** Puoi spostare i tipi di pubblico tra le aree di lavoro utilizzando [!UICONTROL Altre azioni] > [!DNL Move] l&#39;opzione [!UICONTROL Tipi di pubblico] pagina.
* **Creazione di offerte:** Quando crei un’offerta, questa viene creata nell’area di lavoro attualmente selezionata.
* **Pagina Proprietà (Amministrazione > Proprietà):** È possibile utilizzare [!UICONTROL Ricerca] per cercare [!UICONTROL Proprietà] elenco.

   ![immagine properties_list](assets/properties_list.png)

## Avvertenze {#section_9714311B1CD9497A86F4910F8AE635E2}

Quando utilizzi o configuri proprietà e autorizzazioni in , considera quanto segue [!DNL Target] Premium:

* **Importante**: non eliminare le aree di lavoro con le attività. Se elimini un’area di lavoro con attività, collabora con l’assistenza clienti per recuperare tali attività.
* Quando usi la vista Tutte le aree di lavoro:

   * Puoi visualizzare le attività, i destinatari e le offerte per tutti gli spazi di lavoro e le autorizzazioni per accedere.
   * Quando selezioni la [!UICONTROL Tutte le aree di lavoro] viene aggiunta una nuova colonna alla pagina Attività, Tipi di pubblico e Offerte . In questa colonna sono elencate l’area di lavoro dell’elemento e l’autorizzazione utente associate a tale elemento (Osservatore, Editor o Approvatore),
   * Quando crei un&#39;attività, un pubblico o un&#39;offerta nella vista Tutte le aree di lavoro, devi selezionare l&#39;area di lavoro in cui deve essere creato l&#39;elemento. Possono essere selezionate solamente le aree di lavoro per cui si possiedono le autorizzazioni dell&#39;editor o dell&#39;approvatore.
   * Quando copi un&#39;attività, un pubblico o un&#39;offerta nella vista Tutte le aree di lavoro, devi selezionare l&#39;area di lavoro in cui copiare l&#39;elemento. Possono essere selezionate solamente le aree di lavoro per cui si possiedono le autorizzazioni dell&#39;editor o dell&#39;approvatore.

* Qualsiasi impostazione relativa ai seguenti [!UICONTROL Amministrazione] le pagine possono essere controllate da qualsiasi [!UICONTROL Approvatore] in qualsiasi area di lavoro:

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

   * Attività, tipi di pubblico e offerte di codice create in [!DNL Target Standard/Premium] sono disponibili per l&#39;uso dopo che il cliente è abilitato per le autorizzazioni. (Nota: i clienti devono avere diritto [!DNL Target Premium].)
   * È possibile aggiungere proprietà alle attività esistenti nell’area di lavoro predefinita; tuttavia, tale approccio è soggetto a modifiche.
   * Solo le nuove risorse (come attività, offerte di codice e tipi di pubblico) create all&#39;interno di Target Premium (dopo l&#39;abilitazione delle autorizzazioni Enterprise) sono disponibili per limitare le autorizzazioni.
   * Le risorse esterne sono disponibili solo per gli utenti nell&#39;area di lavoro predefinita. Il ruolo di un utente nell&#39;area di lavoro predefinita si applica globalmente (a tutte le richieste Target e a tutte le risorse Target).

* Le risorse seguenti *non* fanno parte del nuovo modello di autorizzazioni Enterprise:

   * Offerte immagine
   * Tutte le risorse di Recommendations, inclusi Libreria criteri, Libreria progettazioni, Catalogo, Configurazione Recommendations.
   * Le risorse esistenti (ad esempio attività, offerte di codice e tipi di pubblico) create in Target Premium prima di abilitare le autorizzazioni Enterprise possono essere copiate ma non possono essere spostate in altre aree di lavoro.
   * Le attività, i tipi di pubblico, le offerte di codice, le offerte di immagini o qualsiasi altra risorsa creata utilizzando le soluzioni o i metodi seguenti non possono essere controllate dal modello di autorizzazioni Enterprise, ma fanno parte dell’area di lavoro predefinita: Target Classic, Adobe Experience Manager (AEM), Adobe Mobile Services e risorse create tramite API. Le risorse create tramite API includono le attività, i tipi di pubblico, le offerte basate su codice e le offerte di immagini.
   * Offerte immagine (risorse memorizzate in `https://[tenantName].marketing.adobe.com/content/mac/[tenantName]/target/offers.html#image-library` attualmente non può essere controllato dal modello di autorizzazioni Enterprise.
   * clickTracking e reindirizzamenti funzionano quando il collegamento di destinazione o la pagina di destinazione fanno parte di una proprietà inclusa nell&#39;attività. Inoltre, clickTracking potrebbe non funzionare quando si utilizza il `targetPageParams()` funzione . La funzione suggerita è `targetPageParamsAll()`.

   [!DNL Target] attualmente richiede un token `at_property` per essere presente in qualsiasi pagina in cui si verifica il rilevamento. Se il token è (1) non presente, (2) non rilevato al momento dell’impostazione dell’attività (all’interno del Compositore esperienza visivo), o (3) non passato alla chiamata clickTracking Target tramite il `targetPageParamsAll()` La metrica non viene incrementata e viene visualizzata come &quot;0&quot;.

   Lo stesso vale per le attività che utilizzano i reindirizzamenti. La pagina di destinazione deve avere un token `at_property` ed essere riconosciuta al momento della configurazione all&#39;interno di Compositore esperienza visivo.

   In una versione futura, Target lavorerà su pagine in cui non è presente alcun token `at_property` o su pagine in cui è presente un token `at_property` diverso.

* La funzionalità Autorizzazioni per gli utenti Enterprise non è supportata in [Adobe I/O di chiamate API](https://developer.adobe.com/target/){target=_blank}.

## Domande frequenti  {#faqs}

Le domande frequenti sulle autorizzazioni Enterprise includono:

### Posso spostare un&#39;attività da un&#39;area di lavoro a un&#39;altra?

Sfortunatamente non è possibile spostare le attività da un&#39;area di lavoro a un&#39;altra. Tuttavia, puoi copiare un’attività in qualsiasi area di lavoro sapendo che i dati di reporting non vengono trasferiti. Per ulteriori informazioni, vedere “Copia/modifica di un&#39;attività quando si utilizzano aree di lavoro” in [Copia/modifica di un&#39;attività quando si utilizzano aree di lavoro](/help/main/c-activities/edit-activity.md#section_45A92E1DD3934523B07E71EF90C4F8B6).

Le attività create prima della migrazione continuano a essere eseguite nello stesso modo nell&#39;area di lavoro predefinita, a meno che non siano proprietà modificate e assegnate. Le attività in un’area di lavoro specifica rispettano le proprietà assegnate a quell’area di lavoro e, pertanto, il comportamento potrebbe non rimanere lo stesso di prima della migrazione.

### È possibile spostare un pubblico da un’area di lavoro a un’altra? {#move-audience}

Sì, puoi spostare i tipi di pubblico tra le aree di lavoro utilizzando [!UICONTROL Altre azioni] l&#39;opzione [!UICONTROL Tipi di pubblico] pagina.

1. Fai clic sul pulsante **[!UICONTROL Altre azioni]** pulsante (i tre puntini di sospensione), quindi fare clic su **[!UICONTROL Sposta]**.

   ![Altre azioni > Sposta](/help/main/administrating-target/c-user-management/property-channel/assets/move-audience.png)

1. Seleziona l’area di lavoro desiderata dal **[!UICONTROL Area di lavoro]** elenco a discesa, quindi fai clic su **[!UICONTROL Sposta]**.

   ![Selezionare il pubblico desiderato da spostare nella nuova area di lavoro](/help/main/administrating-target/c-user-management/property-channel/assets/workspace-move.png)

>[!NOTE]
>
>Devi disporre dei diritti appropriati per modificare un pubblico. Inoltre, il pubblico non deve essere utilizzato in altre attività. Se il pubblico viene utilizzato in altre attività e desideri comunque spostare il pubblico in un&#39;altra area di lavoro, rimuovi il pubblico dalle altre attività in cui viene utilizzato.

### Perché viene visualizzato un messaggio di errore a indicare che nessuna proprietà è associata a questa attività, anche se è stata assegnata una proprietà?

Se hai implementato [!DNL Target] con tag in [!DNL Adobe Experience Platform] e ricevi un messaggio di errore che indica che non esiste alcuna proprietà associata all’attività, passa la `at_property` con il parametro `targetPageParams` funzione .

### Se una pagina di reindirizzamento e l’URL attività appartengono a proprietà diverse, vengono registrate le conversioni con tracciamento dei clic?

Il tracciamento dei clic non viene registrato nelle pagine in cui la pagina e l’URL attività appartengono a proprietà diverse.

Considera lo scenario seguente:

* Pagina1 appartiene a Proprietà1.
* Pagina2 appartiene a Proprietà2.
* Nell’attività, la Pagina 1 reindirizzerà a Pagina 2, contenente le tracce di clic.

Quando un visitatore apre Pagina1 in un browser, il visitatore viene reindirizzato a Pagina2. Poiché la Pagina2 non è qualificata per consegnare l’attività, la chiamata di Target non contiene le tracce di clic nella risposta.

Se la pagina di reindirizzamento e l’URL attività appartengono alla stessa proprietà, le tracce di clic funzionano come previsto. Per ulteriori informazioni, consulta [Tracciamento dei clic](/help/main/c-activities/r-success-metrics/click-tracking.md).

## Video di formazione

I video seguenti contengono ulteriori informazioni sui concetti descritti in questo articolo.

### Video di formazione: Video di formazione sulle autorizzazioni Enterprise ![Badge panoramica](/help/main/assets/overview.png)

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
>L’interfaccia utente di [!DNL Target] del menu [!UICONTROL Amministrazione] (precedentemente [!UICONTROL Configurazione]) è stato riprogettato per fornire prestazioni migliori, ridurre il tempo di manutenzione necessario durante il rilascio di nuove funzioni e migliorare l’esperienza utente nel prodotto. Le informazioni contenute nel video seguente sono corrette; tuttavia, le opzioni potrebbero trovarsi in posizioni leggermente diverse.

>[!VIDEO](https://video.tv.adobe.com/v/23643/)
