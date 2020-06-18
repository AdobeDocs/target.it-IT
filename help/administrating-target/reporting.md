---
keywords: report;reports;reporting;experience cloud solution;timezone;time zone;currency;exclude IPs;estimated lift in revenue;revenue;lift in revenue;fine-grained priorities;fine-grained
description: Configurate il  Adobe Target Visual Experience Composer (VEC) specificandone le impostazioni generali, la configurazione del viewport mobile e i selettori CSS.
title: Configurare i rapporti in  Adobe Target
topic: Standard
translation-type: tm+mt
source-git-commit: 44d9024cb9c1f6a1e28845f9545fed0d56fe176a
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 65%

---


# Configurare i rapporti in Target

Configurate le impostazioni generali da utilizzare nei rapporti Target applicabili all&#39;intero [!DNL Target] account.

>[!NOTE]
>
>Le informazioni riportate in questo argomento sono state aggiornate per fornire un picco spettacolare delle modifiche all&#39;interfaccia utente in arrivo nella release Target Standard/Premium 20.6.1 (luglio 2020). La maggior parte delle informazioni presentate in questo argomento si applica all’interfaccia utente corrente; tuttavia, le opzioni potrebbero trovarsi in posizioni leggermente diverse.

Per accedere alla pagina di configurazione [!UICONTROL Reporting] (Generazione rapporti), fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Reporting (Generazione rapporti)].**

In questa pagina potete specificare le seguenti impostazioni:

* La soluzione Adobe Experience Cloud da utilizzare per il reporting
* Fuso orario da utilizzare per il reporting
* Valuta da utilizzare per il reporting
* Indirizzi IP da escludere dalla segnalazione
* Se mostrare l&#39;incremento stimato delle entrate nei rapporti
* Se consentire priorità di grana fine

![Pagina di reporting](/help/administrating-target/assets/reporting.png)

## Soluzione Reporting Cloud

Imposta le opzioni che determinano quali dati vengono utilizzati per i risultati e i rapporti.

Seleziona l&#39;origine di creazione di rapporti per le attività, sia in [!DNL Target] sia in Adobe Analytics. È inoltre possibile selezionare l&#39;origine per la generazione di rapporti per ogni attività.

Considera le seguenti informazioni nella scelta dell&#39;origine per la generazione di rapporti:

* La creazione, l’attivazione e la disattivazione delle attività di [!UICONTROL Allocazione automatica], [!UICONTROL Targeting automatico] e [!UICONTROL Personalizzazione automatizzata] (AP) sono consentite indipendentemente dall’origine per la generazione di rapporti selezionata. Questi tipi di attività non sono supportati quando si sceglie [Adobe Analytics come origine per la generazione di rapporti per Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md). Anche se si specifica Analytics come origine per la generazione di rapporti, [!DNL Target] viene utilizzato come origine per la generazione di rapporti per questi tipi di attività.
* Se l’origine per la generazione di rapporti è impostata su Analytics qui, non è consentito attivare un’attività che utilizza [!DNL Target] come origine per la generazione di rapporti (l’origine per la generazione di rapporti è specificata come Target per attività). È necessario modificare l&#39;origine per la generazione di rapporti in Analytics nell’attività o modificare il motore di generazione di rapporti in Seleziona per attività in Configurazione > Preferenze.
* Se l&#39;origine per la generazione di rapporti è impostata su [!DNL Target] qui, non è consentito attivare un&#39;attività che utilizza Analytics come origine per la generazione di rapporti. È necessario modificare l&#39;origine per la generazione di rapporti in [!DNL Target] nell’attività o modificare l’origine per la generazione di rapporti in Seleziona per attività in Configurazione > Preferenze.
* Se l&#39;origine per la generazione di rapporti è impostata su Seleziona per attività qui, è possibile creare, attivare e disattivare attività supportate dall&#39;origine per la generazione di rapporti selezionata. Per una matrice delle attività supportate, vedi [Adobe Analytics come origine per la generazione di rapporti per Adobe Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T).
* Quando si passa da Manuale A/B ad [!UICONTROL Allocazione automatica] o [!UICONTROL Targeting automatico] tutte le metriche e i pubblici di reportistica vengono persi se l’origine per la generazione di rapporti dell’attività Manuale A/B non è supportata nelle attività di [!UICONTROL Allocazione automatica] o [!UICONTROL Targeting automatico].

## Fuso orario per reporting

Specificate il fuso orario da utilizzare per il reporting.

## Valuta per reporting

Specificare la valuta da utilizzare per il reporting.

## IP da escludere dai dati di reporting di Target

Specificate eventuali indirizzi IP da escludere dai dati di reporting. Ad esempio, escludere gli indirizzi aziendali interni è un buon modo per garantire che i dati di reporting riflettano le interazioni dei clienti sul sito Web.

Immettete ogni indirizzo IP su una nuova riga.

## Mostra incremento stimato nei ricavi

È possibile scegliere di visualizzare l&#39;incremento stimato delle entrate se si inserisce un valore monetario per l&#39;obiettivo. Con [!DNL Target] puoi stimare l’incremento dei ricavi potenziali se tutti gli utenti visualizzano l’esperienza vincente. La funzione di stima dell&#39;incremento è disabilitata per impostazione predefinita.

Solo gli utenti amministratore di Experience Cloud possono abilitare o disabilitare questa funzione. Se la stima dell’incremento è disattivata, i campi corrispondenti non vengono visualizzati nell’interfaccia. La disattivazione della funzione non si traduce in una perdita di dati, compresi i dati utilizzati per le stime. Le stime si basano sui dati raccolti indipendentemente dallo stato di attivazione della funzione.

Per informazioni dettagliate, vedi [Stima dell’incremento dei ricavi](/help/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md).

## Abilita priorità precise

Consente di specificare voci numeriche per priorità da 0 a 999.

L’interfaccia utente e le opzioni per Priorità variano a seconda delle impostazioni. È possibile utilizzare le impostazioni legacy Bassa, Media o Alta, oppure attivare la priorità precisa da 0 a 999.

La priorità è utilizzata se più attività vengono assegnate alla stessa posizione con lo stesso pubblico. Se due o più attività vengono assegnate alla posizione, viene visualizzata l’attività con priorità maggiore.
