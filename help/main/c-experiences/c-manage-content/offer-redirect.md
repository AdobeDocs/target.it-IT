---
keywords: offerta di reindirizzamento;creare offerta di reindirizzamento;aggiungere offerta HTML;trasmettere tutti i parametri URL nel reindirizzamento
description: Scopri come creare offerte di reindirizzamento per indirizzare facilmente i browser alle nuove pagine.
title: Come si creano le offerte di reindirizzamento?
feature: Experiences and Offers
exl-id: b7b960cb-5057-455b-8fab-86dd37343a04
source-git-commit: e8201198dc6ac36e803153d5c6b345a30716204a
workflow-type: tm+mt
source-wordcount: '1016'
ht-degree: 25%

---

# Creare offerte di reindirizzamento

Scopri come creare offerte di reindirizzamento per indirizzare facilmente i browser alle nuove pagine.

Supponi di dover sottoporre a test due pagine completamente diverse, anziché semplici contenuti all&#39;interno di una pagina. In questo caso, il test A/B confronta la pagina A con la pagina B. Configura un&#39;attività [!UICONTROL A/B Test] con due esperienze: una che punta alla pagina predefinita A e l&#39;altra con reindirizza alla pagina B. L’offerta è configurata per reindirizzare il visitatore a una pagina diversa.

