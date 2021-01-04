---
keywords: add user;manage user;user permissions
description: Aggiungi utenti a  Adobe Target e gestisci le loro autorizzazioni in Adobe Admin Console.
title: Utenti
feature: Administration & Configuration
translation-type: tm+mt
source-git-commit: 1c5fd1062da5f90f24720fc3deb67f7f3b05aee9
workflow-type: tm+mt
source-wordcount: '892'
ht-degree: 46%

---


# Utenti{#users}

Aggiungi utenti e gestisci le loro autorizzazioni in [!DNL Adobe Admin Console].

>[!NOTE]
>
>Le funzionalità [!UICONTROL Proprietà] e [!UICONTROL Autorizzazioni] sono disponibili come parte della soluzione [!DNL Target] Premium. Non sono disponibili in [!DNL Target] Standard senza una licenza [!DNL Target] Premium.
>Per verificare se l&#39;organizzazione dispone di una licenza Standard o Premium, fare clic sul collegamento [!UICONTROL Amministrazione] nella parte superiore dell&#39;interfaccia utente [!DNL Target].
>
>* **[!DNL Target]Clienti** standard: Se viene visualizzata la   scheda Utente ([!UICONTROL Amministrazione > Utenti]) (e non la  **** scheda Proprietà), l&#39;organizzazione dispone di una licenza  [!DNL Target] Standard. [!DNL Target]I clienti [! Standard possono seguire le istruzioni riportate in questo argomento per aggiungere utenti e assegnare autorizzazioni in [!DNL Adobe Admin Console].
   >
   >
* **[!DNL Target]Clienti** Premium: Se visualizzate la   scheda Utente e la scheda   Proprietà ([!UICONTROL Amministrazione > Proprietà]), l&#39;organizzazione dispone di una licenza  [!DNL Target] Premium. I clienti [!DNL Target] Premium devono seguire le istruzioni contenute in [Autorizzazioni per gli utenti Enterprise](/help/administrating-target/c-user-management/property-channel/property-channel.md) e [Configurare le autorizzazioni Enterprise](/help/administrating-target/c-user-management/property-channel/properties-overview.md) per aggiungere utenti e assegnare le autorizzazioni in [!DNL Adobe Admin Console].
>
>
Per informazioni dettagliate su come gestire utenti e autorizzazioni, vedere [Gestione di prodotti e profili](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html) nella *Enterprise &amp; Teams User Guide*.

Quando inizi a usare [!DNL Adobe Target], troverai gli ID (che terminano con Adobe.com) pre-popolati nel tuo account [!DNL Adobe Experience Cloud]. Questi ID sono per i membri dei team [!DNL Adobe] in modo che possano assistervi con il vostro nuovo account e con l&#39;utilizzo di [!DNL Adobe Target], se necessario. Per ottenere assistenza, contatta i team Adobe di riferimento con le modalità usuali.

Il nuovo utente verrà elencato nella pagina [!UICONTROL Utenti] solo dopo che l&#39;utente avrà effettuato l&#39;accesso utilizzando il proprio account [!DNL Adobe Experience Cloud] e quindi effettuerà l&#39;accesso a [!DNL Target Standard/Premium].

Per impostazione predefinita, a tutti gli utenti di [!DNL Target] viene assegnato inizialmente il ruolo di Osservatore.

Gli utenti amministratore sono identificati nell&#39;elenco [!UICONTROL Utenti]. Contattate uno degli utenti amministratori di sistema se avete bisogno di modificare il livello di accesso.

## Visualizzazione delle informazioni utente dall&#39;interno di Target

Puoi visualizzare un elenco degli utenti correnti nell&#39;ambiente Target, inclusi i ruoli per area di lavoro e gli indirizzi e-mail direttamente dall&#39;interno di Target.

Per visualizzare la pagina Utenti, fare clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Utenti]**.

![Elenco utenti da Target](/help/administrating-target/c-user-management/c-user-management/assets/user-list-target.png)

>[!NOTE]
>
>Per gestire l&#39;utente esistente o aggiungere nuovi utenti, è necessario utilizzare l&#39; [!UICONTROL Adobe Admin Console], come illustrato di seguito.

## Accedere ad Adobe Admin Console {#access}

