---
keywords: contenuto;risorse;gestione contenuto;offerte;gestione risorse;inserire modalità selezione;modalità di selezione
description: Scopri come gestire le offerte di codice e immagini utilizzando la libreria Offerte.
title: Come posso gestire le offerte di codice e immagini?
feature: Experiences and Offers
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#beta newtab=true" tooltip="Cosa sono le funzioni beta in [!DNL Adobe Target]."
hide: true
hidefromtoc: true
exl-id: f64aec3d-5f83-4bd1-8e64-df1779809812
source-git-commit: cd8035d9e2a369b9503763474ce09c4fe2434ae9
workflow-type: tm+mt
source-wordcount: '994'
ht-degree: 17%

---

# Offerte

Utilizza il [!UICONTROL Offers] libreria in [!DNL Adobe Target] per gestire il contenuto delle offerte basate su codice e immagine.

>[!NOTE]
>
>Questo articolo contiene informazioni sugli aggiornamenti di [!DNL Target] che fa attualmente parte di un programma beta. Il [!DNL Adobe Target] team abilita spesso nuove funzioni per determinati clienti a scopo di test e feedback. Al termine del periodo di test, queste funzioni saranno abilitate per tutti i clienti in futuro [!DNL Target Standard/Premium] e annunciate nelle note sulla versione.

Fai clic su **[!UICONTROL Offers]** nella parte superiore della sezione [!DNL Target] Interfaccia utente per visualizzare [!UICONTROL Offers] libreria.

![Libreria di offerte in Adobe Target](/help/main/c-experiences/c-manage-content/assets/offers-page-new.png)

Il [!UICONTROL Offers] la libreria contiene offerte che sono state impostate tramite [!DNL Target Standard/Premium], [!DNL Target Classic], [!DNL Adobe Experience Manager] (AEM) [!DNL Adobe Mobile Services] (AMS) e API. Le offerte create in [!DNL Target Classic] o altre soluzioni sono modificabili in [!DNL Target Standard/Premium].

La libreria Offerte fornisce una panoramica di tutte le offerte di codice e immagini e consente di eseguire varie azioni:

| Elemento | Descrizione |
|--- |--- |
| Barra di navigazione a sinistra | Passa da un’inserzione all’altra [!UICONTROL Code Offers] o [!UICONTROL Image Offers]. |
| [!UICONTROL Show filters] icona<P>![Icona Mostra filtri](/help/main/c-activities/assets/show-filters-icon.png) | Fai clic su **[!UICONTROL Show filters]** icona per filtrare le offerte [!UICONTROL Type], [!UICONTROL Source], e [!UICONTROL AEM Type]<P>Per ulteriori informazioni, consulta [Applicare i filtri all’elenco delle offerte](#filters) di seguito. |
| Cerca campo | Utilizza il **[!UICONTROL Search in]** per trovare rapidamente un’offerta o per ridurre il numero di offerte visualizzate nel [!UICONTROL Offers] libreria. Puoi eseguire ricerche per [!UICONTROL Offer Name], [!UICONTROL AEM Paths], o [!UICONTROL AEM Tags]. |
| [!UICONTROL Create Folder] | Fai clic su Crea cartella per creare cartelle in [!UICONTROL Offer] libreria per raccogliere offerte basate su codice, offerte basate su immagini e altre cartelle per creare una struttura di sottocartelle. Per ulteriori informazioni, consulta [Creare cartelle di offerta](/help/main/c-experiences/c-manage-content/create-content-folder.md). |
| [!UICONTROL [!UICONTROL Create Offer]] | Crea un’offerta. Per ulteriori informazioni sulla creazione dei vari tipi di offerta, consulta: <ul><li>Offerta HTML</li><li>[Offerta JSON](/help/main/c-experiences/c-manage-content/create-json-offer.md)</li><li>[Offerta di reindirizzamento](/help/main/c-experiences/c-manage-content/offer-redirect.md)</li><li>[Offerta remota](/help/main/c-experiences/c-manage-content/about-remote-offers.md)</li></ul> |
| Caselle di controllo per le operazioni in blocco | Eseguire operazioni in blocco su tutte le attività o sulle attività selezionate.<P>Per un elenco delle azioni disponibili (a seconda delle autorizzazioni e dello stato dell’offerta), consulta [Eseguire azioni rapide](#quick-actions) di seguito. |
| [!UICONTROL Name] | Il nome di ogni offerta.<P>Fai clic su **[!UICONTROL Quick Info]** accanto al nome di ogni offerta per visualizzare ulteriori informazioni sull’offerta in una scheda a comparsa, tra cui l’ID offerta, il tipo, la data dell’ultima modifica apportata all’offerta, il nome dell’utente e altro ancora.<p>Fai clic su **[!UICONTROL More actions]** (i puntini di sospensione orizzontali) accanto al nome di ogni offerta per aprire un menu che consente di eseguire azioni rapide su un’attività. Sono disponibili le seguenti azioni (a seconda delle autorizzazioni e dello stato dell’offerta): [!UICONTROL Edit], [!UICONTROL Copy], [!UICONTROL Delete], e [!UICONTROL Move]. Per ulteriori informazioni su ciascuna azione, consulta [Eseguire azioni rapide](#quick-actions) di seguito.<P>Fai clic sull’intestazione della tabella per ordinare l’elenco in ordine alfabetico in ordine crescente o decrescente per nome. |
| [!UICONTROL Type] | Il tipo di offerta: Offerte HTML, [Offerte di reindirizzamento](/help/main/c-experiences/c-manage-content/offer-redirect.md), [Offerte remote](/help/main/c-experiences/c-manage-content/about-remote-offers.md), e [Offerte JSON](/help/main/c-experiences/c-manage-content/create-json-offer.md). |
| [!UICONTROL Source] | Mostra dove è stata creata l’offerta: [!DNL Adobe Target], [!DNL Adobe Target Classic], e [!DNL Adobe Experience Manager]. |

## Applicare filtri alla libreria Offerte {#filters}

Fai clic su **[!UICONTROL Show filters]** icona ( ![Mostra l’icona Filtri nella pagina Offerte](/help/main/c-experiences/c-manage-content/assets/show-filters-icon.png) ) per filtrare le offerte per [!UICONTROL Type], [!UICONTROL Source], e [!UICONTROL AEM Type].

![immagine offers_filter](assets/offers-filter-new.png)

Il **[!UICONTROL Show filters]** consente di filtrare le offerte in base alle seguenti categorie:

* **Tipo**: Offerta HTML, [Offerta JSON](/help/main/c-experiences/c-manage-content/create-json-offer.md), [Offerta di reindirizzamento](/help/main/c-experiences/c-manage-content/offer-redirect.md), [Offerta remota](/help/main/c-experiences/c-manage-content/about-remote-offers.md).

* **Sorgente**: [!DNL Adobe Target], [!DNL Adobe Target Classic], e [!DNL Adobe Experience Manager].

* **Tipo di AEM**: [Frammenti di contenuto](/help/main/c-integrating-target-with-mac/aem/content-fragments-aem.md) e [Frammenti esperienza](/help/main/c-integrating-target-with-mac/aem/experience-fragments-aem.md). Per ulteriori informazioni sui diversi tipi di frammenti, consulta [Panoramica sui frammenti di esperienza e sui frammenti di contenuto dell’AEM](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

## Eseguire azioni rapide {#quick-actions}

Puoi eseguire le seguenti azioni rapide facendo clic sull’icona appropriata:

### Informazioni rapide

Fai clic su **[!UICONTROL Quick Info]** accanto al nome di ogni offerta per visualizzare ulteriori informazioni sull’offerta in una scheda a comparsa, tra cui l’ID offerta, il tipo, la data dell’ultima modifica apportata all’offerta, il nome dell’utente e altro ancora. Le opzioni disponibili dipendono dal tipo di offerta: Offerta HTML, [Offerta JSON](/help/main/c-experiences/c-manage-content/create-json-offer.md), [Offerta di reindirizzamento](/help/main/c-experiences/c-manage-content/offer-redirect.md), [Offerta remota](/help/main/c-experiences/c-manage-content/about-remote-offers.md).

![](/help/main/c-experiences/c-manage-content/assets/quick-actions.png)

### Altre azioni

Le azioni disponibili per le offerte codice e per le offerte immagine sono leggermente diverse. Le sezioni che seguono contengono le informazioni seguenti:

#### [!UICONTROL Code Offer] opzioni

Fai clic su **[!UICONTROL More actions]** (i puntini di sospensione orizzontali) accanto al nome di ogni offerta per aprire un menu che consente di eseguire azioni rapide su un’attività. Sono disponibili le seguenti azioni (a seconda delle autorizzazioni e dello stato dell’offerta): [!UICONTROL Edit], [!UICONTROL Copy], [!UICONTROL Delete], e [!UICONTROL Move].

![Opzione Altre azioni nella libreria Offerte di Target](/help/main/c-experiences/c-manage-content/assets/more-actions.png)

* Modifica
* Copia
* Elimina
* Sposta (ad esempio, per spostare uno o più elementi in una cartella, fare clic sul pulsante **[!UICONTROL Move]** per l’elemento desiderato, fai clic sulla cartella desiderata, quindi fai clic su **[!UICONTROL Drop]**.)

A seconda delle autorizzazioni, è possibile che non vengano visualizzate le icone per tutte le opzioni. Ad esempio, un utente con [!UICONTROL Observer] autorizzazioni non dispone dei diritti per utilizzare il [!UICONTROL Copy] opzione.

Per informazioni dettagliate sulle attività eseguibili su offerte e cartelle, consulta [Utilizzare i contenuti della libreria di risorse](/help/main/c-experiences/c-manage-content/assets-working.md).

#### [!UICONTROL Image Offer] opzioni

Per eseguire altre attività, passa il puntatore del mouse sull&#39;offerta o sulla cartella di immagine desiderata sul menu [!UICONTROL Image Offers] , quindi facendo clic sull&#39;icona desiderata.

![Opzioni Offerte immagine](/help/main/c-experiences/c-manage-content/assets/image-offers-icons.png)

Le opzioni includono:

* Seleziona
* Scarica
* View Properties (Visualizza proprietà)
* Modifica
* Annota
* Copia

Per informazioni dettagliate sulle attività eseguibili su offerte e cartelle, consulta [Utilizzare i contenuti della libreria di risorse](/help/main/c-experiences/c-manage-content/assets-working.md).

>[!NOTE]
>
>Le offerte di immagini non fanno parte del [Autorizzazioni per gli utenti Enterprise](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) modello.

## Visualizzazione delle definizioni delle offerte {#section_6B059DD121434E6292CAB393507D010E}

Puoi visualizzare i dettagli della definizione dell’offerta su una scheda a comparsa in [!UICONTROL Offers] senza aprire l’offerta.

Ad esempio, per accedere alla scheda di definizione dell’offerta seguente per un’offerta HTML, passa il puntatore del mouse su un’offerta nella [!UICONTROL Content] , quindi facendo clic sull&#39;icona delle informazioni:

![immagine offer-card-html](assets/offer-card-html.png)

Sono disponibili le seguenti informazioni:

* Nome
* Origine
* Tipo
* ID offerta
* Percorso offerta
* Ultima modifica

Fai clic su [!UICONTROL Offer Usage] per visualizzare le attività che fanno riferimento a un’offerta di codice nella scheda a comparsa di definizione di ogni offerta. Questa funzionalità non è applicabile alle offerte di immagine. In questo modo puoi evitare un impatto su altre attività mentre modifichi le offerte. Le informazioni includono [!UICONTROL Live Activities] e [!UICONTROL Inactive Activities].

![immagine offer-card-usage](assets/offer-card-usage.png)

Di seguito è illustrata la scheda di definizione di un’offerta di reindirizzamento:

![immagine offer-card-redirect](assets/offer-card-redirect.png)

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

![immagine remota offer-card-remote](assets/offer-card-remote.png)

Sono disponibili le seguenti informazioni:

* Nome
* Origine
* Tipo
* ID offerta
* Percorso offerta
* Ultima modifica
* Tipo di URL di reindirizzamento
* URL assoluto o relativo

## Video di formazione: L’archivio dei contenuti ![Badge panoramica](/help/main/assets/overview.png)

Questo video include informazioni sulla gestione delle offerte.

* Connessione tra la [libreria delle risorse di Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/assets/creative-cloud.html) e la libreria dei contenuti di Target
* Offerte HTML personalizzate
* Offerta HTML personalizzata nel Compositore esperienza visivo

>[!VIDEO](https://video.tv.adobe.com/v/17387)
