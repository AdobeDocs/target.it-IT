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
source-git-commit: 48cb808283c9b2858e1bd041feb3fe8228253d6a

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

Enterprise Permissions allows [!DNL Target] customers to use a single organization, but divide it into workspaces for their different teams or workflows. Questo facilita il ridimensionamento efficace del programma di ottimizzazione tra i team. Although the feature was available in the [!DNL Target] UI, the Admin APIs lacked the corresponding support until earlier this year. In the [!DNL Target] February 2019 release, Adobe updated the Admin APIs so that you can use the integration account to access all workspaces created in your organization. So, while earlier, Admin APIs were restricted to just the default workspace, the February update granted access to all workspaces with [!UICONTROL Approver] access.

With the upcoming [!DNL Target] September 2019 release, Target Enterprise Permissions will provide customers with the following access controls:

* Potete scegliere le aree di lavoro a cui applicare l'integrazione.
* You can apply a role to the Adobe I/O integration: [!UICONTROL Approver], [!UICONTROL Editor], or [!UICONTROL Observer].

Questo aggiornamento supporterà i casi d'uso seguenti:

* Grant the Adobe I/O integration access to all workspaces with the [!UICONTROL Observer] role for reporting purposes with no rights to create or edit resources.
* Concedete l'integrazione di I/O con il ruolo appropriato per consentire a un team centrale di apportare modifiche basate su API solo in pochi aree di lavoro.
* Ogni team proprietario della sua area di lavoro decide di disporre della propria integrazione ogni volta che il team è pronto per esplorare le API e sceglie il ruolo di conseguenza.
* Combinate e rispettate qualsiasi scenario precedente.

**Azione richiesta**: I clienti che stanno sfruttando API per operazioni CRUD su risorse (attività, tipi di pubblico, offerte e rapporti) in tutte le aree di lavoro devono concedere l'accesso esistente di integrazione I/O di Adobe a tutte le aree di lavoro con il ruolo desiderato in base al loro caso d'uso. You can do so by selecting each [!DNL Target] [!UICONTROL Product Profile] in the [!DNL Adobe Admin Console] and adding the integration(s) in the [!UICONTROL Integration] tab. Prior to the September release, all integrations operated using [!UICONTROL Approver] access, irrespective of choice made in the [!UICONTROL Product Role] drop-down list. Ora potete scegliere il ruolo desiderato.

This action *must* be performed before September 4, 2019 to not face any disruption on your end. Se non viene eseguita, dopo il [! Versione di settembre di DNL Target, i controlli di accesso vengono attivati e potrai osservare l'accesso solo all'area di lavoro predefinita, se hai già impostato questa impostazione. Non esiste una reazione negativa per impostare in anticipo le integrazioni in base alle linee guida precedenti. Prima di effettuare questa modifica, meglio sarà. A seconda del numero di aree di lavoro nell'organizzazione, è necessario un tempo limitato. Questo processo richiede solo pochi clic per aggiungere un'integrazione esistente alle aree di lavoro con il ruolo desiderato.

## Target Standard/Premium 19.8.1 (20 agosto 2019) {#tgt-19-8-1}

Questa versione di manutenzione include i seguenti miglioramenti:

* Diverse correzioni di protezione, compreso un aggiornamento di sicurezza all'editor Rich Text (RTE) in Visual Experience Composer (Compositore esperienza visivo). (TGT-35383)

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
