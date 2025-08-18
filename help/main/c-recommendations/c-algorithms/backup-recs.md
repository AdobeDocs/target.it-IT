---
keywords: consigli;backup;back up
description: Scopri come utilizzare i consigli di backup in Adobe [!DNL Target Recommendations].
title: Come si utilizza un consiglio di backup in [!DNL Target Recommendations]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: 070aa8ef-5691-4106-b5cf-45eb9f6f334c
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 70%

---

# Utilizzare un consiglio di backup

Se si utilizza la funzione di consiglio di backup in [!DNL Adobe Target], per i consigli privi di un numero sufficiente di elementi consigliati non viene visualizzato il contenuto predefinito. Al loro posto saranno visualizzati i risultati dell’algoritmo di backup.

Se non utilizzi un consiglio di backup e per un consiglio non sono presenti elementi sufficienti a popolare completamente la visualizzazione, nel sistema viene visualizzato il contenuto predefinito per l’utente.

>[!NOTE]
>
>Ulteriori informazioni sono incluse nella sezione [Content dell&#39;argomento Create criteria](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content), inclusa una matrice che spiega i risultati che si osserveranno quando si utilizzano le opzioni [!UICONTROL Partial Design Rendering] e [!UICONTROL Show Backup Recommendations] insieme o separatamente.

La funzione di consigli di backup utilizza sempre gli elementi visualizzati in alto sul sito per riempire eventuali slot rimanenti dopo l’utilizzo dei dati dell’algoritmo. Ad esempio, supponi che il modello sia configurato per mostrare cinque elementi consigliati e che sia in uso l’algoritmo *Affinità di acquisto*. Se tuttavia i dati sono sufficienti solo per popolare due spazi su cinque, la funzione di consiglio di backup popola gli altri tre con gli elementi più visualizzati.

I consigli di backup vengono selezionati in modo casuale tra i 500 prodotti più visualizzati in tutto il sito. I dati raccolti per i consigli di backup coprono una settimana.

I 500 risultati più visualizzati vengono ordinati sequenzialmente e poi divisi in blocchi di 20. I blocchi vengono forniti in ordine, ma i risultati all’interno di ogni blocco sono randomizzati e restituiti alla pagina. Se gli utenti aggiornano la pagina, vengono presentati risultati nuovi e randomizzati. Se il set di risultati dall’unione della raccolta e le regole di filtro sono inferiori a 20, viene selezionato in modo casuale dalla raccolta.

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

Se Abilita rendering design parziale (vedi [Impostazioni contenuto](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content)) non è abilitato e il modello non viene visualizzato, verrà visualizzato il consiglio di backup o il contenuto predefinito.
