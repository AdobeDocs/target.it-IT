---
keywords: Panoramica e riferimento
description: Per impostazione predefinita, i profili dei visitatori vengono memorizzati per 14 giorni. La durata del profilo può essere estesa.
title: Durata del profilo del visitatore
feature: Audiences
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 83%

---


# Durata del profilo del visitatore{#visitor-profile-lifetime}

Per impostazione predefinita, un profilo visitatore scade dopo 14 giorni di inattività del visitatore. La durata del profilo può essere estesa.

[Contatta l’Assistenza clienti o il consulente Adobe](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) di riferimento per estendere la durata del profilo senza costi aggiuntivi. La durata può essere impostata fino a un massimo 90 giorni.

La libreria JavaScript di [!DNL Target] in uso ([!DNL at.js] o [!DNL mbox.js]) determina se è necessario scaricare un nuovo file:

| Libreria di Target | Dettagli |
|--- |--- |
| at.js | Non è necessario scaricare un nuovo file at.js se il profilo è stato esteso oltre il valore predefinito. |
| mbox.js | Se il profilo viene esteso oltre la durata predefinita di 14 giorni, è necessario scaricare un nuovo file mbox.js dopo la modifica delle impostazioni da parte del consulente di riferimento o dell’Assistenza clienti. L’estensione dei cookie per supportare la modifica di durata del profilo è inclusa nel file mbox.js aggiornato. Dopo aver iniziato a utilizzare la nuova libreria, la durata del profilo dei visitatori verrà aggiornata. |

La data di scadenza non viene reimpostata per i profili esistenti. Se un visitatore precedente non torna per 15 giorni, il suo profilo scade. Se un visitatore precedente torna prima della scadenza originale del profilo, il profilo viene reimpostato sulla durata estesa. Tutti i nuovi profili dei visitatori sono impostati sulla durata di profilo estesa.

Nello scenario seguente, si supponga che uno o entrambi i siti siano implementati con mbox.js, che richiede un aggiornamento del codice dopo l&#39;aggiornamento del profilo. Se entrambi i siti si trovano sotto un unico codice client e un visitatore visita entrambi i siti, il profilo è impostato sulla durata dei profili in qualsiasi sito sia stato visitato per ultimo. Ad esempio, se la durata del profilo del sito 1 è di 84 giorni e quella del sito 2 è di 14 giorni, e un visitatore visita prima il sito 1 e poi il sito 2, il suo profilo scadrà dopo 14 giorni. Se il visitatore visita prima il sito 2 e poi il sito 1, il profilo scade dopo 84 giorni.
