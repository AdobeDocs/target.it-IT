---
keywords: api;api;api amministratore;api di consegna;api di reporting;api profilo
description: Trova Adobe [!DNL Target] API, incluse le API amministratore, consegna, reporting e profilo.
title: Dove posso trovare [!DNL Target] Documentazione API e SDK?
feature: APIs/SDKs
role: Developer
exl-id: 2a0232cc-9a6a-42f4-afb6-4b3e2b13939c
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 1%

---

# Adobe [!DNL Target] Panoramica API

[!DNL Adobe Target] Le API possono essere raggruppate in base al tipo: API di amministrazione, distribuzione, reporting e profilo.

| Tipo di API | Cosa ti consente di fare | Collegamento di download | Altri collegamenti utili |
| --- | --- | --- |--- |
| Amministrazione | Creare, modificare ed eliminare attività, tipi di pubblico, offerte e altri oggetti (tra cui [!DNL Recommendations] entità, criteri, progettazioni e così via. La [!DNL Recommendations] Le API sono un tipo di API amministratore.) | <UL><li>[Raccolta Postman dell’API amministratore di Target](https://developers.adobetarget.com/api/#admin-postman-collection)</li><li>[Raccolta Postman API Recommendations](https://developers.adobetarget.com/api/recommendations/#section/Postman)</li></ul> | [Utilizzare le API di Recommendations](https://experienceleague.adobe.com/docs/target-learn/recommendations-api-tutorial/recs-api-overview.html) in *Tutorials Adobe Target* |
| Consegna | Recupera contenuti ottimizzati e personalizzati da [!DNL Target] per la consegna a un utente finale. | [Raccolta Postman API della consegna di Target](https://developers.adobetarget.com/api/delivery-api/#section/Getting-Started/Postman-Collection) |  |
| Generazione di rapporti | Esportare i risultati dell’attività e altri risultati di reporting. | Le API di reporting sono incluse nella [Raccolta Postman dell’API amministratore di Target](https://developers.adobetarget.com/api/#admin-postman-collection). |  |
| Profilo | Recupera e modifica i profili utente memorizzati in Adobe Target. | [Raccolta Postman API del profilo di Target](https://developers.adobetarget.com/api/#profiles) |  |

>[!NOTE]
>
>Esistono importanti distinzioni tra [!DNL Target] API amministratore (tra cui [!DNL Recommendations] API) e [!DNL Target] API di consegna:
>
>* Le API amministratore consentono di configurare vari aspetti di [!DNL Target] che è possibile configurare anche in [!DNL Target] Interfaccia utente. Le API amministratore richiedono l’autenticazione.
>
>* Le API di consegna ti consentono di recuperare il contenuto. Le API di consegna non richiedono l’autenticazione.
>
>Per utilizzare [!DNL Target] API amministratore, devi prima configurare l’autenticazione utilizzando Adobe I/O. Per ulteriori informazioni, consulta [Configurare l’autenticazione](https://experienceleague.adobe.com/docs/target-learn/tutorials/apis/configure-io-target-integration.html) in *Tutorials Adobe Target*.
