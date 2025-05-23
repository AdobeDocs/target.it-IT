---
keywords: aggiungi utente;progetto;gruppo utenti;proprietà;area di lavoro;gestisci proprietà;proprietà;at_property;ruoli;autorizzazioni
description: Scopri come aggiungere utenti ad Adobe Target; creare aree di lavoro, gruppi di utenti e proprietà; aggiornare l’implementazione e specificare ruoli e autorizzazioni.
title: Come Si Configurano Le Autorizzazioni Enterprise?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Administration & Configuration
role: Admin
exl-id: 6494fc86-d2d3-4382-9d2e-63be435ba935
source-git-commit: 0ab5b7d7cbfaef86b9a045883f597900dba72416
workflow-type: tm+mt
source-wordcount: '1392'
ht-degree: 56%

---

# Configurare le autorizzazioni Enterprise

Informazioni sulle attività necessarie per aggiungere utenti all&#39;implementazione di [!DNL Target]; creare aree di lavoro, gruppi di utenti e proprietà; aggiornare l&#39;implementazione di [!DNL Target] per includere il parametro `at_property` e specificare ruoli e autorizzazioni.

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
| 5: aggiorna l&#39;implementazione per includere il parametro `at_property` | [!DNL Target] interfaccia utente, funzioni at.js o tag in [!DNL Adobe Experience Platform] |
| 6. Specificare ruoli e autorizzazioni | [!DNL Adobe Admin Console for Enterprise] |

Per le attività eseguite in [!DNL Adobe Admin Console for Enterprise], accedere alla console eseguendo la procedura seguente:

