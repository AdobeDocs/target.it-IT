---
keywords: recommendations;frequently asked questions;faq
description: Elenco delle domande frequenti sulle progettazioni  raccomandazioni Adobe Target.
title: Domande frequenti sulle progettazioni
feature: designs
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 87%

---


# ![PREMIUM](/help/assets/premium.png) Domande frequenti sulle progettazioni {#design-faq}

List of frequently asked questions (FAQs) about [!DNL Adobe Target] recommendations designs.

## Nel prezzo consigliato dell’articolo non vengono visualizzati i due valori a destra del punto decimale. Come è possibile visualizzarli?

Per impostazione predefinita, i valori numerici (ad esempio `entity.value`) restituiti nei modelli di progettazione non presentano eventuali zeri finali dopo il separatore dei decimali. Ad esempio, se un articolo costa $35,00, `entity.value` è pari a 35 e sulla pagina viene visualizzato solo $35, e non $35,00.

Per risolvere il problema sono disponibili due opzioni:

* Puoi utilizzare uno script Velocity o JavaScript per applicare la formattazione al valore restituito.

* Potete trasmettere il prezzo dell’articolo come due attributi di entità distinti. Il primo, `entity.value`, può essere utilizzato per confronti numerici (ad esempio per regole di confronto dei prezzi). Il secondo, può essere un attributo personalizzato, ad esempio `entity.displayValue`, in cui il valore dell’entità viene memorizzato come stringa per consentirne il rendering corretto.

   Ad esempio,

   `"entity.value" : 35.00, "entity.displayValue" : "$35.00"`

## Perché la categoria non viene visualizzata nella progettazione? Sto utilizzando $entity1.categoryId. {#section_073309B8051049C7953D396A93EA0713}

L&#39;ID categoria non può essere visualizzato nella progettazione. Poiché è possibile archiviare più categorie, il sistema non saprebbe quale categoria visualizzare.

## Come posso modificare una progettazione per ottenere un aggiornamento immediato? {#section_28EE35A5B10B47ECA4A332F0E5B2598F}

L&#39;aggiornamento delle modifiche alla progettazione in uso richiede un po&#39; di tempo. Per modificare immediatamente la progettazione, create una nuova progettazione, selezionatela nell&#39;attività e salvate la raccomandazione.

## Come posso acquisire le informazioni chiave da visualizzare nella progettazione? Esempio: se vogliamo visualizzare la categoria del prodotto chiave, come posso codificare tale valore nel progetto Velocity? {#section_F08043B14BA24BC8815FEF25F4F84C39}

Il parametro `$key. *`value`*` acquisisce la maggior parte delle informazioni relative al prodotto chiave da visualizzare nella progettazione. Esempio: per visualizzare la miniatura del prodotto chiave, puoi utilizzare `$key.thumbnailURL`.

## Quale versione di Velocity viene utilizzata? {#section_28F00E15A4A54A768782A3F5BB0CDB21}

La versione 1.7 senza l’aggiunta di strumenti o librerie ulteriori. È disponibile la funzionalità di Velocity base.

## Come posso sostituire un valore entità esistente con uno vuoto? Ad esempio, per cancellare l&#39;oggetto entity.message di un elemento al termine di una promozione. {#section_B88F2C2925DC4508974B2F8B13F961CB}

L&#39;invio in uno spazio unificatore JavaScript sembra procedere in questo modo. Chiedi agli sviluppatori di inviare il valore `\u00A0`. Esempio: `entity.message=\u00A0`. Considera l&#39;utilizzo di questo valore come impostazione predefinita se non è presente alcun valore, anziché null.

## Posso utilizzare uno script di profilo in una progettazione Consigli? {#section_6BD55203984A4D80A0C6F241AD7806DF}

Sì. Tuttavia, è necessario aggiungere una barra rovesciata (\) prima di $ nel nome dello script del profilo.
