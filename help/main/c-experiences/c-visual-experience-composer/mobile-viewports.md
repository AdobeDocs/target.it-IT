---
keywords: reattivo;riquadri di visualizzazione mobili;riquadro di visualizzazione;dispositivi;dispositivi mobili;responsive web design;rwd
description: I riquadri di visualizzazione mobili consentono di visualizzare l'aspetto delle attività di Adobe [!DNL Target] in Screens di varie dimensioni. Puoi trovare un elenco delle dimensioni e risoluzioni dei riquadri di visualizzazione dei dispositivi più diffusi.
title: Come posso utilizzare i riquadri di visualizzazione mobili per esperienze reattive?
feature: Visual Experience Composer (VEC)
exl-id: 1062e7a1-10b4-4746-bce9-67017978578d
TQID: 'https://experienceleague.adobe.com/uBJtaoaCh28mRGwc-SlK-XhU6sOIK3RaT58-ZXxSsHw'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '1126'
ht-degree: 19%
---
# Riquadri di visualizzazione mobile per esperienze reattive {#mobile-viewports}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come configurare i riquadri di visualizzazione mobili e utilizzarli per visualizzare in anteprima e creare esperienze per schermi di varie dimensioni.

>[!ENDSHADEBOX]

I riquadri di visualizzazione mobili visualizzano [!DNL Adobe Target] attività alle dimensioni dello schermo di vari dispositivi. Sono progettati per i siti dinamici, che si adattano automaticamente a desktop, notebook, tablet e telefoni cellulari e consentono di verificare che un’esperienza sia efficace su ciascuno di essi.

>[!NOTE]
>
> * Utilizza i riquadri di visualizzazione mobili quando il sito è reattivo e la pagina mobile riutilizza gli elementi della pagina desktop in un layout diverso. Quando il sito mobile è separato e ha una propria struttura, ad esempio `m.mysite.com`, utilizza invece un&#39;[attività multipagina](/help/main/c-experiences/c-visual-experience-composer/multipage-activity.md#multipage-activity).
>
>* I riquadri di visualizzazione per dispositivi mobili non sono disponibili quando una sovrapposizione di offerta di reindirizzamento li sovrappone.

## Riquadri di visualizzazione e punti di interruzione CSS

Un riquadro di visualizzazione è l&#39;area dello schermo occupata da una pagina Web: le dimensioni della finestra del browser, meno le barre di scorrimento e le barre degli strumenti. I browser lo misurano in pixel CSS, quindi su molti dispositivi, come quelli con schermi retina, il riquadro di visualizzazione è più piccolo della risoluzione del dispositivo pubblicizzato. Utilizzare sempre le dimensioni del riquadro di visualizzazione in [!DNL Target]. Nella tabella seguente sono elencati entrambi i valori per i dispositivi più diffusi.

+++ Riquadri di visualizzazione e risoluzioni dei dispositivi più diffusi

>[!NOTE]
>
>Ci sono vari siti web che elencano le misure del riquadro di visualizzazione dei dispositivi più popolari. Ad esempio, vedi `https://viewportsizer.com/devices/`. Consulta il sito web del produttore del dispositivo per informazioni più precise e aggiornate.
>
>Dimensioni dei riquadri di visualizzazione contrassegnate con &quot;est&quot;. sono stime.

