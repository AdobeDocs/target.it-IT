---
description: Per impostazione predefinita, i profili dei visitatori vengono memorizzati per 14 giorni. La durata del profilo può essere estesa.
keywords: Panoramica e riferimento
seo-description: Per impostazione predefinita, i profili dei visitatori vengono memorizzati per 14 giorni. La durata del profilo può essere estesa.
seo-title: Durata del profilo del visitatore
solution: Target
subtopic: Introduzione
title: Durata del profilo del visitatore
topic: Standard
uuid: 01ccda60-7e28-4d26-8d5d-1c0a022bbef0
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Durata del profilo del visitatore{#visitor-profile-lifetime}

Per impostazione predefinita, il profilo del visitatore scade dopo 14 giorni di inattività per quel visitatore. La durata del profilo può essere estesa.

[Contatta l’Assistenza clienti o il consulente Adobe](../../cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) di riferimento per estendere la durata del profilo senza costi aggiuntivi. La durata può essere impostata fino a un massimo 90 giorni.

La libreria JavaScript di [!DNL Target] in uso ([!DNL at.js] o [!DNL mbox.js]) determina se è necessario scaricare un nuovo file:

| Libreria di Target | Dettagli |
|--- |--- |
| at.js | Non è necessario scaricare un nuovo file at.js se il profilo è stato esteso oltre il valore predefinito. |
| mbox.js | Se il profilo viene esteso oltre la durata predefinita di 14 giorni, è necessario scaricare un nuovo file mbox.js dopo la modifica delle impostazioni da parte del consulente di riferimento o dell’Assistenza clienti. L’estensione dei cookie per supportare la modifica di durata del profilo è inclusa nel file mbox.js aggiornato. Dopo aver iniziato a utilizzare la nuova libreria, la durata del profilo dei visitatori verrà aggiornata. |

La data di scadenza non viene reimpostata per i profili esistenti. Se un visitatore precedente non torna per 15 giorni, il suo profilo scade. Se un visitatore precedente torna prima della scadenza originale del profilo, il profilo viene reimpostato sulla durata estesa. Tutti i nuovi profili dei visitatori sono impostati sulla durata di profilo estesa.

In presenza di due siti con un unico codice cliente, visitati entrambi dallo stesso visitatore, la durata del profilo sarà pari a quella impostata per il sito visitato per ultimo. Ad esempio, se il sito 1 ha una durata di profilo di 84 giorni e il sito 2 ha una durata di 14 giorni e il visitatore visita il sito 1 e quindi il sito 2, il profilo del visitatore scade dopo 14 giorni di inattività. Se il visitatore visita il sito 1 dopo il sito 2, il profilo scade dopo 84 giorni di inattività.
