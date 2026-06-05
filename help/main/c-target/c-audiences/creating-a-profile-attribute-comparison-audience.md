---
keywords: pubblico;propensione;attributo di profilo;confrontare;confronto;creare pubblico;creazione di pubblico
description: Scopri come definire un pubblico per confrontare due attributi di profilo.
title: È possibile confrontare due attributi di profilo da utilizzare nei tipi di pubblico?
feature: Audiences
exl-id: 033e90f1-5a05-4fce-a520-68826860a908
TQID: https://experienceleague.adobe.com/ri17ME4xHa-HoBjcwOg4fnG7QwIoy2r9Pa3-tB-ECJ8
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: adee20bd-51f4-461d-b9db-d215f8756eebid: c93393a4-e558-47e1-992e-c91ed4d480ce
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 444
ht-degree: 55%

---

# Creare un pubblico per il confronto degli attributi di profilo

Definisci un pubblico in [!DNL Adobe Target] per confrontare due attributi di profilo per la [Libreria tipi di pubblico](/help/main/c-target/c-audiences/audiences.md) o in un [pubblico per sola attività](/help/main/c-target/creating-activity-only-audience.md). L’uso degli operatori, quali maggiore di, minore o uguale a, definisce un pubblico per confrontare in modo dinamico i valori di due attributi di profilo diversi.

>[!NOTE]
>
>Questa funzionalità è disponibile solo per la categoria [[!UICONTROL Profilo visitatore]](/help/main/c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E).

## Panoramica {#section_303CBC78194D49A2A004945D425441E1}

I tipi di pubblico sono definiti da regole che determinano chi è incluso o escluso da un&#39;attività di [!DNL Target]. Una definizione di pubblico può includere più regole e ogni regola può includere più parametri. Se una delle regole incluse utilizza la categoria [!UICONTROL Profilo visitatore], puoi definire una regola in base al valore specifico di un attributo del profilo visitatore o confrontare il valore di tale attributo con un altro attributo del profilo visitatore.

Ad esempio, supponiamo che tu lavori per una società di mobili e abbia caricato due punteggi di tendenza del cliente in [!DNL Target]:

* Probabilità di acquisto di mobili per la sala da pranzo nei prossimi 90 giorni
* Probabilità di acquisto di mobili per il soggiorno nei prossimi 90 giorni

Puoi creare un pubblico la cui propensione ad acquistare mobili per la sala da pranzo è maggiore della propensione ad acquistarne per il soggiorno. [!DNL Target] confronta quindi dinamicamente i punteggi di propensione per la sala da pranzo e il soggiorno per un visitatore specifico per determinare se quel visitatore è idoneo per questo pubblico.

Per ulteriori informazioni, consulta [Metodi per ottenere dati in Target](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=it){target=_blank}.

## Creare un pubblico per il confronto degli attributi di profilo {#section_7A62FD47D5C74C3EBC3417ACDBB85013}

1. Fai clic su **[!UICONTROL Tipi di pubblico]** > **[!UICONTROL Crea pubblico]**.
1. Assegna un nome al pubblico e aggiungi una descrizione facoltativa.
1. Trascina e rilascia **[!UICONTROL Profilo visitatore]** nel riquadro generatore di pubblico.
1. Nell&#39;elenco a discesa **[!UICONTROL Profilo visitatore]**, seleziona un attributo:

   ![Punteggio tendenza 1](assets/propensity_score_1.png)

1. Scegli il tuo valutatore:

   ![Punteggio tendenza 2](assets/propensity_score_2.png)

1. Dall&#39;elenco a discesa **[!UICONTROL Scegli il tipo di confronto]**, scegli **[!UICONTROL Attributo]**.

   Il tipo di confronto &quot;valore statico&quot; consente di confrontare l’attributo del profilo del visitatore con valori specifici.

   ![Punteggio tendenza 3](assets/propensity_score_3.png)

   >[!NOTE]
   >
   >Se utilizzi una delle categorie di profilo visitatore predefinite (ad esempio, Nuovo visitatore o Visitatore di ritorno), puoi scegliere solo l’opzione valore statico. Le opzioni di confronto dinamiche non sono disponibili per le categorie predefinite. Gli altri esempi in cui le opzioni di confronto dinamiche non sono disponibili includono “Prima pagina di sessione”, “Non in altri test”, “Diverso dalla prima pagina di sessione” e “Affinità categoria”.

1. Scegli l&#39;attributo da confrontare con l&#39;attributo iniziale.

   ![immagine propensity_score_4](assets/propensity_score_4.png)

1. Fai clic su **[!UICONTROL Fine]**.

## Video di formazione ![Icona Panoramica](/help/main/assets/overview.png) {#section_3BB8DBF3418F4520B3E274B6F40AF8F3}

Per ulteriori informazioni e uno scenario in cui potresti utilizzare questa funzione, guarda il seguente video:

>[!VIDEO](https://video.tv.adobe.com/v/23218/)
