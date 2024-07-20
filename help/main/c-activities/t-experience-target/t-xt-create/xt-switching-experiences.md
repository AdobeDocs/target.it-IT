---
keywords: priorità;generare esperienze;esperienza;pubblico;passare a un’altra esperienza;compositore esperienza visivo
description: Scopri come i visitatori possono passare da un’esperienza all’altra in un’attività  [!DNL Adobe Target] [!UICONTROL Experience Targeting] (XT) mentre i loro profili evolvono.
title: I visitatori possono cambiare esperienze in un'attività [!UICONTROL Experience Targeting]?
feature: Experience Targeting
exl-id: 8d931764-8ba7-4eac-99db-60659086b8be
source-git-commit: 0dfdd995c00961ed2aed91ec03406e8493292af7
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 43%

---

# Passaggio ad altre esperienze in [!UICONTROL Experience Targeting]

Con [!UICONTROL Experience Targeting], puoi controllare quali esperienze i visitatori visualizzano mentre i loro profili evolvono.

L’elenco seguente presenta solo alcuni scenari in cui i profili dei visitatori possono evolvere e potresti voler presentare contenuti diversi in base a tali modifiche:

| Scenario | Dettagli |
|--- |--- |
| Posizione geografica | Quando un visitatore si sposta per lavoro o per piacere, può accedere al sito web o all’app mobile da posizioni geografiche diverse. |
| Stato del cliente | Il visitatore può essere considerato potenziale cliente prima di creare un account o acquistare un prodotto. |
| Affinità tra categorie | La funzionalità [affinità tra categorie](/help/main/c-target/c-visitor-profile/category-affinity.md) in [!DNL Target] acquisisce automaticamente la visualizzazione delle categorie dei visitatori e quindi calcola l&#39;affinità dei visitatori per la categoria a scopo di targeting. Ad esempio, ai visitatori che hanno visualizzato diversi articoli sul tuo sito web su un particolare argomento viene presentato un contenuto relativo a tale argomento. |
| Giorno della settimana | All’avvicinarsi del fine settimana, potresti mostrare ai visitatori contenuti su film, ristoranti o altre forme di intrattenimento. |

Per utilizzare queste funzionalità in [!DNL Target], è importante comprendere le seguenti informazioni mentre si lavora con [!UICONTROL Experience Targeting] attività:

* **La priorità è controllata dall’ordine delle esperienze, dall’alto verso il basso.** Se un visitatore è idoneo per più di due tipi di pubblico, riceve contenuti dall&#39;esperienza con priorità più elevata.
* **I visitatori passano da un&#39;esperienza all&#39;altra in un&#39;attività [!UICONTROL Experience Targeting] se iniziano a qualificarsi per il pubblico di un&#39;esperienza a priorità più alta.**

  Ad esempio, nella seguente configurazione attività, un visitatore ha visitato il tuo sito web dagli Stati Uniti e poi si è recato in Germania, dove ha visitato il tuo sito web una seconda volta. Durante la prima visita, questo visitatore si è qualificato per l’Esperienza A (visitatori negli Stati Uniti). Dopo aver visitato il tuo sito web dalla Germania, lo stesso visitatore è passato all’Esperienza B (visitatore dalla Germania).

  ![Priorità Stati Uniti > Germania](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_germany-new.png)

* **I visitatori passano da un&#39;esperienza all&#39;altra anche se non si qualificano più per il pubblico corrente ma iniziano a qualificarsi per un&#39;esperienza con priorità inferiore.**
* **Se i visitatori non si qualificano più per la loro esperienza corrente e non si qualificano per un&#39;altra esperienza, visualizzano il contenuto predefinito.**

  Ad esempio, nella seguente configurazione attività, un visitatore ha visitato il tuo sito web dagli Stati Uniti e poi si è recato in Francia, dove ha visitato il tuo sito web una seconda volta. Durante la prima visita, questo visitatore si è qualificato per l’Esperienza A (visitatori negli Stati Uniti). Dopo aver visitato il tuo sito web dalla Francia, questo visitatore rimane nell’esperienza originale.

  ![Priorità Stati Uniti > Germania](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_germany-new.png)

* **Un&#39;esperienza rivolta a &quot;Tutti i visitatori&quot; può essere utilizzata come ultima esperienza nell&#39;attività [!UICONTROL Experience Targeting] per &quot;rilevare&quot; i visitatori che non sono qualificati per nessun&#39;altra esperienza. Se un&#39;esperienza con targeting per &quot;Tutti i visitatori&quot; non è l&#39;ultima dell&#39;ordine, vengono comunque valutate altre esperienze con targeting elencate in una posizione inferiore a questa esperienza.**

  Ad esempio, nella seguente configurazione attività, un visitatore ha visitato il tuo sito web dagli Stati Uniti e poi si è recato in Germania, dove ha visitato il tuo sito web una seconda volta. Durante la prima visita, questo visitatore si è qualificato per l’Esperienza A (visitatori negli Stati Uniti). Dopo aver visitato il tuo sito web dalla Germania, questo visitatore rimane nell’esperienza A (visitatori dagli Stati Uniti).

  ![Priorità Stati Uniti > Tutti i visitatori](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_all_visitors-new.png)

  Se preferisci evitare questa situazione, puoi creare un nuovo pubblico definito esplicitamente come l’inverso del pubblico di destinazione, come illustrato di seguito:

  ![Priorità Stati Uniti > Non Stati Uniti](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_not_us-new.png)

* **Con un&#39;attività [!UICONTROL Experience Targeting] a esperienza singola, i visitatori rimangono in un&#39;esperienza anche se non si qualificano più per il pubblico che li ha portati in tale esperienza.**

  Se preferisci evitare questa situazione, puoi creare un’altra esperienza rivolta al pubblico inverso (per esempio, “Non Stati Uniti” in contrapposizione a “Stati Uniti”).

  In alternativa, puoi creare un&#39;attività [!UICONTROL A/B Test] destinata al pubblico desiderato con un&#39;allocazione del traffico del 100%, come illustrato di seguito:

  ![Priorità una esperienza](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_one_experience-new.png)

* **La priorità delle esperienze è definita dall&#39;ordine (dall&#39;alto verso il basso) in cui vengono visualizzate nell&#39;interfaccia utente di [!DNL Target].**

  È un aspetto importante da tenere presente negli scenari in cui un visitatore potrebbe qualificarsi per più di un pubblico. Ad esempio, se hai due esperienze: una rivolta agli &quot;Stati Uniti&quot; e una rivolta a &quot;New York&quot;, un visitatore che si trova a New York si qualifica per entrambi i tipi di pubblico. Pertanto, devi assicurarti che l&#39;esperienza &quot;New York&quot; sia definita prima dell&#39;esperienza &quot;Stati Uniti&quot; nell&#39;interfaccia utente [!DNL Target]. Questa pratica assicura che l’esperienza di &quot;New York&quot; più mirata abbia la priorità più elevata, come illustrato nell’esempio seguente:

  ![Priorità New York > Stati Uniti](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_ny_us-new.png)
