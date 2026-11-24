---
keywords: regole di inclusione;criteri di inclusione;consigli;promozione;promozioni;filtro dinamico;statico;filtro statico
description: Scopri come immettere manualmente uno o più valori statici da filtrare utilizzando le regole di inclusione in Consigli di Adobe [!DNL Target].
title: Filtro statico
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: 217e19bf-521f-4913-9b41-099c9af8b393
TQID: 'https://experienceleague.adobe.com/-HTJO4YFi0-isyA-5LbVUaEPu7YX1WFgPy-OexMSXFY'
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
source-git-commit: e8a9b6be04169ea3024673babb62085667fe8990
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 2%
---
# Filtro statico {#static-filter}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come filtrare i consigli immettendo manualmente uno o più valori statici nelle regole di inclusione in [!DNL Adobe Target Recommendations].

>[!ENDSHADEBOX]

**[!UICONTROL Filtro statico]** limita gli elementi di un consiglio agli elementi che corrispondono a valori statici immessi manualmente. È possibile creare qualsiasi numero di regole di inclusione. Le regole di inclusione sono collegate con un operatore AND, pertanto affinché un elemento possa essere incluso in un consiglio è necessario che siano soddisfatte tutte le regole. Per informazioni generali sulle regole di inclusione, vedere [Utilizzare regole di inclusione dinamiche e statiche](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md).

## Consiglia contenuti classificati G o PG

Per consigliare solo i contenuti con classificazione Motion Picture Association (MPA) &quot;G&quot; o &quot;PG&quot; (esclusi i contenuti &quot;R&quot; e &quot;NC17&quot;), crea una regola di filtro con l’operatore &quot;classificazione filmato uguale a qualsiasi di&quot; e immetti i valori &quot;g-nominale&quot; e &quot;pg-nominale&quot;.