1. In Adobe Target, fare clic su **[!UICONTROL Administration]** > **[!UICONTROL Properties]** > **[!UICONTROL Assign Properties to Workspaces]**.

   Oppure

   Vai a [https://adminconsole.adobe.com/enterprise](https://adminconsole.adobe.com/enterprise/) e, se non hai già effettuato l&#39;accesso, accedi con il tuo Adobe ID.


1. (Condizionale) Se disponi dell&#39;accesso ad [!DNL Admin Console for Enterprise] per più di un’organizzazione, fai clic sull’avatar utente nell’angolo a destra o sulla barra di navigazione superiore, quindi seleziona l’organizzazione desiderata.

## Passaggio 1: Aggiungi utenti (facoltativo) {#section_A92AF0F921B743FEB9E9033433BD816A}

Quando si inizia a utilizzare la nuova funzionalità [!UICONTROL Properties], tutte le operazioni di gestione degli utenti devono essere eseguite in [!DNL Adobe Admin Console for Enterprise]. Tuttavia, tutti gli utenti esistenti in [!DNL Target] verranno migrati da [!DNL Target] ad [!DNL Admin Console for Enterprise].

1. [In Admin Console](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md#section_79796E0227D048F59BAE0AB02E544EBE), fare clic sulla scheda **[!UICONTROL Users]** nella parte superiore della pagina > **[!UICONTROL Add Users]** per creare nuovi utenti o modificare quelli esistenti.
1. Segui le istruzioni contenute in [Gestire utenti e gruppi in Experience Cloud](https://helpx.adobe.com/it/enterprise/using/users.html) nella *guida utente della versione Enterprise*.

## Passaggio 2: Creare un’area di lavoro (profilo prodotto) {#section_B82EB409B67C4D9D9D20CE30E48DB1DC}

Un’area di lavoro (profilo prodotto) consente a un’organizzazione di assegnare un set specifico di utenti a un set specifico di proprietà. Un’area di lavoro è simile per vari aspetti a una suite di rapporti di [!DNL Analytics].

Le organizzazioni possono iniziare a sfruttare le funzionalità delle autorizzazioni Enterprise creando nuove aree di lavoro all&#39;interno di [!DNL Admin Console], assegnando proprietà [!DNL Target] a queste aree di lavoro e spostando gli utenti dalla configurazione &quot;Default Workspace&quot; a queste nuove aree di lavoro ad accesso limitato.

I clienti possono utilizzare queste aree di lavoro per separare l’accesso ai diversi team per regione, business unit, sezione del sito vista o qualsiasi altro metodo scelto.

Gli utenti possono fare parte di più aree di lavoro e possono anche avere ruoli diversi all’interno di ogni area di lavoro.

1. In [!DNL Admin Console], fare clic su **[!UICONTROL Products]**, quindi selezionare il nome del prodotto desiderato.

   ![workspace](/help/main/administrating-target/c-user-management/c-user-management/assets/workspace-new.png)

1. Creare l&#39;area di lavoro desiderata (profilo prodotto):

   * **Accesso predefinito:** tutte le attività esistenti verranno unite in un singolo progetto denominato “Accesso predefinito”. Questo non avrà alcun impatto sui clienti. Tutti i ruoli e le funzionalità dell&#39;utente rimarranno esattamente uguali a come erano prima di questa modifica.

     Tutte le attività create tramite [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] e [!DNL Target Classic] faranno parte dell’area di lavoro “Accesso predefinito”. Attualmente non è possibile spostare i progetti da “Accesso predefinito” a un altro progetto.

   * **Nuove aree di lavoro (profili prodotto):** è possibile iniziare a sfruttare le nuove funzionalità delle autorizzazioni eseguendo le operazioni seguenti:

      * Creazione di nuove aree di lavoro all’interno di [!DNL Admin Console for Enterprise].
      * Assegnazione delle proprietà di Target alle aree di lavoro.

   È possibile utilizzare queste aree di lavoro per dividere l&#39;accesso per team diversi per regione, business unit, sezione sito o tramite qualsiasi altro metodo scelto. Gli utenti possono fare parte di più aree di lavoro e possono avere ruoli diversi all&#39;interno di ogni area di lavoro.

1. Segui le istruzioni riportate in [Creare e gestire le configurazioni di prodotto](https://helpx.adobe.com/it/enterprise/help/manage-products-and-configurations.html) nella *guida utente della versione Enterprise*.

>[!NOTE]
>Per ulteriori informazioni sulla configurazione delle aree di lavoro, guarda il video di formazione sottostante.

### Ottenere l’ID workspace {#workspace-id}

Per sfruttare le autorizzazioni Enterprise nelle [API di Target](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/server-side-overview.html?lang=it){target=_blank} devi passare l’ID workspace.

1. In [Adobe Admin Console](https://adminconsole.adobe.com), fare clic sulla scheda [!UICONTROL Products], quindi sul prodotto nel menu a sinistra per visualizzare l&#39;elenco di PLC(workspace).
1. Fai clic sulla voce PLC(workspace) desiderata, quindi individua l’ID “profiles” nell’URL, come mostrato di seguito.

   ![workspaceID](/help/main/administrating-target/c-user-management/property-channel/assets/workspace-id-newest.png)

## Passaggio 3: Creare gruppi di utenti (facoltativo) {#section_5F5CB9AA7A9F4D26953E22016DA59605}

È possibile creare gruppi di utenti, ad esempio sviluppatori, analisti, addetti al marketing, dirigenti e così via, e assegnare privilegi a più prodotti Adobe e aree di lavoro. Per assegnare a un nuovo membro del team tutti i privilegi appropriati per i diversi prodotti Adobe, sarà sufficiente aggiungerlo a un gruppo di utenti specifico.

1. In Admin Console, fai clic sulla scheda **[!UICONTROL Users]** nella parte superiore della pagina > **[!UICONTROL User Groups]** per creare nuovi gruppi di utenti o per modificare quelli esistenti.
1. Segui le istruzioni contenute in [Gestire utenti e gruppi nella configurazione di un prodotto](https://helpx.adobe.com/it/enterprise/help/manage-products-and-configurations.html) nella *Guida utente Enterprise*.

## Passaggio 4: Creare proprietà {#section_E8F2C92BE0F4466AB87604059C9CF3FD}

Le proprietà vengono abilitate aggiungendo una coppia nome/valore specifica come parametro con qualsiasi chiamata ([!DNL Target], chiamata API, ecc.) a [!DNL Target].

Le proprietà appartengono a canali specifici (Web, mobile, e-mail e API/altro).

**Suggerimento**: per ulteriori informazioni su come creare le proprietà, guarda il video di formazione sottostante.

1. In [!DNL Target], fare clic su **[!UICONTROL Administration]** > **[!UICONTROL Properties]** per visualizzare l&#39;elenco [!UICONTROL Properties].
1. Fai clic su **Crea proprietà**.

   Compila i campi:

   * **Nome proprietà (obbligatorio):** Specificare un nome descrittivo per la proprietà.
   * **Descrizione:** specifica una descrizione facoltativa per la proprietà.
   * **Canale:** seleziona il canale desiderato per la proprietà: Web, App mobile, E-mail o Altro/API (per esempio un set-top box o una console PlayStation).

1. Fai clic su **[!UICONTROL Copy]** per copiare negli Appunti il codice da utilizzare durante l&#39;esecuzione dei passaggi in [5: Aggiornare l&#39;implementazione per includere il parametro at_property](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md#section_9B17A59807A94712BE642942442EBBC8).
1. Al termine, fai clic su **[!UICONTROL Save]**.

>[!NOTE]
>Per ulteriori informazioni sulla creazione di proprietà, guarda il video di formazione sottostante.

## Passaggio 5: aggiorna l’implementazione per includere il parametro at_property {#section_9B17A59807A94712BE642942442EBBC8}

Per utilizzare la funzionalità di autorizzazioni utente di [!DNL Target], è necessario aggiungere il parametro `at_property` a qualsiasi chiamata che sta raggiungendo [!DNL Target] (chiamata Target, chiamata API, ecc.).

**Per ottenere il `at_property`codice del parametro**:

1. (Facoltativo) Utilizza il codice di implementazione generato e salvato negli appunti durante l&#39;esecuzione dei passaggi del punto [4. Creare le proprietà](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md#section_E8F2C92BE0F4466AB87604059C9CF3FD) e passa al passaggio 2.

   Oppure

   In [!DNL Target], fare clic su **[!UICONTROL Administration]** > **[!UICONTROL Properties]** per visualizzare l&#39;elenco [!UICONTROL Properties].

   1. Passa il puntatore del mouse sulla colonna [!UICONTROL Last Updated] per visualizzare la proprietà desiderata e fai clic sull&#39;icona [!UICONTROL Code] ( ![icona codice](/help/main/assets/icons/Code.svg) ).

      ![Codice proprietà visualizzato al passaggio del mouse](/help/main/administrating-target/c-user-management/property-channel/assets/code_property_new.png)

   1. Fai clic con il pulsante destro del mouse sul codice di implementazione evidenziato per copiarlo negli appunti.

1. Aggiorna l&#39;implementazione di [!DNL Target] con il codice di implementazione ottenuto nel passaggio precedente.

   Esistono diversi modi per aggiornare l&#39;implementazione di [!DNL Target]. Ad esempio, è possibile utilizzare i seguenti metodi per le pagine Web:

   * **Tramite un &quot;parametro personalizzato&quot; nei tag all&#39;interno di [!DNL Adobe Experience Platform]:**

     Per ulteriori informazioni, consulta [Aggiungere parametri Mbox](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/target/overview.html?lang=it#add-mbox-params) nella *Panoramica sui tag* documentazione.

   * **Tramite la funzione targetPageParamsAll():** Inserisci il seguente codice nei tag `<head>`, sopra il riferimento at.js.

     ```javascript
     <script>
      function targetPageParamsAll() {
       return {
        "at_property": "5f8bd98b-1456-a84c-2a96-11s9b8e2b112"
       };
      }
     </script>
     ```

     Per ulteriori informazioni su come eseguire questa operazione con at.js, consulta [targetPageParamsAll](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetpageparamsall.html?lang=it){target=_blank}.

## Passaggio 6: specificare ruoli e autorizzazioni {#section_8C425E43E5DD4111BBFC734A2B7ABC80}

1. In Admin Console, fai clic su **[!UICONTROL Products]**, quindi seleziona il nome del prodotto desiderato.

   ![Workspace](/help/main/administrating-target/c-user-management/c-user-management/assets/workspace-publisher.png)

1. Fai clic sul nome del profilo desiderato (ad esempio, Workspace predefinito).

   ![Default Workspace (Area di lavoro predefinita)](/help/main/administrating-target/c-user-management/c-user-management/assets/default-workspace-new.png)

1. Fare clic su **[!UICONTROL Users]**.

   Nella scheda [!UICONTROL Users] vengono visualizzati tutti gli utenti di quell&#39;area di lavoro.

   ![configurazione degli utenti](/help/main/administrating-target/c-user-management/c-user-management/assets/configuration_users-new-publisher.png)

1. Selezionare il ruolo di autorizzazioni desiderato (Responsabile approvazione, Editor, Osservatore o Editore) utilizzando l&#39;elenco a discesa per ogni utente nella colonna [!UICONTROL Product Role].

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
>L&#39;interfaccia utente del menu [!DNL Target] [!UICONTROL Administration] (in precedenza [!UICONTROL Setup]) è stata riprogettata per fornire prestazioni migliori, ridurre il tempo di manutenzione necessario per il rilascio di nuove funzionalità e migliorare l&#39;esperienza utente nel prodotto. Le informazioni contenute nei video seguenti sono generalmente corrette; tuttavia, le opzioni potrebbero trovarsi in posizioni leggermente diverse. I video aggiornati verranno pubblicati a breve.

### Come configurare le aree di lavoro di Adobe Target (6:55) ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video spiega come creare aree di lavoro.

* Accedere ad Admin Console da Adobe Target (3 modalità)
* Configurare un&#39;area di lavoro in Adobe Admin Console

   * Aggiungere utenti alle aree di lavoro
   * Aggiungere proprietà alle aree di lavoro

* Comprendere le aree di lavoro predefinite

>[!VIDEO](https://video.tv.adobe.com/v/3421732?captions=ita)

### Come creare proprietà in Adobe Target (3:05) ![Icona esercitazione](/help/main/assets/tutorial.png)

* Come creare una proprietà all’interno dell’interfaccia di [!DNL Adobe Target]
* Come generare un token di proprietà da includere nell&#39;implementazione della proprietà
* Familiarizza con i tre metodi di implementazione:

   * Web
   * App mobile
   * Posta elettronica, set top box o chiamate API

>[!VIDEO](https://video.tv.adobe.com/v/18990/)
