---
keywords: multivariate test;mvt;mvt plan;multivariate test plan
description: I test multivariati in Adobe Target richiedono una certa pianificazione prima di poter creare un test di successo.
title: Pianificare un test multivariato in Adobe Target
feature: mvt
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 97%

---


# Pianificare un test multivariato{#plan-a-multivariate-test}

I [!UICONTROL test multivariati] (MVT) in [!DNL Adobe Target] richiedono una certa pianificazione prima di poter creare un test di successo.

I test multivariati richiedono traffico sufficiente a generare risultati utili. Prima di configurare il test, è necessario sapere quanto traffico viene normalmente generato, compreso il numero di impression e di conversioni. Questa informazione consentirà di ridurre la probabilità di progettare un test con requisiti in eccesso rispetto al traffico del sito.

È consigliabile che gli elementi siano indipendenti l’uno dall’altro. Ad esempio, non eseguire il test del layout e del contenuto contemporaneamente.

Esamina il codice HTML per le pagine da sottoporre a test. Assicurati che gli elementi HTML del sito non presentino ID DOM duplicati. Gli ID duplicati possono fare sì che lo stesso contenuto sia distribuito a più posizioni.

Pianifica il test degli elementi sulla pagina che produrranno probabilmente risultati significativi. Ad esempio, un banner o un’immagine protagonista porterà probabilmente più conversioni di una modifica del piè di pagina. L&#39;inclusione di elementi meno significativi nel test aumenta la quantità di traffico e il tempo necessario per eseguire il test sugli elementi più importanti della pagina.

Infine, prima di creare il test, devi creare il contenuto da verificare. Assicurati di comprendere le differenze nel contenuto previsto per ogni offerta, e di creare tutte le offerte immagine, testo e HTML che prevedi di utilizzare nel test.

## Video di formazione: Creazione di test multivariati (9:25) badge ![Esercitazione](/help/assets/tutorial.png)

In questo video viene illustrato come pianificare e creare un test multivariato utilizzando il flusso di lavoro guidato a tre passaggi di Target.

* Definizione e progettazione di un test multivariato
* Creazione di un test multivariato

>[!VIDEO](https://video.tv.adobe.com/v/17395)