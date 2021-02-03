---
keywords: integrazione;ruoli;autorizzazioni utente;admin console
description: Concedere alle  integrazioni Adobe I/O esistenti l'accesso a tutte le aree di lavoro con il ruolo desiderato in  Adobe Target
title: Concedere  accesso alle aree di lavoro e assegnare i ruoli ad Adobe I/O Integrations
feature: Administration & Configuration
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 83%

---


# ![PREMIUM](/help/assets/premium.png) Consentire alle integrazioni Adobe I/O di accedere alle aree di lavoro e assegnare ruoli

Le [!UICONTROL Autorizzazioni Enterprise] consentono ai clienti [!DNL Target] di utilizzare una singola organizzazione, ma di suddividerla in più aree di lavoro per i diversi team o flussi di lavoro.

>[!NOTE]
>
>La funzionalità Proprietà e Autorizzazioni è disponibile come parte della soluzione [Target Premium](/help/c-intro/intro.md#premium). Non sono disponibili in [!DNL Target Standard] senza una licenza [!DNL Target Premium].

La funzione [!UICONTROL Autorizzazioni Enterprise] permette di estendere a più team i programmi di ottimizzazione, in modo facile ed efficace. Questa funzionalità era già disponibile nell’interfaccia utente di [!DNL Target], ma è supportata dalle API amministratore solo dall’inizio del 2019. Nella versione di febbraio 2019 di [!DNL Target], Adobe ha aggiornato le API amministratore per consentire l’utilizzo dell’account di integrazione per accedere a tutte le aree di lavoro create nell’organizzazione. Precedentemente, le API amministratore erano limitate alla sola area di lavoro predefinita. Con l’aggiornamento di febbraio 2019 è possibile accedere a tutte le aree di lavoro con accesso di tipo [!UICONTROL Approvatore].

Con la versione di [!DNL Target] settembre 2019, [!DNL Target] [!UICONTROL Enterprise Permissions] offre ai clienti i seguenti controlli di accesso:

* Possibilità di scegliere le aree di lavoro a cui applicare l’integrazione
* Possibilità di applicare un ruolo all’integrazione Adobe I/O: [!UICONTROL Approvatore], [!UICONTROL Editor] o [!UICONTROL Osservatore].

Questo aggiornamento supporta i casi d’uso seguenti:

* Concedi all’integrazione Adobe I/O l’accesso a tutte le aree di lavoro con il ruolo [!UICONTROL Osservatore] a scopo di reporting, senza poter creare o modificare le risorse.
* Concedi all’integrazione Adobe I/O l’accesso a specifiche aree di lavoro con il ruolo appropriato per consentire a un team centrale di apportare modifiche basate su API solo a poche aree di lavoro.
* Consenti a ogni team proprietario della sua area di lavoro di disporre della propria integrazione non appena il team è pronto per esplorare le API e scegliere il ruolo di conseguenza.
* Puoi combinare insieme questi scenari in base alle esigenze.

**Azione richiesta**: i clienti che sfruttano già le API per operazioni CRUD su risorse (attività, tipi di pubblico, offerte e rapporti) in tutte le aree di lavoro devono concedere all’integrazione Adobe I/O esistente l’accesso a tutte le aree di lavoro con il ruolo desiderato in base allo specifico caso d’uso. A tale scopo, seleziona ogni [!UICONTROL profilo di prodotto] [!DNL Target] in [!DNL Adobe Admin Console] e aggiungi le integrazioni richieste nella scheda [!UICONTROL Integrazione]. Prima della versione di settembre, tutte le integrazioni funzionavano con l’accesso di tipo [!UICONTROL Approvatore], indipendentemente dall’opzione effettuata nell’elenco a discesa [!UICONTROL Ruolo prodotto]. Ora puoi scegliere il ruolo desiderato.

>[!NOTE]
>
>Se non viene eseguita, dopo il rilascio della versione di settembre 2019 di [!DNL Target] verranno attivati i controlli di accesso e potresti essere in grado di accedere solo all’area di lavoro predefinita, qualora questa sia l’impostazione corrente. L’impostazione preventiva delle integrazioni non comporta alcun impatto negativo. Conviene quindi eseguirla quanto prima possibile. A seconda del numero di aree di lavoro nell’organizzazione, questo processo richiede solo pochi clic per aggiungere un’integrazione esistente nelle aree di lavoro con il ruolo desiderato.

**Per consentire alle integrazioni Adobe I/O di accedere alle aree di lavoro e assegnare ruoli:**

1. Aprire il **[Adobe Admin Console](https://adminconsole.adobe.com)**.

1. Fai clic sulla scheda **[!UICONTROL Prodotti]**, quindi seleziona il nome del prodotto desiderato.

   ![Scegliere il prodotto in Adobe Admin Console](/help/administrating-target/c-user-management/property-channel/assets/io-choose-product.png)

1. Seleziona l’area di lavoro desiderata (Profilo prodotto).

   ![Selezionare il profilo prodotto](/help/administrating-target/c-user-management/property-channel/assets/io-select-product-profile.png)

1. Fai clic sulla scheda **[!UICONTROL Integrazioni]**.

   ![Scheda Integrazioni](/help/administrating-target/c-user-management/property-channel/assets/integrations-tab.png)

1. (Condizionale) Per aggiungere una nuova integrazione, fai clic su **[!UICONTROL Aggiungi integrazione]**, seleziona l’integrazione desiderata, quindi fai clic su **[!UICONTROL Salva]**.

1. Dall’elenco a discesa **[!UICONTROL Ruolo prodotto]**, seleziona il ruolo desiderato per tale area di lavoro:

   | Ruolo | Descrizione |
   |--- |--- |
   | Approvatore | Può creare, modificare, attivare o interrompere le attività. |
   | Editor | può creare e modificare le attività prima che siano in diretta, ma non può approvare l&#39;avvio di un&#39;attività. |
   | Osservatore | Può visualizzare le attività, ma non può crearle o modificarle. |
   | Editore | Simile al ruolo Osservatore (può visualizzare le attività, ma non può crearle o modificarle). Tuttavia, il ruolo Editore dispone dell&#39;autorizzazione aggiuntiva per attivare le attività. |
