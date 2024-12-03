---
keywords: contenuto;risorse;gestione contenuto;offerte;gestione risorse;inserire modalità selezione;modalità di selezione
description: Scopri come gestire in modo efficiente le offerte di codice e immagini utilizzando la libreria [!UICONTROL Offers].
title: Come posso gestire le offerte di codice e immagini?
feature: Experiences and Offers
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#beta newtab=true" tooltip="Cosa sono le funzioni beta in [!DNL Adobe Target]."
hide: true
hidefromtoc: true
exl-id: f64aec3d-5f83-4bd1-8e64-df1779809812
source-git-commit: 6d18b76da95ad5c5b4d4144c75921a1c42313789
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 8%

---

# Offerte

Scopri come gestire in modo efficiente le offerte di codice e immagini utilizzando la libreria [!UICONTROL Offers] in [!DNL Adobe Target].

>[!NOTE]
>
>Questo articolo contiene informazioni sugli aggiornamenti dell&#39;interfaccia utente [!DNL Target] che fa attualmente parte di un programma Beta. Il team [!DNL Adobe Target] spesso abilita nuove funzionalità per determinati clienti a scopo di test e feedback. Al termine del periodo di test, queste funzionalità verranno abilitate per tutti i clienti nelle prossime versioni di [!DNL Target] e annunciate nelle [note sulla versione](/help/main/r-release-notes/release-notes.md).

Per visualizzare la libreria [!UICONTROL Offers], fare clic sulla scheda **[!UICONTROL Offers]** nella parte superiore dell&#39;interfaccia utente [!DNL Target].

![Pagina Offerte](/help/main/c-experiences/c-manage-content/assets/offers-page-new.png)

La libreria [!UICONTROL Offers] contiene offerte configurate tramite [!DNL Target Standard/Premium], [!DNL Target Classic], [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] (AMS) e API. Le offerte create in [!DNL Target Classic] o altre soluzioni sono modificabili in [!DNL Target Standard/Premium].

La libreria [!UICONTROL Offers] fornisce una panoramica di tutte le offerte di codice e immagini e consente di eseguire varie azioni:

