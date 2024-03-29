---
keywords: aggiungere utente;gestire utente;autorizzazioni utente
description: Scopri come utilizzare  [!DNL Adobe Admin Console]  per gestire gli utenti e le autorizzazioni e i diritti di questi in  [!DNL Adobe Target Standard].
title: Come si aggiungono utenti e si gestiscono le autorizzazioni per un account  [!DNL Target Standard] ?
feature: Administration & Configuration
role: Admin
exl-id: 535c28c7-179d-4edc-b140-880b9dfe1d59
source-git-commit: d40c25f75103327e749ad864b17df926cb323be0
workflow-type: ht
source-wordcount: '897'
ht-degree: 100%

---

# Utenti

Aggiungere utenti e gestirne le autorizzazioni in [!DNL Adobe Admin Console] per un account [!DNL Target Standard].

>[!NOTE]
>
>Le funzionalità [!UICONTROL Proprietà] e [!UICONTROL Autorizzazioni] sono disponibili come parte della [!DNL Target Premium] soluzione. Non sono disponibili in [!DNL Target] Standard senza una licenza [!DNL Target] Premium.
>
>Per verificare se la tua organizzazione dispone di una licenza [!UICONTROL Standard] o [!UICONTROL Premium], fai clic sul collegamento [!UICONTROL Amministrazione] in alto nell’interfaccia utente di [!DNL Target].
>
>* **[!DNL Target]Clienti Standard**: se è presente la scheda [!UICONTROL Utenti] ([!UICONTROL Amministrazione > Utenti]) (e non la scheda **[!UICONTROL Proprietà]**), la tua organizzazione dispone di una licenza [!DNL Target] Standard.  [!DNL Target]I clienti Standard possono seguire le istruzioni riportate in questo argomento per aggiungere utenti e assegnare autorizzazioni in [!DNL Adobe Admin Console].
>
>* Clienti **[!DNL Target]Premium**: se sono presenti le schede [!UICONTROL Utenti] e [!UICONTROL Proprietà] ([!UICONTROL Amministrazione > Proprietà]), la tua organizzazione dispone di una licenza [!DNL Target] Premium. I clienti [!DNL Target] Premium devono seguire le istruzioni contenute in [Enterprise User Permissions](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) (Autorizzazioni utente di Enterprise) e [Configure enterprise permissions](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md) (Configurazione delle autorizzazioni Enterprise) per aggiungere utenti e assegnare le autorizzazioni in [!DNL Adobe Admin Console].
>
>Per informazioni dettagliate su come gestire utenti e autorizzazioni, consulta [Gestione di prodotti e profili di prodotto](https://helpx.adobe.com/it/enterprise/using/manage-products-and-profiles.html) nella *guida utente di Enterprise &amp; Teams*.

Quando inizi a usare [!DNL Adobe Target], troverai gli ID (che terminano con Adobe.com) pre-popolati nel tuo account [!DNL Adobe Experience Cloud]. Questi ID sono per i membri dei team [!DNL Adobe], in modo che possano aiutarti con il tuo nuovo account e con l’uso di [!DNL Adobe Target], se hai bisogno di assistenza. Per ottenere assistenza, contatta i team Adobe di riferimento con le modalità usuali.

I nuovi utenti non verranno visualizzati nell’elenco [!UICONTROL Utenti] fino a quando il visitatore effettua l’accesso con il proprio account [!DNL Adobe Experience Cloud] e quindi accede a [!DNL Target].

Per impostazione predefinita, tutti gli utenti [!DNL Target] iniziano con autorizzazioni con il ruolo da [!UICONTROL Osservatore].

Gli utenti Admin di sono identificati nell’elenco [!UICONTROL Utenti]. Se hai bisogno di un diverso livello di accesso, contatta uno degli utenti amministratori di sistema.

## Visualizzazione delle informazioni utente all’interno di [!DNL Target]

Puoi visualizzare un elenco degli utenti correnti nell’interfaccia [!DNL Target], inclusi i ruoli per area di lavoro e gli indirizzi e-mail.

Per visualizzare la pagina [!UICONTROL Utenti], fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Utenti]**.

![Elenco utenti all’interno di Target](/help/main/administrating-target/c-user-management/c-user-management/assets/user-list-target.png)

>[!NOTE]
>
>Per gestire un utente esistente o aggiungere nuovi utenti, è necessario utilizzare [!UICONTROL Adobe Admin Console], come spiegato di seguito.

## Accedere a [!DNL Adobe Admin Console] {#access}

Per le attività da eseguire in [!DNL Adobe Admin Console] , accedi alla console seguendo questi passaggi:

1. Da [!DNL Target], fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Utenti]** > **[!UICONTROL Gestione utente]**.

   Oppure

   Vai su [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/) e, se non hai già effettuato l’accesso, accedi con il tuo Adobe ID.

1. (Facoltativo) Se disponi dell’accesso ad [!DNL Admin Console for Enterprise] per più di un’organizzazione, fai clic sull’avatar utente nell’angolo a destra o sulla barra di navigazione superiore, quindi seleziona l’organizzazione desiderata.

## Aggiunta di utenti {#add-users}

