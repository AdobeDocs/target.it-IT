---
keywords: add user;manage user;user permissions
description: Puoi aggiungere utenti e gestirne le autorizzazioni in Adobe Admin Console.
title: Utenti
subtopic: Getting Started
topic: Standard
uuid: 9b311dd3-b8fa-483d-aedd-96761cfcd67e
translation-type: tm+mt
source-git-commit: 2c34371005be851b2a86113050c01182334c2dc9
workflow-type: tm+mt
source-wordcount: '748'
ht-degree: 62%

---


# Utenti{#users}

You can add users and manage their permissions in the [!DNL Adobe Admin Console].

>[!NOTE]
>
>Le funzionalità [!UICONTROL Proprietà] e [!UICONTROL Autorizzazioni] sono disponibili come parte della soluzione [!DNL Target] Premium. Non sono disponibili in [!DNL Target] Standard senza una licenza [!DNL Target] Premium.
>You can tell whether your organization has a Standard or Premium license by clicking the [!UICONTROL Administration] link at the top of the [!DNL Target] UI.
>
>**[!DNL Target]Clienti **standard: Se viene visualizzata la scheda[!UICONTROL Utenti]([!UICONTROL Amministrazione > Utenti]) (e non la scheda**[!UICONTROL Proprietà&#x200B;]**), l&#39;organizzazione dispone di una licenza[!DNL Target]Standard. I clienti [!DNL Target Standard possono seguire le istruzioni riportate in questo argomento per aggiungere utenti e assegnare autorizzazioni in[!DNL Adobe Admin Console].
>
>**[!DNL Target]Clienti **Premium: Se vengono visualizzate le schede[!UICONTROL Utenti]e[!UICONTROL Proprietà]([!UICONTROL Amministrazione > Proprietà]), l&#39;organizzazione dispone di una licenza[!DNL Target]Premium. I clienti[!DNL Target]Premium devono seguire le istruzioni contenute in[Autorizzazioni per gli utenti Enterprise](/help/administrating-target/c-user-management/property-channel/property-channel.md)e[Configurare le autorizzazioni Enterprise](/help/administrating-target/c-user-management/property-channel/properties-overview.md)per aggiungere utenti e assegnare le autorizzazioni in[!DNL Adobe Admin Console].

Per gestire utenti e autorizzazioni, consulta [Gestione di prodotti e profili](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html) nella Guida *utente di* Enterprise &amp; Teams.

Quando inizi a usare [!DNL Adobe Target], troverai gli ID (che terminano con Adobe.com) pre-popolati nel tuo account [!DNL Adobe Experience Cloud]. Questi ID sono per i membri dei team Adobe in modo che possano aiutarti con il tuo nuovo account e con l&#39;uso di [!DNL Adobe Target], se hai bisogno di aiuto. Per ottenere assistenza, contatta i team Adobe di riferimento con le modalità usuali.

You will not see the new user listed on the [!UICONTROL Users] page until the user logs in using his or her [!DNL Adobe Experience Cloud] account and then logs in to [!DNL Target Standard/Premium].

Per impostazione predefinita, a tutti gli utenti di [!DNL Target] viene assegnato inizialmente il ruolo di Osservatore.

Admin users are identified in the [!UICONTROL Users] list. Contattate uno degli utenti amministratori di sistema se avete bisogno di modificare il livello di accesso.

## Accedere ad Adobe Admin Console {#access}

Per le attività da eseguire in Adobe Admin Console, accedi alla console seguendo questi passaggi:

1. Dall’interno [!DNL Target], fate clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Utenti]** > Gestione **** utenti.

   Oppure

   Go to [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/), then sign in using your Adobe ID, if you have not already logged in.

1. (Condizionale) Se disponi dell&#39;accesso ad [!DNL Admin Console for Enterprise] per più di un’organizzazione, fai clic sull’avatar utente nell’angolo a destra o sulla barra di navigazione superiore, quindi seleziona l’organizzazione desiderata.

## Aggiungi utenti {#add-users}

Tutte le operazioni di gestione dell’utente devono essere eseguite in [!DNL Adobe Admin Console for Enterprise]. Tuttavia, tutti gli utenti esistenti in [!DNL Target] verranno migrati da [!DNL Target] ad [!DNL Admin Console for Enterprise].

1. [In Admin Console](../../../administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE), fai clic su **[!UICONTROL Utenti]** > **[!UICONTROL Utenti]** per creare nuovi utenti o per modificare utenti esistenti.
1. Segui le istruzioni contenute in [Gestire utenti e gruppi in Experience Cloud](https://helpx.adobe.com/enterprise/help/users.html) nella *guida utente della versione Enterprise*.

## Creare gruppi di utenti {#user-groups}

È possibile creare gruppi di utenti, ad esempio sviluppatori, analisti, addetti al marketing, dirigenti e così via, e assegnare privilegi a più prodotti Adobe e aree di lavoro. Per assegnare a un nuovo membro del team tutti i privilegi appropriati per i diversi prodotti Adobe, sarà sufficiente aggiungerlo a un gruppo di utenti specifico.

1. [In Admin Console](../../../administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE), fai clic su **[!UICONTROL Utenti]** > Gruppi **[!UICONTROL di]** utenti per creare nuovi gruppi di utenti o per modificare i gruppi esistenti.
1. Segui le istruzioni contenute in [Gestire utenti e gruppi in Experience Cloud](https://helpx.adobe.com/enterprise/help/users.html) nella *guida utente della versione Enterprise*.

## Specificare ruoli e autorizzazioni {#roles-permissions}

Solo gli amministratori di sistema possono impostare i ruoli utente in [!DNL Target]. For example, a Standard approver user cannot change an observer to an approver, without also having [!DNL Experience Cloud] Admin rights.

Devono essere gli utenti amministratori di sistema ad aggiungere gli utenti al sistema. Gli utenti non vengono aggiunti automaticamente. They are invited by email from the [!DNL Experience Cloud] and must confirm their email addresses before their accounts are registered.

1. [In Admin Console](../../../administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE), fai clic su **[!UICONTROL Prodotti]**, quindi seleziona il nome del prodotto desiderato.

   ![Scheda Prodotti](/help/administrating-target/c-user-management/c-user-management/assets/workspace-new.png)

1. Fate clic sull’area di lavoro desiderata (ad esempio, Area di lavoro predefinita).

   ![Area di lavoro predefinita](/help/administrating-target/c-user-management/c-user-management/assets/default-workspace.png)

   Nella scheda [!UICONTROL Utenti] vengono visualizzati tutti gli utenti di quell’area di lavoro.

   ![configurazione degli utenti](/help/administrating-target/c-user-management/c-user-management/assets/configuration_users-new.png)

1. Seleziona il ruolo di autorizzazioni desiderato (Approvatore, Editor o Osservatore) dall’elenco a discesa per ogni utente nella colonna [!UICONTROL Ruolo prodotto].

   ![Elenco a discesa Ruolo prodotto](/help/administrating-target/c-user-management/c-user-management/assets/product-role.png)

   | Ruolo | Descrizione |
   |--- |--- |
   | Approvatore | Può creare, modificare, attivare o interrompere le attività. |
   | Editor | può creare e modificare le attività prima che siano in diretta, ma non può approvare l&#39;avvio di un&#39;attività. |
   | Osservatore | Può visualizzare le attività, ma non può crearle o modificarle. |

Per ulteriori informazioni, vedi [Gestione delle autorizzazioni del prodotto in Admin Console](https://helpx.adobe.com/enterprise/help/manage-permissions-and-roles.html) nella *guida utente della versione Enterprise*.

## Training video: How to Configure Target Workspaces ![Tutorial badge](/help/assets/tutorial.png)

Finalità di apprendimento:

* Accedere ad Admin Console dall’interfaccia di Adobe Target (tre modi)
* Configurare un’area di lavoro in Adobe Admin Console
   * Aggiungere utenti alle aree di lavoro
   * Aggiungere proprietà alle aree di lavoro
* Comprendere le aree di lavoro predefinite

>[!VIDEO](https://video.tv.adobe.com/v/19463/)
