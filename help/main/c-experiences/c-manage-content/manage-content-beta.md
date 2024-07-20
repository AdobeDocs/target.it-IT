---
keywords: contenuto;risorse;gestione contenuto;offerte;gestione risorse;inserire modalità selezione;modalità di selezione
description: Scopri come gestire le offerte di codice e immagini utilizzando la libreria Offerte.
title: Come posso gestire le offerte di codice e immagini?
feature: Experiences and Offers
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#beta newtab=true" tooltip="Cosa sono le funzioni beta in [!DNL Adobe Target]."
hide: true
hidefromtoc: true
exl-id: f64aec3d-5f83-4bd1-8e64-df1779809812
source-git-commit: 5d14dfd700cb1cec0fa62f66da1400bc8d7fd109
workflow-type: tm+mt
source-wordcount: '994'
ht-degree: 17%

---

# Offerte

Utilizza la libreria [!UICONTROL Offers] in [!DNL Adobe Target] per gestire il contenuto delle offerte di codice e immagine.

>[!NOTE]
>
>Questo articolo contiene informazioni sugli aggiornamenti dell&#39;interfaccia utente [!DNL Target] che fa attualmente parte di un programma Beta. Il team [!DNL Adobe Target] spesso abilita nuove funzionalità per determinati clienti a scopo di test e feedback. Al termine del periodo di test, queste funzioni vengono abilitate per tutti i clienti nelle prossime versioni di [!DNL Target Standard/Premium] e annunciate nelle note sulla versione.

Fare clic sulla scheda **[!UICONTROL Offers]** nella parte superiore dell&#39;interfaccia utente di [!DNL Target] per visualizzare la libreria [!UICONTROL Offers].

![Libreria offerte in Adobe Target](/help/main/c-experiences/c-manage-content/assets/offers-page-new.png)

La libreria [!UICONTROL Offers] contiene offerte configurate tramite [!DNL Target Standard/Premium], [!DNL Target Classic], [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] (AMS) e API. Le offerte create in [!DNL Target Classic] o altre soluzioni sono modificabili in [!DNL Target Standard/Premium].

La libreria Offerte fornisce una panoramica di tutte le offerte di codice e immagini e consente di eseguire varie azioni:

