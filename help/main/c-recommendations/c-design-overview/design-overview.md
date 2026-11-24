---
keywords: progettazione di consigli;modello;creare progettazione;consegna;output
description: Scopri come utilizzare le progettazioni in Adobe [!DNL Target] Recommendations per definire la modalità di visualizzazione dei consigli in una pagina (1X4, 1X6, 2X2 e così via).
title: Introduzione alle progettazioni
feature: Recommendations
exl-id: 348b1d77-49c9-4a6b-ba85-7ba051713d5b
TQID: 'https://experienceleague.adobe.com/08jboJLkp6MhgXiISjkVzh2kVze5DRrxO8BbQBFLeA4'
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
source-git-commit: f9c9c7b2b78ec020fcabae420686b8955e350a0e
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 9%
---
# Introduzione alle progettazioni {#design-overview}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come le progettazioni definiscono il layout e il formato dei consigli in [!DNL Adobe Target Recommendations].

>[!ENDSHADEBOX]

Le progettazioni in [!DNL Adobe Target Recommendations] definiscono la modalità di visualizzazione dei consigli in una pagina. Una progettazione definisce il layout e il formato dei consigli.

[!DNL Recommendations] viene fornito con diverse progettazioni predefinite (predefinite) ed è anche possibile creare progettazioni personalizzate. Per ulteriori informazioni, consulta [Creare una progettazione](/help/main/c-recommendations/c-design-overview/create-design.md).

[!DNL Target] può fornire l&#39;aspetto completo dei consigli, come illustrato nella figura seguente. La progettazione può includere HTML, JavaScript e CSS. Questo progetto è denominato progetto 4 x 1: quattro spazi in una riga.

![Esempio di un design 4 x 1 intitolato &quot;Altre attività divertenti&quot;, con quattro elementi ciascuno dei quali mostra una foto, un nome, un prezzo, una valutazione e una distanza](/help/main/c-recommendations/c-design-overview/assets/velocity_example.png)

[!DNL Target] può anche inviare i consigli come oggetti JSON che possono essere utilizzati nei messaggi e-mail, nei dispositivi IoT (Internet of Things), nella console o nei casi di utilizzo della voce (Amazon Alexa o Google Home).

Le progettazioni determinano:

* Quanti elementi vengono visualizzati in un consiglio
* Modalità di visualizzazione degli elementi in una riga, colonna, griglia o tabella
* Se i visitatori vedono solo il numero specificato di elementi o possono scorrere tra più elementi
