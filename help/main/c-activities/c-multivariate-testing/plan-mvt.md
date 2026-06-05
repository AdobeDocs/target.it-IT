---
keywords: test multivariato;mvt;piano mvt;piano test multivariato
description: Scopri come pianificare un [!UICONTROL test multivariato] in [!DNL Adobe Target] in modo da creare un test di successo.
title: Come posso pianificare un [!UICONTROL test multivariato]?
feature: Multivariate Tests
exl-id: 130718d5-7bd9-4b1a-b81a-7a146f0ffd0d
TQID: https://experienceleague.adobe.com/Fg9jOrPlkLxpbJdG-AKoWHD3YvIGEJPu7Os-RdfXvQA
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 295
ht-degree: 63%

---

# Pianifica un [!UICONTROL test multivariato]

[!UICONTROL Le attività di test multivariati] (MVT) in [!DNL Adobe Target] richiedono una certa pianificazione prima di poter creare un test di successo.

MVT richiede traffico sufficiente per generare risultati utili. Prima di configurare il test, è necessario sapere quanto traffico viene normalmente generato, compreso il numero di impression e di conversioni. Disporre di queste informazioni aiuta a ridurre la probabilità di progettare un test con requisiti che superano il traffico del sito.

Gli elementi devono essere indipendenti l&#39;uno dall&#39;altro. Ad esempio, non testare il layout e il contenuto nello stesso test.

Esamina il codice HTML per le pagine da testare. Assicurati che gli elementi HTML del sito non presentino ID DOM duplicati. Gli ID duplicati possono fare sì che lo stesso contenuto sia distribuito a più posizioni.

Pianifica il test degli elementi sulla pagina che produrranno probabilmente risultati significativi. Ad esempio, un banner o un’immagine hero porterà probabilmente più conversioni di una modifica del piè di pagina. L&#39;inclusione di elementi meno significativi nel test aumenta la quantità di traffico e il tempo necessario per eseguire il test sugli elementi più importanti della pagina.

Infine, prima di creare il test, devi creare il contenuto da verificare. Assicurati di comprendere le differenze nel contenuto previsto per ogni offerta, e di creare tutte le offerte immagine, testo e HTML che prevedi di utilizzare nel test.

## Video di formazione: Creazione di test multivariati (9:25) ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video illustra come pianificare e creare un test multivariato utilizzando il flusso di lavoro guidato in tre passaggi di [!DNL Target].

* Definizione e progettazione di un test multivariato
* Creazione di un test multivariato

>[!VIDEO](https://video.tv.adobe.com/v/17395)
