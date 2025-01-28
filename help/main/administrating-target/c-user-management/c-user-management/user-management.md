---
keywords: aggiungere utente;gestire utente;autorizzazioni utente
description: Scopri come utilizzare  [!DNL Adobe Admin Console]  per gestire gli utenti e le autorizzazioni e i diritti di questi in  [!DNL Adobe Target Standard].
title: Come si aggiungono utenti e si gestiscono le autorizzazioni per un account  [!DNL Target Standard] ?
feature: Administration & Configuration
role: Admin
exl-id: 535c28c7-179d-4edc-b140-880b9dfe1d59
source-git-commit: 484971ab0fcd07205935c0fef3ea1484f40c3e96
workflow-type: tm+mt
source-wordcount: '847'
ht-degree: 63%

---

# Utenti

Aggiungere utenti e gestirne le autorizzazioni in [!DNL Adobe Admin Console] per un account [!DNL Target Standard].

>[!NOTE]
>
>Le funzionalità [!UICONTROL Properties] e [!UICONTROL Permissions] sono disponibili come parte della soluzione [!DNL Target Premium]. Non sono disponibili in [!DNL Target] Standard senza una licenza [!DNL Target] Premium.
>
>Per verificare se la tua organizzazione dispone di una licenza di [!UICONTROL Standard] o [!UICONTROL Premium], fai clic sul collegamento [!UICONTROL Administration] nella parte superiore dell&#39;interfaccia utente di [!DNL Target].
>
>* **[!DNL Target][!UICONTROL Standard] Clienti**: se è presente la scheda [!UICONTROL Users] ([!UICONTROL Administration > Users]) (e non la scheda **[!UICONTROL Properties]**), la tua organizzazione dispone di una licenza [!DNL Target] [!UICONTROL Standard]. I clienti [!DNL Target] [!UICONTROL Standard] devono seguire le istruzioni riportate in questo articolo per aggiungere utenti e assegnare autorizzazioni in [!DNL Adobe Admin Console].
>
>* Clienti Premium **[!DNL Target]**: se sono presenti le schede [!UICONTROL Users] e [!UICONTROL Properties] ([!UICONTROL Administration > Properties]), la tua organizzazione dispone di una licenza Premium [!DNL Target]. I clienti [!DNL Target] Premium devono seguire le istruzioni contenute in [Enterprise User Permissions](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) (Autorizzazioni utente di Enterprise) e [Configure enterprise permissions](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md) (Configurazione delle autorizzazioni Enterprise) per aggiungere utenti e assegnare le autorizzazioni in [!DNL Adobe Admin Console].
>
>Per informazioni dettagliate su come gestire utenti e autorizzazioni, consulta [Gestione di prodotti e profili di prodotto](https://helpx.adobe.com/it/enterprise/using/manage-products-and-profiles.html) nella *guida utente di Enterprise &amp; Teams*.

Quando inizi a usare [!DNL Adobe Target], troverai gli ID (che terminano con Adobe.com) pre-popolati nel tuo account [!DNL Adobe Experience Cloud]. Questi ID sono per i membri dei team [!DNL Adobe], in modo che possano aiutarti con il tuo nuovo account e con l’uso di [!DNL Adobe Target], se hai bisogno di assistenza. Per ottenere assistenza, contatta i team Adobe di riferimento con le modalità usuali.

I nuovi utenti verranno visualizzati nella pagina [!UICONTROL Users] solo dopo che avranno effettuato l&#39;accesso con il proprio account [!DNL Adobe Experience Cloud] e quindi a [!DNL Target].

Per impostazione predefinita, tutti gli utenti [!DNL Target] iniziano con [!UICONTROL Observer] autorizzazioni.

Gli utenti amministratori sono identificati nell&#39;elenco [!UICONTROL Users]. Se hai bisogno di un diverso livello di accesso, contatta uno degli utenti amministratori di sistema.

## Visualizzazione delle informazioni utente all’interno di [!DNL Target]

Puoi visualizzare un elenco degli utenti correnti nell’interfaccia [!DNL Target], inclusi i ruoli per area di lavoro e gli indirizzi e-mail.

Per visualizzare la pagina [!UICONTROL Users], fare clic su **[!UICONTROL Administration]** > **[!UICONTROL Users]**.

>[!NOTE]
>
>Per gestire un utente esistente o aggiungere nuovi utenti, è necessario utilizzare [!UICONTROL Adobe Admin Console], come spiegato di seguito.

## Accedere a [!DNL Adobe Admin Console] {#access}

Per le attività da eseguire in [!DNL Adobe Admin Console] , accedi alla console seguendo questi passaggi:

1. Da [!DNL Target], fare clic su **[!UICONTROL Administration]** > **[!UICONTROL Users]** > **[!UICONTROL Users Management]**.

   Oppure

   Vai su [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/) e, se non hai già effettuato l’accesso, accedi con il tuo Adobe ID.

1. (Facoltativo) Se disponi dell’accesso ad [!DNL Admin Console for Enterprise] per più di un’organizzazione, fai clic sull’avatar utente nell’angolo a destra o sulla barra di navigazione superiore, quindi seleziona l’organizzazione desiderata.

## Aggiunta di utenti {#add-users}

Tutte le operazioni di gestione dell’utente devono essere eseguite in [!DNL Adobe Admin Console for Enterprise]. Tuttavia, tutti gli utenti esistenti in [!DNL Target] verranno migrati da [!DNL Target] ad [!DNL Admin Console for Enterprise].

1. [Nell&#39;Admin Console](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE), fare clic su **[!UICONTROL Users]** > **[!UICONTROL Users]** per creare nuovi utenti o modificare quelli esistenti.
1. Segui le istruzioni contenute in [Gestire utenti e gruppi in Experience Cloud](https://helpx.adobe.com/it/enterprise/using/users.html) nella *guida utente della versione Enterprise*.

## Creazione di gruppi di utenti {#user-groups}

È possibile creare gruppi di utenti, ad esempio sviluppatori, analisti, addetti al marketing, dirigenti e così via, e assegnare privilegi a più prodotti e aree di lavoro di [!DNL Adobe]. Per assegnare a un nuovo membro del team tutti i privilegi appropriati per i diversi prodotti [!DNL Adobe], sarà sufficiente aggiungerlo a un gruppo di utenti specifico.

1. [Nell&#39;Admin Console](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE), fare clic su **[!UICONTROL Users]** > **[!UICONTROL User Groups]** per creare nuovi gruppi di utenti o per modificare quelli esistenti.
1. Segui le istruzioni contenute in [Gestire utenti e gruppi in Experience Cloud](https://helpx.adobe.com/it/enterprise/using/users.html) nella *guida utente della versione Enterprise*.

## Specificare ruoli e autorizzazioni {#roles-permissions}

Solo gli amministratori di sistema possono impostare i ruoli utente in [!DNL Target]. Ad esempio, un utente approvatore [!UICONTROL Standard] non può trasformare un osservatore in un approvatore, senza disporre anche dei diritti di amministratore [!DNL Experience Cloud].

Devono essere gli utenti amministratori di sistema ad aggiungere gli utenti al sistema. Gli utenti non vengono aggiunti automaticamente. Vengono invitati via e-mail da [!DNL Experience Cloud] e dovranno confermare i propri indirizzi prima che i relativi account vengano registrati.

>[!NOTE]
>
>Per visualizzare le attività in [!DNL Target], gli utenti devono essere assegnati direttamente a un&#39;area di lavoro con almeno il ruolo [!UICONTROL Observer]. L’assegnazione tramite i soli gruppi di utenti non è sufficiente. In genere, si consiglia di concedere agli utenti l’accesso all’area di lavoro predefinita.

1. [Nell&#39;Admin Console](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE), fare clic su **[!UICONTROL Products]**, quindi selezionare il nome del prodotto desiderato.

1. Fai clic sull’area di lavoro desiderata, ad esempio Default Workspace (Area di lavoro predefinita).

   Nella scheda [!UICONTROL Users] vengono visualizzati tutti gli utenti di quell&#39;area di lavoro.

1. Selezionare il ruolo di autorizzazioni desiderato ([!UICONTROL Approver], [!UICONTROL Editor], [!UICONTROL Observer] o [!UICONTROL Publisher]) utilizzando l&#39;elenco a discesa per ogni utente nella colonna [!UICONTROL Product Role].

   | Ruolo | Descrizione |
   |--- |--- |
   | [!UICONTROL Approver] | Può creare, modificare, attivare o interrompere le attività. |
   | [!UICONTROL Editor] | Può creare e modificare le attività prima che siano in diretta, ma non può approvare l’avvio di un’attività. |
   | [!UICONTROL Observer] | Può visualizzare le attività, ma non può crearle o modificarle. |
   | [!UICONTROL Publisher] | Simile al ruolo [!UICONTROL Observer] (può visualizzare le attività, ma non può crearle o modificarle). Tuttavia, il ruolo [!UICONTROL Publisher] dispone dell&#39;autorizzazione aggiuntiva per attivare le attività. |

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
>L&#39;interfaccia utente del menu [!DNL Target] [!UICONTROL Administration] (in precedenza [!UICONTROL Setup]) è stata riprogettata per fornire prestazioni migliori, ridurre il tempo di manutenzione necessario per il rilascio di nuove funzionalità e migliorare l&#39;esperienza utente nel prodotto. Le informazioni contenute nel video seguente sono generalmente corrette; tuttavia, le opzioni potrebbero trovarsi in punti leggermente diversi. I video aggiornati verranno pubblicati a breve.

>[!VIDEO](https://video.tv.adobe.com/v/19463/)
