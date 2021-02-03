---
keywords: reindirizzare offerta;crea offerta di reindirizzamento;aggiungere offerta HTML;trasmettere tutti i parametri URL nel reindirizzamento;trasmettere mboxSessionId nel reindirizzamento (necessario solo quando si reindirizza a un dominio diverso)
description: Posso utilizzare le offerte di reindirizzamento per reindirizzare un browser a una nuova pagina?
title: Creazione di offerte di reindirizzamento
feature: Experiences and Offers
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '1183'
ht-degree: 49%

---


# Creare offerte di reindirizzamento

Le offerte di reindirizzamento in [!DNL Adobe Target] causano il reindirizzamento di un browser a una nuova pagina.

Supponi di dover sottoporre a test due pagine completamente diverse, anziché semplici contenuti all&#39;interno di una pagina. In questo caso, il test A/B confronta le pagine A e B. Configurate attività di test A/B con due esperienze: uno indica la pagina predefinita A e l&#39;altro reindirizzamento alla pagina B. L&#39;offerta è configurata per reindirizzare il visitatore a un&#39;altra pagina.

>[!NOTE]
>
> * Le offerte di reindirizzamento possono essere create sulla pagina [!UICONTROL Offerte] > [!UICONTROL Offerte di codice] o in [Forms-Based Experience Composer](/help/c-experiences/form-experience-composer.md). Non potete creare o applicare offerte di reindirizzamento in Visual Experience Composer (VEC). Il contenuto verrà inserito nelle posizioni di richiesta [!DNL Target], pertanto è molto probabile che non siano adatte a una richiesta globale [!DNL Target].
   >
   >
* Non è possibile utilizzare le offerte di reindirizzamento in elementi mbox ajax (`mboxUpdate`).
   >
   >
* Per le offerte di reindirizzamento nelle attività che utilizzano A4T, l&#39;implementazione deve soddisfare determinati requisiti minimi. Inoltre, è necessario conoscere alcune informazioni importanti. Per ulteriori informazioni, consulta [Offerte di reindirizzamento - Domande frequenti su A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905).
   >
   >
