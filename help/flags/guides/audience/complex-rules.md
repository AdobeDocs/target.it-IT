---
title: Regole di pubblico complesse
description: Scopri come utilizzare nei flag set di regole per il pubblico complessi o di grandi dimensioni, inclusi i limiti per i valori in blocco e come suddividere le regole in più condizioni.
hide: true
exl-id: 37e037b6-45eb-4261-b580-30d94d8e55da
source-git-commit: eeba7af62ab101e687852ce993a001832ce4a83b
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 2%

---

# Regole di pubblico complesse {#complex-rules}

## Utilizzo della logica nidificata per le regole complesse {#nested-logic}

La logica nidificata consente di combinare più condizioni di pubblico con un controllo AND/OR preciso. Per abilitarlo:

1. Aggiungi le condizioni di pubblico necessarie.
2. Abilita **Logica annidata** nella sezione Regole pubblico.
3. A ogni condizione viene assegnato un numero. Immetti un’espressione logica che faccia riferimento a questi numeri, ad esempio:
   * `1 and (2 or 3)`
   * `(1 and 2) or 3`
   * `(1 and 2) or (3 and 4)`

## Vedi anche {#see-also}

* [Pubblico nei flag di funzione e nei gruppi di funzioni](audience-in-feature-flags-and-feature-groups.md)

<!-- -->