| Dispositivo | Dimensioni del riquadro di visualizzazione (larghezza x altezza) | Risoluzione del dispositivo (larghezza x altezza) |
|---|---|---|
| iPhone 18 Pro Max | 440 x 956 | 1320 x 2868 |
| iPhone 18 Pro | 402 x 874 | 1206 x 2622 |
| iPhone 17 Pro Max | 440 x 956 | 1320 x 2868 |
| iPhone 17 Pro | 402 x 874 | 1206 x 2622 |
| iPhone Air | 420 x 912 | 1260 x 2736 |
| iPhone 17 | 402 x 874 | 1206 x 2622 |
| iPhone 16e | 390 x 844 | 1170 x 2532 |
| iPad (A16) | 820 x 1180 | 1640 x 2360 |
| iPad mini (A17 Pro) | 744 x 1133 | 1488 x 2266 |
| iPad Air 11″ (M3 / M4) | 820 x 1180 | 1640 x 2360 |
| iPad Pro 11″ (M5) | 834 x 1210 | 1668 x 2420 |
| Google Pixel 11 | 412 x 924 (est) | 1080 x 2424 |
| Google Pixel 11 Pro | 410 x 914 (est.) | 1280 x 2856 |
| Google Pixel 11 Pro XL | 448 x 997 (est) | 1344 x 2992 |
| Google Pixel 10 | 412 x 924 | 1080 x 2424 |
| Google Pixel 10 Pro | 410 x 914 (est.) | 1280 x 2856 |
| Google Pixel 10 Pro XL | 448 x 997 (est) | 1344 x 2992 |
| Samsung Galaxy S26 | 360 x 780 | 1080 x 2340 |
| Samsung Galaxy S26 Ultra | 412 x 891 | 1440 x 3120 |
| iPhone Duo (aperto) | 890 x 626 (versione standard) | 2670 x 1878 |
| iPhone Duo (piegato) | 466 x 678 (versione standard) | 1398 x 2034 |
| Samsung Galaxy Z Piega 7 (piegato) | 412 x 960 (versione standard) | 1080 x 2520 |
| Samsung Galaxy Z Flip 8 | 360 x 840 (est) | 1080 x 2520 |
| Pixel Google 11 Pro Fold (aperto) | 791 x 820 (est) | 2076 x 2152 |

+++

Un sito reattivo passa a un layout diverso per schermi di dimensioni specifiche. Queste dimensioni sono denominate punti di interruzione CSS o [query multimediali](https://developer.mozilla.org/es/docs/Web/CSS/Media_Queries/Using_media_queries). Il salvataggio dei punti di interruzione CSS del sito in [!DNL Target] consente di visualizzare in anteprima ogni visualizzazione e facendo clic su un riquadro di visualizzazione nella parte superiore della visualizzazione si apre la visualizzazione corrispondente alla dimensione dello schermo.

Per distribuire un&#39;attività a un determinato dispositivo, seleziona il pubblico per tale dispositivo nel diagramma attività, quindi modifica la pagina per tale dispositivo nel Compositore web per dispositivi mobili. Lo stesso strumento viene utilizzato per visualizzare un sito che non risponde quando l’attività è destinata a un dispositivo specifico. Per eseguire un’attività su tutti i dispositivi, non applicare alcun targeting e visualizzare in anteprima l’attività su ogni dimensione di schermo con i riquadri di visualizzazione mobili.

>[!IMPORTANT]
>
>Le esperienze possono essere modificate dall&#39;interno dei riquadri di visualizzazione mobili, ma le modifiche si applicano a tutti i riquadri e dispositivi, non solo a quello in uso. Allo stesso modo, la modifica di un’esperienza nella vista desktop cambia la pagina per tutte le dimensioni di schermo. [!DNL Target] non supporta attualmente le modifiche di pagina specifiche per i riquadri di visualizzazione.

## Configurazione di riquadri di visualizzazione mobili {#task_B4B161499DC0470584ED922A4D20FCAB}

Definisci i riquadri di visualizzazione mobili disponibili durante la creazione di esperienze.

1. Fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Compositore esperienza visivo]**.
1. Nella sezione **[!UICONTROL Configurazione riquadri di visualizzazione mobili]**, fai clic su **[!UICONTROL Aggiungi]**.

   ![Aggiunta di un riquadro di visualizzazione](/help/main/c-experiences/c-visual-experience-composer/assets/viewpoert_add.png)

   Oppure

   Per modificare la configurazione di un riquadro di visualizzazione mobile esistente, selezionare tale riquadro, quindi fare clic sull&#39;icona **[!UICONTROL Modifica]** (matita).