* Per informazioni sulla configurazione di un’esperienza che effettua un redirect, consulta [Reindirizzare a un URL](/help/c-experiences/c-visual-experience-composer/redirect-offer.md#task_9578678D42784F5EB9638F8AC8C911FA).


Nell&#39;offerta di reindirizzamento viene eseguito il codice JavaScript per reindirizzare il browser. Tale codice utilizza il metodo `window.location.replace();`, in modo che la pagina a cui il visitatore è reindirizzato non venga memorizzata nella cronologia del browser. Questo consente al visitatore di utilizzare il pulsante “Indietro” nel browser.

>[!NOTE]
>
>Per trasmettere il valore referente della pagina di destinazione, è consigliabile utilizzare un’offerta HTML anziché un’offerta di reindirizzamento.

## Creare un&#39;offerta di reindirizzamento dalla pagina Offerte codice

1. Fai clic su **[!UICONTROL Offerte]**, quindi seleziona la scheda **[!UICONTROL Offerte di codice]**.

   ![Code Offers, scheda](/help/c-experiences/c-manage-content/assets/offers-code-offers.png)

1. Fai clic su **[!UICONTROL Crea]** > **[!UICONTROL Offerta di reindirizzamento]**.

   ![Crea offerta di reindirizzamento, finestra di dialogo](/help/c-experiences/c-manage-content/assets/create-redirect-offer.png)

1. Inserisci un nome descrittivo per l’offerta.

   Un nome descrittivo è utile per ritrovare rapidamente l’offerta nella libreria Risorse.

1. Inserisci l&#39;URL per il contenuto o la destinazione univoca a cui si desidera reindirizzare. Deve essere un URL assoluto.

   >[!NOTE]
   >
   >Le offerte di reindirizzamento si traducono in un ciclo infinito se anche l’URL di reindirizzamento rende l’utente idoneo per la stessa attività. È necessario assicurarsi che l&#39;utente non sia reso idoneo per l&#39;attività dopo essere stato reindirizzato.

1. Seleziona le opzioni desiderate per personalizzare l&#39;offerta di reindirizzamento:

   * **Includi tutti i parametri URL:** fate scorrere l’interruttore per attivare questa opzione se desiderate che tutti i parametri URL presenti nella pagina precedente vengano propagati alla pagina reindirizzata.

      Ad esempio, si desidera reindirizzare le persone direttamente dalla pagina degli uomini a una pagina di categoria camicie maschili. Si desidera inoltre trasmettere i parametri dinamici nell&#39;URL poiché necessari per monitorare la modalità in cui le persone hanno raggiunto il sito: via e-mail, banner pubblicitario, annuncio di ricerca o naturalmente. Attivando questa opzione, l&#39;offerta di reindirizzamento a pagina `https://www.mycompany.com/mens.html?emailId=123` diventerà automaticamente `https://www.mycompany.com/mensShirts.html?emailId=123` quando tutto ciò che avete immesso nella casella URL era `https://www.mycompany.com/mensShirts.html`.

   * **Pass mbox session ID:** obbligatorio per il reindirizzamento a un dominio diverso. Fate scorrere l&#39;interruttore per attivare questa opzione se desiderate che la `sessionId` venga inclusa automaticamente nel reindirizzamento. Questo è richiesto solo quando state eseguendo il test dei clic da un&#39;e-mail o dei clic da un dominio all&#39;altro. L&#39;`sessionId` corrisponde al cookie del visitatore grazie a cui il visitatore continua a essere monitorato e può visualizzare il contenuto corretto.

      Se utilizzate la configurazione dei cookie 1st e 3rd party, non è necessario trasmettere l&#39;ID sessione mbox quando si attraversano i domini. È ripetuto nel cookie di terze parti, quindi non è necessario nell&#39;URL.

1. Fai clic su **[!UICONTROL Salva]**.

>[!NOTE]
>
>Chiedi al tuo consulente di implementazione prima di lanciare questi test.

## Creazione di un&#39;offerta di reindirizzamento tramite Experience Composer basato su modulo

1. Durante la creazione di un&#39;attività con [Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md), selezionate il percorso in cui visualizzare la sezione **[!UICONTROL Content]**.

   ![Sezione Contenuto in Experience Composer basato su modulo](/help/c-experiences/c-manage-content/assets/form-based-content.png)

1. Fare clic sull&#39;elenco a discesa **[!UICONTROL Contenuto predefinito]**, quindi fare clic su **[!UICONTROL Modifica offerta di reindirizzamento]**.

   ![Opzione Modifica offerta di reindirizzamento](/help/c-experiences/c-manage-content/assets/change-redirect-offer-option.png)

1. Fai clic su **[!UICONTROL Crea]** > **[!UICONTROL Offerta di reindirizzamento]**.

   ![Crea offerta di reindirizzamento, finestra di dialogo](/help/c-experiences/c-manage-content/assets/create-redirect-offer.png)

1. Inserisci un nome descrittivo per l’offerta.

   Un nome descrittivo è utile per ritrovare rapidamente l’offerta nella libreria Risorse.

1. Inserisci l&#39;URL per il contenuto o la destinazione univoca a cui si desidera reindirizzare. Deve essere un URL assoluto.

   >[!NOTE]
   >
   >Le offerte di reindirizzamento si traducono in un ciclo infinito se anche l’URL di reindirizzamento rende l’utente idoneo per la stessa attività. È necessario assicurarsi che l&#39;utente non sia reso idoneo per l&#39;attività dopo essere stato reindirizzato.

1. Seleziona le opzioni desiderate per personalizzare l&#39;offerta di reindirizzamento:

   * **Includi tutti i parametri URL:** fate scorrere l’interruttore per attivare questa opzione se desiderate che tutti i parametri URL presenti nella pagina precedente vengano propagati alla pagina reindirizzata.

      Ad esempio, si desidera reindirizzare le persone direttamente dalla pagina degli uomini a una pagina di categoria camicie maschili. Si desidera inoltre trasmettere i parametri dinamici nell&#39;URL poiché necessari per monitorare la modalità in cui le persone hanno raggiunto il sito: via e-mail, banner pubblicitario, annuncio di ricerca o naturalmente. Attivando questa opzione, l&#39;offerta di reindirizzamento a pagina `https://www.mycompany.com/mens.html?emailId=123` diventerà automaticamente `https://www.mycompany.com/mensShirts.html?emailId=123` quando tutto ciò che avete immesso nella casella URL era `https://www.mycompany.com/mensShirts.html`.

   * **Pass mbox session ID:** obbligatorio per il reindirizzamento a un dominio diverso. Fate scorrere l&#39;interruttore per attivare questa opzione se desiderate che la `sessionId` venga inclusa automaticamente nel reindirizzamento. Questo è richiesto solo quando state eseguendo il test dei clic da un&#39;e-mail o dei clic da un dominio all&#39;altro. L&#39;`sessionId` corrisponde al cookie del visitatore grazie a cui il visitatore continua a essere monitorato e può visualizzare il contenuto corretto.

      Se utilizzate la configurazione dei cookie 1st e 3rd party, non è necessario trasmettere l&#39;ID sessione mbox quando si attraversano i domini. È ripetuto nel cookie di terze parti, quindi non è necessario nell&#39;URL.

1. Fai clic su **[!UICONTROL Salva]**.

>[!NOTE]
>
>Chiedi al tuo consulente di implementazione prima di lanciare questi test.

## Utilizzare le offerte di reindirizzamento nelle attività

È necessario applicare le offerte di reindirizzamento utilizzando [!UICONTROL Form-Based Experience Composer]. Attualmente non è possibile applicare offerte di reindirizzamento utilizzando il VEC.

[!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] è un&#39;interfaccia per la creazione di esperienze non visive e di offerte che è utile per creare esperienze da utilizzare in [!UICONTROL A/B Tests], [!UICONTROL Experience Targeting] (XT), [!UICONTROL  Automated Personalization] (AP) e [!UICONTROL Recommendations&lt;a a10/> attività quando Visual Experience Composer (Compositore esperienza visivo) non è disponibile o pratico per l&#39;uso. ] Ad esempio, potete utilizzare [!UICONTROL Form-Based Experience Composer] per creare esperienze che utilizzano offerte di reindirizzamento.

1. Create o modificate un&#39;attività in [!UICONTROL Form-Based Experience Composer].

   Per istruzioni dettagliate, consultate [Modulo-Based Experience Composer](/help/c-experiences/form-experience-composer.md).

1. Specificate la posizione desiderata e aggiungete eventuali miglioramenti al pubblico, a seconda delle necessità.

1. Fare clic sull&#39;elenco a discesa nella sezione **[!UICONTROL Contenuto]**, quindi fare clic su **[!UICONTROL Modifica offerta di reindirizzamento]**.

   ![Opzione Modifica offerta di reindirizzamento](/help/c-experiences/c-manage-content/assets/change-redirect-offer-option2.png)

1. Selezionate l&#39;offerta di reindirizzamento desiderata dalla finestra di dialogo [!UICONTROL Seleziona offerta remota], quindi fate clic su **[!UICONTROL Fine]**.

1. Termina la configurazione dell’attività.

## Video di formazione: Logo di Composer basato su modulo ![Tutorial](/help/assets/tutorial.png)

Questo video fornisce una dimostrazione di composer basato su modulo, che potete utilizzare per creare offerte di reindirizzamento.

* Creare un’attività utilizzando il Compositore esperienza basato su moduli
* Quando utilizzare il Compositore esperienza basato su moduli o il Compositore esperienza visivo
* Indirizzare una posizione con i perfezionamenti

>[!VIDEO](https://video.tv.adobe.com/v/17390)
