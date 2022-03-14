---
keywords: consigli;backup;back up
description: Scopri come utilizzare i consigli di backup in Adobe [!DNL Target] Recommendations. Per i consigli privi di un numero sufficiente di elementi consigliati vengono visualizzati i risultati dell'algoritmo di backup.
title: Come si utilizza un consiglio di backup in Recommendations?
feature: Recommendations
exl-id: 070aa8ef-5691-4106-b5cf-45eb9f6f334c
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 82%

---

# ![PREMIUM](/help/main/assets/premium.png) Utilizzare un consiglio di backup

Se utilizzate la funzione di consiglio di backup in Adobe Target, per i consigli privi di un numero sufficiente di elementi consigliati non verrà visualizzato il contenuto predefinito. Al loro posto saranno visualizzati i risultati dell’algoritmo di backup.

Se non utilizzi un consiglio di backup e per un consiglio non sono presenti elementi sufficienti a popolare completamente la visualizzazione, nel sistema viene visualizzato il contenuto predefinito per l’utente.

>[!NOTE]
>
>Ulteriori informazioni sono incluse nella [Sezione del contenuto dei criteri di creazione](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content) argomento, inclusa una matrice che spiega i risultati che osserverai quando utilizzi il [!UICONTROL Rendering design parziale] e [!UICONTROL Mostra Recommendations di backup] opzioni insieme o separatamente.

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

Se l’opzione Abilita rendering design parziale (consulta [Impostazioni contenuto](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content)) non è abilitata e il modello non viene visualizzato, verrà mostrato invece il consiglio di backup o il contenuto predefinito.
