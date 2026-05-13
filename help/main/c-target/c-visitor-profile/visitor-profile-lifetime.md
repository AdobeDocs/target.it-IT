---
keywords: Panoramica e riferimento
description: Ulteriori informazioni su quando scade un profilo visitatore in [!DNL Adobe Target].
title: Qual è la durata del profilo del visitatore e posso estenderlo?
feature: Audiences
exl-id: 70cb5e3b-ed6d-450d-8c6e-f1bfe8d26e54
TQID: https://experienceleague.adobe.com/yMfacKgQthOmpfhFiuO-jGGPWZh5VrliOSi0TQ-uis0
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 147
ht-degree: 62%

---

# Durata del profilo del visitatore

Per impostazione predefinita, un profilo visitatore in [!DNL Adobe Target] scade dopo 14 giorni di inattività del visitatore. La durata del profilo può essere estesa.

[Contatta l’Assistenza clienti o il consulente Adobe](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) di riferimento per estendere la durata del profilo senza costi aggiuntivi. La durata può essere impostata fino a un massimo 90 giorni.

Non è necessario scaricare un nuovo file [!DNL Platform Web SDK] o at.js se il profilo è stato esteso oltre il valore predefinito.

La data di scadenza non viene reimpostata per i profili esistenti. Se un visitatore precedente non torna per 15 giorni, il suo profilo scade. Se un visitatore precedente torna prima della scadenza originale del profilo, il profilo viene reimpostato sulla durata estesa. Tutti i nuovi profili dei visitatori sono impostati sulla durata di profilo estesa.
