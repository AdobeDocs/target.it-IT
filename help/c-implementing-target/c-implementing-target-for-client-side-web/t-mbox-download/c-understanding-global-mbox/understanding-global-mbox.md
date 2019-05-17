---
description: Informazioni sulla mbox globale, ossia la singola chiamata del server effettuata nella parte superiore di ogni pagina Web nell’implementazione Target.
keywords: mbox globale;implementa mbox.js;implementa at.js
seo-description: Informazioni sulla mbox globale, ossia la singola chiamata del server effettuata nella parte superiore di ogni pagina Web nell’implementazione Target.
seo-title: Comprendere la mbox globale
solution: Target
subtopic: Introduzione
title: Comprendere la mbox globale
topic: Standard
uuid: d8f48c94-6487-437b-828f-f9be7da58f48
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Comprendere la mbox globale{#understand-the-global-mbox}

Informazioni sulla mbox globale, ossia la singola chiamata del server effettuata nella parte superiore di ogni pagina Web nell’implementazione Target.

Per impostazione predefinita, la mbox globale è denominata [!DNL target-global-mbox]. Se necessario, puoi rinominarla per il tuo account.

Ci sono varie differenze tra una mbox normale (non globale) e la mbox globale, tra cui:

| Mbox normale | Mbox globale |
|--- |--- |
| In una mbox normale in genere i contenuti sono racchiusi con un tag `<DIV>`. | La mbox globale è “vuota” e non racchiude alcun contenuto. |
| Il contenuto di una sola attività può essere fornito in una mbox normale. | Il contenuto di più attività può essere fornito in una risposta a una mbox globale. |

Se si forniscono più attività tramite la mbox globale o tramite più mbox normali, [!DNL Target] [determina la priorità](../../../../c-activities/priority.md#concept_1780C11FEA57440499F0047DD6900E0F) in base alla quale le attività vengono fornite a una pagina web.

Dati aggiuntivi a livello di pagina possono essere inviati a [!DNL Target] insieme alla mbox globale utilizzando la funzione `targetPageParams`. Questa procedura è simile alla funzionalità del parametro mbox. Per ulteriori informazioni, consulta [Trasmissione di parametri a una mbox globale](../../../../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/pass-parameters-to-global-mbox.md#concept_33362A04146C4E3C8E7089B65F38B5E5).
