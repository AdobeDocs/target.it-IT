---
keywords: implementa;implementazione;impostazione;installazione;parametro di pagina;tomcat;codifica url;attributo profilo di pagina;parametro mbox;attributi profilo di pagina;attributo profilo script;aggiornamento API bulk profilo;aggiornamento API file singolo;attributi cliente;fornitori di dati;fornitori dati;fornitori di dati
description: Trasferisci i dati in Target (parametri di pagina, attributi di profilo, attributi di profilo di script, fornitori di dati, API di aggiornamento di profili singolo e in blocco, attributi del cliente).
title: Come posso inserire dati in Target?
feature: Implementazione
role: Developer
exl-id: b42eb846-d423-4545-a8fe-0b8048ab689e
translation-type: tm+mt
source-git-commit: e8c25685341319fea4381386cad1ce0c5b80face
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 69%

---

# Panoramica dei metodi

Informazioni sui diversi metodi possibili per ottenere i dati in [!DNL Adobe Target].

I metodi disponibili includono:

| Metodo | Dettagli |
| --- | --- |
| [Parametri di pagina](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/page-parameters.md)<br> (detti anche &quot;parametri mbox&quot;) | I parametri di pagina sono coppie di nome e valore passate direttamente tramite codice di pagina che non sono memorizzati nel profilo del visitatore per un utilizzo futuro.<br>I parametri di pagina sono utili per inviare dati di pagina a Target che non devono essere memorizzati con il profilo del visitatore per un utilizzo futuro del targeting. Questi valori vengono invece utilizzati per descrivere la pagina o l&#39;azione che l&#39;utente ha assunto nella pagina specifica. |
| [Attributi di profilo nella pagina](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/in-page-profile-attributes.md)<br> (detti anche &quot;attributi di profilo nella mbox&quot;) | Gli attributi di profilo nella pagina sono coppie di nome e valore passate direttamente tramite il codice della pagina archiviato nel profilo del visitatore per un utilizzo futuro.<br>Gli attributi di profilo nella pagina consentono l&#39;archiviazione dei dati specifici dell&#39;utente nel profilo di Target per targeting e segmentazione in un secondo momento. |
| [Attributi di profilo script](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/script-profile-attributes.md) | Gli attributi di profilo script sono coppie di nome e valore definite nella soluzione di Target. Il valore è determinato dall&#39;esecuzione di un frammento JavaScript sul server di destinazione per ogni chiamata del server.<br>Gli utenti scrivono frammenti di codice di piccole dimensioni che vengono eseguiti per chiamata mbox e prima che un visitatore venga valutato per l&#39;appartenenza al pubblico e all&#39;attività. |
| [Fornitori di dati](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/data-providers.md) | I provider di dati ti consentono di trasmettere facilmente dati da terze parti a Target. |
| [API di aggiornamento del profilo bulk](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/bulk-profile-update-api.md) | Tramite l&#39;API, inviare un file .csv a Target con gli aggiornamenti del profilo visitatori per molti visitatori. Ogni profilo visitatore può essere aggiornato con più attributi di profilo nella pagina in una chiamata. |
| [Aggiornamento di singolo profilo API](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/single-profile-update-api.md) | Quasi identico all&#39;API di aggiornamento del profilo bulk, ma un solo profilo visitatore alla volta viene aggiornato, in linea con la chiamata API anziché con un file .csv. |
| [Attributi del cliente](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/customer-attributes.md) | Gli attributi dei clienti consentono di caricare i dati del profilo visitatori tramite FTP nell&#39;Experience Cloud. Una volta effettuato l’aggiornamento, utilizza i dati in Adobe Analytics e Adobe Target. |












