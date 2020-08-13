---
keywords: api;apis;admin api;delivery api;reporting api;profile api
description: Informazioni  API Adobe Target, incluse le API Admin, Delivery, Reporting and Profile.
title: ' Panoramica dell''API Adobe Target'
feature: api
topic: APIs
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 1%

---


#  Panoramica dell&#39;API Adobe Target

[!DNL Adobe Target] Le API possono essere raggruppate in base al tipo.

| Tipo di API | Cosa consente di fare | Collegamento di download | Altri collegamenti utili |
| --- | --- | --- |--- |
| Amministrazione | Creazione, modifica ed eliminazione di attività, audience, offerte e altri oggetti (incluse [!DNL Recommendations] entità, criteri, progettazioni e così via). Le [!DNL Recommendations] API sono un tipo di API admin.) | <UL><li>[Raccolta Postman API di amministrazione di Target](https://developers.adobetarget.com/api/#admin-postman-collection)</li><li>[Recommendations API Postman Collection](https://developers.adobetarget.com/api/recommendations/#section/Postman)</li></ul> | [Utilizzare le API](https://docs.adobe.com/content/help/en/target-learn/recommendations-api-tutorial/recs-api-overview.html) Recommendations nei Tutorials *Adobe Target* |
| Consegna | Recuperate contenuti ottimizzati e personalizzati da [!DNL Target] distribuire a un utente finale. | [Raccolta Postman API Target Delivery](https://developers.adobetarget.com/api/delivery-api/#section/Getting-Started/Postman-Collection) |  |
| Generazione di rapporti | Esporta risultati attività e altri risultati di reporting. | Le API di reporting sono incluse nella raccolta [Postman API di amministrazione di](https://developers.adobetarget.com/api/#admin-postman-collection)Target. |  |
| Profilo | Recuperate e modificate i profili utente memorizzati in  Adobe Target. | [Raccolta Postman API profilo di destinazione](https://developers.adobetarget.com/api/#profiles) |  |

>[!NOTE]
>
>Esistono importanti differenze tra le API [!DNL Target] di amministrazione (comprese le [!DNL Recommendations] API) e le API di [!DNL Target] consegna:
>
>* Le API di amministrazione consentono di configurare vari aspetti di [!DNL Target] cui è possibile configurare anche nell’ [!DNL Target] interfaccia utente. Le API di amministrazione richiedono l&#39;autenticazione.
   >
   >
* Le API di distribuzione consentono di recuperare il contenuto. Le API di consegna non richiedono l&#39;autenticazione.
>
>
Per utilizzare le API [!DNL Target] di amministrazione, è innanzitutto necessario configurare l&#39;autenticazione utilizzando  I/O Adobe. Per ulteriori informazioni, consultate [Configurare l&#39;autenticazione](https://docs.adobe.com/content/help/en/target-learn/tutorials/apis/configure-io-target-integration.html) in *Tutorials* Adobe Target.