| Elemento | Descrizione |
|--- |--- |
| Barra di navigazione a sinistra | Passare dalla visualizzazione di [!UICONTROL Code Offers] o [!UICONTROL Image Offers]. |
| [!UICONTROL Show Folders] / [!UICONTROL Hide Folders]<P>![Icona Mostra/Nascondi filtri](/help/main/assets/icons/RailLeft.svg) | Fai clic sull&#39;icona **[!UICONTROL Show Folders]** o **[!UICONTROL Hide Folders]** per visualizzare o meno la struttura delle cartelle delle offerte.<P>Per ulteriori informazioni, consulta [Creare cartelle di offerta](/help/main/c-experiences/c-manage-content/create-content-folder.md). |
| Icona [!UICONTROL Show filters]<P>![Icona Mostra filtri](/help/main/assets/icons/Filter.svg) | Fai clic sull&#39;icona **[!UICONTROL Show filters]** per filtrare le offerte in base a [!UICONTROL Type], [!UICONTROL Source] e [!UICONTROL AEM Type].<P>Per ulteriori informazioni, vedere [Applica filtri all&#39;elenco delle offerte](#filters) di seguito. |
| Cerca campo | Utilizzare i campi **[!UICONTROL Search in]** per trovare rapidamente un&#39;offerta o per ridurre il numero di offerte visualizzate nella libreria [!UICONTROL Offers]. È possibile eseguire ricerche per [!UICONTROL Offer Name], [!UICONTROL AEM Paths] o [!UICONTROL AEM Tags]. Le opzioni di ricerca sono persistenti in sessione. |
| [!UICONTROL Create Folder] | Fare clic su **[!UICONTROL Create Folder]** per creare cartelle nella libreria [!UICONTROL Offer] in modo che contengano offerte di codice, offerte di immagini e altre cartelle per creare una struttura di sottocartelle.<P>Per ulteriori informazioni, consulta [Creare cartelle di offerta](/help/main/c-experiences/c-manage-content/create-content-folder.md). |
| [!UICONTROL [!UICONTROL Create Offer]] | Fai clic su **[!UICONTROL Create Offer]** per creare un&#39;offerta.<P>Per ulteriori informazioni sulla creazione dei vari tipi di offerta, consulta: <ul><li>Offerta HTML</li><li>[Offerta JSON](/help/main/c-experiences/c-manage-content/create-json-offer.md)</li><li>[Offerta di reindirizzamento](/help/main/c-experiences/c-manage-content/offer-redirect.md)</li><li>[Offerta remota](/help/main/c-experiences/c-manage-content/about-remote-offers.md)</li></ul> |
| Caselle di controllo per le operazioni in blocco<P>![Icona Operazioni in blocco](/help/main/assets/icons/Rectangle.svg) | Fare clic sulle caselle di controllo [!UICONTROL Bulk Operations] per eseguire operazioni in blocco su tutte le offerte o sulle offerte selezionate.<P>Per un elenco delle azioni disponibili (a seconda delle autorizzazioni e dello stato dell&#39;offerta), consulta [Eseguire azioni rapide](#quick-actions) di seguito. |
| [!UICONTROL Name] | Il nome di ogni offerta.<P>Fai clic sull&#39;icona **[!UICONTROL Quick Info]** ( ![icona Informazioni rapide](/help/main/assets/icons/InfoOutline.svg) ) accanto a ciascun nome dell&#39;offerta per visualizzare ulteriori informazioni sull&#39;offerta in una scheda a comparsa, tra cui l&#39;ID offerta, il tipo, la data dell&#39;ultima modifica dell&#39;offerta, l&#39;autore e altro ancora.<p>Fai clic sull&#39;icona **[!UICONTROL More Actions]** ( ![Icona Altre azioni](/help/main/assets/icons/MoreSmallList.svg) ) accanto al nome di ogni offerta per aprire un menu che consente di eseguire azioni rapide su un&#39;attività. Sono disponibili le azioni seguenti (a seconda delle autorizzazioni e dello stato dell&#39;offerta): [!UICONTROL Edit], [!UICONTROL Copy], [!UICONTROL Delete] e [!UICONTROL Move]. Per ulteriori informazioni su ciascuna azione, vedere [Eseguire azioni rapide](#quick-actions) di seguito.<P>Fai clic sull’intestazione della tabella per ordinare l’elenco in ordine alfabetico in ordine crescente o decrescente per nome. |
| [!UICONTROL Type] | Tipo di offerta: [!UICONTROL HTML Offers], [[!UICONTROL Redirect Offers]](/help/main/c-experiences/c-manage-content/offer-redirect.md), [[!UICONTROL Remote Offers]](/help/main/c-experiences/c-manage-content/about-remote-offers.md) e [[!UICONTROL JSON Offers]](/help/main/c-experiences/c-manage-content/create-json-offer.md). |
| [!UICONTROL Source] | Mostra dove è stata creata l&#39;offerta: [!DNL Adobe Target], [!DNL Adobe Target Classic] e [!DNL Adobe Experience Manager]. |
| [!UICONTROL Last updated] | Visualizza la data e l’ora dell’ultima modifica apportata all’offerta, specificando l’autore.<P>Fai clic sull’intestazione della tabella per ordinare l’elenco in ordine crescente o decrescente per data. |

## Applicare filtri alla libreria Offerte {#filters}

Fai clic sull&#39;icona **[!UICONTROL Show filters]** ( ![Mostra icona Filtri nella pagina Offerte](/help/main/assets/icons/Filter.svg)) per filtrare le offerte per [!UICONTROL Type], [!UICONTROL Source] e [!UICONTROL AEM Type].

L&#39;icona **[!UICONTROL Show filters]** consente di filtrare le offerte in base alle seguenti categorie:

* **[!UICONTROL Type]**: [!UICONTROL HTML Offer], [[!UICONTROL Redirect Offer]](/help/main/c-experiences/c-manage-content/offer-redirect.md), [[!UICONTROL Remote Offer]](/help/main/c-experiences/c-manage-content/about-remote-offers.md) e [[!UICONTROL JSON Offer]](/help/main/c-experiences/c-manage-content/create-json-offer.md).

* **[!UICONTROL Source]**: [!DNL Adobe Target], [!DNL Adobe Target Classic] e [!DNL Adobe Experience Manager].

* **Tipo AEM**: [Frammenti di contenuto](/help/main/c-integrating-target-with-mac/aem/content-fragments-aem.md) e [Frammenti di esperienza](/help/main/c-integrating-target-with-mac/aem/experience-fragments-aem.md). Per ulteriori informazioni sui diversi tipi di frammenti, vedere [Panoramica sui frammenti di esperienza AEM e sui frammenti di contenuto](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

I filtri sono persistenti a livello di sessione.

## Eseguire azioni rapide {#quick-actions}

Puoi eseguire le seguenti azioni rapide facendo clic sull’icona appropriata:

### Informazioni rapide

Fai clic sull&#39;icona **[!UICONTROL Quick Info]** ( ![icona Informazioni rapide](/help/main/assets/icons/InfoOutline.svg) ) accanto a ciascun nome dell&#39;offerta per visualizzare ulteriori informazioni sull&#39;offerta in una scheda a comparsa, tra cui l&#39;ID offerta, il tipo, la data dell&#39;ultima modifica dell&#39;offerta, l&#39;autore e altro ancora. Le opzioni disponibili dipendono dal tipo di offerta: [!UICONTROL HTML Offer], [[!UICONTROL JSON Offer]](/help/main/c-experiences/c-manage-content/create-json-offer.md), [[!UICONTROL Redirect Offer]](/help/main/c-experiences/c-manage-content/offer-redirect.md), [[!UICONTROL Remote Offer]](/help/main/c-experiences/c-manage-content/about-remote-offers.md).

### Altre azioni

Le azioni disponibili per [!UICONTROL Code Offers] e per [!UICONTROL Image Offers] sono leggermente diverse. Le sezioni che seguono contengono le informazioni seguenti:

#### [!UICONTROL Code Offer] opzioni

Fai clic sull&#39;icona **[!UICONTROL More actions]** ( ![Icona Altre azioni](/help/main/assets/icons/MoreSmallList.svg) ) accanto al nome di ogni offerta per aprire un menu che consente di eseguire azioni rapide su un&#39;attività.

Sono disponibili le seguenti azioni (a seconda delle autorizzazioni e dello stato dell’offerta):

* [!UICONTROL Edit]
* [!UICONTROL Copy]
* [!UICONTROL Delete]
* [!UICONTROL Move] (ad esempio, per spostare uno o più elementi in una cartella, fare clic su **[!UICONTROL Move]** accanto all&#39;elemento desiderato, selezionare la cartella desiderata, quindi fare clic su **[!UICONTROL Move]**).

A seconda delle autorizzazioni, è possibile che non vengano visualizzate le icone per tutte le opzioni. Ad esempio, un utente con autorizzazioni [!UICONTROL Observer] non dispone dei diritti per utilizzare l&#39;opzione [!UICONTROL Copy].

Per informazioni dettagliate sulle attività che è possibile eseguire su offerte e cartelle, vedi [Operazioni con il contenuto della libreria di risorse](/help/main/c-experiences/c-manage-content/assets-working.md).

#### [!UICONTROL Image Offer] opzioni

Per eseguire altre attività, passa il mouse sull&#39;offerta immagine o sulla cartella desiderata nella scheda [!UICONTROL Image Offers] e fai clic sull&#39;icona desiderata.

Le opzioni includono:

* [!UICONTROL Select]
* [!UICONTROL Download]
* [!UICONTROL View Properties]
* [!UICONTROL More Actions]
* [!UICONTROL Edit]
* [!UICONTROL Annotate]
* [!UICONTROL Copy]

Per informazioni dettagliate sulle attività che è possibile eseguire su offerte e cartelle, vedi [Operazioni con il contenuto della libreria di risorse](/help/main/c-experiences/c-manage-content/assets-working.md).

>[!NOTE]
>
>Le offerte di immagini non fanno parte del modello [Autorizzazioni utente Enterprise](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

## Visualizzazione delle definizioni delle offerte {#section_6B059DD121434E6292CAB393507D010E}

Per visualizzare i dettagli della definizione dell&#39;offerta in una scheda a comparsa nella libreria [!UICONTROL Offers] senza aprire l&#39;offerta, fare clic sull&#39;icona ( ![Informazioni rapide](/help/main/assets/icons/InfoOutline.svg) ).

Sono disponibili le seguenti informazioni:

* [!UICONTROL Name]
* [!UICONTROL Offer ID]
* [!UICONTROL Type]
* [!UICONTROL Last Modified]

Fai clic sul collegamento [!UICONTROL View Full Details] per visualizzare gli attributi e le attività dell&#39;offerta che fanno riferimento a un&#39;offerta di codice nella scheda a comparsa di definizione di ogni offerta. Questa funzionalità non è applicabile alle offerte di immagine. In questo modo puoi evitare un impatto su altre attività mentre modifichi le offerte. Le informazioni includono dettagli per [!UICONTROL Live Activities] e [!UICONTROL Inactive Activities].
