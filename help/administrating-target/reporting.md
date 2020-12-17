---
keywords: report;reports;reporting;experience cloud solution;timezone;time zone;currency;exclude IPs;estimated lift in revenue;revenue;lift in revenue;fine-grained priorities;fine-grained
description: Configurate  Adobe Target Visual Experience Composer (VEC) specificandone le impostazioni generali, la configurazione del viewport mobile e i selettori CSS.
title: Configurare i rapporti in  Adobe Target
feature: Administration & Configuration
translation-type: tm+mt
source-git-commit: 9b57d5554884b06d278c3baef3b2c1d5f37bdeb5
workflow-type: tm+mt
source-wordcount: '666'
ht-degree: 38%

---


# Configurare il reporting in Target

Configurare le impostazioni generali da utilizzare nei report [!DNL Adobe Target] che si applicano all&#39;intero account [!DNL Target].

Per accedere alla pagina di configurazione [!UICONTROL Reporting], fare clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Reporting].**

In questa pagina potete specificare le seguenti impostazioni:

* La soluzione Adobe Experience Cloud da utilizzare per il reporting
* Fuso orario da utilizzare per il reporting
* Valuta da utilizzare per il reporting
* Indirizzi IP da escludere dalla segnalazione
* Se mostrare l&#39;incremento stimato delle entrate nei rapporti
* Se consentire priorità di grana fine

>[!NOTE]
>
>Tieni presente che il fuso orario, la valuta e gli indirizzi IP per escludere le impostazioni si applicano alle attività che utilizzano il reporting [!DNL Target]. Queste impostazioni non si applicano alle attività che utilizzano [Analytics for Target (A4T)] come origine di reporting (/help/c-integrating-target-with-mac/a4t/a4t.md).

![Pagina di reporting](/help/administrating-target/assets/reporting.png)

## Soluzione di Reporting Cloud

Imposta le opzioni che determinano quali dati vengono utilizzati per i risultati e i rapporti.

Seleziona l&#39;origine di creazione di rapporti per le attività, sia in [!DNL Target] sia in [!DNL Adobe Analytics]. È inoltre possibile selezionare l&#39;origine per la generazione di rapporti per ogni attività.

Considera le seguenti informazioni nella scelta dell&#39;origine per la generazione di rapporti:

* Se l&#39;origine per la generazione di rapporti è impostata su **[!DNL Target]** qui, non è consentito attivare un&#39;attività che utilizza come origine per la generazione di rapporti. [!DNL Analytics] È necessario modificare l&#39;origine di reporting in [!DNL Target] nell&#39;attività oppure cambiare l&#39;origine di reporting in **[!UICONTROL Seleziona per attività]** in **[!UICONTROL Amministrazione] > [!UICONTROL Reporting]**.
* Se l&#39;origine per la generazione di rapporti è impostata su **[!DNL Analytics]**[!DNL Target]**[!UICONTROL qui, non è consentito attivare un&#39;attività che utilizza come origine per la generazione di rapporti (l&#39;origine per la generazione di rapporti è specificata come Target per attività])**. È necessario modificare l&#39;origine di reporting in [!DNL Analytics] nell&#39;attività oppure cambiare il motore di reporting in **[!UICONTROL Seleziona per attività]** in **[!UICONTROL Amministrazione] > [!UICONTROL Reporting]**.
* Se l&#39;origine di reporting è impostata su **[!UICONTROL Seleziona per attività]** qui, puoi creare, attivare e disattivare le attività supportate dall&#39;origine di reporting selezionata. Per una matrice di attività supportate, vedere [Tipi di attività supportati](/help/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA) in *Adobe Analytics come origine di reporting per  Adobe Target (A4t)*.
* [!UICONTROL  creazione, attivazione e disattivazione dell&#39;attività Automated Personalization] (AP) sono consentite indipendentemente dall&#39;origine di reporting selezionata.  le attività Automated Personalization non sono supportate quando si sceglie [ Adobe Analytics come origine di reporting per  Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md). Anche se si specifica [!DNL Analytics] come origine di reporting, [!DNL Target] viene utilizzato come origine di reporting per  attività Automated Personalization. Per ulteriori informazioni, vedere [Tipi di attività supportati](/help/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA) in *Adobe Analytics come origine di reporting per  Adobe Target (A4t)*.

## Fuso orario per reporting

Specificate il fuso orario da utilizzare per il reporting.

## Valuta per reporting

Specificare la valuta da utilizzare per il reporting.

## IP da escludere dai dati di reporting di Target

Specificate eventuali indirizzi IP da escludere dai dati di reporting. Ad esempio, escludere gli indirizzi aziendali interni è un buon modo per garantire che i dati di reporting riflettano le interazioni dei clienti sul sito Web.

Immettete ogni indirizzo IP su una nuova riga.

## Mostra incremento stimato nei ricavi

È possibile scegliere di visualizzare l&#39;incremento stimato delle entrate se si inserisce un valore monetario per l&#39;obiettivo. Con [!DNL Target] puoi stimare l’incremento dei ricavi potenziali se tutti gli utenti visualizzano l’esperienza vincente. La funzione di stima dell&#39;incremento è disabilitata per impostazione predefinita.

Solo gli utenti [!DNL Experience Cloud] amministratori possono attivare o disattivare questa funzione. Se la stima dell’incremento è disattivata, i campi corrispondenti non vengono visualizzati nell’interfaccia. La disattivazione della funzione non si traduce in una perdita di dati, compresi i dati utilizzati per le stime. Le stime si basano sui dati raccolti indipendentemente dallo stato di attivazione della funzione.

Per informazioni dettagliate, vedi [Stima dell’incremento dei ricavi](/help/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md).

## Abilita priorità precise

Consente di specificare voci numeriche per priorità da 0 a 999.

L’interfaccia utente e le opzioni per Priorità variano a seconda delle impostazioni. È possibile utilizzare le impostazioni legacy Bassa, Media o Alta, oppure attivare la priorità precisa da 0 a 999.

La priorità è utilizzata se più attività vengono assegnate alla stessa posizione con lo stesso pubblico. Se due o più attività vengono assegnate alla posizione, viene visualizzata l’attività con priorità maggiore.
