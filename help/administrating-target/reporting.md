---
keywords: report;reports;reporting;experience cloud solution;timezone;time zone;currency;exclude IPs;estimated lift in revenue;revenue;lift in revenue;fine-grained priorities;fine-grained
description: Configurate  Adobe Target Visual Experience Composer (VEC) specificandone le impostazioni generali, la configurazione del viewport mobile e i selettori CSS.
title: Configurare i rapporti in  Adobe Target
feature: null
topic: Standard
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '666'
ht-degree: 38%

---


# Configurare il reporting in Target

Configurate le impostazioni generali da utilizzare nei [!DNL Adobe Target] rapporti che si applicano all&#39;intero [!DNL Target] account.

Per accedere alla pagina di configurazione [!UICONTROL Reporting] (Generazione rapporti), fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Reporting (Generazione rapporti)].**

In questa pagina potete specificare le seguenti impostazioni:

* La soluzione Adobe Experience Cloud da utilizzare per il reporting
* Fuso orario da utilizzare per il reporting
* Valuta da utilizzare per il reporting
* Indirizzi IP da escludere dalla segnalazione
* Se mostrare l&#39;incremento stimato delle entrate nei rapporti
* Se consentire priorità di grana fine

>[!NOTE]
>
>Tieni presente che il fuso orario, la valuta e gli indirizzi IP per escludere le impostazioni si applicano alle attività che utilizzano i [!DNL Target] rapporti. Queste impostazioni non si applicano alle attività che utilizzano [Analytics per Target (A4T)] come origine di reporting (/help/c-integrating-target-with-mac/a4t/a4t.md).

![Pagina di reporting](/help/administrating-target/assets/reporting.png)

## Soluzione Reporting Cloud

Imposta le opzioni che determinano quali dati vengono utilizzati per i risultati e i rapporti.

Seleziona l&#39;origine di creazione di rapporti per le attività, sia in [!DNL Target] sia in [!DNL Adobe Analytics]. È inoltre possibile selezionare l&#39;origine per la generazione di rapporti per ogni attività.

Considera le seguenti informazioni nella scelta dell&#39;origine per la generazione di rapporti:

* Se l&#39;origine per la generazione di rapporti è impostata su **[!DNL Target]** qui, non è consentito attivare un&#39;attività che utilizza come origine per la generazione di rapporti. [!DNL Analytics] You must change the reporting source to [!DNL Target] in your activity or change the reporting source to **[!UICONTROL Select per activity]** in **[!UICONTROL Administration]>[!UICONTROL Reporting]**.
* Se l&#39;origine per la generazione di rapporti è impostata su **[!DNL Analytics]**[!DNL Target]**[!UICONTROL qui, non è consentito attivare un&#39;attività che utilizza come origine per la generazione di rapporti (l&#39;origine per la generazione di rapporti è specificata come Target per attività])**. You must change the reporting source to[!DNL Analytics]in your activity or change the reporting engine to**[!UICONTROL Select per activity ]**in**[!UICONTROL Administration]>[!UICONTROL Reporting ]**.
* If the reporting source is set to **[!UICONTROL Select per activity]** here, you can create, activate, and deactivate activities that are supported by the selected reporting source. For a matrix of supported activities, see [Supported activity types](/help/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA) in *Adobe Analytics as the reporting source for Adobe Target (A4t)*.
* [!UICONTROL creazione, attivazione e disattivazione dell&#39;attività Automated Personalization] (AP) sono consentite indipendentemente dall&#39;origine di reporting selezionata. Automated Personalization activities are not supported when you choose [Adobe Analytics as the reporting source for Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md). Even if you specify [!DNL Analytics] as your reporting source, [!DNL Target] is used as the reporting source for Automated Personalization activities. For more information, see [Supported activity types](/help/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA) in *Adobe Analytics as the reporting source for Adobe Target (A4t)*.

## Fuso orario per reporting

Specificate il fuso orario da utilizzare per il reporting.

## Valuta per reporting

Specificare la valuta da utilizzare per il reporting.

## IP da escludere dai dati di reporting di Target

Specificate eventuali indirizzi IP da escludere dai dati di reporting. Ad esempio, escludere gli indirizzi aziendali interni è un buon modo per garantire che i dati di reporting riflettano le interazioni dei clienti sul sito Web.

Immettete ogni indirizzo IP su una nuova riga.

## Mostra incremento stimato nei ricavi

È possibile scegliere di visualizzare l&#39;incremento stimato delle entrate se si inserisce un valore monetario per l&#39;obiettivo. Con [!DNL Target] puoi stimare l’incremento dei ricavi potenziali se tutti gli utenti visualizzano l’esperienza vincente. La funzione di stima dell&#39;incremento è disabilitata per impostazione predefinita.

Only [!DNL Experience Cloud] Admin users can enable or disable this feature. Se la stima dell’incremento è disattivata, i campi corrispondenti non vengono visualizzati nell’interfaccia. La disattivazione della funzione non si traduce in una perdita di dati, compresi i dati utilizzati per le stime. Le stime si basano sui dati raccolti indipendentemente dallo stato di attivazione della funzione.

Per informazioni dettagliate, vedi [Stima dell’incremento dei ricavi](/help/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md).

## Abilita priorità precise

Consente di specificare voci numeriche per priorità da 0 a 999.

L’interfaccia utente e le opzioni per Priorità variano a seconda delle impostazioni. È possibile utilizzare le impostazioni legacy Bassa, Media o Alta, oppure attivare la priorità precisa da 0 a 999.

La priorità è utilizzata se più attività vengono assegnate alla stessa posizione con lo stesso pubblico. Se due o più attività vengono assegnate alla posizione, viene visualizzata l’attività con priorità maggiore.
