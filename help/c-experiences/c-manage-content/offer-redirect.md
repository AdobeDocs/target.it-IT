---
keywords: reindirizzare offerta;crea offerta di reindirizzamento;aggiungere offerta HTML;trasmettere tutti i parametri URL nel reindirizzamento;trasmettere mboxSessionId nel reindirizzamento (necessario solo quando si reindirizza a un dominio diverso)
description: 'Scopri come creare offerte di reindirizzamento in Adobe [!DNL Target] per reindirizzare un browser a una nuova pagina. '
title: Come Posso Creare Offerte Di Reindirizzamento?
feature: Esperienze e offerte
exl-id: b7b960cb-5057-455b-8fab-86dd37343a04
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '1192'
ht-degree: 48%

---

# Creare offerte di reindirizzamento

Le offerte di reindirizzamento in [!DNL Adobe Target] causano il reindirizzamento di un browser a una nuova pagina.

Supponi di dover sottoporre a test due pagine completamente diverse, anziché semplici contenuti all&#39;interno di una pagina. In questo caso, il test A/B confronta la pagina A e la pagina B. Imposta attività di test A/B con due esperienze: una che indica la pagina predefinita A e l’altra reindirizzerà alla pagina B. L’offerta è configurata per reindirizzare il visitatore a una pagina diversa.

>[!NOTE]
>
> * Le offerte di reindirizzamento possono essere create sulla pagina [!UICONTROL Offerte] > [!UICONTROL Offerte di codice] o nel [Compositore esperienza basato su Forms](/help/c-experiences/form-experience-composer.md). Non puoi creare o applicare offerte di reindirizzamento nel Compositore esperienza visivo. Il contenuto verrà inserito nelle posizioni di richiesta [!DNL Target], pertanto è molto probabile che queste non siano appropriate per una richiesta globale [!DNL Target].
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

## Creare un’offerta di reindirizzamento dalla pagina Offerte di codice

1. Fai clic su **[!UICONTROL Offerte]**, quindi seleziona la scheda **[!UICONTROL Offerte di codice]**.

   ![Scheda Offerte codice](/help/c-experiences/c-manage-content/assets/offers-code-offers.png)

1. Fai clic su **[!UICONTROL Crea]** > **[!UICONTROL Offerta di reindirizzamento]**.

   ![Finestra di dialogo Crea offerta di reindirizzamento](/help/c-experiences/c-manage-content/assets/create-redirect-offer.png)

1. Inserisci un nome descrittivo per l’offerta.

   Un nome descrittivo è utile per ritrovare rapidamente l’offerta nella libreria Risorse.

1. Inserisci l&#39;URL per il contenuto o la destinazione univoca a cui si desidera reindirizzare. Deve essere un URL assoluto.

   >[!NOTE]
   >
   >Le offerte di reindirizzamento si traducono in un ciclo infinito se anche l’URL di reindirizzamento rende l’utente idoneo per la stessa attività. È necessario assicurarsi che l&#39;utente non sia reso idoneo per l&#39;attività dopo essere stato reindirizzato.

1. Seleziona le opzioni desiderate per personalizzare l&#39;offerta di reindirizzamento:

   * **Includi tutti i parametri URL:** fai scorrere l’interruttore per abilitare questa opzione se desideri che tutti i parametri URL presenti nella pagina precedente vengano propagati alla pagina reindirizzata.

      Ad esempio, si desidera reindirizzare le persone direttamente dalla pagina degli uomini a una pagina di categoria camicie maschili. Si desidera inoltre trasmettere i parametri dinamici nell&#39;URL poiché necessari per monitorare la modalità in cui le persone hanno raggiunto il sito: via e-mail, banner pubblicitario, annuncio di ricerca o naturalmente. Attivando questa opzione, l’offerta di reindirizzamento a pagina `https://www.mycompany.com/mens.html?emailId=123` diventerà automaticamente `https://www.mycompany.com/mensShirts.html?emailId=123` quando tutto ciò che hai inserito nella casella URL è `https://www.mycompany.com/mensShirts.html`.

   * **Passa l&#39;ID di sessione mbox:** obbligatorio per reindirizzare a un dominio diverso. Fai scorrere l&#39;interruttore per abilitare questa opzione se desideri che il `sessionId` sia incluso automaticamente nel reindirizzamento. Questa opzione è necessaria solo quando si esegue un test sui clic da un’e-mail o sui clic da un dominio a un altro. L&#39;`sessionId` corrisponde al cookie del visitatore grazie a cui il visitatore continua a essere monitorato e può visualizzare il contenuto corretto.

      Se utilizzi la configurazione dei cookie di prima e terza parte, non devi trasmettere l’ID di sessione mbox quando incroci i domini. È ripetuto nel cookie di terze parti, quindi non è necessario nell&#39;URL.

1. Fai clic su **[!UICONTROL Salva]**.

>[!NOTE]
>
>Chiedi al tuo consulente di implementazione prima di lanciare questi test.

## Creare un’offerta di reindirizzamento utilizzando il Compositore esperienza basato su moduli

1. Durante la creazione di un&#39;attività utilizzando il [Compositore esperienza basato su moduli](/help/c-experiences/form-experience-composer.md), seleziona la posizione in cui visualizzare la sezione **[!UICONTROL Contenuto]**.

   ![Sezione Contenuto nel Compositore esperienza basato su moduli](/help/c-experiences/c-manage-content/assets/form-based-content.png)

