---
keywords: personalizzazione automatizzata;offerte;target;pubblico;regole targeting;targeting;automated personalization;offers;target;audience;targeting rules;targeting rules;targeting rules;targeting
description: Scopri come indirizzare singole offerte a tipi di pubblico specifici utilizzando le attività di [!UICONTROL Automated Personalization] (AP).
title: Come posso indirizzare le [!UICONTROL offerte Automated Personalization]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Automated Personalization
solution: Target,Analytics
exl-id: 633308dd-437b-4525-a7f8-69656c7d89be
TQID: 'https://experienceleague.adobe.com/AVqyD-Von-gzuVXC09N9qHY5hEe1QLQwSavCE0mp7Ok'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: f0055dd2-93f3-4ac8-9abc-d69d4ed2d977
    internal-label: Automated personalization
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 44c6bdd4ab818226e76477782d7e4238b49d5cdc
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 8%
---
# Offerte [!UICONTROL Automated Personalization] di destinazione {#target-ap-offers}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come indirizzare singole offerte a tipi di pubblico specifici in un&#39;attività **[!UICONTROL Automated Personalization]**.

>[!ENDSHADEBOX]

In un&#39;attività [!DNL Adobe Target] **[!UICONTROL Automated Personalization]** (AP), le regole di targeting consentono di limitare un&#39;offerta a tipi di pubblico specifici, in modo che solo i visitatori che appartengono a tali tipi di pubblico possano visualizzarla. Utilizza le regole di targeting con moderazione e solo quando necessario per un&#39;azienda, in quanto riducono il numero di offerte che un visitatore è idoneo a visualizzare e possono ridurre l&#39;efficacia dei modelli di personalizzazione [!DNL Target].

Ad esempio, considera un’attività di Personalizzazione automatizzata con tre offerte. L&#39;offerta 1 ha una regola di targeting che ne limita l&#39;esposizione al Pubblico A. Due visitatori visualizzano questa attività.

| | Visitatore 1 | Visitatore 2 |
|--- |--- |--- |
| Qualificazione del pubblico | Pubblico A | Pubblico B |
| Punteggio del modello di personalizzazione dell&#39;offerta 1 [!DNL Target] | 90 | 90 |
| Punteggio del modello di personalizzazione dell&#39;offerta 2 [!DNL Target] | 50 | 70 |
| Punteggio del modello di personalizzazione dell&#39;offerta 3 [!DNL Target] | 80 | 60 |

Il visitatore 1 si qualifica come parte del pubblico A, quindi vede l&#39;offerta 1, che ha il punteggio più alto. Il visitatore 2 non fa parte del pubblico A, quindi il visitatore vede l&#39;offerta 2, anche se il punteggio più alto è per l&#39;offerta 1.

## Impostare le regole di targeting {#set-up-targeting-rules}

<a id="task_F207ED7A41B84FD39BB6FCBFABF4B23E"></a>

Le regole di targeting del pubblico controllano quali visitatori possono visualizzare ogni offerta, il che consente di soddisfare una specifica esigenza aziendale, ad esempio riservare un’offerta per un segmento di clienti. Ogni regola restringe le scelte del modello di personalizzazione, quindi applica le regole solo alle offerte che le richiedono.

1. Crea o modifica un&#39;attività di [Automated Personalization](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#create-ap-activity) contenente le offerte sulle quali desideri eseguire il targeting.

   È possibile impostare fino a 50 posizioni e 250 offerte per posizione.

1. Dopo aver impostato le offerte per l&#39;attività nel **[!UICONTROL Compositore esperienza visivo]**, fai clic sull&#39;icona **[!UICONTROL Gestisci contenuto]** ( ![icona Gestisci contenuto](/help/main/assets/icons/Experience.svg) ). Viene visualizzata la finestra di dialogo **[!UICONTROL Gestione contenuto]**.

   ![Icona Gestisci contenuto](../assets/ap-offers-1.png)

1. Fai clic sulla scheda **[!UICONTROL Offerte]**.

1. Scegli le offerte di destinazione, quindi scegli i tipi di pubblico idonei per visualizzarle.

   * Per impostare il targeting per una singola offerta, fai clic sull&#39;icona Ulteriori informazioni ( ![Ulteriori informazioni](/help/main/assets/icons/MoreSmallList.svg) ) accanto all&#39;offerta, quindi fai clic su **[!UICONTROL Pubblico di destinazione]** per visualizzare la finestra di dialogo **[!UICONTROL Aggiungi pubblico]**.
   * Per impostare il targeting per più offerte, seleziona la casella di controllo di ciascuna offerta e fai clic sul collegamento **[!UICONTROL Pubblico di destinazione]** che viene visualizzato in fondo all&#39;elenco.

   ![Icona Gestisci contenuto](../assets/ap-offers-2.png)

1. Nella finestra di dialogo **[!UICONTROL Aggiungi pubblico]**, seleziona il pubblico per le offerte, quindi fai clic su **[!UICONTROL Assegna pubblico]** per tornare alla finestra di dialogo **[!UICONTROL Gestisci contenuto]**.

   >[!NOTE]
   >
   >Invece di creare un nuovo pubblico, puoi combinare più tipi di pubblico con quelli esistenti per creare un pubblico combinato su richiesta. Per ulteriori informazioni, consulta [Combinazione di più tipi di pubblico](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. Fai clic su **[!UICONTROL Fine]**.

Le regole di targeting ora si applicano alle offerte selezionate, in modo che possano essere visualizzate solo dai visitatori che appartengono al pubblico assegnato.