| Elemento | Descrizione |
|--- |--- |
| Barra di navigazione a sinistra | Passare dall&#39;elenco [!UICONTROL Code Offers] all&#39;elenco [!UICONTROL Image Offers]. |
| Icona [!UICONTROL Show filters]<P>![Icona Mostra filtri](/help/main/c-activities/assets/show-filters-icon.png) | Fai clic sull&#39;icona **[!UICONTROL Show filters]** per filtrare le offerte per [!UICONTROL Type], [!UICONTROL Source] e [!UICONTROL AEM Type]<P>Per ulteriori informazioni, vedere [Applica filtri all&#39;elenco delle offerte](#filters) di seguito. |
| Cerca campo | Utilizzare i campi **[!UICONTROL Search in]** per trovare rapidamente un&#39;offerta o per ridurre il numero di offerte visualizzate nella libreria [!UICONTROL Offers]. È possibile eseguire ricerche per [!UICONTROL Offer Name], [!UICONTROL AEM Paths] o [!UICONTROL AEM Tags]. |
| [!UICONTROL Create Folder] | Fare clic su Crea cartella per creare cartelle nella raccolta [!UICONTROL Offer] in modo che contengano offerte di codice, offerte di immagini e altre cartelle per creare una struttura di sottocartelle. Per ulteriori informazioni, consulta [Creare cartelle di offerta](/help/main/c-experiences/c-manage-content/create-content-folder.md). |
| [!UICONTROL [!UICONTROL Create Offer]] | Crea un’offerta. Per ulteriori informazioni sulla creazione dei vari tipi di offerta, consulta: <ul><li>Offerta HTML</li><li>[Offerta JSON](/help/main/c-experiences/c-manage-content/create-json-offer.md)</li><li>[Offerta di reindirizzamento](/help/main/c-experiences/c-manage-content/offer-redirect.md)</li><li>[Offerta remota](/help/main/c-experiences/c-manage-content/about-remote-offers.md)</li></ul> |
| Caselle di controllo per le operazioni in blocco | Eseguire operazioni in blocco su tutte le attività o sulle attività selezionate.<P>Per un elenco delle azioni disponibili (a seconda delle autorizzazioni e dello stato dell&#39;offerta), consulta [Eseguire azioni rapide](#quick-actions) di seguito. |
| [!UICONTROL Name] | Il nome di ogni offerta.<P>Fai clic sull&#39;icona **[!UICONTROL Quick Info]** accanto al nome di ogni offerta per visualizzare ulteriori informazioni su di essa in una scheda a comparsa, tra cui l&#39;ID offerta, il tipo, la data dell&#39;ultima modifica dell&#39;offerta, chi l&#39;ha effettuata e altro ancora.<p>Fai clic sull&#39;icona **[!UICONTROL More actions]** (i puntini di sospensione orizzontali) accanto al nome di ogni offerta per aprire un menu che consente di eseguire azioni rapide su un&#39;attività. Sono disponibili le azioni seguenti (a seconda delle autorizzazioni e dello stato dell&#39;offerta): [!UICONTROL Edit], [!UICONTROL Copy], [!UICONTROL Delete] e [!UICONTROL Move]. Per ulteriori informazioni su ciascuna azione, vedere [Eseguire azioni rapide](#quick-actions) di seguito.<P>Fai clic sull’intestazione della tabella per ordinare l’elenco in ordine alfabetico in ordine crescente o decrescente per nome. |
| [!UICONTROL Type] | Tipo di offerta: offerte HTML, [offerte di reindirizzamento](/help/main/c-experiences/c-manage-content/offer-redirect.md), [offerte remote](/help/main/c-experiences/c-manage-content/about-remote-offers.md) e [offerte JSON](/help/main/c-experiences/c-manage-content/create-json-offer.md). |
| [!UICONTROL Source] | Mostra dove è stata creata l&#39;offerta: [!DNL Adobe Target], [!DNL Adobe Target Classic] e [!DNL Adobe Experience Manager]. |

## Applicare filtri alla libreria Offerte {#filters}

Fai clic sull&#39;icona **[!UICONTROL Show filters]** ( ![icona Mostra filtri nella pagina Offerte](/help/main/c-experiences/c-manage-content/assets/show-filters-icon.png) ) per filtrare le offerte per [!UICONTROL Type], [!UICONTROL Source] e [!UICONTROL AEM Type].

![immagine_filtro offerte](assets/offers-filter-new.png)

L&#39;icona **[!UICONTROL Show filters]** consente di filtrare le offerte in base alle seguenti categorie:

* **Tipo**: Offerta HTML, [Offerta JSON](/help/main/c-experiences/c-manage-content/create-json-offer.md), [Offerta di reindirizzamento](/help/main/c-experiences/c-manage-content/offer-redirect.md), [Offerta remota](/help/main/c-experiences/c-manage-content/about-remote-offers.md).

* **Source**: [!DNL Adobe Target], [!DNL Adobe Target Classic] e [!DNL Adobe Experience Manager].

* **Tipo AEM**: [Frammenti di contenuto](/help/main/c-integrating-target-with-mac/aem/content-fragments-aem.md) e [Frammenti di esperienza](/help/main/c-integrating-target-with-mac/aem/experience-fragments-aem.md). Per ulteriori informazioni sui diversi tipi di frammenti, vedere [Panoramica sui frammenti di esperienza AEM e sui frammenti di contenuto](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

## Eseguire azioni rapide {#quick-actions}

Puoi eseguire le seguenti azioni rapide facendo clic sull’icona appropriata:

### Informazioni rapide

Fai clic sull&#39;icona **[!UICONTROL Quick Info]** accanto al nome di ogni offerta per visualizzare ulteriori informazioni su di essa in una scheda a comparsa, tra cui l&#39;ID offerta, il tipo, la data dell&#39;ultima modifica dell&#39;offerta, chi l&#39;ha effettuata e altro ancora. Le opzioni disponibili dipendono dal tipo di offerta: Offerta HTML, [Offerta JSON](/help/main/c-experiences/c-manage-content/create-json-offer.md), [Offerta di reindirizzamento](/help/main/c-experiences/c-manage-content/offer-redirect.md), [Offerta remota](/help/main/c-experiences/c-manage-content/about-remote-offers.md).

![](/help/main/c-experiences/c-manage-content/assets/quick-actions.png)

### Altre azioni

Le azioni disponibili per le offerte codice e per le offerte immagine sono leggermente diverse. Le sezioni che seguono contengono le informazioni seguenti:

#### [!UICONTROL Code Offer] opzioni

Fai clic sull&#39;icona **[!UICONTROL More actions]** (i puntini di sospensione orizzontali) accanto al nome di ogni offerta per aprire un menu che consente di eseguire azioni rapide su un&#39;attività. Sono disponibili le azioni seguenti (a seconda delle autorizzazioni e dello stato dell&#39;offerta): [!UICONTROL Edit], [!UICONTROL Copy], [!UICONTROL Delete] e [!UICONTROL Move].

![Opzione Altre azioni nella libreria Offerte di Target](/help/main/c-experiences/c-manage-content/assets/more-actions.png)

* Modifica
* Copia
* Elimina
* Sposta (ad esempio, per spostare uno o più elementi in una cartella, fare clic sull&#39;icona **[!UICONTROL Move]** dell&#39;elemento desiderato, fare clic sulla cartella desiderata, quindi fare clic su **[!UICONTROL Drop]**.)

A seconda delle autorizzazioni, è possibile che non vengano visualizzate le icone per tutte le opzioni. Ad esempio, un utente con autorizzazioni [!UICONTROL Observer] non dispone dei diritti per utilizzare l&#39;opzione [!UICONTROL Copy].

Per informazioni dettagliate sulle attività che è possibile eseguire su offerte e cartelle, vedi [Operazioni con il contenuto della libreria di risorse](/help/main/c-experiences/c-manage-content/assets-working.md).

#### [!UICONTROL Image Offer] opzioni

Per eseguire altre attività, passa il mouse sull&#39;offerta immagine o sulla cartella desiderata nella scheda [!UICONTROL Image Offers] e fai clic sull&#39;icona desiderata.

![Opzioni offerte immagini](/help/main/c-experiences/c-manage-content/assets/image-offers-icons.png)

Le opzioni includono:

* Seleziona
* Scarica
* View Properties (Visualizza proprietà)
* Modifica
* Annota
* Copia

Per informazioni dettagliate sulle attività che è possibile eseguire su offerte e cartelle, vedi [Operazioni con il contenuto della libreria di risorse](/help/main/c-experiences/c-manage-content/assets-working.md).

>[!NOTE]
>
>Le offerte di immagini non fanno parte del modello [Autorizzazioni utente Enterprise](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

## Visualizzazione delle definizioni delle offerte {#section_6B059DD121434E6292CAB393507D010E}

È possibile visualizzare i dettagli della definizione dell&#39;offerta in una scheda a comparsa nella libreria [!UICONTROL Offers] senza aprire l&#39;offerta.

Ad esempio, per accedere alla scheda di definizione dell&#39;offerta seguente per un&#39;offerta HTML, passa il puntatore del mouse su un&#39;offerta nell&#39;elenco [!UICONTROL Content] e fai clic sull&#39;icona delle informazioni:

![immagine html della scheda offerta](assets/offer-card-html.png)

Sono disponibili le seguenti informazioni:

* Nome
* Origine
* Tipo
* ID offerta
* Percorso offerta
* Ultima modifica

Fai clic sulla scheda [!UICONTROL Offer Usage] per visualizzare le attività che fanno riferimento a un&#39;offerta di codice nella scheda a comparsa della definizione di ogni offerta. Questa funzionalità non è applicabile alle offerte di immagine. In questo modo puoi evitare un impatto su altre attività mentre modifichi le offerte. Le informazioni includono [!UICONTROL Live Activities] e [!UICONTROL Inactive Activities].

![immagine di utilizzo delle schede offerte](assets/offer-card-usage.png)

Di seguito è illustrata la scheda di definizione di un’offerta di reindirizzamento:

![immagine di reindirizzamento scheda offerte](assets/offer-card-redirect.png)

Sono disponibili le seguenti informazioni:

* Nome
* Origine
* Tipo
* ID offerta
* Percorso offerta
* Ultima modifica
* URL di reindirizzamento
* Includi tutti i parametri URL (attivato o disattivato)
* Passa ID sessione mbox (attivato o disattivato)

Di seguito è illustrata la scheda di definizione di un’offerta remota:

![immagine remota scheda offerte](assets/offer-card-remote.png)

Sono disponibili le seguenti informazioni:

* Nome
* Origine
* Tipo
* ID offerta
* Percorso offerta
* Ultima modifica
* Tipo di URL di reindirizzamento
* URL assoluto o relativo

## Video di formazione: Archivio dei contenuti ![Badge panoramica](/help/main/assets/overview.png)

Questo video include informazioni sulla gestione delle offerte.

* Connessione tra la [libreria delle risorse di Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/assets/creative-cloud.html) e la libreria dei contenuti di Target
* Offerte HTML personalizzate
* Offerta HTML personalizzata nel Compositore esperienza visivo

>[!VIDEO](https://video.tv.adobe.com/v/17387)
