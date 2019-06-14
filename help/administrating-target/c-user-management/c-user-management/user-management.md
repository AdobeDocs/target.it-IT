---
description: Puoi aggiungere utenti e gestirne le autorizzazioni in Adobe Admin Console.
keywords: aggiungere utente;gestire utente;autorizzazioni utente
seo-description: Puoi aggiungere utenti e gestirne le autorizzazioni in Adobe Admin Console.
seo-title: Utenti
solution: Target
subtopic: Introduzione
title: Utenti
topic: Standard
uuid: 9b311dd3-b8fa-483d-aedd-96761cfcd67e
translation-type: tm+mt
source-git-commit: e7ec5af38c1ea55a9cb86f0c706a024bd0f96e6e

---


# Utenti{#users}

Puoi aggiungere utenti e gestirne le autorizzazioni in Adobe Admin Console.

>[!NOTE]
>
>Le funzionalità [!UICONTROL Proprietà] e [!UICONTROL Autorizzazioni] sono disponibili come parte della soluzione [!DNL Target] Premium. Non sono disponibili in [!DNL Target] Standard senza una licenza [!DNL Target] Premium.
>Per verificare se la tua organizzazione dispone di una licenza Standard o Premium, fai clic sul collegamento [!UICONTROL Configurazione] in alto nell’interfaccia utente di [!DNL Target].
>
>**Clienti[!DNL Target]Standard**: se è presente la scheda [!UICONTROL Utenti] ([!UICONTROL Configurazione &gt; Utenti]), significa che si dispone di una licenza [!DNL Target] Standard. I clienti [!DNL Target] Standard possono seguire le istruzioni riportate in questo argomento per aggiungere utenti e assegnare autorizzazioni in [!DNL Adobe Admin Console].
>
>**Clienti[!DNL Target]Premium**: se è presente la scheda [!UICONTROL Proprietà] ([!UICONTROL Configurazione &gt; Proprietà]), significa che si dispone di una licenza [!DNL Target] Premium. I clienti [!DNL Target] Premium devono seguire le istruzioni contenute in [Autorizzazioni per gli utenti Enterprise](/help/administrating-target/c-user-management/property-channel/property-channel.md) e [Configurare le autorizzazioni Enterprise](/help/administrating-target/c-user-management/property-channel/properties-overview.md) per aggiungere utenti e assegnare le autorizzazioni in [!DNL Adobe Admin Console].

Solo gli utenti amministratori di sistema possono aggiungere utenti e gestire le loro autorizzazioni. Il ruolo amministratore di sistema viene assegnato a livello di [!DNL Experience Cloud]. I ruoli [!DNL Experience Cloud] sono distinti dai ruoli gestiti in ogni soluzione.

Quando inizi a usare [!DNL Adobe Target], troverai gli ID (che terminano con Adobe.com) pre-popolati nel tuo account [!DNL Adobe Experience Cloud]. Questi ID sono per i membri dei team Adobe in modo che possano aiutarti con il tuo nuovo account e con l&#39;uso di [!DNL Adobe Target], se hai bisogno di aiuto. Per ottenere assistenza, contatta i team Adobe di riferimento con le modalità usuali.

Il nuovo utente viene visualizzato nella pagina [!UICONTROL Utenti] solo dopo che avrà effettuato l’accesso con il proprio account Adobe Experience Cloud e quindi a [!DNL Target Standard/Premium] facendo clic sulla scheda [!DNL Target].

Per impostazione predefinita, a tutti gli utenti di [!DNL Target] viene assegnato inizialmente il ruolo di Osservatore.

Gli utenti amministratori di sistema sono identificati nell&#39;elenco Utenti. Se hai bisogno di un diverlo livello di accesso, contatta uno degli utenti amministratori di sistema.

## Accedere ad Adobe Admin Console {#access}

Per le attività da eseguire in Adobe Admin Console, accedi alla console seguendo questi passaggi:

1. Vai su [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/) e, se non hai già effettuato l&#39;accesso, accedi con il tuo Adobe ID.

   Oppure

   Se hai già eseguito l&#39;accesso a Experience Cloud, vai a [https://www.experiencecloud.adobe.com](https://experiencecloud.adobe.com), quindi fai clic sull&#39;icona [!UICONTROL App] nella barra di navigazione superiore, quindi fai clic **[!UICONTROL su Admin (Amministratore]** ) sul lato destro.

