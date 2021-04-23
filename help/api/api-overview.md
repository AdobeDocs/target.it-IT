---
keywords: api;api;api amministratore;api di consegna;api di reporting;api profilo
description: Trova API di Adobe [!DNL Target] tra cui API amministratore, consegna, reporting e profilo.
title: Dove posso trovare la documentazione API e SDK [!DNL Target] ?
feature: API/SDK
role: Developer
exl-id: 2a0232cc-9a6a-42f4-afb6-4b3e2b13939c
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 1%

---

# Adobe [!DNL Target] Panoramica API

[!DNL Adobe Target] Le API possono essere raggruppate in base al tipo: API di amministrazione, distribuzione, reporting e profilo.

| Tipo di API | Cosa ti consente di fare | Collegamento di download | Altri collegamenti utili |
| --- | --- | --- |--- |
| Amministrazione | Crea, modifica ed elimina attività, tipi di pubblico, offerte e altri oggetti (comprese entità [!DNL Recommendations], criteri, progettazioni e così via). Le API [!DNL Recommendations] sono un tipo di API amministratore.) | <UL><li>[Raccolta Postman dell’API amministratore di Target](https://developers.adobetarget.com/api/#admin-postman-collection)</li><li>[Raccolta Postman API Recommendations](https://developers.adobetarget.com/api/recommendations/#section/Postman)</li></ul> | [Utilizzare ](https://experienceleague.adobe.com/docs/target-learn/recommendations-api-tutorial/recs-api-overview.html) API Recommendations nei Tutorials  *Adobe Target* |
| Consegna | Recupera contenuti ottimizzati e personalizzati da [!DNL Target] per la consegna a un utente finale. | [Raccolta Postman API della consegna di Target](https://developers.adobetarget.com/api/delivery-api/#section/Getting-Started/Postman-Collection) |  |
| Generazione di rapporti | Esportare i risultati dell’attività e altri risultati di reporting. | Le API di reporting sono incluse nella [raccolta Postman API di amministrazione di Target](https://developers.adobetarget.com/api/#admin-postman-collection). |  |
| Profilo | Recupera e modifica i profili utente memorizzati in Adobe Target. | [Raccolta Postman API del profilo di Target](https://developers.adobetarget.com/api/#profiles) |  |

>[!NOTE]
>
>Esistono importanti distinzioni tra le API amministratore [!DNL Target] (incluse le API [!DNL Recommendations]) e le API di consegna [!DNL Target]:
>
>* Le API amministratore ti consentono di configurare vari aspetti di [!DNL Target] che puoi configurare anche nell’ interfaccia utente di [!DNL Target] . Le API amministratore richiedono l’autenticazione.
   >
   >
* Le API di consegna ti consentono di recuperare il contenuto. Le API di consegna non richiedono l’autenticazione.
>
>
Per utilizzare le [!DNL Target] API amministratore, devi prima configurare l’autenticazione utilizzando Adobe I/O. Per ulteriori informazioni, consulta [Configura autenticazione](https://experienceleague.adobe.com/docs/target-learn/tutorials/apis/configure-io-target-integration.html) in *Tutorials Adobe Target*.
