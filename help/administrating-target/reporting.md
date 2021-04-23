---
keywords: rapporto;rapporti;rapporto;soluzione experience cloud;fuso orario;fuso orario;valuta;escludere IP;incremento stimato dei ricavi;ricavi;incremento dei ricavi;priorità precise;priorità precise
description: Utilizza [!DNL Target] o Adobe Analytics come origine per la generazione di rapporti, specifica il fuso orario e il formato della valuta predefiniti, aggiungi gli indirizzi IP da escludere dal rapporto e altro ancora.
title: Come si configura il reporting in Target?
feature: Amministrazione e configurazione
role: Administrator
exl-id: fd83e60e-64a6-4d0e-909f-480d13bac32b
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 36%

---

# Configurare il reporting in Target

Configura le impostazioni generali da utilizzare nei rapporti [!DNL Adobe Target] che si applicano all&#39;intero account [!DNL Target].

Per accedere alla pagina di configurazione [!UICONTROL Reporting], fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Reporting].**

In questa pagina puoi specificare le seguenti impostazioni:

* Soluzione Adobe Experience Cloud da utilizzare per il reporting
* Fuso orario da utilizzare per la generazione di rapporti
* Valuta da utilizzare per la generazione di rapporti
* Indirizzi IP da escludere dal reporting
* Se mostrare un incremento stimato dei ricavi nel reporting
* Se consentire priorità precise

>[!NOTE]
>
>Tieni presente che il fuso orario, la valuta e gli indirizzi IP per escludere le impostazioni si applicano alle attività che utilizzano il reporting [!DNL Target]. Queste impostazioni non si applicano alle attività che utilizzano [Analytics for Target (A4T)] come origine per la generazione di rapporti (/help/c-integrating-target-with-mac/a4t/a4t.md).

![Pagina di reporting](/help/administrating-target/assets/reporting.png)

## Soluzione Reporting Cloud

Imposta le opzioni che determinano quali dati vengono utilizzati per i risultati e i rapporti.

Seleziona l&#39;origine di creazione di rapporti per le attività, sia in [!DNL Target] sia in [!DNL Adobe Analytics]. È inoltre possibile selezionare l&#39;origine per la generazione di rapporti per ogni attività.

Considera le seguenti informazioni nella scelta dell&#39;origine per la generazione di rapporti:

* Se l&#39;origine per la generazione di rapporti è impostata su **[!DNL Target]** qui, non è consentito attivare un&#39;attività che utilizza come origine per la generazione di rapporti. [!DNL Analytics] È necessario modificare l&#39;origine per la generazione di rapporti in [!DNL Target] nell&#39;attività o modificare l&#39;origine per la generazione di rapporti in **[!UICONTROL Seleziona per attività]** in **[!UICONTROL Amministrazione] > [!UICONTROL Generazione di rapporti]**.
* Se l&#39;origine per la generazione di rapporti è impostata su **[!DNL Analytics]**[!DNL Target]**[!UICONTROL qui, non è consentito attivare un&#39;attività che utilizza come origine per la generazione di rapporti (l&#39;origine per la generazione di rapporti è specificata come Target per attività])**. È necessario modificare l&#39;origine per la generazione di rapporti in [!DNL Analytics] nell&#39;attività o modificare il motore di generazione rapporti in **[!UICONTROL Seleziona per attività]** in **[!UICONTROL Amministrazione] > [!UICONTROL Generazione di rapporti]**.
* Se l&#39;origine per la generazione di rapporti è impostata su **[!UICONTROL Seleziona per attività]** qui, puoi creare, attivare e disattivare attività supportate dall&#39;origine per la generazione di rapporti selezionata. Per una matrice delle attività supportate, consulta [Tipi di attività supportate](/help/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA) in *Adobe Analytics come origine per la generazione di rapporti per Adobe Target (A4t)*.
* [!UICONTROL La creazione, l’attivazione e la disattivazione delle attività di Automated Personalization]  (AP) sono consentite indipendentemente dall’origine per la generazione di rapporti selezionata. Le attività Automated Personalization non sono supportate quando scegli [Adobe Analytics come origine per la generazione di rapporti per Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md). Anche se si specifica [!DNL Analytics] come origine per la generazione di rapporti, [!DNL Target] viene utilizzato come origine per la generazione di rapporti per le attività di Automated Personalization. Per ulteriori informazioni, consulta [Tipi di attività supportati](/help/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA) in *Adobe Analytics come origine per la generazione di rapporti per Adobe Target (A4t)*.

## Fuso orario per il reporting

Specifica il fuso orario da utilizzare per il reporting.

## Valuta per la segnalazione

Specifica la valuta da utilizzare per il reporting.

## IP da escludere dai dati di reporting [!DNL Target]

Specifica gli indirizzi IP da escludere dai dati di reporting. Ad esempio, escludere gli indirizzi aziendali interni è un buon modo per garantire che i dati di reporting riflettano le interazioni dei clienti sul sito web.

Inserisci ogni indirizzo IP su una nuova riga.

## Mostra incremento stimato nei ricavi

È possibile scegliere di mostrare l&#39;incremento stimato dei ricavi se si immette un valore monetario per l&#39;obiettivo. Con [!DNL Target] puoi stimare l’incremento dei ricavi potenziali se tutti gli utenti visualizzano l’esperienza vincente. La funzione di stima dell&#39;incremento è disabilitata per impostazione predefinita.

Questa funzione può essere attivata o disattivata solo dagli utenti amministratore [!DNL Experience Cloud]. Se la stima dell’incremento è disattivata, i campi corrispondenti non vengono visualizzati nell’interfaccia. La disattivazione della funzione non si traduce in una perdita di dati, compresi i dati utilizzati per le stime. Le stime si basano sui dati raccolti indipendentemente dallo stato di attivazione della funzione.

Per informazioni dettagliate, vedi [Stima dell’incremento dei ricavi](/help/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md).

## Abilita priorità precise

Consente di specificare voci numeriche per priorità da 0 a 999.

L’interfaccia utente e le opzioni per Priorità variano a seconda delle impostazioni. È possibile utilizzare le impostazioni legacy Bassa, Media o Alta, oppure attivare la priorità precisa da 0 a 999.

La priorità è utilizzata se più attività vengono assegnate alla stessa posizione con lo stesso pubblico. Se due o più attività vengono assegnate alla posizione, viene visualizzata l’attività con priorità maggiore.
