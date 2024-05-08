---
keywords: report;report;reporting;soluzione experience cloud;fuso orario;fuso orario;valuta;escludere gli IP;incremento stimato dei ricavi;ricavi;incremento dei ricavi;priorità dettagliate;fine-grained
description: Utilizzare [!DNL Target], [!DNL Adobe Analytics], or [!DNL Adobe Customer Journey Analytics] come origine per la generazione di rapporti, specifica il fuso orario e il formato della valuta predefiniti, aggiungi indirizzi IP da escludere dalla generazione dei rapporti e altro ancora.
title: Come si configura il reporting in [!DNL Target]?
feature: Administration & Configuration
role: Admin
exl-id: fd83e60e-64a6-4d0e-909f-480d13bac32b
source-git-commit: ea9513c4310d13e1e7899aa7e228b4d7ecdf0748
workflow-type: tm+mt
source-wordcount: '761'
ht-degree: 22%

---

# Configurare il reporting in [!DNL Target]

Configurare le impostazioni generali da utilizzare in [!DNL Adobe Target] generazione di rapporti applicabili all&#39;intero [!DNL Target] account.

Per accedere al [!UICONTROL Reporting] nella pagina di configurazione, fai clic su **[!UICONTROL Administration]** > **[!UICONTROL Reporting].**

In questa pagina è possibile specificare le impostazioni seguenti:

* La soluzione Adobe Experience Cloud da utilizzare per il reporting
* Fuso orario da utilizzare per il reporting
* Valuta da utilizzare per il reporting
* Indirizzi IP da escludere dal reporting
* Se mostrare l’incremento stimato dei ricavi nel reporting
* Se abilitare le priorità dettagliate

