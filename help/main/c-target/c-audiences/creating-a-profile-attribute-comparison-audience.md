---
keywords: pubblico;propensione;attributo di profilo;confrontare;confronto;creare pubblico;creazione di pubblico
description: Scopri come definire un pubblico per confrontare due attributi di profilo.
title: È possibile confrontare due attributi di profilo da utilizzare nei tipi di pubblico?
feature: Audiences
exl-id: 033e90f1-5a05-4fce-a520-68826860a908
source-git-commit: 1383088bb2f6be0432e6f140400d8723048c8530
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 62%

---

# Creare un pubblico per il confronto degli attributi di profilo

Definire un pubblico in [!DNL Adobe Target] per confrontare due attributi di profilo per [Libreria tipi di pubblico](/help/main/c-target/c-audiences/audiences.md) o in un [pubblico per sola attività](/help/main/c-target/creating-activity-only-audience.md). L’uso degli operatori, quali maggiore di, minore o uguale a, definisce un pubblico per confrontare in modo dinamico i valori di due attributi di profilo diversi.

>[!NOTE]
>
>Questa funzionalità è disponibile solo per la categoria [[!UICONTROL Profilo visitatore]](/help/main/c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E).

## Panoramica {#section_303CBC78194D49A2A004945D425441E1}

I tipi di pubblico sono definiti da regole che determinano chi è incluso o escluso da un&#39;attività di [!DNL Target]. Una definizione di pubblico può includere più regole e ogni regola può includere più parametri. Se una delle regole incluse utilizza [!UICONTROL Profilo visitatore] categoria, puoi definire una regola in base al valore specifico di un attributo del profilo visitatore o confrontare il valore di tale attributo con un altro attributo del profilo visitatore.

Ad esempio, supponiamo che tu lavori per un’azienda di mobili e che in sia stato caricato due punteggi di tendenza dei clienti in [!DNL Target]:

* Probabilità di acquisto di mobili per la sala da pranzo nei prossimi 90 giorni
* Probabilità di acquisto di mobili per il soggiorno nei prossimi 90 giorni

Puoi creare un pubblico la cui propensione ad acquistare mobili per la sala da pranzo è maggiore della propensione ad acquistarne per il soggiorno. [!DNL Target] consente quindi di confrontare in modo dinamico il punteggio della propensione per la sala da pranzo e il soggiorno per un visitatore specifico per determinare se tale visitatore è destinato a questo pubblico.

Per ulteriori informazioni, consulta [Metodi per ottenere dati in Target](https://experienceleague.corp.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=it){target=_blank}.

## Creare un pubblico per il confronto degli attributi di profilo {#section_7A62FD47D5C74C3EBC3417ACDBB85013}

1. Clic **[!UICONTROL Tipi di pubblico]** > **[!UICONTROL Crea pubblico]**.
1. Assegna un nome al pubblico e aggiungi una descrizione facoltativa.
1. Trascina **[!UICONTROL Profilo visitatore]** nel riquadro audience builder.
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

## Video di formazione ![Badge panoramica](/help/main/assets/overview.png) {#section_3BB8DBF3418F4520B3E274B6F40AF8F3}

Per ulteriori informazioni e uno scenario in cui potresti utilizzare questa funzione, guarda il seguente video:

>[!VIDEO](https://video.tv.adobe.com/v/23218/)