Per le attività da eseguire in Adobe Admin Console, accedi alla console seguendo questi passaggi:

1. Dall&#39;interno di [!DNL Target], fare clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Utenti]** > **[!UICONTROL Gestione utenti]**.

   Oppure

   Andate a https://adminconsole.adobe.com/enterprise/[](https://adminconsole.adobe.com/enterprise/), quindi effettuate l&#39;accesso utilizzando l&#39;Adobe ID , se non avete già eseguito l&#39;accesso.

1. (Condizionale) Se disponi dell&#39;accesso ad [!DNL Admin Console for Enterprise] per più di un’organizzazione, fai clic sull’avatar utente nell’angolo a destra o sulla barra di navigazione superiore, quindi seleziona l’organizzazione desiderata.

## Aggiungi utenti {#add-users}

Tutte le operazioni di gestione dell’utente devono essere eseguite in [!DNL Adobe Admin Console for Enterprise]. Tuttavia, tutti gli utenti esistenti in [!DNL Target] verranno migrati da [!DNL Target] ad [!DNL Admin Console for Enterprise].

1. [Nel Admin Console](/help/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE) , fate clic su  **[!UICONTROL Utenti]** >  **** Utenti per creare nuovi utenti o per modificare utenti esistenti.
1. Segui le istruzioni contenute in [Gestire utenti e gruppi in Experience Cloud](https://helpx.adobe.com/enterprise/help/users.html) nella *guida utente della versione Enterprise*.

## Creare gruppi di utenti {#user-groups}

È possibile creare gruppi di utenti, ad esempio sviluppatori, analisti, addetti al marketing, dirigenti e così via, e assegnare privilegi a più prodotti Adobe e aree di lavoro. Per assegnare a un nuovo membro del team tutti i privilegi appropriati per i diversi prodotti Adobe, sarà sufficiente aggiungerlo a un gruppo di utenti specifico.

1. [Nel Admin Console](/help/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE) , fate clic su  **[!UICONTROL Utenti]**  >  **[!UICONTROL Gruppi di utenti]** per creare nuovi gruppi di utenti o per modificare i gruppi esistenti.
1. Segui le istruzioni contenute in [Gestire utenti e gruppi in Experience Cloud](https://helpx.adobe.com/enterprise/help/users.html) nella *guida utente della versione Enterprise*.

## Specificare ruoli e autorizzazioni {#roles-permissions}

Solo gli amministratori di sistema possono impostare i ruoli utente in [!DNL Target]. Ad esempio, un utente approver Standard non può convertire un osservatore in un approver, senza avere anche diritti di amministratore [!DNL Experience Cloud].

Devono essere gli utenti amministratori di sistema ad aggiungere gli utenti al sistema. Gli utenti non vengono aggiunti automaticamente. Vengono invitati via e-mail da [!DNL Experience Cloud] e devono confermare i propri indirizzi e-mail prima di registrare gli account.

1. [In Admin Console](/help/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE), fai clic su **[!UICONTROL Prodotti]**, quindi seleziona il nome del prodotto desiderato.

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

## Video di formazione: Come configurare le aree di lavoro di destinazione ![badge di esercitazione](/help/assets/tutorial.png)

Finalità di apprendimento:

* Accedere ad Admin Console dall’interfaccia di Adobe Target (tre modi)
* Configurare un’area di lavoro in Adobe Admin Console
   * Aggiungere utenti alle aree di lavoro
   * Aggiungere proprietà alle aree di lavoro
* Comprendere le aree di lavoro predefinite

>[!NOTE]
>
>L&#39;interfaccia utente del menu [!DNL Target] [!UICONTROL Administration] (precedentemente [!UICONTROL Setup]) è stata riprogettata per fornire prestazioni migliorate, ridurre il tempo di manutenzione necessario per il rilascio delle nuove funzioni e migliorare l&#39;esperienza dell&#39;utente in tutto il prodotto. Le informazioni riportate nel seguente video sono generalmente corrette; tuttavia, le opzioni potrebbero trovarsi in posizioni leggermente diverse. I video aggiornati verranno pubblicati a breve.

>[!VIDEO](https://video.tv.adobe.com/v/19463/)