Tutte le operazioni di gestione dell’utente devono essere eseguite in [!DNL Adobe Admin Console for Enterprise]. Tuttavia, tutti gli utenti esistenti in [!DNL Target] verranno migrati da [!DNL Target] ad [!DNL Admin Console for Enterprise].

1. [In Admin Console](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE), fai clic su **[!UICONTROL Utenti]** > **[!UICONTROL Utenti]** per creare nuovi utenti o modificare quelli esistenti.
1. Segui le istruzioni contenute in [Gestire utenti e gruppi in Experience Cloud](https://helpx.adobe.com/it/enterprise/using/users.html) nella *guida utente della versione Enterprise*.

## Creazione di gruppi di utenti {#user-groups}

È possibile creare gruppi di utenti, ad esempio sviluppatori, analisti, addetti al marketing, dirigenti e così via, e assegnare privilegi a più prodotti e aree di lavoro di [!DNL Adobe]. Per assegnare a un nuovo membro del team tutti i privilegi appropriati per i diversi prodotti [!DNL Adobe], sarà sufficiente aggiungerlo a un gruppo di utenti specifico.

1. [In Admin Console](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE), fai clic su **[!UICONTROL Utenti]** > **[!UICONTROL Gruppi utenti]** per creare nuovi gruppi di utenti o modificare quelli esistenti.
1. Segui le istruzioni contenute in [Gestire utenti e gruppi in Experience Cloud](https://helpx.adobe.com/it/enterprise/using/users.html) nella *guida utente della versione Enterprise*.

## Specificare ruoli e autorizzazioni {#roles-permissions}

Solo gli amministratori di sistema possono impostare i ruoli utente in [!DNL Target]. Ad esempio, un utente approvatore [!UICONTROL Standard] non può attribuire a un utente osservatore il ruolo di approvatore, se non ha i diritti di Amministratore [!DNL Experience Cloud].

Devono essere gli utenti amministratori di sistema ad aggiungere gli utenti al sistema. Gli utenti non vengono aggiunti automaticamente. Vengono invitati via e-mail da [!DNL Experience Cloud] e dovranno confermare i propri indirizzi prima che i relativi account vengano registrati.

1. [In Admin Console](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE), fai clic su **[!UICONTROL Prodotti]**, quindi seleziona il nome del prodotto desiderato.

   ![Scheda Prodotti](/help/main/administrating-target/c-user-management/c-user-management/assets/workspace-publisher.png)

1. Fai clic sull’area di lavoro desiderata, ad esempio Default Workspace (Area di lavoro predefinita).

   ![Default Workspace (Area di lavoro predefinita)](/help/main/administrating-target/c-user-management/c-user-management/assets/default-workspace-new.png)

   Nella scheda [!UICONTROL Utenti] vengono visualizzati tutti gli utenti di quell’area di lavoro.

   ![configurazione degli utenti](/help/main/administrating-target/c-user-management/c-user-management/assets/configuration_users-new-publisher.png)

1. Seleziona il ruolo di autorizzazioni desiderato ([!UICONTROL Approvatore], [!UICONTROL Editor] [!UICONTROL Osservatore] o [!UICONTROL Editore]) dall’elenco a discesa per ogni utente nella colonna [!UICONTROL Ruolo prodotto].

   ![Elenco a discesa Product Role (Ruolo prodotto)](/help/main/administrating-target/c-user-management/c-user-management/assets/product-role-new.png)

   | Ruolo | Descrizione |
   |--- |--- |
   | [!UICONTROL Approvatore] | Può creare, modificare, attivare o interrompere le attività. |
   | [!UICONTROL Editor] | Può creare e modificare le attività prima che siano in diretta, ma non può approvare l’avvio di un’attività. |
   | [!UICONTROL Osservatore] | Può visualizzare le attività, ma non può crearle o modificarle. |
   | [!UICONTROL Editore] | Simile al ruolo [!UICONTROL Osservatore] (può visualizzare le attività, ma non può crearle o modificarle). Tuttavia, il ruolo [!UICONTROL Editore] è anche autorizzato ad attivare le attività. |

Per ulteriori informazioni, vedi [Gestione delle autorizzazioni del prodotto in Admin Console](https://helpx.adobe.com/it/enterprise/using/manage-permissions-and-roles.html) nella *guida utente della versione Enterprise*.

## Video di formazione: configurazione delle aree di lavoro di Adobe Target ![Icona esercitazione](/help/main/assets/tutorial.png)

Finalità di apprendimento:

* Accedere ad Admin Console dall’interfaccia di Adobe Target (tre modi)
* Configurare un’area di lavoro in Adobe Admin Console
   * Aggiungere utenti alle aree di lavoro
   * Aggiungere proprietà alle aree di lavoro
* Comprendere le aree di lavoro predefinite

>[!NOTE]
>
>L’interfaccia utente di [!DNL Target] del menu [!UICONTROL Amministrazione] (precedentemente [!UICONTROL Configurazione]) è stato riprogettato per fornire prestazioni migliori, ridurre il tempo di manutenzione necessario durante il rilascio di nuove funzioni e migliorare l’esperienza utente nel prodotto. Le informazioni contenute nel video seguente sono generalmente corrette; tuttavia, le opzioni potrebbero trovarsi in punti leggermente diversi. I video aggiornati verranno pubblicati a breve.

>[!VIDEO](https://video.tv.adobe.com/v/19463/)
