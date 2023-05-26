---
keywords: reindirizzare offerta;crea offerta di reindirizzamento;aggiungere offerta HTML;trasmettere tutti i parametri URL nel reindirizzamento;trasmettere mboxSessionId nel reindirizzamento (necessario solo quando si reindirizza a un dominio diverso)
description: Scopri come creare le offerte di reindirizzamento in Adobe [!DNL Target] affinché un browser venga reindirizzato a una nuova pagina.
title: Come si creano le offerte di reindirizzamento?
feature: Experiences and Offers
exl-id: b7b960cb-5057-455b-8fab-86dd37343a04
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '1189'
ht-degree: 48%

---

# Creare offerte di reindirizzamento

Offerte di reindirizzamento in [!DNL Adobe Target] fare in modo che un browser reindirizzi a una nuova pagina.

Supponi di dover sottoporre a test due pagine completamente diverse, anziché semplici contenuti all&#39;interno di una pagina. In questo caso, il test A/B confronta la pagina A con la pagina B. Configura un’attività Test A/B con due esperienze: una che punta alla pagina predefinita A e l’altra con reindirizza alla pagina B. L’offerta è configurata per reindirizzare il visitatore a una pagina diversa.

>[!NOTE]
>
> * Le offerte di reindirizzamento possono essere create su [!UICONTROL Offerte] > [!UICONTROL Offerte di codice] pagina o in [Compositore esperienza basato su Forms](/help/main/c-experiences/form-experience-composer.md). Non è possibile creare o applicare offerte di reindirizzamento nel Compositore esperienza visivo. Il contenuto verrà iniettato nel [!DNL Target] richiedono posizioni, quindi molto probabilmente non sono appropriate per un [!DNL Target] richiesta.
>
>* Non è possibile utilizzare le offerte di reindirizzamento in elementi mbox ajax (`mboxUpdate`).
>
>* Per le offerte di reindirizzamento nelle attività che utilizzano A4T, l&#39;implementazione deve soddisfare determinati requisiti minimi. Inoltre, è necessario conoscere alcune informazioni importanti. Per ulteriori informazioni, consulta [Offerte di reindirizzamento: domande frequenti su A4T](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905).
>
>* Per informazioni sulla configurazione di un’esperienza che effettua un redirect, consulta [Reindirizzare a un URL](/help/main/c-experiences/c-visual-experience-composer/redirect-offer.md#task_9578678D42784F5EB9638F8AC8C911FA).


Nell&#39;offerta di reindirizzamento viene eseguito il codice JavaScript per reindirizzare il browser. Tale codice utilizza il metodo `window.location.replace();`, in modo che la pagina a cui il visitatore è reindirizzato non venga memorizzata nella cronologia del browser. Questo consente al visitatore di utilizzare il pulsante “Indietro” nel browser.

>[!NOTE]
>
>Per trasmettere il valore referente della pagina di destinazione, è consigliabile utilizzare un’offerta HTML anziché un’offerta di reindirizzamento.

## Creare un’offerta di reindirizzamento dalla pagina Offerte di codice

1. Fai clic su **[!UICONTROL Offerte]**, quindi seleziona la scheda **[!UICONTROL Offerte di codice]**.

   ![Scheda Offerte di codice](/help/main/c-experiences/c-manage-content/assets/offers-code-offers.png)

1. Fai clic su **[!UICONTROL Crea]** > **[!UICONTROL Offerta di reindirizzamento]**.

   ![Finestra di dialogo Crea offerta di reindirizzamento](/help/main/c-experiences/c-manage-content/assets/create-redirect-offer.png)

1. Inserisci un nome descrittivo per l’offerta.

   Un nome descrittivo è utile per ritrovare rapidamente l’offerta nella libreria Risorse.

1. Inserisci l&#39;URL per il contenuto o la destinazione univoca a cui si desidera reindirizzare. Deve essere un URL assoluto.

   >[!NOTE]
   >
   >Le offerte di reindirizzamento si traducono in un ciclo infinito se anche l’URL di reindirizzamento rende l’utente idoneo per la stessa attività. È necessario assicurarsi che l&#39;utente non sia reso idoneo per l&#39;attività dopo essere stato reindirizzato.

1. Seleziona le opzioni desiderate per personalizzare l&#39;offerta di reindirizzamento:

   * **Includi tutti i parametri URL:** Fai scorrere l’interruttore per abilitare questa opzione se desideri che tutti i parametri URL presenti nella pagina precedente vengano propagati alla pagina reindirizzata.

      Ad esempio, si desidera reindirizzare le persone direttamente dalla pagina degli uomini a una pagina di categoria camicie maschili. Si desidera inoltre trasmettere i parametri dinamici nell&#39;URL poiché necessari per monitorare la modalità in cui le persone hanno raggiunto il sito: via e-mail, banner pubblicitario, annuncio di ricerca o naturalmente. Attivando questa opzione, la tua offerta di reindirizzamento alla pagina `https://www.mycompany.com/mens.html?emailId=123` diventerà automaticamente `https://www.mycompany.com/mensShirts.html?emailId=123` quando tutto ciò che hai immesso nella casella URL era `https://www.mycompany.com/mensShirts.html`.

   * **Passa ID sessione mbox:** Obbligatorio per il reindirizzamento a un dominio diverso. Sposta l’interruttore per abilitare questa opzione se desideri `sessionId` da includere automaticamente nel reindirizzamento. Questa opzione è necessaria solo quando si esegue un test sui clic da un messaggio e-mail o sui clic da un dominio all’altro. L&#39;`sessionId` corrisponde al cookie del visitatore grazie a cui il visitatore continua a essere monitorato e può visualizzare il contenuto corretto.

      Se utilizzi la configurazione dei cookie di prima parte e di terze parti, non è necessario trasmettere l’ID sessione mbox quando si attraversano i domini. È ripetuto nel cookie di terze parti, quindi non è necessario nell&#39;URL.

1. Fai clic su **[!UICONTROL Salva]**.

>[!NOTE]
>
>Chiedi al tuo consulente di implementazione prima di lanciare questi test.

## Creare un’offerta di reindirizzamento utilizzando il Compositore esperienza basato su moduli

1. Durante la creazione di un’attività tramite [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md), selezionare la posizione in cui visualizzare **[!UICONTROL Contenuto]** sezione.

   ![Sezione Contenuto nel Compositore esperienza basato su moduli](/help/main/c-experiences/c-manage-content/assets/form-based-content.png)

1. Fai clic su **[!UICONTROL Contenuto predefinito]** , quindi fai clic su **[!UICONTROL Cambia offerta di reindirizzamento]**.

   ![Modifica offerta di reindirizzamento, opzione](/help/main/c-experiences/c-manage-content/assets/change-redirect-offer-option.png)

1. Fai clic su **[!UICONTROL Crea]** > **[!UICONTROL Offerta di reindirizzamento]**.

   ![Finestra di dialogo Crea offerta di reindirizzamento](/help/main/c-experiences/c-manage-content/assets/create-redirect-offer.png)

1. Inserisci un nome descrittivo per l’offerta.

   Un nome descrittivo è utile per ritrovare rapidamente l’offerta nella libreria Risorse.

1. Inserisci l&#39;URL per il contenuto o la destinazione univoca a cui si desidera reindirizzare. Deve essere un URL assoluto.

   >[!NOTE]
   >
   >Le offerte di reindirizzamento si traducono in un ciclo infinito se anche l’URL di reindirizzamento rende l’utente idoneo per la stessa attività. È necessario assicurarsi che l&#39;utente non sia reso idoneo per l&#39;attività dopo essere stato reindirizzato.

1. Seleziona le opzioni desiderate per personalizzare l&#39;offerta di reindirizzamento:

   * **Includi tutti i parametri URL:** Fai scorrere l’interruttore per abilitare questa opzione se desideri che tutti i parametri URL presenti nella pagina precedente vengano propagati alla pagina reindirizzata.

      Ad esempio, si desidera reindirizzare le persone direttamente dalla pagina degli uomini a una pagina di categoria camicie maschili. Si desidera inoltre trasmettere i parametri dinamici nell&#39;URL poiché necessari per monitorare la modalità in cui le persone hanno raggiunto il sito: via e-mail, banner pubblicitario, annuncio di ricerca o naturalmente. Attivando questa opzione, la tua offerta di reindirizzamento alla pagina `https://www.mycompany.com/mens.html?emailId=123` diventerà automaticamente `https://www.mycompany.com/mensShirts.html?emailId=123` quando tutto ciò che hai immesso nella casella URL era `https://www.mycompany.com/mensShirts.html`.

   * **Passa ID sessione mbox:** Obbligatorio per il reindirizzamento a un dominio diverso. Sposta l’interruttore per abilitare questa opzione se desideri `sessionId` da includere automaticamente nel reindirizzamento. Questa opzione è necessaria solo quando si esegue un test sui clic da un messaggio e-mail o sui clic da un dominio all’altro. L&#39;`sessionId` corrisponde al cookie del visitatore grazie a cui il visitatore continua a essere monitorato e può visualizzare il contenuto corretto.

      Se utilizzi la configurazione dei cookie di prima parte e di terze parti, non è necessario trasmettere l’ID sessione mbox quando si attraversano i domini. È ripetuto nel cookie di terze parti, quindi non è necessario nell&#39;URL.

1. Fai clic su **[!UICONTROL Salva]**.

>[!NOTE]
>
>Chiedi al tuo consulente di implementazione prima di lanciare questi test.

## Utilizzare le offerte di reindirizzamento nelle attività

È necessario applicare le offerte di reindirizzamento utilizzando [!UICONTROL Compositore esperienza basato su moduli]. Al momento non è possibile applicare offerte di reindirizzamento utilizzando il Compositore esperienza visivo.

Il [!DNL Adobe Target] [!UICONTROL Compositore esperienza basato su moduli] è un’interfaccia non visiva per la creazione di esperienze, utile per creare le esperienze da utilizzare in [!UICONTROL Test A/B], [!UICONTROL Targeting esperienza] XT [!UICONTROL Automated Personalization] (AP), e [!UICONTROL Recommendations] attività quando il compositore esperienza visivo non è disponibile o se non risulta pratico. Ad esempio, puoi utilizzare il [!UICONTROL Compositore esperienza basato su moduli] per creare esperienze che utilizzano le offerte di reindirizzamento.

1. Creare o modificare un’attività in [!UICONTROL Compositore esperienza basato su moduli].

   Consulta [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md) per istruzioni dettagliate.

1. Specifica la posizione desiderata e aggiungi eventuali perfezionamenti del pubblico secondo necessità.

1. Fai clic sull’elenco a discesa nella sezione **[!UICONTROL Contenuto]** , quindi fai clic su **[!UICONTROL Cambia offerta di reindirizzamento]**.

   ![Modifica offerta di reindirizzamento, opzione](/help/main/c-experiences/c-manage-content/assets/change-redirect-offer-option2.png)

1. Seleziona l’offerta di reindirizzamento desiderata da [!UICONTROL Seleziona offerta remota] , quindi fare clic su **[!UICONTROL Fine]**.

1. Termina la configurazione dell’attività.

## Video di formazione: Compositore basato su moduli ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video offre una demo del compositore basato su moduli, che puoi utilizzare per creare offerte di reindirizzamento.

* Creare un’attività utilizzando il Compositore esperienza basato su moduli
* Quando utilizzare il Compositore esperienza basato su moduli o il Compositore esperienza visivo
* Indirizzare una posizione con i perfezionamenti

>[!VIDEO](https://video.tv.adobe.com/v/17390)
