---
description: Note sulla versione che forniscono informazioni su funzioni, miglioramenti e correzioni per i prossimi o imminenti [! DNL Adobe Target].
keywords: note sulla versione
seo-description: Note sulla versione che forniscono informazioni su funzioni, miglioramenti e correzioni per i prossimi o imminenti [! DNL Adobe Target].
seo-title: Note di rilascio di Adobe Target (prerelease)
solution: Target
title: Note sulla versione di Target (prerelease)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: a6aae8602b8f3c3f879bd6e3e37591f330197cf8

---


# Note sulla versione di Target (prerelease){#target-release-notes-prerelease}

Queste note sulla versione contengono informazioni su funzioni, miglioramenti e correzioni per le versioni più recenti o in arrivo di [!DNL Adobe Target].

**Ultimo aggiornamento: 31 luglio 2019**

>[!NOTE]
>
>Queste note sulla versione contengono delle informazioni in anteprima. Le date di rilascio, le funzioni e altre informazioni sono soggette a modifiche senza preavviso. Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali o possono essere diverse, a seconda della tempistica delle release.
>
>The issue numbers in parentheses are for internal [!DNL Adobe] use.

## Annunci

**31 luglio 2019**

[!UICONTROL Le autorizzazioni Enterprise] consentono [!DNL Target] ai clienti di utilizzare un'unica organizzazione, ma dividerla in aree di lavoro per diversi team o flussi di lavoro. The [!UICONTROL Enterprise Permissions] feature facilitates effective scaling of optimization programs across teams. Although this feature was available in the [!DNL Target] UI, the Admin APIs lacked the corresponding support until the [!DNL Target] February 2019 release. Adobe ha aggiornato le API Amministratore per poter utilizzare l'account di integrazione per accedere a tutte le aree di lavoro create nell'organizzazione. So, while earlier, Admin APIs were restricted to the default workspace, the February 2019 update granted access to all workspaces with [!UICONTROL Approver] access.

With the upcoming [!DNL Target] September 2019 release, [!UICONTROL Enterprise Permissions] will provide customers with the following access controls:

* Potete scegliere le aree di lavoro a cui applicare l'integrazione.
* You can apply a role to the Adobe I/O integration: [!UICONTROL Approver], [!UICONTROL Editor], or [!UICONTROL Observer].

**Azione richiesta**: I clienti che stanno sfruttando API per operazioni CRUD su risorse (attività, tipi di pubblico, offerte e rapporti) in tutte le aree di lavoro devono concedere l'accesso esistente di integrazione I/O di Adobe a tutte le aree di lavoro con il ruolo desiderato. Prior to the September release, all integrations operated using [!UICONTROL Approver] access, regardless of the role selected from the [!UICONTROL Product Role] drop-down list. Con la prossima release, è possibile selezionare il ruolo desiderato.

This action should be performed before **September 4, 2019**. After the [!DNL Target] September 2019 release, the access controls will activate and you will observe access to just the default workspace if that's how you are currently set up. Non vi sono conseguenze negative per configurare i ruoli di integrazione in anticipo.

For step-by-step instructions and more information, see [Grant Adobe I/O integrations access to workspaces and assign roles](/help/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md).

## Target Standard/Premium 19.8.1 (20 agosto 2019) {#tgt-19-8-1}

Questa versione di manutenzione include i seguenti miglioramenti:

* Diverse correzioni di protezione, compreso un aggiornamento di sicurezza all'editor Rich Text (RTE) in Visual Experience Composer (Compositore esperienza visivo). (TGT-35383)

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
