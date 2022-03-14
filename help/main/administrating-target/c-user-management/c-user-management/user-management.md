---
keywords: aggiungere utente;gestire utente;autorizzazioni utente
description: Scopri come utilizzare Adobe Admin Console per gestire gli utenti e le loro autorizzazioni e i loro diritti in Adobe Target.
title: Come si aggiungono utenti e si gestiscono le autorizzazioni?
feature: Administration & Configuration
role: Admin
exl-id: 535c28c7-179d-4edc-b140-880b9dfe1d59
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '911'
ht-degree: 47%

---

# Utenti

Aggiungi utenti e gestisci le relative autorizzazioni in [!DNL Adobe Admin Console].

>[!NOTE]
>
>Le funzionalità [!UICONTROL Proprietà] e [!UICONTROL Autorizzazioni] sono disponibili come parte della soluzione [!DNL Target] Premium. Non sono disponibili in [!DNL Target] Standard senza una licenza [!DNL Target] Premium.
>Per verificare se la tua organizzazione dispone di una licenza Standard o Premium, fai clic sul pulsante [!UICONTROL Amministrazione] nella parte superiore della [!DNL Target] Interfaccia utente.
>
>* **[!DNL Target]Clienti standard**: Se vedi la [!UICONTROL Utenti] scheda ([!UICONTROL Amministrazione > Utenti]) (e non il **[!UICONTROL Proprietà]** , la tua organizzazione dispone di un [!DNL Target] Licenza standard. [!DNL Target]I clienti [! Standard possono seguire le istruzioni riportate in questo argomento per aggiungere utenti e assegnare autorizzazioni in [!DNL Adobe Admin Console].
>
>* **[!DNL Target]Clienti Premium**: Se vedi la [!UICONTROL Utenti] e [!UICONTROL Proprietà] scheda ([!UICONTROL Amministrazione > Proprietà]), la tua organizzazione dispone di un [!DNL Target] Licenza Premium. I clienti [!DNL Target] Premium devono seguire le istruzioni contenute in [Autorizzazioni per gli utenti Enterprise](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) e [Configurare le autorizzazioni Enterprise](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md) per aggiungere utenti e assegnare le autorizzazioni in [!DNL Adobe Admin Console].
>
>Per informazioni dettagliate su come gestire utenti e autorizzazioni, consulta [Gestione di prodotti e profili](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html) in *Guida utente Enterprise e Team*.

Quando inizi a usare [!DNL Adobe Target], troverai gli ID (che terminano con Adobe.com) pre-popolati nel tuo account [!DNL Adobe Experience Cloud]. Questi ID sono per i membri di [!DNL Adobe] team in modo che possano aiutarti con il tuo nuovo account e con l&#39;utilizzo di [!DNL Adobe Target]Se hai bisogno di aiuto. Per ottenere assistenza, contatta i team Adobe di riferimento con le modalità usuali.

Il nuovo utente non verrà visualizzato nella sezione [!UICONTROL Utenti] fino a quando l’utente non effettua l’accesso utilizzando [!DNL Adobe Experience Cloud] e quindi effettua l&#39;accesso a [!DNL Target Standard/Premium].

Per impostazione predefinita, a tutti gli utenti di [!DNL Target] viene assegnato inizialmente il ruolo di Osservatore.

Gli utenti amministratore sono identificati nella sezione [!UICONTROL Utenti] elenco. Contatta uno degli utenti amministratori di sistema se hai bisogno di modificare il livello di accesso.

## Visualizzazione delle informazioni utente da Target

Puoi visualizzare un elenco degli utenti correnti nel tuo ambiente Target, inclusi i loro ruoli per area di lavoro e gli indirizzi e-mail direttamente dall’interno di Target.

Per visualizzare la pagina Utenti, fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Utenti]**.

![Elenco utenti da Target](/help/main/administrating-target/c-user-management/c-user-management/assets/user-list-target.png)

>[!NOTE]
>
>Per gestire l&#39;utente esistente o aggiungere nuovi utenti, è necessario utilizzare il [!UICONTROL Adobe Admin Console], come spiegato di seguito.

## Accedere ad Adobe Admin Console {#access}

Per le attività da eseguire in Adobe Admin Console, accedi alla console seguendo questi passaggi:

1. Da [!DNL Target], fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Utenti]** > **[!UICONTROL Gestione utenti]**.

   Oppure

   Vai a [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/), quindi effettua l’accesso con il tuo Adobe ID, se non hai già effettuato l’accesso.

1. (Condizionale) Se disponi dell&#39;accesso ad [!DNL Admin Console for Enterprise] per più di un’organizzazione, fai clic sull’avatar utente nell’angolo a destra o sulla barra di navigazione superiore, quindi seleziona l’organizzazione desiderata.

## Aggiungi utenti {#add-users}

Tutte le operazioni di gestione dell’utente devono essere eseguite in [!DNL Adobe Admin Console for Enterprise]. Tuttavia, tutti gli utenti esistenti in [!DNL Target] verranno migrati da [!DNL Target] ad [!DNL Admin Console for Enterprise].

