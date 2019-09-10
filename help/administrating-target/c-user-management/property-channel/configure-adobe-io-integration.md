---
description: Informazioni sulla concessione dell'accesso ai/O Adobe a tutte le aree di lavoro con il ruolo desiderato.
keywords: integrazione; ruoli; autorizzazioni utente; admin console
seo-description: Informazioni sulla concessione di integrazioni I/O esistenti a tutte le aree di lavoro con il ruolo desiderato in Adobe Target
seo-title: Consentire l'accesso alle integrazioni I/O di Adobe alle aree di lavoro e assegnare ruoli in Adobe Target
solution: Target
subtopic: Introduzione
title: Consenti agli integrazioni I/O di accedere alle aree di lavoro e assegna ruoli
translation-type: tm+mt
source-git-commit: 13ad42da73dd3fcbf4e07be1de646e0eac8c991e

---


# ![PREMIUM](/help/assets/premium.png) Concedi accesso alle integrazioni I/O di Adobe alle aree di lavoro e assegna ruoli

[!UICONTROL Le autorizzazioni Enterprise] consentono [!DNL Target] ai clienti di utilizzare un'unica organizzazione, ma dividerla in aree di lavoro per i loro diversi team o flussi di lavoro.

>[!NOTE]
>
>La funzionalità Proprietà e Autorizzazioni è disponibile come parte della soluzione [Target Premium](/help/c-intro/intro.md#premium). Non sono disponibili in [!DNL Target Standard] senza una licenza [!DNL Target Premium].

La [!UICONTROL funzione Autorizzazioni] Enterprise semplifica il ridimensionamento efficace dei programmi di ottimizzazione tra i team. Anche se la funzionalità era disponibile nell' [!DNL Target] interfaccia utente, le API amministratore non hanno superato il supporto corrispondente fino alla prima in 2019. Nella versione [!DNL Target] di febbraio 2019, Adobe ha aggiornato le API Amministratore per poter utilizzare il account di integrazione per accedere a tutte le aree di lavoro create nell'organizzazione. Così, mentre nelle versioni precedenti, le API amministratore erano limitate solo all'area di lavoro predefinita, l'aggiornamento di febbraio 2019 consentiva l'accesso a tutte le aree di lavoro con accesso [!UICONTROL Approver] .

Con la [!DNL Target] versione di settembre 2019, [!DNL Target][!UICONTROL l'Enterprise Permissions] offre ai clienti i seguenti controlli di accesso:

* Potete scegliere le aree di lavoro a cui applicare l'integrazione.
* Potete applicare un ruolo all'integrazione I/O di Adobe: [!UICONTROL Approver], [!UICONTROL Editor]o [!UICONTROL Observer].

Questo aggiornamento supporta i casi d'uso seguenti:

* Concedete l'accesso all'integrazione di Adobe I/O a tutte le aree di lavoro con il ruolo [!UICONTROL Observer] a scopo di reporting, senza diritti per creare o modificare le risorse.
* Concedete l'integrazione di I/O con il ruolo appropriato per consentire a un team centrale di apportare modifiche basate su API solo in pochi aree di lavoro.
* Consentite a ogni team proprietario della sua area di lavoro di avere la propria integrazione ogni volta che il team è pronto per esplorare le API e scegliete il ruolo di conseguenza.
* Combinate e rispettate qualsiasi scenario precedente.

**Azione richiesta**: I clienti che stanno sfruttando API per operazioni CRUD su risorse (attività, tipi di pubblico, offerte e rapporti) in tutte le aree di lavoro devono concedere l'accesso esistente di integrazione I/O di Adobe a tutte le aree di lavoro con il ruolo desiderato in base al loro caso d'uso. Puoi farlo selezionando ogni [!DNL Target][!UICONTROL profilo di prodotto] nell' [!DNL Adobe Admin Console] e aggiungendo le integrazioni nella scheda [!UICONTROL Integrazione] . Prima del rilascio di settembre, tutte le integrazioni gestite utilizzando l'accesso [!UICONTROL a Approver] (Responsabile approvazione), indipendentemente dalla scelta effettuata dall' [!UICONTROL elenco a discesa Product Role] (Ruolo prodotto). Ora potete scegliere il ruolo desiderato.

>[!NOTE]
>
>Se questa azione non viene eseguita, dopo la [!DNL Target] versione di settembre 2019 i controlli di accesso vengono attivati e potrai osservare l'accesso solo all'area di lavoro predefinita, se hai già impostato questa impostazione. Non esiste una reazione negativa alla configurazione di integrazioni in anticipo. Prima di effettuare questa modifica, meglio sarà. A seconda del numero di aree di lavoro nell'organizzazione, questo processo richiede solo alcuni clic per aggiungere un'integrazione esistente alle aree di lavoro con il ruolo desiderato.

**Per concedere l'accesso delle integrazioni I/O alle aree di lavoro e assegnare ruoli:**

1. Apri **[Adobe Admin Console](https://adminconsole.adobe.com)**.

1. Fate clic sulla scheda **[!UICONTROL Prodotti]** , quindi selezionate il nome del prodotto desiderato.

   ![Scegli il prodotto in Adobe Admin Console](/help/administrating-target/c-user-management/property-channel/assets/io-choose-product.png)

1. Seleziona l'area di lavoro desiderata (Profilo di prodotto).

   ![Selezionare il profilo di prodotto](/help/administrating-target/c-user-management/property-channel/assets/io-select-product-profile.png)

1. Click the **[!UICONTROL Integrations]** tab.

   ![Scheda Integrazioni](/help/administrating-target/c-user-management/property-channel/assets/integrations-tab.png)

1. (Condizionale) Per aggiungere una nuova integrazione, fate clic **[!UICONTROL su Aggiungi integrazione]**, selezionate l'integrazione desiderata, quindi fate clic **[!UICONTROL su Salva]**.

1. Dall' **[!UICONTROL elenco a discesa Ruolo]** prodotto, selezionate il ruolo desiderato per tale area di lavoro:

   * [!UICONTROL Approvatore]
   * [!UICONTROL Editor]
   * [!UICONTROL Osservatore]
   ![Scegliere il ruolo Profilo di prodotto](/help/administrating-target/c-user-management/property-channel/assets/product-profile-role.png)
