---
keywords: inserire nell'elenco Consentiti;offerta remota;amministrazione;pattern URL;convalida;attività;offerte;carattere jolly;regex
description: Scopri come visualizzare, cercare, aggiungere ed eliminare URL inseriti nell'elenco Consentiti per le offerte remote nella sezione Amministrazione di Adobe Target, incluso il comportamento di convalida e l’ambito a livello di account.
title: Gestire gli URL inseriti nell'elenco Consentiti delle offerte remote
feature: Administration & Configuration
topic: Implementation
role: Admin
level: Intermediate
solution: Target
product: Target
source-git-commit: 882c91244e5dae0977c8a6a1e5878525f497a720
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---

# URL INSERITI NELL&#39;ELENCO CONSENTITI

Gli URL inseriti nell&#39;elenco Consentiti definiscono pattern di URL affidabili in cui l&#39;organizzazione può creare ed eseguire [!DNL Adobe Target] esperienze, anche quando si utilizzano offerte remote o di reindirizzamento. L&#39;elenco funziona insieme alla [gestione host](/help/main/administrating-target/hosts.md) e agli [ambienti](/help/main/administrating-target/environments.md), ma si applica in modo specifico ai modelli di URL di offerta remota consentiti e alle convalide correlate.

Per gestire gli URL inseriti nell&#39;elenco Consentiti, fare clic su **[!UICONTROL Administration]** > **[!UICONTROL Allowlisted URLs]**.

![Pagina URL Inseriti nell&#39;elenco Consentiti con elenco URL, campo di ricerca e controllo Aggiungi URL](../administrating-target/assets/allowlist-1.png)

## Gestire gli URL inseriti nell&#39;elenco Consentiti {#add-url}

La tabella principale elenca ogni pattern inserito nell&#39;elenco Consentiti in una singola colonna. Le voci supportate possono includere URL esatti, percorsi con caratteri jolly o formati di pattern accettati dalla tua organizzazione per le esperienze remote.

1. Fare clic su **[!UICONTROL Add URL]**.

   ![](../administrating-target/assets/allowlist-2.png)

1. Nella finestra di dialogo, immetti l’URL o il modello consentito dalla tua organizzazione.

   ![](../administrating-target/assets/allowlist-3.png)

1. Salva le modifiche.

   Dopo aver inserito nell&#39;elenco Consentiti il modello, gli utenti possono creare o eseguire attività e offerte che si basano su tale URL, in base alle altre regole di [!DNL Target].

1. Utilizzare il campo **[!UICONTROL Search URLs]** per filtrare la tabella.

1. Per eliminare un URL, individua la riga del pattern non più necessario e fai clic sull&#39;icona ![Elimina](../administrating-target/assets/do-not-localize/Smock_Delete_18_N.svg).

   ![](../administrating-target/assets/allowlist-4.png)