>[!NOTE]
>
>Tieni presente che il fuso orario, la valuta e gli indirizzi IP da escludere si applicano alle attività che utilizzano [!DNL Target] reportistica. Queste impostazioni non si applicano alle attività che utilizzano [Analytics for Target (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md) o [!DNL Customer Journey Analytics] come origine per la generazione di rapporti.

![Pagina di reporting](/help/main/administrating-target/assets/reporting.png)

## Soluzione Reporting Cloud {#solution}

Imposta le opzioni che determinano quali dati vengono utilizzati per i risultati e i rapporti.

Seleziona l&#39;origine per la generazione di rapporti per le attività, [!DNL Target], [!DNL Adobe Analytics], o [!DNL Adobe Customer Journey Analytics]. Puoi anche scegliere di selezionare l’origine per la generazione di rapporti per attività nell’ambito del flusso di lavoro guidato in tre parti durante la creazione dell’attività.

Considera le seguenti informazioni nella scelta dell&#39;origine per la generazione di rapporti:

* **[!DNL Adobe Target]**: se l’origine per la generazione di rapporti è impostata su **[!DNL Target]** in questo caso, non ti è consentito creare o attivare un’attività che utilizza [!DNL Analytics] o [!DNL Customer Journey Analytics] come origine per la generazione di rapporti. È necessario modificare l’origine per la generazione di rapporti in **[!UICONTROL Select per activity]**.
* **[!DNL Adobe Analytics]**: se l’origine per la generazione di rapporti è impostata su **[!DNL Analytics]** in questo caso, non ti è consentito creare o attivare un’attività che utilizza [!DNL Target] o [!DNL Customer Journey Analytics] come origine per la generazione di rapporti. È necessario modificare l’origine per la generazione di rapporti in **[!UICONTROL Select per activity]**.
* **[!DNL Adobe Customer Journey Analytics]**: se l’origine per la generazione di rapporti è impostata su **[!DNL Customer Journey Analytics]** in questo caso, non ti è consentito creare o attivare un’attività che utilizza [!DNL Target] o [!DNL Analytics] come origine per la generazione di rapporti. È necessario modificare l’origine per la generazione di rapporti in **[!UICONTROL Select per activity]**.
* **Seleziona per attività**: se l’origine per la generazione di rapporti è impostata su **[!UICONTROL Select per activity]** qui puoi creare e attivare attività supportate dall’origine per la generazione di rapporti selezionata.

Quando determini l’origine per la generazione di rapporti, considera le seguenti informazioni:

* **[!DNL Analytics]**: per una matrice di attività supportate che utilizza [!DNL Analytics] come origine per la generazione di rapporti (A4T), consulta [Tipi di attività supportati](/help/main/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA) in *Adobe Analytics come origine per la generazione di rapporti per Adobe Target (A4T)*.

  [!UICONTROL Automated Personalization] (AP) la creazione e l&#39;attivazione di attività sono consentite indipendentemente dall&#39;origine per la generazione di rapporti selezionata. [!UICONTROL Automated Personalization] Le attività non sono supportate quando si sceglie [Adobe Analytics come origine per la generazione di rapporti per Adobe Target (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

  Anche se si specifica [!DNL Analytics] come origine per la generazione di rapporti, [!DNL Target] viene utilizzato come origine di reporting per [!DNL Automated Personalization] attività.

* **[!DNL Customer Journey Analytics]**: per una matrice di attività supportate che utilizza [!DNL Target] creazione di rapporti in [!DNL Customer Journey Analytics], vedi [Tipi di attività supportati](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md#supported-activities) in *[!DNL Target]creazione di rapporti in[!DNL Adobe Customer Journey Analytics]*.

  [!UICONTROL Automated Personalization] AP) [!UICONTROL Auto-Allocate], e [!UICONTROL Auto-Target] la creazione e l’attivazione delle attività sono consentite indipendentemente dall’origine per la generazione di rapporti selezionata. Queste attività non sono supportate quando si sceglie [Adobe Customer Journey Analytics come origine per la generazione di rapporti](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md).

  Anche se si specifica [!DNL Customer Journey Analytics] come origine per la generazione di rapporti, [!DNL Target] viene utilizzato come origine di reporting per [!DNL Automated Personalization] attività.

  Se si specifica [!DNL Customer Journey Analytics] come origine per la generazione di rapporti per [!UICONTROL Auto-Allocate] o [!UICONTROL Auto-Target] attività, [!DNL Target] o [!DNL Analytics] può essere utilizzato come origine per la generazione di rapporti.

## Fuso orario per il reporting

Specifica il fuso orario da utilizzare per i rapporti.

## Valuta per il reporting

Specifica la valuta da utilizzare per il reporting.

## IP da escludere [!DNL Target] dati di reporting

Specifica eventuali indirizzi IP da escludere dai dati di reporting. Ad esempio, escludere gli indirizzi aziendali interni è un buon modo per garantire che i dati di reporting riflettano le interazioni dei clienti sul sito web.

Inserisci ogni indirizzo IP su una nuova riga.

## Mostra incremento stimato nei ricavi

Se inserisci un valore monetario per l’obiettivo, puoi scegliere di visualizzare l’incremento stimato dei ricavi. Con [!DNL Target] puoi stimare l’incremento dei ricavi potenziali se tutti gli utenti visualizzano l’esperienza vincente. La funzione di stima dell&#39;incremento è disabilitata per impostazione predefinita.

Solo [!DNL Experience Cloud] Gli utenti amministratori possono abilitare o disabilitare questa funzione. Se la stima dell’incremento è disattivata, i campi corrispondenti non vengono visualizzati nell’interfaccia. La disattivazione della funzione non si traduce in una perdita di dati, compresi i dati utilizzati per le stime. Le stime si basano sui dati raccolti indipendentemente dallo stato di attivazione della funzione.

Per informazioni dettagliate, vedi [Stima dell’incremento dei ricavi](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md).

## Abilita priorità precise

Consente di specificare voci numeriche per priorità da 0 a 999.

L’interfaccia utente e le opzioni per Priorità variano a seconda delle impostazioni. È possibile utilizzare le impostazioni legacy Bassa, Media o Alta, oppure attivare la priorità precisa da 0 a 999.

La priorità è utilizzata se più attività vengono assegnate alla stessa posizione con lo stesso pubblico. Se due o più attività vengono assegnate alla posizione, viene visualizzata l’attività con priorità maggiore.
