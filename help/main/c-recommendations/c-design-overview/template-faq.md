---
keywords: consigli;domande frequenti;FAQ
description: Domande frequenti e relative risposte sulle progettazioni di [!DNL Target Recommendations]
title: Domande frequenti sulle progettazioni
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: e970f734-9bc7-43b8-af1b-75e527d6353c
TQID: 'https://experienceleague.adobe.com/xRu0XEnc8wX8PZngba7CO67mFdja7HALL-1OSnhAmuY'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: d5030abcda38bbc6d33b88ce3bb5d64f69e4e492
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 19%
---
# Domande frequenti sulle progettazioni {#design-faq}

>[!BEGINSHADEBOX]

**In questa pagina:** Trova le risposte alle domande più frequenti sulle progettazioni di [!DNL Adobe Target] [!DNL Recommendations].

>[!ENDSHADEBOX]

+++ In che modo il prezzo di un articolo consigliato può visualizzare entrambe le cifre a destra del punto decimale?

Per impostazione predefinita, i valori numerici (ad esempio `entity.value`) restituiti nelle progettazioni non presentano eventuali zeri finali dopo il punto decimale. Ad esempio, se un articolo costa $35,00, `entity.value` è pari a 35 e sulla pagina viene visualizzato solo $35, e non $35,00.

Per risolvere il problema sono disponibili due opzioni:

* Velocity scripting o JavaScript può applicare la formattazione al valore restituito.

* Il prezzo dell’articolo può essere trasmesso in due attributi di entità separati. Il primo, `entity.value`, può essere utilizzato per confronti numerici (ad esempio per regole di confronto dei prezzi). Il secondo deve essere un attributo personalizzato, ad esempio `entity.displayValue`, che memorizza il valore dell&#39;entità come stringa per consentirne il rendering corretto.

  Ad esempio,

  `"entity.value" : 35.00, "entity.displayValue" : "$35.00"`

+++

+++ Perché la categoria non viene visualizzata nella progettazione quando si utilizza $entity1.categoryId?

Impossibile visualizzare l&#39;ID categoria in una progettazione. È possibile memorizzare più categorie, pertanto il sistema non sa quale categoria visualizzare.

+++

+++ Come si può modificare una progettazione per ottenere un aggiornamento immediato?

L&#39;aggiornamento delle modifiche alla progettazione in uso richiede un po&#39; di tempo. Per modificare immediatamente la progettazione, creane una nuova, selezionala nell’attività e salva il consiglio.

+++

+++ In che modo le informazioni chiave, ad esempio la categoria del prodotto chiave, possono essere visualizzate in una progettazione?

I parametri `$key` acquisiscono la maggior parte delle informazioni del prodotto chiave da visualizzare nella progettazione. Ad esempio, per visualizzare la miniatura del prodotto chiave, utilizzare `$key.thumbnailURL`.

+++

+++ Quale versione di Velocity viene utilizzata?

Versione 1.7, senza l’aggiunta di strumenti o librerie. È disponibile la funzionalità di Velocity base.

+++

+++ In che modo un valore di entità esistente può essere sostituito con uno vuoto, ad esempio quando il valore entity.message di un elemento deve essere cancellato al termine di una promozione?

A tale scopo, viene visualizzato l’invio di uno spazio unificatore JavaScript. Gli sviluppatori inviano `\u00A0` come valore, ad esempio `entity.message=\u00A0`. È inoltre possibile utilizzare tale valore come valore predefinito quando non è presente alcun valore, anziché null.

+++

+++ È possibile utilizzare uno script di profilo in una progettazione [!DNL Recommendations]?

Sì. Per utilizzare uno script di profilo in una progettazione [!DNL Recommendations], racchiudi il nome in `\${...}`. Ad esempio, se lo script di profilo è denominato `user.basket`, nella progettazione fare riferimento a esso come `\${user.basket}`. La barra rovesciata implica che lo script di profilo non viene renderizzato da Velocity, pertanto non è possibile eseguire operazioni sullo script di profilo in un modello Velocity. Il valore viene stampato direttamente sulla pagina.

+++