1. Fai clic sull&#39;elenco a discesa **[!UICONTROL Contenuto predefinito]** , quindi fai clic su **[!UICONTROL Cambia offerta di reindirizzamento]**.

   ![Opzione Cambia offerta di reindirizzamento](/help/c-experiences/c-manage-content/assets/change-redirect-offer-option.png)

1. Fai clic su **[!UICONTROL Crea]** > **[!UICONTROL Offerta di reindirizzamento]**.

   ![Finestra di dialogo Crea offerta di reindirizzamento](/help/c-experiences/c-manage-content/assets/create-redirect-offer.png)

1. Inserisci un nome descrittivo per l’offerta.

   Un nome descrittivo è utile per ritrovare rapidamente l’offerta nella libreria Risorse.

1. Inserisci l&#39;URL per il contenuto o la destinazione univoca a cui si desidera reindirizzare. Deve essere un URL assoluto.

   >[!NOTE]
   >
   >Le offerte di reindirizzamento si traducono in un ciclo infinito se anche l’URL di reindirizzamento rende l’utente idoneo per la stessa attività. È necessario assicurarsi che l&#39;utente non sia reso idoneo per l&#39;attività dopo essere stato reindirizzato.

1. Seleziona le opzioni desiderate per personalizzare l&#39;offerta di reindirizzamento:

   * **Includi tutti i parametri URL:** fai scorrere l’interruttore per abilitare questa opzione se desideri che tutti i parametri URL presenti nella pagina precedente vengano propagati alla pagina reindirizzata.

      Ad esempio, si desidera reindirizzare le persone direttamente dalla pagina degli uomini a una pagina di categoria camicie maschili. Si desidera inoltre trasmettere i parametri dinamici nell&#39;URL poiché necessari per monitorare la modalità in cui le persone hanno raggiunto il sito: via e-mail, banner pubblicitario, annuncio di ricerca o naturalmente. Attivando questa opzione, l’offerta di reindirizzamento a pagina `https://www.mycompany.com/mens.html?emailId=123` diventerà automaticamente `https://www.mycompany.com/mensShirts.html?emailId=123` quando tutto ciò che hai inserito nella casella URL è `https://www.mycompany.com/mensShirts.html`.

   * **Passa l&#39;ID di sessione mbox:** obbligatorio per reindirizzare a un dominio diverso. Fai scorrere l&#39;interruttore per abilitare questa opzione se desideri che il `sessionId` sia incluso automaticamente nel reindirizzamento. Questa opzione è necessaria solo quando si esegue un test sui clic da un’e-mail o sui clic da un dominio a un altro. L&#39;`sessionId` corrisponde al cookie del visitatore grazie a cui il visitatore continua a essere monitorato e può visualizzare il contenuto corretto.

      Se utilizzi la configurazione dei cookie di prima e terza parte, non devi trasmettere l’ID di sessione mbox quando incroci i domini. È ripetuto nel cookie di terze parti, quindi non è necessario nell&#39;URL.

1. Fai clic su **[!UICONTROL Salva]**.

>[!NOTE]
>
>Chiedi al tuo consulente di implementazione prima di lanciare questi test.

## Utilizzare le offerte di reindirizzamento nelle attività

È necessario applicare le offerte di reindirizzamento utilizzando il [!UICONTROL Compositore esperienza basato su moduli]. Al momento non è possibile applicare le offerte di reindirizzamento utilizzando il Compositore esperienza visivo.

Il [!DNL Adobe Target] [!UICONTROL Compositore esperienza basato su moduli] è un&#39;interfaccia per la creazione di esperienze non visive ed offerte, utile per creare esperienze da utilizzare in [!UICONTROL Test A/B], [!UICONTROL Targeting esperienza] (XT), [!UICONTROL Automated Personalization] (AP) e [!UICONTROL Recommendations attività a10/> quando il compositore esperienza visivo non è disponibile o se non è pratico per l’uso. ] Ad esempio, puoi utilizzare il [!UICONTROL Compositore esperienza basato su moduli] per creare esperienze che utilizzano offerte di reindirizzamento.

1. Crea o modifica un&#39;attività nel [!UICONTROL Compositore esperienza basato su moduli].

   Per istruzioni dettagliate, consulta [Compositore esperienza basato su moduli](/help/c-experiences/form-experience-composer.md) .

1. Specifica la posizione desiderata e aggiungi eventuali perfezionamenti al pubblico, a seconda delle necessità.

1. Fai clic sull&#39;elenco a discesa nella sezione **[!UICONTROL Contenuto]** , quindi fai clic su **[!UICONTROL Cambia offerta di reindirizzamento]**.

   ![Opzione Cambia offerta di reindirizzamento](/help/c-experiences/c-manage-content/assets/change-redirect-offer-option2.png)

1. Seleziona l&#39;offerta di reindirizzamento desiderata dalla finestra di dialogo [!UICONTROL Seleziona offerta remota], quindi fai clic su **[!UICONTROL Fine]**.

1. Termina la configurazione dell’attività.

## Video di formazione: Compositore basato su moduli ![Badge tutorial](/help/assets/tutorial.png)

Questo video fornisce una demo del compositore basato su moduli, che può essere utilizzato per creare offerte di reindirizzamento.

* Creare un’attività utilizzando il Compositore esperienza basato su moduli
* Quando utilizzare il Compositore esperienza basato su moduli o il Compositore esperienza visivo
* Indirizzare una posizione con i perfezionamenti

>[!VIDEO](https://video.tv.adobe.com/v/17390)
