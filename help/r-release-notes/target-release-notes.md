---
description: Note sulla versione che forniscono informazioni su funzioni, miglioramenti e correzioni per le versioni più recenti o imminenti di Adobe Target.
keywords: note sulla versione;rilasci;aggiornamenti;release futura;miglioramenti;nuove funzioni;correzioni
seo-description: Note sulla versione che forniscono informazioni su funzioni, miglioramenti e correzioni per le versioni DNL Adobe Target più recenti o imminenti.
seo-title: Note sulla versione di Adobe Target (prerelease)
solution: Target
title: Note sulla versione di Target (prerelease)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 1d91c46c78c0bcb58607def4cacaff0b761162fa

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

Le [!UICONTROL Autorizzazioni Enterprise] consentono ai clienti [!DNL Target] di utilizzare una singola organizzazione, ma di suddividerla in più aree di lavoro per i diversi team o flussi di lavoro. La funzione [!UICONTROL Autorizzazioni Enterprise] permette di estendere a più team i programmi di ottimizzazione, in modo facile ed efficace. Anche se questa funzione era disponibile nell’interfaccia utente di [!DNL Target], è supportata dalle API amministratore solo a partire dalla versione di febbraio 2019 di [!DNL Target]. Adobe ha aggiornato le API amministratore per consentire l’uso dell’account di integrazione per accedere a tutte le aree di lavoro create nell’organizzazione. Precedentemente, le API amministratore erano limitate all’area di lavoro predefinita. Con l’aggiornamento di febbraio 2019 è possibile accedere a tutte le aree di lavoro con accesso di tipo [!UICONTROL Approvatore].

Con la versione di [!DNL Target] di settembre 2019, le [!UICONTROL Autorizzazioni Enterprise] forniranno ai clienti i seguenti controlli di accesso:

* Possibilità di scegliere le aree di lavoro a cui applicare l’integrazione
* Possibilità di applicare un ruolo all’integrazione Adobe I/O: [!UICONTROL Approvatore], [!UICONTROL Editor] o [!UICONTROL Osservatore].

**Azione richiesta**: i clienti che sfruttano già le API per operazioni CRUD su risorse (attività, tipi di pubblico, offerte e rapporti) in tutte le aree di lavoro devono concedere all’integrazione Adobe I/O esistente l’accesso a tutte le aree di lavoro con il ruolo desiderato in base allo specifico caso d’uso. Prima della versione di settembre, tutte le integrazioni funzionavano con accesso di tipo [!UICONTROL Approvatore], a prescindere dal ruolo selezionato dall’elenco a discesa [!UICONTROL Ruolo prodotto]. A partire da questa versione, è possibile selezionare il ruolo desiderato.

Questa azione deve essere eseguita nel corso del mese di **agosto 2019**. Dopo il rilascio della versione di settembre 2019 di [!DNL Target] verranno attivati i controlli di accesso e potresti essere in grado di accedere solo all’area di lavoro predefinita, qualora questa sia l’impostazione corrente. L’impostazione anticipata dei ruoli dell’integrazione non comporta alcun impatto negativo.

Per istruzioni dettagliate e ulteriori informazioni, consulta [Consentire alle integrazioni Adobe I/O di accedere alle aree di lavoro e assegnare ruoli](/help/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md).

## Target Standard/Premium 19.9.2 (30 settembre 2019)

Questa versione di manutenzione include i seguenti miglioramenti:

* Diverse correzioni di sicurezza, compreso l’aggiornamento di sicurezza dell’editor Rich Text (RTE) nel Compositore esperienza visivo. (TGT-35383)

## Target Standard/Premium 19.9.1 (10 settembre 2019)

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| ![Autorizzazioni Enterprise badge](/help/assets/premium.png) Premium | Con la release di settembre 2019 di Target, le Autorizzazioni Enterprise forniscono ai clienti i seguenti controlli di accesso:<UL><li>Possibilità di scegliere le aree di lavoro a cui applicare l’integrazione.</li><li>Possibilità di applicare un ruolo all’integrazione Adobe I/O: Approvatore, Editor o Osservatore.</li></ul>Per istruzioni dettagliate e ulteriori informazioni, consulta [Consentire alle integrazioni Adobe I/O di accedere alle aree di lavoro e assegnare ruoli](/help/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md). |

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
