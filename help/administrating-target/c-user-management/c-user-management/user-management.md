---
keywords: add user;manage user;user permissions
description: Puoi aggiungere utenti e gestirne le autorizzazioni in Adobe Admin Console.
title: Utenti
feature: null
subtopic: Getting Started
topic: Standard
uuid: 9b311dd3-b8fa-483d-aedd-96761cfcd67e
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '895'
ht-degree: 48%

---


# Utenti{#users}

You can add users and manage their permissions in the [!DNL Adobe Admin Console].

>[!NOTE]
>
>Le funzionalità [!UICONTROL Proprietà] e [!UICONTROL Autorizzazioni] sono disponibili come parte della soluzione [!DNL Target] Premium. Non sono disponibili in [!DNL Target] Standard senza una licenza [!DNL Target] Premium.
>You can tell whether your organization has a Standard or Premium license by clicking the [!UICONTROL Administration] link at the top of the [!DNL Target] UI.
>
>* **[!DNL Target]Clienti **standard: Se viene visualizzata la scheda[!UICONTROL Utenti]([!UICONTROL Amministrazione > Utenti]) (e non la scheda**[!UICONTROL Proprietà&#x200B;]**), l&#39;organizzazione dispone di una licenza[!DNL Target]Standard. I clienti [!DNL Target Standard possono seguire le istruzioni riportate in questo argomento per aggiungere utenti e assegnare autorizzazioni in[!DNL Adobe Admin Console].
   >
   >
* **[!DNL Target]Clienti **Premium: Se vengono visualizzate le schede[!UICONTROL Utenti]e[!UICONTROL Proprietà]([!UICONTROL Amministrazione > Proprietà]), l&#39;organizzazione dispone di una licenza[!DNL Target]Premium. I clienti[!DNL Target]Premium devono seguire le istruzioni contenute in[Autorizzazioni per gli utenti Enterprise](/help/administrating-target/c-user-management/property-channel/property-channel.md)e[Configurare le autorizzazioni Enterprise](/help/administrating-target/c-user-management/property-channel/properties-overview.md)per aggiungere utenti e assegnare le autorizzazioni in[!DNL Adobe Admin Console].
>
>
Per informazioni dettagliate su come gestire utenti e autorizzazioni, consultate [Gestire prodotti e profili](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html) nella Guida *utente di* Enterprise &amp; Teams.

Quando inizi a usare [!DNL Adobe Target], troverai gli ID (che terminano con Adobe.com) pre-popolati nel tuo account [!DNL Adobe Experience Cloud]. These IDs are for members of [!DNL Adobe] teams so that they can assist you with your new account and with your use of [!DNL Adobe Target], should you need help. Per ottenere assistenza, contatta i team Adobe di riferimento con le modalità usuali.

You will not see the new user listed on the [!UICONTROL Users] page until the user logs in using his or her [!DNL Adobe Experience Cloud] account and then logs in to [!DNL Target Standard/Premium].

Per impostazione predefinita, a tutti gli utenti di [!DNL Target] viene assegnato inizialmente il ruolo di Osservatore.

Admin users are identified in the [!UICONTROL Users] list. Contattate uno degli utenti amministratori di sistema se avete bisogno di modificare il livello di accesso.

## Visualizzazione delle informazioni utente dall&#39;interno di Target

Puoi visualizzare un elenco degli utenti correnti nell&#39;ambiente Target, inclusi i ruoli per area di lavoro e gli indirizzi e-mail direttamente dall&#39;interno di Target.

Per visualizzare la pagina Utenti, fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Utenti]**.

![Elenco utenti da Target](/help/administrating-target/c-user-management/c-user-management/assets/user-list-target.png)

>[!NOTE]
>
>Per gestire un utente esistente o aggiungere nuovi utenti, è necessario utilizzare l&#39; [!UICONTROL Adobe Admin Console], come illustrato di seguito.

## Accedere ad Adobe Admin Console {#access}

Per le attività da eseguire in Adobe Admin Console, accedi alla console seguendo questi passaggi:

1. Dall’interno [!DNL Target], fate clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Utenti]** > Gestione **** utenti.

   Oppure

   Go to [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/), then sign in using your Adobe ID, if you have not already logged in.

1. (Condizionale) Se disponi dell&#39;accesso ad [!DNL Admin Console for Enterprise] per più di un’organizzazione, fai clic sull’avatar utente nell’angolo a destra o sulla barra di navigazione superiore, quindi seleziona l’organizzazione desiderata.

## Add users {#add-users}

Tutte le operazioni di gestione dell’utente devono essere eseguite in [!DNL Adobe Admin Console for Enterprise]. Tuttavia, tutti gli utenti esistenti in [!DNL Target] verranno migrati da [!DNL Target] ad [!DNL Admin Console for Enterprise].

