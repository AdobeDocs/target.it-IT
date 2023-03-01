---
keywords: aggiungi utente;progetto;gruppo utenti;proprietà;area di lavoro;gestisci proprietà;proprietà;at_property;ruoli;autorizzazioni
description: Scopri come aggiungere utenti ad Adobe Target; creare aree di lavoro, gruppi di utenti e proprietà; aggiornare l’implementazione e specificare ruoli e autorizzazioni.
title: Come Si Configurano Le Autorizzazioni Enterprise?
feature: Administration & Configuration
role: Admin
exl-id: 6494fc86-d2d3-4382-9d2e-63be435ba935
source-git-commit: 3ac61272ee1ccd72a8670966f181e7798cbe9f76
workflow-type: tm+mt
source-wordcount: '1444'
ht-degree: 66%

---

# ![PREMIUM](/help/main/assets/premium.png) Configurare le autorizzazioni Enterprise

Informazioni sulle attività necessarie per aggiungere utenti al tuo [!DNL Target] implementazione; creare aree di lavoro, gruppi di utenti e proprietà; aggiornare [!DNL Target] implementazione per includere `at_property` e specificare ruoli e autorizzazioni.

>[!NOTE]
>
>La funzionalità Proprietà e Autorizzazioni è disponibile come parte della soluzione [Target Premium](/help/main/c-intro/intro.md#premium). Non sono disponibili in [!DNL Target Standard] senza una licenza [!DNL Target Premium].

Nella tabella seguente sono elencate le attività da eseguire per creare proprietà e assegnare ruoli utente e autorizzazioni. Per ulteriori informazioni su ciascuna attività, fai riferimento alle sezioni seguenti.

| Attività | Eseguita in |
|--- |--- |
| 1. Aggiungere utenti (facoltativo) | [!DNL Adobe Admin Console for Enterprise] |
| 2. Creare un’area di lavoro (profilo prodotto) | [!DNL Adobe Admin Console for Enterprise] |
| 3. Creare gruppi di utenti (facoltativo) | [!DNL Adobe Admin Console for Enterprise] |
| 4. Creare le proprietà | Interfaccia utente [!DNL Target] |
| 5: aggiorna l’implementazione per includere `at_property` parametro | [!DNL Target] Interfaccia utente, funzioni at.js o tag in [!DNL Adobe Experience Platform] |
| 6. Specificare ruoli e autorizzazioni | [!DNL Adobe Admin Console for Enterprise] |

Per le attività eseguite in [!DNL Adobe Admin Console for Enterprise], accedi alla console seguendo questi passaggi:

1. In Adobe Target, fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Proprietà]** > **[!UICONTROL Assegna proprietà alle aree di lavoro]**.

   Oppure

   Vai a [https://adminconsole.adobe.com/enterprise](https://adminconsole.adobe.com/enterprise/) > accedi con il tuo Adobe ID, se non hai già effettuato l’accesso.


1. (Condizionale) Se disponi dell&#39;accesso ad [!DNL Admin Console for Enterprise] per più di un’organizzazione, fai clic sull’avatar utente nell’angolo a destra o sulla barra di navigazione superiore, quindi seleziona l’organizzazione desiderata.

## Passaggio 1: Aggiungi utenti (facoltativo) {#section_A92AF0F921B743FEB9E9033433BD816A}

Quando si inizia a utilizzare la nuova funzionalità [!UICONTROL Proprietà], tutte le attività di gestione degli utenti devono essere eseguite in [!DNL Adobe Admin Console for Enterprise]. Tuttavia, tutti gli utenti esistenti in [!DNL Target] verranno migrati da [!DNL Target] ad [!DNL Admin Console for Enterprise].

1. [In Admin Console](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md#section_79796E0227D048F59BAE0AB02E544EBE), fai clic sulla scheda **[!UICONTROL Utenti]** nella parte superiore della pagina > **[!UICONTROL Aggiungi utenti]** per creare nuovi utenti o modificare quelli esistenti.
1. Segui le istruzioni contenute in [Gestire utenti e gruppi in Experience Cloud](https://helpx.adobe.com/it/enterprise/using/users.html) nella *guida utente della versione Enterprise*.

## Passaggio 2: Creare un’area di lavoro (profilo prodotto) {#section_B82EB409B67C4D9D9D20CE30E48DB1DC}

Un’area di lavoro (profilo prodotto) consente a un’organizzazione di assegnare un set specifico di utenti a un set specifico di proprietà. Un’area di lavoro è simile per vari aspetti a una suite di rapporti di [!DNL Analytics].

Le organizzazioni possono iniziare a sfruttare le funzionalità delle autorizzazioni Enterprise creando nuove aree di lavoro all’interno di [!DNL Admin Console], assegnazione [!DNL Target] e spostando gli utenti dalla configurazione &quot;Area di lavoro predefinita&quot; a queste nuove aree di lavoro ad accesso limitato.

I clienti possono utilizzare queste aree di lavoro per separare l’accesso ai diversi team per regione, business unit, sezione del sito vista o qualsiasi altro metodo scelto.

Gli utenti possono fare parte di più aree di lavoro e possono anche avere ruoli diversi all’interno di ogni area di lavoro.

1. In [!DNL Admin Console], fai clic su **[!UICONTROL Prodotti]**, quindi seleziona il nome del prodotto desiderato.

   ![workspace](/help/main/administrating-target/c-user-management/c-user-management/assets/workspace-new.png)

1. Creare l&#39;area di lavoro desiderata (profilo prodotto):

   * **Accesso predefinito:** tutte le attività esistenti verranno unite in un singolo progetto denominato “Accesso predefinito”. Questo non avrà alcun impatto sui clienti. Tutti i ruoli e le funzionalità dell&#39;utente rimarranno esattamente uguali a come erano prima di questa modifica.

      Tutte le attività create tramite [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] e [!DNL Target Classic] faranno parte dell’area di lavoro “Accesso predefinito”. Attualmente non è possibile spostare i progetti da “Accesso predefinito” a un altro progetto.

   * **Nuove aree di lavoro (profili prodotto):** è possibile iniziare a sfruttare le nuove funzionalità delle autorizzazioni eseguendo le operazioni seguenti:

      * Creazione di nuove aree di lavoro all’interno di [!DNL Admin Console for Enterprise].
      * Assegnazione delle proprietà di Target alle aree di lavoro.

   È possibile utilizzare queste aree di lavoro per dividere l&#39;accesso per team diversi per regione, business unit, sezione sito o tramite qualsiasi altro metodo scelto. Gli utenti possono fare parte di più aree di lavoro e possono avere ruoli diversi all&#39;interno di ogni area di lavoro.

1. Segui le istruzioni riportate in [Creare e gestire le configurazioni di prodotto](https://helpx.adobe.com/enterprise/help/manage-products-and-configurations.html) nella *guida utente della versione Enterprise*.

>[!NOTE]
>Per ulteriori informazioni sulla configurazione delle aree di lavoro, guarda il video di formazione sottostante.

### Ottenere l’ID workspace {#workspace-id}

Per sfruttare le autorizzazioni Enterprise in devi passare l’ID workspace. [API di Target](https://developer.adobe.com/target/implement/server-side/){target=_blank}.

1. In [Adobe Admin Console](https://adminconsole.adobe.com), fai clic sulla scheda [!UICONTROL Prodotti], quindi sul prodotto nel menu a sinistra per visualizzare l’elenco di PLC(workspace).
1. Fai clic sulla voce PLC(workspace) desiderata, quindi individua l’ID “profiles” nell’URL, come mostrato di seguito.

   ![workspaceID](/help/main/administrating-target/c-user-management/property-channel/assets/workspace-id-newest.png)

## Passaggio 3: Creare gruppi di utenti (facoltativo) {#section_5F5CB9AA7A9F4D26953E22016DA59605}

È possibile creare gruppi di utenti, ad esempio sviluppatori, analisti, addetti al marketing, dirigenti e così via, e assegnare privilegi a più prodotti Adobe e aree di lavoro. Per assegnare a un nuovo membro del team tutti i privilegi appropriati per i diversi prodotti Adobe, sarà sufficiente aggiungerlo a un gruppo di utenti specifico.

1. In Admin Console, fai clic sulla scheda **[!UICONTROL Utenti]** nella parte superiore della pagina > **[!UICONTROL Gruppi di utenti]** per creare nuovi gruppi di utenti o per modificare gruppi esistenti.
1. Segui le istruzioni contenute in [Gestire utenti e gruppi nella configurazione di un prodotto](https://helpx.adobe.com/enterprise/help/manage-products-and-configurations.html) nella *Guida utente Enterprise*.

## Passaggio 4: Creare proprietà {#section_E8F2C92BE0F4466AB87604059C9CF3FD}

Le proprietà vengono abilitate aggiungendo una coppia nome/valore specifica come parametro con qualsiasi chiamata (chiamata Target, chiamata API, ecc.) a Target.

Le proprietà appartengono a canali specifici (Web, mobile, e-mail e API/altro).

**Suggerimento**: per ulteriori informazioni su come creare le proprietà, guarda il video di formazione sottostante.

1. In entrata [!DNL Target], fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Proprietà]** per visualizzare [!UICONTROL Proprietà] elenco.
1. Fai clic su **Crea proprietà**.

   Compila i campi:

   * **Nome proprietà (obbligatorio):** Specifica un nome descrittivo per la proprietà.
   * **Descrizione:** specifica una descrizione facoltativa per la proprietà.
   * **Canale:** seleziona il canale desiderato per la proprietà: Web, App mobile, E-mail o Altro/API (per esempio un set-top box o una console PlayStation).

1. Clic **[!UICONTROL Copia]** per copiare il codice negli Appunti che utilizzerai durante l&#39;esecuzione dei passaggi in [5: Aggiornare l’implementazione per includere il parametro at_property](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md#section_9B17A59807A94712BE642942442EBBC8).
1. Al termine, fai clic su **[!UICONTROL Salva]**.

>[!NOTE]
>Per ulteriori informazioni sulla creazione di proprietà, guarda il video di formazione sottostante.

## Passaggio 5: aggiorna l’implementazione per includere il parametro at_property {#section_9B17A59807A94712BE642942442EBBC8}

Per utilizzare [!DNL Target] delle autorizzazioni utente, è necessario aggiungere il `at_property` parametro per qualsiasi chiamata che sta raggiungendo [!DNL Target] (Chiamata di Target, chiamata API, ecc.).

**Per ottenere il `at_property`codice del parametro**:

1. (Facoltativo) Utilizza il codice di implementazione generato e salvato negli appunti durante l&#39;esecuzione dei passaggi del punto [4. Creare le proprietà](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md#section_E8F2C92BE0F4466AB87604059C9CF3FD) e passa al passaggio 2.

   Oppure

   In entrata [!DNL Target], fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Proprietà]** per visualizzare [!UICONTROL Proprietà] elenco.

   1. Passa il puntatore del mouse sull&#39;[!UICONTROL ultima colonna aggiornata] per visualizzare la proprietà desiderata e fai clic sull&#39;[!UICONTROL icona del codice].

      ![Codice proprietà visualizzato al passaggio del mouse](/help/main/administrating-target/c-user-management/property-channel/assets/code_property_new.png)

   1. Fai clic con il pulsante destro del mouse sul codice di implementazione evidenziato per copiarlo negli appunti.

1. Aggiorna il tuo [!DNL Target] implementazione con il codice di implementazione ottenuto nel passaggio precedente.

   Esistono diversi modi per aggiornare l&#39;implementazione di [!DNL Target]. Ad esempio, è possibile utilizzare i seguenti metodi per le pagine Web:

   * **Tramite un &quot;parametro personalizzato&quot; nei tag in [!DNL Adobe Experience Platform]:**

      Per ulteriori informazioni, consulta [Aggiungi parametri mbox](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/target/overview.html?lang=en#add-mbox-params) nel *Panoramica sui tag* documentazione.

   * **Tramite la funzione targetPageParamsAll():** Inserisci il seguente codice nel `<head>` tag, sopra il riferimento at.js.

      ```javascript
      <script>
       function targetPageParamsAll() {
        return {
         "at_property": "5f8bd98b-1456-a84c-2a96-11s9b8e2b112"
        };
       }
      </script>
      ```

      Per ulteriori informazioni su come eseguire questa procedura con at.js, consulta [targetPageParamsAll](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetpageparamsall/){target=_blank}.

## Passaggio 6: specificare ruoli e autorizzazioni {#section_8C425E43E5DD4111BBFC734A2B7ABC80}

1. In Admin Console, fai clic su **[!UICONTROL Prodotti]**, quindi seleziona il nome del prodotto desiderato.

   ![Workspace](/help/main/administrating-target/c-user-management/c-user-management/assets/workspace-publisher.png)

1. Fai clic sul nome del profilo desiderato (ad esempio, Area di lavoro predefinita).

   ![Default Workspace (Area di lavoro predefinita)](/help/main/administrating-target/c-user-management/c-user-management/assets/default-workspace-new.png)

1. Fai clic su **[!UICONTROL Utenti]**.

   Nella scheda [!UICONTROL Utenti] vengono visualizzati tutti gli utenti di quell’area di lavoro.

   ![configurazione degli utenti](/help/main/administrating-target/c-user-management/c-user-management/assets/configuration_users-new-publisher.png)

1. Seleziona il ruolo di autorizzazioni desiderato (Responsabile approvazione, Editor, Osservatore o Editore) dall’elenco a discesa per ogni utente nella sezione [!UICONTROL Ruolo prodotto] colonna.

   ![Elenco a discesa Product Role (Ruolo prodotto)](/help/main/administrating-target/c-user-management/c-user-management/assets/product-role-new.png)

   | Ruolo | Descrizione |
   |--- |--- |
   | Responsabile approvazione | Può creare, modificare, attivare o interrompere le attività. |
   | Editor | Può creare e modificare le attività prima che siano in diretta, ma non può approvare l’avvio di un’attività. |
   | Osservatore | Può visualizzare le attività, ma non può crearle o modificarle. |
   | Editore | Simile al ruolo Osservatore (può visualizzare le attività, ma non può crearle o modificarle). Tuttavia, il ruolo Editore è anche autorizzato ad attivare le attività. |

   Per ulteriori informazioni, vedi [Gestione delle autorizzazioni del prodotto in Admin Console](https://helpx.adobe.com/it/enterprise/using/manage-permissions-and-roles.html) nella *guida utente della versione Enterprise*.

## Video di formazione

I video seguenti contengono ulteriori informazioni sui concetti descritti in questo articolo.

>[!NOTE]
>
>L’interfaccia utente di [!DNL Target] del menu [!UICONTROL Amministrazione] (precedentemente [!UICONTROL Configurazione]) è stato riprogettato per fornire prestazioni migliori, ridurre il tempo di manutenzione necessario durante il rilascio di nuove funzioni e migliorare l’esperienza utente nel prodotto. Le informazioni contenute nei video seguenti sono generalmente corrette; tuttavia, le opzioni potrebbero trovarsi in posizioni leggermente diverse. I video aggiornati verranno pubblicati a breve.

### Come configurare le aree di lavoro di Adobe Target (6:55) ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video spiega come creare aree di lavoro.

* Accedere ad Admin Console da Adobe Target (3 modalità)
* Configurare un&#39;area di lavoro in Adobe Admin Console

   * Aggiungere utenti alle aree di lavoro
   * Aggiungere proprietà alle aree di lavoro

* Comprendere le aree di lavoro predefinite

>[!VIDEO](https://video.tv.adobe.com/v/19463/)

### Come creare proprietà in Adobe Target (3:05) ![Icona esercitazione](/help/main/assets/tutorial.png)

* Come creare una proprietà all’interno dell’interfaccia di [!DNL Adobe Target]
* Come generare un token di proprietà da includere nell&#39;implementazione della proprietà
* Familiarizza con i tre metodi di implementazione:

   * Web
   * App mobile
   * Posta elettronica, set top box o chiamate API

>[!VIDEO](https://video.tv.adobe.com/v/18990/)
