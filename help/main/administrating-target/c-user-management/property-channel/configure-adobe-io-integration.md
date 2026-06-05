---
keywords: integrazione;ruoli;autorizzazioni utente;admin console
description: Scopri come consentire alle integrazioni Adobe I/O esistenti di accedere a tutte le aree di lavoro con il ruolo desiderato in Adobe Target.
title: Come posso concedere l’accesso Adobe I/O alle aree di lavoro e assegnare ruoli?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Administration & Configuration
role: Admin
exl-id: 62f6399f-c590-470c-ac3b-e0c84db63112
TQID: https://experienceleague.adobe.com/8WUCeb4ztjDdWUEtawLYeC-4FDgn1SiGarmS1hqGNgI
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
  - id: f7c7de77-382f-4f48-8b36-61a170f06d3d
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 647
ht-degree: 56%

---

# Consentire alle integrazioni Adobe I/O di accedere alle aree di lavoro e assegnare ruoli

[!UICONTROL Autorizzazioni Enterprise] consente a [!DNL Target] clienti di utilizzare una singola organizzazione, ma di suddividerla in più aree di lavoro per i diversi team o flussi di lavoro.

>[!NOTE]
>
>La funzionalità Proprietà e Autorizzazioni è disponibile come parte della soluzione [Target Premium](/help/main/c-intro/intro.md#premium). Non sono disponibili in [!DNL Target Standard] senza una licenza [!DNL Target Premium].

La funzione [!UICONTROL Autorizzazioni Enterprise] facilita l&#39;efficace scalabilità dei programmi di ottimizzazione tra i team. Questa funzionalità era già disponibile nell’interfaccia utente di [!DNL Target], ma è supportata dalle API amministratore solo dall’inizio del 2019. Nella versione di febbraio 2019 di [!DNL Target], Adobe ha aggiornato le API amministratore per consentire l’utilizzo dell’account di integrazione per accedere a tutte le aree di lavoro create nell’organizzazione. Precedentemente, le API amministratore erano limitate alla sola area di lavoro predefinita. Con l&#39;aggiornamento di febbraio 2019 è possibile accedere a tutte le aree di lavoro con accesso [!UICONTROL Approvatore].

Con la versione di [!DNL Target] settembre 2019, [!DNL Target] [!UICONTROL Autorizzazioni Enterprise] fornisce ai clienti i seguenti controlli di accesso:

* Possibilità di scegliere le aree di lavoro a cui applicare l’integrazione
* Puoi applicare un ruolo all&#39;integrazione Adobe I/O: [!UICONTROL Approvatore], [!UICONTROL Editor] o [!UICONTROL Osservatore].

Questo aggiornamento supporta i casi d’uso seguenti:

* Concedi all&#39;integrazione Adobe I/O l&#39;accesso a tutte le aree di lavoro con il ruolo [!UICONTROL Osservatore] a scopo di reporting, senza poter creare o modificare le risorse.
* Concedi all’integrazione Adobe I/O l’accesso a specifiche aree di lavoro con il ruolo appropriato per consentire a un team centrale di apportare modifiche basate su API solo a poche aree di lavoro.
* Consenti a ogni team proprietario della sua area di lavoro di disporre della propria integrazione non appena il team è pronto per esplorare le API e scegliere il ruolo di conseguenza.
* Puoi combinare insieme questi scenari in base alle esigenze.

**Azione richiesta**: i clienti che sfruttano già le API per operazioni CRUD su risorse (attività, tipi di pubblico, offerte e rapporti) in tutte le aree di lavoro devono concedere all’integrazione Adobe I/O esistente l’accesso a tutte le aree di lavoro con il ruolo desiderato in base allo specifico caso d’uso. A tale scopo, selezionare ogni [!DNL Target] [!UICONTROL profilo di prodotto] in [!DNL Adobe Admin Console] e aggiungere le integrazioni nella scheda [!UICONTROL Integrazione]. Prima della versione di settembre, tutte le integrazioni funzionavano con accesso [!UICONTROL Approvatore], indipendentemente dall&#39;opzione effettuata nell&#39;elenco a discesa [!UICONTROL Ruolo prodotto]. Ora puoi scegliere il ruolo desiderato.

>[!NOTE]
>
>Se non viene eseguita, dopo il rilascio della versione di settembre 2019 di [!DNL Target] verranno attivati i controlli di accesso e potresti essere in grado di accedere solo all’area di lavoro predefinita, qualora questa sia l’impostazione corrente. L’impostazione preventiva delle integrazioni non comporta alcun impatto negativo. Conviene quindi eseguirla quanto prima possibile. A seconda del numero di aree di lavoro dell’organizzazione, questo processo richiede solo pochi clic per aggiungere un’integrazione esistente alle aree di lavoro con il ruolo desiderato.

**Per consentire alle integrazioni Adobe I/O di accedere alle aree di lavoro e assegnare ruoli:**

1. Apri **[Adobe Admin Console](https://adminconsole.adobe.com)**.

1. Fai clic sulla scheda **[!UICONTROL Prodotti]**, quindi seleziona il nome del prodotto desiderato.

   ![Scegliere il prodotto in Adobe Admin Console](/help/main/administrating-target/c-user-management/property-channel/assets/io-choose-product.png)

1. Seleziona l’area di lavoro desiderata (Profilo prodotto).

   ![Selezionare il profilo prodotto](/help/main/administrating-target/c-user-management/property-channel/assets/io-select-product-profile.png)

1. Fai clic sulla scheda **[!UICONTROL Integrazioni]**.

   ![Scheda Integrazioni](/help/main/administrating-target/c-user-management/property-channel/assets/integrations-tab.png)

1. (Condizionale) Per aggiungere una nuova integrazione, fai clic su **[!UICONTROL Aggiungi integrazione]**, seleziona l&#39;integrazione desiderata, quindi fai clic su **[!UICONTROL Salva]**.

1. Dall&#39;elenco a discesa **[!UICONTROL Ruolo prodotto]**, selezionare il ruolo desiderato per l&#39;area di lavoro:

   | Ruolo | Descrizione |
   |--- |--- |
   | Responsabile approvazione | Può creare, modificare, attivare o interrompere le attività. |
   | Editor | Può creare e modificare le attività prima che siano in diretta, ma non può approvare l’avvio di un’attività. |
   | Osservatore | Può visualizzare le attività, ma non può crearle o modificarle. |
   | Editore | Simile al ruolo Osservatore (può visualizzare le attività, ma non può crearle o modificarle). Tuttavia, il ruolo Editore è anche autorizzato ad attivare le attività. |
