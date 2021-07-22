---
keywords: Panoramica e riferimento
description: Ulteriori informazioni su quando scade un profilo visitatore in [!DNL Adobe Target].
title: Qual è la durata del profilo del visitatore e posso estenderlo?
feature: Tipi di pubblico
exl-id: 70cb5e3b-ed6d-450d-8c6e-f1bfe8d26e54
source-git-commit: c19163020cdcb41a17ea6b65b5b500fadc9c7512
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 45%

---

# Durata del profilo del visitatore

Per impostazione predefinita, un profilo visitatore in [!DNL Adobe Target] scade dopo 14 giorni di inattività del visitatore. La durata del profilo può essere estesa.

[Contatta l’Assistenza clienti o il consulente Adobe](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) di riferimento per estendere la durata del profilo senza costi aggiuntivi. La durata può essere impostata fino a un massimo 90 giorni.

Non è necessario scaricare un nuovo file [!DNL Platform Web SDK] o at.js se il profilo è esteso oltre il valore predefinito.

La data di scadenza non viene reimpostata per i profili esistenti. Se un visitatore precedente non torna per 15 giorni, il suo profilo scade. Se un visitatore precedente torna prima della scadenza originale del profilo, il profilo viene reimpostato sulla durata estesa. Tutti i nuovi profili dei visitatori sono impostati sulla durata di profilo estesa.

Nel seguente scenario, si supponga che uno o entrambi i siti siano implementati con [!DNL Platform Web SDK]. Se entrambi i siti si trovano in un unico codice cliente e un visitatore visita entrambi i siti, il profilo è impostato sulla durata dei profili in qualsiasi sito sia stato visitato per ultimo. Ad esempio, si supponga che la durata del profilo del sito 1 sia di 84 giorni. Il sito 2 ha una durata di 14 giorni. Se il visitatore visita il sito 1 e poi il sito 2, il suo profilo scade dopo 14 giorni di inattività. Se il visitatore visita prima il sito 2 e poi il sito 1, il profilo scade dopo 84 giorni.