>[!NOTE]
>
> * Le offerte di reindirizzamento possono essere create nella pagina [!UICONTROL Offers] > [!UICONTROL Code Offers] o nel [Compositore esperienza basato su Forms](/help/main/c-experiences/form-experience-composer.md). Non è possibile creare o applicare offerte di reindirizzamento nel Compositore esperienza visivo [!UICONTROL Visual Experience Composer]. Il contenuto viene inserito nei percorsi di richiesta [!DNL Target], pertanto è molto probabile che questi percorsi non siano appropriati per una richiesta globale di [!DNL Target].
>
>* Impossibile utilizzare le offerte di reindirizzamento nelle mbox AJAX (`mboxUpdate`).
>
>* Per le offerte di reindirizzamento nelle attività che utilizzano [[!UICONTROL Analytics as the reporting source]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T), l&#39;implementazione deve soddisfare determinati requisiti minimi. Inoltre, è necessario conoscere alcune informazioni importanti. Vedi [Offerte di reindirizzamento - Domande frequenti su A4T](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905).
>
>* Per informazioni sulla configurazione di un’esperienza che effettua un redirect, consulta [Reindirizzare a un URL](/help/main/c-experiences/c-visual-experience-composer/redirect-offer.md#task_9578678D42784F5EB9638F8AC8C911FA).

Nell&#39;offerta di reindirizzamento viene eseguito il codice JavaScript per reindirizzare il browser. Tale codice utilizza il metodo `window.location.replace();`, in modo che la pagina a cui il visitatore è reindirizzato non venga memorizzata nella cronologia del browser. Questo processo consente ai visitatori di utilizzare il pulsante Indietro nei loro browser.

>[!NOTE]
>
>Se desideri trasmettere il valore referente della pagina di destinazione, utilizza un’offerta HTML anziché un’offerta di reindirizzamento.

## Crea un&#39;offerta di reindirizzamento dalla pagina [!UICONTROL Code Offers]

1. Fare clic su **[!UICONTROL Offers]**, quindi selezionare la scheda **[!UICONTROL Code Offers]**.
1. Fare clic su **[!UICONTROL Create Offer]** > **[!UICONTROL Redirect Offer]**.
1. Inserisci un nome descrittivo per l’offerta.

   Un nome descrittivo consente a te e agli altri utenti di trovare rapidamente l&#39;offerta nella libreria [!UICONTROL Assets].

1. (Condizionale) Se disponi di un [account Target Premium](/help/main/c-intro/intro.md#premium), seleziona l&#39;[area di lavoro](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md##section_B82EB409B67C4D9D9D20CE30E48DB1DC) desiderata.

1. Specifica l’URL per il contenuto o la destinazione univoca a cui desideri reindirizzare. Questo URL deve essere assoluto.

   >[!NOTE]
   >
   >Le offerte di reindirizzamento si traducono in un ciclo infinito se anche l’URL di reindirizzamento rende l’utente idoneo per la stessa attività. Assicurati che l’utente non sia idoneo per l’attività dopo essere stato reindirizzato.

1. Seleziona le opzioni desiderate per personalizzare l&#39;offerta di reindirizzamento:

   * **[!UICONTROL Include all URL parameters]:** Abilitare questa opzione se si desidera che tutti i parametri URL presenti nella pagina precedente vengano propagati alla pagina reindirizzata.

     Ad esempio, si desidera reindirizzare le persone direttamente dalla pagina degli uomini a una pagina di categoria camicie maschili. Inoltre, desideri che vengano trasmessi i parametri dinamici nell’URL, perché questo è il metodo con cui puoi monitorare se le persone hanno raggiunto il tuo sito tramite e-mail, banner pubblicitario, annunci di ricerca o in modo organico. Attivando questa opzione, l&#39;offerta di reindirizzamento a pagina `https://www.mycompany.com/mens.html?emailId=123` diventa automaticamente `https://www.mycompany.com/mensShirts.html?emailId=123` quando tutto quello che hai immesso nella casella URL è `https://www.mycompany.com/mensShirts.html`.

   * **[!UICONTROL Pass mbox session ID]:** Obbligatorio per il reindirizzamento a un dominio diverso. Fare scorrere l&#39;interruttore per attivare questa opzione se si desidera includere automaticamente `sessionId` nel reindirizzamento. Questa opzione è necessaria solo quando esegui un test sui clic da un messaggio e-mail o sui clic da un dominio all’altro. L&#39;`sessionId` corrisponde al cookie del visitatore grazie a cui il visitatore continua a essere monitorato e può visualizzare il contenuto corretto.

     Se utilizzi la configurazione dei cookie di prima parte e di terze parti, non è necessario trasmettere l’ID sessione mbox quando si attraversano i domini. È ripetuto nel cookie di terze parti, quindi non è necessario nell&#39;URL.

1. Fare clic su **[!UICONTROL Create]**.

>[!IMPORTANT]
>
>Chiedi al tuo consulente di implementazione prima di lanciare questi test.

## Creare un&#39;offerta di reindirizzamento utilizzando [!UICONTROL Form-Based Experience Composer]

1. Durante la creazione di un&#39;attività tramite [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md), selezionare il percorso in cui visualizzare la sezione **[!UICONTROL Content]**.
1. Fai clic sull&#39;elenco a discesa **[!UICONTROL Content]**, fai clic sull&#39;icona **[!UICONTROL List]** ( ![Elenco](/help/main/assets/icons/MoreSmallList.svg) ), quindi fai clic su **[!UICONTROL Change Redirect Offer]**.
1. Fare clic su **[!UICONTROL Create Offer]** > **[!UICONTROL Redirect Offer]**.
1. Inserisci un nome descrittivo per l’offerta.

   Un nome descrittivo consente a te e agli altri utenti di trovare rapidamente l&#39;offerta nella libreria [!UICONTROL Assets].

1. Specifica l’URL per il contenuto o la destinazione univoca a cui desideri reindirizzare. Questo URL deve essere assoluto.

   >[!NOTE]
   >
   >Le offerte di reindirizzamento si traducono in un ciclo infinito se anche l’URL di reindirizzamento rende l’utente idoneo per la stessa attività. Assicurati che l’utente non sia idoneo per l’attività dopo essere stato reindirizzato.

1. Seleziona le opzioni desiderate per personalizzare l&#39;offerta di reindirizzamento:

   * **[!UICONTROL Include all URL parameters]:** Sposta l&#39;interruttore per attivare questa opzione se vuoi che tutti i parametri URL presenti nella pagina precedente vengano propagati alla pagina reindirizzata.

     Ad esempio, si desidera reindirizzare le persone direttamente dalla pagina degli uomini a una pagina di categoria camicie maschili. Inoltre, desideri che vengano trasmessi i parametri dinamici nell’URL, perché questo è il metodo con cui puoi monitorare se le persone hanno raggiunto il tuo sito tramite e-mail, banner pubblicitario, annunci di ricerca o in modo organico. Attivando questa opzione, l&#39;offerta di reindirizzamento a pagina `https://www.mycompany.com/mens.html?emailId=123` diventa automaticamente `https://www.mycompany.com/mensShirts.html?emailId=123` quando tutto quello che hai immesso nella casella URL è `https://www.mycompany.com/mensShirts.html`.

   * **[!UICONTROL Pass mbox session ID]:** Obbligatorio per il reindirizzamento a un dominio diverso. Fare scorrere l&#39;interruttore per attivare questa opzione se si desidera includere automaticamente `sessionId` nel reindirizzamento. Questa opzione è necessaria solo quando esegui un test sui clic da un messaggio e-mail o sui clic da un dominio all’altro. L&#39;`sessionId` corrisponde al cookie del visitatore grazie a cui il visitatore continua a essere monitorato e può visualizzare il contenuto corretto.

     Se utilizzi la configurazione dei cookie di prima parte e di terze parti, non è necessario trasmettere l’ID sessione mbox quando si attraversano i domini. È ripetuto nel cookie di terze parti, quindi non è necessario nell&#39;URL.

1. Fare clic su **[!UICONTROL Create]**.

>[!IMPORTANT]
>
>Chiedi al tuo consulente di implementazione prima di lanciare questi test.

## Utilizzare le offerte di reindirizzamento nelle attività

Applica le offerte di reindirizzamento utilizzando [[!UICONTROL Form-Based Experience Composer]](/help/main/c-experiences/form-experience-composer.md). Al momento non è possibile applicare offerte di reindirizzamento utilizzando [!UICONTROL Visual Experience Composer] (VEC).

[!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] è un&#39;interfaccia non visiva per la creazione di esperienze e offerte, utile per creare le esperienze da utilizzare nelle attività [!UICONTROL A/B Tests], [!UICONTROL Experience Targeting] (XT), [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Recommendations] quando [!UICONTROL Visual Experience Composer] non è disponibile o se non risulta pratico. È ad esempio possibile utilizzare [!UICONTROL Form-Based Experience Composer] per creare esperienze che utilizzano offerte di reindirizzamento.

1. Crea o modifica un&#39;attività in [!UICONTROL Form-Based Experience Composer].

   Per istruzioni dettagliate, consulta [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md).

1. Specifica la posizione desiderata e aggiungi eventuali perfezionamenti del pubblico secondo necessità.

1. Fai clic sull&#39;elenco a discesa **[!UICONTROL Content]**, fai clic sull&#39;icona **[!UICONTROL List]** ( ![Elenco](/help/main/assets/icons/MoreSmallList.svg) ), quindi fai clic su **[!UICONTROL Change Redirect Offer]**.
1. Selezionare l&#39;offerta di reindirizzamento desiderata dalla finestra di dialogo [!UICONTROL Select Redirect Offer], quindi fare clic su **[!UICONTROL Add]**.
1. Termina la configurazione dell’attività.