1. [Nell’Admin Console](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE), fai clic su **[!UICONTROL Utenti]** > **[!UICONTROL Utenti]** per creare nuovi utenti o modificare quelli esistenti.
1. Segui le istruzioni contenute in [Gestire utenti e gruppi in Experience Cloud](https://helpx.adobe.com/enterprise/help/users.html) nella *guida utente della versione Enterprise*.

## Creare gruppi di utenti {#user-groups}

È possibile creare gruppi di utenti, ad esempio sviluppatori, analisti, addetti al marketing, dirigenti e così via, e assegnare privilegi a più prodotti Adobe e aree di lavoro. Per assegnare a un nuovo membro del team tutti i privilegi appropriati per i diversi prodotti Adobe, sarà sufficiente aggiungerlo a un gruppo di utenti specifico.

1. [Nell’Admin Console](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE), fai clic su **[!UICONTROL Utenti]** > **[!UICONTROL Gruppi di utenti]** per creare nuovi gruppi di utenti o per modificare quelli esistenti.
1. Segui le istruzioni contenute in [Gestire utenti e gruppi in Experience Cloud](https://helpx.adobe.com/enterprise/help/users.html) nella *guida utente della versione Enterprise*.

## Specificare ruoli e autorizzazioni {#roles-permissions}

Solo gli amministratori di sistema possono impostare i ruoli utente in [!DNL Target]. Ad esempio, un utente approvatore Standard non può cambiare un utente Osservatore in approvatore, senza che sia necessario [!DNL Experience Cloud] Diritti di amministrazione.

Devono essere gli utenti amministratori di sistema ad aggiungere gli utenti al sistema. Gli utenti non vengono aggiunti automaticamente. Sono invitati via e-mail dal [!DNL Experience Cloud] e devono confermare i propri indirizzi e-mail prima che i loro account siano registrati.

1. [In Admin Console](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE), fai clic su **[!UICONTROL Prodotti]**, quindi seleziona il nome del prodotto desiderato.

   ![Scheda Prodotti](/help/main/administrating-target/c-user-management/c-user-management/assets/workspace-publisher.png)

1. Fai clic sull’area di lavoro desiderata (ad esempio, Area di lavoro predefinita).

   ![Area di lavoro predefinita](/help/main/administrating-target/c-user-management/c-user-management/assets/default-workspace-new.png)

   Nella scheda [!UICONTROL Utenti] vengono visualizzati tutti gli utenti di quell’area di lavoro.

   ![configurazione degli utenti](/help/main/administrating-target/c-user-management/c-user-management/assets/configuration_users-new-publisher.png)

1. Seleziona il ruolo di autorizzazioni desiderato (Approvatore, Editor o Osservatore) dall’elenco a discesa per ogni utente nella colonna [!UICONTROL Ruolo prodotto].

   ![Elenco a discesa Ruolo prodotto](/help/main/administrating-target/c-user-management/c-user-management/assets/product-role-new.png)

   | Ruolo | Descrizione |
   |--- |--- |
   | Approvatore | Può creare, modificare, attivare o interrompere le attività. |
   | Editor | può creare e modificare le attività prima che siano in diretta, ma non può approvare l&#39;avvio di un&#39;attività. |
   | Osservatore | Può visualizzare le attività, ma non può crearle o modificarle. |
   | Editore | Simile al ruolo Osservatore (può visualizzare le attività, ma non può crearle o modificarle). Tuttavia, il ruolo Editore è anche autorizzato ad attivare le attività. |

Per ulteriori informazioni, vedi [Gestione delle autorizzazioni del prodotto in Admin Console](https://helpx.adobe.com/enterprise/help/manage-permissions-and-roles.html) nella *guida utente della versione Enterprise*.

## Video di formazione: Come configurare le aree di lavoro di Adobe Target ![Badge tutorial](/help/main/assets/tutorial.png)

Finalità di apprendimento:

* Accedere ad Admin Console dall’interfaccia di Adobe Target (tre modi)
* Configurare un’area di lavoro in Adobe Admin Console
   * Aggiungere utenti alle aree di lavoro
   * Aggiungere proprietà alle aree di lavoro
* Comprendere le aree di lavoro predefinite

>[!NOTE]
>
>La [!DNL Target] [!UICONTROL Amministrazione] interfaccia utente del menu (precedentemente [!UICONTROL Configurazione]) è stato riprogettato per fornire prestazioni migliori, ridurre il tempo di manutenzione necessario per il rilascio di nuove funzioni e migliorare l’esperienza utente nel prodotto. Le informazioni contenute nel video seguente sono generalmente corrette; tuttavia, le opzioni potrebbero trovarsi in posizioni leggermente diverse. I video aggiornati verranno pubblicati a breve.

>[!VIDEO](https://video.tv.adobe.com/v/19463/)