1. [Nel Admin Console](../../../administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE), fate clic su **[!UICONTROL Utenti]** > **[!UICONTROL Utenti]** per creare nuovi utenti o per modificare utenti esistenti.
1. Segui le istruzioni contenute in [Gestire utenti e gruppi in Experience Cloud](https://helpx.adobe.com/enterprise/help/users.html) nella *guida utente della versione Enterprise*.

## Create user groups {#user-groups}

È possibile creare gruppi di utenti, ad esempio sviluppatori, analisti, addetti al marketing, dirigenti e così via, e assegnare privilegi a più prodotti Adobe e aree di lavoro. Per assegnare a un nuovo membro del team tutti i privilegi appropriati per i diversi prodotti Adobe, sarà sufficiente aggiungerlo a un gruppo di utenti specifico.

1. [Nel Admin Console](../../../administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE), fate clic su **[!UICONTROL Utenti]** > Gruppi **[!UICONTROL di]** utenti per creare nuovi gruppi di utenti o per modificare i gruppi esistenti.
1. Segui le istruzioni contenute in [Gestire utenti e gruppi in Experience Cloud](https://helpx.adobe.com/enterprise/help/users.html) nella *guida utente della versione Enterprise*.

## Specify roles and permissions {#roles-permissions}

Solo gli amministratori di sistema possono impostare i ruoli utente in [!DNL Target]. For example, a Standard approver user cannot change an observer to an approver, without also having [!DNL Experience Cloud] Admin rights.

Devono essere gli utenti amministratori di sistema ad aggiungere gli utenti al sistema. Gli utenti non vengono aggiunti automaticamente. They are invited by email from the [!DNL Experience Cloud] and must confirm their email addresses before their accounts are registered.

1. [In Admin Console](../../../administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE), fai clic su **[!UICONTROL Prodotti]**, quindi seleziona il nome del prodotto desiderato.

   ![Scheda Prodotti](/help/administrating-target/c-user-management/c-user-management/assets/workspace-publisher.png)

1. Fate clic sull’area di lavoro desiderata (ad esempio, Area di lavoro predefinita).

   ![Area di lavoro predefinita](/help/administrating-target/c-user-management/c-user-management/assets/default-workspace-new.png)

   Nella scheda [!UICONTROL Utenti] vengono visualizzati tutti gli utenti di quell’area di lavoro.

   ![configurazione degli utenti](/help/administrating-target/c-user-management/c-user-management/assets/configuration_users-new-publisher.png)

1. Seleziona il ruolo di autorizzazioni desiderato (Approvatore, Editor o Osservatore) dall’elenco a discesa per ogni utente nella colonna [!UICONTROL Ruolo prodotto].

   ![Elenco a discesa Ruolo prodotto](/help/administrating-target/c-user-management/c-user-management/assets/product-role-new.png)

   | Ruolo | Descrizione |
   |--- |--- |
   | Approvatore | Può creare, modificare, attivare o interrompere le attività. |
   | Editor | può creare e modificare le attività prima che siano in diretta, ma non può approvare l&#39;avvio di un&#39;attività. |
   | Osservatore | Può visualizzare le attività, ma non può crearle o modificarle. |
   | Editore | Simile al ruolo Osservatore (può visualizzare le attività, ma non può crearle o modificarle). Tuttavia, il ruolo Editore dispone dell&#39;autorizzazione aggiuntiva per attivare le attività. |

Per ulteriori informazioni, vedi [Gestione delle autorizzazioni del prodotto in Admin Console](https://helpx.adobe.com/enterprise/help/manage-permissions-and-roles.html) nella *guida utente della versione Enterprise*.

## Training video: How to Configure Target Workspaces ![Tutorial badge](/help/assets/tutorial.png)

Finalità di apprendimento:

* Accedere ad Admin Console dall’interfaccia di Adobe Target (tre modi)
* Configurare un’area di lavoro in Adobe Admin Console
   * Aggiungere utenti alle aree di lavoro
   * Aggiungere proprietà alle aree di lavoro
* Comprendere le aree di lavoro predefinite

>[!NOTE]
>
>L’interfaccia utente del menu [!DNL Target] Amministrazione [!UICONTROL (precedentemente] Configurazione ) è stata riprogettata per fornire prestazioni migliori, ridurre il tempo di manutenzione necessario per rilasciare nuove funzioni e migliorare l’esperienza dell’utente nel prodotto. Le informazioni riportate nel seguente video sono generalmente corrette; tuttavia, le opzioni potrebbero trovarsi in posizioni leggermente diverse. I video aggiornati verranno pubblicati a breve.

>[!VIDEO](https://video.tv.adobe.com/v/19463/)