1. (Condizionale) Se disponi dell&#39;accesso ad [!DNL Admin Console for Enterprise] per più di un’organizzazione, fai clic sull’avatar utente nell’angolo a destra o sulla barra di navigazione superiore, quindi seleziona l’organizzazione desiderata.

## Aggiungi utenti {#add-users}

Tutte le operazioni di gestione dell’utente devono essere eseguite in [!DNL Adobe Admin Console for Enterprise]. Tuttavia, tutti gli utenti esistenti in [!DNL Target] verranno migrati da [!DNL Target] ad [!DNL Admin Console for Enterprise].

1. [In Admin Console](../../../administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE), fai clic su **[!UICONTROL Utenti]** &gt; **[!UICONTROL Utenti]** per creare nuovi utenti o per modificare gli utenti esistenti.
1. Segui le istruzioni contenute in [Gestire utenti e gruppi in Experience Cloud](https://helpx.adobe.com/enterprise/help/users.html) nella *guida utente della versione Enterprise*.

## Creare gruppi di utenti {#user-groups}

È possibile creare gruppi di utenti, ad esempio sviluppatori, analisti, addetti al marketing, dirigenti e così via, e assegnare privilegi a più prodotti Adobe e aree di lavoro. Per assegnare a un nuovo membro del team tutti i privilegi appropriati per i diversi prodotti Adobe, sarà sufficiente aggiungerlo a un gruppo di utenti specifico.

1. [In Admin Console](../../../administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE), fai clic **[!UICONTROL su Utenti]** &gt; Gruppi **[!UICONTROL di utenti]** per creare nuovi gruppi di utenti o per modificare gruppi esistenti.
1. Segui le istruzioni contenute in [Gestire utenti e gruppi in Experience Cloud](https://helpx.adobe.com/enterprise/help/users.html) nella *guida utente della versione Enterprise*.

## Specificare ruoli e autorizzazioni {#roles-permissions}

Solo gli amministratori di sistema possono impostare i ruoli utente in [!DNL Target]. Ad esempio, un utente Approvatore di Standard non può attribuire a un utente Osservatore il ruolo di Approvatore, se non ha i diritti di amministratore di Experience Cloud.

Devono essere gli utenti amministratori di sistema ad aggiungere gli utenti al sistema. Gli utenti non vengono aggiunti automaticamente. Vengono invitati via e-mail da Experience Cloud e dovranno confermare i propri indirizzi prima che i relativi account vengano registrati.

1. [In Admin Console](../../../administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE), fai clic su **[!UICONTROL Prodotti]**, quindi seleziona il nome del prodotto desiderato.

   ![Scheda Prodotti](/help/administrating-target/c-user-management/c-user-management/assets/workspace-new.png)

1. Fai clic sul nome della configurazione desiderata.
1. Fai clic su **[!UICONTROL Utenti]**.

   Nella [!UICONTROL scheda Utenti] sono visualizzati tutti gli utenti di tale area di lavoro.

   ![utenti di configurazione](/help/administrating-target/c-user-management/c-user-management/assets/configuration_users-new.png)

1. Seleziona il ruolo di autorizzazioni desiderato (Osservatore, Editor o Approvatore) dall’elenco a discesa per ogni utente nella colonna [!UICONTROL Ruolo prodotto].

   | Ruolo | Descrizione |
   |--- |--- |
   | Osservatore | Può visualizzare le attività, ma non può crearle o modificarle. |
   | Editor | può creare e modificare le attività prima che siano in diretta, ma non può approvare l&#39;avvio di un&#39;attività. |
   | Approvatore | Può creare, modificare, attivare o interrompere le attività. |

Per ulteriori informazioni, vedi [Gestione delle autorizzazioni del prodotto in Admin Console](https://helpx.adobe.com/enterprise/help/manage-permissions-and-roles.html) nella *guida utente della versione Enterprise*.

## Video formazione: Come configurare le aree di lavoro di Target

Finalità di apprendimento:

* Accesso ad Adobe Admin Console dall&#39;interfaccia di Adobe Target (tre modi)
* Configurare un&#39;area di lavoro in Adobe Admin Console
   * Aggiungere utenti alle aree di lavoro
   * Aggiungere proprietà alle aree di lavoro
* Comprendere le aree di lavoro predefinite

>[!VIDEO](https://video.tv.adobe.com/v/19463/?captions=ita)
