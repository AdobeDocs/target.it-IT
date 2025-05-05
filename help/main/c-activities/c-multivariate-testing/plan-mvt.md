---
keywords: test multivariato;mvt;piano mvt;piano test multivariato
description: Scopri come pianificare un [!UICONTROL Multivariate Test] in [!DNL Adobe Target] in modo da creare un test riuscito.
title: Come posso pianificare [!UICONTROL Multivariate Test]?
feature: Multivariate Tests
exl-id: 130718d5-7bd9-4b1a-b81a-7a146f0ffd0d
source-git-commit: 0d73a062f70080057c3323f5150af067e3a2e27e
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 64%

---

# Pianifica [!UICONTROL Multivariate Test]

[!UICONTROL Multivariate Tests] attività (MVT) in [!DNL Adobe Target] richiedono una certa pianificazione prima di poter creare un test di successo.

MVT richiede traffico sufficiente per generare risultati utili. Prima di configurare il test, è necessario sapere quanto traffico viene normalmente generato, compreso il numero di impression e di conversioni. Disporre di queste informazioni aiuta a ridurre la probabilità di progettare un test con requisiti che superano il traffico del sito.

Gli elementi devono essere indipendenti l&#39;uno dall&#39;altro. Ad esempio, non testare il layout e il contenuto nello stesso test.

Esamina il codice HTML per le pagine da testare. Assicurati che gli elementi HTML del sito non presentino ID DOM duplicati. Gli ID duplicati possono fare sì che lo stesso contenuto sia distribuito a più posizioni.

Pianifica il test degli elementi sulla pagina che produrranno probabilmente risultati significativi. Ad esempio, un banner o un’immagine protagonista porterà probabilmente più conversioni di una modifica del piè di pagina. L&#39;inclusione di elementi meno significativi nel test aumenta la quantità di traffico e il tempo necessario per eseguire il test sugli elementi più importanti della pagina.

Infine, prima di creare il test, devi creare il contenuto da verificare. Assicurati di comprendere le differenze nel contenuto previsto per ogni offerta, e di creare tutte le offerte immagine, testo e HTML che prevedi di utilizzare nel test.

## Video di formazione: Creazione di test multivariati (9:25) ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video illustra come pianificare e creare un test multivariato utilizzando il flusso di lavoro guidato in tre passaggi di [!DNL Target].

* Definizione e progettazione di un test multivariato
* Creazione di un test multivariato

>[!VIDEO](https://video.tv.adobe.com/v/36329?captions=ita)
