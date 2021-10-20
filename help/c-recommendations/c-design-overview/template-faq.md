---
keywords: consigli;domande frequenti;FAQ
description: Rivedi un elenco di domande frequenti (FAQ) e relative risposte sulle progettazioni di Adobe  [!DNL Target]  Recommendations.
title: Dove posso trovare risposte a domande sulla progettazione per  [!DNL Target]  Recommendations?
feature: Recommendations
exl-id: e970f734-9bc7-43b8-af1b-75e527d6353c
source-git-commit: c7d5c8eb50b28ee3f7651e510d005e3f37912f62
workflow-type: ht
source-wordcount: '456'
ht-degree: 100%

---

# ![PREMIUM](/help/assets/premium.png) Domande frequenti sulle progettazioni

Elenco di domande frequenti sulle progettazioni di [!DNL Adobe Target] [!DNL Recommendations].

## Nel prezzo consigliato dell’articolo non vengono visualizzati i due valori a destra del punto decimale. Come è possibile visualizzarli?

Per impostazione predefinita, i valori numerici (ad esempio `entity.value`) restituiti nei modelli di progettazione non presentano eventuali zeri finali dopo il separatore dei decimali. Ad esempio, se un articolo costa $35,00, `entity.value` è pari a 35 e sulla pagina viene visualizzato solo $35, e non $35,00.

Per risolvere il problema sono disponibili due opzioni:

* Puoi utilizzare uno script Velocity o JavaScript per applicare la formattazione al valore restituito.

* Potete trasmettere il prezzo dell’articolo come due attributi di entità distinti. Il primo, `entity.value`, può essere utilizzato per confronti numerici (ad esempio per regole di confronto dei prezzi). Il secondo, può essere un attributo personalizzato, ad esempio `entity.displayValue`, in cui il valore dell’entità viene memorizzato come stringa per consentirne il rendering corretto.

   Ad esempio,

   `"entity.value" : 35.00, "entity.displayValue" : "$35.00"`

## Perché la categoria non viene visualizzata nella progettazione? Sto utilizzando `$entity1.categoryId`. {#section_073309B8051049C7953D396A93EA0713}

L&#39;ID categoria non può essere visualizzato nella progettazione. Poiché è possibile archiviare più categorie, il sistema non saprebbe quale categoria visualizzare.

## Come posso modificare una progettazione per ottenere un aggiornamento immediato? {#section_28EE35A5B10B47ECA4A332F0E5B2598F}

L&#39;aggiornamento delle modifiche alla progettazione in uso richiede un po&#39; di tempo. Per modificare immediatamente la progettazione, creane una nuova, selezionala nell’attività e salva il consiglio.

## Come posso acquisire le informazioni chiave da visualizzare nella progettazione? Esempio: se vogliamo visualizzare la categoria del prodotto chiave, come posso codificare tale valore nel progetto Velocity? {#section_F08043B14BA24BC8815FEF25F4F84C39}

Il parametro `$key. *`value`*` acquisisce la maggior parte delle informazioni relative al prodotto chiave da visualizzare nella progettazione. Esempio: per visualizzare la miniatura del prodotto chiave, puoi utilizzare `$key.thumbnailURL`.

## Quale versione di Velocity viene utilizzata? {#section_28F00E15A4A54A768782A3F5BB0CDB21}

La versione 1.7 senza l’aggiunta di strumenti o librerie ulteriori. È disponibile la funzionalità di Velocity base.

## Come posso sostituire un valore entità esistente con uno vuoto? Ad esempio, per cancellare l&#39;oggetto entity.message di un elemento al termine di una promozione. {#section_B88F2C2925DC4508974B2F8B13F961CB}

Sembrerebbe possibile ottenere questo risultato mediante uno spazio unificatore JavaScript. Chiedi agli sviluppatori di inviare il valore `\u00A0`. Esempio: `entity.message=\u00A0`. Considera l&#39;utilizzo di questo valore come impostazione predefinita se non è presente alcun valore, anziché null.

## Posso utilizzare uno script di profilo in una progettazione [!DNL Recommendations]? {#section_6BD55203984A4D80A0C6F241AD7806DF}

Sì. Per utilizzare uno script di profilo in una progettazione [!DNL Recommendations], racchiudi il nome in `\${...}`. Ad esempio, se lo script di profilo è denominato `user.basket`, nella progettazione dovrai fare riferimento a `\${user.basket}`. La barra rovesciata implica che lo script del profilo non viene renderizzato da Velocity. Pertanto, non è possibile eseguire alcuna operazione sullo script del profilo in un modello Velocity. Il valore verrà stampato direttamente sulla pagina.
