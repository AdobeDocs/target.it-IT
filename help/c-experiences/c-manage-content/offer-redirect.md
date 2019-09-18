---
description: Con un’offerta di reindirizzamento, il browser viene reindirizzato a una nuova pagina.
keywords: reindirizzare offerta;crea offerta di reindirizzamento;aggiungere offerta HTML;trasmettere tutti i parametri URL nel reindirizzamento;trasmettere mboxSessionId nel reindirizzamento (necessario solo quando si reindirizza a un dominio diverso)
seo-description: Informazioni sulle offerte di reindirizzamento in Adobe Target che determinano il reindirizzamento di un browser a una nuova pagina.
seo-title: Creare offerte di reindirizzamento
solution: Target
title: Creare offerte di reindirizzamento
topic: Standard
uuid: 54336965-a26e-47c3-b3bc-079d3573502a
translation-type: tm+mt
source-git-commit: 8dc94ca1ed48366e6b3ac7a75b03c214f1db71d9

---


# Creare offerte di reindirizzamento{#create-redirect-offers}

Con un’offerta di reindirizzamento, il browser viene reindirizzato a una nuova pagina.

Supponi di dover sottoporre a test due pagine completamente diverse, anziché semplici contenuti all'interno di una pagina. In questo caso, nel test A/B vengono messe a confronto la pagina A e la pagina B. Configura una campagna di test A/B con due esperienze: una dirige alla pagina predefinita A e l'altra reindirizza alla pagina B. L'offerta viene configurata per reindirizzare il visitatore a una pagina diversa.

>[!NOTE] {class=“- topic/note ”}
>
>Non è possibile utilizzare le offerte di reindirizzamento in elementi mbox ajax (`mboxUpdate`).
>
>Per le offerte di reindirizzamento nelle attività che utilizzano A4T, l'implementazione deve soddisfare determinati requisiti minimi. Inoltre, è necessario conoscere alcune informazioni importanti. Per ulteriori informazioni, consulta [Offerte di reindirizzamento - Domande frequenti su A4T](../../c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905).

Per informazioni sulla configurazione di un’esperienza che effettua un redirect, consulta [Reindirizzare a un URL](../../c-experiences/c-visual-experience-composer/redirect-offer.md#task_9578678D42784F5EB9638F8AC8C911FA).

Nell'offerta di reindirizzamento viene eseguito il codice JavaScript per reindirizzare il browser. Tale codice utilizza il metodo `window.location.replace();`, in modo che la pagina a cui il visitatore è reindirizzato non venga memorizzata nella cronologia del browser. Questo consente al visitatore di utilizzare il pulsante “Indietro” nel browser.

>[!NOTE] {class=“- topic/note ”}
>
>Per trasmettere il valore referente della pagina di destinazione, è consigliabile utilizzare un’offerta HTML anziché un’offerta di reindirizzamento.

**Per creare un'offerta di reindirizzamento:**

1. Fai clic su **[!UICONTROL Offerte]**, quindi seleziona la scheda **[!UICONTROL Offerte di codice]**.
1. Fai clic su **[!UICONTROL Crea]** &gt; **[!UICONTROL Offerta di reindirizzamento]**.
1. Digita un nome per l’offerta.
1. Inserisci l'URL per il contenuto o la destinazione univoca a cui si desidera reindirizzare. Deve essere un URL assoluto.

   >[!NOTE]
   >
   >Le offerte di reindirizzamento si traducono in un ciclo infinito se anche l’URL di reindirizzamento rende l’utente idoneo per la stessa attività. È necessario assicurarsi che l'utente non sia reso idoneo per l'attività dopo essere stato reindirizzato.

1. Seleziona le opzioni desiderate per personalizzare l'offerta di reindirizzamento:

* **Includi tutti i parametri URL:** seleziona questa casella se desideri che tutti i parametri URL presenti nella pagina precedente vengano propagati alla pagina reindirizzata.

   Ad esempio, si desidera reindirizzare le persone direttamente dalla pagina degli uomini a una pagina di categoria camicie maschili. Si desidera inoltre trasmettere i parametri dinamici nell'URL poiché necessari per monitorare la modalità in cui le persone hanno raggiunto il sito: via e-mail, banner pubblicitario, annuncio di ricerca o naturalmente. Selezionando questa casella, la tua offerta di reindirizzamento alla pagina [!DNL `https://www.mycompany.com/mens.html?emailId=123`] diventerà automaticamente [!DNL `https://www.mycompany.com/mensShirts.html?emailId=123`] anche se hai inserito nella casella URL solamente [!DNL `https://www.mycompany.com/mensShirts.html`].

* **Trasmetti ID sessione mbox ID (necessario per reindirizzare a un dominio diverso):** seleziona questa casella se desideri che il `sessionId` venga automaticamente incluso nel reindirizzamento. Tale opzione è necessaria solo quando si esegue un test sui clic da un messaggio di posta elettronica o sui quelli da un dominio a un altro. L'`sessionId` corrisponde al cookie del visitatore grazie a cui il visitatore continua a essere monitorato e può visualizzare il contenuto corretto.

   Se si utilizza l'impostazione cookie proprietario e di terze parti, non è necessario trasmetter l'ID sessione mbox quando si attraversano i domini. È ripetuto nel cookie di terze parti, quindi non è necessario nell'URL.

>[!NOTE] {class=“- topic/note ”}
>
>Chiedi al tuo consulente di implementazione prima di lanciare questi test.

## Video di formazione: L’archivio dei contenuti (4:56)

Questo video include informazioni sulla gestione del contenuto.

* Connessione tra la [libreria delle risorse di Experience Cloud](https://docs.adobe.com/content/help/en/core-services/interface/assets/creative-cloud.html) e la libreria dei contenuti di Target
* Offerte HTML personalizzate
* Offerta HTML personalizzata nel Compositore esperienza visivo

>[!VIDEO](https://video.tv.adobe.com/v/17387?captions=ita)
