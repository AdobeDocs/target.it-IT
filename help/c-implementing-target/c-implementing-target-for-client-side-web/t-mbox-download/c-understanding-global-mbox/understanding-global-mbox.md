---
keywords: mbox globale;implementa mbox.js;implementa at.js
description: Scopri la mbox globale in  Adobe Target, un nome utilizzato per fare riferimento alla chiamata del singolo server effettuata nella parte superiore di ogni pagina Web nell'implementazione di Target.
title: Cos'è una mbox globale?
feature: at.js
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 83%

---


# Comprendere la mbox globale

Informazioni sulla mbox globale, ossia la singola chiamata del server effettuata nella parte superiore di ogni pagina Web nell’implementazione [!DNL Adobe Target].

Per impostazione predefinita, la mbox globale è denominata `target-global-mbox`. Se necessario, puoi rinominarla per il tuo account.

Ci sono varie differenze tra una mbox normale (non globale) e la mbox globale, tra cui:

| Mbox normale | Mbox globale |
|--- |--- |
| In una mbox normale in genere i contenuti sono racchiusi con un tag `<DIV>`. | La mbox globale è “vuota” e non racchiude alcun contenuto. |
| Il contenuto di una sola attività può essere fornito in una mbox normale. | Il contenuto di più attività può essere fornito in una risposta a una mbox globale. |

Se si forniscono più attività tramite la mbox globale o tramite più mbox normali, [!DNL Target] [determina la priorità](/help/c-activities/priority.md#concept_1780C11FEA57440499F0047DD6900E0F) in base alla quale le attività vengono fornite a una pagina web.

Dati aggiuntivi a livello di pagina possono essere inviati a [!DNL Target] insieme alla mbox globale utilizzando la funzione `targetPageParams`. Questa procedura è simile alla funzionalità del parametro mbox. Per ulteriori informazioni, consulta [Trasmissione di parametri a una mbox globale](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/pass-parameters-to-global-mbox.md#concept_33362A04146C4E3C8E7089B65F38B5E5).
