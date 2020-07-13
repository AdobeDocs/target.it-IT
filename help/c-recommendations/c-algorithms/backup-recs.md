---
keywords: recommendation;backup;back up
description: Se utilizzi la funzione di consiglio di backup, per i consigli privi di un numero sufficiente di elementi consigliati non saranno visualizzati i contenuti predefiniti. Al loro posto saranno visualizzati i risultati dell’algoritmo di backup.
title: Utilizzare un consiglio di backup
uuid: 2910a844-9dd6-4e69-8652-b2215fed1545
translation-type: tm+mt
source-git-commit: 32217a752574f671b790880667ac869443778f51
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 100%

---


# ![PREMIUM](/help/assets/premium.png) Utilizzare un consiglio di backup{#use-a-backup-recommendation}

Se utilizzi la funzione di consiglio di backup, per i consigli privi di un numero sufficiente di elementi consigliati non saranno visualizzati i contenuti predefiniti. Al loro posto saranno visualizzati i risultati dell’algoritmo di backup.

Se non utilizzi un consiglio di backup e per un consiglio non sono presenti elementi sufficienti a popolare completamente la visualizzazione, nel sistema viene visualizzato il contenuto predefinito per l’utente.

La funzionalità di consiglio di backup utilizza sempre gli elementi più visualizzati sul sito per popolare gli spazi rimanenti dopo l’utilizzo dei dati dell’algoritmo. Ad esempio, supponi che il modello sia configurato per mostrare cinque elementi consigliati e che sia in uso l’algoritmo *Affinità di acquisto*. Se tuttavia i dati sono sufficienti solo per popolare due spazi su cinque, la funzione di consiglio di backup popola gli altri tre con gli elementi più visualizzati.

I consigli di backup vengono selezionati in modo casuale tra i 500 prodotti più visualizzati in tutto il sito. I dati raccolti per i consigli di backup coprono una settimana.

I 500 risultati più visualizzati vengono ordinati sequenzialmente e poi divisi in blocchi di 20. I blocchi vengono forniti in ordine, ma i risultati all’interno di ogni blocco sono randomizzati e restituiti alla pagina. Se gli utenti aggiornano la pagina, vengono presentati risultati nuovi e randomizzati. Se l’insieme di risultati dell’unione di raccolta e regole di filtro è minore di 20, verrà selezionato in modo casuale dalla raccolta.

Questo processo di divisione in blocchi determina che i consigli di backup vengano visualizzati nell’ordine seguente:

1. Mostra i 20 elementi più visualizzati, randomizzati, quindi
1. Mostra i successivi 20 elementi più visualizzati, randomizzati, quindi
1. Mostra i successivi 20 elementi più visualizzati, randomizzati,
1. E così via

Senza la divisione in blocchi dei consigli di backup, il primo consiglio presentato potrebbe essere ad esempio il 499° elemento più visualizzato, seguito dal 200°, dal 380° e così via. Grazie al processo di divisione in blocchi, invece, gli articoli più visualizzati vengono consigliati per primi.

>[!NOTE]
>
>Se raggruppi gli articoli in cataloghi, anche i consigli di backup generati per ogni algoritmo all’interno dei consigli utilizzano questo catalogo; di conseguenza, nei consigli di backup vengono inclusi solo gli articoli del catalogo.

Gli articoli esclusi dalle regole di esclusione globali non vengono distribuiti come consigli di backup.

I consigli di backup sono abilitati per impostazione predefinita e popolano gli spazi aggiuntivi in un modello con una selezione casuale degli articoli più popolari sul sito.

I duplicati vengono rimossi dai blocchi di consigli.

L’utilizzo dei consigli di backup viene di solito discusso con il team di implementazione durante la configurazione iniziale. Se desideri modificare l’impostazione relativa ai consigli di backup dopo l’implementazione, contatta il tuo Account Manager.

Se l’opzione Abilita rendering design parziale (consulta [Impostazioni contenuto](../../c-recommendations/c-algorithms/create-new-algorithm.md#concept_BC16005C7A1E4F1A87E33D16221F4A96)) non è abilitata e il modello non viene visualizzato, verrà mostrato invece il consiglio di backup o il contenuto predefinito.
