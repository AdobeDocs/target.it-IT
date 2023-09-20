---
keywords: priorità;generare esperienze;esperienza;pubblico;passare a un’altra esperienza;compositore esperienza visivo
description: Scopri come i visitatori possono passare da un’esperienza all’altra in una [!DNL Adobe Target] [!UICONTROL Targeting esperienza] (XT) man mano che i loro profili evolvono.
title: I visitatori possono cambiare le esperienze in un [!UICONTROL Targeting esperienza] Attività?
feature: Experience Targeting
exl-id: 8d931764-8ba7-4eac-99db-60659086b8be
source-git-commit: 0dfdd995c00961ed2aed91ec03406e8493292af7
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 44%

---

# Passare ad altre esperienze in [!UICONTROL Targeting esperienza]

Con [!UICONTROL Targeting esperienza], puoi controllare quali esperienze i visitatori visualizzano man mano che i loro profili evolvono.

L’elenco seguente presenta solo alcuni scenari in cui i profili dei visitatori possono evolvere e potresti voler presentare contenuti diversi in base a tali modifiche:

| Scenario | Dettagli |
|--- |--- |
| Posizione geografica | Quando un visitatore si sposta per lavoro o per piacere, può accedere al sito web o all’app mobile da posizioni geografiche diverse. |
| Stato del cliente | Il visitatore può essere considerato potenziale cliente prima di creare un account o acquistare un prodotto. |
| Affinità tra categorie | La funzione di [affinità tra categorie](/help/main/c-target/c-visitor-profile/category-affinity.md) funzionalità in [!DNL Target] acquisisce automaticamente le categorie visualizzate dai visitatori e quindi calcola l’affinità dei visitatori per la categoria a scopo di targeting. Ad esempio, ai visitatori che hanno visualizzato diversi articoli sul tuo sito web su un particolare argomento viene presentato un contenuto relativo a tale argomento. |
| Giorno della settimana | All’avvicinarsi del fine settimana, potresti mostrare ai visitatori contenuti su film, ristoranti o altre forme di intrattenimento. |

Per utilizzare queste funzionalità in [!DNL Target], è importante comprendere le seguenti informazioni mentre si lavora con [!UICONTROL Targeting esperienza] attività:

* **La priorità è controllata dall’ordine delle esperienze, dall’alto verso il basso.** Se un visitatore è idoneo per più di due tipi di pubblico, riceve contenuti dall’esperienza con priorità più elevata.
* **I visitatori passano da un’esperienza all’altra in una [!UICONTROL Targeting esperienza] attività se iniziano a qualificarsi per il pubblico di un’esperienza a priorità più elevata.**

  Ad esempio, nella seguente configurazione attività, un visitatore ha visitato il tuo sito web dagli Stati Uniti e poi si è recato in Germania, dove ha visitato il tuo sito web una seconda volta. Durante la prima visita, questo visitatore si è qualificato per l’Esperienza A (visitatori negli Stati Uniti). Dopo aver visitato il tuo sito web dalla Germania, lo stesso visitatore è passato all’Esperienza B (visitatore dalla Germania).

  ![Priorità Stati Uniti > Germania](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_germany-new.png)

* **I visitatori passano da un’esperienza all’altra anche se non si qualificano più per il pubblico corrente ma iniziano a qualificarsi per un’esperienza a priorità inferiore.**
* **Se i visitatori non si qualificano più per la loro esperienza corrente e non si qualificano per un’altra esperienza, visualizzano il contenuto predefinito.**

  Ad esempio, nella seguente configurazione attività, un visitatore ha visitato il tuo sito web dagli Stati Uniti e poi si è recato in Francia, dove ha visitato il tuo sito web una seconda volta. Durante la prima visita, questo visitatore si è qualificato per l’Esperienza A (visitatori negli Stati Uniti). Dopo aver visitato il tuo sito web dalla Francia, questo visitatore rimane nell’esperienza originale.

  ![Priorità Stati Uniti > Germania](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_germany-new.png)

* **Un’esperienza rivolta a &quot;Tutti i visitatori&quot; può essere utilizzata come ultima esperienza nel [!UICONTROL Targeting esperienza] per &quot;catturare&quot; i visitatori che non si sono qualificati per nessun’altra esperienza. Se un’esperienza con targeting per &quot;Tutti i visitatori&quot; non è l’ultima nell’ordine, vengono comunque valutate altre esperienze con targeting elencate in una posizione inferiore a questa esperienza.**

  Ad esempio, nella seguente configurazione attività, un visitatore ha visitato il tuo sito web dagli Stati Uniti e poi si è recato in Germania, dove ha visitato il tuo sito web una seconda volta. Durante la prima visita, questo visitatore si è qualificato per l’Esperienza A (visitatori negli Stati Uniti). Dopo aver visitato il tuo sito web dalla Germania, questo visitatore rimane nell’esperienza A (visitatori dagli Stati Uniti).

  ![Priorità Stati Uniti > Tutti i visitatori](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_all_visitors-new.png)

  Se preferisci evitare questa situazione, puoi creare un nuovo pubblico definito esplicitamente come l’inverso del pubblico di destinazione, come illustrato di seguito:

  ![Priorità Stati Uniti > Non Stati Uniti](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_not_us-new.png)

* **Con una singola esperienza [!UICONTROL Targeting esperienza] attività, i visitatori rimangono in un’esperienza anche se non si qualificano più per il pubblico che li ha portati in tale esperienza.**

  Se preferisci evitare questa situazione, puoi creare un’altra esperienza rivolta al pubblico inverso (per esempio, “Non Stati Uniti” in contrapposizione a “Stati Uniti”).

  In alternativa, puoi creare un’ [!UICONTROL Test A/B] attività mirata al pubblico desiderato con un’allocazione del traffico del 100%, come illustrato di seguito:

  ![Priorità una esperienza](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_one_experience-new.png)

* **[!DNL Target]La priorità delle esperienze è definita dall’ordine (dall’alto verso il basso) in cui vengono visualizzate nell’interfaccia utente di .**

  È un aspetto importante da tenere presente negli scenari in cui un visitatore potrebbe qualificarsi per più di un pubblico. Ad esempio, se hai due esperienze: una rivolta agli &quot;Stati Uniti&quot; e una rivolta a &quot;New York&quot;, un visitatore che si trova a New York si qualifica per entrambi i tipi di pubblico. Pertanto, devi assicurarti che l’esperienza &quot;New York&quot; sia definita prima dell’esperienza &quot;Stati Uniti&quot; in [!DNL Target] UI. Questa pratica assicura che l’esperienza di &quot;New York&quot; più mirata abbia la priorità più elevata, come illustrato nell’esempio seguente:

  ![Priorità New York > Stati Uniti](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_ny_us-new.png)
