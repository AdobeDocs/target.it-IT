---
keywords: contenuto;risorse;gestione contenuto;offerte;gestione risorse;inserire modalità selezione;modalità di selezione
description: Scopri come gestire in modo efficiente le offerte di codice e immagini utilizzando la libreria [!UICONTROL Offerte].
title: Come posso gestire le offerte di codice e immagini?
feature: Experiences and Offers
exl-id: d8c24656-64d6-4a4b-a5f2-bcde57180007
TQID: https://experienceleague.adobe.com/A8ZLHW-FrWHGPJR7P-mhl2pO6SPoDc--LWpFEjtQzBY
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 958
ht-degree: 7%

---

# Offerte

Scopri come gestire in modo efficiente le offerte di codice e immagini utilizzando la libreria [!UICONTROL Offerte] in [!DNL Adobe Target].

Per visualizzare la libreria [!UICONTROL Offerte], fai clic sulla scheda **[!UICONTROL Offerte]** nella parte superiore dell&#39;interfaccia utente [!DNL Target].

![Pagina Offerte](/help/main/c-experiences/c-manage-content/assets/offers-page-new.png)

La libreria [!UICONTROL Offerte] contiene offerte configurate tramite [!DNL Target Standard/Premium], [!DNL Target Classic], [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] (AMS) e API. Le offerte create in [!DNL Target Classic] o altre soluzioni sono modificabili in [!DNL Target Standard/Premium].

La libreria [!UICONTROL Offerte] fornisce una panoramica di tutte le offerte di codice e immagini e consente di eseguire varie azioni:

| Elemento | Descrizione |
|--- |--- |
| Barra di navigazione a sinistra | Passa dalla visualizzazione di [!UICONTROL Offerte codice] alla visualizzazione di [!UICONTROL Offerte immagine]. |
| [!UICONTROL Mostra cartelle] / [!UICONTROL Nascondi cartelle]<P>![Icona Mostra/Nascondi filtri](/help/main/assets/icons/RailLeft.svg) | Fai clic sull&#39;icona **[!UICONTROL Mostra cartelle]** o **[!UICONTROL Nascondi cartelle]** per visualizzare o meno la struttura delle cartelle delle offerte.<P>Per ulteriori informazioni, consulta [Creare cartelle di offerta](/help/main/c-experiences/c-manage-content/create-content-folder.md). |
| [!UICONTROL Icona Mostra filtri]<P>![Icona Mostra filtri](/help/main/assets/icons/Filter.svg) | Fai clic sull&#39;icona **[!UICONTROL Mostra filtri]** per filtrare le offerte per [!UICONTROL Tipo], [!UICONTROL Source] e [!UICONTROL Tipo AEM].<P>Per ulteriori informazioni, vedere [Applica filtri all&#39;elenco delle offerte](#filters) di seguito. |
| Cerca campi | Utilizza i campi **[!UICONTROL Cerca in]** per trovare rapidamente un&#39;offerta o per ridurre il numero di offerte visualizzate nella libreria [!UICONTROL Offerte]. Puoi eseguire ricerche per [!UICONTROL Nome offerta], [!UICONTROL Percorsi AEM] o [!UICONTROL Tag AEM]. Le opzioni di ricerca sono persistenti in sessione. |
| [!UICONTROL Crea cartella] | Fai clic su **[!UICONTROL Crea cartella]** per creare cartelle nella libreria [!UICONTROL Offerta] in cui inserire offerte di codice, offerte di immagini e altre cartelle per creare una struttura di sottocartelle.<P>Per ulteriori informazioni, consulta [Creare cartelle di offerta](/help/main/c-experiences/c-manage-content/create-content-folder.md). |
| [!UICONTROL [!UICONTROL Crea offerta]] | Fai clic su **[!UICONTROL Crea offerta]** per creare un&#39;offerta.<P>Per ulteriori informazioni sulla creazione dei vari tipi di offerta, consulta: <ul><li>Offerta HTML</li><li>[Offerta JSON](/help/main/c-experiences/c-manage-content/create-json-offer.md)</li><li>[Offerta di reindirizzamento](/help/main/c-experiences/c-manage-content/offer-redirect.md)</li><li>[Offerta remota](/help/main/c-experiences/c-manage-content/about-remote-offers.md)</li></ul> |
| Caselle di controllo per le operazioni in blocco<P>![Icona Operazioni in blocco](/help/main/assets/icons/Rectangle.svg) | Fai clic sulle caselle di controllo [!UICONTROL Operazioni in blocco] per eseguire operazioni in blocco su tutte le offerte o sulle offerte selezionate.<P>Per un elenco delle azioni disponibili (a seconda delle autorizzazioni e dello stato dell&#39;offerta), consulta [Eseguire azioni rapide](#quick-actions) di seguito. |
| [!UICONTROL Nome] | Il nome di ogni offerta.<P>Fai clic sull&#39;icona **[!UICONTROL Informazioni rapide]** ( ![Icona Informazioni rapide](/help/main/assets/icons/InfoOutline.svg) ) accanto al nome di ciascuna offerta per visualizzare ulteriori informazioni sull&#39;offerta in una scheda a comparsa, tra cui l&#39;ID offerta, il tipo, la data dell&#39;ultima modifica dell&#39;offerta, l&#39;autore e altro ancora.<p>Fai clic sull&#39;icona **[!UICONTROL Altre azioni]** ( ![Icona Altre azioni](/help/main/assets/icons/MoreSmallList.svg) ) accanto al nome di ciascuna offerta per aprire un menu che consente di eseguire azioni rapide su un&#39;attività. Sono disponibili le seguenti azioni (a seconda delle autorizzazioni e dello stato dell&#39;offerta): [!UICONTROL Modifica], [!UICONTROL Copia], [!UICONTROL Elimina] e [!UICONTROL Sposta]. Per ulteriori informazioni su ciascuna azione, vedere [Eseguire azioni rapide](#quick-actions) di seguito.<P>Fai clic sull’intestazione della tabella per ordinare l’elenco in ordine alfabetico in ordine crescente o decrescente per nome. |
| [!UICONTROL Tipo] | Tipo di offerta: [!UICONTROL Offerte HTML], [[!UICONTROL Offerte di reindirizzamento]](/help/main/c-experiences/c-manage-content/offer-redirect.md), [[!UICONTROL Offerte remote]](/help/main/c-experiences/c-manage-content/about-remote-offers.md) e [[!UICONTROL Offerte JSON]](/help/main/c-experiences/c-manage-content/create-json-offer.md). |
| [!UICONTROL Source] | Mostra dove è stata creata l&#39;offerta: [!DNL Adobe Target], [!DNL Adobe Target Classic] e [!DNL Adobe Experience Manager]. |
| [!UICONTROL Ultimo aggiornamento] | Visualizza la data e l’ora dell’ultima modifica apportata all’offerta, specificando l’autore.<P>Fai clic sull’intestazione della tabella per ordinare l’elenco in ordine crescente o decrescente per data. |

## Applicare filtri alla libreria Offerte {#filters}

Fai clic sull&#39;icona **[!UICONTROL Mostra filtri]** (![Mostra icona Filtri nella pagina Offerte](/help/main/assets/icons/Filter.svg)) per filtrare le offerte per [!UICONTROL Tipo], [!UICONTROL Source] e [!UICONTROL Tipo AEM].

L&#39;icona **[!UICONTROL Mostra filtri]** consente di filtrare le offerte in base alle categorie seguenti:

* **[!UICONTROL Tipo]**: [!UICONTROL Offerta HTML], [[!UICONTROL Offerta di reindirizzamento]](/help/main/c-experiences/c-manage-content/offer-redirect.md), [[!UICONTROL Offerta remota]](/help/main/c-experiences/c-manage-content/about-remote-offers.md) e [[!UICONTROL Offerta JSON]](/help/main/c-experiences/c-manage-content/create-json-offer.md).

* **[!UICONTROL Source]**: [!DNL Adobe Target], [!DNL Adobe Target Classic] e [!DNL Adobe Experience Manager].

* **Tipo AEM**: [Frammenti di contenuto](/help/main/c-integrating-target-with-mac/aem/content-fragments-aem.md) e [Frammenti di esperienza](/help/main/c-integrating-target-with-mac/aem/experience-fragments-aem.md). Per ulteriori informazioni sui diversi tipi di frammenti, vedere [Panoramica sui frammenti di esperienza e sui frammenti di contenuto di AEM](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

I filtri sono persistenti a livello di sessione.

## Eseguire azioni rapide {#quick-actions}

Puoi eseguire le seguenti azioni rapide facendo clic sull’icona appropriata:

### Informazioni rapide

Fai clic sull&#39;icona **[!UICONTROL Informazioni rapide]** ( ![Icona Informazioni rapide](/help/main/assets/icons/InfoOutline.svg) ) accanto al nome di ciascuna offerta per visualizzare ulteriori informazioni sull&#39;offerta in una scheda a comparsa, tra cui l&#39;ID offerta, il tipo, la data dell&#39;ultima modifica dell&#39;offerta, l&#39;autore e altro ancora. Le opzioni disponibili dipendono dal tipo di offerta: [!UICONTROL Offerta HTML], [[!UICONTROL Offerta JSON]](/help/main/c-experiences/c-manage-content/create-json-offer.md), [[!UICONTROL Offerta di reindirizzamento]](/help/main/c-experiences/c-manage-content/offer-redirect.md), [[!UICONTROL Offerta remota]](/help/main/c-experiences/c-manage-content/about-remote-offers.md).

### Altre azioni

Le azioni disponibili per [!UICONTROL Offerte codice] e per [!UICONTROL Offerte immagine] sono leggermente diverse. Le sezioni che seguono contengono le informazioni seguenti:

#### [!UICONTROL Offerta codice] opzioni

Fai clic sull&#39;icona **[!UICONTROL Altre azioni]** ( ![Icona Altre azioni](/help/main/assets/icons/MoreSmallList.svg) ) accanto al nome di ciascuna offerta per aprire un menu che consente di eseguire azioni rapide su un&#39;attività.

Sono disponibili le seguenti azioni (a seconda delle autorizzazioni e dello stato dell’offerta):

* [!UICONTROL Modifica]
* [!UICONTROL Copia]
* [!UICONTROL Elimina]
* [!UICONTROL Sposta] (ad esempio, per spostare uno o più elementi in una cartella, fai clic su **[!UICONTROL Sposta]** accanto all&#39;elemento desiderato, fai clic sulla cartella desiderata, quindi fai clic su **[!UICONTROL Sposta]**.)

A seconda delle autorizzazioni, è possibile che non vengano visualizzate le icone per tutte le opzioni. Ad esempio, un utente con autorizzazioni [!UICONTROL Osservatore] non dispone dei diritti per utilizzare l&#39;opzione [!UICONTROL Copia].

Per informazioni dettagliate sulle attività che è possibile eseguire su offerte e cartelle, vedi [Operazioni con il contenuto della libreria di risorse](/help/main/c-experiences/c-manage-content/assets-working.md).

#### Opzioni [!UICONTROL Offerta immagine]

Per eseguire altre attività, passa il mouse sull&#39;offerta o sulla cartella di immagine desiderata nella scheda [!UICONTROL Offerte immagine] e fai clic sull&#39;icona desiderata.

Le opzioni includono:

* [!UICONTROL Select]
* [!UICONTROL Download]
* [!UICONTROL Visualizza proprietà]
* [!UICONTROL Altre azioni]
* [!UICONTROL Modifica]
* [!UICONTROL Annota]
* [!UICONTROL Copia]

Per informazioni dettagliate sulle attività che è possibile eseguire su offerte e cartelle, vedi [Operazioni con il contenuto della libreria di risorse](/help/main/c-experiences/c-manage-content/assets-working.md).

>[!NOTE]
>
>Le offerte di immagini non fanno parte del modello [Autorizzazioni utente Enterprise](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

## Visualizzazione delle definizioni delle offerte {#section_6B059DD121434E6292CAB393507D010E}

Per visualizzare i dettagli della definizione dell&#39;offerta in una scheda a comparsa nella libreria [!UICONTROL Offerte] senza aprire l&#39;offerta, fai clic sull&#39;icona ( ![Informazioni rapide](/help/main/assets/icons/InfoOutline.svg) ).

Sono disponibili le seguenti informazioni:

* [!UICONTROL Nome]
* [!UICONTROL ID offerta]
* [!UICONTROL Tipo]
* [!UICONTROL Ultima modifica]

Fai clic sul collegamento [!UICONTROL Visualizza dettagli completi] per visualizzare gli attributi e le attività dell&#39;offerta che fanno riferimento a un&#39;offerta di codice nella scheda a comparsa della definizione di ogni offerta. Questa funzionalità non è applicabile alle offerte di immagine. In questo modo puoi evitare un impatto su altre attività mentre modifichi le offerte. Le informazioni includono i dettagli per [!UICONTROL Attività live] e [!UICONTROL Attività inattive].
