---
description: Elenco delle domande frequenti sulla generazione di rapporti in Target.
keywords: risoluzione dei problemi;discrepanze metriche;FAQ;domande frequenti;rapporti
seo-description: Elenco delle domande frequenti sui rapporti in Adobe Target.
seo-title: Domande frequenti sui rapporti per Adobe Target
solution: Target
title: Domande frequenti sulla generazione di rapporti
topic: Standard
uuid: 0be40d3f-3274-493d-899b-cb7bb3612baf
translation-type: tm+mt
source-git-commit: a6f2eceaddf67653b36a1687ba071f7226169516

---


# Domande frequenti sulla generazione di rapporti{#reporting-faq}

Elenco delle domande frequenti sulla generazione di rapporti in [!DNL Target].

## Why do my [!UICONTROL Experience Targeting] (XT) reports contain metrics for control experiences?

Le attività XT dovrebbero avere sempre un'esperienza di controllo. If you are using an XT activity in a similar manner to an [!UICONTROL A/B Test] activity, which is a fairly common scenario, the control experience data is useful. Se lo ritenete inutile nei rapporti, potete ignorare i dati sull'esperienza di controllo.

## Why are the number of visits lower in [!DNL Target] than in other [!DNL Adobe Experience Cloud] solutions? {#section_7E626FDB417E41B8B58BBF30FB207409}

I numeri delle metriche, ad esempio le visite, segnalati da [!DNL Target] saranno sempre inferiori ai numeri riportati in altre soluzioni di [!DNL Experience Cloud] per una serie di motivi:

* [!DNL Target] conta le visite solo per i visitatori che si qualificano per l’attività. Altre soluzioni contano le visite per i visitatori che visualizzano la pagina, indipendentemente dall’attività che li ha portati alla pagina.
* Potrebbero verificarsi situazioni in cui le varie attività competono per la stessa posizione (escludendo a vicenda). Di conseguenza, i visitatori visualizzano contenuti diversi in una pagina web, che influiscono sui numeri della metrica riportati da [!DNL Target].

## Perché non sono disponibili dati per il rapporto della mia attività? {#section_E4722F6445884130951DF79981C8289B}

If an activity's content was successfully delivered to users but its report contains no data, ensure that you have the correct environment ([host group](/help/administrating-target/hosts.md)) selected in the report's settings.

Se hai selezionato un ambiente di sviluppo, potresti visualizzare il seguente messaggio di errore: “Non sono disponibili dati per le impostazioni di rapporto selezionate.”.

Per modificare l’ambiente per il rapporto di un’attività:

1. Fai clic su **[!UICONTROL Attività]**, scegli l’attività desiderata dall’elenco, quindi fai clic sulla scheda **[!UICONTROL Rapporti]**.
1. Fai clic sull’icona a forma di ruota dentata per configurare le impostazioni dei rapporti.

   ![Finestra di dialogo Impostazioni A/B](/help/c-reports/c-report-settings/assets/ab_settings_dialog.png)

   >[!NOTE]
   >
   >The gear icon is not available for [!UICONTROL Automated Personalization] (AP) reports.

1. Dall’elenco a discesa **[!UICONTROL Ambiente]**, seleziona **[!UICONTROL Produzione]**.

   I dati del rapporto potrebbero non essere disponibili se hai selezionato un ambiente di sviluppo.

1. Fai clic su **[!UICONTROL Salva]**.

Per ulteriori informazioni sugli ambienti, vedi [Host](../administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E).
