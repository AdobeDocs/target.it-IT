---
description: Note sulla versione che forniscono informazioni su funzioni, miglioramenti e correzioni per le versioni più recenti o imminenti di [!DNL Adobe Target].
keywords: note sulla versione
seo-description: Note sulla versione che forniscono informazioni su funzioni, miglioramenti e correzioni per le versioni più recenti o imminenti di [!DNL Adobe Target].
seo-title: Note sulla versione di Adobe Target (prerelease)
solution: Target
title: Note sulla versione di Target (prerelease)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: d675c6875c8474ba490956ea395076eef5b9e58f

---


# Note sulla versione di Target (prerelease){#target-release-notes-prerelease}

Queste note sulla versione contengono informazioni su funzioni, miglioramenti e correzioni per le versioni più recenti o in arrivo di [!DNL Adobe Target].

**Ultimo aggiornamento: 24 settembre 2019**

>[!NOTE]
>
>Queste note sulla versione contengono delle informazioni sulla versione prerelease. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso. Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali o possono essere diverse, a seconda della tempistica delle release.
>
>I codici tra parentesi sono per uso interno di [!DNL Adobe].

## Annunci

**31 luglio 2019**

[!UICONTROL Enterprise Permissions allows  customers to use a single organization, but divide it into workspaces for different teams or workflows. ][!DNL Target] The Enterprise Permissions feature facilitates effective scaling of optimization programs across teams.  Although this feature was available in the  UI, the Admin APIs lacked the corresponding support until the  February 2019 release. [!DNL Target][!DNL Target] Adobe updated the Admin APIs so that you can use the integration account to access all workspaces created in your organization. Pertanto, mentre in precedenza le API Amministratore erano limitate all'area di lavoro predefinita, l'aggiornamento di febbraio 2019 consentiva l'accesso a tutte le aree di lavoro con accesso [!UICONTROL Approver] .

Con la prossima release di [!DNL Target] settembre 2019, [!UICONTROL Enterprise Permissions] fornirà ai clienti i seguenti controlli di accesso:

* Potete scegliere le aree di lavoro a cui applicare l'integrazione
* Puoi assegnare un ruolo all'integrazione I/O di Adobe: [!UICONTROL Approver], [!UICONTROL Editor]o [!UICONTROL Osservatore].

**Azione richiesta**: I clienti che attualmente utilizzano le API per le operazioni CRUD su risorse (attività, audience, offerte e reporting) in tutte le aree di lavoro devono concedere all'integrazione I/O Adobe esistente l'accesso a tutte le aree di lavoro con il ruolo desiderato. Prior to the September release, all integrations operated using Approver access, regardless of the role selected from the Product Role drop-down list.  With the upcoming release, you can now select the desired role.

This action should be performed during the month of **August 2019**. After the  September 2019 release, the access controls will activate and you will observe access to just the default workspace if that's how you are currently set up. [!DNL Target] There is no adverse consequence to setting up integration roles in advance.

For step-by-step instructions and more information, see Grant Adobe I/O integrations access to workspaces and assign roles.[](/help/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md)

## Target Standard/Premium 19.9.2 (30 settembre 2019)

Questa versione di manutenzione include i seguenti miglioramenti:

* Several security fixes, including a security update to the Rich Text Editor (RTE) in the Visual Experience Composer (VEC). (TGT-35383)

## Target Standard/Premium 19.9.1 (10 settembre 2019)

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| ![Premium badge](/help/assets/premium.png) Enterprise Permissions | With the Target September 2019 release, Enterprise Permissions provides customers with the following access controls:<UL><li>Potete scegliere le aree di lavoro a cui applicare l'integrazione.</li><li>You can apply a role to the Adobe I/O integration: Approver, Editor, or Observer.</li></ul>Per istruzioni dettagliate e ulteriori informazioni, consultate [Concedere alle integrazioni di I/O Adobe l'accesso alle aree di lavoro e assegnare ruoli](/help/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md). |

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