1. Digita un nome descrittivo per il riquadro di visualizzazione mobile. Il nome può essere lungo fino a 36 caratteri.
1. Inserisci le dimensioni dello schermo del dispositivo mobile. La larghezza può essere compresa tra 150 e 968 pixel e l&#39;altezza tra 150 e 1280 pixel.
1. (Facoltativo) Seleziona il sistema operativo del dispositivo.

   Opzioni:

   * Android
   * iOS
   * Windows
   * Symbian
   * BlackBerry

   Se il [Compositore esperienza avanzato](/help/main/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#enable-eec) è abilitato e viene selezionato un sistema operativo, [!DNL Target] emula tale dispositivo quando viene visualizzata la pagina. Ad esempio, se il sito reattivo ha un aspetto diverso per Android rispetto ad iOS, [!DNL Target] imita quel comportamento.

1. Fai clic su **[!UICONTROL Salva]**.

>[!NOTE]
>
>Quando si tenta di eliminare un riquadro di visualizzazione mobile in uso, viene visualizzato il seguente messaggio: &quot;Questo riquadro di visualizzazione è attualmente associato a una o più attività. (Questo riquadro di visualizzazione è attualmente associato a una o più attività. Per eliminarlo, rimuovilo da tali attività.).

## Creazione di un’esperienza reattiva {#task_D6332438B5EE48CCA8AF199270F1CAEF}

Aggiungi i riquadri di visualizzazione mobili alle attività [!DNL Target] per creare esperienze reattive per gli schermi dei cellulari.

1. Crea l’[attività desiderata](/help/main/c-activities/activities.md).
1. Nel **[!UICONTROL Compositore esperienza visivo]** (VEC), fai clic sull&#39;icona a forma di ingranaggio **[!UICONTROL Impostazioni]**, quindi seleziona **[!UICONTROL Aggiungi riquadri di visualizzazione mobili]**.

   ![Opzione Aggiungi riquadri di visualizzazione mobili](/help/main/c-experiences/c-visual-experience-composer/assets/add-mobile-viewports.png)

1. Fai clic sull&#39;icona **[!UICONTROL Dispositivi]**, quindi attiva tutti i dispositivi che devono avere un riquadro di visualizzazione per dispositivi mobili.

   ![Abilitazione di riquadri di visualizzazione mobili](/help/main/c-experiences/c-visual-experience-composer/assets/mobileviewports.png)

   I riquadri di visualizzazione mobili sono elencati dai più piccola ai più grandi secondo la larghezza.

1. Modifica l’esperienza nei riquadri di visualizzazione mobili in base alle esigenze. Qualsiasi modifica si applica all’esperienza su tutti i dispositivi, ad esempio una modifica al testo di un’intestazione. Passa il cursore del mouse sul nome di un riquadro di visualizzazione per visualizzarne le dimensioni.

   ![Esperienza reattiva su iPhone 11 Pro Max](/help/main/c-experiences/c-visual-experience-composer/assets/iphone11.png)

1. (Facoltativo) Per passare dalla modalità verticale a quella orizzontale, fai clic sull’icona orientamento.

   ![Opzioni di orientamento](/help/main/c-experiences/c-visual-experience-composer/assets/orientation.png)

## Video di formazione

I video seguenti contengono ulteriori informazioni sui riquadri di visualizzazione per dispositivi mobili.

### Compositore esperienza visivo (2 di 2) (7:29) ![Badge panoramica](/help/main/assets/overview.png)

Il video dimostrativo seguente include informazioni sull’utilizzo del Compositore esperienza visivo per lavorare con i riquadri di visualizzazione per dispositivi mobili:

* Rinominare e duplicare un’esperienza
* Creare un’esperienza con reindirizzamento
* Indirizzare un’attività a un singolo URL o a un gruppo di URL
* Creare un’attività multipagina
* Creare un’esperienza e visualizzarne l’anteprima per i siti web reattivi
* Evidenziare tipi di elementi con le sovrapposizioni

>[!VIDEO](https://video.tv.adobe.com/v/36327?captions=ita)

### Preferenze account in Adobe Target ![Icona panoramica](/help/main/assets/overview.png)

Questo video include informazioni sulla configurazione dei riquadri di visualizzazione per dispositivi mobili, a partire dal minuto 4:40.

>[!VIDEO](https://video.tv.adobe.com/v/3507631?captions=ita)
