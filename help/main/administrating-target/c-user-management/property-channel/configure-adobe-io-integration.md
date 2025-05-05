---
keywords: integrazione;ruoli;autorizzazioni utente;admin console
description: Scopri come consentire alle integrazioni Adobe I/O esistenti di accedere a tutte le aree di lavoro con il ruolo desiderato in Adobe Target.
title: Come posso concedere l’accesso Adobe I/O alle aree di lavoro e assegnare ruoli?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."
feature: Administration & Configuration
role: Admin
exl-id: 62f6399f-c590-470c-ac3b-e0c84db63112
source-git-commit: fa11f93058b69e5e59e0ee20c65cffa4a1344ca0
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 59%

---

# Consentire alle integrazioni Adobe I/O di accedere alle aree di lavoro e assegnare ruoli

[!UICONTROL Enterprise Permissions] consente a [!DNL Target] clienti di utilizzare una singola organizzazione, ma di suddividerla in più aree di lavoro per i diversi team o flussi di lavoro.

>[!NOTE]
>
>La funzionalità Proprietà e Autorizzazioni è disponibile come parte della soluzione [Target Premium](/help/main/c-intro/intro.md#premium). Non sono disponibili in [!DNL Target Standard] senza una licenza [!DNL Target Premium].

La funzionalità [!UICONTROL Enterprise Permissions] facilita l&#39;effettiva scalabilità dei programmi di ottimizzazione tra i team. Questa funzionalità era già disponibile nell’interfaccia utente di [!DNL Target], ma è supportata dalle API amministratore solo dall’inizio del 2019. Nella versione di febbraio 2019 di [!DNL Target], Adobe ha aggiornato le API amministratore per consentire l’utilizzo dell’account di integrazione per accedere a tutte le aree di lavoro create nell’organizzazione. Precedentemente, le API amministratore erano limitate alla sola area di lavoro predefinita. Con l&#39;aggiornamento di febbraio 2019 è possibile accedere a tutte le aree di lavoro con accesso [!UICONTROL Approver].

Con la versione di [!DNL Target] settembre 2019, [!DNL Target] [!UICONTROL Enterprise Permissions] fornisce ai clienti i seguenti controlli di accesso:

* Possibilità di scegliere le aree di lavoro a cui applicare l’integrazione
* È possibile applicare un ruolo all&#39;integrazione Adobe I/O: [!UICONTROL Approver], [!UICONTROL Editor] o [!UICONTROL Observer].

Questo aggiornamento supporta i casi d’uso seguenti:

* Concedi all&#39;integrazione Adobe I/O l&#39;accesso a tutte le aree di lavoro con il ruolo [!UICONTROL Observer] a scopo di reporting, senza poter creare o modificare le risorse.
* Concedi all’integrazione Adobe I/O l’accesso a specifiche aree di lavoro con il ruolo appropriato per consentire a un team centrale di apportare modifiche basate su API solo a poche aree di lavoro.
* Consenti a ogni team proprietario della sua area di lavoro di disporre della propria integrazione non appena il team è pronto per esplorare le API e scegliere il ruolo di conseguenza.
* Puoi combinare insieme questi scenari in base alle esigenze.

**Azione richiesta**: i clienti che sfruttano già le API per operazioni CRUD su risorse (attività, tipi di pubblico, offerte e rapporti) in tutte le aree di lavoro devono concedere all’integrazione Adobe I/O esistente l’accesso a tutte le aree di lavoro con il ruolo desiderato in base allo specifico caso d’uso. A tale scopo, selezionare ogni [!DNL Target] [!UICONTROL Product Profile] in [!DNL Adobe Admin Console] e aggiungere le integrazioni nella scheda [!UICONTROL Integration]. Prima della versione di settembre, tutte le integrazioni funzionavano con l&#39;accesso [!UICONTROL Approver], indipendentemente dall&#39;opzione effettuata nell&#39;elenco a discesa [!UICONTROL Product Role]. Ora puoi scegliere il ruolo desiderato.

>[!NOTE]
>
>Se non viene eseguita, dopo il rilascio della versione di settembre 2019 di [!DNL Target] verranno attivati i controlli di accesso e potresti essere in grado di accedere solo all’area di lavoro predefinita, qualora questa sia l’impostazione corrente. L’impostazione preventiva delle integrazioni non comporta alcun impatto negativo. Conviene quindi eseguirla quanto prima possibile. A seconda del numero di aree di lavoro dell’organizzazione, questo processo richiede solo pochi clic per aggiungere un’integrazione esistente alle aree di lavoro con il ruolo desiderato.

**Per consentire alle integrazioni Adobe I/O di accedere alle aree di lavoro e assegnare ruoli:**

1. Apri **[Adobe Admin Console](https://adminconsole.adobe.com)**.

1. Fare clic sulla scheda **[!UICONTROL Products]**, quindi selezionare il nome del prodotto desiderato.

   ![Scegliere il prodotto in Adobe Admin Console](/help/main/administrating-target/c-user-management/property-channel/assets/io-choose-product.png)

1. Seleziona l’area di lavoro desiderata (Profilo prodotto).

   ![Selezionare il profilo prodotto](/help/main/administrating-target/c-user-management/property-channel/assets/io-select-product-profile.png)

1. Fare clic sulla scheda **[!UICONTROL Integrations]**.

   ![Scheda Integrazioni](/help/main/administrating-target/c-user-management/property-channel/assets/integrations-tab.png)

1. (Condizionale) Per aggiungere una nuova integrazione, fare clic su **[!UICONTROL Add Integration]**, selezionare l&#39;integrazione desiderata, quindi fare clic su **[!UICONTROL Save]**.

1. Dall&#39;elenco a discesa **[!UICONTROL Product Role]**, selezionare il ruolo desiderato per l&#39;area di lavoro:

   | Ruolo | Descrizione |
   |--- |--- |
   | Responsabile approvazione | Può creare, modificare, attivare o interrompere le attività. |
   | Editor | Può creare e modificare le attività prima che siano in diretta, ma non può approvare l’avvio di un’attività. |
   | Osservatore | Può visualizzare le attività, ma non può crearle o modificarle. |
   | Editore | Simile al ruolo Osservatore (può visualizzare le attività, ma non può crearle o modificarle). Tuttavia, il ruolo Editore è anche autorizzato ad attivare le attività. |
