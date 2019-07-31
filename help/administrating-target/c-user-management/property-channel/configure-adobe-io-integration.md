---
description: Informazioni sulla concessione dell'accesso ai/O Adobe a tutte le aree di lavoro con il ruolo desiderato.
keywords: integrazione; ruoli; autorizzazioni utente; admin console
seo-description: Informazioni sulla concessione di integrazioni I/O esistenti a tutte le aree di lavoro con il ruolo desiderato in Adobe Target
seo-title: Consentire l'accesso alle integrazioni I/O di Adobe alle aree di lavoro e assegnare ruoli in Adobe Target
solution: Target
subtopic: Introduzione
title: Consenti agli integrazioni I/O di accedere alle aree di lavoro e assegna ruoli
translation-type: tm+mt
source-git-commit: a6aae8602b8f3c3f879bd6e3e37591f330197cf8

---


# ![PREMIUM](/help/assets/premium.png) Concedi accesso alle integrazioni I/O di Adobe alle aree di lavoro e assegna ruoli

[!UICONTROL Le autorizzazioni Enterprise] consentono [!DNL Target] ai clienti di utilizzare un'unica organizzazione, ma dividerla in aree di lavoro per i loro diversi team o flussi di lavoro.

>[!NOTE]
>
>La funzionalità Proprietà e Autorizzazioni è disponibile come parte della soluzione [Target Premium](/help/c-intro/intro.md#premium). Non sono disponibili in [!DNL Target Standard] senza una licenza [!DNL Target Premium].

The [!UICONTROL Enterprise Permissions] feature facilitates effective scaling of optimization programs across teams. Although the feature was available in the [!DNL Target] UI, the Admin APIs lacked the corresponding support until earlier in 2019. In the [!DNL Target] February 2019 release, Adobe updated the Admin APIs so that you can use the integration account to access all workspaces created in your organization. So, while earlier, Admin APIs were restricted to just the default workspace, the February 2019 update granted access to all workspaces with [!UICONTROL Approver] access.

With the upcoming [!DNL Target] September 2019 release, [!DNL Target] [!UICONTROL Enterprise Permissions] will provide customers with the following access controls:

* Potete scegliere le aree di lavoro a cui applicare l'integrazione.
* You can apply a role to the Adobe I/O integration: [!UICONTROL Approver], [!UICONTROL Editor], or [!UICONTROL Observer].

Questo aggiornamento supporta i casi d'uso seguenti:

* Grant the Adobe I/O integration access to all workspaces with the [!UICONTROL Observer] role for reporting purposes with no rights to create or edit resources.
* Concedete l'integrazione di I/O con il ruolo appropriato per consentire a un team centrale di apportare modifiche basate su API solo in pochi aree di lavoro.
* Consentite a ogni team proprietario della sua area di lavoro di avere la propria integrazione ogni volta che il team è pronto per esplorare le API e scegliete il ruolo di conseguenza.
* Combinate e rispettate qualsiasi scenario precedente.

**Azione richiesta**: I clienti che stanno sfruttando API per operazioni CRUD su risorse (attività, tipi di pubblico, offerte e rapporti) in tutte le aree di lavoro devono concedere l'accesso esistente di integrazione I/O di Adobe a tutte le aree di lavoro con il ruolo desiderato in base al loro caso d'uso. You can do so by selecting each [!DNL Target] [!UICONTROL Product Profile] in the [!DNL Adobe Admin Console] and adding the integration(s) in the [!UICONTROL Integration] tab. Prior to the September release, all integrations operated using [!UICONTROL Approver] access, regardless of choice made from the [!UICONTROL Product Role] drop-down list. Ora potete scegliere il ruolo desiderato.

This action should be performed before **September 4, 2019** to not face any disruption on your end. If this action is not performed, after the [!DNL Target] September 2019 release, the access controls will activate and you will observe access to just the default workspace if that's how you are currently set up. Non esiste una reazione negativa per impostare in anticipo le integrazioni in base alle linee guida precedenti. Prima di effettuare questa modifica, meglio sarà. A seconda del numero di aree di lavoro nell'organizzazione, è necessario un tempo limitato. Questo processo richiede solo pochi clic per aggiungere un'integrazione esistente alle aree di lavoro con il ruolo desiderato.

**Per concedere l'accesso delle integrazioni I/O alle aree di lavoro e assegnare ruoli:**

1. Open the **[!DNL[Adobe Admin Console](https://adminconsole.adobe.com)]**.

1. Click the **[!UICONTROL Products]** tab, then select the name of the desired product.

   ![Scegli il prodotto in Adobe Admin Console](/help/administrating-target/c-user-management/property-channel/assets/io-choose-product.png)

1. Seleziona l'area di lavoro desiderata (Profilo di prodotto).

   ![Selezionare il profilo di prodotto](/help/administrating-target/c-user-management/property-channel/assets/io-select-product-profile.png)

1. Click the **[!UICONTROL Integrations]** tab.

   ![Scheda Integrazioni](/help/administrating-target/c-user-management/property-channel/assets/integrations-tab.png)

1. (Conditional) To add a new integration, click **[!UICONTROL Add Integration]**, select the desired integration, then click **[!UICONTROL Save]**.

1. From the **[!UICONTROL Product Role]** drop-down list, select the desired role for that workspace:

   * [!UICONTROL Approvatore]
   * [!UICONTROL Editor]
   * [!UICONTROL Osservatore]
   ![Scegliere il ruolo Profilo di prodotto](/help/administrating-target/c-user-management/property-channel/assets/product-profile-role.png)
