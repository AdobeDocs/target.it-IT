---
keywords: troubleshooting;metric discrepancies;FAQ;reports
description: Elenco delle domande frequenti sulla generazione di rapporti in Adobe Target.
title: Domande frequenti sulla generazione di rapporti in Adobe Target
topic: Standard
uuid: 0be40d3f-3274-493d-899b-cb7bb3612baf
translation-type: tm+mt
source-git-commit: 9168a8f14ad45dfc48ad5c314df61ee8c02156d5

---


# Domande frequenti sulla generazione di rapporti{#reporting-faq}

Elenco delle domande frequenti sulla generazione di rapporti in [!DNL Target].

## Perché i miei rapporti [!UICONTROL Targeting esperienze] (XT) contengono metriche per le esperienze di controllo?

Nelle attività Targeting esperienze (XT) deve essere sempre presente un’esperienza di controllo. Se utilizzi un’attività XT in modo simile a un’[!UICONTROL attività Test A/B], come spesso avviene, i dati sull’esperienza di controllo sono utili. Se ritieni che non siano utili nei tuoi rapporti, puoi semplicemente ignorarli.

## Perché il numero di visite in [!DNL Target] è inferiore rispetto ad altre soluzioni [!DNL Adobe Experience Cloud]?{#section_7E626FDB417E41B8B58BBF30FB207409}

I numeri delle metriche, ad esempio le visite, segnalati da [!DNL Target] saranno sempre inferiori ai numeri riportati in altre soluzioni di [!DNL Experience Cloud] per una serie di motivi:

* [!DNL Target] conta le visite solo per i visitatori che si qualificano per l’attività. Altre soluzioni contano le visite per i visitatori che visualizzano la pagina, indipendentemente dall’attività che li ha portati alla pagina.
* In alcune situazioni, attività differenti competono per la stessa posizione (reciprocamente esclusive). Di conseguenza, i visitatori visualizzano contenuti diversi in una pagina web, che influiscono sui numeri della metrica riportati da [!DNL Target].

## Perché non sono disponibili dati per il rapporto della mia attività? {#section_E4722F6445884130951DF79981C8289B}

Se il contenuto di un’attività è stato recapitato correttamente agli utenti ma il relativo rapporto non contiene dati, assicurati di aver selezionato l’ambiente corretto ([gruppo host](/help/administrating-target/hosts.md)) nelle impostazioni del rapporto.

Se hai selezionato un ambiente di sviluppo, potresti visualizzare il seguente messaggio di errore: “Non sono disponibili dati per le impostazioni di rapporto selezionate.”.

Per modificare l’ambiente per il rapporto di un’attività:

1. Fai clic su **[!UICONTROL Attività]**, scegli l’attività desiderata dall’elenco, quindi fai clic sulla scheda **[!UICONTROL Rapporti]**.
1. Fai clic sull’icona a forma di ruota dentata per configurare le impostazioni dei rapporti.

   ![Finestra di dialogo Impostazioni A/B](/help/c-reports/c-report-settings/assets/ab_settings_dialog.png)

   >[!NOTE]
   >
   >L’icona a forma di ingranaggio non è disponibile per i rapporti di [!UICONTROL Personalizzazione automatizzata].

1. Dall’elenco a discesa **[!UICONTROL Ambiente]**, seleziona **[!UICONTROL Produzione]**.

   I dati del rapporto potrebbero non essere disponibili se hai selezionato un ambiente di sviluppo.

1. Fai clic su **[!UICONTROL Salva]**.

Per ulteriori informazioni sugli ambienti, vedi [Host](../administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E).

## Perché la divisione del traffico tra le mie esperienze non è uniforme nell&#39;attività A/B o MVT? {#uneven}

Ad esempio, ho impostato la suddivisione del traffico su 50/50 o 33/33/33, ma vedo una distribuzione molto diversa tra le esperienze nel reporting.

Nella generazione dei [!DNL Target] rapporti sono disponibili diversi motivi per cui è possibile suddividere il traffico in modo discontinuo:

* Quando un&#39; [!DNL Target] attività viene avviata per la prima volta, la distribuzione del traffico potrebbe non essere uniforme a causa dell&#39;architettura dei nodi periferici che [!DNL Target] utilizza per ottimizzare la distribuzione dell&#39;esperienza. La procedura ottimale consiste nel concedere a un&#39;attività un certo tempo per la raccolta di dati aggiuntivi e la distribuzione si normalizzerà. Per ulteriori informazioni sull&#39; [!DNL Adobe Target] architettura e sui nodi Edge, consulta [Funzionamento](/help/c-intro/how-target-works.md)di Adobe Target.
* Quale metrica di normalizzazione stai utilizzando? Se vi trovate in [!DNL Target] o [!DNL Analytics] e utilizzate la metrica **[!UICONTROL Visite]** , ricordate che [!DNL Target] è un sistema basato sui visitatori e che la distribuzione del traffico per un test A/B o MVT è assegnata a livello di visitatore. Pertanto, se si esaminano i risultati dell&#39;attività utilizzando la metrica **[!UICONTROL Visite]** , la distribuzione del traffico potrebbe apparire diseguale perché alcuni visitatori potrebbero avere più visite.
* La procedura ottimale per i test A/B e MVT consiste nel mantenere uniformi le suddivisioni del traffico. La modifica della distribuzione del traffico tra le esperienze (ad esempio da 90/10 a 50/50) durante un test può portare a visitatori irregolari tra le esperienze.
* Se state seguendo le best practice sopra riportate e la suddivisione del traffico non si normalizza nel tempo, è necessario verificare quanto segue:

   * Utilizzi la libreria at.js più recente? Per ulteriori informazioni sulla versione corrente e sulle relative note sulla versione, consulta i dettagli [della versione](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)at.js.

   * È un test di reindirizzamento? I tempi errati per l&#39;attivazione dei tag sulla pagina possono causare interruzioni di traffico non uniformi, soprattutto se utilizzati [!DNL Analytics] come origine dati per un&#39; [!DNL Target] attività. Per informazioni dettagliate per correggere la distribuzione del traffico diseguale in un&#39;attività di reindirizzamento con Analytics for Target (A4T), consultate [Offerte di reindirizzamento - Domande frequenti](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md)A4T.
