---
keywords: consigli;backup;back up
description: Scopri come utilizzare i consigli di backup in Adobe [!DNL Target Recommendations].
title: Utilizzare un consiglio di backup
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Recommendations
exl-id: 070aa8ef-5691-4106-b5cf-45eb9f6f334c
TQID: 'https://experienceleague.adobe.com/TziWJoAuEdCqa7uMTpX0O0InnlnjtbPXP-0wzQ-FCM0'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: e8a9b6be04169ea3024673babb62085667fe8990
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 18%
---
# Utilizzare un consiglio di backup {#backup-recommendations}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come i consigli di backup riempiono gli slot rimanenti di una progettazione in [!DNL Adobe Target Recommendations].

>[!ENDSHADEBOX]

Quando un consiglio non dispone di un numero sufficiente di elementi consigliati per riempire la progettazione, la funzionalità di consiglio di backup in [!DNL Adobe Target] visualizza i risultati dell&#39;algoritmo di backup anziché il contenuto predefinito. Senza un consiglio di backup, il sistema visualizza il contenuto predefinito all’utente.

>[!NOTE]
>
>Per ulteriori informazioni, inclusa una matrice che spiega i risultati dell&#39;utilizzo delle opzioni **[!UICONTROL Rendering design parziale]** e **[!UICONTROL Mostra contenuto di backup]** insieme o separatamente, vedere la sezione [Contenuto di backup dei criteri di creazione](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content).

La funzione di consigli di backup utilizza sempre gli elementi visualizzati in alto sul sito per riempire eventuali slot rimanenti dopo l’utilizzo dei dati dell’algoritmo. Ad esempio, una progettazione è configurata per mostrare cinque elementi consigliati, ma l’algoritmo dispone di dati sufficienti per riempire solo due dei cinque slot. La funzione di consiglio di backup riempie gli altri tre slot con gli elementi visualizzati in alto.

I consigli di backup vengono selezionati in modo casuale tra i 500 prodotti più visualizzati in tutto il sito. I dati raccolti per i consigli di backup coprono una settimana.

I 500 risultati più visualizzati vengono ordinati sequenzialmente e poi suddivisi in bucket di 20. I bucket vengono serviti in ordine, ma i risultati all’interno di ogni bucket vengono randomizzati e restituiti alla pagina, in modo che gli utenti che aggiornano la pagina ricevano nuovi risultati randomizzati. Se il set di risultati dall’unione della raccolta e le regole di filtro sono inferiori a 20, gli elementi vengono selezionati in modo casuale dalla raccolta.

Grazie a questo processo di suddivisione in bucket, i consigli di backup vengono visualizzati nell’ordine seguente:

1. I 20 elementi più visualizzati, randomizzati.
1. I successivi 20 elementi più visualizzati, randomizzati.
1. I successivi 20 elementi più visualizzati, randomizzati e così via.

Senza bucket, è possibile visualizzare il 499esimo elemento più visualizzato, seguito dal 200esimo, dal 380esimo e così via. Il bucket assicura che gli articoli più visualizzati siano consigliati per primi.

Se gli elementi sono raggruppati in raccolte, anche i consigli di backup generati per ciascun criterio utilizzano la raccolta, in modo da includere nel consiglio di backup solo gli elementi della raccolta. Gli articoli esclusi dalle regole di esclusione globali non vengono distribuiti come consigli di backup. I duplicati vengono rimossi dai blocchi di consigli.

I consigli di backup sono abilitati per impostazione predefinita e riempiono gli slot aggiuntivi in una progettazione con una selezione casuale degli elementi più popolari sul sito.

L’utilizzo dei consigli di backup solitamente fa parte della discussione con il team di implementazione durante la configurazione iniziale. Per modificare l’impostazione dei consigli di backup dopo l’implementazione, contatta l’account manager.

Quando **[!UICONTROL Rendering design parziale]** (vedi [Contenuto backup](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content)) non è abilitato e la progettazione non può essere riempita, vengono visualizzati i consigli di backup (se abilitati) o il contenuto predefinito.
