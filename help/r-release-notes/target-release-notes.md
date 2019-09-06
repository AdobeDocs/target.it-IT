---
description: Note sulla versione che forniscono informazioni su funzioni, miglioramenti e correzioni per i prossimi o imminenti [! DNL Adobe Target].
keywords: note sulla versione
seo-description: Note sulla versione che forniscono informazioni su funzioni, miglioramenti e correzioni per i prossimi o imminenti [! DNL Adobe Target].
seo-title: Note sulla versione di Adobe Target (prerelease)
solution: Target
title: Note sulla versione di Target (prerelease)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 27963738d0935427bd9c96df6922911394df31c3

---


# Note sulla versione di Target (prerelease){#target-release-notes-prerelease}

Queste note sulla versione contengono informazioni su funzioni, miglioramenti e correzioni per le versioni più recenti o in arrivo di [!DNL Adobe Target].

**Ultimo aggiornamento: 6 settembre 2019**

>[!NOTE]
>
>Queste note sulla versione contengono delle informazioni sulla versione prerelease. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso. Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali o possono essere diverse, a seconda della tempistica delle release.
>
>I codici tra parentesi sono per uso interno di [!DNL Adobe].

## Annunci

**31 luglio 2019**

[!UICONTROL Le autorizzazioni Enterprise] consentono [!DNL Target] ai clienti di utilizzare un'unica organizzazione, ma dividerla in aree di lavoro per diversi team o flussi di lavoro. La [!UICONTROL funzione Autorizzazioni] Enterprise semplifica il ridimensionamento efficace dei programmi di ottimizzazione tra i team. Anche se questa funzione era disponibile nell' [!DNL Target] interfaccia utente, le API amministratore non hanno superato il supporto corrispondente fino alla release [!DNL Target] di febbraio 2019. Adobe ha aggiornato le API Amministratore per poter utilizzare l'account di integrazione per accedere a tutte le aree di lavoro create nell'organizzazione. Così, mentre nelle versioni precedenti, le API amministratore erano limitate all'area di lavoro predefinita, l'aggiornamento di febbraio 2019 consentiva l'accesso a tutte le aree di lavoro con accesso [!UICONTROL Approver] .

Con la prossima release [!DNL Target] di settembre 2019, [!UICONTROL le autorizzazioni Enterprise] concederanno ai clienti i seguenti controlli di accesso:

* Potete scegliere le aree di lavoro a cui applicare l'integrazione.
* Potete applicare un ruolo all'integrazione I/O di Adobe: [!UICONTROL Approver], [!UICONTROL Editor]o [!UICONTROL Observer].

**Azione richiesta**: I clienti che stanno sfruttando API per operazioni CRUD su risorse (attività, tipi di pubblico, offerte e rapporti) in tutte le aree di lavoro devono concedere l'accesso esistente di integrazione I/O di Adobe a tutte le aree di lavoro con il ruolo desiderato. Prior to the September release, all integrations operated using [!UICONTROL Approver] access, regardless of the role selected from the [!UICONTROL Product Role] drop-down list. Con la prossima release, è possibile selezionare il ruolo desiderato.

Questa azione deve essere eseguita nel corso del mese **di agosto 2019**. Dopo la [!DNL Target] versione di settembre 2019, i controlli di accesso verranno attivati e potrete osservare l'accesso solo all'area di lavoro predefinita, se questa è la modalità di configurazione. Non vi sono conseguenze negative per configurare i ruoli di integrazione in anticipo.

Per istruzioni dettagliate e ulteriori informazioni, consultate [Concedere l'accesso alle integrazioni I/O Adobe alle aree di lavoro e assegnare ruoli](/help/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md).

## Target Standard/Premium 19.9.1 (10 settembre 2019)

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| ![Badge Premium](/help/assets/premium.png) Enterprise Permissions | Con la prossima release di Target 2019, Enterprise Permissions offre ai clienti i seguenti controlli di accesso:<UL><li>Potete scegliere le aree di lavoro a cui applicare l'integrazione.</li><li>Potete applicare un ruolo all'integrazione I/O di Adobe: Approver, Editor o Observer.</li></ul>Per istruzioni dettagliate e ulteriori informazioni, consultate [Concedere l'accesso alle integrazioni I/O Adobe alle aree di lavoro e assegnare ruoli](/help/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md). |

## Target Standard/Premium 19.9.2 (24 settembre 2019)

Questa versione di manutenzione include i seguenti miglioramenti:

* Diverse correzioni di protezione, compreso un aggiornamento di sicurezza all'editor Rich Text (RTE) in Visual Experience Composer (Compositore esperienza visivo). (TGT-35383)

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
