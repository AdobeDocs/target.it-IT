---
keywords: Panoramica e riferimento
description: Ulteriori informazioni sulla scadenza di un profilo visitatore (per impostazione predefinita, 14 giorni) in Adobe Target. La durata del profilo può essere estesa contattando l’Assistenza clienti di Adobe.
title: Qual è la durata del profilo del visitatore e posso estenderlo?
feature: Tipi di pubblico
exl-id: 70cb5e3b-ed6d-450d-8c6e-f1bfe8d26e54
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 73%

---

# Durata del profilo del visitatore

Per impostazione predefinita, un profilo visitatore scade dopo 14 giorni di inattività del visitatore. La durata del profilo può essere estesa.

[Contatta l’Assistenza clienti o il consulente Adobe](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) di riferimento per estendere la durata del profilo senza costi aggiuntivi. La durata può essere impostata fino a un massimo 90 giorni.

La libreria JavaScript di [!DNL Target] in uso ([!DNL at.js] o [!DNL mbox.js]) determina se è necessario scaricare un nuovo file:

| Libreria di Target | Dettagli |
|--- |--- |
| at.js | Non è necessario scaricare un nuovo file at.js se il profilo è stato esteso oltre il valore predefinito. |
| mbox.js | Se il profilo viene esteso oltre la durata predefinita di 14 giorni, è necessario scaricare un nuovo file mbox.js dopo la modifica delle impostazioni da parte del consulente di riferimento o dell’Assistenza clienti. L’estensione dei cookie per supportare la modifica di durata del profilo è inclusa nel file mbox.js aggiornato. Dopo aver iniziato a utilizzare la nuova libreria, la durata del profilo dei visitatori verrà aggiornata. |

La data di scadenza non viene reimpostata per i profili esistenti. Se un visitatore precedente non torna per 15 giorni, il suo profilo scade. Se un visitatore precedente torna prima della scadenza originale del profilo, il profilo viene reimpostato sulla durata estesa. Tutti i nuovi profili dei visitatori sono impostati sulla durata di profilo estesa.

Nel seguente scenario, si supponga che uno o entrambi i siti siano implementati con mbox.js, che richiede un aggiornamento del codice dopo l’aggiornamento del profilo. Se entrambi i siti si trovano in un unico codice cliente e un visitatore visita entrambi i siti, il profilo è impostato sulla durata dei profili in qualsiasi sito sia stato visitato per ultimo. Ad esempio, se la durata del profilo del sito 1 è di 84 giorni e quella del sito 2 è di 14 giorni, e un visitatore visita prima il sito 1 e poi il sito 2, il suo profilo scadrà dopo 14 giorni. Se il visitatore visita prima il sito 2 e poi il sito 1, il profilo scade dopo 84 giorni.
