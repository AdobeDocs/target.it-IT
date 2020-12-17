---
keywords: api;apis;admin api;delivery api;reporting api;profile api
description: Informazioni  API Adobe Target, incluse le API Admin, Delivery, Reporting and Profile.
title: ' Panoramica dell''API Adobe Target'
feature: APIs/SDKs
translation-type: tm+mt
source-git-commit: 9b57d5554884b06d278c3baef3b2c1d5f37bdeb5
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 1%

---


#  Panoramica dell&#39;API Adobe Target

[!DNL Adobe Target] Le API possono essere raggruppate in base al tipo.

| Tipo di API | Cosa consente di fare | Collegamento di download | Altri collegamenti utili |
| --- | --- | --- |--- |
| Amministrazione | Creazione, modifica ed eliminazione di attività, audience, offerte e altri oggetti (comprese entità [!DNL Recommendations], criteri, progettazioni e così via). Le [!DNL Recommendations] API sono un tipo di API admin.) | <UL><li>[Raccolta Postman API di amministrazione di Target](https://developers.adobetarget.com/api/#admin-postman-collection)</li><li>[Recommendations API Postman Collection](https://developers.adobetarget.com/api/recommendations/#section/Postman)</li></ul> | [Usa ](https://experienceleague.adobe.com/docs/target-learn/recommendations-api-tutorial/recs-api-overview.html) API Recommendations in  *Tutorials Adobe Target* |
| Consegna | Recuperate contenuti ottimizzati e personalizzati da [!DNL Target] per la distribuzione a un utente finale. | [Raccolta Postman API Target Delivery](https://developers.adobetarget.com/api/delivery-api/#section/Getting-Started/Postman-Collection) |  |
| Generazione di rapporti | Esporta risultati attività e altri risultati di reporting. | Le API di reporting sono incluse nella [raccolta Postman API di amministrazione di Target](https://developers.adobetarget.com/api/#admin-postman-collection). |  |
| Profilo | Recuperate e modificate i profili utente memorizzati in  Adobe Target. | [Raccolta Postman API profilo di destinazione](https://developers.adobetarget.com/api/#profiles) |  |

>[!NOTE]
>
>Esistono importanti differenze tra le [!DNL Target] API Amministratore (incluse le [!DNL Recommendations] API) e le [!DNL Target] API di consegna:
>
>* Le API Admin consentono di configurare vari aspetti di [!DNL Target] che è anche possibile configurare nell&#39;interfaccia [!DNL Target]. Le API di amministrazione richiedono l&#39;autenticazione.
   >
   >
* Le API di distribuzione consentono di recuperare il contenuto. Le API di consegna non richiedono l&#39;autenticazione.
>
>
Per utilizzare le [!DNL Target] API Amministratore, è innanzitutto necessario configurare l&#39;autenticazione tramite  Adobe I/O. Per ulteriori informazioni, vedere [Configurare l&#39;autenticazione](https://experienceleague.adobe.com/docs/target-learn/tutorials/apis/configure-io-target-integration.html) in *Tutorials Adobe Target*.
