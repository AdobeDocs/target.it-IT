---
title: Impostare un gruppo di funzioni per il rollout graduale
description: Scopri come configurare un rollout graduale basato su percentuali per un gruppo di funzioni in Flag.
badge: label="Beta" type="Informative"
hide: true
exl-id: fcf187f1-2f33-4e3a-b740-985d5bc0bcdc
source-git-commit: 8fffd619232b2cae2f5dd0aa1e0a55183c4be698
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 3%

---

# Impostare un gruppo di funzioni per il rollout graduale {#gradual-rollout-feature-group}

Il rollout percentuale per un gruppo di funzionalità è configurato nella scheda **Dettagli di base**. Puoi regolare questo valore verso l’alto o verso il basso in qualsiasi momento con l’avanzare del rollout.

## Come funziona {#how-it-works}

Quando imposti un rollout percentuale (ad esempio, 60%), tale percentuale del pubblico definito viene esposta al gruppo di funzioni. Il rollout percentuale è **obbligatorio** e il valore predefinito è **100%** (il gruppo di funzionalità viene distribuito all&#39;intero pubblico corrispondente). Puoi regolarlo in **1% incrementi**. La percentuale rimanente viene inserita nel **gruppo di controllo**, che riceve il comportamento predefinito.

Se hai configurato più varianti (per il test A/B), la percentuale di esposizione viene distribuita equamente tra le varianti. Ad esempio, un’esposizione del 60% con tre varianti risulta del 20% per variante, con il 40% nel gruppo di controllo.

Puoi aumentare o diminuire la percentuale in qualsiasi momento per espandere, ridurre o sospendere il rollout.

## Vedi anche {#see-also}

* [Creare un gruppo di funzioni](create-a-feature-group.md)
* [Test A/B con flag di funzione](a-b-testing.md)
* [Rollout graduale](../../concepts/gradual-rollout.md)

<!-- -->
