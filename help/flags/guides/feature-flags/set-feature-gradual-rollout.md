---
title: Impostare una funzione per il rollout graduale
description: Scopri come configurare un rollout graduale basato su percentuali per un flag di funzione in Flag.
badge: label="Beta" type="Informative"
hide: true
exl-id: 1e03c533-398d-4a83-9f4a-c0419828b460
source-git-commit: 8fffd619232b2cae2f5dd0aa1e0a55183c4be698
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 3%

---

# Impostare una funzione per il rollout graduale {#gradual-rollout-feature}

Il rollout percentuale per un flag di funzionalità è configurato nella scheda **Dettagli di base**. Puoi regolare questo valore verso l’alto o verso il basso in qualsiasi momento con l’avanzare del rollout.

## Come funziona {#how-it-works}

Quando imposti un rollout percentuale (ad esempio, 25%), tale percentuale del pubblico definito viene esposta alla funzione. La percentuale di rollout è **obbligatoria** e il valore predefinito è **100%** (la funzionalità viene fornita all&#39;intero pubblico corrispondente). Puoi regolarlo in **1% incrementi**. La percentuale rimanente viene inserita nel **gruppo di controllo**, che riceve l&#39;esperienza predefinita.

Puoi aumentare o diminuire la percentuale nel tempo per espandere o contrarre il rollout. Se si riduce la percentuale allo 0%, la funzione viene disattivata per tutti gli utenti del pubblico senza eliminare il flag.

## Vedi anche {#see-also}

* [Rollout graduale](../../concepts/gradual-rollout.md)
* [Impostare un gruppo di funzioni per il rollout graduale](set-feature-group-gradual-rollout.md)
* [Creare il primo flag di funzione](create-your-first-feature-flag.md)

<!-- -->
